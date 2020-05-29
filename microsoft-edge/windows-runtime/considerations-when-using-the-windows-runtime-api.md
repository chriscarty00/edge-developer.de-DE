---
title: Überlegungen bei der Verwendung der Windows-Runtime-API
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 95b082e27c4f247b841a9540e13bd49bd4c8bd67
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568727"
---
# Überlegungen bei der Verwendung der Windows-Runtime-API  

Sie können nahezu jedes Element der Windows-Runtime-API in JavaScript verwenden.  Es gibt jedoch einige Aspekte der JavaScript-Darstellung von Windows-Runtime-Elementen, die Sie berücksichtigen sollten.  

> [!IMPORTANT]
> Informationen zum Erstellen von Komponenten für Windows-Runtime in c++, c# oder Visual Basic und deren Verwendung in JavaScript finden Sie unter Erstellen von Komponenten für Windows-Runtime [in c++][WindowsUwpComponentsCreatingCpp] und [Erstellen von Komponenten für Windows-Runtime in C# und Visual Basic][WindowsUwpComponentsCreatingCsharpVb].  

## Sonderfälle in der JavaScript-Darstellung von Windows-Runtime-Typen  

*   Zeichenfolgen: eine nicht initialisierte Zeichenfolge wird als Zeichenfolge "undefined" an eine Windows-Runtime-Methode übergeben, und ein Zeichenfolgensatz, `null` der als Zeichenfolge "Null" übergeben wird.  \ (Dies ist wahr, wenn ein `null` oder `undefined` -Wert in eine Zeichenfolge umgewandelt wird. \) bevor Sie eine Zeichenfolge an eine Windows-Runtime-Methode übergeben, sollten Sie Sie als leere Zeichenfolge initialisieren \ ("" \).  
*   Schnittstellen: Sie können in JavaScript keine Windows-Runtime-Schnittstelle implementieren.  
*   Arrays: Windows-Runtime-Arrays sind nicht veränderbar, daher funktionieren Methoden, die die Größe von Arrays in JavaScript ändern, nicht auf Windows-Runtime-Arrays.  
*   Arrays: Wenn Sie einen JavaScript-Array Wert an eine Windows-Runtime-Methode übergeben, wird das Array kopiert.  Die Windows-Runtime-Methode kann das Array oder seine Member nicht ändern und an Ihre JavaScript-App zurückgeben.  Sie können jedoch typisierte Arrays verwenden (beispielsweise Int32Array- [Objekt][MDNInt32array]\), die nicht kopiert werden.  
*   Strukturen: Windows-Runtime-Strukturen sind Objekte in JavaScript.  Wenn Sie eine Windows-Runtime-Struktur an eine Windows-Runtime-Methode übergeben möchten, instanziieren Sie die Struktur nicht mit dem `new` Schlüsselwort.  Erstellen Sie stattdessen ein Objekt, und fügen Sie die relevanten Member und deren Werte hinzu.  Die Namen der Mitglieder sollten im Camel-Fall liegen: `SomeStruct.firstMember` .  
*   Objekte: JavaScript-Objekte sind nicht identisch mit verwalteten Code Objekten \ ( `System.Object` \).  Sie können ein JavaScript-Objekt nicht an eine Windows-Runtime-Methode übergeben, für die ein `System.Object` .  
*   Objektidentität: in den meisten Fällen ändern sich die Objekte, die zwischen der Windows-Runtime und JavaScript hin-und hergeleitet werden, nicht.  Das JavaScript-Modul verwaltet eine Karte mit bekannten Objekten.  Wenn ein Objekt von der Windows-Runtime zurückgegeben wird, wird es mit der Zuordnung abgeglichen, und wenn es nicht vorhanden ist, wird ein neues Objekt erstellt.  Das gleiche Verfahren wird für Objekte befolgt, die Schnittstellen darstellen, die von Windows-Runtime-Methoden zurückgegeben werden.  Es gibt zwei Arten von Ausnahmen:  

    *   Objekte, die von einem Windows-Runtime-Aufruf zurückgegeben werden und dann neue \ (Expando \)-Eigenschaften hinzugefügt wurden, behalten ihre neuen Eigenschaften nicht bei, wenn Sie an die Windows-Runtime zurückgegeben werden.  Wenn Sie jedoch an die JavaScript-App zurückgegeben werden, da Sie dem vorhandenen Objekt zugeordnet sind, verfügt das zurückgegebene Objekt über die Expando-Eigenschaften.  
    *   Strukturen und Stellvertretungen in der Windows-Runtime können nicht als identisch mit zuvor verwendeten Strukturen oder Stellvertretungen identifiziert werden.  Jedes Mal, wenn eine Struktur oder ein Delegat zurückgegeben wird, wird ein neuer Verweis abgerufen.  

*   Namenskollisionen: mehrere Windows-Runtime-Schnittstellen verfügen möglicherweise über Member mit denselben Namen.  Wenn Sie in einem einzelnen JavaScript-Objekt kombiniert werden (Dies kann eine Darstellung einer Runtime-Klasse oder einer Schnittstelle sein), werden die Member durch vollqualifizierte Namen dargestellt.  Sie können diese Member mithilfe der folgenden Syntax aufrufen:  
    
    ```cpp
    Class["MemberName"](parameter)
    ```  
    
    Im folgenden Code verfügen zwei Schnittstellen über eine Draw-Methode, und eine Runtime-Klasse implementiert beide Schnittstellen.  
    
    ```cpp
    namespace CollisionExample {
        interface InterfaceA
        {
            HRESULT Draw([in] Int32 a);
        }
        interface InterfaceB
        {
            HRESULT Draw([in] HString a);
        }
        runtimeclass ExampleObject {
          interface InterfaceA
          interface InterfaceB
        }
    }
    ```  
    
    Hier erfahren Sie, wie Sie den obigen Code in JavaScript aufrufen können.  
    
    ```javascript
    var example = new ExampleObject();
    example["CollisionExample.InterfaceA.draw"](12);
    example["CollisionExample.InterfaceB.draw"]("hello");
    ```  
    
*   `Out` Parameter: Wenn eine Windows-Runtime-Methode über mehrere `out` Parameter verfügt, verfügt die Methode in JavaScript über ein JavaScript-Objekt als Rückgabewert, und das Objekt verfügt über Eigenschaften, die dem `out` Parameter entsprechen.  Nehmen Sie beispielsweise die folgende Windows-Runtime-Signatur in C++ in Frage.  
    
    ```cpp
    void ExampleMethod(
      [OutAttribute] char^ first,
      [OutAttribute] char^ second
    )
    ```  
    
    Die JavaScript-Version dieser Signatur lautet:  
    
    ```javascript
    var returnValue = exampleMethod();
    ```  
    
    In diesem Beispiel `returnValue` ist ein JavaScript-Objekt mit zwei Feldern: `first` und `second` .  
    
*   Statische Member: die Windows-Runtime definiert sowohl statische Member als auch Instanzmember.  In JavaScript werden statische Member dem Objekt hinzugefügt, das der Windows-Runtime-Klasse oder-Schnittstelle zugeordnet ist.  
    
    ```javascript
    // Static method.
    var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
    // Instance method.
    var reading = accel.getCurrentReading();
    ```  
    
Weitere Informationen zur JavaScript-Darstellung von Windows-Runtime Basic-Typen finden Sie unter [JavaScript-Darstellung von Windows-Runtime-Typen][WindowsRuntimeJavascriptTypes].  

<!-- image links -->  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "JavaScript-Darstellung von Windows-Runtime-Typen"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Komponenten für Windows-Runtime mit C++/CX"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Komponenten für Windows-Runtime mit C# und Visual Basic"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  
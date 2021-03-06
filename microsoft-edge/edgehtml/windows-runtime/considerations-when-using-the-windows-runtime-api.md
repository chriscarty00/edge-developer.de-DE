---
description: Überlegungen bei der Verwendung der Windows-Runtime-API
title: Überlegungen bei der Verwendung der Windows-Runtime-API
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 170374fd109802bff0aa0fc93cea6c8d50c9d7c7
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399344"
---
# <a name="considerations-when-using-the-windows-runtime-api"></a>Überlegungen bei der Verwendung der Windows-Runtime-API  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Sie können fast jedes Element der Windows-Runtime-API in JavaScript verwenden.  Es gibt jedoch einige Aspekte der JavaScript-Darstellung von Windows-Runtime-Elementen, die Sie berücksichtigen sollten.  

> [!IMPORTANT]
> Informationen zum Erstellen von Windows-Runtime-Komponenten in C++, C# oder Visual Basic und deren Verwendung in JavaScript finden Sie unter [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] und Creating Windows Runtime Components in C# and [Visual Basic][WindowsUwpComponentsCreatingCsharpVb].  

## <a name="special-cases-in-the-javascript-representation-of-windows-runtime-types"></a>Sonderfälle in der JavaScript-Darstellung von Windows-Runtime-Typen  

:::row:::
   :::column span="1":::
      Zeichenfolgen  
   :::column-end:::
   :::column span="3":::
      Eine nicht initialisierte Zeichenfolge wird an eine Windows-Runtime-Methode als Zeichenfolge "undefined" übergeben, und eine Zeichenfolge, die auf festgelegt ist, wird als Zeichenfolge `null` "null" übergeben.  \(Dies gilt, wenn ein oder ein Wert an eine Zeichenfolge gecced wird.\) Bevor Sie eine Zeichenfolge an eine Windows-Runtime-Methode übergeben, sollten Sie sie als leere Zeichenfolge `null` `undefined` \(""\) initialisieren.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Schnittstellen  
   :::column-end:::
   :::column span="3":::
      Sie können keine Windows-Runtime-Schnittstelle in JavaScript implementieren.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Arrays  
   :::column-end:::
   :::column span="3":::
      Windows-Runtime-Arrays können nicht geändert werden, sodass Methoden, die die Größe von Arrays in JavaScript ändern, nicht auf Windows-Runtime-Arrays funktionieren.  
      *   Arrays: Wenn Sie einen JavaScript-Arraywert an eine Windows-Runtime-Methode übergeben, wird das Array kopiert.  Die Windows-Runtime-Methode kann das Array oder seine Member nicht ändern und an Ihre JavaScript-App zurückgeben.  Sie können jedoch typierte Arrays \(z. B. [Int32Array-Objekt][MDNInt32array]\) verwenden, die nicht kopiert werden.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Strukturen  
   :::column-end:::
   :::column span="3":::
      Windows-Runtime-Strukturen sind Objekte in JavaScript.  Wenn Sie eine Windows-Runtime-Struktur an eine Windows-Runtime-Methode übergeben möchten, instanziieren Sie die Struktur nicht mit dem `new` Schlüsselwort.  Erstellen Sie stattdessen ein Objekt, und fügen Sie die relevanten Elemente und deren Werte hinzu.  Die Namen der Mitglieder sollten in Kamelfall sein: `SomeStruct.firstMember` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Objekte  
   :::column-end:::
   :::column span="3":::
      JavaScript-Objekte sind nicht mit verwalteten Codeobjekten \( `System.Object` \) identisch.  Sie können ein JavaScript-Objekt nicht an eine Windows-Runtime-Methode übergeben, die eine `System.Object` erfordert.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Objektidentität  
   :::column-end:::
   :::column span="3":::
      In den meisten Fällen ändern sich die zwischen der Windows-Runtime und JavaScript übergebenen Objekte nicht.  Das JavaScript-Modul verwaltet eine Karte bekannter Objekte.  Wenn ein Objekt von der Windows-Runtime zurückgegeben wird, wird es mit der Karte abgestimmt, und wenn es nicht vorhanden ist, wird ein neues Objekt erstellt.  Dasselbe Verfahren wird für Objekte befolgt, die Schnittstellen darstellen, die von Windows-Runtime-Methoden zurückgegeben werden.  Es gibt zwei Arten von Ausnahmen:  
      
      *   Objekte, die von einem Windows-Runtime-Aufruf zurückgegeben werden und dann neue \(expando\)-Eigenschaften hinzugefügt haben, behalten ihre neuen Eigenschaften nicht bei, wenn sie an die Windows-Runtime übergeben werden.  Wenn sie jedoch an die JavaScript-App zurückgegeben werden, da sie mit dem vorhandenen Objekt übereinstimmen, verfügt das zurückgegebene Objekt über die expando-Eigenschaften.  
      *   Strukturen und Delegaten in der Windows-Runtime können nicht als identisch mit zuvor verwendeten Strukturen oder Delegaten identifiziert werden.  Jedes Mal, wenn eine Struktur oder ein Delegat zurückgegeben wird, erhält sie einen neuen Verweis.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Namenskollision  
   :::column-end:::
   :::column span="3":::
      Mehrere Windows-Runtime-Schnittstellen können Mitglieder mit denselben Namen haben.  Wenn sie in einem einzelnen JavaScript-Objekt kombiniert werden (dies kann eine Darstellung einer Laufzeitklasse oder einer Schnittstelle sein), werden die Member mit vollqualifizierten Namen dargestellt.  Sie können diese Elemente mithilfe der folgenden Syntax aufrufen:  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      Im folgenden Code verfügen zwei Schnittstellen über eine Draw-Methode, und eine Laufzeitklasse implementiert beide Schnittstellen.  
      
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
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` parameter  
   :::column-end:::
   :::column span="3":::
      Wenn eine Windows-Runtime-Methode über mehrere Parameter verfügt, verfügt die Methode in JavaScript über ein JavaScript-Objekt als Rückgabewert, und das Objekt verfügt über Eigenschaften, die `out` dem Parameter `out` entsprechen.  Berücksichtigen Sie beispielsweise die folgende Windows-Runtime-Signatur in C++.  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      Die JavaScript-Version dieser Signatur ist:  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      In diesem Beispiel `returnValue` ist ein JavaScript-Objekt mit zwei Feldern: `first` und `second` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Statische Elemente  
   :::column-end:::
   :::column span="3":::
      Die Windows-Runtime definiert sowohl statische Member als auch Instanzmitglieder.  In JavaScript werden statische Member dem Objekt hinzugefügt, das der Windows-Runtime-Klasse oder -Schnittstelle zugeordnet ist.  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
Weitere Informationen zur JavaScript-Darstellung von grundlegenden Windows-Runtime-Typen finden Sie unter [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "JavaScript-Darstellung von Windows-Laufzeittypen | Microsoft Docs"  

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Windows-Runtime-Komponenten mit C++/CX-| Microsoft Docs"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Windows-Runtime-Komponenten mit C# und Visual Basic | Microsoft Docs"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  

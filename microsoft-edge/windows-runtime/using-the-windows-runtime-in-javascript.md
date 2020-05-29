---
title: Verwenden der Windows-Runtime in JavaScript
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime
ms.assetid: 90658546-f746-4e34-a7d1-71cf9ee322a2
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bffde93aa973f492189aedcfcaa9c3694d9e61bc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568712"
---
# Verwenden der Windows-Runtime in JavaScript  

Wenn Sie eine universelle Windows-Plattform \ (UWP \)-app schreiben, können Sie Windows-Runtime-Klassen,-Methoden und-Eigenschaften auf die gleiche Weise verwenden wie systemeigene JavaScript-Objekte,-Methoden und-Eigenschaften.  Dieses Thema enthält einführende Informationen und Links zu Themen, in denen die grundlegenden Konzepte der Verwendung von Windows-Runtime-APIs in JavaScript erläutert werden, einschließlich einer Erläuterung, wie Windows-Runtime-Typen dargestellt werden, wie asynchrone Windows-Runtime-Methoden verwendet werden und wie Windows-Runtime-Ereignisse überwacht und behandelt werden.  

Informationen zur allgemeinen Sprachdokumentation finden Sie in der [JavaScript-Referenz][MDNJavascriptReference] Bibliothek von MDN.  

> [!IMPORTANT]
> Windows-Runtime-Features stehen für apps, die in Internet Explorer ausgeführt werden, nicht zur Verfügung.  

## Windows-Runtime-Referenzdokumentation  

Eine Referenzdokumentation finden Sie unter [Windows-Runtime-Referenz][UwpApiIndex].  Code Beispiele stehen in JavaScript und auch in C++, C# und Visual Basic zur Verfügung.  

## Schreiben von Komponenten für Windows-Runtime in C++, C# oder Visual Basic  

Anweisungen und Richtlinien zum Schreiben von Komponenten für Windows-Runtime, die in JavaScript verwendet werden können, finden Sie unter [Erstellen von Komponenten für Windows-Runtime in C++][WindowsUwpWinrtCpp] und [Erstellen von Komponenten für Windows-Runtime in C# und Visual Basic][WindowsUwpWinrtCsharpVb].  

## Konventionen für die Groß-/Kleinschreibung mit Windows-Runtime-Features  

Die Konventionen für die Groß-/Kleinschreibung für Windows-Runtime-Features in JavaScript unterscheiden sich geringfügig von denen für andere Sprachen:  

*   Namespaces und Klassen sind in Pascal-Fall:  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   Mitglieder von Klassen, einschließlich Methoden und Eigenschaften sowie Member von Strukturen und Enumerationen, befinden sich im Camel-Fall:  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   Ereignisnamen sind in Kleinbuchstaben:  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## Weitere Informationen  

[Überlegungen bei der Verwendung der Windows-Runtime-API][WindowsRuntimeConsiderationsApi]  
[Verwenden von asynchronen Windows-Runtime-Methoden][WindowsRuntimeAsynchronousMethods]   
[Behandeln von Windows-Runtime-Ereignissen in JavaScript][WindowsRuntimeEventsJavascript]   
[JavaScript-Darstellung von Windows-Runtime-Typen][WindowsRuntimeJavascriptTypes]   
[JavaScript-Projektion der Windows-Runtime DateTime und TimeSpan][WindowsRuntimeDatetimeTimespan]  
 
<!-- image links -->  

<!-- links  -->  

[WindowsRuntimeConsiderationsApi]: /microsoft-edge/windows-runtime/considerations-when-using-the-windows-runtime-api "Überlegungen bei der Verwendung der Windows-Runtime-API"  
[WindowsRuntimeEventsJavascript]: /microsoft-edge/windows-runtime/handling-windows-runtime-events-in-javascript "Behandeln von Windows-Runtime-Ereignissen in JavaScript"  
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "JavaScript-Darstellung von Windows-Runtime-Typen"  
[WindowsRuntimeAsynchronousMethods]: /microsoft-edge/windows-runtime/using-windows-runtime-asynchronous-methods "Verwenden von asynchronen Windows-Runtime-Methoden"  
[WindowsRuntimeDatetimeTimespan]: /microsoft-edge/windows-runtime/windows-runtime-datetime-and-timespan-representations "Windows-Runtime-DateTime-und TimeSpan-Darstellungen"  

[UwpApiIndex]: /uwp/api/index "Windows UWP-Namespaces"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Komponenten für Windows-Runtime mit C++/CX"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Komponenten für Windows-Runtime mit C# und Visual Basic"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "JavaScript-Referenz | MDN"  

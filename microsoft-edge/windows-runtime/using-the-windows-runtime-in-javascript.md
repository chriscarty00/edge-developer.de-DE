---
title: Verwenden der Windows-Runtime in JavaScript
ms.custom: ''
ms.date: 07/29/2020
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
ms.openlocfilehash: 444008598a2f7a2f5257544304bed87fbfaa203a
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942173"
---
# Verwenden der Windows-Runtime in JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

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
[Verwenden von den asynchronen Methoden von Windows Runtime][WindowsRuntimeAsynchronousMethods]   
[Behandeln von Windows-Runtime-Ereignissen in JavaScript][WindowsRuntimeEventsJavascript]   
[JavaScript-Darstellung von Windows Runtime-Typen][WindowsRuntimeJavascriptTypes]   
[JavaScript-Projektion der Windows-Runtime DateTime und TimeSpan][WindowsRuntimeDatetimeTimespan]  

<!-- links  -->  

[WindowsRuntimeConsiderationsApi]: ./considerations-when-using-the-windows-runtime-api.md "Überlegungen bei der Verwendung der Windows-Runtime-API | Microsoft docs"  
[WindowsRuntimeEventsJavascript]: ./handling-windows-runtime-events-in-javascript.md "Behandeln von Windows-Runtime-Ereignissen in JavaScript | Microsoft docs"  
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "JavaScript-Darstellung von Windows-Runtime-Typen | Microsoft docs"  
[WindowsRuntimeAsynchronousMethods]: ./using-windows-runtime-asynchronous-methods.md "Verwenden von asynchronen Methoden für die Windows-Runtime | Microsoft docs"  
[WindowsRuntimeDatetimeTimespan]: ./windows-runtime-datetime-and-timespan-representations.md "Windows-Runtime-DateTime-und TimeSpan-Darstellungen | Microsoft docs"  

[UwpApiIndex]: /uwp/api/index "Windows UWP-Namespaces | Microsoft docs"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Komponenten für Windows-Runtime mit C++/CX | Microsoft docs"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Komponenten für Windows-Runtime mit C# und Visual Basic | Microsoft docs"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "JavaScript-Referenz | MDN"  

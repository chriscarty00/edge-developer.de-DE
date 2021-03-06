---
description: Verwenden der Windows-Runtime in JavaScript
title: Verwenden der Windows-Runtime in JavaScript
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime
ms.assetid: 90658546-f746-4e34-a7d1-71cf9ee322a2
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4e137526ce147cdeb82749474bd43d1b3697361b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399323"
---
# <a name="using-the-windows-runtime-in-javascript"></a>Verwenden der Windows-Runtime in JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Wenn Sie eine App für die universelle Windows-Plattform \(UWP\) schreiben, können Sie Windows-Runtime-Klassen, -Methoden und -Eigenschaften genauso verwenden wie systemeigene JavaScript-Objekte, -Methoden und -Eigenschaften.  Dieses Thema enthält Einführungsinformationen und Links zu Themen, in denen die grundlegenden Konzepte der Verwendung von Windows-Runtime-APIs in JavaScript erläutert werden, einschließlich einer Erläuterung, wie Windows-Runtime-Typen dargestellt werden, wie asynchrone Windows-Runtime-Methoden verwendet werden und wie Windows-Runtime-Ereignisse abgehört und behandelt werden.  

Allgemeine Sprachdokumentation finden Sie in der [JavaScript-Referenzbibliothek][MDNJavascriptReference] von MDN.  

> [!IMPORTANT]
> Windows-Runtime-Features sind für Apps, die in Internet Explorer ausgeführt werden, nicht verfügbar.  

## <a name="windows-runtime-reference-documentation"></a>Referenzdokumentation zur Windows-Runtime  

Referenzdokumentation finden Sie unter [Windows Runtime Reference][UwpApiIndex].  Codebeispiele sind in JavaScript und auch in C++, C# und Visual Basic.  

## <a name="writing-windows-runtime-components-in-c-c-or-visual-basic"></a>Schreiben von Windows-Runtime-Komponenten in C++, C# oder Visual Basic  

Anweisungen und Richtlinien zum Schreiben von Windows-Runtime-Komponenten, die in JavaScript verwendet werden können, finden Sie unter [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] und Creating Windows Runtime Components in C# and [Visual Basic][WindowsUwpWinrtCsharpVb].  

## <a name="casing-conventions-with-windows-runtime-features"></a>Casing-Konventionen mit Windows-Runtime-Features  

Die Casing-Konventionen für Windows-Runtime-Features in JavaScript unterscheiden sich geringfügig von denen für andere Sprachen:  

*   Namespaces und Klassen sind im Fall Von Pascal:  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   Elemente von Klassen, einschließlich Methoden und Eigenschaften, sowie Elemente von Strukturen und Enumerationen, befinden sich im Kamelfall:  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   Ereignisnamen sind in Klein klein:  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  
    
## <a name="see-also"></a>Weitere Informationen  

[Überlegungen bei der Verwendung der Windows-Runtime-API][WindowsRuntimeConsiderationsApi]  
[Verwenden von den asynchronen Methoden von Windows Runtime][WindowsRuntimeAsynchronousMethods]   
[Behandeln von Windows-Runtime-Ereignissen in JavaScript][WindowsRuntimeEventsJavascript]   
[JavaScript-Darstellung von Windows Runtime-Typen][WindowsRuntimeJavascriptTypes]   
[JavaScript-Projektion von DateTime und TimeSpan der Windows-Runtime][WindowsRuntimeDatetimeTimespan]  

<!-- links -->  

[WindowsRuntimeConsiderationsApi]: ./considerations-when-using-the-windows-runtime-api.md "Überlegungen bei der Verwendung der Windows-Runtime-API | Microsoft Docs"  
[WindowsRuntimeEventsJavascript]: ./handling-windows-runtime-events-in-javascript.md "Behandeln von Windows-Runtime-Ereignissen in JavaScript-| Microsoft Docs"  
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "JavaScript-Darstellung von Windows-Laufzeittypen | Microsoft Docs"  
[WindowsRuntimeAsynchronousMethods]: ./using-windows-runtime-asynchronous-methods.md "Verwenden von asynchronen Methoden für die Windows-Runtime | Microsoft Docs"  
[WindowsRuntimeDatetimeTimespan]: ./windows-runtime-datetime-and-timespan-representations.md "Windows-Runtime-DateTime- und TimeSpan-| Microsoft Docs"  

[UwpApiIndex]: /uwp/api/index "Windows UWP-Namespaces | Microsoft Docs"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Windows-Runtime-Komponenten mit C++/CX-| Microsoft Docs"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Windows-Runtime-Komponenten mit C# und Visual Basic | Microsoft Docs"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "JavaScript-| MDN"  

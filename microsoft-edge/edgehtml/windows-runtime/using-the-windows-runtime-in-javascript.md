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
# <a name="using-the-windows-runtime-in-javascript"></a><span data-ttu-id="55d3a-103">Verwenden der Windows-Runtime in JavaScript</span><span class="sxs-lookup"><span data-stu-id="55d3a-103">Using the Windows Runtime in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="55d3a-104">Wenn Sie eine App für die universelle Windows-Plattform \(UWP\) schreiben, können Sie Windows-Runtime-Klassen, -Methoden und -Eigenschaften genauso verwenden wie systemeigene JavaScript-Objekte, -Methoden und -Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="55d3a-104">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="55d3a-105">Dieses Thema enthält Einführungsinformationen und Links zu Themen, in denen die grundlegenden Konzepte der Verwendung von Windows-Runtime-APIs in JavaScript erläutert werden, einschließlich einer Erläuterung, wie Windows-Runtime-Typen dargestellt werden, wie asynchrone Windows-Runtime-Methoden verwendet werden und wie Windows-Runtime-Ereignisse abgehört und behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="55d3a-105">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="55d3a-106">Allgemeine Sprachdokumentation finden Sie in der [JavaScript-Referenzbibliothek][MDNJavascriptReference] von MDN.</span><span class="sxs-lookup"><span data-stu-id="55d3a-106">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="55d3a-107">Windows-Runtime-Features sind für Apps, die in Internet Explorer ausgeführt werden, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="55d3a-107">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="windows-runtime-reference-documentation"></a><span data-ttu-id="55d3a-108">Referenzdokumentation zur Windows-Runtime</span><span class="sxs-lookup"><span data-stu-id="55d3a-108">Windows Runtime reference documentation</span></span>  

<span data-ttu-id="55d3a-109">Referenzdokumentation finden Sie unter [Windows Runtime Reference][UwpApiIndex].</span><span class="sxs-lookup"><span data-stu-id="55d3a-109">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="55d3a-110">Codebeispiele sind in JavaScript und auch in C++, C# und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="55d3a-110">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <a name="writing-windows-runtime-components-in-c-c-or-visual-basic"></a><span data-ttu-id="55d3a-111">Schreiben von Windows-Runtime-Komponenten in C++, C# oder Visual Basic</span><span class="sxs-lookup"><span data-stu-id="55d3a-111">Writing Windows Runtime components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="55d3a-112">Anweisungen und Richtlinien zum Schreiben von Windows-Runtime-Komponenten, die in JavaScript verwendet werden können, finden Sie unter [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] und Creating Windows Runtime Components in C# and [Visual Basic][WindowsUwpWinrtCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="55d3a-112">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <a name="casing-conventions-with-windows-runtime-features"></a><span data-ttu-id="55d3a-113">Casing-Konventionen mit Windows-Runtime-Features</span><span class="sxs-lookup"><span data-stu-id="55d3a-113">Casing conventions with Windows Runtime features</span></span>  

<span data-ttu-id="55d3a-114">Die Casing-Konventionen für Windows-Runtime-Features in JavaScript unterscheiden sich geringfügig von denen für andere Sprachen:</span><span class="sxs-lookup"><span data-stu-id="55d3a-114">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="55d3a-115">Namespaces und Klassen sind im Fall Von Pascal:</span><span class="sxs-lookup"><span data-stu-id="55d3a-115">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="55d3a-116">Elemente von Klassen, einschließlich Methoden und Eigenschaften, sowie Elemente von Strukturen und Enumerationen, befinden sich im Kamelfall:</span><span class="sxs-lookup"><span data-stu-id="55d3a-116">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="55d3a-117">Ereignisnamen sind in Klein klein:</span><span class="sxs-lookup"><span data-stu-id="55d3a-117">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  
    
## <a name="see-also"></a><span data-ttu-id="55d3a-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="55d3a-118">See also</span></span>  

[<span data-ttu-id="55d3a-119">Überlegungen bei der Verwendung der Windows-Runtime-API</span><span class="sxs-lookup"><span data-stu-id="55d3a-119">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="55d3a-120">Verwenden von den asynchronen Methoden von Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="55d3a-120">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="55d3a-121">Behandeln von Windows-Runtime-Ereignissen in JavaScript</span><span class="sxs-lookup"><span data-stu-id="55d3a-121">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="55d3a-122">JavaScript-Darstellung von Windows Runtime-Typen</span><span class="sxs-lookup"><span data-stu-id="55d3a-122">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="55d3a-123">JavaScript-Projektion von DateTime und TimeSpan der Windows-Runtime</span><span class="sxs-lookup"><span data-stu-id="55d3a-123">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  

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

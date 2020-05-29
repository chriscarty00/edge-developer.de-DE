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
# <span data-ttu-id="e594b-102">Verwenden der Windows-Runtime in JavaScript</span><span class="sxs-lookup"><span data-stu-id="e594b-102">Using the Windows Runtime in JavaScript</span></span>  

<span data-ttu-id="e594b-103">Wenn Sie eine universelle Windows-Plattform \ (UWP \)-app schreiben, können Sie Windows-Runtime-Klassen,-Methoden und-Eigenschaften auf die gleiche Weise verwenden wie systemeigene JavaScript-Objekte,-Methoden und-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e594b-103">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="e594b-104">Dieses Thema enthält einführende Informationen und Links zu Themen, in denen die grundlegenden Konzepte der Verwendung von Windows-Runtime-APIs in JavaScript erläutert werden, einschließlich einer Erläuterung, wie Windows-Runtime-Typen dargestellt werden, wie asynchrone Windows-Runtime-Methoden verwendet werden und wie Windows-Runtime-Ereignisse überwacht und behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="e594b-104">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="e594b-105">Informationen zur allgemeinen Sprachdokumentation finden Sie in der [JavaScript-Referenz][MDNJavascriptReference] Bibliothek von MDN.</span><span class="sxs-lookup"><span data-stu-id="e594b-105">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="e594b-106">Windows-Runtime-Features stehen für apps, die in Internet Explorer ausgeführt werden, nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e594b-106">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="e594b-107">Windows-Runtime-Referenzdokumentation</span><span class="sxs-lookup"><span data-stu-id="e594b-107">Windows Runtime Reference Documentation</span></span>  

<span data-ttu-id="e594b-108">Eine Referenzdokumentation finden Sie unter [Windows-Runtime-Referenz][UwpApiIndex].</span><span class="sxs-lookup"><span data-stu-id="e594b-108">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="e594b-109">Code Beispiele stehen in JavaScript und auch in C++, C# und Visual Basic zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e594b-109">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <span data-ttu-id="e594b-110">Schreiben von Komponenten für Windows-Runtime in C++, C# oder Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e594b-110">Writing Windows Runtime Components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="e594b-111">Anweisungen und Richtlinien zum Schreiben von Komponenten für Windows-Runtime, die in JavaScript verwendet werden können, finden Sie unter [Erstellen von Komponenten für Windows-Runtime in C++][WindowsUwpWinrtCpp] und [Erstellen von Komponenten für Windows-Runtime in C# und Visual Basic][WindowsUwpWinrtCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="e594b-111">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <span data-ttu-id="e594b-112">Konventionen für die Groß-/Kleinschreibung mit Windows-Runtime-Features</span><span class="sxs-lookup"><span data-stu-id="e594b-112">Casing Conventions with Windows Runtime Features</span></span>  

<span data-ttu-id="e594b-113">Die Konventionen für die Groß-/Kleinschreibung für Windows-Runtime-Features in JavaScript unterscheiden sich geringfügig von denen für andere Sprachen:</span><span class="sxs-lookup"><span data-stu-id="e594b-113">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="e594b-114">Namespaces und Klassen sind in Pascal-Fall:</span><span class="sxs-lookup"><span data-stu-id="e594b-114">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="e594b-115">Mitglieder von Klassen, einschließlich Methoden und Eigenschaften sowie Member von Strukturen und Enumerationen, befinden sich im Camel-Fall:</span><span class="sxs-lookup"><span data-stu-id="e594b-115">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="e594b-116">Ereignisnamen sind in Kleinbuchstaben:</span><span class="sxs-lookup"><span data-stu-id="e594b-116">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## <span data-ttu-id="e594b-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e594b-117">See Also</span></span>  

[<span data-ttu-id="e594b-118">Überlegungen bei der Verwendung der Windows-Runtime-API</span><span class="sxs-lookup"><span data-stu-id="e594b-118">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="e594b-119">Verwenden von asynchronen Windows-Runtime-Methoden</span><span class="sxs-lookup"><span data-stu-id="e594b-119">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="e594b-120">Behandeln von Windows-Runtime-Ereignissen in JavaScript</span><span class="sxs-lookup"><span data-stu-id="e594b-120">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="e594b-121">JavaScript-Darstellung von Windows-Runtime-Typen</span><span class="sxs-lookup"><span data-stu-id="e594b-121">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="e594b-122">JavaScript-Projektion der Windows-Runtime DateTime und TimeSpan</span><span class="sxs-lookup"><span data-stu-id="e594b-122">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  
 
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

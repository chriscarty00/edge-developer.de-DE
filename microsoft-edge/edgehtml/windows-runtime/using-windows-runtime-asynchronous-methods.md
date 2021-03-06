---
description: Verwenden von den asynchronen Methoden von Windows Runtime
title: Verwenden von den asynchronen Methoden von Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c7e8ac4690525ee89a06eccf843531c2c7a20324
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398154"
---
# <a name="using-windows-runtime-asynchronous-methods"></a><span data-ttu-id="9fc2a-103">Asynchrone Methoden von Windows-Runtime verwenden</span><span class="sxs-lookup"><span data-stu-id="9fc2a-103">Using Windows Runtime asynchronous methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="9fc2a-104">Viele Windows-Runtime-Methoden, insbesondere Methoden, die sehr lange dauern können, sind asynchron.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-104">Many Windows Runtime methods, especially methods that might take a long time to complete, are asynchronous.</span></span>  <span data-ttu-id="9fc2a-105">Diese Methoden geben im Allgemeinen eine asynchrone Aktion oder einen Vorgang \(z. B. `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` , , oder `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \) zurück.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-105">These methods generally return an asynchronous action or operation \(for example, `Windows.Foundation.IAsyncAction`, `Windows.Foundation.IAsyncOperation`, `Windows.Foundation.IAsyncActionWithProgress`, or `Windows.Foundation.IAsyncOperationWithProgress`\).</span></span>  <span data-ttu-id="9fc2a-106">Diese Methoden werden in JavaScript durch das [CommonJS/Promises/A-Muster dargestellt.][CommonjsWikiPromises]</span><span class="sxs-lookup"><span data-stu-id="9fc2a-106">These methods are represented in JavaScript by the [CommonJS/Promises/A pattern][CommonjsWikiPromises].</span></span>  <span data-ttu-id="9fc2a-107">Das heißt, sie geben ein Promise-Objekt zurück, das eine [then-Funktion][PreviousVersionsWindowsAppsBr229728]besitzt, für die Sie eine Funktion bereitstellen müssen, die das Ergebnis verarbeitet, wenn der Vorgang `completed` erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-107">That is, they return a Promise object that has a [then function][PreviousVersionsWindowsAppsBr229728], for which you must provide a `completed` function that handles the result if the operation succeeds.</span></span>  <span data-ttu-id="9fc2a-108">Wenn Sie keinen Fehlerhandler bereitstellen möchten, sollten Sie die [Done-Funktion anstelle][PreviousVersionsWindowsAppsHr701079] der -Funktion `then` verwenden.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-108">If you don't want to provide an error handler, you should use the [done function][PreviousVersionsWindowsAppsHr701079] instead of the `then` function.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="9fc2a-109">Windows-Runtime-Features sind für Apps, die in Internet Explorer ausgeführt werden, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-109">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="examples-of-asynchronous-methods"></a><span data-ttu-id="9fc2a-110">Beispiele für asynchrone Methoden</span><span class="sxs-lookup"><span data-stu-id="9fc2a-110">Examples of asynchronous methods</span></span>  

<span data-ttu-id="9fc2a-111">Im folgenden Beispiel verwendet die `then` Funktion einen Parameter, der den abgeschlossenen Wert der Methode `createResourceAsync` darstellt.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-111">In the following example, the `then` function takes a parameter that represents the completed value of the `createResourceAsync` method.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="9fc2a-112">Wenn die Methode in diesem Fall fehlschlägt, gibt sie eine Zusage im Fehlerstatus zurück, gibt jedoch `createResourceAsync` keine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-112">In this case, if the `createResourceAsync` method fails, it returns a promise in the error state, but does not throw an exception.</span></span>  <span data-ttu-id="9fc2a-113">Sie können einen Fehler behandeln, indem Sie die `then` Funktion wie folgt verwenden.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-113">You can handle an error by using the `then` function as follows.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
              console.log("New item is: " + newItem.id);
          }
          function(err) {
              console.log("Got error: " + err.message);
          });
```  

<span data-ttu-id="9fc2a-114">Wenn Sie den Fehler nicht explizit behandeln, aber eine Ausnahme auswerfen möchten, können Sie stattdessen die `done` Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-114">If you don't want to handle the error explicitly, but do want it to throw an exception, you can use the `done` function instead.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="9fc2a-115">Sie können den Fortschritt zum Abschluss auch mithilfe einer dritten Funktion anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9fc2a-115">You can also display the progress made towards completion by using a third function.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .then(function(newItem) {
               console.log("New item is: " + newItem.id);
            },
    // Error.
            function(error) {
               alert("Failed to create a resource.");
            },
    // Progress.
            function(progress, resultSoFar) {
               setProgressBar(progress);
            });
```  

<span data-ttu-id="9fc2a-116">Weitere Informationen zur asynchronen Programmierung finden Sie unter [Asynchrone Programmierung in JavaScript][PreviousVersionsWindowsAppsHh700330].</span><span class="sxs-lookup"><span data-stu-id="9fc2a-116">For more information about asynchronous programming, see [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span></span>  

## <a name="see-also"></a><span data-ttu-id="9fc2a-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9fc2a-117">See also</span></span>  

[<span data-ttu-id="9fc2a-118">Verwenden der Windows-Runtime in JavaScript</span><span class="sxs-lookup"><span data-stu-id="9fc2a-118">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript-| Microsoft Docs"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promise.then-Methode | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Asynchrone Programmierung in JavaScript (HTML) | Microsoft Docs"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Promise.done-Methode | Microsoft Docs"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Zusagen | CommonJS Spec Wiki"  

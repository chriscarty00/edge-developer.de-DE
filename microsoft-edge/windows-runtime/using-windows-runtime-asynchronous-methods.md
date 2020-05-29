---
title: Verwenden von asynchronen Windows-Runtime-Methoden
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6d0f174d22d0d13571d78bc215356ad90a0ae7fa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568709"
---
# <span data-ttu-id="8fa3c-102">Verwenden von asynchronen Windows-Runtime-Methoden</span><span class="sxs-lookup"><span data-stu-id="8fa3c-102">Using Windows Runtime Asynchronous Methods</span></span>  

<span data-ttu-id="8fa3c-103">Viele Windows-Runtime-Methoden, insbesondere Methoden, die möglicherweise eine lange Zeit in Anspruch nehmen, sind asynchron.</span><span class="sxs-lookup"><span data-stu-id="8fa3c-103">Many Windows Runtime methods, especially methods that might take a long time to complete, are asynchronous.</span></span>  <span data-ttu-id="8fa3c-104">Diese Methoden geben in der Regel eine asynchrone Aktion oder Operation zurück (beispielsweise,,,, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` `Windows.Foundation.IAsyncActionWithProgress` oder `Windows.Foundation.IAsyncOperationWithProgress` ).</span><span class="sxs-lookup"><span data-stu-id="8fa3c-104">These methods generally return an asynchronous action or operation (for example, `Windows.Foundation.IAsyncAction`, `Windows.Foundation.IAsyncOperation`, `Windows.Foundation.IAsyncActionWithProgress`, or `Windows.Foundation.IAsyncOperationWithProgress`).</span></span>  <span data-ttu-id="8fa3c-105">Diese Methoden werden in JavaScript anhand des [CommonJS/Promises/A-Musters][CommonjsWikiPromises]dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8fa3c-105">These methods are represented in JavaScript by the [CommonJS/Promises/A pattern][CommonjsWikiPromises].</span></span>  <span data-ttu-id="8fa3c-106">Das heißt, Sie geben ein Promise-Objekt zurück, das über eine [Then-Funktion][PreviousVersionsWindowsAppsBr229728]verfügt, für die Sie eine Funktion bereitstellen müssen `completed` , die das Ergebnis behandelt, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8fa3c-106">That is, they return a Promise object that has a [then function][PreviousVersionsWindowsAppsBr229728], for which you must provide a `completed` function that handles the result if the operation succeeds.</span></span>  <span data-ttu-id="8fa3c-107">Wenn Sie keinen Fehlerhandler bereitstellen möchten, sollten Sie die Funktion [done][PreviousVersionsWindowsAppsHr701079] anstelle der `then` Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fa3c-107">If you don't want to provide an error handler, you should use the [done function][PreviousVersionsWindowsAppsHr701079] instead of the `then` function.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="8fa3c-108">Windows-Runtime-Features stehen für apps, die in Internet Explorer ausgeführt werden, nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8fa3c-108">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="8fa3c-109">Beispiele für asynchrone Methoden</span><span class="sxs-lookup"><span data-stu-id="8fa3c-109">Examples of Asynchronous Methods</span></span>  

<span data-ttu-id="8fa3c-110">Im folgenden Beispiel `then` akzeptiert die Funktion einen Parameter, der den abgeschlossenen Wert der Methode darstellt `createResourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="8fa3c-110">In the following example, the `then` function takes a parameter that represents the completed value of the `createResourceAsync` method.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="8fa3c-111">In diesem Fall wird bei einer `createResourceAsync` fehlgeschlagenen Methode eine Zusage im Fehlerzustand zurückgegeben, jedoch keine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8fa3c-111">In this case, if the `createResourceAsync` method fails, it returns a promise in the error state, but does not throw an exception.</span></span>  <span data-ttu-id="8fa3c-112">Sie können einen Fehler behandeln, indem Sie die `then` Funktion wie folgt verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fa3c-112">You can handle an error by using the `then` function as follows.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
              console.log("New item is: " + newItem.id);
          }
          function(err) {
              console.log("Got error: " + err.message);
          });
```  

<span data-ttu-id="8fa3c-113">Wenn Sie den Fehler nicht explizit behandeln, aber eine Ausnahme auslösen möchten, können Sie `done` stattdessen die Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fa3c-113">If you don't want to handle the error explicitly, but do want it to throw an exception, you can use the `done` function instead.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="8fa3c-114">Mit einer dritten Funktion können Sie auch den Fortschritt zur Vervollständigung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8fa3c-114">You can also display the progress made towards completion by using a third function.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .then(function(newItem) {
               console.log("New item is: " + newItem.id);
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

<span data-ttu-id="8fa3c-115">Weitere Informationen zur asynchronen Programmierung finden Sie unter [asynchrone Programmierung in JavaScript][PreviousVersionsWindowsAppsHh700330].</span><span class="sxs-lookup"><span data-stu-id="8fa3c-115">For more information about asynchronous programming, see [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span></span>  

## <span data-ttu-id="8fa3c-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8fa3c-116">See Also</span></span>  

[<span data-ttu-id="8fa3c-117">Verwenden der Windows-Runtime in JavaScript</span><span class="sxs-lookup"><span data-stu-id="8fa3c-117">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Verwenden der Windows-Runtime in JavaScript"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promise. then-Methode"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Asynchrone Programmierung in JavaScript (HTML)"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Promise. Done-Methode"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Versprechungen | CommonJS spec-wiki"  

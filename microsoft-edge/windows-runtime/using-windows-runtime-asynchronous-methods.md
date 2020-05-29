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
# Verwenden von asynchronen Windows-Runtime-Methoden  

Viele Windows-Runtime-Methoden, insbesondere Methoden, die möglicherweise eine lange Zeit in Anspruch nehmen, sind asynchron.  Diese Methoden geben in der Regel eine asynchrone Aktion oder Operation zurück (beispielsweise,,,, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` `Windows.Foundation.IAsyncActionWithProgress` oder `Windows.Foundation.IAsyncOperationWithProgress` ).  Diese Methoden werden in JavaScript anhand des [CommonJS/Promises/A-Musters][CommonjsWikiPromises]dargestellt.  Das heißt, Sie geben ein Promise-Objekt zurück, das über eine [Then-Funktion][PreviousVersionsWindowsAppsBr229728]verfügt, für die Sie eine Funktion bereitstellen müssen `completed` , die das Ergebnis behandelt, wenn der Vorgang erfolgreich ausgeführt wurde.  Wenn Sie keinen Fehlerhandler bereitstellen möchten, sollten Sie die Funktion [done][PreviousVersionsWindowsAppsHr701079] anstelle der `then` Funktion verwenden.  

> [!IMPORTANT]
> Windows-Runtime-Features stehen für apps, die in Internet Explorer ausgeführt werden, nicht zur Verfügung.  

## Beispiele für asynchrone Methoden  

Im folgenden Beispiel `then` akzeptiert die Funktion einen Parameter, der den abgeschlossenen Wert der Methode darstellt `createResourceAsync` .  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

In diesem Fall wird bei einer `createResourceAsync` fehlgeschlagenen Methode eine Zusage im Fehlerzustand zurückgegeben, jedoch keine Ausnahme ausgelöst.  Sie können einen Fehler behandeln, indem Sie die `then` Funktion wie folgt verwenden.  

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

Wenn Sie den Fehler nicht explizit behandeln, aber eine Ausnahme auslösen möchten, können Sie `done` stattdessen die Funktion verwenden.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

Mit einer dritten Funktion können Sie auch den Fortschritt zur Vervollständigung anzeigen.  

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

Weitere Informationen zur asynchronen Programmierung finden Sie unter [asynchrone Programmierung in JavaScript][PreviousVersionsWindowsAppsHh700330].  

## Weitere Informationen  

[Verwenden der Windows-Runtime in JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Verwenden der Windows-Runtime in JavaScript"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promise. then-Methode"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Asynchrone Programmierung in JavaScript (HTML)"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Promise. Done-Methode"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Versprechungen | CommonJS spec-wiki"  

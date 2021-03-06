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
# <a name="using-windows-runtime-asynchronous-methods"></a>Asynchrone Methoden von Windows-Runtime verwenden  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Viele Windows-Runtime-Methoden, insbesondere Methoden, die sehr lange dauern können, sind asynchron.  Diese Methoden geben im Allgemeinen eine asynchrone Aktion oder einen Vorgang \(z. B. `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` , , oder `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \) zurück.  Diese Methoden werden in JavaScript durch das [CommonJS/Promises/A-Muster dargestellt.][CommonjsWikiPromises]  Das heißt, sie geben ein Promise-Objekt zurück, das eine [then-Funktion][PreviousVersionsWindowsAppsBr229728]besitzt, für die Sie eine Funktion bereitstellen müssen, die das Ergebnis verarbeitet, wenn der Vorgang `completed` erfolgreich ist.  Wenn Sie keinen Fehlerhandler bereitstellen möchten, sollten Sie die [Done-Funktion anstelle][PreviousVersionsWindowsAppsHr701079] der -Funktion `then` verwenden.  

> [!IMPORTANT]
> Windows-Runtime-Features sind für Apps, die in Internet Explorer ausgeführt werden, nicht verfügbar.  

## <a name="examples-of-asynchronous-methods"></a>Beispiele für asynchrone Methoden  

Im folgenden Beispiel verwendet die `then` Funktion einen Parameter, der den abgeschlossenen Wert der Methode `createResourceAsync` darstellt.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

Wenn die Methode in diesem Fall fehlschlägt, gibt sie eine Zusage im Fehlerstatus zurück, gibt jedoch `createResourceAsync` keine Ausnahme aus.  Sie können einen Fehler behandeln, indem Sie die `then` Funktion wie folgt verwenden.  

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

Wenn Sie den Fehler nicht explizit behandeln, aber eine Ausnahme auswerfen möchten, können Sie stattdessen die `done` Funktion verwenden.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

Sie können den Fortschritt zum Abschluss auch mithilfe einer dritten Funktion anzeigen.  

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

Weitere Informationen zur asynchronen Programmierung finden Sie unter [Asynchrone Programmierung in JavaScript][PreviousVersionsWindowsAppsHh700330].  

## <a name="see-also"></a>Weitere Informationen  

[Verwenden der Windows-Runtime in JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript-| Microsoft Docs"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promise.then-Methode | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Asynchrone Programmierung in JavaScript (HTML) | Microsoft Docs"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Promise.done-Methode | Microsoft Docs"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Zusagen | CommonJS Spec Wiki"  

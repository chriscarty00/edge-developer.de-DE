---
description: Verwenden Sie die Konsolen-API, um Nachrichten in die Konsole zu schreiben.
title: Konsolen-API-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: f38a7403cf11fbec5f5833fc0b1ed10207b436de
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398049"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="console-api-reference"></a><span data-ttu-id="a9574-104">Konsolen-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="a9574-104">Console API reference</span></span>  

<span data-ttu-id="a9574-105">Verwenden Sie die Console-API-Methoden, um Nachrichten aus Ihrem JavaScript in die Konsole zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="a9574-105">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="a9574-106">Eine interaktive Einführung in das Thema finden Sie unter Erste Schritte [mit protokollieren von Nachrichten an der Konsole.][DevtoolsConsoleLog]</span><span class="sxs-lookup"><span data-stu-id="a9574-106">For an interactive introduction to the topic, navigate to [Get Started With Logging Messages To The Console][DevtoolsConsoleLog].</span></span>  <span data-ttu-id="a9574-107">Navigieren Sie zu `debug()` `monitorEvents()` [Konsolenprogramme-API-Referenz,][DevtoolConsoleUtilities] \*\*\*\* um die Praktischkeitsmethoden wie oder die nur im Konsolenbereich verfügbar sind zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="a9574-107">For the convenience methods like `debug()` or `monitorEvents()` which are only available from the **Console** pane, navigate to [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <a name="assert"></a><span data-ttu-id="a9574-108">assert</span><span class="sxs-lookup"><span data-stu-id="a9574-108">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="a9574-109">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="a9574-109">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="a9574-110">Schreibt einen [Fehler](#error) in die Konsole, wenn `expression` er in ausgewertet `false` wird.</span><span class="sxs-lookup"><span data-stu-id="a9574-110">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Das Ergebnis des Beispiels console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
   <span data-ttu-id="a9574-112">Abbildung 1: Das Ergebnis des `console.assert()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-112">Figure 1:  The result of the `console.assert()` example</span></span>  
:::image-end:::  

---  

## <a name="clear"></a><span data-ttu-id="a9574-113">clear</span><span class="sxs-lookup"><span data-stu-id="a9574-113">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="a9574-114">Die Konsole wird geräumt.</span><span class="sxs-lookup"><span data-stu-id="a9574-114">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="a9574-115">Wenn ["Protokoll beibehalten"][DevtoolsConsoleReferenceLevel] aktiviert ist, ist [die clear-Methode](#clear) deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a9574-115">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

### <a name="see-also"></a><span data-ttu-id="a9574-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a9574-116">See also</span></span>  

*   [<span data-ttu-id="a9574-117">Löschen der Konsole</span><span class="sxs-lookup"><span data-stu-id="a9574-117">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a><span data-ttu-id="a9574-118">count</span><span class="sxs-lookup"><span data-stu-id="a9574-118">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="a9574-119">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="a9574-119">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="a9574-120">Schreibt die Anzahl der Aufrufe der [Count-Methode](#count) in derselben Zeile und mit derselben `label` .</span><span class="sxs-lookup"><span data-stu-id="a9574-120">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="a9574-121">Verwenden Sie die [countReset-Methode,](#countreset) um die Anzahl zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="a9574-121">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Das Ergebnis des Beispiels console.count()" lightbox="../media/console-demo-count-button.msft.png":::
   <span data-ttu-id="a9574-123">Abbildung 2: Das Ergebnis des `console.count()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-123">Figure 2:  The result of the `console.count()` example</span></span>  
:::image-end:::  

---  

## <a name="countreset"></a><span data-ttu-id="a9574-124">countReset</span><span class="sxs-lookup"><span data-stu-id="a9574-124">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="a9574-125">Setzt eine Anzahl zurück.</span><span class="sxs-lookup"><span data-stu-id="a9574-125">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <a name="debug"></a><span data-ttu-id="a9574-126">debuggen</span><span class="sxs-lookup"><span data-stu-id="a9574-126">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="a9574-127">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="a9574-127">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`

<span data-ttu-id="a9574-128">Identisch mit [Protokoll mit](#log) Ausnahme unterschiedlicher Protokollebene.</span><span class="sxs-lookup"><span data-stu-id="a9574-128">Identical to [log](#log) except different log level.</span></span>  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Das Ergebnis des Beispiels console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
   <span data-ttu-id="a9574-130">Abbildung 3: Das Ergebnis des `console.debug()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-130">Figure 3:  The result of the `console.debug()` example</span></span>  
:::image-end:::  

---  

## <a name="dir"></a><span data-ttu-id="a9574-131">dir</span><span class="sxs-lookup"><span data-stu-id="a9574-131">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="a9574-132">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="a9574-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="a9574-133">Druckt eine JSON-Darstellung des angegebenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="a9574-133">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Das Ergebnis des Beispiels console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
   <span data-ttu-id="a9574-135">Abbildung 4: Das Ergebnis des `console.dir()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-135">Figure 4:  The result of the `console.dir()` example</span></span>  
:::image-end:::  

---  

## <a name="dirxml"></a><span data-ttu-id="a9574-136">dirxml</span><span class="sxs-lookup"><span data-stu-id="a9574-136">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="a9574-137">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="a9574-137">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="a9574-138">Druckt eine XML-Darstellung der untergeordneten Elemente von `node` .</span><span class="sxs-lookup"><span data-stu-id="a9574-138">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Das Ergebnis des Console.dirxml()-Beispiels" lightbox="../media/console-demo-dirxml-button.msft.png":::
   <span data-ttu-id="a9574-140">Abbildung 5: Das Ergebnis des `console.dirxml()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-140">Figure 5:  The result of the `console.dirxml()` example</span></span>  
:::image-end:::  

---  

## <a name="error"></a><span data-ttu-id="a9574-141">Fehler</span><span class="sxs-lookup"><span data-stu-id="a9574-141">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="a9574-142">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="a9574-142">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="a9574-143">Druckt `object` die in die Konsole, formatiert sie als Fehler und enthält eine Stapelverfolgung.</span><span class="sxs-lookup"><span data-stu-id="a9574-143">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Das Ergebnis des Beispiels console.error()" lightbox="../media/console-demo-error-button.msft.png":::
   <span data-ttu-id="a9574-145">Abbildung 6: Das Ergebnis des `console.error()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-145">Figure 6:  The result of the `console.error()` example</span></span>  
:::image-end:::  

---  

## <a name="group"></a><span data-ttu-id="a9574-146">Gruppe</span><span class="sxs-lookup"><span data-stu-id="a9574-146">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="a9574-147">Gruppen von Nachrichten visuell, bis [die groupEnd-Methode](#groupend) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9574-147">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="a9574-148">Verwenden Sie [die groupCollapsed-Methode,](#groupcollapsed) um die Gruppe zu reduzieren, wenn sie anfänglich bei der Konsole protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="a9574-148">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Das Ergebnis des Beispiels console.group()" lightbox="../media/console-demo-group-button.msft.png":::
   <span data-ttu-id="a9574-150">Abbildung 7: Das Ergebnis des `console.group()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-150">Figure 7:  The result of the `console.group()` example</span></span>  
:::image-end:::  

---  

## <a name="groupcollapsed"></a><span data-ttu-id="a9574-151">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="a9574-151">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="a9574-152">Identisch mit der [Protokollmethode,](#log) mit der Ausnahme, dass die Gruppe anfänglich reduziert wird, wenn sie bei der Konsole protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="a9574-152">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

---  

## <a name="groupend"></a><span data-ttu-id="a9574-153">groupEnd</span><span class="sxs-lookup"><span data-stu-id="a9574-153">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="a9574-154">Beendet das visuelle Gruppieren von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="a9574-154">Stops visually grouping messages.</span></span>  <span data-ttu-id="a9574-155">Navigieren Sie zur [Gruppenmethode.](#group)</span><span class="sxs-lookup"><span data-stu-id="a9574-155">Navigate to the [group](#group) method.</span></span>  

---  

## <a name="info"></a><span data-ttu-id="a9574-156">„Informationen”</span><span class="sxs-lookup"><span data-stu-id="a9574-156">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="a9574-157">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="a9574-157">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="a9574-158">Identisch mit der [Protokollmethode.](#log)</span><span class="sxs-lookup"><span data-stu-id="a9574-158">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Das Ergebnis des beispiels console.info()" lightbox="../media/console-demo-info-button.msft.png":::
   <span data-ttu-id="a9574-160">Abbildung 8: Das Ergebnis des `console.info()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-160">Figure 8:  The result of the `console.info()` example</span></span>  
:::image-end:::  

---  

## <a name="log"></a><span data-ttu-id="a9574-161">log</span><span class="sxs-lookup"><span data-stu-id="a9574-161">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="a9574-162">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="a9574-162">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="a9574-163">Druckt eine Nachricht an die Konsole.</span><span class="sxs-lookup"><span data-stu-id="a9574-163">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Das Ergebnis des Beispiels console.log()" lightbox="../media/console-demo-log-button.msft.png":::
   <span data-ttu-id="a9574-165">Abbildung 9: Das Ergebnis des `console.log()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-165">Figure 9:  The result of the `console.log()` example</span></span>  
:::image-end:::  

---  

## <a name="table"></a><span data-ttu-id="a9574-166">Tabelle</span><span class="sxs-lookup"><span data-stu-id="a9574-166">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="a9574-167">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="a9574-167">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="a9574-168">Protokolliert ein Array von Objekten als Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a9574-168">Logs an array of objects as a table.</span></span>  

```javascript
console.table([
    {
        first: 'René',
        last: 'Magritte',
    },
    {
        first: 'Chaim',
        last: 'Soutine',
        birthday: '18930113',
    },
    {
        first: 'Henri',
        last: 'Matisse',
    }
]);
```  

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Das Ergebnis des Beispiels console.table()" lightbox="../media/console-demo-table-button.msft.png":::
   <span data-ttu-id="a9574-170">Abbildung 10: Das Ergebnis des `console.table()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-170">Figure 10:  The result of the `console.table()` example</span></span>  
:::image-end:::  

---  

## <a name="time"></a><span data-ttu-id="a9574-171">time</span><span class="sxs-lookup"><span data-stu-id="a9574-171">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="a9574-172">Startet einen neuen Timer.</span><span class="sxs-lookup"><span data-stu-id="a9574-172">Starts a new timer.</span></span>  <span data-ttu-id="a9574-173">Verwenden Sie [die timeEnd-Methode,](#timeend) um den Timer zu beenden und die verstrichene Zeit in der Konsole zu drucken.</span><span class="sxs-lookup"><span data-stu-id="a9574-173">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Das Ergebnis des Beispiels console.time()" lightbox="../media/console-demo-time-button.msft.png":::
   <span data-ttu-id="a9574-175">Abbildung 11: Das Ergebnis des `console.time()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-175">Figure 11:  The result of the `console.time()` example</span></span>  
:::image-end:::  

---  

## <a name="timeend"></a><span data-ttu-id="a9574-176">timeEnd</span><span class="sxs-lookup"><span data-stu-id="a9574-176">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="a9574-177">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="a9574-177">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="a9574-178">Stoppt einen Timer.</span><span class="sxs-lookup"><span data-stu-id="a9574-178">Stops a timer.</span></span>  <span data-ttu-id="a9574-179">Navigieren Sie zur [Time-Methode.](#time)</span><span class="sxs-lookup"><span data-stu-id="a9574-179">Navigate to the [time](#time) method.</span></span>  

---  

## <a name="trace"></a><span data-ttu-id="a9574-180">trace</span><span class="sxs-lookup"><span data-stu-id="a9574-180">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="a9574-181">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="a9574-181">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="a9574-182">Druckt eine Stapelverfolgung in die Konsole.</span><span class="sxs-lookup"><span data-stu-id="a9574-182">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Das Ergebnis des Beispiels console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
   <span data-ttu-id="a9574-184">Abbildung 12: Das Ergebnis des `console.trace()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-184">Figure 12:  The result of the `console.trace()` example</span></span>  
:::image-end:::  

---  

## <a name="warn"></a><span data-ttu-id="a9574-185">warnen</span><span class="sxs-lookup"><span data-stu-id="a9574-185">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="a9574-186">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="a9574-186">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="a9574-187">Druckt eine Warnung an die Konsole.</span><span class="sxs-lookup"><span data-stu-id="a9574-187">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Das Ergebnis des Console.warn()-Beispiels" lightbox="../media/console-demo-warn-button.msft.png":::
   <span data-ttu-id="a9574-189">Abbildung 13: Das Ergebnis des `console.warn()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="a9574-189">Figure 13:  The result of the `console.warn()` example</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a9574-190">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="a9574-190">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Erste Schritte mit der Protokollierung von Nachrichten in der Konsole"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Apireferenz für Konsolenprogramme"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Löschen der Konsole – Konsolenreferenz"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Nachrichten über Seitenlasten hinweg beibehalten – Konsolenreferenz"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtern nach Protokollebene – Konsolenreferenz"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chromium)-Entwicklertools"  

> [!NOTE]
> <span data-ttu-id="a9574-197">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9574-197">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a9574-198">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/api) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="a9574-198">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a9574-200">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a9574-200">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

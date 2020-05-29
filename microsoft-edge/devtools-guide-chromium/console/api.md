---
title: Konsolen-API-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: e54bae7c7c61584ccd39568f1bb54312cc2082c0
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601754"
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





# <span data-ttu-id="38e41-103">Konsolen-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="38e41-103">Console API Reference</span></span>   

  

<span data-ttu-id="38e41-104">Verwenden Sie die API-Methoden für die Konsole, um Nachrichten aus Ihrem JavaScript in die Konsole zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="38e41-104">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="38e41-105">Eine interaktive Einführung in das Thema finden Sie unter [Erste Schritte mit der Protokollierung von Nachrichten in der Konsole][DevtoolsConsoleLog] .</span><span class="sxs-lookup"><span data-stu-id="38e41-105">See [Get Started With Logging Messages To The Console][DevtoolsConsoleLog] for an interactive introduction to the topic.</span></span>  <span data-ttu-id="38e41-106">Weitere Informationen finden Sie unter [Console Utilities API Reference] [DevtoolConsoleUtilities] , wenn Sie nach den Convenience-Methoden suchen, die `debug()` `monitorEvents()` nur über die Konsole verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="38e41-106">See [Console Utilities API Reference] [DevtoolConsoleUtilities] if you are looking for the convenience methods like `debug()` or `monitorEvents()` which are only available from the Console.</span></span>  

## <span data-ttu-id="38e41-107">kann</span><span class="sxs-lookup"><span data-stu-id="38e41-107">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="38e41-108">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="38e41-108">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="38e41-109">Schreibt einen [Fehler](#error) in die Konsole, wenn `expression` ausgewertet wird `false` .</span><span class="sxs-lookup"><span data-stu-id="38e41-109">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

> ##### <span data-ttu-id="38e41-110">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="38e41-110">Figure 1</span></span>  
> <span data-ttu-id="38e41-111">Das Ergebnis des `console.assert()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-111">The result of the `console.assert()` example</span></span>  
> ![Das Ergebnis des Console. Assert ()-Beispiels][ImageAssert]  

## <span data-ttu-id="38e41-113">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="38e41-113">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="38e41-114">Löscht die Konsole.</span><span class="sxs-lookup"><span data-stu-id="38e41-114">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="38e41-115">Wenn [Protokoll beibehalten][DevtoolsConsoleReferenceLevel] aktiviert ist, ist die [Clear](#clear) -Methode deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="38e41-115">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

<span data-ttu-id="38e41-116">Siehe auch: [Löschen der Konsole][DevtoolsConsoleReferenceClear]</span><span class="sxs-lookup"><span data-stu-id="38e41-116">See also: [Clear the Console][DevtoolsConsoleReferenceClear]</span></span>  

## <span data-ttu-id="38e41-117">Anzahl</span><span class="sxs-lookup"><span data-stu-id="38e41-117">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="38e41-118">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="38e41-118">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="38e41-119">Schreibt die Häufigkeit, mit der die [count](#count) -Methode in derselben Zeile und mit der gleichen aufgerufen wurde `label` .</span><span class="sxs-lookup"><span data-stu-id="38e41-119">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="38e41-120">Verwenden Sie die [countReset](#countreset) -Methode, um die Anzahl zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="38e41-120">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

> ##### <span data-ttu-id="38e41-121">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="38e41-121">Figure 2</span></span>  
> <span data-ttu-id="38e41-122">Das Ergebnis des `console.count()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-122">The result of the `console.count()` example</span></span>  
> ![Das Ergebnis des Console. Count ()-Beispiels][ImageCount]  

## <span data-ttu-id="38e41-124">countReset</span><span class="sxs-lookup"><span data-stu-id="38e41-124">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="38e41-125">Setzt die Anzahl zurück.</span><span class="sxs-lookup"><span data-stu-id="38e41-125">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

## <span data-ttu-id="38e41-126">debuggen</span><span class="sxs-lookup"><span data-stu-id="38e41-126">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="38e41-127">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="38e41-127">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="38e41-128">Identisch mit der [Log](#log) -Methode.</span><span class="sxs-lookup"><span data-stu-id="38e41-128">Identical to the [log](#log) method.</span></span>  

```javascript
console.debug('debug');  
```  

> ##### <span data-ttu-id="38e41-129">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="38e41-129">Figure 3</span></span>  
> <span data-ttu-id="38e41-130">Das Ergebnis des `console.debug()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-130">The result of the `console.debug()` example</span></span>  
> ![Das Ergebnis des Console. Debug ()-Beispiels][ImageDebug]  

## <span data-ttu-id="38e41-132">dir</span><span class="sxs-lookup"><span data-stu-id="38e41-132">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="38e41-133">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="38e41-133">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="38e41-134">Druckt eine JSON-Darstellung des angegebenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="38e41-134">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

> ##### <span data-ttu-id="38e41-135">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="38e41-135">Figure 4</span></span>  
> <span data-ttu-id="38e41-136">Das Ergebnis des `console.dir()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-136">The result of the `console.dir()` example</span></span>  
> ![Das Ergebnis des Console. dir ()-Beispiels][ImageDir]  

## <span data-ttu-id="38e41-138">DirXML</span><span class="sxs-lookup"><span data-stu-id="38e41-138">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="38e41-139">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="38e41-139">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="38e41-140">Druckt eine XML-Darstellung der untergeordneten Elemente von `node` .</span><span class="sxs-lookup"><span data-stu-id="38e41-140">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

> ##### <span data-ttu-id="38e41-141">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="38e41-141">Figure 5</span></span>  
> <span data-ttu-id="38e41-142">Das Ergebnis des `console.dirxml()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-142">The result of the `console.dirxml()` example</span></span>  
> ![Das Ergebnis des Console. DirXML ()-Beispiels][ImageDirXml]  

## <span data-ttu-id="38e41-144">Fehler</span><span class="sxs-lookup"><span data-stu-id="38e41-144">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="38e41-145">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="38e41-145">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="38e41-146">Druckt die `object` auf der Konsole, formatiert sie als Fehler und enthält eine Stapelüberwachung.</span><span class="sxs-lookup"><span data-stu-id="38e41-146">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

> ##### <span data-ttu-id="38e41-147">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="38e41-147">Figure 6</span></span>  
> <span data-ttu-id="38e41-148">Das Ergebnis des `console.error()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-148">The result of the `console.error()` example</span></span>  
> ![Das Ergebnis des Console. Error ()-Beispiels][ImageError]  

## <span data-ttu-id="38e41-150">Gruppe</span><span class="sxs-lookup"><span data-stu-id="38e41-150">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="38e41-151">Gruppiert Nachrichten visuell, bis die [groupEnd](#groupend) -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="38e41-151">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="38e41-152">Verwenden Sie die [groupCollapsed](#groupcollapsed) -Methode, um die Gruppe zu reduzieren, wenn Sie zuerst in der Konsole angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="38e41-152">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

> ##### <span data-ttu-id="38e41-153">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="38e41-153">Figure 7</span></span>  
> <span data-ttu-id="38e41-154">Das Ergebnis des `console.group()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-154">The result of the `console.group()` example</span></span>  
> ![Das Ergebnis des Console. Group ()-Beispiels][ImageGroup]  

## <span data-ttu-id="38e41-156">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="38e41-156">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="38e41-157">Identisch mit der [Log](#log) -Methode, mit der Ausnahme, dass die Gruppe anfänglich reduziert wird, wenn Sie in der Konsole protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="38e41-157">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

## <span data-ttu-id="38e41-158">groupEnd</span><span class="sxs-lookup"><span data-stu-id="38e41-158">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="38e41-159">Beendet die visuelle Gruppierung von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="38e41-159">Stops visually grouping messages.</span></span>  <span data-ttu-id="38e41-160">Sehen Sie sich die [Group](#group) -Methode an.</span><span class="sxs-lookup"><span data-stu-id="38e41-160">See the [group](#group) method.</span></span>  

## <span data-ttu-id="38e41-161">„Informationen”</span><span class="sxs-lookup"><span data-stu-id="38e41-161">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="38e41-162">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="38e41-162">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="38e41-163">Identisch mit der [Log](#log) -Methode.</span><span class="sxs-lookup"><span data-stu-id="38e41-163">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

> ##### <span data-ttu-id="38e41-164">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="38e41-164">Figure 8</span></span>  
> <span data-ttu-id="38e41-165">Das Ergebnis des `console.info()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-165">The result of the `console.info()` example</span></span>  
> ![Das Ergebnis des Console.info ()-Beispiels][ImageInfo]  

## <span data-ttu-id="38e41-167">Protokoll</span><span class="sxs-lookup"><span data-stu-id="38e41-167">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="38e41-168">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="38e41-168">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="38e41-169">Druckt eine Nachricht an die Konsole.</span><span class="sxs-lookup"><span data-stu-id="38e41-169">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

> ##### <span data-ttu-id="38e41-170">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="38e41-170">Figure 9</span></span>  
> <span data-ttu-id="38e41-171">Das Ergebnis des `console.log()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-171">The result of the `console.log()` example</span></span>  
> ![Das Ergebnis des Console. log ()-Beispiels][ImageLog]  

## <span data-ttu-id="38e41-173">Tabelle</span><span class="sxs-lookup"><span data-stu-id="38e41-173">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="38e41-174">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="38e41-174">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="38e41-175">Protokolliert ein Array von Objekten als Tabelle.</span><span class="sxs-lookup"><span data-stu-id="38e41-175">Logs an array of objects as a table.</span></span>  

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

> ##### <span data-ttu-id="38e41-176">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="38e41-176">Figure 10</span></span>  
> <span data-ttu-id="38e41-177">Das Ergebnis des `console.table()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-177">The result of the `console.table()` example</span></span>  
> ![Das Ergebnis des Console. Table ()-Beispiels][ImageTable]  

## <span data-ttu-id="38e41-179">time</span><span class="sxs-lookup"><span data-stu-id="38e41-179">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="38e41-180">Startet einen neuen Timer.</span><span class="sxs-lookup"><span data-stu-id="38e41-180">Starts a new timer.</span></span>  <span data-ttu-id="38e41-181">Verwenden Sie die [timeEnd](#timeend) -Methode, um den Zeitgeber zu beenden und die verstrichene Zeit auf der Konsole zu drucken.</span><span class="sxs-lookup"><span data-stu-id="38e41-181">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

> ##### <span data-ttu-id="38e41-182">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="38e41-182">Figure 11</span></span>  
> <span data-ttu-id="38e41-183">Das Ergebnis des `console.time()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-183">The result of the `console.time()` example</span></span>  
> ![Das Ergebnis des Console. time ()-Beispiels][ImageTime]  

## <span data-ttu-id="38e41-185">timeEnd</span><span class="sxs-lookup"><span data-stu-id="38e41-185">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="38e41-186">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="38e41-186">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="38e41-187">Stoppt einen Timer.</span><span class="sxs-lookup"><span data-stu-id="38e41-187">Stops a timer.</span></span>  <span data-ttu-id="38e41-188">Sehen Sie sich die [Zeit](#time) Methode an.</span><span class="sxs-lookup"><span data-stu-id="38e41-188">See the [time](#time) method.</span></span>  

## <span data-ttu-id="38e41-189">Trace</span><span class="sxs-lookup"><span data-stu-id="38e41-189">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="38e41-190">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="38e41-190">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="38e41-191">Druckt eine Stapelüberwachung auf der Konsole.</span><span class="sxs-lookup"><span data-stu-id="38e41-191">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

> ##### <span data-ttu-id="38e41-192">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="38e41-192">Figure 12</span></span>  
> <span data-ttu-id="38e41-193">Das Ergebnis des `console.trace()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-193">The result of the `console.trace()` example</span></span>  
> ![Das Ergebnis des Console. Trace ()-Beispiels][ImageTrace]  

## <span data-ttu-id="38e41-195">warnen</span><span class="sxs-lookup"><span data-stu-id="38e41-195">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="38e41-196">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="38e41-196">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="38e41-197">Druckt eine Warnung an die Konsole.</span><span class="sxs-lookup"><span data-stu-id="38e41-197">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

> ##### <span data-ttu-id="38e41-198">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="38e41-198">Figure 13</span></span>  
> <span data-ttu-id="38e41-199">Das Ergebnis des `console.warn()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="38e41-199">The result of the `console.warn()` example</span></span>  
> ![Das Ergebnis des Console. Warn ()-Beispiels][ImageWarn]  

   

  

<!-- image links -->  

[ImageAssert]: /microsoft-edge/devtools-guide-chromium/media/console-demo-assert-button.msft.png "Abbildung 1: das Ergebnis des Console. Assert ()-Beispiels"  
[ImageCount]: /microsoft-edge/devtools-guide-chromium/media/console-demo-count-button.msft.png "Abbildung 2: das Ergebnis des Console. Count ()-Beispiels"  
[ImageDebug]: /microsoft-edge/devtools-guide-chromium/media/console-demo-debug-button.msft.png "Abbildung 3: das Ergebnis des Console. Debug ()-Beispiels"  
[ImageDir]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dir-button.msft.png "Abbildung 4: das Ergebnis des Console. dir ()-Beispiels"  
[ImageDirXml]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dirxml-button.msft.png "Abbildung 5: das Ergebnis des Console. DirXML ()-Beispiels"  
[ImageError]: /microsoft-edge/devtools-guide-chromium/media/console-demo-error-button.msft.png "Abbildung 6: das Ergebnis des Console. Error ()-Beispiels"  
[ImageGroup]: /microsoft-edge/devtools-guide-chromium/media/console-demo-group-button.msft.png "Abbildung 7: das Ergebnis des Console. Group ()-Beispiels"  
[ImageInfo]: /microsoft-edge/devtools-guide-chromium/media/console-demo-info-button.msft.png "Abbildung 8: das Ergebnis des Console.info ()-Beispiels"  
[ImageLog]: /microsoft-edge/devtools-guide-chromium/media/console-demo-log-button.msft.png "Abbildung 9: das Ergebnis des Console. log ()-Beispiels"  
[ImageTable]: /microsoft-edge/devtools-guide-chromium/media/console-demo-table-button.msft.png "Abbildung 10: das Ergebnis des Console. Table ()-Beispiels"  
[ImageTime]: /microsoft-edge/devtools-guide-chromium/media/console-demo-time-button.msft.png "Abbildung 11: das Ergebnis des Console. time ()-Beispiels"  
[ImageTrace]: /microsoft-edge/devtools-guide-chromium/media/console-demo-trace-button.msft.png "Abbildung 12: das Ergebnis des Console. Trace ()-Beispiels"  
[ImageWarn]: /microsoft-edge/devtools-guide-chromium/media/console-demo-warn-button.msft.png "Abbildung 13: das Ergebnis des Console. Warn ()-Beispiels"  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Erste Schritte mit der Protokollierung von Nachrichten in der Konsole"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "API-Referenz für Konsolen Dienstprogramme"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Deaktivieren der Konsole-Konsolen Referenz"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Beibehalten von Nachrichten über Seitenlasten – Konsolen Referenz"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtern nach Protokollebene – Konsolen Referenz"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  

> [!NOTE]
> <span data-ttu-id="38e41-220">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38e41-220">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="38e41-221">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/api) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="38e41-221">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="38e41-223">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="38e41-223">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

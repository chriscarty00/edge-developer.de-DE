---
description: Verwenden Sie die Konsolen-API, um Nachrichten in die Konsole zu schreiben.
title: Konsolen-API-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 54b89e25501449a1e5119afa812a0535fbc6ffbb
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483254"
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
# <a name="console-api-reference"></a><span data-ttu-id="8fe73-104">Konsolen-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="8fe73-104">Console API reference</span></span>  

<span data-ttu-id="8fe73-105">Das **Konsolentool** ist hilfreich, wenn Sie mehrere Aufgaben in devTools ausführen.</span><span class="sxs-lookup"><span data-stu-id="8fe73-105">The **Console** tool is helpful when you complete multiple tasks in the DevTools.</span></span>  <span data-ttu-id="8fe73-106">APIs stehen in Ihren Skripts zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8fe73-106">APIs are available to include in your scripts.</span></span> <span data-ttu-id="8fe73-107">Convenience-Methoden sind nur für \*\*\*\* die Verwendung im Konsolentool verfügbar, z. B. für `debug()` die `monitorEvents()` und-Methoden.</span><span class="sxs-lookup"><span data-stu-id="8fe73-107">Convenience methods are only available for use in the **Console** tool, such as the `debug()` and `monitorEvents()` methods.</span></span>  <span data-ttu-id="8fe73-108">Weitere Informationen zum Einstieg \*\*\*\* in die Konsole finden Sie unter Erste Schritte mit der [Protokollierung von Nachrichten an der Konsole.][DevtoolsConsoleConsoleLog]</span><span class="sxs-lookup"><span data-stu-id="8fe73-108">For more information on getting started with the **Console**, navigate to [Get started with logging messages to the Console][DevtoolsConsoleConsoleLog].</span></span>  <span data-ttu-id="8fe73-109">Weitere Informationen zu den Komfortmethoden in der **Konsole finden**Sie unter [Console Utilities API Reference][DevtoolConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="8fe73-109">For more information on the convenience methods in the **Console**, navigate to [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <a name="assert"></a><span data-ttu-id="8fe73-110">assert</span><span class="sxs-lookup"><span data-stu-id="8fe73-110">assert</span></span>  

<span data-ttu-id="8fe73-111">Diese Methode schreibt einen [Fehler in](#error) die **Konsole,** wenn `expression` sie in ausgewertet `false` wird.</span><span class="sxs-lookup"><span data-stu-id="8fe73-111">This method writes an [error](#error) to the **Console** when `expression` evaluates to `false`.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-112">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-112">JavaScript syntax</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="8fe73-113">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="8fe73-113">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-114">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-114">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-115">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-115">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const x = 5;
      const y = 3;
      const reason = 'x is expected to be less than y';
      console.assert(x < y, {x, y, reason});
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-116">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-116">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Das Ergebnis des Beispiels console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
         <span data-ttu-id="8fe73-118">Das Ergebnis des `console.assert()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-118">The result of the `console.assert()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="clear"></a><span data-ttu-id="8fe73-119">clear</span><span class="sxs-lookup"><span data-stu-id="8fe73-119">clear</span></span>  

<span data-ttu-id="8fe73-120">Mit dieser Methode wird die **Konsole geräumt.**</span><span class="sxs-lookup"><span data-stu-id="8fe73-120">This method clears the **Console**.</span></span>  

<span data-ttu-id="8fe73-121">Wenn [Das Protokoll beibehalten][DevtoolsConsoleReferenceFilter] aktiviert ist, ist die [clear-Methode](#clear) deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8fe73-121">If [Preserve Log][DevtoolsConsoleReferenceFilter] is turned on, the [clear](#clear) method is turned off.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-122">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-122">JavaScript syntax</span></span>  

```javascript
console.clear()
```

### <a name="javascript-example"></a><span data-ttu-id="8fe73-123">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-123">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-124">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-124">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.clear();  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-125">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-125">Output</span></span>
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

### <a name="see-also"></a><span data-ttu-id="8fe73-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8fe73-126">See also</span></span>  

*   [<span data-ttu-id="8fe73-127">Löschen der Konsole</span><span class="sxs-lookup"><span data-stu-id="8fe73-127">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a><span data-ttu-id="8fe73-128">count</span><span class="sxs-lookup"><span data-stu-id="8fe73-128">count</span></span>  

<span data-ttu-id="8fe73-129">Diese Methode schreibt die Anzahl der Aufrufe der [Count-Methode](#count) in derselben Zeile und mit derselben `label` .</span><span class="sxs-lookup"><span data-stu-id="8fe73-129">This method writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="8fe73-130">Verwenden Sie die [countReset-Methode,](#countreset) um die Anzahl zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="8fe73-130">Use the [countReset](#countreset) method to reset the count.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-131">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-131">JavaScript syntax</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="8fe73-132">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="8fe73-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-133">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-133">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-134">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.count();
      console.count('coffee');
      console.count();
      console.count();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-135">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-135">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Das Ergebnis des Beispiels console.count()" lightbox="../media/console-demo-count-button.msft.png":::
         <span data-ttu-id="8fe73-137">Das Ergebnis des `console.count()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-137">The result of the `console.count()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="countreset"></a><span data-ttu-id="8fe73-138">countReset</span><span class="sxs-lookup"><span data-stu-id="8fe73-138">countReset</span></span>  

<span data-ttu-id="8fe73-139">Mit dieser Methode wird eine Anzahl zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="8fe73-139">This method resets a count.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-140">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-140">JavaScript syntax</span></span>  

```javascript
console.countReset([label])
```  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-141">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-141">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-142">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-142">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.countReset();
      console.countReset('coffee');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-143">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-143">Output</span></span>
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

---  

## <a name="debug"></a><span data-ttu-id="8fe73-144">debuggen</span><span class="sxs-lookup"><span data-stu-id="8fe73-144">debug</span></span>  

<span data-ttu-id="8fe73-145">Diese Methode ist mit der [Protokollmethode identisch,](#log) mit Ausnahme der unterschiedlichen Protokollebene.</span><span class="sxs-lookup"><span data-stu-id="8fe73-145">This method is identical to the [log](#log) method, except different log level.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-146">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-146">JavaScript syntax</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="8fe73-147">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="8fe73-147">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-148">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-148">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-149">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-149">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.debug('debug');  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-150">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-150">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Das Ergebnis des Beispiels console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
         <span data-ttu-id="8fe73-152">Das Ergebnis des `console.debug()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-152">The result of the `console.debug()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dir"></a><span data-ttu-id="8fe73-153">dir</span><span class="sxs-lookup"><span data-stu-id="8fe73-153">dir</span></span>  

<span data-ttu-id="8fe73-154">Diese Methode druckt eine JSON-Darstellung des angegebenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="8fe73-154">This method prints a JSON representation of the specified object.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-155">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-155">JavaScript syntax</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="8fe73-156">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="8fe73-156">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-157">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-157">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-158">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dir(document.head);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-159">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-159">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Das Ergebnis des Beispiels console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
         <span data-ttu-id="8fe73-161">Das Ergebnis des `console.dir()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-161">The result of the `console.dir()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dirxml"></a><span data-ttu-id="8fe73-162">dirxml</span><span class="sxs-lookup"><span data-stu-id="8fe73-162">dirxml</span></span>  

<span data-ttu-id="8fe73-163">Diese Methode druckt eine XML-Darstellung der untergeordneten Elemente von `node` aus.</span><span class="sxs-lookup"><span data-stu-id="8fe73-163">This method prints an XML representation of the descendants of `node`.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-164">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-164">JavaScript syntax</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="8fe73-165">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="8fe73-165">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-166">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-166">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-167">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-167">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dirxml(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-168">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-168">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Das Ergebnis des Console.dirxml()-Beispiels" lightbox="../media/console-demo-dirxml-button.msft.png":::
         <span data-ttu-id="8fe73-170">Das Ergebnis des `console.dirxml()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-170">The result of the `console.dirxml()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="error"></a><span data-ttu-id="8fe73-171">Fehler</span><span class="sxs-lookup"><span data-stu-id="8fe73-171">error</span></span>  

<span data-ttu-id="8fe73-172">Diese Methode druckt `object` die in die **Konsole,** formatiert sie als Fehler und enthält eine Stapelverfolgung.</span><span class="sxs-lookup"><span data-stu-id="8fe73-172">This method prints the `object` to the **Console**, formats it as an error, and includes a stack trace.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-173">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-173">JavaScript syntax</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="8fe73-174">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="8fe73-174">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-175">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-175">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-176">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-177">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-177">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Das Ergebnis des Beispiels console.error()" lightbox="../media/console-demo-error-button.msft.png":::
         <span data-ttu-id="8fe73-179">Das Ergebnis des `console.error()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-179">The result of the `console.error()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="group"></a><span data-ttu-id="8fe73-180">Gruppe</span><span class="sxs-lookup"><span data-stu-id="8fe73-180">group</span></span>  

<span data-ttu-id="8fe73-181">Diese Methode gruppieren Nachrichten visuell, bis [die groupEnd-Methode](#groupend) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fe73-181">This method visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="8fe73-182">Verwenden Sie die [groupCollapsed-Methode,](#groupcollapsed) um die Gruppe zu reduzieren, wenn sie sich zunächst bei der Konsole **anmeldet.**</span><span class="sxs-lookup"><span data-stu-id="8fe73-182">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it initially logs to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-183">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-183">JavaScript syntax</span></span>  

```javascript
console.group(label)
```  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-184">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-184">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-185">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const label = 'Adolescent Irradiated Espionage Tortoises';
      console.group(label);
      console.info('Leo');
      console.info('Mike');
      console.info('Don');
      console.info('Raph');
      console.groupEnd(label);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-186">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-186">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Das Ergebnis des Beispiels console.group()" lightbox="../media/console-demo-group-button.msft.png":::
         <span data-ttu-id="8fe73-188">Das Ergebnis des `console.group()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-188">The result of the `console.group()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="groupcollapsed"></a><span data-ttu-id="8fe73-189">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="8fe73-189">groupCollapsed</span></span>  

<span data-ttu-id="8fe73-190">Diese Methode ist identisch mit der [Protokollmethode,](#log) mit der Ausnahme, dass die Gruppe anfänglich reduziert wird, wenn sie sich bei der Konsole **anmeldet.**</span><span class="sxs-lookup"><span data-stu-id="8fe73-190">This method is identical to the [log](#log) method, except the group is initially collapsed when it logs to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-191">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-191">JavaScript syntax</span></span>  

```javascript
console.groupCollapsed(label)
```  

---  

## <a name="groupend"></a><span data-ttu-id="8fe73-192">groupEnd</span><span class="sxs-lookup"><span data-stu-id="8fe73-192">groupEnd</span></span>  

<span data-ttu-id="8fe73-193">Diese Methode beendet das visuelle Gruppieren von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="8fe73-193">This method stops visually grouping messages.</span></span>  <span data-ttu-id="8fe73-194">Navigieren Sie zur [Gruppenmethode.](#group)</span><span class="sxs-lookup"><span data-stu-id="8fe73-194">Navigate to the [group](#group) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-195">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-195">JavaScript syntax</span></span>  

```javascript
console.groupEnd(label)
```  

---  

## <a name="info"></a><span data-ttu-id="8fe73-196">Info</span><span class="sxs-lookup"><span data-stu-id="8fe73-196">info</span></span>  

<span data-ttu-id="8fe73-197">Diese Methode ist identisch mit der [Protokollmethode.](#log)</span><span class="sxs-lookup"><span data-stu-id="8fe73-197">This method is identical to the [log](#log) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-198">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-198">JavaScript syntax</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="8fe73-199">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="8fe73-199">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-200">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-200">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-201">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.info('info');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-202">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-202">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Das Ergebnis des beispiels console.info()" lightbox="../media/console-demo-info-button.msft.png":::
         <span data-ttu-id="8fe73-204">Das Ergebnis des `console.info()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-204">The result of the `console.info()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="log"></a><span data-ttu-id="8fe73-205">log</span><span class="sxs-lookup"><span data-stu-id="8fe73-205">log</span></span>  

<span data-ttu-id="8fe73-206">Diese Methode druckt eine Nachricht an die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="8fe73-206">This method prints a message to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-207">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-207">JavaScript syntax</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="8fe73-208">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="8fe73-208">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-209">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-209">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-210">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-210">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.log('log');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-211">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-211">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Das Ergebnis des Beispiels console.log()" lightbox="../media/console-demo-log-button.msft.png":::
         <span data-ttu-id="8fe73-213">Das Ergebnis des `console.log()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-213">The result of the `console.log()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="8fe73-214">Tabelle</span><span class="sxs-lookup"><span data-stu-id="8fe73-214">table</span></span>  

<span data-ttu-id="8fe73-215">Diese Methode protokolliert ein Array von Objekten als Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8fe73-215">This method logs an array of objects as a table.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-216">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-216">JavaScript syntax</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="8fe73-217">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="8fe73-217">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-218">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-218">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-219">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-219">Input</span></span>  
   :::column-end:::
   :::column span="3":::
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
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-220">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-220">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Das Ergebnis des Beispiels console.table()" lightbox="../media/console-demo-table-button.msft.png":::
         <span data-ttu-id="8fe73-222">Das Ergebnis des `console.table()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-222">The result of the `console.table()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="time"></a><span data-ttu-id="8fe73-223">time</span><span class="sxs-lookup"><span data-stu-id="8fe73-223">time</span></span>  

<span data-ttu-id="8fe73-224">Diese Methode startet einen neuen Timer.</span><span class="sxs-lookup"><span data-stu-id="8fe73-224">This method starts a new timer.</span></span>  <span data-ttu-id="8fe73-225">Verwenden Sie die [timeEnd-Methode,](#timeend) um den Timer zu beenden und die verstrichene Zeit in der Konsole **zu drucken.**</span><span class="sxs-lookup"><span data-stu-id="8fe73-225">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-226">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-226">JavaScript syntax</span></span>  

```javascript
console.time([label])
```  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-227">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-227">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-228">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.time();
      for (var i = 0; i < 100000; i++) {
          let square = i ** 2;
      }
      console.timeEnd();
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-229">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-229">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Das Ergebnis des Beispiels console.time()" lightbox="../media/console-demo-time-button.msft.png":::
         <span data-ttu-id="8fe73-231">Das Ergebnis des `console.time()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-231">The result of the `console.time()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="timeend"></a><span data-ttu-id="8fe73-232">timeEnd</span><span class="sxs-lookup"><span data-stu-id="8fe73-232">timeEnd</span></span>  

<span data-ttu-id="8fe73-233">Mit dieser Methode wird ein Timer angehalten.</span><span class="sxs-lookup"><span data-stu-id="8fe73-233">This method stops a timer.</span></span>  <span data-ttu-id="8fe73-234">Weitere Informationen finden Sie in der [Time-Methode.](#time)</span><span class="sxs-lookup"><span data-stu-id="8fe73-234">For more information, navigate to the [time](#time) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-235">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-235">JavaScript syntax</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="8fe73-236">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="8fe73-236">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

---  

## <a name="trace"></a><span data-ttu-id="8fe73-237">trace</span><span class="sxs-lookup"><span data-stu-id="8fe73-237">trace</span></span>  

<span data-ttu-id="8fe73-238">Diese Methode druckt eine Stapelverfolgung an die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="8fe73-238">This method prints a stack trace to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-239">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-239">JavaScript syntax</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="8fe73-240">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="8fe73-240">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-241">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-241">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-242">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-242">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const first = () => { second(); };
      const second = () => { third(); };
      const third = () => { fourth(); };
      const fourth = () => { console.trace(); };
      first();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-243">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-243">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Das Ergebnis des Beispiels console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
         <span data-ttu-id="8fe73-245">Das Ergebnis des `console.trace()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-245">The result of the `console.trace()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="warn"></a><span data-ttu-id="8fe73-246">warnen</span><span class="sxs-lookup"><span data-stu-id="8fe73-246">warn</span></span>  

<span data-ttu-id="8fe73-247">Diese Methode druckt eine Warnung an die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="8fe73-247">This method prints a warning to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="8fe73-248">#A0</span><span class="sxs-lookup"><span data-stu-id="8fe73-248">JavaScript syntax</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="8fe73-249">[Protokollebene][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="8fe73-249">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

### <a name="javascript-example"></a><span data-ttu-id="8fe73-250">JavaScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fe73-250">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-251">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.warn('warn');
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="8fe73-252">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8fe73-252">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Das Ergebnis des Console.warn()-Beispiels" lightbox="../media/console-demo-warn-button.msft.png":::
         <span data-ttu-id="8fe73-254">Das Ergebnis des `console.warn()` Beispiels</span><span class="sxs-lookup"><span data-stu-id="8fe73-254">The result of the `console.warn()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8fe73-255">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="8fe73-255">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleLog]: ./console-log.md "Protokolle im Konsolentool | Microsoft Docs"  
[DevtoolConsoleUtilities]: ./utilities.md "Console Utilities API reference | Microsoft Docs"  
[DevtoolsConsoleReferenceClear]: ./reference.md#clear-the-console "Löschen der Konsole – Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleReferenceFilter]: ./reference.md#filter-by-log-level "Filtern nach Protokollebene – Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleReferencePersist]: ./reference.md#persist-messages-across-page-loads "Nachrichten über Seitenlasten hinweg beibehalten – Konsolenreferenz | Microsoft Docs"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chromium) Developer Tools (Übersicht) | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="8fe73-262">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fe73-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8fe73-263">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/api) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="8fe73-263">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="8fe73-265">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8fe73-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

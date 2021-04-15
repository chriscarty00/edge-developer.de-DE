---
description: Ein Verweis auf Komfortbefehle, die in der Microsoft Edge DevTools-Konsole verfügbar sind.
title: API-Referenz zu Konsolen-Dienstprogrammen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: c6a0356bd590809f9164aa62fd42156f901cef0f
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483282"
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
# <a name="console-utilities-api-reference"></a><span data-ttu-id="95832-104">API-Referenz zu Konsolen-Dienstprogrammen</span><span class="sxs-lookup"><span data-stu-id="95832-104">Console Utilities API reference</span></span>  

<span data-ttu-id="95832-105">Die Console Utilities-API enthält eine Auflistung von Komfortbefehlen, um die folgenden allgemeinen Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="95832-105">The Console Utilities API contains a collection of convenience commands to complete the following common tasks.</span></span>  

*   <span data-ttu-id="95832-106">Auswählen und Überprüfen von DOM-Elementen</span><span class="sxs-lookup"><span data-stu-id="95832-106">Choose and inspect DOM elements</span></span>  
*   <span data-ttu-id="95832-107">Anzeigen von Daten im lesbaren Format</span><span class="sxs-lookup"><span data-stu-id="95832-107">Display data in readable format</span></span>  
*   <span data-ttu-id="95832-108">Beenden und Starten des Profilers</span><span class="sxs-lookup"><span data-stu-id="95832-108">Stop and start the profiler</span></span>  
*   <span data-ttu-id="95832-109">Überwachen von DOM-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="95832-109">Monitor DOM events</span></span>  
    
> [!WARNING]
> <span data-ttu-id="95832-110">Die folgenden Befehle funktionieren nur in der Microsoft Edge **DevTools-Konsole.**</span><span class="sxs-lookup"><span data-stu-id="95832-110">The following commands only work in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="95832-111">Die Befehle funktionieren nicht, wenn sie aus Ihren Skripts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95832-111">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="95832-112">Weitere Informationen zu den `console.log()` und-Methoden und den restlichen Methoden finden `console.error()` Sie unter Console API `console.*` [Reference][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="95832-112">For more information about the `console.log()` and `console.error()` methods and the rest of the `console.*` methods, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  

## <a name="recently-evaluated-expression"></a><span data-ttu-id="95832-113">Kürzlich ausgewerteter Ausdruck</span><span class="sxs-lookup"><span data-stu-id="95832-113">Recently evaluated expression</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-114">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-114">Console syntax</span></span>  

```console
$_
```  

<span data-ttu-id="95832-115">Dieser Befehl gibt den Wert des zuletzt ausgewerteten Ausdrucks zurück.</span><span class="sxs-lookup"><span data-stu-id="95832-115">This command returns the value of the most recently evaluated expression.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-116">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-116">Console example</span></span>  

<span data-ttu-id="95832-117">In der folgenden Abbildung wird ein einfacher Ausdruck \( `2 + 2` \) ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="95832-117">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="95832-118">Die `$_` Eigenschaft wird dann ausgewertet, die denselben Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="95832-118">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-arithmatic.msft.png":::
   `$_` <span data-ttu-id="95832-120">ist der zuletzt ausgewertete Ausdruck</span><span class="sxs-lookup"><span data-stu-id="95832-120">is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="95832-121">In der folgenden Abbildung enthält der ausgewertete Ausdruck zunächst ein Array von Namen.</span><span class="sxs-lookup"><span data-stu-id="95832-121">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="95832-122">Auswerten, um die Länge des Arrays zu finden, wird der in gespeicherte Wert `$_.length` `$_` zum neuesten ausgewerteten Ausdruck, `4` .</span><span class="sxs-lookup"><span data-stu-id="95832-122">Evaluating `$_.length` to find the length of the array, the value stored in `$_` becomes the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ ändert sich, wenn neue Befehle ausgewertet werden" lightbox="../media/console-array-length.msft.png":::
   `$_` <span data-ttu-id="95832-124">Änderungen bei der Auswertung neuer Befehle</span><span class="sxs-lookup"><span data-stu-id="95832-124">changes when new commands are evaluated</span></span>  
:::image-end:::  

---  

## <a name="recently-chosen-element-or-javascript-object"></a><span data-ttu-id="95832-125">Zuletzt ausgewähltes Element oder JavaScript-Objekt</span><span class="sxs-lookup"><span data-stu-id="95832-125">Recently chosen element or JavaScript object</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-126">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-126">Console syntax</span></span>  

```console
$0
```  

<span data-ttu-id="95832-127">Dieser Befehl gibt das zuletzt ausgewählte Element oder JavaScript-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="95832-127">This command returns the most recently chosen element or JavaScript object.</span></span>  `$1` <span data-ttu-id="95832-128">gibt die zuletzt ausgewählte zweite zurück, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="95832-128">returns the second most recently chosen one, and so on.</span></span>  <span data-ttu-id="95832-129">Die Befehle , , , und funktionieren als verlaufshistorische Referenz zu den letzten fünf DOM-Elementen, die im Elementtool oder den letzten fünf im Speichertool ausgewählten `$0` `$1` `$2` `$3` `$4` JavaScript-Heapobjekten überprüft wurden. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="95832-129">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** tool or the last five JavaScript heap objects chosen in the **Memory** tool.</span></span>  

:::row:::
   :::column span="1":::
      ```console
      $0
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $1
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $2
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ```console
      $3
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $4
      ```  
   :::column-end:::
   :::column span="1":::
      &nbsp;
   :::column-end:::
:::row-end:::  

### <a name="console-example"></a><span data-ttu-id="95832-130">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-130">Console example</span></span>  

<span data-ttu-id="95832-131">In der folgenden Abbildung wird `img` ein Element im **Elementtool ausgewählt.**</span><span class="sxs-lookup"><span data-stu-id="95832-131">In the following figure, an `img` element is chosen in the **Elements** tool.</span></span>  <span data-ttu-id="95832-132">In der **Konsolenschube** `$0` wurde ausgewertet und zeigt dasselbe Element an.</span><span class="sxs-lookup"><span data-stu-id="95832-132">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Die $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="95832-134">Der</span><span class="sxs-lookup"><span data-stu-id="95832-134">The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="95832-135">In der folgenden Abbildung zeigt das Bild ein anderes Element an, das auf derselben Webseite ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="95832-135">In the following figure, the image displays a different element chosen in the same webpage.</span></span>  <span data-ttu-id="95832-136">The `$0` bezieht sich nun auf das neu ausgewählte Element, während das zuvor ausgewählte Element zurückgegeben `$1` wird.</span><span class="sxs-lookup"><span data-stu-id="95832-136">The `$0` now refers to the newly chosen element, while `$1` returns the previously chosen one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="Die $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="95832-138">Der</span><span class="sxs-lookup"><span data-stu-id="95832-138">The</span></span> `$1`  
:::image-end:::  

---  

## <a name="query-selector"></a><span data-ttu-id="95832-139">Abfrageauswahl</span><span class="sxs-lookup"><span data-stu-id="95832-139">Query selector</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-140">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-140">Console syntax</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="95832-141">Dieser Befehl gibt den Verweis auf das erste DOM-Element mit dem angegebenen CSS-Selektor zurück.</span><span class="sxs-lookup"><span data-stu-id="95832-141">This command returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="95832-142">Diese Methode ist ein Alias für die [document.querySelector()-Methode.][MdnDocsWebApiDocumentQueryselector]</span><span class="sxs-lookup"><span data-stu-id="95832-142">This method is an alias for the [document.querySelector()][MdnDocsWebApiDocumentQueryselector] method.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-143">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-143">Console example</span></span>  

<span data-ttu-id="95832-144">In der folgenden Abbildung wird ein Verweis auf das erste `<img>` Element auf der Webseite zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="95832-144">In the following figure, a reference to the first `<img>` element in the webpage is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="95832-146">Der</span><span class="sxs-lookup"><span data-stu-id="95832-146">The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="95832-147">Führen Sie die folgenden Aktionen aus, um das erste Element im DOM zu finden oder es auf der Webseite zu finden und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="95832-147">To find the first element in the DOM or to find and display it on the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="95832-148">Zeigen Sie auf das zurückgegebene Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="95832-148">Hover on the returned result.</span></span>  
1.  <span data-ttu-id="95832-149">Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).</span><span class="sxs-lookup"><span data-stu-id="95832-149">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="95832-150">Wählen Sie **Einblenden im Elementbereich aus.**</span><span class="sxs-lookup"><span data-stu-id="95832-150">Choose **Reveal in Elements Panel**.</span></span>  

<span data-ttu-id="95832-151">In der folgenden Abbildung wird ein Verweis auf das aktuell ausgewählte Element zurückgegeben, und die `src` Eigenschaft wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95832-151">In the following figure, a reference to the currently chosen element is returned and the `src` property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="95832-153">Der</span><span class="sxs-lookup"><span data-stu-id="95832-153">The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="95832-154">Diese Methode unterstützt auch einen zweiten Parameter, , der ein Element oder einen Knoten angibt, von dem aus `startNode` nach Elementen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="95832-154">This method also supports a second parameter, `startNode`, that specifies an element or node from which to search for elements.</span></span>  <span data-ttu-id="95832-155">Der Standardwert des Parameters ist `document` .</span><span class="sxs-lookup"><span data-stu-id="95832-155">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="95832-156">In der folgenden Abbildung wird das erste Element, nachdem das Element gefunden wurde, und die Eigenschaft des `img` `title--image` Elements `src` `img` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="95832-156">In the following figure, the first `img` element after the `title--image` element is found, and the `src` property of the `img` element is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="The $('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="95832-158">Der</span><span class="sxs-lookup"><span data-stu-id="95832-158">The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="95832-159">Wenn Sie eine Bibliothek wie jQuery verwenden, die verwendet, wird die Funktionalität überschrieben und entspricht der Implementierung `$` `$` aus dieser Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="95832-159">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

---  

## <a name="query-selector-all"></a><span data-ttu-id="95832-160">Abfrageauswahl alle</span><span class="sxs-lookup"><span data-stu-id="95832-160">Query selector all</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-161">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-161">Console syntax</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="95832-162">Dieser Befehl gibt ein Array von Elementen zurück, die mit dem angegebenen CSS-Selektor übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95832-162">This command returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="95832-163">Diese Methode entspricht dem Ausführen der [document.querySelectorAll()-Methode.][MdnDocsWebApiDocumentQueryselectorall]</span><span class="sxs-lookup"><span data-stu-id="95832-163">This method is equivalent to running the [document.querySelectorAll()][MdnDocsWebApiDocumentQueryselectorall] method.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-164">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-164">Console example</span></span>  

<span data-ttu-id="95832-165">Verwenden Sie im folgenden Codebeispiel und der folgenden Abbildung, um ein Array aller Elemente auf der aktuellen Webseite zu erstellen und den Wert der Eigenschaft `$$()` `<img>` für jedes Element `src` anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="95832-165">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current webpage and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Verwenden von $$() zum Auswählen aller Bilder auf der Webseite und Anzeigen der Quellen" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="95832-167">Verwenden, `$$()` um alle Bilder auf der Webseite zu wählen und die Quellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="95832-167">Using `$$()` to choose all images in the webpage and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="95832-168">Diese Methode unterstützt auch einen zweiten Parameter, , der ein Element oder einen Knoten angibt, von dem aus `startNode` nach Elementen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="95832-168">This method also supports a second parameter, `startNode`, that specifies an element or node from which to search for elements.</span></span>  <span data-ttu-id="95832-169">Der Standardwert des Parameters ist `document` .</span><span class="sxs-lookup"><span data-stu-id="95832-169">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="95832-170">Im folgenden Codebeispiel und der folgenden Abbildung wird eine geänderte Version des vorherigen Codebeispiels und der abbildung verwendet, um ein Array aller Elemente zu erstellen, die auf der aktuellen Webseite nach dem ausgewählten `$$()` `<img>` Knoten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="95832-170">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current webpage after the chosen node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Verwenden von $$(), um alle Bilder zu wählen, die nach dem angegebenen <div->-Element auf der Webseite angezeigt werden, und die Quellen anzuzeigen" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="95832-172">Verwenden, um alle Bilder zu wählen, die nach dem angegebenen Element auf der Webseite angezeigt `$$()` `<div>` werden, und die Quellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="95832-172">Using `$$()` to choose all images that appear after the specified `<div>` element in the webpage and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="95832-173">Wählen `Shift` + `Enter` Sie in **der Konsole** aus, um eine neue Zeile zu starten, ohne das Skript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="95832-173">Select `Shift`+`Enter` in the **Console** to start a new line without running the script.</span></span>  

---  

## <a name="xpath"></a><span data-ttu-id="95832-174">XPath</span><span class="sxs-lookup"><span data-stu-id="95832-174">XPath</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-175">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-175">Console syntax</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="95832-176">Dieser Befehl gibt ein Array von DOM-Elementen zurück, die mit dem angegebenen XPath-Ausdruck übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95832-176">This command returns an array of DOM elements that match the specified XPath expression.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-177">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-177">Console example</span></span>  

<span data-ttu-id="95832-178">Im folgenden Codebeispiel und der folgenden Abbildung werden alle Elemente auf der Webseite `<p>` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="95832-178">In the following code sample and figure, all of the `<p>` elements on the webpage are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Verwenden eines XPath-Selektors" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="95832-180">Verwenden eines XPath-Selektors</span><span class="sxs-lookup"><span data-stu-id="95832-180">Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="95832-181">Im folgenden Codebeispiel und der folgenden Abbildung werden alle Elemente zurückgegeben, die Elemente `<p>` `<a>` enthalten.</span><span class="sxs-lookup"><span data-stu-id="95832-181">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Verwenden eines komplizierteren XPath-Selektors" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="95832-183">Verwenden eines komplizierteren XPath-Selektors</span><span class="sxs-lookup"><span data-stu-id="95832-183">Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="95832-184">Ähnlich wie die anderen Selektorbefehle hat einen optionalen zweiten Parameter, der ein Element oder einen Knoten angibt, von dem aus `$x(path)` nach Elementen gesucht werden `startNode` soll.</span><span class="sxs-lookup"><span data-stu-id="95832-184">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Verwenden eines XPath-Selektors mit startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="95832-186">Verwenden eines XPath-Selektors mit</span><span class="sxs-lookup"><span data-stu-id="95832-186">Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

---  

## <a name="clear"></a><span data-ttu-id="95832-187">clear</span><span class="sxs-lookup"><span data-stu-id="95832-187">clear</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-188">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-188">Console syntax</span></span>  

```console
clear()
```  

<span data-ttu-id="95832-189">Mit diesem Kommmnad wird die Konsole des Verlaufs geräumt.</span><span class="sxs-lookup"><span data-stu-id="95832-189">This commnad clears the console of the history.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-190">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-190">Console example</span></span>  

```console
clear()
```  

## <a name="copy"></a><span data-ttu-id="95832-191">copy</span><span class="sxs-lookup"><span data-stu-id="95832-191">copy</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-192">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-192">Console syntax</span></span>  

```console
copy(object)
```  

<span data-ttu-id="95832-193">Diese Methode kopiert eine Zeichenfolgendarstellung des angegebenen Objekts in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="95832-193">This method copies a string representation of the specified object to the clipboard.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-194">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-194">Console example</span></span>  

```console
copy($0)
```  

---  

## <a name="debug"></a><span data-ttu-id="95832-195">debuggen</span><span class="sxs-lookup"><span data-stu-id="95832-195">debug</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-196">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-196">Console syntax</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="95832-197">Das [#A0 #1050237][CR1050237] verfolgt einen Fehler mit der `debug()` Funktion.</span><span class="sxs-lookup"><span data-stu-id="95832-197">The [Chromium issue #1050237][CR1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="95832-198">Wenn das Problem auftreten sollte, versuchen Sie stattdessen, [Haltepunkte zu][DevtoolsJavascriptBreakpoints] verwenden.</span><span class="sxs-lookup"><span data-stu-id="95832-198">If you encounter the issue, try using [breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="95832-199">Wenn Sie die angegebene Methode anfordern, ruft der Debugger die Methode im Tool Sources auf und bricht **sie** auf.</span><span class="sxs-lookup"><span data-stu-id="95832-199">When you request the specified method, the debugger invokes and breaks inside the method on the **Sources** tool.</span></span>  <span data-ttu-id="95832-200">Sie können den Code schrittweise ausführen und debuggen.</span><span class="sxs-lookup"><span data-stu-id="95832-200">It allows you to step through and debug the code.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-201">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-201">Console example</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Durchbrechen einer Methode mit debug()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="95832-203">Durchbrechen einer Methode mit</span><span class="sxs-lookup"><span data-stu-id="95832-203">Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="95832-204">Verwenden Sie diese Methode, um die Unterbrechung der Methode zu beenden, oder verwenden Sie `undebug(method)` die Benutzeroberfläche, um alle Haltepunkte zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="95832-204">Use `undebug(method)` to stop breaking on the method, or use the UI to turn off all breakpoints.</span></span>  

<span data-ttu-id="95832-205">Weitere Informationen zu Haltepunkten finden Sie unter [How to pause your code with breakpoints in Microsoft Edge DevTools][DevtoolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="95832-205">For more information on breakpoints, navigate to [How to pause your code with breakpoints in Microsoft Edge DevTools][DevtoolsJavascriptBreakpoints].</span></span>  

---  

## <a name="dir"></a><span data-ttu-id="95832-206">dir</span><span class="sxs-lookup"><span data-stu-id="95832-206">dir</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-207">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-207">Console syntax</span></span>  

```console
dir(object)
```  

<span data-ttu-id="95832-208">Dieser Befehl zeigt eine Objektformatliste aller Eigenschaften für das angegebene Objekt an.</span><span class="sxs-lookup"><span data-stu-id="95832-208">This command displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="95832-209">Diese Methode ist ein Alias für die [console.dir()-Methode.][MdnDocsWebApiConsoleDir]</span><span class="sxs-lookup"><span data-stu-id="95832-209">This method is an alias for the [console.dir()][MdnDocsWebApiConsoleDir] method.</span></span>  

<span data-ttu-id="95832-210">Werten `document.head` Sie in der Konsole **aus,** um den HTML-Code zwischen den tags `<head>` und zu `</head>` anzeigen.</span><span class="sxs-lookup"><span data-stu-id="95832-210">Evaluate `document.head` in the **Console** to display the HTML between the `<head>` and `</head>` tags.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-211">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-211">Console example</span></span>  

<span data-ttu-id="95832-212">Im folgenden Codebeispiel und der folgenden Abbildung wird nach verwendung in der Konsole ein Objektstileintrag `console.dir()` **angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="95832-212">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the **Console**.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Protokollierung von document.head mit dir()-Methode" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="95832-214">Protokollierung `document.head` mit `dir()` Methode</span><span class="sxs-lookup"><span data-stu-id="95832-214">Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="95832-215">Weitere Informationen finden Sie unter [console.dir()][DevToolsConsoleApiConsoleDirObject] in der Konsolen-API.</span><span class="sxs-lookup"><span data-stu-id="95832-215">For more information, navigate to [console.dir()][DevToolsConsoleApiConsoleDirObject] in the Console API.</span></span>  

---  

## <a name="dirxml"></a><span data-ttu-id="95832-216">dirxml</span><span class="sxs-lookup"><span data-stu-id="95832-216">dirxml</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-217">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-217">Console syntax</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="95832-218">Dieser Befehl druckt eine XML-Darstellung des angegebenen Objekts, wie im **Elementtool** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95832-218">This command prints an XML representation of the specified object, as displayed in the **Elements** tool.</span></span>  <span data-ttu-id="95832-219">Diese Methode entspricht der [console.dirxml()-Methode.][MdnDocsWebApiConsoleDirxml]</span><span class="sxs-lookup"><span data-stu-id="95832-219">This method is equivalent to the [console.dirxml()][MdnDocsWebApiConsoleDirxml] method.</span></span>  

---  

## <a name="inspect"></a><span data-ttu-id="95832-220">inspect</span><span class="sxs-lookup"><span data-stu-id="95832-220">inspect</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-221">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-221">Console syntax</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="95832-222">Dieser Befehl wird geöffnet und wählt das angegebene Element oder Objekt im entsprechenden Bereich aus: entweder das **Elementtool** für DOM-Elemente oder das **Speichertool** für JavaScript-Heapobjekte.</span><span class="sxs-lookup"><span data-stu-id="95832-222">This command opens and chooses the specified element or object in the appropriate panel:  either the **Elements** tool for DOM elements or the **Memory** tool for JavaScript heap objects.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-223">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-223">Console example</span></span>  

<span data-ttu-id="95832-224">Im folgenden Codebeispiel und der folgenden Abbildung wird `document.body` das im **Elementtool** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="95832-224">In the following code sample and figure, the `document.body` opens in the **Elements** tool.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-225">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-225">Console example</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Überprüfen eines Elements mit inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="95832-227">Überprüfen eines Elements mit</span><span class="sxs-lookup"><span data-stu-id="95832-227">Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="95832-228">Beim Übergeben einer Zu überprüfenden Methode öffnet die Methode die Webseite im **Tool Sources,** damit Sie diese überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="95832-228">When passing a method to inspect, the method opens the webpage in the **Sources** tool for you to inspect.</span></span>  

---  

## <a name="geteventlisteners"></a><span data-ttu-id="95832-229">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="95832-229">getEventListeners</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-230">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-230">Console syntax</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="95832-231">Dieser Befehl gibt die Ereignislistener zurück, die für das angegebene Objekt registriert sind.</span><span class="sxs-lookup"><span data-stu-id="95832-231">This command returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="95832-232">Der Rückgabewert ist ein Objekt, das ein Array für jeden registrierten Ereignistyp \(z. B. `click` oder `keydown` \) enthält.</span><span class="sxs-lookup"><span data-stu-id="95832-232">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="95832-233">Die Member der einzelnen Arrays sind Objekte, die den für jeden Typ registrierten Listener beschreiben.</span><span class="sxs-lookup"><span data-stu-id="95832-233">The members of each array are objects that describe the listener registered for each type.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-234">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-234">Console example</span></span>  

<span data-ttu-id="95832-235">Im folgenden Codeausschnitt und der folgenden Abbildung werden alle ereignislistener aufgeführt, die für das Objekt `document` registriert sind.</span><span class="sxs-lookup"><span data-stu-id="95832-235">In the following code snippet and figure, all of the event listeners registered on the `document` object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Ausgabe der Verwendung von getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="95832-237">Das Ergebnis der Verwendung</span><span class="sxs-lookup"><span data-stu-id="95832-237">The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="95832-238">Wenn mehrere Listener für das angegebene Objekt registriert sind, enthält das Array ein Element für jeden Listener.</span><span class="sxs-lookup"><span data-stu-id="95832-238">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="95832-239">In der folgenden Abbildung werden zwei Ereignislistener für das `document` Element für das Ereignis `click` registriert.</span><span class="sxs-lookup"><span data-stu-id="95832-239">In the following figure, two event listeners are registered on the `document` element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Mehrere Listener" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="95832-241">Mehrere Listener</span><span class="sxs-lookup"><span data-stu-id="95832-241">Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="95832-242">Sie können jedes der folgenden Objekte weiter erweitern, um die Eigenschaften zu erkunden.</span><span class="sxs-lookup"><span data-stu-id="95832-242">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Erweiterte Ansicht des Listenerobjekts" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="95832-244">Erweiterte Ansicht des Listenerobjekts</span><span class="sxs-lookup"><span data-stu-id="95832-244">Expanded view of listener object</span></span>  
:::image-end:::  

---  

## <a name="keys"></a><span data-ttu-id="95832-245">Tasten</span><span class="sxs-lookup"><span data-stu-id="95832-245">keys</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-246">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-246">Console syntax</span></span>  

```console
keys(object)
```  

<span data-ttu-id="95832-247">Dieser Befehl gibt ein Array zurück, das die Namen der Eigenschaften enthält, die zum angegebenen Objekt gehören.</span><span class="sxs-lookup"><span data-stu-id="95832-247">This command returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="95832-248">Um die zugeordneten Werte derselben Eigenschaften zu erhalten, verwenden Sie `values()` .</span><span class="sxs-lookup"><span data-stu-id="95832-248">To get the associated values of the same properties, use `values()`.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-249">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-249">Console example</span></span>  

<span data-ttu-id="95832-250">Angenommen, Ihre Anwendung hat das folgende Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="95832-250">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = {"name": "Ted", "level": 42}
```  

<span data-ttu-id="95832-251">In den folgenden Codebeispielen und abbildung wird davon ausgegangen, dass das Ergebnis im globalen Namespace \(zur Einfachheit\) definiert wurde, bevor Sie die Konsole `player1` eingeben und in die Konsole `keys(player1)` `values(player1)` eingeben.</span><span class="sxs-lookup"><span data-stu-id="95832-251">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) before you type `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Die Befehle keys() und values()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="95832-253">Die `keys()` Befehle und `values()`</span><span class="sxs-lookup"><span data-stu-id="95832-253">The `keys()` and `values()` commands</span></span>  
:::image-end:::  

---  

## <a name="monitor"></a><span data-ttu-id="95832-254">Monitor</span><span class="sxs-lookup"><span data-stu-id="95832-254">monitor</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-255">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-255">Console syntax</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="95832-256">Mit diesem Befehl wird eine Meldung an die Konsole protokolliert, die den Methodennamen zusammen mit den Argumenten an die -Methode als Teil einer Anforderung angibt.</span><span class="sxs-lookup"><span data-stu-id="95832-256">This command logs a message to the console that indicates the method name along with the arguments passed to the method as part of a request.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-257">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-257">Console example</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Die monitor()-Methode" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="95832-259">Die `monitor()` Methode</span><span class="sxs-lookup"><span data-stu-id="95832-259">The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="95832-260">Verwenden `unmonitor(method)` Sie, um die Überwachung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="95832-260">Use `unmonitor(method)` to end monitoring.</span></span>  

---  

## <a name="monitorevents"></a><span data-ttu-id="95832-261">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="95832-261">monitorEvents</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-262">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-262">Console syntax</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="95832-263">Wenn eines der angegebenen Ereignisse für das angegebene Objekt auftritt, wird das Ereignisobjekt bei der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="95832-263">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="95832-264">Sie können ein einzelnes zu überwachende Ereignis, ein Array von Ereignissen oder einen der generischen Ereignistypen angeben, die einer vordefinierten Auflistung von Ereignissen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="95832-264">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-265">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-265">Console example</span></span>  

<span data-ttu-id="95832-266">Überprüfen Sie das folgende Codebeispiel und die folgende Abbildung.</span><span class="sxs-lookup"><span data-stu-id="95832-266">Review the following code sample and figure.</span></span>  

<span data-ttu-id="95832-267">Im Folgenden werden alle Größenänderungsereignisse des Fensterobjekts überwacht.</span><span class="sxs-lookup"><span data-stu-id="95832-267">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Überwachen von Fenstergrößeereignissen" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="95832-269">Überwachen von Fenstergrößeereignissen</span><span class="sxs-lookup"><span data-stu-id="95832-269">Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="95832-270">Der folgende Codeausschnitt definiert ein Array, um sowohl ereignisse als `resize` `scroll` auch ereignisse des Window-Objekts zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="95832-270">The following code snippet defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="95832-271">Sie können auch einen der verfügbaren Ereignistypen angeben, Zeichenfolgen, die vordefinierten Ereignissätzen zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="95832-271">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="95832-272">In der folgenden Tabelle werden die verfügbaren Ereignistypen und die zugeordneten Ereigniszuordnungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95832-272">The following table displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="95832-273">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="95832-273">Event type</span></span> | <span data-ttu-id="95832-274">Entsprechende zugeordnete Ereignisse</span><span class="sxs-lookup"><span data-stu-id="95832-274">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="95832-275">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span><span class="sxs-lookup"><span data-stu-id="95832-275">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="95832-276">"keydown", "keypress", "keyup", "textInput"</span><span class="sxs-lookup"><span data-stu-id="95832-276">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="95832-277">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="95832-277">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="95832-278">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span><span class="sxs-lookup"><span data-stu-id="95832-278">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="95832-279">Im folgenden Codebeispiel wird der Ereignistyp, der Ereignissen in einem Eingabetextfeld entspricht, `key` `key` derzeit im **Elementtool** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="95832-279">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently chosen in the **Elements** tool.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="95832-280">In der folgenden Abbildung wird die Beispielausgabe nach dem Eingeben eines Zeichens in das Textfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95832-280">In the following figure, the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Überwachen wichtiger Ereignisse" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="95832-282">Überwachen wichtiger Ereignisse</span><span class="sxs-lookup"><span data-stu-id="95832-282">Monitoring key events</span></span>  
:::image-end:::  

---  

## <a name="profile"></a><span data-ttu-id="95832-283">profile</span><span class="sxs-lookup"><span data-stu-id="95832-283">profile</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-284">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-284">Console syntax</span></span>  

```console
profile([name])
```  

<span data-ttu-id="95832-285">Mit diesem Befehl wird eine JavaScript-CPU-Profilerstellungssitzung mit einem optionalen Namen gestartet.</span><span class="sxs-lookup"><span data-stu-id="95832-285">This command starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="95832-286">Die [profileEnd()-Methode](#profileend) schließt das Profil ab und zeigt die Ergebnisse im **Speichertool** an.</span><span class="sxs-lookup"><span data-stu-id="95832-286">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** tool.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a><span data-ttu-id="95832-287">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-287">Console example</span></span>  

1.  <span data-ttu-id="95832-288">Führen Sie die `profile()` Methode aus, um die Profilerstellung zu starten.</span><span class="sxs-lookup"><span data-stu-id="95832-288">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="95832-289">Führen Sie die [profileEnd()-Methode](#profileend) aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speichertool anzeigen** zu können.</span><span class="sxs-lookup"><span data-stu-id="95832-289">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** tool.</span></span>  

<span data-ttu-id="95832-290">Profile können auch geschachtelt sein.</span><span class="sxs-lookup"><span data-stu-id="95832-290">Profiles may also be nested.</span></span>  <span data-ttu-id="95832-291">In den folgenden Codebeispielen und abbildung ist das Ergebnis unabhängig von der Reihenfolge gleich.</span><span class="sxs-lookup"><span data-stu-id="95832-291">In the following code samples and figure, the result is the same whatever the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="95832-292">Es können mehrere CPU-Profile gleichzeitig ausgeführt werden, und Sie müssen nicht jedes in der Erstellungsreihenfolge schließen.</span><span class="sxs-lookup"><span data-stu-id="95832-292">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

---  

## <a name="profileend"></a><span data-ttu-id="95832-293">profileEnd</span><span class="sxs-lookup"><span data-stu-id="95832-293">profileEnd</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-294">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-294">Console syntax</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="95832-295">Dieser Befehl schließt eine JavaScript-CPU-Profilerstellungssitzung ab und zeigt die Ergebnisse im **Speichertool** an.</span><span class="sxs-lookup"><span data-stu-id="95832-295">This command completes a JavaScript CPU profiling session and displays the results in the **Memory** tool.</span></span>  <span data-ttu-id="95832-296">Sie müssen die [profile()-Methode](#profile) ausführen.</span><span class="sxs-lookup"><span data-stu-id="95832-296">You must be running the [profile()](#profile) method.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a><span data-ttu-id="95832-297">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-297">Console example</span></span>  

1.  <span data-ttu-id="95832-298">Führen Sie die [profile()-Methode](#profile) aus, um die Profilerstellung zu starten.</span><span class="sxs-lookup"><span data-stu-id="95832-298">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="95832-299">Führen Sie `profileEnd()` die Methode aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speichertool** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="95832-299">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** tool.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="95832-300">Profile können auch geschachtelt sein.</span><span class="sxs-lookup"><span data-stu-id="95832-300">Profiles may also be nested.</span></span>  <span data-ttu-id="95832-301">Im folgenden Codebeispiel und der folgenden Abbildung ist das Ergebnis unabhängig von der Reihenfolge identisch.</span><span class="sxs-lookup"><span data-stu-id="95832-301">In the following code sample and figure, the result is the same whatever the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="95832-302">Das Ergebnis wird als Heap-Momentaufnahme im **Speichertool** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95832-302">The result appears as a Heap Snapshot in the **Memory** tool.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Gruppieren von Profilen" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="95832-304">Gruppieren von Profilen</span><span class="sxs-lookup"><span data-stu-id="95832-304">Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="95832-305">Es können mehrere CPU-Profile gleichzeitig ausgeführt werden, und Sie müssen nicht jedes in der Erstellungsreihenfolge schließen.</span><span class="sxs-lookup"><span data-stu-id="95832-305">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

---  

## <a name="queryobjects"></a><span data-ttu-id="95832-306">queryObjects</span><span class="sxs-lookup"><span data-stu-id="95832-306">queryObjects</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-307">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-307">Console syntax</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="95832-308">Dieser Befehl gibt ein Array von Objekten zurück, die mit dem angegebenen Konstruktor erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="95832-308">This command returns an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="95832-309">Der Bereich von `queryObjects()` ist der aktuell ausgewählte Laufzeitkontext in der **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="95832-309">The scope of `queryObjects()` is the currently chosen runtime context in the **Console**.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-310">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-310">Console example</span></span>  

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="95832-311">Gibt alle `Promises` zurück.</span><span class="sxs-lookup"><span data-stu-id="95832-311">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="95832-312">Gibt alle HTML-Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="95832-312">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="95832-313">Gibt alle Objekte zurück, die mit instanziiert `new functionName()` wurden.</span><span class="sxs-lookup"><span data-stu-id="95832-313">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="95832-314">Tabelle</span><span class="sxs-lookup"><span data-stu-id="95832-314">table</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-315">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-315">Console syntax</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="95832-316">Dieser Befehl protokolliert Objektdaten mit Tabellenformatierung basierend auf dem Datenobjekt in mit optionalen Spaltenüberschriften.</span><span class="sxs-lookup"><span data-stu-id="95832-316">This command logs object data with table formatting based upon the data object in with optional column headings.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-317">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-317">Console example</span></span>  

<span data-ttu-id="95832-318">Im folgenden Codebeispiel und der folgenden Abbildung wird eine Liste der Namen angezeigt, die eine Tabelle in der Konsole verwenden.</span><span class="sxs-lookup"><span data-stu-id="95832-318">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

```console
var names = {
    0:  {
        firstName:  "John",
        lastName:  "Smith"
    },
    1:  {
        firstName:  "Jane",
        lastName:  "Doe"
    }
};
table(names);
```  

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="Das Ergebnis der table()-Methode" lightbox="../media/console-table-display.msft.png":::
   <span data-ttu-id="95832-320">Das Ergebnis der `table()` Methode</span><span class="sxs-lookup"><span data-stu-id="95832-320">The result of the `table()` method</span></span>  
:::image-end:::  

---  

## <a name="undebug"></a><span data-ttu-id="95832-321">undebug</span><span class="sxs-lookup"><span data-stu-id="95832-321">undebug</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-322">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-322">Console syntax</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="95832-323">Mit diesem Befehl wird das Debuggen der angegebenen Methode beendet.</span><span class="sxs-lookup"><span data-stu-id="95832-323">This command stops the debug of the specified method.</span></span> <span data-ttu-id="95832-324">Wenn also die Methode angefordert wird, wird der Debugger nicht mehr aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="95832-324">So when the method is requested, the debugger is no longer invoked.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-325">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-325">Console example</span></span>  

```console
undebug(getData);
```  

---  

## <a name="unmonitor"></a><span data-ttu-id="95832-326">unmonitor</span><span class="sxs-lookup"><span data-stu-id="95832-326">unmonitor</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-327">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-327">Console syntax</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="95832-328">Mit diesem Befehl wird die Überwachung der angegebenen Methode beendet.</span><span class="sxs-lookup"><span data-stu-id="95832-328">This command stops the monitoring of the specified method.</span></span>  <span data-ttu-id="95832-329">Diese Methode wird in Zusammenarbeit mit der [monitor()-Methode](#monitor) verwendet.</span><span class="sxs-lookup"><span data-stu-id="95832-329">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-330">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-330">Console example</span></span>  

```console
unmonitor(getData);
```  

---  

## <a name="unmonitorevents"></a><span data-ttu-id="95832-331">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="95832-331">unmonitorEvents</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-332">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-332">Console syntax</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="95832-333">Mit diesem Befehl werden Überwachungsereignisse für das angegebene Objekt und die angegebenen Ereignisse beendet.</span><span class="sxs-lookup"><span data-stu-id="95832-333">This command stops monitoring events for the specified object and events.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-334">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-334">Console example</span></span>  

<span data-ttu-id="95832-335">Der folgende Codeausschnitt beendet beispielsweise die Ereignisüberwachung für das Window-Objekt.</span><span class="sxs-lookup"><span data-stu-id="95832-335">For example, the following code snippet stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="95832-336">Sie können auch selektiv die Überwachung bestimmter Ereignisse für ein Objekt beenden.</span><span class="sxs-lookup"><span data-stu-id="95832-336">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="95832-337">Der folgende Code startet beispielsweise die Überwachung aller Ereignisse für das aktuell ausgewählte Element und beendet dann Überwachungsereignisse \(möglicherweise, um das Rauschen in der `mouse` Konsolenausgabe `mousemove` zu reduzieren\).</span><span class="sxs-lookup"><span data-stu-id="95832-337">For example, the following code starts monitoring all `mouse` events on the currently chosen element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

---  

## <a name="values"></a><span data-ttu-id="95832-338">werte</span><span class="sxs-lookup"><span data-stu-id="95832-338">values</span></span>  

### <a name="console-syntax"></a><span data-ttu-id="95832-339">Konsolensyntax</span><span class="sxs-lookup"><span data-stu-id="95832-339">Console syntax</span></span>  

```console
values(object)
```  

<span data-ttu-id="95832-340">Dieser Befehl gibt ein Array zurück, das die Werte aller Eigenschaften enthält, die zum angegebenen Objekt gehören.</span><span class="sxs-lookup"><span data-stu-id="95832-340">This command returns an array containing the values of all properties belonging to the specified object.</span></span>  

### <a name="console-example"></a><span data-ttu-id="95832-341">Konsolenbeispiel</span><span class="sxs-lookup"><span data-stu-id="95832-341">Console example</span></span>  

```console
values(object);
```  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="95832-342">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="95832-342">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevToolsConsoleApiConsoleDirObject]: ./api.md#dir "dir – Konsolen-API-| Microsoft Docs"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "So halten Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools | Microsoft Docs"  

[DevtoolsRenderingToolsJsRuntime]: ../rendering-tools/js-runtime.md "Beschleunigen sie die JavaScript-Laufzeit | Microsoft Docs"  

[CR1050237]: https://crbug.com/1050237 "Problem 1050237: debug(function) funktioniert nicht | Chromium-Fehler"  

[MdnDocsWebApiConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MdnDocsWebApiConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MdnDocsWebApiDocumentQueryselector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MdnDocsWebApiDocumentQueryselectorall]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

> [!NOTE]
> <span data-ttu-id="95832-352">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95832-352">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="95832-353">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/utilities) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="95832-353">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="95832-355">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="95832-355">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

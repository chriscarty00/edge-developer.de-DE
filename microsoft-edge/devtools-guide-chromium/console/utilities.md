---
description: Ein Verweis auf Komfortbefehle, die in der Microsoft Edge DevTools-Konsole verfügbar sind.
title: Referenz zur Konsolen-Hilfsprogramme-API
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: e7253bf5402a03d1659f56ba083bb87e93b3af38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398826"
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

# <a name="console-utilities-api-reference"></a><span data-ttu-id="946be-104">Referenz zur Konsolen-Hilfsprogramme-API</span><span class="sxs-lookup"><span data-stu-id="946be-104">Console Utilities API reference</span></span>  

<span data-ttu-id="946be-105">Die Console Utilities-API enthält eine Auflistung von Komfortbefehlen zum Ausführen gängiger Aufgaben: Auswählen und Überprüfen von DOM-Elementen, Anzeigen von Daten im lesbaren Format, Beenden und Starten des Profilers und Überwachen von DOM-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="946be-105">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="946be-106">Die folgenden Befehle funktionieren nur in der Microsoft Edge DevTools-Konsole.</span><span class="sxs-lookup"><span data-stu-id="946be-106">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="946be-107">Die Befehle funktionieren nicht, wenn sie aus Ihren Skripts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="946be-107">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="946be-108">Navigieren Sie `console.log()` für `console.error()` die und-Methoden der restlichen `console.*` Methoden zu [Konsolen-API-Referenz][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="946be-108">For the `console.log()` and `console.error()` methods the rest of the `console.*` methods, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  

## <a name="recently-evaluated-expression"></a><span data-ttu-id="946be-109">Kürzlich ausgewerteter Ausdruck</span><span class="sxs-lookup"><span data-stu-id="946be-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="946be-110">Gibt den Wert des zuletzt ausgewerteten Ausdrucks zurück.</span><span class="sxs-lookup"><span data-stu-id="946be-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="946be-111">In der folgenden Abbildung wird ein einfacher Ausdruck \( `2 + 2` \) ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="946be-111">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="946be-112">Die `$_` Eigenschaft wird dann ausgewertet, die denselben Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="946be-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-arithmatic.msft.png":::
   <span data-ttu-id="946be-114">Abbildung 1:  `$_` ist der zuletzt ausgewertete Ausdruck</span><span class="sxs-lookup"><span data-stu-id="946be-114">Figure 1:  `$_` is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="946be-115">In der folgenden Abbildung enthält der ausgewertete Ausdruck zunächst ein Array von Namen.</span><span class="sxs-lookup"><span data-stu-id="946be-115">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="946be-116">Auswerten, um die Länge des Arrays zu finden, wird der in Änderungen gespeicherte Wert zum `$_.length` `$_` neuesten ausgewerteten Ausdruck, `4` .</span><span class="sxs-lookup"><span data-stu-id="946be-116">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ ändert sich, wenn neue Befehle ausgewertet werden" lightbox="../media/console-array-length.msft.png":::
   <span data-ttu-id="946be-118">Abbildung 2:  `$_` Änderungen bei der Auswertung neuer Befehle</span><span class="sxs-lookup"><span data-stu-id="946be-118">Figure 2:  `$_` changes when new commands are evaluated</span></span>  
:::image-end:::  

## <a name="recently-chosen-element-or-javascript-object"></a><span data-ttu-id="946be-119">Kürzlich ausgewähltes Element oder JavaScript-Objekt</span><span class="sxs-lookup"><span data-stu-id="946be-119">Recently Chosen Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="946be-120">Gibt das zuletzt ausgewählte Element oder JavaScript-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="946be-120">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="946be-121">gibt den zweiten zuletzt ausgewählten zurück, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="946be-121">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="946be-122">Die Befehle , , , und funktionieren als verlaufshistorische Referenz zu den letzten fünf DOM-Elementen, die im Elementtool oder den letzten fünf im Speichertool ausgewählten `$0` `$1` `$2` `$3` `$4` JavaScript-Heapobjekten überprüft wurden. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="946be-122">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** tool or the last five JavaScript heap objects selected in the **Memory** tool.</span></span>  

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
   :::column-end:::
:::row-end:::  

<span data-ttu-id="946be-123">In der folgenden Abbildung wird `img` ein Element im **Elementtool ausgewählt.**</span><span class="sxs-lookup"><span data-stu-id="946be-123">In the following figure, an `img` element is selected in the **Elements** tool.</span></span>  <span data-ttu-id="946be-124">In der **Konsolenschube** `$0` wurde ausgewertet und zeigt dasselbe Element an.</span><span class="sxs-lookup"><span data-stu-id="946be-124">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Die $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="946be-126">Abbildung 3: Die</span><span class="sxs-lookup"><span data-stu-id="946be-126">Figure 3:  The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="946be-127">In der folgenden Abbildung zeigt die Abbildung ein anderes Element, das auf derselben Seite ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="946be-127">In the following figure, the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="946be-128">The `$0` bezieht sich nun auf das neu ausgewählte Element, während das zuvor ausgewählte Element zurückgegeben `$1` wird.</span><span class="sxs-lookup"><span data-stu-id="946be-128">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="Die $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="946be-130">Abbildung 4: Die</span><span class="sxs-lookup"><span data-stu-id="946be-130">Figure 4:  The</span></span> `$1`  
:::image-end:::  

## <a name="query-selector"></a><span data-ttu-id="946be-131">Abfrageauswahl</span><span class="sxs-lookup"><span data-stu-id="946be-131">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="946be-132">Gibt den Verweis auf das erste DOM-Element mit dem angegebenen CSS-Selektor zurück.</span><span class="sxs-lookup"><span data-stu-id="946be-132">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="946be-133">Diese Methode ist ein Alias für die [document.querySelector()-Methode.][MDNDocumentQuerySelector]</span><span class="sxs-lookup"><span data-stu-id="946be-133">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="946be-134">In der folgenden Abbildung wird ein Verweis auf das erste `<img>` Element im Dokument zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="946be-134">In the following figure, a reference to the first `<img>` element in the document is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="946be-136">Abbildung 5: Die</span><span class="sxs-lookup"><span data-stu-id="946be-136">Figure 5:  The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="946be-137">Zeigen Sie auf das zurückgegebene Ergebnis, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie Im Elementbereich einblenden aus, um es im DOM zu finden, oder scrollen Sie **in** ansicht, um es auf der Seite anzuzeigen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="946be-137">Hover on the returned result, open the contextual menu \(right-click\), and choose **Reveal in Elements Panel** to find it in the DOM or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="946be-138">In der folgenden Abbildung wird ein Verweis auf das aktuell ausgewählte Element zurückgegeben, und die src-Eigenschaft wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="946be-138">In the following figure, a reference to the currently selected element is returned and the src property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="946be-140">Abbildung 6: Die</span><span class="sxs-lookup"><span data-stu-id="946be-140">Figure 6:  The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="946be-141">Diese Methode unterstützt auch einen zweiten Parameter, startNode, der ein "Element" oder einen Knoten angibt, von dem aus nach Elementen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="946be-141">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="946be-142">Der Standardwert des Parameters ist `document` .</span><span class="sxs-lookup"><span data-stu-id="946be-142">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="946be-143">In der folgenden Abbildung wird das erste Element gefunden, nachdem das gefunden wurde und das ordnungsgemäß `img` `title--image` angezeigt `src` wird.</span><span class="sxs-lookup"><span data-stu-id="946be-143">In the following figure, the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="The $('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="946be-145">Abbildung 7: Die</span><span class="sxs-lookup"><span data-stu-id="946be-145">Figure 7:  The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="946be-146">Wenn Sie eine Bibliothek wie jQuery verwenden, die verwendet, wird die Funktionalität überschrieben und entspricht der Implementierung `$` `$` aus dieser Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="946be-146">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <a name="query-selector-all"></a><span data-ttu-id="946be-147">Abfrageauswahl alle</span><span class="sxs-lookup"><span data-stu-id="946be-147">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="946be-148">Gibt ein Array von Elementen zurück, die mit dem angegebenen CSS-Selektor übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="946be-148">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="946be-149">Diese Methode entspricht dem Ausführen der [document.querySelectorAll()-Methode.][MDNDocumentQuerySelectorAll]</span><span class="sxs-lookup"><span data-stu-id="946be-149">This method is equivalent to running the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="946be-150">Im folgenden Codebeispiel und der folgenden Abbildung können Sie ein Array aller Elemente im aktuellen Dokument erstellen und den Wert der Eigenschaft `$$()` `<img>` für jedes Element `src` anzeigen.</span><span class="sxs-lookup"><span data-stu-id="946be-150">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Verwenden von $$() zum Auswählen aller Bilder im Dokument und Anzeigen der Quellen" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="946be-152">Abbildung 8: Verwenden `$$()` zum Auswählen aller Bilder im Dokument und Anzeigen der Quellen</span><span class="sxs-lookup"><span data-stu-id="946be-152">Figure 8:  Using `$$()` to select all images in the document and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="946be-153">Diese Methode unterstützt auch einen zweiten Parameter, startNode, der ein Element oder einen Knoten angibt, von dem aus nach Elementen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="946be-153">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="946be-154">Der Standardwert des Parameters ist `document` .</span><span class="sxs-lookup"><span data-stu-id="946be-154">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="946be-155">Im folgenden Codebeispiel und der folgenden Abbildung wird eine geänderte Version des vorherigen Codebeispiels und der abbildung verwendet, um ein Array aller Elemente zu erstellen, die im aktuellen Dokument nach dem ausgewählten `$$()` `<img>` Knoten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="946be-155">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Verwenden von $$(), um alle Bilder auszuwählen, die nach dem angegebenen <div> im Dokument angezeigt werden, und die Quellen anzeigen" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="946be-157">Abbildung 9: `$$()` Verwenden, um alle Bilder auszuwählen, die nach dem angegebenen Element im Dokument angezeigt werden, und `<div>` die Quellen anzeigen</span><span class="sxs-lookup"><span data-stu-id="946be-157">Figure 9:  Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="946be-158">Wählen `Shift` + `Enter` Sie in der Konsole aus, um eine neue Zeile zu starten, ohne das Skript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="946be-158">Select `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <a name="xpath"></a><span data-ttu-id="946be-159">XPath</span><span class="sxs-lookup"><span data-stu-id="946be-159">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="946be-160">Gibt ein Array von DOM-Elementen zurück, die mit dem angegebenen XPath-Ausdruck übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="946be-160">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="946be-161">Im folgenden Codebeispiel und der folgenden Abbildung werden alle Elemente auf der Seite `<p>` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="946be-161">In the following code sample and figure, all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Verwenden eines XPath-Selektors" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="946be-163">Abbildung 10: Verwenden eines XPath-Selektors</span><span class="sxs-lookup"><span data-stu-id="946be-163">Figure 10:  Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="946be-164">Im folgenden Codebeispiel und der folgenden Abbildung werden alle Elemente zurückgegeben, die Elemente `<p>` `<a>` enthalten.</span><span class="sxs-lookup"><span data-stu-id="946be-164">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Verwenden eines komplizierteren XPath-Selektors" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="946be-166">Abbildung 11: Verwenden eines komplizierteren XPath-Selektors</span><span class="sxs-lookup"><span data-stu-id="946be-166">Figure 11:  Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="946be-167">Ähnlich wie die anderen Selektorbefehle verfügt über einen optionalen zweiten Parameter, der ein Element oder einen Knoten angibt, von dem aus `$x(path)` nach Elementen gesucht werden `startNode` soll.</span><span class="sxs-lookup"><span data-stu-id="946be-167">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Verwenden eines XPath-Selektors mit startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="946be-169">Abbildung 12: Verwenden eines XPath-Selektors mit</span><span class="sxs-lookup"><span data-stu-id="946be-169">Figure 12:  Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

## <a name="clear"></a><span data-ttu-id="946be-170">clear</span><span class="sxs-lookup"><span data-stu-id="946be-170">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="946be-171">Die Konsole des Verlaufs wird geräumt.</span><span class="sxs-lookup"><span data-stu-id="946be-171">Clears the console of the history.</span></span>  

```console
clear()
```  

## <a name="copy"></a><span data-ttu-id="946be-172">copy</span><span class="sxs-lookup"><span data-stu-id="946be-172">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="946be-173">Die `copy(object)` Methode kopiert eine Zeichenfolgendarstellung des angegebenen Objekts in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="946be-173">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <a name="debug"></a><span data-ttu-id="946be-174">debuggen</span><span class="sxs-lookup"><span data-stu-id="946be-174">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="946be-175">Das [#A0 #1050237][MonorailIssue1050237] verfolgt einen Fehler mit der `debug()` Funktion.</span><span class="sxs-lookup"><span data-stu-id="946be-175">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="946be-176">Wenn das Problem auftreten sollte, versuchen Sie stattdessen, [Haltepunkte zu][DevtoolsJavascriptBreakpoints] verwenden.</span><span class="sxs-lookup"><span data-stu-id="946be-176">If you encounter the issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="946be-177">Wenn Sie die angegebene Methode anfordern, wird der Debugger aufgerufen und innerhalb der Methode im **Sources-Tool** umbricht, sodass Sie den Code schrittweise durchbrechen und debuggen können.</span><span class="sxs-lookup"><span data-stu-id="946be-177">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** tool allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Durchbrechen einer Methode mit debug()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="946be-179">Abbildung 13: Einbrechen in eine Methode mit</span><span class="sxs-lookup"><span data-stu-id="946be-179">Figure 13:  Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="946be-180">Verwenden `undebug(method)` Sie diese Option, um die Unterbrechung der Methode zu beenden, oder verwenden Sie die Benutzeroberfläche, um alle Haltepunkte zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="946be-180">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="946be-181">Weitere Informationen zu Haltepunkten finden Sie unter [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="946be-181">For more information on breakpoints, navigate to [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <a name="dir"></a><span data-ttu-id="946be-182">dir</span><span class="sxs-lookup"><span data-stu-id="946be-182">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="946be-183">Zeigt eine Objektformatliste aller Eigenschaften für das angegebene Objekt an.</span><span class="sxs-lookup"><span data-stu-id="946be-183">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="946be-184">Diese Methode ist ein Alias für die [console.dir()-Methode.][MDNConsoleDir]</span><span class="sxs-lookup"><span data-stu-id="946be-184">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="946be-185">Werten `document.head` Sie in der Konsole aus, um den HTML-Code zwischen den tags und zu `<head>` `</head>` anzeigen.</span><span class="sxs-lookup"><span data-stu-id="946be-185">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="946be-186">Im folgenden Codebeispiel und der folgenden Abbildung wird nach der Verwendung in der Konsole eine Auflistung im `console.dir()` Objektstil angezeigt.</span><span class="sxs-lookup"><span data-stu-id="946be-186">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Protokollierung von document.head mit dir()-Methode" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="946be-188">Abbildung 14: `document.head` Protokollierung mit `dir()` Methode</span><span class="sxs-lookup"><span data-stu-id="946be-188">Figure 14:  Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="946be-189">Weitere Informationen finden Sie unter Eintrag [`console.dir()`][DevToolsConsoleApiConsoleDirObject] in der Konsolen-API.</span><span class="sxs-lookup"><span data-stu-id="946be-189">For more information, navigate to [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <a name="dirxml"></a><span data-ttu-id="946be-190">dirxml</span><span class="sxs-lookup"><span data-stu-id="946be-190">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="946be-191">Druckt eine XML-Darstellung des angegebenen Objekts, wie im **Elementtool** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="946be-191">Prints an XML representation of the specified object, as displayed in the **Elements** tool.</span></span>  <span data-ttu-id="946be-192">Diese Methode entspricht der [console.dirxml()-Methode.][MDNConsoleDirxml]</span><span class="sxs-lookup"><span data-stu-id="946be-192">This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <a name="inspect"></a><span data-ttu-id="946be-193">inspect</span><span class="sxs-lookup"><span data-stu-id="946be-193">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="946be-194">Öffnet und wählt das angegebene Element oder Objekt im entsprechenden Bereich aus: entweder das **Elementtool** für DOM-Elemente oder das **Speichertool** für JavaScript-Heapobjekte.</span><span class="sxs-lookup"><span data-stu-id="946be-194">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** tool for DOM elements or the **Memory** tool for JavaScript heap objects.</span></span>  

<span data-ttu-id="946be-195">Im folgenden Codebeispiel und der folgenden Abbildung wird `document.body` das im **Elementtool** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="946be-195">In the following code sample and figure, the `document.body` opens in the **Elements** tool.</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Überprüfen eines Elements mit inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="946be-197">Abbildung 15: Überprüfen eines Elements mit</span><span class="sxs-lookup"><span data-stu-id="946be-197">Figure 15:  Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="946be-198">Beim Übergeben einer Zu überprüfenden Methode öffnet \*\*\*\* die Methode das Dokument im Sources-Tool, damit Sie es überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="946be-198">When passing a method to inspect, the method opens the document in the **Sources** tool for you to inspect.</span></span>  

## <a name="geteventlisteners"></a><span data-ttu-id="946be-199">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="946be-199">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="946be-200">Gibt die Ereignislistener zurück, die für das angegebene Objekt registriert sind.</span><span class="sxs-lookup"><span data-stu-id="946be-200">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="946be-201">Der Rückgabewert ist ein Objekt, das ein Array für jeden registrierten Ereignistyp \(z. B. `click` oder `keydown` \) enthält.</span><span class="sxs-lookup"><span data-stu-id="946be-201">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="946be-202">Die Member der einzelnen Arrays sind Objekte, die den für jeden Typ registrierten Listener beschreiben.</span><span class="sxs-lookup"><span data-stu-id="946be-202">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="946be-203">In der folgenden Codebeispielfigur werden alle ereignislistener aufgeführt, die für das Dokumentobjekt registriert sind.</span><span class="sxs-lookup"><span data-stu-id="946be-203">In the following code sample figure, all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Ausgabe der Verwendung von getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="946be-205">Abbildung 16: Das Ergebnis der Verwendung</span><span class="sxs-lookup"><span data-stu-id="946be-205">Figure 16:  The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="946be-206">Wenn mehrere Listener für das angegebene Objekt registriert sind, enthält das Array ein Element für jeden Listener.</span><span class="sxs-lookup"><span data-stu-id="946be-206">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="946be-207">In der folgenden Abbildung sind zwei Ereignislistener für das Dokumentelement für das Ereignis `click` registriert.</span><span class="sxs-lookup"><span data-stu-id="946be-207">In the following figure, there are two event listeners registered on the document element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Mehrere Listener" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="946be-209">Abbildung 17: Mehrere Listener</span><span class="sxs-lookup"><span data-stu-id="946be-209">Figure 17:  Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="946be-210">Sie können jedes der folgenden Objekte weiter erweitern, um die Eigenschaften zu erkunden.</span><span class="sxs-lookup"><span data-stu-id="946be-210">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Erweiterte Ansicht des Listenerobjekts" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="946be-212">Abbildung 18: Erweiterte Ansicht des Listenerobjekts</span><span class="sxs-lookup"><span data-stu-id="946be-212">Figure 18:  Expanded view of listener object</span></span>  
:::image-end:::  

## <a name="keys"></a><span data-ttu-id="946be-213">Tasten</span><span class="sxs-lookup"><span data-stu-id="946be-213">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="946be-214">Gibt ein Array zurück, das die Namen der Eigenschaften enthält, die zum angegebenen Objekt gehören.</span><span class="sxs-lookup"><span data-stu-id="946be-214">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="946be-215">Um die zugeordneten Werte derselben Eigenschaften zu erhalten, verwenden Sie `values()` .</span><span class="sxs-lookup"><span data-stu-id="946be-215">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="946be-216">Angenommen, Ihre Anwendung hat das folgende Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="946be-216">For example, suppose your application defined the following object.</span></span>  

```console
var player1 =   
```  

<span data-ttu-id="946be-217">In den folgenden Codebeispielen und abbildung wird davon ausgegangen, dass das Ergebnis vor der Eingabe und in der Konsole im globalen `player1` Namespace \(zur Einfachheit\) `keys(player1)` `values(player1)` definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="946be-217">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Die Befehle keys() und values()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="946be-219">Abbildung 19: Die `keys()` Befehle und `values()`</span><span class="sxs-lookup"><span data-stu-id="946be-219">Figure 19:  The `keys()` and `values()` commands</span></span>  
:::image-end:::  

## <a name="monitor"></a><span data-ttu-id="946be-220">Monitor</span><span class="sxs-lookup"><span data-stu-id="946be-220">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="946be-221">Protokolliert eine Nachricht an die Konsole, die den Methodennamen zusammen mit den Argumenten angibt, die beim Aufgerufen an die -Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="946be-221">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Die monitor()-Methode" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="946be-223">Abbildung 20: Die `monitor()` Methode</span><span class="sxs-lookup"><span data-stu-id="946be-223">Figure 20:  The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="946be-224">Verwenden `unmonitor(method)` Sie, um die Überwachung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="946be-224">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <a name="monitorevents"></a><span data-ttu-id="946be-225">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="946be-225">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="946be-226">Wenn eines der angegebenen Ereignisse für das angegebene Objekt auftritt, wird das Ereignisobjekt bei der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="946be-226">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="946be-227">Sie können ein einzelnes zu überwachende Ereignis, ein Array von Ereignissen oder einen der generischen Ereignistypen angeben, die einer vordefinierten Auflistung von Ereignissen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="946be-227">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="946be-228">Überprüfen Sie das folgende Codebeispiel und die folgende Abbildung.</span><span class="sxs-lookup"><span data-stu-id="946be-228">Review the following code sample and figure.</span></span>  

<span data-ttu-id="946be-229">Im Folgenden werden alle Größenänderungsereignisse des Fensterobjekts überwacht.</span><span class="sxs-lookup"><span data-stu-id="946be-229">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Überwachen von Fenstergrößeereignissen" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="946be-231">Abbildung 21: Überwachen von Fenstergrößeereignissen</span><span class="sxs-lookup"><span data-stu-id="946be-231">Figure 21:  Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="946be-232">Im Folgenden wird ein Array definiert, das sowohl die Ereignisse als `resize` `scroll` auch das Fensterobjekt überwacht.</span><span class="sxs-lookup"><span data-stu-id="946be-232">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="946be-233">Sie können auch einen der verfügbaren Ereignistypen angeben, Zeichenfolgen, die vordefinierten Ereignissätzen zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="946be-233">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="946be-234">In der folgenden Tabelle werden die verfügbaren Ereignistypen und die zugeordneten Ereigniszuordnungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="946be-234">The following table displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="946be-235">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="946be-235">Event type</span></span> | <span data-ttu-id="946be-236">Entsprechende zugeordnete Ereignisse</span><span class="sxs-lookup"><span data-stu-id="946be-236">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="946be-237">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span><span class="sxs-lookup"><span data-stu-id="946be-237">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="946be-238">"keydown", "keypress", "keyup", "textInput"</span><span class="sxs-lookup"><span data-stu-id="946be-238">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="946be-239">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="946be-239">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="946be-240">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span><span class="sxs-lookup"><span data-stu-id="946be-240">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="946be-241">Im folgenden Codebeispiel wird der Ereignistyp, der Ereignissen in einem Eingabetextfeld entspricht, `key` `key` derzeit im **Elementtool** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="946be-241">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** tool.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="946be-242">In der folgenden Abbildung wird die Beispielausgabe nach dem Eingeben eines Zeichens in das Textfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="946be-242">In the following figure the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Überwachen wichtiger Ereignisse" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="946be-244">Abbildung 22: Überwachen wichtiger Ereignisse</span><span class="sxs-lookup"><span data-stu-id="946be-244">Figure 22:  Monitoring key events</span></span>  
:::image-end:::  

## <a name="profile"></a><span data-ttu-id="946be-245">profile</span><span class="sxs-lookup"><span data-stu-id="946be-245">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="946be-246">Startet eine JavaScript-CPU-Profilerstellungssitzung mit einem optionalen Namen.</span><span class="sxs-lookup"><span data-stu-id="946be-246">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="946be-247">Die [profileEnd()-Methode](#profileend) schließt das Profil ab und zeigt die Ergebnisse im **Speichertool** an.</span><span class="sxs-lookup"><span data-stu-id="946be-247">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** tool.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="946be-248">Führen Sie die `profile()` Methode aus, um die Profilerstellung zu starten.</span><span class="sxs-lookup"><span data-stu-id="946be-248">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="946be-249">Führen Sie die [profileEnd()-Methode](#profileend) aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speichertool anzeigen** zu können.</span><span class="sxs-lookup"><span data-stu-id="946be-249">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** tool.</span></span>  

<span data-ttu-id="946be-250">Profile können auch geschachtelt sein.</span><span class="sxs-lookup"><span data-stu-id="946be-250">Profiles may also be nested.</span></span>  <span data-ttu-id="946be-251">In den folgenden Codebeispielen und abbildung ist das Ergebnis unabhängig von der Reihenfolge gleich.</span><span class="sxs-lookup"><span data-stu-id="946be-251">In the following code samples and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="946be-252">Es können mehrere CPU-Profile gleichzeitig ausgeführt werden, und Sie müssen nicht jedes in der Erstellungsreihenfolge schließen.</span><span class="sxs-lookup"><span data-stu-id="946be-252">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <a name="profileend"></a><span data-ttu-id="946be-253">profileEnd</span><span class="sxs-lookup"><span data-stu-id="946be-253">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="946be-254">Schließt eine JavaScript-CPU-Profilerstellungssitzung ab und zeigt die Ergebnisse im **Speichertool** an.</span><span class="sxs-lookup"><span data-stu-id="946be-254">Completes a JavaScript CPU profiling session and displays the results in the **Memory** tool.</span></span>  <span data-ttu-id="946be-255">Sie müssen die [profile()-Methode](#profile) ausführen.</span><span class="sxs-lookup"><span data-stu-id="946be-255">You must be running the [profile()](#profile) method.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="946be-256">Führen Sie die [profile()-Methode](#profile) aus, um die Profilerstellung zu starten.</span><span class="sxs-lookup"><span data-stu-id="946be-256">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="946be-257">Führen Sie `profileEnd()` die Methode aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speichertool** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="946be-257">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** tool.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="946be-258">Profile können auch geschachtelt sein.</span><span class="sxs-lookup"><span data-stu-id="946be-258">Profiles may also be nested.</span></span>  <span data-ttu-id="946be-259">Im folgenden Codebeispiel und in der abbildung ist das Ergebnis unabhängig von der Reihenfolge identisch.</span><span class="sxs-lookup"><span data-stu-id="946be-259">In the following code sample and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="946be-260">Das Ergebnis wird als Heap-Momentaufnahme im **Speichertool** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="946be-260">The result appears as a Heap Snapshot in the **Memory** tool.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Gruppieren von Profilen" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="946be-262">Abbildung 23: Gruppieren von Profilen</span><span class="sxs-lookup"><span data-stu-id="946be-262">Figure 23:  Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="946be-263">Es können mehrere CPU-Profile gleichzeitig ausgeführt werden, und Sie müssen nicht jedes in der Erstellungsreihenfolge schließen.</span><span class="sxs-lookup"><span data-stu-id="946be-263">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <a name="queryobjects"></a><span data-ttu-id="946be-264">queryObjects</span><span class="sxs-lookup"><span data-stu-id="946be-264">queryObjects</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="946be-265">Gibt ein Array von Objekten zurück, die mit dem angegebenen Konstruktor erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="946be-265">Return an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="946be-266">Der Bereich `queryObjects()` von ist der aktuell ausgewählte Laufzeitkontext in der Konsole.</span><span class="sxs-lookup"><span data-stu-id="946be-266">The scope of `queryObjects()` is the currently-selected runtime context in the console.</span></span>

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="946be-267">Gibt alle `Promises` zurück.</span><span class="sxs-lookup"><span data-stu-id="946be-267">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="946be-268">Gibt alle HTML-Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="946be-268">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="946be-269">Gibt alle Objekte zurück, die mit instanziiert `new functionName()` wurden.</span><span class="sxs-lookup"><span data-stu-id="946be-269">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="946be-270">Tabelle</span><span class="sxs-lookup"><span data-stu-id="946be-270">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="946be-271">Protokolliert Objektdaten mit Tabellenformatierung basierend auf dem Datenobjekt in mit optionalen Spaltenüberschriften.</span><span class="sxs-lookup"><span data-stu-id="946be-271">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="946be-272">Im folgenden Codebeispiel und der folgenden Abbildung wird eine Liste der Namen angezeigt, die eine Tabelle in der Konsole verwenden.</span><span class="sxs-lookup"><span data-stu-id="946be-272">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

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
   <span data-ttu-id="946be-274">Abbildung 24: Das Ergebnis der `table()` Methode</span><span class="sxs-lookup"><span data-stu-id="946be-274">Figure 24:  The result of the `table()` method</span></span>  
:::image-end:::  

## <a name="undebug"></a><span data-ttu-id="946be-275">undebug</span><span class="sxs-lookup"><span data-stu-id="946be-275">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="946be-276">Beendet das Debuggen der angegebenen Methode, sodass beim Aufruf der Methode der Debugger nicht mehr aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="946be-276">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <a name="unmonitor"></a><span data-ttu-id="946be-277">unmonitor</span><span class="sxs-lookup"><span data-stu-id="946be-277">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="946be-278">Beendet die Überwachung der angegebenen Methode.</span><span class="sxs-lookup"><span data-stu-id="946be-278">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="946be-279">Diese Methode wird in Zusammenarbeit mit der [monitor()-Methode](#monitor) verwendet.</span><span class="sxs-lookup"><span data-stu-id="946be-279">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <a name="unmonitorevents"></a><span data-ttu-id="946be-280">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="946be-280">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="946be-281">Beendet Überwachungsereignisse für das angegebene Objekt und die angegebenen Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="946be-281">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="946be-282">Im Folgenden wird beispielsweise die Ereignisüberwachung für das Window-Objekt beendet.</span><span class="sxs-lookup"><span data-stu-id="946be-282">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="946be-283">Sie können auch selektiv die Überwachung bestimmter Ereignisse für ein Objekt beenden.</span><span class="sxs-lookup"><span data-stu-id="946be-283">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="946be-284">Der folgende Code startet beispielsweise die Überwachung aller Ereignisse für das aktuell ausgewählte Element und beendet dann Überwachungsereignisse \(möglicherweise, um das Rauschen in der `mouse` Konsolenausgabe `mousemove` zu reduzieren\).</span><span class="sxs-lookup"><span data-stu-id="946be-284">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <a name="values"></a><span data-ttu-id="946be-285">werte</span><span class="sxs-lookup"><span data-stu-id="946be-285">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="946be-286">Gibt ein Array zurück, das die Werte aller Eigenschaften enthält, die zum angegebenen Objekt gehören.</span><span class="sxs-lookup"><span data-stu-id="946be-286">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="946be-287">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="946be-287">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Konsolen-API-Referenz"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir – Konsolen-API-Referenz"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "So unterbrechen Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Beschleunigen der JavaScript-Runtime"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problem 1050237: debug(function) funktioniert nicht | Monorail"  

> [!NOTE]
> <span data-ttu-id="946be-297">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="946be-297">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="946be-298">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/utilities) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="946be-298">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="946be-300">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="946be-300">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

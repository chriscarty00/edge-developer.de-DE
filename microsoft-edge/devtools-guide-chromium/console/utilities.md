---
title: API-Referenz für Konsolen Dienstprogramme
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 28b40f3f79928725d3d49418e01cf02247224370
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601796"
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





# <span data-ttu-id="011b2-103">API-Referenz für Konsolen Dienstprogramme</span><span class="sxs-lookup"><span data-stu-id="011b2-103">Console Utilities API Reference</span></span>   



<span data-ttu-id="011b2-104">Die API für Konsolen Dienstprogramme enthält eine Sammlung von praktischen Befehlen zum Ausführen allgemeiner Aufgaben: auswählen und Überprüfen von DOM-Elementen, Anzeigen von Daten im lesbaren Format, beenden und Starten des Profilers sowie überwachen von DOM-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="011b2-104">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="011b2-105">Die folgenden Befehle funktionieren nur in der Microsoft Edge devtools-Konsole.</span><span class="sxs-lookup"><span data-stu-id="011b2-105">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="011b2-106">Die Befehle funktionieren nicht, wenn Sie aus Ihren Skripts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="011b2-106">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="011b2-107">Suchen Sie `console.log()` nach `console.error()` und die restlichen `console.*` Methoden?</span><span class="sxs-lookup"><span data-stu-id="011b2-107">Looking for `console.log()`, `console.error()`, and the rest of the `console.*` methods?</span></span>  <span data-ttu-id="011b2-108">Siehe [API-Referenz][DevToolsConsoleApi]für die Konsole.</span><span class="sxs-lookup"><span data-stu-id="011b2-108">See [Console API Reference][DevToolsConsoleApi].</span></span>  

## <span data-ttu-id="011b2-109">Kürzlich ausgewerteter Ausdruck</span><span class="sxs-lookup"><span data-stu-id="011b2-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="011b2-110">Gibt den Wert des zuletzt ausgewerteten Ausdrucks zurück.</span><span class="sxs-lookup"><span data-stu-id="011b2-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="011b2-111">In [Abbildung 1](#figure-1)wird ein einfacher Ausdruck \ ( `2 + 2` \) ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="011b2-111">In [Figure 1](#figure-1), a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="011b2-112">`$_`Anschließend wird die Eigenschaft ausgewertet, die den gleichen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="011b2-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

> ##### <span data-ttu-id="011b2-113">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="011b2-113">Figure 1</span></span>  
> `$_` <span data-ttu-id="011b2-114">ist der zuletzt ausgewertete Ausdruck</span><span class="sxs-lookup"><span data-stu-id="011b2-114">is the most recently evaluated expression</span></span>  
> ![$ _ ist der zuletzt ausgewertete Ausdruck][ImageRecentExpression]  

<span data-ttu-id="011b2-116">In [Abbildung 2](#figure-2)enthält der ausgewertete Ausdruck zunächst ein Array von Namen.</span><span class="sxs-lookup"><span data-stu-id="011b2-116">In [Figure 2](#figure-2), the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="011b2-117">Auswerten, `$_.length` um die Länge des Arrays zu ermitteln, wird der Wert, der in Änderungen gespeichert wird, `$_` zum neuesten ausgewerteten Ausdruck `4` .</span><span class="sxs-lookup"><span data-stu-id="011b2-117">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

> ##### <span data-ttu-id="011b2-118">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="011b2-118">Figure 2</span></span>  
> `$_` <span data-ttu-id="011b2-119">ändert sich, wenn neue Befehle ausgewertet werden</span><span class="sxs-lookup"><span data-stu-id="011b2-119">changes when new commands are evaluated</span></span>  
> ![$ _ ändert sich, wenn neue Befehle ausgewertet werden][ImageChangedRecentExpression]  

## <span data-ttu-id="011b2-121">Zuletzt ausgewähltes Element oder JavaScript-Objekt</span><span class="sxs-lookup"><span data-stu-id="011b2-121">Recently Selected Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="011b2-122">Gibt das zuletzt ausgewählte Element oder JavaScript-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="011b2-122">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="011b2-123">Gibt die zweite zuletzt ausgewählte Person zurück usw.</span><span class="sxs-lookup"><span data-stu-id="011b2-123">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="011b2-124">Die `$0` `$1` Befehle,,, und werden `$2` `$3` `$4` als historischer Bezug auf die letzten fünf im Bereich **Elemente** geprüften DOM-Elemente oder die letzten fünf im **Speicher** Bereich ausgewählten JavaScript-Heapobjekte ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="011b2-124">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** panel or the last five JavaScript heap objects selected in the **Memory** panel.</span></span>  

```console
$1
```  

```console
$2
```  

```console
$3
```  

```console
$4
```  

<span data-ttu-id="011b2-125">In [Abbildung 3](#figure-3) `img` wird im Panel **Elemente** ein Element ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="011b2-125">In [Figure 3](#figure-3), an `img` element is selected in the **Elements** panel.</span></span>  <span data-ttu-id="011b2-126">Wurde im **Konsolen** Einzug `$0` ausgewertet und zeigt dasselbe Element an.</span><span class="sxs-lookup"><span data-stu-id="011b2-126">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

> ##### <span data-ttu-id="011b2-127">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="011b2-127">Figure 3</span></span>  
> <span data-ttu-id="011b2-128">Der</span><span class="sxs-lookup"><span data-stu-id="011b2-128">The</span></span> `$0`  
> ![Das $0][ImageElement0]  

<span data-ttu-id="011b2-130">In [Abbildung 4](#figure-4)zeigt das Bild ein anderes Element, das auf der gleichen Seite markiert ist.</span><span class="sxs-lookup"><span data-stu-id="011b2-130">In [Figure 4](#figure-4), the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="011b2-131">Das `$0` jetzt bezieht sich auf das neu ausgewählte Element, `$1` gibt aber die zuvor ausgewählte zurück.</span><span class="sxs-lookup"><span data-stu-id="011b2-131">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

> ##### <span data-ttu-id="011b2-132">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="011b2-132">Figure 4</span></span>  
> <span data-ttu-id="011b2-133">Der</span><span class="sxs-lookup"><span data-stu-id="011b2-133">The</span></span> `$1`  
> ![Das $1][ImageElement1]  

## <span data-ttu-id="011b2-135">Abfrageauswahl</span><span class="sxs-lookup"><span data-stu-id="011b2-135">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="011b2-136">Gibt den Verweis auf das erste DOM-Element mit der angegebenen CSS-Auswahl zurück.</span><span class="sxs-lookup"><span data-stu-id="011b2-136">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="011b2-137">Diese Methode ist ein Alias für die [Document. querySelector ()][MDNDocumentQuerySelector] -Methode.</span><span class="sxs-lookup"><span data-stu-id="011b2-137">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="011b2-138">In [Abbildung 5](#figure-5)wird ein Verweis auf das erste `<img>` Element im Dokument zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="011b2-138">In [Figure 5](#figure-5), a reference to the first `<img>` element in the document is returned.</span></span>  

> ##### <span data-ttu-id="011b2-139">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="011b2-139">Figure 5</span></span>  
> <span data-ttu-id="011b2-140">Der</span><span class="sxs-lookup"><span data-stu-id="011b2-140">The</span></span> `$('img')`  
> ![$ (' Img ')][ImageElementImg]  

<span data-ttu-id="011b2-142">Klicken Sie mit der rechten Maustaste auf das zurückgegebene Ergebnis, und wählen Sie **im Element Fenster** anzeigen aus, um es im Dom zu finden, oder **Scrollen Sie zur Ansicht** , um es auf der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="011b2-142">Right-click on the returned result and select **Reveal in Elements Panel** to find it in the DOM, or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="011b2-143">In [Abbildung 6](#figure-6)wird ein Verweis auf das aktuell ausgewählte Element zurückgegeben, und die src-Eigenschaft wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="011b2-143">In [Figure 6](#figure-6), a reference to the currently selected element is returned and the src property is displayed.</span></span>  

> ##### <span data-ttu-id="011b2-144">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="011b2-144">Figure 6</span></span>  
> <span data-ttu-id="011b2-145">Der</span><span class="sxs-lookup"><span data-stu-id="011b2-145">The</span></span> `$('img').src`  
> ![$ (' Img '). src][ImageElementImgSource]  

<span data-ttu-id="011b2-147">Diese Methode unterstützt auch einen zweiten Parameter, startNode, der ein "Element" oder einen Knoten angibt, aus dem nach Elementen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="011b2-147">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="011b2-148">Der Standardwert für diesen Parameter ist `document` .</span><span class="sxs-lookup"><span data-stu-id="011b2-148">The default value of this parameter is `document`.</span></span>  

<span data-ttu-id="011b2-149">In [Abbildung 7](#figure-7) `img` befindet sich das erste Element nach dem `title--image` und zeigt die `src` ordnungsgemäße Rückgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="011b2-149">In [Figure 7](#figure-7), the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

> ##### <span data-ttu-id="011b2-150">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="011b2-150">Figure 7</span></span>  
> <span data-ttu-id="011b2-151">Der $ (' img ', Document. querySelector (' Titel--Bild ')). src</span><span class="sxs-lookup"><span data-stu-id="011b2-151">The $('img', document.querySelector('title--image')).src</span></span>  
> ![Der $ (' img ', Document. querySelector (' Titel--Bild ')). src][ImageElementImgNodeSource]  

> [!NOTE]
> <span data-ttu-id="011b2-153">Wenn Sie eine Bibliothek wie jQuery verwenden, die verwendet wird `$` , wird diese Funktionalität überschrieben und `$` entspricht der Implementierung aus dieser Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="011b2-153">If you are using a library such as jQuery that uses `$`, this functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <span data-ttu-id="011b2-154">Abfrageauswahl alle</span><span class="sxs-lookup"><span data-stu-id="011b2-154">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="011b2-155">Gibt ein Array von Elementen zurück, die der angegebenen CSS-Auswahl entsprechen.</span><span class="sxs-lookup"><span data-stu-id="011b2-155">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="011b2-156">Diese Methode entspricht dem Aufrufen der [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] -Methode.</span><span class="sxs-lookup"><span data-stu-id="011b2-156">This method is equivalent to calling the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="011b2-157">In [Abbildung 8](#figure-8)verwenden Sie, `$$()` um ein Array aller `<img>` Elemente im aktuellen Dokument zu erstellen und den Wert der `src` Eigenschaft für jedes Element anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="011b2-157">In [Figure 8](#figure-8), use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

> ##### <span data-ttu-id="011b2-158">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="011b2-158">Figure 8</span></span>  
> <span data-ttu-id="011b2-159">Verwenden `$$()` , um alle Bilder im Dokument auszuwählen und die Quellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="011b2-159">Using `$$()` to select all images in the document and display the sources</span></span>  
> ![Verwenden von $ $ (), um alle Bilder im Dokument auszuwählen und die Quellen anzuzeigen][ImageArrayElementImgSource]  

<span data-ttu-id="011b2-161">Diese Methode unterstützt auch einen zweiten Parameter, startNode, der ein Element oder einen Knoten angibt, aus dem nach Elementen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="011b2-161">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="011b2-162">Der Standardwert für diesen Parameter ist `document` .</span><span class="sxs-lookup"><span data-stu-id="011b2-162">The default value of this parameter is `document`.</span></span>  

<span data-ttu-id="011b2-163">In [Abbildung 9](#figure-9)wird eine geänderte Version von [Abbildung 8](#figure-8) verwendet `$$()` , um ein Array aller Elemente zu erstellen `<img>` , die im aktuellen Dokument nach dem ausgewählten Knoten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="011b2-163">In [Figure 9](#figure-9), a modified version of [Figure 8](#figure-8) uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

> ##### <span data-ttu-id="011b2-164">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="011b2-164">Figure 9</span></span>  
> <span data-ttu-id="011b2-165">Verwenden `$$()` zum Auswählen aller Bilder, die nach dem angegebenen `<div>` Element im Dokument angezeigt werden, und Anzeigen der Quellen</span><span class="sxs-lookup"><span data-stu-id="011b2-165">Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
> ![Verwenden von $ $ (), um alle Bilder auszuwählen, die nach dem angegebenen <div->-Element im Dokument angezeigt werden, und Anzeigen der Quellen][ImageArrayElementImgNodeSource]  

> [!NOTE]
> <span data-ttu-id="011b2-167">Drücken Sie `Shift` + `Enter` in der Konsole, um eine neue Zeile zu starten, ohne das Skript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="011b2-167">Press `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <span data-ttu-id="011b2-168">XPath</span><span class="sxs-lookup"><span data-stu-id="011b2-168">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="011b2-169">Gibt ein Array von DOM-Elementen zurück, die dem angegebenen XPath-Ausdruck entsprechen.</span><span class="sxs-lookup"><span data-stu-id="011b2-169">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="011b2-170">In [Abbildung 10](#figure-10) `<p>` werden alle Elemente auf der Seite zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="011b2-170">In [Figure 10](#figure-10), all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

> ##### <span data-ttu-id="011b2-171">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="011b2-171">Figure 10</span></span>  
> <span data-ttu-id="011b2-172">Verwenden einer XPath-Auswahl</span><span class="sxs-lookup"><span data-stu-id="011b2-172">Using an XPath selector</span></span>  
> ![Verwenden einer XPath-Auswahl][ImageArrayXpath]  

<span data-ttu-id="011b2-174">In [Abbildung 11](#figure-11) `<p>` werden alle Elemente zurückgegeben, die `<a>` Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="011b2-174">In [Figure 11](#figure-11), all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

> ##### <span data-ttu-id="011b2-175">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="011b2-175">Figure 11</span></span>  
> <span data-ttu-id="011b2-176">Verwenden einer komplexeren XPath-Auswahl</span><span class="sxs-lookup"><span data-stu-id="011b2-176">Using a more complicated XPath selector</span></span>  
> ![Verwenden einer komplexeren XPath-Auswahl][ImageArrayXpathChild]  

<span data-ttu-id="011b2-178">Ähnlich wie bei den anderen Auswahlbefehlen `$x(path)` verfügt ein optionaler zweiter Parameter, der `startNode` ein Element oder einen Knoten angibt, aus dem nach Elementen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="011b2-178">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

> ##### <span data-ttu-id="011b2-179">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="011b2-179">Figure 12</span></span>  
> <span data-ttu-id="011b2-180">Verwenden einer XPath-Auswahl mit</span><span class="sxs-lookup"><span data-stu-id="011b2-180">Using an XPath selector with</span></span> `startNode`  
> ![Verwenden einer XPath-Auswahl mit startNode][ImageArrayXpathNode]  

## <span data-ttu-id="011b2-182">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="011b2-182">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="011b2-183">Löscht die Konsole des Verlaufs.</span><span class="sxs-lookup"><span data-stu-id="011b2-183">Clears the console of the history.</span></span>  

```console
clear()
```  

## <span data-ttu-id="011b2-184">copy</span><span class="sxs-lookup"><span data-stu-id="011b2-184">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="011b2-185">Die `copy(object)` Methode kopiert eine Zeichenfolgendarstellung des angegebenen Objekts in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="011b2-185">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <span data-ttu-id="011b2-186">debuggen</span><span class="sxs-lookup"><span data-stu-id="011b2-186">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="011b2-187">Das [Chrom Problem #1050237][MonorailIssue1050237] verfolgt einen Fehler mit der `debug()` Funktion.</span><span class="sxs-lookup"><span data-stu-id="011b2-187">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="011b2-188">Wenn dieses Problem auftritt, versuchen Sie stattdessen, [Haltepunkte zu verwenden][DevtoolsJavascriptBreakpoints] .</span><span class="sxs-lookup"><span data-stu-id="011b2-188">If you encounter this issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="011b2-189">Wenn Sie die angegebene Methode anfordern, wird der Debugger aufgerufen und innerhalb der Methode im Bereich " **Quellen** " unterbricht, sodass Sie den Code schrittweise durchlaufen und Debuggen können.</span><span class="sxs-lookup"><span data-stu-id="011b2-189">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** panel allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

> ##### <span data-ttu-id="011b2-190">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="011b2-190">Figure 13</span></span>  
> <span data-ttu-id="011b2-191">Durchbrechen innerhalb einer Methode mit</span><span class="sxs-lookup"><span data-stu-id="011b2-191">Breaking inside a method with</span></span> `debug()`  
> ![Durchbrechen innerhalb einer Methode mit Debug ()][ImageDebugMethod]  

<span data-ttu-id="011b2-193">Verwenden Sie diese Option, `undebug(method)` um die Unterbrechung der Methode zu beenden, oder verwenden Sie die Benutzeroberfläche, um alle Haltepunkte zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="011b2-193">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="011b2-194">Weitere Informationen zu Haltepunkten finden Sie unter [Anhalten des Codes mit Haltepunkten][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="011b2-194">For more information on breakpoints, see [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <span data-ttu-id="011b2-195">dir</span><span class="sxs-lookup"><span data-stu-id="011b2-195">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="011b2-196">Zeigt eine Objektstil Auflistung aller Eigenschaften für das angegebene Objekt an.</span><span class="sxs-lookup"><span data-stu-id="011b2-196">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="011b2-197">Diese Methode ist ein Alias für die [Console. dir ()][MDNConsoleDir] -Methode.</span><span class="sxs-lookup"><span data-stu-id="011b2-197">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="011b2-198">Werten `document.head` Sie in der Konsole aus, um den HTML-Code zwischen den `<head>` und- `</head>` Tags anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="011b2-198">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="011b2-199">In [Abbildung 14](#figure-14)wird nach `console.dir()` der Verwendung in der Konsole ein Objektformat Eintrag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="011b2-199">In [Figure 14](#figure-14), an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

> ##### <span data-ttu-id="011b2-200">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="011b2-200">Figure 14</span></span>  
> <span data-ttu-id="011b2-201">Protokollierung `document.head` mit `dir()` Methode</span><span class="sxs-lookup"><span data-stu-id="011b2-201">Logging `document.head` with `dir()` method</span></span>  
> ![Protokollierungs Dokument. Head mit dir ()-Methode][ImageLogObject]  

<span data-ttu-id="011b2-203">Weitere Informationen finden Sie im [`console.dir()`][DevToolsConsoleApiConsoleDirObject] Eintrag in der Konsolen-API.</span><span class="sxs-lookup"><span data-stu-id="011b2-203">For more information, see the [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <span data-ttu-id="011b2-204">DirXML</span><span class="sxs-lookup"><span data-stu-id="011b2-204">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="011b2-205">Druckt eine XML-Darstellung des angegebenen Objekts, wie auf der Registerkarte **Elemente** zu sehen ist.  Diese Methode entspricht der [Console. DirXML ()][MDNConsoleDirxml] -Methode.</span><span class="sxs-lookup"><span data-stu-id="011b2-205">Prints an XML representation of the specified object, as seen in the **Elements** tab.  This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <span data-ttu-id="011b2-206">prüfen</span><span class="sxs-lookup"><span data-stu-id="011b2-206">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="011b2-207">Das angegebene Element oder Objekt wird in der entsprechenden Leiste geöffnet und markiert: entweder der **Element Panel für** DOM-Elemente oder der **Speicher** Panel für JavaScript-Heapobjekte.</span><span class="sxs-lookup"><span data-stu-id="011b2-207">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** panel for DOM elements or the **Memory** panel for JavaScript heap objects.</span></span>  

<span data-ttu-id="011b2-208">In [Abbildung 15](#figure-15)wird das `document.body` im **Element** Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="011b2-208">In [Figure 15](#figure-15), the `document.body` opens in the **Elements** panel.</span></span>  

```console
inspect(document.body);
```  

> ##### <span data-ttu-id="011b2-209">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="011b2-209">Figure 15</span></span>  
> <span data-ttu-id="011b2-210">Überprüfen eines Elements mit</span><span class="sxs-lookup"><span data-stu-id="011b2-210">Inspecting an element with</span></span> `inspect()`  
> ![Überprüfen eines Elements mit Inspect ()][ImageInspectElement]  

<span data-ttu-id="011b2-212">Beim Übergeben einer zu überprüfenden Methode wird das Dokument im **Quellen** Panel geöffnet, damit Sie es überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="011b2-212">When passing a method to inspect, the method opens the document up in the **Sources** panel for you to inspect.</span></span>  

## <span data-ttu-id="011b2-213">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="011b2-213">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="011b2-214">Gibt die für das angegebene Objekt registrierten Ereignislistener zurück.</span><span class="sxs-lookup"><span data-stu-id="011b2-214">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="011b2-215">Der Rückgabewert ist ein Objekt, das für jeden registrierten Ereignistyp \ (wie `click` oder \) ein Array enthält `keydown` .</span><span class="sxs-lookup"><span data-stu-id="011b2-215">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="011b2-216">Die Mitglieder jedes Arrays sind Objekte, die den für jeden Typ registrierten Listener beschreiben.</span><span class="sxs-lookup"><span data-stu-id="011b2-216">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="011b2-217">In [Abbildung 16](#figure-16)werden alle Ereignislistener aufgelistet, die für das Document-Objekt registriert sind.</span><span class="sxs-lookup"><span data-stu-id="011b2-217">In [Figure 16](#figure-16), all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

> ##### <span data-ttu-id="011b2-218">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="011b2-218">Figure 16</span></span>  
> <span data-ttu-id="011b2-219">Ausgabe der Verwendung</span><span class="sxs-lookup"><span data-stu-id="011b2-219">Output of using</span></span> `getEventListeners(document)`  
> ![Ausgabe der Verwendung von getEventListeners (Dokument)][ImageGetListeners]  

<span data-ttu-id="011b2-221">Wenn mehr als ein Listener für das angegebene Objekt registriert ist, enthält das Array ein Element für jeden Listener.</span><span class="sxs-lookup"><span data-stu-id="011b2-221">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="011b2-222">In [Abbildung 16](#figure-16)sind zwei Ereignis-Listener für das Dokumentelement für das Ereignis registriert `click` .</span><span class="sxs-lookup"><span data-stu-id="011b2-222">In [Figure 16](#figure-16), there are two event listeners registered on the document element for the `click` event.</span></span>  

> ##### <span data-ttu-id="011b2-223">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="011b2-223">Figure 17</span></span>  
> <span data-ttu-id="011b2-224">Mehrere Listener</span><span class="sxs-lookup"><span data-stu-id="011b2-224">Multiple listeners</span></span>  
> ![Mehrere Listener][ImageMultipleListeners]  

<span data-ttu-id="011b2-226">Sie können jedes der folgenden Objekte erweitern, um die Eigenschaften zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="011b2-226">You may further expand each of the following objects to explore the properties.</span></span>  

> ##### <span data-ttu-id="011b2-227">Abbildung 18</span><span class="sxs-lookup"><span data-stu-id="011b2-227">Figure 18</span></span>  
> <span data-ttu-id="011b2-228">Erweiterte Ansicht des Listener-Objekts</span><span class="sxs-lookup"><span data-stu-id="011b2-228">Expanded view of listener object</span></span>  
> ![Erweiterte Ansicht des Listener-Objekts][ImageListenersExpanded]  

## <span data-ttu-id="011b2-230">Tasten</span><span class="sxs-lookup"><span data-stu-id="011b2-230">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="011b2-231">Gibt ein Array zurück, das die Namen der Eigenschaften enthält, die zum angegebenen Objekt gehören.</span><span class="sxs-lookup"><span data-stu-id="011b2-231">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="011b2-232">Um die zugeordneten Werte der gleichen Eigenschaften abzurufen, verwenden Sie `values()` .</span><span class="sxs-lookup"><span data-stu-id="011b2-232">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="011b2-233">Angenommen, Ihre Anwendung hat das folgende Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="011b2-233">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

<span data-ttu-id="011b2-234">In [Abbildung 19](#figure-19)wurde davon ausgegangen, dass das Ergebnis `player1` vor der Eingabe `keys(player1)` und in der Konsole im globalen Namespace \ (zur Vereinfachung \) definiert wurde `values(player1)` .</span><span class="sxs-lookup"><span data-stu-id="011b2-234">In [Figure 19](#figure-19), the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)
```  

```console
values(player1)
```  

> ##### <span data-ttu-id="011b2-235">Abbildung 19</span><span class="sxs-lookup"><span data-stu-id="011b2-235">Figure 19</span></span>  
> <span data-ttu-id="011b2-236">Die `keys()` `values()` Befehle und</span><span class="sxs-lookup"><span data-stu-id="011b2-236">The `keys()` and `values()` commands</span></span>  
> ![Die Befehle "Keys ()" und "Values ()"][ImageConsoleKeysValues]  

## <span data-ttu-id="011b2-238">Monitor</span><span class="sxs-lookup"><span data-stu-id="011b2-238">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="011b2-239">Protokolliert eine Nachricht an die Konsole, die den Methodennamen zusammen mit den Argumenten angibt, die beim Aufrufen an die Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="011b2-239">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

> ##### <span data-ttu-id="011b2-240">Abbildung 20</span><span class="sxs-lookup"><span data-stu-id="011b2-240">Figure 20</span></span>  
> <span data-ttu-id="011b2-241">Die `monitor()` Methode</span><span class="sxs-lookup"><span data-stu-id="011b2-241">The `monitor()` method</span></span>  
> ![Die Monitor ()-Methode][ImageConsoleMonitorSum]  

<span data-ttu-id="011b2-243">Verwenden Sie diese Einstellung `unmonitor(method)` , um die Überwachung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="011b2-243">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <span data-ttu-id="011b2-244">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="011b2-244">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="011b2-245">Wenn eines der angegebenen Ereignisse für das angegebene Objekt eintritt, wird das Ereignisobjekt in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="011b2-245">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="011b2-246">Sie können ein einzelnes Ereignis angeben, das überwacht werden soll, ein Array von Ereignissen oder einen der generischen Ereignistypen, die einer vordefinierten Sammlung von Ereignissen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="011b2-246">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="011b2-247">Siehe [Abbildung 21](#figure-21).</span><span class="sxs-lookup"><span data-stu-id="011b2-247">See [Figure 21](#figure-21).</span></span>  

<span data-ttu-id="011b2-248">Im folgenden werden alle Größen Änderungsereignisse für das Window-Objekt überwacht.</span><span class="sxs-lookup"><span data-stu-id="011b2-248">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

> ##### <span data-ttu-id="011b2-249">Abbildung 21</span><span class="sxs-lookup"><span data-stu-id="011b2-249">Figure 21</span></span>  
> <span data-ttu-id="011b2-250">Überwachen von Fenstergrößen Ereignissen</span><span class="sxs-lookup"><span data-stu-id="011b2-250">Monitoring window resize events</span></span>  
> ![Überwachen von Fenstergrößen Ereignissen][ImageMonitorResize]  

<span data-ttu-id="011b2-252">Im folgenden wird ein Array zum Überwachen `resize` von beiden und `scroll` Ereignissen für das Window-Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="011b2-252">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="011b2-253">Sie können auch einen der verfügbaren Arten von Ereignissen angeben, Zeichenfolgen, die vordefinierten Gruppen von Ereignissen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="011b2-253">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="011b2-254">In der folgenden Tabelle werden die verfügbaren Ereignistypen und die zugehörigen Ereigniszuordnungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="011b2-254">The table below displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="011b2-255">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="011b2-255">Event type</span></span> | <span data-ttu-id="011b2-256">Entsprechende zugeordnete Ereignisse</span><span class="sxs-lookup"><span data-stu-id="011b2-256">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="011b2-257">"klicken", "DblClick", "MouseDown", "MouseMove", "Mouse Out", "MouseOver", "MouseUp", "Mausrad"</span><span class="sxs-lookup"><span data-stu-id="011b2-257">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="011b2-258">"KeyDown"; "keypress"; "KeyUp"; "TextInput"</span><span class="sxs-lookup"><span data-stu-id="011b2-258">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="011b2-259">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="011b2-259">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="011b2-260">"Blur"; "ändern"; "Fokus"; "Zurücksetzen"; "Größe"; "Scrollen"; "auswählen"; "Absenden"; "Zoom"</span><span class="sxs-lookup"><span data-stu-id="011b2-260">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="011b2-261">In [Abbildung 22](#figure-22)ist der `key` Ereignistyp, der `key` Ereignissen in einem Eingabetextfeld entspricht, aktuell im Bereich **Elemente** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="011b2-261">In [Figure 22](#figure-22), the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** panel.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="011b2-262">In [Abbildung 22](#figure-22) wird die Beispielausgabe nach dem Eingeben eines Zeichens in das Textfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="011b2-262">In [Figure 22](#figure-22) the sample output after typing a character in the text field is displayed.</span></span>  

> ##### <span data-ttu-id="011b2-263">Abbildung 22</span><span class="sxs-lookup"><span data-stu-id="011b2-263">Figure 22</span></span>  
> <span data-ttu-id="011b2-264">Überwachen von Schlüsselereignissen</span><span class="sxs-lookup"><span data-stu-id="011b2-264">Monitoring key events</span></span>  
> ![Überwachen von Schlüsselereignissen][ImageMonitorKey]  

## <span data-ttu-id="011b2-266">profile</span><span class="sxs-lookup"><span data-stu-id="011b2-266">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="011b2-267">Startet eine JavaScript-CPU-Profilerstellungssitzung mit einem optionalen Namen.</span><span class="sxs-lookup"><span data-stu-id="011b2-267">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="011b2-268">Die [profileEnd ()](#profileend) -Methode vervollständigt das Profil und zeigt die Ergebnisse im **Speicher** Panel an.</span><span class="sxs-lookup"><span data-stu-id="011b2-268">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** panel.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="011b2-269">Führen `profile()` Sie die Methode aus, um die Profilerstellung zu starten.</span><span class="sxs-lookup"><span data-stu-id="011b2-269">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="011b2-270">Führen Sie die [profileEnd ()](#profileend) -Methode aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speicher** Panel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="011b2-270">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** panel.</span></span>  

<span data-ttu-id="011b2-271">Profile können auch geschachtelt sein.</span><span class="sxs-lookup"><span data-stu-id="011b2-271">Profiles may also be nested.</span></span>  <span data-ttu-id="011b2-272">In [Abbildung 23](#figure-23) ist das Ergebnis unabhängig von der Reihenfolge identisch.</span><span class="sxs-lookup"><span data-stu-id="011b2-272">In [Figure 23](#figure-23) the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="011b2-273">Mehrere CPU-Profile können gleichzeitig ausgeführt werden, und es ist nicht erforderlich, jede Person in der Erstellungsreihenfolge zu schließen.</span><span class="sxs-lookup"><span data-stu-id="011b2-273">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="011b2-274">profileEnd</span><span class="sxs-lookup"><span data-stu-id="011b2-274">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="011b2-275">Schließt eine JavaScript-CPU-Profilerstellungssitzung ab und zeigt die Ergebnisse im **Speicher** Panel an.</span><span class="sxs-lookup"><span data-stu-id="011b2-275">Completes a JavaScript CPU profiling session and displays the results in the **Memory** panel.</span></span>  <span data-ttu-id="011b2-276">Sie müssen die [profile ()](#profile) -Methode ausführen.</span><span class="sxs-lookup"><span data-stu-id="011b2-276">You must be running the [profile()](#profile) method.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="011b2-277">Führen Sie die [profile ()](#profile) -Methode aus, um die Profilerstellung zu starten.</span><span class="sxs-lookup"><span data-stu-id="011b2-277">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="011b2-278">Führen `profileEnd()` Sie die Methode aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speicher** Panel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="011b2-278">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** panel.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="011b2-279">Profile können auch geschachtelt sein.</span><span class="sxs-lookup"><span data-stu-id="011b2-279">Profiles may also be nested.</span></span>  <span data-ttu-id="011b2-280">In [Abbildung 23](#figure-23) ist das Ergebnis unabhängig von der Reihenfolge identisch.</span><span class="sxs-lookup"><span data-stu-id="011b2-280">In [Figure 23](#figure-23) the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="011b2-281">Das Ergebnis wird als Heap-Momentaufnahme im **Speicher** Panel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="011b2-281">The result appears as a Heap Snapshot in the **Memory** panel.</span></span>  

> ##### <span data-ttu-id="011b2-282">Abbildung 23</span><span class="sxs-lookup"><span data-stu-id="011b2-282">Figure 23</span></span>  
> <span data-ttu-id="011b2-283">Gruppierte profile</span><span class="sxs-lookup"><span data-stu-id="011b2-283">Grouped profiles</span></span>  
> ![Gruppierte profile][ImageGroupedProfiles]  

> [!NOTE]
> <span data-ttu-id="011b2-285">Mehrere CPU-Profile können gleichzeitig ausgeführt werden, und es ist nicht erforderlich, jede Person in der Erstellungsreihenfolge zu schließen.</span><span class="sxs-lookup"><span data-stu-id="011b2-285">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="011b2-286">Tabelle</span><span class="sxs-lookup"><span data-stu-id="011b2-286">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="011b2-287">Protokolliert Objektdaten mit Tabellenformatierung basierend auf dem Datenobjekt mit optionalen Spaltenüberschriften.</span><span class="sxs-lookup"><span data-stu-id="011b2-287">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="011b2-288">In [Abbildung 24](#figure-24)wird eine Liste mit Namen angezeigt, die eine Tabelle in der Konsole verwenden.</span><span class="sxs-lookup"><span data-stu-id="011b2-288">In [Figure 24](#figure-24), a list of names using a table in the console is displayed.</span></span>  

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

> ##### <span data-ttu-id="011b2-289">Abbildung 24</span><span class="sxs-lookup"><span data-stu-id="011b2-289">Figure 24</span></span>  
> <span data-ttu-id="011b2-290">Die `table()` Methode</span><span class="sxs-lookup"><span data-stu-id="011b2-290">The `table()` method</span></span>  
> ![Die Table ()-Methode][ImageConsoleTable]  

## <span data-ttu-id="011b2-292">undebug</span><span class="sxs-lookup"><span data-stu-id="011b2-292">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="011b2-293">Beendet das Debuggen der angegebenen Methode, sodass der Debugger beim Aufrufen der Methode nicht mehr aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="011b2-293">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <span data-ttu-id="011b2-294">Unmonitor</span><span class="sxs-lookup"><span data-stu-id="011b2-294">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="011b2-295">Beendet die Überwachung der angegebenen Methode.</span><span class="sxs-lookup"><span data-stu-id="011b2-295">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="011b2-296">Dies wird in Concert mit der [Monitor ()](#monitor) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="011b2-296">This is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <span data-ttu-id="011b2-297">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="011b2-297">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="011b2-298">Beendet das Überwachen von Ereignissen für das angegebene Objekt und die Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="011b2-298">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="011b2-299">Im folgenden Beispiel werden alle Ereignisüberwachungen für das Window-Objekt angehalten.</span><span class="sxs-lookup"><span data-stu-id="011b2-299">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="011b2-300">Sie können auch selektiv die Überwachung bestimmter Ereignisse für ein Objekt beenden.</span><span class="sxs-lookup"><span data-stu-id="011b2-300">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="011b2-301">Mit dem folgenden Code wird beispielsweise das Überwachen aller `mouse` Ereignisse für das aktuell ausgewählte Element gestartet und dann die Überwachung von `mousemove` Ereignissen beendet \ (vielleicht, um Rauschen in der Konsolenausgabe zu verringern \).</span><span class="sxs-lookup"><span data-stu-id="011b2-301">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <span data-ttu-id="011b2-302">Werte</span><span class="sxs-lookup"><span data-stu-id="011b2-302">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="011b2-303">Gibt ein Array zurück, das die Werte aller Eigenschaften enthält, die zum angegebenen Objekt gehören.</span><span class="sxs-lookup"><span data-stu-id="011b2-303">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

<!--   -->  



<!-- image links -->  

[ImageRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-arithmatic.msft.png "Abbildung 1: $ _ ist der zuletzt ausgewertete Ausdruck"  
[ImageChangedRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-array-length.msft.png "Abbildung 2: $ _ ändert sich, wenn neue Befehle ausgewertet werden"  
[ImageElement0]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$0.msft.png "Abbildung 3: die $0"  
[ImageElement1]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$1.msft.png "Abbildung 4: die $1"  
[ImageElementImg]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image.msft.png "Abbildung 5: $ (' img ')"  
[ImageElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-source.msft.png "Abbildung 6: $ (' img '). src"  
[ImageElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-source.msft.png "Abbildung 7: $ (' img ', Document. querySelector (' Titel--Bild ')). src"  
[ImageArrayElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-all.msft.png "Abbildung 8: Verwenden von $ $ () zum Auswählen aller Bilder im Dokument und Anzeigen der Quellen"  
[ImageArrayElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-all.msft.png "Abbildung 9: Verwenden von $ $ () zum Auswählen aller Bilder, die nach dem angegebenen <div->-Element im Dokument angezeigt werden, und Anzeigen der Quellen"  
[ImageArrayXpath]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath.msft.png "Abbildung 10: Verwenden einer XPath-Auswahl"  
[ImageArrayXpathChild]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-sub-element.msft.png "Abbildung 11: Verwenden einer komplexeren XPath-Auswahl"  
[ImageArrayXpathNode]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-startnode.msft.png "Abbildung 12: Verwenden einer XPath-Auswahl mit startNode"  
[ImageDebugMethod]: /microsoft-edge/devtools-guide-chromium/media/console-debug-text.msft.png "Abbildung 13: durchbrechen innerhalb einer Methode mit Debug ()"  
[ImageLogObject]: /microsoft-edge/devtools-guide-chromium/media/console-dir-document-head-expanded.msft.png "Abbildung 14: Protokollieren von Document. Body mit dir ()-Methode"  
[ImageInspectElement]: /microsoft-edge/devtools-guide-chromium/media/console-inspect-document-body.msft.png "Abbildung 15: Überprüfen eines Elements mit Inspect ()"  
[ImageGetListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document.msft.png "Abbildung 16: Ausgabe der Verwendung von getEventListeners (Dokument)"  
[ImageMultipleListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png "Abbildung 17: mehrere Listener"  
[ImageListenersExpanded]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png "Abbildung 18: Erweiterte Ansicht des Listener-Objekts"  
[ImageConsoleKeysValues]: /microsoft-edge/devtools-guide-chromium/media/console-keys-values.msft.png "Abbildung 19: die Befehle "Keys ()" und "Values ()""  
[ImageConsoleMonitorSum]: /microsoft-edge/devtools-guide-chromium/media/console-function-monitor-sum.msft.png "Abbildung 20: die Monitor ()-Methode"  
[ImageMonitorResize]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-resize-window.msft.png "Abbildung 21: Überwachen von Fenstergrößen Ereignissen"  
[ImageMonitorKey]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-type-t-y.msft.png "Abbildung 22: Überwachen von Schlüsselereignissen"  
[ImageGroupedProfiles]: /microsoft-edge/devtools-guide-chromium/media/console-memory-multiple-cpu-profiles.msft.png "Abbildung 23: gruppierte profile"  
[ImageConsoleTable]: /microsoft-edge/devtools-guide-chromium/media/console-table-display.msft.png "Abbildung 24: die Tabelle ()-Methode"  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Konsolen-API-Referenz"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir-Console-API-Referenz"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Beschleunigen der JavaScript-Laufzeit"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console. dir () | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console. DirXML () | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document. querySelector () | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document. querySelectorAll () | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problem 1050237: Debuggen (Funktion) funktioniert nicht | Monorail"  

> [!NOTE]
> <span data-ttu-id="011b2-337">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="011b2-337">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="011b2-338">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/utilities) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="011b2-338">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="011b2-340">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="011b2-340">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

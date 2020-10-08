---
description: Eine Referenz zu den in der Microsoft Edge devtools-Konsole verfügbaren Convenience-Befehlen.
title: API-Referenz für Konsolen Dienstprogramme
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 2882d980e6da45072cab4b028ceb1838a9078064
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993107"
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

# <span data-ttu-id="58a49-104">API-Referenz für Konsolen Dienstprogramme</span><span class="sxs-lookup"><span data-stu-id="58a49-104">Console Utilities API Reference</span></span>  

<span data-ttu-id="58a49-105">Die API für Konsolen Dienstprogramme enthält eine Sammlung von praktischen Befehlen zum Ausführen allgemeiner Aufgaben: auswählen und Überprüfen von DOM-Elementen, Anzeigen von Daten im lesbaren Format, beenden und Starten des Profilers sowie überwachen von DOM-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="58a49-105">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="58a49-106">Die folgenden Befehle funktionieren nur in der Microsoft Edge devtools-Konsole.</span><span class="sxs-lookup"><span data-stu-id="58a49-106">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="58a49-107">Die Befehle funktionieren nicht, wenn Sie aus Ihren Skripts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="58a49-107">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="58a49-108">Suchen Sie `console.log()` nach `console.error()` und die restlichen `console.*` Methoden?</span><span class="sxs-lookup"><span data-stu-id="58a49-108">Looking for `console.log()`, `console.error()`, and the rest of the `console.*` methods?</span></span>  <span data-ttu-id="58a49-109">Siehe [API-Referenz][DevToolsConsoleApi]für die Konsole.</span><span class="sxs-lookup"><span data-stu-id="58a49-109">See [Console API Reference][DevToolsConsoleApi].</span></span>  

## <span data-ttu-id="58a49-110">Kürzlich ausgewerteter Ausdruck</span><span class="sxs-lookup"><span data-stu-id="58a49-110">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="58a49-111">Gibt den Wert des zuletzt ausgewerteten Ausdrucks zurück.</span><span class="sxs-lookup"><span data-stu-id="58a49-111">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="58a49-112">In der folgenden Abbildung wird ein einfacher Ausdruck \ ( `2 + 2` \) ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="58a49-112">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="58a49-113">`$_`Anschließend wird die Eigenschaft ausgewertet, die den gleichen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="58a49-113">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-arithmatic.msft.png":::
   <span data-ttu-id="58a49-115">Abbildung 1:  `$_` ist der zuletzt ausgewertete Ausdruck</span><span class="sxs-lookup"><span data-stu-id="58a49-115">Figure 1:  `$_` is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="58a49-116">In der folgenden Abbildung enthält der ausgewertete Ausdruck zunächst ein Array von Namen.</span><span class="sxs-lookup"><span data-stu-id="58a49-116">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="58a49-117">Auswerten, `$_.length` um die Länge des Arrays zu ermitteln, wird der Wert, der in Änderungen gespeichert wird, `$_` zum neuesten ausgewerteten Ausdruck `4` .</span><span class="sxs-lookup"><span data-stu-id="58a49-117">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-array-length.msft.png":::
   <span data-ttu-id="58a49-119">Abbildung 2:  `$_` Änderungen, wenn neue Befehle ausgewertet werden</span><span class="sxs-lookup"><span data-stu-id="58a49-119">Figure 2:  `$_` changes when new commands are evaluated</span></span>  
:::image-end:::  

## <span data-ttu-id="58a49-120">Zuletzt ausgewähltes Element oder JavaScript-Objekt</span><span class="sxs-lookup"><span data-stu-id="58a49-120">Recently Selected Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="58a49-121">Gibt das zuletzt ausgewählte Element oder JavaScript-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="58a49-121">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="58a49-122">Gibt die zweite zuletzt ausgewählte Person zurück usw.</span><span class="sxs-lookup"><span data-stu-id="58a49-122">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="58a49-123">Die `$0` `$1` Befehle,,, und werden `$2` `$3` `$4` als historischer Bezug auf die letzten fünf im Bereich **Elemente** geprüften DOM-Elemente oder die letzten fünf im **Speicher** Bereich ausgewählten JavaScript-Heapobjekte ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58a49-123">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** panel or the last five JavaScript heap objects selected in the **Memory** panel.</span></span>  

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

<span data-ttu-id="58a49-124">In der folgenden Abbildung ist ein `img` Element im Panel **Elemente** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="58a49-124">In the following figure, an `img` element is selected in the **Elements** panel.</span></span>  <span data-ttu-id="58a49-125">Wurde im **Konsolen** Einzug `$0` ausgewertet und zeigt dasselbe Element an.</span><span class="sxs-lookup"><span data-stu-id="58a49-125">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="58a49-127">Abbildung 3: die</span><span class="sxs-lookup"><span data-stu-id="58a49-127">Figure 3:  The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="58a49-128">In der folgenden Abbildung zeigt das Bild ein anderes Element, das auf der gleichen Seite markiert ist.</span><span class="sxs-lookup"><span data-stu-id="58a49-128">In the following figure, the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="58a49-129">Das `$0` jetzt bezieht sich auf das neu ausgewählte Element, `$1` gibt aber die zuvor ausgewählte zurück.</span><span class="sxs-lookup"><span data-stu-id="58a49-129">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="58a49-131">Abbildung 4: die</span><span class="sxs-lookup"><span data-stu-id="58a49-131">Figure 4:  The</span></span> `$1`  
:::image-end:::  

## <span data-ttu-id="58a49-132">Abfrageauswahl</span><span class="sxs-lookup"><span data-stu-id="58a49-132">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="58a49-133">Gibt den Verweis auf das erste DOM-Element mit der angegebenen CSS-Auswahl zurück.</span><span class="sxs-lookup"><span data-stu-id="58a49-133">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="58a49-134">Diese Methode ist ein Alias für die [Document. querySelector ()][MDNDocumentQuerySelector] -Methode.</span><span class="sxs-lookup"><span data-stu-id="58a49-134">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="58a49-135">In der folgenden Abbildung wird ein Verweis auf das erste `<img>` Element im Dokument zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58a49-135">In the following figure, a reference to the first `<img>` element in the document is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="58a49-137">Abbildung 5: die</span><span class="sxs-lookup"><span data-stu-id="58a49-137">Figure 5:  The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="58a49-138">Zeigen Sie auf das zurückgegebene Ergebnis, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **im Element Panel** anzeigen aus, um es im Dom zu finden, oder **Scrollen Sie in zu Ansicht** , um es auf der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="58a49-138">Hover on the returned result, open the contextual menu \(right-click\), and select **Reveal in Elements Panel** to find it in the DOM or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="58a49-139">In der folgenden Abbildung wird ein Verweis auf das aktuell ausgewählte Element zurückgegeben, und die src-Eigenschaft wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58a49-139">In the following figure, a reference to the currently selected element is returned and the src property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="58a49-141">Abbildung 6: die</span><span class="sxs-lookup"><span data-stu-id="58a49-141">Figure 6:  The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="58a49-142">Diese Methode unterstützt auch einen zweiten Parameter, startNode, der ein "Element" oder einen Knoten angibt, aus dem nach Elementen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="58a49-142">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="58a49-143">Der Standardwert des Parameters ist `document` .</span><span class="sxs-lookup"><span data-stu-id="58a49-143">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="58a49-144">In der folgenden Abbildung `img` befindet sich das erste Element nach dem `title--image` und zeigt die `src` ordnungsgemäße zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="58a49-144">In the following figure, the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="58a49-146">Abbildung 7: die</span><span class="sxs-lookup"><span data-stu-id="58a49-146">Figure 7:  The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="58a49-147">Wenn Sie eine Bibliothek wie jQuery verwenden, die verwendet wird `$` , wird die Funktionalität überschrieben und `$` entspricht der Implementierung aus dieser Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="58a49-147">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <span data-ttu-id="58a49-148">Abfrageauswahl alle</span><span class="sxs-lookup"><span data-stu-id="58a49-148">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="58a49-149">Gibt ein Array von Elementen zurück, die der angegebenen CSS-Auswahl entsprechen.</span><span class="sxs-lookup"><span data-stu-id="58a49-149">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="58a49-150">Diese Methode entspricht dem Aufrufen der [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] -Methode.</span><span class="sxs-lookup"><span data-stu-id="58a49-150">This method is equivalent to calling the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="58a49-151">Verwenden Sie im folgenden Codebeispiel und in der Abbildung `$$()` ein Array aller `<img>` Elemente im aktuellen Dokument, und zeigen Sie den Wert der `src` Eigenschaft für jedes Element an.</span><span class="sxs-lookup"><span data-stu-id="58a49-151">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="58a49-153">Abbildung 8: verwenden `$$()` , um alle Bilder im Dokument auszuwählen und die Quellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="58a49-153">Figure 8:  Using `$$()` to select all images in the document and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="58a49-154">Diese Methode unterstützt auch einen zweiten Parameter, startNode, der ein Element oder einen Knoten angibt, aus dem nach Elementen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="58a49-154">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="58a49-155">Der Standardwert des Parameters ist `document` .</span><span class="sxs-lookup"><span data-stu-id="58a49-155">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="58a49-156">Im folgenden Codebeispiel und in der Abbildung wird eine geänderte Version des vorherigen Codebeispiels und der Abbildung verwendet, `$$()` um ein Array aller `<img>` Elemente zu erstellen, die im aktuellen Dokument nach dem ausgewählten Knoten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="58a49-156">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="58a49-158">Abbildung 9: verwenden `$$()` , um alle Bilder auszuwählen, die nach dem angegebenen `<div>` Element im Dokument angezeigt werden, und Anzeigen der Quellen</span><span class="sxs-lookup"><span data-stu-id="58a49-158">Figure 9:  Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="58a49-159">Drücken Sie `Shift` + `Enter` in der Konsole, um eine neue Zeile zu starten, ohne das Skript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="58a49-159">Press `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <span data-ttu-id="58a49-160">XPath</span><span class="sxs-lookup"><span data-stu-id="58a49-160">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="58a49-161">Gibt ein Array von DOM-Elementen zurück, die dem angegebenen XPath-Ausdruck entsprechen.</span><span class="sxs-lookup"><span data-stu-id="58a49-161">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="58a49-162">Im folgenden Codebeispiel und in der Abbildung `<p>` werden alle Elemente auf der Seite zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58a49-162">In the following code sample and figure, all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="58a49-164">Abbildung 10: Verwenden einer XPath-Auswahl</span><span class="sxs-lookup"><span data-stu-id="58a49-164">Figure 10:  Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="58a49-165">Im folgenden Codebeispiel und in der Abbildung `<p>` werden alle Elemente `<a>` zurückgegeben, die Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="58a49-165">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="58a49-167">Abbildung 11: Verwenden einer komplexeren XPath-Auswahl</span><span class="sxs-lookup"><span data-stu-id="58a49-167">Figure 11:  Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="58a49-168">Ähnlich wie bei den anderen Auswahlbefehlen `$x(path)` verfügt ein optionaler zweiter Parameter, der `startNode` ein Element oder einen Knoten angibt, aus dem nach Elementen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="58a49-168">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="58a49-170">Abbildung 12: Verwenden einer XPath-Auswahl mit</span><span class="sxs-lookup"><span data-stu-id="58a49-170">Figure 12:  Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

## <span data-ttu-id="58a49-171">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="58a49-171">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="58a49-172">Löscht die Konsole des Verlaufs.</span><span class="sxs-lookup"><span data-stu-id="58a49-172">Clears the console of the history.</span></span>  

```console
clear()
```  

## <span data-ttu-id="58a49-173">copy</span><span class="sxs-lookup"><span data-stu-id="58a49-173">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="58a49-174">Die `copy(object)` Methode kopiert eine Zeichenfolgendarstellung des angegebenen Objekts in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="58a49-174">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <span data-ttu-id="58a49-175">debuggen</span><span class="sxs-lookup"><span data-stu-id="58a49-175">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="58a49-176">Das [Chrom Problem #1050237][MonorailIssue1050237] verfolgt einen Fehler mit der `debug()` Funktion.</span><span class="sxs-lookup"><span data-stu-id="58a49-176">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="58a49-177">Wenn das Problem auftritt, versuchen Sie stattdessen, [Haltepunkte zu verwenden][DevtoolsJavascriptBreakpoints] .</span><span class="sxs-lookup"><span data-stu-id="58a49-177">If you encounter the issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="58a49-178">Wenn Sie die angegebene Methode anfordern, wird der Debugger aufgerufen und innerhalb der Methode im Bereich " **Quellen** " unterbricht, sodass Sie den Code schrittweise durchlaufen und Debuggen können.</span><span class="sxs-lookup"><span data-stu-id="58a49-178">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** panel allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="58a49-180">Abbildung 13: durchbrechen innerhalb einer Methode mit</span><span class="sxs-lookup"><span data-stu-id="58a49-180">Figure 13:  Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="58a49-181">Verwenden Sie diese Option, `undebug(method)` um die Unterbrechung der Methode zu beenden, oder verwenden Sie die Benutzeroberfläche, um alle Haltepunkte zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="58a49-181">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="58a49-182">Weitere Informationen zu Haltepunkten finden Sie unter [Anhalten des Codes mit Haltepunkten][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="58a49-182">For more information on breakpoints, see [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <span data-ttu-id="58a49-183">dir</span><span class="sxs-lookup"><span data-stu-id="58a49-183">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="58a49-184">Zeigt eine Objektstil Auflistung aller Eigenschaften für das angegebene Objekt an.</span><span class="sxs-lookup"><span data-stu-id="58a49-184">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="58a49-185">Diese Methode ist ein Alias für die [Console. dir ()][MDNConsoleDir] -Methode.</span><span class="sxs-lookup"><span data-stu-id="58a49-185">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="58a49-186">Werten `document.head` Sie in der Konsole aus, um den HTML-Code zwischen den `<head>` und- `</head>` Tags anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="58a49-186">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="58a49-187">Im folgenden Codebeispiel und in der Abbildung wird nach der Verwendung in der Konsole ein Objektformat Eintrag angezeigt `console.dir()` .</span><span class="sxs-lookup"><span data-stu-id="58a49-187">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="58a49-189">Abbildung 14: Protokollierung `document.head` mit `dir()` Methode</span><span class="sxs-lookup"><span data-stu-id="58a49-189">Figure 14:  Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="58a49-190">Weitere Informationen finden Sie im [`console.dir()`][DevToolsConsoleApiConsoleDirObject] Eintrag in der Konsolen-API.</span><span class="sxs-lookup"><span data-stu-id="58a49-190">For more information, see the [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <span data-ttu-id="58a49-191">DirXML</span><span class="sxs-lookup"><span data-stu-id="58a49-191">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="58a49-192">Druckt eine XML-Darstellung des angegebenen Objekts, wie auf der Registerkarte **Elemente** zu sehen ist.  Diese Methode entspricht der [Console. DirXML ()][MDNConsoleDirxml] -Methode.</span><span class="sxs-lookup"><span data-stu-id="58a49-192">Prints an XML representation of the specified object, as seen in the **Elements** tab.  This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <span data-ttu-id="58a49-193">prüfen</span><span class="sxs-lookup"><span data-stu-id="58a49-193">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="58a49-194">Das angegebene Element oder Objekt wird in der entsprechenden Leiste geöffnet und markiert: entweder der **Element Panel für** DOM-Elemente oder der **Speicher** Panel für JavaScript-Heapobjekte.</span><span class="sxs-lookup"><span data-stu-id="58a49-194">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** panel for DOM elements or the **Memory** panel for JavaScript heap objects.</span></span>  

<span data-ttu-id="58a49-195">Im folgenden Codebeispiel und in der Abbildung `document.body` wird das im Panel **Elemente** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="58a49-195">In the following code sample and figure, the `document.body` opens in the **Elements** panel.</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="58a49-197">Abbildung 15: Überprüfen eines Elements mit</span><span class="sxs-lookup"><span data-stu-id="58a49-197">Figure 15:  Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="58a49-198">Beim Übergeben einer zu überprüfenden Methode wird das Dokument im **Quellen** Panel geöffnet, damit Sie es überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="58a49-198">When passing a method to inspect, the method opens the document in the **Sources** panel for you to inspect.</span></span>  

## <span data-ttu-id="58a49-199">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="58a49-199">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="58a49-200">Gibt die für das angegebene Objekt registrierten Ereignislistener zurück.</span><span class="sxs-lookup"><span data-stu-id="58a49-200">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="58a49-201">Der Rückgabewert ist ein Objekt, das für jeden registrierten Ereignistyp \ (wie `click` oder \) ein Array enthält `keydown` .</span><span class="sxs-lookup"><span data-stu-id="58a49-201">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="58a49-202">Die Mitglieder jedes Arrays sind Objekte, die den für jeden Typ registrierten Listener beschreiben.</span><span class="sxs-lookup"><span data-stu-id="58a49-202">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="58a49-203">Im folgenden Codebeispiel werden alle für das Document-Objekt registrierten Ereignislistener aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="58a49-203">In the following code sample figure, all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="58a49-205">Abbildung 16: das Ergebnis der Verwendung</span><span class="sxs-lookup"><span data-stu-id="58a49-205">Figure 16:  The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="58a49-206">Wenn mehr als ein Listener für das angegebene Objekt registriert ist, enthält das Array ein Element für jeden Listener.</span><span class="sxs-lookup"><span data-stu-id="58a49-206">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="58a49-207">In der folgenden Abbildung sind zwei Ereignis-Listener für das Document-Element für das `click` Ereignis registriert.</span><span class="sxs-lookup"><span data-stu-id="58a49-207">In the following figure, there are two event listeners registered on the document element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="58a49-209">Abbildung 17: mehrere Listener</span><span class="sxs-lookup"><span data-stu-id="58a49-209">Figure 17:  Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="58a49-210">Sie können jedes der folgenden Objekte erweitern, um die Eigenschaften zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="58a49-210">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="58a49-212">Abbildung 18: Erweiterte Ansicht des Listener-Objekts</span><span class="sxs-lookup"><span data-stu-id="58a49-212">Figure 18:  Expanded view of listener object</span></span>  
:::image-end:::  

## <span data-ttu-id="58a49-213">Tasten</span><span class="sxs-lookup"><span data-stu-id="58a49-213">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="58a49-214">Gibt ein Array zurück, das die Namen der Eigenschaften enthält, die zum angegebenen Objekt gehören.</span><span class="sxs-lookup"><span data-stu-id="58a49-214">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="58a49-215">Um die zugeordneten Werte der gleichen Eigenschaften abzurufen, verwenden Sie `values()` .</span><span class="sxs-lookup"><span data-stu-id="58a49-215">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="58a49-216">Angenommen, Ihre Anwendung hat das folgende Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="58a49-216">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

<span data-ttu-id="58a49-217">In den folgenden Codebeispielen und einer Abbildung wird davon ausgegangen, dass das Ergebnis `player1` vor der Eingabe `keys(player1)` und in der Konsole im globalen Namespace \ (zur Vereinfachung \) definiert wurde `values(player1)` .</span><span class="sxs-lookup"><span data-stu-id="58a49-217">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="58a49-219">Abbildung 19: die `keys()` `values()` Befehle und</span><span class="sxs-lookup"><span data-stu-id="58a49-219">Figure 19:  The `keys()` and `values()` commands</span></span>  
:::image-end:::  

## <span data-ttu-id="58a49-220">Monitor</span><span class="sxs-lookup"><span data-stu-id="58a49-220">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="58a49-221">Protokolliert eine Nachricht an die Konsole, die den Methodennamen zusammen mit den Argumenten angibt, die beim Aufrufen an die Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="58a49-221">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="58a49-223">Abbildung 20: die `monitor()` Methode</span><span class="sxs-lookup"><span data-stu-id="58a49-223">Figure 20:  The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="58a49-224">Verwenden Sie diese Einstellung `unmonitor(method)` , um die Überwachung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="58a49-224">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <span data-ttu-id="58a49-225">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="58a49-225">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="58a49-226">Wenn eines der angegebenen Ereignisse für das angegebene Objekt eintritt, wird das Ereignisobjekt in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="58a49-226">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="58a49-227">Sie können ein einzelnes Ereignis angeben, das überwacht werden soll, ein Array von Ereignissen oder einen der generischen Ereignistypen, die einer vordefinierten Sammlung von Ereignissen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="58a49-227">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="58a49-228">Das folgende Codebeispiel und die Abbildung finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="58a49-228">See the following code sample and figure.</span></span>  

<span data-ttu-id="58a49-229">Im folgenden werden alle Größen Änderungsereignisse für das Window-Objekt überwacht.</span><span class="sxs-lookup"><span data-stu-id="58a49-229">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="58a49-231">Abbildung 21: Überwachen von Fenstergrößen Ereignissen</span><span class="sxs-lookup"><span data-stu-id="58a49-231">Figure 21:  Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="58a49-232">Im folgenden wird ein Array zum Überwachen `resize` von beiden und `scroll` Ereignissen für das Window-Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="58a49-232">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="58a49-233">Sie können auch einen der verfügbaren Arten von Ereignissen angeben, Zeichenfolgen, die vordefinierten Gruppen von Ereignissen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="58a49-233">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="58a49-234">In der folgenden Tabelle werden die verfügbaren Ereignistypen und die zugehörigen Ereigniszuordnungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58a49-234">The table below displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="58a49-235">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="58a49-235">Event type</span></span> | <span data-ttu-id="58a49-236">Entsprechende zugeordnete Ereignisse</span><span class="sxs-lookup"><span data-stu-id="58a49-236">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="58a49-237">"klicken", "DblClick", "MouseDown", "MouseMove", "Mouse Out", "MouseOver", "MouseUp", "Mausrad"</span><span class="sxs-lookup"><span data-stu-id="58a49-237">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="58a49-238">"KeyDown"; "keypress"; "KeyUp"; "TextInput"</span><span class="sxs-lookup"><span data-stu-id="58a49-238">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="58a49-239">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="58a49-239">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="58a49-240">"Blur"; "ändern"; "Fokus"; "Zurücksetzen"; "Größe"; "Scrollen"; "auswählen"; "Absenden"; "Zoom"</span><span class="sxs-lookup"><span data-stu-id="58a49-240">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="58a49-241">Im folgenden Codebeispiel ist der `key` Ereignistyp, der `key` Ereignissen in einem Eingabetextfeld entspricht, aktuell im Bereich **Elemente** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="58a49-241">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** panel.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="58a49-242">In der folgenden Abbildung wird die Beispielausgabe nach dem Eingeben eines Zeichens in das Textfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58a49-242">In the following figure the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="58a49-244">Abbildung 22: Überwachen von Schlüsselereignissen</span><span class="sxs-lookup"><span data-stu-id="58a49-244">Figure 22:  Monitoring key events</span></span>  
:::image-end:::  

## <span data-ttu-id="58a49-245">profile</span><span class="sxs-lookup"><span data-stu-id="58a49-245">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="58a49-246">Startet eine JavaScript-CPU-Profilerstellungssitzung mit einem optionalen Namen.</span><span class="sxs-lookup"><span data-stu-id="58a49-246">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="58a49-247">Die [profileEnd ()](#profileend) -Methode vervollständigt das Profil und zeigt die Ergebnisse im **Speicher** Panel an.</span><span class="sxs-lookup"><span data-stu-id="58a49-247">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** panel.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="58a49-248">Führen `profile()` Sie die Methode aus, um die Profilerstellung zu starten.</span><span class="sxs-lookup"><span data-stu-id="58a49-248">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="58a49-249">Führen Sie die [profileEnd ()](#profileend) -Methode aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speicher** Panel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="58a49-249">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** panel.</span></span>  

<span data-ttu-id="58a49-250">Profile können auch geschachtelt sein.</span><span class="sxs-lookup"><span data-stu-id="58a49-250">Profiles may also be nested.</span></span>  <span data-ttu-id="58a49-251">In den folgenden Codebeispielen und Abbildung ist das Ergebnis unabhängig von der Reihenfolge identisch.</span><span class="sxs-lookup"><span data-stu-id="58a49-251">In the following code samples and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="58a49-252">Mehrere CPU-Profile können gleichzeitig ausgeführt werden, und es ist nicht erforderlich, jede Person in der Erstellungsreihenfolge zu schließen.</span><span class="sxs-lookup"><span data-stu-id="58a49-252">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="58a49-253">profileEnd</span><span class="sxs-lookup"><span data-stu-id="58a49-253">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="58a49-254">Schließt eine JavaScript-CPU-Profilerstellungssitzung ab und zeigt die Ergebnisse im **Speicher** Panel an.</span><span class="sxs-lookup"><span data-stu-id="58a49-254">Completes a JavaScript CPU profiling session and displays the results in the **Memory** panel.</span></span>  <span data-ttu-id="58a49-255">Sie müssen die [profile ()](#profile) -Methode ausführen.</span><span class="sxs-lookup"><span data-stu-id="58a49-255">You must be running the [profile()](#profile) method.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="58a49-256">Führen Sie die [profile ()](#profile) -Methode aus, um die Profilerstellung zu starten.</span><span class="sxs-lookup"><span data-stu-id="58a49-256">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="58a49-257">Führen `profileEnd()` Sie die Methode aus, um die Profilerstellung zu beenden und die Ergebnisse im **Speicher** Panel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="58a49-257">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** panel.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="58a49-258">Profile können auch geschachtelt sein.</span><span class="sxs-lookup"><span data-stu-id="58a49-258">Profiles may also be nested.</span></span>  <span data-ttu-id="58a49-259">Im folgenden Codebeispiel und in Abbildung ist das Ergebnis unabhängig von der Reihenfolge identisch.</span><span class="sxs-lookup"><span data-stu-id="58a49-259">In the following code sample and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="58a49-260">Das Ergebnis wird als Heap-Momentaufnahme im **Speicher** Panel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58a49-260">The result appears as a Heap Snapshot in the **Memory** panel.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="58a49-262">Abbildung 23: gruppierte profile</span><span class="sxs-lookup"><span data-stu-id="58a49-262">Figure 23:  Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="58a49-263">Mehrere CPU-Profile können gleichzeitig ausgeführt werden, und es ist nicht erforderlich, jede Person in der Erstellungsreihenfolge zu schließen.</span><span class="sxs-lookup"><span data-stu-id="58a49-263">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="58a49-264">queryObjects</span><span class="sxs-lookup"><span data-stu-id="58a49-264">queryObjects</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="58a49-265">Gibt ein Array von Objekten zurück, die mit dem angegebenen Konstruktor erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="58a49-265">Return an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="58a49-266">Der Bereich von `queryObjects()` ist der aktuell ausgewählte Laufzeitkontext in der Konsole.</span><span class="sxs-lookup"><span data-stu-id="58a49-266">The scope of `queryObjects()` is the currently-selected runtime context in the console.</span></span>

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="58a49-267">Gibt alle zurück `Promises` .</span><span class="sxs-lookup"><span data-stu-id="58a49-267">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="58a49-268">Gibt alle HTML-Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="58a49-268">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="58a49-269">Gibt alle Objekte zurück, die mithilfe von instanziiert wurden `new functionName()` .</span><span class="sxs-lookup"><span data-stu-id="58a49-269">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <span data-ttu-id="58a49-270">Tabelle</span><span class="sxs-lookup"><span data-stu-id="58a49-270">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="58a49-271">Protokolliert Objektdaten mit Tabellenformatierung basierend auf dem Datenobjekt mit optionalen Spaltenüberschriften.</span><span class="sxs-lookup"><span data-stu-id="58a49-271">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="58a49-272">Im folgenden Codebeispiel und in der Abbildung wird eine Liste mit Namen angezeigt, die eine Tabelle in der Konsole verwenden.</span><span class="sxs-lookup"><span data-stu-id="58a49-272">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

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

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="$ _ ist der zuletzt ausgewertete Ausdruck" lightbox="../media/console-table-display.msft.png":::
   <span data-ttu-id="58a49-274">Abbildung 24: das Ergebnis der `table()` Methode</span><span class="sxs-lookup"><span data-stu-id="58a49-274">Figure 24:  The result of the `table()` method</span></span>  
:::image-end:::  

## <span data-ttu-id="58a49-275">undebug</span><span class="sxs-lookup"><span data-stu-id="58a49-275">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="58a49-276">Beendet das Debuggen der angegebenen Methode, sodass der Debugger beim Aufrufen der Methode nicht mehr aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="58a49-276">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <span data-ttu-id="58a49-277">Unmonitor</span><span class="sxs-lookup"><span data-stu-id="58a49-277">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="58a49-278">Beendet die Überwachung der angegebenen Methode.</span><span class="sxs-lookup"><span data-stu-id="58a49-278">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="58a49-279">Diese Methode wird in Concert mit der [Monitor ()](#monitor) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="58a49-279">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <span data-ttu-id="58a49-280">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="58a49-280">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="58a49-281">Beendet das Überwachen von Ereignissen für das angegebene Objekt und die Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="58a49-281">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="58a49-282">Im folgenden Beispiel werden alle Ereignisüberwachungen für das Window-Objekt angehalten.</span><span class="sxs-lookup"><span data-stu-id="58a49-282">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="58a49-283">Sie können auch selektiv die Überwachung bestimmter Ereignisse für ein Objekt beenden.</span><span class="sxs-lookup"><span data-stu-id="58a49-283">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="58a49-284">Mit dem folgenden Code wird beispielsweise das Überwachen aller `mouse` Ereignisse für das aktuell ausgewählte Element gestartet und dann die Überwachung von `mousemove` Ereignissen beendet \ (vielleicht, um Rauschen in der Konsolenausgabe zu verringern \).</span><span class="sxs-lookup"><span data-stu-id="58a49-284">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <span data-ttu-id="58a49-285">Werte</span><span class="sxs-lookup"><span data-stu-id="58a49-285">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="58a49-286">Gibt ein Array zurück, das die Werte aller Eigenschaften enthält, die zum angegebenen Objekt gehören.</span><span class="sxs-lookup"><span data-stu-id="58a49-286">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

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
> <span data-ttu-id="58a49-296">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58a49-296">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="58a49-297">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/utilities) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="58a49-297">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="58a49-299">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="58a49-299">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

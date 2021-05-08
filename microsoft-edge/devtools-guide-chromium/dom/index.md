---
description: Anzeigen von Knoten, Suchen nach Knoten, Bearbeiten von Knoten, Referenzknoten in der Konsole, Umbruch bei Knotenänderungen und vieles mehr.
title: Erste Schritte mit dem Anzeigen und Ändern des DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: e4c08fb2fd5f360f037502c04edabaabb873ba16
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439240"
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

# <a name="get-started-with-viewing-and-changing-the-dom"></a><span data-ttu-id="443e5-104">Erste Schritte mit dem Anzeigen und Ändern des DOM</span><span class="sxs-lookup"><span data-stu-id="443e5-104">Get started with viewing and changing the DOM</span></span>  

<span data-ttu-id="443e5-105">Führen Sie diese interaktiven Lernprogramme aus, um die Grundlagen des Anzeigens und Änderns des DOM einer Seite mithilfe von Microsoft Edge DevTools zu erlernen.</span><span class="sxs-lookup"><span data-stu-id="443e5-105">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="443e5-106">In diesem Lernprogramm wird davon ausgegangen, dass Sie den Unterschied zwischen DOM und HTML kennen.</span><span class="sxs-lookup"><span data-stu-id="443e5-106">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="443e5-107">Navigieren Sie [zu Anhang: HTML im Vergleich zum DOM,](#appendix-html-versus-the-dom) um eine Erläuterung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="443e5-107">Navigate to [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <a name="open-dom-examples"></a><span data-ttu-id="443e5-108">Öffnen von DOM-Beispielen</span><span class="sxs-lookup"><span data-stu-id="443e5-108">Open DOM examples</span></span>  

1.  <span data-ttu-id="443e5-109">Halten `Control` Sie \(Windows, Linux\) oder \(macOS\) fest, und wählen Sie `Command` **DOM-Beispiele aus,** um sie auf einer neuen Registerkarte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="443e5-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="443e5-110">DOM-Beispiele</span><span class="sxs-lookup"><span data-stu-id="443e5-110">DOM Examples</span></span>][GlitchDomExamples]  
    
## <a name="view-dom-nodes"></a><span data-ttu-id="443e5-111">Anzeigen von DOM-Knoten</span><span class="sxs-lookup"><span data-stu-id="443e5-111">View DOM nodes</span></span>  

<span data-ttu-id="443e5-112">In der DOM-Struktur des Elements-Panels werden alle DOM-bezogenen Aktivitäten in DevTools verwendet.</span><span class="sxs-lookup"><span data-stu-id="443e5-112">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <a name="inspect-a-node"></a><span data-ttu-id="443e5-113">Überprüfen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="443e5-113">Inspect a node</span></span>  

<span data-ttu-id="443e5-114">Wenn Sie an einem bestimmten DOM-Knoten interessiert sind, ist **Inspect** eine schnelle Möglichkeit, DevTools zu öffnen und den Knoten zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="443e5-114">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="443e5-115">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-115">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-116">Wählen **Sie unter Prüfen eines Knotens**mit der rechten Option **"Michelangelo"** aus, und wählen Sie **Inspect aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-116">Under **Inspect a Node**, right-choose **Michelangelo** and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="443e5-118">Überprüfen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="443e5-118">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="443e5-119">Das **Elementtool** von DevTools wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="443e5-119">The **Elements** tool of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="443e5-120">wird in der **DOM-Struktur hervorgehoben.**</span><span class="sxs-lookup"><span data-stu-id="443e5-120">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Hervorheben des Knotens "Michelangelo"" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="443e5-122">Hervorheben des `Michelangelo` Knotens</span><span class="sxs-lookup"><span data-stu-id="443e5-122">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="443e5-123">Wählen Sie in der oberen linken Ecke von DevTools das Symbol **Inspect** ![ \( Inspect ](../media/inspect-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-123">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Das Symbol "Überprüfen"" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="443e5-125">Das **Symbol "Überprüfen"**</span><span class="sxs-lookup"><span data-stu-id="443e5-125">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="443e5-126">Wählen **Sie unter Überprüfen eines Knotens**den **Tokio-Text** aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-126">Under **Inspect a Node**, choose the **Tokyo** text.</span></span>  <span data-ttu-id="443e5-127">Wird nun `<li>Tokyo</li>` in der DOM-Struktur hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="443e5-127">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="443e5-128">Das Überprüfen eines Knotens ist auch der erste Schritt zum Anzeigen und Ändern der Formatvorlagen eines Knotens.</span><span class="sxs-lookup"><span data-stu-id="443e5-128">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="443e5-129">Navigieren Sie zu [Erste Schritte mit dem Anzeigen und Ändern von CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="443e5-129">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <a name="navigate-the-dom-tree-with-a-keyboard"></a><span data-ttu-id="443e5-130">Navigieren in der DOM-Struktur mit einer Tastatur</span><span class="sxs-lookup"><span data-stu-id="443e5-130">Navigate the DOM Tree with a keyboard</span></span>  

<span data-ttu-id="443e5-131">Nachdem Sie einen Knoten in der DOM-Struktur ausgewählt haben, können Sie mit der Tastatur in der DOM-Struktur navigieren.</span><span class="sxs-lookup"><span data-stu-id="443e5-131">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="443e5-132">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-132">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-133">Wählen **Sie unter Navigieren in der DOM-Struktur mit einer Tastatur**mit der rechten Option **Ringo** aus, und wählen Sie **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-133">Under **Navigate the DOM Tree with a Keyboard**, right-choose **Ringo** and choose **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="443e5-134">ist in der DOM-Struktur ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="443e5-134">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Überprüfen des Knotens Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="443e5-136">Überprüfen des `Ringo` Knotens</span><span class="sxs-lookup"><span data-stu-id="443e5-136">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="443e5-137">Wählen Sie `Up` die Pfeiltaste 2 mal aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-137">Select the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="443e5-138"> markiert ist.</span><span class="sxs-lookup"><span data-stu-id="443e5-138">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Überprüfen des ul-Knotens" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="443e5-140">Überprüfen des `ul` Knotens</span><span class="sxs-lookup"><span data-stu-id="443e5-140">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="443e5-141">Wählen Sie `Left` die Pfeiltaste aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-141">Select the `Left` arrow key.</span></span>  <span data-ttu-id="443e5-142">Die `<ul>` Liste wird reduziert.</span><span class="sxs-lookup"><span data-stu-id="443e5-142">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="443e5-143">Wählen Sie `Left` die Pfeiltaste erneut aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-143">Select the `Left` arrow key again.</span></span>  <span data-ttu-id="443e5-144">Das übergeordnete Element des `<ul>` Knotens ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="443e5-144">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="443e5-145">In diesem Fall ist es die `<div>` mit der ID `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="443e5-145">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="443e5-146">Wählen Sie die Pfeiltaste 2 mal aus, damit Sie die Liste, die Sie `Down` `<ul>` gerade reduziert haben, erneut ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="443e5-146">Select the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="443e5-147">Es sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="443e5-147">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="443e5-148">Wählen Sie `Right` die Pfeiltaste aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-148">Select the `Right` arrow key.</span></span>  <span data-ttu-id="443e5-149">Die Liste wird erweitert.</span><span class="sxs-lookup"><span data-stu-id="443e5-149">The list expands.</span></span>  

### <a name="scroll-into-view"></a><span data-ttu-id="443e5-150">Bildlauf in die Ansicht</span><span class="sxs-lookup"><span data-stu-id="443e5-150">Scroll into view</span></span>  

<span data-ttu-id="443e5-151">Wenn Sie die DOM-Struktur anzeigen, interessieren Sie sich möglicherweise für einen DOM-Knoten, der sich derzeit nicht im Viewport befindet.</span><span class="sxs-lookup"><span data-stu-id="443e5-151">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="443e5-152">Angenommen, Sie haben einen Bildlauf zum unteren Rand der Seite durchgeführt, und Sie interessieren sich für den Knoten am oberen Rand `<h1>` der Seite.</span><span class="sxs-lookup"><span data-stu-id="443e5-152">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="443e5-153">**Mit einem Bildlauf** in die Ansicht können Sie den Viewport schnell neu positionieren, sodass Sie den Knoten überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="443e5-153">**Scroll into view** lets you quickly reposition the viewport so that you are able to review the node.</span></span>  

1.  <span data-ttu-id="443e5-154">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-154">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-155">Wählen **Sie unter Scroll into View**mit der rechten Option **Magritte aus,** und wählen Sie **Inspect aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-155">Under **Scroll into View**, right-choose **Magritte** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="443e5-156">Scrollen Sie zum Unteren Rand der Seite DOM-Beispiele.</span><span class="sxs-lookup"><span data-stu-id="443e5-156">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="443e5-157">Der `<li>Magritte</li>` Knoten sollte weiterhin in der DOM-Struktur ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="443e5-157">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="443e5-158">Wenn nicht, wechseln Sie zurück zu [Bildlauf in die Ansicht,](#scroll-into-view) und starten Sie von vorn.</span><span class="sxs-lookup"><span data-stu-id="443e5-158">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="443e5-159">Zeigen Sie auf `<li>Magritte</li>` den Knoten, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Scroll into view aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-159">Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.</span></span>  <span data-ttu-id="443e5-160">Ihr Viewport führt einen Bildlauf nach oben aus, sodass Sie den **Knoten Magritte überprüfen** können.</span><span class="sxs-lookup"><span data-stu-id="443e5-160">Your viewport scrolls back up so that you may review the **Magritte** node.</span></span>  <span data-ttu-id="443e5-161">Navigieren Sie [zu Anhang: Fehlende Optionen,](#appendix-missing-options) wenn Sie die Option In Ansicht **scrollen nicht überprüfen** können.</span><span class="sxs-lookup"><span data-stu-id="443e5-161">Navigate to [Appendix: Missing options](#appendix-missing-options) if you are not able to review the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Bildlauf in die Ansicht" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="443e5-163">Bildlauf in die Ansicht</span><span class="sxs-lookup"><span data-stu-id="443e5-163">Scroll into view</span></span>**  
    :::image-end:::  

### <a name="search-for-nodes"></a><span data-ttu-id="443e5-164">Suchen nach Knoten</span><span class="sxs-lookup"><span data-stu-id="443e5-164">Search for nodes</span></span>  

<span data-ttu-id="443e5-165">Sie können die DOM-Struktur nach Zeichenfolge, CSS-Selektor oder XPath-Selektor durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="443e5-165">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="443e5-166">Fokussieren Sie den Cursor auf das **Elementtool.**</span><span class="sxs-lookup"><span data-stu-id="443e5-166">Focus your cursor on the **Elements** tool.</span></span>  
1.  <span data-ttu-id="443e5-167">Wählen `Control` + `F` Sie \(Windows, Linux\) oder `Command` + `F` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-167">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="443e5-168">Die Suchleiste wird am unteren Rand der DOM-Struktur geöffnet.</span><span class="sxs-lookup"><span data-stu-id="443e5-168">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="443e5-169">Geben Sie `The Moon is a Harsh Mistress` ein.</span><span class="sxs-lookup"><span data-stu-id="443e5-169">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="443e5-170">Der letzte Satz wird in der DOM-Struktur hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="443e5-170">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Hervorheben der Abfrage in der Suchleiste" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="443e5-172">Hervorheben der Abfrage in der Suchleiste</span><span class="sxs-lookup"><span data-stu-id="443e5-172">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="443e5-173">Wie oben erwähnt, unterstützt die Suchleiste auch CSS- und XPath-Selektoren.</span><span class="sxs-lookup"><span data-stu-id="443e5-173">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <a name="edit-the-dom"></a><span data-ttu-id="443e5-174">Bearbeiten des DOM</span><span class="sxs-lookup"><span data-stu-id="443e5-174">Edit the DOM</span></span>  

<span data-ttu-id="443e5-175">Sie können das DOM im Schnellmodus bearbeiten und überprüfen, wie sich die Änderungen auf die Seite auswirken.</span><span class="sxs-lookup"><span data-stu-id="443e5-175">You may edit the DOM on the fly and review how the changes affect the page.</span></span>  

### <a name="edit-content"></a><span data-ttu-id="443e5-176">Bearbeiten von Inhalten</span><span class="sxs-lookup"><span data-stu-id="443e5-176">Edit content</span></span>  

<span data-ttu-id="443e5-177">Doppelklicken Sie zum Bearbeiten des Inhalts eines Knotens in der DOM-Struktur auf den Inhalt.</span><span class="sxs-lookup"><span data-stu-id="443e5-177">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="443e5-178">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-178">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-179">Wählen **Sie unter Inhalt bearbeiten**mit der rechten Option **Michelle** aus, und wählen Sie **Inspect aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-179">Under **Edit Content**, right-choose **Michelle** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="443e5-180">Doppelklicken Sie in der DOM-Struktur auf `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="443e5-180">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="443e5-181">Doppelklicken Sie also auf den Text zwischen `<li>` und `</li>` .</span><span class="sxs-lookup"><span data-stu-id="443e5-181">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="443e5-182">Der Text wird hervorgehoben, um anzugeben, dass er ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="443e5-182">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Bearbeiten des Texts" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="443e5-184">Bearbeiten des Texts</span><span class="sxs-lookup"><span data-stu-id="443e5-184">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="443e5-185">Delete `Michelle` , type , `Leela` then select to confirm the `Enter` change.</span><span class="sxs-lookup"><span data-stu-id="443e5-185">Delete `Michelle`, type `Leela`, then select `Enter` to confirm the change.</span></span>  <span data-ttu-id="443e5-186">Der Text im DOM wird von **Michelle** zu **Leela geändert.**</span><span class="sxs-lookup"><span data-stu-id="443e5-186">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <a name="edit-attributes"></a><span data-ttu-id="443e5-187">Bearbeiten von Attributen</span><span class="sxs-lookup"><span data-stu-id="443e5-187">Edit attributes</span></span>  

<span data-ttu-id="443e5-188">Doppelklicken Sie zum Bearbeiten von Attributen auf den Attributnamen oder -wert.</span><span class="sxs-lookup"><span data-stu-id="443e5-188">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="443e5-189">Befolgen Sie die Anweisungen, um zu erfahren, wie Sie einem Knoten Attribute hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="443e5-189">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="443e5-190">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-190">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-191">Wählen **Sie unter Attribute bearbeiten**mit der rechten Option **Howard** aus, und wählen Sie **Inspect aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-191">Under **Edit Attributes**, right-choose **Howard** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="443e5-192">Doppelklicken Sie `<li>` auf .</span><span class="sxs-lookup"><span data-stu-id="443e5-192">Double-click `<li>`.</span></span>  <span data-ttu-id="443e5-193">Der Text wird hervorgehoben, um anzugeben, dass der Knoten ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="443e5-193">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Bearbeiten des Knotens" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="443e5-195">Bearbeiten des Knotens</span><span class="sxs-lookup"><span data-stu-id="443e5-195">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="443e5-196">Wählen Sie `Right` die Pfeiltaste aus, fügen Sie ein Leerzeichen hinzu, geben Sie `style="background-color:gold"` ein, und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-196">Select the `Right` arrow key, add a space, type `style="background-color:gold"`, and then select `Enter`.</span></span>  <span data-ttu-id="443e5-197">Die Hintergrundfarbe des Knotens wird in Gold geändert.</span><span class="sxs-lookup"><span data-stu-id="443e5-197">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Hinzufügen eines Formatattributs zum Knoten" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="443e5-199">Hinzufügen eines `style` Attributs zum Knoten</span><span class="sxs-lookup"><span data-stu-id="443e5-199">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <a name="edit-node-type"></a><span data-ttu-id="443e5-200">Knotentyp bearbeiten</span><span class="sxs-lookup"><span data-stu-id="443e5-200">Edit node type</span></span>  

<span data-ttu-id="443e5-201">Doppelklicken Sie zum Bearbeiten des Knotentyps auf den Typ, und geben Sie dann den neuen Typ ein.</span><span class="sxs-lookup"><span data-stu-id="443e5-201">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="443e5-202">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-202">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-203">Wählen **Sie unter Knotentyp bearbeiten**mit der rechten Option **Hank aus,** und wählen Sie **Inspect aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-203">Under **Edit Node Type**, right-choose **Hank** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="443e5-204">Doppelklicken Sie `<li>` auf .</span><span class="sxs-lookup"><span data-stu-id="443e5-204">Double-click `<li>`.</span></span>  <span data-ttu-id="443e5-205">Der Text `li` wird hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="443e5-205">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="443e5-206">Delete `li` , type , `button` then select `Enter` .</span><span class="sxs-lookup"><span data-stu-id="443e5-206">Delete `li`, type `button`, then select `Enter`.</span></span>  <span data-ttu-id="443e5-207">Der `<li>` Knoten wird in einen Knoten `<button>` geändert.</span><span class="sxs-lookup"><span data-stu-id="443e5-207">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Ändern des Knotentyps in Schaltfläche" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="443e5-209">Ändern des Knotentyps in</span><span class="sxs-lookup"><span data-stu-id="443e5-209">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <a name="reorder-dom-nodes"></a><span data-ttu-id="443e5-210">Neu anordnen von DOM-Knoten</span><span class="sxs-lookup"><span data-stu-id="443e5-210">Reorder DOM nodes</span></span>  

<span data-ttu-id="443e5-211">Ziehen Sie Knoten, um sie neu anordnen zu können.</span><span class="sxs-lookup"><span data-stu-id="443e5-211">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="443e5-212">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-212">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-213">Wählen Sie unter Neu anordnen von **DOM-Knoten**mit der rechten Option **"Elvis Presley"** aus, und wählen Sie **Inspect aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-213">Under **Reorder DOM Nodes**, right-choose **Elvis Presley** and choose **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="443e5-214">Es ist das letzte Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="443e5-214">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="443e5-215">Ziehen Sie in der DOM-Struktur `<li>Elvis Presley</li>` an den oberen Rand der Liste.</span><span class="sxs-lookup"><span data-stu-id="443e5-215">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Ziehen Sie den Knoten an den oberen Rand der Liste" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="443e5-217">Ziehen Sie den Knoten an den oberen Rand der Liste</span><span class="sxs-lookup"><span data-stu-id="443e5-217">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <a name="force-state"></a><span data-ttu-id="443e5-218">Force-Status</span><span class="sxs-lookup"><span data-stu-id="443e5-218">Force state</span></span>  

<span data-ttu-id="443e5-219">Sie können erzwingen, dass Knoten in Zustände wie `:active` , , , und `:hover` `:focus` `:visited` `:focus-within` verbleiben.</span><span class="sxs-lookup"><span data-stu-id="443e5-219">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="443e5-220">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-220">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-221">Zeigen **Sie unter Force-Zustand**auf **Der Herr der Fliegt.**</span><span class="sxs-lookup"><span data-stu-id="443e5-221">Under **Force state**, hover on **The Lord of the Flies**.</span></span>  <span data-ttu-id="443e5-222">Die Hintergrundfarbe wird orange.</span><span class="sxs-lookup"><span data-stu-id="443e5-222">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="443e5-223">Zeigen Sie **auf Der Herr der Fliegt,** öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie Überprüfen **aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-223">Hover on **The Lord of the Flies**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="443e5-224">Zeigen Sie `<li class="demo--hover">The Lord of the Flies</li>` auf , öffnen Sie das Kontextmenü \(mit der rechten Maustaste\), und wählen Sie Force **State**  >  **:hover aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-224">Hover on `<li class="demo--hover">The Lord of the Flies</li>`, open the contextual menu \(right-click\), and choose **Force State** > **:hover**.</span></span>  <span data-ttu-id="443e5-225">Navigieren Sie [zu Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="443e5-225">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  <span data-ttu-id="443e5-226">Die Hintergrundfarbe bleibt orange, auch wenn Sie nicht mit dem Mauszeiger auf den Knoten zeigen.</span><span class="sxs-lookup"><span data-stu-id="443e5-226">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <a name="hide-a-node"></a><span data-ttu-id="443e5-227">Ausblenden eines Knotens</span><span class="sxs-lookup"><span data-stu-id="443e5-227">Hide a node</span></span>  

<span data-ttu-id="443e5-228">Wählen `H` Sie diese Option aus, um einen Knoten auszublenden.</span><span class="sxs-lookup"><span data-stu-id="443e5-228">Select `H` to hide a node.</span></span>  

1.  <span data-ttu-id="443e5-229">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-229">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-230">Wählen **Sie unter Knoten ausblenden**mit der rechten Option The Stars My **Destination** aus, und wählen Sie **Inspect aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-230">Under **Hide a node**, right-choose **The Stars My Destination** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="443e5-231">Wählen Sie den `H` Schlüssel aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-231">Select the `H` key.</span></span>  <span data-ttu-id="443e5-232">Der Knoten ist ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="443e5-232">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="So sieht der Knoten im DOM-Struktur aus, nachdem er ausgeblendet wurde" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="443e5-234">So sieht der Knoten im DOM-Struktur aus, nachdem er ausgeblendet wurde</span><span class="sxs-lookup"><span data-stu-id="443e5-234">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="443e5-235">Wählen Sie `H` den Schlüssel erneut aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-235">Select the `H` key again.</span></span>  <span data-ttu-id="443e5-236">Der Knoten wird erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="443e5-236">The node is shown again.</span></span>  

### <a name="delete-a-node"></a><span data-ttu-id="443e5-237">Löschen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="443e5-237">Delete a node</span></span>  

<span data-ttu-id="443e5-238">Wählen `Delete` Sie diese Option aus, um einen Knoten zu löschen.</span><span class="sxs-lookup"><span data-stu-id="443e5-238">Select `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="443e5-239">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-239">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-240">Wählen **Sie unter Knoten löschen**mit der rechten Option Foundation **aus,** und wählen Sie **Inspect aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-240">Under **Delete a Node**, right-choose **Foundation** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="443e5-241">Wählen Sie den `Delete` Schlüssel aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-241">Select the `Delete` key.</span></span>  <span data-ttu-id="443e5-242">Der Knoten wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="443e5-242">The node is deleted.</span></span>  
    1.  <span data-ttu-id="443e5-243">Wählen `Control` + `Z` Sie \(Windows, Linux\) oder `Command` + `Z` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="443e5-243">Select `Control`+`Z` \(Windows, Linux\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="443e5-244">Die letzte Aktion wird rückgängig gemacht, und der Knoten wird erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="443e5-244">The last action is undone and the node reappears.</span></span>  

## <a name="access-nodes-in-the-console"></a><span data-ttu-id="443e5-245">Zugriffsknoten in der Konsole</span><span class="sxs-lookup"><span data-stu-id="443e5-245">Access nodes in the Console</span></span>  

<span data-ttu-id="443e5-246">DevTools bietet einige Verknüpfungen für den Zugriff auf DOM-Knoten über die Konsole oder das Abrufen von JavaScript-Verweisen auf die einzelnen.</span><span class="sxs-lookup"><span data-stu-id="443e5-246">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <a name="reference-the-currently-selected-node-with-0"></a><span data-ttu-id="443e5-247">Verweisen auf den aktuell ausgewählten Knoten mit $0</span><span class="sxs-lookup"><span data-stu-id="443e5-247">Reference the currently-selected node with $0</span></span>  

<span data-ttu-id="443e5-248">Wenn Sie einen Knoten überprüfen, bedeutet der Text neben dem Knoten, dass Sie in der Konsole mit der Variablen auf `== $0` diesen Knoten verweisen `$0` können.</span><span class="sxs-lookup"><span data-stu-id="443e5-248">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="443e5-249">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-249">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-250">Wählen **Sie unter Verweis auf den aktuell ausgewählten Knoten mit $0**die linke Hand **der** Dunklen aus, und wählen Sie **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-250">Under **Reference the currently-selected node with $0**, right-choose **The Left Hand of Darkness** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="443e5-251">Wählen Sie die `Escape` Taste aus, um die Konsolenschubschubte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="443e5-251">Select the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="443e5-252">Geben `$0` Sie den Schlüssel ein, und wählen Sie diesen `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-252">Type `$0` and select the `Enter` key.</span></span>  <span data-ttu-id="443e5-253">Das Ergebnis des Ausdrucks zeigt, dass `$0` als ausgewertet `<li>The Left Hand of Darkness</li>` wird.</span><span class="sxs-lookup"><span data-stu-id="443e5-253">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Das Ergebnis des ersten $0-Ausdrucks in der Konsole" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="443e5-255">Das Ergebnis des ersten `$0` Ausdrucks in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="443e5-255">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="443e5-256">Zeigen Sie auf das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="443e5-256">Hover on the result.</span></span>  <span data-ttu-id="443e5-257">Der Knoten wird im Viewport hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="443e5-257">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="443e5-258">Wählen `<li>Dune</li>` Sie in der DOM-Struktur aus, geben Sie die Konsole erneut `$0` ein, und wählen Sie dann erneut `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-258">Choose `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then select `Enter` again.</span></span>  <span data-ttu-id="443e5-259">Ausgewertet `$0` wird nun als `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="443e5-259">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Das Ergebnis des zweiten $0-Ausdrucks in der Konsole" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="443e5-261">Das Ergebnis des zweiten `$0` Ausdrucks in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="443e5-261">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <a name="store-as-global-variable"></a><span data-ttu-id="443e5-262">Store als globale Variable</span><span class="sxs-lookup"><span data-stu-id="443e5-262">Store as global variable</span></span>  

<span data-ttu-id="443e5-263">Wenn Sie mehrmals auf einen Knoten verweisen müssen, speichern Sie ihn als globale Variable.</span><span class="sxs-lookup"><span data-stu-id="443e5-263">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="443e5-264">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-264">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-265">Zeigen **Sie Store**als globale Variable auf The Big **Sleep,** öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-265">Under **Store as global variable**, hover on **The Big Sleep**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="443e5-266">Zeigen Sie in der DOM-Struktur auf, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen `<li>The Big Sleep</li>` Store als globale Variable **aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-266">Hover on `<li>The Big Sleep</li>` in the DOM Tree, open the contextual menu \(right-click\), and choose **Store as global variable**.</span></span>  <span data-ttu-id="443e5-267">Navigieren Sie [zu Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="443e5-267">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="443e5-268">Geben `temp1` Sie in die Konsole ein, und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-268">Type `temp1` in the Console and then select `Enter`.</span></span>  <span data-ttu-id="443e5-269">Das Ergebnis des Ausdrucks zeigt, dass die Variable zum Knoten ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="443e5-269">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Das Ergebnis des temp1-Ausdrucks" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="443e5-271">Das Ergebnis des `temp1` Ausdrucks</span><span class="sxs-lookup"><span data-stu-id="443e5-271">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <a name="copy-js-path"></a><span data-ttu-id="443e5-272">Kopieren des JS-Pfads</span><span class="sxs-lookup"><span data-stu-id="443e5-272">Copy JS path</span></span>  

<span data-ttu-id="443e5-273">Kopieren Sie den JavaScript-Pfad in einen Knoten, wenn Sie in einem automatisierten Test darauf verweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="443e5-273">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="443e5-274">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-274">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-275">Zeigen **Sie unter JS-Pfad**kopieren auf **The Brothers Karamazov,** öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-275">Under **Copy JS path**, hover on **The Brothers Karamazov**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="443e5-276">Zeigen Sie in der DOM-Struktur auf, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `<li>The Brothers Karamazov</li>` Maustaste\), und wählen Sie **Kopieren**  >  **JS-Pfad kopieren aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-276">Hover on `<li>The Brothers Karamazov</li>` in the DOM Tree, open the contextual menu \(right-click\), and choose **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="443e5-277">Ein `document.querySelector()` Ausdruck, der in den Knoten aufgelöst wird, wurde in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="443e5-277">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="443e5-278">Wählen `Control` + `V` Sie \(Windows, Linux\) oder `Command` + `V` \(macOS\) aus, um den Ausdruck in die Konsole zu einfügen.</span><span class="sxs-lookup"><span data-stu-id="443e5-278">Select `Control`+`V` \(Windows, Linux\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="443e5-279">Wählen `Enter` Sie diese Option aus, um den Ausdruck auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="443e5-279">Select `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Das Ergebnis des Copy JS Path-Ausdrucks" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="443e5-281">Das Ergebnis des **Copy JS Path-Ausdrucks**</span><span class="sxs-lookup"><span data-stu-id="443e5-281">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <a name="break-on-dom-changes"></a><span data-ttu-id="443e5-282">Pause bei DOM-Änderungen</span><span class="sxs-lookup"><span data-stu-id="443e5-282">Break on DOM changes</span></span>  

<span data-ttu-id="443e5-283">Mit DevTools können Sie das JavaScript einer Seite anhalten, wenn JavaScript das DOM ändert.</span><span class="sxs-lookup"><span data-stu-id="443e5-283">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <a name="break-on-attribute-modifications"></a><span data-ttu-id="443e5-284">Unterbrechung von Attributänderungen</span><span class="sxs-lookup"><span data-stu-id="443e5-284">Break on attribute modifications</span></span>  

<span data-ttu-id="443e5-285">Verwenden Sie Haltepunkte für Attributänderung, wenn Sie das JavaScript anhalten möchten, das bewirkt, dass sich jedes Attribut eines Knotens ändert.</span><span class="sxs-lookup"><span data-stu-id="443e5-285">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="443e5-286">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-286">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-287">Wählen **Sie unter Break on attribute modifications**mit der rechten Option **"Sauerkraut" aus,** und wählen Sie **Inspect aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-287">Under **Break on attribute modifications**, right-choose **Sauerkraut** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="443e5-288">Zeigen Sie in der DOM-Struktur auf , öffnen Sie das kontextbezogene Menü \(mit der rechten Maustaste auf\), und wählen Sie `<li id="target">Sauerkraut</li>` **Break On**  >  **Attribute Modifications aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-288">In the DOM Tree, hover on `<li id="target">Sauerkraut</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="443e5-289">Navigieren Sie [zu Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="443e5-289">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Unterbrechung von Attributänderungen" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="443e5-291">Unterbrechung von Attributänderungen</span><span class="sxs-lookup"><span data-stu-id="443e5-291">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="443e5-292">Im nächsten Schritt werden Sie angewiesen, eine Schaltfläche zu wählen, mit der der Code der Seite angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="443e5-292">In the next step you are going to be instructed to choose a button that pauses the code of the page.</span></span>  <span data-ttu-id="443e5-293">Nachdem die Seite angehalten wurde, können Sie keinen Bildlauf mehr auf der Seite durchführen.</span><span class="sxs-lookup"><span data-stu-id="443e5-293">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="443e5-294">Sie müssen Skript **fortsetzen** \( Skript fortsetzen \) auswählen, damit die Seite wieder ![ ](../media/resume-script-icon.msft.png) scrollbar ist.</span><span class="sxs-lookup"><span data-stu-id="443e5-294">You must choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Where to resume script running" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="443e5-296">Where to resume script running</span><span class="sxs-lookup"><span data-stu-id="443e5-296">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="443e5-297">Wählen Sie **oben die Schaltfläche Hintergrund** festlegen aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-297">Choose the **Set Background** button above.</span></span>  <span data-ttu-id="443e5-298">Dadurch wird das `style` Attribut des Knotens auf . `background-color:thistle`</span><span class="sxs-lookup"><span data-stu-id="443e5-298">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="443e5-299">DevTools hält die Seite an und hebt den Code hervor, der dazu führte, dass das Attribut geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="443e5-299">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="443e5-300">Wählen **Sie Skript fortsetzen** \( Skript fortsetzen ![ ](../media/resume-script-icon.msft.png) \), wie bereits erwähnt.</span><span class="sxs-lookup"><span data-stu-id="443e5-300">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\), as mentioned earlier.</span></span>  
    
### <a name="break-on-node-removal"></a><span data-ttu-id="443e5-301">Unterbrechung beim Entfernen von Knoten</span><span class="sxs-lookup"><span data-stu-id="443e5-301">Break on node removal</span></span>  

<span data-ttu-id="443e5-302">Wenn Sie anhalten möchten, wenn ein bestimmter Knoten entfernt wird, verwenden Sie Haltepunkte für die Knotenentfernung.</span><span class="sxs-lookup"><span data-stu-id="443e5-302">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="443e5-303">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-303">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-304">Wählen **Sie unter Unterbrechung beim Entfernen**von Knoten mit der rechten Option **Neuromancer aus,** und wählen Sie **Inspect aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-304">Under **Break on Node Removal**, right-choose **Neuromancer** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="443e5-305">Zeigen Sie in der DOM-Struktur auf , öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie Beim Knotenentfernung `<li id="target">Neuromancer</li>` \*\*\*\*  >  **pausenlos aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-305">In the DOM Tree, hover on `<li id="target">Neuromancer</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="443e5-306">Navigieren Sie [zu Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="443e5-306">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="443e5-307">Wählen Sie oben **die Schaltfläche** Löschen aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-307">Choose the **Delete** button above.</span></span>  <span data-ttu-id="443e5-308">DevTools hält die Seite an und hebt den Code hervor, der dazu führte, dass der Knoten entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="443e5-308">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="443e5-309">Wählen **Sie Skript fortsetzen** \( Skript fortsetzen ![ ](../media/resume-script-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="443e5-309">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\).</span></span>  
    
### <a name="break-on-subtree-modifications"></a><span data-ttu-id="443e5-310">Unterbrechung bei Änderungen der Unterstruktur</span><span class="sxs-lookup"><span data-stu-id="443e5-310">Break on subtree modifications</span></span>  

<span data-ttu-id="443e5-311">Nachdem Sie einen Unterstrukturänderungs-Haltepunkt auf einem Knoten eingefügt haben, hält DevTools die Seite an, wenn eines der untergeordneten Elemente des Knotens hinzugefügt oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="443e5-311">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="443e5-312">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="443e5-312">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="443e5-313">Wählen **Sie unter Break on Subtree Modifications**mit der rechten Option A Fire Upon The **Deep** aus, und wählen Sie **Inspect aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-313">Under **Break on Subtree Modifications**, right-choose **A Fire Upon The Deep** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="443e5-314">Zeigen Sie in der DOM-Struktur auf , der den obigen Knoten ist, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie Bei Unterstrukturänderungen `<ul id="target">` `<li>A Fire Upon the Deep</li>` \*\*\*\*  >  **pausen aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-314">In the DOM Tree, hover on `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="443e5-315">Wenn die Option nicht angezeigt wird, navigieren Sie zu [Anhang: Fehlende Optionen](#appendix-missing-options).</span><span class="sxs-lookup"><span data-stu-id="443e5-315">If the option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).</span></span>  
    1.  <span data-ttu-id="443e5-316">Wählen **Sie Untergeordnetes Hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="443e5-316">Choose **Add Child**.</span></span>  <span data-ttu-id="443e5-317">Der Code wird angehalten, da `<li>` der Liste ein Knoten hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="443e5-317">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="443e5-318">Wählen **Sie Skript fortsetzen** \( Skript fortsetzen ![ ](../media/resume-script-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="443e5-318">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\).</span></span>  
    
## <a name="next-steps"></a><span data-ttu-id="443e5-319">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="443e5-319">Next steps</span></span>  

<span data-ttu-id="443e5-320">Dies deckt die meisten DOM-bezogenen Features in DevTools ab.</span><span class="sxs-lookup"><span data-stu-id="443e5-320">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="443e5-321">Sie können die restlichen Features ermitteln, indem Sie auf Knoten in der DOM-Struktur zeigen, das Kontextmenü \(rechtsklicken\) öffnen und mit den anderen Optionen experimentieren, die in diesem Lernprogramm nicht behandelt wurden.</span><span class="sxs-lookup"><span data-stu-id="443e5-321">You are able to discover the rest of the features by hovering on nodes in the DOM Tree, opening the contextual menu \(right-click\), and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="443e5-322">Navigieren Sie zu [Tastenkombinationen des Elements-Panels.][DevToolsShortcutsElements]</span><span class="sxs-lookup"><span data-stu-id="443e5-322">Navigate to [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="443e5-323">Sehen Sie sich die [Microsoft Edge DevTools-Homepage an,][MicrosoftEdgeDevTools] um alles zu entdecken, was Sie mit DevTools tun können.</span><span class="sxs-lookup"><span data-stu-id="443e5-323">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <a name="appendix-html-versus-the-dom"></a><span data-ttu-id="443e5-324">Anhang: HTML im Vergleich zum DOM</span><span class="sxs-lookup"><span data-stu-id="443e5-324">Appendix: HTML versus the DOM</span></span>  

<span data-ttu-id="443e5-325">Im folgenden Abschnitt wird der Unterschied zwischen HTML und DOM schnell erläutert.</span><span class="sxs-lookup"><span data-stu-id="443e5-325">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="443e5-326">Wenn Sie einen Webbrowser zum Anfordern einer Seite verwenden, gibt der Server HTML wie den folgenden Codeausschnitt zurück.</span><span class="sxs-lookup"><span data-stu-id="443e5-326">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="443e5-327">Der Browser analysiert den HTML-Code und erstellt eine Struktur mit Objekten wie der folgenden Liste.</span><span class="sxs-lookup"><span data-stu-id="443e5-327">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="443e5-328">Diese Struktur von Objekten oder Knoten, die den Inhalt der Seite darstellen, wird als DOM bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="443e5-328">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="443e5-329">Derzeit sieht es genauso aus wie der HTML- Code, aber angenommen, das Skript, auf das unten im HTML verwiesen wird, führt den folgenden Codeausschnitt aus.</span><span class="sxs-lookup"><span data-stu-id="443e5-329">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="443e5-330">Dieser Code entfernt den `h1` Knoten und fügt dem DOM einen weiteren Knoten `p` hinzu.</span><span class="sxs-lookup"><span data-stu-id="443e5-330">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="443e5-331">Das vollständige DOM zeigt nun die folgende Liste an.</span><span class="sxs-lookup"><span data-stu-id="443e5-331">The complete DOM now displays the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="443e5-332">Der HTML-Code für die Seite ist jetzt anders als das DOM.</span><span class="sxs-lookup"><span data-stu-id="443e5-332">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="443e5-333">Mit anderen Worten, HTML stellt anfänglichen Seiteninhalt dar, und das DOM stellt den aktuellen Seiteninhalt dar.</span><span class="sxs-lookup"><span data-stu-id="443e5-333">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="443e5-334">Wenn JavaScript Knoten hinzufügt, entfernt oder bearbeitet, wird das DOM anders als der HTML-Code.</span><span class="sxs-lookup"><span data-stu-id="443e5-334">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="443e5-335">Navigieren Sie [zu Einführung in das DOM,][MDNIntroductionToDOM] um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="443e5-335">Navigate to [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.  Your viewport scrolls back up so that the **Magritte** node is displayed.  If you the **Scroll into view** option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <a name="appendix-missing-options"></a><span data-ttu-id="443e5-336">Anhang: Fehlende Optionen</span><span class="sxs-lookup"><span data-stu-id="443e5-336">Appendix: Missing options</span></span>  

<span data-ttu-id="443e5-337">In vielen Anweisungen in diesem Lernprogramm werden Sie angewiesen, den Mauszeiger auf einen Knoten in der DOM-Struktur zu zeigen, das Kontextmenü \(rechtsklicken\) zu öffnen und dann eine Option aus dem Kontextmenü zu wählen, das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="443e5-337">Many of the instructions in this tutorial instruct you to hover on a node in the DOM Tree, open the contextual menu \(right-click\), and then choose an option from the context menu that pops up.</span></span>  <span data-ttu-id="443e5-338">Wenn die angegebene Option im Kontextmenü nicht angezeigt wird, versuchen Sie, mit dem Mauszeiger vom Knotentext zu zeigen und das Kontextmenü \(rechtsklicken\) zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="443e5-338">If the specified option in the context menu is not displayed, try hovering away from the node text and opening the contextual menu \(right-click\).</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Auswählen, ob nicht alle Optionen angezeigt werden" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="443e5-340">Auswählen, ob nicht alle Optionen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="443e5-340">Where to choose if all of the options are not displayed</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="443e5-341">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="443e5-341">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge \(Chromium\) Developer Tools | Microsoft Docs"  
[DevToolsCssGetStarted]: ../css/index.md "Erste Schritte Mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-tool-keyboard-shortcuts "Tastenkombinationen des Elements-Tools – Microsoft Edge DevTools-Tastenkombinationen | Microsoft Docs"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chromium) DevTools DOM Beispiel | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in die DOM-| MDN"  

> [!NOTE]
> <span data-ttu-id="443e5-347">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="443e5-347">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="443e5-348">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/dom/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="443e5-348">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="443e5-350">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="443e5-350">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

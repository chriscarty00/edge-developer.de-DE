---
description: Hier erfahren Sie, wie Sie Knoten anzeigen, nach Knoten suchen, Knoten bearbeiten, auf Knoten in der Konsole verweisen, Knoten Änderungen unterbrechen und vieles mehr.
title: Erste Schritte beim Anzeigen und Ändern des DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 5b12b984aed7e35ce11dd45e8bc33f5d5fd454f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231104"
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

# <span data-ttu-id="d8812-104">Erste Schritte beim Anzeigen und Ändern des DOM</span><span class="sxs-lookup"><span data-stu-id="d8812-104">Get started with viewing and changing the DOM</span></span>  

<span data-ttu-id="d8812-105">Führen Sie diese interaktiven Lernprogramme aus, um die Grundlagen zum Anzeigen und Ändern des DOM einer Seite mit Microsoft Edge devtools zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="d8812-105">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="d8812-106">In diesem Lernprogramm wird davon ausgegangen, dass Sie den Unterschied zwischen Dom und HTML kennen.</span><span class="sxs-lookup"><span data-stu-id="d8812-106">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="d8812-107">Navigieren Sie zu [Anhang: HTML im Vergleich zum Dom](#appendix-html-versus-the-dom) , um eine Erläuterung zu geben.</span><span class="sxs-lookup"><span data-stu-id="d8812-107">Navigate to [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <span data-ttu-id="d8812-108">Öffnen von Dom-Beispielen</span><span class="sxs-lookup"><span data-stu-id="d8812-108">Open DOM examples</span></span>  

1.  <span data-ttu-id="d8812-109">Halten `Control` Sie \ (Windows, Linux \) oder `Command` \ (macOS \) gedrückt, und wählen Sie **DOM-Beispiele** aus, die auf einer neuen Registerkarte geöffnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8812-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="d8812-110">DOM-Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8812-110">DOM Examples</span></span>][GlitchDomExamples]  
    
## <span data-ttu-id="d8812-111">DOM-Knoten anzeigen</span><span class="sxs-lookup"><span data-stu-id="d8812-111">View DOM nodes</span></span>  

<span data-ttu-id="d8812-112">In der DOM-Struktur des Elements Panels werden alle DOM-bezogenen Aktivitäten in devtools durchführen.</span><span class="sxs-lookup"><span data-stu-id="d8812-112">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <span data-ttu-id="d8812-113">Überprüfen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="d8812-113">Inspect a node</span></span>  

<span data-ttu-id="d8812-114">Wenn Sie an einem bestimmten DOM-Knoten interessiert sind, ist über **prüfen** eine schnelle Möglichkeit, devtools zu öffnen und diesen Knoten zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="d8812-114">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="d8812-115">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-115">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-116">Wählen Sie unter **Knoten überprüfen die**Option **Michelangelo** aus, und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-116">Under **Inspect a Node**, right-choose **Michelangelo** and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="d8812-118">Überprüfen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="d8812-118">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="d8812-119">Das **Element** Panel von devtools wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d8812-119">The **Elements** panel of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="d8812-120">ist in der **DOM-Struktur**hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="d8812-120">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Markieren des Michelangelo-Knotens" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="d8812-122">Markieren des `Michelangelo` Knotens</span><span class="sxs-lookup"><span data-stu-id="d8812-122">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="d8812-123">Klicken Sie in der oberen linken Ecke von devtools auf das Symbol **inspizieren** \ ( ![ Inspect ][ImageInspectIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d8812-123">Click the **Inspect** \(![Inspect][ImageInspectIcon]\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Das Symbol "überprüfen"" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="d8812-125">Das Symbol "über **prüfen** "</span><span class="sxs-lookup"><span data-stu-id="d8812-125">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="d8812-126">Klicken Sie unter **Knoten prüfen**auf den Text **Tokyo** .</span><span class="sxs-lookup"><span data-stu-id="d8812-126">Under **Inspect a Node**, click the **Tokyo** text.</span></span>  <span data-ttu-id="d8812-127">Ist nun `<li>Tokyo</li>` in der DOM-Struktur hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="d8812-127">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="d8812-128">Das Überprüfen eines Knotens ist auch der erste Schritt zum Anzeigen und Ändern der Formatvorlagen eines Knotens.</span><span class="sxs-lookup"><span data-stu-id="d8812-128">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="d8812-129">Navigieren Sie zu den [ersten Schritten beim Anzeigen und Ändern von CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="d8812-129">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <span data-ttu-id="d8812-130">Navigieren in der DOM-Struktur mithilfe einer Tastatur</span><span class="sxs-lookup"><span data-stu-id="d8812-130">Navigate the DOM Tree with a keyboard</span></span>  

<span data-ttu-id="d8812-131">Nachdem Sie einen Knoten in der DOM-Struktur ausgewählt haben, können Sie mit der Tastatur in der DOM-Struktur navigieren.</span><span class="sxs-lookup"><span data-stu-id="d8812-131">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="d8812-132">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-132">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-133">Wählen Sie unter **DOM-Struktur mit einer Tastatur navigieren mit der**rechten Maustaste **Ringo** aus, und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-133">Under **Navigate the DOM Tree with a Keyboard**, right-choose **Ringo** and choose **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="d8812-134">ist in der DOM-Struktur ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d8812-134">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Überprüfen des Ringo-Knotens" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="d8812-136">Überprüfen des `Ringo` Knotens</span><span class="sxs-lookup"><span data-stu-id="d8812-136">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="d8812-137">Drücken Sie zweimal die `Up` Pfeiltaste.</span><span class="sxs-lookup"><span data-stu-id="d8812-137">Press the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="d8812-138"> markiert ist.</span><span class="sxs-lookup"><span data-stu-id="d8812-138">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Überprüfen des UL-Knotens" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="d8812-140">Überprüfen des `ul` Knotens</span><span class="sxs-lookup"><span data-stu-id="d8812-140">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="d8812-141">Drücken Sie die `Left` Pfeiltaste.</span><span class="sxs-lookup"><span data-stu-id="d8812-141">Press the `Left` arrow key.</span></span>  <span data-ttu-id="d8812-142">Die `<ul>` Liste wird reduziert.</span><span class="sxs-lookup"><span data-stu-id="d8812-142">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="d8812-143">Drücken Sie `Left` erneut die Pfeiltaste.</span><span class="sxs-lookup"><span data-stu-id="d8812-143">Press the `Left` arrow key again.</span></span>  <span data-ttu-id="d8812-144">Das übergeordnete Element des `<ul>` Knotens ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d8812-144">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="d8812-145">In diesem Fall ist es die `<div>` mit der ID `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="d8812-145">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="d8812-146">Drücken Sie `Down` zweimal die Pfeiltaste, damit Sie die `<ul>` Liste, die Sie soeben reduziert haben, erneut ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="d8812-146">Press the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="d8812-147">Es sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="d8812-147">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="d8812-148">Drücken Sie die `Right` Pfeiltaste.</span><span class="sxs-lookup"><span data-stu-id="d8812-148">Press the `Right` arrow key.</span></span>  <span data-ttu-id="d8812-149">Die Liste wird erweitert.</span><span class="sxs-lookup"><span data-stu-id="d8812-149">The list expands.</span></span>  

### <span data-ttu-id="d8812-150">Scrollen Sie in die Ansicht</span><span class="sxs-lookup"><span data-stu-id="d8812-150">Scroll into view</span></span>  

<span data-ttu-id="d8812-151">Wenn Sie die DOM-Struktur anzeigen, sind Sie möglicherweise an einem DOM-Knoten interessiert, der sich derzeit nicht im Viewport befindet.</span><span class="sxs-lookup"><span data-stu-id="d8812-151">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="d8812-152">Angenommen, Sie haben einen Bildlauf zum Ende der Seite durchgeführt, und Sie sind an dem `<h1>` Knoten oben auf der Seite interessiert.</span><span class="sxs-lookup"><span data-stu-id="d8812-152">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="d8812-153">Durch **Scrollen in die Ansicht** können Sie das Ansichtsfenster schnell neu positionieren, sodass Sie den Knoten überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="d8812-153">**Scroll into view** lets you quickly reposition the viewport so that you are able to review the node.</span></span>  

1.  <span data-ttu-id="d8812-154">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-154">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-155">Klicken Sie unter **Ansicht scrollen**mit der rechten Maustaste auf **Magritte** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-155">Under **Scroll into View**, right-choose **Magritte** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="d8812-156">Scrollen Sie zum Ende der Seite "DOM-Beispiele".</span><span class="sxs-lookup"><span data-stu-id="d8812-156">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="d8812-157">Der `<li>Magritte</li>` Knoten sollte weiterhin in ihrer DOM-Struktur ausgewählt sein.</span><span class="sxs-lookup"><span data-stu-id="d8812-157">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="d8812-158">Wenn dies nicht der Fall ist, gehen Sie zurück, um [in die Ansicht zu scrollen](#scroll-into-view) und neu zu beginnen</span><span class="sxs-lookup"><span data-stu-id="d8812-158">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="d8812-159">Zeigen Sie auf den `<li>Magritte</li>` Knoten, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Bildlaufansicht**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-159">Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.</span></span>  <span data-ttu-id="d8812-160">Ihr Viewport scrollt wieder nach oben, sodass Sie den **Magritte** -Knoten überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="d8812-160">Your viewport scrolls back up so that you may review the **Magritte** node.</span></span>  <span data-ttu-id="d8812-161">Navigieren Sie zu [Anhang: fehlende Optionen](#appendix-missing-options) , wenn Sie die Option **Scrollen in Ansicht** nicht überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="d8812-161">Navigate to [Appendix: Missing options](#appendix-missing-options) if you are not able to review the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scrollen Sie in die Ansicht" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="d8812-163">Scrollen Sie in die Ansicht</span><span class="sxs-lookup"><span data-stu-id="d8812-163">Scroll into view</span></span>**  
    :::image-end:::  

### <span data-ttu-id="d8812-164">Suchen nach Knoten</span><span class="sxs-lookup"><span data-stu-id="d8812-164">Search for nodes</span></span>  

<span data-ttu-id="d8812-165">Sie können die DOM-Struktur nach Zeichenfolge, CSS-Auswahl oder XPath-Auswahl Durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="d8812-165">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="d8812-166">Fokussieren Sie den Cursor auf das **Element** Panel.</span><span class="sxs-lookup"><span data-stu-id="d8812-166">Focus your cursor on the **Elements** panel.</span></span>  
1.  <span data-ttu-id="d8812-167">Wählen Sie `Control` + `F` \ (Windows, Linux \) oder `Command` + `F` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-167">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="d8812-168">Die Suchleiste wird am unteren Rand der DOM-Struktur geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d8812-168">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="d8812-169">Geben Sie `The Moon is a Harsh Mistress` ein.</span><span class="sxs-lookup"><span data-stu-id="d8812-169">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="d8812-170">Der letzte Satz ist in der DOM-Struktur hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="d8812-170">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Markieren der Abfrage in der Suchleiste" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="d8812-172">Markieren der Abfrage in der Suchleiste</span><span class="sxs-lookup"><span data-stu-id="d8812-172">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d8812-173">Wie bereits erwähnt, unterstützt die Suchleiste auch CSS-und XPath-Auswahlen.</span><span class="sxs-lookup"><span data-stu-id="d8812-173">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <span data-ttu-id="d8812-174">Bearbeiten des DOM</span><span class="sxs-lookup"><span data-stu-id="d8812-174">Edit the DOM</span></span>  

<span data-ttu-id="d8812-175">Sie können das Dom im Handumdrehen bearbeiten und überprüfen, wie sich die Änderungen auf die Seite auswirken.</span><span class="sxs-lookup"><span data-stu-id="d8812-175">You may edit the DOM on the fly and review how the changes affect the page.</span></span>  

### <span data-ttu-id="d8812-176">Bearbeiten von Inhalten</span><span class="sxs-lookup"><span data-stu-id="d8812-176">Edit content</span></span>  

<span data-ttu-id="d8812-177">Um den Inhalt eines Knotens zu bearbeiten, doppelklicken Sie auf den Inhalt in der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d8812-177">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="d8812-178">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-178">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-179">Klicken Sie unter **Inhalt bearbeiten**mit der rechten Maustaste auf **Michelle** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-179">Under **Edit Content**, right-choose **Michelle** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="d8812-180">Doppelklicken Sie in der DOM-Struktur auf `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="d8812-180">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="d8812-181">Mit anderen Worten: Doppelklicken Sie auf den Text zwischen `<li>` und `</li>` .</span><span class="sxs-lookup"><span data-stu-id="d8812-181">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="d8812-182">Der Text wird hervorgehoben, um anzugeben, dass er markiert ist.</span><span class="sxs-lookup"><span data-stu-id="d8812-182">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Bearbeiten des Texts" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="d8812-184">Bearbeiten des Texts</span><span class="sxs-lookup"><span data-stu-id="d8812-184">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="d8812-185">Löschen `Michelle` Sie, geben `Leela` Sie ein, und wählen Sie dann aus, `Enter` um die Änderung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="d8812-185">Delete `Michelle`, type `Leela`, then select `Enter` to confirm the change.</span></span>  <span data-ttu-id="d8812-186">Der Text im Dom wechselt von **Michelle** zu **Leela**.</span><span class="sxs-lookup"><span data-stu-id="d8812-186">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <span data-ttu-id="d8812-187">Bearbeiten von Attributen</span><span class="sxs-lookup"><span data-stu-id="d8812-187">Edit attributes</span></span>  

<span data-ttu-id="d8812-188">Um Attribute zu bearbeiten, doppelklicken Sie auf den Attributnamen oder-Wert.</span><span class="sxs-lookup"><span data-stu-id="d8812-188">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="d8812-189">Befolgen Sie die Anweisungen, um zu erfahren, wie Sie einem Knoten Attribute hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d8812-189">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="d8812-190">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-190">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-191">Klicken Sie unter **Attribute bearbeiten**mit der rechten Maustaste auf **Howard** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-191">Under **Edit Attributes**, right-choose **Howard** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="d8812-192">Doppelklicken Sie auf `<li>` .</span><span class="sxs-lookup"><span data-stu-id="d8812-192">Double-click `<li>`.</span></span>  <span data-ttu-id="d8812-193">Der Text wird hervorgehoben, um anzugeben, dass der Knoten markiert ist.</span><span class="sxs-lookup"><span data-stu-id="d8812-193">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Bearbeiten des Knotens" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="d8812-195">Bearbeiten des Knotens</span><span class="sxs-lookup"><span data-stu-id="d8812-195">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d8812-196">Drücken Sie die `Right` Pfeiltaste, fügen Sie ein Leerzeichen hinzu, geben `style="background-color:gold"` Sie ein, und wählen Sie dann aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d8812-196">Press the `Right` arrow key, add a space, type `style="background-color:gold"`, and then select `Enter`.</span></span>  <span data-ttu-id="d8812-197">Die Hintergrundfarbe des Knotens ändert sich in Gold.</span><span class="sxs-lookup"><span data-stu-id="d8812-197">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Hinzufügen eines Formatvorlagenattributs zum Knoten" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="d8812-199">Hinzufügen eines `style` Attributs zum Knoten</span><span class="sxs-lookup"><span data-stu-id="d8812-199">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="d8812-200">Knotentyp bearbeiten</span><span class="sxs-lookup"><span data-stu-id="d8812-200">Edit node type</span></span>  

<span data-ttu-id="d8812-201">Um den Typ eines Knotens zu bearbeiten, doppelklicken Sie auf den Typ, und geben Sie dann den neuen Typ ein.</span><span class="sxs-lookup"><span data-stu-id="d8812-201">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="d8812-202">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-202">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-203">Klicken Sie unter **Knotentyp bearbeiten**mit der rechten Maustaste auf **Hank** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-203">Under **Edit Node Type**, right-choose **Hank** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="d8812-204">Doppelklicken Sie auf `<li>` .</span><span class="sxs-lookup"><span data-stu-id="d8812-204">Double-click `<li>`.</span></span>  <span data-ttu-id="d8812-205">Der Text `li` ist hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="d8812-205">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="d8812-206">Löschen `li` Sie, geben `button` Sie ein, und wählen Sie dann aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d8812-206">Delete `li`, type `button`, then select `Enter`.</span></span>  <span data-ttu-id="d8812-207">Der `<li>` Knoten wird in einen `<button>` Knoten geändert.</span><span class="sxs-lookup"><span data-stu-id="d8812-207">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Ändern des Knotentyps in die Schaltfläche" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="d8812-209">Ändern des Knotentyps in</span><span class="sxs-lookup"><span data-stu-id="d8812-209">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <span data-ttu-id="d8812-210">Neuanordnen von DOM-Knoten</span><span class="sxs-lookup"><span data-stu-id="d8812-210">Reorder DOM nodes</span></span>  

<span data-ttu-id="d8812-211">Ziehen Sie Knoten, um Sie neu anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d8812-211">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="d8812-212">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-212">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-213">Klicken Sie unter **DOM-Knoten neu anordnen**auf **Elvis Presley** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-213">Under **Reorder DOM Nodes**, right-choose **Elvis Presley** and choose **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d8812-214">Dies ist das letzte Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="d8812-214">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="d8812-215">Ziehen Sie den Mauszeiger in der DOM-Struktur `<li>Elvis Presley</li>` an den Anfang der Liste.</span><span class="sxs-lookup"><span data-stu-id="d8812-215">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Ziehen des Knotens an den Anfang der Liste" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="d8812-217">Ziehen des Knotens an den Anfang der Liste</span><span class="sxs-lookup"><span data-stu-id="d8812-217">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="d8812-218">Zustand erzwingen</span><span class="sxs-lookup"><span data-stu-id="d8812-218">Force state</span></span>  

<span data-ttu-id="d8812-219">Sie können die Knoten zwingen, in Zuständen wie,,, und zu bleiben `:active` `:hover` `:focus` `:visited` `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="d8812-219">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="d8812-220">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-220">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-221">Zeigen Sie unter **Kraftzustand**auf **den Lord of the Flies**.</span><span class="sxs-lookup"><span data-stu-id="d8812-221">Under **Force state**, hover over **The Lord of the Flies**.</span></span>  <span data-ttu-id="d8812-222">Die Hintergrundfarbe wird Orange.</span><span class="sxs-lookup"><span data-stu-id="d8812-222">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="d8812-223">Klicken Sie mit der rechten Maustaste **auf den Lord of the Flies** und wählen Sie **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-223">Right-choose **The Lord of the Flies** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="d8812-224">Klicken Sie mit der rechten Maustaste `<li class="demo--hover">The Lord of the Flies</li>` , und wählen Sie **Zustand erzwingen**  >  **: hover**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-224">Right-click `<li class="demo--hover">The Lord of the Flies</li>` and choose **Force State** > **:hover**.</span></span>  <span data-ttu-id="d8812-225">Navigieren Sie zu [Anhang: fehlende Optionen](#appendix-missing-options) , wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8812-225">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  <span data-ttu-id="d8812-226">Die Hintergrundfarbe bleibt Orange, auch wenn Sie nicht tatsächlich über den Knoten zeigen.</span><span class="sxs-lookup"><span data-stu-id="d8812-226">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <span data-ttu-id="d8812-227">Ausblenden eines Knotens</span><span class="sxs-lookup"><span data-stu-id="d8812-227">Hide a node</span></span>  

<span data-ttu-id="d8812-228">Wählen Sie aus `H` , um einen Knoten auszublenden.</span><span class="sxs-lookup"><span data-stu-id="d8812-228">Select `H` to hide a node.</span></span>  

1.  <span data-ttu-id="d8812-229">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-229">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-230">Klicken Sie unter **Knoten ausblenden**mit der rechten Maustaste auf **den Stern mein Ziel** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-230">Under **Hide a node**, right-choose **The Stars My Destination** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="d8812-231">Drücken Sie die Eingabe `H` Taste.</span><span class="sxs-lookup"><span data-stu-id="d8812-231">Press the `H` key.</span></span>  <span data-ttu-id="d8812-232">Der Knoten ist ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="d8812-232">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Wie der Knoten in der DOM-Struktur aussieht, nachdem er ausgeblendet wurde" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="d8812-234">Wie der Knoten in der DOM-Struktur aussieht, nachdem er ausgeblendet wurde</span><span class="sxs-lookup"><span data-stu-id="d8812-234">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="d8812-235">Drücken Sie die `H` Taste erneut.</span><span class="sxs-lookup"><span data-stu-id="d8812-235">Press the `H` key again.</span></span>  <span data-ttu-id="d8812-236">Der Knoten wird wieder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8812-236">The node is shown again.</span></span>  

### <span data-ttu-id="d8812-237">Löschen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="d8812-237">Delete a node</span></span>  

<span data-ttu-id="d8812-238">Wählen Sie aus `Delete` , um einen Knoten zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d8812-238">Select `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="d8812-239">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-239">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-240">Klicken Sie unter **Knoten löschen mit der**rechten Maustaste auf **Fundament** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-240">Under **Delete a Node**, right-choose **Foundation** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="d8812-241">Drücken Sie die Eingabe `Delete` Taste.</span><span class="sxs-lookup"><span data-stu-id="d8812-241">Press the `Delete` key.</span></span>  <span data-ttu-id="d8812-242">Der Knoten wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d8812-242">The node is deleted.</span></span>  
    1.  <span data-ttu-id="d8812-243">Wählen Sie `Control` + `Z` \ (Windows, Linux \) oder `Command` + `Z` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-243">Select `Control`+`Z` \(Windows, Linux\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="d8812-244">Die letzte Aktion wird rückgängig gemacht, und der Knoten wird wieder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8812-244">The last action is undone and the node reappears.</span></span>  

## <span data-ttu-id="d8812-245">Access-Knoten in der Konsole</span><span class="sxs-lookup"><span data-stu-id="d8812-245">Access nodes in the Console</span></span>  

<span data-ttu-id="d8812-246">DevTools bietet einige Tastenkombinationen für den Zugriff auf DOM-Knoten über die Konsole oder das Abrufen von JavaScript-verweisen auf jede einzelne.</span><span class="sxs-lookup"><span data-stu-id="d8812-246">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <span data-ttu-id="d8812-247">Verweisen auf den aktuell ausgewählten Knoten mit $0</span><span class="sxs-lookup"><span data-stu-id="d8812-247">Reference the currently-selected node with $0</span></span>  

<span data-ttu-id="d8812-248">Wenn Sie einen Knoten überprüfen, `== $0` bedeutet der Text neben dem Knoten, dass Sie auf diesen Knoten in der Konsole mit der Variablen verweisen können `$0` .</span><span class="sxs-lookup"><span data-stu-id="d8812-248">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="d8812-249">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-249">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-250">Wählen Sie unter **Bezug auf den aktuell ausgewählten Knoten mit $0 mit**der rechten Maustaste **die linke Hand von Darkness** aus, und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-250">Under **Reference the currently-selected node with $0**, right-choose **The Left Hand of Darkness** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="d8812-251">Drücken Sie die Eingabe `Escape` Taste, um den Konsolen Einzug zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d8812-251">Press the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="d8812-252">Geben `$0` Sie ein, und drücken Sie die Eingabe `Enter` Taste.</span><span class="sxs-lookup"><span data-stu-id="d8812-252">Type `$0` and press the `Enter` key.</span></span>  <span data-ttu-id="d8812-253">Das Ergebnis des Ausdrucks zeigt, dass `$0` ausgewertet wird `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="d8812-253">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Das Ergebnis des ersten $0-Ausdrucks in der Konsole" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="d8812-255">Das Ergebnis des ersten `$0` Ausdrucks in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="d8812-255">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="d8812-256">Zeigen Sie mit der Maus auf das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="d8812-256">Hover over the result.</span></span>  <span data-ttu-id="d8812-257">Der Knoten ist im Viewport hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="d8812-257">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="d8812-258">Klicken Sie `<li>Dune</li>` in die DOM-Struktur, geben Sie `$0` die Konsole erneut ein, und wählen Sie dann `Enter` erneut aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-258">Click `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then select `Enter` again.</span></span>  <span data-ttu-id="d8812-259">Wird nun `$0` ausgewertet `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="d8812-259">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Das Ergebnis des zweiten $0-Ausdrucks in der Konsole" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="d8812-261">Das Ergebnis des zweiten `$0` Ausdrucks in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="d8812-261">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="d8812-262">Speichern als globale Variable</span><span class="sxs-lookup"><span data-stu-id="d8812-262">Store as global variable</span></span>  

<span data-ttu-id="d8812-263">Wenn Sie viele Male wieder auf einen Knoten verweisen müssen, speichern Sie ihn als globale Variable.</span><span class="sxs-lookup"><span data-stu-id="d8812-263">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="d8812-264">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-264">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-265">Wählen Sie unter **als globale Variable speichern** **den großen Ruhezustand** aus, und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-265">Under **Store as global variable**, right-choose **The Big Sleep** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="d8812-266">Klicken Sie `<li>The Big Sleep</li>` mit der rechten Maustaste in die DOM-Struktur, und wählen Sie **als globale Variable speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-266">Right-click `<li>The Big Sleep</li>` in the DOM Tree and choose **Store as global variable**.</span></span>  <span data-ttu-id="d8812-267">Navigieren Sie zu [Anhang: fehlende Optionen](#appendix-missing-options) , wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8812-267">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="d8812-268">Geben `temp1` Sie die Konsole ein, und wählen Sie dann aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d8812-268">Type `temp1` in the Console and then select `Enter`.</span></span>  <span data-ttu-id="d8812-269">Das Ergebnis des Ausdrucks zeigt, dass die Variable zum Knoten ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="d8812-269">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Das Ergebnis des temp1-Ausdrucks" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="d8812-271">Das Ergebnis des `temp1` Ausdrucks</span><span class="sxs-lookup"><span data-stu-id="d8812-271">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="d8812-272">Kopieren des js-Pfads</span><span class="sxs-lookup"><span data-stu-id="d8812-272">Copy JS path</span></span>  

<span data-ttu-id="d8812-273">Kopieren Sie den JavaScript-Pfad zu einem Knoten, wenn Sie in einem automatisierten Test darauf verweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="d8812-273">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="d8812-274">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-274">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-275">Klicken Sie unter **js-Pfad kopieren**mit der rechten Maustaste auf **die Brüder Karamazov** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-275">Under **Copy JS path**, right-choose **The Brothers Karamazov** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="d8812-276">Klicken Sie `<li>The Brothers Karamazov</li>` mit der rechten Maustaste in die DOM \*\*\*\*-Struktur, und wählen Sie Copy  >  **js Path**kopieren aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-276">Right-click `<li>The Brothers Karamazov</li>` in the DOM Tree and choose **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="d8812-277">Ein `document.querySelector()` Ausdruck, der in den Knoten aufgelöst wird, wurde in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="d8812-277">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="d8812-278">Wählen Sie `Control` + `V` \ (Windows, Linux \) oder `Command` + `V` \ (macOS \) aus, um den Ausdruck in die Konsole einzufügen.</span><span class="sxs-lookup"><span data-stu-id="d8812-278">Select `Control`+`V` \(Windows, Linux\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="d8812-279">Wählen Sie aus `Enter` , um den Ausdruck auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="d8812-279">Select `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Das Ergebnis des Ausdrucks "JS-Pfad kopieren"" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="d8812-281">Das Ergebnis des Ausdrucks " **js-Pfad kopieren** "</span><span class="sxs-lookup"><span data-stu-id="d8812-281">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <span data-ttu-id="d8812-282">Änderungen am Dom unterbrechen</span><span class="sxs-lookup"><span data-stu-id="d8812-282">Break on DOM changes</span></span>  

<span data-ttu-id="d8812-283">Mit devtools können Sie das JavaScript einer Seite anhalten, wenn das DOM vom JavaScript geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d8812-283">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <span data-ttu-id="d8812-284">Unterbrechen von Attributänderungen</span><span class="sxs-lookup"><span data-stu-id="d8812-284">Break on attribute modifications</span></span>  

<span data-ttu-id="d8812-285">Verwenden Sie die Attribut Änderungs Haltepunkte, wenn Sie das JavaScript anhalten möchten, das dazu führt, dass das Attribut eines Knotens geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d8812-285">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="d8812-286">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-286">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-287">Klicken Sie unter **Umbruch bei Attributänderungen auf** **Sauerkraut** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-287">Under **Break on attribute modifications**, right-choose **Sauerkraut** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="d8812-288">Klicken Sie in der DOM-Struktur mit der rechten Maustaste, `<li id="target">Sauerkraut</li>` und wählen Sie **bei**  >  **Attributänderungen**aufheben aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-288">In the DOM Tree, right-click `<li id="target">Sauerkraut</li>` and choose **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="d8812-289">Navigieren Sie zu [Anhang: fehlende Optionen](#appendix-missing-options) , wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8812-289">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Unterbrechen von Attributänderungen" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="d8812-291">Unterbrechen von Attributänderungen</span><span class="sxs-lookup"><span data-stu-id="d8812-291">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="d8812-292">Im nächsten Schritt werden Sie angewiesen, auf eine Schaltfläche zu klicken, mit der der Code der Seite angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d8812-292">In the next step you are going to be instructed to click a button that pauses the code of the page.</span></span>  <span data-ttu-id="d8812-293">Nachdem die Seite angehalten wurde, können Sie die Seite nicht mehr scrollen.</span><span class="sxs-lookup"><span data-stu-id="d8812-293">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="d8812-294">Sie müssen **Resume-Skript** \ ( ![ Resume ][ImageResumeScriptIcon] -Skript \) auswählen, um die Seite erneut scrollen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="d8812-294">You must choose **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Wo wird das Skript fortgesetzt?" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="d8812-296">Wo wird das Skript fortgesetzt?</span><span class="sxs-lookup"><span data-stu-id="d8812-296">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="d8812-297">Klicken Sie oben auf die Schaltfläche **Hintergrund einstellen** .</span><span class="sxs-lookup"><span data-stu-id="d8812-297">Click the **Set Background** button above.</span></span>  <span data-ttu-id="d8812-298">Dadurch wird das `style` Attribut des Knotens auf festgelegt `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="d8812-298">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="d8812-299">DevTools hält die Seite an und hebt den Code hervor, der zum Ändern des Attributs geführt hat.</span><span class="sxs-lookup"><span data-stu-id="d8812-299">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="d8812-300">Wählen Sie, wie bereits erwähnt, **fortsetzen-Skript** \ ( ![ Skript fortsetzen ][ImageResumeScriptIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-300">Choose **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\), as mentioned earlier.</span></span>  
    
### <span data-ttu-id="d8812-301">Unterbrechung beim Entfernen von Knoten</span><span class="sxs-lookup"><span data-stu-id="d8812-301">Break on node removal</span></span>  

<span data-ttu-id="d8812-302">Wenn Sie anhalten möchten, wenn ein bestimmter Knoten entfernt wird, verwenden Sie Haltepunkte für die Knoten Entfernung.</span><span class="sxs-lookup"><span data-stu-id="d8812-302">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="d8812-303">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-303">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-304">Klicken Sie unter **Unterbrechungs Vorgang beim Entfernen von Knoten mit der**rechten Maustaste auf **Neuromancer** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-304">Under **Break on Node Removal**, right-choose **Neuromancer** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="d8812-305">Klicken Sie in der DOM-Struktur mit der rechten Maustaste, `<li id="target">Neuromancer</li>` und wählen Sie **Unterbrechung beim**  >  **Entfernen von Knoten**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-305">In the DOM Tree, right-click `<li id="target">Neuromancer</li>` and choose **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="d8812-306">Navigieren Sie zu [Anhang: fehlende Optionen](#appendix-missing-options) , wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8812-306">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="d8812-307">Klicken Sie oben auf die Schaltfläche **Löschen** .</span><span class="sxs-lookup"><span data-stu-id="d8812-307">Click the **Delete** button above.</span></span>  <span data-ttu-id="d8812-308">DevTools hält die Seite an und hebt den Code hervor, der dazu geführt hat, dass der Knoten entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="d8812-308">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="d8812-309">Wählen Sie **Skript fortsetzen** \ ( ![ Skript fortsetzen ][ImageResumeScriptIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-309">Choose **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
### <span data-ttu-id="d8812-310">Unterbrechen von Änderungen an Teilstruktur</span><span class="sxs-lookup"><span data-stu-id="d8812-310">Break on subtree modifications</span></span>  

<span data-ttu-id="d8812-311">Nachdem Sie einen Haltepunkt für die Unterstruktur Änderung auf einem Knoten platziert haben, wird die Seite von devtools angehalten, wenn ein Nachfolger des Knotens hinzugefügt oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d8812-311">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="d8812-312">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="d8812-312">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="d8812-313">Wählen Sie unter unter **Brechung bei Teilstruktur Änderungen**mit der rechten Maustaste **ein Feuer auf der Tiefe** aus, und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-313">Under **Break on Subtree Modifications**, right-choose **A Fire Upon The Deep** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="d8812-314">Klicken Sie in der DOM-Struktur mit der rechten Maustaste auf `<ul id="target">` den Knoten oben `<li>A Fire Upon the Deep</li>` , und wählen Sie unter Teil \*\*\*\*  >  **Strukturänderungen**aufheben aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-314">In the DOM Tree, right-click `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, and choose **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="d8812-315">Navigieren Sie zu [Anhang: fehlende Optionen](#appendix-missing-options) , wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8812-315">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="d8812-316">Wählen Sie **Kind hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-316">Choose **Add Child**.</span></span>  <span data-ttu-id="d8812-317">Der Code wird angehalten `<li>` , weil der Liste ein Knoten hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d8812-317">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="d8812-318">Wählen Sie **Skript fortsetzen** \ ( ![ Skript fortsetzen ][ImageResumeScriptIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-318">Choose **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
## <span data-ttu-id="d8812-319">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d8812-319">Next steps</span></span>  

<span data-ttu-id="d8812-320">, Die die meisten der Dom-bezogenen Features in devtools abdeckt.</span><span class="sxs-lookup"><span data-stu-id="d8812-320">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="d8812-321">Sie können die restlichen Personen entdecken, indem Sie mit der rechten Maustaste auf Knoten in der DOM-Struktur klicken und mit den anderen Optionen experimentieren, die in diesem Lernprogramm nicht behandelt wurden.</span><span class="sxs-lookup"><span data-stu-id="d8812-321">You are able to discover the rest of them by right-clicking nodes in the DOM Tree and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="d8812-322">Navigieren Sie zu den [Tastenkombinationen des Elements Panel][DevToolsShortcutsElements].</span><span class="sxs-lookup"><span data-stu-id="d8812-322">Navigate to [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="d8812-323">Schauen Sie sich die [Microsoft Edge devtools-Startseite][MicrosoftEdgeDevTools] an, um alles mögliche zu entdecken, was Sie mit devtools tun können.</span><span class="sxs-lookup"><span data-stu-id="d8812-323">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <span data-ttu-id="d8812-324">Anhang: HTML im Vergleich zum Dom</span><span class="sxs-lookup"><span data-stu-id="d8812-324">Appendix: HTML versus the DOM</span></span>  

<span data-ttu-id="d8812-325">Im folgenden Abschnitt wird schnell der Unterschied zwischen HTML und dem Dom erläutert.</span><span class="sxs-lookup"><span data-stu-id="d8812-325">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d8812-326">Wenn Sie eine Seite mit einem Webbrowser anfordern, gibt der Server HTML wie den folgenden Codeausschnitt zurück.</span><span class="sxs-lookup"><span data-stu-id="d8812-326">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

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
      <span data-ttu-id="d8812-327">Der Browser analysiert den HTML-Code und erstellt eine Struktur von Objekten wie der folgenden Liste.</span><span class="sxs-lookup"><span data-stu-id="d8812-327">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
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

<span data-ttu-id="d8812-328">Diese Struktur von Objekten oder Knoten, die den Inhalt der Seite darstellen, wird als DOM bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d8812-328">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d8812-329">Im Moment sieht es genauso aus wie das HTML, aber angenommen, das Skript, auf das am Ende des HTML-Codes verwiesen wird, führt den folgenden Codeausschnitt aus.</span><span class="sxs-lookup"><span data-stu-id="d8812-329">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d8812-330">Dieser Code entfernt den `h1` Knoten und fügt `p` dem DOM einen weiteren Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="d8812-330">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="d8812-331">Das vollständige Dom zeigt nun die folgende Liste an.</span><span class="sxs-lookup"><span data-stu-id="d8812-331">The complete DOM now displays the following list.</span></span>  
      
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

<span data-ttu-id="d8812-332">Der HTML-Code für die Seite ist jetzt anders als das DOM.</span><span class="sxs-lookup"><span data-stu-id="d8812-332">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="d8812-333">Mit anderen Worten, HTML steht für den anfänglichen Seiteninhalt, und das DOM steht für den aktuellen Seiteninhalt.</span><span class="sxs-lookup"><span data-stu-id="d8812-333">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="d8812-334">Wenn JavaScript-Knoten hinzugefügt, entfernt oder bearbeitet werden, wird das DOM anders als das HTML-Code.</span><span class="sxs-lookup"><span data-stu-id="d8812-334">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="d8812-335">Navigieren Sie zu [Einführung in das DOM][MDNIntroductionToDOM] , um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d8812-335">Navigate to [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and choose **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  Navigate to [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <span data-ttu-id="d8812-336">Anhang: fehlende Optionen</span><span class="sxs-lookup"><span data-stu-id="d8812-336">Appendix: Missing options</span></span>  

<span data-ttu-id="d8812-337">Viele der Anweisungen in diesem Lernprogramm weisen Sie an, mit der rechten Maustaste auf einen Knoten in der DOM-Struktur zu klicken und dann im Kontextmenü, das eingeblendet wird, eine Option auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d8812-337">Many of the instructions in this tutorial instruct you to right-click a node in the DOM Tree and then select an option from the context menu that pops up.</span></span>  <span data-ttu-id="d8812-338">Wenn die angegebene Option im Kontextmenü nicht angezeigt wird, versuchen Sie, mit der rechten Maustaste auf den Knotentext zu klicken.</span><span class="sxs-lookup"><span data-stu-id="d8812-338">If the specified option in the context menu is not displayed, try right-clicking away from the node text.</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Auswahlmöglichkeiten, wenn alle Optionen nicht angezeigt werden" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="d8812-340">Auswahlmöglichkeiten, wenn alle Optionen nicht angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="d8812-340">Where to choose if all of the options are not displayed</span></span>  
:::image-end:::  

## <span data-ttu-id="d8812-341">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="d8812-341">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge \ (Chrom \) Developer Tools | Microsoft docs"  
[DevToolsCssGetStarted]: ../css/index.md "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-panel-keyboard-shortcuts "Tastenkombinationen im Element Panel – Tastenkombinationen für Microsoft Edge devtools | Microsoft docs"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chrom) devtools Dom-Beispiel | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in das DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="d8812-347">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8812-347">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d8812-348">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/dom/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d8812-348">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="d8812-350">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d8812-350">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

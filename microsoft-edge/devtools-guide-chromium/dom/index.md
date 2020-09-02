---
title: Erste Schritte beim Anzeigen und Ändern des DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 6d41b072a8bd19ae728cc02b43eb2f843d91b332
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991205"
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





# <span data-ttu-id="3cf3a-103">Erste Schritte beim Anzeigen und Ändern des DOM</span><span class="sxs-lookup"><span data-stu-id="3cf3a-103">Get started with viewing and changing the DOM</span></span>   



<span data-ttu-id="3cf3a-104">Führen Sie diese interaktiven Lernprogramme aus, um die Grundlagen zum Anzeigen und Ändern des DOM einer Seite mit Microsoft Edge devtools zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-104">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="3cf3a-105">In diesem Lernprogramm wird davon ausgegangen, dass Sie den Unterschied zwischen Dom und HTML kennen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-105">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="3cf3a-106">Eine Erläuterung finden Sie unter [Anhang: HTML im Vergleich zum Dom](#appendix-html-versus-the-dom) .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-106">See [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <span data-ttu-id="3cf3a-107">Öffnen von Dom-Beispielen</span><span class="sxs-lookup"><span data-stu-id="3cf3a-107">Open DOM examples</span></span>  

1.  <span data-ttu-id="3cf3a-108">Halten `Control` Sie \ (Windows \) oder `Command` \ (macOS \) gedrückt, und klicken Sie auf **DOM-Beispiele** , um Sie in einer neuen Registerkarte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="3cf3a-109">DOM-Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cf3a-109">DOM Examples</span></span>][GlitchDomExamples]  
    
## <span data-ttu-id="3cf3a-110">DOM-Knoten anzeigen</span><span class="sxs-lookup"><span data-stu-id="3cf3a-110">View DOM nodes</span></span>   

<span data-ttu-id="3cf3a-111">In der DOM-Struktur des Elements Panels werden alle DOM-bezogenen Aktivitäten in devtools durchführen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-111">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <span data-ttu-id="3cf3a-112">Überprüfen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="3cf3a-112">Inspect a node</span></span>   

<span data-ttu-id="3cf3a-113">Wenn Sie an einem bestimmten DOM-Knoten interessiert sind, ist über **prüfen** eine schnelle Möglichkeit, devtools zu öffnen und diesen Knoten zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-113">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="3cf3a-114">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-114">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-115">Klicken Sie unter **Knoten prüfen mit der**rechten Maustaste auf **Michelangelo** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-115">Under **Inspect a Node**, right-click **Michelangelo** and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="3cf3a-117">Überprüfen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="3cf3a-117">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="3cf3a-118">Das **Element** Panel von devtools wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-118">The **Elements** panel of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="3cf3a-119">ist in der **DOM-Struktur**hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-119">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Markieren des Michelangelo-Knotens" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="3cf3a-121">Markieren des `Michelangelo` Knotens</span><span class="sxs-lookup"><span data-stu-id="3cf3a-121">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="3cf3a-122">Klicken Sie in der oberen linken Ecke von devtools auf das Symbol **inspizieren** \ ( ![ Inspect ][ImageInspectIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-122">Click the **Inspect** \(![Inspect][ImageInspectIcon]\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Das Symbol "überprüfen"" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="3cf3a-124">Das Symbol "über **prüfen** "</span><span class="sxs-lookup"><span data-stu-id="3cf3a-124">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="3cf3a-125">Klicken Sie unter **Knoten prüfen**auf den Text **Tokyo** .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-125">Under **Inspect a Node**, click the **Tokyo** text.</span></span>  <span data-ttu-id="3cf3a-126">Ist nun `<li>Tokyo</li>` in der DOM-Struktur hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-126">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="3cf3a-127">Das Überprüfen eines Knotens ist auch der erste Schritt zum Anzeigen und Ändern der Formatvorlagen eines Knotens.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-127">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="3cf3a-128">Weitere Informationen finden Sie unter [Erste Schritte beim Anzeigen und Ändern von CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="3cf3a-128">See [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <span data-ttu-id="3cf3a-129">Navigieren in der DOM-Struktur mithilfe einer Tastatur</span><span class="sxs-lookup"><span data-stu-id="3cf3a-129">Navigate the DOM Tree with a keyboard</span></span>   

<span data-ttu-id="3cf3a-130">Nachdem Sie einen Knoten in der DOM-Struktur ausgewählt haben, können Sie mit der Tastatur in der DOM-Struktur navigieren.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-130">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="3cf3a-131">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-131">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-132">Klicken Sie unter **der DOM-Struktur mit einer Tastatur navigieren mit der**rechten Maustaste auf **Ringo** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-132">Under **Navigate the DOM Tree with a Keyboard**, right-click **Ringo** and select **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="3cf3a-133">ist in der DOM-Struktur ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-133">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Überprüfen des Ringo-Knotens" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="3cf3a-135">Überprüfen des `Ringo` Knotens</span><span class="sxs-lookup"><span data-stu-id="3cf3a-135">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="3cf3a-136">Drücken Sie zweimal die `Up` Pfeiltaste.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-136">Press the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="3cf3a-137"> markiert ist.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-137">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Überprüfen des UL-Knotens" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="3cf3a-139">Überprüfen des `ul` Knotens</span><span class="sxs-lookup"><span data-stu-id="3cf3a-139">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="3cf3a-140">Drücken Sie die `Left` Pfeiltaste.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-140">Press the `Left` arrow key.</span></span>  <span data-ttu-id="3cf3a-141">Die `<ul>` Liste wird reduziert.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-141">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="3cf3a-142">Drücken Sie `Left` erneut die Pfeiltaste.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-142">Press the `Left` arrow key again.</span></span>  <span data-ttu-id="3cf3a-143">Das übergeordnete Element des `<ul>` Knotens ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-143">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="3cf3a-144">In diesem Fall ist es die `<div>` mit der ID `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-144">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="3cf3a-145">Drücken Sie `Down` zweimal die Pfeiltaste, damit Sie die `<ul>` Liste, die Sie soeben reduziert haben, erneut ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-145">Press the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="3cf3a-146">Es sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="3cf3a-146">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="3cf3a-147">Drücken Sie die `Right` Pfeiltaste.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-147">Press the `Right` arrow key.</span></span>  <span data-ttu-id="3cf3a-148">Die Liste wird erweitert.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-148">The list expands.</span></span>  

### <span data-ttu-id="3cf3a-149">Scrollen Sie in die Ansicht</span><span class="sxs-lookup"><span data-stu-id="3cf3a-149">Scroll into view</span></span>   

<span data-ttu-id="3cf3a-150">Wenn Sie die DOM-Struktur anzeigen, sind Sie möglicherweise an einem DOM-Knoten interessiert, der sich derzeit nicht im Viewport befindet.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-150">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="3cf3a-151">Angenommen, Sie haben einen Bildlauf zum Ende der Seite durchgeführt, und Sie sind an dem `<h1>` Knoten oben auf der Seite interessiert.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-151">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="3cf3a-152">Durch **Scrollen in die Ansicht** können Sie das Ansichtsfenster schnell neu positionieren, damit Sie den Knoten sehen können.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-152">**Scroll into view** lets you quickly reposition the viewport so that you are able to see the node.</span></span>  

1.  <span data-ttu-id="3cf3a-153">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-153">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-154">Klicken Sie unter **Ansicht scrollen**mit der rechten Maustaste auf **Magritte** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-154">Under **Scroll into View**, right-click **Magritte** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="3cf3a-155">Scrollen Sie zum Ende der Seite "DOM-Beispiele".</span><span class="sxs-lookup"><span data-stu-id="3cf3a-155">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="3cf3a-156">Der `<li>Magritte</li>` Knoten sollte weiterhin in ihrer DOM-Struktur ausgewählt sein.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-156">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="3cf3a-157">Wenn dies nicht der Fall ist, gehen Sie zurück, um [in die Ansicht zu scrollen](#scroll-into-view) und neu zu beginnen</span><span class="sxs-lookup"><span data-stu-id="3cf3a-157">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="3cf3a-158">Klicken Sie mit der rechten Maustaste auf den `<li>Magritte</li>` Knoten, und wählen Sie **in Ansicht scrollen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-158">Right-click the `<li>Magritte</li>` node and select **Scroll into view**.</span></span>  <span data-ttu-id="3cf3a-159">Ihr Viewport führt einen Bildlauf nach oben durch, damit Sie den **Magritte** -Knoten sehen können.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-159">Your viewport scrolls back up so that you may see the **Magritte** node.</span></span>  <span data-ttu-id="3cf3a-160">Weitere Informationen finden Sie im [Anhang: fehlende Optionen](#appendix-missing-options) , wenn die Option **Scrollen in Ansicht** nicht angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-160">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scrollen Sie in die Ansicht" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="3cf3a-162">Scrollen Sie in die Ansicht</span><span class="sxs-lookup"><span data-stu-id="3cf3a-162">Scroll into view</span></span>**  
    :::image-end:::  

### <span data-ttu-id="3cf3a-163">Suchen nach Knoten</span><span class="sxs-lookup"><span data-stu-id="3cf3a-163">Search for nodes</span></span>   

<span data-ttu-id="3cf3a-164">Sie können die DOM-Struktur nach Zeichenfolge, CSS-Auswahl oder XPath-Auswahl Durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-164">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="3cf3a-165">Fokussieren Sie den Cursor auf das **Element** Panel.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-165">Focus your cursor on the **Elements** panel.</span></span>  
1.  <span data-ttu-id="3cf3a-166">Drücken Sie `Control` + `F` \ (Windows \) oder `Command` + `F` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-166">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="3cf3a-167">Die Suchleiste wird am unteren Rand der DOM-Struktur geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-167">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="3cf3a-168">Geben Sie `The Moon is a Harsh Mistress` ein.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-168">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="3cf3a-169">Der letzte Satz ist in der DOM-Struktur hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-169">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Markieren der Abfrage in der Suchleiste" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="3cf3a-171">Markieren der Abfrage in der Suchleiste</span><span class="sxs-lookup"><span data-stu-id="3cf3a-171">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="3cf3a-172">Wie bereits erwähnt, unterstützt die Suchleiste auch CSS-und XPath-Auswahlen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-172">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <span data-ttu-id="3cf3a-173">Bearbeiten des DOM</span><span class="sxs-lookup"><span data-stu-id="3cf3a-173">Edit the DOM</span></span>   

<span data-ttu-id="3cf3a-174">Sie können das Dom im Handumdrehen bearbeiten und sehen, wie sich diese Änderungen auf die Seite auswirken.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-174">You may edit the DOM on the fly and see how those changes affect the page.</span></span>  

### <span data-ttu-id="3cf3a-175">Bearbeiten von Inhalten</span><span class="sxs-lookup"><span data-stu-id="3cf3a-175">Edit content</span></span>   

<span data-ttu-id="3cf3a-176">Um den Inhalt eines Knotens zu bearbeiten, doppelklicken Sie auf den Inhalt in der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-176">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="3cf3a-177">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-177">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-178">Klicken Sie unter **Inhalt bearbeiten**mit der rechten Maustaste auf **Michelle** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-178">Under **Edit Content**, right-click **Michelle** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3cf3a-179">Doppelklicken Sie in der DOM-Struktur auf `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-179">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="3cf3a-180">Mit anderen Worten: Doppelklicken Sie auf den Text zwischen `<li>` und `</li>` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-180">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="3cf3a-181">Der Text wird hervorgehoben, um anzugeben, dass er markiert ist.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-181">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Bearbeiten des Texts" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="3cf3a-183">Bearbeiten des Texts</span><span class="sxs-lookup"><span data-stu-id="3cf3a-183">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="3cf3a-184">Löschen `Michelle` Sie, geben `Leela` Sie ein, und drücken Sie dann, `Enter` um die Änderung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-184">Delete `Michelle`, type `Leela`, then press `Enter` to confirm the change.</span></span>  <span data-ttu-id="3cf3a-185">Der Text im Dom wechselt von **Michelle** zu **Leela**.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-185">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <span data-ttu-id="3cf3a-186">Bearbeiten von Attributen</span><span class="sxs-lookup"><span data-stu-id="3cf3a-186">Edit attributes</span></span>   

<span data-ttu-id="3cf3a-187">Um Attribute zu bearbeiten, doppelklicken Sie auf den Attributnamen oder-Wert.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-187">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="3cf3a-188">Befolgen Sie die Anweisungen, um zu erfahren, wie Sie einem Knoten Attribute hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-188">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="3cf3a-189">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-189">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-190">Klicken Sie unter **Attribute bearbeiten**mit der rechten Maustaste auf **Howard** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-190">Under **Edit Attributes**, right-click **Howard** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="3cf3a-191">Doppelklicken Sie auf `<li>` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-191">Double-click `<li>`.</span></span>  <span data-ttu-id="3cf3a-192">Der Text wird hervorgehoben, um anzugeben, dass der Knoten markiert ist.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-192">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Bearbeiten des Knotens" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="3cf3a-194">Bearbeiten des Knotens</span><span class="sxs-lookup"><span data-stu-id="3cf3a-194">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3cf3a-195">Drücken Sie die `Right` Pfeiltaste, fügen Sie ein Leerzeichen hinzu, geben Sie ein `style="background-color:gold"` , und drücken Sie dann `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-195">Press the `Right` arrow key, add a space, type `style="background-color:gold"`, and then press `Enter`.</span></span>  <span data-ttu-id="3cf3a-196">Die Hintergrundfarbe des Knotens ändert sich in Gold.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-196">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Hinzufügen eines Formatvorlagenattributs zum Knoten" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="3cf3a-198">Hinzufügen eines `style` Attributs zum Knoten</span><span class="sxs-lookup"><span data-stu-id="3cf3a-198">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="3cf3a-199">Knotentyp bearbeiten</span><span class="sxs-lookup"><span data-stu-id="3cf3a-199">Edit node type</span></span>   

<span data-ttu-id="3cf3a-200">Um den Typ eines Knotens zu bearbeiten, doppelklicken Sie auf den Typ, und geben Sie dann den neuen Typ ein.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-200">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="3cf3a-201">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-201">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-202">Klicken Sie unter **Knotentyp bearbeiten**mit der rechten Maustaste auf **Hank** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-202">Under **Edit Node Type**, right-click **Hank** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3cf3a-203">Doppelklicken Sie auf `<li>` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-203">Double-click `<li>`.</span></span>  <span data-ttu-id="3cf3a-204">Der Text `li` ist hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-204">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="3cf3a-205">Löschen `li` Sie, geben `button` Sie ein, und drücken Sie dann `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-205">Delete `li`, type `button`, then press `Enter`.</span></span>  <span data-ttu-id="3cf3a-206">Der `<li>` Knoten wird in einen `<button>` Knoten geändert.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-206">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Ändern des Knotentyps in die Schaltfläche" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="3cf3a-208">Ändern des Knotentyps in</span><span class="sxs-lookup"><span data-stu-id="3cf3a-208">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <span data-ttu-id="3cf3a-209">Neuanordnen von DOM-Knoten</span><span class="sxs-lookup"><span data-stu-id="3cf3a-209">Reorder DOM nodes</span></span>   

<span data-ttu-id="3cf3a-210">Ziehen Sie Knoten, um Sie neu anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-210">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="3cf3a-211">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-211">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-212">Klicken Sie unter **DOM-Knoten neu anordnen**mit der rechten Maustaste auf **Elvis Presley** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-212">Under **Reorder DOM Nodes**, right-click **Elvis Presley** and select **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3cf3a-213">Dies ist das letzte Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-213">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="3cf3a-214">Ziehen Sie den Mauszeiger in der DOM-Struktur `<li>Elvis Presley</li>` an den Anfang der Liste.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-214">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Ziehen des Knotens an den Anfang der Liste" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="3cf3a-216">Ziehen des Knotens an den Anfang der Liste</span><span class="sxs-lookup"><span data-stu-id="3cf3a-216">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="3cf3a-217">Zustand erzwingen</span><span class="sxs-lookup"><span data-stu-id="3cf3a-217">Force state</span></span>   

<span data-ttu-id="3cf3a-218">Sie können die Knoten zwingen, in Zuständen wie,,, und zu bleiben `:active` `:hover` `:focus` `:visited` `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-218">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="3cf3a-219">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-219">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-220">Zeigen Sie unter **Kraftzustand**auf **den Lord of the Flies**.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-220">Under **Force state**, hover over **The Lord of the Flies**.</span></span>  <span data-ttu-id="3cf3a-221">Die Hintergrundfarbe wird Orange.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-221">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="3cf3a-222">Klicken Sie mit der rechten Maustaste auf **den Lord of the Flies** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-222">Right-click **The Lord of the Flies** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3cf3a-223">Klicken Sie mit der rechten Maustaste `<li class="demo--hover">The Lord of the Flies</li>` , und wählen Sie **Zustand erzwingen**  >  **: hover**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-223">Right-click `<li class="demo--hover">The Lord of the Flies</li>` and select **Force State** > **:hover**.</span></span>  <span data-ttu-id="3cf3a-224">Siehe [Anhang: fehlende Optionen](#appendix-missing-options) , wenn diese Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-224">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  <span data-ttu-id="3cf3a-225">Die Hintergrundfarbe bleibt Orange, auch wenn Sie nicht tatsächlich über den Knoten zeigen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-225">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <span data-ttu-id="3cf3a-226">Ausblenden eines Knotens</span><span class="sxs-lookup"><span data-stu-id="3cf3a-226">Hide a node</span></span>   

<span data-ttu-id="3cf3a-227">Drücken Sie `H` , um einen Knoten auszublenden.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-227">Press `H` to hide a node.</span></span>  

1.  <span data-ttu-id="3cf3a-228">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-228">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-229">Klicken Sie unter **Knoten ausblenden**mit der rechten Maustaste auf **das Sternchen mein Ziel** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-229">Under **Hide a node**, right-click **The Stars My Destination** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3cf3a-230">Drücken Sie die Eingabe `H` Taste.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-230">Press the `H` key.</span></span>  <span data-ttu-id="3cf3a-231">Der Knoten ist ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-231">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Wie der Knoten in der DOM-Struktur aussieht, nachdem er ausgeblendet wurde" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="3cf3a-233">Wie der Knoten in der DOM-Struktur aussieht, nachdem er ausgeblendet wurde</span><span class="sxs-lookup"><span data-stu-id="3cf3a-233">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="3cf3a-234">Drücken Sie die `H` Taste erneut.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-234">Press the `H` key again.</span></span>  <span data-ttu-id="3cf3a-235">Der Knoten wird wieder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-235">The node is shown again.</span></span>  

### <span data-ttu-id="3cf3a-236">Löschen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="3cf3a-236">Delete a node</span></span>   

<span data-ttu-id="3cf3a-237">Drücken Sie `Delete` , um einen Knoten zu löschen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-237">Press `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="3cf3a-238">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-238">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-239">Klicken Sie unter **Knoten löschen mit der**rechten Maustaste auf **Foundation** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-239">Under **Delete a Node**, right-click **Foundation** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3cf3a-240">Drücken Sie die Eingabe `Delete` Taste.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-240">Press the `Delete` key.</span></span>  <span data-ttu-id="3cf3a-241">Der Knoten wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-241">The node is deleted.</span></span>  
    1.  <span data-ttu-id="3cf3a-242">Drücken Sie `Control` + `Z` \ (Windows \) oder `Command` + `Z` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-242">Press `Control`+`Z` \(Windows\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="3cf3a-243">Die letzte Aktion wird rückgängig gemacht, und der Knoten wird wieder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-243">The last action is undone and the node reappears.</span></span>  

## <span data-ttu-id="3cf3a-244">Access-Knoten in der Konsole</span><span class="sxs-lookup"><span data-stu-id="3cf3a-244">Access nodes in the Console</span></span>   

<span data-ttu-id="3cf3a-245">DevTools bietet einige Tastenkombinationen für den Zugriff auf DOM-Knoten über die Konsole oder das Abrufen von JavaScript-verweisen auf jede einzelne.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-245">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <span data-ttu-id="3cf3a-246">Verweisen auf den aktuell ausgewählten Knoten mit $0</span><span class="sxs-lookup"><span data-stu-id="3cf3a-246">Reference the currently-selected node with $0</span></span>   

<span data-ttu-id="3cf3a-247">Wenn Sie einen Knoten überprüfen, `== $0` bedeutet der Text neben dem Knoten, dass Sie auf diesen Knoten in der Konsole mit der Variablen verweisen können `$0` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-247">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="3cf3a-248">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-248">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-249">Klicken Sie unter **Verweis auf den aktuell ausgewählten Knoten mit $0 mit**der rechten Maustaste auf **die linke Hand der Dunkelheit** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-249">Under **Reference the currently-selected node with $0**, right-click **The Left Hand of Darkness** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3cf3a-250">Drücken Sie die Eingabe `Escape` Taste, um den Konsolen Einzug zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-250">Press the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="3cf3a-251">Geben `$0` Sie ein, und drücken Sie die Eingabe `Enter` Taste.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-251">Type `$0` and press the `Enter` key.</span></span>  <span data-ttu-id="3cf3a-252">Das Ergebnis des Ausdrucks zeigt, dass `$0` ausgewertet wird `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-252">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Das Ergebnis des ersten $0-Ausdrucks in der Konsole" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="3cf3a-254">Das Ergebnis des ersten `$0` Ausdrucks in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="3cf3a-254">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="3cf3a-255">Zeigen Sie mit der Maus auf das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-255">Hover over the result.</span></span>  <span data-ttu-id="3cf3a-256">Der Knoten ist im Viewport hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-256">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="3cf3a-257">Klicken Sie `<li>Dune</li>` in die DOM-Struktur, geben Sie `$0` die Konsole erneut ein, und drücken Sie dann `Enter` erneut.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-257">Click `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then press `Enter` again.</span></span>  <span data-ttu-id="3cf3a-258">Wird nun `$0` ausgewertet `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-258">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Das Ergebnis des zweiten $0-Ausdrucks in der Konsole" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="3cf3a-260">Das Ergebnis des zweiten `$0` Ausdrucks in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="3cf3a-260">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="3cf3a-261">Speichern als globale Variable</span><span class="sxs-lookup"><span data-stu-id="3cf3a-261">Store as global variable</span></span>   

<span data-ttu-id="3cf3a-262">Wenn Sie viele Male wieder auf einen Knoten verweisen müssen, speichern Sie ihn als globale Variable.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-262">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="3cf3a-263">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-263">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-264">Klicken Sie unter **als globale Variable speichern**mit der rechten Maustaste auf **den großen Ruhezustand** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-264">Under **Store as global variable**, right-click **The Big Sleep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3cf3a-265">Klicken Sie `<li>The Big Sleep</li>` mit der rechten Maustaste in die DOM-Struktur, und wählen Sie **als globale Variable speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-265">Right-click `<li>The Big Sleep</li>` in the DOM Tree and select **Store as global variable**.</span></span>  <span data-ttu-id="3cf3a-266">Siehe [Anhang: fehlende Optionen](#appendix-missing-options) , wenn diese Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-266">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  
    1.  <span data-ttu-id="3cf3a-267">Geben `temp1` Sie die Konsole ein, und drücken Sie dann `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-267">Type `temp1` in the Console and then press `Enter`.</span></span>  <span data-ttu-id="3cf3a-268">Das Ergebnis des Ausdrucks zeigt, dass die Variable zum Knoten ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-268">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Das Ergebnis des temp1-Ausdrucks" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="3cf3a-270">Das Ergebnis des `temp1` Ausdrucks</span><span class="sxs-lookup"><span data-stu-id="3cf3a-270">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="3cf3a-271">Kopieren des js-Pfads</span><span class="sxs-lookup"><span data-stu-id="3cf3a-271">Copy JS path</span></span>   

<span data-ttu-id="3cf3a-272">Kopieren Sie den JavaScript-Pfad zu einem Knoten, wenn Sie in einem automatisierten Test darauf verweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-272">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="3cf3a-273">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-273">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-274">Klicken Sie unter **js-Pfad kopieren**mit der rechten Maustaste auf **das Brothers-Karamazov** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-274">Under **Copy JS path**, right-click **The Brothers Karamazov** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3cf3a-275">Klicken Sie `<li>The Brothers Karamazov</li>` mit der rechten Maustaste in die DOM **Copy**-Struktur, und wählen Sie Copy  >  **js Path**kopieren aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-275">Right-click `<li>The Brothers Karamazov</li>` in the DOM Tree and select **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="3cf3a-276">Ein `document.querySelector()` Ausdruck, der in den Knoten aufgelöst wird, wurde in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-276">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="3cf3a-277">Drücken Sie `Control` + `V` \ (Windows \) oder `Command` + `V` \ (macOS \), um den Ausdruck in die Konsole einzufügen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-277">Press `Control`+`V` \(Windows\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="3cf3a-278">Drücken Sie `Enter` , um den Ausdruck auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-278">Press `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Das Ergebnis des Ausdrucks "JS-Pfad kopieren"" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="3cf3a-280">Das Ergebnis des Ausdrucks " **js-Pfad kopieren** "</span><span class="sxs-lookup"><span data-stu-id="3cf3a-280">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <span data-ttu-id="3cf3a-281">Änderungen am Dom unterbrechen</span><span class="sxs-lookup"><span data-stu-id="3cf3a-281">Break on DOM changes</span></span>   

<span data-ttu-id="3cf3a-282">Mit devtools können Sie das JavaScript einer Seite anhalten, wenn das DOM vom JavaScript geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-282">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <span data-ttu-id="3cf3a-283">Unterbrechen von Attributänderungen</span><span class="sxs-lookup"><span data-stu-id="3cf3a-283">Break on attribute modifications</span></span>   

<span data-ttu-id="3cf3a-284">Verwenden Sie die Attribut Änderungs Haltepunkte, wenn Sie das JavaScript anhalten möchten, das dazu führt, dass das Attribut eines Knotens geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-284">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="3cf3a-285">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-285">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-286">Klicken Sie unter **Umbruch bei Attributänderungen mit der**rechten Maustaste auf **Sauerkraut** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-286">Under **Break on attribute modifications**, right-click **Sauerkraut** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3cf3a-287">Klicken Sie in der DOM-Struktur mit der rechten Maustaste, `<li id="target">Sauerkraut</li>` und wählen Sie **bei**  >  **Attributänderungen**aufheben aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-287">In the DOM Tree, right-click `<li id="target">Sauerkraut</li>` and select **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="3cf3a-288">Siehe [Anhang: fehlende Optionen](#appendix-missing-options) , wenn diese Option nicht angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-288">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Unterbrechen von Attributänderungen" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="3cf3a-290">Unterbrechen von Attributänderungen</span><span class="sxs-lookup"><span data-stu-id="3cf3a-290">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="3cf3a-291">Im nächsten Schritt werden Sie angewiesen, auf eine Schaltfläche zu klicken, mit der der Code der Seite angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-291">In the next step you are going to be instructed to click a button that pauses the code of the page.</span></span>  <span data-ttu-id="3cf3a-292">Nachdem die Seite angehalten wurde, können Sie die Seite nicht mehr scrollen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-292">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="3cf3a-293">Sie müssen auf **Skript fortsetzen** \ ( ![ Skript fortsetzen ][ImageResumeScriptIcon] \) klicken, um die Seite erneut scrollen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-293">You must click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Wo wird das Skript fortgesetzt?" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="3cf3a-295">Wo wird das Skript fortgesetzt?</span><span class="sxs-lookup"><span data-stu-id="3cf3a-295">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="3cf3a-296">Klicken Sie oben auf die Schaltfläche **Hintergrund einstellen** .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-296">Click the **Set Background** button above.</span></span>  <span data-ttu-id="3cf3a-297">Dadurch wird das `style` Attribut des Knotens auf festgelegt `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-297">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="3cf3a-298">DevTools hält die Seite an und hebt den Code hervor, der zum Ändern des Attributs geführt hat.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-298">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="3cf3a-299">Klicken Sie, wie bereits erwähnt, auf **Skript fortsetzen** \ ( ![ Fortsetzen des Skripts ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-299">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\), as mentioned earlier.</span></span>  
    
### <span data-ttu-id="3cf3a-300">Unterbrechung beim Entfernen von Knoten</span><span class="sxs-lookup"><span data-stu-id="3cf3a-300">Break on node removal</span></span>   

<span data-ttu-id="3cf3a-301">Wenn Sie anhalten möchten, wenn ein bestimmter Knoten entfernt wird, verwenden Sie Haltepunkte für die Knoten Entfernung.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-301">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="3cf3a-302">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-302">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-303">Klicken Sie unter **Umbruch beim Entfernen von Knoten mit der**rechten Maustaste auf **Neuromancer** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-303">Under **Break on Node Removal**, right-click **Neuromancer** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3cf3a-304">Klicken Sie in der DOM-Struktur mit der rechten Maustaste, `<li id="target">Neuromancer</li>` und wählen Sie **beim Entfernen von Knoten unterbrechen**aus  >  **Node Removal**.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-304">In the DOM Tree, right-click `<li id="target">Neuromancer</li>` and select **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="3cf3a-305">Siehe [Anhang: fehlende Optionen](#appendix-missing-options) , wenn diese Option nicht angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-305">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="3cf3a-306">Klicken Sie oben auf die Schaltfläche **Löschen** .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-306">Click the **Delete** button above.</span></span>  <span data-ttu-id="3cf3a-307">DevTools hält die Seite an und hebt den Code hervor, der dazu geführt hat, dass der Knoten entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-307">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="3cf3a-308">Klicken Sie auf **Skript fortsetzen** \ ( ![ Skript fortsetzen ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-308">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
### <span data-ttu-id="3cf3a-309">Unterbrechen von Änderungen an Teilstruktur</span><span class="sxs-lookup"><span data-stu-id="3cf3a-309">Break on subtree modifications</span></span>   

<span data-ttu-id="3cf3a-310">Nachdem Sie einen Haltepunkt für die Unterstruktur Änderung auf einem Knoten platziert haben, wird die Seite von devtools angehalten, wenn ein Nachfolger des Knotens hinzugefügt oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-310">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="3cf3a-311">[Öffnen Sie DOM-Beispiele](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-311">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="3cf3a-312">Klicken Sie unter **Umbruch bei Teilstruktur Änderungen**mit der rechten Maustaste auf **ein Feuer auf der Tiefe** , und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-312">Under **Break on Subtree Modifications**, right-click **A Fire Upon The Deep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="3cf3a-313">Klicken Sie in der DOM-Struktur mit der rechten Maustaste auf `<ul id="target">` den Knoten oben `<li>A Fire Upon the Deep</li>` , und wählen Sie **unter**Teil  >  **Strukturänderungen**aufheben aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-313">In the DOM Tree, right-click `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, and select **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="3cf3a-314">Siehe [Anhang: fehlende Optionen](#appendix-missing-options) , wenn diese Option nicht angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-314">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="3cf3a-315">Klicken Sie auf **Kind hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-315">Click **Add Child**.</span></span>  <span data-ttu-id="3cf3a-316">Der Code wird angehalten `<li>` , weil der Liste ein Knoten hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-316">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="3cf3a-317">Klicken Sie auf **Skript fortsetzen** \ ( ![ Skript fortsetzen ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3cf3a-317">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
## <span data-ttu-id="3cf3a-318">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="3cf3a-318">Next steps</span></span>   

<span data-ttu-id="3cf3a-319">, Die die meisten der Dom-bezogenen Features in devtools abdeckt.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-319">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="3cf3a-320">Sie können die restlichen Personen entdecken, indem Sie mit der rechten Maustaste auf Knoten in der DOM-Struktur klicken und mit den anderen Optionen experimentieren, die in diesem Lernprogramm nicht behandelt wurden.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-320">You are able to discover the rest of them by right-clicking nodes in the DOM Tree and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="3cf3a-321">Siehe auch [Tastenkombinationen im Element Panel][DevToolsShortcutsElements].</span><span class="sxs-lookup"><span data-stu-id="3cf3a-321">See also [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="3cf3a-322">Schauen Sie sich die [Microsoft Edge devtools-Startseite][MicrosoftEdgeDevTools] an, um alles mögliche zu entdecken, was Sie mit devtools tun können.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-322">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## <span data-ttu-id="3cf3a-323">Anhang: HTML im Vergleich zum Dom</span><span class="sxs-lookup"><span data-stu-id="3cf3a-323">Appendix: HTML versus the DOM</span></span>   

<span data-ttu-id="3cf3a-324">Im folgenden Abschnitt wird schnell der Unterschied zwischen HTML und dem Dom erläutert.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-324">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="3cf3a-325">Wenn Sie eine Seite mit einem Webbrowser anfordern, gibt der Server HTML wie den folgenden Codeausschnitt zurück.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-325">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

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
      <span data-ttu-id="3cf3a-326">Der Browser analysiert den HTML-Code und erstellt eine Struktur von Objekten wie der folgenden Liste.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-326">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
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

<span data-ttu-id="3cf3a-327">Diese Struktur von Objekten oder Knoten, die den Inhalt der Seite darstellen, wird als DOM bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-327">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="3cf3a-328">Im Moment sieht es genauso aus wie das HTML, aber angenommen, das Skript, auf das am Ende des HTML-Codes verwiesen wird, führt den folgenden Codeausschnitt aus.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-328">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="3cf3a-329">Dieser Code entfernt den `h1` Knoten und fügt `p` dem DOM einen weiteren Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-329">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="3cf3a-330">Das vollständige Dom zeigt nun die folgende Liste an.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-330">The complete DOM now displays the following list.</span></span>  
      
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

<span data-ttu-id="3cf3a-331">Der HTML-Code für die Seite ist jetzt anders als das DOM.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-331">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="3cf3a-332">Mit anderen Worten, HTML steht für den anfänglichen Seiteninhalt, und das DOM steht für den aktuellen Seiteninhalt.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-332">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="3cf3a-333">Wenn JavaScript-Knoten hinzugefügt, entfernt oder bearbeitet werden, wird das DOM anders als das HTML-Code.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-333">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="3cf3a-334">Weitere Informationen finden Sie unter [Einführung in das DOM][MDNIntroductionToDOM] .</span><span class="sxs-lookup"><span data-stu-id="3cf3a-334">See [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view   

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and select **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    > ##### Figure 19  
    > Scroll into view  
    > :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
   Scroll into view  
:::image-end:::  
    -->  

## <span data-ttu-id="3cf3a-335">Anhang: fehlende Optionen</span><span class="sxs-lookup"><span data-stu-id="3cf3a-335">Appendix: Missing options</span></span>   

<span data-ttu-id="3cf3a-336">Viele der Anweisungen in diesem Lernprogramm weisen Sie an, mit der rechten Maustaste auf einen Knoten in der DOM-Struktur zu klicken und dann im Kontextmenü, das eingeblendet wird, eine Option auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-336">Many of the instructions in this tutorial instruct you to right-click a node in the DOM Tree and then select an option from the context menu that pops up.</span></span>  <span data-ttu-id="3cf3a-337">Wenn die angegebene Option im Kontextmenü nicht angezeigt wird, versuchen Sie, mit der rechten Maustaste auf den Knotentext zu klicken.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-337">If you do not see the specified option in the context menu, try right-clicking away from the node text.</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Wo klicken, wenn nicht alle Optionen angezeigt werden" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="3cf3a-339">Wo klicken, wenn nicht alle Optionen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="3cf3a-339">Where to click if you are not seeing all the options</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge \ (Chrom \) Developer Tools | Microsoft docs"  
[DevToolsCssGetStarted]: ../css/index.md "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  
[DevToolsShortcutsElements]: ../shortcuts.md#elements-panel-keyboard-shortcuts "Tastenkombinationen im Element Panel – Tastenkombinationen für Microsoft Edge devtools | Microsoft docs"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chrom) devtools Dom-Beispiel | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in das DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="3cf3a-345">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-345">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3cf3a-346">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/dom/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="3cf3a-346">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="3cf3a-348">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3cf3a-348">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
title: CSS-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 4f0370b83d8c939476a1ed378dbdf750101c9527
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843967"
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







# <span data-ttu-id="5db20-103">CSS-Referenz</span><span class="sxs-lookup"><span data-stu-id="5db20-103">CSS Reference</span></span>   



<span data-ttu-id="5db20-104">Entdecken Sie neue Workflows in dieser umfassenden Referenz zu den Microsoft Edge devtools-Features, die sich auf das Anzeigen und Ändern von CSS beziehen.</span><span class="sxs-lookup"><span data-stu-id="5db20-104">Discover new workflows in this comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="5db20-105">Informationen zu den Grundlagen finden Sie unter [Erste Schritte beim Anzeigen und Ändern von CSS][DevToolsCSSGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="5db20-105">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="5db20-106">Auswählen eines Elements</span><span class="sxs-lookup"><span data-stu-id="5db20-106">Select an element</span></span>   

<span data-ttu-id="5db20-107">Mit dem Element Panel von devtools können **Sie das CSS** eines Elements gleichzeitig anzeigen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="5db20-107">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="5db20-108">Das ausgewählte Element ist in der **DOM-Struktur**hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="5db20-108">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="5db20-109">Die Formatvorlagen des Elements werden im Bereich **Formatvorlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5db20-109">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="5db20-110">Weitere Informationen finden Sie unter [Anzeigen des CSS für ein Element][DevToolsCSSGetStartedTutorial] für ein Lernprogramm.</span><span class="sxs-lookup"><span data-stu-id="5db20-110">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="5db20-111">In [Abbildung 1](#figure-1)ist das `h1` Element, das in der **DOM-Struktur** hervorgehoben wird, das ausgewählte Element.</span><span class="sxs-lookup"><span data-stu-id="5db20-111">In [Figure 1](#figure-1), the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="5db20-112">Auf der rechten Seite werden die Formatvorlagen des Elements im Bereich **Formatvorlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5db20-112">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="5db20-113">Auf der linken Seite ist das Element im Viewport hervorgehoben, allerdings nur, weil die Maus gerade in der DOM- **Struktur**darüber schwebt.</span><span class="sxs-lookup"><span data-stu-id="5db20-113">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

> ##### <span data-ttu-id="5db20-114">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="5db20-114">Figure 1</span></span>  
> <span data-ttu-id="5db20-115">Ein Beispiel für ein ausgewähltes Element</span><span class="sxs-lookup"><span data-stu-id="5db20-115">An example of a selected element</span></span>  
> ![Ein Beispiel für ein ausgewähltes Element][ImageSelectedElement]  

<span data-ttu-id="5db20-117">Es gibt viele Möglichkeiten zum Auswählen eines Elements:</span><span class="sxs-lookup"><span data-stu-id="5db20-117">There are many ways to select an element:</span></span>  

*   <span data-ttu-id="5db20-118">Klicken Sie im Viewport mit der rechten Maustaste auf das Element, und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="5db20-118">In your viewport, right-click the element and select **Inspect**.</span></span>  
*   <span data-ttu-id="5db20-119">Klicken Sie in devtools auf **Element auswählen** , ![ Wählen Sie ein Element aus, ][ImageSelectAnElementIcon] oder drücken Sie \ ( `Control` + `Shift` + `C` Windows \) oder `Command` + `Shift` + `C` \ (macOS \), und klicken Sie dann auf das Element im Viewport.</span><span class="sxs-lookup"><span data-stu-id="5db20-119">In DevTools, click **Select an element** ![Select an element][ImageSelectAnElementIcon] or press `Control`+`Shift`+`C` \(Windows\) or `Command`+`Shift`+`C` \(macOS\), and then click the element in the viewport.</span></span>  
*   <span data-ttu-id="5db20-120">Klicken Sie in devtools auf das Element in der **DOM-Struktur**.</span><span class="sxs-lookup"><span data-stu-id="5db20-120">In DevTools, click the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="5db20-121">Führen Sie in devtools eine Abfrage wie `document.querySelector('p')` in der **Konsole**aus, klicken Sie mit der rechten Maustaste auf das Ergebnis, und wählen Sie dann **im Dialogfeldelemente**anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="5db20-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, right-click the result, and then select **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="5db20-122">CSS anzeigen</span><span class="sxs-lookup"><span data-stu-id="5db20-122">View CSS</span></span>   

### <span data-ttu-id="5db20-123">Anzeigen des externen Stylesheets, in dem eine Regel definiert ist</span><span class="sxs-lookup"><span data-stu-id="5db20-123">View the external stylesheet where a rule is defined</span></span>   

<span data-ttu-id="5db20-124">Klicken Sie im Bereich **Formatvorlagen** auf den Link neben einer CSS-Regel, um das externe Stylesheet zu öffnen, das die Regel definiert.</span><span class="sxs-lookup"><span data-stu-id="5db20-124">In the **Styles** pane, click the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="5db20-125">Wenn das Stylesheet minimierte ist, lesen Sie [Erstellen einer minimierte-Datei][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="5db20-125">If the stylesheet is minified, see [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="5db20-126">Klicken Sie in [Abbildung 2](#figure-2) `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` auf die Zeile 2 von, in der `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` die `.content h1:first-of-type` CSS-Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="5db20-126">In [Figure 2](#figure-2), clicking `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` takes you to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

> ##### <span data-ttu-id="5db20-127">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="5db20-127">Figure 2</span></span>  
> <span data-ttu-id="5db20-128">Anzeigen des Stylesheets, in dem eine Regel definiert ist</span><span class="sxs-lookup"><span data-stu-id="5db20-128">Viewing the stylesheet where a rule is defined</span></span>  
> ![Anzeigen des Stylesheets, in dem eine Regel definiert ist][ImageViewRuleStylesheet]  

### <span data-ttu-id="5db20-130">Anzeigen nur des CSS, das tatsächlich auf ein Element angewendet wird</span><span class="sxs-lookup"><span data-stu-id="5db20-130">View only the CSS that is actually applied to an element</span></span>   

<span data-ttu-id="5db20-131">Auf der Registerkarte **Formatvorlagen** werden alle Regeln angezeigt, die für ein Element gelten, einschließlich Deklarationen, die überschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="5db20-131">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="5db20-132">Wenn Sie nicht an überschriebenen Deklarationen interessiert sind, verwenden Sie die Registerkarte **berechnet** , um nur das CSS anzuzeigen, das tatsächlich auf ein Element angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5db20-132">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="5db20-133">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5db20-133">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5db20-134">Wechseln Sie im **Element** Fenster zur Registerkarte **berechnet** .</span><span class="sxs-lookup"><span data-stu-id="5db20-134">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="5db20-135">In einem breiten devtools-Fenster ist die Registerkarte **berechnet** nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5db20-135">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="5db20-136">Der Inhalt der Registerkarte **berechnet** wird auf der Registerkarte **Formatvorlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5db20-136">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="5db20-137">Geerbte Eigenschaften sind nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="5db20-137">Inherited properties are opaque.</span></span>  <span data-ttu-id="5db20-138">Aktivieren Sie das Kontrollkästchen **Alle anzeigen** , um alle geerbten Werte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5db20-138">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="5db20-139">In [Abbildung 3](#figure-3)werden auf der Registerkarte **berechnet** die CSS-Eigenschaften angezeigt, die auf das aktuell ausgewählte Element angewendet werden `h1` .</span><span class="sxs-lookup"><span data-stu-id="5db20-139">In [Figure 3](#figure-3), the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

> ##### <span data-ttu-id="5db20-140">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="5db20-140">Figure 3</span></span>  
> <span data-ttu-id="5db20-141">Die Registerkarte " **berechnet** "</span><span class="sxs-lookup"><span data-stu-id="5db20-141">The **Computed** tab</span></span>  
> ![Die Registerkarte "berechnet"][ImageComputedTab]  

### <span data-ttu-id="5db20-143">Anzeigen von CSS-Eigenschaften in alphabetischer Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="5db20-143">View CSS properties in alphabetical order</span></span>   

<span data-ttu-id="5db20-144">Verwenden Sie die Registerkarte **berechnet** .  Informationen finden Sie unter [Anzeigen der CSS, die tatsächlich auf ein Element angewendet](#view-only-the-css-that-is-actually-applied-to-an-element)werden.</span><span class="sxs-lookup"><span data-stu-id="5db20-144">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="5db20-145">Anzeigen von geerbten CSS-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5db20-145">View inherited CSS properties</span></span>   

<span data-ttu-id="5db20-146">Aktivieren Sie das Kontrollkästchen **Alle anzeigen** auf der Registerkarte **berechnet** .  Informationen finden Sie unter [Anzeigen der CSS, die tatsächlich auf ein Element angewendet](#view-only-the-css-that-is-actually-applied-to-an-element)werden.</span><span class="sxs-lookup"><span data-stu-id="5db20-146">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="5db20-147">Anzeigen des Box-Modells für ein Element</span><span class="sxs-lookup"><span data-stu-id="5db20-147">View the box model for an element</span></span>   

<span data-ttu-id="5db20-148">Wenn Sie [das Feld Modell][MDNBoxModel] eines Elements anzeigen möchten, wechseln Sie zur Registerkarte **Formatvorlagen** .  Wenn Ihr devtools-Fenster schmal ist, befindet sich das **Feld Modell** Diagramm unten auf der Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="5db20-148">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="5db20-149">Um einen Wert zu ändern, doppelklicken Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="5db20-149">To change a value, double-click on it.</span></span>  

> [!NOTE]
> <span data-ttu-id="5db20-150">In [Abbildung 4](#figure-4)zeigt das **Diagramm auf** der Registerkarte **Formatvorlagen** das Feld Modell für das aktuell ausgewählte `h1` Element.</span><span class="sxs-lookup"><span data-stu-id="5db20-150">In [Figure 4](#figure-4), the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

> ##### <span data-ttu-id="5db20-151">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="5db20-151">Figure 4</span></span>  
> <span data-ttu-id="5db20-152">Das Diagramm des **Feld Modells**</span><span class="sxs-lookup"><span data-stu-id="5db20-152">The **Box Model** diagram</span></span>  
> ![Das Diagramm des Feld Modells][ImageBoxModel]  

### <span data-ttu-id="5db20-154">Suchen und Filtern des CSS eines Elements</span><span class="sxs-lookup"><span data-stu-id="5db20-154">Search and filter the CSS of an element</span></span>   

<span data-ttu-id="5db20-155">Verwenden Sie das Textfeld " **Filter** " auf den Registerkarten " **Formatvorlagen** " und " **berechnet** ", um nach bestimmten CSS-Eigenschaften oder-Werten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="5db20-155">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="5db20-156">Wenn Sie auch geerbte Eigenschaften auf der Registerkarte **berechnet** durchsuchen möchten, aktivieren Sie das Kontrollkästchen **Alle anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="5db20-156">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="5db20-157">In [Abbildung 5](#figure-5)wird die Registerkarte **Formatvorlagen** so gefiltert, dass nur Regeln angezeigt werden, die die Suchabfrage enthalten `color` .</span><span class="sxs-lookup"><span data-stu-id="5db20-157">In [Figure 5](#figure-5), the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

> ##### <span data-ttu-id="5db20-158">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="5db20-158">Figure 5</span></span>  
> <span data-ttu-id="5db20-159">Filtern der Registerkarte " **Formatvorlagen** "</span><span class="sxs-lookup"><span data-stu-id="5db20-159">Filtering the **Styles** tab</span></span>  
> ![Filtern der Registerkarte "Formatvorlagen"][ImageStylesFilter]  

> [!NOTE]
> <span data-ttu-id="5db20-161">In [Abbildung 6](#figure-6)wird die Registerkarte **berechnet** so gefiltert, dass nur Deklarationen angezeigt werden, die die Suchabfrage enthalten `100%` .</span><span class="sxs-lookup"><span data-stu-id="5db20-161">In [Figure 6](#figure-6), the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

> ##### <span data-ttu-id="5db20-162">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="5db20-162">Figure 6</span></span>  
> <span data-ttu-id="5db20-163">Filtern der **berechneten** Registerkarte</span><span class="sxs-lookup"><span data-stu-id="5db20-163">Filtering the **Computed** tab</span></span>  
> ![Filtern der berechneten Registerkarte][ImageComputerFilter]  

### <span data-ttu-id="5db20-165">Umschalten einer Pseudoklasse</span><span class="sxs-lookup"><span data-stu-id="5db20-165">Toggle a pseudo-class</span></span>   

<span data-ttu-id="5db20-166">So wechseln Sie eine Pseudoklasse wie `:active` , `:focus` , `:hover` oder `:visited` :</span><span class="sxs-lookup"><span data-stu-id="5db20-166">To toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`:</span></span>  

1.  <span data-ttu-id="5db20-167">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5db20-167">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5db20-168">Wechseln Sie im **Element** Fenster zur Registerkarte **Formatvorlagen** .</span><span class="sxs-lookup"><span data-stu-id="5db20-168">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="5db20-169">Klicken Sie auf **: Hov**.</span><span class="sxs-lookup"><span data-stu-id="5db20-169">Click **:hov**.</span></span>  
1.  <span data-ttu-id="5db20-170">Überprüfen Sie die Pseudoklasse, die Sie aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5db20-170">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="5db20-171">Wechseln Sie in [Abbildung 7](#figure-7)zur `:hover` Pseudoklasse.</span><span class="sxs-lookup"><span data-stu-id="5db20-171">In [Figure 7](#figure-7), toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="5db20-172">Überprüfen Sie im Viewport, ob die `background-color: cornflowerblue` Deklaration auf das Element angewendet wird, obwohl das Element nicht tatsächlich über den Zeiger bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="5db20-172">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

> ##### <span data-ttu-id="5db20-173">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="5db20-173">Figure 7</span></span>  
> <span data-ttu-id="5db20-174">Umschalten der `:hover` Pseudoklasse</span><span class="sxs-lookup"><span data-stu-id="5db20-174">Toggling the `:hover` pseudo-class</span></span>  
> ![Umschalten der: hover-Pseudoklasse][ImagePseudoClass]  

<span data-ttu-id="5db20-176">Weitere Informationen finden Sie unter [Hinzufügen eines PseudoState zu einer Klasse][DevToolsCSSGetStartedAddPseudoState] für ein interaktives Lernprogramm.</span><span class="sxs-lookup"><span data-stu-id="5db20-176">See [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState] for an interactive tutorial.</span></span> 

### <span data-ttu-id="5db20-177">Anzeigen einer Seite im Druckmodus</span><span class="sxs-lookup"><span data-stu-id="5db20-177">View a page in print mode</span></span>   

<span data-ttu-id="5db20-178">So zeigen Sie eine Seite im Druckmodus an:</span><span class="sxs-lookup"><span data-stu-id="5db20-178">To view a page in print mode:</span></span>  
1.  <span data-ttu-id="5db20-179">[Öffnen des Befehlsmenüs][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="5db20-179">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="5db20-180">Beginnen `Rendering` Sie mit der Eingabe, und wählen Sie aus `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="5db20-180">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="5db20-181">Wählen Sie für die Dropdownliste **CSS-Medien emulieren** die Option **Drucken**aus.</span><span class="sxs-lookup"><span data-stu-id="5db20-181">For the **Emulate CSS Media** dropdown, select **print**.</span></span>  

### <span data-ttu-id="5db20-182">Anzeigen der verwendeten und nicht verwendeten CSS mit der Registerkarte "Coverage"</span><span class="sxs-lookup"><span data-stu-id="5db20-182">View used and unused CSS with the Coverage tab</span></span>   

<span data-ttu-id="5db20-183">Auf der Registerkarte Coverage wird angezeigt, welche CSS-Seiten tatsächlich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5db20-183">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="5db20-184">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), während sich devtools im Fokus befindet, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5db20-184">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to open the Command Menu.</span></span>  
1.  <span data-ttu-id="5db20-185">Beginnen `coverage` Sie mit der Eingabe, und wählen Sie **Berichterstattung anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="5db20-185">Start typing `coverage` and select **Show Coverage**.</span></span>  <span data-ttu-id="5db20-186">Die Registerkarte Coverage wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5db20-186">The Coverage tab appears.</span></span>  
    
    > ##### <span data-ttu-id="5db20-187">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="5db20-187">Figure 8</span></span>  
    > <span data-ttu-id="5db20-188">Öffnen der Registerkarte "Abdeckung" über das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="5db20-188">Opening the Coverage tab from the Command Menu</span></span>  
    > ![Öffnen der Registerkarte "Abdeckung" über das Befehlsmenü][ImageCommandMenu]  
    
    > ##### <span data-ttu-id="5db20-190">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="5db20-190">Figure 9</span></span>  
    > <span data-ttu-id="5db20-191">Die Registerkarte "Coverage"</span><span class="sxs-lookup"><span data-stu-id="5db20-191">The Coverage tab</span></span>  
    > ![Die Registerkarte "Coverage"][ImageCoverageEmpty]  
    
1.  <span data-ttu-id="5db20-193">Klicken Sie auf **Instrumentations Abdeckung starten, und aktualisieren Sie die Abdeckung für die Seiten** ![ Anfang Instrumentation, und aktualisieren Sie die Seite ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="5db20-193">Click **Start instrumenting coverage and refresh the page** ![Start instrumenting coverage and refresh the page][ImageRefreshIcon].</span></span>  <span data-ttu-id="5db20-194">Die Seite wird aktualisiert, und die Registerkarte Coverage bietet eine Übersicht darüber, wie viel CSS \ (und JavaScript \) aus jeder Datei, die der Browser lädt, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5db20-194">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="5db20-195">Grün steht für verwendetes CSS.</span><span class="sxs-lookup"><span data-stu-id="5db20-195">Green represents used CSS.</span></span>  <span data-ttu-id="5db20-196">Rot steht für nicht verwendetes CSS.</span><span class="sxs-lookup"><span data-stu-id="5db20-196">Red represents unused CSS.</span></span>  
    
    > ##### <span data-ttu-id="5db20-197">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="5db20-197">Figure 10</span></span>  
    > <span data-ttu-id="5db20-198">Eine Übersicht darüber, wie viel CSS (und JavaScript) verwendet und nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="5db20-198">An overview of how much CSS (and JavaScript) is used and unused</span></span>  
    > ![Eine Übersicht darüber, wie viel CSS (und JavaScript) verwendet und nicht verwendet wird][ImageCoverageOverview]  

1.  <span data-ttu-id="5db20-200">Klicken Sie auf eine CSS-Datei, um eine Zeile für Zeile zu sehen, welche CSS-Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5db20-200">Click a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5db20-201">In [Abbildung 11](#figure-11)werden die Zeilen 145 bis 147 und 149 bis 151 nicht `b66bc881.site-ltr.css` verwendet, während Zeilen 163 bis 166 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5db20-201">In [Figure 11](#figure-11), lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    > ##### <span data-ttu-id="5db20-202">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="5db20-202">Figure 11</span></span>  
    > <span data-ttu-id="5db20-203">Eine Zeile-für-Zeile-Aufteilung der verwendeten und nicht verwendeten CSS</span><span class="sxs-lookup"><span data-stu-id="5db20-203">A line-by-line breakdown of used and unused CSS</span></span>  
    > ![Eine Zeile-für-Zeile-Aufteilung der verwendeten und nicht verwendeten CSS][ImageCoverageDetail]  
    
### <span data-ttu-id="5db20-205">Erzwingen des Druckvorschau Modus</span><span class="sxs-lookup"><span data-stu-id="5db20-205">Force print preview mode</span></span>   

<span data-ttu-id="5db20-206">Siehe [Erzwingen von devtools in den Druckvorschau Modus][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="5db20-206">See [Force DevTools Into Print Preview Mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="5db20-207">CSS ändern</span><span class="sxs-lookup"><span data-stu-id="5db20-207">Change CSS</span></span>   

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="5db20-208">Hinzufügen einer CSS-Deklaration zu einem Element</span><span class="sxs-lookup"><span data-stu-id="5db20-208">Add a CSS declaration to an element</span></span>   

<span data-ttu-id="5db20-209">Da die Reihenfolge der Deklarationen beeinflusst, wie ein Element formatiert wird, können Sie Deklarationen auf unterschiedliche Weise hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="5db20-209">Since the order of declarations affects how an element is styled, you may add declarations in different ways:</span></span>  

*   <span data-ttu-id="5db20-210">[Fügen Sie eine Inline Deklaration hinzu](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="5db20-210">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="5db20-211">Entspricht dem Hinzufügen eines `style` Attributs zum HTML-Code eines Elements.</span><span class="sxs-lookup"><span data-stu-id="5db20-211">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="5db20-212">[Hinzufügen einer Deklaration zu einer Formatvorlagenregel](#add-a-declaration-to-a-style-rule)</span><span class="sxs-lookup"><span data-stu-id="5db20-212">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="5db20-213">Welchen Workflow sollten Sie verwenden?</span><span class="sxs-lookup"><span data-stu-id="5db20-213">What workflow should you use?</span></span>** <span data-ttu-id="5db20-214">In den meisten Fällen möchten Sie wahrscheinlich den Inline Deklarations Workflow verwenden.</span><span class="sxs-lookup"><span data-stu-id="5db20-214">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="5db20-215">Inline Deklarationen haben eine höhere Spezifität als externe, sodass der Inline-Workflow sicherstellt, dass die Änderungen in dem Element wie erwartet wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="5db20-215">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in the element as you would expect.</span></span>  <span data-ttu-id="5db20-216">Weitere Informationen zur Spezifität finden Sie unter [Selektor-Typen][MDNSelectorTypes] .</span><span class="sxs-lookup"><span data-stu-id="5db20-216">See [Selector Types][MDNSelectorTypes] for more on specificity.</span></span>  

<span data-ttu-id="5db20-217">Wenn Sie alle Formatvorlagen des Elements Debuggen und insbesondere testen möchten, was geschieht, wenn eine Deklaration an verschiedenen Stellen definiert ist, verwenden Sie den anderen Workflow.</span><span class="sxs-lookup"><span data-stu-id="5db20-217">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="5db20-218">Hinzufügen einer Inline Deklaration</span><span class="sxs-lookup"><span data-stu-id="5db20-218">Add an inline declaration</span></span>   

<span data-ttu-id="5db20-219">So fügen Sie eine Inline Deklaration hinzu:</span><span class="sxs-lookup"><span data-stu-id="5db20-219">To add an inline declaration:</span></span>  

1.  <span data-ttu-id="5db20-220">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5db20-220">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5db20-221">Klicken Sie im Bereich " **Formatvorlagen** " zwischen den Klammern des Abschnitts " **Element. Format** ".</span><span class="sxs-lookup"><span data-stu-id="5db20-221">In the **Styles** pane, click between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="5db20-222">Der Cursor konzentriert sich, sodass Sie Text eingeben können.</span><span class="sxs-lookup"><span data-stu-id="5db20-222">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="5db20-223">Geben Sie einen Eigenschaftsnamen ein, und drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5db20-223">Enter a property name and press `Enter`.</span></span>  
1.  <span data-ttu-id="5db20-224">Geben Sie einen gültigen Wert für diese Eigenschaft ein, und drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5db20-224">Enter a valid value for that property and press `Enter`.</span></span>  <span data-ttu-id="5db20-225">Überprüfen Sie in der **DOM-Struktur**, ob `style` dem Element ein Attribut hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="5db20-225">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="5db20-226">In [Abbildung 12](#figure-12)wurden die `margin-top` `background-color` Eigenschaften und auf das ausgewählte Element angewendet.</span><span class="sxs-lookup"><span data-stu-id="5db20-226">In [Figure 12](#figure-12), the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="5db20-227">Überprüfen Sie in der **DOM-Struktur** , ob die Deklarationen im `style` Attribut für ein Element widergespiegelt werden.</span><span class="sxs-lookup"><span data-stu-id="5db20-227">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

> ##### <span data-ttu-id="5db20-228">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="5db20-228">Figure 12</span></span>  
> <span data-ttu-id="5db20-229">Hinzufügen von Inline Deklarationen</span><span class="sxs-lookup"><span data-stu-id="5db20-229">Adding inline declarations</span></span>  
> ![Hinzufügen von Inline Deklarationen][ImageInlineDeclarations]  

#### <span data-ttu-id="5db20-231">Hinzufügen einer Deklaration zu einer Stilregel</span><span class="sxs-lookup"><span data-stu-id="5db20-231">Add a declaration to a style rule</span></span>   

<span data-ttu-id="5db20-232">So fügen Sie einer vorhandenen Stilregel eine Deklaration hinzu:</span><span class="sxs-lookup"><span data-stu-id="5db20-232">To add a declaration to an existing style rule:</span></span>  

1.  <span data-ttu-id="5db20-233">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5db20-233">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5db20-234">Klicken Sie im Bereich **Formatvorlagen** auf die eckigen Klammern der Stilregel, der Sie die Deklaration hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="5db20-234">In the **Styles** pane, click between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="5db20-235">Der Cursor konzentriert sich, sodass Sie Text eingeben können.</span><span class="sxs-lookup"><span data-stu-id="5db20-235">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="5db20-236">Geben Sie einen Eigenschaftsnamen ein, und drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5db20-236">Enter a property name and press `Enter`.</span></span>  
1.  <span data-ttu-id="5db20-237">Geben Sie einen gültigen Wert für diese Eigenschaft ein, und drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5db20-237">Enter a valid value for that property and press `Enter`.</span></span>  

> ##### <span data-ttu-id="5db20-238">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="5db20-238">Figure 13</span></span>  
> <span data-ttu-id="5db20-239">Hinzufügen der `border-bottom-style:groove` Deklaration zu einer Stilregel</span><span class="sxs-lookup"><span data-stu-id="5db20-239">Adding the `border-bottom-style:groove` declaration to a style rule</span></span>  
> ![Hinzufügen einer Deklaration zu einer Formatvorlagenregel][ImageAddDeclarationExistingRule]  

### <span data-ttu-id="5db20-241">Ändern des Namens oder Werts einer Deklaration</span><span class="sxs-lookup"><span data-stu-id="5db20-241">Change a declaration name or value</span></span>   

<span data-ttu-id="5db20-242">Doppelklicken Sie auf den Namen oder Wert einer Deklaration, um Sie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5db20-242">Double-click the name or value of a declaration to change it.</span></span>  <span data-ttu-id="5db20-243">Informationen dazu finden Sie unter [Ändern von Deklarations Werten mit Tastenkombinationen](#change-declaration-values-with-keyboard-shortcuts) für Tastenkombinationen, um einen Wert schnell zu erhöhen oder zu verringern `0.1` `1` `10` `100` .</span><span class="sxs-lookup"><span data-stu-id="5db20-243">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

> ##### <span data-ttu-id="5db20-244">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="5db20-244">Figure 14</span></span>  
> <span data-ttu-id="5db20-245">Ändern des Werts der</span><span class="sxs-lookup"><span data-stu-id="5db20-245">Changing the value of the</span></span> `border-bottom-style`  
> ![Ändern des Werts einer Deklaration][ImageAddDeclarationExistingRule2]  

### <span data-ttu-id="5db20-247">Ändern von Deklarations Werten mit Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="5db20-247">Change declaration values with keyboard shortcuts</span></span>   

<span data-ttu-id="5db20-248">Wenn Sie den Wert einer Deklaration bearbeiten, können Sie die folgenden Tastenkombinationen verwenden, um den Wert um einen festen Betrag zu erhöhen:</span><span class="sxs-lookup"><span data-stu-id="5db20-248">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a fixed amount:</span></span>  

*   <span data-ttu-id="5db20-249">Drücken Sie `Alt` + `Up` \ (Windows \) oder `Option` + `Up` \ (macOS \), um den Wert zu erhöhen `0.1` .</span><span class="sxs-lookup"><span data-stu-id="5db20-249">Press `Alt`+`Up` \(Windows\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="5db20-250">Drücken Sie, `Up` um den Wert nach `1` oder nach zu ändern, `0.1` Wenn der aktuelle Wert zwischen `-1` und ist `1` .</span><span class="sxs-lookup"><span data-stu-id="5db20-250">Press `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="5db20-251">Drücken Sie `Shift` + `Up` , um den Wert zu erhöhen `10` .</span><span class="sxs-lookup"><span data-stu-id="5db20-251">Press `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="5db20-252">Drücken Sie `Shift` + `Page Up` \ (Windows \) oder `Shift` + `Command` + `Up` \ (macOS \), um den Wert um zu erhöhen `100` .</span><span class="sxs-lookup"><span data-stu-id="5db20-252">Press `Shift`+`Page Up` \(Windows\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="5db20-253">Das Dekrementieren funktioniert auch.</span><span class="sxs-lookup"><span data-stu-id="5db20-253">Decrementing also works.</span></span>  <span data-ttu-id="5db20-254">Ersetzen Sie einfach alle `Up` oben genannten Instanzen durch `Down` .</span><span class="sxs-lookup"><span data-stu-id="5db20-254">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="5db20-255">Hinzufügen einer Klasse zu einem Element</span><span class="sxs-lookup"><span data-stu-id="5db20-255">Add a class to an element</span></span>   

<span data-ttu-id="5db20-256">So fügen Sie einem Element eine Klasse hinzu:</span><span class="sxs-lookup"><span data-stu-id="5db20-256">To add a class to an element:</span></span>  

1.  <span data-ttu-id="5db20-257">[Wählen Sie das Element](#select-an-element) in der **DOM-Struktur**aus.</span><span class="sxs-lookup"><span data-stu-id="5db20-257">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="5db20-258">Klicken Sie auf **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="5db20-258">Click **.cls**.</span></span>  
1.  <span data-ttu-id="5db20-259">Geben Sie den Namen der Klasse in das Textfeld **neue Klasse hinzufügen** ein.</span><span class="sxs-lookup"><span data-stu-id="5db20-259">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="5db20-260">Drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5db20-260">Press `Enter`.</span></span>  

> ##### <span data-ttu-id="5db20-261">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="5db20-261">Figure 15</span></span>  
> <span data-ttu-id="5db20-262">Der Bereich " **Element Klassen** "</span><span class="sxs-lookup"><span data-stu-id="5db20-262">The **Element Classes** pane</span></span>  
> ![Der Bereich "Element Klassen"][ImageElementClasses]  

### <span data-ttu-id="5db20-264">Umschalten einer Klasse</span><span class="sxs-lookup"><span data-stu-id="5db20-264">Toggle a class</span></span>   

<span data-ttu-id="5db20-265">So aktivieren oder deaktivieren Sie eine Klasse für ein Element:</span><span class="sxs-lookup"><span data-stu-id="5db20-265">To enable or disable a class on an element:</span></span>  

1.  <span data-ttu-id="5db20-266">[Wählen Sie das Element](#select-an-element) in der **DOM-Struktur**aus.</span><span class="sxs-lookup"><span data-stu-id="5db20-266">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="5db20-267">Öffnen Sie den Bereich **Element Klassen** .</span><span class="sxs-lookup"><span data-stu-id="5db20-267">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="5db20-268">Weitere Informationen finden Sie unter [Hinzufügen einer Klasse zu einem Element](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="5db20-268">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="5db20-269">Unter dem Textfeld " **neue Klasse hinzufügen** " befinden sich alle Klassen, die auf dieses Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5db20-269">Below the **Add New Class** text box are all of the classes that are being applied to this element.</span></span>  
1.  <span data-ttu-id="5db20-270">Aktivieren oder deaktivieren Sie das Kontrollkästchen neben der Klasse, die Sie aktivieren oder deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5db20-270">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="5db20-271">Hinzufügen einer Stilregel</span><span class="sxs-lookup"><span data-stu-id="5db20-271">Add a style rule</span></span>   

<span data-ttu-id="5db20-272">So fügen Sie eine neue Stilregel hinzu:</span><span class="sxs-lookup"><span data-stu-id="5db20-272">To add a new style rule:</span></span>  

1.  <span data-ttu-id="5db20-273">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5db20-273">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5db20-274">Klicken Sie auf **neue** Stilregel Regel ![ ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="5db20-274">Click **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon].</span></span>  <span data-ttu-id="5db20-275">DevTools fügt eine neue Regel unterhalb der **Element. Style** -Regel ein.</span><span class="sxs-lookup"><span data-stu-id="5db20-275">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="5db20-276">In [Abbildung 16](#figure-16)fügt devtools die Stilregel hinzu, `h1.devsite-page-title` nachdem Sie **auf neue Stilregel**geklickt haben.</span><span class="sxs-lookup"><span data-stu-id="5db20-276">In [Figure 16](#figure-16), DevTools adds the `h1.devsite-page-title` style rule after clicking **New Style Rule**.</span></span>  

> ##### <span data-ttu-id="5db20-277">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="5db20-277">Figure 16</span></span>  
> <span data-ttu-id="5db20-278">Hinzufügen einer neuen Stilregel</span><span class="sxs-lookup"><span data-stu-id="5db20-278">Adding a new style rule</span></span>  
> ![Hinzufügen einer neuen Stilregel][ImageStyleRule]  

#### <span data-ttu-id="5db20-280">Auswählen des Stylesheets, dem eine Regel hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="5db20-280">Choose which stylesheet to add a rule to</span></span>   

<span data-ttu-id="5db20-281">Wenn Sie [eine neue Stilregel hinzufügen](#add-a-style-rule), klicken und **halten Sie** die neue Stilregel Regel neu, um ![ auszuwählen, ][ImageNewStyleRuleIcon] welchem Stylesheet die Stilregel hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5db20-281">When [adding a new style rule](#add-a-style-rule), click and hold **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon] to choose which stylesheet to add the style rule to.</span></span>  

> ##### <span data-ttu-id="5db20-282">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="5db20-282">Figure 17</span></span>  
> <span data-ttu-id="5db20-283">Auswählen eines Stylesheets</span><span class="sxs-lookup"><span data-stu-id="5db20-283">Choosing a stylesheet</span></span>  
> ![Auswählen eines Stylesheets][ImageChooseStylesheet]  

#### <span data-ttu-id="5db20-285">Hinzufügen einer Stilregel zu einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="5db20-285">Add a style rule to a specific location</span></span>   

<span data-ttu-id="5db20-286">So fügen Sie auf der Registerkarte **Formatvorlagen** eine Stilregel zu einer bestimmten Position hinzu:</span><span class="sxs-lookup"><span data-stu-id="5db20-286">To add a style rule to a specific location in the **Styles** tab:</span></span>  

1.  <span data-ttu-id="5db20-287">Zeigen Sie mit der Maus auf die Stilregel, die sich direkt darüber befindet, wo Sie die neue Stilregel hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="5db20-287">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="5db20-288">[Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5db20-288">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5db20-289">Klicken Sie unter Formatvorlagenregel einfügen auf **Stil Regel einfügen** ![ ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="5db20-289">Click **Insert Style Rule Below** ![Insert Style Rule Below][ImageNewStyleRuleIcon].</span></span>  

> ##### <span data-ttu-id="5db20-290">Abbildung 18</span><span class="sxs-lookup"><span data-stu-id="5db20-290">Figure 18</span></span>  
> **<span data-ttu-id="5db20-291">Einfügen einer Stilregel unten</span><span class="sxs-lookup"><span data-stu-id="5db20-291">Insert Style Rule Below</span></span>**  
> ![Einfügen einer Stilregel unten][ImageInsertStyleRuleBelow]  

### <span data-ttu-id="5db20-293">Anzeigen der Symbolleiste "Weitere Aktionen"</span><span class="sxs-lookup"><span data-stu-id="5db20-293">Reveal the More Actions toolbar</span></span>   

<span data-ttu-id="5db20-294">Auf der Symbolleiste **Weitere Aktionen** können Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="5db20-294">The **More Actions** toolbar lets you:</span></span>  

*   <span data-ttu-id="5db20-295">Fügen Sie eine Stilregel direkt unter die Regel ein, auf die Sie sich konzentrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5db20-295">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="5db20-296">Fügen `background-color` `color` `box-shadow` `text-shadow` Sie der Stilregel, auf die Sie sich konzentrieren, eine,-oder-Deklaration hinzu.</span><span class="sxs-lookup"><span data-stu-id="5db20-296">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="5db20-297">So zeigen Sie die Symbolleiste " **Weitere Aktionen** " an:</span><span class="sxs-lookup"><span data-stu-id="5db20-297">To reveal the **More Actions** toolbar:</span></span>  

1.  <span data-ttu-id="5db20-298">Zeigen Sie auf der Registerkarte **Formatvorlagen** auf eine Stilregel.</span><span class="sxs-lookup"><span data-stu-id="5db20-298">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="5db20-299">**Weitere Aktionen** `...` wird in der unteren rechten Ecke des Abschnitts Stilregel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5db20-299">**More Actions** `...` is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5db20-300">Zeigen Sie in [Abbildung 19](#figure-19)auf die `.header-holder.has-default-focus` Stilregel, und klicken Sie unten rechts im Abschnitt Stilregel auf **Weitere Aktionen** .</span><span class="sxs-lookup"><span data-stu-id="5db20-300">In [Figure 19](#figure-19), hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    > ##### <span data-ttu-id="5db20-301">Abbildung 19</span><span class="sxs-lookup"><span data-stu-id="5db20-301">Figure 19</span></span>  
    > <span data-ttu-id="5db20-302">Aufdecken **weiterer Aktionen**</span><span class="sxs-lookup"><span data-stu-id="5db20-302">Revealing **More Actions**</span></span>  
    > ![Aufdecken weiterer Aktionen][ImageRevealMore]  
    
1.  <span data-ttu-id="5db20-304">Zeigen Sie auf **Weitere Aktionen** `...` , um die oben genannten Aktionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5db20-304">Hover over **More Actions** `...` to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5db20-305">Die **Regel "Stil einfügen" unterhalb** der Aktion wird nach dem Hovern auf **Weitere Aktionen**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5db20-305">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    > ##### <span data-ttu-id="5db20-306">Abbildung 20</span><span class="sxs-lookup"><span data-stu-id="5db20-306">Figure 20</span></span>  
    > <span data-ttu-id="5db20-307">Die Symbolleiste " **Weitere Aktionen** "</span><span class="sxs-lookup"><span data-stu-id="5db20-307">The **More Actions** toolbar</span></span>  
    > ![Die Symbolleiste "Weitere Aktionen"][ImageInsertStyleRuleBelow2]  
    
### <span data-ttu-id="5db20-309">Umschalten einer Deklaration</span><span class="sxs-lookup"><span data-stu-id="5db20-309">Toggle a declaration</span></span>   

<span data-ttu-id="5db20-310">So aktivieren oder deaktivieren Sie eine einzelne Deklaration:</span><span class="sxs-lookup"><span data-stu-id="5db20-310">To toggle a single declaration on or off:</span></span>  

1.  <span data-ttu-id="5db20-311">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5db20-311">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5db20-312">Zeigen Sie im Bereich **Formatvorlagen** auf die Regel, die die Deklaration definiert.</span><span class="sxs-lookup"><span data-stu-id="5db20-312">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="5db20-313">Kontrollkästchen werden neben jeder Deklaration angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5db20-313">Checkboxes appear next to each declaration.</span></span>  
1.  <span data-ttu-id="5db20-314">Aktivieren oder deaktivieren Sie das Kontrollkästchen neben der Deklaration.</span><span class="sxs-lookup"><span data-stu-id="5db20-314">Check or uncheck the checkbox next to the declaration.</span></span>  <span data-ttu-id="5db20-315">Wenn Sie eine Deklaration deaktivieren, wird Sie von devtools durchgestrichen, um anzugeben, dass Sie nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="5db20-315">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="5db20-316">In [Abbildung 21](#figure-21)wurde die `margin-top` Eigenschaft für das aktuell ausgewählte Element deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5db20-316">In [Figure 21](#figure-21), the `margin-top` property for the currently selected element has been toggled off.</span></span>  

> ##### <span data-ttu-id="5db20-317">Abbildung 21</span><span class="sxs-lookup"><span data-stu-id="5db20-317">Figure 21</span></span>  
> <span data-ttu-id="5db20-318">Umschalten einer Deklaration</span><span class="sxs-lookup"><span data-stu-id="5db20-318">Toggling a declaration</span></span>  
> ![Umschalten einer Deklaration][ImageToggleDeclaration]  

### <span data-ttu-id="5db20-320">Hinzufügen einer Hintergrundfarben Deklaration</span><span class="sxs-lookup"><span data-stu-id="5db20-320">Add a background-color declaration</span></span>   

<span data-ttu-id="5db20-321">So fügen Sie einem `background-color` Element eine Deklaration hinzu:</span><span class="sxs-lookup"><span data-stu-id="5db20-321">To add a `background-color` declaration to an element:</span></span>  

1.  <span data-ttu-id="5db20-322">Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `background-color` .</span><span class="sxs-lookup"><span data-stu-id="5db20-322">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="5db20-323">[Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5db20-323">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5db20-324">Klicken Sie auf **Hintergrundfarbe hinzu** fügen ![ , um Hintergrundfarbe hinzuzufügen ][ImageAddBackgroundColorIcon] .</span><span class="sxs-lookup"><span data-stu-id="5db20-324">Click **Add Background Color** ![Add Background Color][ImageAddBackgroundColorIcon].</span></span>  

> ##### <span data-ttu-id="5db20-325">Abbildung 22</span><span class="sxs-lookup"><span data-stu-id="5db20-325">Figure 22</span></span>  
> **<span data-ttu-id="5db20-326">Hinzufügen einer Hintergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="5db20-326">Add Background Color</span></span>**  
> ![Hinzufügen einer Hintergrundfarbe][ImageAddBackgroundColor]  

### <span data-ttu-id="5db20-328">Hinzufügen einer Farb Deklaration</span><span class="sxs-lookup"><span data-stu-id="5db20-328">Add a color declaration</span></span>   

<span data-ttu-id="5db20-329">So fügen Sie einem `color` Element eine Deklaration hinzu:</span><span class="sxs-lookup"><span data-stu-id="5db20-329">To add a `color` declaration to an element:</span></span>  

1.  <span data-ttu-id="5db20-330">Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `color` .</span><span class="sxs-lookup"><span data-stu-id="5db20-330">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="5db20-331">[Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5db20-331">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5db20-332">Klicken Sie auf **Farbe** hinzufügen ![ ][ImageAddColorIcon] .</span><span class="sxs-lookup"><span data-stu-id="5db20-332">Click **Add Color** ![Add Color][ImageAddColorIcon].</span></span>  

> ##### <span data-ttu-id="5db20-333">Abbildung 23</span><span class="sxs-lookup"><span data-stu-id="5db20-333">Figure 23</span></span>  
> **<span data-ttu-id="5db20-334">Farbe hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5db20-334">Add Color</span></span>**  
> ![Farbe hinzufügen][ImageAddColor]  

### <span data-ttu-id="5db20-336">Hinzufügen einer Box-Shadow-Deklaration</span><span class="sxs-lookup"><span data-stu-id="5db20-336">Add a box-shadow declaration</span></span>   

<span data-ttu-id="5db20-337">So fügen Sie einem `box-shadow` Element eine Deklaration hinzu:</span><span class="sxs-lookup"><span data-stu-id="5db20-337">To add a `box-shadow` declaration to an element:</span></span>  

1.  <span data-ttu-id="5db20-338">Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `box-shadow` .</span><span class="sxs-lookup"><span data-stu-id="5db20-338">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="5db20-339">[Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5db20-339">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5db20-340">Klicken Sie auf **Feld** Schatten hinzufügen ![ ][ImageAddBoxShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="5db20-340">Click **Add Box Shadow** ![Add Box Shadow][ImageAddBoxShadowIcon].</span></span>  

> ##### <span data-ttu-id="5db20-341">Abbildung 24</span><span class="sxs-lookup"><span data-stu-id="5db20-341">Figure 24</span></span>  
> **<span data-ttu-id="5db20-342">Feld Schatten hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5db20-342">Add Box Shadow</span></span>**  
> ![Feld Schatten hinzufügen][ImageAddBoxShadow]  

### <span data-ttu-id="5db20-344">Hinzufügen einer Text-Shadow-Deklaration</span><span class="sxs-lookup"><span data-stu-id="5db20-344">Add a text-shadow declaration</span></span>   

<span data-ttu-id="5db20-345">So fügen Sie einem `text-shadow` Element eine Deklaration hinzu:</span><span class="sxs-lookup"><span data-stu-id="5db20-345">To add a `text-shadow` declaration to an element:</span></span>  

1.  <span data-ttu-id="5db20-346">Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `text-shadow` .</span><span class="sxs-lookup"><span data-stu-id="5db20-346">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="5db20-347">[Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5db20-347">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5db20-348">Klicken Sie auf **Text** Schatten hinzufügen ![ , um Text Schatten hinzuzufügen ][ImageAddTextShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="5db20-348">Click **Add Text Shadow** ![Add Text Shadow][ImageAddTextShadowIcon].</span></span>  

> ##### <span data-ttu-id="5db20-349">Abbildung 25</span><span class="sxs-lookup"><span data-stu-id="5db20-349">Figure 25</span></span>  
> **<span data-ttu-id="5db20-350">Hinzufügen von Text Schatten</span><span class="sxs-lookup"><span data-stu-id="5db20-350">Add Text Shadow</span></span>**  
> ![Hinzufügen von Text Schatten][ImageAddTextShadow]  

### <span data-ttu-id="5db20-352">Ändern von Farben mit der Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="5db20-352">Change colors with the Color Picker</span></span>   

<span data-ttu-id="5db20-353">Die **Farbauswahl** bietet eine GUI für Änderungen `color` und `background-color` Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="5db20-353">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="5db20-354">So öffnen Sie die **Farbauswahl**:</span><span class="sxs-lookup"><span data-stu-id="5db20-354">To open the **Color Picker**:</span></span>  

1.  <span data-ttu-id="5db20-355">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5db20-355">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5db20-356">Suchen Sie auf der Registerkarte **Formatvorlagen** nach der `color` `background-color` oder ähnlichen Deklaration, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="5db20-356">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="5db20-357">Links vom `color` `background-color` oder ähnlichen Wert befindet sich ein kleines Quadrat, das eine Vorschau der Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="5db20-357">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5db20-358">In [Abbildung 26](#figure-26)ist das kleine Quadrat links von `rgba(0, 0, 0, 0.7)` einer Vorschau dieser Farbe.</span><span class="sxs-lookup"><span data-stu-id="5db20-358">In [Figure 26](#figure-26), the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    > ##### <span data-ttu-id="5db20-359">Abbildung 26</span><span class="sxs-lookup"><span data-stu-id="5db20-359">Figure 26</span></span>  
    > <span data-ttu-id="5db20-360">Farbvorschau</span><span class="sxs-lookup"><span data-stu-id="5db20-360">Color preview</span></span>  
    > ![Farbvorschau][ImageColorPreview]  
    
1.  <span data-ttu-id="5db20-362">Klicken Sie auf die Vorschau, um die **Farbauswahl**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5db20-362">Click the preview to open the **Color Picker**.</span></span>  
    
    > ##### <span data-ttu-id="5db20-363">Abbildung 27</span><span class="sxs-lookup"><span data-stu-id="5db20-363">Figure 27</span></span>  
    > <span data-ttu-id="5db20-364">Die **Farbauswahl**</span><span class="sxs-lookup"><span data-stu-id="5db20-364">The **Color Picker**</span></span>  
    > ![Die Farbauswahl][ImageColorPicker]  
    
<span data-ttu-id="5db20-366">Nachfolgend finden Sie eine Beschreibung der einzelnen UI-Elemente der **Farbauswahl**:</span><span class="sxs-lookup"><span data-stu-id="5db20-366">Here is a description of each of the UI elements of the **Color Picker**:</span></span>  

> ##### <span data-ttu-id="5db20-367">Abbildung 28</span><span class="sxs-lookup"><span data-stu-id="5db20-367">Figure 28</span></span>  
> <span data-ttu-id="5db20-368">Die Farbauswahl mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="5db20-368">The Color Picker, annotated</span></span>  
> ![Die Farbauswahl mit Anmerkungen][ImageColorPickerAnnotated]  

1.  <span data-ttu-id="5db20-370">**Schattierungen**.</span><span class="sxs-lookup"><span data-stu-id="5db20-370">**Shades**.</span></span>  
1.  <span data-ttu-id="5db20-371">**Pipette**.</span><span class="sxs-lookup"><span data-stu-id="5db20-371">**Eyedropper**.</span></span>  <span data-ttu-id="5db20-372">Sehen Sie sich das [Beispiel einer Farbe auf der Seite mit der Pipette an](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="5db20-372">See [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
1.  <span data-ttu-id="5db20-373">**In die Zwischenablage kopieren**</span><span class="sxs-lookup"><span data-stu-id="5db20-373">**Copy To Clipboard**.</span></span>  <span data-ttu-id="5db20-374">Kopieren Sie den **Anzeigewert** in Ihre Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="5db20-374">Copy the **Display Value** to your clipboard.</span></span>  
1.  <span data-ttu-id="5db20-375">**Anzeigewert**.</span><span class="sxs-lookup"><span data-stu-id="5db20-375">**Display Value**.</span></span>  <span data-ttu-id="5db20-376">Die RGBA-, HSLA-oder Hex-Darstellung der Farbe.</span><span class="sxs-lookup"><span data-stu-id="5db20-376">The RGBA, HSLA, or Hex representation of the color.</span></span>  
1.  <span data-ttu-id="5db20-377">**Farb Palette**</span><span class="sxs-lookup"><span data-stu-id="5db20-377">**Color Palette**.</span></span>  <span data-ttu-id="5db20-378">Klicken Sie auf eines dieser Quadrate, um die Farbe in das Quadrat zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5db20-378">Click one of these squares to change the color to that square.</span></span>  
1.  <span data-ttu-id="5db20-379">**Farbton**aus.</span><span class="sxs-lookup"><span data-stu-id="5db20-379">**Hue**.</span></span>  
1.  <span data-ttu-id="5db20-380">**Deckkraft**.</span><span class="sxs-lookup"><span data-stu-id="5db20-380">**Opacity**.</span></span>  
1.  <span data-ttu-id="5db20-381">**Anzeigen des Wert Umschalters**</span><span class="sxs-lookup"><span data-stu-id="5db20-381">**Display Value Switcher**.</span></span>  <span data-ttu-id="5db20-382">Wechseln zwischen den RGBA-, HSLA-und Hex-Darstellungen der aktuellen Farbe</span><span class="sxs-lookup"><span data-stu-id="5db20-382">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
1.  <span data-ttu-id="5db20-383">**Farbpaletten-Switcher**</span><span class="sxs-lookup"><span data-stu-id="5db20-383">**Color Palette Switcher**.</span></span>  <span data-ttu-id="5db20-384">Wechseln zwischen der [Material Design Palette][MaterialDesignColorSystem], einer benutzerdefinierten Palette oder einer Seitenfarben-Palette</span><span class="sxs-lookup"><span data-stu-id="5db20-384">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="5db20-385">DevTools generiert die Seiten Farbpalette basierend auf den Farben, die in ihren Stylesheets gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="5db20-385">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  

#### <span data-ttu-id="5db20-386">Beispiel für eine Farbe auf der Seite mit der Pipette</span><span class="sxs-lookup"><span data-stu-id="5db20-386">Sample a color off the page with the Eyedropper</span></span>   

<span data-ttu-id="5db20-387">Wenn Sie die **Farbauswahl**öffnen, ist **die Pipette** ![ ][ImageEyedropperIcon] standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5db20-387">When you open the **Color Picker**, the **Eyedropper** ![Eyedropper][ImageEyedropperIcon] is on by default.</span></span>  <span data-ttu-id="5db20-388">So ändern Sie die ausgewählte Farbe auf eine andere Farbe auf der Seite:</span><span class="sxs-lookup"><span data-stu-id="5db20-388">To change the selected color to some other color on the page:</span></span>  

1.  <span data-ttu-id="5db20-389">Zeigen Sie mit der Maus auf die Zielfarbe im Viewport.</span><span class="sxs-lookup"><span data-stu-id="5db20-389">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="5db20-390">Klicken Sie, um zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="5db20-390">Click to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5db20-391">In [Abbildung 29](#figure-29)zeigt die **Farbauswahl** einen aktuellen Farbwert von, der sich in der `rgba(0,0,0,0.7)` Nähe von schwarz befindet.</span><span class="sxs-lookup"><span data-stu-id="5db20-391">In [Figure 29](#figure-29), the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="5db20-392">Diese Farbe sollte auf das Schwarz geändert werden, das aktuell im Viewport hervorgehoben ist, nachdem auf das schwarze geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="5db20-392">This color should change to the black that is currently highlighted in the viewport once the black was clicked.</span></span>  
    
    > ##### <span data-ttu-id="5db20-393">Abbildung 29</span><span class="sxs-lookup"><span data-stu-id="5db20-393">Figure 29</span></span>  
    > <span data-ttu-id="5db20-394">Verwenden der Pipette</span><span class="sxs-lookup"><span data-stu-id="5db20-394">Using the Eyedropper</span></span>  
    > ![Verwenden der Pipette][ImageUsingEyedropper]  
    
 



<!-- image links -->  

[ImageAddBackgroundColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: /microsoft-edge/devtools-guide-chromium/media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-an-element-icon.msft.png  

[ImageSelectedElement]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1.msft.png "Abbildung 1: ein Beispiel für ein ausgewähltes Element"  
[ImageViewRuleStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-highlight.msft.png "Abbildung 2: Anzeigen des Stylesheets, in dem eine Regel definiert ist"  
[ImageComputedTab]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-h1.msft.png "Abbildung 3: die Registerkarte "berechnet""  
[ImageBoxModel]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-2.msft.png "Abbildung 4: das Diagramm des Feld Modells"  
[ImageStylesFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-color.msft.png "Abbildung 5: Filtern der Registerkarte "Formatvorlagen""  
[ImageComputerFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-filter-100.msft.png "Abbildung 6: Filtern der berechneten Registerkarte"  
[ImagePseudoClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-hov-hover.msft.png "Abbildung 7: Umschalten der: hover-Pseudoklasse"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-coverage.msft.png "Abbildung 8: Öffnen der Registerkarte Coverage über das Befehlsmenü"  
[ImageCoverageEmpty]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-empty.msft.png "Abbildung 9: Registerkarte "Coverage""  
[ImageCoverageOverview]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-run.msft.png "Abbildung 10: eine Übersicht darüber, wie viel CSS (und JavaScript) verwendet und nicht verwendet wird"  
[ImageCoverageDetail]: /microsoft-edge/devtools-guide-chromium/media/css-sources-css-coverage.msft.png "Abbildung 11: eine Zeile-für-Zeile-Aufteilung der verwendeten und nicht verwendeten CSS"  
[ImageInlineDeclarations]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-margin-top-background-color.msft.png "Abbildung 12: Hinzufügen von Inline Deklarationen"  
[ImageAddDeclarationExistingRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style.msft.png "Abbildung 13: Hinzufügen einer Deklaration zu einer Formatvorlagenregel"  
[ImageAddDeclarationExistingRule2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style-dropdown.msft.png "Abbildung 14: Ändern des Werts einer Deklaration"  
[ImageElementClasses]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-classes.msft.png "Abbildung 15: Bereich "Element Klassen""  
[ImageStyleRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new.msft.png "Abbildung 16: Hinzufügen einer neuen Stilregel"  
[ImageChooseStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new-select-exisiting.msft.png "Abbildung 17: Auswählen eines Stylesheets"  
[ImageInsertStyleRuleBelow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-insert-style-rule-below.msft.png "Abbildung 18: Einfügen einer Stilregel nach unten"  
[ImageRevealMore]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-new-rule-styles.msft.png "Abbildung 19: aufdecken weiterer Aktionen"  
[ImageInsertStyleRuleBelow2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png "Abbildung 20: die Symbolleiste "Weitere Aktionen""  
[ImageToggleDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-deactivated.msft.png "Abbildung 21: Umschalten einer Deklaration"  
[ImageAddBackgroundColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-background-color.msft.png "Abbildung 22: Hinzufügen einer Hintergrundfarbe"  
[ImageAddColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-color.msft.png "Abbildung 23: Hinzufügen von Farben"  
[ImageAddBoxShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-box-shadow.msft.png "Abbildung 24: Hinzufügen eines Feld Schattens"  
[ImageAddTextShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-text-shadow.msft.png "Abbildung 25: Hinzufügen von Text Schatten"  
[ImageColorPreview]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-overlay-color-box.msft.png "Abbildung 26: Farbvorschau"  
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker.msft.png "Abbildung 27: die Farbauswahl"  
[ImageColorPickerAnnotated]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker-annotated.msft.png "Abbildung 28: die Farbauswahl mit Anmerkungen"  
[ImageUsingEyedropper]: /microsoft-edge/devtools-guide-chromium/media/css-color-picker-eye-dropper.msft.png "Abbildung 29: Verwenden der Pipette"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Erste Schritte beim Anzeigen und Ändern von CSS"  
[DevToolsCSSGetStartedAddPseudoState]: /microsoft-edge/devtools-guide-chromium/css/index#add-a-pseudostate-to-a-class "Hinzufügen eines PseudoState zu einer Klasse – erste Schritte mit dem anzeigen und Ändern von CSS"  
[DevToolsCSSGetStartedTutorial]: /microsoft-edge/devtools-guide-chromium/css/index#view-the-css-for-an-element "Anzeigen der CSS für ein Element – erste Schritte mit dem anzeigen und Ändern von CSS"  
[DevToolsCssPrintPreview]: /microsoft-edge/devtools-guide-chromium/css/print-preview "Erzwingen von Microsoft Edge devtools in den Druckvorschau Modus (CSS-Druckmedientyp)"  
[DevToolsJavascriptReferenceFormat]: /microsoft-edge/devtools-guide-chromium/javascript/reference#make-a-minified-file-readable "Erstellen einer minimierte-Datei lesbar-JavaScript-Debug-Referenz"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Das Farbsystem – Material Design"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Das Feld Modell | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Auswahltypen – Spezifität | MDN"  

> [!NOTE]
> <span data-ttu-id="5db20-434">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5db20-434">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5db20-435">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="5db20-435">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="5db20-437">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5db20-437">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

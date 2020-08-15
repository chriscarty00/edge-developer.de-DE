---
title: CSS-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 908e32140d9deb89489089442055e188cd2d9378
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931386"
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

# <span data-ttu-id="cd010-103">CSS-Referenz</span><span class="sxs-lookup"><span data-stu-id="cd010-103">CSS reference</span></span>  

<span data-ttu-id="cd010-104">Entdecken Sie neue Workflows in der folgenden umfassenden Referenz zu den Microsoft Edge devtools-Features, die sich auf das Anzeigen und Ändern von CSS beziehen.</span><span class="sxs-lookup"><span data-stu-id="cd010-104">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="cd010-105">Informationen zu den Grundlagen finden Sie unter [Erste Schritte beim Anzeigen und Ändern von CSS][DevToolsCSSGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="cd010-105">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="cd010-106">Auswählen eines Elements</span><span class="sxs-lookup"><span data-stu-id="cd010-106">Select an element</span></span>  

<span data-ttu-id="cd010-107">Mit dem Element Panel von devtools können **Sie das CSS** eines Elements gleichzeitig anzeigen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="cd010-107">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="cd010-108">Das ausgewählte Element ist in der **DOM-Struktur**hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="cd010-108">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="cd010-109">Die Formatvorlagen des Elements werden im Bereich **Formatvorlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd010-109">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="cd010-110">Weitere Informationen finden Sie unter [Anzeigen des CSS für ein Element][DevToolsCSSGetStartedTutorial] für ein Lernprogramm.</span><span class="sxs-lookup"><span data-stu-id="cd010-110">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="cd010-111">In der folgenden Abbildung ist das `h1` in der **DOM-Struktur** hervorgehobene Element das ausgewählte Element.</span><span class="sxs-lookup"><span data-stu-id="cd010-111">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="cd010-112">Auf der rechten Seite werden die Formatvorlagen des Elements im Bereich **Formatvorlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd010-112">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="cd010-113">Auf der linken Seite ist das Element im Viewport hervorgehoben, allerdings nur, weil die Maus gerade in der DOM- **Struktur**darüber schwebt.</span><span class="sxs-lookup"><span data-stu-id="cd010-113">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="cd010-115">Ein Beispiel für ein ausgewähltes Element</span><span class="sxs-lookup"><span data-stu-id="cd010-115">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="cd010-116">Verwenden Sie eine der folgenden Aktionen, um ein Element auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="cd010-116">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="cd010-117">Zeigen Sie im Viewport auf das Element, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-117">In your viewport, hover on the element, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
*   <span data-ttu-id="cd010-118">Wählen Sie in devtools **Element auswählen** \ ( ![ Element auswählen ][ImageSelectAnElementIcon] \) aus, oder wählen Sie `Control` + `Shift` + `C` \ (Windows \) oder `Command` + `Shift` + `C` \ (macOS \) aus, und wählen Sie dann das Element im Viewport aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-118">In DevTools, choose **Select an element** \(![Select an element][ImageSelectAnElementIcon]\) or select `Control`+`Shift`+`C` \(Windows\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="cd010-119">Wählen Sie in devtools das Element in der **DOM-Struktur**aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-119">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="cd010-120">Führen Sie in devtools eine Abfrage wie `document.querySelector('p')` in der **Konsole**aus, zeigen Sie auf das Ergebnis, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **im Dialogfeldelemente**anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-120">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and select **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="cd010-121">CSS anzeigen</span><span class="sxs-lookup"><span data-stu-id="cd010-121">View CSS</span></span>  

### <span data-ttu-id="cd010-122">Anzeigen des externen Stylesheets, in dem eine Regel definiert ist</span><span class="sxs-lookup"><span data-stu-id="cd010-122">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="cd010-123">Wählen Sie im Bereich **Formatvorlagen** den Link neben einer CSS-Regel aus, um das externe Stylesheet zu öffnen, das die Regel definiert.</span><span class="sxs-lookup"><span data-stu-id="cd010-123">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="cd010-124">Wenn das Stylesheet minimierte ist, lesen Sie [Erstellen einer minimierte-Datei][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="cd010-124">If the stylesheet is minified, see [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="cd010-125">In der folgenden Abbildung werden Sie nach der Auswahl `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` an Zeile 2 von `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , in der die `.content h1:first-of-type` CSS-Regel definiert ist, weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="cd010-125">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Anzeigen des Stylesheets, in dem eine Regel definiert ist" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="cd010-127">Anzeigen des Stylesheets, in dem eine Regel definiert ist</span><span class="sxs-lookup"><span data-stu-id="cd010-127">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <span data-ttu-id="cd010-128">Anzeigen nur des CSS, das tatsächlich auf ein Element angewendet wird</span><span class="sxs-lookup"><span data-stu-id="cd010-128">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="cd010-129">Auf der Registerkarte **Formatvorlagen** werden alle Regeln angezeigt, die für ein Element gelten, einschließlich Deklarationen, die überschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="cd010-129">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="cd010-130">Wenn Sie nicht an überschriebenen Deklarationen interessiert sind, verwenden Sie die Registerkarte **berechnet** , um nur das CSS anzuzeigen, das tatsächlich auf ein Element angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd010-130">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="cd010-131">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="cd010-131">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="cd010-132">Wechseln Sie im **Element** Fenster zur Registerkarte **berechnet** .</span><span class="sxs-lookup"><span data-stu-id="cd010-132">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="cd010-133">In einem breiten devtools-Fenster ist die Registerkarte **berechnet** nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cd010-133">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="cd010-134">Der Inhalt der Registerkarte **berechnet** wird auf der Registerkarte **Formatvorlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd010-134">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="cd010-135">Geerbte Eigenschaften sind nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="cd010-135">Inherited properties are opaque.</span></span>  <span data-ttu-id="cd010-136">Aktivieren Sie das Kontrollkästchen **Alle anzeigen** , um alle geerbten Werte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cd010-136">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="cd010-137">In der folgenden Abbildung werden auf der Registerkarte **berechnet** die CSS-Eigenschaften angezeigt, die auf das aktuell ausgewählte Element angewendet werden `h1` .</span><span class="sxs-lookup"><span data-stu-id="cd010-137">In the following figure, the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Die Registerkarte "berechnet"" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="cd010-139">Die Registerkarte " **berechnet** "</span><span class="sxs-lookup"><span data-stu-id="cd010-139">The **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="cd010-140">Anzeigen von CSS-Eigenschaften in alphabetischer Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="cd010-140">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="cd010-141">Verwenden Sie die Registerkarte **berechnet** .  Informationen finden Sie unter [Anzeigen der CSS, die tatsächlich auf ein Element angewendet](#view-only-the-css-that-is-actually-applied-to-an-element)werden.</span><span class="sxs-lookup"><span data-stu-id="cd010-141">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="cd010-142">Anzeigen von geerbten CSS-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd010-142">View inherited CSS properties</span></span>  

<span data-ttu-id="cd010-143">Aktivieren Sie das Kontrollkästchen **Alle anzeigen** auf der Registerkarte **berechnet** .  Informationen finden Sie unter [Anzeigen der CSS, die tatsächlich auf ein Element angewendet](#view-only-the-css-that-is-actually-applied-to-an-element)werden.</span><span class="sxs-lookup"><span data-stu-id="cd010-143">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="cd010-144">Anzeigen des Box-Modells für ein Element</span><span class="sxs-lookup"><span data-stu-id="cd010-144">View the box model for an element</span></span>  

<span data-ttu-id="cd010-145">Wenn Sie [das Feld Modell][MDNBoxModel] eines Elements anzeigen möchten, wechseln Sie zur Registerkarte **Formatvorlagen** .  Wenn Ihr devtools-Fenster schmal ist, befindet sich das **Feld Modell** Diagramm unten auf der Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="cd010-145">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="cd010-146">Wählen Sie einen Wert aus, und bearbeiten Sie ihn, um einen Wert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cd010-146">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="cd010-147">In der folgenden Abbildung wird im **Feld Modell** Diagramm auf der Registerkarte **Formatvorlagen** das Feld Modell für das aktuell ausgewählte `h1` Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd010-147">In the following figure, the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Das Diagramm des Feld Modells" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="cd010-149">Das Diagramm des **Feld Modells**</span><span class="sxs-lookup"><span data-stu-id="cd010-149">The **Box Model** diagram</span></span>  
:::image-end:::  

### <span data-ttu-id="cd010-150">Suchen und Filtern des CSS eines Elements</span><span class="sxs-lookup"><span data-stu-id="cd010-150">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="cd010-151">Verwenden Sie das Textfeld " **Filter** " auf den Registerkarten " **Formatvorlagen** " und " **berechnet** ", um nach bestimmten CSS-Eigenschaften oder-Werten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="cd010-151">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="cd010-152">Wenn Sie auch geerbte Eigenschaften auf der Registerkarte **berechnet** durchsuchen möchten, aktivieren Sie das Kontrollkästchen **Alle anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="cd010-152">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="cd010-153">In der folgenden Abbildung wird die Registerkarte **Formatvorlagen** so gefiltert, dass nur Regeln angezeigt werden, die die Suchabfrage enthalten `color` .</span><span class="sxs-lookup"><span data-stu-id="cd010-153">In the following figure, the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtern der Registerkarte "Formatvorlagen"" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="cd010-155">Filtern der Registerkarte " **Formatvorlagen** "</span><span class="sxs-lookup"><span data-stu-id="cd010-155">Filter the **Styles** tab</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="cd010-156">In der folgenden Abbildung wird die Registerkarte **berechnet** so gefiltert, dass nur Deklarationen angezeigt werden, die die Suchabfrage enthalten `100%` .</span><span class="sxs-lookup"><span data-stu-id="cd010-156">In the following figure, the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtern der berechneten Registerkarte" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="cd010-158">Filtern der **berechneten** Registerkarte</span><span class="sxs-lookup"><span data-stu-id="cd010-158">Filter the **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="cd010-159">Umschalten einer Pseudoklasse</span><span class="sxs-lookup"><span data-stu-id="cd010-159">Toggle a pseudo-class</span></span>  

<span data-ttu-id="cd010-160">Führen Sie die folgenden Aktionen aus, um eine Pseudoklasse wie, `:active` `:focus` , oder zu wechseln `:hover` `:visited` .</span><span class="sxs-lookup"><span data-stu-id="cd010-160">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="cd010-161">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="cd010-161">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="cd010-162">Wechseln Sie im **Element** Fenster zur Registerkarte **Formatvorlagen** .</span><span class="sxs-lookup"><span data-stu-id="cd010-162">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="cd010-163">Wählen Sie **: Hov**aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-163">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="cd010-164">Überprüfen Sie die Pseudoklasse, die Sie aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cd010-164">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="cd010-165">Wechseln Sie in der folgenden Abbildung zur `:hover` Pseudoklasse.</span><span class="sxs-lookup"><span data-stu-id="cd010-165">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="cd010-166">Überprüfen Sie im Viewport, ob die `background-color: cornflowerblue` Deklaration auf das Element angewendet wird, obwohl das Element nicht tatsächlich über den Zeiger bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="cd010-166">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Umschalten der: hover-Pseudoklasse" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="cd010-168">Umschalten der `:hover` Pseudoklasse</span><span class="sxs-lookup"><span data-stu-id="cd010-168">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="cd010-169">Ein interaktives Lernprogramm finden Sie unter [Hinzufügen eines PseudoState zu einer Klasse][DevToolsCSSGetStartedAddPseudoState].</span><span class="sxs-lookup"><span data-stu-id="cd010-169">For an interactive tutorial, see [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <span data-ttu-id="cd010-170">Anzeigen einer Seite im Druckmodus</span><span class="sxs-lookup"><span data-stu-id="cd010-170">View a page in print mode</span></span>  

<span data-ttu-id="cd010-171">Führen Sie die folgenden Aktionen aus, um eine Seite im Druckmodus anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cd010-171">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="cd010-172">[Öffnen des Befehlsmenüs][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="cd010-172">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="cd010-173">Beginnen `Rendering` Sie mit der Eingabe, und wählen Sie aus `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="cd010-173">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="cd010-174">Wählen Sie für die Dropdownliste **CSS-Medien emulieren** die Option **Drucken**aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-174">For the **Emulate CSS Media** dropdown, select **print**.</span></span>  

### <span data-ttu-id="cd010-175">Anzeigen der verwendeten und nicht verwendeten CSS mit der Registerkarte "Coverage"</span><span class="sxs-lookup"><span data-stu-id="cd010-175">View used and unused CSS with the Coverage tab</span></span>  

<span data-ttu-id="cd010-176">Auf der Registerkarte Coverage wird angezeigt, welche CSS-Seiten tatsächlich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd010-176">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="cd010-177">Wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus, während sich devtools im Fokus befindet, um [das Befehlsmenü zu öffnen][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="cd010-177">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="cd010-178">Beginnen `coverage` Sie mit der Eingabe, und wählen Sie **Berichterstattung anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-178">Start typing `coverage` and select **Show Coverage**.</span></span>  <span data-ttu-id="cd010-179">Die Registerkarte Coverage wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd010-179">The Coverage tab appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Öffnen der Registerkarte "Abdeckung" über das Befehlsmenü" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="cd010-181">Öffnen der Registerkarte " **Abdeckung** " über das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="cd010-181">Open the **Coverage** tab from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Die Registerkarte "Coverage"" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="cd010-183">Die Registerkarte " **Coverage** "</span><span class="sxs-lookup"><span data-stu-id="cd010-183">The **Coverage** tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="cd010-184">Wählen Sie **Instrumentations Abdeckung starten und aktualisieren Sie die Seite** aus, und aktualisieren Sie die Seite ![ mit der Instrumentations Abdeckung und aktualisieren Sie die Seite ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="cd010-184">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="cd010-185">Die Seite wird aktualisiert, und die Registerkarte Coverage bietet eine Übersicht darüber, wie viel CSS \ (und JavaScript \) aus jeder Datei, die der Browser lädt, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd010-185">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="cd010-186">Grün steht für verwendetes CSS.</span><span class="sxs-lookup"><span data-stu-id="cd010-186">Green represents used CSS.</span></span>  <span data-ttu-id="cd010-187">Rot steht für nicht verwendetes CSS.</span><span class="sxs-lookup"><span data-stu-id="cd010-187">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Eine Übersicht darüber, wie viel CSS (und JavaScript) verwendet und nicht verwendet wird" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="cd010-189">Eine Übersicht darüber, wie viel CSS \ (und JavaScript \) verwendet und nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="cd010-189">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="cd010-190">Wählen Sie eine CSS-Datei aus, um eine Zeile für Zeile aufzuschlüsseln, was CSS verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd010-190">Choose a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cd010-191">In der folgenden Abbildung werden die Zeilen 145 bis 147 und 149 bis 151 nicht `b66bc881.site-ltr.css` verwendet, während Zeilen 163 bis 166 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd010-191">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Eine Zeile-für-Zeile-Aufteilung der verwendeten und nicht verwendeten CSS" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="cd010-193">Eine Zeile-für-Zeile-Aufteilung der verwendeten und nicht verwendeten CSS</span><span class="sxs-lookup"><span data-stu-id="cd010-193">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="cd010-194">Erzwingen des Druckvorschau Modus</span><span class="sxs-lookup"><span data-stu-id="cd010-194">Force print preview mode</span></span>  

<span data-ttu-id="cd010-195">Siehe [Erzwingen von devtools in den Druckvorschau Modus][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="cd010-195">See [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="cd010-196">CSS ändern</span><span class="sxs-lookup"><span data-stu-id="cd010-196">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="cd010-197">Hinzufügen einer CSS-Deklaration zu einem Element</span><span class="sxs-lookup"><span data-stu-id="cd010-197">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="cd010-198">Die Reihenfolge der Deklarationen wirkt sich darauf aus, wie ein Element formatiert wird, indem Sie die folgende Liste verwenden, um Deklarationen auf unterschiedliche Weise hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd010-198">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="cd010-199">[Fügen Sie eine Inline Deklaration hinzu](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="cd010-199">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="cd010-200">Entspricht dem Hinzufügen eines `style` Attributs zum HTML-Code eines Elements.</span><span class="sxs-lookup"><span data-stu-id="cd010-200">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="cd010-201">[Hinzufügen einer Deklaration zu einer Formatvorlagenregel](#add-a-declaration-to-a-style-rule)</span><span class="sxs-lookup"><span data-stu-id="cd010-201">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="cd010-202">Welchen Workflow sollten Sie verwenden?</span><span class="sxs-lookup"><span data-stu-id="cd010-202">What workflow should you use?</span></span>** <span data-ttu-id="cd010-203">In den meisten Fällen möchten Sie wahrscheinlich den Inline Deklarations Workflow verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd010-203">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="cd010-204">Inline Deklarationen haben eine höhere Spezifität als externe, sodass der Inline-Workflow sicherstellt, dass die Änderungen in Ihrem erwarteten Element wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="cd010-204">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="cd010-205">Weitere Informationen zur Spezifität finden Sie unter [Selector-Typen][MDNSelectorTypes].</span><span class="sxs-lookup"><span data-stu-id="cd010-205">For more information about specificity, see [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="cd010-206">Wenn Sie alle Formatvorlagen des Elements Debuggen und insbesondere testen möchten, was geschieht, wenn eine Deklaration an verschiedenen Stellen definiert ist, verwenden Sie den anderen Workflow.</span><span class="sxs-lookup"><span data-stu-id="cd010-206">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="cd010-207">Hinzufügen einer Inline Deklaration</span><span class="sxs-lookup"><span data-stu-id="cd010-207">Add an inline declaration</span></span>  

<span data-ttu-id="cd010-208">Führen Sie die folgenden Aktionen aus, um eine Inline Deklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd010-208">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="cd010-209">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="cd010-209">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="cd010-210">Wählen Sie im Bereich **Formatvorlagen** zwischen den Klammern des Abschnitts **Element. Format** aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-210">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="cd010-211">Der Cursor konzentriert sich, sodass Sie Text eingeben können.</span><span class="sxs-lookup"><span data-stu-id="cd010-211">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="cd010-212">Geben Sie einen Eigenschaftsnamen ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cd010-212">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="cd010-213">Geben Sie einen gültigen Wert für diese Eigenschaft ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cd010-213">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="cd010-214">Überprüfen Sie in der **DOM-Struktur**, ob `style` dem Element ein Attribut hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="cd010-214">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="cd010-215">In der folgenden Abbildung wurden die `margin-top` `background-color` Eigenschaften und auf das ausgewählte Element angewendet.</span><span class="sxs-lookup"><span data-stu-id="cd010-215">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="cd010-216">Überprüfen Sie in der **DOM-Struktur** , ob die Deklarationen im `style` Attribut für ein Element widergespiegelt werden.</span><span class="sxs-lookup"><span data-stu-id="cd010-216">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Hinzufügen von Inline Deklarationen" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="cd010-218">Hinzufügen von Inline Deklarationen</span><span class="sxs-lookup"><span data-stu-id="cd010-218">Add inline declarations</span></span>  
:::image-end:::  

#### <span data-ttu-id="cd010-219">Hinzufügen einer Deklaration zu einer Stilregel</span><span class="sxs-lookup"><span data-stu-id="cd010-219">Add a declaration to a style rule</span></span>  

<span data-ttu-id="cd010-220">Führen Sie die folgenden Aktionen aus, um eine Deklaration zu einer vorhandenen Stilregel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd010-220">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="cd010-221">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="cd010-221">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="cd010-222">Wählen Sie im Bereich **Formatvorlagen** zwischen den Klammern der Stilregel aus, der Sie die Deklaration hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="cd010-222">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="cd010-223">Der Cursor konzentriert sich, sodass Sie Text eingeben können.</span><span class="sxs-lookup"><span data-stu-id="cd010-223">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="cd010-224">Geben Sie einen Eigenschaftsnamen ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cd010-224">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="cd010-225">Geben Sie einen gültigen Wert für diese Eigenschaft ein, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cd010-225">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Hinzufügen einer Deklaration zu einer Formatvorlagenregel" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="cd010-227">Hinzufügen der `border-bottom-style:groove` Deklaration zu einer Stilregel</span><span class="sxs-lookup"><span data-stu-id="cd010-227">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <span data-ttu-id="cd010-228">Ändern des Namens oder Werts einer Deklaration</span><span class="sxs-lookup"><span data-stu-id="cd010-228">Change a declaration name or value</span></span>  

<span data-ttu-id="cd010-229">Wählen Sie den Namen oder den Wert einer Deklaration aus, und bearbeiten Sie ihn, um ihn zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cd010-229">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="cd010-230">Informationen dazu finden Sie unter [Ändern von Deklarations Werten mit Tastenkombinationen](#change-declaration-values-with-keyboard-shortcuts) für Tastenkombinationen, um einen Wert schnell zu erhöhen oder zu verringern `0.1` `1` `10` `100` .</span><span class="sxs-lookup"><span data-stu-id="cd010-230">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Ändern des Werts einer Deklaration" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="cd010-232">Ändern des Werts der `border-bottom-style` Deklaration</span><span class="sxs-lookup"><span data-stu-id="cd010-232">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="cd010-233">Ändern von Deklarations Werten mit Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="cd010-233">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="cd010-234">Wenn Sie den Wert einer Deklaration bearbeiten, können Sie die folgenden Tastenkombinationen verwenden, um den Wert um einen bestimmten Betrag zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="cd010-234">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="cd010-235">Wählen Sie `Alt` + `Up` \ (Windows \) oder `Option` + `Up` \ (macOS \) aus, um den Wert zu erhöhen `0.1` .</span><span class="sxs-lookup"><span data-stu-id="cd010-235">Select `Alt`+`Up` \(Windows\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="cd010-236">Wählen Sie aus, `Up` um den Wert nach `1` oder nach zu ändern, `0.1` Wenn der aktuelle Wert zwischen `-1` und ist `1` .</span><span class="sxs-lookup"><span data-stu-id="cd010-236">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="cd010-237">Wählen Sie aus `Shift` + `Up` , um zu inkrementieren `10` .</span><span class="sxs-lookup"><span data-stu-id="cd010-237">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="cd010-238">Wählen Sie `Shift` + `Page Up` \ (Windows \) oder `Shift` + `Command` + `Up` \ (macOS \) aus, um den Wert zu erhöhen `100` .</span><span class="sxs-lookup"><span data-stu-id="cd010-238">Select `Shift`+`Page Up` \(Windows\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="cd010-239">Das Dekrementieren funktioniert auch.</span><span class="sxs-lookup"><span data-stu-id="cd010-239">Decrementing also works.</span></span>  <span data-ttu-id="cd010-240">Ersetzen Sie einfach alle `Up` oben genannten Instanzen durch `Down` .</span><span class="sxs-lookup"><span data-stu-id="cd010-240">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="cd010-241">Hinzufügen einer Klasse zu einem Element</span><span class="sxs-lookup"><span data-stu-id="cd010-241">Add a class to an element</span></span>  

<span data-ttu-id="cd010-242">Führen Sie die folgenden Aktionen aus, um einem Element eine Klasse hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd010-242">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="cd010-243">[Wählen Sie das Element](#select-an-element) in der **DOM-Struktur**aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-243">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="cd010-244">Wählen Sie **CLS**aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-244">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="cd010-245">Geben Sie den Namen der Klasse in das Textfeld **neue Klasse hinzufügen** ein.</span><span class="sxs-lookup"><span data-stu-id="cd010-245">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="cd010-246">Wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cd010-246">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Der Bereich "Element Klassen"" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="cd010-248">Der Bereich " **Element Klassen** "</span><span class="sxs-lookup"><span data-stu-id="cd010-248">The **Element Classes** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="cd010-249">Umschalten einer Klasse</span><span class="sxs-lookup"><span data-stu-id="cd010-249">Toggle a class</span></span>  

<span data-ttu-id="cd010-250">Führen Sie die folgenden Aktionen aus, um eine Klasse für ein Element zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="cd010-250">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="cd010-251">[Wählen Sie das Element](#select-an-element) in der **DOM-Struktur**aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-251">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="cd010-252">Öffnen Sie den Bereich **Element Klassen** .</span><span class="sxs-lookup"><span data-stu-id="cd010-252">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="cd010-253">Weitere Informationen finden Sie unter [Hinzufügen einer Klasse zu einem Element](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="cd010-253">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="cd010-254">Unter dem Textfeld " **neue Klasse hinzufügen** " befinden sich alle Klassen, die auf das jeweilige Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd010-254">Below the **Add New Class** text box are all of the classes that are being applied to the specific element.</span></span>  
1.  <span data-ttu-id="cd010-255">Aktivieren oder deaktivieren Sie das Kontrollkästchen neben der Klasse, die Sie aktivieren oder deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cd010-255">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="cd010-256">Hinzufügen einer Stilregel</span><span class="sxs-lookup"><span data-stu-id="cd010-256">Add a style rule</span></span>  

<span data-ttu-id="cd010-257">Führen Sie die folgenden Aktionen aus, um eine neue Stilregel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd010-257">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="cd010-258">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="cd010-258">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="cd010-259">Wählen Sie **neue Formatvorlagenregel** \ ( ![ neue Stilregel ][ImageNewStyleRuleIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-259">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\).</span></span>  <span data-ttu-id="cd010-260">DevTools fügt eine neue Regel unterhalb der **Element. Style** -Regel ein.</span><span class="sxs-lookup"><span data-stu-id="cd010-260">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="cd010-261">In der folgenden Abbildung fügt devtools die Stilregel hinzu, `h1.devsite-page-title` nachdem Sie eine **neue Stilregel**ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="cd010-261">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Hinzufügen einer neuen Stilregel" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="cd010-263">Hinzufügen einer neuen Stilregel</span><span class="sxs-lookup"><span data-stu-id="cd010-263">Add a new style rule</span></span>  
:::image-end:::  

#### <span data-ttu-id="cd010-264">Auswählen des Stylesheets, dem eine Regel hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="cd010-264">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="cd010-265">Wenn Sie [eine neue Stilregel hinzufügen](#add-a-style-rule)möchten, wählen Sie **neue** Stilregel aus, und halten Sie die Regel \ (neue Stilregel \) gedrückt, um ![ auszuwählen, ][ImageNewStyleRuleIcon] welchem Stylesheet die Stilregel hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd010-265">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Auswählen eines Stylesheets" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="cd010-267">Auswählen eines Stylesheets</span><span class="sxs-lookup"><span data-stu-id="cd010-267">Choose a stylesheet</span></span>  
:::image-end:::  

#### <span data-ttu-id="cd010-268">Hinzufügen einer Stilregel zu einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="cd010-268">Add a style rule to a specific location</span></span>  

<span data-ttu-id="cd010-269">Führen Sie die folgenden Aktionen aus, um einer bestimmten Position auf der Registerkarte **Formatvorlagen** eine Stilregel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd010-269">Complete the following actions to add a style rule to a specific location in the **Styles** tab.</span></span>  

1.  <span data-ttu-id="cd010-270">Zeigen Sie mit der Maus auf die Stilregel, die sich direkt darüber befindet, wo Sie die neue Stilregel hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="cd010-270">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="cd010-271">[Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="cd010-271">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="cd010-272">Wählen Sie **unter** \ (Stilregel ![ Einfügen unter \) die Option Stilregel einfügen aus ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="cd010-272">Choose **Insert Style Rule Below** \(![Insert Style Rule Below][ImageNewStyleRuleIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Einfügen einer Stilregel unten" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="cd010-274">Einfügen einer Stilregel unten</span><span class="sxs-lookup"><span data-stu-id="cd010-274">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <span data-ttu-id="cd010-275">Anzeigen der Symbolleiste "Weitere Aktionen"</span><span class="sxs-lookup"><span data-stu-id="cd010-275">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="cd010-276">Auf der Symbolleiste **Weitere Aktionen** können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="cd010-276">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="cd010-277">Fügen Sie eine Stilregel direkt unter die Regel ein, auf die Sie sich konzentrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cd010-277">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="cd010-278">Fügen `background-color` `color` `box-shadow` `text-shadow` Sie der Stilregel, auf die Sie sich konzentrieren, eine,-oder-Deklaration hinzu.</span><span class="sxs-lookup"><span data-stu-id="cd010-278">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="cd010-279">Führen Sie die folgenden Aktionen aus, um die Symbolleiste **Weitere Aktionen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cd010-279">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="cd010-280">Zeigen Sie auf der Registerkarte **Formatvorlagen** auf eine Stilregel.</span><span class="sxs-lookup"><span data-stu-id="cd010-280">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="cd010-281">**More Actions** `...` In der unteren rechten Ecke des Abschnitts Stilregel werden weitere Aktionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd010-281">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cd010-282">Zeigen Sie in der folgenden Abbildung auf die `.header-holder.has-default-focus` Stilregel, und **Weitere Aktionen** werden in der unteren rechten Ecke des Abschnitts Stilregel eingeblendet.</span><span class="sxs-lookup"><span data-stu-id="cd010-282">In the following figure, hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Weitere Aktionen anzeigen" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="cd010-284">**Weitere Aktionen** anzeigen \ ( `...` \)</span><span class="sxs-lookup"><span data-stu-id="cd010-284">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cd010-285">Zeigen Sie auf **Weitere Aktionen** \ ( `...` \), um die oben genannten Aktionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cd010-285">Hover over **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cd010-286">Die **Regel "Stil einfügen" unterhalb** der Aktion wird nach dem Hovern auf **Weitere Aktionen**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd010-286">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Die Symbolleiste "Weitere Aktionen"" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="cd010-288">Die Symbolleiste " **Weitere Aktionen** "</span><span class="sxs-lookup"><span data-stu-id="cd010-288">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="cd010-289">Umschalten einer Deklaration</span><span class="sxs-lookup"><span data-stu-id="cd010-289">Toggle a declaration</span></span>  

<span data-ttu-id="cd010-290">Führen Sie die folllwoing-Aktionen aus, um eine einzelne Deklaration auf \ (oder aus \) umzuschalten.</span><span class="sxs-lookup"><span data-stu-id="cd010-290">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="cd010-291">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="cd010-291">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="cd010-292">Zeigen Sie im Bereich **Formatvorlagen** auf die Regel, die die Deklaration definiert.</span><span class="sxs-lookup"><span data-stu-id="cd010-292">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="cd010-293">Neben jeder Deklaration wird ein Kontrollkästchen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd010-293">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="cd010-294">Aktivieren Sie das Kontrollkästchen neben der Deklaration.</span><span class="sxs-lookup"><span data-stu-id="cd010-294">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="cd010-295">Wenn Sie eine Deklaration deaktivieren, wird Sie von devtools durchgestrichen, um anzugeben, dass Sie nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="cd010-295">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="cd010-296">In der folgenden Abbildung wurde die `margin-top` Eigenschaft für das aktuell ausgewählte Element deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="cd010-296">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Umschalten einer Deklaration" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="cd010-298">Umschalten einer Deklaration</span><span class="sxs-lookup"><span data-stu-id="cd010-298">Toggle a declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="cd010-299">Hinzufügen einer Hintergrundfarben Deklaration</span><span class="sxs-lookup"><span data-stu-id="cd010-299">Add a background-color declaration</span></span>  

<span data-ttu-id="cd010-300">Führen Sie die folgenden Aktionen aus, um einem Element eine Deklaration hinzuzufügen `background-color` .</span><span class="sxs-lookup"><span data-stu-id="cd010-300">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="cd010-301">Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `background-color` .</span><span class="sxs-lookup"><span data-stu-id="cd010-301">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="cd010-302">[Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="cd010-302">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="cd010-303">Wählen Sie **Hintergrundfarbe hinzufügen** \ ( ![ Hintergrundfarbe hinzufügen ][ImageAddBackgroundColorIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-303">Choose **Add Background Color** \(![Add Background Color][ImageAddBackgroundColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Hinzufügen einer Hintergrundfarbe" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="cd010-305">Hinzufügen einer Hintergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="cd010-305">Add Background Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="cd010-306">Hinzufügen einer Farb Deklaration</span><span class="sxs-lookup"><span data-stu-id="cd010-306">Add a color declaration</span></span>  

<span data-ttu-id="cd010-307">Führen Sie die folgenden Aktionen aus, um einem Element eine Deklaration hinzuzufügen `color` .</span><span class="sxs-lookup"><span data-stu-id="cd010-307">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="cd010-308">Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `color` .</span><span class="sxs-lookup"><span data-stu-id="cd010-308">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="cd010-309">[Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="cd010-309">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="cd010-310">Wählen Sie **Farbe hinzufügen** ( ![ Farbe hinzufügen ][ImageAddColorIcon] ) aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-310">Choose **Add Color** \(![Add Color][ImageAddColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Farbe hinzufügen" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="cd010-312">Farbe hinzufügen</span><span class="sxs-lookup"><span data-stu-id="cd010-312">Add Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="cd010-313">Hinzufügen einer Box-Shadow-Deklaration</span><span class="sxs-lookup"><span data-stu-id="cd010-313">Add a box-shadow declaration</span></span>  

<span data-ttu-id="cd010-314">Führen Sie die folgenden Aktionen aus, um einem Element eine Deklaration hinzuzufügen `box-shadow` .</span><span class="sxs-lookup"><span data-stu-id="cd010-314">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="cd010-315">Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `box-shadow` .</span><span class="sxs-lookup"><span data-stu-id="cd010-315">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="cd010-316">[Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="cd010-316">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="cd010-317">Wählen Sie " **Feld Schatten hinzufügen** " aus ![ ][ImageAddBoxShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="cd010-317">Choose **Add Box Shadow** \(![Add Box Shadow][ImageAddBoxShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Feld Schatten hinzufügen" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="cd010-319">Feld Schatten hinzufügen</span><span class="sxs-lookup"><span data-stu-id="cd010-319">Add Box Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="cd010-320">Hinzufügen einer Text-Shadow-Deklaration</span><span class="sxs-lookup"><span data-stu-id="cd010-320">Add a text-shadow declaration</span></span>  

<span data-ttu-id="cd010-321">Führen Sie die folgenden Aktionen aus, um einem Element eine Deklaration hinzuzufügen `text-shadow` .</span><span class="sxs-lookup"><span data-stu-id="cd010-321">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="cd010-322">Zeigen Sie mit der Maus auf die Stilregel, der Sie die Deklaration hinzufügen möchten `text-shadow` .</span><span class="sxs-lookup"><span data-stu-id="cd010-322">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="cd010-323">[Blenden Sie die Symbolleiste " **Weitere Aktionen** " ein](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="cd010-323">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="cd010-324">Wählen Sie **Text Schatten hinzufügen** \ ( ![ Text Schatten hinzufügen ][ImageAddTextShadowIcon] ) aus.</span><span class="sxs-lookup"><span data-stu-id="cd010-324">Choose **Add Text Shadow** \(![Add Text Shadow][ImageAddTextShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Hinzufügen von Text Schatten" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="cd010-326">Hinzufügen von Text Schatten</span><span class="sxs-lookup"><span data-stu-id="cd010-326">Add Text Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="cd010-327">Ändern von Farben mit der Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="cd010-327">Change colors with the Color Picker</span></span>  

<span data-ttu-id="cd010-328">Die **Farbauswahl** bietet eine GUI für Änderungen `color` und `background-color` Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="cd010-328">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="cd010-329">Führen Sie die folgenden Aktionen aus, um die **Farbauswahl**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cd010-329">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="cd010-330">[Wählen Sie ein Element aus](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="cd010-330">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="cd010-331">Suchen Sie auf der Registerkarte **Formatvorlagen** nach der `color` `background-color` oder ähnlichen Deklaration, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="cd010-331">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="cd010-332">Links vom `color` `background-color` oder ähnlichen Wert befindet sich ein kleines Quadrat, das eine Vorschau der Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="cd010-332">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cd010-333">In der folgenden Abbildung ist das kleine Quadrat links von `rgba(0, 0, 0, 0.7)` einer Vorschau dieser Farbe.</span><span class="sxs-lookup"><span data-stu-id="cd010-333">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Farbvorschau" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="cd010-335">Farbvorschau</span><span class="sxs-lookup"><span data-stu-id="cd010-335">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cd010-336">Wählen Sie die Vorschau aus, um die **Farbauswahl**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cd010-336">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Die Farbauswahl" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="cd010-338">Die **Farbauswahl**</span><span class="sxs-lookup"><span data-stu-id="cd010-338">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="cd010-339">Die folgende Abbildung und Listen beschreibt der einzelnen UI-Elemente der **Farbauswahl**.</span><span class="sxs-lookup"><span data-stu-id="cd010-339">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Die Farbauswahl mit Anmerkungen" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="cd010-341">Die **Farbauswahl**mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="cd010-341">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="cd010-342">1</span><span class="sxs-lookup"><span data-stu-id="cd010-342">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="cd010-343">Schattierungen</span><span class="sxs-lookup"><span data-stu-id="cd010-343">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="cd010-344">2</span><span class="sxs-lookup"><span data-stu-id="cd010-344">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="cd010-345">Pipette</span><span class="sxs-lookup"><span data-stu-id="cd010-345">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cd010-346">Weitere Informationen finden Sie unter [Beispiel für eine Farbe außerhalb der Seite mit der Pipette](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="cd010-346">For more information, see [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="cd010-347">3</span><span class="sxs-lookup"><span data-stu-id="cd010-347">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="cd010-348">In Zwischenablage kopieren</span><span class="sxs-lookup"><span data-stu-id="cd010-348">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cd010-349">Kopieren Sie den **Anzeigewert** in Ihre Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="cd010-349">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="cd010-350">4</span><span class="sxs-lookup"><span data-stu-id="cd010-350">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="cd010-351">Anzeigewert</span><span class="sxs-lookup"><span data-stu-id="cd010-351">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cd010-352">Die RGBA-, HSLA-oder Hex-Darstellung der Farbe.</span><span class="sxs-lookup"><span data-stu-id="cd010-352">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="cd010-353">5</span><span class="sxs-lookup"><span data-stu-id="cd010-353">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="cd010-354">Farb Palette</span><span class="sxs-lookup"><span data-stu-id="cd010-354">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cd010-355">Wählen Sie eines der Quadrate aus, um die Farbe in das Quadrat zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cd010-355">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="cd010-356">6</span><span class="sxs-lookup"><span data-stu-id="cd010-356">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="cd010-357">Farbton</span><span class="sxs-lookup"><span data-stu-id="cd010-357">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="cd010-358">7</span><span class="sxs-lookup"><span data-stu-id="cd010-358">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="cd010-359">Opacity</span><span class="sxs-lookup"><span data-stu-id="cd010-359">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="cd010-360">8</span><span class="sxs-lookup"><span data-stu-id="cd010-360">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="cd010-361">Anzeigewert-Umschalter</span><span class="sxs-lookup"><span data-stu-id="cd010-361">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cd010-362">Wechseln zwischen den RGBA-, HSLA-und Hex-Darstellungen der aktuellen Farbe</span><span class="sxs-lookup"><span data-stu-id="cd010-362">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="cd010-363">9</span><span class="sxs-lookup"><span data-stu-id="cd010-363">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="cd010-364">Farbpaletten-Umschalter</span><span class="sxs-lookup"><span data-stu-id="cd010-364">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cd010-365">Wechseln zwischen der [Material Design Palette][MaterialDesignColorSystem], einer benutzerdefinierten Palette oder einer Seitenfarben-Palette</span><span class="sxs-lookup"><span data-stu-id="cd010-365">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="cd010-366">DevTools generiert die Seiten Farbpalette basierend auf den Farben, die in ihren Stylesheets gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="cd010-366">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="cd010-367">Beispiel für eine Farbe auf der Seite mit der Pipette</span><span class="sxs-lookup"><span data-stu-id="cd010-367">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="cd010-368">Wenn Sie die **Farbauswahl**öffnen, ist die **Pipette** (Pipette ![ ][ImageEyedropperIcon] ) standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cd010-368">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper][ImageEyedropperIcon]\) is on by default.</span></span>  <span data-ttu-id="cd010-369">Führen Sie die folgenden Aktionen aus, um die ausgewählte Farbe auf eine andere Farbe auf der Seite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cd010-369">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="cd010-370">Zeigen Sie mit der Maus auf die Zielfarbe im Viewport.</span><span class="sxs-lookup"><span data-stu-id="cd010-370">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="cd010-371">Wählen Sie aus, um zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="cd010-371">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cd010-372">In der folgenden Abbildung zeigt die **Farbauswahl** einen aktuellen Farbwert von, der sich in der `rgba(0,0,0,0.7)` Nähe von schwarz befindet.</span><span class="sxs-lookup"><span data-stu-id="cd010-372">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="cd010-373">Die spezifische Farbe sollte auf die Version von Schwarz geändert werden, die aktuell im Viewport hervorgehoben ist, nachdem Sie Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="cd010-373">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Verwenden der Pipette" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="cd010-375">Verwenden der Pipette</span><span class="sxs-lookup"><span data-stu-id="cd010-375">Using the Eyedropper</span></span>  
    :::image-end:::  
    
<!-- image links -->  

[ImageAddBackgroundColorIcon]: ../media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: ../media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: ../media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: ../media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: ../media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: ../media/select-an-element-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevToolsCSSGetStarted]: ../css/index.md "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Hinzufügen eines PseudoState zu einer Klasse – erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Anzeigen der CSS für ein Element – erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Erzwingen von Microsoft Edge devtools in den Druckvorschau Modus (CSS-Druckmedientyp) | Microsoft docs"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Erstellen einer minimierte-Datei lesbar – JavaScript-Debug-Referenz | Microsoft docs"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Das Farbsystem – Material Design"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Das Feld Modell | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Auswahltypen – Spezifität | MDN"  

> [!NOTE]
> <span data-ttu-id="cd010-385">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd010-385">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cd010-386">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd010-386">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="cd010-388">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cd010-388">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

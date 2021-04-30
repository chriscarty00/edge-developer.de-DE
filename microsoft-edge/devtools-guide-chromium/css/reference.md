---
description: Entdecken Sie neue Workflows zum Anzeigen und Ändern von CSS in Microsoft Edge DevTools.
title: CSS-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: bddbf14e73f5c29bfd4757c9cd6d255f419c331f
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519331"
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

# <a name="css-reference"></a><span data-ttu-id="f601e-104">CSS-Referenz</span><span class="sxs-lookup"><span data-stu-id="f601e-104">CSS reference</span></span>  

<span data-ttu-id="f601e-105">Entdecken Sie neue Workflows in der folgenden umfassenden Referenz zu Microsoft Edge DevTools-Features im Zusammenhang mit dem Anzeigen und Ändern von CSS.</span><span class="sxs-lookup"><span data-stu-id="f601e-105">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="f601e-106">Um die Grundlagen zu erlernen, navigieren Sie zu [Erste Schritte mit dem Anzeigen und Ändern von CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="f601e-106">To learn the basics, navigate to [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted].</span></span>  

## <a name="choose-an-element"></a><span data-ttu-id="f601e-107">Auswählen eines Elements</span><span class="sxs-lookup"><span data-stu-id="f601e-107">Choose an element</span></span>  

<span data-ttu-id="f601e-108">Mit **dem Tool Elemente** von DevTools können Sie die CSS eines Elements gleichzeitig anzeigen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="f601e-108">The **Elements** tool of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="f601e-109">Das ausgewählte Element wird in der **DOM-Struktur hervorgehoben.**</span><span class="sxs-lookup"><span data-stu-id="f601e-109">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="f601e-110">Die Formatvorlagen des Elements werden im Bereich **Formatvorlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f601e-110">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="f601e-111">Navigieren Sie für ein Lernprogramm zu [Css für ein Element anzeigen.][DevToolsCSSGetStartedTutorial]</span><span class="sxs-lookup"><span data-stu-id="f601e-111">For a tutorial, navigate to [View the CSS for an element][DevToolsCSSGetStartedTutorial].</span></span>  

> [!NOTE]
> <span data-ttu-id="f601e-112">In der folgenden Abbildung ist das Element, das in der `h1` **DOM-Struktur** hervorgehoben ist, das ausgewählte Element.</span><span class="sxs-lookup"><span data-stu-id="f601e-112">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="f601e-113">Auf der rechten Seite werden die Formatvorlagen des Elements im Bereich **Formatvorlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f601e-113">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="f601e-114">Auf der linken Seite wird das Element im Viewport hervorgehoben, aber nur, weil die Maus derzeit in der **DOM-Struktur**auf das Element zeigt.</span><span class="sxs-lookup"><span data-stu-id="f601e-114">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Ein Beispiel für ein ausgewähltes Element" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="f601e-116">Ein Beispiel für ein ausgewähltes Element</span><span class="sxs-lookup"><span data-stu-id="f601e-116">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="f601e-117">Verwenden Sie eine der folgenden Aktionen, um ein Element auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f601e-117">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="f601e-118">Zeigen Sie in Ihrem Viewport auf das Element, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie **Überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="f601e-118">In your viewport, hover on the element, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
*   <span data-ttu-id="f601e-119">Wählen Sie in DevTools **Ein** Element auswählen \( Element auswählen ![ ](../media/select-an-element-icon.msft.png) \) oder `Control` + `Shift` + `C` \(Windows, Linux\) oder `Command` + `Shift` + `C` \(macOS\) aus, und wählen Sie dann das Element im Viewport aus.</span><span class="sxs-lookup"><span data-stu-id="f601e-119">In DevTools, choose **Select an element** \(![Select an element](../media/select-an-element-icon.msft.png)\) or select `Control`+`Shift`+`C` \(Windows, Linux\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="f601e-120">Wählen Sie in DevTools das Element in der **DOM-Struktur aus.**</span><span class="sxs-lookup"><span data-stu-id="f601e-120">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="f601e-121">Führen Sie in DevTools eine Abfrage wie in der Konsole aus, zeigen Sie auf das Ergebnis, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste auf\), und wählen Sie im Bereich Elemente anzeigen `document.querySelector('p')` **aus.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f601e-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel**.</span></span>  

## <a name="view-css"></a><span data-ttu-id="f601e-122">Anzeigen von CSS</span><span class="sxs-lookup"><span data-stu-id="f601e-122">View CSS</span></span>  

### <a name="view-the-external-stylesheet-where-a-rule-is-defined"></a><span data-ttu-id="f601e-123">Anzeigen des externen Stylesheets, in dem eine Regel definiert ist</span><span class="sxs-lookup"><span data-stu-id="f601e-123">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="f601e-124">Wählen Sie **im Bereich** Formatvorlagen den Link neben einer CSS-Regel aus, um das externe Stylesheet zu öffnen, das die Regel definiert.</span><span class="sxs-lookup"><span data-stu-id="f601e-124">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  <span data-ttu-id="f601e-125">Das Stylesheet wird im **Editorbereich** des Tools **Quellen** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f601e-125">The stylesheet opens in the **Editor** pane of the **Sources** tool.</span></span>  

<span data-ttu-id="f601e-126">Wenn das Stylesheet minified ist, wählen Sie die Schaltfläche **Format** \( Format \) am unteren Rand ![ des ](../media/format-icon.msft.png) **Editorbereichs** aus.</span><span class="sxs-lookup"><span data-stu-id="f601e-126">If the stylesheet is minified, choose the **Format** \(![Format](../media/format-icon.msft.png)\) button, at the bottom of the **Editor** pane.</span></span>  <span data-ttu-id="f601e-127">Weitere Informationen finden Sie unter [Reformat a minified JavaScript file with pretty-print][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="f601e-127">For more information, navigate to [Reformat a minified JavaScript file with pretty-print][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="f601e-128">In der folgenden Abbildung werden Sie nach der Auswahl zu Zeile 2 von `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` übernommen, in der die `.content h1:first-of-type` CSS-Regel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f601e-128">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Anzeigen des Stylesheets, in dem eine Regel definiert ist" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="f601e-130">Anzeigen des Stylesheets, in dem eine Regel definiert ist</span><span class="sxs-lookup"><span data-stu-id="f601e-130">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <a name="view-only-the-css-that-is-actually-applied-to-an-element"></a><span data-ttu-id="f601e-131">Nur das CSS anzeigen, das tatsächlich auf ein Element angewendet wird</span><span class="sxs-lookup"><span data-stu-id="f601e-131">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="f601e-132">Im **Bereich** Formatvorlagen werden alle Regeln angezeigt, die für ein Element gelten, einschließlich überschriebener Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="f601e-132">The **Styles** panel shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="f601e-133">Wenn Sie nicht an überschriebenen Deklarationen interessiert sind, zeigen Sie im **Bereich Berechnet** nur das CSS an, das tatsächlich auf ein Element angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f601e-133">When you are not interested in overridden declarations, use the **Computed** panel to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="f601e-134">[Wählen Sie ein Element aus.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="f601e-134">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="f601e-135">Navigieren Sie im **Tool** Elemente zum **Berechneten** Bereich.</span><span class="sxs-lookup"><span data-stu-id="f601e-135">Navigate to the **Computed** panel in the **Elements** tool.</span></span>  

> [!NOTE]
> <span data-ttu-id="f601e-136">In einem breiten DevTools-Fenster ist der **Berechnete** Bereich nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f601e-136">On a wide DevTools window, the **Computed** panel does not exist.</span></span>  <span data-ttu-id="f601e-137">Der Inhalt des **Berechneten** Panels wird im **Formatvorlagenbereich** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f601e-137">The contents of the **Computed** panel are shown on the **Styles** panel.</span></span>  

<span data-ttu-id="f601e-138">Geerbte Eigenschaften sind undurchsichtig.</span><span class="sxs-lookup"><span data-stu-id="f601e-138">Inherited properties are opaque.</span></span>  <span data-ttu-id="f601e-139">Aktivieren Sie zum Anzeigen aller geerbten Werte das **Kontrollkästchen Alle** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f601e-139">To display all inherited values, select the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="f601e-140">In der folgenden Abbildung zeigt der **Berechnete** Bereich die CSS-Eigenschaften, die auf das aktuell ausgewählte Element angewendet `h1` werden.</span><span class="sxs-lookup"><span data-stu-id="f601e-140">In the following figure, the **Computed** panel shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Der Berechnete Bereich" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="f601e-142">Der **Berechnete** Bereich</span><span class="sxs-lookup"><span data-stu-id="f601e-142">The **Computed** panel</span></span>  
:::image-end:::  

### <a name="view-css-properties-in-alphabetical-order"></a><span data-ttu-id="f601e-143">Anzeigen von CSS-Eigenschaften in alphabetischer Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="f601e-143">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="f601e-144">Verwenden Sie den **Berechneten** Bereich.</span><span class="sxs-lookup"><span data-stu-id="f601e-144">Use the **Computed** panel.</span></span>  <span data-ttu-id="f601e-145">Navigieren Sie [zu Nur css anzeigen, das tatsächlich auf ein Element angewendet wird.](#view-only-the-css-that-is-actually-applied-to-an-element)</span><span class="sxs-lookup"><span data-stu-id="f601e-145">Navigate to [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <a name="view-inherited-css-properties"></a><span data-ttu-id="f601e-146">Anzeigen geerbter CSS-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f601e-146">View inherited CSS properties</span></span>  

<span data-ttu-id="f601e-147">Aktivieren Sie **das Kontrollkästchen Alle** anzeigen im **Bereich Berechnet.**</span><span class="sxs-lookup"><span data-stu-id="f601e-147">Check the **Show All** checkbox in the **Computed** panel.</span></span>  <span data-ttu-id="f601e-148">Navigieren Sie [zu Nur css anzeigen, das tatsächlich auf ein Element angewendet wird.](#view-only-the-css-that-is-actually-applied-to-an-element)</span><span class="sxs-lookup"><span data-stu-id="f601e-148">Navigate to [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <a name="view-the-box-model-for-an-element"></a><span data-ttu-id="f601e-149">Anzeigen des Boxmodells für ein Element</span><span class="sxs-lookup"><span data-stu-id="f601e-149">View the box model for an element</span></span>  

<span data-ttu-id="f601e-150">Zum Anzeigen [des Feldmodells][MDNBoxModel] eines Elements navigieren Sie zum **Formatvorlagenbereich.**</span><span class="sxs-lookup"><span data-stu-id="f601e-150">To view [the box model][MDNBoxModel] of an element, navigate to the **Styles** panel.</span></span>  <span data-ttu-id="f601e-151">Wenn Ihr DevTools-Fenster schmal ist, befindet sich das **Box Model-Diagramm** am unteren Rand des Panels.</span><span class="sxs-lookup"><span data-stu-id="f601e-151">If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the panel.</span></span>  

<span data-ttu-id="f601e-152">Wählen Und bearbeiten Sie einen Wert, um einen Wert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f601e-152">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="f601e-153">In der folgenden Abbildung zeigt das \*\*\*\* **Diagramm Feldmodell** im Bereich Formatvorlagen das Feldmodell für das aktuell ausgewählte `h1` Element.</span><span class="sxs-lookup"><span data-stu-id="f601e-153">In the following figure, the **Box Model** diagram in the **Styles** panel shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Das Diagramm Boxmodell" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="f601e-155">Das **Diagramm "Boxmodell"**</span><span class="sxs-lookup"><span data-stu-id="f601e-155">The **Box Model** diagram</span></span>  
:::image-end:::  

### <a name="search-and-filter-the-css-of-an-element"></a><span data-ttu-id="f601e-156">Suchen und Filtern der CSS eines Elements</span><span class="sxs-lookup"><span data-stu-id="f601e-156">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="f601e-157">Verwenden Sie **das Textfeld Filter** in den **Feldern Formatvorlagen** und **Berechnet,** um nach bestimmten CSS-Eigenschaften oder -Werten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f601e-157">Use the **Filter** text box on the **Styles** and **Computed** panels to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="f601e-158">Aktivieren Sie das Kontrollkästchen Alle anzeigen, um auch geerbte Eigenschaften im **Berechneten** Bereich **zu** durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="f601e-158">To also search inherited properties in the **Computed** panel, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="f601e-159">In der folgenden Abbildung wird der **Formatvorlagenbereich** so gefiltert, dass nur Regeln angezeigt werden, die die Suchabfrage `color` enthalten.</span><span class="sxs-lookup"><span data-stu-id="f601e-159">In the following figure, the **Styles** panel is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtern des Formatvorlagenbereichs" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="f601e-161">Filtern des **Formatvorlagenbereichs**</span><span class="sxs-lookup"><span data-stu-id="f601e-161">Filter the **Styles** panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="f601e-162">In der folgenden Abbildung wird der **Berechnete** Bereich so gefiltert, dass nur Deklarationen angezeigt werden, die die Suchabfrage `100%` enthalten.</span><span class="sxs-lookup"><span data-stu-id="f601e-162">In the following figure, the **Computed** panel is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtern des berechneten Panels" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="f601e-164">Filtern des **berechneten Panels**</span><span class="sxs-lookup"><span data-stu-id="f601e-164">Filter the **Computed** panel</span></span>  
:::image-end:::  

### <a name="toggle-a-pseudo-class"></a><span data-ttu-id="f601e-165">Umschalten einer Pseudoklasse</span><span class="sxs-lookup"><span data-stu-id="f601e-165">Toggle a pseudo-class</span></span>  

<span data-ttu-id="f601e-166">Führen Sie die folgenden Aktionen aus, um eine Pseudoklasse wie `:active` , `:focus` , oder `:hover` umzuschalten. `:visited`</span><span class="sxs-lookup"><span data-stu-id="f601e-166">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="f601e-167">[Wählen Sie ein Element aus.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="f601e-167">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="f601e-168">Navigieren Sie **im Tool** Elemente zum **Formatvorlagenbereich.**</span><span class="sxs-lookup"><span data-stu-id="f601e-168">On the **Elements** tool, navigate to the **Styles** panel.</span></span>  
1.  <span data-ttu-id="f601e-169">Wählen **Sie :hov**aus.</span><span class="sxs-lookup"><span data-stu-id="f601e-169">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="f601e-170">Überprüfen Sie die Pseudoklasse, die Sie aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f601e-170">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="f601e-171">In der folgenden Abbildung umschalten Sie die `:hover` Pseudoklasse.</span><span class="sxs-lookup"><span data-stu-id="f601e-171">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="f601e-172">Vergewissern Sie sich im viewport, dass die Deklaration auf das Element angewendet wird, auch wenn das Element nicht tatsächlich über `background-color: cornflowerblue` das Element bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="f601e-172">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Umschalten der Pseudoklasse :hover" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="f601e-174">Umschalten `:hover` der Pseudoklasse</span><span class="sxs-lookup"><span data-stu-id="f601e-174">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="f601e-175">Navigieren Sie für ein interaktives Lernprogramm zu [Hinzufügen eines Pseudozustands zu einer Klasse][DevToolsCSSGetStartedAddPseudoState].</span><span class="sxs-lookup"><span data-stu-id="f601e-175">For an interactive tutorial, navigate to [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <a name="view-a-page-in-print-mode"></a><span data-ttu-id="f601e-176">Anzeigen einer Seite im Druckmodus</span><span class="sxs-lookup"><span data-stu-id="f601e-176">View a page in print mode</span></span>  

<span data-ttu-id="f601e-177">Führen Sie die folgenden Aktionen aus, um eine Seite im Druckmodus zu sehen.</span><span class="sxs-lookup"><span data-stu-id="f601e-177">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="f601e-178">[Öffnen Sie das Befehlsmenü][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="f601e-178">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="f601e-179">Beginnen Sie mit der `Rendering` Eingabe und wählen Sie `Show Rendering` aus.</span><span class="sxs-lookup"><span data-stu-id="f601e-179">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="f601e-180">Wählen Sie **im Dropdownmenü Emulieren von CSS-Medien** die Option **Drucken aus.**</span><span class="sxs-lookup"><span data-stu-id="f601e-180">For the **Emulate CSS Media** dropdown, choose **print**.</span></span>  

### <a name="view-used-and-unused-css-with-the-coverage-tool"></a><span data-ttu-id="f601e-181">Anzeigen verwendeter und nicht verwendeter CSS mit dem Tool "Abdeckung"</span><span class="sxs-lookup"><span data-stu-id="f601e-181">View used and unused CSS with the Coverage tool</span></span>  

<span data-ttu-id="f601e-182">Das **Coverage-Tool** zeigt, welche CSS eine Seite tatsächlich verwendet.</span><span class="sxs-lookup"><span data-stu-id="f601e-182">The **Coverage** tool shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="f601e-183">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, während DevTools [][DevToolsCommandMenu]im Fokus steht, um das Befehlsmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f601e-183">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="f601e-184">Beginnen Sie mit der `coverage` Eingabe und wählen Sie Abdeckung anzeigen **aus.**</span><span class="sxs-lookup"><span data-stu-id="f601e-184">Start typing `coverage` and choose **Show Coverage**.</span></span>  <span data-ttu-id="f601e-185">Das **Abdeckungstool** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f601e-185">The **Coverage** tool appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Öffnen des Coverage-Tools über das Befehlsmenü" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="f601e-187">Öffnen Sie **das Tool** "Abdeckung" im **Befehlsmenü.**</span><span class="sxs-lookup"><span data-stu-id="f601e-187">Open the **Coverage** tool from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Das Tool Abdeckung" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="f601e-189">Das **Tool "Abdeckung"**</span><span class="sxs-lookup"><span data-stu-id="f601e-189">The **Coverage** tool</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="f601e-190">Wählen **Sie Die Instrumentierungsabdeckung starten aus, und aktualisieren Sie die Seite** \( Starten Sie die ![ Instrumentierungsabdeckung, und aktualisieren Sie die Seite ](../media/refresh-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="f601e-190">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page](../media/refresh-icon.msft.png)\).</span></span>  <span data-ttu-id="f601e-191">Die Seite wird aktualisiert, und das **Coverage-Tool** bietet eine Übersicht darüber, wie viel CSS \(und JavaScript\) aus jeder Datei verwendet wird, die der Browser lädt.</span><span class="sxs-lookup"><span data-stu-id="f601e-191">The page refreshes and the **Coverage** tool provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="f601e-192">Grün steht für verwendete CSS.</span><span class="sxs-lookup"><span data-stu-id="f601e-192">Green represents used CSS.</span></span>  <span data-ttu-id="f601e-193">Rot steht für nicht verwendete CSS.</span><span class="sxs-lookup"><span data-stu-id="f601e-193">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Eine Übersicht darüber, wie viel CSS (und JavaScript) verwendet und nicht verwendet wird" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="f601e-195">Eine Übersicht darüber, wie viel CSS \(und JavaScript\) verwendet und nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="f601e-195">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="f601e-196">Wählen Sie eine CSS-Datei aus, um eine zeilenweise Aufschlüsselung der verwendeten CSS-Dateien anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="f601e-196">To display a line-by-line breakdown of what CSS is used, choose a CSS file.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f601e-197">In der folgenden Abbildung werden die Zeilen 145 bis 147 und 149 bis 151 nicht verwendet, während die Zeilen `b66bc881.site-ltr.css` 163 bis 166 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f601e-197">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Eine zeilenweise Aufschlüsselung der verwendeten und nicht verwendeten CSS" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="f601e-199">Eine zeilenweise Aufschlüsselung der verwendeten und nicht verwendeten CSS</span><span class="sxs-lookup"><span data-stu-id="f601e-199">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <a name="force-print-preview-mode"></a><span data-ttu-id="f601e-200">Erzwingen des Druckvorschaumodus</span><span class="sxs-lookup"><span data-stu-id="f601e-200">Force print preview mode</span></span>  

<span data-ttu-id="f601e-201">Navigieren Sie [zu Erzwingen von DevTools in den Druckvorschaumodus.][DevToolsCssPrintPreview]</span><span class="sxs-lookup"><span data-stu-id="f601e-201">Navigate to [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <a name="change-css"></a><span data-ttu-id="f601e-202">Ändern von CSS</span><span class="sxs-lookup"><span data-stu-id="f601e-202">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <a name="add-a-css-declaration-to-an-element"></a><span data-ttu-id="f601e-203">Hinzufügen einer CSS-Deklaration zu einem Element</span><span class="sxs-lookup"><span data-stu-id="f601e-203">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="f601e-204">Die Reihenfolge der Deklarationen wirkt sich darauf aus, wie ein Element formatiert wird. Verwenden Sie die folgende Liste, um Deklarationen auf unterschiedliche Weise hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f601e-204">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="f601e-205">[Fügen Sie eine Inlinedeklaration hinzu.](#add-an-inline-declaration)</span><span class="sxs-lookup"><span data-stu-id="f601e-205">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="f601e-206">Entspricht dem Hinzufügen `style` eines Attributs zum HTML eines Elements.</span><span class="sxs-lookup"><span data-stu-id="f601e-206">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="f601e-207">[Fügen Sie einer Formatvorlageregel eine Deklaration hinzu.](#add-a-declaration-to-a-style-rule)</span><span class="sxs-lookup"><span data-stu-id="f601e-207">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="f601e-208">Welchen Workflow sollten Sie verwenden?</span><span class="sxs-lookup"><span data-stu-id="f601e-208">What workflow should you use?</span></span>** <span data-ttu-id="f601e-209">In den meisten Szenarien möchten Sie wahrscheinlich den Inlinedeklarationsworkflow verwenden.</span><span class="sxs-lookup"><span data-stu-id="f601e-209">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="f601e-210">Inlinedeklarationen haben eine höhere Spezifizität als externe, sodass der Inlineworkflow sicherstellt, dass die Änderungen in Ihrem erwarteten Element wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="f601e-210">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="f601e-211">Weitere Informationen zur Spezifizität finden Sie unter [Selector Types][MDNSelectorTypes].</span><span class="sxs-lookup"><span data-stu-id="f601e-211">For more information about specificity, navigate to [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="f601e-212">Wenn Sie Formatvorlagen des Elements debuggen und speziell testen müssen, was geschieht, wenn eine Deklaration an verschiedenen Stellen definiert ist, verwenden Sie den anderen Workflow.</span><span class="sxs-lookup"><span data-stu-id="f601e-212">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <a name="add-an-inline-declaration"></a><span data-ttu-id="f601e-213">Hinzufügen einer Inlinedeklaration</span><span class="sxs-lookup"><span data-stu-id="f601e-213">Add an inline declaration</span></span>  

<span data-ttu-id="f601e-214">Führen Sie die folgenden Aktionen aus, um eine Inlinedeklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f601e-214">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="f601e-215">[Wählen Sie ein Element aus.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="f601e-215">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="f601e-216">Wählen Sie **im Bereich** Formatvorlagen zwischen den Klammern des **Abschnitts element.style** aus.</span><span class="sxs-lookup"><span data-stu-id="f601e-216">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="f601e-217">Der Cursor konzentriert sich, sodass Sie Text eingeben können.</span><span class="sxs-lookup"><span data-stu-id="f601e-217">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="f601e-218">Geben Sie einen Eigenschaftennamen ein, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="f601e-218">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="f601e-219">Geben Sie einen gültigen Wert für diese Eigenschaft ein, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="f601e-219">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="f601e-220">Überprüfen Sie **in der DOM-Struktur,** ob dem Element ein `style` Attribut hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f601e-220">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="f601e-221">In der folgenden Abbildung wurden `margin-top` die Eigenschaften und auf das ausgewählte Element `background-color` angewendet.</span><span class="sxs-lookup"><span data-stu-id="f601e-221">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="f601e-222">Überprüfen Sie **in der DOM-Struktur,** ob die Deklarationen im `style` Attribut für ein Element enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f601e-222">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Hinzufügen von Inlinedeklarationen" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="f601e-224">Hinzufügen von Inlinedeklarationen</span><span class="sxs-lookup"><span data-stu-id="f601e-224">Add inline declarations</span></span>  
:::image-end:::  

#### <a name="add-a-declaration-to-a-style-rule"></a><span data-ttu-id="f601e-225">Hinzufügen einer Deklaration zu einer Formatvorlageregel</span><span class="sxs-lookup"><span data-stu-id="f601e-225">Add a declaration to a style rule</span></span>  

<span data-ttu-id="f601e-226">Führen Sie die folgenden Aktionen aus, um einer vorhandenen Formatvorlageregel eine Deklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f601e-226">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="f601e-227">[Wählen Sie ein Element aus.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="f601e-227">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="f601e-228">Wählen Sie **im Bereich** Formatvorlagen zwischen den Klammern der Formatvorlagenregel aus, der Sie die Deklaration hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="f601e-228">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="f601e-229">Der Cursor konzentriert sich, sodass Sie Text eingeben können.</span><span class="sxs-lookup"><span data-stu-id="f601e-229">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="f601e-230">Geben Sie einen Eigenschaftennamen ein, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="f601e-230">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="f601e-231">Geben Sie einen gültigen Wert für diese Eigenschaft ein, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="f601e-231">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Hinzufügen einer Deklaration zu einer Formatvorlageregel" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="f601e-233">Hinzufügen der `border-bottom-style:groove` Deklaration zu einer Formatvorlageregel</span><span class="sxs-lookup"><span data-stu-id="f601e-233">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <a name="change-a-declaration-name-or-value"></a><span data-ttu-id="f601e-234">Ändern eines Deklarationsnamens oder -werts</span><span class="sxs-lookup"><span data-stu-id="f601e-234">Change a declaration name or value</span></span>  

<span data-ttu-id="f601e-235">Wählen Und bearbeiten Sie den Namen oder Wert einer Deklaration, um sie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f601e-235">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="f601e-236">Für Verknüpfungen zum schnellen Inkrementieren oder Dekrementieren eines Werts durch , , oder Einheiten navigieren Sie zu Ändern von `0.1` `1` `10` `100` [Deklarationswerte mit Tastenkombinationen](#change-declaration-values-with-keyboard-shortcuts).</span><span class="sxs-lookup"><span data-stu-id="f601e-236">For shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units, navigate to [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts).</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Ändern des Werts einer Deklaration" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="f601e-238">Ändern des Werts der `border-bottom-style` Deklaration</span><span class="sxs-lookup"><span data-stu-id="f601e-238">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <a name="change-declaration-values-with-keyboard-shortcuts"></a><span data-ttu-id="f601e-239">Ändern von Deklarationswerten mit Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="f601e-239">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="f601e-240">Beim Bearbeiten des Werts einer Deklaration können Sie die folgenden Tastenkombinationen verwenden, um den Wert um einen bestimmten Betrag zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="f601e-240">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="f601e-241">Wählen `Alt` + `Up` Sie \(Windows, Linux\) oder `Option` + `Up` \(macOS\) aus, um um zu `0.1` erhöhen.</span><span class="sxs-lookup"><span data-stu-id="f601e-241">Select `Alt`+`Up` \(Windows, Linux\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="f601e-242">Wählen `Up` Sie diese Option aus, um den Wert durch oder durch zu ändern, wenn sich der aktuelle Wert zwischen und `1` `0.1` `-1` `1` befindet.</span><span class="sxs-lookup"><span data-stu-id="f601e-242">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="f601e-243">Wählen `Shift` + `Up` Sie aus, um um zu `10` erhöhen.</span><span class="sxs-lookup"><span data-stu-id="f601e-243">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="f601e-244">Wählen `Shift` + `Page Up` Sie \(Windows, Linux\) oder `Shift` + `Command` + `Up` \(macOS\) aus, um den Wert um zu `100` erhöhen.</span><span class="sxs-lookup"><span data-stu-id="f601e-244">Select `Shift`+`Page Up` \(Windows, Linux\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="f601e-245">Die Dekrementierung funktioniert ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="f601e-245">Decrementing also works.</span></span>  <span data-ttu-id="f601e-246">Ersetzen Sie einfach jede oben `Up` genannte Instanz durch `Down` .</span><span class="sxs-lookup"><span data-stu-id="f601e-246">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <a name="add-a-class-to-an-element"></a><span data-ttu-id="f601e-247">Hinzufügen einer Klasse zu einem Element</span><span class="sxs-lookup"><span data-stu-id="f601e-247">Add a class to an element</span></span>  

<span data-ttu-id="f601e-248">Führen Sie die folgenden Aktionen aus, um einem Element eine Klasse hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f601e-248">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="f601e-249">[Wählen Sie das Element](#choose-an-element) in der **DOM-Struktur aus.**</span><span class="sxs-lookup"><span data-stu-id="f601e-249">[Select the element](#choose-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="f601e-250">Wählen **Sie .cls**aus.</span><span class="sxs-lookup"><span data-stu-id="f601e-250">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="f601e-251">Geben Sie den Namen der Klasse in das Textfeld **Neue Klasse** hinzufügen ein.</span><span class="sxs-lookup"><span data-stu-id="f601e-251">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="f601e-252">Wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="f601e-252">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Der Bereich Elementklassen" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="f601e-254">Der **Bereich Elementklassen**</span><span class="sxs-lookup"><span data-stu-id="f601e-254">The **Element Classes** pane</span></span>  
:::image-end:::  

### <a name="toggle-a-class"></a><span data-ttu-id="f601e-255">Umschalten einer Klasse</span><span class="sxs-lookup"><span data-stu-id="f601e-255">Toggle a class</span></span>  

<span data-ttu-id="f601e-256">Führen Sie die folgenden Aktionen aus, um eine Klasse für ein Element zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f601e-256">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="f601e-257">[Wählen Sie das Element](#choose-an-element) in der **DOM-Struktur aus.**</span><span class="sxs-lookup"><span data-stu-id="f601e-257">[Select the element](#choose-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="f601e-258">Öffnen Sie den **Bereich Elementklassen.**</span><span class="sxs-lookup"><span data-stu-id="f601e-258">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="f601e-259">Navigieren Sie [zu Hinzufügen einer Klasse zu einem Element](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="f601e-259">Navigate to [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="f601e-260">Unterhalb des **Textfelds Neue Klasse** hinzufügen werden alle Klassen auf das spezifische Element angewendet.</span><span class="sxs-lookup"><span data-stu-id="f601e-260">Below the **Add New Class** text box are all of the classes applied to the specific element.</span></span>  
1.  <span data-ttu-id="f601e-261">Aktivieren Sie das Kontrollkästchen neben der Klasse, die Sie aktivieren oder deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f601e-261">Toggle the checkbox next to the class that you want to turn on or off.</span></span>  

### <a name="add-a-style-rule"></a><span data-ttu-id="f601e-262">Hinzufügen einer Formatvorlageregel</span><span class="sxs-lookup"><span data-stu-id="f601e-262">Add a style rule</span></span>  

<span data-ttu-id="f601e-263">Führen Sie die folgenden Aktionen aus, um eine neue Formatvorlageregel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f601e-263">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="f601e-264">[Wählen Sie ein Element aus.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="f601e-264">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="f601e-265">Wählen **Sie Neue Formatvorlageregel** \( ![ Neue Formatvorlageregel ](../media/new-style-rule-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="f601e-265">Choose **New Style Rule** \(![New Style Rule](../media/new-style-rule-icon.msft.png)\).</span></span>  <span data-ttu-id="f601e-266">DevTools fügt eine neue Regel unter der **element.style-Regel** ein.</span><span class="sxs-lookup"><span data-stu-id="f601e-266">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="f601e-267">In der folgenden Abbildung fügt DevTools die `h1.devsite-page-title` Formatvorlageregel hinzu, nachdem Sie **Neue Formatvorlageregel auswählen.**</span><span class="sxs-lookup"><span data-stu-id="f601e-267">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Hinzufügen einer neuen Formatvorlageregel" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="f601e-269">Hinzufügen einer neuen Formatvorlageregel</span><span class="sxs-lookup"><span data-stu-id="f601e-269">Add a new style rule</span></span>  
:::image-end:::  

#### <a name="choose-which-stylesheet-to-add-a-rule-to"></a><span data-ttu-id="f601e-270">Auswählen des Stylesheets, dem eine Regel hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="f601e-270">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="f601e-271">Wenn [Sie eine neue Formatvorlageregel hinzufügen,](#add-a-style-rule)wählen Sie Neue Formatvorlageregel \( Neue Formatvorlageregel \) aus, und halten Sie diese fest, um zu wählen, zu welchem Stylesheet die \*\*\*\* ![ ](../media/new-style-rule-icon.msft.png) Formatvorlageregel hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f601e-271">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule](../media/new-style-rule-icon.msft.png)\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Auswählen eines Stylesheets" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="f601e-273">Auswählen eines Stylesheets</span><span class="sxs-lookup"><span data-stu-id="f601e-273">Choose a stylesheet</span></span>  
:::image-end:::  

#### <a name="add-a-style-rule-to-a-specific-location"></a><span data-ttu-id="f601e-274">Hinzufügen einer Formatvorlageregel zu einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="f601e-274">Add a style rule to a specific location</span></span>  

<span data-ttu-id="f601e-275">Führen Sie die folgenden Aktionen aus, um einer bestimmten Position im Formatvorlagenbereich eine **Formatregel hinzuzufügen.**</span><span class="sxs-lookup"><span data-stu-id="f601e-275">Complete the following actions to add a style rule to a specific location in the **Styles** panel.</span></span>  

1.  <span data-ttu-id="f601e-276">Zeigen Sie auf die Formatvorlageregel, die sich direkt über der Stelle befindet, an der Sie die neue Formatvorlageregel hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="f601e-276">Hover on the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="f601e-277">[Zeigen Sie die **Symbolleiste Weitere Aktionen** an.](#reveal-the-more-actions-toolbar)</span><span class="sxs-lookup"><span data-stu-id="f601e-277">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="f601e-278">Wählen **Sie Formatvorlageregel einfügen unten** \( ![ Formatvorlageregel einfügen unten symbol ](../media/new-style-rule-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="f601e-278">Choose **Insert Style Rule Below** \(![Insert Style Rule Below icon](../media/new-style-rule-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Einfügen von Formatvorlageregel unten" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="f601e-280">Einfügen von Formatvorlageregel unten</span><span class="sxs-lookup"><span data-stu-id="f601e-280">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <a name="reveal-the-more-actions-toolbar"></a><span data-ttu-id="f601e-281">Anzeigen der Symbolleiste "Weitere Aktionen"</span><span class="sxs-lookup"><span data-stu-id="f601e-281">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="f601e-282">Mit **der Symbolleiste** Weitere Aktionen können Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="f601e-282">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="f601e-283">Fügen Sie eine Formatvorlageregel direkt unterhalb der Formatvorlage ein, auf die Sie sich konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="f601e-283">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="f601e-284">Fügen Sie der Formatregel, auf die Sie sich konzentrieren, eine , , oder `background-color` `color` `box-shadow` `text-shadow` -Deklaration hinzu.</span><span class="sxs-lookup"><span data-stu-id="f601e-284">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="f601e-285">Führen Sie die folgenden Aktionen aus, um die Symbolleiste **Weitere Aktionen anzuzeigen.**</span><span class="sxs-lookup"><span data-stu-id="f601e-285">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="f601e-286">Zeigen Sie **im Bereich** Formatvorlagen auf eine Formatvorlageregel.</span><span class="sxs-lookup"><span data-stu-id="f601e-286">In the **Styles** panel, hover on a style rule.</span></span>  <span data-ttu-id="f601e-287">**Weitere Aktionen** \( \) werden unten rechts im Abschnitt `...` Formatregel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f601e-287">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f601e-288">Zeigen Sie in der folgenden Abbildung auf die Formatregel, und weitere Aktionen werden unten rechts im Abschnitt `.header-holder.has-default-focus` Formatregel angezeigt. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f601e-288">In the following figure, hover on the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Weitere Aktionen" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="f601e-290">Reveal **More Actions** \( `...` \)</span><span class="sxs-lookup"><span data-stu-id="f601e-290">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f601e-291">Zeigen Sie auf **Weitere Aktionen** \( `...` \), um die oben genannten Aktionen zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="f601e-291">Hover on **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f601e-292">Die **Aktion Style Rule Below** einfügen wird nach dem Zeigen auf weitere Aktionen **angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="f601e-292">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Die Symbolleiste Weitere Aktionen" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="f601e-294">Die **Symbolleiste "Weitere Aktionen"**</span><span class="sxs-lookup"><span data-stu-id="f601e-294">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <a name="toggle-a-declaration"></a><span data-ttu-id="f601e-295">Umschalten einer Deklaration</span><span class="sxs-lookup"><span data-stu-id="f601e-295">Toggle a declaration</span></span>  

<span data-ttu-id="f601e-296">Führen Sie die folgenden Aktionen aus, um eine einzelne Deklaration auf \(oder off\) umzuschalten.</span><span class="sxs-lookup"><span data-stu-id="f601e-296">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="f601e-297">[Wählen Sie ein Element aus.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="f601e-297">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="f601e-298">Zeigen Sie **im Bereich** Formatvorlagen auf die Regel, die die Deklaration definiert.</span><span class="sxs-lookup"><span data-stu-id="f601e-298">In the **Styles** pane, hover on the rule that defines the declaration.</span></span>  <span data-ttu-id="f601e-299">Neben jeder Deklaration wird ein Kontrollkästchen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f601e-299">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="f601e-300">Aktivieren Sie \(oder deaktivieren Sie\) das Kontrollkästchen neben der Deklaration.</span><span class="sxs-lookup"><span data-stu-id="f601e-300">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="f601e-301">Wenn Sie eine Deklaration deaktivieren, durchkreuzt DevTools sie, um anzugeben, dass sie nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="f601e-301">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="f601e-302">In der folgenden Abbildung wurde die Eigenschaft für das aktuell ausgewählte Element `margin-top` deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f601e-302">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Umschalten einer Deklaration" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="f601e-304">Umschalten einer Deklaration</span><span class="sxs-lookup"><span data-stu-id="f601e-304">Toggle a declaration</span></span>  
:::image-end:::  

### <a name="add-a-background-color-declaration"></a><span data-ttu-id="f601e-305">Hinzufügen einer Hintergrundfarbdeklaration</span><span class="sxs-lookup"><span data-stu-id="f601e-305">Add a background-color declaration</span></span>  

<span data-ttu-id="f601e-306">Führen Sie die folgenden Aktionen aus, um einem `background-color` Element eine Deklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f601e-306">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="f601e-307">Zeigen Sie auf die Formatvorlageregel, der Sie die `background-color` Deklaration hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="f601e-307">Hover on the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="f601e-308">[Zeigen Sie die **Symbolleiste Weitere Aktionen** an.](#reveal-the-more-actions-toolbar)</span><span class="sxs-lookup"><span data-stu-id="f601e-308">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="f601e-309">Wählen **Sie Hintergrundfarbe hinzufügen** \( Symbol ![ Hintergrundfarbe hinzufügen ](../media/add-background-color-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="f601e-309">Choose **Add Background Color** \(![Add Background Color icon](../media/add-background-color-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Hinzufügen von Hintergrundfarbe" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="f601e-311">Hinzufügen von Hintergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="f601e-311">Add Background Color</span></span>**  
:::image-end:::  

### <a name="add-a-color-declaration"></a><span data-ttu-id="f601e-312">Hinzufügen einer Farbdeklaration</span><span class="sxs-lookup"><span data-stu-id="f601e-312">Add a color declaration</span></span>  

<span data-ttu-id="f601e-313">Führen Sie die folgenden Aktionen aus, um einem `color` Element eine Deklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f601e-313">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="f601e-314">Zeigen Sie auf die Formatvorlageregel, der Sie die `color` Deklaration hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="f601e-314">Hover on the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="f601e-315">[Zeigen Sie die **Symbolleiste Weitere Aktionen** an.](#reveal-the-more-actions-toolbar)</span><span class="sxs-lookup"><span data-stu-id="f601e-315">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="f601e-316">Wählen **Sie Farbe hinzufügen** \( ![ Farbsymbol hinzufügen ](../media/add-color-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="f601e-316">Choose **Add Color** \(![Add Color icon](../media/add-color-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Hinzufügen von Farbe" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="f601e-318">Hinzufügen von Farbe</span><span class="sxs-lookup"><span data-stu-id="f601e-318">Add Color</span></span>**  
:::image-end:::  

### <a name="add-a-box-shadow-declaration"></a><span data-ttu-id="f601e-319">Hinzufügen einer Box-Shadow-Deklaration</span><span class="sxs-lookup"><span data-stu-id="f601e-319">Add a box-shadow declaration</span></span>  

<span data-ttu-id="f601e-320">Führen Sie die folgenden Aktionen aus, um einem `box-shadow` Element eine Deklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f601e-320">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="f601e-321">Zeigen Sie auf die Formatvorlageregel, der Sie die `box-shadow` Deklaration hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="f601e-321">Hover on the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="f601e-322">[Zeigen Sie die **Symbolleiste Weitere Aktionen** an.](#reveal-the-more-actions-toolbar)</span><span class="sxs-lookup"><span data-stu-id="f601e-322">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="f601e-323">Wählen **Sie Hinzufügen von Feldschatten** \( Hinzufügen des ![ Feldschattensymbols ](../media/add-box-shadow-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="f601e-323">Choose **Add Box Shadow** \(![Add Box Shadow icon](../media/add-box-shadow-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Hinzufügen von Box Shadow" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="f601e-325">Hinzufügen von Box Shadow</span><span class="sxs-lookup"><span data-stu-id="f601e-325">Add Box Shadow</span></span>**  
:::image-end:::  

### <a name="add-a-text-shadow-declaration"></a><span data-ttu-id="f601e-326">Hinzufügen einer Text-Schatten-Deklaration</span><span class="sxs-lookup"><span data-stu-id="f601e-326">Add a text-shadow declaration</span></span>  

<span data-ttu-id="f601e-327">Führen Sie die folgenden Aktionen aus, um einem `text-shadow` Element eine Deklaration hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f601e-327">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="f601e-328">Zeigen Sie auf die Formatvorlageregel, der Sie die `text-shadow` Deklaration hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="f601e-328">Hover on the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="f601e-329">[Zeigen Sie die **Symbolleiste Weitere Aktionen** an.](#reveal-the-more-actions-toolbar)</span><span class="sxs-lookup"><span data-stu-id="f601e-329">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="f601e-330">Wählen **Sie Textschatten** hinzufügen \( ![ Textschattensymbol ](../media/add-text-shadow-icon.msft.png) hinzufügen \).</span><span class="sxs-lookup"><span data-stu-id="f601e-330">Choose **Add Text Shadow** \(![Add Text Shadow icon](../media/add-text-shadow-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Hinzufügen von Textschatten" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="f601e-332">Hinzufügen von Textschatten</span><span class="sxs-lookup"><span data-stu-id="f601e-332">Add Text Shadow</span></span>**  
:::image-end:::  

### <a name="change-colors-with-the-color-picker"></a><span data-ttu-id="f601e-333">Ändern von Farben mit der Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="f601e-333">Change colors with the Color Picker</span></span>  

<span data-ttu-id="f601e-334">Die **Farbauswahl bietet** eine GUI zum Ändern `color` und `background-color` Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="f601e-334">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="f601e-335">Führen Sie die folgenden Aktionen aus, um die **Farbauswahl zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="f601e-335">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="f601e-336">[Wählen Sie ein Element aus.](#choose-an-element)</span><span class="sxs-lookup"><span data-stu-id="f601e-336">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="f601e-337">Suchen Sie **im Bereich** Formatvorlagen nach der , oder ähnlichen Deklaration, die Sie `color` ändern `background-color` möchten.</span><span class="sxs-lookup"><span data-stu-id="f601e-337">In the **Styles** panel, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="f601e-338">Links vom Wert , oder einem ähnlichen Wert befindet sich ein kleines Quadrat, das eine `color` `background-color` Vorschau der Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="f601e-338">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f601e-339">In der folgenden Abbildung ist das kleine Quadrat links von eine `rgba(0, 0, 0, 0.7)` Vorschau dieser Farbe.</span><span class="sxs-lookup"><span data-stu-id="f601e-339">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Farbvorschau" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="f601e-341">Farbvorschau</span><span class="sxs-lookup"><span data-stu-id="f601e-341">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f601e-342">Wählen Sie die Vorschau aus, um die **Farbauswahl zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="f601e-342">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Die Farbauswahl" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="f601e-344">Die **Farbauswahl**</span><span class="sxs-lookup"><span data-stu-id="f601e-344">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f601e-345">In der folgenden Abbildung und Liste werden die einzelnen Benutzeroberflächenelemente der Farbauswahl **aufgeführt.**</span><span class="sxs-lookup"><span data-stu-id="f601e-345">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Die Farbauswahl mit Anmerkungen" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="f601e-347">The **Color Picker**, annotated</span><span class="sxs-lookup"><span data-stu-id="f601e-347">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="f601e-348">1</span><span class="sxs-lookup"><span data-stu-id="f601e-348">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="f601e-349">Schattierungen</span><span class="sxs-lookup"><span data-stu-id="f601e-349">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="f601e-350">2</span><span class="sxs-lookup"><span data-stu-id="f601e-350">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="f601e-351">Eyedropper</span><span class="sxs-lookup"><span data-stu-id="f601e-351">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f601e-352">Weitere Informationen finden Sie unter [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="f601e-352">For more information, navigate to [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="f601e-353">3</span><span class="sxs-lookup"><span data-stu-id="f601e-353">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="f601e-354">In Zwischenablage kopieren</span><span class="sxs-lookup"><span data-stu-id="f601e-354">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f601e-355">Kopieren Sie **den Anzeigewert** in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="f601e-355">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="f601e-356">4</span><span class="sxs-lookup"><span data-stu-id="f601e-356">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="f601e-357">Anzeigewert</span><span class="sxs-lookup"><span data-stu-id="f601e-357">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f601e-358">Die RGBA-, HSLA- oder Hexdarstellung der Farbe.</span><span class="sxs-lookup"><span data-stu-id="f601e-358">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="f601e-359">5</span><span class="sxs-lookup"><span data-stu-id="f601e-359">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="f601e-360">Farbpalette</span><span class="sxs-lookup"><span data-stu-id="f601e-360">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f601e-361">Wählen Sie eines der Quadrate aus, um die Farbe in dieses Quadrat zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f601e-361">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="f601e-362">6</span><span class="sxs-lookup"><span data-stu-id="f601e-362">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="f601e-363">Hue</span><span class="sxs-lookup"><span data-stu-id="f601e-363">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="f601e-364">7</span><span class="sxs-lookup"><span data-stu-id="f601e-364">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="f601e-365">Opacity</span><span class="sxs-lookup"><span data-stu-id="f601e-365">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="f601e-366">8</span><span class="sxs-lookup"><span data-stu-id="f601e-366">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="f601e-367">Display Value Switcher</span><span class="sxs-lookup"><span data-stu-id="f601e-367">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f601e-368">Umschalten zwischen den RGBA-, HSLA- und Hex-Darstellungen der aktuellen Farbe.</span><span class="sxs-lookup"><span data-stu-id="f601e-368">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="f601e-369">9</span><span class="sxs-lookup"><span data-stu-id="f601e-369">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="f601e-370">Farbpaletten-Switcher</span><span class="sxs-lookup"><span data-stu-id="f601e-370">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="f601e-371">Umschalten zwischen der [Palette Materialdesign,][MaterialDesignColorSystem]einer benutzerdefinierten Palette oder einer Seitenfarbenpalette.</span><span class="sxs-lookup"><span data-stu-id="f601e-371">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="f601e-372">DevTools generiert die Seitenfarbpalette basierend auf den Farben, die sie in Ihren Stylesheets findet.</span><span class="sxs-lookup"><span data-stu-id="f601e-372">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <a name="sample-a-color-off-the-page-with-the-eyedropper"></a><span data-ttu-id="f601e-373">Beispiel für eine Farbe von der Seite mit der Eyedropper</span><span class="sxs-lookup"><span data-stu-id="f601e-373">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="f601e-374">Wenn Sie die **Farbauswahl öffnen,** ist **die Eyedropper** \( ![ Eyedropper ](../media/eyedropper-icon.msft.png) \) standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f601e-374">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper](../media/eyedropper-icon.msft.png)\) is on by default.</span></span>  <span data-ttu-id="f601e-375">Führen Sie die folgenden Aktionen aus, um die ausgewählte Farbe in eine andere Farbe auf der Seite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f601e-375">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="f601e-376">Zeigen Sie im Viewport auf die Zielfarbe.</span><span class="sxs-lookup"><span data-stu-id="f601e-376">Hover on the target color in the viewport.</span></span>  
1.  <span data-ttu-id="f601e-377">Wählen Sie aus, um dies zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="f601e-377">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f601e-378">In der folgenden Abbildung zeigt die **Farbauswahl** den aktuellen Farbwert von , der in der Nähe von `rgba(0,0,0,0.7)` Schwarz liegt.</span><span class="sxs-lookup"><span data-stu-id="f601e-378">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="f601e-379">Die spezifische Farbe sollte in die Version von Schwarz geändert werden, die derzeit im Ansichtsfenster hervorgehoben ist, nachdem Sie sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="f601e-379">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Verwenden der Eyedropper" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="f601e-381">Verwenden der Eyedropper</span><span class="sxs-lookup"><span data-stu-id="f601e-381">Using the Eyedropper</span></span>  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f601e-382">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="f601e-382">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Führen Sie Befehle mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft Docs"  
[DevToolsCSSGetStarted]: ../css/index.md "Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Hinzufügen eines Pseudozustands zu einer Klasse – Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Anzeigen der CSS für ein Element – Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Erzwingen von Microsoft Edge DevTools in den Druckvorschaumodus (CSS Print Media Type) | Microsoft Docs"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Neuschreiben einer minifizierten JavaScript-Datei mit &quot;Pretty-Print&quot; – Verwenden der Debugger-| Microsoft Docs"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Das Farbsystem – Materialdesign"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Das Feldmodell | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Auswahltypen – Spezifizitätstypen | MDN"  

> [!NOTE]
> <span data-ttu-id="f601e-392">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f601e-392">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f601e-393">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="f601e-393">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="f601e-395">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f601e-395">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
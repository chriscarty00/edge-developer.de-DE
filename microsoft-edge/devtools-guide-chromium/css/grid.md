---
description: Erfahren Sie, wie Sie Microsoft Edge DevTools zum Anzeigen und Ändern der CSS einer Seite CSS verwenden.
title: Überprüfen des CSS-Rasters in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 68493fae5e96ef1b2c7ed1205d67fd2b4cf67df5
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564455"
---
# <a name="inspect-css-grid"></a><span data-ttu-id="a64f4-104">Überprüfen des CSS-Rasters</span><span class="sxs-lookup"><span data-stu-id="a64f4-104">Inspect CSS Grid</span></span>  

<span data-ttu-id="a64f4-105">In diesem Artikel werden Sie durch das Identifizieren von CSS-Rastern auf einer Website und das Debuggen von Rasterlayoutproblemen mithilfe anpassbarer Rasterüberlagerungen erläutert.</span><span class="sxs-lookup"><span data-stu-id="a64f4-105">This article walks you through identifying CSS grids on a website and debugging grid layout issues using customizable grid overlays.</span></span>  

<span data-ttu-id="a64f4-106">Die In den Abbildungen in diesem Artikel verwendeten Beispiele sind den folgenden Webseiten zu finden.</span><span class="sxs-lookup"><span data-stu-id="a64f4-106">The examples used in the figures in this article are taken from the following webpages.</span></span>  

*   [<span data-ttu-id="a64f4-107">Obstfeld</span><span class="sxs-lookup"><span data-stu-id="a64f4-107">Fruit box</span></span>][JecFyiDemoCssGridFruit]  
*   [<span data-ttu-id="a64f4-108">Feld "ImBiss"</span><span class="sxs-lookup"><span data-stu-id="a64f4-108">Snack box</span></span>][JecFyiDemoCssGridSnack]  

## <a name="before-you-begin"></a><span data-ttu-id="a64f4-109">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="a64f4-109">Before you begin</span></span>  

<span data-ttu-id="a64f4-110">CSS Grid ist ein leistungsfähiges Layoutparadigma für das Web.</span><span class="sxs-lookup"><span data-stu-id="a64f4-110">CSS Grid is a powerful layout paradigm for the web.</span></span>  <span data-ttu-id="a64f4-111">Ein großartiger Ort, um sich mit css Grid und den vielen Features zu beginnen, ist die [CSS Grid Layout-Anleitung][MdnCssGridLayout] auf MDN.</span><span class="sxs-lookup"><span data-stu-id="a64f4-111">A great place to get started learning about CSS Grid and the many features is the [CSS Grid Layout guide][MdnCssGridLayout] on MDN.</span></span>  

## <a name="discover-css-grids"></a><span data-ttu-id="a64f4-112">Entdecken von CSS-Rastern</span><span class="sxs-lookup"><span data-stu-id="a64f4-112">Discover CSS grids</span></span>  

<span data-ttu-id="a64f4-113">Wenn ein HTML-Element auf Ihrer Seite darauf angewendet wurde oder darauf angewendet wurde, wird daneben im Bereich Elemente ein Signal `display: grid` `display: inline-grid` `grid` angezeigt. [][DevtoolsGuideChromiumOpen]</span><span class="sxs-lookup"><span data-stu-id="a64f4-113">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a `grid` badge is displayed next to it in the [Elements][DevtoolsGuideChromiumOpen] panel.</span></span>  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Raster ermitteln" lightbox="../media/grid-discover-grid.msft.png":::
   <span data-ttu-id="a64f4-115">Raster ermitteln</span><span class="sxs-lookup"><span data-stu-id="a64f4-115">Discover grid</span></span>  
:::image-end:::  

<span data-ttu-id="a64f4-116">Wählen Sie das Signal aus, um die Anzeige einer Rasterüberlagerung auf der Seite umschalten zu können.</span><span class="sxs-lookup"><span data-stu-id="a64f4-116">Choose the badge to toggle the display of a grid overlay on the page.</span></span>  <span data-ttu-id="a64f4-117">Die Überlagerung wird über dem Element angezeigt, das wie ein Raster ausgelegt ist, um die Position der Gitternetzlinien und -spuren zu zeigen:</span><span class="sxs-lookup"><span data-stu-id="a64f4-117">The overlay appears over the element, laid out like a grid to display the position of the grid lines and tracks:</span></span>  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Gitternetzabzeichen umschalten" lightbox="../media/grid-highlight-grid.msft.png":::
   <span data-ttu-id="a64f4-119">Gitternetzabzeichen umschalten</span><span class="sxs-lookup"><span data-stu-id="a64f4-119">Toggle grid badge</span></span>  
:::image-end:::  

<span data-ttu-id="a64f4-120">Öffnen Sie den **Bereich Layout.**</span><span class="sxs-lookup"><span data-stu-id="a64f4-120">Open the **Layout** pane.</span></span>  <span data-ttu-id="a64f4-121">Wenn Raster auf einer Seite enthalten sind, enthält der **Layoutbereich** einen **Abschnitt Grid** mit einer Reihe von Optionen zum Anzeigen der Raster.</span><span class="sxs-lookup"><span data-stu-id="a64f4-121">When grids are included on a page, the **Layout** pane includes a **Grid** section containing a number of options for viewing the grids.</span></span>  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Layoutbereich" lightbox="../media/grid-layout-pane.msft.png":::
   <span data-ttu-id="a64f4-123">**Layoutbereich**</span><span class="sxs-lookup"><span data-stu-id="a64f4-123">**Layout** pane</span></span>  
:::image-end:::  

<span data-ttu-id="a64f4-124">Der **Abschnitt Grid** im **Layoutbereich** enthält die folgenden 2 Unterabschnitte.</span><span class="sxs-lookup"><span data-stu-id="a64f4-124">The **Grid** section in the **Layout** pane contains the following 2 sub-sections.</span></span>  

*   <span data-ttu-id="a64f4-125">Überlagerungsanzeigeeinstellungen</span><span class="sxs-lookup"><span data-stu-id="a64f4-125">Overlay display settings</span></span>  
*   <span data-ttu-id="a64f4-126">Rasterüberlagerungen</span><span class="sxs-lookup"><span data-stu-id="a64f4-126">Grid overlays</span></span>  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <a name="overlay-display-settings"></a><span data-ttu-id="a64f4-127">Überlagerungsanzeigeeinstellungen</span><span class="sxs-lookup"><span data-stu-id="a64f4-127">Overlay display settings</span></span>  

<span data-ttu-id="a64f4-128">Die **Überlagerungsanzeigeeinstellungen** bestehen aus den folgenden 2 Teilen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-128">The **Overlay display settings** consists of following 2 parts.</span></span>  

*   <span data-ttu-id="a64f4-129">Wählen Sie im Dropdownmenü eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="a64f4-129">Choose one of the following options from the dropdown menu.</span></span>  
    
    | <span data-ttu-id="a64f4-130">Line-Option</span><span class="sxs-lookup"><span data-stu-id="a64f4-130">Line option</span></span> | <span data-ttu-id="a64f4-131">Details</span><span class="sxs-lookup"><span data-stu-id="a64f4-131">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="a64f4-132">Ausblenden von Linienbeschriftungen</span><span class="sxs-lookup"><span data-stu-id="a64f4-132">Hide line labels</span></span>** | <span data-ttu-id="a64f4-133">Blenden Sie die Beschriftungen der Linien für jede Rasterüberlagerung aus.</span><span class="sxs-lookup"><span data-stu-id="a64f4-133">Hide the labels of the lines for each grid overlay.</span></span> |  
    | **<span data-ttu-id="a64f4-134">Anzeigen von Zeilennummern</span><span class="sxs-lookup"><span data-stu-id="a64f4-134">Show line numbers</span></span>** | <span data-ttu-id="a64f4-135">Zeigt die Nummern der Zeilen für jede Rasterüberlagerung \(standardmäßig ausgewählt\) an.</span><span class="sxs-lookup"><span data-stu-id="a64f4-135">Display the numbers of the lines for each grid overlay \(selected by default\).</span></span> |  
    | **<span data-ttu-id="a64f4-136">Anzeigen von Zeilennamen</span><span class="sxs-lookup"><span data-stu-id="a64f4-136">Show line names</span></span>** | <span data-ttu-id="a64f4-137">Zeigt die Namen der Zeilen für jede Rasterüberlagerung an, wenn Namen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a64f4-137">Display the names of the lines for each grid overlay when names are provided.</span></span> |  
    
*  <span data-ttu-id="a64f4-138">Aktivieren Sie das Kontrollkästchen neben den folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-138">Choose the checkbox next the following options.</span></span>  
    
    | <span data-ttu-id="a64f4-139">Option</span><span class="sxs-lookup"><span data-stu-id="a64f4-139">Option</span></span> | <span data-ttu-id="a64f4-140">Details</span><span class="sxs-lookup"><span data-stu-id="a64f4-140">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="a64f4-141">Anzeigen von Titelgrößen</span><span class="sxs-lookup"><span data-stu-id="a64f4-141">Show track sizes</span></span>**  | <span data-ttu-id="a64f4-142">Zeigen Sie \(oder ausblenden\) die Größen der Titel an.</span><span class="sxs-lookup"><span data-stu-id="a64f4-142">Display \(or hide\) the sizes of the tracks.</span></span> |  
    | **<span data-ttu-id="a64f4-143">Anzeigen von Bereichsnamen</span><span class="sxs-lookup"><span data-stu-id="a64f4-143">Show area names</span></span>** | <span data-ttu-id="a64f4-144">Zeigen Sie \(oder ausblenden\) die Namen des Bereichs an, wenn Namen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a64f4-144">Display \(or hide\) the names of the area, when names are provided.</span></span> |  
    | **<span data-ttu-id="a64f4-145">Erweitern von Gitternetzlinien</span><span class="sxs-lookup"><span data-stu-id="a64f4-145">Extend grid lines</span></span>** | <span data-ttu-id="a64f4-146">Zeigt \(oder blendet\) die Erweiterungen der Rasterdimensionen entlang jeder Achse an.</span><span class="sxs-lookup"><span data-stu-id="a64f4-146">Displays \(or hides\) the extensions of the grid dimensions along each axis.</span></span>  <span data-ttu-id="a64f4-147">Standardmäßig werden Gitternetzlinien nur innerhalb des Elements angezeigt, für das `display: grid` `display: inline-grid` css festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a64f4-147">By default, grid lines are only shown inside the element with `display: grid` or `display: inline-grid` CSS set on it.</span></span> |  
    
<span data-ttu-id="a64f4-148">In den folgenden Abschnitten finden Sie Details für jede der **Überlagerungsanzeigeeinstellungen.**</span><span class="sxs-lookup"><span data-stu-id="a64f4-148">The following sections provide details for each of the **Overlay display settings**.</span></span>  

### <a name="show-line-numbers"></a><span data-ttu-id="a64f4-149">Anzeigen von Zeilennummern</span><span class="sxs-lookup"><span data-stu-id="a64f4-149">Show line numbers</span></span>  

<span data-ttu-id="a64f4-150">Standardmäßig werden die positiven und negativen Zeilennummern auf der Rasterüberlagerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a64f4-150">By default, the positive and negative line numbers are displayed on the grid overlay.</span></span>  

<span data-ttu-id="a64f4-151">Weitere Informationen zu negativen Zahlen in der Rasterüberlagerung finden Sie unter [Line-based placement with CSS Grid][MdnLineBasedPlacementCssGrid].</span><span class="sxs-lookup"><span data-stu-id="a64f4-151">For more information about negative numbers in the grid overlay, navigate to [Line-based placement with CSS Grid][MdnLineBasedPlacementCssGrid].</span></span>  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Anzeigen von Zeilennummern" lightbox="../media/grid-show-line-numbers.msft.png":::
   <span data-ttu-id="a64f4-153">Anzeigen von Zeilennummern</span><span class="sxs-lookup"><span data-stu-id="a64f4-153">Display line numbers</span></span>  
:::image-end:::  

### <a name="hide-line-labels"></a><span data-ttu-id="a64f4-154">Ausblenden von Linienbeschriftungen</span><span class="sxs-lookup"><span data-stu-id="a64f4-154">Hide line labels</span></span>  

<span data-ttu-id="a64f4-155">Wählen **Sie Zeilenbeschriftungen ausblenden aus,** um die Zeilennummern auszublenden.</span><span class="sxs-lookup"><span data-stu-id="a64f4-155">Choose **Hide line labels** to hide the line numbers.</span></span>  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Ausblenden von Linienbeschriftungen" lightbox="../media/grid-hide-line-labels.msft.png":::
   <span data-ttu-id="a64f4-157">Ausblenden von Linienbeschriftungen</span><span class="sxs-lookup"><span data-stu-id="a64f4-157">Hide line labels</span></span>  
:::image-end:::  

### <a name="show-line-names"></a><span data-ttu-id="a64f4-158">Anzeigen von Zeilennamen</span><span class="sxs-lookup"><span data-stu-id="a64f4-158">Show line names</span></span>  

<span data-ttu-id="a64f4-159">Weitere Informationen zu Liniennamen in der Rasterüberlagerung finden Sie unter [Layout mit benannten Gitternetzlinien.][MdnLayoutUsingNamedGridLines]</span><span class="sxs-lookup"><span data-stu-id="a64f4-159">For more information about line names in the grid overlay, navigate to [Layout using named grid lines][MdnLayoutUsingNamedGridLines].</span></span>  

<span data-ttu-id="a64f4-160">Wählen **Sie Zeilennamen anzeigen aus,** um die Zeilennamen anstelle von Zahlen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-160">Choose **Show line names** to view the line names instead of numbers.</span></span>  <span data-ttu-id="a64f4-161">Im Beispiel haben 4 Zeilen Namen: `left` , , , und `middle1` `middle2` `right` .</span><span class="sxs-lookup"><span data-stu-id="a64f4-161">In the example, 4 lines have names: `left`, `middle1`, `middle2`, and `right`.</span></span>  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Anzeigen von Zeilennamen" lightbox="../media/grid-show-line-names.msft.png":::
   **<span data-ttu-id="a64f4-163">Anzeigen von Zeilennamen</span><span class="sxs-lookup"><span data-stu-id="a64f4-163">Show line names</span></span>**  
:::image-end:::  

### <a name="show-track-sizes"></a><span data-ttu-id="a64f4-164">Anzeigen von Titelgrößen</span><span class="sxs-lookup"><span data-stu-id="a64f4-164">Show track sizes</span></span>  

<span data-ttu-id="a64f4-165">Aktivieren Sie das **Kontrollkästchen Titelgrößen anzeigen,** um die Titelgrößen des Rasters anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-165">Enable the **Show track sizes** checkbox to view the track sizes of the grid.</span></span>  

<span data-ttu-id="a64f4-166">DevTools zeigt `[authored size]` und `[computed size]` in jeder Zeilenbeschriftung an.</span><span class="sxs-lookup"><span data-stu-id="a64f4-166">DevTools displays `[authored size]` and `[computed size]` in each line label.</span></span>  

| <span data-ttu-id="a64f4-167">Size</span><span class="sxs-lookup"><span data-stu-id="a64f4-167">Size</span></span> | <span data-ttu-id="a64f4-168">Details</span><span class="sxs-lookup"><span data-stu-id="a64f4-168">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="a64f4-169">Erstellungsgröße</span><span class="sxs-lookup"><span data-stu-id="a64f4-169">authored size</span></span>** | <span data-ttu-id="a64f4-170">Die größe, die in stylesheet \(omitted if not defined\) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a64f4-170">The size defined in stylesheet \(omitted if not defined\).</span></span> |  
| **<span data-ttu-id="a64f4-171">berechnete Größe</span><span class="sxs-lookup"><span data-stu-id="a64f4-171">computed size</span></span>** | <span data-ttu-id="a64f4-172">Die tatsächliche Größe auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="a64f4-172">The actual size on screen.</span></span> |  

<span data-ttu-id="a64f4-173">In der Demo werden `snack-box` die Spaltengrößen im CSS `grid-template-columns:1fr 2fr;` definiert.</span><span class="sxs-lookup"><span data-stu-id="a64f4-173">In the demo, the `snack-box` column sizes are defined in the `grid-template-columns:1fr 2fr;` CSS.</span></span>  <span data-ttu-id="a64f4-174">Daher werden in den Spaltenlinienbeschriftungen sowohl die erstellungs- als auch die berechnete Größe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a64f4-174">Therefore, the column line labels display both authored and computed sizes.</span></span>  

| <span data-ttu-id="a64f4-175">Track-Größe</span><span class="sxs-lookup"><span data-stu-id="a64f4-175">Track size</span></span> | <span data-ttu-id="a64f4-176">Größe des Autors</span><span class="sxs-lookup"><span data-stu-id="a64f4-176">Authored size</span></span> | <span data-ttu-id="a64f4-177">Berechnete Größe</span><span class="sxs-lookup"><span data-stu-id="a64f4-177">Computed size</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a64f4-178">**1fr** &#x2022; **96,66px**</span><span class="sxs-lookup"><span data-stu-id="a64f4-178">**1fr** &#x2022; **96.66px**</span></span> | <span data-ttu-id="a64f4-179">1fr</span><span class="sxs-lookup"><span data-stu-id="a64f4-179">1fr</span></span> | <span data-ttu-id="a64f4-180">96,66px</span><span class="sxs-lookup"><span data-stu-id="a64f4-180">96.66px</span></span> |  
| <span data-ttu-id="a64f4-181">**2fr** &#x2022; **193.32px**</span><span class="sxs-lookup"><span data-stu-id="a64f4-181">**2fr** &#x2022; **193.32px**</span></span> | <span data-ttu-id="a64f4-182">2fr</span><span class="sxs-lookup"><span data-stu-id="a64f4-182">2fr</span></span> | <span data-ttu-id="a64f4-183">193.32px</span><span class="sxs-lookup"><span data-stu-id="a64f4-183">193.32px</span></span> |  

<span data-ttu-id="a64f4-184">Die Zeilenlinienbeschriftungen zeigen nur berechnete Größen an, da im Stylesheet keine Zeilengrößen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a64f4-184">The row line labels display only computed sizes, since there are no row sizes defined in the stylesheet.</span></span>  

| <span data-ttu-id="a64f4-185">Track-Größe</span><span class="sxs-lookup"><span data-stu-id="a64f4-185">Track size</span></span> | <span data-ttu-id="a64f4-186">Größe des Autors</span><span class="sxs-lookup"><span data-stu-id="a64f4-186">Authored size</span></span> | <span data-ttu-id="a64f4-187">Berechnete Größe</span><span class="sxs-lookup"><span data-stu-id="a64f4-187">Computed size</span></span> |  
|:--- |:--- |:--- |  
| **<span data-ttu-id="a64f4-188">80px</span><span class="sxs-lookup"><span data-stu-id="a64f4-188">80px</span></span>** | &nbsp;| <span data-ttu-id="a64f4-189">80px</span><span class="sxs-lookup"><span data-stu-id="a64f4-189">80px</span></span> |  
| **<span data-ttu-id="a64f4-190">80px</span><span class="sxs-lookup"><span data-stu-id="a64f4-190">80px</span></span>** | &nbsp;| <span data-ttu-id="a64f4-191">80px</span><span class="sxs-lookup"><span data-stu-id="a64f4-191">80px</span></span> |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Anzeigen von Titelgrößen" lightbox="../media/grid-show-track-sizes.msft.png":::
   **<span data-ttu-id="a64f4-193">Anzeigen von Titelgrößen</span><span class="sxs-lookup"><span data-stu-id="a64f4-193">Show track sizes</span></span>**  
:::image-end:::  

### <a name="show-area-names"></a><span data-ttu-id="a64f4-194">Anzeigen von Bereichsnamen</span><span class="sxs-lookup"><span data-stu-id="a64f4-194">Show area names</span></span>  

<span data-ttu-id="a64f4-195">Aktivieren Sie zum Anzeigen der Bereichsnamen das Kontrollkästchen **Bereichsnamen** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-195">To view the area names, enable the **Show area names** checkbox.</span></span>  <span data-ttu-id="a64f4-196">Im Beispiel sind drei Bereiche im Raster: **oben,** **unten1** und **unten2**.</span><span class="sxs-lookup"><span data-stu-id="a64f4-196">In the example, there are 3 areas in the grid: **top**, **bottom1** and **bottom2**.</span></span>  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Anzeigen von Bereichsnamen" lightbox="../media/grid-show-area-names.msft.png":::
   **<span data-ttu-id="a64f4-198">Anzeigen von Bereichsnamen</span><span class="sxs-lookup"><span data-stu-id="a64f4-198">Show area names</span></span>**  
:::image-end:::  

### <a name="extend-grid-lines"></a><span data-ttu-id="a64f4-199">Erweitern von Gitternetzlinien</span><span class="sxs-lookup"><span data-stu-id="a64f4-199">Extend grid lines</span></span>  

<span data-ttu-id="a64f4-200">Aktivieren Sie **das Kontrollkästchen Gitternetzlinien** erweitern, um die Gitternetzlinien bis zum Rand des Viewports entlang jeder Achse zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="a64f4-200">Enable the **Extend grid lines** checkbox to extend the grid lines to the edge of the viewport along each axis.</span></span>  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Erweitern von Gitternetzlinien" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **<span data-ttu-id="a64f4-202">Erweitern von Gitternetzlinien</span><span class="sxs-lookup"><span data-stu-id="a64f4-202">Extend grid lines</span></span>**  
:::image-end:::  

## <a name="grid-overlays"></a><span data-ttu-id="a64f4-203">Rasterüberlagerungen</span><span class="sxs-lookup"><span data-stu-id="a64f4-203">Grid overlays</span></span>  

<span data-ttu-id="a64f4-204">Der **Abschnitt Rasterüberlagerungen** enthält eine Liste der Raster, die auf der Seite vorhanden sind, jeweils mit einem Kontrollkästchen sowie verschiedenen Optionen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-204">The **Grid overlays** section contains a list of grids that are present on the page, each with a checkbox, along with various options.</span></span>  

### <a name="enable-overlay-views-of-multiple-grids"></a><span data-ttu-id="a64f4-205">Aktivieren von Überlagerungsansichten mehrerer Raster</span><span class="sxs-lookup"><span data-stu-id="a64f4-205">Enable overlay views of multiple grids</span></span>  

<span data-ttu-id="a64f4-206">Wenn Sie das Überlagerungsraster für mehrere Raster anzeigen möchten, aktivieren Sie das Kontrollkästchen neben jedem Namen des Rasters.</span><span class="sxs-lookup"><span data-stu-id="a64f4-206">To display the overlay grid for multiple grids, choose the checkbox next to each name of the grid.</span></span>  <span data-ttu-id="a64f4-207">Im Beispiel sind zwei Rasterüberlagerungen aktiviert, die jeweils mit unterschiedlichen Farben dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a64f4-207">In the example, there are 2 grid overlays enabled that are each represented with different colors.</span></span>  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Aktivieren von Überlagerungsansichten mehrerer Raster" lightbox="../media/grid-grid-overlays.msft.png":::
   <span data-ttu-id="a64f4-209">Aktivieren von Überlagerungsansichten mehrerer Raster</span><span class="sxs-lookup"><span data-stu-id="a64f4-209">Enable overlay views of multiple grids</span></span>  
:::image-end:::  

### <a name="customize-the-grid-overlay-color"></a><span data-ttu-id="a64f4-210">Anpassen der Rasterüberlagerungsfarbe</span><span class="sxs-lookup"><span data-stu-id="a64f4-210">Customize the grid overlay color</span></span>  

<span data-ttu-id="a64f4-211">Um die Farbauswahl zu öffnen und die Rasterüberlagerungsfarbe anzupassen, wählen Sie das Feld neben dem Namen der Rasterüberlagerung aus.</span><span class="sxs-lookup"><span data-stu-id="a64f4-211">To open the color picker and customize the grid overlay color, choose the box next to the name of the grid overlay.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Anpassen der Rasterüberlagerungsfarbe" lightbox="../media/grid-grid-overlays-color.msft.png":::
   <span data-ttu-id="a64f4-213">Anpassen der Rasterüberlagerungsfarbe</span><span class="sxs-lookup"><span data-stu-id="a64f4-213">Customize the grid overlay color</span></span>  
:::image-end:::  

### <a name="highlight-the-grid"></a><span data-ttu-id="a64f4-214">Hervorheben des Rasters</span><span class="sxs-lookup"><span data-stu-id="a64f4-214">Highlight the grid</span></span>  

<span data-ttu-id="a64f4-215">Um das HTML-Element \*\*\*\* im Elementtool zu markieren und auf der Webseite zu diesem zu scrollen, wählen Sie das Element Anzeigen **im** Bereich Elemente \( Element anzeigen im Elementbereichssymbol ![ ](../media/show-element-in-element-panel-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="a64f4-215">To highlight the HTML element in the **Elements** tool and scroll to it on the webpage, choose the **Show element in the Elements panel** \(![Show element in the Elements panel icon](../media/show-element-in-element-panel-icon.msft.png)\) icon.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Hervorheben des Rasters" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   <span data-ttu-id="a64f4-217">Hervorheben des Rasters</span><span class="sxs-lookup"><span data-stu-id="a64f4-217">Highlight the grid</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a64f4-218">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="a64f4-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Öffnen Microsoft Edge DevTools | Microsoft Docs"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "CSS-Raster | jec.fyi"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "CSS-Raster | jec.fyi"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "CSS Grid Layout | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Layout mit benannten Gitternetzlinien | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Zeilenbasierte Platzierung mit CSS Grid | MDN"  

> [!NOTE]
> <span data-ttu-id="a64f4-225">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a64f4-225">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a64f4-226">Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/grid) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="a64f4-226">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/grid) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a64f4-228">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a64f4-228">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  

---
description: Erfahren Sie, wie Sie Microsoft Edge devtools verwenden, um das CSS einer Seite CSS anzuzeigen und zu ändern.
title: Überprüfen des CSS-Rasters in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 1fe6bd1c8efd244315fb9a38777df6ea3e9b1a4d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231097"
---
# <span data-ttu-id="68735-104">Überprüfen des CSS-Rasters</span><span class="sxs-lookup"><span data-stu-id="68735-104">Inspect CSS Grid</span></span>  

<span data-ttu-id="68735-105">In diesem Artikel wird erläutert, wie Sie CSS-Raster auf einer Website identifizieren und Probleme mit Rasterlayouts mithilfe anpassbarer Raster Überlagerungen Debuggen.</span><span class="sxs-lookup"><span data-stu-id="68735-105">This article walks you through identifying CSS grids on a website and debugging grid layout issues using customizable grid overlays.</span></span>  

<span data-ttu-id="68735-106">Die in den Abbildungen in diesem Artikel verwendeten Beispiele sind den folgenden Webseiten zu entgenommen.</span><span class="sxs-lookup"><span data-stu-id="68735-106">The examples used in the figures in this article are taken from the following webpages.</span></span>  

*   [<span data-ttu-id="68735-107">Obst Kasten</span><span class="sxs-lookup"><span data-stu-id="68735-107">Fruit box</span></span>][JecFyiDemoCssGridFruit]  
*   [<span data-ttu-id="68735-108">Snack-Box</span><span class="sxs-lookup"><span data-stu-id="68735-108">Snack box</span></span>][JecFyiDemoCssGridSnack]  

## <span data-ttu-id="68735-109">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="68735-109">Before you begin</span></span>  

<span data-ttu-id="68735-110">CSS-Raster ist ein leistungsfähiges Layout-Paradigma für das Web.</span><span class="sxs-lookup"><span data-stu-id="68735-110">CSS Grid is a powerful layout paradigm for the web.</span></span>  <span data-ttu-id="68735-111">Ein toller Ort, um mit dem Erlernen des CSS-Rasters und der vielen Features vertraut zu werden, ist die [CSS-Raster Layout-Anleitung][MdnCssGridLayout] auf MDN.</span><span class="sxs-lookup"><span data-stu-id="68735-111">A great place to get started learning about CSS Grid and the many features is the [CSS Grid Layout guide][MdnCssGridLayout] on MDN.</span></span>  

## <span data-ttu-id="68735-112">Entdecken von CSS-Rastern</span><span class="sxs-lookup"><span data-stu-id="68735-112">Discover CSS grids</span></span>  

<span data-ttu-id="68735-113">Wenn auf der Seite ein HTML-Element auf der Seite `display: grid` `display: inline-grid` angelegt oder angewendet wurde, `grid` wird im [Element][DevtoolsGuideChromiumOpen] Panel daneben ein Badge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68735-113">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a `grid` badge is displayed next to it in the [Elements][DevtoolsGuideChromiumOpen] panel.</span></span>  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-discover-grid.msft.png":::
   <span data-ttu-id="68735-115">Raster entdecken</span><span class="sxs-lookup"><span data-stu-id="68735-115">Discover grid</span></span>  
:::image-end:::  

<span data-ttu-id="68735-116">Wählen Sie das Abzeichen aus, um die Anzeige einer Raster Überlagerung auf der Seite umzuschalten.</span><span class="sxs-lookup"><span data-stu-id="68735-116">Select the badge to toggle the display of a grid overlay on the page.</span></span>  <span data-ttu-id="68735-117">Die Überlagerung wird über dem Element dargestellt, wie ein Raster angeordnet, um die Position der Rasterlinien und Titel anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="68735-117">The overlay appears over the element, laid out like a grid to display the position of the grid lines and tracks:</span></span>  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Rastersignal umschalten" lightbox="../media/grid-highlight-grid.msft.png":::
   <span data-ttu-id="68735-119">Rastersignal umschalten</span><span class="sxs-lookup"><span data-stu-id="68735-119">Toggle grid badge</span></span>  
:::image-end:::  

<span data-ttu-id="68735-120">Öffnen Sie den Bereich " **Layout** ".</span><span class="sxs-lookup"><span data-stu-id="68735-120">Open the **Layout** pane.</span></span>  <span data-ttu-id="68735-121">Wenn Raster auf einer Seite enthalten sind, enthält der Bereich **Layout** einen **Raster** Abschnitt, der eine Reihe von Optionen zum Anzeigen der Raster enthält.</span><span class="sxs-lookup"><span data-stu-id="68735-121">When grids are included on a page, the **Layout** pane includes a **Grid** section containing a number of options for viewing the grids.</span></span>  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Bereich ' Layout '" lightbox="../media/grid-layout-pane.msft.png":::
   <span data-ttu-id="68735-123">Bereich ' **Layout** '</span><span class="sxs-lookup"><span data-stu-id="68735-123">**Layout** pane</span></span>  
:::image-end:::  

<span data-ttu-id="68735-124">Der Abschnitt " **Raster** " im Bereich " **Layout** " enthält die folgenden 2 Unterabschnitte.</span><span class="sxs-lookup"><span data-stu-id="68735-124">The **Grid** section in the **Layout** pane contains the following 2 sub-sections.</span></span>  

*   <span data-ttu-id="68735-125">Anzeigeeinstellungen für Overlays</span><span class="sxs-lookup"><span data-stu-id="68735-125">Overlay display settings</span></span>  
*   <span data-ttu-id="68735-126">Raster Überlagerungen</span><span class="sxs-lookup"><span data-stu-id="68735-126">Grid overlays</span></span>  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <span data-ttu-id="68735-127">Anzeigeeinstellungen für Overlays</span><span class="sxs-lookup"><span data-stu-id="68735-127">Overlay display settings</span></span>  

<span data-ttu-id="68735-128">Die **Einstellungen** für die Overlay-Anzeige bestehen aus zwei Teilen.</span><span class="sxs-lookup"><span data-stu-id="68735-128">The **Overlay display settings** consists of following 2 parts.</span></span>  

*   <span data-ttu-id="68735-129">Wählen Sie eine der folgenden Optionen aus dem Dropdown-Menü aus.</span><span class="sxs-lookup"><span data-stu-id="68735-129">Choose one of the following options from the dropdown menu.</span></span>  
    
    | <span data-ttu-id="68735-130">Option "Zeile"</span><span class="sxs-lookup"><span data-stu-id="68735-130">Line option</span></span> | <span data-ttu-id="68735-131">Details</span><span class="sxs-lookup"><span data-stu-id="68735-131">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="68735-132">Ausblenden von Strich Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="68735-132">Hide line labels</span></span>** | <span data-ttu-id="68735-133">Blenden Sie die Beschriftungen der Linien für jede Raster Überlagerung aus.</span><span class="sxs-lookup"><span data-stu-id="68735-133">Hide the labels of the lines for each grid overlay.</span></span> |  
    | **<span data-ttu-id="68735-134">Anzeigen von Positionsnummern</span><span class="sxs-lookup"><span data-stu-id="68735-134">Show line numbers</span></span>** | <span data-ttu-id="68735-135">Zeigen Sie die Nummern der Zeilen für jede Raster Überlagerung an \ (standardmäßig ausgewählt).</span><span class="sxs-lookup"><span data-stu-id="68735-135">Display the numbers of the lines for each grid overlay \(selected by default\).</span></span> |  
    | **<span data-ttu-id="68735-136">Anzeigen von Leitungsnamen</span><span class="sxs-lookup"><span data-stu-id="68735-136">Show line names</span></span>** | <span data-ttu-id="68735-137">Zeigen Sie die Namen der Zeilen für jede Raster Überlagerung an, wenn Namen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="68735-137">Display the names of the lines for each grid overlay when names are provided.</span></span> |  
    
*  <span data-ttu-id="68735-138">Aktivieren Sie das Kontrollkästchen neben den folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="68735-138">Choose the checkbox next the following options.</span></span>  
    
    | <span data-ttu-id="68735-139">Option</span><span class="sxs-lookup"><span data-stu-id="68735-139">Option</span></span> | <span data-ttu-id="68735-140">Details</span><span class="sxs-lookup"><span data-stu-id="68735-140">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="68735-141">Anzeigen von Titel Größen</span><span class="sxs-lookup"><span data-stu-id="68735-141">Show track sizes</span></span>**  | <span data-ttu-id="68735-142">Zeigen Sie die Größe der Tracks an, oder blenden Sie Sie aus.</span><span class="sxs-lookup"><span data-stu-id="68735-142">Display \(or hide\) the sizes of the tracks.</span></span> |  
    | **<span data-ttu-id="68735-143">Anzeigen von Bereichsnamen</span><span class="sxs-lookup"><span data-stu-id="68735-143">Show area names</span></span>** | <span data-ttu-id="68735-144">Zeigen Sie die Namen des Bereichs an, wenn Namen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="68735-144">Display \(or hide\) the names of the area, when names are provided.</span></span> |  
    | **<span data-ttu-id="68735-145">Erweitern von Rasterlinien</span><span class="sxs-lookup"><span data-stu-id="68735-145">Extend grid lines</span></span>** | <span data-ttu-id="68735-146">Zeigt die Erweiterungen der Raster Bemaßungen auf jeder Achse an.</span><span class="sxs-lookup"><span data-stu-id="68735-146">Displays \(or hides\) the extensions of the grid dimensions along each axis.</span></span>  <span data-ttu-id="68735-147">Standardmäßig werden Rasterlinien nur innerhalb des Elements angezeigt, wobei `display: grid` oder `display: inline-grid` CSS darauf gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="68735-147">By default, grid lines are only shown inside the element with `display: grid` or `display: inline-grid` CSS set on it.</span></span> |  
    
<span data-ttu-id="68735-148">Die folgenden Abschnitte enthalten Details zu den einzelnen **Overlay-Anzeigeeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="68735-148">The following sections provide details for each of the **Overlay display settings**.</span></span>  

### <span data-ttu-id="68735-149">Anzeigen von Positionsnummern</span><span class="sxs-lookup"><span data-stu-id="68735-149">Show line numbers</span></span>  

<span data-ttu-id="68735-150">Standardmäßig werden die Zahlen für positive und negative Linien auf der Raster Überlagerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68735-150">By default, the positive and negative line numbers are displayed on the grid overlay.</span></span>  

<span data-ttu-id="68735-151">Wenn Sie weitere Informationen zu negativen Zahlen in der Raster Überlagerung erhalten möchten, navigieren Sie zu [Zeile-basierter Platzierung mit CSS-Raster][MdnLineBasedPlacementCssGrid].</span><span class="sxs-lookup"><span data-stu-id="68735-151">For more information about negative numbers in the grid overlay, navigate to [Line-based placement with CSS Grid][MdnLineBasedPlacementCssGrid].</span></span>  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Anzeigen von Positionsnummern" lightbox="../media/grid-show-line-numbers.msft.png":::
   <span data-ttu-id="68735-153">Anzeigen von Positionsnummern</span><span class="sxs-lookup"><span data-stu-id="68735-153">Display line numbers</span></span>  
:::image-end:::  

### <span data-ttu-id="68735-154">Ausblenden von Strich Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="68735-154">Hide line labels</span></span>  

<span data-ttu-id="68735-155">Wählen Sie " **Leitungs Beschriftungen ausblenden** " aus, um die Positionsnummern auszublenden.</span><span class="sxs-lookup"><span data-stu-id="68735-155">Select **Hide line labels** to hide the line numbers.</span></span>  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Ausblenden von Strich Beschriftungen" lightbox="../media/grid-hide-line-labels.msft.png":::
   <span data-ttu-id="68735-157">Ausblenden von Strich Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="68735-157">Hide line labels</span></span>  
:::image-end:::  

### <span data-ttu-id="68735-158">Anzeigen von Leitungsnamen</span><span class="sxs-lookup"><span data-stu-id="68735-158">Show line names</span></span>  

<span data-ttu-id="68735-159">Weitere Informationen zu Linien Namen in der Raster Überlagerung finden Sie unter [Verwenden benannter Rasterlinien zum Layout][MdnLayoutUsingNamedGridLines].</span><span class="sxs-lookup"><span data-stu-id="68735-159">For more information about line names in the grid overlay, navigate to [Layout using named grid lines][MdnLayoutUsingNamedGridLines].</span></span>  

<span data-ttu-id="68735-160">Wählen Sie " **Leitungsnamen anzeigen** " aus, um die Namen der Zeile anstelle von Zahlen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="68735-160">Select **Show line names** to view the line names instead of numbers.</span></span>  <span data-ttu-id="68735-161">Im Beispiel haben 4 Zeilennamen: `left` , `middle1` , `middle2` und `right` .</span><span class="sxs-lookup"><span data-stu-id="68735-161">In the example, 4 lines have names: `left`, `middle1`, `middle2`, and `right`.</span></span>  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Anzeigen von Leitungsnamen" lightbox="../media/grid-show-line-names.msft.png":::
   **<span data-ttu-id="68735-163">Anzeigen von Leitungsnamen</span><span class="sxs-lookup"><span data-stu-id="68735-163">Show line names</span></span>**  
:::image-end:::  

### <span data-ttu-id="68735-164">Anzeigen von Titel Größen</span><span class="sxs-lookup"><span data-stu-id="68735-164">Show track sizes</span></span>  

<span data-ttu-id="68735-165">Aktivieren Sie das Kontrollkästchen " **Spur Größen anzeigen** ", um die Größe des Rasters anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="68735-165">Enable the **Show track sizes** checkbox to view the track sizes of the grid.</span></span>  

<span data-ttu-id="68735-166">DevTools wird `[authored size]` `[computed size]` in jeder Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68735-166">DevTools displays `[authored size]` and `[computed size]` in each line label.</span></span>  

| <span data-ttu-id="68735-167">Size</span><span class="sxs-lookup"><span data-stu-id="68735-167">Size</span></span> | <span data-ttu-id="68735-168">Details</span><span class="sxs-lookup"><span data-stu-id="68735-168">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="68735-169">Schriftgrad</span><span class="sxs-lookup"><span data-stu-id="68735-169">authored size</span></span>** | <span data-ttu-id="68735-170">Die in Stylesheet definierte Größe (wird ausgelassen, wenn Sie nicht definiert ist).</span><span class="sxs-lookup"><span data-stu-id="68735-170">The size defined in stylesheet \(omitted if not defined\).</span></span> |  
| **<span data-ttu-id="68735-171">berechnete Größe</span><span class="sxs-lookup"><span data-stu-id="68735-171">computed size</span></span>** | <span data-ttu-id="68735-172">Die tatsächliche Größe auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="68735-172">The actual size on screen.</span></span> |  

<span data-ttu-id="68735-173">In der Demo werden die `snack-box` Spaltengrößen im `grid-template-columns:1fr 2fr;` CSS definiert.</span><span class="sxs-lookup"><span data-stu-id="68735-173">In the demo, the `snack-box` column sizes are defined in the `grid-template-columns:1fr 2fr;` CSS.</span></span>  <span data-ttu-id="68735-174">Daher werden in den Spaltenbeschriftungen sowohl erstellte als auch berechnete Größen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68735-174">Therefore, the column line labels display both authored and computed sizes.</span></span>  

| <span data-ttu-id="68735-175">Titel Größe</span><span class="sxs-lookup"><span data-stu-id="68735-175">Track size</span></span> | <span data-ttu-id="68735-176">Schriftgrad</span><span class="sxs-lookup"><span data-stu-id="68735-176">Authored size</span></span> | <span data-ttu-id="68735-177">Berechnete Größe</span><span class="sxs-lookup"><span data-stu-id="68735-177">Computed size</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="68735-178">**1Fr** &#x2022; **96.66 px**</span><span class="sxs-lookup"><span data-stu-id="68735-178">**1fr** &#x2022; **96.66px**</span></span> | <span data-ttu-id="68735-179">1Fr</span><span class="sxs-lookup"><span data-stu-id="68735-179">1fr</span></span> | <span data-ttu-id="68735-180">96.66 px</span><span class="sxs-lookup"><span data-stu-id="68735-180">96.66px</span></span> |  
| <span data-ttu-id="68735-181">**2FR** &#x2022; **193.32 px**</span><span class="sxs-lookup"><span data-stu-id="68735-181">**2fr** &#x2022; **193.32px**</span></span> | <span data-ttu-id="68735-182">2fr</span><span class="sxs-lookup"><span data-stu-id="68735-182">2fr</span></span> | <span data-ttu-id="68735-183">193.32 px</span><span class="sxs-lookup"><span data-stu-id="68735-183">193.32px</span></span> |  

<span data-ttu-id="68735-184">Die Zeilenbeschriftungen zeigen nur berechnete Größen an, da im Stylesheet keine Zeilengrößen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="68735-184">The row line labels display only computed sizes, since there are no row sizes defined in the stylesheet.</span></span>  

| <span data-ttu-id="68735-185">Titel Größe</span><span class="sxs-lookup"><span data-stu-id="68735-185">Track size</span></span> | <span data-ttu-id="68735-186">Schriftgrad</span><span class="sxs-lookup"><span data-stu-id="68735-186">Authored size</span></span> | <span data-ttu-id="68735-187">Berechnete Größe</span><span class="sxs-lookup"><span data-stu-id="68735-187">Computed size</span></span> |  
|:--- |:--- |:--- |  
| **<span data-ttu-id="68735-188">80px</span><span class="sxs-lookup"><span data-stu-id="68735-188">80px</span></span>** | &nbsp;| <span data-ttu-id="68735-189">80px</span><span class="sxs-lookup"><span data-stu-id="68735-189">80px</span></span> |  
| **<span data-ttu-id="68735-190">80px</span><span class="sxs-lookup"><span data-stu-id="68735-190">80px</span></span>** | &nbsp;| <span data-ttu-id="68735-191">80px</span><span class="sxs-lookup"><span data-stu-id="68735-191">80px</span></span> |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Anzeigen von Titel Größen" lightbox="../media/grid-show-track-sizes.msft.png":::
   **<span data-ttu-id="68735-193">Anzeigen von Titel Größen</span><span class="sxs-lookup"><span data-stu-id="68735-193">Show track sizes</span></span>**  
:::image-end:::  

### <span data-ttu-id="68735-194">Anzeigen von Bereichsnamen</span><span class="sxs-lookup"><span data-stu-id="68735-194">Show area names</span></span>  

<span data-ttu-id="68735-195">Aktivieren Sie das Kontrollkästchen **Bereichsnamen anzeigen** , um die Bereichsnamen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="68735-195">To view the area names, enable the **Show area names** checkbox.</span></span>  <span data-ttu-id="68735-196">Im Beispiel gibt es drei Bereiche im Raster: **Top**, **bottom1** und **bottom2**.</span><span class="sxs-lookup"><span data-stu-id="68735-196">In the example, there are 3 areas in the grid: **top**, **bottom1** and **bottom2**.</span></span>  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Anzeigen von Bereichsnamen" lightbox="../media/grid-show-area-names.msft.png":::
   **<span data-ttu-id="68735-198">Anzeigen von Bereichsnamen</span><span class="sxs-lookup"><span data-stu-id="68735-198">Show area names</span></span>**  
:::image-end:::  

### <span data-ttu-id="68735-199">Erweitern von Rasterlinien</span><span class="sxs-lookup"><span data-stu-id="68735-199">Extend grid lines</span></span>  

<span data-ttu-id="68735-200">Aktivieren Sie das Kontrollkästchen **Rasterlinien erweitern** , um die Rasterlinien entlang der einzelnen Achsen an den Rand des Viewports zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="68735-200">Enable the **Extend grid lines** checkbox to extend the grid lines to the edge of the viewport along each axis.</span></span>  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Erweitern von Rasterlinien" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **<span data-ttu-id="68735-202">Erweitern von Rasterlinien</span><span class="sxs-lookup"><span data-stu-id="68735-202">Extend grid lines</span></span>**  
:::image-end:::  

## <span data-ttu-id="68735-203">Raster Überlagerungen</span><span class="sxs-lookup"><span data-stu-id="68735-203">Grid overlays</span></span>  

<span data-ttu-id="68735-204">Der Abschnitt **Raster Überlagerungen** enthält eine Liste der auf der Seite vorhandenen Raster, die jeweils ein Kontrollkästchen sowie verschiedene Optionen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="68735-204">The **Grid overlays** section contains a list of grids that are present on the page, each with a checkbox, along with various options.</span></span>  

### <span data-ttu-id="68735-205">Aktivieren von überlagerungsansichten mehrerer Raster</span><span class="sxs-lookup"><span data-stu-id="68735-205">Enable overlay views of multiple grids</span></span>  

<span data-ttu-id="68735-206">Um das Overlay-Raster für mehrere Raster anzuzeigen, aktivieren Sie das Kontrollkästchen neben jedem Namen des Rasters.</span><span class="sxs-lookup"><span data-stu-id="68735-206">To display the overlay grid for multiple grids, choose the checkbox next to each name of the grid.</span></span>  <span data-ttu-id="68735-207">Im Beispiel sind zwei Raster Überlagerungen aktiviert, die jeweils mit unterschiedlichen Farben dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="68735-207">In the example, there are 2 grid overlays enabled that are each represented with different colors.</span></span>  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Aktivieren von überlagerungsansichten mehrerer Raster" lightbox="../media/grid-grid-overlays.msft.png":::
   <span data-ttu-id="68735-209">Aktivieren von überlagerungsansichten mehrerer Raster</span><span class="sxs-lookup"><span data-stu-id="68735-209">Enable overlay views of multiple grids</span></span>  
:::image-end:::  

### <span data-ttu-id="68735-210">Anpassen der Raster Überlagerungsfarbe</span><span class="sxs-lookup"><span data-stu-id="68735-210">Customize the grid overlay color</span></span>  

<span data-ttu-id="68735-211">Wenn Sie die Farbauswahl öffnen und die Raster Überlagerungsfarbe anpassen möchten, aktivieren Sie das Kontrollkästchen neben dem Namen der Raster Überlagerung.</span><span class="sxs-lookup"><span data-stu-id="68735-211">To open the color picker and customize the grid overlay color, choose the box next to the name of the grid overlay.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Anpassen der Raster Überlagerungsfarbe" lightbox="../media/grid-grid-overlays-color.msft.png":::
   <span data-ttu-id="68735-213">Anpassen der Raster Überlagerungsfarbe</span><span class="sxs-lookup"><span data-stu-id="68735-213">Customize the grid overlay color</span></span>  
:::image-end:::  

### <span data-ttu-id="68735-214">Markieren des Rasters</span><span class="sxs-lookup"><span data-stu-id="68735-214">Highlight the grid</span></span>  

<span data-ttu-id="68735-215">Wenn Sie das HTML-Element im **Element Panel hervor** heben und auf der Webseite zu ihm Scrollen möchten, wählen Sie im **Panel Elemente** das Element anzeigen aus, und klicken Sie auf der Symbolleiste des Elements ![ Panels auf Symbol ][ImageShowElementInElementsPanelIcon] .</span><span class="sxs-lookup"><span data-stu-id="68735-215">To highlight the HTML element in the **Elements** panel and scroll to it on the webpage, choose the **Show element in the Elements panel** \(![Show element in the Elements panel icon][ImageShowElementInElementsPanelIcon]\) icon.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Markieren des Rasters" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   <span data-ttu-id="68735-217">Markieren des Rasters</span><span class="sxs-lookup"><span data-stu-id="68735-217">Highlight the grid</span></span>  
:::image-end:::  

## <span data-ttu-id="68735-218">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="68735-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "CSS-Raster | JEC. FYI"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "CSS-Raster | JEC. FYI"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "CSS-Raster Layout | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Layout mit benannten Rasterlinien | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Linien basierte Platzierung mit CSS-Raster | MDN"  

> [!NOTE]
> <span data-ttu-id="68735-225">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68735-225">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="68735-226">Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/grid) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="68735-226">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/grid) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="68735-228">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="68735-228">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

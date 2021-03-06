---
description: Erfahren Sie, wie Sie Microsoft Edge DevTools zum Anzeigen und Ändern der CSS einer Seiten-CSS verwenden.
title: Überprüfen des CSS-Rasters in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 5e4b20690eac3a692f6428f391def102a4f78ecb
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398770"
---
# <a name="inspect-css-grid"></a>Überprüfen des CSS-Rasters  

In diesem Artikel werden Sie durch das Identifizieren von CSS-Rastern auf einer Website und das Debuggen von Rasterlayoutproblemen mithilfe anpassbarer Rasterüberlagerungen erläutert.  

Die In den Abbildungen in diesem Artikel verwendeten Beispiele sind den folgenden Webseiten zu finden.  

*   [Obstfeld][JecFyiDemoCssGridFruit]  
*   [Feld "ImBiss"][JecFyiDemoCssGridSnack]  

## <a name="before-you-begin"></a>Vorbemerkungen  

CSS Grid ist ein leistungsfähiges Layoutparadigma für das Web.  Ein großartiger Ort, um sich mit css Grid und den vielen Features zu beginnen, ist die [CSS Grid Layout-Anleitung][MdnCssGridLayout] auf MDN.  

## <a name="discover-css-grids"></a>Entdecken von CSS-Rastern  

Wenn ein HTML-Element auf Ihrer Seite darauf angewendet wurde oder darauf angewendet wurde, wird daneben im Bereich Elemente ein Signal `display: grid` `display: inline-grid` `grid` angezeigt. [][DevtoolsGuideChromiumOpen]  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Raster ermitteln" lightbox="../media/grid-discover-grid.msft.png":::
   Raster ermitteln  
:::image-end:::  

Wählen Sie das Signal aus, um die Anzeige einer Rasterüberlagerung auf der Seite umschalten zu können.  Die Überlagerung wird über dem Element angezeigt, das wie ein Raster ausgelegt ist, um die Position der Gitternetzlinien und -spuren zu zeigen:  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Gitternetzabzeichen umschalten" lightbox="../media/grid-highlight-grid.msft.png":::
   Gitternetzabzeichen umschalten  
:::image-end:::  

Öffnen Sie den **Bereich Layout.**  Wenn Raster auf einer Seite enthalten sind, enthält der **Layoutbereich** einen **Abschnitt Grid** mit einer Reihe von Optionen zum Anzeigen der Raster.  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Layoutbereich" lightbox="../media/grid-layout-pane.msft.png":::
   **Layoutbereich**  
:::image-end:::  

Der **Abschnitt Grid** im **Layoutbereich** enthält die folgenden 2 Unterabschnitte.  

*   Überlagerungsanzeigeeinstellungen  
*   Rasterüberlagerungen  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <a name="overlay-display-settings"></a>Überlagerungsanzeigeeinstellungen  

Die **Überlagerungsanzeigeeinstellungen** bestehen aus den folgenden 2 Teilen.  

*   Wählen Sie im Dropdownmenü eine der folgenden Optionen aus.  
    
    | Line-Option | Details |  
    |:--- |:--- |  
    | **Ausblenden von Linienbeschriftungen** | Blenden Sie die Beschriftungen der Linien für jede Rasterüberlagerung aus. |  
    | **Anzeigen von Zeilennummern** | Zeigt die Nummern der Zeilen für jede Rasterüberlagerung \(standardmäßig ausgewählt\) an. |  
    | **Anzeigen von Zeilennamen** | Zeigt die Namen der Zeilen für jede Rasterüberlagerung an, wenn Namen angegeben werden. |  
    
*  Aktivieren Sie das Kontrollkästchen neben den folgenden Optionen.  
    
    | Option | Details |  
    |:--- |:--- |  
    | **Anzeigen von Titelgrößen**  | Zeigen Sie \(oder ausblenden\) die Größen der Titel an. |  
    | **Anzeigen von Bereichsnamen** | Zeigen Sie \(oder ausblenden\) die Namen des Bereichs an, wenn Namen angegeben werden. |  
    | **Erweitern von Gitternetzlinien** | Zeigt \(oder blendet\) die Erweiterungen der Rasterdimensionen entlang jeder Achse an.  Standardmäßig werden Gitternetzlinien nur innerhalb des Elements angezeigt, für das `display: grid` `display: inline-grid` css festgelegt ist. |  
    
In den folgenden Abschnitten finden Sie Details für jede der **Überlagerungsanzeigeeinstellungen.**  

### <a name="show-line-numbers"></a>Anzeigen von Zeilennummern  

Standardmäßig werden die positiven und negativen Zeilennummern auf der Rasterüberlagerung angezeigt.  

Weitere Informationen zu negativen Zahlen in der Rasterüberlagerung finden Sie unter [Line-based placement with CSS Grid][MdnLineBasedPlacementCssGrid].  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Anzeigen von Zeilennummern" lightbox="../media/grid-show-line-numbers.msft.png":::
   Anzeigen von Zeilennummern  
:::image-end:::  

### <a name="hide-line-labels"></a>Ausblenden von Linienbeschriftungen  

Wählen **Sie Zeilenbeschriftungen ausblenden aus,** um die Zeilennummern auszublenden.  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Ausblenden von Linienbeschriftungen" lightbox="../media/grid-hide-line-labels.msft.png":::
   Ausblenden von Linienbeschriftungen  
:::image-end:::  

### <a name="show-line-names"></a>Anzeigen von Zeilennamen  

Weitere Informationen zu Liniennamen in der Rasterüberlagerung finden Sie unter [Layout mit benannten Gitternetzlinien.][MdnLayoutUsingNamedGridLines]  

Wählen **Sie Zeilennamen anzeigen aus,** um die Zeilennamen anstelle von Zahlen anzeigen.  Im Beispiel haben 4 Zeilen Namen: `left` , , , und `middle1` `middle2` `right` .  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Anzeigen von Zeilennamen" lightbox="../media/grid-show-line-names.msft.png":::
   **Anzeigen von Zeilennamen**  
:::image-end:::  

### <a name="show-track-sizes"></a>Anzeigen von Titelgrößen  

Aktivieren Sie das **Kontrollkästchen Titelgrößen anzeigen,** um die Titelgrößen des Rasters anzeigen.  

DevTools zeigt `[authored size]` und `[computed size]` in jeder Zeilenbeschriftung an.  

| Size | Details |  
|:--- |:--- |  
| **Erstellungsgröße** | Die größe, die in stylesheet \(omitted if not defined\) definiert ist. |  
| **berechnete Größe** | Die tatsächliche Größe auf dem Bildschirm. |  

In der Demo werden `snack-box` die Spaltengrößen im CSS `grid-template-columns:1fr 2fr;` definiert.  Daher werden in den Spaltenlinienbeschriftungen sowohl die erstellungs- als auch die berechnete Größe angezeigt.  

| Track-Größe | Größe des Autors | Berechnete Größe |  
|:--- |:--- |:--- |  
| **1fr** &#x2022; **96,66px** | 1fr | 96,66px |  
| **2fr** &#x2022; **193.32px** | 2fr | 193.32px |  

Die Zeilenlinienbeschriftungen zeigen nur berechnete Größen an, da im Stylesheet keine Zeilengrößen definiert sind.  

| Track-Größe | Größe des Autors | Berechnete Größe |  
|:--- |:--- |:--- |  
| **80px** | &nbsp;| 80px |  
| **80px** | &nbsp;| 80px |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Anzeigen von Titelgrößen" lightbox="../media/grid-show-track-sizes.msft.png":::
   **Anzeigen von Titelgrößen**  
:::image-end:::  

### <a name="show-area-names"></a>Anzeigen von Bereichsnamen  

Aktivieren Sie zum Anzeigen der Bereichsnamen das Kontrollkästchen **Bereichsnamen** anzeigen.  Im Beispiel sind drei Bereiche im Raster: **oben,** **unten1** und **unten2**.  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Anzeigen von Bereichsnamen" lightbox="../media/grid-show-area-names.msft.png":::
   **Anzeigen von Bereichsnamen**  
:::image-end:::  

### <a name="extend-grid-lines"></a>Erweitern von Gitternetzlinien  

Aktivieren Sie **das Kontrollkästchen Gitternetzlinien** erweitern, um die Gitternetzlinien bis zum Rand des Viewports entlang jeder Achse zu erweitern.  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Erweitern von Gitternetzlinien" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **Erweitern von Gitternetzlinien**  
:::image-end:::  

## <a name="grid-overlays"></a>Rasterüberlagerungen  

Der **Abschnitt Rasterüberlagerungen** enthält eine Liste der Raster, die auf der Seite vorhanden sind, jeweils mit einem Kontrollkästchen sowie verschiedenen Optionen.  

### <a name="enable-overlay-views-of-multiple-grids"></a>Aktivieren von Überlagerungsansichten mehrerer Raster  

Wenn Sie das Überlagerungsraster für mehrere Raster anzeigen möchten, aktivieren Sie das Kontrollkästchen neben jedem Namen des Rasters.  Im Beispiel sind zwei Rasterüberlagerungen aktiviert, die jeweils mit unterschiedlichen Farben dargestellt werden.  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Aktivieren von Überlagerungsansichten mehrerer Raster" lightbox="../media/grid-grid-overlays.msft.png":::
   Aktivieren von Überlagerungsansichten mehrerer Raster  
:::image-end:::  

### <a name="customize-the-grid-overlay-color"></a>Anpassen der Rasterüberlagerungsfarbe  

Um die Farbauswahl zu öffnen und die Rasterüberlagerungsfarbe anzupassen, wählen Sie das Feld neben dem Namen der Rasterüberlagerung aus.  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Anpassen der Rasterüberlagerungsfarbe" lightbox="../media/grid-grid-overlays-color.msft.png":::
   Anpassen der Rasterüberlagerungsfarbe  
:::image-end:::  

### <a name="highlight-the-grid"></a>Hervorheben des Rasters  

Um das HTML-Element **** im Elementtool zu markieren und auf der Webseite zu diesem zu scrollen, wählen Sie das Element Anzeigen **im** Bereich Elemente \( Element anzeigen im Elementbereichssymbol ![ ][ImageShowElementInElementsPanelIcon] \) aus.  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Hervorheben des Rasters" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   Hervorheben des Rasters  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Öffnen Sie Microsoft Edge DevTools | Microsoft Docs"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "CSS-Raster | jec.fyi"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "CSS-Raster | jec.fyi"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "CSS Grid Layout | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Layout mit benannten Gitternetzlinien | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Zeilenbasierte Platzierung mit CSS Grid | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/grid) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

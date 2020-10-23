---
description: Erfahren Sie, wie Sie Microsoft Edge devtools verwenden, um das CSS einer Seite CSS anzuzeigen und zu ändern.
title: Überprüfen des CSS-Rasters in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 150aea57aa676580b554cc74292671ed567a0a2c
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134058"
---
# Überprüfen des CSS-Rasters  

In diesem Artikel wird erläutert, wie Sie CSS-Raster auf einer Website identifizieren und Probleme mit Rasterlayouts mithilfe anpassbarer Raster Überlagerungen Debuggen.  

Die in den Abbildungen in diesem Artikel verwendeten Beispiele sind den folgenden Webseiten zu entgenommen.  

*   [Obst Kasten][JecFyiDemoCssGridFruit]  
*   [Snack-Box][JecFyiDemoCssGridSnack]  

## Vorbemerkungen  

CSS-Raster ist ein leistungsfähiges Layout-Paradigma für das Web.  Ein toller Ort, um mit dem Erlernen des CSS-Rasters und der vielen Features vertraut zu werden, ist die [CSS-Raster Layout-Anleitung][MdnCssGridLayout] auf MDN.  

## Entdecken von CSS-Rastern  

Wenn auf der Seite ein HTML-Element auf der Seite `display: grid` `display: inline-grid` angelegt oder angewendet wurde, `grid` wird im [Element][DevtoolsGuideChromiumOpen] Panel daneben ein Badge angezeigt.  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-discover-grid.msft.png":::
   Raster entdecken  
:::image-end:::  

Wählen Sie das Abzeichen aus, um die Anzeige einer Raster Überlagerung auf der Seite umzuschalten.  Die Überlagerung wird über dem Element dargestellt, wie ein Raster angeordnet, um die Position der Rasterlinien und Titel anzuzeigen:  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-highlight-grid.msft.png":::
   Rastersignal umschalten  
:::image-end:::  

Öffnen Sie den Bereich " **Layout** ".  Wenn Raster auf einer Seite enthalten sind, enthält der Bereich **Layout** einen **Raster** Abschnitt, der eine Reihe von Optionen zum Anzeigen der Raster enthält.  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-layout-pane.msft.png":::
   Bereich ' **Layout** '  
:::image-end:::  

Der Abschnitt " **Raster** " im Bereich " **Layout** " enthält die folgenden 2 Unterabschnitte.  

*   Anzeigeeinstellungen für Overlays  
*   Raster Überlagerungen  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## Anzeigeeinstellungen für Overlays  

Die **Einstellungen** für die Overlay-Anzeige bestehen aus zwei Teilen.  

*   Wählen Sie eine der folgenden Optionen aus dem Dropdown-Menü aus.  
    
    | Option "Zeile" | Details |  
    |:--- |:--- |  
    | **Ausblenden von Strich Beschriftungen** | Blenden Sie die Beschriftungen der Linien für jede Raster Überlagerung aus. |  
    | **Anzeigen von Positionsnummern** | Zeigen Sie die Nummern der Zeilen für jede Raster Überlagerung an \ (standardmäßig ausgewählt). |  
    | **Anzeigen von Leitungsnamen** | Zeigen Sie die Namen der Zeilen für jede Raster Überlagerung an, wenn Namen bereitgestellt werden. |  
    
*  Aktivieren Sie das Kontrollkästchen neben den folgenden Optionen.  
    
    | Option | Details |  
    |:--- |:--- |  
    | **Anzeigen von Titel Größen**  | Zeigen Sie die Größe der Tracks an, oder blenden Sie Sie aus. |  
    | **Anzeigen von Bereichsnamen** | Zeigen Sie die Namen des Bereichs an, wenn Namen bereitgestellt werden. |  
    | **Erweitern von Rasterlinien** | Zeigt die Erweiterungen der Raster Bemaßungen auf jeder Achse an.  Standardmäßig werden Rasterlinien nur innerhalb des Elements angezeigt, wobei `display: grid` oder `display: inline-grid` CSS darauf gesetzt ist. |  
    
Die folgenden Abschnitte enthalten Details zu den einzelnen **Overlay-Anzeigeeinstellungen**.  

### Anzeigen von Positionsnummern  

Standardmäßig werden die Zahlen für positive und negative Linien auf der Raster Überlagerung angezeigt.  

Wenn Sie weitere Informationen zu negativen Zahlen in der Raster Überlagerung erhalten möchten, navigieren Sie zu [Zeile-basierter Platzierung mit CSS-Raster][MdnLineBasedPlacementCssGrid].  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-show-line-numbers.msft.png":::
   Anzeigen von Positionsnummern  
:::image-end:::  

### Ausblenden von Strich Beschriftungen  

Wählen Sie " **Leitungs Beschriftungen ausblenden** " aus, um die Positionsnummern auszublenden.  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-hide-line-labels.msft.png":::
   Ausblenden von Strich Beschriftungen  
:::image-end:::  

### Anzeigen von Leitungsnamen  

<!--todo: @rachel verify the link and text for line name -->  
Weitere Informationen zu Linien Namen in der Raster Überlagerung finden Sie unter [Verwenden benannter Rasterlinien zum Layout][MdnLayoutUsingNamedGridLines].  

Wählen Sie " **Leitungsnamen anzeigen** " aus, um die Namen der Zeile anstelle von Zahlen anzuzeigen.  Im Beispiel haben 4 Zeilennamen: `left` , `middle1` , `middle2` und `right` .  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-show-line-names.msft.png":::
   **Anzeigen von Leitungsnamen**  
:::image-end:::  

### Anzeigen von Titel Größen  

Aktivieren Sie das Kontrollkästchen " **Spur Größen anzeigen** ", um die Größe des Rasters anzuzeigen.  

DevTools wird `[authored size]` `[computed size]` in jeder Zeile angezeigt.  

| Size | Details |  
|:--- |:--- |  
| **Schriftgrad** | Die in Stylesheet definierte Größe (wird ausgelassen, wenn Sie nicht definiert ist). |  
| **berechnete Größe** | Die tatsächliche Größe auf dem Bildschirm. |  

In der Demo werden die `snack-box` Spaltengrößen im `grid-template-columns:1fr 2fr;` CSS definiert.  Daher werden in den Spaltenbeschriftungen sowohl erstellte als auch berechnete Größen angezeigt.  

| Titel Größe | Schriftgrad | Berechnete Größe |  
|:--- |:--- |:--- |  
| **1Fr** &#x2022; **96.66 px** | 1Fr | 96.66 px |  
| **2FR** &#x2022; **193.32 px** | 2fr | 193.32 px |  

Die Zeilenbeschriftungen zeigen nur berechnete Größen an, da im Stylesheet keine Zeilengrößen definiert sind.  

| Titel Größe | Schriftgrad | Berechnete Größe |  
|:--- |:--- |:--- |  
| **80px** | &nbsp;| 80px |  
| **80px** | &nbsp;| 80px |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-show-track-sizes.msft.png":::
   **Anzeigen von Titel Größen**  
:::image-end:::  

### Anzeigen von Bereichsnamen  

Aktivieren Sie das Kontrollkästchen **Bereichsnamen anzeigen** , um die Bereichsnamen anzuzeigen.  Im Beispiel gibt es drei Bereiche im Raster: **Top**, **bottom1** und **bottom2**.  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-show-area-names.msft.png":::
   **Anzeigen von Bereichsnamen**  
:::image-end:::  

### Erweitern von Rasterlinien  

Aktivieren Sie das Kontrollkästchen **Rasterlinien erweitern** , um die Rasterlinien entlang der einzelnen Achsen an den Rand des Viewports zu erweitern.  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **Erweitern von Rasterlinien**  
:::image-end:::  

## Raster Überlagerungen  

Der Abschnitt **Raster Überlagerungen** enthält eine Liste der auf der Seite vorhandenen Raster, die jeweils ein Kontrollkästchen sowie verschiedene Optionen aufweisen.  

### Aktivieren von überlagerungsansichten mehrerer Raster  

<!--todo: @zoher verify and provide updates -->  

Um das Overlay-Raster für mehrere Raster anzuzeigen, aktivieren Sie das Kontrollkästchen neben jedem Namen des Rasters.  Im Beispiel sind zwei Raster Überlagerungen aktiviert, die jeweils mit unterschiedlichen Farben dargestellt werden.  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-grid-overlays.msft.png":::
   Aktivieren von überlagerungsansichten mehrerer Raster  
:::image-end:::  

### Anpassen der Raster Überlagerungsfarbe  

Wenn Sie die Farbauswahl öffnen und die Raster Überlagerungsfarbe anpassen möchten, aktivieren Sie das Kontrollkästchen neben dem Namen der Raster Überlagerung.  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-grid-overlays-color.msft.png":::
   Anpassen der Raster Überlagerungsfarbe  
:::image-end:::  

### Markieren des Rasters  

Wenn Sie das HTML-Element im **Element Panel hervor** heben und auf der Webseite zu ihm Scrollen möchten, wählen Sie im **Panel Elemente** das Element anzeigen aus, und klicken Sie auf der Symbolleiste des Elements ![ Panels auf Symbol ][ImageShowElementInElementsPanelIcon] .  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Raster entdecken" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   Markieren des Rasters  
:::image-end:::  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "CSS-Raster | JEC. FYI"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "CSS-Raster | JEC. FYI"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "CSS-Raster Layout | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Layout mit benannten Rasterlinien | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Linien basierte Platzierung mit CSS-Raster | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/css/grid) gefunden und von [Jecelyn Yeen][JecelynYeen] \ (Developer Advocate, Chrome devtools \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

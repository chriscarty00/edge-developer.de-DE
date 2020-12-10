---
description: Alles zur 3D-Ansicht und deren Verwendung.
title: 3D View
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: bd91939a19f02a426834a85ef92eca388f8f1eda
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "11203970"
---
# 3D View  

Verwenden Sie die **3D-Ansicht** , um Ihre Web-App zu debuggen, indem Sie durch das [Dokumentobjektmodell (DOM)][MDNDocumentObjectModel] oder den Stapel Kontext des [z-Index][MDNZIndex] navigieren.  Damit können Sie die folgenden Aufgaben ausführen:  

*   [Erkunden der in eine 3D-Perspektive übersetzten Webseite](#3d-dom)  
*   [Debuggen basierend auf dem Stapeln des z-Index-Kontexts](#z-index)  
*   [Zugreifen auf die Funktionen des Layer-Tools aus der 3D-Ansicht mit zusammengesetzten Ebenen](#composited-layers)  
*   [Löschen eines Teils der Übersichtlichkeit im Dom-Bereich](#changing-your-view) oder im [Bereich "z-index"](#change-the-scope-of-your-exploration)  
*   [Das Farbschema zum besten Debuggen von Dom](#dom-color-type) [-oder z-Index Problemen](#z-index-color-type) aussuchen  

Wenn Sie einen frühen Prototyp eines 3D-Ansichts Projekts erkunden und den Code selbst ausführen möchten, navigieren Sie zu [3D-Ansicht-Beispiel][GithubMicrosoftedgeDevtoolssamples3dview].  

Auf der linken Seite gibt es drei Bereiche, die Sie für die Fehlerbehebung verwenden können.  

*   Der Bereich " [Z-Index](#z-index) "  Navigieren Sie durch die verschiedenen Elemente in der Web-App, wobei der z-Index-Kontext berücksichtigt wird.  Der Bereich " **Z-Index** " ist der Standardbereich.  
*   Der [3D-Dom-](#3d-dom) Bereich.  Erkunden Sie das DOM als Ganzes, wobei alle Elemente leicht zugänglich sind.  Um auf den Bereich zuzugreifen, wählen Sie den Bereich **DOM** neben dem Bereich **Z-Index** aus.  
*   Der Bereich " [zusammengesetzte Ebenen](#composited-layers) "  Fügen Sie ein weiteres 3D-Element hinzu, um aus einer Ebenen Perspektive ein umfassenderes Erlebnis zu erzielen.  Um auf den Bereich zuzugreifen, wählen Sie den Bereich **zusammengesetzte Ebenen** neben dem **DOM** -Bereich aus.  
    
Auf der rechten Seite zeigt die Leinwand Ihre Auswahl aus dem [Z-Index](#z-index), [3D-Dom](#3d-dom)oder [zusammengesetzten Layern](#composited-layers)an.  

## Navigieren im Arbeitsbereich  

:::image type="complex" source="../media/3d-view-canvas.msft.png" alt-text="Leinwand der 3D-Ansicht" lightbox="../media/3d-view-canvas.msft.png":::
   Leinwand der 3D-Ansicht  
:::image-end:::  

### Tastenkombinationen  

*   Drehen des Dom: um horizontal zu rotieren, wählen Sie die `left-arrow` Tasten und aus `right-arrow` .  Wenn Sie vertikal drehen möchten, wählen Sie die `up-arrow` Tasten und aus `down-arrow` .  
*   Navigieren im Dom: um die benachbarten Elemente zu durchlaufen, wählen Sie ein Element aus, und wählen Sie die `up-arrow` Tasten und aus `down-arrow` .  

### Maussteuerungen  

*   Drehen des Dom: Wählen Sie den Zeichenbereich aus, und ziehen Sie ihn.  
*   Schwenken um das DOM: Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und ziehen Sie den Mauszeiger in die Richtung, in die das DOM verschoben werden soll.  
*   Zoom: ziehen Sie zwei Finger über das Touchpad, oder verwenden Sie das Mausrad auf der Maus.  

### Steuerelemente auf dem Bildschirm  

:::image type="complex" source="../media/3d-view-controls-small.msft.png" alt-text="Steuerelemente auf dem Bildschirm" lightbox="../media/3d-view-controls-small.msft.png":::
   Steuerelemente auf dem Bildschirm  
:::image-end:::  

*   Setzen Sie die Leinwandansicht auf die ursprüngliche Ansicht zurück: Wählen Sie die Schaltfläche **Kamera zurücksetzen** aus, oder wählen Sie die Schaltfläche **Elemente zurücksetzen in Ansicht und Re-Center-Kamera** \ (seitliches Aktualisierungssymbol \) aus.  
*   Aktualisieren Sie die Leinwand \ (wenn sich beispielsweise der Browser geändert hat oder Sie zu einer Geräte emulatoransicht gewechselt sind \): Wählen Sie die Schaltfläche Snapshot erneut über **nehmen** aus, oder klicken Sie auf die Schaltfläche **neuen Schnappschuss aufnehmen** \ (Symbol "Aktualisieren" \).  

## Z-Index  

:::image type="complex" source="../media/3d-view-z-index-view-box.msft.png" alt-text="Z-Indexansicht" lightbox="../media/3d-view-z-index-view-box.msft.png":::
   Z-Indexansicht  
:::image-end:::  

Während der Bereich " **Z-Index** " über freigegebene Features mit dem **3D-Dom** -Bereich verfügt, verfügen die Bereiche weiterhin über Elemente, die für den Bereich eindeutig sind.  

### Markieren von Elementen mit Stapel Kontext  

Mit der Einstellung " **Highlight-Elemente mit Stapel Kontext** " können Sie die z-Index-Tags für die Elemente auf der Leinwand auf \ (und Off \) aktivieren.  Das Kontrollkästchen ist standardmäßig ausgewählt.  

### Ändern des Umfangs ihrer Exploration  

Die Schaltfläche **alle Elemente anzeigen** ist die schnellste Möglichkeit, alle Elemente des DOM anzuzeigen, nachdem die Einstellungen darunter geändert wurden.  

Mit der Schaltfläche **nur Elemente mit Stapel-Kontext anzeigen** werden Elemente ohne Stapel Kontext entfernt, und das DOM wird vereinfacht, um die Navigation zu vereinfachen.  

Die Schaltfläche " **ausgewähltes Element isolieren** " besteht im Wesentlichen aus drei Schaltflächen in einer.  Es gibt zwei Kontrollkästchen unter der Schaltfläche " **ausgewähltes Element isolieren** ": das Kontrollkästchen " **alle übergeordneten Elemente anzeigen** " und " **nur Eltern mit neuem Stapel-Kontext beibehalten** ".  

Das Kontrollkästchen **alle übergeordneten Elemente anzeigen** ist standardmäßig aktiviert.  Wenn Sie das Element und alle übergeordneten Elemente im Canvas-Bereich anzeigen möchten, wählen Sie ein Element aus, und wählen Sie die Schaltfläche **ausgewähltes Element isolieren** aus.  

Um das Element und die übergeordneten Elemente anzuzeigen, die über einen neuen Stapel Kontext auf der Leinwand verfügen, aktivieren Sie die Einstellung **nur übergeordnete Elemente mit neuem Stapel Kontext beibehalten** , und wählen Sie die Schaltfläche **ausgewähltes Element isolieren** aus.  

Um das Element anzuzeigen, das Sie im Zeichenbereich ausgewählt haben, deaktivieren Sie die beiden Einstellungen, und wählen Sie die Schaltfläche **ausgewähltes Element isolieren** aus.  

Suchen Sie am unteren Rand des **3D-Dom-** Bereichs nach dem Kontrollkästchen **Elemente ausblenden mit der gleichen Farbreihenfolge wie das übergeordnete Element** .  Durch auswählen und Aufheben der Auswahl des Kontrollkästchens werden die Elemente basierend auf Ihrer Auswahl aktualisiert.  Wenn Sie ausgewählt sind, werden Elemente, die die Farbreihenfolge freigeben, auf das übergeordnete Element reduziert.  

Die Optionen sollen einige der Übersichtlichkeit aufklären, die komplexere Webseiten in ihrer Leinwand erstellen.  

### Z-Index-Farbtyp  

Das sind die verschiedenen Visualisierungen, die Sie für das DOM in ihrer Leinwand verwenden können.  Ganz gleich, ob Sie es zum Spaß verwenden oder weil die Visualisierungen Ihnen dabei helfen, das DOM besser zu visualisieren, haben die devtools unterschiedliche Farb Farben und die Option " **Hintergrundfarbe verwenden** ".  Der Bereich " **Z-Index** " teilt die **lila-weiß** -und die **Hintergrundfarbe** mit dem **3D-Dom** -Bereich.  Angesichts des hinzugefügten visuellen Elements der z-Index Beschriftungen hat Ihr Feedback zu einer Verringerung der Anzahl der Farboptionen geführt.  Die neue Einfachheit verbessert das Debuggen von z-index.  Über die Optionsfelder können Sie die Optionen durchlaufen und den gewünschten Farbtyp wählen.  Der Farbtyp ist entweder am besten für Ihr Projekt geeignet oder für ein Projekt, das Ihnen am besten gefällt.  

## 3D-Dom  

:::image type="complex" source="../media/3d-view-dom-purple-box.msft.png" alt-text="DOM-Ansicht" lightbox="../media/3d-view-dom-purple-box.msft.png":::
   DOM-Ansicht  
:::image-end:::  

Wenn Sie eine allgemeine Debugansicht anstelle der z-Index-Oberfläche nutzen möchten, bietet das 3D- **DOM** eine Gesamtdarstellung des DOM.  Da der Kontext des z-Index entfernt wird, wird das DOM genauer und übersichtlicher gestapelt.  Der **3D-Dom-** Bereich hat eine ähnliche Funktionalität, aber es gibt ein paar Nuancen.  

### Ändern der Ansicht  

Im **3D-Dom-** Bereich enthält die Schaltfläche **ausgewählte Elemente isolieren** unter **geordnete** Kontrollkästchen und übergeordnete **Elemente einbeziehen.**  Beide Kontrollkästchen sind standardmäßig aktiviert.  Das heißt, wenn Sie die Schaltfläche " **ausgewähltes Element isolieren** " auswählen, nachdem Sie ein Element ausgewählt haben, zeigt der Canvas das ausgewählte Element, die übergeordneten Elemente des Elements und die untergeordneten Elemente des Elements an.  Deaktivieren Sie die Einstellung unter **geordnete Elemente einbeziehen** , und wählen Sie die Schaltfläche **ausgewähltes Element isolieren** erneut aus, um das ausgewählte Element und die übergeordneten Elemente des Elements anzuzeigen.  Wenn Sie die Einstellung " **Kinder einbeziehen** " aktivieren und die Einstellung " **Eltern einbeziehen** " deaktivieren und dann die Schaltfläche " **ausgewähltes Element isolieren** " auswählen, werden im Arbeitsbereich das Element und alle untergeordneten Elemente angezeigt.  Wenn Sie beide Einstellungen deaktivieren und die Schaltfläche " **ausgewähltes Element isolieren** " auswählen, zeigt der Canvas nur das zuvor ausgewählte Element an.  

Ein Schieberegler im Steuerbereich mit dem Namen " **Schachtelungsebene für Seite** mit einer Zahl daneben".  Die Zahl gibt die Anzahl der Layer für das Dokument an.  Wenn Sie den Schieberegler nach links ziehen, werden die äußersten Ebenen entfernt, bis Sie mit einer Verschachtelungsebene auf gesetzt sind `1` , die nur das am weitesten zurückliegende Element im Dom anzeigt.  Ziehen Sie den Schieberegler, um einen Teil der Verwirrung zu entfernen.  Es hilft Ihnen, sich genauer anzusehen, was in den unteren Ebenen passiert.  

### Dom-Farbtyp  

Der **3D-Dom-** Bereich zeigt die folgenden Optionen an:  

*   Drei verschiedene Farbgebungen.  
    *   **Heatmapfarbgebung-lila bis weiß**  
    *   **Heatmapfarbgebung-blau zu gelb**  
    *   **Heatmapfarbgebung-Rainbow**  
*   **Verwenden der Hintergrundfarbe**  
*   **Verwenden der Bildschirm Textur**  
    
Mit der Option **"Bildschirm Textur verwenden** " können Sie der Debugfunktion Kontext hinzufügen.  Der Inhalt wird direkt von der Webseite auf den Elementen angezeigt.  

## Zusammengesetzte Layer

:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Bereich ' zusammengesetzte Ebenen '" lightbox="../media/experiments-layers.msft.png":::
   Bereich ' **zusammengesetzte Ebenen** '
:::image-end:::  

Der Bereich " **zusammengesetzte Ebenen** " öffnet die Elemente des **Layer** -Tools, ohne die Kontexte zu ändern.  Sie haben möglicherweise weiterhin Zugriff auf die Details der einzelnen Ebenen und die **langsamen Scroll-rects** und **Paint**.

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

Das Microsoft Edge devtools-Team arbeitet auf der Benutzeroberfläche und fügt der 3D-Ansicht basierend auf Ihrem Feedback mehr Funktionalität hinzu.  Senden Sie Ihr Feedback, um die Microsoft Edge-devtools zu verbessern.  Wählen Sie das Symbol " **Feedback senden** " im devtools oder wählen Sie `Alt` + `Shift` + `I` unter Windows/Linux oder `Option` + `Shift` + `I` unter macOS und geben Sie Feedback-oder Feature-Anfragen ein, die Sie für die devtools haben.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Microsoft Edge devtools 3D-Ansicht – MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Dokumentobjektmodell (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  

---
description: Alles zur 3D-Ansicht und deren Verwendung.
title: 3D View
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ba1125654c46be6ef4da99efc9ba027ba5e40672
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986080"
---
# 3D View  

Verwenden Sie die **3D-Ansicht** , um Ihre Webanwendung zu debuggen, indem Sie durch das [Dokumentobjektmodell (DOM)][MDNDocumentObjectModel] oder den Stapel Kontext des [z-Index][MDNZIndex] navigieren.  Damit können Sie die folgenden Aufgaben ausführen:  

*   [Erkunden der in eine 3D-Perspektive übersetzten Webseite](#3d-dom)  
*   [Debuggen basierend auf dem Stapeln des z-Index-Kontexts](#z-index)  
*   [Löschen eines Teils der Übersichtlichkeit im Dom-Bereich](#changing-your-view) oder im [Bereich "z-index"](#change-the-scope-of-your-exploration)  
*   [Das Farbschema zum besten Debuggen von Dom](#dom-color-type) [-oder z-Index Problemen](#z-index-color-type) aussuchen  

Wenn Sie einen frühen Prototyp eines 3D-Ansichts Projekts erkunden und den Code selbst ausführen möchten, lesen Sie [Beispiel für 3D-Ansicht][GithubMicrosoftedgeDevtoolssamples3dview].   

Auf der linken Seite gibt es zwei Bereiche, die Sie für Ihre Fehlerbehebung verwenden können.  

1.  Der Bereich " [Z-Index](#z-index) "  Navigieren Sie durch die verschiedenen Elemente in der Webanwendung, wobei der z-Index-Kontext berücksichtigt wird.  Der Bereich " **Z-Index** " ist der Standardbereich.  
1.  Der [3D-Dom-](#3d-dom) Bereich.  Erkunden Sie das DOM als Ganzes mit allen Elementen, die Ihnen zur Verfügung stehen.  Um auf den Bereich zuzugreifen, wählen Sie im **DOM** -Bereich neben dem Bereich **Z-Index** aus.  
    
Auf der rechten Seite zeigt die Leinwand Ihre Auswahl aus dem [Z-Index](#z-index) oder [3D-Dom](#3d-dom)an.  

## Navigieren im Arbeitsbereich  

:::image type="complex" source="../media/canvas.png" alt-text="Leinwand der 3D-Ansicht" lightbox="../media/canvas.png":::
   Leinwand der 3D-Ansicht  
:::image-end:::  

### Tastenkombinationen  

*   Drehen des Dom: um horizontal zu drehen, drücken Sie die `left-arrow` Tastenkombination und `right-arrow` .  Um vertikal zu drehen, drücken Sie die `up-arrow` Tastenkombination und `down-arrow` .  
*   Navigieren im Dom: um die benachbarten Elemente zu durchlaufen, wählen Sie ein Element aus, und drücken Sie die `up-arrow` Tastenkombination und `down-arrow` .  

### Maussteuerungen  

*   Drehen des Dom: Wählen Sie den Bereich aus, und ziehen Sie ihn um den Zeichenbereich.  
*   Schwenken um das DOM: Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und ziehen Sie den Mauszeiger in die Richtung, in die das DOM verschoben werden soll.  
*   Zoom: ziehen Sie zwei Finger über das Touchpad, oder verwenden Sie das Mausrad auf der Maus.  

### Steuerelemente auf dem Bildschirm  

:::image type="complex" source="../media/controls-small.png" alt-text="Leinwand der 3D-Ansicht" lightbox="../media/controls-small.png":::
   Steuerelemente auf dem Bildschirm  
:::image-end:::  

*   Zurücksetzen der Canvas-Ansicht auf die ursprüngliche Ansicht: Wählen Sie die Schaltfläche **Kamera zurücksetzen** aus, oder wählen Sie die Schaltfläche **Elemente zurücksetzen in Ansicht und Re-Center-Kamera** \ (seitliches Aktualisierungssymbol \) aus.  
*   Aktualisieren des Arbeitsbereichs \ (beispielsweise, wenn sich der Browser geändert hat oder Sie zu einer Geräte emulatoransicht gewechselt sind \): Wählen Sie die Schaltfläche " **Snapshot** erneut erstellen" aus, oder klicken Sie auf die Schaltfläche " **neuen Schnappschuss aufnehmen** " \ (Symbol "Aktualisieren" \).  

## Z-Index  

:::image type="complex" source="../media/z-index-view-box.png" alt-text="Leinwand der 3D-Ansicht" lightbox="../media/z-index-view-box.png":::
   Z-Indexansicht  
:::image-end:::  

Während der Bereich " **Z-Index** " über freigegebene Features mit dem **3D-Dom** -Bereich verfügt, verfügen die Bereiche weiterhin über Elemente, die für den Bereich eindeutig sind.  

### Markieren von Elementen mit Stapel Kontext  

Mit der Einstellung " **Highlight-Elemente mit Stapel Kontext** " können Sie die z-Index-Tags für die Elemente auf der Leinwand auf \ (und Off \) aktivieren.  Das Kontrollkästchen ist standardmäßig aktiviert.  

### Ändern des Umfangs ihrer Exploration  

Die Schaltfläche **alle Elemente anzeigen** ist die schnellste Möglichkeit, alle Elemente des DOM anzuzeigen, nachdem die Einstellungen unten geändert wurden.  

Mit der Schaltfläche **nur Elemente mit Stapel-Kontext anzeigen** werden Elemente ohne Stapel Kontext entfernt, und das DOM wird vereinfacht, um die Navigation zu vereinfachen.  

Die Schaltfläche " **ausgewähltes Element isolieren** " besteht im Wesentlichen aus drei Schaltflächen in einer.  Es gibt zwei Kontrollkästchen unter der Schaltfläche " **ausgewähltes Element isolieren** ": das Kontrollkästchen " **alle übergeordneten Elemente anzeigen** " und " **nur Eltern mit neuem Stapel-Kontext beibehalten** ".  

Das Kontrollkästchen **alle übergeordneten Elemente anzeigen** ist standardmäßig aktiviert.  Wenn Sie ein Element im Bereich "Leinwand" auswählen und dann die Schaltfläche " **ausgewähltes Element isolieren** " auswählen, zeigt der Canvas nur das Element und alle übergeordneten Elemente an.  

Wenn Sie das Kontrollkästchen **nur übergeordnete Elemente mit neuem Stacking-Kontext beibehalten** aktivieren und die Schaltfläche **ausgewähltes Element isolieren** auswählen, werden im Canvas nur das Element und die übergeordneten Elemente angezeigt, die einen neuen Stapel Kontext aufweisen.  

Wenn Sie beide Kontrollkästchen deaktivieren und die Schaltfläche " **ausgewähltes Element isolieren** " auswählen, zeigt die Leinwand nur das Element an, das Sie an erster Stelle gewählt haben.  

Suchen Sie am unteren Rand des **3D-Dom-** Panels das Kontrollkästchen **Elemente ausblenden mit der gleichen Farbreihenfolge wie das übergeordnete Element** .  Durch auswählen und Aufheben der Auswahl des Kontrollkästchens werden die Elemente basierend auf Ihrer Auswahl aktualisiert.  Wenn diese Option ausgewählt ist, werden Elemente, die die Farbreihenfolge freigeben, auf das übergeordnete Element reduziert.  

Die Optionen sollen einige der Übersichtlichkeit aufklären, die komplexere Webseiten in ihrer Leinwand erstellen.  

### Z-Index-Farbtyp  

Das sind die verschiedenen Visualisierungen, die Sie für das DOM in ihrer Leinwand verwenden können.  Unabhängig davon, ob Sie es zum Spaß verwenden oder weil die Visualisierungen Ihnen helfen, das DOM besser zu visualisieren, verfügt das devtools über drei verschiedene **Farben und eine Hintergrund Farb** Einstellung.  Über die Optionsfelder können Sie die Optionen durchlaufen und den Farbtyp wählen, der für Ihr Projekt am besten geeignet ist \ (oder das Sie am meisten möchten).  

## 3D-Dom  

:::image type="complex" source="../media/dom-purple-box.png" alt-text="Leinwand der 3D-Ansicht" lightbox="../media/dom-purple-box.png":::
   DOM-Ansicht  
:::image-end:::  

Wenn Sie eine allgemeine Debugansicht anstelle der z-Index-Oberfläche nutzen möchten, bietet das 3D- **DOM** eine Gesamtdarstellung des DOM.  Da der Kontext des z-Index entfernt wird, wird das DOM genauer und übersichtlicher gestapelt.  Der **3D-Dom-** Bereich hat eine ähnliche Funktionalität, aber es gibt ein paar Nuancen.  

### Ändern der Ansicht  

Im **3D-Dom-** Bereich enthält die Schaltfläche **ausgewählte Elemente isolieren** unter **geordnete** Kontrollkästchen und übergeordnete **Elemente einbeziehen.**  Standardmäßig sind beide Kontrollkästchen aktiviert, was bedeutet, dass durch Auswählen der Schaltfläche " **ausgewähltes Element isolieren** " nach dem Auswählen eines Elements auf der Leinwand das ausgewählte Element, die übergeordneten Elemente des Elements und die untergeordneten Elemente des Elements angezeigt werden sollen.  Wenn Sie das Kontrollkästchen unter **geordnete Elemente einbeziehen** deaktivieren und die Schaltfläche **ausgewählte Elemente isolieren** erneut auswählen, sollten das ausgewählte Element und die übergeordneten Elemente des Elements angezeigt werden.  Wenn Sie das Kontrollkästchen " **Kinder einbeziehen** " aktivieren und das Kontrollkästchen " **Eltern einbeziehen** " deaktivieren, bevor Sie die Schaltfläche " **ausgewähltes Element isolieren** " auswählen, werden im Canvas-Element und untergeordnete Elemente angezeigt.  Wenn Sie beide Kontrollkästchen deaktivieren und die Schaltfläche " **ausgewähltes Element isolieren** " auswählen, zeigt die Leinwand nur das zuvor ausgewählte Element an.  

Ein Schieberegler im Steuerbereich mit dem Titel " **Schachtelungsebene für Seite** mit einer Zahl daneben".  Die Zahl gibt die Anzahl der Layer für das Dokument an.  Wenn Sie den Schieberegler nach links ziehen, werden die äußersten Ebenen entfernt, bis Sie mit einer Schachtelungsebene, die auf 1 gesetzt ist, verbleibt, wodurch nur das am weitesten zurückliegende Element im DOM angezeigt wird.  Durch Ziehen des Schiebereglers können Sie einige der Unklarheiten entfernen, wenn Sie versuchen, sich genauer anzusehen, was in den unteren Ebenen geschieht.  

### Dom-Farbtyp  

Zusätzlich zur **heatmapfarbgebung-lila-zu-weiß**-, **heatmapfarbgebung-blau-zu-gelb**-, **heatmapfarbgebung-Rainbow-** und der **use-Hintergrundfarbe** , gibt es die **Verwendung der Bildschirm Textur**.  Die Bildschirm Textur fügt dem Debugvorgang Kontext hinzu, indem der Inhalt der Webseite direkt auf die Elemente angezeigt wird.  Im **3D-Dom-** Bereich ist die  **Farbtyp** Einstellung immer noch ein work in Progress, da einige Websites in der 3D-Ansicht eine schwierigere Darstellung der Bildschirm Struktur aufweisen.  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen

Das Microsoft Edge devtools-Team arbeitet auf der Benutzeroberfläche und fügt der 3D-Ansicht basierend auf den Fragen von Benutzern wie Ihnen weitere Funktionen hinzu.  Bitte senden Sie Ihr Feedback, um die Microsoft Edge-devtools zu verbessern.  Wählen Sie einfach das Feedback-Symbol im devtools aus, oder drücken Sie `Alt` + `Shift` + `I` \ (Windows \), oder drücken Sie `Option` + `Shift` + `I` \ (macOS \), und geben Sie alle Feedback-oder Funktionsanforderungen für das devtools ein.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Microsoft Edge devtools 3D-Ansicht – MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Dokumentobjektmodell (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  

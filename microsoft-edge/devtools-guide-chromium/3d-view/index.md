---
description: Alles über die 3D-Ansicht und deren Verwendung.
title: 3D View
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: bd91939a19f02a426834a85ef92eca388f8f1eda
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "11203970"
---
# 3D View  

Verwenden Sie **die 3D-Ansicht,** um Ihre Web-App zu debuggen, indem Sie durch das [Dokumentobjektmodell (DOM)][MDNDocumentObjectModel] oder den Kontext zum Stapeln des [Z-Index][MDNZIndex] navigieren.  Damit können Sie die folgenden Aufgaben ausführen.  

*   [Erkunden der in eine 3D-Perspektive übersetzten Webseite](#3d-dom)  
*   [Debuggen basierend auf Z-Index-Stapelkontext](#z-index)  
*   [Zugreifen auf die Funktionen des Tools Layer aus der 3D-Ansicht mit zusammengesetzten Ebenen](#composited-layers)  
*   [Löschen einiger Unübersichtlichkeiten im DOM-](#changing-your-view) oder [Z-Indexbereich](#change-the-scope-of-your-exploration)  
*   [Wählen Sie das Farbschema aus, um Ihre DOM-](#dom-color-type) oder [Z-Index-Probleme am besten zu debuggen.](#z-index-color-type)  

Wenn Sie einen frühen Prototyp des 3D-Ansichtsprojekts erkunden und den Code selbst ausführen möchten, navigieren Sie zum [Beispiel für die 3D-Ansicht.][GithubMicrosoftedgeDevtoolssamples3dview]  

Auf der linken Seite gibt es drei Bereiche, die Sie für die Debugerfahrung verwenden können.  

*   Der [Z-Index-Bereich.](#z-index)  Navigieren Sie durch die verschiedenen Elemente in der Web-App, und berücksichtigen Sie dabei den Z-Index-Kontext.  Der **Z-Index-Bereich** ist der Standardbereich.  
*   Der [3D-DOM-Bereich.](#3d-dom)  Erkunden Sie das DOM als Ganzes, und alle Elemente sind leicht zugänglich.  Um auf den Bereich zu zugreifen, wählen Sie den **DOM-Bereich** neben dem **Z-Indexbereich** aus.  
*   Der [Bereich "Zusammengesetzte Layer".](#composited-layers)  Fügen Sie ein weiteres 3D-Element hinzu, um eine umfassendere Erfahrung aus der Sicht der Ebenen zu erstellen.  Um auf den Bereich zu zugreifen, wählen Sie den Bereich **zusammengesetzte Layer** neben dem **DOM-Bereich.**  
    
Auf der rechten Seite zeigt der Zeichenbereich Ihre Auswahl aus dem [Z-Index,](#z-index) [3D-DOM](#3d-dom)oder [zusammengesetzten Layern an.](#composited-layers)  

## Navigieren im Zeichenbereich  

:::image type="complex" source="../media/3d-view-canvas.msft.png" alt-text="Zeichenbereich der 3D-Ansicht" lightbox="../media/3d-view-canvas.msft.png":::
   Zeichenbereich der 3D-Ansicht  
:::image-end:::  

### Tastenkombinationen  

*   DOM drehen: Wählen Sie zum horizontalen Drehen die Tasten `left-arrow` und die Tasten `right-arrow` aus.  Um vertikal zu drehen, wählen Sie die Tasten `up-arrow` und die Tasten `down-arrow` aus.  
*   Navigieren Sie im DOM: Um durch die benachbarten Elemente zu navigieren, wählen Sie ein Element und die Tasten `up-arrow` `down-arrow` aus.  

### Maussteuerelemente  

*   Drehen Sie das DOM: Wählen Sie den Bereich des Zeichenbereichs aus, und ziehen Sie ihn.  
*   Schwenken Sie das DOM: Öffnen Sie das Kontextmenü \(Rechtsklick\), und ziehen Sie in die Richtung, in die das DOM bewegt werden soll.  
*   Zoom: Ziehen Sie zwei Finger über das Touchpad, oder verwenden Sie das Bildlaufrad der Maus.  

### Steuerelemente auf dem Bildschirm  

:::image type="complex" source="../media/3d-view-controls-small.msft.png" alt-text="Steuerelemente auf dem Bildschirm" lightbox="../media/3d-view-controls-small.msft.png":::
   Steuerelemente auf dem Bildschirm  
:::image-end:::  

*   Setzen Sie die Canvasansicht auf **** die ursprüngliche Ansicht zurück: Klicken Sie auf die Schaltfläche "Kamera zurücksetzen", oder wählen Sie die Schaltfläche "Elemente **in** der Ansicht zurücksetzen" und die Kamera erneut zentriert \(sideways refresh icon\) aus.  
*   Aktualisieren Sie den Zeichenbereich \(z. B. wenn der Browser geändert **** wurde oder Sie zu **** einer Geräteemulatoransicht gewechselt haben\): Wählen Sie die Schaltfläche "Momentaufnahme erneut übernehmen" oder die Schaltfläche "Neue Momentaufnahme erstellen" \(Aktualisierungssymbol\) aus.  

## Z-Index  

:::image type="complex" source="../media/3d-view-z-index-view-box.msft.png" alt-text="Z-Index-Ansicht" lightbox="../media/3d-view-z-index-view-box.msft.png":::
   Z-Index-Ansicht  
:::image-end:::  

Während der **Z-Index-Bereich** über gemeinsame Features für den **3D-DOM-Bereich** verfügt, verfügen die Bereiche weiterhin über Elemente, die für den Bereich einzigartig sind.  

### Hervorheben von Elementen mit Stapelkontext  

Mit **den Highlight-Elementen mit** der Kontexteinstellung "Stapeln" können Sie die Z-Index-Tags für die Elemente im Zeichenbereich aktivieren (und deaktivieren).  Das Kontrollkästchen ist standardmäßig aktiviert.  

### Ändern des Umfangs Ihrer Untersuchung  

Die **Schaltfläche "Alle Elemente anzeigen"** ist die schnellste Möglichkeit zum Anzeigen aller Elemente des DOM, nachdem Sie die Einstellungen darunter geändert haben.  

Mit **der Schaltfläche "Nur Elemente anzeigen"** mit der Kontextschaltfläche "Stapeln" werden Elemente entfernt, ohne kontextbezogene Elemente zu stapeln, und das DOM wird für eine einfachere Navigation vereinfacht.  

Die **Schaltfläche "Ausgewähltes Element** isolieren" besteht im Wesentlichen aus drei Schaltflächen in einer.  Unter der Schaltfläche "Ausgewähltes Element isolieren" befinden sich **** zwei Kontrollkästchen: das Kontrollkästchen "Alle über- und über- und abgrenzen" mit dem neuen Kontrollkästchen "Kontext isolieren". **** ****  

Das **Kontrollkästchen "Alle** Eltern anzeigen" ist standardmäßig aktiviert.  Um das Element und alle über- und über- n nen Elemente im Zeichenbereich anzeigen zu können, wählen Sie ein Element aus, und wählen Sie die Schaltfläche **"Ausgewähltes Element isolieren"** aus.  

Aktivieren Sie zum Anzeigen des Elements und der über- und **** über- 10-Elemente, die einen neuen Stapelkontext auf dem Zeichenbereich haben, die Option "Nur über-Elemente mit neuer Stapelkontexteinstellung behalten", und wählen Sie die Schaltfläche "Ausgewähltes Element isolieren" aus. ****  

Wenn Sie das ausgewählte Element auf der Canvas anzeigen möchten, deaktivieren Sie die Einstellungen, und wählen Sie "Ausgewählte **Element isolieren"** aus.  

Suchen Sie unten im **3D-DOM-Bereich** die Elemente mit der gleichen Farbreihenfolge wie das übergeordnete **Kontrollkästchen.**  Wenn Sie das Kontrollkästchen auswählen und deaktivieren, werden die Elemente basierend auf Ihrer Wahl aktualisiert.  Wenn sie ausgewählt wird, werden Elemente, die die Gemeinsame Farbreihenfolge gemeinsam haben, auf das übergeordnete Element abgeflachtet.  

Die Optionen sollen einige der Unübersichtlichkeiten, die komplexere Webseiten in Ihrer Canvas erstellen, löschen.  

### Z-Index-Farbtyp  

Dies sind die verschiedenen Visualisierungen, die Sie für das DOM in Ihrer Canvas verwenden können.  Unabhängig davon, ob Sie es für Spaß verwenden oder weil die Visualisierungen Ihnen helfen, das DOM besser zu visualisieren, verfügen die DevTools über unterschiedliche Farbschemas und die Option **"Hintergrundfarbe** verwenden".  Im **Z-Index-Bereich** wird das Lila in **Weiß und** die **Hintergrundfarbe** mit dem **3D-DOM-Bereich** verwendet.  Angesichts des hinzugefügten visuellen Elements der Z-Index-Bezeichnungen hat Ihr Feedback zu einer Reduzierung der Anzahl der Farboptionen geführt.  Die neue Einfachheit verbessert die Debugerfahrung für den Z-Index.  Mit den Optionsfeldern können Sie die Optionen umschalten und den Farbtyp auswählen.  Der Farbtyp ist entweder für Ihr Projekt am besten geeignet oder am besten geeignet.  

## 3D-DOM  

:::image type="complex" source="../media/3d-view-dom-purple-box.msft.png" alt-text="DOM-Ansicht" lightbox="../media/3d-view-dom-purple-box.msft.png":::
   DOM-Ansicht  
:::image-end:::  

Wenn Sie eine allgemeine Debugansicht anstelle der Z-Index-Ansicht verwenden möchten, bietet **das 3D-DOM** einen Gesamtanschauungs-DOM-Look.  Da der Z-Index-Kontext entfernt wird, wird das DOM genauer und sauberer gestapelt.  Der **3D-DOM-Bereich** verfügt über eine ähnliche Funktionalität, aber es gibt einige Nuancen.  

### Ändern der Ansicht  

Im **3D-DOM-Bereich** verfügt die **Schaltfläche** "Ausgewähltes Element isolieren" über die Kontrollkästchen "Elemente ein- und **ein-** und ausgrenzen". ****  Beide Kontrollkästchen sind standardmäßig aktiviert.  Das bedeutet, wenn **** Sie die Schaltfläche "Ausgewähltes Element isolieren" auswählen, nachdem Sie ein Element ausgewählt haben, zeigt der Zeichenbereich das ausgewählte Element, die über- und unter- en Elemente des Elements an.  Deaktivieren Sie die Einstellung **"Elemente ein-** und ausschalten", und wählen Sie erneut die Schaltfläche "Ausgewähltes Element isolieren" aus, um das ausgewählte Element und die über- und unter- en Elemente des Elements anzeigen zu können. ****  Wenn Sie die **** Einstellung "Elemente hinzufügen" aktivieren und die **** Einstellung "Eltern ein- und ausschalten" deaktivieren und dann auf die Schaltfläche "Ausgewähltes Element isolieren" klicken, zeigt der Zeichenbereich das Element und alle unterst nkten Elemente an. ****  Wenn Sie beide Einstellungen deaktivieren **** und die Schaltfläche "Ausgewähltes Element isolieren" auswählen, zeigt der Zeichenbereich nur das zuvor ausgewählte Element an.  

Ein Schieberegler im Steuerelementbereich namens **Schachtelungsebene für die** Seite mit einer Zahl daneben.  Die Zahl gibt die Anzahl der Ebenen für das Dokument an.  Durch Ziehen des Schiebereglers nach links werden die äußersten Ebenen entfernt, bis eine Schachtelungsebene festgelegt ist, die nur das am weitesten hinten im DOM angezeigte Element `1` anzeigt.  Ziehen Sie den Schieberegler, um einige der Unübersichtlichkeiten zu entfernen.  Sie erhalten einen genaueren Blick auf die Vorgänge auf den unteren Ebenen.  

### DOM-Farbtyp  

Im **3D-DOM-Bereich** werden die folgenden Optionen angezeigt.  

*   Drei verschiedene Farbschemas.  
    *   **Heatmap – Lila bis Weiß**  
    *   **Heatmap – Blau in Gelb**  
    *   **Heatmap – Kita**  
*   **Verwenden der Hintergrundfarbe**  
*   **Verwenden der Bildschirmtextur**  
    
Die **Option "Bildschirmtextur verwenden"** fügt Ihrer Debugerfahrung Kontext hinzu.  Der Inhalt der Webseite wird direkt auf den Elementen angezeigt.  

## Zusammengesetzte Ebenen

:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Bereich Zusammengesetzte Ebenen" lightbox="../media/experiments-layers.msft.png":::
   Bereich **Zusammengesetzte Ebenen**
:::image-end:::  

Im **Bereich "Zusammengesetzte Layer"** werden die Elemente des Tools Layer **geöffnet,** ohne Kontexte zu ändern.  Sie können weiterhin auf die Details der einzelnen Ebenen zugreifen und über die Langsamen **Bildlauf-Rects** und **Paint verfügen.**

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

Das Microsoft Edge Devtools-Team arbeitet basierend auf Ihrem Feedback an der Benutzeroberfläche und fügt der 3D-Ansicht weitere Funktionen hinzu.  Senden Sie Ihr Feedback, um die Microsoft Edge DevTools zu verbessern.  Wählen Sie **das Symbol "Feedback** senden" in den DevTools oder unter Windows/Linux oder unter macOS aus, und geben Sie Feedback oder Featureanforderungen ein, die Sie für `Alt` + `Shift` + `I` `Option` + `Shift` + `I` devTools haben.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Microsoft Edge DevTools 3D-Ansicht – MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Document Object Model (DOM)-| MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "Z-Index-| MDN"  

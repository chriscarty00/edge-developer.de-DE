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
ms.sourcegitcommit: 5e218b24fb21fcfa9c82b99f17373fed1ba5a21c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/30/2021
ms.locfileid: "11203970"
---
# <a name="3d-view"></a>3D View  

Verwenden Sie **die 3D-Ansicht,** um Ihre Web-App zu debuggen, indem Sie durch das [Dokumentobjektmodell (Document Object Model, DOM)][MDNDocumentObjectModel] oder den [Z-Index-Stapelkontext][MDNZIndex] navigieren.  Damit können Sie die folgenden Aufgaben ausführen.  

*   [Erkunden der in eine 3D-Perspektive übersetzten Webseite](#3d-dom)  
*   [Debuggen basierend auf dem Z-Index-Stackingkontext](#z-index)  
*   [Zugreifen auf die Funktionen des Layers-Tools aus der 3D-Ansicht mit zusammengesetzten Ebenen](#composited-layers)  
*   [Löschen einiger Unübersichtlichkeiten im DOM-](#changing-your-view) oder [Z-Indexbereich](#change-the-scope-of-your-exploration)  
*   [Wählen Sie das Farbschema aus, um Ihre DOM-Probleme](#dom-color-type) oder [Z-Index-Probleme am besten zu debuggen.](#z-index-color-type)  

Wenn Sie einen frühen Prototyp des 3D-Ansichtsprojekts erkunden und den Code selbst ausführen möchten, navigieren Sie zu [3D-Ansichtsbeispiel][GithubMicrosoftedgeDevtoolssamples3dview].  

Auf der linken Seite gibt es drei Bereiche, die Sie für Ihre Debugerfahrung verwenden können.  

*   Der [Z-Index-Bereich.](#z-index)  Navigieren Sie durch die verschiedenen Elemente in der Web-App, und berücksichtigen Sie dabei den Z-Index-Kontext.  Der **Z-Index-Bereich** ist der Standardbereich.  
*   Der [3D-DOM-Bereich.](#3d-dom)  Erkunden Sie das DOM als Ganzes mit allen Elementen, auf die leicht zugegriffen werden kann.  Um auf den Bereich zu zugreifen, wählen Sie den **DOM-Bereich** neben dem **Z-Index-Bereich** aus.  
*   Der [Bereich Zusammengesetzte Ebenen.](#composited-layers)  Fügen Sie ein weiteres 3D-Element hinzu, um eine umfassendere Erfahrung aus der Ebenenperspektive zu erstellen.  Um auf den Bereich zu zugreifen, wählen Sie den Bereich **Zusammengesetzte Ebenen** neben dem **DOM-Bereich** aus.  
    
Auf der rechten Seite zeigt der Zeichenbereich Ihre Auswahl aus dem [Z-Index,](#z-index) [3D-DOM](#3d-dom)oder [zusammengesetzten Ebenen an.](#composited-layers)  

## <a name="navigating-the-canvas"></a>Navigieren im Zeichenbereich  

:::image type="complex" source="../media/3d-view-canvas.msft.png" alt-text="Canvas of 3D View" lightbox="../media/3d-view-canvas.msft.png":::
   Canvas of 3D View  
:::image-end:::  

### <a name="keyboard-shortcuts"></a>Tastenkombinationen  

*   Dom drehen: Wählen Sie zum horizontalen Drehen die Tasten `left-arrow` und `right-arrow` aus.  Um vertikal zu drehen, wählen Sie die Tasten `up-arrow` und `down-arrow` aus.  
*   Navigieren Sie zum DOM: Wählen Sie ein Element und die Tasten aus, um durch die angrenzenden Elemente `up-arrow` zu `down-arrow` navigieren.  

### <a name="mouse-controls"></a>Maussteuerelemente  

*   Dom drehen: Wählen Sie den Bereich des Zeichenbereichs aus, und ziehen Sie ihn.  
*   Schwenken Sie das DOM: Öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und ziehen Sie in die Richtung, in die das DOM bewegt werden soll.  
*   Zoom: Ziehen Sie zwei Finger über das Touchpad, oder verwenden Sie das Bildlaufrad der Maus.  

### <a name="on-screen-controls"></a>Bildschirmsteuerelemente  

:::image type="complex" source="../media/3d-view-controls-small.msft.png" alt-text="Bildschirmsteuerelemente" lightbox="../media/3d-view-controls-small.msft.png":::
   Bildschirmsteuerelemente  
:::image-end:::  

*   Setzen Sie die Canvasansicht auf **** die ursprüngliche Ansicht zurück: Wählen Sie die Schaltfläche Kamera zurücksetzen aus, oder wählen Sie die Schaltfläche **Elemente zurücksetzen in** der Ansicht und Kamera neu zentriert \(Seitwärtsaktualisierungssymbol\) aus.  
*   Aktualisieren Sie den Canvas \(z. B. wenn der Browser geändert wurde **** oder Sie zu **** einer Geräteemulatoransicht gewechselt haben\): Wählen Sie die Schaltfläche Momentaufnahme erneut übernehmen aus, oder wählen Sie die Schaltfläche Neue Momentaufnahme erstellen \(Aktualisierungssymbol\).  

## <a name="z-index"></a>Z-Index  

:::image type="complex" source="../media/3d-view-z-index-view-box.msft.png" alt-text="Z-Index-Ansicht" lightbox="../media/3d-view-z-index-view-box.msft.png":::
   Z-Index-Ansicht  
:::image-end:::  

Während der **Z-Index-Bereich** über freigegebene Features für den **3D-DOM-Bereich** verfügt, verfügen die Bereiche weiterhin über Elemente, die für den Bereich eindeutig sind.  

### <a name="highlight-elements-with-stacking-context"></a>Hervorheben von Elementen mit Stapelkontext  

Mit **der Einstellung Elemente mit Stapelkontext** hervorheben können Sie die Z-Index-Tags für die Elemente auf dem Zeichenbereich aktivieren.  Das Kontrollkästchen ist standardmäßig aktiviert.  

### <a name="change-the-scope-of-your-exploration"></a>Ändern des Umfangs Ihrer Erkundung  

Mit der Schaltfläche Alle **Elemente anzeigen** können Sie am schnellsten alle Elemente des DOM anzeigen, nachdem Sie die Einstellungen darunter geändert haben.  

Die **Schaltfläche Nur Elemente mit** Stapelkontext anzeigen entfernt Elemente ohne Kontextstapeln und vereinfacht das DOM für eine einfachere Navigation.  

Die **Schaltfläche ausgewähltes Element isolieren** besteht im Wesentlichen aus drei Schaltflächen in einer.  Es gibt zwei Kontrollkästchen **** unterhalb der **** Schaltfläche Ausgewähltes Element isolieren: Das Kontrollkästchen Alle Eltern anzeigen und **Nur** eltern mit neuem Stapelkontext behalten.  

Das **Kontrollkästchen Alle eltern anzeigen** ist standardmäßig aktiviert.  Wählen Sie ein Element aus, und wählen Sie die Schaltfläche Ausgewähltes Element isolieren aus, um das Element und alle auf dem Zeichenbereich dargestellten **Elemente zu** zeigen.  

Aktivieren Sie zum Anzeigen des Elements und der über einen neuen **** Stapelkontext auf dem Zeichenbereich verfügenden Elemente die Einstellung Nur eltern mit neuem Stapelkontext behalten, und wählen Sie die Schaltfläche ausgewähltes Element **isolieren** aus.  

Wenn Sie das ausgewählte Element auf dem Zeichenbereich anzeigen möchten, deaktivieren Sie beide Einstellungen, und wählen Sie **ausgewählte Elementschaltfläche isolieren** aus.  

Suchen Sie unten im **3D-DOM-Bereich** das Kontrollkästchen Elemente ausblenden mit der gleichen **Farbreihenfolge** wie das übergeordnete Kontrollkästchen.  Wenn Sie das Kontrollkästchen auswählen und deaktivieren, werden die Elemente basierend auf Ihrer Wahl aktualisiert.  Wenn ausgewählt, werden Elemente, die die Farbreihenfolge gemeinsam haben, auf das übergeordnete Element abgeflachtet.  

Die Optionen sollen einige der Unübersichtlichkeiten, die komplexere Webseiten in Ihrem Zeichenbereich erstellen, aufräumen.  

### <a name="z-index-color-type"></a>Z-Index-Farbtyp  

Die sind die verschiedenen Visualisierungen, die Sie für das DOM in Ihrer Canvas verwenden können.  Unabhängig davon, ob Sie es zum Spaß verwenden oder weil die Visualisierungen Ihnen helfen, das DOM besser zu visualisieren, haben die DevTools unterschiedliche Farbwege und eine **Option Hintergrundfarbe** verwenden.  Der **Z-Index-Bereich** teilt lila in **Weiß** und **Hintergrundfarbe** mit dem **3D-DOM-Bereich.**  Angesichts des hinzugefügten visuellen Elements der Z-Index-Beschriftungen, ihres Feedbacks, das zu einer Reduzierung der Anzahl von Farboptionen führte.  Die neue Einfachheit verbessert die Debugerfahrung des Z-Index.  Mit den Optionsfeldern können Sie die Optionen umschalten und den Farbtyp auswählen.  Der Farbtyp ist für Ihr Projekt am besten geeignet oder am besten geeignet.  

## <a name="3d-dom"></a>3D-DOM  

:::image type="complex" source="../media/3d-view-dom-purple-box.msft.png" alt-text="DOM-Ansicht" lightbox="../media/3d-view-dom-purple-box.msft.png":::
   DOM-Ansicht  
:::image-end:::  

Wenn Sie eine allgemeine Debugansicht anstelle der Z-Index-Erfahrung verwenden möchten, gibt das **3D-DOM** ein Gesamtbild des DOM.  Da der Z-Index-Kontext entfernt wurde, wird das DOM genauer und sauberer gestapelt.  Der **3D-DOM-Bereich** verfügt über ähnliche Funktionen, aber es gibt einige Nuancen.  

### <a name="changing-your-view"></a>Ändern der Ansicht  

Im **3D-DOM-Bereich** verfügt **die** Schaltfläche ausgewähltes Element isolieren über die Kontrollkästchen **"Kinder** enthalten" und **"Eltern** enthalten".  Beide Kontrollkästchen sind standardmäßig aktiviert.  Das bedeutet, wenn **** Sie die Schaltfläche ausgewähltes Element isolieren auswählen, nachdem Sie ein Element ausgewählt haben, zeigt der Canvas das ausgewählte Element, die eltern des Elements und die untere Elemente des Elements an.  Deaktivieren Sie die Einstellung "Kinder **hinzufügen",** und wählen Sie **die** Schaltfläche ausgewähltes Element isolieren erneut aus, um das ausgewählte Element und die eltern des Elements angezeigt zu werden.  Wenn Sie die **** Einstellung "Kinder hinzufügen" aktivieren und die **** Einstellung "Eltern eingrenzen" deaktivieren und dann die Schaltfläche ausgewähltes Element isolieren auswählen, zeigt der Zeichenbereich das Element und alle kinder elemente an. ****  Wenn Sie beide Einstellungen deaktivieren **** und die Schaltfläche ausgewähltes Element isolieren auswählen, zeigt der Canvas nur das zuvor ausgewählte Element an.  

Ein Schieberegler im Steuerelementbereich namens **Schachtelungsebene für Seite** mit einer Zahl daneben.  Die Zahl gibt die Anzahl der Ebenen für das Dokument an.  Wenn Sie den Schieberegler nach links ziehen, werden die äußersten Ebenen so lange entfernt, bis eine Schachtelungsebene auf festgelegt ist, die nur das am weitesten hinten im DOM angezeigte Element `1` anzeigt.  Ziehen Sie den Schieberegler, um einen Teil der Unübersichtlichkeit zu entfernen.  Es hilft Ihnen, einen genaueren Blick auf die Vorgänge auf den unteren Ebenen zu erhalten.  

### <a name="dom-color-type"></a>DOM-Farbtyp  

Im **3D-DOM-Bereich** werden die folgenden Optionen angezeigt.  

*   Drei unterschiedliche Farbways.  
    *   **Heatmap – Lila bis Weiß**  
    *   **Heatmap – Blau bis Gelb**  
    *   **Heatmap – Rainbow**  
*   **Verwenden der Hintergrundfarbe**  
*   **Verwenden der Bildschirmtextur**  
    
Die **Option Bildschirmtextur verwenden** fügt Ihrer Debugerfahrung Kontext hinzu.  Der Inhalt der Webseite wird direkt in den Elementen angezeigt.  

## <a name="composited-layers"></a>Zusammengesetzte Ebenen

:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Verbundebenenbereich" lightbox="../media/experiments-layers.msft.png":::
   Bereich **Zusammengesetzte Ebenen**
:::image-end:::  

Im **Bereich Zusammengesetzte Ebenen** werden die Elemente des **Layers-Tools** geöffnet, ohne Kontexte zu ändern.  Möglicherweise greifen Sie weiterhin auf die Details der einzelnen Ebenen zu und verfügen über die **Langsamen** Bildlauf-Rects **und Paint**.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

Das Microsoft Edge Devtools-Team arbeitet an der Benutzeroberfläche und fügt der 3D-Ansicht basierend auf Ihrem Feedback weitere Funktionen hinzu.  Senden Sie Ihr Feedback, um die Microsoft Edge DevTools zu verbessern.  Wählen Sie **das Symbol Feedback** senden in den DevTools aus, oder wählen Sie auf Windows/Linux oder unter macOS aus, und geben Sie Feedback oder Featureanforderungen ein, die Sie für die `Alt` + `Shift` + `I` `Option` + `Shift` + `I` DevTools haben.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Microsoft Edge DevTools 3D-Ansicht – MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Document Object Model (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  

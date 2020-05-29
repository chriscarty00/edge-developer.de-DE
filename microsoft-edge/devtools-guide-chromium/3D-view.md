---
description: Alles zur 3D-Ansicht und deren Verwendung.
title: 3D View
author: erdraud
ms.author: erdraud
ms.date: 11/27/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: f2ae80426da71797d4bee4060d33965f04047e19
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567074"
---
# 3D View

Verwenden Sie die **3D-Ansicht** , um Ihre Webanwendung zu debuggen, indem Sie durch das [Dokumentobjektmodell](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) (DOM) oder den Stapel Kontext des [z-Index](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index) navigieren. Damit haben Sie folgende Möglichkeiten: 

- [Erkunden der in eine 3D-perspevtive übersetzten Webseite](#3d-dom)
- [Debuggen basierend auf dem Stapeln des z-Index-Kontexts](#z-index)
- [Löschen eines Teils der Übersichtlichkeit im Dom-Bereich](#changing-your-view) oder im [Bereich "z-index"](#change-the-scope-of-your-exploration)
- [Das Farbschema zum besten Debuggen von Dom](#dom-color-type) [-oder z-Index Problemen](#z-index-color-type) aussuchen

Es gibt zwei Bereiche, die Sie für Ihre Fehlerbehebung verwenden können.

1. **Z-Index** Navigieren Sie durch die verschiedenen Elemente in der Webanwendung, wobei der z-Index-Kontext berücksichtigt wird. Dies ist der Standardbereich.
2. **3D-Dom** Erkunden Sie das DOM als Ganzes mit allen Elementen, die Ihnen zur Verfügung stehen. Um auf diesen Bereich zuzugreifen, klicken Sie auf den Bereich "Dom" neben dem Bereich "Z-Index".

![Leinwand der 3D-Ansicht](./media/canvas.png)

## Navigieren im Arbeitsbereich

### Tastenkombinationen
- Drehen des Dom: Verwenden Sie die nach-links-und die nach-rechts-Taste, um horizontal zu rotieren, und verwenden Sie die nach-oben-und nach-unten-Taste
- Navigieren im Dom: Wenn ein Element markiert ist, können Sie die nach-oben-und nach-unten-Taste verwenden, um die benachbarten Elemente zu durchlaufen.

### Maussteuerungen
- Drehen Sie das DOM: Klicken Sie mit der linken Maustaste, und ziehen Sie den Zeichenbereich um.
- Schwenken um das DOM: Klicken Sie mit der rechten Maustaste, und ziehen Sie die Maus in die Richtung, in die das DOM verschoben werden soll.
- Zoom: ziehen Sie zwei Finger über das Touchpad, oder verwenden Sie das Mausrad auf der Maus.

![Steuerelemente auf dem Bildschirm](./media/controls-small.png)
### Steuerelemente auf dem Bildschirm
- Zurücksetzen der Canvas-Ansicht auf die ursprüngliche Ansicht: Klicken Sie auf die Schaltfläche mit der Bezeichnung "Kamera zurücksetzen", oder klicken Sie auf das Symbol, das wie eine seitliche Schaltfläche "Aktualisieren" aussieht, und hat "Elemente in Ansicht zurücksetzen und Kamera neu zentrieren".
- Aktualisieren Sie die Leinwand (z.b. wenn sich der Browser geändert hat oder Sie zu einer Geräteemulator-Ansicht gewechselt haben): Klicken Sie auf die Schaltfläche mit dem Titel "Schnappschuss erneut aufnehmen" oder klicken Sie auf die Schaltfläche, die wie ein Aktualisierungssymbol aussieht, und hat "neuen Schnappschuss aufnehmen" als Hovertext.

![Z-Indexansicht](./media/z-index-view-box.png)

## Z-Index

Während der Bereich "Z-Index" über freigegebene Features mit dem Dom-Bereich verfügt, verfügen Sie weiterhin über Elemente, die für den Bereich eindeutig sind.

### Markieren von Elementen mit Stapel Kontext

Mit dieser Einstellung können Sie die z-Index-Tags für die Elemente im Canvas-Element ein-und ausblenden. Das Kontrollkästchen ist standardmäßig aktiviert.

### Ändern des Umfangs ihrer Exploration

Die Schaltfläche **alle Elemente anzeigen** ist die schnellste Möglichkeit, alle Elemente des DOM anzuzeigen, nachdem die Einstellungen unten geändert wurden.

**Nur Elemente mit Stapel Kontext anzeigen** entfernt Elemente ohne Stapeln des Kontexts und vereinfacht das DOM, um die Navigation zu vereinfachen.

Der Filter " **ausgewählte Elemente isolieren** " besteht im Wesentlichen aus drei Schaltflächen in einem. Es gibt zwei Kontrollkästchen unter dieser Schaltfläche: eine ist "alle Eltern anzeigen" und "nur Eltern mit neuem Stapel Kontext behalten". 

Das Kontrollkästchen "alle übergeordneten Elemente anzeigen" ist standardmäßig aktiviert. Wenn Sie ein Element im Bereich "Leinwand" auswählen und auf " **ausgewähltes Element isolieren**" klicken, werden im Arbeitsbereich nur das Element und seine übergeordneten Elemente angezeigt.

Wenn Sie die Option "nur übergeordnete Elemente mit neuem Stapel Kontext beibehalten" auswählen und auf **ausgewähltes Element isolieren**klicken, werden in der Canvas nur das Element und die übergeordneten Elemente angezeigt, die einen neuen Stapel Kontext aufweisen.

Wenn Sie beide Kontrollkästchen deaktivieren und auf **ausgewähltes Element isolieren**klicken, zeigt der Canvas nur das Element an, das Sie an erster Stelle gewählt haben.

Am unteren Rand des Steuerelement Panels befinden sich die **Hide-Elemente mit der gleichen Farbreihenfolge wie die übergeordnete** Umschaltfläche. Wenn Sie das Kontrollkästchen aktivieren und deaktivieren, werden die Elemente basierend auf Ihrer Auswahl neu geladen. Wenn diese Option ausgewählt ist, werden Elemente, die die Farbreihenfolge freigeben, auf das übergeordnete Element reduziert.

Mithilfe dieser Optionen können Sie einen Teil der Übersichtlichkeit aufklären, die komplexere Webseiten in ihrer Leinwand erstellen.

### Z-Index-Farbtyp

Hierbei handelt es sich um die verschiedenen Visualisierungen, die Sie für das DOM in ihrer Leinwand verwenden können. Egal, ob Sie es zum Spaß verwenden oder weil es Ihnen hilft, das DOM besser zu visualisieren, wir haben drei verschiedene Farben sowie eine Einstellung "Hintergrundfarbe". Über die Optionsfelder können Sie die Optionen durchlaufen und den Farbtyp wählen, der für Ihr Projekt am besten geeignet ist (oder am besten gefällt).

![DOM-Ansicht](./media/dom-purple-box.png)

## 3D-Dom

Wenn Sie eine allgemeine Debugansicht anstelle der z-Index-Oberfläche nutzen möchten, bietet das 3D-DOM eine Gesamtdarstellung des DOM. Da der Kontext des z-Index entfernt wird, wird das DOM genauer und übersichtlicher gestapelt. Dieser Bereich hat eine ähnliche Funktionalität, aber es gibt ein paar Nuancen.

### Ändern der Ansicht

Im **3D-Dom-** Bereich hat der Filter " **ausgewählte Elemente isolieren** " "untergeordnete Elemente" und "Eltern einbeziehen". Standardmäßig sind beide Kontrollkästchen aktiviert, was bedeutet, dass durch Klicken auf die Schaltfläche " **ausgewähltes Element isolieren** " nach dem Auswählen eines Elements im Canvas-Element das ausgewählte Element, die übergeordneten Elemente des Elements und die untergeordneten Elemente des Elements angezeigt werden. Wenn Sie das Kontrollkästchen "Kinder einbeziehen" deaktivieren und dann erneut auf die Schaltfläche " **ausgewähltes Element isolieren** " klicken, werden das ausgewählte Element und die übergeordneten Elemente des Elements angezeigt. Wenn Sie das Kontrollkästchen "Kinder einbeziehen" aktivieren und das Kontrollkästchen "Eltern einbeziehen" deaktivieren, bevor Sie auf " **ausgewählte Elemente isolieren**" klicken, wird das Element und seine untergeordneten Elemente im Canvas-Bereich angezeigt. Wenn Sie beide Kontrollkästchen deaktivieren und auf **ausgewähltes Element isolieren**klicken, zeigt der Canvas nur das zuvor ausgewählte Element an.

Sie werden einen Schieberegler im Kontrollbereich mit dem Titel " **Schachtelungsebene** mit einer Zahl daneben" feststellen. Die Zahl gibt die Anzahl der Ebenen im Dokument an. Wenn Sie den Schieberegler nach links ziehen, werden die äußersten Ebenen entfernt, bis Sie mit einer Schachtelungsebene von 1 versehen sind, sodass nur das am weitesten zurückliegende Element im DOM angezeigt wird. Dies ermöglicht Ihnen, einige der Unklarheiten zu entfernen, wenn Sie versuchen, sich genauer anzusehen, was in den unteren Ebenen vorgeht.

### Dom-Farbtyp

Sie werden feststellen, dass neben den Optionen " *lila zu weiß*", " *blau zu gelb*", " *Regenbogen*" und " *Hintergrundfarbe verwenden* *" eine Bildschirm Textur verwendet*wird. Die Bildschirm Textur fügt dem Debugvorgang Kontext hinzu, indem der Inhalt der Webseite direkt auf die Elemente angezeigt wird. Dies ist immer noch ein work in Progress, da es einigen Websites schwerer fällt, die Bildschirm Textur in der 3D-Ansicht wieder zu rendern. 

## Nächste Schritte

Wir arbeiten an der Benutzeroberfläche und fügen der 3D-Ansicht basierend auf den Fragen von Benutzern wie Ihnen weitere Funktionen hinzu. Bitte senden Sie uns Ihr Feedback, damit wir die Microsoft Edge-devtools für Sie weiter verbessern können. Klicken Sie einfach auf das Feedback-Symbol im devtools, oder drücken Sie `Alt`  +  `Shift`  +  `I` auf Windows ( `Option`  +  `Shift`  +  `I` unter Mac), und geben Sie Feedback-oder Funktionsanforderungen für das devtools ein.
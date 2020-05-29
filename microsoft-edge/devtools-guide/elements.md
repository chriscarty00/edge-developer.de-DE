---
description: Verwenden Sie das Panel Elemente, um die HTML-, CSS-, Dom-und Barrierefreiheit Ihrer Seite zu überprüfen.
title: DevTools-Elemente
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Elemente, HTML, CSS, Dom-Haltepunkte, Ereignisse, Barrierefreiheit
ms.custom: seodec18
ms.openlocfilehash: 8948ddb3291bd122521e0b0800c0113a576d49e4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568427"
---
# Elemente

Das Panel " **Elemente** " hilft Ihnen dabei, Folgendes zu tun:

* [Identifizieren und Bearbeiten von Elementen in der HTML-Struktur](#html-tree-view) der aktuellen Seite
* Über [prüfen und Ändern von CSS](./elements/styles.md) auf der Seite, einschließlich Pseudo Zuständen und Pseudo Elementen
* Grund [Legendes zu den CSS-Layouts und-Stilen](./elements/computed.md) auf der Seite
* [Aufspüren von Rogue-Ereignishandlern](./elements/events.md) , damit Sie diese Debuggen können
* [Festlegen von Debug-Haltepunkten für unerwartete visuelle Änderungen](./elements/dom-breakpoints.md) , um in den Code zu springen, der Sie verursacht
* [Abrufen detaillierter Informationen zu den Schriftarten, die auf der Seite verwendet](./elements/fonts.md) werden, und von der Stelle, von der Sie geladen werden
* [Anzeigen der Seite aus der Sicht einer Bildschirmsprachausgabe](./elements/accessibility.md) , um die Barrierefreiheit zu überprüfen und zu testen 
* [Überprüfen einer ausgeführten Unterschiede der CSS-Änderungen](./elements/changes.md) , die Sie beim Debuggen der Benutzeroberfläche Ihrer Seite vornehmen

## HTML-Strukturansicht

![Das Microsoft Edge devtools-Element Panel](./media/elements.png)

1. Verwenden Sie das Tool **SELECT Element** ( `Ctrl+B` ), um ein Element in der **HTML-Strukturansicht** zu finden, indem Sie auf der Seite darauf klicken.

2. Verwenden Sie das Tool zum **hervorheben von Elementen** ( `Ctrl+Shift+L` ), um ein Element auf der Seite zu finden, indem Sie in der **HTML-Strukturansicht**darauf zeigen.

3. Öffnen Sie das Tool **Farbauswahl** ( `Ctrl+K` ), um eine Liste der verwendeten Farben auf der aktuellen Seite anzuzeigen. Wenn Sie auf eine Farbe in der Liste klicken, werden weitere Details angezeigt (Farbton, Sättigung, Helligkeit, Alpha). Die *Farbauswahl* wird auch geöffnet, wenn Sie im Bereich **Formatvorlagen** auf das farbige Quadrat neben einem Farbwert klicken, sodass Sie die Farbe eines Seitenelements bearbeiten und sofort die Ergebnisse sehen können.

4. Die Schaltfläche **Barrierefreiheits Struktur** ( `Ctrl+Shift+A` ) öffnet den Bereich [Barrierefreiheit](./elements/accessibility.md) , in dem die Struktur der Seite angezeigt wird, wie dies bei einer Hilfstechnologie wie der [Windows-Sprachausgabe](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) Screenreader der Fall wäre.

5. Sie können auch **Find** `Ctrl+F` ein Element in der HTML-Strukturansicht suchen, indem Sie nach seinem Tagnamen, Attributen oder Textinhalt suchen.

### Bearbeiten von Elementen

Sie können ein Element bearbeiten, indem Sie in der HTML-Strukturansicht mit der rechten Maustaste darauf klicken und im Kontextmenü **als HTML bearbeiten** auswählen. Das Kontextmenü bietet auch Optionen zum Löschen, Ausschneiden, kopieren, einfügen, Einrichten von CSS-Pseudoklassen (*: aktiv*, *: Fokus*, *: hover*, *: besucht*) und Hinzufügen von Attributen. Eine weitere Möglichkeit zum Bearbeiten eines Attributs und/oder des zugehörigen Werts besteht darin, in der HTML-Strukturansicht auf das Attribut zu doppelklicken.

![Kontextmenü der HTML-Strukturansicht](./media/elements_html_tree_context.png)

> [!NOTE]
> Das Bearbeiten der HTML-Struktur hat keinen Einfluss auf das zugrunde liegende Quellmarkup. Beim Aktualisieren der Seite werden Ihre Änderungen zurückgesetzt und nur das Layout gerendert, das von der Seitenquelle bestimmt wird. Sie können ihren geänderten HTML-Code in die Zwischenablage **Kopieren** , indem Sie mit der rechten Maustaste auf das gewünschte Element klicken (oder das globale `html` Element, wenn die gesamte Seite angezeigt werden soll), um das Kontextmenü zu öffnen. (Optionen für**Ausschneiden** und **Einfügen** sind ebenfalls verfügbar).

Im Bereich " [Formatvorlagen](./elements/styles.md) " können Sie auch CSS-Pseudo Zustände und Pseudoelemente hinzufügen/löschen oder bearbeiten.

## Tool Bereiche

Nachdem Sie ein interessantes Seitenelement ausgewählt haben, können Sie die Toolfenster verwenden, um die unterschiedlichen Formatvorlagen und Barrierefreiheitseigenschaften weiter zu überprüfen, die Ereignislistener anzuzeigen und die Haltepunkte für die DOM-Mutation festzulegen.

![Fenster ' Tools ' im Bereich ' Elemente '](./media/elements_toolpanes.png)

1. [**Formatvorlagen**](./elements/styles.md): aktuell angewendete Formatvorlagen, die nach Stylesheets angeordnet sind

2. [**Berechnet**](./elements/computed.md): aktuell angewendete Formatvorlagen, die nach CSS-Attributen strukturiert sind

3. [**Ereignisse**](./elements/events.md): Ereignis-Listener, die für das aktuelle Element und übergeordnete Elemente registriert sind

4. [**DOM-Haltepunkte**](./elements/dom-breakpoints.md): Dom-mutations Haltepunkte 

5. [**Schriftarten**](./elements/fonts.md): aktuell angewendete Schriftarten für ein ausgewähltes Element

6. [**Barrierefreiheit**](./elements/accessibility.md): Barrierefreiheitseigenschaften

7. [**Änderungen**](./elements/changes.md): während der Diagnosesitzung vorgenommene CSS-Änderungen  

## Kombinationen

| Aktion               | Tastenkombination               |
|:---------------------|:-----------------------|
| Element Panel       | `Ctrl` + `1`           |
| Element Hervorhebung | `Ctrl` + `Shift` + `L` |
| Element auswählen       | `Ctrl` + `B`           |
| Farbwähler         | `Ctrl` + `K`           |
| Barrierefreiheits Struktur   | `Ctrl` + `Shift` + `A` |

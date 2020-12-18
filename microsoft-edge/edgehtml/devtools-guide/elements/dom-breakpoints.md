---
description: Verwenden von Dom-Haltepunkten zum visuellen Debuggen von Layout-Pannen auf Ihrer Seite
title: DevTools-Elemente-Dom-Haltepunkte
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Elemente, Dom-Haltepunkte, Dom-Mutation
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb60fa0497c98c152ca2c5adf28e9dee5d7c9f98
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233850"
---
# DOM-Haltepunkte

Verwalten Sie Ihre Dom-mutations Haltepunkte in diesem Bereich, einschließlich Deaktivierung, löschen und erneute Bindung.

Sie können Dom-mutations Haltepunkte verwenden, um in den Debugger einzubrechen, wenn sich ein ausgewählter Elementknoten ändert. Dies ist hilfreich bei der Nachverfolgung des Codes, der für das Auslösen von visuellen Problemen mit der Benutzeroberfläche verantwortlich ist, ohne einzelne Haltepunkte für jede der 450 + DOM-APIs in *EdgeHTML* festzulegen, die solche Änderungen auslösen können. 

Zum Festlegen eines DOM-Haltepunkts klicken Sie mit der rechten Maustaste auf ein beliebiges Element in der *HTML-Strukturansicht* des **Elements** Panels, um das Kontextmenü zu öffnen.

![Dom-Haltepunkte-Kontextmenü](../media/elements_dom_breakpoints_contextmenu.png)

Sie können einen der folgenden Haltepunkte festlegen:

 - **Unterbrechung beim Entfernen des Knotens**: unterbrechen Sie den Debugger, wenn das ausgewählte Element aus dem Dokument entfernt wird (DOM-Struktur).

 - **Unterbrechung**in der Teilstruktur geändert: unterbrechen Sie den Debugger, wenn eines der Nachfolgerelemente des ausgewählten Elements geändert (hinzugefügt, entfernt oder deren unter Strukturen geändert wurden). Dies wird nicht unterbrechen, wenn Attribute geändert werden (siehe die nächste Option dafür).

 - **Break-on-Attribut geändert**: unterbrechen Sie den Debugger, wenn ein Attribut des ausgewählten Elements hinzugefügt, entfernt oder in Value geändert wird.

Der Bereich " **DOM-Haltepunkte** " listet dann das ausgewählte Element auf (durch Generieren einer Auswahl, die seine Position im Dom beschreibt) und die Typen von Haltepunkten, die Sie festlegen (*Knoten entfernt, Struktur geändert, Attribut geändert*). Von hier aus können Sie Ihre Haltepunkte auch einzeln (über das RT-Click-Kontextmenü) oder alle gleichzeitig (mithilfe der Schaltflächen) erneut *binden*, *Deaktivieren*oder *Löschen* .

![Bereich "Dom-Haltepunkte"](../media/elements_dom_breakpoints.png)

## Haltepunkt Persistenz

Haltepunkte werden im Rahmen ihrer devtools-Einstellungen gespeichert (und sind auf die URL der Seite beschränkt, in der Sie sich befinden). Wenn die Seite neu geladen wird oder die Tools geschlossen und erneut geöffnet werden, versucht devtools, die Haltepunkte erneut an die zugehörigen Elemente zu binden.

Haltepunkte, die nicht automatisch erneut gebunden werden konnten, werden mit einem Warnungssymbol im Kreis des Haltepunkts angezeigt. Für diese können Sie warten, bis das Element manuell (mithilfe der Schaltfläche " **Haltepunkt erneut binden** " und/oder der Kontextmenüoption) erneut gebunden wird, sobald ein entsprechendes Element im DOM angezeigt wird (und das Symbol "Haltepunkt" nicht mehr die Warnanzeige zeigt) oder den Haltepunkt ganz **Löschen** .

![Indikator für ungebundenen Haltepunkt](../media/elements_dom_breakpoint_unbound.png)

Zusätzlich zu diesem Bereich des *DOM-Haltepunkts* können Sie auch Ihre [DOM-Haltepunkte](../debugger.md#dom-breakpoints) im **Debugger**verwalten.

## Aktuelle Einschränkungen

Beachten Sie die folgenden Einschränkungen des Debuggens von Dom-Haltepunkten in Edge-devtools:

- Edge-devtools unterstützen derzeit keine rebindungs Haltepunkte innerhalb von [ `<iframe>` s](https://developer.mozilla.org/docs/Web/HTML/Element/iframe). Wenn Sie einen Haltepunkt in einem IFRAME festlegen und den Edge-devtools schließen oder die Seite aktualisieren, geht der Haltepunkt verloren.

- Wenn Ihr Skript vor Abschluss des DOM einen synchron ausgeführten Haltepunkt findet [`readyState`](https://developer.mozilla.org/docs/Web/API/Document/readyState) , können Sie keinen DOM-Haltepunkt festlegen, während der Debugger angehalten wird. Sie können diese Situation in der Regel beheben, indem Sie die [`defer`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) oder [`async`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) Skript Attribute festlegen.

- Für synchrone Skripts wird die automatische erneute Bindung von Haltepunkten ausgelöst, wenn das [`window.onload`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/onload) Ereignis aufgerufen wird. In diesem Fall verpassen wir möglicherweise Bindungs Haltepunkte, die während des anfänglichen skriptgesteuerten Aufbaus des DOM ausgelöst werden. Bei asynchronen Skripts wird ein erneuter Binde Versuch ausgelöst, bevor das erste Skript ausgeführt wird, sodass Ihre Haltepunkte ggf. erneut gebunden und ausgelöst werden können.

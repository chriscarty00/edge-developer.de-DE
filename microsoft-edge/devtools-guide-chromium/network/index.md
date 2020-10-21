---
description: Ein Lernprogramm zu den am häufigsten verwendeten netzwerkbezogenen Features in Microsoft Edge devtools
title: Überprüfen der Netzwerkaktivität in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: a55ff05e29817c483cbf13b8713ef37cf96424d5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125426"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.  
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# Überprüfen der Netzwerkaktivität in Microsoft Edge devtools  

Hierbei handelt es sich um ein praktisches Lernprogramm einiger der am häufigsten verwendeten devtools-Features im Zusammenhang mit der Überprüfung der Netzwerkaktivität für eine Seite.  

Weitere Informationen finden Sie unter [Netzwerk Referenz][DevtoolsNetworkReference] , wenn Sie stattdessen Features durchsuchen möchten.  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## Verwendung des Netzwerk Panels  

Verwenden Sie im Allgemeinen das Netzwerk Panel, wenn Sie sicherstellen möchten, dass Ressourcen wie erwartet heruntergeladen oder hochgeladen werden.  Die häufigsten Anwendungsfälle für das Netzwerk Panel sind:  

*   Sicherstellen, dass Ressourcen tatsächlich hochgeladen oder überhaupt heruntergeladen werden.  
*   Überprüfen der Eigenschaften einer einzelnen Ressource, wie HTTP-Header, Inhalt, Größe usw.  
    
Wenn Sie nach Möglichkeiten suchen, die Seiten Ladeleistung zu verbessern, beginnen Sie **nicht** mit dem Netzwerk Panel.  Es gibt viele Arten von Problemen mit der Auslastungs Leistung, die nicht mit der Netzwerkaktivität zusammenhängen.  Beginnen Sie mit dem Überwachungs Panel, da Sie gezielte Vorschläge zum Verbessern Ihrer Seite erhalten.  Weitere Informationen finden Sie unter [Optimieren der Website Geschwindigkeit][DevtoolsSpeedGetStarted].  

## Öffnen des Netzwerk Panels  

Um dieses Lernprogramm optimal zu nutzen, öffnen Sie die Demo und testen Sie die Features auf der Demo-Seite.  

1.  Öffnen [Sie die Demo für erste Schritte][GlitchNetworkGetStarted].  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       Die Demo  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="Die Demo" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  [Öffnen Sie devtools][DevToolsOpen] , indem Sie `Control` + `Shift` + `J` \ (Windows, Linux \) oder `Command` + `Option` + `J` \ (macOS \) drücken.  Das **Konsolen** Fenster wird geöffnet.  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-console.msft.png":::
       Der **Konsole**  
    :::image-end:::  
    
    Sie können [devtools am unteren Rand des Fensters andocken][DevToolsCustomizePlacement].  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-console-bottom.msft.png":::
       DevTools an den unteren Rand des Fensters angedockt  
    :::image-end:::  
    
1.  Wählen Sie die Registerkarte **Netzwerk** aus.  Das **Netzwerk** Fenster wird geöffnet.  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-bottom.msft.png":::
       **Konsolen** Tool im devtools, das am unteren Rand des Fensters angedockt ist  
    :::image-end:::  
    
Im Moment ist das Netzwerk Panel leer.  DevTools protokolliert nur Netzwerkaktivitäten, nachdem Sie Sie geöffnet haben und seit dem Öffnen von devtools keine Netzwerkaktivität stattgefunden hat.  

## Protokollieren von Netzwerkaktivitäten  

So zeigen Sie die Netzwerkaktivität an, die eine Seite verursacht:  

1.  Laden Sie die Seite neu.  Das Netzwerk Panel protokolliert alle Netzwerkaktivitäten im **Netzwerkprotokoll**.  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network.msft.png":::
       Das **Netzwerkprotokoll**  
    :::image-end:::  
    
    Jede Zeile des **Netzwerkprotokolls** stellt eine Ressource dar.  Standardmäßig werden die Ressourcen in chronologischer Reihenfolge aufgeführt.  Die oberste Ressource ist in der Regel das wichtigste HTML-Dokument.  Die untere Ressource ist, was zuletzt angefordert wurde.  
    
    Jede Spalte stellt Informationen zu einer Ressource dar.  In der vorhergehenden Abbildung werden die Standardspalten angezeigt.  

    *   **Status**aus.  Der HTTP-Statuscode für die Antwort.  
    *   **Typ**.  Der Ressourcentyp.  
    *   **Initiator**.  Die Ursache der Ressourcenanforderung.  Wenn Sie einen Link in der Spalte Initiator auswählen, gelangen Sie zu dem Quellcode, der die Anforderung verursacht hat.  
    *   **Zeit**.  Die Dauer der Anforderung.  
    *   **Wasserfall**.  Eine grafische Darstellung der verschiedenen Phasen der Anforderung.  Zeigen Sie mit der Maus auf einen Wasserfall, um eine Unterbrechung anzuzeigen.  
    
    > [!NOTE]
    > Das Diagramm oberhalb des Netzwerkprotokolls wird als Übersicht bezeichnet.  Sie werden das Übersichtsdiagramm in diesem Lernprogramm nicht verwenden, sodass Sie es möglicherweise ausblenden können.  Weitere Informationen finden Sie unter [Ausblenden des][DevtoolsReferenceHideOverview]Übersichtsbereichs.
    
1.  Nachdem Sie devtools geöffnet haben, werden die Netzwerkaktivitäten im Netzwerkprotokoll aufgezeichnet.  
    Um dies zu veranschaulichen, schauen Sie sich zuerst den unteren Rand des **Netzwerkprotokolls** an und machen Sie sich mit der letzten Aktivität auf den Kopf.  
1.  Wählen Sie nun in der Demo die Schaltfläche **Daten abrufen** aus.  
1.  Sehen Sie sich die untere Seite des **Netzwerkprotokolls** erneut an.  Es sollte eine neue Ressource mit dem Namen angezeigt werden `getstarted.json` .  Durch Auswählen der Schaltfläche " **Daten abrufen** " wurde die Datei von der Seite angefordert.  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       Eine neue Ressource im **Netzwerkprotokoll**  
    :::image-end:::  
    
## Weitere Informationen anzeigen  

Die Spalten des Netzwerkprotokolls können konfiguriert werden.  Sie können Spalten, die Sie nicht verwenden, ausblenden.  
Es gibt auch viele Spalten, die standardmäßig ausgeblendet sind, die Sie möglicherweise als nützlich empfinden.  

1.  Klicken Sie mit der rechten Maustaste auf die Kopfzeile der Netzwerkprotokoll Tabelle, und wählen Sie **Domäne**aus.  Die Domäne jeder Ressource wird nun angezeigt.  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       Aktivieren der Spalte "Domäne"  
    :::image-end:::  
    
    > [!TIP]
    > Zeigen Sie die vollständige URL einer Ressource an, indem Sie in der Spalte **Name** auf die Zelle zeigen.  
    
## Simulieren einer langsameren Netzwerkverbindung  

Die Netzwerkverbindung des Computers, den Sie zum Erstellen von Websites verwenden, ist wahrscheinlich schneller als die Netzwerkverbindungen der mobilen Geräte ihrer Benutzer.  Durch Drosselung der Seite erhalten Sie eine bessere Vorstellung davon, wie lange eine Seite zum Laden auf einem mobilen Gerät dauert.  

1.  Wählen Sie die Dropdownliste **Drosselung** aus, die standardmäßig auf **Online** gesetzt ist.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-throttling.msft.png":::
       Aktivieren der Drosselung  
    :::image-end:::  
    
1.  Wählen Sie **Slow 3G**aus.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       Wählen Sie Slow 3G aus.  
    :::image-end:::  
    
1.  Lange drücken Sie **Reload** (Reload ![ ][ImageRefreshIcon] \), und wählen Sie dann **Cache leeren und Hard Reload**aus.  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **Leerer Cache und schweres erneutes Laden**  
    :::image-end:::  
    
    Bei wiederholten Besuchen dient der Browser in der Regel einigen Dateien aus dem [Cache][MDNHTTPCache], wodurch die Seitenauslastung beschleunigt wird.  **Leerer Cache und harter Reload** erzwingt den Browser, das Netzwerk für alle Ressourcen zu wechseln.  Dies ist hilfreich, wenn Sie sehen möchten, wie ein Erstbesucher eine Seitenbelastung erlebt.  
    
    > [!NOTE]
    > Der Workflow " **leerer Cache" und "harter Reload** " steht nur zur Verfügung, wenn devtools geöffnet ist.  
    
## Screenshots aufzeichnen  

Mit Screenshots können Sie sehen, wie eine Seite im Laufe der Zeit aussah, während Sie geladen wurde.  

1.  Wählen Sie \ ( ![ Netzwerkeinstellungen ][ImageSettingsIcon] \) aus, und aktivieren Sie das Kontrollkästchen **Screenshots aufnehmen** .
1.  Laden Sie die Seite erneut über den **leeren Cache und** den Arbeitsablauf für das erneute Laden.  Weitere Informationen hierzu finden Sie unter [Simulieren einer langsameren Verbindung](#simulate-a-slower-network-connection) .  
    Der Bereich "Screenshots" bietet Miniaturansichten, wie die Seite während des Ladevorgangs an verschiedenen Punkten aussah.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       Screenshots des Ladens der Seite  
    :::image-end:::  
    
1.  Wählen Sie die erste Miniaturansicht aus.  DevTools zeigt Ihnen, welche Netzwerkaktivität zu diesem Zeitpunkt stattgefunden hat.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       Die Netzwerkaktivität, die während des ersten Screenshots stattgefunden hat  
    :::image-end:::  
    
1.  Wählen Sie erneut \ ( ![ Netzwerkeinstellungen ][ImageSettingsIcon] \) aus, und deaktivieren Sie das Kontrollkästchen **Screenshots aufnehmen** , um den Bereich Screenshots zu schließen.
1.  Laden Sie die Seite erneut.  
    
## Überprüfen der Details der Ressource  

Wählen Sie eine Ressource aus, um weitere Informationen dazu zu erhalten.  Probieren Sie es jetzt aus:  

1.  Wählen Sie aus `getstarted.html` .  Die Registerkarte über **Schriften** wird angezeigt.  Verwenden Sie diese Registerkarte, um HTTP-Header zu überprüfen.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       Die Registerkarte "über **Schriften** "  
    :::image-end:::  
    
1.  Wählen Sie die Registerkarte **Vorschau** aus.  Eine grundlegende Darstellung des HTML-Code wird angezeigt.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       Registerkarte " **Vorschau** "  
    :::image-end:::  
    
    Diese Registerkarte ist hilfreich, wenn eine API einen Fehlercode in HTML zurückgibt.  Möglicherweise ist es einfacher, den gerenderten HTML-Code zu lesen als den HTML-Quellcode, oder wenn Sie Bilder untersuchen.  

1.  Wählen Sie die Registerkarte **Antwort** aus.  Der HTML-Quellcode wird angezeigt.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       Die Registerkarte " **Antwort** "  
    :::image-end:::  
    
    > [!TIP]
    > Wenn eine Datei minimierte ist, wird durch Auswählen der Schaltfläche **Format** \ ( ![ Format ][ImageFormatIcon] \) am unteren Rand der Registerkarte **Antwort** der Inhalt der Datei zur Lesbarkeit neu formatiert.  
    
1.  Wählen Sie die Registerkarte **Anzeige** Dauer aus.  Eine Aufschlüsselung der Netzwerkaktivität für diese Ressource wird angezeigt.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       Registerkarte " **Anzeige** Dauer"  
    :::image-end:::  
    
1.  Wählen Sie **Schließen** \ ( ![ Schließen ][ImageCloseIcon] \) aus, um das Netzwerkprotokoll erneut anzuzeigen.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       Schaltfläche " **Schließen** "  
    :::image-end:::  
    
## Durchsuchen von Netzwerk Kopfzeilen und-Antworten  

Verwenden Sie den **Such** Bereich, wenn Sie die HTTP-Header und Antworten aller Ressourcen nach einer bestimmten Zeichenfolge oder einem regulären Ausdruck durchsuchen müssen.  

Angenommen, Sie möchten beispielsweise überprüfen, ob Ihre Ressourcen angemessene **Cacherichtlinien**verwenden.  

<!--TODO: add cache policies section when available  -->

1.  Wählen Sie **Suchen** \ ( ![ Suchen ][ImageSearchIcon] \) aus.  Der Suchbereich wird links neben dem Netzwerkprotokoll geöffnet.  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       Der **Such** Bereich  
    :::image-end:::  
    
1.  Geben `Cache-Control` Sie ein, und wählen Sie aus `Enter` .  Der Suchbereich listet alle Instanzen auf `Cache-Control` , die in Ressourcen Kopfzeilen oder-Inhalten gefunden werden.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       Suchergebnisse‎‏ für:  `Cache-Control`  
    :::image-end:::  
    
1.  Wählen Sie ein Ergebnis aus, um die Ressource anzuzeigen, in der das Ergebnis gefunden wurde.  Wenn Sie die Details der Ressource sehen möchten, wählen Sie ein Ergebnis aus, um direkt dorthin zu wechseln.  Wenn die Abfrage beispielsweise in einer Kopfzeile gefunden wurde, wird die Registerkarte Überschriften geöffnet.   Wenn die Abfrage im Inhalt gefunden wurde, wird die Registerkarte " **Antwort** " geöffnet.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       Auf der Registerkarte "über **Schriften** " hervorgehobenes Suchergebnis  
    :::image-end:::  
    
1.  Schließen Sie den Suchbereich und die Registerkarte Überschriften.  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-search-close.msft.png":::
       Die Schaltflächen " **Schließen** "  
    :::image-end:::  
    
## Filtern von Ressourcen  

DevTools bietet zahlreiche Workflows zum Filtern von Ressourcen, die für die jeweilige Aufgabe nicht relevant sind.  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   Die Symbolleiste " **Filter** "  
:::image-end:::  

Die **Filter** Symbolleiste sollte standardmäßig aktiviert sein.  Wenn nicht,:  

1.  Wählen Sie **Filter** \ ( ![ Filter ][ImageFilterIcon] \) aus, um Sie anzuzeigen.  
    
### Filtern nach Zeichenfolge, regulärem Ausdruck oder Eigenschaft  

Das Textfeld " **Filter** " unterstützt viele verschiedene Filterarten.  

1.  Geben Sie `png` in das Textfeld **Filter** ein.  Nur die Dateien, die den Text enthalten, `png` werden angezeigt.  In diesem Fall sind die einzigen Dateien, die dem Filter entsprechen, die PNG-Bilder.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       Ein Zeichenfolgenfilter  
    :::image-end:::  
    
1.  Geben Sie `/.*\.[cj]s+$/` ein.  DevTools filtert jede Ressource mit einem Dateinamen, der nicht mit a `j` oder a, `c` gefolgt von 1 oder mehr Zeichen, endet `s` .  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       Ein Filter für reguläre Ausdrücke  
    :::image-end:::  
    
1.  Geben Sie `-main.css` ein.  DevTools filtert aus `main.css` .  Wenn eine andere Datei mit dem Muster übereinstimmt, würden Sie ebenfalls herausgefiltert.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       Ein negativer Filter  
    :::image-end:::  
    
1.  Geben Sie `domain:cdn.glitch.com` in das Textfeld **Filter** ein.  DevTools filtert jede Ressource mit einer URL ab, die dieser Domäne nicht entspricht.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       Ein Eigenschaften Filter  
    :::image-end:::  
    
    Die vollständige Liste der filterbaren Eigenschaften finden Sie unter [Filtern von Anforderungen nach Eigenschaften][DevtoolsReferenceProperty] .  
    
1.  Deaktivieren Sie das Textfeld " **Filter** " eines beliebigen Texts.  
    
### Nach Ressourcentyp Filtern  

So konzentrieren Sie sich auf eine bestimmte Art von Datei, beispielsweise Stylesheets:  

1.  Wählen Sie **CSS**aus.  Alle anderen Dateitypen werden herausgefiltert.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       Nur CSS-Dateien anzeigen  
    :::image-end:::  
    
1.  Wenn Sie auch Skripts anzeigen möchten, halten Sie `Control` \ (Windows, Linux \) oder `Command` \ (macOS \) gedrückt, und wählen Sie dann **js**aus.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       Nur CSS-und JS-Dateien anzeigen  
    :::image-end:::  
    
1.  Wählen Sie **alle** aus, um die Filter zu entfernen und alle Ressourcen erneut anzuzeigen.  
    
Weitere Informationen finden Sie unter [Filteranforderungen][DevtoolsNetworkReferenceFilter] für andere Filter Workflows.  

## Anfragen blockieren  

Wie wird eine Seite aussehen und sich Verhalten, wenn einige Seitenressourcen nicht verfügbar sind?  Funktioniert es nicht vollständig, oder ist es immer noch etwas funktionell?  Anfragen blockieren, um Folgendes zu erfahren:  

1.  Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das **Befehlsmenü**zu öffnen.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Geben `block` Sie die Option **Blockierungs Anforderung anzeigen**ein, und wählen Sie aus `Enter` .  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **Anforderungs Blockierung anzeigen**  
    :::image-end:::  
    
1.  Wählen Sie **Muster hinzufügen** \ ( ![ Muster hinzufügen ][ImageAddIcon] \) aus.  
1.  Geben Sie `main.css` ein.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       Blockieren `main.css`  
    :::image-end:::  
    
1.  Wählen Sie **Hinzufügen**.  
1.  Laden Sie die Seite neu.  Wie erwartet, wird das Design der Seite etwas durcheinander gebracht, da das Haupt-Stylesheet blockiert wurde.  
    
    > [!NOTE]
    > Die `main.css` Zeile im Netzwerkprotokoll.  Der rote Text bedeutet, dass die Ressource blockiert wurde.
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` wurde blockiert  
    :::image-end:::  
    
1.  Deaktivieren Sie das Kontrollkästchen **Anforderungs Blockierung aktivieren** .  

## Fazit  

Herzlichen Glückwunsch, Sie haben das Lernprogramm abgeschlossen.  Sie wissen jetzt, wie Sie das **Netzwerk** Panel im Microsoft Edge-devtools verwenden!

Navigieren Sie zu der [Netzwerk Referenz][DevtoolsNetworkReference] , um weitere devtools-Features im Zusammenhang mit der Überprüfung von Netzwerkaktivitäten zu entdecken.  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Ändern der Position von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsNetworkReference]: ./reference.md "Netzwerkanalyse Referenz | Microsoft docs"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Filter Anforderungen – Netzwerkanalyse Referenz | Microsoft docs"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Ausblenden des Übersichtsbereichs-Netzwerkanalyse Referenz | Microsoft docs"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filtern von Anforderungen nach Eigenschaften-Netzwerkanalyse Referenz | Microsoft docs"
[DevToolsOpen]: ../open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools | Microsoft docs"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Überprüfen der Netzwerk Aktivitäts Demo | Glitch"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "HTTP-Caching | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

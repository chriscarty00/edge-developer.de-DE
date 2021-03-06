---
description: Ein Lernprogramm zu den beliebtesten netzwerkbezogenen Features in Microsoft Edge DevTools.
title: Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 16b60716c91d2f4ce778f1fac37afc0e73e30ab6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398658"
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

# <a name="inspect-network-activity-in-microsoft-edge-devtools"></a>Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools  

Dies ist ein praktisches Lernprogramm zu einigen der am häufigsten verwendeten DevTools-Features im Zusammenhang mit der Überprüfung der Netzwerkaktivität für eine Seite.  

Wenn Sie Features durchsuchen möchten, navigieren Sie zu [Netzwerkreferenz][DevtoolsNetworkReference].  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <a name="when-to-use-the-network-panel"></a>Verwendung des Netzwerkbereichs  

Verwenden Sie im Allgemeinen den Netzwerkbereich, wenn Sie sicherstellen müssen, dass Ressourcen wie erwartet heruntergeladen oder hochgeladen werden.  Die häufigsten Verwendungsfälle für den Netzwerkbereich sind:  

*   Stellen Sie sicher, dass Ressourcen tatsächlich hochgeladen oder heruntergeladen werden.  
*   Überprüfen der Eigenschaften einer einzelnen Ressource, z. B. http-Header, Inhalt, Größe und so weiter.  
    
Wenn Sie nach Möglichkeiten zur Verbesserung der Seitenladeleistung suchen, **beginnen Sie nicht** mit dem **Netzwerktool.**  Es gibt viele Arten von Lastenleistungsproblemen, die nicht mit der Netzwerkaktivität in Zusammenhang stehen.  Beginnen Sie mit dem Prüfungspanel, da es Ihnen gezielte Vorschläge zur Verbesserung Ihrer Seite gibt.  Navigieren Sie zu [Optimieren der Websitegeschwindigkeit][DevtoolsSpeedGetStarted].  

## <a name="open-the-network-panel"></a>Öffnen des Netzwerkbereichs  

Um dieses Lernprogramm zu nutzen, öffnen Sie die Demo, und testen Sie die Features auf der Demoseite.  

1.  Öffnen Sie [die Erste Schritte Demo][GlitchNetworkGetStarted].  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Die Demo" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       Die Demo  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  Wählen [Sie zum Öffnen von DevTools][DevToolsOpen] `Control` + `Shift` + `J` \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.  Das **Konsolentool** wird geöffnet.  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="Die Konsole" lightbox="../media/network-glitch-console.msft.png":::
       Die **Konsole**  
    :::image-end:::  
    
    Möglicherweise docken Sie [DevTools am unteren Rand Des Fensters an.][DevToolsCustomizePlacement]  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools am unteren Rand des Fensters angedockt" lightbox="../media/network-glitch-console-bottom.msft.png":::
       DevTools am unteren Rand des Fensters angedockt  
    :::image-end:::  
    
1.  Öffnen Sie das **Netzwerktool.**  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Konsolentool in den DevTools, die am unteren Rand des Fensters angedockt sind" lightbox="../media/network-glitch-network-bottom.msft.png":::
       **Konsolentool** in den DevTools, die am unteren Rand des Fensters angedockt sind  
    :::image-end:::  
    
Derzeit ist das **Netzwerktool** leer.  DevTools protokolliert die Netzwerkaktivität nur, nachdem Sie sie geöffnet haben, und es sind seit dem Öffnen von DevTools keine Netzwerkaktivitäten aufgetreten.  

## <a name="log-network-activity"></a>Protokollnetzwerkaktivität  

So zeigen Sie die Netzwerkaktivität an, die von einer Seite verursacht wird:  

1.  Aktualisieren Sie die Webseite.  Im Netzwerkbereich werden alle Netzwerkaktivitäten im **Netzwerkprotokoll protokolliert.**  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Das Netzwerkprotokoll" lightbox="../media/network-glitch-network.msft.png":::
       Das **Netzwerkprotokoll**  
    :::image-end:::  
    
    Jede Zeile des **Netzwerkprotokolls stellt** eine Ressource dar.  Standardmäßig werden die Ressourcen chronologisch aufgelistet.  Die wichtigste Ressource ist in der Regel das Haupt-HTML-Dokument.  Die untere Ressource ist das, was zuletzt angefordert wurde.  
    
    Jede Spalte stellt Informationen zu einer Ressource dar.  In der vorherigen Abbildung werden die Standardspalten angezeigt.  

    *   **Status**.  Der HTTP-Statuscode für die Antwort.  
    *   **Typ**.  Der Ressourcentyp.  
    *   **Initiator**.  Die Ursache der Ressourcenanforderung.  Wenn Sie einen Link in der Spalte Initiator verwenden, erhalten Sie den Quellcode, der die Anforderung verursacht hat.  
    *   **Zeit**.  Die Dauer der Anforderung.  
    *   **Wasserfall**.  Eine grafische Darstellung der verschiedenen Phasen der Anforderung.  Zeigen Sie zum Anzeigen einer Aufschlüsselung auf einen Wasserfall.  
    
    > [!NOTE]
    > Das Diagramm über dem Netzwerkprotokoll wird als Übersicht bezeichnet.  Sie verwenden das Diagramm Übersicht in diesem Lernprogramm nicht, daher können Sie es ausblenden.  Navigieren Sie zu [Ausblenden des Übersichtsbereichs][DevtoolsReferenceHideOverview].
    
1.  Nachdem Sie DevTools geöffnet haben, wird die Netzwerkaktivität im Netzwerkprotokoll aufgezeichnet.  
    Um dies zu veranschaulichen, **** sehen Sie sich zunächst den unteren Rand des Netzwerkprotokolls an, und notieren Sie sich die letzte Aktivität.  
1.  Wählen Sie nun in der **Demo** die Schaltfläche Daten herunterladen aus.  
1.  Sehen Sie sich das Netzwerkprotokoll unten **erneut** an.  Eine neue Ressource namens `getstarted.json` wird angezeigt.  Um zu verursachen, dass die Webseite die Datei angibt, wählen Sie die Schaltfläche **Daten** anfordern aus.  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Eine neue Ressource im Netzwerkprotokoll" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       Eine neue Ressource im **Netzwerkprotokoll**  
    :::image-end:::  
    
## <a name="show-more-information"></a>Weitere Informationen anzeigen  

Die Spalten des Netzwerkprotokolls können konfiguriert werden.  Sie können Spalten ausblenden, die Sie nicht verwenden.  
Es gibt auch viele Spalten, die standardmäßig ausgeblendet sind und möglicherweise hilfreich sind.  

1.  Zeigen Sie auf die Kopfzeile der Tabelle Netzwerkprotokoll, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Domäne aus.**  Die Domäne der einzelnen Ressourcen wird nun angezeigt.  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Aktivieren der Spalte "Domäne"" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       Aktivieren der Spalte "Domäne"  
    :::image-end:::  
    
    > [!TIP]
    > Um die vollständige URL einer Ressource zu überprüfen, zeigen Sie auf die Zelle in der **Spalte Name.**  
    
## <a name="simulate-a-slower-network-connection"></a>Simulieren einer langsameren Netzwerkverbindung  

Die Netzwerkverbindung des Computers, den Sie zum Erstellen von Standorten verwenden, ist wahrscheinlich schneller als die Netzwerkverbindungen der mobilen Geräte Ihrer Benutzer.  Wenn Sie die Seite drosseln, erhalten Sie eine bessere Vorstellung davon, wie lange eine Seite zum Laden auf einem mobilen Gerät benötigt.  

1.  Wählen Sie **das Dropdownmenü Einschränkung** aus, das standardmäßig **auf Online** festgelegt ist.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Aktivieren der Einschränkung" lightbox="../media/network-glitch-network-throttling.msft.png":::
       Aktivieren der Einschränkung  
    :::image-end:::  
    
1.  Wählen **Sie Langsam 3G**aus.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Wählen Sie Langsame 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       Wählen Sie Langsame 3G  
    :::image-end:::  
    
1.  Lang drücken **Sie Reload** \( Reload ![ ][ImageRefreshIcon] \) und wählen Sie dann Leeren Cache und **Hard Reload aus.**  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Leerer Cache und Hard Reload" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **Leerer Cache und Hard Reload**  
    :::image-end:::  
    
    Bei wiederholten Besuchen werden im Browser in der Regel einige Dateien aus dem [Cache verwendet,][MDNHTTPCache]wodurch die Seitenlast beschleunigt wird.  **Leerer Cache und hard reload** erzwingt, dass der Browser für alle Ressourcen in das Netzwerk wechseln muss.  Verwenden Sie diese, um zu zeigen, wie ein Besucher beim ersten Mal eine Seite laden kann.  
    
    > [!NOTE]
    > Der **Workflow Leerer Cache und Hard Reload** ist nur verfügbar, wenn DevTools geöffnet ist.  
    
## <a name="capture-screenshots"></a>Screenshots erfassen  

Screenshots zeigen, wie eine Webseite im Laufe der Zeit aussieht, während sie geladen wird.  

1.  Wählen Sie \( ![ Netzwerkeinstellungen ][ImageSettingsIcon] \) aus, und aktivieren Sie das Kontrollkästchen Screenshots **erfassen.**
1.  Aktualisieren Sie die Seite erneut mithilfe des **Workflows Leerer Cache und Hard Reload.**  Navigieren Sie [zu Simulieren einer langsameren Verbindung,](#simulate-a-slower-network-connection) wenn Sie eine Erinnerung dazu benötigen.  
    Der Bildschirmfotobereich enthält Miniaturansichten, wie die Seite während des Ladevorgangs an verschiedenen Punkten betrachtet wurde.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Screenshots der Seitenlast" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       Screenshots der Seitenlast  
    :::image-end:::  
    
1.  Wählen Sie die erste Miniaturansicht aus.  DevTools zeigt Ihnen, welche Netzwerkaktivität zu diesem Zeitpunkt aufgetreten ist.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Die Netzwerkaktivität, die während des ersten Screenshots passierte" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       Die Netzwerkaktivität, die während des ersten Screenshots passierte  
    :::image-end:::  
    
1.  Wählen Sie \( Netzwerkeinstellungen \) erneut aus, und deaktivieren Sie das Kontrollkästchen Screenshots ![ ][ImageSettingsIcon] erfassen, um den Bildschirmfotobereich zu schließen. ****
1.  Aktualisieren Sie die Seite erneut.  
    
## <a name="inspect-the-details-of-the-resource"></a>Überprüfen der Details der Ressource  

Wählen Sie eine Ressource aus, um weitere Informationen dazu zu erhalten.  Probieren Sie es jetzt aus:  

1.  Wählen Sie `getstarted.html` aus.  Der **Bereich Kopfzeilen** wird angezeigt.  Verwenden Sie diesen Bereich, um HTTP-Header zu überprüfen.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Der Kopfzeilenbereich" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       Der **Kopfzeilenbereich**  
    :::image-end:::  
    
1.  Wählen Sie den **Bereich Vorschau** aus.  Es wird ein einfaches Rendern des HTML angezeigt.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Der Vorschaubereich" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       Der **Vorschaubereich**  
    :::image-end:::  
    
    Der Bereich ist hilfreich, wenn eine API einen Fehlercode in HTML zurückgibt.  Möglicherweise ist es einfacher, den gerenderten HTML-Code als den HTML-Quellcode zu lesen, oder wenn Sie Bilder überprüfen.  

1.  Wählen Sie den **Antwortbereich** aus.  Der HTML-Quellcode wird angezeigt.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Der Antwortbereich" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       Der **Antwortbereich**  
    :::image-end:::  
    
    > [!TIP]
    > Wenn eine Datei vermint wird, wählen Sie die Schaltfläche **Format** \( Format \) am unteren Rand des Antwortbereichs aus, um den Inhalt der Datei zur Lesbarkeit neu zu ![ ][ImageFormatIcon] **** formatieren.  
    
1.  Wählen Sie den **Zeitsteuerungsbereich** aus.  Eine Aufschlüsselung der Netzwerkaktivität für die Ressource wird angezeigt.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Der Zeitsteuerungsbereich" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       Der **Zeitsteuerungsbereich**  
    :::image-end:::  
    
1.  Wählen **Sie Schließen** \( Schließen ![ ][ImageCloseIcon] \) aus, um das Netzwerkprotokoll erneut anzeigen zu können.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Die Schaltfläche Schließen" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       Die **Schaltfläche** Schließen  
    :::image-end:::  
    
## <a name="search-network-headers-and-responses"></a>Durchsuchen von Netzwerkkopfzeilen und -antworten  

Verwenden Sie **den Suchbereich,** wenn Sie die HTTP-Header und -Antworten aller Ressourcen nach einer bestimmten Zeichenfolge oder einem regulären Ausdruck durchsuchen müssen.  

Angenommen, Sie möchten überprüfen, ob Ihre Ressourcen angemessene **Cacherichtlinien verwenden.**  

<!--TODO: add cache policies section when available  -->

1.  Wählen **Sie Suchen** \( Suche ![ ][ImageSearchIcon] \).  Der Suchbereich wird links vom Netzwerkprotokoll geöffnet.  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Der Suchbereich" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       Der **Suchbereich**  
    :::image-end:::  
    
1.  Geben `Cache-Control` Sie ein, und wählen Sie `Enter` aus.  Der Suchbereich listet alle Instanzen `Cache-Control` auf, die in Ressourcenkopfzeilen oder Inhalten gefunden werden.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Suchergebnisse für Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       Suchergebnisse‎‏ für:  `Cache-Control`  
    :::image-end:::  
    
1.  Wählen Sie ein Ergebnis aus, um die Ressource, in der das Ergebnis gefunden wurde, anzeigen zu können.  Wenn Sie sich die Details der Ressource anschauen, wählen Sie ein Ergebnis aus, um direkt zu ihr zu wechseln.  Wenn die Abfrage beispielsweise in einer Kopfzeile gefunden wurde, wird der **Bereich Kopfzeilen** geöffnet.   Wenn die Abfrage im Inhalt gefunden wurde, wird der **Antwortbereich** geöffnet.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Ein im Kopfzeilenbereich hervorgehobenes Suchergebnis" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       Ein im Kopfzeilenbereich **hervorgehobenes Suchergebnis**  
    :::image-end:::  
    
1.  Schließen Sie den Suchbereich und **den Kopfzeilenbereich.**  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Die Schaltflächen Schließen" lightbox="../media/network-glitch-network-search-close.msft.png":::
       Die **Schaltflächen** Schließen  
    :::image-end:::  
    
## <a name="filter-resources"></a>Filtern von Ressourcen  

DevTools bietet zahlreiche Workflows zum Filtern von Ressourcen, die für den jeweiligen Vorgang nicht relevant sind.  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Die Symbolleiste Filter" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   Die **Symbolleiste Filter**  
:::image-end:::  

Die **Symbolleiste** Filter sollte standardmäßig aktiviert sein.  Wenn nicht,:  

1.  Wählen **Sie Filter** \( Filter ![ ][ImageFilterIcon] \) aus, um es zu zeigen.  
    
### <a name="filter-by-string-regular-expression-or-property"></a>Filtern nach Zeichenfolge, regulärem Ausdruck oder Eigenschaft  

Das **Textfeld Filter** unterstützt viele verschiedene Filtertypen.  

1.  Geben `png` Sie in das Textfeld **Filter** ein.  Es werden nur die Dateien angezeigt, die `png` den Text enthalten.  In diesem Fall sind die einzigen Dateien, die mit dem Filter übereinstimmen, die PNG-Bilder.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Ein Zeichenfolgenfilter" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       Ein Zeichenfolgenfilter  
    :::image-end:::  
    
1.  Geben Sie `/.*\.[cj]s+$/` ein.  DevTools filtert jede Ressource mit einem Dateinamen heraus, der nicht mit einem oder mehreren Zeichen `j` `c` `s` endet.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Filter für reguläre Ausdrücke" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       Filter für reguläre Ausdrücke  
    :::image-end:::  
    
1.  Geben Sie `-main.css` ein.  DevTools filtert heraus `main.css` .  Wenn eine Datei dem Muster entspricht, wird auch der Titt herausgefiltert.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Ein negativer Filter" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       Ein negativer Filter  
    :::image-end:::  
    
1.  Geben `domain:cdn.glitch.com` Sie in das Textfeld **Filter** ein.  DevTools filtert jede Ressource mit einer URL heraus, die nicht mit dieser Domäne übereinstimmen.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Ein Eigenschaftenfilter" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       Ein Eigenschaftenfilter  
    :::image-end:::  
    
    Navigieren Sie zur vollständigen Liste der filterbaren Eigenschaften zu [Filter requests by properties][DevtoolsReferenceProperty].  
    
1.  Löschen Sie **das Textfeld Filter** eines beliebigen Texts.  
    
### <a name="filter-by-resource-type"></a>Filtern nach Ressourcentyp  

So konzentrieren Sie sich auf einen bestimmten Dateityp, z. B. Stylesheets:  

1.  Wählen Sie **CSS**aus.  Alle anderen Dateitypen werden herausgefiltert.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Nur CSS-Dateien anzeigen" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       Nur CSS-Dateien anzeigen  
    :::image-end:::  
    
1.  Um auch Skripts anzeigen zu können, wählen Sie `Control` \(Windows, Linux\) oder \(macOS\) aus, und wählen `Command` Sie **dann JS aus.**  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Nur CSS- und JS-Dateien anzeigen" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       Nur CSS- und JS-Dateien anzeigen  
    :::image-end:::  
    
1.  Wenn Sie die Filter entfernen und alle Ressourcen erneut anzeigen möchten, wählen Sie **Alle aus.**  
    
Navigieren Sie für andere Filterworkflows zu [Filteranforderungen][DevtoolsNetworkReferenceFilter].  

## <a name="block-requests"></a>Blockieren von Anforderungen  

Wie sieht eine Seite aus und verhält sich, wenn einige der Seitenressourcen nicht verfügbar sind?  Ist der Fehler vollständig, oder ist er noch ein wenig funktionsfähig?  Blockieren von Anforderungen zum Herausfinden:  

1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Geben `block` Sie ein, wählen **Sie Anforderungsblockierung anzeigen**aus, und wählen Sie `Enter` aus.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Anzeigen der Anforderungsblockierung" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **Anzeigen der Anforderungsblockierung**  
    :::image-end:::  
    
1.  Wählen **Sie Muster hinzufügen** \( Muster hinzufügen ![ ][ImageAddIcon] \).  
1.  Geben Sie `main.css` ein.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Blockieren von main.css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       Blockieren `main.css`  
    :::image-end:::  
    
1.  Wählen Sie **Hinzufügen**.  
1.  Aktualisieren Sie die Seite.  Wie erwartet ist das Format der Seite etwas verfedert, da das Hauptformatblatt blockiert wurde.  
    
    > [!NOTE]
    > Die `main.css` Zeile im Netzwerkprotokoll.  Der rote Text bedeutet, dass die Ressource blockiert wurde.
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main.css wurde blockiert" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` wurde blockiert  
    :::image-end:::  
    
1.  Deaktivieren Sie das **Kontrollkästchen Anforderungsblockierung** aktivieren.  

## <a name="conclusion"></a>Fazit  

Herzlichen Glückwunsch, Sie haben das Lernprogramm abgeschlossen.  Sie wissen nun, wie Sie das **Netzwerktool** in den Microsoft Edge DevTools verwenden können.

Navigieren Sie zum [Netzwerkverweis,][DevtoolsNetworkReference] um weitere DevTools-Features im Zusammenhang mit der Überprüfung der Netzwerkaktivität zu ermitteln.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

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

[DevToolsCustomizePlacement]: ../customize/placement.md "Ändern der Platzierung von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkReference]: ./reference.md "Netzwerkanalysereferenz | Microsoft Docs"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Filteranforderungen – Netzwerkanalysereferenz | Microsoft Docs"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Ausblenden des Bereichs Übersicht – Netzwerkanalysereferenz | Microsoft Docs"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Filteranforderungen nach Eigenschaften – Netzwerkanalysereferenz | Microsoft Docs"
[DevToolsOpen]: ../open/index.md "Öffnen Sie Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimieren der Websitegeschwindigkeit mit Microsoft Edge DevTools | Microsoft Docs"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Inspect Network Activity Demo | Glitch"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "HTTP-Zwischenspeicherung | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

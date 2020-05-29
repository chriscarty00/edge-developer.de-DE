---
title: Überprüfen der Netzwerkaktivität in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 267b0113e07085dd565a3ff3437a3fcac2dff9d7
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611812"
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

1.  Öffnen [Sie die Demo für erste Schritte][GlitchNetworkGetStarted] .  
    
    > ##### Abbildung1  
    > Die Demo  
    > ![Die Demo][ImagesTutorialDemo]  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    > ##### old Figure 2  
    > The demo in one window and this tutorial in a different window  
    > ![The demo in one window and this tutorial in a different window][ImagesTutorialWindows]  -->

1.  [Öffnen Sie devtools][DevToolsOpen] , indem Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \) drücken.  Das **Konsolen** Fenster wird geöffnet.  
    
    > ##### Abbildung2  
    > Der Konsole  
    > ! [Konsole] [ImagesTutorialConsole]  
    
    Sie können [devtools am unteren Rand des Fensters andocken][DevToolsCustomizePlacement].  
    
    > ##### Abbildung 3  
    > DevTools an den unteren Rand des Fensters angedockt  
    > ! [Devtools angedockt am unteren Rand des Fensters] [ImagesTutorialDocked]  

1.  Wählen Sie die Registerkarte **Netzwerk** aus.  Das Netzwerkfenster wird geöffnet.  
    
    > ##### Abbildung4  
    > DevTools an den unteren Rand des Fensters angedockt  
    > ! [Devtools angedockt am unteren Rand des Fensters] [ImagesTutorialNetwork]  

Im Moment ist das Netzwerk Panel leer.  DevTools protokolliert nur Netzwerkaktivitäten, nachdem Sie Sie geöffnet haben und seit dem Öffnen von devtools keine Netzwerkaktivität stattgefunden hat.  

## Protokollieren von Netzwerkaktivitäten   

So zeigen Sie die Netzwerkaktivität an, die eine Seite verursacht:  

1.  Laden Sie die Seite neu.  Das Netzwerk Panel protokolliert alle Netzwerkaktivitäten im **Netzwerkprotokoll**.  
    
    > ##### Abbildung5  
    > Das Netzwerkprotokoll  
    > ! [Netzwerkprotokoll] [ImagesTutorialLog]  
    
    Jede Zeile des **Netzwerkprotokolls** stellt eine Ressource dar.  Standardmäßig werden die Ressourcen in chronologischer Reihenfolge aufgeführt.  Die oberste Ressource ist in der Regel das wichtigste HTML-Dokument.  Die untere Ressource ist, was zuletzt angefordert wurde.  
    
    Jede Spalte stellt Informationen zu einer Ressource dar.  [**Abbildung 6**](#figure-6) zeigt die Standardspalten:  

    *   **Status**aus.  Der HTTP-Statuscode für die Antwort.  
    *   **Typ**.  Der Ressourcentyp.  
    *   **Initiator**.  Die Ursache der Ressourcenanforderung.  Wenn Sie einen Link in der Spalte Initiator auswählen, gelangen Sie zu dem Quellcode, der die Anforderung verursacht hat.  
    *   **Zeit**.  Die Dauer der Anforderung.  
    *   **Wasserfall**.  Eine grafische Darstellung der verschiedenen Phasen der Anforderung.  
        Zeigen Sie mit der Maus auf einen Wasserfall, um eine Unterbrechung anzuzeigen.  
    
    > [!NOTE]
    > Das Diagramm oberhalb des Netzwerkprotokolls wird als Übersicht bezeichnet.  Sie werden das Übersichtsdiagramm in diesem Lernprogramm nicht verwenden, sodass Sie es möglicherweise ausblenden können.  Weitere Informationen finden Sie unter [Ausblenden des][DevtoolsReferenceHideOverview]Übersichtsbereichs.
        
1.  Nachdem Sie devtools geöffnet haben, werden die Netzwerkaktivitäten im Netzwerkprotokoll aufgezeichnet.  
    Um dies zu veranschaulichen, schauen Sie sich zuerst den unteren Rand des **Netzwerkprotokolls** an und machen Sie sich mit der letzten Aktivität auf den Kopf.  
1.  Wählen Sie nun in der Demo die Schaltfläche **Daten abrufen** aus.  
1.  Sehen Sie sich die untere Seite des **Netzwerkprotokolls** erneut an.  Es sollte eine neue Ressource mit dem Namen angezeigt werden `getstarted.json` .  Durch Auswählen der Schaltfläche " **Daten abrufen** " wurde die Datei von der Seite angefordert.  
    
    > ##### Abbildung6  
    > Eine neue Ressource im Netzwerkprotokoll  
    > ! [Eine neue Ressource im Netzwerkprotokoll] [ImagesTutorialRuntime]  

## Weitere Informationen anzeigen   

Die Spalten des Netzwerkprotokolls können konfiguriert werden.  Sie können Spalten, die Sie nicht verwenden, ausblenden.  
Es gibt auch viele Spalten, die standardmäßig ausgeblendet sind, die Sie möglicherweise als nützlich empfinden.  

1.  Klicken Sie mit der rechten Maustaste auf die Kopfzeile der Netzwerkprotokoll Tabelle, und wählen Sie **Domäne**aus.  Die Domäne jeder Ressource wird nun angezeigt.  
    
    > ##### Abbildung7  
    > Aktivieren der Spalte "Domäne"  
    > ! [Aktivieren der Domänen Spalte] [ImagesTutorialDomain]  
    
    > [!TIP]
    > Zeigen Sie die vollständige URL einer Ressource an, indem Sie in der Spalte **Name** auf die Zelle zeigen.  

## Simulieren einer langsameren Netzwerkverbindung   

Die Netzwerkverbindung des Computers, den Sie zum Erstellen von Websites verwenden, ist wahrscheinlich schneller als die Netzwerkverbindungen der mobilen Geräte ihrer Benutzer.  Durch Drosselung der Seite erhalten Sie eine bessere Vorstellung davon, wie lange eine Seite zum Laden auf einem mobilen Gerät dauert.  

1.  Wählen Sie die Dropdownliste **Drosselung** aus, die standardmäßig auf **Online** gesetzt ist.  
    
    > ##### Abbildung8  
    > Aktivieren der Drosselung  
    > ! [Aktivieren der Drosselung] [ImagesTutorialThrottling]  
    
1.  Wählen Sie **Slow 3G**aus.  
    
    > ##### Abbildung 9  
    > Auswählen von Slow 3G  
    > ! [Auswahl von Slow 3G] [ImagesTutorialSlow3G]  
    
1.  Lange drücken Sie **Reload** Reload ![ ][ImageRefreshIcon] , und wählen Sie dann **Cache leeren und Hard Reload**aus.  
    
    > ##### Abbildung 10  
    > Leerer Cache und schweres erneutes Laden  
    > ! [Cache leeren und Hard Reload] [ImagesTutorialHardReload]  
    
    Bei wiederholten Besuchen dient der Browser in der Regel einigen Dateien aus dem [Cache][MDNHTTPCache] , wodurch die Seitenauslastung beschleunigt wird.  **Leerer Cache und harter Reload** erzwingt den Browser, das Netzwerk für alle Ressourcen zu wechseln.  Dies ist hilfreich, wenn Sie sehen möchten, wie ein Erstbesucher eine Seitenbelastung erlebt.  
    
    > [!NOTE]
    > Der Workflow " **leerer Cache" und "harter Reload** " steht nur zur Verfügung, wenn devtools geöffnet ist.  

## Screenshots aufzeichnen   

Mit Screenshots können Sie sehen, wie eine Seite im Laufe der Zeit aussah, während Sie geladen wurde.  

1.  Wählen Sie ![ Netzwerkeinstellungen aus ][ImageSettingsIcon] , und aktivieren Sie das Kontrollkästchen **Screenshots aufnehmen** .
1.  Laden Sie die Seite erneut über den **leeren Cache und** den Arbeitsablauf für das erneute Laden.  Weitere Informationen hierzu finden Sie unter [Simulieren einer langsameren Verbindung](#simulate-a-slower-network-connection) .  
    Der Bereich "Screenshots" bietet Miniaturansichten, wie die Seite während des Ladevorgangs an verschiedenen Punkten aussah.  
    
    > ##### Abbildung 11  
    > Screenshots des Ladens der Seite  
    > ! [Screenshots der Seite laden] [ImagesTutorialAllScreenshots]  

1.  Wählen Sie die erste Miniaturansicht aus.  DevTools zeigt Ihnen, welche Netzwerkaktivität zu diesem Zeitpunkt stattgefunden hat.  
    
    > ##### Abbildung 12  
    > Die Netzwerkaktivität, die während des ersten Screenshots stattgefunden hat  
    > ! [Die Netzwerkaktivität, die während des ersten Screenshots stattgefunden hat] [ImagesTutorialFirstScreenshot]  

1.  Wählen Sie ![ erneut Netzwerkeinstellungen aus, ][ImageSettingsIcon] und deaktivieren Sie das Kontrollkästchen **Screenshots aufnehmen** , um den Bereich Screenshots zu schließen.
1.  Laden Sie die Seite erneut.  

## Überprüfen der Details der Ressource   

Wählen Sie eine Ressource aus, um weitere Informationen dazu zu erhalten.  Probieren Sie es jetzt aus:  

1.  Wählen Sie aus `getstarted.html` .  Die Registerkarte über **Schriften** wird angezeigt.  Verwenden Sie diese Registerkarte, um HTTP-Header zu überprüfen.  
    
    > ##### Abbildung 13  
    > Die Registerkarte "Überschriften"  
    > ! [Die Registerkarte ' Überschriften '] [ImagesTutorialHeaders]  
    
1.  Wählen Sie die Registerkarte **Vorschau** aus.  Eine grundlegende Darstellung des HTML-Code wird angezeigt.  
    
    > ##### Abbildung 14  
    > Registerkarte "Vorschau"  
    > ! [Vorschau-Reiter] [ImagesTutorialPreview]  

     Diese Registerkarte ist hilfreich, wenn eine API einen Fehlercode in HTML zurückgibt.  Möglicherweise ist es einfacher, den gerenderten HTML-Code zu lesen als den HTML-Quellcode, oder wenn Sie Bilder untersuchen.  

1.  Wählen Sie die Registerkarte **Antwort** aus.  Der HTML-Quellcode wird angezeigt.  
    
    > ##### Abbildung 15  
    > Die Registerkarte "Antwort"  
    > ! [Die Registerkarte ' Antwort '] [ImagesTutorialResponse]  
    
    > [!TIP]
    > Wenn eine Datei minimierte ist, wird durch **Format** auswählen der ![ ][ImageFormatIcon] Schaltfläche Format Format unten auf der Registerkarte **Antwort** der Inhalt der Datei zur Lesbarkeit neu formatiert.  

1.  Wählen Sie die Registerkarte **Anzeige** Dauer aus.  Eine Aufschlüsselung der Netzwerkaktivität für diese Ressource wird angezeigt.  
    
    > ##### Abbildung 16  
    > Registerkarte "Anzeigedauer"  
    > ! [Die Registerkarte Anzeigedauer] [ImagesTutorialTiming]  

1.  Wählen **Sie schließen aus** ![ ][ImageCloseIcon] , um das Netzwerkprotokoll erneut anzuzeigen.  
    
    > ##### Abbildung 17  
    > Schaltfläche "Schließen"  
    > ! [Die Schaltfläche ' Schließen '] [ImagesTutorialCloseTiming]  

## Durchsuchen von Netzwerk Kopfzeilen und-Antworten   

Verwenden Sie den **Such** Bereich, wenn Sie die HTTP-Header und Antworten aller Ressourcen nach einer bestimmten Zeichenfolge oder einem regulären Ausdruck durchsuchen müssen.  

Angenommen, Sie möchten beispielsweise überprüfen, ob Ihre Ressourcen angemessene **Cacherichtlinien**verwenden.  

<!--TODO: add cache policies section when available  -->

1.  Wählen **Sie Suche suchen** aus ![ ][ImageSearchIcon] .  Der Suchbereich wird links neben dem Netzwerkprotokoll geöffnet.  
    
    > ##### Abbildung 18  
    > Der Suchbereich  
    > ! [Der Suchbereich] [ImagesTutorialSearch]  

1.  Geben `Cache-Control` Sie ein, und drücken Sie `Enter` .  Der Suchbereich listet alle Instanzen auf `Cache-Control` , die in Ressourcen Kopfzeilen oder-Inhalten gefunden werden.  
    
    > ##### Abbildung 19  
    > Suchergebnisse‎‏ für:  `Cache-Control`  
    > ! [Suchergebnisse für Cache-Control] [ImagesTutorialResults]  

1.  Wählen Sie ein Ergebnis aus, um die Ressource anzuzeigen, in der das Ergebnis gefunden wurde.  Wenn Sie die Details der Ressource sehen möchten, wählen Sie ein Ergebnis aus, um direkt dorthin zu wechseln.  Wenn die Abfrage beispielsweise in einer Kopfzeile gefunden wurde, wird die Registerkarte Überschriften geöffnet.   Wenn die Abfrage im Inhalt gefunden wurde, wird die Registerkarte " **Antwort** " geöffnet.  
    
    > ##### Abbildung 20  
    > Auf der Registerkarte "Überschriften" hervorgehobenes Suchergebnis  
    > ! [Ein Suchergebnis ist auf der Registerkarte ' Überschriften ' hervorgehoben] [ImagesTutorialCache]  
    
1.  Schließen Sie den Suchbereich und die Registerkarte Überschriften.  
    
    > ##### Abbildung 21  
    > Die Schaltflächen "Schließen"  
    > ! [Die Schaltflächen zum Schließen] [ImagesTutorialCloseButtons]  
    
## Filtern von Ressourcen   

DevTools bietet zahlreiche Workflows zum Filtern von Ressourcen, die für die jeweilige Aufgabe nicht relevant sind.  

> ##### Abbildung 22  
> Die Symbolleiste "Filter"  
> ! [Die Filtersymbolleiste] [ImagesTutorialFilters]  

Die **Filter** Symbolleiste sollte standardmäßig aktiviert sein.  Wenn nicht,:  

1.  Wählen Sie **Filter** ![ Filter aus ][ImageFilterIcon] , um ihn anzuzeigen.  

### Filtern nach Zeichenfolge, regulärem Ausdruck oder Eigenschaft   

Das Textfeld " **Filter** " unterstützt viele verschiedene Filterarten.  

1.  Geben Sie `png` in das Textfeld **Filter** ein.  Nur die Dateien, die den Text enthalten, `png` werden angezeigt.  In diesem Fall sind die einzigen Dateien, die dem Filter entsprechen, die PNG-Bilder.  
    
    > ##### Abbildung 23  
    > Ein Zeichenfolgenfilter  
    > ! [Ein Zeichenfolgenfilter] [ImagesTutorialPNG]  

1.  Geben Sie `/.*\.[cj]s+$/` ein.  DevTools filtert jede Ressource mit einem Dateinamen, der nicht mit a `j` oder a, `c` gefolgt von 1 oder mehr Zeichen, endet `s` .  
    
    > ##### Abbildung 24  
    > Ein Filter für reguläre Ausdrücke  
    > ! [Ein Filter für reguläre Ausdrücke] [ImagesTutorialRegEx]  
    
1.  Geben Sie `-main.css` ein.  DevTools filtert aus `main.css` .  Wenn eine andere Datei mit dem Muster übereinstimmt, würden Sie ebenfalls herausgefiltert.  
    
    > ##### Abbildung 25  
    > Ein negativer Filter  
    > ! [Ein negativer Filter] [ImagesTutorialNegative]  
    
1.  Geben Sie `domain:cdn.glitch.com` in das Textfeld **Filter** ein.  DevTools filtert jede Ressource mit einer URL ab, die dieser Domäne nicht entspricht.  
    
    > ##### Abbildung 26  
    > Ein Eigenschaften Filter  
    > ! [Ein Eigenschaften Filter] [ImagesTutorialProperty]  

    Die vollständige Liste der filterbaren Eigenschaften finden Sie unter [Filtern von Anforderungen nach Eigenschaften][DevtoolsReferenceProperty] .  
    
    
1.  Deaktivieren Sie das Textfeld " **Filter** " eines beliebigen Texts.  

### Nach Ressourcentyp Filtern   

So konzentrieren Sie sich auf eine bestimmte Art von Datei, beispielsweise Stylesheets:  

1.  Wählen Sie **CSS**aus.  Alle anderen Dateitypen werden herausgefiltert.  
    
    > ##### Abbildung 27  
    > Nur CSS-Dateien anzeigen  
    > ! [Nur CSS-Dateien anzeigen] [ImagesTutorialCSS]  
    
1.  Wenn Sie auch Skripts anzeigen möchten, halten Sie `Control` \ (Windows \) oder `Command` \ (macOS \) gedrückt, und wählen Sie dann **js**aus.  
    
    > ##### Abbildung 28  
    > Nur CSS-und JS-Dateien anzeigen  
    > ! [Nur CSS-und JS-Dateien anzeigen] [ImagesTutorialCSSJS]  
    
1.  Wählen Sie **alle** aus, um die Filter zu entfernen und alle Ressourcen erneut anzuzeigen.  

Weitere Informationen finden Sie unter [Filteranforderungen][DevtoolsNetworkReferenceFilter] für andere Filter Workflows.  

## Anfragen blockieren   

Wie wird eine Seite aussehen und sich Verhalten, wenn einige Seitenressourcen nicht verfügbar sind?  Funktioniert es nicht vollständig, oder ist es immer noch etwas funktionell?  Anfragen blockieren, um Folgendes zu erfahren:  

1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.  
    
    > ##### Abbildung 29  
    > Das Befehlsmenü  
    > ! [Befehlsmenü] [ImagesTutorialCommandMenu]  
    
1.  Geben `block` Sie die Option **Blockierungs Anforderung anzeigen**ein, und drücken Sie `Enter` .  
    
    > ##### Abbildung 30  
    > Anforderungs Blockierung anzeigen  
    > ! [Anzeige der Anforderungs Blockierung] [ImagesTutorialBlock]  

1.  Wählen Sie **Muster** ![ hinzufügen aus ][ImageAddIcon] .  
1.  Geben Sie `main.css` ein.  
    
    > ##### Abbildung 31  
    > Blockieren `main.css`  
    > ! [Blockieren von Main. CSS] [ImagesTutorialAddBlock]  
    
1.  Wählen Sie **Hinzufügen** aus.  
1.  Laden Sie die Seite neu.  Wie erwartet, wird das Design der Seite etwas durcheinander gebracht, da das Haupt-Stylesheet blockiert wurde.  
    
    > [!NOTE]
    > Die `main.css` Zeile im Netzwerkprotokoll.  Der rote Text bedeutet, dass die Ressource blockiert wurde.
    
    > ##### Abbildung 32  
    > `main.css` wurde blockiert  
    > ! [Main. CSS wurde blockiert] [ImagesTutorialBlockedStyles]  

1.  Deaktivieren Sie das Kontrollkästchen **Anforderungs Blockierung aktivieren** .  

## Fazit  

Herzlichen Glückwunsch, Sie haben das Lernprogramm abgeschlossen.  Sie wissen jetzt, wie Sie das Netzwerk Panel im Microsoft Edge-devtools verwenden!






Schauen Sie sich die [Netzwerk Referenz][DevtoolsNetworkReference] an, um weitere devtools-Features im Zusammenhang mit der Überprüfung von Netzwerkaktivitäten zu entdecken.  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-icon.msft.png  
[ImageCloseIcon]: /microsoft-edge/devtools-guide-chromium/media/close-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/screenshots-icon.msft.png  
[ImageSearchIcon]: /microsoft-edge/devtools-guide-chromium/media/search-icon.msft.png  
[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png

[ImagesTutorialDemo]: /microsoft-edge/devtools-guide-chromium/media/network-glitch-inspect-network-activity-demo.msft.png "Abbildung 1: die Demo"  
<!--[ImagesTutorialWindows]: /microsoft-edge/devtools-guide-chromium/media/network-tutorial/windows.msft.png " old Figure 2: The demo in one window and this tutorial in a different window"  -->  
[ImagesTutorialConsole]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Console.msft.png "Abbildung 2: die Konsole"  
[ImagesTutorialDocked]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Console-Bottom.msft.png "Abbildung 3: devtools an den unteren Rand des Fensters angedockt"  
[ImagesTutorialNetwork]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Bottom.msft.png "Abbildung 4: devtools an den unteren Rand des Fensters angedockt"  
[ImagesTutorialLog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network.msft.png "Abbildung 5: das Netzwerkprotokoll"  
[ImagesTutorialRuntime]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-New-Resource.msft.png "Abbildung 6: eine neue Ressource im Netzwerkprotokoll"  
[ImagesTutorialDomain]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Edit-column.msft.png "Abbildung 7: Aktivieren der Spalte" Domäne "  
[ImagesTutorialThrottling]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Throttling.msft.png "Abbildung 8: Aktivieren der Drosselung"  
[ImagesTutorialSlow3G]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Throttling-Slow-3G.msft.png "Abbildung 9: Auswählen von" Slow 3G "  
[ImagesTutorialHardReload]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Empty-Cache-and-Hard-Reset.msft.png "Abbildung 10: leerer Cache und Hard Reload"  
[ImagesTutorialAllScreenshots]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Screenshots.msft.png "Abbildung 11: Screenshots der Seite laden"  
[ImagesTutorialFirstScreenshot]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Screenshots-First.msft.png "Abbildung 12: die Netzwerkaktivität, die während des ersten Screenshots stattgefunden hat"  
[ImagesTutorialHeaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Headers.msft.png "Abbildung 13: die Registerkarte" Überschriften "  
[ImagesTutorialPreview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Preview.msft.png "Abbildung 14: die Registerkarte" Vorschau "  
[ImagesTutorialResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Response.msft.png "Abbildung 15: die Registerkarte" Antwort "  
[ImagesTutorialTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Timing.msft.png "Abbildung 16: die Registerkarte" Anzeigedauer "  
[ImagesTutorialCloseTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Close-Tabs.msft.png "Abbildung 17: die Schaltfläche" Schließen "  
[ImagesTutorialSearch]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Empty.msft.png "Abbildung 18: der Suchbereich"  
[ImagesTutorialResults]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Cache-Control.msft.png "Abbildung 19: Suchergebnisse für Cache-Control"  
[ImagesTutorialCache]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Cache-Control-Headers-Response-Headers.msft.png "Abbildung 20: hervorgehobenes Suchergebnis auf der Registerkarte" Überschriften "  
[ImagesTutorialCloseButtons]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-close.msft.png "Abbildung 21: die Schaltflächen" Schließen "  
[ImagesTutorialFilters]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Empty.msft.png "Abbildung 22: die Symbolleiste" Filter "  
[ImagesTutorialPNG]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-PNG.msft.png "Abbildung 23: ein Zeichenfolgenfilter"  
[ImagesTutorialRegEx]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Regex.msft.png "Abbildung 24: ein Filter für reguläre Ausdrücke"  
[ImagesTutorialNegative]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-negative-Statement.msft.png "Abbildung 25: ein negativer Filter"  
[ImagesTutorialProperty]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Property-Value.msft.png "Abbildung 26: ein Eigenschaften Filter"  
[ImagesTutorialCSS]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-File-Type-CSS.msft.png "Abbildung 27: nur CSS-Dateien anzeigen"  
[ImagesTutorialCSSJS]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-File-Type-CSS-js.msft.png "Abbildung 28: nur CSS-und JS-Dateien anzeigen"  
[ImagesTutorialCommandMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Empty.msft.png "Abbildung 29: das Befehlsmenü"  
[ImagesTutorialBlock]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Block.msft.png "Abbildung 30: Anzeigen der Anforderungs Blockierung"  
[ImagesTutorialAddBlock]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Block-Add-Pattern.msft.png "Abbildung 31: Blockieren von Main. CSS"  
[ImagesTutorialBlockedStyles]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Block-Main-CSS.msft.png "Abbildung 32: Main. CSS wurde blockiert"  

<!-- links -->  


<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Ändern der Platzierung von Microsoft Edge devtools (abdocken, docken an den unteren Rand, docken nach links)"  
[DevtoolsNetworkReference]: /microsoft-edge/devtools-guide-chromium/network/reference "Netzwerkanalyse Referenz"
[DevtoolsNetworkReferenceFilter]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests "Filter Anforderungen – Netzwerkanalyse Referenz"  
[DevtoolsReferenceHideOverview]: /microsoft-edge/devtools-guide-chromium/network/reference#hide-the-overview-pane "Ausblenden des Übersichtsbereichs – Netzwerkanalyse Referenz"
[DevtoolsReferenceProperty]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtern von Anforderungen nach Eigenschaften-Netzwerkanalyse Referenz"
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Öffnen von Microsoft Edge devtools"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Überprüfen der Netzwerk Aktivitäts Demo"  

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

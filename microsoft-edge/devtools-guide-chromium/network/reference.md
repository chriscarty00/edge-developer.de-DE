---
title: Netzwerkanalyse Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: ec8969fbf7b54512f00120ac4a253b952c55768f
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844019"
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

# Netzwerkanalyse Referenz  

Entdecken Sie neue Möglichkeiten zur Analyse, wie Ihre Seite in dieser umfassenden Referenz der Microsoft Edge devtools-Netzwerkanalyse Features geladen werden kann.  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## Aufzeichnen von Netzwerkanforderungen  

Standardmäßig zeichnet devtools alle Netzwerkanforderungen im Netzwerk Panel auf, solange devtools geöffnet ist.  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-panel.msft.png":::
   Abbildung 1: **Netzwerk** Panel  
:::image-end:::  

### Beenden der Aufzeichnung von Netzwerkanforderungen  

Führen Sie die folgenden Schritte aus, um die Aufzeichnung von Anforderungen zu beenden.  

1.  Wählen **Stop recording network log** Sie ![ ][ImageRecordOnIcon] auf der Registerkarte **Netzwerk** die Option Aufzeichnung des Netzwerkprotokolls beenden Aufzeichnung beenden aus.  Es wird grau, um anzugeben, dass devtools keine Anforderungen mehr aufzeichnet.  
1.  Drücken Sie `Control` + `E` \ (Windows \) oder `Command` + `E` \ (macOS \), während sich der Fokus des **Netzwerk** Panels befindet.  

### Löschen von Anforderungen  

Wählen **Sie** ![ ][ImageClearIcon] im Netzwerk Panel löschen aus, um alle Anforderungen aus der Tabelle Anforderungen zu löschen.  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Die Schaltfläche Löschen" lightbox="../media/network-network-clear-button.msft.png":::
   Abbildung 2: die Schaltfläche " **Löschen** "  
:::image-end:::  

### Speichern von Anforderungen über Seitenlasten hinweg  

Aktivieren Sie das Kontrollkästchen **Protokoll beibehalten** auf der Registerkarte Netzwerk, um Anforderungen zwischen den Seitenlasten zu speichern.  DevTools speichert alle Anforderungen, bis Sie **Protokoll beibehalten**deaktivieren.  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Kontrollkästchen Protokoll beibehalten" lightbox="../media/network-network-preserve-log.msft.png":::
   Abbildung 3: Kontrollkästchen " **Protokoll beibehalten** "  
:::image-end:::  

### Aufzeichnen von Screenshots beim Laden der Seite  

Erfassen Sie Screenshots, um zu analysieren, was die Benutzer sehen, während Sie auf Ihre Seite warten, um Sie zu laden.  

Wenn Sie Screenshots aktivieren möchten, wählen Sie **Netzwerkeinstellungen** und dann auf der Registerkarte **Netzwerk** das Kontrollkästchen **Screenshots aufzeichnen** aus.  

Aktualisieren Sie die Seite, während sich das **Netzwerk** Panel im Fokus befindet, um Screenshots zu erfassen.  

Nachdem Sie einen Screenshot aufgezeichnet haben, interagieren Sie mit ihm auf die folgende Weise.  

*   Zeigen Sie mit der Maus auf einen Screenshot, um den Punkt anzuzeigen, an dem dieser Screenshot aufgenommen wurde.  Im Bereich " **Übersicht** " wird eine gelbe Zeile angezeigt.  
*   Wählen Sie die Miniaturansicht eines Bildschirms aus, um alle Anforderungen zu filtern, die nach dem Erfassen des Screenshots aufgetreten sind.  
*   Doppelklicken Sie auf eine Miniaturansicht, um Sie zu vergrößern.  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Zeigen auf einen Screenshot" lightbox="../media/network-network-screenshot-hover.msft.png":::
   Abbildung 4: Bewegen des Mauszeigers über einen Screenshot  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Selecting Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Old Figure 5:  Selecting Replay XHR  
:::image-end:::  
-->  

## Ändern des Ladeverhaltens  

### Emulieren eines erstmaligen Besuchers durch Deaktivieren des Browsercaches  

Aktivieren Sie das Kontrollkästchen **Cache deaktivieren** , um zu emulieren, wie ein Erstbenutzer Ihre Website erlebt.  DevTools deaktiviert den Browsercache.  Dadurch wird die Benutzererfahrung des ersten Benutzers genauer emuliert, da Anforderungen im Browsercache bei wiederholten Besuchen bereitgestellt werden.  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Kontrollkästchen Cache deaktivieren" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   Abbildung 5: Kontrollkästchen " **Cache deaktivieren** "  
:::image-end:::  

#### Deaktivieren des Browser-Caches aus der Schublade "Netzwerkbedingungen"  

Wenn Sie den Cache während der Arbeit in anderen devtools-Panels deaktivieren möchten, verwenden Sie die Schublade Netzwerkbedingungen.  

1.  Öffnen Sie die Schublade **Netzwerkbedingungen** .  
1.  Aktivieren oder deaktivieren Sie das Kontrollkästchen **Cache deaktivieren** .  

<!--todo: add network condition section when available -->  

### Manuelles Löschen des Browsercaches  

Wenn Sie den Browser-Cache jederzeit manuell löschen möchten, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browsercache löschen**aus.  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Auswählen des Browser Cache löschen" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   Abbildung 6: Auswählen des **Browser Cache löschen**  
:::image-end:::  

### Offline emulieren  

Eine neue Klasse von Web-Apps mit dem Namen " [Progressive Web Apps][DevtoolsProgressiveWebApps]" funktioniert mit Hilfe von **Servicemitarbeitern**offline.  Möglicherweise ist es hilfreich, ein Gerät, das keine Datenverbindung aufweist, schnell zu simulieren, wenn Sie diese Art von App erstellen.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Wählen Sie das Dropdownmenü **Online** aus, suchen Sie unter **Voreinstellungen**, und wählen Sie **Offline** aus, um eine vollständig Offlinenetzwerk Umgebung zu simulieren.  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Das Offline-Dropdownmenü" lightbox="../media/network-network-offline-dropdown.msft.png":::
   Abbildung 7: **Offline** -Dropdownmenü  
:::image-end:::  

### Emulieren langsamer Netzwerkverbindungen  

Emulieren Sie langsames 3G, fast 3G und andere Verbindungsgeschwindigkeiten über das **Online-Dropdown-** Menü.  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Dropdownmenü Drosselung" lightbox="../media/network-network-throttling-menu.msft.png":::
   Abbildung 8: das Dropdownmenü " **Drosselung** "  
:::image-end:::  

Sie können aus einer Vielzahl von Voreinstellungen auswählen, wie etwa langsames 3G oder fast 3G.  Sie können auch eigene benutzerdefinierte Voreinstellungen hinzufügen, indem Sie das Menü Drosselung öffnen und **benutzerdefiniertes**  >  **Add**auswählen.  

DevTools zeigt ein Warnungssymbol neben der Registerkarte " **Netzwerk** " an, um Sie daran zu erinnern, dass die Drosselung aktiviert ist.  

#### Emulieren von langsamen Netzwerkverbindungen über die Netzwerkbedingungen Schublade  

Wenn Sie die Netzwerkverbindung während der Arbeit in anderen devtools-Panels Drosseln möchten, verwenden Sie den Netzwerkbedingungen-Einzug.  

1.  Öffnen Sie die Schublade **Netzwerkbedingungen** .  
1.  Wählen Sie die gewünschte Verbindungsgeschwindigkeit im Menü " **Drosselung** " aus.  

<!--todo: add network condition section when available -->  

### Manuelles Löschen von Browser-Cookies  

Wenn Sie Browser-Cookies jederzeit manuell löschen möchten, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browser-Cookies löschen**aus.  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Auswählen von Browser-Cookies löschen" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   Abbildung 9: Auswählen von **Browser-Cookies löschen**  
:::image-end:::  

### Überschreiben des Benutzer-Agents  

So überschreiben Sie den Benutzer-Agent manuell:  

1.  Öffnen Sie die Schublade **Netzwerkbedingungen** .  
1.  Deaktivieren **Sie SELECT automatisch**.  
1.  Wählen Sie eine Option für den Benutzer-Agent aus dem Menü aus, oder geben Sie eine benutzerdefinierte Option in das Textfeld ein.  

<!--todo: add network condition section when available -->  

## Filter Anforderungen  

### Filtern von Anforderungen nach Eigenschaften  

Verwenden Sie das Textfeld **Filtern** , um Anforderungen nach Eigenschaften wie der Domäne oder der Größe der Anforderung zu filtern.  

Wenn das Textfeld nicht angezeigt wird, ist der Bereich Filter wahrscheinlich ausgeblendet.  
Weitere Informationen finden Sie unter [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Das Textfeld Filter" lightbox="../media/network-network-filters-textbox.msft.png":::
   Abbildung 10: das Textfeld " **Filter** "  
:::image-end:::  

Sie können mehrere Eigenschaften gleichzeitig verwenden, indem Sie jede Eigenschaft mit einem Leerzeichen voneinander trennen.  Zeigt beispielsweise `mime-type:image/png larger-than:1K` alle PNGs an, die größer als ein Kilobyte sind.  Diese Filter mit mehreren Eigenschaften sind äquivalent zu `AND` Vorgängen.  `OR` Vorgänge werden zurzeit nicht unterstützt.  

Die vollständige Liste der unterstützten Eigenschaften.  

| Eigenschaft | Details |  
|:--- | :--- |  
| `domain` | Zeigt nur Ressourcen aus der angegebenen Domäne an.  Sie können ein Platzhalterzeichen \ ( `*` \) verwenden, um mehrere Domänen einzubeziehen.  Zeigt beispielsweise `*.com` Ressourcen aus allen Domänennamen an, die in endet `.com` .  DevTools füllt das Dropdownmenü AutoVervollständigen mit allen Domänen auf, die es gefunden hat. |  
| `has-response-header` | Anzeigen der Ressourcen, die den angegebenen HTTP-Antwortheader enthalten  DevTools füllt die Dropdownliste AutoVervollständigen mit allen Antwortheadern auf, die Sie gefunden hat. |  
| `is` | Verwendet `is:running` , um `WebSocket` Ressourcen zu finden. |  
| `larger-than` | Zeigen Sie Ressourcen an, die größer als die angegebene Größe in Bytes sind.  Das Festlegen eines Werts von entspricht dem `1000` Festlegen eines Werts von `1k` . |  
| `method` | Zeigen Sie Ressourcen an, die über einen angegebenen http-Methodentyp abgerufen wurden.  DevTools füllt die Dropdownliste mit allen HTTP-Methoden auf, die Sie gefunden hat. |  
| `mime-type` | Anzeigen von Ressourcen eines angegebenen MIME-Typs  DevTools füllt die Dropdownliste mit allen MIME-Typen auf, die Sie gefunden hat. |  
| `mixed-content` | Alle gemischten Inhalts Ressourcen anzeigen \ ( `mixed-content:all` \) oder nur diejenigen, die aktuell angezeigt werden \ ( `mixed-content:displayed` \). |  
| `scheme` | Zeigt Ressourcen an, die über ungeschützten http \ ( `scheme:http` \) oder geschütztes HTTPS \ ( `scheme:https` \) abgerufen wurden. |  
| `set-cookie-domain` | Zeigen Sie die Ressourcen mit einer `Set-Cookie` Kopfzeile mit einem `Domain` Attribut an, das dem angegebenen Wert entspricht.  DevTools füllt das AutoVervollständigen mit allen Cookie-Domänen auf, die es gefunden hat. |  
| `set-cookie-name` | Zeigen Sie die Ressourcen mit einer `Set-Cookie` Kopfzeile mit einem Namen an, der dem angegebenen Wert entspricht.  DevTools füllt das AutoVervollständigen mit allen Cookie-Namen auf, die es gefunden hat. |  
| `set-cookie-value` | Zeigen Sie die Ressourcen mit einer `Set-Cookie` Kopfzeile mit einem Wert an, der dem angegebenen Wert entspricht.  DevTools füllt das AutoVervollständigen mit allen Cookie-Werten auf, die es gefunden hat. |  
| `status-code` | Nur die Ressourcen anzeigen, für die der HTTP-Statuscode mit dem angegebenen Code übereinstimmt.  DevTools füllt das Dropdownmenü AutoVervollständigen mit allen Statuscodes auf, die es gefunden hat. |  

### Filtern von Anforderungen nach Typ  

Wenn Sie Anforderungen nach Anforderungsfiltern möchten, wählen Sie die Schaltflächen **XMLHttpRequest**, **js**, **CSS**, **IMG**, **Media**, **Font**, **doc**, **WS** \ (WebSocket \), **Manifest**oder **andere** \ (alle anderen Typen, die hier nicht aufgelistet sind) im Netzwerk Panel aus.  

Wenn diese Schaltflächen nicht angezeigt werden, ist der Bereich Filter wahrscheinlich ausgeblendet.  
Weitere Informationen finden Sie unter [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).  

Wenn Sie mehrere Typfilter gleichzeitig aktivieren möchten, halten `Control` Sie \ (Windows \) oder `Command` \ (macOS \) gedrückt, und wählen Sie dann aus.  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Verwenden des Typs Filter zum Anzeigen von JS-, CSS-und Dokument Ressourcen" lightbox="../media/network-network-type-filters.msft.png":::
   Abbildung 11: Verwenden der Typfilter zum Anzeigen von JS-, CSS-und Dokument Ressourcen  
:::image-end:::  

### Filtern von Anforderungen nach Zeit  

Wählen Sie aus, und ziehen Sie im Übersichtsbereich nach links oder rechts, um nur Anforderungen anzuzeigen, die während dieses Zeitrahmens aktiv waren.  Der Filter ist inklusive.  Jede Anforderung, die während der hervorgehobenen Zeit aktiv war, wird angezeigt.  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Herausfiltern von Anforderungen, die um 300 m inaktiv waren" lightbox="../media/network-network-overview-filter.msft.png":::
   Abbildung 12: Filtern von Anforderungen, die um 300 m inaktiv waren  
:::image-end:::  

### Ausblenden von Daten-URLs  

[Daten-URLs][MDNHTTPDataURIs] sind kleine Dateien, die in andere Dokumente eingebettet sind.  Jede Anforderung, die Sie in der Tabelle Anforderungen sehen, die mit beginnt, `data:` ist eine Daten-URL.  

Aktivieren Sie das Kontrollkästchen **Daten-URLs ausblenden** , um die Anforderungen auszublenden.  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Das Kontrollkästchen Daten-URLs ausblenden" lightbox="../media/network-network-hide-data-urls.msft.png":::
   Abbildung 13: Kontrollkästchen " **Daten-URLs ausblenden** "  
:::image-end:::  

## Sortieren von Anforderungen  

Standardmäßig werden die Anforderungen in der Tabelle Anforderungen nach Initiierungs Zeit sortiert, aber Sie können die Tabelle mit anderen Kriterien sortieren.  

### Nach Spalte sortieren  

Wählen Sie die Kopfzeile einer beliebigen Spalte in den Anforderungen aus, um Anforderungen nach dieser Spalte zu sortieren.  

### Nach Aktivitätsphase sortieren  

Wenn Sie ändern möchten, wie der Wasserfall Anforderungen sortiert, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), zeigen Sie mit der Maus auf **Wasserfall**, und wählen Sie eine der folgenden Optionen aus.  

*   **Startzeit**.  Die erste Anforderung, die initiiert wurde, ist oben.  
*   **Antwortzeit**.  Die erste Anforderung, die den Download begonnen hat, ist ganz oben.  
*   **Endzeit**.  Die erste abgeschlossene Anforderung ist oben.  
*   **Gesamtdauer**.  Die Anforderung mit der kürzesten Verbindungseinrichtung und Anforderung/Antwort ist oben.  
*   **Latenz**.  Die Anforderung, die die kürzeste Zeit für eine Antwort gewartet hat, ist oben.  

Bei diesen Beschreibungen wird davon ausgegangen, dass die jeweilige Option von kürzester bis längster Position bewertet wird.  Wenn Sie die Kopfzeile der Spalte **Wasserfall** auswählen, wird die Reihenfolge umgekehrt.  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Sortieren des Wasserfalls nach Gesamtdauer" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   Abbildung 14: Sortieren des Wasserfalls nach Gesamtdauer \ (der leichtere Teil der einzelnen Balken ist die Zeit, die gewartet wird, und der dunklere Teil ist die Zeit, die zum Herunterladen von Bytes verwendet wird \)  
:::image-end:::  

## Analysieren von Anforderungen  

Solange devtools geöffnet ist, werden alle Anforderungen im Netzwerk Panel protokolliert.  
Verwenden Sie das Netzwerk Panel, um Anforderungen zu analysieren.  

### Anzeigen eines Protokolls der Anforderungen  

Verwenden Sie die Tabelle "Anforderungen", um ein Protokoll aller Anforderungen anzuzeigen, die während der devtools geöffnet wurden.  Wenn Sie über Anforderungen auswählen oder darauf zeigen, werden weitere Informationen zu den einzelnen Elementen eingeblendet.  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Die Tabelle Anforderungen" lightbox="../media/network-network-requests-table.msft.png":::
   Abbildung 15: die Tabelle "Anforderungen"  
:::image-end:::  

In der Tabelle Anforderungen werden standardmäßig die folgenden Spalten angezeigt.  

*   **Name**  Der Dateiname von oder ein Bezeichner für die Ressource.  
*   **Status**aus.  Der HTTP-Statuscode.  
*   **Typ**.  Der MIME-Typ der angeforderten Ressource.  
*   **Initiator**.  Die folgenden Objekte oder Prozesse initiieren Anforderungen:  
    *   **Parser**aus.  Der HTML-Parser für Microsoft Edge.  
    *   **Umleiten**.  Eine HTTP-Umleitung.  
    *   **Skript**aus.  Eine JavaScript-Funktion.  
    *   **Andere**.  Einige andere Prozesse oder Aktionen, wie das Navigieren zu einer Seite über einen Link oder das Eingeben einer URL in die Adressleiste.  
*   **Größe**aus.  Die kombinierte Größe der Antwortheader sowie des Antworttexts, wie vom Server bereitgestellt.  
*   **Zeit**.  Die Gesamtdauer vom Anfang der Anforderung bis zum Empfang des letzten Bytes in der Antwort.  
*   [**Wasserfall**](#view-the-timing-of-requests-in-relation-to-one-another).  Eine visuelle Gliederung der Aktivität für jede Anforderung.  

#### Hinzufügen oder Entfernen von Spalten  

Zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie eine Option aus, um sie auszublenden oder anzuzeigen.  Die aktuell angezeigten Optionen verfügen über Kontrollkästchen neben den einzelnen Elementen.  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Hinzufügen einer Spalte zur Tabelle Anforderungen" lightbox="../media/network-network-requests-add-column.msft.png":::
   Abbildung 16: Hinzufügen einer Spalte zur Tabelle "Anforderungen"  
:::image-end:::  

#### Hinzufügen benutzerdefinierter Spalten  

Wenn Sie der Tabelle Anforderungen eine benutzerdefinierte Spalte hinzufügen möchten, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Antwortheader**  >  **Verwalten von Kopfzeilen Spalten**aus.  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Hinzufügen einer benutzerdefinierten Spalte zur Tabelle Anforderungen" lightbox="../media/network-network-requests-add-custom.msft.png":::
   Abbildung 17: Hinzufügen einer benutzerdefinierten Spalte zur Tabelle "Anforderungen"  
:::image-end:::  

### Anzeigen der Anzeigedauer von Anforderungen im Verhältnis zueinander  

Verwenden Sie den Wasserfall, um die Anzeigedauer von Anforderungen im Verhältnis zueinander anzuzeigen.  
Standardmäßig wird der Wasserfall nach dem Anfangszeitpunkt der Anforderungen organisiert.  
Anfragen, die weiter Links sind, wurden früher als die weiter rechts eingegangenen Anforderungen gestartet.  

Sehen Sie sich die verschiedenen Arten an, wie Sie den Wasserfall sortieren können, [indem Sie nach Aktivitätsphase sortieren](#sort-by-activity-phase) .  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Spalte Wasserfall im Bereich Anforderungen" lightbox="../media/network-network-requests-waterfall.msft.png":::
   Abbildung 18: Spalte "Wasserfall" im Bereich " **Anforderungen** "  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
   Old Figure 20:  The **Frames** tab  
:::image-end:::  
-->

<!--The table contains three columns:  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to their type:  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### Anzeigen einer Vorschau eines Antworttexts  

So zeigen Sie eine Vorschau eines Antworttexts an:  

1.  Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie die Registerkarte **Vorschau** aus.  

Diese Registerkarte ist hauptsächlich für die Anzeige von Bildern hilfreich.  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Registerkarte Vorschau" lightbox="../media/network-network-resources-preview.msft.png":::
   Abbildung 19: Registerkarte " **Vorschau** "  
:::image-end:::  

### Anzeigen eines Antworttexts  

So zeigen Sie den Antworttext auf eine Anforderung an:  

1.  Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie die Registerkarte **Antwort** aus.  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Die Registerkarte Antwort" lightbox="../media/network-network-resources-response.msft.png":::
   Abbildung 20: die Registerkarte " **Antwort** "  
:::image-end:::  

### Anzeigen von HTTP-Headern  

So zeigen Sie HTTP-Header Daten zu einer Anforderung an:  

1.  Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie die Registerkarte über **Schriften** aus.  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Die Registerkarte Überschriften" lightbox="../media/network-resources-headers.msft.png":::
   Abbildung 21: Registerkarte "über **Schriften** "  
:::image-end:::  

#### Anzeigen der HTTP-Header Quelle  

Standardmäßig werden auf der Registerkarte Kopfzeilennamen in alphabetischer Reihenfolge angezeigt.  So zeigen Sie die HTTP-Headernamen in der Reihenfolge an, in der Sie empfangen wurden:  

1.  Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.  Siehe [Anzeigen von HTTP-Kopfzeilen](#view-http-headers).  
1.  Wählen Sie **Quelle anzeigen**neben dem Abschnitt **Anforderungs Kopfzeile** oder **Antwort Kopf** aus.  

### Anzeigen von Abfragezeichenfolgenparametern  

So zeigen Sie die Abfragezeichenfolgenparameter einer URL in einem Menschen lesbaren Format an:  

1.  Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.  Siehe [Anzeigen von HTTP-Kopfzeilen](#view-http-headers).  
1.  Wechseln Sie zum Abschnitt **Abfragezeichenfolgenparameter** .  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Der Abfragezeichenfolgenparameter Abschnitt" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   Abbildung 22: Abschnitt " **Abfragezeichenfolgen-Parameter** "  
:::image-end:::  

#### Anzeigen der Parameterquelle für Abfragezeichenfolgen  

So zeigen Sie die Abfragezeichenfolgenparameter Quelle einer Anforderung an:  

1.  Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.  Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#view-query-string-parameters).  
1.  Wählen Sie **Quelltext anzeigen**aus.  

#### Anzeigen von URL-codierten Abfragezeichenfolgenparametern  

So zeigen Sie Abfragezeichenfolgenparameter in einem menschlich lesbaren Format an, jedoch mit erhaltenen Codierungen:  

1.  Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.  Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#view-query-string-parameters).  
1.  Wählen Sie **URL-codiert anzeigen**aus.  

### Cookies anzeigen  

So zeigen Sie die im HTTP-Header einer Anforderung gesendeten Cookies an:  

1.  Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie die Registerkarte **Cookies** aus.  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Die Registerkarte Cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   Abbildung 23: die Registerkarte "Cookies"  
:::image-end:::  

### Anzeigen der Zeit Plan Aufteilung einer Anforderung  

So zeigen Sie die Anzeigedauer einer Anforderung an:  

1.  Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie die Registerkarte **Anzeige** Dauer aus.  

Eine schnellere Möglichkeit für den Zugriff auf diese Daten finden Sie unter [Anzeigen einer Zeit Plan Vorschau](#preview-a-timing-breakdown) .  

Weitere Informationen zu den einzelnen Phasen, die auf der Registerkarte "Anzeigedauer" angezeigt werden, finden Sie unter [erläuterte Phasen der zeitlichen Verteilung](#timing-breakdown-phases-explained) .  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Registerkarte Anzeigedauer" lightbox="../media/network-network-resources-timing.msft.png":::
   Abbildung 24: Registerkarte " **Anzeige** Dauer"  
:::image-end:::  

Weitere Informationen zu den einzelnen Phasen.  

Eine weitere Möglichkeit für den Zugriff auf diese Ansicht finden Sie unter [Aufschlüsselung der Anzeige](#view-the-timing-breakdown-of-a-request) Dauer.  

#### Anzeigen einer Vorschau einer Anzeigedauer  

Wenn Sie eine Vorschau der Anzeigedauer einer Anforderung anzeigen möchten, zeigen Sie in der Spalte **Wasserfall** in der Tabelle Anforderungen auf den Eintrag für die Anforderung.  

Weitere Informationen finden Sie unter [Anzeigen der zeitlichen Aufschlüsselung einer Anforderung](#view-the-timing-breakdown-of-a-request) für eine Möglichkeit, auf diese Daten zuzugreifen, für die kein Hovern erforderlich ist.  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> Vorschau der Anzeigedauer einer Anforderung" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   Abbildung 25: Anzeigen einer Vorschau der Anzeigedauer einer Anforderung  
:::image-end:::  

#### Erläuterte Phasen Aufgliederungs Phasen  

Weitere Informationen zu den einzelnen Phasen, die auf der Registerkarte **Anzeige** Dauer angezeigt werden.  

*   **Warteschlange**.  Der Browser Warteschlangenanforderungen, wenn:  
    *   Es gibt Anforderungen mit höherer Priorität.  
    *   Für diesen Ursprung sind bereits sechs TCP-Verbindungen geöffnet, was die Grenze ist.  Gilt nur für HTTP/1.0 und HTTP/1.1.  
    *   Der Browser reserviert kurzzeitig Speicherplatz im Datenträgercache.  
*   Im **Stall**.  Die Anforderung konnte aus einem der in der **Warteschlange**beschriebenen Gründe blockiert werden.  
*   **DNS-Lookup**.  Der Browser löst die IP-Adresse für die Anforderung auf.  
*   **Anfängliche Verbindung**.  Der Browser stellt eine Verbindung her, einschließlich TCP-Handshakes, TCP-Wiederholungen und Aushandeln eines SSL.
*   **Proxy Verhandlung**.  Der Browser verhandelt die Anforderung mit einem [Proxy Server][WikiProxyServer].  
*   **Anfrage gesendet**.  Die Anfrage wird gesendet.  
*   **ServiceWorker-Vorbereitung**.  Der Browser startet den Dienstmitarbeiter.  
*   **Anforderung an ServiceWorker**.  Die Anforderung wird an den Dienstmitarbeiter gesendet.  
*   **Waiting \ (TTFB \)**.  Der Browser wartet auf das erste Byte einer Antwort.  TTFB steht für Time to First Byte.  Diese Anzeigedauer umfasst eine Roundtrip-Wartezeit und den Zeitpunkt, zu dem der Server die Antwort vorbereitet hat.  
*   **Inhalt herunterladen**.  Der Browser empfängt die Antwort.  
*   **Push wird empfangen**.  Der Browser empfängt Daten für diese Antwort über http/2 Server Push.  
*   **Lese Push**.  Der Browser liest die zuvor empfangenen lokalen Daten.  

### Anzeigen von Initiatoren und Abhängigkeiten  

Wenn Sie die Initiatoren und Abhängigkeiten einer Anforderung anzeigen möchten, halten Sie `Shift` die Anforderung in der Tabelle Anforderungen gedrückt, und zeigen Sie darauf.  DevTools Farben: Initiatoren werden in grün angezeigt, und Abhängigkeiten werden in rot angezeigt.  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   Abbildung 26: Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung  
:::image-end:::  

Wenn die Anforderungstabelle chronologisch geordnet ist, ist die erste grüne Anforderung oberhalb des Cursors der Initiator der Abhängigkeit.  Wenn darüber eine weitere grüne Anforderung angezeigt wird, ist diese höhere Anforderung der Initiator des Initiators.  Und so weiter.  

### Laden Ereignisse anzeigen  

DevTools zeigt die Anzeigedauer der `DOMContentLoaded` `load` Ereignisse und Ereignisse an mehreren Stellen im Netzwerk Panel an.  Das `DOMContentLoaded` Ereignis ist blau gefärbt, und das `load` Ereignis ist rot.  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Die Speicherorte der DOMContentLoaded-und Load-Ereignisse im Netzwerk Panel" lightbox="../media/network-network-requests-load-events.msft.png":::
   Abbildung 27: die Speicherorte der `DOMContentLoaded` und- `load` Ereignisse im Netzwerk Panel  
:::image-end:::  

### Anzeigen der Gesamtzahl der Anforderungen  

Die Gesamtzahl der Anforderungen wird im Bereich "Zusammenfassung" unten im Netzwerkbereich aufgelistet.  

> [!CAUTION]
> Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.  Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden diese Anforderungen nicht gezählt.  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Die Gesamtzahl der Anforderungen seit dem Öffnen von devtools" lightbox="../media/network-network-total-requests.msft.png":::
   Abbildung 28: die Gesamtzahl der Anforderungen seit dem Öffnen von devtools  
:::image-end:::  

### Anzeigen der Gesamtgröße des Downloads  

Die Gesamtgröße der Downloadanforderungen wird im Bereich "Zusammenfassung" am unteren Rand des Netzwerkbereichs angezeigt.  

> [!CAUTION]
> Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.  Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden die vorherigen Anforderungen nicht gezählt.  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Die Gesamtgröße der Downloads von Anforderungen" lightbox="../media/network-network-total-download-size.msft.png":::
   Abbildung 29: die Gesamtgröße der Downloads von Anforderungen  
:::image-end:::  

Weitere Informationen finden Sie unter [Anzeigen der unkomprimierten Größe einer Ressource](#view-the-uncompressed-size-of-a-resource) , um zu sehen, wie groß die Ressourcen sind, nachdem der Browser die einzelnen Elemente dekomprimiert hat.  

### Anzeigen der Stapelüberwachung, die eine Anforderung verursacht hat  

Nachdem eine JavaScript-Anweisung eine Ressource angefordert hat, zeigen Sie mit der Maus auf die Spalte **Initiator** , um die Stapelüberwachung anzuzeigen, die zur Anforderung führt.  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Die Stapelüberwachung, die zu einer Ressourcenanforderung führt" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   Abbildung 30: die Stapelüberwachung, die zu einer Ressourcenanforderung führt  
:::image-end:::  

### Anzeigen der unkomprimierten Größe einer Ressource  

Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , und schauen Sie sich den niedrigsten Wert der Spalte **Größe** an.  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Beispiel für nicht komprimierte Ressourcen" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   Abbildung 31: ein Beispiel für nicht komprimierte Ressourcen \ (die komprimierte Größe der `jquery-3.3.1.min.js` Datei, die über das Netzwerk gesendet wurde `29.9 KB` , während die unkomprimierte Größe `84.9 KB` \) war  
:::image-end:::  

## Exportieren von Anforderungsdaten  

### Speichern aller Netzwerkanforderungen in einer har-Datei  

Führen Sie die folgenden Schritte aus, um alle Netzwerkanforderungen in einer har-Datei zu speichern.  

1.  Zeigen Sie auf jede Anforderung in der Tabelle Anforderungen, und öffnen Sie das Kontextmenü \ (mit der rechten Maustaste auf \).  
1.  Wählen Sie **als har mit Inhalt speichern**aus.  DevTools speichert alle Anforderungen, die seit dem Öffnen von devtools in der har-Datei aufgetreten sind.  Es gibt keine Möglichkeit, Anforderungen zu filtern oder nur eine einzige Anforderung zu speichern.  

Nachdem Sie eine har-Datei gespeichert haben, können Sie Sie für die Analyse wieder in devtools importieren.  Ziehen Sie die har-Datei einfach per Drag & Drop in die Tabelle "Anforderungen".  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Auswählen von als har mit Inhalt speichern" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   Abbildung 32: auswählen **von "als har mit Inhalt speichern** "  
:::image-end:::  

### Kopieren einer oder mehrerer Anforderungen in die Zwischenablage  

Zeigen Sie unter der Spalte **Name** der Tabelle Anforderungen auf eine Anforderung, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), zeigen Sie auf **Kopieren**, und wählen Sie eine der folgenden Optionen aus.  

*   **Link Adresse kopieren**  Kopieren Sie die URL der Anforderung in die Zwischenablage.  
*   **Antwort kopieren**  Kopieren Sie den Antworttext in die Zwischenablage.  
*   **Als FETCH kopieren**  
*   **Als curl kopieren**  Kopieren Sie die Anforderung als curl-Befehl.  
*   **Kopieren Sie alle als FETCH**.  
*   **Kopieren Sie alle als curl**.  Kopieren Sie alle Anforderungen als eine Kette von curl-Befehlen.  
*   **Kopieren Sie alle als har**.  Kopieren Sie alle Anforderungen als har-Daten.  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Auswählen von Antwort kopieren" lightbox="../media/network-network-requests-copy-response.msft.png":::
   Abbildung 33: Auswählen von " **Antwort kopieren** "  
:::image-end:::  

## Ändern des Layouts des Netzwerk Panels  

Sie können Abschnitte der Netzwerk Panel-UI erweitern oder reduzieren, um wichtige Informationen zu konzentrieren.  

### Ausblenden des Bereichs "Filter"  

Standardmäßig zeigt devtools den **Bereich "Filter"** an.  
Wählen Sie **Filter** ![ Filter aus ][ImageFilterIcon] , um sie auszublenden.  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Schaltfläche Filter ausblenden" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   Abbildung 34: die Schaltfläche "Filter ausblenden"  
:::image-end:::  

### Verwenden von umfangreichen Anforderungs Zeilen  

Verwenden Sie große Zeilen, wenn in Ihrer Netzwerk Anforderungstabelle mehr Leerzeichen verwendet werden sollen.  Einige Spalten liefern auch ein wenig mehr Informationen, wenn Sie große Zeilen verwenden.  Der untere Wert der Spalte **size** entspricht beispielsweise der unkomprimierten Größe einer Anforderung.  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Ein Beispiel für große Anforderungs Zeilen im Bereich Anforderungen" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   Abbildung 35: ein Beispiel für große Anforderungs Zeilen im Bereich " **Anforderungen** "  
:::image-end:::  

Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , um große Zeilen zu aktivieren.  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Das Kontrollkästchen große Anforderungs Zeilen verwenden" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   Abbildung 36: Kontrollkästchen " **große Anforderungs Zeilen verwenden** "  
:::image-end:::  

### Ausblenden des Bereichs "Übersicht"  

Standardmäßig zeigt devtools den **Bereich "Übersicht"** an.  Deaktivieren Sie das Kontrollkästchen " **Übersicht anzeigen** ", um es auszublenden.  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Kontrollkästchen ' Übersicht anzeigen '" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   Abbildung 37: Kontrollkästchen ' **Übersicht anzeigen** '  
:::image-end:::  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Debuggen von progressiven Web-Apps"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Daten-URLs | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Proxy Server – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

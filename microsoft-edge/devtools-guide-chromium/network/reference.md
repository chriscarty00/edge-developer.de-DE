---
description: Eine umfassende Referenz zu den Features des Microsoft Edge devtools-Netzwerk Panels.
title: Netzwerkanalyse Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 8123fbebadf1d43fd1460ecebf91190cac793e19
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125370"
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
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  To verify which version of Microsoft Edge you are running, navigate to `edge://help`.  
-->

## Aufzeichnen von Netzwerkanforderungen  

Standardmäßig zeichnet devtools alle Netzwerkanforderungen im Netzwerk Panel auf, solange devtools geöffnet ist.  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-panel.msft.png":::
   **Netzwerk** Panel  
:::image-end:::  

### Beenden der Aufzeichnung von Netzwerkanforderungen  

Führen Sie die folgenden Schritte aus, um die Aufzeichnung von Anforderungen zu beenden.  

1.  Wählen Sie im Netzwerk Panel die Option **Aufzeichnung** ![ des Netzwerkprotokolls beenden aufzeichnen ][ImageRecordOnIcon] aus. **Network**  Es wird grau, um anzugeben, dass devtools keine Anforderungen mehr aufzeichnet.  
1.  Wählen Sie `Control` + `E` \ (Windows, Linux \) oder `Command` + `E` \ (macOS \) aus, während sich der Fokus des **Netzwerk** Panels befindet.  

### Löschen von Anforderungen  

Wählen Sie im Netzwerk Panel die Option **"Löschen"** ![ ][ImageClearIcon] aus, um alle Anforderungen aus der Tabelle "Anforderungen" zu löschen.  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-clear-button.msft.png":::
   Die Schaltfläche " **Löschen** "  
:::image-end:::  

### Speichern von Anforderungen über Seitenlasten hinweg  

Aktivieren Sie das Kontrollkästchen **Protokoll beibehalten** auf der Registerkarte Netzwerk, um Anforderungen zwischen den Seitenlasten zu speichern.  DevTools speichert alle Anforderungen, bis Sie **Protokoll beibehalten**deaktivieren.  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-preserve-log.msft.png":::
   Kontrollkästchen " **Protokoll beibehalten** "  
:::image-end:::  

### Aufzeichnen von Screenshots beim Laden der Seite  

Screenshots aufzeichnen, um zu analysieren, was für Benutzer angezeigt wird, während Sie darauf warten, dass Ihre Seite geladen wird.  

Wenn Sie Screenshots aktivieren möchten, wählen Sie **Netzwerkeinstellungen** und dann auf der Registerkarte **Netzwerk** die Option **Screenshots aufzeichnen** aus.  

Aktualisieren Sie die Seite, während sich das **Netzwerk** Panel im Fokus befindet, um Screenshots zu erfassen.  

Nachdem Sie einen Screenshot aufgezeichnet haben, interagieren Sie mit ihm auf die folgende Weise.  

*   Zeigen Sie mit der Maus auf einen Screenshot, um den Punkt anzuzeigen, an dem dieser Screenshot aufgenommen wurde.  Im Bereich " **Übersicht** " wird eine gelbe Zeile angezeigt.  
*   Wählen Sie die Miniaturansicht eines Bildschirms aus, um alle Anforderungen zu filtern, die nach dem Erfassen des Screenshots aufgetreten sind.  
*   Doppelklicken Sie auf eine Miniaturansicht, um Sie zu vergrößern.  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-screenshot-hover.msft.png":::
   Zeigen auf einen Screenshot  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-replay-xhr.msft.png":::
   Selecting Replay XHR  
:::image-end:::  
-->  

## Ändern des Ladeverhaltens  

### Emulieren eines erstmaligen Besuchers durch Deaktivieren des Browsercaches  

Aktivieren Sie das Kontrollkästchen **Cache deaktivieren** , um zu emulieren, wie ein Erstbenutzer Ihre Website erlebt.  DevTools deaktiviert den Browsercache.  Dieses Feature emuliert die Benutzerfreundlichkeit des ersten Benutzers genauer, da Anforderungen im Browser-Cache für wiederholte Besuche bereitgestellt werden.  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   Kontrollkästchen " **Cache deaktivieren** "  
:::image-end:::  

#### Deaktivieren des Browser-Caches aus der Schublade "Netzwerkbedingungen"  

Wenn Sie den Cache während der Arbeit in anderen devtools-Panels deaktivieren möchten, verwenden Sie die Schublade Netzwerkbedingungen.  

1.  Öffnen Sie die Schublade **Netzwerkbedingungen** .  
1.  Aktivieren oder deaktivieren Sie das Kontrollkästchen **Cache deaktivieren** .  

<!--todo: add network condition section when available -->  

### Manuelles Löschen des Browsercaches  

Wenn Sie den Browser-Cache jederzeit manuell löschen möchten, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browsercache löschen**aus.  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   Auswählen des **Browser Cache löschen**  
:::image-end:::  

### Offline emulieren  

Eine neue Klasse von Web-Apps mit dem Namen " [Progressive Web Apps][DevtoolsProgressiveWebApps]" funktioniert mit Hilfe von **Servicemitarbeitern**offline.  Möglicherweise ist es hilfreich, ein Gerät, das keine Datenverbindung aufweist, schnell zu simulieren, wenn Sie diese Art von App erstellen.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Wählen Sie das Dropdownmenü **Online** aus, suchen Sie unter **Voreinstellungen**, und wählen Sie **Offline** aus, um eine Offlinenetzwerk Umgebung zu simulieren.  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-offline-dropdown.msft.png":::
   Das **Offline** -Dropdownmenü  
:::image-end:::  

### Emulieren langsamer Netzwerkverbindungen  

Emulieren Sie langsames 3G, fast 3G und andere Verbindungsgeschwindigkeiten über das **Online-Dropdown-** Menü.  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-throttling-menu.msft.png":::
   Dropdownmenü " **Drosselung** "  
:::image-end:::  

Sie können aus unterschiedlichen Voreinstellungen wie Slow 3G oder fast 3G wählen.  Sie können auch eigene benutzerdefinierte Voreinstellungen hinzufügen, indem Sie das Menü Drosselung öffnen und **benutzerdefiniertes**  >  **Add**auswählen.  

DevTools zeigt ein Warnungssymbol neben der Registerkarte " **Netzwerk** " an, um Sie daran zu erinnern, dass die Drosselung aktiviert ist.  

#### Emulieren von langsamen Netzwerkverbindungen über die Netzwerkbedingungen Schublade  

Wenn Sie die Netzwerkverbindung während der Arbeit in anderen devtools-Panels Drosseln möchten, verwenden Sie den Netzwerkbedingungen-Einzug.  

1.  Öffnen Sie die Schublade **Netzwerkbedingungen** .  
1.  Wählen Sie im Menü **Drosselung** Ihre Verbindungsgeschwindigkeit aus.  

<!--todo: add network condition section when available -->  

### Manuelles Löschen von Browser-Cookies  

Wenn Sie Browser-Cookies jederzeit manuell löschen möchten, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browser-Cookies löschen**aus.  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   Auswählen von **Browser-Cookies löschen**  
:::image-end:::  

### Überschreiben des Benutzer-Agents  

Führen Sie die folgenden Schritte aus, um den Benutzer-Agent manuell zu überschreiben.  

1.  Öffnen Sie die Schublade **Netzwerkbedingungen** .  
1.  Deaktivieren **Sie SELECT automatisch**.  
1.  Wählen Sie eine Option für den Benutzer-Agent aus dem Menü aus, oder geben Sie eine benutzerdefinierte Option in das Textfeld ein.  

<!--todo: add network condition section when available -->  

## Filter Anforderungen  

### Filtern von Anforderungen nach Eigenschaften  

Verwenden Sie das Textfeld **Filtern** , um Anforderungen nach Eigenschaften wie der Domäne oder der Größe der Anforderung zu filtern.  

Wenn das Textfeld nicht angezeigt wird, ist der **Filter** Bereich wahrscheinlich ausgeblendet.  
Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zum [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-filters-textbox.msft.png":::
   Das Textfeld " **Filter** "  
:::image-end:::  

Sie können mehrere Eigenschaften gleichzeitig verwenden, indem Sie jede Eigenschaft mit einem Leerzeichen voneinander trennen.  Zeigt beispielsweise `mime-type:image/png larger-than:1K` alle PNGs an, die größer als 1 KB sind.  Die Filter für mehrere Eigenschaften sind äquivalent zu `AND` Vorgängen.  `OR` Vorgänge werden zurzeit nicht unterstützt.  

Die vollständige Liste der unterstützten Eigenschaften.  

| Eigenschaft | Details |  
|:--- | :--- |  
| `domain` | Zeigt nur Ressourcen aus der angegebenen Domäne an.  Sie können ein Platzhalterzeichen \ ( `*` \) verwenden, um mehrere Domänen einzubeziehen.  Zeigt beispielsweise `*.com` Ressourcen aus allen Domänennamen an, die in endet `.com` .  DevTools füllen Sie das Dropdownmenü AutoVervollständigen mit allen gefundenen Domänen auf. |  
| `has-response-header` | Zeigt die Ressourcen an, die den angegebenen HTTP-Antwortheader enthalten.  DevTools füllen Sie die Dropdownliste AutoVervollständigen mit allen gefundenen Antwortheadern auf. |  
| `is` | Verwendet `is:running` , um `WebSocket` Ressourcen zu finden. |  
| `larger-than` | Zeigt Ressourcen an, die größer als die angegebene Größe in Bytes sind.  Das Festlegen eines Werts von entspricht dem `1000` Festlegen eines Werts von `1k` . |  
| `method` | Zeigt Ressourcen an, die über einen angegebenen http-Methodentyp abgerufen wurden.  DevTools füllen Sie die Dropdownliste mit allen gefundenen HTTP-Methoden auf. |  
| `mime-type` | Zeigt Ressourcen eines angegebenen MIME-Typs an.  DevTools füllen Sie die Dropdownliste mit allen gefundenen MIME-Typen auf. |  
| `mixed-content` | Alle gemischten Inhalts Ressourcen anzeigen \ ( `mixed-content:all` \) oder nur diejenigen, die aktuell angezeigt werden \ ( `mixed-content:displayed` \). |  
| `scheme` | Zeigt Ressourcen an, die über ungeschützten http \ ( `scheme:http` \) oder geschütztes HTTPS \ ( `scheme:https` \) abgerufen wurden. |  
| `set-cookie-domain` | Zeigt Ressourcen `Set-Cookie` mit einer Kopfzeile mit einem `Domain` Attribut an, das dem angegebenen Wert entspricht.  DevTools füllen Sie das AutoVervollständigen mit allen gefundenen Cookie-Domänen auf. |  
| `set-cookie-name` | Zeigt Ressourcen `Set-Cookie` mit einer Kopfzeile mit einem Namen an, der dem angegebenen Wert entspricht.  DevTools füllen Sie die AutoVervollständigen-Datei mit allen gefundenen Cookienamen auf. |  
| `set-cookie-value` | Zeigt Ressourcen `Set-Cookie` mit einer Kopfzeile mit einem Wert an, der dem angegebenen Wert entspricht.  DevTools füllen Sie das AutoVervollständigen mit allen gefundenen Cookie-Werten auf. |  
| `status-code` | Zeigt Ressourcen an, die dem spezifischen HTTP-Statuscode entsprechen.  DevTools füllt das Dropdownmenü AutoVervollständigen mit allen gefundenen Statuscodes auf. |  

### Filtern von Anforderungen nach Typ  

Wenn Sie Anforderungen nach Anforderungsfiltern möchten, wählen Sie eine der folgenden Schaltflächen im **Netzwerk** Panel aus.  

:::row:::
   :::column span="1":::
      **XMLHttpRequest**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **JS**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **CSS**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **IMG**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Media**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Font**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Doc**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **WS**  
   :::column-end:::
   :::column span="2":::
      WebSocket.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Manifest**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Other**  
   :::column-end:::
   :::column span="2":::
      Jeder andere Typ, der nicht aufgeführt ist.  
   :::column-end:::
:::row-end:::  

Wenn die Schaltflächen nicht angezeigt werden, ist der Bereich " **Filter** " möglicherweise ausgeblendet.  
Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zum [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).  

Wenn Sie mehrere Typen Filter gleichzeitig aktivieren möchten, halten `Control` Sie \ (Windows, Linux \) oder `Command` \ (macOS \), und wählen Sie dann aus.  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-type-filters.msft.png":::
   Verwenden des Typs "Filter" zum Anzeigen von JS-, CSS-und Dokument Ressourcen  
:::image-end:::  

### Filtern von Anforderungen nach Zeit  

Wählen Sie aus, und ziehen Sie im Übersichtsbereich nach links oder rechts, um nur Anforderungen anzuzeigen, die während dieses Zeitrahmens aktiv waren.  Der Filter ist inklusive.  Jede Anforderung, die während der hervorgehobenen Zeit aktiv war, wird angezeigt.  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-overview-filter.msft.png":::
   Herausfiltern von Anforderungen, die um 300 ms inaktiv waren  
:::image-end:::  

### Ausblenden von Daten-URLs  

[Daten-URLs][MDNHTTPDataURIs] sind kleine Dateien, die in andere Dokumente eingebettet sind.  Jede Anforderung, die in der Tabelle "Anforderungen" angezeigt wird, beginnt mit `data:` einer Daten-URL.  

Aktivieren Sie das Kontrollkästchen **Daten-URLs ausblenden** , um die Anforderungen auszublenden.  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-hide-data-urls.msft.png":::
   Das Kontrollkästchen " **Daten-URLs ausblenden** "  
:::image-end:::  

## Sortieren von Anforderungen  

Standardmäßig werden die Anforderungen in der Tabelle Anforderungen nach Initiierungs Zeit sortiert, aber Sie können die Tabelle mit anderen Kriterien sortieren.  

### Nach Spalte sortieren  

Wählen Sie die Kopfzeile einer beliebigen Spalte in den Anforderungen aus, um Anforderungen nach dieser Spalte zu sortieren.  

### Nach Aktivitätsphase sortieren  

Wenn Sie ändern möchten, wie der Wasserfall Anforderungen sortiert, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), zeigen Sie mit der Maus auf **Wasserfall**, und wählen Sie eine der folgenden Optionen aus.  

:::row:::
   :::column span="1":::
      **Startzeit**  
   :::column-end:::
   :::column span="2":::
      Die erste Anforderung, die initiiert wurde, ist oben.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Antwortzeit**  
   :::column-end:::
   :::column span="2":::
      Die erste Anforderung, die den Download begonnen hat, ist ganz oben.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Endzeit**  
   :::column-end:::
   :::column span="2":::
      Die erste abgeschlossene Anforderung ist oben.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Gesamtdauer**  
   :::column-end:::
   :::column span="2":::
      Die Anforderung mit den kürzesten Verbindungseinstellungen und der Anforderung oder Antwort ist oben.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Latenz**  
   :::column-end:::
   :::column span="2":::
      Die Anforderung, die die kürzeste Zeit für eine Antwort gewartet hat, ist oben.  
   :::column-end:::
:::row-end:::  

Bei diesen Beschreibungen wird davon ausgegangen, dass die jeweilige Option von kürzester bis längster Position bewertet wird.  Wenn Sie die Kopfzeile der Spalte **Wasserfall** auswählen, wird die Reihenfolge umgekehrt.  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   Sortieren des Wasserfalls nach Gesamtdauer \ (der leichtere Teil der einzelnen Balken ist die Zeit, die gewartet wird, und der dunklere Teil ist die Zeit, die zum Herunterladen von Bytes verwendet wird \)  
:::image-end:::  

## Analysieren von Anforderungen  

Solange devtools geöffnet sind, werden alle Anforderungen im Netzwerk Panel protokolliert.  
Verwenden Sie das Netzwerk Panel, um Anforderungen zu analysieren.  

### Anzeigen eines Protokolls der Anforderungen  

Verwenden Sie die Tabelle "Anforderungen", um ein Protokoll aller Anforderungen anzuzeigen, die während der devtools geöffnet wurden.  Wenn Sie über Anforderungen auswählen oder darauf zeigen, werden weitere Informationen zu den einzelnen Elementen eingeblendet.  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-table.msft.png":::
   Die Tabelle "Anforderungen"  
:::image-end:::  

In der Tabelle Anforderungen werden standardmäßig die folgenden Spalten angezeigt.  

:::row:::
   :::column span="1":::
      **Name**  
   :::column-end:::
   :::column span="2":::
      Der Dateiname von oder ein Bezeichner für die Ressource.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Status**  
   :::column-end:::
   :::column span="2":::
      Der HTTP-Statuscode.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Typ**  
   :::column-end:::
   :::column span="2":::
      Der MIME-Typ der angeforderten Ressource.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Initiator**  
   :::column-end:::
   :::column span="2":::
      Die folgenden Objekte oder Prozesse initiieren Anforderungen.  
      
      *   **Parser**  Der HTML-Parser für Microsoft Edge.  
      *   **Umleitung**  Eine HTTP-Umleitung.  
      *   **Skript**  Eine JavaScript-Funktion.  
      *   **Andere**  Personen  Einige andere Prozesse oder Aktionen, wie das Navigieren zu einer Seite mithilfe eines Links oder das Eingeben einer URL in der Adressleiste.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Size**  
   :::column-end:::
   :::column span="2":::
      Die kombinierte Größe der Antwortheader sowie des Antworttexts, wie vom Server bereitgestellt.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Zeit**  
   :::column-end:::
   :::column span="2":::
      Die Gesamtdauer vom Anfang der Anforderung bis zum Empfang des letzten Bytes in der Antwort.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Wasserfall](#view-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      Eine visuelle Gliederung der Aktivität für jede Anforderung.  
   :::column-end:::
:::row-end:::  

#### Hinzufügen oder Entfernen von Spalten  

Zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie eine Option aus, um sie auszublenden oder anzuzeigen.  Die aktuell angezeigten Optionen verfügen über Kontrollkästchen neben den einzelnen Elementen.  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-add-column.msft.png":::
   Hinzufügen einer Spalte zur Tabelle "Anforderungen"  
:::image-end:::  

#### Hinzufügen benutzerdefinierter Spalten  

Wenn Sie der Tabelle Anforderungen eine benutzerdefinierte Spalte hinzufügen möchten, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Antwortheader**  >  **Verwalten von Kopfzeilen Spalten**aus.  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-add-custom.msft.png":::
   Hinzufügen einer benutzerdefinierten Spalte zur Tabelle "Anforderungen"  
:::image-end:::  

### Anzeigen der Zeit Steuerungsbeziehung von Anforderungen  

Verwenden Sie den Wasserfall, um die Timing-Beziehungen von Anforderungen anzuzeigen.  
Die Standardorganisation des Wasserfalls verwendet die Startzeit der Anforderungen.  
Anforderungen, die weiter Links sind, wurden früher als die Anforderungen weiter rechts gestartet.  

Wenn Sie die verschiedenen Möglichkeiten zum Sortieren des Wasserfalls überprüfen möchten, navigieren Sie zu nach [Aktivitätsphase sortieren](#sort-by-activity-phase).  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-waterfall.msft.png":::
   Spalte "Wasserfall" im Bereich " **Anforderungen** "  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection, use the following steps.  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** tab  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### Anzeigen einer Vorschau eines Antworttexts  

Führen Sie die folgenden Schritte aus, um eine Vorschau eines Antworttexts anzuzeigen.  

1.  Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie die Registerkarte **Vorschau** aus.  

Diese Registerkarte ist hauptsächlich für die Anzeige von Bildern hilfreich.  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-preview.msft.png":::
   Registerkarte " **Vorschau** "  
:::image-end:::  

### Anzeigen eines Antworttexts  

Führen Sie die folgenden Schritte aus, um den Antworttext für eine Anforderung anzuzeigen.  

1.  Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie die Registerkarte **Antwort** aus.  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-response.msft.png":::
   Die Registerkarte " **Antwort** "  
:::image-end:::  

### Anzeigen von HTTP-Headern  

Führen Sie die folgenden Schritte aus, um die HTTP-Header Daten zu einer Anforderung anzuzeigen.  

1.  Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie die Registerkarte über **Schriften** aus.  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-resources-headers.msft.png":::
   Die Registerkarte "über **Schriften** "  
:::image-end:::  

#### Anzeigen der HTTP-Header Quelle  

Standardmäßig werden auf der Registerkarte Kopfzeilennamen in alphabetischer Reihenfolge angezeigt.  Führen Sie die folgenden Schritte aus, um die HTTP-Headernamen in der eingegangenen Reihenfolge anzuzeigen.  

1.  Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.  Weitere Informationen finden Sie unter [Anzeigen von HTTP-Kopfzeilen](#view-http-headers).  
1.  Wählen Sie **Quelle anzeigen**neben dem Abschnitt **Anforderungs Kopfzeile** oder **Antwort Kopf** aus.  

### Anzeigen von Abfragezeichenfolgenparametern  

Führen Sie die folgenden Schritte aus, um die Abfragezeichenfolgenparameter einer URL in einem menschlich lesbaren Format anzuzeigen.  

1.  Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.  Weitere Informationen finden Sie unter [Anzeigen von HTTP-Kopfzeilen](#view-http-headers).  
1.  Wechseln Sie zum Abschnitt **Abfragezeichenfolgenparameter** .  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   Der **Abfragezeichenfolgenparameter** Abschnitt  
:::image-end:::  

#### Anzeigen der Parameterquelle für Abfragezeichenfolgen  

Führen Sie die folgenden Schritte aus, um die Abfragezeichenfolgenparameter Quelle einer Anforderung anzuzeigen.  

1.  Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.  Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#view-query-string-parameters).  
1.  Wählen Sie **Quelltext anzeigen**aus.  

#### Anzeigen von URL-codierten Abfragezeichenfolgenparametern  

Führen Sie die folgenden Schritte aus, um Abfragezeichenfolgenparameter in einem menschlich lesbaren Format anzuzeigen, jedoch mit erhaltenen Codierungen.  

1.  Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.  Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#view-query-string-parameters).  
1.  Wählen Sie **View URL encoded**aus.  

### Cookies anzeigen  

Führen Sie die folgenden Schritte aus, um die im HTTP-Header einer Anforderung gesendeten Cookies anzuzeigen.  

1.  Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie die Registerkarte **Cookies** aus.  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-cookies.msft.png":::
   Die Registerkarte "Cookies"  
:::image-end:::  

### Anzeigen der Zeit Plan Aufteilung einer Anforderung  

Führen Sie die folgenden Schritte aus, um die Anzeigedauer einer Anforderung anzuzeigen.  

1.  Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie die Registerkarte **Anzeige** Dauer aus.  

Um eine schnellere Möglichkeit für den Zugriff auf die Daten zu erhalten, navigieren Sie zu [Vorschau einer Anzeige](#preview-a-timing-breakdown)Dauer.  

Weitere Informationen zu den einzelnen Phasen, die möglicherweise auf der Registerkarte **Anzeige** Dauer angezeigt werden, finden Sie unter [erläuterte](#timing-breakdown-phases-explained)Phasen der Anzeigedauer.  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-timing.msft.png":::
   Registerkarte " **Anzeige** Dauer"  
:::image-end:::  

Weitere Informationen zu den einzelnen Phasen.  

Weitere Informationen zum Zugriff auf die Ansicht finden Sie unter [Aufschlüsselung](#view-the-timing-breakdown-of-a-request)der Anzeigedauer.  

#### Anzeigen einer Vorschau einer Anzeigedauer  

Wenn Sie eine Vorschau der Zeit Plan Aufteilung einer Anforderung anzeigen möchten, zeigen Sie in der Spalte **Wasserfall** der Tabelle Anforderungen auf den Eintrag für die Anforderung.  

Weitere Informationen dazu, wie Sie auf die Daten zugreifen können, ohne zu schweben, finden Sie unter [Anzeigen der Anzeigedauer einer Anforderung](#view-the-timing-breakdown-of-a-request).  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   Anzeigen einer Vorschau der Anzeigedauer einer Anforderung  
:::image-end:::  

#### Erläuterte Phasen Aufgliederungs Phasen  

Weitere Informationen zu den einzelnen Phasen **, die auf der Registerkarte** Anzeigedauer angezeigt werden können.  

:::row:::
   :::column span="1":::
      **Queueing**  
   :::column-end:::
   :::column span="2":::
      Der Browser Warteschlangenanforderungen, wenn eine der folgenden Bedingungen erfüllt ist.  
      *   Anforderungen mit höherer Priorität bestehen.  
      *   Sechs TCP-Verbindungen sind für denselben Ursprung geöffnet, was die Grenze ist.  Gilt nur für HTTP/1.0 und HTTP/1.1.  
      *   Der Browser reserviert kurzzeitig Speicherplatz im Datenträgercache.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Blockiert**  
   :::column-end:::
   :::column span="2":::
      Die Anforderung wird aus den in der **Warteschlange**beschriebenen Gründen angehalten.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **DNS-Lookup**  
   :::column-end:::
   :::column span="2":::
      Der Browser löst die IP-Adresse für die Anforderung auf.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Anfängliche Verbindung**  
   :::column-end:::
   :::column span="2":::
      Der Browser stellt eine Verbindung her, einschließlich TCP-Handshakes, TCP-Wiederholungen und verhandelt eine sichere Socketebene.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Proxy Verhandlung**  
   :::column-end:::
   :::column span="2":::
      Der Browser verhandelt die Anforderung mit einem [Proxy Server][WikiProxyServer].  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Anfrage gesendet**  
   :::column-end:::
   :::column span="2":::
      Die Anfrage wird gesendet.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **ServiceWorker-Vorbereitung**  
   :::column-end:::
   :::column span="2":::
      Der Browser startet den Dienstmitarbeiter.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Anforderung an ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      Die Anforderung wird an den Dienstmitarbeiter gesendet.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Waiting \ (TTFB \)**  
   :::column-end:::
   :::column span="2":::
      Der Browser wartet auf das erste Byte einer Antwort.  TTFB steht für Time to First Byte.  Dieser Zeitpunkt umfasst eine Roundtrip-Wartezeit und die Zeitdauer, die der Server zum Vorbereiten der Antwort benötigte.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Herunterladen von Inhalten**  
   :::column-end:::
   :::column span="2":::
      Der Browser empfängt die Antwort.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Empfangen von Push**  
   :::column-end:::
   :::column span="2":::
      Der Browser empfängt Daten für diese Antwort über http/2 Server Push.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Lese Push**  
   :::column-end:::
   :::column span="2":::
      Der Browser liest die zuvor empfangenen lokalen Daten.  
   :::column-end:::
:::row-end:::  

### Anzeigen von Initiatoren und Abhängigkeiten  

Wenn Sie die Initiatoren und Abhängigkeiten einer Anforderung anzeigen möchten, halten Sie `Shift` die Anforderung in der Tabelle Anforderungen gedrückt, und zeigen Sie darauf.  DevTools Farben: Initiatoren werden in grün angezeigt, und Abhängigkeiten werden in rot angezeigt.  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung  
:::image-end:::  

Wenn die Anforderungstabelle chronologisch geordnet ist, wenn Sie auf eine Zeile zeigen, wird in der davor liegenden Zeile eine grüne Anforderung angezeigt.  Die grüne Anforderung ist der Initiator der Abhängigkeit.  Wenn zuvor eine andere grüne Anforderung in der Zeile angezeigt wird, ist diese höhere Anforderung der Initiator des Initiators.  Und so weiter.  

### Laden Ereignisse anzeigen  

DevTools zeigt die Anzeigedauer der `DOMContentLoaded` `load` Ereignisse und Ereignisse an mehreren Stellen im Netzwerk Panel an.  Das `DOMContentLoaded` Ereignis ist blau gefärbt, und das `load` Ereignis ist rot.  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-load-events.msft.png":::
   Die Speicherorte der `DOMContentLoaded` und- `load` Ereignisse im Netzwerk Panel  
:::image-end:::  

### Anzeigen der Gesamtzahl der Anforderungen  

Die Gesamtzahl der Anforderungen wird im Bereich "Zusammenfassung" unten im Netzwerkbereich aufgelistet.  

> [!CAUTION]
> Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.  Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden diese Anforderungen nicht gezählt.  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-total-requests.msft.png":::
   Die Gesamtzahl der Anforderungen seit dem Öffnen von devtools  
:::image-end:::  

### Anzeigen der Gesamtgröße des Downloads  

Die Gesamtgröße der Downloadanforderungen wird im Bereich "Zusammenfassung" am unteren Rand des Netzwerkbereichs angezeigt.  

> [!CAUTION]
> Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.  Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden die vorherigen Anforderungen nicht gezählt.  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-total-download-size.msft.png":::
   Die Gesamtgröße der Downloads von Anforderungen  
:::image-end:::  

Navigieren Sie zum [Anzeigen der unkomprimierten Größe einer Ressource](#view-the-uncompressed-size-of-a-resource), um zu überprüfen, wie umfangreiche Ressourcen sind, nachdem der Browser die einzelnen Elemente dekomprimiert hat.  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   Die Stapelüberwachung, die zu einer Ressourcenanforderung führt  
:::image-end:::  

### Anzeigen der unkomprimierten Größe einer Ressource  

Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , und schauen Sie sich den niedrigsten Wert der Spalte **Größe** an.  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   Ein Beispiel für unkomprimierte Ressourcen \ (die komprimierte Größe der `jquery-3.3.1.min.js` Datei, die über das Netzwerk gesendet wurde `29.9 KB` , während die unkomprimierte Größe `84.9 KB` \) war  
:::image-end:::  

## Exportieren von Anforderungsdaten  

### Speichern aller Netzwerkanforderungen in einer har-Datei  

Führen Sie die folgenden Schritte aus, um alle Netzwerkanforderungen in einer har-Datei zu speichern.  

1.  Zeigen Sie auf jede Anforderung in der Tabelle Anforderungen, und öffnen Sie das Kontextmenü \ (mit der rechten Maustaste auf \).  
1.  Wählen Sie **als har mit Inhalt speichern**aus.  DevTools speichert alle Anforderungen, die seit dem Öffnen von devtools in der har-Datei aufgetreten sind.  Sie können keine Anforderungen filtern.  Sie können auch keine einzelne Anfrage speichern.  

Nachdem Sie eine har-Datei gespeichert haben, können Sie Sie für die Analyse wieder in devtools importieren.  Ziehen Sie die har-Datei einfach per Drag & Drop in die Tabelle "Anforderungen".  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   Auswählen **von "als har mit Inhalt speichern** "  
:::image-end:::  

### Kopieren einer oder mehrerer Anforderungen in die Zwischenablage  

Zeigen Sie unter der Spalte **Name** der Tabelle Anforderungen auf eine Anforderung, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), zeigen Sie auf **Kopieren**, und wählen Sie eine der folgenden Optionen aus.  

:::row:::
   :::column span="1":::
      **Link Adresse kopieren**  
   :::column-end:::
   :::column span="2":::
      Kopieren Sie die URL der Anforderung in die Zwischenablage.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Antwort kopieren**  
   :::column-end:::
   :::column span="2":::
      Kopieren Sie den Antworttext in die Zwischenablage.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Als FETCH kopieren**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Als curl kopieren**  
   :::column-end:::
   :::column span="2":::
      Kopieren Sie die Anforderung als curl-Befehl.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Alle als FETCH kopieren**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Alle als curl kopieren**  
   :::column-end:::
   :::column span="2":::
      Kopieren Sie alle Anforderungen als eine Kette von curl-Befehlen.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Alle als har kopieren**  
   :::column-end:::
   :::column span="2":::
      Kopieren Sie alle Anforderungen als har-Daten.  
   :::column-end:::
:::row-end:::  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-copy-response.msft.png":::
   Auswählen von " **Antwort kopieren** "  
:::image-end:::  

## Ändern des Layouts des Netzwerk Panels  

Sie können Abschnitte der Netzwerk Panel-UI erweitern oder reduzieren, um wichtige Informationen zu konzentrieren.  

### Ausblenden des Bereichs "Filter"  

Standardmäßig zeigt devtools den **Bereich "Filter"** an.  
Wählen Sie **Filter** \ ( ![ Filter ][ImageFilterIcon] \) aus, um sie auszublenden.  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   Schaltfläche "Filter ausblenden"  
:::image-end:::  

### Verwenden von umfangreichen Anforderungs Zeilen  

Verwenden Sie große Zeilen, wenn in Ihrer Netzwerk Anforderungstabelle mehr Leerzeichen verwendet werden sollen.  Einige Spalten liefern auch ein wenig mehr Informationen, wenn Sie große Zeilen verwenden.  Der untere Wert der Spalte **size** entspricht beispielsweise der unkomprimierten Größe einer Anforderung.  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   Ein Beispiel für große Anforderungs Zeilen im Bereich " **Anforderungen** "  
:::image-end:::  

Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , um große Zeilen zu aktivieren.  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   Das Kontrollkästchen " **große Anforderungs Zeilen verwenden** "  
:::image-end:::  

### Ausblenden des Bereichs "Übersicht"  

Standardmäßig zeigt devtools den **Bereich "Übersicht"** an.  Deaktivieren Sie das Kontrollkästchen " **Übersicht anzeigen** ", um es auszublenden.  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   Kontrollkästchen ' **Übersicht anzeigen** '  
:::image-end:::  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps.md "Debuggen von progressiven Web-Apps | Microsoft docs"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

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

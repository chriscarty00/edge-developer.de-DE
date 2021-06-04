---
description: Eine umfassende Referenz zu Microsoft Edge DevTools Network Panel Features.
title: Netzwerkanalysereferenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: bdb1145e7ee8ed7865b68f9fd632c4b1a30007e9
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564833"
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
# <a name="network-analysis-reference"></a>Netzwerkanalysereferenz  

Entdecken Sie neue Möglichkeiten, wie Ihre Seite geladen wird, in diesem umfassenden Verweis Microsoft Edge DevTools-Netzwerkanalysefeatures.  

## <a name="record-network-requests"></a>Aufzeichnen von Netzwerkanforderungen  

Standardmäßig zeichnen DevTools alle Netzwerkanforderungen im **Netzwerktool** auf, solange DevTools geöffnet ist.  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Netzwerkbereich" lightbox="../media/network-network-panel.msft.png":::
   Das **Netzwerktool**  
:::image-end:::  

### <a name="stop-recording-network-requests"></a>Beenden der Aufzeichnung von Netzwerkanforderungen  

Führen Sie die folgenden Schritte aus, um aufzeichnungsanforderungen zu beenden.  

1.  Wählen Sie **im Tool** Netzwerk die Option **Aufzeichnungsnetzwerkprotokoll beenden** \( ![ Aufzeichnungsnetzwerkprotokoll beenden ](../media/record-on-icon.msft.png) \).  Es wird grau, um anzugeben, dass DevTools keine Anforderungen mehr aufzeichnen.  
1.  Wählen `Control` + `E` Sie \(Windows, Linux\) oder `Command` + `E` \(macOS\) **** aus, während das Netzwerktool im Fokus steht.  

### <a name="clear-requests"></a>Löschen von Anforderungen  

Klicken **Sie im** Netzwerktool auf Löschen \( Löschen \), um alle Anforderungen aus der Tabelle Anforderungen zu ![ ](../media/clear-requests-icon.msft.png) löschen. ****  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Die Schaltfläche Löschen" lightbox="../media/network-network-clear-button.msft.png":::
   Die **Schaltfläche Löschen**  
:::image-end:::  

### <a name="save-requests-across-page-loads"></a>Speichern von Anforderungen über Seitenlasten hinweg  

Aktivieren Sie zum Speichern von **** Anforderungen über Seitenlasten hinweg das Kontrollkästchen Protokoll **beibehalten** im Netzwerktool.  DevTools speichert alle Anforderungen, bis Sie **preserve log deaktivieren.**  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Das Kontrollkästchen Protokoll beibehalten" lightbox="../media/network-network-preserve-log.msft.png":::
   Das **Kontrollkästchen Protokoll** beibehalten  
:::image-end:::  

### <a name="capture-screenshots-during-page-load"></a>Erfassen von Screenshots beim Laden der Seite  

Erfassen Sie Screenshots, um zu analysieren, was für Benutzer angezeigt wird, während Sie darauf warten, dass Ihre Seite geladen wird.  

Um Screenshots zu aktivieren, wählen Sie **Netzwerkeinstellungen**aus, und aktivieren Sie im **Netzwerktool** das Kontrollkästchen Screenshots **erfassen.**  

Aktualisieren Sie die Seite, während das **Netzwerktool** im Fokus steht, um Screenshots zu erfassen.  

Nachdem Sie einen Screenshot erfasst haben, interagieren Sie wie folgt mit ihm.  

*   Zeigen Sie auf einen Screenshot, um den Punkt zu zeigen, an dem dieser Screenshot aufgenommen wurde.  Im Bereich Übersicht wird eine gelbe **Linie** angezeigt.  
*   Wählen Sie die Miniaturansicht eines Bildschirms aus, um alle Anforderungen herausfiltern zu können, die nach der Aufnahme des Screenshots aufgetreten sind.  
*   Doppelklicken Sie auf eine Miniaturansicht, um sie zu vergrößern.  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Zeigen auf einen Screenshot" lightbox="../media/network-network-screenshot-hover.msft.png":::
   Zeigen auf einen Screenshot  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <a name="change-loading-behavior"></a>Ändern des Ladeverhaltens  

### <a name="emulate-a-first-time-visitor-by-disabling-the-browser-cache"></a>Emulieren eines ersten Besuchers durch Deaktivieren des Browsercaches  

Aktivieren Sie das Kontrollkästchen Cache deaktivieren, um **** zu emulieren, wie ein Benutzer ihre Website zum ersten Mal erlebt.  DevTools deaktiviert den Browsercache.  Dieses Feature emuliert die Benutzererfahrung eines Erstbenutzers genauer, da Anforderungen beim wiederholten Besuch aus dem Browsercache übermittelt werden.  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Das Kontrollkästchen Cache deaktivieren" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   Das **Kontrollkästchen Cache** deaktivieren  
:::image-end:::  

#### <a name="disable-the-browser-cache-from-the-network-conditions-drawer"></a>Deaktivieren des Browsercaches aus der Schublade "Netzwerkbedingungen"  

Wenn Sie den Cache deaktivieren möchten, während Sie in anderen DevTools-Panels arbeiten, verwenden Sie die Schublade Netzwerkbedingungen.  

1.  Öffnen Sie **die Schublade Netzwerkbedingungen.**  
1.  Aktivieren Sie \(or off\) das **Kontrollkästchen Cache deaktivieren.**  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-the-browser-cache"></a>Löschen des Browsercaches manuell  

Um den Browsercache jederzeit manuell zu löschen, öffnen Sie das Kontextmenü \(rechtsklicken\) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browsercache löschen aus.**  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Wählen Sie Browsercache löschen aus" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   Wählen **Sie Browsercache löschen aus**  
:::image-end:::  

### <a name="emulate-offline"></a>Emulieren offline  

Eine neue Klasse von Web-Apps namens [Progressive Web Apps][DevtoolsProgressiveWebApps]funktioniert offline mit Hilfe von **Servicemitarbeitern.**  Möglicherweise ist es hilfreich, beim Erstellen dieser Art von App schnell ein Gerät zu simulieren, das keine Datenverbindung hat.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Wählen Sie das **Dropdownmenü Online** aus, suchen Sie unter **Presets,** und wählen Sie **Offline** aus, um eine Offlinenetzwerkerfahrung zu simulieren.  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Das Dropdownmenü Offline" lightbox="../media/network-network-offline-dropdown.msft.png":::
   Das **Dropdownmenü Offline**  
:::image-end:::  

### <a name="emulate-slow-network-connections"></a>Emulieren langsamer Netzwerkverbindungen  

Emulieren Sie langsame 3G, schnelle 3G und andere Verbindungsgeschwindigkeiten aus dem **Online-Dropdownmenü.**  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Das Dropdownmenü Einschränkung" lightbox="../media/network-network-throttling-menu.msft.png":::
   Das **Dropdownmenü Einschränkung**  
:::image-end:::  

Sie können aus verschiedenen Voreinstellungen auswählen, z. B. Slow 3G oder Fast 3G.  Öffnen Sie zum Hinzufügen eigener benutzerdefinierter Voreinstellungen das Menü Einschränkung, und wählen Sie **Benutzerdefiniertes**  >  **Hinzufügen aus.**  

DevTools zeigt ein Warnsymbol neben dem **Netzwerktool** an, um Sie daran zu erinnern, dass die Drosselung aktiviert ist.  

#### <a name="emulate-slow-network-connections-from-the-network-conditions-drawer&quot;></a>Emulieren langsamer Netzwerkverbindungen aus der Schublade &quot;Netzwerkbedingungen"  

Wenn Sie die Netzwerkverbindung drosseln möchten, während Sie in anderen DevTools-Panels arbeiten, verwenden Sie die Schublade Netzwerkbedingungen.  

1.  Öffnen Sie **die Schublade Netzwerkbedingungen.**  
1.  Wählen Sie ihre Verbindungsgeschwindigkeit im Menü **Einschränkung** aus.  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-browser-cookies"></a>Löschen von Browsercookies manuell  

Wenn Sie Browsercookies jederzeit manuell löschen möchten, zeigen Sie auf eine beliebige Stelle in der Tabelle Anforderungen, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste auf\), und wählen Sie Browsercookies **löschen aus.**  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Wählen Sie Browsercookies löschen aus" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   Wählen **Sie Browsercookies löschen aus**  
:::image-end:::  

### <a name="override-the-user-agent"></a>Überschreiben des Benutzer-Agents  

Verwenden Sie die folgenden Schritte, um den Benutzer-Agent manuell außer Kraft zu setzen.  

1.  Öffnen Sie **die Schublade Netzwerkbedingungen.**  
1.  Deaktivieren Sie das **Kontrollkästchen Automatisch** auswählen.  
1.  Wählen Sie im Menü eine Benutzer-Agent-Option aus, oder geben Sie eine benutzerdefinierte Option in das Textfeld ein.  

<!--todo: add network condition section when available -->  

## <a name="filter-requests"></a>Filteranforderungen  

### <a name="filter-requests-by-properties"></a>Filtern von Anforderungen nach Eigenschaften  

Verwenden Sie **das Textfeld Filter,** um Anforderungen nach Eigenschaften zu filtern, z. B. der Domäne oder der Größe der Anforderung.  

Wenn das Textfeld nicht angezeigt wird, **ist** der Filterbereich wahrscheinlich ausgeblendet.  
Weitere Informationen finden Sie unter [Ausblenden des Filterbereichs.](#hide-the-filters-pane)  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Das Textfeld Filter" lightbox="../media/network-network-filters-textbox.msft.png":::
   Das **Textfeld Filter**  
:::image-end:::  

Sie können mehrere Eigenschaften gleichzeitig verwenden, indem Sie jede Eigenschaft durch ein Leerzeichen trennen.  Zeigt beispielsweise `mime-type:image/png larger-than:1K` alle PNGs an, die größer als 1 KB sind.  Die Filter mit mehreren Eigenschaften entsprechen `AND` Vorgängen.  `OR` vorgänge werden derzeit nicht unterstützt.  

Die vollständige Liste der unterstützten Eigenschaften.  

| Eigenschaft | Details |  
|:--- | :--- |  
| `domain` | Nur Ressourcen aus der angegebenen Domäne anzeigen.  Sie können ein Platzhalterzeichen \( \) verwenden, `*` um mehrere Domänen zu enthalten.  Zeigt beispielsweise `*.com` Ressourcen aus allen Domänennamen an, die in enden. `.com`  DevTools füllen das Dropdownmenü autocomplete mit allen gefundenen Domänen auf. |  
| `has-response-header` | Zeigt die Ressourcen an, die den angegebenen HTTP-Antwortheader enthalten.  DevTools füllen das Dropdownmenü autocomplete mit allen gefundenen Antwortkopfzeilen auf. |  
| `is` | Verwenden `is:running` Sie zum Suchen von `WebSocket` Ressourcen. |  
| `larger-than` | Zeigt Ressourcen an, die größer als die angegebene Größe in Byte sind.  Das Festlegen eines `1000` Werts von entspricht dem Festlegen eines Werts von `1k` . |  
| `method` | Zeigt Ressourcen an, die über einen angegebenen HTTP-Methodentyp abgerufen wurden.  DevTools füllen das Dropdown mit allen gefundenen HTTP-Methoden auf. |  
| `mime-type` | Zeigt Ressourcen eines angegebenen MIME-Typs an.  DevTools füllen die Dropdownliste mit allen gefundenen MIME-Typen auf. |  
| `mixed-content` | Zeigen Sie alle gemischten Inhaltsressourcen \( \) oder nur die Ressourcen an, die derzeit `mixed-content:all` angezeigt werden \( `mixed-content:displayed` \). |  
| `scheme` | Zeigt Ressourcen an, die über ungeschütztes HTTP \( `scheme:http` \) oder geschütztes HTTPS \( `scheme:https` \) abgerufen werden. |  
| `set-cookie-domain` | Zeigt Ressourcen mit einem `Set-Cookie` Header mit einem Attribut `Domain` an, das dem angegebenen Wert entspricht.  DevTools füllen das autocomplete mit allen gefundenen Cookiedomänen auf. |  
| `set-cookie-name` | Zeigt Ressourcen an, die über `Set-Cookie` einen Header mit einem Namen verfügen, der dem angegebenen Wert entspricht.  DevTools füllen das AutoComplete mit allen gefundenen Cookienamen auf. |  
| `set-cookie-value` | Zeigt Ressourcen an, die über `Set-Cookie` einen Header mit einem Wert verfügen, der dem angegebenen Wert entspricht.  DevTools füllen das AutoComplete mit allen gefundenen Cookiewerten auf. |  
| `status-code` | Zeigt Ressourcen an, die dem spezifischen HTTP-Statuscode entsprechen.  DevTools füllt das Dropdownmenü für die automatische Vervollständigung mit allen gefundenen Statuscodes auf. |  

### <a name="filter-requests-by-type"></a>Filtern von Anforderungen nach Typ  

Um Anforderungen nach Anforderungstyp zu filtern, wählen Sie eine der folgenden Schaltflächen im **Netzwerktool** aus.  

:::row:::
   :::column span="1":::
      **XHR**  
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
      **Img**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Medien**  
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
      Alle anderen Nicht aufgeführten Typen.  
   :::column-end:::
:::row-end:::  

Wenn die Schaltflächen nicht angezeigt werden, **wird** der Filterbereich möglicherweise ausgeblendet.  
Weitere Informationen finden Sie unter [Ausblenden des Filterbereichs.](#hide-the-filters-pane)  

Um mehrere Filter gleichzeitig zu aktivieren, halten Sie `Control` \(Windows, Linux\) oder \(macOS\) fest, und wählen `Command` Sie dann aus.  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Verwenden der Typfilter zum Anzeigen von JS-, CSS- und Dokumentressourcen" lightbox="../media/network-network-type-filters.msft.png":::
   Verwenden der Typfilter zum Anzeigen von JS-, CSS- und Dokumentressourcen  
:::image-end:::  

### <a name="filter-requests-by-time"></a>Filtern von Anforderungen nach Zeit  

Klicken Sie im Bereich **** Übersicht nach links oder rechts, und ziehen Sie es, um nur Anforderungen anzuzeigen, die während dieses Zeitrahmens aktiv waren.  Der Filter ist inklusive.  Jede Anforderung, die während der hervorgehobenen Zeit aktiv war, wird angezeigt.  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtern von Anforderungen, die etwa 300 ms inaktiv waren" lightbox="../media/network-network-overview-filter.msft.png":::
   Filtern von Anforderungen, die etwa 300 ms inaktiv waren  
:::image-end:::  

### <a name="hide-data-urls"></a>Ausblenden von Daten-URLs  

[Daten-URLs][MDNHTTPDataURIs] sind kleine Dateien, die in andere Dokumente eingebettet sind.  Jede Anforderung, die in der Tabelle Anforderungen angezeigt wird, die mit `data:` beginnt, ist eine Daten-URL.  

Deaktivieren Sie das Kontrollkästchen **Daten-URLs** ausblenden, um die Anforderungen auszublenden.  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Das Kontrollkästchen Daten-URLs ausblenden" lightbox="../media/network-network-hide-data-urls.msft.png":::
   Das **Kontrollkästchen Daten-URLs** ausblenden  
:::image-end:::  

## <a name="sort-requests"></a>Sortieren von Anforderungen  

Standardmäßig werden die Anforderungen in der Tabelle Anforderungen nach Initiierungszeit sortiert, Sie können die Tabelle jedoch anhand anderer Kriterien sortieren.  

### <a name="sort-by-column"></a>Sortieren nach Spalte  

Wählen Sie die Kopfzeile einer beliebigen Spalte in der Spalte Anforderungen zum Sortieren von Anforderungen nach dieser Spalte aus.  

### <a name="sort-by-activity-phase"></a>Sortieren nach Aktivitätsphase  

Wenn Sie ändern möchten, wie der Wasserfall Anforderungen sortiert, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \(rechtsklicken\), zeigen Sie auf **Wasserfall,** und wählen Sie eine der folgenden Optionen aus.  

:::row:::
   :::column span="1":::
      **Startzeit**  
   :::column-end:::
   :::column span="2":::
      Die erste Anforderung, die initiiert wurde, befindet sich oben.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Antwortzeit**  
   :::column-end:::
   :::column span="2":::
      Die erste Anforderung, die mit dem Herunterladen begonnen hat, befindet sich oben.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Endzeit**  
   :::column-end:::
   :::column span="2":::
      Die erste abgeschlossene Anforderung befindet sich oben.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Gesamtdauer**  
   :::column-end:::
   :::column span="2":::
      Die Anforderung mit den kürzesten Verbindungseinstellungen und Anforderung oder Antwort befindet sich oben.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Latenz**  
   :::column-end:::
   :::column span="2":::
      Die Anforderung, die die kürzeste Zeit auf eine Antwort gewartet hat, befindet sich oben.  
   :::column-end:::
:::row-end:::  

In diesen Beschreibungen wird davon ausgegangen, dass jede option vom kürzesten zum längsten rangiert wird.  Wählen Sie die Kopfzeile der **Spalte Wasserfall** aus, um die Reihenfolge umzukehren.  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Sortieren des Wasserfalls nach Gesamtdauer" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   Sortieren Sie den Wasserfall nach gesamter Dauer \(Der hellere Teil jeder Leiste ist die Wartezeit, und der dunklere Teil ist die Zeit für das Herunterladen von Bytes\)  
:::image-end:::  

## <a name="analyze-requests"></a>Analysieren von Anforderungen  

Solange DevTools geöffnet sind, werden alle Anforderungen im **Netzwerktool** protokolliert.  
Verwenden Sie den Netzwerkbereich, um Anforderungen zu analysieren.  

### <a name="display-a-log-of-requests"></a>Anzeigen eines Protokolls mit Anforderungen  

Verwenden Sie die Tabelle Anforderungen, um ein Protokoll aller Anforderungen anzeigen zu können, die während des Öffnens von DevTools vorgenommen wurden.  Um weitere Informationen zu jedem Element zu erhalten, wählen Oder zeigen Sie auf Anforderungen.  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Die Tabelle Anforderungen" lightbox="../media/network-network-requests-table.msft.png":::
   Die Tabelle Anforderungen  
:::image-end:::  

In der Tabelle Anforderungen werden standardmäßig die folgenden Spalten angezeigt.  

:::row:::
   :::column span="1":::
      **Name**  
   :::column-end:::
   :::column span="2":::
      Der Dateiname oder ein Bezeichner für die Ressource.  
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
      *   **Andere**  Ein anderer Prozess oder eine andere Aktion, z. B. das Navigieren zu einer Seite mithilfe eines Links oder das Eingeben einer URL in der Adressleiste.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Size**  
   :::column-end:::
   :::column span="2":::
      Die kombinierte Größe der Antwortkopfzeilen und des Antworttexts, wie vom Server zugestellt.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Zeit**  
   :::column-end:::
   :::column span="2":::
      Die Gesamtdauer vom Beginn der Anforderung bis zum Eingang des letzten Bytes in der Antwort.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Wasserfall](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      Eine visuelle Aufschlüsselung der Aktivität für jede Anforderung.  
   :::column-end:::
:::row-end:::  

#### <a name="add-or-remove-columns"></a>Hinzufügen oder Entfernen von Spalten  

Zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie eine Option aus, um sie auszublenden oder anzuzeigen.  Derzeit angezeigte Optionen verfügen neben jedem Element über Häkchen.  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Hinzufügen einer Spalte zur Tabelle Anforderungen" lightbox="../media/network-network-requests-add-column.msft.png":::
   Hinzufügen einer Spalte zur Tabelle Anforderungen  
:::image-end:::  

#### <a name="add-custom-columns"></a>Hinzufügen benutzerdefinierter Spalten  

Wenn Sie der Tabelle Anforderungen eine benutzerdefinierte Spalte hinzufügen möchten, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Antwortkopfzeilen**Kopfzeilen verwalten  >  **aus.**  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Hinzufügen einer benutzerdefinierten Spalte zur Tabelle Anforderungen" lightbox="../media/network-network-requests-add-custom.msft.png":::
   Hinzufügen einer benutzerdefinierten Spalte zur Tabelle Anforderungen  
:::image-end:::  

### <a name="display-the-timing-relationship-of-requests"></a>Anzeigen der Zeitlichen Beziehung von Anforderungen  

Verwenden Sie den Wasserfall, um die Zeitlichen Beziehungen von Anforderungen anzeigen.  
Die Standardorganisation des Wasserfalls verwendet die Startzeit der Anforderungen.  
Anforderungen, die weiter links liegen, wurden also früher gestartet als die Anforderungen, die weiter rechts liegen.  

Um die verschiedenen Methoden zum Sortieren des Wasserfalls zu überprüfen, navigieren Sie zu [Sortieren nach Aktivitätsphase](#sort-by-activity-phase).  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Die Spalte "Wasserfall" im Bereich Anforderungen" lightbox="../media/network-network-requests-waterfall.msft.png":::
   Die Spalte "Wasserfall" im **Bereich Anforderungen**  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** panel.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** panel  
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

### <a name="display-a-preview-of-a-response-body"></a>Anzeigen einer Vorschau eines Antworttexts  

Um eine Vorschau eines Antworttexts anzuzeigen, verwenden Sie die folgenden Schritte.  

1.  Wählen Sie die URL der Anforderung unter der **Spalte Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie den **Bereich Vorschau** aus.  

Die Registerkarte Vorschau ist hauptsächlich hilfreich, um Bilder anzuzeigen.  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Der Vorschaubereich" lightbox="../media/network-network-resources-preview.msft.png":::
   Der **Vorschaubereich**  
:::image-end:::  

### <a name="display-a-response-body"></a>Anzeigen eines Antworttexts  

Zum Anzeigen des Antworttexts für eine Anforderung verwenden Sie die folgenden Schritte.  

1.  Wählen Sie die URL der Anforderung unter der **Spalte Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie den **Antwortbereich** aus.  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Der Antwortbereich" lightbox="../media/network-network-resources-response.msft.png":::
   Der **Antwortbereich**  
:::image-end:::  

### <a name="display-http-headers"></a>Anzeigen von HTTP-Headern  

Zum Anzeigen von HTTP-Headerdaten zu einer Anforderung verwenden Sie die folgenden Schritte.  

1.  Wählen Sie die URL der Anforderung unter der **Spalte Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie **das Kopfzeilen-Karussell** aus.  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Der Kopfzeilenbereich" lightbox="../media/network-resources-headers.msft.png":::
   Der **Kopfzeilenbereich**  
:::image-end:::  

#### <a name="display-http-header-source"></a>Anzeigen der HTTP-Headerquelle  

Standardmäßig werden im **Kopfzeilenbereich** Kopfzeilennamen alphabetisch angezeigt.  Verwenden Sie die folgenden Schritte, um die HTTP-Headernamen in der empfangenen Reihenfolge zu spielen.  

1.  Öffnen Sie **den Bereich** Kopfzeilen für die Anforderung, die Sie interessiert.  Weitere Informationen finden Sie unter [Anzeigen von HTTP-Headern](#display-http-headers).  
1.  Wählen **Sie Neben dem**Abschnitt **Anforderungsheader** oder **Antwortkopf** die Option Quelle anzeigen aus.  

### <a name="display-query-string-parameters"></a>Anzeigen von Abfragezeichenfolgenparametern  

Wenn Sie die Abfragezeichenfolgenparameter einer URL in einem lesbaren Format anzeigen möchten, verwenden Sie die folgenden Schritte.  

1.  Öffnen Sie **den Bereich** Kopfzeilen für die Anforderung, die Sie interessiert.  Weitere Informationen finden Sie unter [Anzeigen von HTTP-Headern](#display-http-headers).  
1.  Navigieren Sie zum **Abschnitt Abfragezeichenfolgenparameter.**  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Der Abschnitt Abfragezeichenfolgenparameter" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   Der **Abschnitt Abfragezeichenfolgenparameter**  
:::image-end:::  

#### <a name="display-query-string-parameters-source"></a>Quelle für Abfragezeichenfolgenparameter anzeigen  

Zum Anzeigen der Abfragezeichenfolgenparameterquelle einer Anforderung verwenden Sie die folgenden Schritte.  

1.  Navigieren Sie zum Abschnitt Abfragezeichenfolgenparameter.  Weitere Informationen finden Sie unter Anzeigen von [Abfragezeichenfolgenparametern.](#display-query-string-parameters)  
1.  Wählen **Sie Ansichtsquelle**aus.  

#### <a name="display-url-encoded-query-string-parameters"></a>Anzeigen von URL-codierten Abfragezeichenfolgenparametern  

Verwenden Sie die folgenden Schritte, um Abfragezeichenfolgenparameter in einem vom Menschen lesbaren Format, jedoch bei beibehaltenen Codierungen, anzeigen zu können.  

1.  Navigieren Sie zum Abschnitt Abfragezeichenfolgenparameter.  Weitere Informationen finden Sie unter Anzeigen von [Abfragezeichenfolgenparametern.](#display-query-string-parameters)  
1.  Wählen **Sie die url-codierte Ansicht aus.**  

### <a name="display-cookies"></a>Anzeigen von Cookies  

Verwenden Sie die folgenden Schritte, um die im HTTP-Header einer Anforderung gesendeten Cookies anzeigen zu können.  

1.  Wählen Sie die URL der Anforderung unter der **Spalte Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie den **Bereich Cookies** aus.  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Der Bereich Cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   Der Bereich "Cookies"  
:::image-end:::  

### <a name="display-the-timing-breakdown-of-a-request"></a>Anzeigen der Zeitlichen Aufschlüsselung einer Anforderung  

Verwenden Sie die folgenden Schritte, um die Zeitliche Aufschlüsselung einer Anforderung zu zeigen.  

1.  Wählen Sie die URL der Anforderung unter der **Spalte Name** der Tabelle Anforderungen aus.  
1.  Wählen Sie den **Zeitsteuerungsbereich** aus.  

Wenn Sie schneller auf die Daten zugreifen möchten, navigieren Sie zu [Vorschau einer Zeitplanungsaufschlüsselung.](#preview-a-timing-breakdown)  

Weitere Informationen zu den einzelnen Phasen, die möglicherweise **** im Zeitsteuerungsfenster angezeigt werden, finden Sie unter [Timing breakdown phases explained](#timing-breakdown-phases-explained).  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Der Zeitsteuerungsbereich" lightbox="../media/network-network-resources-timing.msft.png":::
   Der **Zeitsteuerungsbereich**  
:::image-end:::  

Weitere Informationen zu den einzelnen Phasen.  

Weitere Informationen zum Zugriff auf die Anzeige finden Sie unter [Anzeigezeitplan .](#display-the-timing-breakdown-of-a-request)  

#### <a name="preview-a-timing-breakdown"></a>Vorschau einer Zeitlichen Aufschlüsselung  

Wenn Sie eine Vorschau der Zeitlichen Aufschlüsselung einer Anforderung anzeigen möchten, zeigen Sie in der **Spalte Wasserfall** der Tabelle Anforderungen auf den Eintrag für die Anforderung.  

Weitere Informationen dazu, wie Sie auf die Daten zugreifen können, ohne darauf zu zeigen, finden Sie unter Anzeigen der Zeitlichen [Aufschlüsselung einer Anforderung.](#display-the-timing-breakdown-of-a-request)  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> Vorschau der Zeitlichen Aufschlüsselung einer Anforderung" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   Vorschau der Zeitlichen Aufschlüsselung einer Anforderung  
:::image-end:::  

#### <a name="timing-breakdown-phases-explained"></a>Erläuterte Phasen für die Zeitliche Aufschlüsselung  

Weitere Informationen zu den einzelnen Phasen, die möglicherweise im **Zeitsteuerungsfenster angezeigt** werden.  

:::row:::
   :::column span="1":::
      **Warteschlangen**  
   :::column-end:::
   :::column span="2":::
      Der Browser warteschlanget Anforderungen, wenn eine der folgenden Bedingungen zutrifft.  
      
      *   Anforderungen mit höherer Priorität sind vorhanden.  
      *   Sechs TCP-Verbindungen sind für denselben Ursprung geöffnet, d. h. die Grenze.  Gilt nur für HTTP/1.0 und HTTP/1.1.  
      *   Der Browser verteilt kurz Speicherplatz im Datenträgercache.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Ins Stocken geraten**  
   :::column-end:::
   :::column span="2":::
      Die Anforderung wird aus einem der unter Warteschlangen **beschriebenen Gründe ins Stocken geraten.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **DNS-Nachschlage**  
   :::column-end:::
   :::column span="2":::
      Der Browser aufgelöst die IP-Adresse für die Anforderung.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Anfängliche Verbindung**  
   :::column-end:::
   :::column span="2":::
      Der Browser richtet eine Verbindung ein, einschließlich TCP-Handshakes, TCP-Wiederholungen und aushandelt eine Secure Socket Layer.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Proxyaushandlung**  
   :::column-end:::
   :::column span="2":::
      Der Browser handelt die Anforderung mit einem [Proxyserver aus.][WikiProxyServer]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Gesendete Anforderung**  
   :::column-end:::
   :::column span="2":::
      Die Anforderung wird gesendet.  
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
      Die Anforderung wird an den Servicemitarbeiter gesendet.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Waiting \(TTFB\)**  
   :::column-end:::
   :::column span="2":::
      Der Browser wartet auf das erste Byte einer Antwort.  TTFB steht für Time To First Byte.  Dieser Zeitpunkt umfasst eine Roundtrip-Wartezeit und die Zeit, die der Server zum Vorbereiten der Antwort brauchte.  
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
      Der Browser empfängt Daten für diese Antwort über HTTP/2 Server Push.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Lese-Push**  
   :::column-end:::
   :::column span="2":::
      Der Browser liest die zuvor empfangenen lokalen Daten.  
   :::column-end:::
:::row-end:::  

### <a name="display-initiators-and-dependencies"></a>Anzeigen von Initiatoren und Abhängigkeiten  

Um die Initiatoren und Abhängigkeiten einer Anforderung anzuzeigen, halten Sie die Anforderung in der Tabelle Anforderungen, und zeigen Sie `Shift` auf die Anforderung.  DevTools-Farben: Initiatoren werden grün und Abhängigkeiten in Rot angezeigt.  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung  
:::image-end:::  

Wenn die Tabelle Anforderungen chronologisch geordnet ist, zeigt die zeile vor der Tabelle eine grüne Anforderung an, wenn Sie auf eine Linie zeigen.  Die grüne Anforderung ist der Initiator der Abhängigkeit.  Wenn zuvor eine weitere grüne Anforderung in der Zeile angezeigt wird, ist diese höhere Anforderung der Initiator des Initiators.  Und so weiter.  

### <a name="display-load-events"></a>Anzeigen von Lastereignissen  

DevTools zeigt das Timing der `DOMContentLoaded` Ereignisse und `load` an mehreren Stellen im **Netzwerktool** an.  Das `DOMContentLoaded` Ereignis ist blau gefärbt, und das Ereignis ist `load` rot.  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Die Speicherorte der DOMContentLoaded- und Load-Ereignisse im Netzwerkbereich" lightbox="../media/network-network-requests-load-events.msft.png":::
   Die Speicherorte und `DOMContentLoaded` `load` Ereignisse im **Netzwerktool**  
:::image-end:::  

### <a name="display-the-total-number-of-requests"></a>Anzeigen der Gesamtzahl der Anforderungen  

Die Gesamtanzahl der Anforderungen wird **** im Zusammenfassungsbereich unten im **Netzwerktool** aufgelistet.  

> [!CAUTION]
> Diese Zahl verfolgt nur Anforderungen, die seit dem Öffnen von DevTools protokolliert wurden.  Wenn vor dem Öffnen von DevTools andere Anforderungen aufgetreten sind, werden diese Anforderungen nicht gezählt.  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Die Gesamtzahl der Anforderungen seit dem Öffnen von DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   Die Gesamtzahl der Anforderungen seit dem Öffnen von DevTools  
:::image-end:::  

### <a name="display-the-total-download-size"></a>Anzeigen der Downloadgröße insgesamt  

Die Gesamtgröße der Downloads von **** Anforderungen wird im Zusammenfassungsbereich unten im **Netzwerktool** aufgeführt.  

> [!CAUTION]
> Diese Zahl verfolgt nur Anforderungen, die seit dem Öffnen von DevTools protokolliert wurden.  Wenn vor dem Öffnen von DevTools andere Anforderungen aufgetreten sind, werden die vorherigen Anforderungen nicht gezählt.  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Die Gesamtgröße der Downloads von Anforderungen" lightbox="../media/network-network-total-download-size.msft.png":::
   Die Gesamtgröße der Downloads von Anforderungen  
:::image-end:::  

Navigieren Sie, um zu überprüfen, wie groß ressourcen sind, nachdem der Browser die Komprimierung der einzelnen Elemente deaktiviert hat, um die nicht komprimierte Größe [einer Ressource anzuzeigen.](#display-the-uncompressed-size-of-a-resource)  

### <a name="display-the-stack-trace-that-caused-a-request"></a>Anzeigen der Stapelverfolgung, die eine Anforderung verursacht hat  

Nachdem eine JavaScript-Anweisung eine Ressource anfordert, zeigen Sie auf die **Spalte Initiator,** um die Stapelverfolgung zu zeigen, die zur Anforderung führt.  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Die Stapelverfolgung, die zu einer Ressourcenanforderung führt" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   Die Stapelverfolgung, die zu einer Ressourcenanforderung führt  
:::image-end:::  

### <a name="display-the-uncompressed-size-of-a-resource"></a>Anzeigen der unkomprimierten Größe einer Ressource  

Aktivieren Sie das **Kontrollkästchen Große Anforderungszeilen** verwenden, und überprüfen Sie dann den unteren Wert der **Spalte Größe.**  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Beispiel für nicht komprimierte Ressourcen" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   Ein Beispiel für nicht komprimierte Ressourcen \(Die komprimierte Größe der Datei, die über das Netzwerk gesendet wurde, war , während die nicht komprimierte `jquery-3.3.1.min.js` `29.9 KB` Größe `84.9 KB` \) war.  
:::image-end:::  

## <a name="export-requests-data"></a>Exportieren von Anforderungensdaten  

### <a name="save-all-network-requests-to-a-har-file"></a>Speichern aller Netzwerkanforderungen in einer HAR-Datei  

Führen Sie die folgenden Schritte aus, um alle Netzwerkanforderungen in einer HAR-Datei zu speichern.  

1.  Zeigen Sie auf eine beliebige Anforderung in der Tabelle Anforderungen, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).  
1.  Wählen **Sie Speichern als HAR mit Inhalt aus.**  DevTools speichert alle Anforderungen, die seit dem Öffnen von DevTools in der HAR-Datei aufgetreten sind.  Anforderungen können nicht gefiltert werden.  Sie können auch keine einzelne Anforderung speichern.  

Nachdem Sie eine HAR-Datei gespeichert haben, können Sie sie zur Analyse wieder in DevTools importieren.  Ziehen Sie einfach die HAR-Datei per Drag -and-Drop in die Requests-Tabelle.  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Wählen Sie Speichern als HAR mit Inhalt aus" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   Wählen **Sie Speichern als HAR mit Inhalt aus**  
:::image-end:::  

### <a name="copy-one-or-more-requests-to-the-clipboard"></a>Kopieren einer oder mehreren Anforderungen in die Zwischenablage  

Zeigen Sie in der Spalte **Name** der Tabelle Anforderungen auf eine Anforderung, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), zeigen Sie auf **Kopieren,** und wählen Sie eine der folgenden Optionen aus.  

| Name | Details |  
|:--- |:--- |  
| **Linkadresse kopieren** | Kopieren Sie die URL der Anforderung in die Zwischenablage. |  
| **Antwort kopieren** | Kopieren Sie den Antworttext in die Zwischenablage. |  
| **Kopieren als Abrufen** | &nbsp; |  
| **Kopieren als cURL** | Kopieren Sie die Anforderung als cURL-Befehl. |  
| **Copy All as Fetch** | &nbsp; |  
| **Copy All as cURL** | Kopieren Sie alle Anforderungen als Kette von cURL-Befehlen. |  
| **Copy All as HAR** | Kopieren Sie alle Anforderungen als HAR-Daten. |  

<!--
:::row:::
   :::column span="1":::
      **Copy Link Address**  
   :::column-end:::
   :::column span="2":::
      Copy the URL of the request to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy Response**  
   :::column-end:::
   :::column span="2":::
      Copy the response body to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy the request as a cURL command.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as a chain of cURL commands.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as HAR**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as HAR data.  
   :::column-end:::
:::row-end:::  
-->  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Wählen Sie Antwort kopieren aus" lightbox="../media/network-network-requests-copy-response.msft.png":::
   Wählen Sie **Antwort kopieren aus**  
:::image-end:::  

### <a name="copy-formatted-response-json-to-the-clipboard"></a>Formatierte Antwort-JSON in die Zwischenablage kopieren  

Wählen Sie eine Netzwerkanforderung aus, und navigieren Sie zum **Bereich Kopfzeilen.**  Navigieren Sie zum Kopieren des JSON-Werts einer Antwort zu Nutzlast **anfordern,** zeigen Sie auf den Inhalt der JSON-Antwort, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Wert kopieren aus.**  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Wert im Kontextmenü kopieren" lightbox="../media/network-header-copy-property-value.msft.png":::
          **Wert im** Kontextmenü kopieren  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Microsoft Visual Studio Code mit formatierter Antwort-JSON" lightbox="../media/network-header-paste-property-value.msft.png":::
          Pasting formatted response JSON in Microsoft Visual Studio Code  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="copy-property-values-from-network-requests-to-your-clipboard"></a>Kopieren von Eigenschaftswerten aus Netzwerkanforderungen in die Zwischenablage  

Führen Sie die folgenden Aktionen aus, um Eigenschaftswerte aus Netzwerkanforderungen in die Zwischenablage zu kopieren.  

1.  Öffnen Sie den **Bereich Kopfzeilen.**  
1.  Öffnen Sie einen der folgenden Kopfzeilenabschnitte.  
    *   Anforderungsnutzlast \(JSON\)  
    *   Formulardaten  
    *   Abfragezeichenfolgenparameter  
    *   Anforderungsheader  
    *   Antwortheader  
1.  Öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\) > **Wert kopieren**.  Sie können den Wert nun in einen beliebigen Editor einfügen, um ihn zu überprüfen.  
    
## <a name="change-the-layout-of-the-network-panel"></a>Ändern des Layouts des Netzwerkbereichs  

Sie können Abschnitte der **** Benutzeroberfläche des Netzwerktools erweitern oder reduzieren, um wichtige Informationen zu fokussieren.  

### <a name="hide-the-filters-pane"></a>Ausblenden des Bereichs Filter  

In DevTools wird standardmäßig der Bereich **Filter** angezeigt.  
Wählen **Sie Filter** \( Filter ![ ](../media/filter-icon.msft.png) \) aus, um ihn auszublenden.  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Schaltfläche Filter ausblenden" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   Schaltfläche Filter ausblenden  
:::image-end:::  

### <a name="use-large-request-rows"></a>Verwenden großer Anforderungszeilen  

Verwenden Sie große Zeilen, wenn Sie mehr Leerzeichen in ihrer Netzwerkanforderungentabelle wünschen.  Einige Spalten bieten auch ein wenig mehr Informationen, wenn große Zeilen verwendet werden.  Der untere Wert der Spalte **Größe** ist beispielsweise die nicht komprimierte Größe einer Anforderung.  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Ein Beispiel für große Anforderungszeilen im Bereich Anforderungen" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   Ein Beispiel für große Anforderungszeilen im **Bereich Anforderungen**  
:::image-end:::  

Aktivieren Sie zum Aktivieren großer Zeilen das Kontrollkästchen **Große Anforderungszeilen** verwenden.  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Das Kontrollkästchen Große Anforderungszeilen verwenden" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   Das **Kontrollkästchen Große Anforderungszeilen** verwenden  
:::image-end:::  

### <a name="hide-the-overview-pane"></a>Ausblenden des Übersichtsbereichs  

Standardmäßig zeigt DevTools den Bereich **Übersicht** an.  Deaktivieren Sie zum Ausblenden das Kontrollkästchen **Übersicht** anzeigen.  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Das Kontrollkästchen Übersicht anzeigen" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   Das **Kontrollkästchen Übersicht** anzeigen  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Debuggen von Progressive Web Apps | Microsoft Docs"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Daten-URLs | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Proxyserver – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

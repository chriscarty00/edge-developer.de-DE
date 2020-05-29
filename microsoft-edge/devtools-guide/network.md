---
description: Verwenden des Netzwerk Panels zum Überwachen und Anzeigen von Seitenressourcen Anforderungen
title: DevTools-Netzwerk
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Netzwerk, Ladezeit, http, HTTPS, Browser-Cache, har
ms.custom: seodec18
ms.openlocfilehash: 0b190f5163f9b7a9f9920877a94577177053e4f6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567597"
---
# Netzwerk

Verwenden Sie das **Netzwerk** Panel, um die über den Draht gesendeten Anfragen und Antworten zu überwachen, zu überprüfen und zu profilieren. Damit haben Sie folgende Möglichkeiten:

 - Durch [Suchen eines Datensatzes aller Ressourcenanforderungen](#network-summary) , die von der Seite vorgenommen wurden
 - [Messen der Ladezeit Ihrer Website](#summary-bar) für neue und wiederkehrende Benutzer 
 - Über [Prüfen der Überschriften, Nachrichtentexte, Parameter und Cookies](#request-details) , die zwischen Ihrer Seite und dem Netzwerk ausgetauscht wurden
 - [Ermitteln der Netzwerkereignisse](#timings) , die zu Engpässen beim Laden der Website führen

![Das Microsoft Edge devtools-Netzwerk Panel](./media/network.png)

## Netzwerk Zusammenfassung

Wenn Sie devtools öffnen, ist die Netzwerkprofil Erstellung standardmäßig aktiviert. Der gesamte Netzwerkdatenverkehr von der Registerkarte "aktiver Browser" wird in der Liste "Netzwerk Zusammenfassung" aufgezeichnet, auch wenn Sie in einem anderen devtools als dem *Netzwerk*arbeiten.

![In-Progress-Netzwerkprofil Erstellungs Indikator](./media/network_profile_indicator.png)

### Symbolleiste

Die Symbolleiste bietet Steuerelemente zum profilieren und Filtern der Netzwerkaktivität Ihrer Seite. 

![Netzwerk Profiler-Symbolleiste](./media/network_toolbar.png)

1. **Starten/Beenden der Profilerstellungssitzung**: Standardmäßig ist die Netzwerkprofil Erstellung aktiviert, und der Netzwerkdatenverkehr wird in der Liste " [**Netzwerk Profiler**](#network-request-list) " protokolliert. Mit der Schaltfläche **Stopp** () können Sie die Netzwerkaufzeichnung deaktivieren `Ctrl+E` .

2. **Als har exportieren**: Sie können die aktuelle Netzwerkprofil Erstellungs Sitzung ( `Ctrl+S` ) als JSON-formatierte [http-Archivdatei (har)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) speichern. 

3. **Inhaltstyp Filter**: Filtern Sie die Liste der Netzwerkanforderungen nach bestimmten Inhaltsanforderungen (*Dokumente, Stylesheets, Bilder, Skripts, Medien, Schriftarten, XMLHttpRequest usw*.). Standardmäßig werden alle Inhaltstypen angezeigt.

4. **Suchen**: Filtern ( `Ctrl+F` ) Sie die Netzwerk Anforderungsliste nach Eintragsnamen (Ressourcenpfade), die eine angegebene Suchzeichenfolge enthalten.

5. **Immer vom Server aktualisieren**: Wenn Sie diese Schaltfläche drücken, wird das Laden von Seitenressourcen aus dem Netzwerk und nicht vom Browsercache erzwungen. Sie können die Seite aus dem Netzwerk ein einziges Mal aktualisieren, indem Sie auf klicken `Ctrl+F5` .

6. **Bypass Service Worker für alle Netzwerkanforderungen**: Deaktivieren Sie Ihre registrierten Servicemitarbeiter als Netzwerk Proxys. 

7. Schaltflächen Löschen

   - **Cache löschen**: entfernt alle im Browsercache gespeicherten Ressourcen (und emuliert eine erstmalige Benutzeroberfläche beim Laden der Seite).
   - **Cookies löschen**: entfernt alle Cookies für die angegebene Domäne (und emuliert eine erstmalige Nutzung der Website).
   - **Einträge beim Navigieren löschen: der**aufgezeichnete Datenverkehr wird bei der Seitennavigation gelöscht. Dies ist standardmäßig aktiviert.
   - **Sitzung löschen**: Löscht alle Netzwerk Anforderungs Einträge aus der **Netzwerk Zusammenfassungs** Liste.

### Liste der Netzwerkanforderungen

Der gesamte Netzwerkdatenverkehr wird in einer Liste aufgezeichnet (bis zum Zeitpunkt der Navigation, manuelles Löschen oder devtools geschlossen). Wenn Sie auf einen Eintrag klicken, wird eine [detailliertere Ansicht der Anfrage](#request-details)geöffnet.

![Liste der Netzwerkanforderungen](./media/network_request_list.png)

Die Netzwerk Anforderungsliste enthält die folgenden Informationen: 

Spalte | Beschreibung 
:------------ | :------------- 
**Name** | Name und URL-Pfad der Anforderung
**Protokoll** |  Der Typ des Protokolls für die Anforderung (wie *https; HTTP/2*)
**Methode** |    Für die Anforderung verwendete [http-Methode](https://developer.mozilla.org/docs/Web/HTTP/Methods)
**Ergebnis** |    [HTTP-Antwortstatus](https://developer.mozilla.org/docs/Web/HTTP/Status) Code
**Inhaltstyp** |  Art des angeforderten Mediums ([MIME-Typ](https://en.wikipedia.org/wiki/Media_type))
**Empfangen** | Die Größe der Antwort, wie Sie vom Server bereitgestellt wurde (wird nicht für zwischengespeicherte Antworten berechnet)
**Zeit** |  Zeit zum Laden der Serverantwort (nicht für zwischengespeicherte Antworten berechnet)
**Initiator** | Subsystem, das für das Initiieren der Anforderung verantwortlich ist (wie *Parser, Redirect, Skript usw*.)
**Zeitachse** | Visuelle Zeitachse für die Netzwerkereignisse der Anforderung (wie *verzögert, auflösen (DNS), verbinden (TCP), SSL, senden, warten (TTFB), herunterladen*). Wenn Sie den Mauszeiger über das Diagramm bewegen, erhalten Sie eine genauere Unterbrechung der Netzwerk [Anzeige](#timings)dauern.

### Zusammenfassungs Leiste

Die Leiste am unteren Rand des **Netzwerk** Panels fasst die Gesamtzahl der HTTP-Netzwerkfehler,-Anforderungen,-Datenübertragungen und-Ladezeiten während der Netzwerkprofil Erstellungs Sitzung zusammen (d. h., seit devtools geöffnet wurden und den Netzwerkdatenverkehr aufzeichnen).

![Netzwerk Zusammenfassungs Leiste](./media/network_summary_bar.png)

**Verstrichene Zeit** bedeutet die Zeit zwischen dem Start der Profilerstellungssitzung und dem Zeitpunkt, zu dem die letzte Ressource aus dem Netzwerk heruntergeladen wurde. Ressourcen, die aus dem Browser-Cache abgerufen werden, werden dieser Nummer nicht Zeit gutgeschrieben. 

**DOM Load Time** bezeichnet die Zeit zwischen dem Beginn der Profilerstellungssitzung und dem Zeitpunkt, zu dem das [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) -Ereignis ausgelöst wurde, um anzugeben, dass die Struktur des Seitendokuments geladen und analysiert wurde (aber nicht unbedingt alle Stylesheets, Bilder oder unter Frames).

**"Seitenladezeit"** bedeutet die Zeit zwischen dem Start der Profilerstellungssitzung und dem Zeitpunkt, zu dem das [Load](https://developer.mozilla.org/docs/Web/Events/load) -Ereignis ausgelöst wurde, um anzugeben, dass das Seiten Dokument (und alle zugehörigen Ressourcen) vollständig geladen wurde.

## Details anfordern

Wenn Sie auf einen Eintrag in der [**Netzwerk Zusammenfassungs**](#network-summary) Liste klicken, wird der Bereich [**Anforderungsdetails**](#request-details) mit weiteren Informationen auf den folgenden Registerkarten geöffnet.

![Bereich ' Netzwerk Anforderungsdetails '](./media/network_request_details.png)

### Header
Zeigt die [http-Header](https://developer.mozilla.org/docs/Web/HTTP/Headers) an, die vom Server gesendet und empfangen wurden. Klicken Sie mit der rechten Maustaste auf einen beliebigen kopfzeileneintrag, um ihn ( `Ctrl+C` ) in die Zwischenablage zu kopieren. Sie können auch eine Mehrfachauswahl von Einträgen durchführen, indem Sie die Taste gedrückt halten `Shift` oder alle auswählen ( `Ctrl+A` ).

### Textkörper
Zeigt die Textkörper Daten (sofern verfügbar) der Anforderungs-und Antwort Nutzlast an.

Bildinhalte werden mit Bemaßungen und Größendaten angezeigt.

Text Inhalte werden in einem (schreibgeschützten) Editor mit Optionen zum Formatieren von minimierte-Inhalten mit **Pretty Print** und/oder **Word Wrap** angezeigt, um die Lesbarkeit zu verbessern.

![Registerkarte "Text" im Bereich "Anforderungsdetails"](./media/network_details_body.png)

### Parameter
Zeigt Abfragezeichenfolgenparameter für Get-Anforderungen an. Während die Parameter von Post-Anforderungen in den Kopfzeilen gesendet werden, werden Sie von Get-Anforderungen in die URL eingefügt. Sie sind hier ausgebrochen, um einfacher zu lesen.

Klicken Sie mit der rechten Maustaste auf eine beliebige Zeile, um Sie ( `Ctrl+C` ) in die Zwischenablage zu kopieren. Sie können auch eine Mehrfachauswahl von Einträgen durchführen, indem Sie die Taste gedrückt halten `Shift` oder alle auswählen ( `Ctrl+A` ).

### Cookies
Zeigt Cookies an, die als Schlüssel-Wert-Paare gesendet oder empfangen werden.

Klicken Sie mit der rechten Maustaste auf eine beliebige Zeile, um Sie ( `Ctrl+C` ) in die Zwischenablage zu kopieren. Sie können auch eine Mehrfachauswahl von Einträgen durchführen, indem Sie die Taste gedrückt halten `Shift` oder alle auswählen ( `Ctrl+A` ).

Sie können die gespeicherten Cookies für die angegebene Domäne über die [Symbolleiste](#network-summary) löschen (Schaltfläche "**Cookies löschen** "). 

### Timings

Die Registerkarte **Anzeige** Dauer enthält eine Zeitachse mit Netzwerkereignissen, die am Laden der ausgewählten Ressource beteiligt sind. Dies ähnelt den Informationen, die in der Spalte " *Zeitachse* " der [Netzwerk Anforderungsliste](#network-request-list)enthalten sind, enthält aber auch die Ereignisse, die zu der Anforderung führen, die über den Draht gesendet wird*Stalled*, wie etwa die Wartezeit in der Anforderungswarteschlange, die DNS-Auflösung und das Einrichten der TCP-Verbindung. 

![Registerkarte "Anzeigedauern" im Bereich "Anforderungsdetails"](./media/network_details_timings.png)

Umleitungen zu/von anderen Ressourcen werden notiert, und durch Klicken auf den Link wird der Fokus auf diese Ressource im Bereich Netzwerk [Anforderungsdetails](#request details) gesetzt.

Resouces, die aus dem Cache geladen werden, sind von der Netzwerklatenz nicht betroffen, daher wird *kein Diagramm für Netzwerk Anzeigedauern* angezeigt.

![Umgeleitete Ressource, die aus dem Cache geladen wurde](./media/network_details_timings_cache_redirect.png)

Hier sind die verschiedenen Netzwerkereignisse, die für eine bestimmte Ressource möglicherweise in chronologischer Reihenfolge angezeigt werden:

#### Blockiert

Zeit, die auf eine verfügbare Netzwerkverbindung in der Anforderungswarteschlange wartet. Für HTTP 1.0/1.1 ermöglicht Microsoft Edge maximal sechs (6) gleichzeitige TCP-Verbindungen pro Hostname. 

#### Auflösen (DNS)

Zeit, die die IP-Adresse für den Hostnamen der Ressource im DNS ([Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System)) nachschlagen soll.

#### Verbinden (TCP)

Zeit, die für das Einrichten der TCP-Verbindung ([Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)) aufgewendet wurde.

#### SSL

Zeit, die für die Aushandlung einer SSL-Verbindung ([Secure Sockets Layer](https://en.wikipedia.org/wiki/Transport_Layer_Security)) mit dem [Proxy Server](https://en.wikipedia.org/wiki/Proxy_server) für den Host aufgewendet wurde.

#### Senden

Der Zeitaufwand für das Senden der Ressourcenanforderung.

#### Warten (TTFB)

Die Wartezeit für das erste Byte der Antwort vom Hostserver ("Time to First Byte" oder *TTFB*).

#### Herunterladen

Die Zeit, die beim Lesen der Antwort vom Server aufgewendet wurde.

## Kombinationen

| Aktion                         | Tastenkombination     |
|:-------------------------------|:-------------|
| Starten/Beenden der Profilerstellungssitzung | `Ctrl` + `E` |
| Als har exportieren                  | `Ctrl` + `S` |
| Suchen                           | `Ctrl` + `F` |
| Kopieren                           | `Ctrl` + `C` |

## Bekannte Probleme

### Der Netzwerk Sammlungs-Agent konnte nicht gestartet werden.

Wenn diese Fehlermeldung angezeigt wird: Fehler beim **Starten des Netzwerk Sammlungs-Agents** im Netzwerktool, führen Sie die folgenden Schritte aus, um eine Problemumgehung zu erhalten.

1. Drücken Sie `Windows Key`  +  `R` .

2. Geben Sie im Dialogfeld Ausführen den **Dienst "Services. msc**" ein.
![Bekannte Probleme-1](./media/known_issues_1.PNG)

3. Suchen Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst** , und klicken Sie mit der rechten Maustaste darauf.
![Bekannte Probleme-2](./media/known_issues_2.PNG)

4. Starten Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst**erneut.
![Bekannte Probleme-3](./media/known_issues_3.PNG)

5. Schließen Sie die Microsoft Edge-Entwickler Tools und die Registerkarte. Öffnen Sie eine neue Registerkarte, navigieren Sie zu Ihrer Seite, und drücken Sie `F12` .

6. Neben **Netzwerk** und Netzwerkanforderungen für Ihre Webseite sollte nun ein Play-Signal angezeigt werden.
![Bekannte Probleme-4](./media/known_issues_4-network.PNG)

Gibt es immer noch Probleme? Senden Sie uns Ihr Feedback über das Symbol **Feedback senden** ! 

![Bekannte Probleme-5](./media/known_issues_5.PNG)

### Fehler beim Beenden des Netzwerk Sammlungs-Agents.

Wenn diese Fehlermeldung angezeigt wird: Fehler beim **Beenden des Netzwerk Sammlungs-Agents** im Netzwerktool, führen Sie die folgenden Schritte aus, um eine Problemumgehung zu erhalten.

1. Drücken Sie `Windows Key`  +  `R` .

2. Geben Sie im Dialogfeld Ausführen den **Dienst "Services. msc**" ein.
![Bekannte Probleme-1](./media/known_issues_1.PNG)

3. Suchen Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst** , und klicken Sie mit der rechten Maustaste darauf.
![Bekannte Probleme-2](./media/known_issues_2.PNG)

4. Starten Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst**erneut.
![Bekannte Probleme-3](./media/known_issues_3.PNG)

5. Schließen Sie die Microsoft Edge-Entwickler Tools und die Registerkarte. Öffnen Sie eine neue Registerkarte, navigieren Sie zu Ihrer Seite, und drücken Sie `F12` .

6. Neben **Netzwerk** und Netzwerkanforderungen für Ihre Webseite sollte nun ein Play-Signal angezeigt werden.
![Bekannte Probleme-4](./media/known_issues_4-network.PNG)

Gibt es immer noch Probleme? Senden Sie uns Ihr Feedback über das Symbol **Feedback senden** ! 

![Bekannte Probleme-5](./media/known_issues_5.PNG)

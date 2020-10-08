---
description: Verwenden des Leistungs Panels zum Analysieren der responsivenes Ihrer Seite während der Benutzerinteraktion
title: DevTools-Leistung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Leistung, Profil, Framerate, FPS, CPU-Auslastung, JavaScript-Ausführung
ms.custom: seodec18
ms.openlocfilehash: aecf3cf49592dbf1f24231e76f14ddc2ca1228c3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567609"
---
# Leistung

Der **Leistungs** Panel bietet Tools für die Profilerstellung und Analyse der Reaktionsfähigkeit der Benutzeroberfläche im Verlauf der Benutzerinteraktion. Damit haben Sie folgende Möglichkeiten:

 - [Messen der Ausführungszeiten](#recording-a-profile) der verschiedenen Komponenten Ihrer Seite 
 - Führen Sie einen Drilldown zu dem Ort durch, an [dem Sie die meisten CPU-Zyklen](#timeline-ruler) für Ihre Seite und die resultierende visuelle Wirkung für Ihre Benutzer ausgeben.
 - [Abrufen einer schrittweisen Aufschlüsselung der Prozesse, die die](#timeline-details) Ausführungszeit der Seite verbrauchen 
 - Führen [Sie Ihre JavaScript-Anruflisten](#javascript-call-stacks) durch, um kostspielige Vorgänge zu identifizieren, beispielsweise für solche, die eine Neuberechnung des Layouts erfordern. 

![DevTools-Leistungs Leiste](./media/performance.png)

## Aufzeichnen eines Profils

Der erste Schritt zur Analyse der Leistung Ihrer Seite besteht darin, ein Profil zu erfassen, während Sie ein bestimmtes Benutzerszenario durchführen, beispielsweise die Repro Schritte eines Leistungs Fehlers, den Sie beheben möchten, oder einen typischen Anwendungsfall, den Sie für eine bessere Benutzererfahrung optimieren möchten. 

### Symbolleiste

Verwenden Sie **Start**die  /  Schaltflächen für Start**Stopp** auf der Symbolleiste (oder `Ctrl+E` ), um die Leistungsablaufverfolgung zu initiieren und abzuschließen. Auf der Registerkarte **Leistung** wird eine grüne Anzeige apear, um anzugeben, dass eine Aufzeichnung gerade ausgeführt wird. 

![Symbolleiste des Leistungs Fensters](./media/performance_toolbar.png)

Beim Beenden des Profils wird ein Leistungsbericht generiert. Sie können festlegen, dass die Datei zu einem späteren Zeitpunkt auf dem Datenträger ( `Ctrl+S` ) und Reload ( `Ctrl+O` ) in devtools gespeichert werden soll.  DevTools-Diagnose Sitzungen werden mit der Erweiterung *. diagsession* gespeichert.

Hier sind einige Punkte, die Sie beim Aufzeichnen eines Profils beachten sollten:

- Führen Sie die wenigsten Aktionen aus, die Sie zum Erfassen des Szenarios benötigen, das Sie analysieren möchten. Durch überflüssige Aktionen mit der Seite werden zusätzliche Daten erzeugt und ihre Ergebnisse überladen.

- Der Profiler kennzeichnet wichtige App-Lebenszyklusereignisse im Bericht automatisch, beispielsweise Seitennavigation, [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded)und Seiten [Ladevorgang](https://developer.mozilla.org/docs/Web/Events/load). Sie können benutzerdefinierte Marker hinzufügen, indem Sie die [Performance. Mark ()](https://developer.mozilla.org/docs/Web/API/Performance/mark) -Methode im Code oder in der Konsole aufrufen. 

- Wenn für Ihre Analyse anfängliche Seitenladezeiten wichtig sind, stellen Sie sicher, dass Sie den Browsercache (aus dem [Netzwerk](./network.md) Fenster) löschen, um sicherzustellen, dass alle Seitenressourcen aus dem Netzwerk geladen werden.

- Manchmal hilft es, mehrere Sitzungen aufzuzeichnen und/oder das gleiche Szenario auf verschiedenen Computern zu testen, um das Leistungsproblem in der Wildnis besser zu verstehen.

## Zeitachsenlineal

Die Zeitachse funktioniert als Schiebe Lineal. Verwenden Sie es, um den Umfang des Berichts auf den jeweiligen Zeitrahmen (oder die Spanne von Ereignissen) zu begrenzen, die von Interesse sind. Ziehen Sie die schwarzen **Schiebe** Regler, um den Zeitbereich zu begrenzen, den Sie untersuchen möchten, und Filtern Sie externe Profilerstellungsdaten aus der [Zeitachse](#timeline-details) und den [JavaScript-Aufruflisten](#javascript-call-stacks) Berichten im unteren *Detailbereich*. 

Auf dem Lineal werden zwei Arten von Markierungen angezeigt:

 - **App-Lebenszyklus Markierungen** auf der Zeitachse (wie Seitennavigation, [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded)und Seiten [Laden](https://developer.mozilla.org/docs/Web/Events/load)) werden automatisch protokolliert, während Sie ein Profil aufzeichnen.

 - **Benutzer Marken** sind benutzerdefinierte Marker, die Sie mit Aufrufen der [Performance. Mark ()](https://developer.mozilla.org/docs/Web/API/Performance/mark) -Methode im Code oder in der devtools- [**Konsole**](./console.md)hinzufügen können. Sie können *Start* -und *endmarks* zusammen als einzelnes, benanntes Measure mit der [Performance. Measure ()](https://developer.mozilla.org/docs/Web/API/Performance/measure) -Methode gruppieren. 

Nachdem Sie einen Zeitbereich ausgewählt haben, können Sie von der Symbolleiste weiter **vergrößern** oder **Zoom zurücksetzen** und **Auswahl löschen** , um zur vollständigen Ansicht der Leistungsablaufverfolgung zurückzukehren (ohne Zeitbereich ausgewählt). Diese Steuerelemente sind auch über das Kontextmenü der rechten Maustaste verfügbar.

![Leistungsbereich-Zeitachse](./media/performance_timeline.png)

### CPU-Auslastung

Das Diagramm **CPU-Auslastung%** Zeitachsen beschreibt die Verarbeitungsressourcen, die von den verschiedenen für die Ausführung der Seite erforderlichen Browser-Subsysteme verwendet werden, aufgeschlüsselt nach Kategorie:

#### Laden
Zeigt die Zeit an, die zum Abrufen von App-Ressourcen und zum Analysieren von HTML und CSS verwendet wurde. Dies kann Netzwerkanforderungen umfassen. Die folgenden zugehörigen Ereignisse werden in der [Zeitachse](#timeline-details)protokolliert:

Ereignis | Beschreibung
:------------ | :-------------
CssParsing  | Es wurde ein neuer CSS-Inhalt gefunden, der analysiert werden musste.
HtmlParsing | Es wurde ein neuer HTML-Inhalt gefunden, der in Knoten analysiert und in das DOM eingefügt werden musste.
HttpRequest | Es wurde eine Remoteressource im Dom gefunden, oder es wurde ein XMLHttpRequest-Objekt erstellt, für das eine HTTP-Anforderung ausgeführt werden musste.
HtmlSpeculativeDownloading | Der HTML-Inhalt der Seite wurde nach erforderlichen Ressourcen durchsucht, damit die HTTP-Anforderungen für Sie so schnell wie möglich geplant werden können.


#### Skripting
Zeigt die Zeit an, die für die Analyse und Ausführung von JavaScript verwendet wurde Dazu gehören DOM-Ereignisse, Timer, Skript Auswertung und Animationsframe Rückrufe. Die folgenden zugehörigen Ereignisse werden in der [Zeitachse](#timeline-details)protokolliert:

Ereignis | Beschreibung
:------------ | :-------------
DomEvent | Ein Ereignis wurde für ein DOM-Objekt ausgelöst.
EvaluatingScript | `<script>`Es wurde ein neues Element im Dom gefunden, das analysiert und ausgeführt werden musste.
EventHandler | Ein registrierter Ereignislistener wurde als Reaktion auf ein ausgelöstes DOM-Ereignis ausgelöst.
Frame | Während ein neuer Frame vorbereitet wurde, wurde ein registrierter Rückruf ausgelöst, um visuelle Änderungen zu unterstützen.
Messen | Ein App-spezifisches Szenario wurde mit der `performance.measure()` Methode gemessen.
MediaQueryListener | Eine registrierte medienabfrage wurde ungültig, was zur Ausführung der zugehörigen Listener (s) führte.
MutationObserver | Mindestens ein beobachtetes DOM-Element wurde geändert, was zur Ausführung des zugehörigen Rückrufs eines MutationObserver führte.
TimerFired | Es wurde ein geplanter Zeitgeber verstrichen, der zur Ausführung des zugehörigen Rückrufs führte.
WindowsRuntimeAsyncCallback | Ein asynchroner Vorgang wurde von einem Windows-Runtime-Objekt abgeschlossen, das einen Rückruf ausgelöst hat `Promise` .
WindowsRuntimeEvent | Ein Ereignis wurde für ein Windows-Runtime-Objekt ausgelöst, das einen registrierten Listener ausgelöst hat.

#### GC
Gibt an, dass Zeit für das Sammeln von Speicher für nicht mehr verwendete Objekte aufgewendet wird. Die folgenden zugehörigen Ereignisse werden in der [Zeitachse](#timeline-details)protokolliert:

Ereignis | Beschreibung
:------------ | :-------------
GarbageCollection | Die JavaScript-Laufzeit hat die aktuelle Speicherauslastung der APP überwacht, um festzustellen, welche Objekte nicht mehr referenziert werden und daher gesammelt werden können.

#### Formatieren
Zeigt die Zeit an, die für die Berechnung der Element Präsentation und des Layouts verwendet Die folgenden zugehörigen Ereignisse werden in der [Zeitachse](#timeline-details)protokolliert:

Ereignis | Beschreibung
:------------ | :-------------
AlignedBeat | Ausstehende visuelle Änderungen, die am Dom vorgenommen wurden, wurden verarbeitet, sodass die Anzeige der APP aktualisiert werden konnte.
CssCalculation | Änderungen an der Dom-oder neuen CSS-Inhalte wurden hinzugefügt, sodass die Formateigenschaften aller betroffenen Elemente neu berechnet werden müssen.
Layout | Am Dom wurden Änderungen vorgenommen, bei denen die Größe und/oder Position aller betroffenen Elemente berechnet werden musste.

#### Rendern
Zeigt die Zeit an, die beim Malen des Bildschirms ausgegeben wurde. Die folgenden zugehörigen Ereignisse werden in der [Zeitachse](#timeline-details)protokolliert:

Ereignis | Beschreibung
:------------ | :-------------
Paint | Visuelle Änderungen wurden am Dom vorgenommen, bei denen alle betroffenen Teile der Seite neu gezeichnet werden mussten.
RenderLayer | Visuelle Änderungen wurden an einem unabhängig gerenderten Fragment des DOM (ein Layer genannt) vorgenommen, in dem der jeweilige Teil der Seite neu gezeichnet werden musste.

#### Bild Decodierung
Zeigt die Zeit an, die zum Dekomprimieren und Decodieren von Bildern verwendet wurde. Die folgenden zugehörigen Ereignisse werden in der [Zeitachse](#timeline-details)protokolliert:

Ereignis | Beschreibung
:------------ | :-------------
Decodiert | Ein Bild wurde in das DOM aufgenommen und musste vom ursprünglichen Format in eine Bitmap dekomprimiert werden.

### Visueller Durchsatz

Der **visuelle Durchsatz (fps)** zeigt die geschätzten *Bilder pro Sekunde* (fps) im Verlauf des Profilerstellungs-Szenarios, wobei 60 fps die ideale Anzeigerate darstellt. Dips in der Framerate deuten auf Leistungsengpässe hin, und eine Frame Rate von NULL bedeutet, dass Frames vollständig gelöscht werden.

## Zeitachsen Details

Verwenden Sie den untersten-Detailbereich, um die vollständige Aufschlüsselung der Geschehnisse auf der Seite zu erhalten. Auf der Registerkarte **Details** finden Sie eine Aufschlüsselung der Ereignisse, die in den verschiedenen Browser-Subsysteme aufgetreten sind.

![Detailbereich der Leistungs Zeitachse](./media/performance_details_timeline.png)

1. **Sortierungssteuerelement für Ereignislisten**

    Verwenden Sie das Dropdown-Steuerelement **Sortieren** nach, um die Reihenfolge der [Ereignislisten](#event-list) zwischen *Startzeit* oder *Dauer (einschließlich*) umzuschalten. Dadurch wird auch die Ansicht der [ausgewählten Zeitachsen Details](#selected-timeline-details)geändert.

2. **Gruppieren von Ereignissen nach Frame**

    Verwenden Sie die **Gruppen Ereignisse auf oberster Ebene nach Frames** umschalten, um Ereignisse der obersten Ebene (*HTML-Analyse, Layout, DOM-Ereignis* usw.) in der entsprechenden Arbeitseinheit (oder "Frame") in Zeiträumen zu gruppieren, in denen Animationen/visuelle Aktualisierungen stattgefunden haben. Die Frames werden wie andere Ereignisse behandelt, sodass Sie sortiert/gefiltert werden können und eine *inklusive Zeit* Zusammenfassung bereitstellen, wenn in der [Ereignisliste](#event-list)darauf geklickt wird.

3. **Filtersteuerelemente für Ereignislisten**

    Verwenden Sie das Menü **Ereignisse filtern** , um die Typen von Ereignissen zu konfigurieren, die in den [Zeitachsen Details](#timeline-details)angezeigt werden. 

    ![Steuerelement zum Filtern von Leistungs Ereignissen](./media/performance_filter_events.png) 

    Die folgenden Filter stehen zur Verfügung:

   - **Bild Decodierung**: zeigt Ereignisse an, die in einem Hintergrundthread aufgetreten sind (beispielsweise Bild Decodierung, GC). 
   - **Netzwerkdatenverkehr**: zeigt HTTP-Anforderungen an, die Netzwerk gebunden sind.
   - **UI-Aktivität**: zeigt Ereignisse an, die im UI-Thread und/oder Render-Thread aufgetreten sind (beispielsweise DOM-Ereignishandler, Layout).
   - **Benutzer Measures**: zeigen Sie benutzerdefinierte Ereignisse an, die auf Aufrufe der Performance. Measure ()-Methode hinweisen.

     Sie können Ereignisse auf oberster Ebene weiter nach deren inklusiver Dauer filtern.

### Ereignisliste

Die *Ereignisliste* enthält eine chronologische Liste der [Ereignisse des Browser-Subsystems](#cpu-utilization) , die während der ausgewählten Zeitspanne aufgetreten sind. 

Klicken Sie auf einen beliebigen Eintrag, um das **ausgewählte Ereignisdetail** Diagramm für dieses Element aufzufüllen. Einträge mit geschachtelten Ereignissen/Funktionen zeigen ihre **inklusiven** (Zeit, die die Ausführung der Funktion *und* alle anderen Funktionen, die Sie aufgerufen hat) und **Exclusive** (Zeit, die nur innerhalb des Texts der aufrufenden Funktion selbst verbracht wurde) Zeiten, die im Diagramm angezeigt werden.

Klicken Sie mit der rechten Maustaste auf einen beliebigen Eintrag, um das Kontextmenü zu öffnen, um die Zeitachse auf dieses Ereignis zu filtern, und zeigen Sie den für [**Elements**](./elements.md) das Ereignis Verantwortlichen Quellcode im [**Debugger**](./debugger.md) an (falls zutreffend).

### Ausgewählte Zeitachsen Details

Die *Details der ausgewählten Zeitachse* enthalten eine detaillierte Balkengrafik der inklusiven/exklusiven Veranstaltungszeiten während der ausgewählten Zeitspanne. Wenn Sie nach *Dauer (einschließlich)* mithilfe des **Ereignislisten-Sortier Steuerelements**sortieren, werden die am längsten ausgeführten Ereignisse in diesem Diagramm visuell hervorgehoben. 

### Ausgewählte Ereignisdetails

Dieser Bericht enthält weitere Informationen zu dem ausgewählten Ereignis, einschließlich *Startzeit*, dem ausgeführten Threadtyp (beispielsweise *Download*, *UI*, *Render*) und anderen kontextbezogenen Details, die für den jeweiligen Ereignistyp spezifisch sind. *Ereignislistener* -Typen bieten beispielsweise Debugger-Links zur *Rückruffunktion* und zur *Terminplan Aufrufliste*.

## JavaScript-Anruflisten

![Leistungsanzeige dauern für JavaScript-Anruflisten](./media/performance_details_javascript.png)

Die Registerkarte " **JavaScript-Anruflisten** " bietet Informationen zur CPU-Nutzung und die Anzeigedauer für die Skriptfunktionen, die während des ausgewählten Zeitbereichs ausgeführt wurden:

 Spalte | Beschreibung
:------------ | :-------------
Funktionsname | Name des Browsers oder benutzerdefinierte Funktion.
Inklusive CPU (%) | Prozentsatz der ausgewählten CPU-Aktivität in dieser Funktion und in Funktionen, die von dieser Funktion aufgerufen werden.
Exklusive CPU (%) | Prozentsatz der ausgewählten CPU-Aktivität in dieser Funktion, ohne Aktivität in Funktionen, die von dieser Funktion aufgerufen werden.
Inklusive CPU (MS) | CPU-Zeit für die Ausführung von Code in dieser Funktion und in Funktionen, die von dieser Funktion aufgerufen werden.
Exklusive CPU (MS) | CPU-Zeit für die Ausführung von Code in dieser Funktion, mit Ausnahme der Zeit in Funktionen, die von dieser Funktion aufgerufen werden.
URL | URL (s), in dem Stapelrahmen aufgetreten ist. Funktionsaufrufe, die vom Browser (auf Standards basierende Web-APIs) stammen, werden als *[DOM]* bezeichnet.

## Verknüpfungen

| Aktion                         | Tastenkombination     |
|:-------------------------------|:-------------|
| Starten/Beenden der Profilerstellungssitzung | `Ctrl` + `E` |
| Profilerstellungssitzung importieren       | `Ctrl` + `O` |
| Profilerstellungssitzung exportieren       | `Ctrl` + `S` |

## Bekannte Probleme

### Beim Starten der Profilerstellungssitzung ist ein Fehler aufgetreten.

Wenn diese Fehlermeldung angezeigt wird: **beim Starten der Profilerstellungssitzung im Leistungstool ist ein Fehler aufgetreten** , führen Sie die folgenden Schritte aus, um eine Problemumgehung zu erhalten.

1. Drücken Sie `Windows Key`  +  `R` .

2. Geben Sie im Dialogfeld Ausführen den **Dienst "Services. msc**" ein.
![Bekannte Probleme-1](./media/known_issues_1.PNG)

3. Suchen Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst** , und klicken Sie mit der rechten Maustaste darauf.
![Bekannte Probleme-2](./media/known_issues_2.PNG)

4. Starten Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst**erneut.
![Bekannte Probleme-3](./media/known_issues_3.PNG)

5. Schließen Sie die Microsoft Edge-Entwickler Tools und die Registerkarte. Öffnen Sie eine neue Registerkarte, navigieren Sie zu Ihrer Seite, und drücken Sie `F12` .

6. Sie sollten jetzt in der Lage sein, mit der Profilerstellung zu beginnen.
![Bekannte Probleme-4](./media/known_issues_4-performance.PNG)

Gibt es immer noch Probleme? Senden Sie uns Ihr Feedback über das Symbol **Feedback senden** ! 

![Bekannte Probleme-5](./media/known_issues_5.PNG)

### Beim Beenden der Profilerstellungssitzung ist ein Fehler aufgetreten.

Wenn diese Fehlermeldung angezeigt wird: **beim Beenden der Profilerstellungssitzung im Leistungstool ist ein Fehler aufgetreten** , führen Sie die folgenden Schritte aus, um eine Problemumgehung zu erhalten.

1. Drücken Sie `Windows Key`  +  `R` .

2. Geben Sie im Dialogfeld Ausführen den **Dienst "Services. msc**" ein.
![Bekannte Probleme-1](./media/known_issues_1.PNG)

3. Suchen Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst** , und klicken Sie mit der rechten Maustaste darauf.
![Bekannte Probleme-2](./media/known_issues_2.PNG)

4. Starten Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst**erneut.
![Bekannte Probleme-3](./media/known_issues_3.PNG)

5. Schließen Sie die Microsoft Edge-Entwickler Tools und die Registerkarte. Öffnen Sie eine neue Registerkarte, navigieren Sie zu Ihrer Seite, und drücken Sie `F12` .

6. Sie sollten jetzt in der Lage sein, mit der Profilerstellung zu beginnen.
![Bekannte Probleme-4](./media/known_issues_4-performance.PNG)

Gibt es immer noch Probleme? Senden Sie uns Ihr Feedback über das Symbol **Feedback senden** ! 

![Bekannte Probleme-5](./media/known_issues_5.PNG)

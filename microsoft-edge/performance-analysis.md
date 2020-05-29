---
ms.assetid: 7a5f9fd0-90a9-43db-b271-178c06da5896
description: Verwenden Sie F12-Entwicklertools, um die allgemeine Leistung von Websites zu analysieren.
title: Leistungsanalyse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/08/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: 7bf71744298502c9edf8ee1262fceff5640bedf1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568682"
---
# Leistungsanalyse

Wenn Sie mit der Leistung noch nicht vertraut sind, sollten Sie sich das [F12-Handbuch für devtools](./devtools-guide.md).
Die in Microsoft Edge integrierten [F12-Tools](./devtools-guide.md) können verwendet werden, um die allgemeine Leistung einer Website zu analysieren. Es bietet ähnliche (aber noch begrenzte) Funktionen für das [Windows Performance Toolkit](https://docs.microsoft.com/windows-hardware/test/wpt/index) direkt im Browser.



Wenn Sie eine genauere Analyse der Browserleistung wünschen, verwendet das Microsoft Edge-Team das [Windows Performance Toolkit](https://docs.microsoft.com/windows-hardware/test/wpt/index) (WPT). WPT wurde vom Windows-Team erstellt, um eine detaillierte Programm Leistungsanalyse durchzuführen. Sie überspannt die Grenzen zwischen Website-JavaScript und Microsoft Edge-systemeigenem Code, sodass beide innerhalb desselben Tools angezeigt werden können. WPT kann verwendet werden, um:
 - Messen der CPU-Zeit, die für Software zum Abschließen der Arbeit genommen wurde
 - Berechnen des von der Software zugewiesenen Arbeitsspeichers
 - Anzeigen der Details zum Herunterladen von Dateien von Remoteservern
 - Frame-Rate Messen


Um mit der Verwendung des Windows Performance Toolkit zum Analysieren Ihrer Website zu beginnen, müssen Sie zunächst das [Windows 10 Assessment and Deployment Kit (ADK)](https://developer.microsoft.com/windows/hardware/windows-assessment-deployment-kit)herunterladen. Wählen Sie die Option *Windows Performance Toolkit* während der Installation aus:

![ADK-Installationsoptionen](./media/adk-installoptions.png)

Hier erfahren Sie, wie Sie eine Leistungsablaufverfolgung aufzeichnen und analysieren. Weitere Informationen zu den Funktionen, die im Windows Performance Toolkit enthalten sind, finden Sie in der vollständigen [WPT-Dokumentation](https://docs.microsoft.com/windows-hardware/test/wpt/index).

## Aufzeichnen einer Ablaufverfolgung
Richten Sie als nächstes Ihr Benutzerszenario ein, und bereiten Sie die Erfassung einer Ablaufverfolgung mithilfe der Windows-Leistungsaufzeichnung vor.
Hier erfahren Sie, wie Sie Ihr Webszenario mit der *Windows-Leistungsaufzeichnung (WPR)* profilieren.

### 1. Vorbereiten Ihrer Umgebung zum Sammeln einer Leistungs Spur
Beenden Sie so viele ausgeführte Programme wie möglich, um Rauschen in der Ablaufverfolgung zu vermeiden, die Sie aufzeichnen möchten. Im Idealfall handelt es sich bei der einzigen ausgeführten Software um Windows Performance Recorder (WPR) und den Browser.

### 2. Starten Sie Windows Performance Recorder (WPR), und wählen Sie Optionen aus.
Starten Sie die Windows-Leistungsaufzeichnung, und stellen Sie sicher, dass die Umschaltfläche **Weitere Optionen** erweitert ist. Aktivieren Sie die Kontrollkästchen *Edge-Browser* und *HTML-Reaktions Szenarien-* Analyse.

![Windows-Leistungsdaten Satz Optionen](./media/wprui-options.png)

#### Tipps und Kniffe für das Sammeln von Ablaufverfolgungen
- Versuchen Sie, Hintergrundaktivitäten auf ein absolut erforderliches Minimum zu beschränken. Hintergrundprozesse können sowohl die wahrgenommene Leistung als auch die tatsächlichen Leistungsmerkmale verzerren und die Ergebnisse beeinflussen. Im Idealfall gibt es keine anderen ausgeführten Anwendungen neben Browser-und WPR.
- Ermitteln Sie die Szenarien, die Sie analysieren, und versuchen Sie, Sie so atomar wie möglich zu halten. Wenn Ihre Website beispielsweise Leistungsprobleme beim Laden der Seite, beim Scrollen und Auswählen von etwas in einer Tabelle aufweist, trennen Sie die Probleme in drei Szenarien:
  - Seitenladevorgang (vom Anfang der Navigation bis zum Laden der Seite)
  - Scroll
  - Auswählen von etwas in der Tabelle
- Wenn ein Szenario eine Navigation zu einer Website beinhaltet, sollten Sie das Szenario mit ungefähr: leer beginnen. Ab etwa: leer wird der Overhead der vorherigen Seite vermieden. Wenn Sie von einer Website entfernt navigieren möchten, navigieren Sie zu about: leer, um das Szenario abzuschließen. Dadurch wird das Rauschen anderer Websites außerhalb der Ablaufverfolgung beibehalten, es sei denn, die spezifische Interaktion zwischen Websites ist das untersuchte Problem.

### 3. Aufzeichnen des Szenarios
Klicken Sie auf **Start** , um mit der Aufzeichnung zu beginnen. Das Tool meldet die Größe des verwendeten Puffers, damit Sie die Größe der generierten Datei antizipieren können. Führen Sie das Benutzerszenario aus, das Sie messen möchten, und klicken Sie auf **Speichern** , um die Aufzeichnung zu beenden und die Ablaufverfolgung zu speichern. Wenn Sie das Szenario unmittelbar nach Abschluss Ihres Szenarios speichern, können Sie die Größe der Ablaufverfolgungsdatei minimieren.

![Windows-Leistungsdaten Satzanfang](./media/wprui-recording.png)

Das WPR-Tool gibt an, dass Ihre Ablaufverfolgungsinformationen erfolgreich gespeichert wurden:

![Windows-Leistungsdaten Satzanfang](./media/wprui-savecomplete.png)


## Analysieren einer Ablaufverfolgung
Nachdem Sie nun Ihre Leistungsdaten gesammelt haben, können Sie die Ablaufverfolgung mithilfe von Windows Performance Analyzer analysieren, um zu sehen, welche Optimierungen vorgenommen werden können.
Hier erfahren Sie, wie Sie die Performance-Daten Ihres Webszenarios analysieren.

### 1. Öffnen Sie Windows Performance Analyzer (WPA).
Starten Sie Windows Performance Analyzer, und öffnen `.etl` Sie die Datei, die analysiert werden soll (**Datei**  >  **Öffnen...**).

### 2. Laden von Symbolen und Anwenden des *HTML-Analyse* Profils

>[!WARNING]
> Wenn Sie Symbole zum ersten Mal laden, wird ein großer Download benötigt, und es dauert eine beträchtliche Zeitdauer für eine typische Internetverbindung.

Laden Sie Ihre Symbole, indem Sie im Menü die Option nach **Verfolgungs**  >  **Lade Symbole** auswählen. Die Symbole werden auf dem Datenträger zwischengespeichert, und in zukünftigen Ablaufverfolgungen werden Symbole wesentlich schneller geladen.

Sie können Symbole erheblich schneller laden, indem Sie das Laden von Microsoft Edge und dem Web-Apps-Host einschränken. Wählen Sie **Ablauf Verfolgungs**  >  **Symbole konfigurieren** aus, und beschränken Sie die **Auslastungs Einstellungen** auf nur `MicrosoftEdgeCP.exe` und `WWAHost.exe` .

![Symbol Einschränkungen](./media/wpa-symbolrestrictions.png)

Nachdem Symbole mit dem Laden beginnen, wenden Sie das *HTML-Analyse Profil* an (**profile**  >  **gelten...**  >  **Katalog durchsuchen...**  >  **HtmlResponsivenessAnalysis. wpaProfile**) im Profil werden mehrere Diagramme und Tabellen für Ihre Analyse geladen. Für nahezu alle Website-Untersuchungen empfehlen wir, mit diesem Profil zu beginnen.

![Großes Bild](./media/wpa-bigpicture.png)


#### Das HTML-Reaktionsanalyse Profil
Das *HTML-* Analyse Profil für Reaktionsfähigkeit bietet vier Registerkarten:

**Großes Bild** – Dies ist nützlich, um zu bestätigen, dass es keine unerwarteten Quellen für die CPU-Aktivität gibt und der Browser tatsächlich alle verfügbaren Ressourcen verwendet. Überprüfen Sie die CPU-Auslastung, und stellen Sie sicher, dass keine Prozesse erheblich zur CPU-Nutzung außer dem Browser beitragen.

**Frame Analyse** – dieser Abschnitt wird für die grundlegende Analyse verwendet. Das Diagramm *CPU-Auslastung (attributiert)* ermöglicht einen schnellen Überblick über die für die CPU-Nutzung Verantwortlichen Subsysteme. Das Aufschlüsseln der Beispiele in der Tabelle *CPU-Auslastung (abgetastet)* im *HTML-UI-Thread* ist hilfreich, um kritische Leistungsengpässe zu identifizieren.

**Ablauf Verfolgungs Markierungen** – in diesem Abschnitt werden alle nach Verfolgungs Marken angezeigt, die aus dem Browser (Microsoft Edge) kommen, einschließlich *msWriteProfilerMark*, das genaue Punkte für die Code Messung bietet. Um die *msWriteProfilerMark* -Ablaufverfolgung anzuzeigen, Scrollen Sie nach unten zum Diagramm *generische Ereignisse* , und wählen Sie im Dropdownmenü **HTML-msWriteProfilerMark** aus.

**Analyse der Thread Verzögerung** -diese Registerkarte wird häufig von Microsoft Edge-Entwicklern verwendet, um zu untersuchen, ob ein Thread blockiert ist und auf einen anderen wartet. In seltenen Fällen kann es auch für Web-Entwickler nützlich sein.


### 3. Zoom zum Entfernen der Ablaufverfolgung
Sie können Ihre Analyse fokussieren, indem Sie die leeren nach *verfolgten Ablauf Verfolgungs* Abschnitte in Ihren Diagrammen entfernen. In einem der aktuell angezeigten Diagramme:
 - Klicken Sie mit der linken Maustaste auf den Anfang der Diagrammdaten, die Sie untersuchen möchten.
 - Halten, ziehen und loslassen, um die gewünschte Region auszuwählen
 - Klicken Sie mit der rechten Maustaste, und wählen Sie **Zoom** aus.

Der Zoom wird auf alle Diagramme und Diagramme auf der aktiven Registerkarte angewendet.

![Nach Zoom](./media/wpa-postzoom.png)


### 4. untersuchen, was CPU-Zyklen beansprucht
 In der Tabelle " **CPU-Auslastung (abgetastet)** " auf der Registerkarte " **Frame Analyse** " werden die meisten ihrer Analysen wahrscheinlich vorkommen. Sie können die verschiedenen Prozesse erweitern, um die meisten rechenintensiven JavaScript-und Browser-Codes zu identifizieren. Oft ist ein einzelnes JavaScript-Bit für ein Leistungsproblem verantwortlich, und die Zeit für die Optimierung kann einen entscheidenden Unterschied ausmachen.

### 5. führen Sie einen Drilldown zu einem langsam ausgeführten JavaScript-Code durch.
Bottom-up-Dom-anrufanalyse kann hilfreich sein, um das JavaScript zu identifizieren, das für den Großteil der Zeit während des Szenarios verantwortlich ist. Dies ist besonders hilfreich, wenn viele Anrufe auf oberster Ebene die gleichen JavaScript-Bibliotheken wieder verwenden.

Schauen Sie sich zunächst die *CPU-Auslastung (abgetastet) an, aufgeschlüsselt nach Prozess, Thread, Aktivität und Stack*. Klicken Sie auf eine beliebige Zelle in der **Stapel** Spalte. Drücken Sie *STRG + F* , und suchen Sie nach *ExternalFunctionThunk*.

>[!NOTE] 
>Dies funktioniert nur, wenn Symbole erfolgreich geladen wurden.

![Suchen nach ExternalFunctionThunk](./media/wpa-externalfunctionthunk.png)

Untersuchen Sie alle Linien mit *ExternalFunctionThunk*. Hierbei handelt es sich um die Schnittstelle des Chakra JavaScript-Moduls zum Microsoft Edge-Modul. Sie zeigt an, wo Code Brücken vom Browser zur JavaScript-Ausführung sind. Klicken Sie mit der rechten Maustaste auf die Zeile, und wählen Sie " **aufgerufene**  >  **nach Modulen** anzeigen" aus, um eine gewichtete Liste der am längsten ausgeführten Browsermodul Funktionen anzuzeigen.

![Anzeigen von Anrufen](./media/wpa-viewcallees.png)

Um alle JavaScript-Aufrufe einer bestimmten API zu identifizieren, klicken Sie mit der rechten Maustaste darauf, und wählen Sie **Anrufer**  >  **nach Funktion** anzeigen aus, und erweitern Sie die Struktur, um die relativen Gewichtung anzuzeigen und zu vergleichen.

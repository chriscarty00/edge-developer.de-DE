---
description: Microsoft Edge (Chrom) und Visual Studio
title: Visual Studio
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/12/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, vs, Visual Studio, Debugger
ms.openlocfilehash: 27f4b7d4dc85e3cd5ba49497dec2d4658166794b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568654"
---
# Visual Studio

In [Visual Studio](https://visualstudio.microsoft.com/vs/) handelt es sich um eine integrierte Entwicklungsumgebung (IDE), die Sie zum Bearbeiten, Debuggen, erstellen und Veröffentlichen von Webanwendungen verwenden können. Es handelt sich um ein funktionsreiches Programm, das für viele Aspekte Ihrer Web-Entwicklung verwendet werden kann. Neben dem Standard-Editor und-Debugger, den die meisten IDES bereitstellen, enthält Visual Studio Compiler, Tools für die Codevervollständigung, grafische Designer und viele weitere Features, um den Entwicklungsprozess zu vereinfachen. Wechseln Sie zu [dieser Seite](https://visualstudio.microsoft.com/downloads/) , um Visual Studio herunterzuladen, wenn Sie es noch nicht verwenden.

Derzeit unterstützt Visual Studio 2019 das Debuggen von JavaScript in Microsoft Edge für Ihre ASP\.NET-Framework-und ASP\.net-Core-Anwendungen. Führen Sie die folgenden Schritte aus, um Microsoft Edge in Visual Studio zu debuggen.

## Starten von Microsoft Edge
Visual Studio erstellt Ihre ASP\.net-und ASP\.net-Kernanwendung, startet Ihren Webserver, startet Microsoft Edge und verbindet den Visual Studio-Debugger mit nur einem Mausklick. Auf diese Weise können Sie JavaScript Debuggen, das in Microsoft Edge direkt aus Ihrer IDE ausgeführt wird!

### Erstellen einer neuen ASP.net Core-Webanwendung

Öffnen Sie Visual Studio 2019, und wählen Sie **Neues Projekt erstellen**aus. Wählen Sie auf dem nächsten Bildschirm **ASP\.net Core Web Application** aus, und klicken Sie auf **weiter**.

> ##### Abbildung1  
> Erstellen einer neuen ASP.net Core-Webanwendung ![ Erstellen einer neuen ASP.net-Core-Webanwendung](./media/create-new-project.png)  

Geben Sie einen **Projektnamen** für das neue Projekt ein, und klicken Sie auf **Erstellen**. Wählen Sie in diesem Beispiel als Vorlage **reagieren. js** aus, in der Sie erfahren, wie Sie mit einer ASP.net Core-Anwendung reagieren. js integrieren, und klicken Sie auf **Erstellen**.

### Starten von Microsoft Edge in Visual Studio

Nachdem Ihr Projekt erstellt wurde, öffnen Sie **ClientApp/src/Components/Counter. js**. Visual Studio soll nun JavaScript Debuggen, indem Sie die Dropdownliste neben der grünen Schaltfläche " **Wiedergabe** " und " **IIS Express**" auswählen. 

> ##### Abbildung2  
> Die Dropdown-Liste neben der grünen Schaltfläche " **Wiedergabe** " und " **IIS" drücken** 
> ![ die Dropdown-Liste neben der grünen Schaltfläche "Wiedergabe" und IIS Express](./media/vs-dropdown.png)  

Wählen Sie **Skript Debugging** aus, und klicken Sie auf **aktiviert**.

> ##### Abbildung 3  
> Aktivieren des Skriptdebuggings in Visual Studio ![ Aktivieren des Skriptdebuggings in Visual Studio](./media/enable-script-debugging.png)  

Wählen Sie in derselben Dropdownliste **Webbrowser** aus, und klicken Sie auf den Vorschau Kanal von Microsoft Edge, den Visual Studio starten soll: Microsoft Edge Canary, dev oder Beta. Wenn Sie dies noch nicht getan haben, wechseln Sie zu [dieser Seite](https://www.microsoftedgeinsider.com/download) , um die Microsoft Edge Preview-Kanäle zu installieren.

> ##### Abbildung4  
> Wählen Sie den Vorschau Kanal von Microsoft Edge aus, den Visual Studio starten soll, und ![ Wählen Sie den Vorschau Kanal von Microsoft Edge aus, den Visual Studio starten soll.](./media/set-web-browser.png)  

> [!NOTE]
> Wenn Sie Microsoft Edge (EdgeHTML) auswählen, startet Visual Studio diesen anstelle von Microsoft Edge (Chrom). [Installieren Sie die Vorschau Kanäle von Microsoft Edge](https://www.microsoftedgeinsider.com/download) , und wählen Sie Sie aus, oder stellen Sie sicher, dass die Version von Microsoft Edge, die auf Ihrem Computer installiert ist, Microsoft Edge (Chrom) und nicht Microsoft Edge (EdgeHTML) ist.

Nachdem Visual Studio nun ordnungsgemäß konfiguriert wurde, klicken Sie auf die grüne Schaltfläche **Wiedergabe** . Visual Studio erstellt Ihre Anwendung, startet den Webserver, startet Microsoft Edge und navigiert zu dem `https://localhost:44362/` in **launchSettings. JSON**angegebenen Port.

> ##### Abbildung5  
> Microsoft Edge, gestartet von Visual Studio ![ Microsoft Edge, gestartet von Visual Studio](./media/edge-launch.png)  

### Debuggen von JavaScript, das in Microsoft Edge ausgeführt wird

Wechseln Sie zurück zu Visual Studio. Setzen Sie in **counter. js**einen Haltepunkt in Zeile 13, indem Sie in den Bundsteg neben dieser Zeile klicken.

> ##### Abbildung6
> Festlegen eines Haltepunkts in Visual Studio durch Klicken auf den Bundsteg neben Zeile 13 in **counter. js** 
> ![ Festlegen eines Haltepunkts in Visual Studio durch Klicken auf den Bundsteg neben Zeile 13 in Counter. js](./media/set-breakpoint.png)  

Wechseln Sie nun zurück zu der Instanz von Microsoft Edge, die von Visual Studio gestartet wurde. Klicken Sie im NavMenu Links auf der Seite auf **Zähler** . Klicken Sie nun auf **Inkrement**.

> ##### Abbildung7
> Die Counter-Seite in unserer ASP.net Core-Webanwendung ![ die Counter-Seite in unserer ASP.net-Core-Webanwendung](./media/edge-counter.png)  

Der JavaScript-Debugger in Visual Studio wird den in **counter. js**gesetzten Haltepunkt erreichen. Visual Studio hat nun die Ausführung des in Microsoft Edge ausgeführten Javascripts angehalten, und Sie können das Skript Zeile für Zeile durchlaufen.

> ##### Abbildung8
> Visual Studio pausieren von JavaScript, das in Microsoft Edge Visual Studio ausgeführt wird, hält ![ JavaScript in Microsoft Edge auf](./media/hit-breakpoint.png)  

Dieses Beispiel war nur eine kleine Demonstration der in Visual Studio verfügbaren Funktionen. Erfahren Sie mehr über alle Funktionen, die Sie in Visual Studio 2019 durchführen können, indem Sie [deren Dokumentation](https://docs.microsoft.com/visualstudio/windows/?view=vs-2019)lesen.

## An Microsoft Edge anfügen
Im vorherigen Workflow startet Visual Studio Microsoft Edge. Mit diesem Workflow können Sie den Visual Studio-Debugger an eine bereits ausgeführte Instanz von Microsoft Edge anfügen. 

Stellen Sie zunächst sicher, dass keine ausgeführten Instanzen von Microsoft Edge vorhanden sind. Führen Sie nun über Ihr Terminal den folgenden Befehl aus:

```console
start msedge –remote-debugging-port=9222
```

Öffnen Sie in Visual Studio das Menü **Debuggen** , und wählen Sie **an Prozess anfügen** aus, oder drücken Sie `Ctrl`  +  `Alt`  +  `P` .

> ##### Abbildung 9
> Auswählen von **Anfügen an den Prozess** in Visual Studio ![ Auswählen von * * an den Prozess anfügen * * in Visual Studio](./media/attach-to-process.png)  

Legen Sie im Dialogfeld **an den Prozess anfügen** den **Verbindungstyp** auf **Chrome devtools Protocol WebSocket (keine Authentifizierung)**. Geben Sie in das Textfeld **Verbindungsziel** ein, `http://localhost:9222/` und drücken Sie `Enter` . Im Dialogfeld **an den Prozess anfügen wird** die Liste der geöffneten Registerkarten angezeigt, die in Microsoft Edge aufgeführt sind.

> ##### Abbildung 10
> Konfigurieren des Dialogfelds **an den Prozess anfügen** in Visual Studio ![ Konfigurieren des Dialogfelds an den Prozess anfügen in Visual Studio](./media/attach-to-process-dialog.png)  

Klicken Sie auf **auswählen.** .. und prüfen Sie **JavaScript (Microsoft Edge – Chrom)**. Sie können Registerkarten hinzufügen, zu neuen Registerkarten navigieren und Registerkarten schließen, und diese Änderungen werden im Dialogfeld **an den Prozess anfügen** angezeigt, indem Sie auf die Schaltfläche **Aktualisieren** klicken. Wählen Sie die Registerkarte aus, die Sie debuggen möchten, und klicken Sie auf **Anfügen**.

Der Visual Studio-Debugger ist nun an Microsoft Edge angefügt! Sie können die Ausführung von JavaScript anhalten, Haltepunkte festlegen und `console.log()` Anweisungen direkt im Fenster Debug-Ausgabe in Visual Studio anzeigen.

## Feedback senden
Wir möchten gerne mehr darüber erfahren, wie Sie mit JavaScript in Visual Studio arbeiten können! Senden Sie uns Feedback, indem Sie auf das **Feedback** Symbol in Visual Studio klicken oder [@VisualStudio und @EdgeDevTools](https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools)tweeten.

> ##### Abbildung 11
> Das **Feedback** Symbol in Visual Studio ![ das Feedback Symbol in Visual Studio](./media/feedback-icon.png)  

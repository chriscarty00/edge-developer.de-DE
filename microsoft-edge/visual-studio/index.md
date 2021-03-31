---
description: Microsoft Edge (Chromium) und Visual Studio
title: Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, vs, visual studio, debugger
ms.openlocfilehash: 562952ef238c05922e468501706ab75e1976273d
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387275"
---
# <a name="visual-studio"></a>Visual Studio  

Microsoft [Visual Studio][MicrosoftVisualstudioVs] ist eine integrierte Entwicklungsumgebung \(IDE\).   Verwenden Sie sie, um Ihre Web-Apps zu bearbeiten, zu debuggen, zu erstellen und zu veröffentlichen.  Es handelt sich um ein funktionsreiches Programm, das für viele Aspekte Ihrer Webentwicklung verwendet werden kann.  Neben dem Standard-Editor und Debugger, den die meisten IDEs bereitstellen, enthält Visual Studio die folgenden Features, um Ihren Entwicklungsprozess zu erleichtern.  

*   Compiler  
*   Codevollständigungstools  
*   Grafische Designer  
*   viele weitere  
    
Wenn Sie die Datei noch nicht Visual Studio, navigieren Sie zu [Download Visual Studio,][MicrosoftVisualstudioDownloads] um sie herunterzuladen.  

Derzeit unterstützt Visual Studio 2019 das Debuggen von JavaScript in Microsoft Edge für Ihr ASP.NET Framework und ASP.NET Core-Apps.  Führen Sie die folgenden Schritte aus, um Visual Studio Microsoft Edge zu debuggen.  

## <a name="launch-microsoft-edge"></a>Starten von Microsoft Edge  

Visual Studio den folgenden Workflow mithilfe einer einzelnen Schaltfläche ab.  

1.  Erstellt Ihre ASP.NET und ASP.NET Core-App.  
1.  Startet den Webserver.  
1.  Startet Microsoft Edge.  
1.  Verbindet den Visual Studio Debugger.  
    
Mit dem vereinfachten Workflow können Sie JavaScript debuggen, das in Microsoft Edge direkt über Ihre IDE ausgeführt wird.  

### <a name="create-a-new-aspnet-core-web-app"></a>Erstellen einer neuen ASP.NET Core Web App  

Öffnen Visual Studio 2019, und wählen **Sie Erstellen eines neuen Projekts aus.**  Wählen Sie auf dem nächsten Bildschirm **ASP.NET Core Web app**Next  >  **aus.**  

:::image type="complex" source="./media/create-new-project.png" alt-text="Erstellen einer neuen ASP.NET Core Web App" lightbox="./media/create-new-project.png":::
   Erstellen einer neuen ASP.NET Core Web App  
:::image-end:::  

Geben Sie **einen Projektnamen** für Ihr neues Projekt an, und wählen Sie **Erstellen aus.**  Wählen Sie für die Zwecke des Beispiels **React.js** als Vorlage aus, und wählen Sie **Erstellen aus.**  Die **React.js-Vorlage ** gibt an, wie React.js in eine ASP.NET Core-App integriert wird.  

### <a name="launch-microsoft-edge-from-visual-studio"></a>Starten von Microsoft Edge von Visual Studio  

Öffnen Sie nach dem Erstellen Des Projekts `ClientApp/src/components/Counter.js` .  Wenn Sie nun javaScript Visual Studio, wählen Sie das Dropdown neben der grünen Schaltfläche **Play** und **IIS Express aus.**  

:::image type="complex" source="./media/vs-dropdown.png" alt-text="Das Dropdown neben der grünen Schaltfläche Play und IIS Express" lightbox="./media/vs-dropdown.png":::
   Das Dropdown neben der grünen **Schaltfläche "Play"** und **"IIS Express"**  
:::image-end:::  

Wählen **Sie Skriptdebubuing**  >  **aktiviert aus.**  

:::image type="complex" source="./media/enable-script-debugging.png" alt-text="Aktivieren des Skriptdebudings in Visual Studio" lightbox="./media/enable-script-debugging.png":::
   Aktivieren des Skriptdebudings in Visual Studio  
:::image-end:::  

Wählen Sie in derselben Dropdownliste Webbrowser **>** dem Vorschaukanal von Microsoft Edge aus, den Sie Visual Studio starten möchten, z. B. Microsoft Edge Canary, Dev oder Beta.  Wenn Sie noch keinen der Microsoft Edge-Vorschaukanäle verwenden, navigieren Sie zu [Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload] herunterladen, um einen herunterzuladen.  

:::image type="complex" source="./media/set-web-browser.png" alt-text="Wählen Sie den Vorschaukanal von Microsoft Edge aus, den Visual Studio starten möchten" lightbox="./media/set-web-browser.png":::
   Wählen Sie den Vorschaukanal von Microsoft Edge aus, den Visual Studio starten möchten  
:::image-end:::  

> [!NOTE]
> Wenn Sie Microsoft Edge \(EdgeHTML\) auswählen, wird Visual Studio Microsoft Edge \(Chromium\) gestartet.  Installieren Sie einen der Vorschaukanäle von [Microsoft Edge,][MicrosoftedgeinsiderDownload] oder stellen Sie sicher, dass die auf Ihrem Computer installierte Version von Microsoft Edge Microsoft Edge \(Chromium\) und nicht Microsoft Edge \(EdgeHTML\) ist.  

Nachdem Visual Studio richtig konfiguriert ist, wählen Sie die grüne Schaltfläche **Wiedergabe** aus.  Visual Studio Sie Ihre App, starten Sie den Webserver, starten Sie Microsoft Edge, und navigieren Sie zu oder zu dem Port, der `https://localhost:44362/` in angegeben `launchSettings.json` ist.  

:::image type="complex" source="./media/edge-launch.png" alt-text="Microsoft Edge wird von Visual Studio" lightbox="./media/edge-launch.png":::
   Microsoft Edge wird von Visual Studio  
:::image-end:::  

### <a name="debug-javascript-running-in-microsoft-edge"></a>Debuggen von JavaScript, das in Microsoft Edge ausgeführt wird  

Wechseln Sie zurück zu Visual Studio.  Wählen Sie in die Rinne neben der Linie aus, um einen Haltepunkt für Zeile `Counter.js` 13 zu setzen.  

:::image type="complex" source="./media/set-breakpoint.png" alt-text="Wählen Sie die Rinne neben Zeile 13 in Counter.js, um einen Haltepunkt in Visual Studio" lightbox="./media/set-breakpoint.png":::
   Wählen Sie die Rinne neben Zeile 13 in aus, um einen `Counter.js` Haltepunkt in Visual Studio  
:::image-end:::  

Wechseln Sie nun zurück zur Instanz von Microsoft Edge, die Visual Studio wurde.  Wählen Sie **im** NavMenu auf der linken Seite der Webseite den Zähler aus.  Wählen Sie jetzt **Erhöhen aus.**  

:::image type="complex" source="./media/edge-counter.png" alt-text="The Counter page in our ASP.NET Core web app" lightbox="./media/edge-counter.png":::
   The Counter page in our ASP.NET Core web app  
:::image-end:::  

Der JavaScript-Debugger in Visual Studio den haltepunkt, den Sie in festgelegt `Counter.js` haben.  Visual Studio die Laufzeit von JavaScript, das in Microsoft Edge ausgeführt wird, an, und Sie können das Skript zeile für Zeile durchschritten.  

:::image type="complex" source="./media/hit-breakpoint.png" alt-text="Visual Studio hält JavaScript an, das in Microsoft Edge ausgeführt wird" lightbox="./media/hit-breakpoint.png":::
   Visual Studio hält JavaScript an, das in Microsoft Edge ausgeführt wird  
:::image-end:::  

Das Beispiel war nur eine geringfügige Demonstration der funktionalität, die in Visual Studio.  Weitere Informationen zu den Funktionen in Visual Studio 2019 finden Sie [in Visual Studio Dokumentation][VisualStudioWindowsIndex].  

## <a name="attach-to-microsoft-edge"></a>An Microsoft Edge anfügen  

Zuvor mussten Sie Microsoft Edge von einem Visual Studio.  Jetzt können Sie den Visual Studio an eine bereits ausgeführte Instanz von Microsoft Edge anfügen.  

Stellen Sie zunächst sicher, dass keine Instanzen von Microsoft Edge ausgeführt werden.  Führen Sie nun über die Befehlszeile den folgenden Befehl aus.  

```console
start msedge –remote-debugging-port=9222
```  

Öffnen Visual Studio sie das Menü **Debuggen,** und wählen Sie An Prozess anfügen **aus,** oder wählen Sie `Ctrl` + `Alt` + `P` aus.  

:::image type="complex" source="./media/attach-to-process.png" alt-text="Wählen Sie An Prozess anfügen in Visual Studio" lightbox="./media/attach-to-process.png":::
   Wählen **Sie An Prozess anfügen** in Visual Studio  
:::image-end:::  

Legen Sie **im Dialogfeld An Prozess** anfügen **den** Verbindungstyp auf **Chrome devtools-Protokollwebsocket (keine Authentifizierung) ein.**  Geben Sie **im Textfeld Verbinden** des Ziels ein, und wählen Sie `http://localhost:9222/` `Enter` aus.  Überprüfen Sie die Liste der geöffneten Registerkarten in Microsoft Edge, die im **Dialogfeld An** Prozess anfügen aufgeführt sind.  

:::image type="complex" source="./media/attach-to-process-dialog.png" alt-text="Konfigurieren des Dialogfelds An Prozess anfügen in Visual Studio" lightbox="./media/attach-to-process-dialog.png":::
   Konfigurieren des **Dialogfelds An Prozess anfügen** in Visual Studio  
:::image-end:::  

Wählen **Sie Select...** > das Kontrollkästchen neben **JavaScript (Microsoft Edge – Chromium) aus.**  Um Registerkarten hinzuzufügen, zu neuen Registerkarten zu navigieren und Registerkarten zu schließen und die änderungen anzuzeigen, die im Dialogfeld **An** Prozess anfügen angezeigt werden, wählen Sie die **Schaltfläche Aktualisieren** aus.  Wählen Sie die Registerkarte aus, die Sie debuggen möchten, und wählen Sie **Anhängen aus.**  

Der Visual Studio Debugger ist jetzt an Microsoft Edge angefügt.  Sie können die Ausführung von JavaScript anhalten, Haltepunkte festlegen und Anweisungen direkt `console.log()` im Fenster Debugausgabe in Visual Studio.  

## <a name="getting-in-touch-with-the-microsoft-visual-studio-team"></a>Kontakt mit dem Microsoft Visual Studio Team  

Die Microsoft Visual Studio- und Microsoft Edge-Teams möchten mehr darüber erfahren, wie Sie mit JavaScript in Visual Studio.  Um Ihr Feedback zu senden, wählen Sie das **Symbol** Feedback senden in Visual Studio oder tweet @VisualStudio [und @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].  

:::image type="complex" source="./media/feedback-icon.png" alt-text="Das Symbol Feedback senden in Visual Studio" lightbox="./media/feedback-icon.png":::
   Das **Symbol Feedback** senden in Visual Studio  
:::image-end:::  

<!-- links -->  

[VisualStudioWindowsIndex]: /visualstudio/windows/index "Visual Studio Dokumentation | Microsoft Docs"  

[MicrosoftVisualstudioDownloads]: https://visualstudio.microsoft.com/downloads "Download Visual Studio"  
[MicrosoftVisualstudioVs]: https://visualstudio.microsoft.com/vs "Visual Studio IDE"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[TwitterIntentTweetViualstudioEdgdevtools]: https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools "Tweet zu @VisualStudio und @EdgeDevTools | Twitter"  

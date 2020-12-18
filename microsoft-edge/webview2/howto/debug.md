---
description: Erfahren Sie, wie Sie WebView2-Steuerelemente Debuggen.
title: Erste Schritte beim Debuggen von WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 4f94fe880f66f8aeb387d2db4a8bfaab20699466
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230698"
---
# Erste Schritte beim Debuggen von WebView2-Anwendungen  

Das Ziel des Microsoft Edge WebView2-Steuerelements besteht darin, die besten Features und Tools für die Entwicklung von Web-und systemeigenen Anwendungen zu kombinieren.  Wenn Sie Ihre WebView2-Anwendung entwickeln, sollten Sie Ihre Anwendung debuggen.  In diesem Artikel werden die verschiedenen Tools erläutert, die Sie verwenden können, um Ihren Web-und systemeigenen Code in ihrer WebView2-Anwendung zu debuggen.  

## [Microsoft Edge DevTools](#tab/devtools)  

Verwenden Sie die [Microsoft Edge (Chrom)-Entwickler Tools][DevtoolsGuideChromiumMain] zum Debuggen von Webinhalten, die in WebView2-Steuerelementen angezeigt werden, auf die gleiche Weise, wie Sie für eine andere in Microsoft Edge angezeigte Webseite debuggen können.  Um das devtools zu öffnen, setzen Sie den Fokus auf das WebView-Steuerelement, und verwenden Sie dann eine der folgenden Aktionen.  

*   Wählen Sie aus `F12` .  
*   Wählen Sie aus `Ctrl` + `Shift` + `I` .  
*   Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie aus `Inspect` .  
    
Weitere Informationen finden Sie unter [Übersicht über devtools][DevtoolsGuideChromiumMain].  

:::image type="complex" source="./media/f12.png" alt-text="DevTools-Debuggen" lightbox="./media/f12.png":::
   DevTools-Debuggen  
:::image-end:::  

## [Visual Studio](#tab/visualstudio)  

Visual Studio bietet verschiedene Debugging-Tools für Web-und systemeigenen Code in WebView2-Anwendungen.  Im Abschnitt Visual Studio liegt der Hauptfokus auf dem Debuggen von WebView-Steuerelementen, doch die anderen Methoden zum Debuggen in Visual Studio sind wie gewohnt verfügbar.  Mit dem folgenden Verfahren können Sie Web-und systemeigenen Code nur in Win32-Anwendungen oder Office-Add-ins Debuggen.  

> [!IMPORTANT]
> Wenn Sie die Anwendung in Visual Studio debuggen, wobei der systemeigene Debugger angefügt ist, `F12` kann die Auswahl den systemeigenen Debugger anstelle der Entwickler Tools auslösen.  Wählen Sie aus `Ctrl` + `Shift` + `I` , oder verwenden Sie das Kontextmenü \ (mit der rechten Maustaste auf \), um die Situation zu vermeiden.  

Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Anforderungen erfüllt sind.  

*   Zum Debuggen von Skripts muss die app in Visual Studio gestartet werden.  
*   Sie können keinen Debugger an einen ausgeführten WebView2-Prozess anfügen.  
*   Installieren Sie Visual Studio 2019, Version 16,4 Preview 2 oder höher.  
    
Installieren und Einrichten der Skriptdebugger Tools in Visual Studio.  

1.  Führen Sie die folgenden Aktionen aus, um die Komponente **JavaScript-Diagnose** in der **Desktop Entwicklung mit C++** zu installieren.  
    
    1.  Geben Sie in der Windows-Explorer-Leiste ein `Visual Studio Installer` .  
    1.  Wählen Sie **Visual Studio-Installationsprogramm** aus, um es zu öffnen.  
    1.  Wählen Sie im Visual Studio-Installationsprogramm in der installierten Version die Schaltfläche **mehr** aus, und wählen Sie dann **ändern**aus.  
    1.  Wählen Sie in Visual Studio unter **Arbeits auslasten**die Einstellung **Desktop Entwicklung in C++** aus.  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Bildschirm ' Ändern von Arbeitslasten ' in Visual Studio" lightbox="./media/workloads.png":::
            Bildschirm ' Ändern von Arbeitslasten ' in Visual Studio
        :::image-end:::  
        
    1.  Wählen Sie **einzelne Komponenten**aus.  
    1.  Geben Sie im Suchfeld ein `JavaScript diagnostics` .  
    1.  Wählen Sie die **JavaScript-Diagnose** Einstellung aus.  
    1.  Wählen Sie **ändern**aus. 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio-Registerkarte ' einzelne Komponenten ändern '" lightbox="./media/indivcomp.png":::
           Visual Studio-Registerkarte ' einzelne Komponenten ändern '  
        :::image-end:::  
        
1.  Aktivieren Sie das Skriptdebugging für WebView2-Anwendungen.  
    1.  Öffnen Sie in Ihrem WebView2-Projekt das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Eigenschaften**aus.  
    1.  Wählen Sie unter den **Konfigurationseigenschaften**die Option **Debuggen**aus.  
    1.  Wählen Sie unter dem **Debuggertyp**die Option **JavaScript (WebView2)** aus.  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Visual Studio-Konfigurationseigenschaft "Debuggen"" lightbox="./media/enbjs.png":::
           Visual Studio-Konfigurationseigenschaft " **Debuggen** "  
        :::image-end:::  
        
Führen Sie die folgenden Aktionen aus, um Ihre WebView2-Anwendung zu debuggen.  

1.  Wenn Sie einen Haltepunkt im Quellcode festlegen möchten, zeigen Sie auf die linke Seite der Zeile, und wählen Sie einen Haltepunkt aus.  Der JS/TS-Debug-Adapter führt keine Quell Pfadzuordnung aus.  Sie müssen exakt denselben Pfad öffnen, der Ihrem WebView2 zugeordnet ist.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio-Haltepunkt hinzufügen" lightbox="./media/breakpoint.png"::: 
       Visual Studio-Haltepunkt hinzufügen  
    :::image-end:::  
    
1.  Zum Ausführen des Debuggers wählen Sie die Bit-Größe der Plattform aus, und wählen Sie dann die grüne Schaltfläche Wiedergabe neben dem **lokalen Windows-Debugger**aus.  Die Anwendung wird ausgeführt, und der Debugger stellt eine Verbindung mit dem ersten WebView2-Prozess her, der erstellt wird.  
    
    :::image type="complex" source="./media/run.png" alt-text=" Lokaler Windows-Debugger in Visual Studio" lightbox="./media/run.png"::: 
       **Lokaler Windows-Debugger** in Visual Studio  
    :::image-end:::  
    
1.  Suchen Sie in der **Debug-Konsole**die Ausgabe des Debuggers.  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio-Debug-Konsole" lightbox="./media/console.png"::: 
       Visual Studio- **Debug-Konsole**  
    :::image-end:::  
    
## [Visual Studio Code](#tab/visualstudiocode)  

Verwenden Sie Microsoft Visual Studio-Code zum Debuggen von Skripts, die in WebView2-Steuerelementen ausgeführt werden.  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

Führen Sie in Visual Studio-Code die folgenden Aktionen aus, um den Code zu debuggen. 

1.  Für Ihr Projekt ist eine Datei erforderlich `launch.json` .  Wenn Ihr Projekt keine Datei enthält `launch.json` , kopieren Sie den folgenden Codeausschnitt, und erstellen Sie eine neue `launch.json` Datei.  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",
        "env": {
            // Customize for your application location if needed
            "Path": "%path%;e:/path/to/your/application/location; "
        },
        "useWebView": true,
    ```  
    
1.  Wenn Sie einen Haltepunkt im Quellcode festlegen möchten, zeigen Sie auf die Zeile, und wählen Sie `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="Der Haltepunkt wird in Visual Studio-Code gesetzt" lightbox="./media/breakpointvs.png":::
       Der Haltepunkt wird in Visual Studio-Code gesetzt  
    :::image-end:::
    
    > [!NOTE]
    > Da Visual Studio-Code keine Quell Zuordnung ausführt, stellen Sie sicher, dass Sie Haltepunkte in derselben Datei festlegen, die von WebView2 verwendet wird.  Wenn die Pfade nicht übereinstimmen, wird der ausgeführte Code nicht vom Visual Studio-Code am Haltepunkt angehalten.  
    
1.  Führen Sie den Code aus.  
    1.  Wählen Sie auf der Registerkarte **Ausführen** im Dropdownmenü die Option Startkonfiguration aus.  
    1.  Wenn Sie mit dem Debuggen der Anwendung beginnen möchten, wählen Sie Debuggen starten (das grüne Dreieck neben der Dropdownliste Startkonfiguration) aus.  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Visual Studio-Registerkarte "Code ausführen"" lightbox="./media/runvs.png":::
           Visual Studio-Registerkarte "Code ausführen"  
        :::image-end:::  
        
1.  Öffnen Sie die **Debug-Konsole** , um die Debug-Ausgabe und die Fehler anzuzeigen.  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Visual Studio-Code Debug-Konsole" lightbox="./media/resultsvs.png":::
       Visual Studio-Code Debug-Konsole  
    :::image-end:::  
    
**Erweiterte Einstellungen**:  

*   Gezieltes WebView Debuggen 
    
    In einigen WebView2-Anwendungen können Sie mehr als ein WebView2-Steuerelement verwenden. So wählen Sie das WebView2-Steuerelement aus, das in dieser Situation gedebuggt werden soll Sie können das gezielte WebView2 Debuggen verwenden. 
    
    Öffnen `launch.json` und führen Sie die folgenden Aktionen aus, um ein gezieltes WebView-Debugging zu verwenden.  
    
    1.  Überprüfen Sie, ob der `useWebview` Parameter auf festgesetzt ist `true` .  
    1.  Fügen Sie den `urlFilter` Parameter hinzu.  Wenn das WebView2-Steuerelement zu einer URL navigiert, `urlFilter` wird der Parameterwert verwendet, um Zeichenfolgen zu vergleichen, die in der URL angezeigt werden.  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    Wenn Sie Ihre Anwendung debuggen, müssen Sie möglicherweise den Code vom Anfang des Rendering Prozesses aus durchlaufen. Wenn Sie Webseiten auf Websites Rendern und keinen Zugriff auf den Quellcode haben, können Sie die Option verwenden, da Webseiten nicht `?=value`  erkannte Parameter ignorieren.   
    
    > [!IMPORTANT]
    > Nachdem die erste Übereinstimmung in der URL gefunden wurde, wird der Debugger angehalten.  Zwei WebView2-Steuerelemente können nicht gleichzeitig gedebuggt werden, da der CDP-Port von allen WebView2-Steuerelementen freigegeben wird und eine einzelne Portnummer verwendet wird.  
    
*   Debuggen von ausgeführten Prozessen  
    
    Möglicherweise müssen Sie den Debugger an die ausgeführten WebView2-Prozesse anfügen. Aktualisieren Sie dazu `launch.json` den `request` Parameter in `attach` .
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    Das WebView2-Steuerelement muss den CDP-Port öffnen, um das Debuggen des WebView2-Steuerelements zu ermöglichen.  Ihr Code muss erstellt werden, um sicherzustellen, dass nur ein WebView2-Steuerelement einen CDP-Port (Chrome Developer Protocol) geöffnet hat, bevor der Debugger gestartet wird.  
    
*   Debug-Ablaufverfolgungsoptionen  
    
    Fügen Sie den zu `trace` launch.jsden Parameter hinzu, um die Debug-Ablaufverfolgung zu aktivieren.  
    
    1.  Parameter hinzufügen `trace` .  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Speichern Sie die Debug-Ausgabe in einer Protokolldatei." lightbox="./media/tracelog.png":::
                 Speichern der Debug-Ausgabe in einer Protokolldatei  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Ausführliche Ausgabe" lightbox="./media/verbose.png":::
                 Visual Studio-Code Debug-Ausgabe mit aktivierter ausführlicher Ablaufverfolgung  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   Debuggen von Office-Add-ins
    
    Wenn Sie Office-Add-ins Debuggen, öffnen Sie den Add-in-Quellcode in einer separaten Instanz von Visual Studio-Code.  Öffnen Sie launch.jsin ihrer WebView2-Anwendung, und fügen Sie den folgenden Codeausschnitt hinzu, um den Debugger an das Office-Add-in anzufügen.
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   Problembehandlung des Debuggers  
    
    Bei Verwendung des Debuggers können die folgenden Szenarien auftreten.  
    
    *   Der Debugger wird nicht am Haltepunkt angehalten, und Sie haben die Debug-Ausgabe.  Um das Problem zu beheben, stellen Sie sicher, dass die Datei mit dem Haltepunkt dieselbe Datei ist, die vom WebView2-Steuerelement verwendet wird.  Der Debugger führt keine Quell Pfadzuordnung aus.  
    *   Sie können nicht an einen ausgeführten Prozess anfügen, und Sie erhalten einen Timeoutfehler.  Um das Problem zu beheben, stellen Sie sicher, dass das WebView2-Steuerelement den CDP-Port geöffnet hat.  Stellen Sie sicher, dass Ihr  `additionalBrowserArguments`  Wert in der Registrierung richtig ist, oder die Optionen richtig sind.  Weitere Informationen finden Sie unter [additionalBrowserArguments für dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] und [additionalBrowserArguments für Win32][Webview2ReferenceWin32Webview2IdlParameters].  
    
* * *  

## Weitere Informationen  

*   Informationen zum Einstieg in die Verwendung von WebView2 finden Sie unter [WebView2 erste Schritte][Webview2MainGettingStarted].  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie im [WebView2Samples][GithubMicrosoftedgeWebview2samples] -Repo auf GitHub.
*   Ausführlichere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].
*   Weitere Informationen zu WebView2 finden Sie unter [WebView2-Ressourcen][Webview2MainNextSteps].
    
## Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "CoreWebView2EnvironmentOptions. AdditionalBrowserArguments-Eigenschaft (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment-Globals | Microsoft docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Was ist neu? -JavaScript-Debugger für Visual Studio-Code – Microsoft/vscode-js – Debuggen | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chrom) WebView-Anwendungen – Visual Studio-Code – Debugger für Microsoft Edge – Microsoft/vscode-Edge-debug2 | GitHub"  

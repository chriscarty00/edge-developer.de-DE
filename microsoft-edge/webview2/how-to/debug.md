---
description: Erfahren Sie, wie Sie WebView2-Steuerelemente debuggen.
title: Erste Schritte beim Debuggen von WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 01cd67897f7041bca0cedcee2cc3242f3ebcc962
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535964"
---
# <a name="get-started-debugging-webview2-apps"></a>Erste Schritte beim Debuggen von WebView2-Apps  

Das Ziel des Microsoft Edge WebView2-Steuerelements besteht in der Kombination der besten Features und Tools für die Web- und native App-Entwicklung.  Wenn Sie Ihre WebView2-App entwickeln, sollten Sie Ihre App debuggen.  In diesem Artikel werden die verschiedenen Tools beschrieben, die zum Debuggen ihres Web- und systemeigenen Codes in Ihrer WebView2-App verwendet werden.  

## [<a name="microsoft-edge-devtools"></a>Microsoft Edge DevTools](#tab/devtools)  

Verwenden [Microsoft Edge (Chromium)-Entwicklertools][DevtoolsGuideChromiumMain] zum Debuggen von Webinhalten, die in WebView2-Steuerelementen angezeigt werden, auf die gleiche Weise wie für eine andere Webseite, die in webView2-Steuerelementen angezeigt Microsoft Edge.  Zum Öffnen der DevTools legen Sie den Fokus auf das WebView-Steuerelement, und verwenden Sie dann eine der folgenden Aktionen.  

*   Wählen Sie `F12` aus.  
*   Wählen Sie `Ctrl` + `Shift` + `I` aus.  
*   Öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie `Inspect` aus.  
    
Weitere Informationen finden Sie unter [DevTools overview][DevtoolsGuideChromiumMain].  

:::image type="complex" source="./media/f12.png" alt-text="DevTools-Debugging" lightbox="./media/f12.png":::
   DevTools-Debugging  
:::image-end:::    

## [<a name="visual-studio"></a>Visual Studio](#tab/visualstudio)  

Visual Studio bietet verschiedene Debuggingtools für Web- und systemeigenen Code in WebView2-Apps.  Im Abschnitt Visual Studio liegt der Hauptfokus auf dem Debuggen von WebView-Steuerelementen, die anderen Methoden des Debuggens in Visual Studio sind jedoch wie gewohnt verfügbar.  Verwenden Sie den folgenden Prozess, um Web- und systemeigenen Code nur in Win32-Apps oder Office-Add-Ins zu debuggen.  

> [!IMPORTANT]
> Wenn Sie Ihre App in Visual Studio mit dem systemeigenen Debugger debuggen, kann die Auswahl den systemeigenen Debugger anstelle von `F12` Entwicklertools auslösen.  Wählen `Ctrl` + `Shift` + `I` Sie aus, oder verwenden Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), um die Situation zu vermeiden.  

Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Anforderungen erfüllt sind.  

*   Zum Debuggen von Skripts muss die App innerhalb eines Visual Studio.  
*   Sie können keinen Debugger an einen ausgeführten WebView2-Prozess anfügen.  
*   Installieren Visual Studio 2019, Version 16.4 Preview 2 oder höher.  
    
Installieren und Einrichten der Skriptdebuggertools in Visual Studio.  

1.  Führen Sie die folgenden Aktionen aus, um die **#A0** in der **Desktopentwicklung mit C++ zu installieren.**  
    1.  Geben Sie in Windows Explorerleiste `Visual Studio Installer` ein.  
    1.  Wählen **Visual Studio-Installer,** um es zu öffnen.  
    1.  Wählen Sie Visual Studio-Installer in der installierten Version die Schaltfläche **Mehr** aus, und wählen Sie dann **Ändern aus.**  
    1.  Wählen Visual Studio unter **Arbeitsauslastungen**die Einstellung **Desktopentwicklung in C++** aus.  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Visual Studio Ändern des Bildschirms für Arbeitsauslastungen" lightbox="./media/workloads.png":::
            Visual Studio Ändern des Bildschirms für Arbeitsauslastungen
        :::image-end:::  
        
    1.  Wählen **Sie Einzelne Komponenten aus.**  
    1.  Geben Sie im Suchfeld `JavaScript diagnostics` ein.  
    1.  Wählen Sie die **JavaScript-Diagnoseeinstellung** aus.  
    1.  Wählen Sie **Ändern**aus. 
        
        :::image type="complex" source="./media/indiv-comp.png" alt-text="Visual Studio Ändern der Registerkarte Einzelne Komponenten" lightbox="./media/indiv-comp.png":::
           Visual Studio Ändern der Registerkarte "Einzelne Komponenten"  
        :::image-end:::  
        
1.  Aktivieren sie das Skriptdebubuing für WebView2-Apps.  
    1.  Öffnen Sie in Ihrem WebView2-Projekt das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Eigenschaften aus.**  
    1.  Wählen Sie **unter Konfigurationseigenschaften** **Debuggen aus.**  
    1.  Wählen Sie **unter Debuggertyp** **JavaScript (WebView2)** aus.  
        
        :::image type="complex" source="./media/enb-js.png" alt-text="Visual Studio Debugkonfigurationseigenschaft" lightbox="./media/enb-js.png":::
           Visual Studio **Debugkonfigurationseigenschaft**  
        :::image-end:::  
        
Führen Sie die folgenden Aktionen aus, um Ihre WebView2-App zu debuggen.  

1.  Wenn Sie einen Haltepunkt im Quellcode festlegen, zeigen Sie links neben der Zeilennummer, und wählen Sie einen Haltepunkt aus.  Der JS/TS-Debugadapter führt keine Quellpfadzuordnung durch.  Sie müssen den exakt gleichen Pfad öffnen, der Mit WebView2 verknüpft ist.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio haltepunkt hinzufügen" lightbox="./media/breakpoint.png"::: 
       Visual Studio haltepunkt hinzufügen  
    :::image-end:::  
    
1.  Wählen Sie zum Ausführen des Debuggers die Bitgröße der Plattform aus, und wählen Sie dann die grüne Wiedergabeschaltfläche neben **Local Windows Debugger aus.**  Die App wird ausgeführt, und der Debugger stellt eine Verbindung mit dem ersten erstellten WebView2-Prozess sicher.  
    
    :::image type="complex" source="./media/run.png" alt-text=" Visual Studio Lokaler Windows Debugger" lightbox="./media/run.png"::: 
       Visual Studio Local **Windows Debugger**  
    :::image-end:::  
    
1.  Suchen Sie **in der Debugkonsole**nach der Ausgabe des Debuggers.  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio Debugkonsole" lightbox="./media/console.png"::: 
       Visual Studio Debug **console**  
    :::image-end:::  
    
## [<a name="visual-studio-code"></a>Visual Studio Code](#tab/visualstudiocode)  

Verwenden Microsoft Visual Studio Code zum Debuggen von Skripts, die in WebView2-Steuerelementen ausgeführt werden.  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

Führen Visual Studio Code die folgenden Aktionen aus, um Den Code zu debuggen. 

1.  Ihr Projekt muss über eine Datei `launch.json` verfügen.  Wenn Ihr Projekt keine Datei enthält, kopieren Sie den `launch.json` folgenden Codeausschnitt, und erstellen Sie eine neue `launch.json` Datei.  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",
        "env": {
            // Customize for your app location if needed
            "Path": "%path%;e:/path/to/your/app/location; "
        },
        "useWebView": true,
        // The following two lines setup source path mapping, where `url` is the start page of your app, and `webRoot` is the top level directory with all your code files.
        "url": "file:///${workspaceFolder}/path/to/your/toplevel/foo.html",
        "webRoot": "${workspaceFolder}/path/to/your/assets"
    ```  
    
    > [!NOTE]
    > Visual Studio Code Die Zuordnung des Quellpfads erfordert nun die URL, sodass Ihre App jetzt beim Starten einen Befehlszeilenparameter empfängt.  Sie können den Parameter bei Bedarf `url` sicher ignorieren.  
    
1.  Zum Festlegen eines Haltepunkts im Quellcode zeigen Sie auf die Zeile, und wählen Sie `F9`
    
    :::image type="complex" source="./media/breakpoint-vs.png" alt-text="Der Haltepunkt wird in Visual Studio Code" lightbox="./media/breakpoint-vs.png":::
       Der Haltepunkt wird in Visual Studio Code  
    :::image-end:::
    
1.  Führen Sie den Code aus.  
    1.  Wählen Sie **auf der** Registerkarte Ausführen im Dropdownmenü die Startkonfiguration aus.  
    1.  Wenn Sie mit dem Debuggen Ihrer App beginnen möchten, wählen Sie Debuggen starten aus. Dabei handelt es sich um das grüne Dreieck neben der Startkonfiguration.  
        
        :::image type="complex" source="./media/run-vs.png" alt-text="Visual Studio Code Registerkarte Ausführen" lightbox="./media/run-vs.png":::
           Visual Studio Code Registerkarte "Ausführen"  
        :::image-end:::  
        
1.  Öffnen **Sie die Debugkonsole,** um die Debugausgabe und Fehler anzeigen zu können.  
    
    :::image type="complex" source="./media/results-vs.png" alt-text=" Visual Studio Code Debugkonsole" lightbox="./media/results-vs.png":::
       Visual Studio Code Debugkonsole  
    :::image-end:::  
    
**Erweiterte Einstellungen**:  

*   Gezieltes Webview-Debugging. 
    
    In einigen WebView2-Apps können Sie mehrere WebView2-Steuerelemente verwenden. Zum Auswählen des zu debuggenden WebView2-Steuerelements in dieser Situation können Sie das gezielte Webview2-Debuggen verwenden. 
    
    Öffnen `launch.json` Und führen Sie die folgenden Aktionen aus, um das gezielte Webview-Debugging zu verwenden.  
    
    1.  Vergewissern Sie `useWebview` sich, dass der Parameter auf festgelegt `true` ist.  
    1.  Fügen Sie den Parameter `urlFilter` hinzu.  Wenn das WebView2-Steuerelement zu einer URL navigiert, wird der Parameterwert zum Vergleichen von Zeichenfolgen verwendet, `urlFilter` die in der URL angezeigt werden.  
        
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    Beim Debuggen Ihrer App müssen Sie den Code möglicherweise von Beginn des Renderingprozesses aus durchschritten. Wenn Sie Webseiten auf Websites rendern und keinen Zugriff auf den Quellcode haben, können Sie die Option verwenden, da Webseiten unbekannte Parameter `?=value`  ignorieren.   
    
    > [!IMPORTANT]
    > Nachdem die erste Übereinstimmung in der URL gefunden wurde, wird der Debugger beendet.  Sie können zwei WebView2-Steuerelemente nicht gleichzeitig debuggen, da der CDP-Port von allen WebView2-Steuerelementen gemeinsam genutzt wird und eine einzelne Portnummer verwendet.  
    
*   Debuggen ausgeführter Prozesse  
    
    Möglicherweise müssen Sie den Debugger an die Ausführung von WebView2-Prozessen anfügen. Aktualisieren Sie dazu in `launch.json` den Parameter `request` auf `attach` .
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    Ihr WebView2-Steuerelement muss den CDP-Port öffnen, um das Debuggen des WebView2-Steuerelements zu ermöglichen.  Ihr Code muss so erstellt werden, dass nur ein WebView2-Steuerelement über einen geöffneten Chrome Developer Protocol (CDP)-Port verfügt, bevor der Debugger gestartet wird.  
    
*   Debuggen von Ablaufverfolgungsoptionen  
    
    Fügen Sie den `trace` Parameter hinzu, launch.jsaktiviert werden soll, um die Debugablaufverfolgung zu aktivieren.  
    
    1.  `trace`Add-Parameter.  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/trace-log.png" alt-text=" Speichern Sie die Debugausgabe in einer Protokolldatei." lightbox="./media/trace-log.png":::
                 Speichern der Debugausgabe in einer Protokolldatei  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Ausführliche Ausgabe" lightbox="./media/verbose.png":::
                 Visual Studio Code Debuggen der Ausgabe mit aktivierter ausführlicher Ablaufverfolgung  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   Debuggen Office Add-Ins.  
    
    Öffnen Sie beim Debuggen Office Add-Ins den Add-In-Quellcode in einer separaten Instanz Visual Studio Code.  Öffnen launch.jsin Ihrer WebView2-App, und fügen Sie den folgenden Codeausschnitt hinzu, um den Debugger an das Office anfügen.
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   Problembehandlung beim Debugger  
    
    Bei Verwendung des Debuggers können die folgenden Szenarien auftreten.  
    
    *   Der Debugger wird nicht am Haltepunkt beendet, und Sie haben eine Debugausgabe.  Um das Problem zu beheben, vergewissern Sie sich, dass die Datei mit dem Haltepunkt dieselbe Datei ist, die vom WebView2-Steuerelement verwendet wird.  Der Debugger führt keine Quellpfadzuordnung durch.  
    *   Sie können keinen laufenden Prozess anfügen, und Es wird ein Timeoutfehler angezeigt.  Um das Problem zu beheben, vergewissern Sie sich, dass das WebView2-Steuerelement den CDP-Port geöffnet hat.  Stellen Sie  `additionalBrowserArguments`  sicher, dass der Wert in der Registrierung korrekt ist oder die Optionen richtig sind.  Weitere Informationen finden Sie unter [additionalBrowserArguments for dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] und [additionalBrowserArguments for Win32][Webview2ReferenceWin32Webview2IdlParameters].  
        
* * *  

## <a name="see-also"></a>Weitere Informationen  

*   Um mit WebView2 zu beginnen, navigieren Sie zu [WebView2 Erste Schritte Guides][Webview2MainGetStarted].  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie im [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samples] GitHub.
*   Weitere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].
*   Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2MainNextSteps].
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "CoreWebView2EnvironmentOptions.AdditionalBrowserArguments Property (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment – Globale | Microsoft Docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webview2MainGetStarted]: ../index.md#get-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

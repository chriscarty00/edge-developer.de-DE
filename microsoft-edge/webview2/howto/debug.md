---
description: Erfahren Sie, wie Sie WebView2-Steuerelemente Debuggen.
title: Erste Schritte beim Debuggen von WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/13/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: dcdeeadc2c25bcf50834176706b8d181f06f994a
ms.sourcegitcommit: 6c7ededf8677fd7add5e4060e92f9ec4cfdb6952
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "10927909"
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

    1. Geben Sie in der Windows-Explorer-Leiste ein `Visual Studio Installer` .  
    1. Wählen Sie **Visual Studio-Installationsprogramm** aus, um es zu öffnen.  
    1. Wählen Sie im Visual Studio-Installationsprogramm in der installierten Version die Schaltfläche **mehr** aus, und wählen Sie dann **ändern**aus.  
    1. Wählen Sie in Visual Studio unter **Arbeits auslasten**die Einstellung **Desktop Entwicklung in C++** aus.  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Bildschirm ' Ändern von Arbeitslasten ' in Visual Studio" lightbox="./media/workloads.png":::
            Bildschirm ' Ändern von Arbeitslasten ' in Visual Studio :::image-end:::  
        
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
    
* * *  

## Weitere Informationen  

*   Informationen zum Einstieg in die Verwendung von WebView2 finden Sie unter [WebView2 erste Schritte][Webview2MainGettingStarted].  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie im [WebView2Samples][GithubMicrosoftedgeWebview2samples] -Repo auf GitHub.
*   Ausführlichere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].
*   Weitere Informationen zu WebView2 finden Sie unter [WebView2-Ressourcen][Webview2MainNextSteps].

## Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools"  

[Webview2ReferenceDotnet09515MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-515/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions Klasse | Microsoft docs"  
[Webview2ReferenceWin3209538Webview2IdlParameters]: ../reference/win32/0-9-538/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-Globals | Microsoft docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Was ist neu? -JavaScript-Debugger für Visual Studio-Code – Microsoft/vscode-js – Debuggen | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chrom) WebView-Anwendungen – Visual Studio-Code – Debugger für Microsoft Edge – Microsoft/vscode-Edge-debug2 | GitHub"  

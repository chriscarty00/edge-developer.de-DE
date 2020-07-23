---
description: Erfahren Sie, wie Sie WebView2-Steuerelemente Debuggen.
title: Debuggen von WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ad6f334e5796d2f22146f2853ae1ef1d854e329c
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894319"
---
# Debuggen mit WebView2  

Das Ziel des Microsoft Edge WebView2-Steuerelements ist die Kombination der besten Features der Web-und nativen Anwendungsentwicklung sowie der Entwicklertools.  Auf der folgenden Seite werden die verschiedenen Tools erläutert, die bei der Entwicklung mit WebView2-Steuerelementen zu verwenden sind.  

## Microsoft Edge DevTools  

Verwenden Sie [Microsoft Edge (Chrom)-Entwickler Tools][DevtoolsGuideChromiumMain] zum Debuggen von Webinhalten, die in WebView2-Steuerelementen angezeigt werden, auf die gleiche Weise wie Microsoft Edge.  Um das devtools zu öffnen, setzen Sie den Fokus auf das WebView-Fenster, und verwenden Sie dann eine der folgenden Aktionen.  
*   Wählen Sie aus `F12` .  
*   Wählen Sie aus `Ctrl` + `Shift` + `I` .  
*   Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) > auswählen `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   Microsoft Edge DevTools  
:::image-end:::  

> [!NOTE]
> Wenn Sie die Anwendung in Visual Studio debuggen, wobei der systemeigene Debugger angefügt ist, wird durch Drücken `F12` möglicherweise der systemeigene Debugger anstelle der Entwickler Tools ausgelöst.  Drücken Sie `Ctrl` + `Shift` + `I` , oder verwenden Sie das Kontextmenü \ (mit der rechten Maustaste auf \), um die Situation zu vermeiden.  

> [!NOTE]
> Sie können das `--auto-open-devtools-for-tabs` Befehlszeilenargument verwenden, um ein neues devtools-Fenster zu öffnen, wenn Sie das erste Mal eine WebView erstellen.  <!--See `CreateCoreWebView2Controller` documentation for how to provide additional command-line arguments to the browser process.  See `LoaderOverride` registry key to examine different builds of WebView2 without modifying your application in the `CreateCoreWebView2Controller` documentation.  -->  

## Visual Studio  

Verwenden Sie den Skriptdebugger in Visual Studio 2019, Version 16,4 Preview 2 oder höher, um Ihr Skript in Visual Studio zu debuggen.  Überprüfen Sie, ob die Komponente **JavaScript-Diagnose** in der **Desktop Entwicklung mit C++** -Arbeitsauslastung installiert ist.  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Visual Studio-JavaScript-Diagnose":::
   Visual Studio-JavaScript-Diagnose  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Zum Aktivieren des WebView2-Skript Debuggens öffnen Sie das Kontextmenü \ (mit der rechten Maustaste auf \) in Ihrem Projekt, > **Eigenschaften**auswählen.  

*   Wählen Sie unter **Konfigurationseigenschaften**die Option **Debuggen**aus.  
*   Wählen Sie in der Eigenschaft **Debuggertyp** in der Liste der Optionen **JavaScript (WebView2)** aus. 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Visual Studio-JavaScript-Debugger":::
   Visual Studio-JavaScript-Debugger  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Sie sind alle eingerichtet und können Debuggen.  

Führen Sie zum Debuggen die folgenden Aktionen aus.  

1.  Festlegen von Haltepunkten  
    *   Öffnen Sie die Skriptdatei, und legen Sie den Haltepunkt an die gewünschte Stelle.  
        
        > [!NOTE]
        > Der JS/TS-Debug-Adapter führt keine Quellpfad-Zuordnung aus.Sie müssen exakt denselben Pfad öffnen, der Ihrem WebView2 zugeordnet ist.  
        
1.  Ausführen von Code  
    *   Wählen Sie die geeignete Build-Flavor-und Laufzeitumgebung aus, und starten Sie dann den lokalen Windows-Debugger.  
1.  Anzeigen der Debug-Konsole  
    *   Die Anwendung wird ausgeführt, und der Debugger stellt eine Verbindung her, nachdem die erste webview2 erstellt wurde.Alle ausstehenden Debug-Ausgaben werden angezeigt.  
        
        > [!NOTE]
        > Diese Methode des Debuggens ist derzeit auf Win32-Anwendungen und Office-Add-ins beschränkt.  
        
## Visual Studio Code  

Sie können Visual Studio-Code verwenden, um Skripts zu debuggen, die in WebView2-Steuerelementen ausgeführt werden.  Weitere Informationen finden Sie unter [Microsoft Edge (Chrom) WebView-Anwendungen][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].  

<!--todo:  add See also heading  -->  

## Kontakt mit dem Microsoft Edge WebView-Team  

Helfen Sie beim Aufbau einer reicheren WebView2-Erfahrung, indem Sie Ihr Feedback freigeben.  Besuchen Sie das [Feedback-Repo][GithubMicrosoftedgeWebviewfeedbackMain] , um Funktionsanforderungen oder Fehlerberichte einzureichen.  

<!--## Debugging  

Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`. You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView. See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process. Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.  -->  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chrom) WebView-Anwendungen-vs-Code-Debugger für Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  

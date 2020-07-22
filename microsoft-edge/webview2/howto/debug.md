---
description: Erfahren Sie, wie Sie WebView2-Steuerelemente Debuggen.
title: Debuggen von WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 232104abc360cfa660d567ffb66535213fcb3ae0
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888581"
---
# Debuggen mit WebView2  

Das Ziel des Microsoft Edge WebView2-Steuerelements ist die Kombination der besten Features der Web-und nativen Anwendungsentwicklung sowie der Entwicklertools.  Auf der folgenden Seite werden die verschiedenen Tools erläutert, die bei der Entwicklung mit WebView2-Steuerelementen zu verwenden sind.  

## Microsoft Edge DevTools  

Verwenden Sie die [Microsoft Edge (Chrom)-Entwickler Tools][DevtoolsMain] zum Debuggen von Webinhalten, die in WebView2-Steuerelementen angezeigt werden, auf die gleiche Weise wie bei Verwendung von Microsoft Edge.  Um das devtools zu öffnen, setzen Sie den Fokus auf das WebView-Fenster, und verwenden Sie dann eine der folgenden Aktionen.  

*   Wählen Sie aus `F12` .  
*   Wählen Sie aus `Ctrl` + `Shift` + `I` .  
*   Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie aus `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   Microsoft Edge DevTools  
:::image-end:::  

> [!IMPORTANT]
> Wenn Sie die Anwendung in Visual Studio debuggen, wobei der systemeigene Debugger angefügt ist, `F12` kann die Auswahl den systemeigenen Debugger anstelle der Entwickler Tools auslösen.  Verwenden Sie `Ctrl` + `Shift` + `I` das Kontextmenü, oder klicken Sie mit der rechten Maustaste auf \), um die Situation zu vermeiden.  

## Visual Studio  

Sie können Visual Studio verwenden, um Anwendungscode und Debug-Skripts zur gleichen Zeit zu entwickeln.  

Beachten Sie die folgenden Punkte.  

*   Visual Studio unterstützt nur das Debuggen von Skripts, wenn die app in Visual Studio gestartet wird.  \ (Das Anfügen eines ausgeführten Prozesses zum Debuggen wird nicht unterstützt. \)  
*   Das Debugging-Szenario für zielgerichtete WebView wird nicht unterstützt.  

Verwenden Sie den Skriptdebugger in Visual Studio 2019, Version 16,4 Preview 2 oder höher, um Ihr Skript in Visual Studio zu debuggen.  

Richten Sie den Debugger ein.  

*   Überprüfen Sie, ob die Komponente **JavaScript-Diagnose** in der **Desktop Entwicklung mit C++** -Arbeitsauslastung installiert ist.  
    
    1.  Navigieren Sie zu **apps & Features** -Einstellungen in Windows.  Suchen Sie es mithilfe der Windows-Taskleiste.  
    1.  Wählen Sie **ändern**aus.  
    1.  Überprüfen Sie, ob die Kontrollkästchen **JavaScript-Diagnose** und **Desktop Entwicklung in C++** aktiviert sind.  
        
        :::image type="complex" source="../media/appsandfeatures.png" alt-text="Apps & Features" lightbox="../media/appsandfeatures.png":::
           Apps & Features  
        :::image-end:::  
        
*   Aktivieren Sie das WebView2-Skriptdebugging.  
    1.  Zeigen Sie mit der Maus auf das Projekt, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Eigenschaften**aus.  
    1.  Wählen Sie unter **Konfigurationseigenschaften**die Option **Debuggen**aus.  
    1.  Suchen Sie in der Eigenschaft **Debuggertyp** in der Liste der Optionen, und wählen Sie **JavaScript (WebView2)** aus.  
        
        :::image type="complex" source="../media/enbjs.png" alt-text="Visual Studio-JavaScript-Debugger" lightbox="../media/enbjs.png":::
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

Sie können Visual Studio-Code verwenden, um Skripts zu debuggen, die in WebView2-Steuerelementen ausgeführt werden.  Weitere Informationen finden Sie unter [Microsoft Edge (Chrom) WebView-Anwendungen][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].  

<!--todo:  add See also heading  -->  

## Kontakt mit dem Microsoft Edge WebView-Team  

Helfen Sie beim Aufbau einer reicheren WebView2-Erfahrung, indem Sie Ihr Feedback freigeben.  Besuchen Sie das [Feedback-Repo][GithubMicrosoftedgeWebviewfeedback] , um Funktionsanforderungen oder Fehlerberichte einzureichen.  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chrom) WebView-Anwendungen – vs-Code – Debugger für Microsoft Edge | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

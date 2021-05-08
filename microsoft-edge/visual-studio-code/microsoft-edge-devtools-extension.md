---
description: Verwenden von Elementen für Microsoft Edge (Chromium) aus Visual Studio Code
title: Elemente für Microsoft Edge (Chromium) aus Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, vs code, visual studio code, elements
ms.openlocfilehash: 83bac187fa2a9b1766a52f3f2cd176f171846e02
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398455"
---
# <a name="microsoft-edge-devtools-for-visual-studio-code-extension"></a>Microsoft Edge DevTools für Visual Studio Code Erweiterung  

Verwendung <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] -->diese Erweiterung für den Zugriff in Microsoft Edge DevTools innerhalb [Microsoft Visual Studio Code .][VisualstudioCode]  Sie haben Zugriff auf die **Elemente** **und** Netzwerktools in Microsoft Edge DevTools.  Sie können eine Instanz der Datei entweder starten oder Microsoft Edge.  Nachdem Sie eine Verbindung hergestellt haben, können Sie die Laufzeit-HTML-Struktur anzeigen, das Layout ändern, Formatierungsprobleme beheben und den Netzwerkdatenverkehr überprüfen.  

## <a name="elements-tool"></a>Elementtool  

Standardmäßig startet die Erweiterung eine Browserinstanz in einem eindeutigen Fenster und bietet Ihnen die **Elements-Funktionalität** Microsoft Edge DevTools.  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools für Visual Studio Code, die mit einem vollständigen Browserfenster ausgeführt werden" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   Microsoft Edge DevTools für Visual Studio Code, die mit einem vollständigen Browserfenster ausgeführt werden  
:::image-end:::  

In den Erweiterungseinstellungen können Sie weitere Funktionen wie **headless Mode** und **Network aktivieren.**  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Aktivieren (oder Deaktivieren) des kopflosen Modus und der Netzwerkprüfung in den Erweiterungseinstellungen" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   Aktivieren des kopflosen Modus \(oder Deaktivieren\) und Netzwerkprüfung in den Erweiterungseinstellungen  
:::image-end:::  

## <a name="headless-mode"></a>Kopfloser Modus  

Im kopflosen Modus startet diese Erweiterung keine vollständige Browserinstanz zum Debuggen.  Es wird eine Instanz im Hintergrund ausgeführt.  Möglicherweise müssen Sie im Editor bleiben und mit dem eingebetteten Browser interagieren.  Ein zusätzliches Browsersymbol wird nicht in der Taskleiste angezeigt.  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools für Visual Studio Code, die ohne Kopf ausgeführt werden" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   Microsoft Edge DevTools für Visual Studio Code, die mit einem kopflosen Browser ausgeführt werden  
:::image-end:::  

> [!NOTE]
> Unter macOS sollten Sie den Kopflosenmodus als bevorzugten Modus aktivieren.  Die Verwendung des Kopflosenmodus sollte ein Problem lösen, bei dem das Browserfenster meldet, dass es sich um handelt, wenn das Fenster nicht sichtbar `Not Active` ist.  

## <a name="network-tool"></a>Network-Tool  

Wenn Sie auch den Netzwerkdatenverkehr Ihrer Anwendung überprüfen möchten, öffnen Sie die Einstellungen, und aktivieren Sie **die** Registerkarte Netzwerk.  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Netzwerkprüfung in Microsoft Edge DevTools für Visual Studio Code" lightbox="./media/edge-devtools-for-vscode-network.png":::
    Netzwerkprüfung in Microsoft Edge DevTools für Visual Studio Code  
:::image-end:::  

## <a name="launching-microsoft-edge-from-the-extension"></a>Starten Microsoft Edge aus der Erweiterung  

Navigieren Sie zu Microsoft Edge Tools in der **Aktivitätsleiste**.  Neben der Stelle, Microsoft Edge **Tools: Targets steht,** gibt es ein Pluszeichen, das den Browser für Ihre App öffnet.  Wenn Sie die **Option about:blank** auswählen, müssen Sie zu Ihrer Web-App im Browser navigieren, damit sie im Bereich Elemente in der Visual Studio Code. ****  

## <a name="launching-microsoft-edge-from-the-debug-view"></a>Starten Microsoft Edge aus der Debugansicht  

Wenn Sie die Verwendung der Debugansicht in Visual Studio Code gewohnt sind, greifen Sie Microsoft Edge DevTools darauf zu.  

1.  Navigieren Visual Studio Code zur Debugansicht 
    *   Wählen `Ctrl` + `Shift` + `D` Sie unter Windows/Linux \( `Command` + `Shift` + `D` unter macOS\) aus.  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  Wenn sie keine Konfigurationen in Visual Studio Code, führen Sie eine der folgenden Aktionen aus.  
>     *   Wählen Sie `F5` aus.  
>     *   Wählen Sie **die Schaltfläche** Wiedergabe \(grün\) aus.  
> 1.  Wählen Sie im Dropdownmenü **Edge** aus.  
> 1.  Es `launch.json` sollte eine Datei angezeigt werden, die die folgende Konfiguration enthält.  
>     
>     ```json
>     {
>       "version": "0.2.0",
>       "configurations": [
>         {
>           "name": "Launch Microsoft Edge and open the Edge DevTools",
>           "request": "launch",
>           "type": "vscode-edge-devtools.debug",
>           "url": "http://localhost:8080"
>         }
>       ]
>     }
>     ```  
>     
> Führen Sie nach dem Laden der richtigen Konfiguration die folgende Aktion aus.  

1.  Führen Sie zum Starten des **Elements-Visual Studio Code** eine der folgenden Aktionen aus. 
    *   Wählen Sie `F5` aus.  
    *   Wählen Sie **die Schaltfläche** Wiedergabe \(grün\) aus.  
         
Jetzt können Sie die folgenden Aktionen ausführen.  

*   Greifen Sie auf einen Screencast Ihres Browsers zu.  
*   Überprüfen Sie das DOM und die Formatierung der Komponenten auf Ihrer Seite.  

## <a name="attaching-to-microsoft-edge"></a>Anfügen an Microsoft Edge  

Führen Sie die folgenden Schritte aus, um einen Browser zu öffnen und die Instanz Visual Studio Code anfügen. 

1.  Um eine Instanz von Microsoft Edge \(Chromium\) zu öffnen, kopieren Und führen Sie den folgenden Befehl aus.  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  Kopieren Sie nach dem Starten der Instanz den folgenden Codeausschnitt, und fügen Sie ihn in Die Datei `launch.json` ein.  
    
    ```json
    {
        "type": "vscode-edge-devtools.debug",
        "request": "attach",
        "name": "Attach to Microsoft Edge and open the developer tools",
        "url": "http://localhost:3000/",
        "webRoot": "${workspaceFolder}/out",
        "port": 9222
    }
    ```  
    
1.  Öffnen Visual Studio Code sie das Dropdownmenü **Debugger,** und wählen Sie An Microsoft Edge anhängen aus, und öffnen Sie **die Entwicklertools**.  
1.  Führen Sie zum Starten des **Elements-Visual Studio Code** eine der folgenden Aktionen aus. 
    *   Wählen Sie `F5` aus.  
    *   Wählen Sie **die Schaltfläche** Wiedergabe \(grün\) aus.  
         
Jetzt können Sie die folgenden Aktionen ausführen.  

*   Greifen Sie auf einen Screencast Ihres Browsers zu.  
*   Überprüfen Sie das DOM und die Formatierung der Komponenten auf Ihrer Seite.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-for-visual-studio-code-extension-team"></a>In Kontakt mit dem Microsoft Edge DevTools for Visual Studio Code Extension Team  

Senden Sie Ihr Feedback, [indem Sie ein Problem][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] gegen das GitHub [der][GithubMicrosoftVscodeEdgeDevtools] Erweiterung einreichen.  

Wenn Sie helfen möchten, <!--the Microsoft Edge DevTools for Visual Studio Code -->diese Erweiterung besser, Ihre Beiträge sind willkommen.  Finden Sie alles, was Sie benötigen, um im GitHub [der][GithubMicrosoftVscodeEdgeDevtools] Erweiterung zu beginnen.  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Neues Problem – microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code"  

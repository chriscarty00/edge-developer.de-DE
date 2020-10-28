---
description: Verwenden von Elementen für Microsoft Edge (Chrom) aus Visual Studio-Code
title: Elemente für Microsoft Edge (Chrom) aus Visual Studio-Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, vs-Code, Visual Studio-Code, Elemente
ms.openlocfilehash: 81488c08a76a16b80a415cbd17cd0617df916f54
ms.sourcegitcommit: 1cfcf2c8970a6c2221cfbf09a23d36b08bd60690
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "11135490"
---
# Microsoft Edge-devtools für Visual Studio-Code Erweiterung  

Verwendung <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] -->Diese Erweiterung für den Zugriff auf Microsoft Edge devtools in [Visual Studio-Code][VisualstudioCode].  Sie haben Zugriff auf die **Elemente** und **Netzwerk** Tools in Microsoft Edge devtools.  Sie können eine Instanz von Microsoft Edge entweder starten oder anfügen.  Nachdem Sie eine Verbindung hergestellt haben, können Sie die HTML-Laufzeitstruktur anzeigen, das Layout ändern, Styling-Probleme beheben und den Netzwerkdatenverkehr überprüfen.  

## Elemente-Tool  

Standardmäßig startet die Erweiterung eine Browserinstanz in einem eindeutigen Fenster und gibt Ihnen **die Funktionen von** Microsoft Edge devtools.  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge-devtools für Visual Studio-Code, der mit einem vollständigen Browserfenster ausgeführt wird" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   Microsoft Edge-devtools für Visual Studio-Code, der mit einem vollständigen Browserfenster ausgeführt wird  
:::image-end:::  

In den Erweiterungseinstellungen können Sie mehr Funktionen wie headless- **Modus** und **Netzwerk**aktivieren.  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Microsoft Edge-devtools für Visual Studio-Code, der mit einem vollständigen Browserfenster ausgeführt wird" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   Aktivieren von \ (oder deaktivieren \) Headless-Modus und Netzwerkprüfung in den Erweiterungseinstellungen  
:::image-end:::  

## Headless-Modus  

Im Headless-Modus wird mit dieser Erweiterung keine vollständige Browserinstanz zum Debuggen gestartet.  Sie führt eine Instanz im Hintergrund aus.  Möglicherweise müssen Sie im Editor bleiben und mit dem eingebetteten Browser interagieren.  In der Taskleiste wird kein zusätzliches Browser Symbol angezeigt.  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge-devtools für Visual Studio-Code, der mit einem vollständigen Browserfenster ausgeführt wird" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   Microsoft Edge-devtools für Visual Studio-Code, der mit einem headless-Browser ausgeführt wird  
:::image-end:::  

> [!NOTE]
> Unter macOS sollten Sie den Modus "headless" als bevorzugten Modus aktivieren.  Bei Verwendung des Headless-Modus sollte ein Problem gelöst werden, bei dem das Fenster im Browserfenster, wenn es nicht sichtbar ist `Not Active` .  

## Netzwerktool  

Wenn Sie auch den Netzwerkdatenverkehr Ihrer Anwendung prüfen möchten, öffnen Sie die Einstellungen, und aktivieren Sie die Registerkarte **Netzwerk** .  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Microsoft Edge-devtools für Visual Studio-Code, der mit einem vollständigen Browserfenster ausgeführt wird" lightbox="./media/edge-devtools-for-vscode-network.png":::
    Netzwerk Inspektion in Microsoft Edge devtools for Visual Studio-Code  
:::image-end:::  

## Starten von Microsoft Edge aus der Erweiterung  

Navigieren Sie in der **Aktivitäts Leiste**zu Microsoft Edge Tools.  Neben der Position, an der **Microsoft Edge Tools: Targets steht,** gibt es ein Pluszeichen, mit dem der Browser für Ihre APP geöffnet wird.  Wenn Sie die Option **about: blank** auswählen, müssen Sie im Browser zu Ihrer Web-App navigieren, damit Sie im Visual Studio-Code im Panel **Elemente** angezeigt wird.  

## Starten von Microsoft Edge aus der Ansicht "Debuggen"  

Wenn Sie es gewohnt sind, die Debugansicht in Visual Studio-Code zu verwenden, greifen Sie auf Microsoft Edge devtools.  

1.  Navigieren Sie in Visual Studio-Code zur Debug-Ansicht. 
    *   Wählen Sie `Ctrl` + `Shift` + `D` unter Windows/Linux \ ( `Command` + `Shift` + `D` unter macOS).  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  Wenn Sie keine Konfigurationen in Visual Studio-Code haben, führen Sie eine der folgenden Aktionen aus.  
>     *   Wählen Sie aus `F5` .  
>     *   Wählen Sie die Schaltfläche " **Wiedergabe** \ (grün \)" aus.  
> 1.  Wählen Sie im Dropdownmenü die Option **Edge** in der Dropdownliste aus.  
> 1.  `launch.json`Es sollte eine Datei mit der folgenden Konfiguration angezeigt werden.  
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
> Nachdem Sie die richtige Konfiguration geladen haben, führen Sie die folgende Aktion aus.  

1.  Führen Sie eine der folgenden Aktionen aus, um das **Element** Tool aus Visual Studio-Code zu starten. 
    *   Wählen Sie aus `F5` .  
    *   Wählen Sie die Schaltfläche " **Wiedergabe** \ (grün \)" aus.  
         
Nun können Sie die folgenden Aktionen ausführen:  

*   Greifen Sie auf einen Screencast Ihres Browsers zu.  
*   Überprüfen Sie das DOM und die Formatierung der Komponenten auf der Seite.  

## Anfügen an Microsoft Edge  

Führen Sie die folgenden Schritte aus, um einen Browser zu öffnen und die Instanz an Visual Studio-Code anzufügen. 

1.  Wenn Sie eine Instanz von Microsoft Edge \ (Chrom \) öffnen möchten, kopieren Sie den folgenden Befehl, und führen Sie ihn aus.  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  Nachdem die Instanz gestartet wurde, kopieren Sie den folgenden Codeausschnitt in Ihre Datei, und fügen Sie ihn ein `launch.json` .  
    
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
    
1.  Öffnen Sie in Visual Studio-Code das Dropdownmenü **Debugger** , und wählen Sie **an Microsoft Edge anfügen aus, und öffnen Sie die Entwicklertools**.  
1.  Führen Sie eine der folgenden Aktionen aus, um das **Element** Tool aus Visual Studio-Code zu starten. 
    *   Wählen Sie aus `F5` .  
    *   Wählen Sie die Schaltfläche " **Wiedergabe** \ (grün \)" aus.  
         
Nun können Sie die folgenden Aktionen ausführen:  

*   Greifen Sie auf einen Screencast Ihres Browsers zu.  
*   Überprüfen Sie das DOM und die Formatierung der Komponenten auf der Seite.  
    
## Kontaktieren des Microsoft Edge devtools for Visual Studio-Code Erweiterungs Teams  

Senden Sie Ihr Feedback, indem Sie [ein Problem][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] mit dem [GitHub-Repo][GithubMicrosoftVscodeEdgeDevtools] der Erweiterung einreichen.  

Wenn Sie helfen möchten, <!--the Microsoft Edge DevTools for Visual Studio Code -->Diese Erweiterung besser, ihre Beiträge sind willkommen.  Finden Sie alles, was Sie für den Einstieg in das [GitHub-Repo][GithubMicrosoftVscodeEdgeDevtools] der Erweiterung benötigen.  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio-Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio-Code"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Neues Problem-Microsoft/vscode-Edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge-Tools für vs-Code"  

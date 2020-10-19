---
description: Verwenden von Elementen für Microsoft Edge (Chrom) aus vs-Code
title: Elemente für Microsoft Edge (Chrom) aus vs-Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, vs-Code, Visual Studio-Code, Elemente
ms.openlocfilehash: ef516d8364c68b550f889bcad0fe762a73ce5f99
ms.sourcegitcommit: 652009c5cea9e75c22b077f0cbcdc0d96bd337ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "10694862"
---
# Elemente für Microsoft Edge vs Code Extension  

Mit den [Elementen für Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] vs Code Extension verwenden Sie das Tool Elemente des Microsoft Edge-Browsers in [Visual Studio-Code][VisualstudioCode].  Durch Starten oder Anfügen wird das elementtool mit einer Instanz von Microsoft Edge verbunden, zeigt die HTML-Laufzeitstruktur an und ermöglicht Ihnen, das Layout zu ändern oder Formatierungsprobleme zu beheben.  

:::image type="complex" source="./media/elements-for-edge.gif" alt-text="Elemente für Edge-vs-Code Erweiterung am Arbeitsplatz":::
   Elemente für Edge-vs-Code Erweiterung am Arbeitsplatz  
:::image-end:::

<!--![Elements for Edge VS Code extension at work][ImageGifElementsEdge]  -->  

## Starten von Microsoft Edge aus der Elements-Erweiterung  

Navigieren Sie zu Elementen in der **Aktivitäts Leiste**.  Neben der Position &quot; **Elemente für Microsoft Edge: Ziele** &quot; gibt es ein Pluszeichen, mit dem der Browser für Ihre APP geöffnet wird.  Wenn Sie die Option **about: blank** ausgewählt haben, müssen Sie im Browser zu Ihrer Web-App navigieren, damit Sie im vs-Code im Bedienfeld &quot;Elemente&quot; angezeigt wird.  

## Starten von Microsoft Edge aus der Ansicht &quot;Debuggen&quot;  

Wenn Sie es gewohnt sind, die Debugansicht in Visual Studio-Code zu verwenden, greifen Sie auf Elemente dieses Tools zu.  Navigieren Sie zur Debugansicht \ ( `Ctrl` + `Shift` + `D` unter Windows oder `Command` + `Shift` + `D` unter macOS \).  

Wenn Sie keine Konfigurationen im vs-Code haben, drücken Sie `F5` Windows oder macOS oder wählen Sie die grüne **Wiedergabe** Schaltfläche. Wählen Sie in der Dropdownliste die Option **Edge** aus. Es sollte eine `launch.json` Datei mit der folgenden Konfiguration angezeigt werden.  

```json
{
    &quot;version&quot;: &quot;0.2.0&quot;,
    &quot;configurations&quot;: [
        {
            
            &quot;name&quot;: &quot;Launch Microsoft Edge and open the Elements tool&quot;,
            &quot;request&quot;: &quot;launch&quot;,
            &quot;type&quot;: &quot;vscode-edge-devtools.debug&quot;,
            &quot;url&quot;: &quot;http://localhost:3000"
        
        }
    ]
}
```  

Nachdem Sie nun die richtige Konfiguration geladen haben, drücken Sie entweder `F5` Windows oder macOS oder wählen Sie die grüne **Wiedergabe** Schaltfläche. Das für Sie vertraute Elemente-Tool aus dem Microsoft Edge-Browser wird im vs-Code gestartet, sodass Sie auf einen Screencast Ihres Browsers zugreifen und die Komponenten Ihrer Seite untersuchen können.  

## Anfügen an Microsoft Edge  

Wenn Sie vs-Code an eine Instanz von Microsoft Edge \ (Chrom \) anfügen möchten, müssen Sie den Browser starten, indem Sie den folgenden Befehl von Ihrem Terminal aus ausführen.  

`start msedge --remote-debugging-port=9222`  

Nachdem die APP gestartet wurde, fügen Sie die folgende Konfiguration zu Ihrem **launch.jsin** Datei hinzu:  

```json
{
    "type": "vscode-edge-devtools.debug",
    "request": "attach",
    "name": "Attach to Microsoft Edge and open the Elements tool",
    "url": "http://localhost:3000/",
    "webRoot": "${workspaceFolder}/out",
    "port": 9222
}
```  

Wählen Sie **an Microsoft Edge anfügen aus, und öffnen Sie das elementtool** aus dem Dropdownmenü Debugger.  Drücken Sie dann entweder `F5` auf Windows oder macOS oder wählen Sie die grüne **Wiedergabe** Schaltfläche.  Im vs-Code wird das elementtool gestartet, sodass Sie auf einen Screencast Ihres Browsers zugreifen, das DOM und die Formatierung der Komponenten auf der Seite überprüfen können.  

## Mit den Elementen für Microsoft Edge vs Code Extension Team in Verbindung treten  

Senden Sie Ihr Feedback, indem Sie [ein Problem][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] mit dem [GitHub-Repo][GithubMicrosoftVscodeEdgeDevtools] der Erweiterung einreichen.  

Wenn Sie helfen möchten, die Elemente für Microsoft Edge vs Code Extension besser zu gestalten, sind Ihre Beiträge Willkommen!  Finden Sie alles, was Sie für den Einstieg in das [GitHub-Repo][GithubMicrosoftVscodeEdgeDevtools] der Erweiterung benötigen.  

<!-- image links -->  

<!--[ImageGifElementsEdge]: ./media/elements-for-edge.gif "Elements for Edge VS Code extension in action"  -->  
[ImagePngElementsEdge]:./Media/elements-for-edge.png "Elemente für Edge-vs-Code Erweiterung in Aktion"  

<!--links -->  

[VscodeElementsEdge]: ./elements-for-edge.md "Elemente für Microsoft Edge vs Code Extension | Microsoft docs"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio-Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio-Code"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Neues Problem-Microsoft/vscode-Edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elemente für Microsoft Edge (Chrom) | Visual Studio Marketplace"  

---
description: Debuggen von Microsoft Edge (Chromium) und Microsoft Edge (EdgeHTML) aus Visual Studio Code
title: Debuggen von Microsoft Edge (Chromium) Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, vs code, visual studio code, debugger
ms.openlocfilehash: e36348fc1ef5e30a511e6eda73c7646a85d8717e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399295"
---
# <a name="debugger-for-microsoft-edge-visual-studio-code-extension"></a>Debugger für Microsoft Edge Visual Studio Codeerweiterung  

Debuggen Sie mit dem [Debugger für Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Codeerweiterung Ihre Front-End-JavaScript-Codezeile zeile für Zeile, und sehen Sie anweisungen direkt aus Visual Studio `console.log()` [Code][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Debugger für Edge Visual Studio Codeerweiterung bei der Arbeit" lightbox="./media/debugger-for-edge.gif":::
   Debugger für Edge Visual Studio Codeerweiterung bei der Arbeit  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <a name="launching-microsoft-edge"></a>Starten von Microsoft Edge  

Navigieren Sie in der Aktivitätsleiste zur Debugansicht \( unter Windows oder `Ctrl` + `Shift` + `D` `Command` + `Shift` + `D` unter macOS\). ****  Wenn Sie keine Konfigurationen in Visual Studio Code haben, wählen Sie unter Windows oder macOS aus, oder wählen Sie die grüne Schaltfläche `F5` Wiedergabe aus. ****  Wählen **Sie im Dropdownmenü** Edge aus.  Es sollte eine Datei `launch.json` mit der folgenden Konfiguration angezeigt werden.  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "edge",
            "request": "launch",
            "name": "Launch Edge against localhost",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```  

Wenn Sie unter Windows oder macOS auswählen oder erneut die grüne Schaltfläche "Wiedergabe" auswählen, startet `F5` Visual Studio Code Microsoft Edge \(EdgeHTML\) und Sie können jedes Webprojekt debuggen, das Sie im Port ausgeführt haben, direkt aus Visual Studio **** `8080` Code!  

### <a name="microsoft-edge-chromium"></a>Microsoft Edge (Chromium)  

Wenn Sie Microsoft Edge \(Chromium\) starten möchten, fügen Sie dem neuen Microsoft Edge anstelle von Microsoft Edge \(EdgeHTML\) einfach ein Attribut zu Ihrer vorhandenen Konfiguration mit der Version von Microsoft Edge \(Chromium\) hinzu, die Sie `version` starten möchten \( `dev` , oder `beta` `canary` \).  Mit der folgenden Konfiguration wird die Canary-Version von Microsoft Edge \(Chromium\) gestartet.  

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Edge against localhost",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}"
}
```  

## <a name="attaching-to-microsoft-edge"></a>Anfügen an Microsoft Edge  

Fügen Visual Studio Code an Microsoft Edge \(Chromium\) an.  Führen Sie in Ihrem Terminal den folgenden Befehl aus.  

```shell
start msedge --remote-debugging-port=9222
```  

Fügen Sie der Datei die folgende Konfiguration `launch.json` hinzu.   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

Wenn Sie diese Konfiguration jetzt ausführen, Visual Studio Code an Microsoft Edge \(Chromium\) anfügen und mit dem Debuggen beginnen.  

## <a name="getting-in-touch-with-the-elements-for-microsoft-edge-visual-studio-code-extension-team"></a>Kontakt mit dem Team für Elemente für Microsoft Edge Visual Studio Codeerweiterung    

Senden Sie Ihr Feedback, [indem Sie ein Problem im][GithubMicrosoftVscodeEdgeDebug2NewIssue] [GitHub-Repository der][GithubMicrosoftVscodeEdgeDebug2] Erweiterung einreichen.  Fügen Sie die Protokolldatei des Debugadapters ein, die für jede Ausführung im Verzeichnis mit `%temp%` dem Namen erstellt `vscode-edge-debug2.txt` wird.  Ziehen Sie diese Datei in einen Problemkommentar, um sie auf GitHub hochzuladen.  

Um die Elemente für Microsoft Edge und Visual Studio Codeerweiterung zu verbessern, sind Ihre Beiträge willkommen!  Finden Sie alles, was Sie zum Einstieg in [das GitHub-Repository der][GithubMicrosoftVscodeEdgeDebug2] Erweiterung benötigen.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]: ./media/debugger-for-edge.png "Debugger für Edge Visual Studio Codeerweiterung in Aktion"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "microsoft/vscode-edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Neues Problem – microsoft/vscode-edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

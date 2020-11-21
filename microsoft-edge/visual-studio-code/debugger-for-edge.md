---
description: Debuggen von Microsoft Edge (Chrom) und Microsoft Edge (EdgeHTML) aus Visual Studio-Code
title: Debuggen von Microsoft Edge (Chrom) aus Visual Studio-Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, vs-Code, Visual Studio-Code, Debugger
ms.openlocfilehash: df15b76cc26ad01d3b8508362aa4b86998f8b41b
ms.sourcegitcommit: acf8ad7cb6c8ecf83a6170f8eeb9bec32878f8ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182505"
---
# Debugger für Microsoft Edge Visual Studio-Code Erweiterung  

Mit der [Debugger für Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio-Code Erweiterung Debuggen Sie den Front-End-JavaScript-Code Zeile für Zeile, und lesen Sie `console.log()` Anweisungen direkt aus [Visual Studio-Code][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Debugger für Edge Visual Studio-Code Erweiterung am Arbeitsplatz" lightbox="./media/debugger-for-edge.gif":::
   Debugger für Edge Visual Studio-Code Erweiterung am Arbeitsplatz  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## Starten von Microsoft Edge  

Navigieren Sie in der Aktivitäts Leiste zur Debugansicht \ ( `Ctrl` + `Shift` + `D` unter Windows oder `Command` + `Shift` + `D` unter macOS **Activity Bar**\).  Wenn Sie keine Konfigurationen in Visual Studio-Code haben, drücken Sie `F5` Windows oder macOS, oder wählen Sie die grüne Schaltfläche **Wiedergabe** aus.  Wählen Sie in der Dropdownliste die Option **Edge** aus.  Es sollte eine `launch.json` Datei mit der folgenden Konfiguration angezeigt werden.  

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

Wenn Sie `F5` Windows oder macOS drücken oder die grüne wieder **Gabe** -Schaltfläche erneut auswählen, startet Visual Studio-Code Microsoft Edge \ (EdgeHTML \), und Sie können jedes Webprojekt Debuggen, das Sie `8080` direkt im Visual Studio-Code auf Port ausgeführt haben!  

### Microsoft Edge (Chromium)  

Wenn Sie Microsoft Edge \ (Chrom \) starten möchten, fügen Sie dem neuen Microsoft Edge anstelle von Microsoft Edge \ (EdgeHTML \) einfach ein `version` Attribut zu Ihrer vorhandenen Konfiguration mit der Version von Microsoft Edge \ (Chromium \) hinzu, die Sie starten möchten \ ( `dev` , `beta` oder `canary` \).  In der folgenden Konfiguration wird die Canary-Version von Microsoft Edge (Chrom \) gestartet.  

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

## Anfügen an Microsoft Edge  

Anfügen von Visual Studio-Code an Microsoft Edge \ (Chrom \).  Führen Sie auf Ihrem Terminal den folgenden Befehl aus.  

```shell
start msedge --remote-debugging-port=9222
```  

Fügen Sie Ihrer Datei die unten aufgeführte Konfiguration hinzu `launch.json` .   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

Wenn Sie diese Konfiguration jetzt ausführen, wird Visual Studio-Code an Microsoft Edge \ (Chrom \) angefügt, und Sie können mit dem Debuggen beginnen.  

## Mit den Elementen für Microsoft Edge Visual Studio Code Extension Team in Verbindung treten    

Senden Sie Ihr Feedback, indem Sie im [GitHub Repo][GithubMicrosoftVscodeEdgeDebug2] der Erweiterung [ein Problem einreichen][GithubMicrosoftVscodeEdgeDebug2NewIssue] .  Fügen Sie die Debug-Adapter Protokolldatei ein, die für jeden Testlauf im `%temp%` Verzeichnis mit dem Namen erstellt wird `vscode-edge-debug2.txt` .  Ziehen Sie diese Datei in einen Problem Kommentar, um Sie in GitHub hochzuladen.  

Damit die Elemente für die Microsoft Edge Visual Studio-Code Erweiterung besser sind, sind Ihre Beiträge Willkommen!  Finden Sie alles, was Sie für den Einstieg in [GitHub Repo][GithubMicrosoftVscodeEdgeDebug2] der Erweiterung benötigen.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "Debugger für Edge Visual Studio-Code Erweiterung in Aktion"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio-Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio-Code"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Neues Problem-Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

---
description: Debuggen von Microsoft Edge (Chrom) und Microsoft Edge (EdgeHTML) aus vs-Code
title: Debuggen von Microsoft Edge (Chrom) aus vs-Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, vs-Code, Visual Studio-Code, Debugger
ms.openlocfilehash: 58bcbc927505f4c5a1f493349c3e9475cb75e1be
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695866"
---
# Debugger für Microsoft Edge-vs-Code Erweiterung  

Debuggen Sie mit dem [Debugger für Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] vs Code Extension den Front-End-JavaScript-Code Zeile für Zeile, und lesen Sie `console.log()` Anweisungen direkt aus [Visual Studio-Code][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Debugger für Edge-vs-Code Erweiterung am Arbeitsplatz&quot;:::
   Debugger für Edge-vs-Code Erweiterung am Arbeitsplatz  
:::image-end:::

<!--![Debugger for Edge VS Code extension at work][ImageGifDebuggerEdge]  -->  

## Starten von Microsoft Edge  

Navigieren Sie in der Aktivitäts Leiste zur Debugansicht \ ( `Ctrl` + `Shift` + `D` unter Windows oder `Command` + `Shift` + `D` unter macOS **Activity Bar**\).  Wenn Sie keine Konfigurationen im vs-Code haben, drücken Sie `F5` Windows oder macOS oder wählen Sie die grüne **Wiedergabe** Schaltfläche.  Wählen Sie in der Dropdownliste die Option **Edge** aus.  Es sollte eine `launch.json` Datei mit der folgenden Konfiguration angezeigt werden.  

```json
{
    &quot;version&quot;: &quot;0.2.0&quot;,
    &quot;configurations&quot;: [
        {
            &quot;type&quot;: &quot;edge&quot;,
            &quot;request&quot;: &quot;launch&quot;,
            &quot;name&quot;: &quot;Launch Edge against localhost&quot;,
            &quot;url&quot;: &quot;http://localhost:8080&quot;,
            &quot;webRoot&quot;: &quot;${workspaceFolder}&quot;
        }
    ]
}
```  

Wenn Sie `F5` Windows oder macOS drücken oder die grüne wieder **Gabe** -Schaltfläche erneut auswählen, wird mit dem vs-Code Microsoft Edge \ (EdgeHTML \) gestartet, und Sie können jedes Webprojekt Debuggen, das Sie `8080` direkt von vs-Code auf Port ausgeführt haben!  

### Microsoft Edge (Chromium)  

Wenn Sie Microsoft Edge \ (Chrom \), die nächste Version von Microsoft Edge, anstatt Microsoft Edge \ (EdgeHTML \) starten möchten, fügen Sie der `version` vorhandenen Konfiguration einfach ein Attribut mit der Version von Microsoft Edge \ (Chromium \) hinzu, die Sie starten möchten \ ( `dev` , `beta` oder `canary` \). In der folgenden Konfiguration wird die Canary-Version von Microsoft Edge (Chrom \) gestartet.  

```json
{
    &quot;type&quot;: &quot;edge&quot;,
    &quot;request&quot;: &quot;launch&quot;,
    &quot;version&quot;: &quot;canary&quot;,
    &quot;name&quot;: &quot;Launch Edge against localhost&quot;,
    &quot;url&quot;: &quot;http://localhost:8080&quot;,
    &quot;webRoot&quot;: &quot;${workspaceFolder}"
}
```  

## Anfügen an Microsoft Edge  

Anfügen des vs-Codes an Microsoft Edge \ (Chrom \).  Führen Sie auf Ihrem Terminal den folgenden Befehl aus.  

```console
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

Wenn Sie diese Konfiguration jetzt ausführen, wird vs-Code an Microsoft Edge \ (Chrom \) angefügt, und Sie können mit dem Debuggen beginnen!  

## Mit den Elementen für Microsoft Edge vs Code Extension Team in Verbindung treten    

Senden Sie Ihr Feedback, indem Sie im [GitHub Repo][GithubMicrosoftVscodeEdgeDebug2] der Erweiterung [ein Problem einreichen][GithubMicrosoftVscodeEdgeDebug2NewIssue] .  Fügen Sie die Debug-Adapter Protokolldatei ein, die für jeden Testlauf im `%temp%` Verzeichnis mit dem Namen erstellt wird `vscode-edge-debug2.txt` .  Ziehen Sie diese Datei in einen Problem Kommentar, um Sie in GitHub hochzuladen.  

Um die Elemente für Microsoft Edge vs Code Extension besser zu gestalten, sind Ihre Beiträge Willkommen!  Finden Sie alles, was Sie für den Einstieg in [GitHub Repo][GithubMicrosoftVscodeEdgeDebug2] der Erweiterung benötigen.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge VS Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "Debugger für Edge-vs-Code Erweiterung in Aktion"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio-Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio-Code"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Neues Problem-Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

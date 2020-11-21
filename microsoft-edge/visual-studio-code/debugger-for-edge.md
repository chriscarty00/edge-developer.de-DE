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
# <span data-ttu-id="d4af7-104">Debugger für Microsoft Edge Visual Studio-Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="d4af7-104">Debugger For Microsoft Edge Visual Studio Code Extension</span></span>  

<span data-ttu-id="d4af7-105">Mit der [Debugger für Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio-Code Erweiterung Debuggen Sie den Front-End-JavaScript-Code Zeile für Zeile, und lesen Sie `console.log()` Anweisungen direkt aus [Visual Studio-Code][VisualstudioCode]!</span><span class="sxs-lookup"><span data-stu-id="d4af7-105">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line by line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode]!</span></span>  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Debugger für Edge Visual Studio-Code Erweiterung am Arbeitsplatz" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="d4af7-107">Debugger für Edge Visual Studio-Code Erweiterung am Arbeitsplatz</span><span class="sxs-lookup"><span data-stu-id="d4af7-107">Debugger for Edge Visual Studio Code extension at work</span></span>  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <span data-ttu-id="d4af7-108">Starten von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d4af7-108">Launching Microsoft Edge</span></span>  

<span data-ttu-id="d4af7-109">Navigieren Sie in der Aktivitäts Leiste zur Debugansicht \ ( `Ctrl` + `Shift` + `D` unter Windows oder `Command` + `Shift` + `D` unter macOS **Activity Bar**\).</span><span class="sxs-lookup"><span data-stu-id="d4af7-109">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\) in the **Activity Bar**.</span></span>  <span data-ttu-id="d4af7-110">Wenn Sie keine Konfigurationen in Visual Studio-Code haben, drücken Sie `F5` Windows oder macOS, oder wählen Sie die grüne Schaltfläche **Wiedergabe** aus.</span><span class="sxs-lookup"><span data-stu-id="d4af7-110">If you do not have any configurations in Visual Studio Code, press `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="d4af7-111">Wählen Sie in der Dropdownliste die Option **Edge** aus.</span><span class="sxs-lookup"><span data-stu-id="d4af7-111">Select **Edge** in the dropdown.</span></span>  <span data-ttu-id="d4af7-112">Es sollte eine `launch.json` Datei mit der folgenden Konfiguration angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d4af7-112">You should see a `launch.json` file with the following configuration.</span></span>  

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

<span data-ttu-id="d4af7-113">Wenn Sie `F5` Windows oder macOS drücken oder die grüne wieder **Gabe** -Schaltfläche erneut auswählen, startet Visual Studio-Code Microsoft Edge \ (EdgeHTML \), und Sie können jedes Webprojekt Debuggen, das Sie `8080` direkt im Visual Studio-Code auf Port ausgeführt haben!</span><span class="sxs-lookup"><span data-stu-id="d4af7-113">If you press `F5` on Windows or macOS or select the green **Play** button again, Visual Studio Code launches Microsoft Edge \(EdgeHTML\) and you are able to debug any web project you have running on port `8080` directly from Visual Studio Code!</span></span>  

### <span data-ttu-id="d4af7-114">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="d4af7-114">Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="d4af7-115">Wenn Sie Microsoft Edge \ (Chrom \) starten möchten, fügen Sie dem neuen Microsoft Edge anstelle von Microsoft Edge \ (EdgeHTML \) einfach ein `version` Attribut zu Ihrer vorhandenen Konfiguration mit der Version von Microsoft Edge \ (Chromium \) hinzu, die Sie starten möchten \ ( `dev` , `beta` oder `canary` \).</span><span class="sxs-lookup"><span data-stu-id="d4af7-115">If you want to launch Microsoft Edge \(Chromium\), the new Microsoft Edge, instead of Microsoft Edge \(EdgeHTML\), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge \(Chromium\) you want to launch \(`dev`, `beta`, or `canary`\).</span></span>  <span data-ttu-id="d4af7-116">In der folgenden Konfiguration wird die Canary-Version von Microsoft Edge (Chrom \) gestartet.</span><span class="sxs-lookup"><span data-stu-id="d4af7-116">The following configuration below launches the Canary version of Microsoft Edge \(Chromium\).</span></span>  

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

## <span data-ttu-id="d4af7-117">Anfügen an Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d4af7-117">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="d4af7-118">Anfügen von Visual Studio-Code an Microsoft Edge \ (Chrom \).</span><span class="sxs-lookup"><span data-stu-id="d4af7-118">Attach Visual Studio Code to Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="d4af7-119">Führen Sie auf Ihrem Terminal den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="d4af7-119">From your terminal, run the following command.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="d4af7-120">Fügen Sie Ihrer Datei die unten aufgeführte Konfiguration hinzu `launch.json` .</span><span class="sxs-lookup"><span data-stu-id="d4af7-120">Add the configuration below to your `launch.json` file.</span></span>   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

<span data-ttu-id="d4af7-121">Wenn Sie diese Konfiguration jetzt ausführen, wird Visual Studio-Code an Microsoft Edge \ (Chrom \) angefügt, und Sie können mit dem Debuggen beginnen.</span><span class="sxs-lookup"><span data-stu-id="d4af7-121">If you now run this configuration, Visual Studio Code attaches to Microsoft Edge \(Chromium\) and start debugging.</span></span>  

## <span data-ttu-id="d4af7-122">Mit den Elementen für Microsoft Edge Visual Studio Code Extension Team in Verbindung treten</span><span class="sxs-lookup"><span data-stu-id="d4af7-122">Getting in touch with the Elements for Microsoft Edge Visual Studio Code extension team</span></span>    

<span data-ttu-id="d4af7-123">Senden Sie Ihr Feedback, indem Sie im [GitHub Repo][GithubMicrosoftVscodeEdgeDebug2] der Erweiterung [ein Problem einreichen][GithubMicrosoftVscodeEdgeDebug2NewIssue] .</span><span class="sxs-lookup"><span data-stu-id="d4af7-123">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDebug2NewIssue] against in the [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  <span data-ttu-id="d4af7-124">Fügen Sie die Debug-Adapter Protokolldatei ein, die für jeden Testlauf im `%temp%` Verzeichnis mit dem Namen erstellt wird `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="d4af7-124">Please include the debug adapter log file, which is created for each run in the `%temp%` directory with the name `vscode-edge-debug2.txt`.</span></span>  <span data-ttu-id="d4af7-125">Ziehen Sie diese Datei in einen Problem Kommentar, um Sie in GitHub hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="d4af7-125">Drag this file into an issue comment to upload it to GitHub.</span></span>  

<span data-ttu-id="d4af7-126">Damit die Elemente für die Microsoft Edge Visual Studio-Code Erweiterung besser sind, sind Ihre Beiträge Willkommen!</span><span class="sxs-lookup"><span data-stu-id="d4af7-126">To help make the Elements for Microsoft Edge Visual Studio Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="d4af7-127">Finden Sie alles, was Sie für den Einstieg in [GitHub Repo][GithubMicrosoftVscodeEdgeDebug2] der Erweiterung benötigen.</span><span class="sxs-lookup"><span data-stu-id="d4af7-127">Find everything you need to get started in [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "Debugger für Edge Visual Studio-Code Erweiterung in Aktion"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio-Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio-Code"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Neues Problem-Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

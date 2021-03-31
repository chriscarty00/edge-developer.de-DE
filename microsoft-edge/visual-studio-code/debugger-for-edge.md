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
# <a name="debugger-for-microsoft-edge-visual-studio-code-extension"></a><span data-ttu-id="f0df5-104">Debugger für Microsoft Edge Visual Studio Codeerweiterung</span><span class="sxs-lookup"><span data-stu-id="f0df5-104">Debugger For Microsoft Edge Visual Studio Code Extension</span></span>  

<span data-ttu-id="f0df5-105">Debuggen Sie mit dem [Debugger für Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Codeerweiterung Ihre Front-End-JavaScript-Codezeile zeile für Zeile, und sehen Sie anweisungen direkt aus Visual Studio `console.log()` [Code][VisualstudioCode]!</span><span class="sxs-lookup"><span data-stu-id="f0df5-105">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line by line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode]!</span></span>  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Debugger für Edge Visual Studio Codeerweiterung bei der Arbeit" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="f0df5-107">Debugger für Edge Visual Studio Codeerweiterung bei der Arbeit</span><span class="sxs-lookup"><span data-stu-id="f0df5-107">Debugger for Edge Visual Studio Code extension at work</span></span>  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <a name="launching-microsoft-edge"></a><span data-ttu-id="f0df5-108">Starten von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f0df5-108">Launching Microsoft Edge</span></span>  

<span data-ttu-id="f0df5-109">Navigieren Sie in der Aktivitätsleiste zur Debugansicht \( unter Windows oder `Ctrl` + `Shift` + `D` `Command` + `Shift` + `D` unter macOS\). </span><span class="sxs-lookup"><span data-stu-id="f0df5-109">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\) in the **Activity Bar**.</span></span>  <span data-ttu-id="f0df5-110">Wenn Sie keine Konfigurationen in Visual Studio Code haben, wählen Sie unter Windows oder macOS aus, oder wählen Sie die grüne Schaltfläche `F5` Wiedergabe aus. </span><span class="sxs-lookup"><span data-stu-id="f0df5-110">If you do not have any configurations in Visual Studio Code, select `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="f0df5-111">Wählen **Sie im Dropdownmenü** Edge aus.</span><span class="sxs-lookup"><span data-stu-id="f0df5-111">Select **Edge** in the dropdown.</span></span>  <span data-ttu-id="f0df5-112">Es sollte eine Datei `launch.json` mit der folgenden Konfiguration angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f0df5-112">You should see a `launch.json` file with the following configuration.</span></span>  

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

<span data-ttu-id="f0df5-113">Wenn Sie unter Windows oder macOS auswählen oder erneut die grüne Schaltfläche "Wiedergabe" auswählen, startet `F5` Visual Studio Code Microsoft Edge \(EdgeHTML\) und Sie können jedes Webprojekt debuggen, das Sie im Port ausgeführt haben, direkt aus Visual Studio  `8080` Code!</span><span class="sxs-lookup"><span data-stu-id="f0df5-113">If you select `F5` on Windows or macOS or select the green **Play** button again, Visual Studio Code launches Microsoft Edge \(EdgeHTML\) and you are able to debug any web project you have running on port `8080` directly from Visual Studio Code!</span></span>  

### <a name="microsoft-edge-chromium"></a><span data-ttu-id="f0df5-114">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="f0df5-114">Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="f0df5-115">Wenn Sie Microsoft Edge \(Chromium\) starten möchten, fügen Sie dem neuen Microsoft Edge anstelle von Microsoft Edge \(EdgeHTML\) einfach ein Attribut zu Ihrer vorhandenen Konfiguration mit der Version von Microsoft Edge \(Chromium\) hinzu, die Sie `version` starten möchten \( `dev` , oder `beta` `canary` \).</span><span class="sxs-lookup"><span data-stu-id="f0df5-115">If you want to launch Microsoft Edge \(Chromium\), the new Microsoft Edge, instead of Microsoft Edge \(EdgeHTML\), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge \(Chromium\) you want to launch \(`dev`, `beta`, or `canary`\).</span></span>  <span data-ttu-id="f0df5-116">Mit der folgenden Konfiguration wird die Canary-Version von Microsoft Edge \(Chromium\) gestartet.</span><span class="sxs-lookup"><span data-stu-id="f0df5-116">The following configuration below launches the Canary version of Microsoft Edge \(Chromium\).</span></span>  

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

## <a name="attaching-to-microsoft-edge"></a><span data-ttu-id="f0df5-117">Anfügen an Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f0df5-117">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="f0df5-118">Fügen Visual Studio Code an Microsoft Edge \(Chromium\) an.</span><span class="sxs-lookup"><span data-stu-id="f0df5-118">Attach Visual Studio Code to Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="f0df5-119">Führen Sie in Ihrem Terminal den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="f0df5-119">From your terminal, run the following command.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="f0df5-120">Fügen Sie der Datei die folgende Konfiguration `launch.json` hinzu.</span><span class="sxs-lookup"><span data-stu-id="f0df5-120">Add the configuration below to your `launch.json` file.</span></span>   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

<span data-ttu-id="f0df5-121">Wenn Sie diese Konfiguration jetzt ausführen, Visual Studio Code an Microsoft Edge \(Chromium\) anfügen und mit dem Debuggen beginnen.</span><span class="sxs-lookup"><span data-stu-id="f0df5-121">If you now run this configuration, Visual Studio Code attaches to Microsoft Edge \(Chromium\) and start debugging.</span></span>  

## <a name="getting-in-touch-with-the-elements-for-microsoft-edge-visual-studio-code-extension-team"></a><span data-ttu-id="f0df5-122">Kontakt mit dem Team für Elemente für Microsoft Edge Visual Studio Codeerweiterung</span><span class="sxs-lookup"><span data-stu-id="f0df5-122">Getting in touch with the Elements for Microsoft Edge Visual Studio Code extension team</span></span>    

<span data-ttu-id="f0df5-123">Senden Sie Ihr Feedback, [indem Sie ein Problem im][GithubMicrosoftVscodeEdgeDebug2NewIssue] [GitHub-Repository der][GithubMicrosoftVscodeEdgeDebug2] Erweiterung einreichen.</span><span class="sxs-lookup"><span data-stu-id="f0df5-123">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDebug2NewIssue] against in the [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  <span data-ttu-id="f0df5-124">Fügen Sie die Protokolldatei des Debugadapters ein, die für jede Ausführung im Verzeichnis mit `%temp%` dem Namen erstellt `vscode-edge-debug2.txt` wird.</span><span class="sxs-lookup"><span data-stu-id="f0df5-124">Please include the debug adapter log file, which is created for each run in the `%temp%` directory with the name `vscode-edge-debug2.txt`.</span></span>  <span data-ttu-id="f0df5-125">Ziehen Sie diese Datei in einen Problemkommentar, um sie auf GitHub hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="f0df5-125">Drag this file into an issue comment to upload it to GitHub.</span></span>  

<span data-ttu-id="f0df5-126">Um die Elemente für Microsoft Edge und Visual Studio Codeerweiterung zu verbessern, sind Ihre Beiträge willkommen!</span><span class="sxs-lookup"><span data-stu-id="f0df5-126">To help make the Elements for Microsoft Edge Visual Studio Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="f0df5-127">Finden Sie alles, was Sie zum Einstieg in [das GitHub-Repository der][GithubMicrosoftVscodeEdgeDebug2] Erweiterung benötigen.</span><span class="sxs-lookup"><span data-stu-id="f0df5-127">Find everything you need to get started in [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]: ./media/debugger-for-edge.png "Debugger für Edge Visual Studio Codeerweiterung in Aktion"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "microsoft/vscode-edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Neues Problem – microsoft/vscode-edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

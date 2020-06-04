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
# <span data-ttu-id="2b861-104">Elemente für Microsoft Edge vs Code Extension</span><span class="sxs-lookup"><span data-stu-id="2b861-104">Elements For Microsoft Edge VS Code Extension</span></span>  

<span data-ttu-id="2b861-105">Mit den [Elementen für Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] vs Code Extension verwenden Sie das Tool Elemente des Microsoft Edge-Browsers in [Visual Studio-Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="2b861-105">With the [Elements for Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] VS Code extension, use the Elements tool of the Microsoft Edge browser from within [Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="2b861-106">Durch Starten oder Anfügen wird das elementtool mit einer Instanz von Microsoft Edge verbunden, zeigt die HTML-Laufzeitstruktur an und ermöglicht Ihnen, das Layout zu ändern oder Formatierungsprobleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="2b861-106">By either launching or attaching, the Elements tool connects to an instance of Microsoft Edge, displays the runtime HTML structure, and allows you to alter the layout or fix styling issues.</span></span>  

:::image type="complex" source="./media/elements-for-edge.gif" alt-text="Elemente für Edge-vs-Code Erweiterung am Arbeitsplatz":::
   <span data-ttu-id="2b861-108">Elemente für Edge-vs-Code Erweiterung am Arbeitsplatz</span><span class="sxs-lookup"><span data-stu-id="2b861-108">Elements for Edge VS Code extension at work</span></span>  
:::image-end:::

<!--![Elements for Edge VS Code extension at work][ImageGifElementsEdge]  -->  

## <span data-ttu-id="2b861-109">Starten von Microsoft Edge aus der Elements-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="2b861-109">Launching Microsoft Edge From the Elements extension</span></span>  

<span data-ttu-id="2b861-110">Navigieren Sie zu Elementen in der **Aktivitäts Leiste**.</span><span class="sxs-lookup"><span data-stu-id="2b861-110">Navigate to Elements in the **Activity Bar**.</span></span>  <span data-ttu-id="2b861-111">Neben der Position " **Elemente für Microsoft Edge: Ziele** " gibt es ein Pluszeichen, mit dem der Browser für Ihre APP geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="2b861-111">Next to where it says **Elements for Microsoft Edge: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="2b861-112">Wenn Sie die Option **about: blank** ausgewählt haben, müssen Sie im Browser zu Ihrer Web-App navigieren, damit Sie im vs-Code im Bedienfeld "Elemente" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2b861-112">If you selected the **about:blank** option, you must navigate to your web app in the browser for it to appear in the Elements panel in VS Code.</span></span>  

## <span data-ttu-id="2b861-113">Starten von Microsoft Edge aus der Ansicht "Debuggen"</span><span class="sxs-lookup"><span data-stu-id="2b861-113">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="2b861-114">Wenn Sie es gewohnt sind, die Debugansicht in Visual Studio-Code zu verwenden, greifen Sie auf Elemente dieses Tools zu.</span><span class="sxs-lookup"><span data-stu-id="2b861-114">If you are accustomed to using the Debug view in Visual Studio Code, access Elements from that tool.</span></span>  <span data-ttu-id="2b861-115">Navigieren Sie zur Debugansicht \ ( `Ctrl` + `Shift` + `D` unter Windows oder `Command` + `Shift` + `D` unter macOS \).</span><span class="sxs-lookup"><span data-stu-id="2b861-115">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\).</span></span>  

<span data-ttu-id="2b861-116">Wenn Sie keine Konfigurationen im vs-Code haben, drücken Sie `F5` Windows oder macOS oder wählen Sie die grüne **Wiedergabe** Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="2b861-116">If you do not have any configurations in VS Code, press `F5` on Windows or macOS or select the green **Play** button.</span></span> <span data-ttu-id="2b861-117">Wählen Sie in der Dropdownliste die Option **Edge** aus.</span><span class="sxs-lookup"><span data-stu-id="2b861-117">Select **Edge** in the dropdown.</span></span> <span data-ttu-id="2b861-118">Es sollte eine `launch.json` Datei mit der folgenden Konfiguration angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2b861-118">You should see a `launch.json` file with the following configuration.</span></span>  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            
            "name": "Launch Microsoft Edge and open the Elements tool",
            "request": "launch",
            "type": "vscode-edge-devtools.debug",
            "url": "http://localhost:3000"
        
        }
    ]
}
```  

<span data-ttu-id="2b861-119">Nachdem Sie nun die richtige Konfiguration geladen haben, drücken Sie entweder `F5` Windows oder macOS oder wählen Sie die grüne **Wiedergabe** Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="2b861-119">Now that you have loaded the correct configuration, either press `F5` on Windows or macOS or select the green **Play** button.</span></span> <span data-ttu-id="2b861-120">Das für Sie vertraute Elemente-Tool aus dem Microsoft Edge-Browser wird im vs-Code gestartet, sodass Sie auf einen Screencast Ihres Browsers zugreifen und die Komponenten Ihrer Seite untersuchen können.</span><span class="sxs-lookup"><span data-stu-id="2b861-120">The Elements tool, that is familiar to you, from the Microsoft Edge browser launches in VS Code, allowing you to access a screencast of your browser and examine the components of your page.</span></span>  

## <span data-ttu-id="2b861-121">Anfügen an Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2b861-121">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="2b861-122">Wenn Sie vs-Code an eine Instanz von Microsoft Edge \ (Chrom \) anfügen möchten, müssen Sie den Browser starten, indem Sie den folgenden Befehl von Ihrem Terminal aus ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b861-122">To attach VS Code to an instance of Microsoft Edge\(Chromium\), you must start the browser by running the following command from your terminal.</span></span>  

`start msedge --remote-debugging-port=9222`  

<span data-ttu-id="2b861-123">Nachdem die APP gestartet wurde, fügen Sie die folgende Konfiguration zu Ihrer **Start. JSON** -Datei hinzu:</span><span class="sxs-lookup"><span data-stu-id="2b861-123">Once the app has launched, add the configuration below to your **launch.json** file:</span></span>  

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

<span data-ttu-id="2b861-124">Wählen Sie **an Microsoft Edge anfügen aus, und öffnen Sie das elementtool** aus dem Dropdownmenü Debugger.</span><span class="sxs-lookup"><span data-stu-id="2b861-124">Select **Attach to Microsoft Edge and open the Elements tool** from the Debugger drop-down menu.</span></span>  <span data-ttu-id="2b861-125">Drücken Sie dann entweder `F5` auf Windows oder macOS oder wählen Sie die grüne **Wiedergabe** Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="2b861-125">Next, either press `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="2b861-126">Im vs-Code wird das elementtool gestartet, sodass Sie auf einen Screencast Ihres Browsers zugreifen, das DOM und die Formatierung der Komponenten auf der Seite überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="2b861-126">VS Code launches the Elements tool, allowing you to access a screencast of your browser, inspect the DOM, and the styling of the components on your page.</span></span>  

## <span data-ttu-id="2b861-127">Mit den Elementen für Microsoft Edge vs Code Extension Team in Verbindung treten</span><span class="sxs-lookup"><span data-stu-id="2b861-127">Getting in touch with the Elements for Microsoft Edge VS Code extension team</span></span>  

<span data-ttu-id="2b861-128">Senden Sie Ihr Feedback, indem Sie [ein Problem][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] mit dem [GitHub-Repo][GithubMicrosoftVscodeEdgeDevtools] der Erweiterung einreichen.</span><span class="sxs-lookup"><span data-stu-id="2b861-128">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="2b861-129">Wenn Sie helfen möchten, die Elemente für Microsoft Edge vs Code Extension besser zu gestalten, sind Ihre Beiträge Willkommen!</span><span class="sxs-lookup"><span data-stu-id="2b861-129">If you want to help make the Elements for Microsoft Edge VS Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="2b861-130">Finden Sie alles, was Sie für den Einstieg in das [GitHub-Repo][GithubMicrosoftVscodeEdgeDevtools] der Erweiterung benötigen.</span><span class="sxs-lookup"><span data-stu-id="2b861-130">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!-- image links -->  

<!--[ImageGifElementsEdge]: ./media/elements-for-edge.gif "Elements for Edge VS Code extension in action"  -->  
[ImagePngElementsEdge]:./Media/Elements-for-Edge.png "Elemente für Edge-vs-Code Erweiterung in Aktion"  

<!--links -->  

[VscodeElementsEdge]: ./elements-for-edge.md "Elemente für Microsoft Edge vs Code Extension | Microsoft docs"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio-Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio-Code"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Neues Problem-Microsoft/vscode-Edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elemente für Microsoft Edge (Chrom) | Visual Studio Marketplace"  

---
description: Erfahren Sie, wie Sie WebView2-Steuerelemente Debuggen.
title: Debuggen von WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ad6f334e5796d2f22146f2853ae1ef1d854e329c
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894319"
---
# <span data-ttu-id="daa49-104">Debuggen mit WebView2</span><span class="sxs-lookup"><span data-stu-id="daa49-104">How to Debug with WebView2</span></span>  

<span data-ttu-id="daa49-105">Das Ziel des Microsoft Edge WebView2-Steuerelements ist die Kombination der besten Features der Web-und nativen Anwendungsentwicklung sowie der Entwicklertools.</span><span class="sxs-lookup"><span data-stu-id="daa49-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="daa49-106">Auf der folgenden Seite werden die verschiedenen Tools erläutert, die bei der Entwicklung mit WebView2-Steuerelementen zu verwenden sind.</span><span class="sxs-lookup"><span data-stu-id="daa49-106">The following page outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="daa49-107">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="daa49-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="daa49-108">Verwenden Sie [Microsoft Edge (Chrom)-Entwickler Tools][DevtoolsGuideChromiumMain] zum Debuggen von Webinhalten, die in WebView2-Steuerelementen angezeigt werden, auf die gleiche Weise wie Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="daa49-108">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you use Microsoft Edge.</span></span>  <span data-ttu-id="daa49-109">Um das devtools zu öffnen, setzen Sie den Fokus auf das WebView-Fenster, und verwenden Sie dann eine der folgenden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="daa49-109">To open the DevTools, set focus on the WebView window and then use any of the following actions.</span></span>  
*   <span data-ttu-id="daa49-110">Wählen Sie aus `F12` .</span><span class="sxs-lookup"><span data-stu-id="daa49-110">Select `F12`.</span></span>  
*   <span data-ttu-id="daa49-111">Wählen Sie aus `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="daa49-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="daa49-112">Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) > auswählen `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="daa49-112">Open the context menu \(right-click\) > select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   <span data-ttu-id="daa49-114">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="daa49-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="daa49-115">Wenn Sie die Anwendung in Visual Studio debuggen, wobei der systemeigene Debugger angefügt ist, wird durch Drücken `F12` möglicherweise der systemeigene Debugger anstelle der Entwickler Tools ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="daa49-115">When you debug your application in Visual Studio with the native debugger attached, pressing `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="daa49-116">Drücken Sie `Ctrl` + `Shift` + `I` , oder verwenden Sie das Kontextmenü \ (mit der rechten Maustaste auf \), um die Situation zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="daa49-116">Press `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

> [!NOTE]
> <span data-ttu-id="daa49-117">Sie können das `--auto-open-devtools-for-tabs` Befehlszeilenargument verwenden, um ein neues devtools-Fenster zu öffnen, wenn Sie das erste Mal eine WebView erstellen.</span><span class="sxs-lookup"><span data-stu-id="daa49-117">You may use the `--auto-open-devtools-for-tabs` command-line argument to open a new DevTools window when you first create a WebView.</span></span>  <!--See `CreateCoreWebView2Controller` documentation for how to provide additional command-line arguments to the browser process.  See `LoaderOverride` registry key to examine different builds of WebView2 without modifying your application in the `CreateCoreWebView2Controller` documentation.  -->  

## <span data-ttu-id="daa49-118">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="daa49-118">Visual Studio</span></span>  

<span data-ttu-id="daa49-119">Verwenden Sie den Skriptdebugger in Visual Studio 2019, Version 16,4 Preview 2 oder höher, um Ihr Skript in Visual Studio zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="daa49-119">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  <span data-ttu-id="daa49-120">Überprüfen Sie, ob die Komponente **JavaScript-Diagnose** in der **Desktop Entwicklung mit C++** -Arbeitsauslastung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="daa49-120">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Visual Studio-JavaScript-Diagnose":::
   <span data-ttu-id="daa49-122">Visual Studio-JavaScript-Diagnose</span><span class="sxs-lookup"><span data-stu-id="daa49-122">Visual Studio JavaScript diagnostics</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="daa49-123">Zum Aktivieren des WebView2-Skript Debuggens öffnen Sie das Kontextmenü \ (mit der rechten Maustaste auf \) in Ihrem Projekt, > **Eigenschaften**auswählen.</span><span class="sxs-lookup"><span data-stu-id="daa49-123">To enable WebView2 script debugging, open the context menu \(right-click\) on your project > select **Properties**.</span></span>  

*   <span data-ttu-id="daa49-124">Wählen Sie unter **Konfigurationseigenschaften**die Option **Debuggen**aus.</span><span class="sxs-lookup"><span data-stu-id="daa49-124">On **Configuration Properties**, select **Debugging**.</span></span>  
*   <span data-ttu-id="daa49-125">Wählen Sie in der Eigenschaft **Debuggertyp** in der Liste der Optionen **JavaScript (WebView2)** aus.</span><span class="sxs-lookup"><span data-stu-id="daa49-125">On the **Debugger Type** property, select **JavaScript (WebView2)** from the list of options.</span></span> 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Visual Studio-JavaScript-Debugger":::
   <span data-ttu-id="daa49-127">Visual Studio-JavaScript-Debugger</span><span class="sxs-lookup"><span data-stu-id="daa49-127">Visual Studio JavaScript Debugger</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="daa49-128">Sie sind alle eingerichtet und können Debuggen.</span><span class="sxs-lookup"><span data-stu-id="daa49-128">You are all set up and ready to debug.</span></span>  

<span data-ttu-id="daa49-129">Führen Sie zum Debuggen die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="daa49-129">To Debug, complete the following actions.</span></span>  

1.  <span data-ttu-id="daa49-130">Festlegen von Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="daa49-130">Set Breakpoints</span></span>  
    *   <span data-ttu-id="daa49-131">Öffnen Sie die Skriptdatei, und legen Sie den Haltepunkt an die gewünschte Stelle.</span><span class="sxs-lookup"><span data-stu-id="daa49-131">Open the script file and set the breakpoint where you want it.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="daa49-132">Der JS/TS-Debug-Adapter führt keine Quellpfad-Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="daa49-132">The JS/TS debug adapter does not do source path mapping.</span></span><span data-ttu-id="daa49-133">Sie müssen exakt denselben Pfad öffnen, der Ihrem WebView2 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="daa49-133">  You must open the exact same path associated with your WebView2.</span></span>  
        
1.  <span data-ttu-id="daa49-134">Ausführen von Code</span><span class="sxs-lookup"><span data-stu-id="daa49-134">Run Code</span></span>  
    *   <span data-ttu-id="daa49-135">Wählen Sie die geeignete Build-Flavor-und Laufzeitumgebung aus, und starten Sie dann den lokalen Windows-Debugger.</span><span class="sxs-lookup"><span data-stu-id="daa49-135">Select your appropriate build flavor and runtime environment and then start the local windows debugger.</span></span>  
1.  <span data-ttu-id="daa49-136">Anzeigen der Debug-Konsole</span><span class="sxs-lookup"><span data-stu-id="daa49-136">View Debug Console</span></span>  
    *   <span data-ttu-id="daa49-137">Die Anwendung wird ausgeführt, und der Debugger stellt eine Verbindung her, nachdem die erste webview2 erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="daa49-137">You application runs and the debugger connects after the first webview2 is created.</span></span><span data-ttu-id="daa49-138">Alle ausstehenden Debug-Ausgaben werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="daa49-138">  Any pending debug output is displayed.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="daa49-139">Diese Methode des Debuggens ist derzeit auf Win32-Anwendungen und Office-Add-ins beschränkt.</span><span class="sxs-lookup"><span data-stu-id="daa49-139">This method of debugging is currently restricted to Win32 applications and Office add-ins.</span></span>  
        
## <span data-ttu-id="daa49-140">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="daa49-140">Visual Studio Code</span></span>  

<span data-ttu-id="daa49-141">Sie können Visual Studio-Code verwenden, um Skripts zu debuggen, die in WebView2-Steuerelementen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="daa49-141">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="daa49-142">Weitere Informationen finden Sie unter [Microsoft Edge (Chrom) WebView-Anwendungen][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].</span><span class="sxs-lookup"><span data-stu-id="daa49-142">For more information, see [Microsoft Edge (Chromium) WebView Applications][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="daa49-143">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="daa49-143">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="daa49-144">Helfen Sie beim Aufbau einer reicheren WebView2-Erfahrung, indem Sie Ihr Feedback freigeben.</span><span class="sxs-lookup"><span data-stu-id="daa49-144">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="daa49-145">Besuchen Sie das [Feedback-Repo][GithubMicrosoftedgeWebviewfeedbackMain] , um Funktionsanforderungen oder Fehlerberichte einzureichen.</span><span class="sxs-lookup"><span data-stu-id="daa49-145">Visit the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain] to submit feature requests or bug reports.</span></span>  

<!--## Debugging  

Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`. You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView. See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process. Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.  -->  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chrom) WebView-Anwendungen-vs-Code-Debugger für Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  

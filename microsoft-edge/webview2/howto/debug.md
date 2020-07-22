---
description: Erfahren Sie, wie Sie WebView2-Steuerelemente Debuggen.
title: Debuggen von WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 232104abc360cfa660d567ffb66535213fcb3ae0
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888581"
---
# <span data-ttu-id="9cd45-104">Debuggen mit WebView2</span><span class="sxs-lookup"><span data-stu-id="9cd45-104">How to Debug with WebView2</span></span>  

<span data-ttu-id="9cd45-105">Das Ziel des Microsoft Edge WebView2-Steuerelements ist die Kombination der besten Features der Web-und nativen Anwendungsentwicklung sowie der Entwicklertools.</span><span class="sxs-lookup"><span data-stu-id="9cd45-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="9cd45-106">Auf der folgenden Seite werden die verschiedenen Tools erläutert, die bei der Entwicklung mit WebView2-Steuerelementen zu verwenden sind.</span><span class="sxs-lookup"><span data-stu-id="9cd45-106">The following page outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="9cd45-107">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9cd45-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="9cd45-108">Verwenden Sie die [Microsoft Edge (Chrom)-Entwickler Tools][DevtoolsMain] zum Debuggen von Webinhalten, die in WebView2-Steuerelementen angezeigt werden, auf die gleiche Weise wie bei Verwendung von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9cd45-108">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsMain] to debug web content displayed in WebView2 controls, in the same way that you would if you were using Microsoft Edge.</span></span>  <span data-ttu-id="9cd45-109">Um das devtools zu öffnen, setzen Sie den Fokus auf das WebView-Fenster, und verwenden Sie dann eine der folgenden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="9cd45-109">To open the DevTools, set focus on the WebView window and then use any of the following actions.</span></span>  

*   <span data-ttu-id="9cd45-110">Wählen Sie aus `F12` .</span><span class="sxs-lookup"><span data-stu-id="9cd45-110">Select `F12`.</span></span>  
*   <span data-ttu-id="9cd45-111">Wählen Sie aus `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="9cd45-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="9cd45-112">Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie aus `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="9cd45-112">Open the context menu \(right-click\) and select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   <span data-ttu-id="9cd45-114">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9cd45-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!IMPORTANT]
> <span data-ttu-id="9cd45-115">Wenn Sie die Anwendung in Visual Studio debuggen, wobei der systemeigene Debugger angefügt ist, `F12` kann die Auswahl den systemeigenen Debugger anstelle der Entwickler Tools auslösen.</span><span class="sxs-lookup"><span data-stu-id="9cd45-115">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="9cd45-116">Verwenden Sie `Ctrl` + `Shift` + `I` das Kontextmenü, oder klicken Sie mit der rechten Maustaste auf \), um die Situation zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="9cd45-116">Use `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

## <span data-ttu-id="9cd45-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9cd45-117">Visual Studio</span></span>  

<span data-ttu-id="9cd45-118">Sie können Visual Studio verwenden, um Anwendungscode und Debug-Skripts zur gleichen Zeit zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="9cd45-118">You may use Visual Studio to develop application code and debug scripts at the same time.</span></span>  

<span data-ttu-id="9cd45-119">Beachten Sie die folgenden Punkte.</span><span class="sxs-lookup"><span data-stu-id="9cd45-119">Keep the following things in mind.</span></span>  

*   <span data-ttu-id="9cd45-120">Visual Studio unterstützt nur das Debuggen von Skripts, wenn die app in Visual Studio gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="9cd45-120">Visual Studio only supports debugging scripts when the app is launched from within Visual Studio.</span></span>  <span data-ttu-id="9cd45-121">\ (Das Anfügen eines ausgeführten Prozesses zum Debuggen wird nicht unterstützt. \)</span><span class="sxs-lookup"><span data-stu-id="9cd45-121">\(Attaching a running process for debugging is not supported.\)</span></span>  
*   <span data-ttu-id="9cd45-122">Das Debugging-Szenario für zielgerichtete WebView wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9cd45-122">The targeted WebView debugging scenario is not supported.</span></span>  

<span data-ttu-id="9cd45-123">Verwenden Sie den Skriptdebugger in Visual Studio 2019, Version 16,4 Preview 2 oder höher, um Ihr Skript in Visual Studio zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="9cd45-123">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  

<span data-ttu-id="9cd45-124">Richten Sie den Debugger ein.</span><span class="sxs-lookup"><span data-stu-id="9cd45-124">Set up the debugger.</span></span>  

*   <span data-ttu-id="9cd45-125">Überprüfen Sie, ob die Komponente **JavaScript-Diagnose** in der **Desktop Entwicklung mit C++** -Arbeitsauslastung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9cd45-125">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  
    
    1.  <span data-ttu-id="9cd45-126">Navigieren Sie zu **apps & Features** -Einstellungen in Windows.</span><span class="sxs-lookup"><span data-stu-id="9cd45-126">Navigate to **Apps & features** settings in Windows.</span></span>  <span data-ttu-id="9cd45-127">Suchen Sie es mithilfe der Windows-Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="9cd45-127">Search for it using the Windows task bar.</span></span>  
    1.  <span data-ttu-id="9cd45-128">Wählen Sie **ändern**aus.</span><span class="sxs-lookup"><span data-stu-id="9cd45-128">Choose **Modify**.</span></span>  
    1.  <span data-ttu-id="9cd45-129">Überprüfen Sie, ob die Kontrollkästchen **JavaScript-Diagnose** und **Desktop Entwicklung in C++** aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="9cd45-129">Verify the **Javascript diagnostics** and **Desktop Development in C++** checkboxes are selected.</span></span>  
        
        :::image type="complex" source="../media/appsandfeatures.png" alt-text="Apps & Features" lightbox="../media/appsandfeatures.png":::
           <span data-ttu-id="9cd45-131">Apps & Features</span><span class="sxs-lookup"><span data-stu-id="9cd45-131">Apps & Features</span></span>  
        :::image-end:::  
        
*   <span data-ttu-id="9cd45-132">Aktivieren Sie das WebView2-Skriptdebugging.</span><span class="sxs-lookup"><span data-stu-id="9cd45-132">Enable WebView2 script debugging.</span></span>  
    1.  <span data-ttu-id="9cd45-133">Zeigen Sie mit der Maus auf das Projekt, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="9cd45-133">Hover on your project, open the context menu \(right-click\), and select **Properties**.</span></span>  
    1.  <span data-ttu-id="9cd45-134">Wählen Sie unter **Konfigurationseigenschaften**die Option **Debuggen**aus.</span><span class="sxs-lookup"><span data-stu-id="9cd45-134">On **Configuration Properties**, select **Debugging**.</span></span>  
    1.  <span data-ttu-id="9cd45-135">Suchen Sie in der Eigenschaft **Debuggertyp** in der Liste der Optionen, und wählen Sie **JavaScript (WebView2)** aus.</span><span class="sxs-lookup"><span data-stu-id="9cd45-135">On the **Debugger Type** property, search the the list of options, and select **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="../media/enbjs.png" alt-text="Visual Studio-JavaScript-Debugger" lightbox="../media/enbjs.png":::
           <span data-ttu-id="9cd45-137">Visual Studio-JavaScript-Debugger</span><span class="sxs-lookup"><span data-stu-id="9cd45-137">Visual Studio JavaScript Debugger</span></span>  
        :::image-end:::  
        
<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="9cd45-138">Sie sind alle eingerichtet und können Debuggen.</span><span class="sxs-lookup"><span data-stu-id="9cd45-138">You are all set up and ready to debug.</span></span>  

<span data-ttu-id="9cd45-139">Führen Sie zum Debuggen die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="9cd45-139">To Debug, complete the following actions.</span></span>  

1.  <span data-ttu-id="9cd45-140">Festlegen von Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="9cd45-140">Set Breakpoints</span></span>  
    *   <span data-ttu-id="9cd45-141">Öffnen Sie die Skriptdatei, und legen Sie den Haltepunkt an die gewünschte Stelle.</span><span class="sxs-lookup"><span data-stu-id="9cd45-141">Open the script file and set the breakpoint where you want it.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="9cd45-142">Der JS/TS-Debug-Adapter führt keine Quellpfad-Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="9cd45-142">The JS/TS debug adapter does not do source path mapping.</span></span><span data-ttu-id="9cd45-143">Sie müssen exakt denselben Pfad öffnen, der Ihrem WebView2 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9cd45-143">  You must open the exact same path associated with your WebView2.</span></span>  
        
1.  <span data-ttu-id="9cd45-144">Ausführen von Code</span><span class="sxs-lookup"><span data-stu-id="9cd45-144">Run Code</span></span>  
    *   <span data-ttu-id="9cd45-145">Wählen Sie die geeignete Build-Flavor-und Laufzeitumgebung aus, und starten Sie dann den lokalen Windows-Debugger.</span><span class="sxs-lookup"><span data-stu-id="9cd45-145">Select your appropriate build flavor and runtime environment and then start the local windows debugger.</span></span>  
1.  <span data-ttu-id="9cd45-146">Anzeigen der Debug-Konsole</span><span class="sxs-lookup"><span data-stu-id="9cd45-146">View Debug Console</span></span>  
    *   <span data-ttu-id="9cd45-147">Die Anwendung wird ausgeführt, und der Debugger stellt eine Verbindung her, nachdem die erste webview2 erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9cd45-147">You application runs and the debugger connects after the first webview2 is created.</span></span><span data-ttu-id="9cd45-148">Alle ausstehenden Debug-Ausgaben werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9cd45-148">  Any pending debug output is displayed.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="9cd45-149">Diese Methode des Debuggens ist derzeit auf Win32-Anwendungen und Office-Add-ins beschränkt.</span><span class="sxs-lookup"><span data-stu-id="9cd45-149">This method of debugging is currently restricted to Win32 applications and Office add-ins.</span></span>  
        
## <span data-ttu-id="9cd45-150">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="9cd45-150">Visual Studio Code</span></span>  

<span data-ttu-id="9cd45-151">Sie können Visual Studio-Code verwenden, um Skripts zu debuggen, die in WebView2-Steuerelementen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9cd45-151">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="9cd45-152">Weitere Informationen finden Sie unter [Microsoft Edge (Chrom) WebView-Anwendungen][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].</span><span class="sxs-lookup"><span data-stu-id="9cd45-152">For more information, see [Microsoft Edge (Chromium) WebView Applications][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="9cd45-153">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="9cd45-153">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="9cd45-154">Helfen Sie beim Aufbau einer reicheren WebView2-Erfahrung, indem Sie Ihr Feedback freigeben.</span><span class="sxs-lookup"><span data-stu-id="9cd45-154">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="9cd45-155">Besuchen Sie das [Feedback-Repo][GithubMicrosoftedgeWebviewfeedback] , um Funktionsanforderungen oder Fehlerberichte einzureichen.</span><span class="sxs-lookup"><span data-stu-id="9cd45-155">Visit the [feedback repo][GithubMicrosoftedgeWebviewfeedback] to submit feature requests or bug reports.</span></span>  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chrom) WebView-Anwendungen – vs-Code – Debugger für Microsoft Edge | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

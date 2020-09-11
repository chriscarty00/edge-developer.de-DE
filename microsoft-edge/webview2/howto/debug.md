---
description: Erfahren Sie, wie Sie WebView2-Steuerelemente Debuggen.
title: Erste Schritte beim Debuggen von WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/13/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 15171147b847b1d41cd603efed1b8ee42185dc29
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010698"
---
# <span data-ttu-id="b93e0-104">Erste Schritte beim Debuggen von WebView2-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b93e0-104">Get started debugging WebView2 applications</span></span>  

<span data-ttu-id="b93e0-105">Das Ziel des Microsoft Edge WebView2-Steuerelements besteht darin, die besten Features und Tools für die Entwicklung von Web-und systemeigenen Anwendungen zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="b93e0-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native application development features and tools.</span></span>  <span data-ttu-id="b93e0-106">Wenn Sie Ihre WebView2-Anwendung entwickeln, sollten Sie Ihre Anwendung debuggen.</span><span class="sxs-lookup"><span data-stu-id="b93e0-106">When you develop your WebView2 application, you should debug your application.</span></span>  <span data-ttu-id="b93e0-107">In diesem Artikel werden die verschiedenen Tools erläutert, die Sie verwenden können, um Ihren Web-und systemeigenen Code in ihrer WebView2-Anwendung zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="b93e0-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 application.</span></span>  

## [<span data-ttu-id="b93e0-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b93e0-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="b93e0-109">Verwenden Sie die [Microsoft Edge (Chrom)-Entwickler Tools][DevtoolsGuideChromiumMain] zum Debuggen von Webinhalten, die in WebView2-Steuerelementen angezeigt werden, auf die gleiche Weise, wie Sie für eine andere in Microsoft Edge angezeigte Webseite debuggen können.</span><span class="sxs-lookup"><span data-stu-id="b93e0-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="b93e0-110">Um das devtools zu öffnen, setzen Sie den Fokus auf das WebView-Steuerelement, und verwenden Sie dann eine der folgenden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="b93e0-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="b93e0-111">Wählen Sie aus `F12` .</span><span class="sxs-lookup"><span data-stu-id="b93e0-111">Select `F12`.</span></span>  
*   <span data-ttu-id="b93e0-112">Wählen Sie aus `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="b93e0-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="b93e0-113">Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie aus `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="b93e0-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  

<span data-ttu-id="b93e0-114">Weitere Informationen finden Sie unter [Übersicht über devtools][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="b93e0-114">For more information, see [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="DevTools-Debuggen" lightbox="./media/f12.png":::
   <span data-ttu-id="b93e0-116">DevTools-Debuggen</span><span class="sxs-lookup"><span data-stu-id="b93e0-116">DevTools debugging</span></span>  
:::image-end:::  

## [<span data-ttu-id="b93e0-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b93e0-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="b93e0-118">Visual Studio bietet verschiedene Debugging-Tools für Web-und systemeigenen Code in WebView2-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b93e0-118">Visual Studio provides various debugging tools for web and native code in WebView2 applications.</span></span>  <span data-ttu-id="b93e0-119">Im Abschnitt Visual Studio liegt der Hauptfokus auf dem Debuggen von WebView-Steuerelementen, doch die anderen Methoden zum Debuggen in Visual Studio sind wie gewohnt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b93e0-119">In the Visual Studio section, the primarily focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="b93e0-120">Mit dem folgenden Verfahren können Sie Web-und systemeigenen Code nur in Win32-Anwendungen oder Office-Add-ins Debuggen.</span><span class="sxs-lookup"><span data-stu-id="b93e0-120">Use the following process to debug web and native code in Win32 applications or Office add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b93e0-121">Wenn Sie die Anwendung in Visual Studio debuggen, wobei der systemeigene Debugger angefügt ist, `F12` kann die Auswahl den systemeigenen Debugger anstelle der Entwickler Tools auslösen.</span><span class="sxs-lookup"><span data-stu-id="b93e0-121">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="b93e0-122">Wählen Sie aus `Ctrl` + `Shift` + `I` , oder verwenden Sie das Kontextmenü \ (mit der rechten Maustaste auf \), um die Situation zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="b93e0-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="b93e0-123">Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Anforderungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="b93e0-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="b93e0-124">Zum Debuggen von Skripts muss die app in Visual Studio gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="b93e0-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="b93e0-125">Sie können keinen Debugger an einen ausgeführten WebView2-Prozess anfügen.</span><span class="sxs-lookup"><span data-stu-id="b93e0-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="b93e0-126">Installieren Sie Visual Studio 2019, Version 16,4 Preview 2 oder höher.</span><span class="sxs-lookup"><span data-stu-id="b93e0-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  

<span data-ttu-id="b93e0-127">Installieren und Einrichten der Skriptdebugger Tools in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b93e0-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="b93e0-128">Führen Sie die folgenden Aktionen aus, um die Komponente **JavaScript-Diagnose** in der **Desktop Entwicklung mit C++** zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b93e0-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  

    1. <span data-ttu-id="b93e0-129">Geben Sie in der Windows-Explorer-Leiste ein `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="b93e0-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1. <span data-ttu-id="b93e0-130">Wählen Sie **Visual Studio-Installationsprogramm** aus, um es zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b93e0-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1. <span data-ttu-id="b93e0-131">Wählen Sie im Visual Studio-Installationsprogramm in der installierten Version die Schaltfläche **mehr** aus, und wählen Sie dann **ändern**aus.</span><span class="sxs-lookup"><span data-stu-id="b93e0-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1. <span data-ttu-id="b93e0-132">Wählen Sie in Visual Studio unter **Arbeits auslasten**die Einstellung **Desktop Entwicklung in C++** aus.</span><span class="sxs-lookup"><span data-stu-id="b93e0-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Bildschirm ' Ändern von Arbeitslasten ' in Visual Studio" lightbox="./media/workloads.png":::
            <span data-ttu-id="b93e0-134">Bildschirm ' Ändern von Arbeitslasten ' in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b93e0-134">Visual Studio Modifying Workloads Screen</span></span> :::image-end:::  
        
    1.  <span data-ttu-id="b93e0-135">Wählen Sie **einzelne Komponenten**aus.</span><span class="sxs-lookup"><span data-stu-id="b93e0-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="b93e0-136">Geben Sie im Suchfeld ein `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="b93e0-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="b93e0-137">Wählen Sie die **JavaScript-Diagnose** Einstellung aus.</span><span class="sxs-lookup"><span data-stu-id="b93e0-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="b93e0-138">Wählen Sie **ändern**aus.</span><span class="sxs-lookup"><span data-stu-id="b93e0-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio-Registerkarte ' einzelne Komponenten ändern '" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="b93e0-140">Visual Studio-Registerkarte ' einzelne Komponenten ändern '</span><span class="sxs-lookup"><span data-stu-id="b93e0-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="b93e0-141">Aktivieren Sie das Skriptdebugging für WebView2-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b93e0-141">Enable script debugging for WebView2 applications.</span></span>  
    1.  <span data-ttu-id="b93e0-142">Öffnen Sie in Ihrem WebView2-Projekt das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="b93e0-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="b93e0-143">Wählen Sie unter den **Konfigurationseigenschaften**die Option **Debuggen**aus.</span><span class="sxs-lookup"><span data-stu-id="b93e0-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="b93e0-144">Wählen Sie unter dem **Debuggertyp**die Option **JavaScript (WebView2)** aus.</span><span class="sxs-lookup"><span data-stu-id="b93e0-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Visual Studio-Konfigurationseigenschaft "Debuggen"" lightbox="./media/enbjs.png":::
           <span data-ttu-id="b93e0-146">Visual Studio-Konfigurationseigenschaft " **Debuggen** "</span><span class="sxs-lookup"><span data-stu-id="b93e0-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="b93e0-147">Führen Sie die folgenden Aktionen aus, um Ihre WebView2-Anwendung zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="b93e0-147">Complete the following actions to debug your WebView2 application.</span></span>  

1.  <span data-ttu-id="b93e0-148">Wenn Sie einen Haltepunkt im Quellcode festlegen möchten, zeigen Sie auf die linke Seite der Zeile, und wählen Sie einen Haltepunkt aus.</span><span class="sxs-lookup"><span data-stu-id="b93e0-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="b93e0-149">Der JS/TS-Debug-Adapter führt keine Quell Pfadzuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="b93e0-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="b93e0-150">Sie müssen exakt denselben Pfad öffnen, der Ihrem WebView2 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b93e0-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio-Haltepunkt hinzufügen" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="b93e0-152">Visual Studio-Haltepunkt hinzufügen</span><span class="sxs-lookup"><span data-stu-id="b93e0-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b93e0-153">Zum Ausführen des Debuggers wählen Sie die Bit-Größe der Plattform aus, und wählen Sie dann die grüne Schaltfläche Wiedergabe neben dem **lokalen Windows-Debugger**aus.</span><span class="sxs-lookup"><span data-stu-id="b93e0-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="b93e0-154">Die Anwendung wird ausgeführt, und der Debugger stellt eine Verbindung mit dem ersten WebView2-Prozess her, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b93e0-154">The application runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Lokaler Windows-Debugger in Visual Studio" lightbox="./media/run.png"::: 
       <span data-ttu-id="b93e0-156">**Lokaler Windows-Debugger** in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b93e0-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b93e0-157">Suchen Sie in der **Debug-Konsole**die Ausgabe des Debuggers.</span><span class="sxs-lookup"><span data-stu-id="b93e0-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio-Debug-Konsole" lightbox="./media/console.png"::: 
       <span data-ttu-id="b93e0-159">Visual Studio- **Debug-Konsole**</span><span class="sxs-lookup"><span data-stu-id="b93e0-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
* * *  

## <span data-ttu-id="b93e0-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b93e0-160">See also</span></span>  

*   <span data-ttu-id="b93e0-161">Informationen zum Einstieg in die Verwendung von WebView2 finden Sie unter [WebView2 erste Schritte][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="b93e0-161">To get started using WebView2, see [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="b93e0-162">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie im [WebView2Samples][GithubMicrosoftedgeWebview2samples] -Repo auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="b93e0-162">For a comprehensive example of WebView2 capabilities, see the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="b93e0-163">Ausführlichere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="b93e0-163">For more detailed information about WebView2 APIs, see [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="b93e0-164">Weitere Informationen zu WebView2 finden Sie unter [WebView2-Ressourcen][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="b93e0-164">For more information about WebView2, see [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="b93e0-165">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="b93e0-165">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions Klasse | Microsoft docs"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-Globals | Microsoft docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Was ist neu? -JavaScript-Debugger für Visual Studio-Code – Microsoft/vscode-js – Debuggen | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chrom) WebView-Anwendungen – Visual Studio-Code – Debugger für Microsoft Edge – Microsoft/vscode-Edge-debug2 | GitHub"  

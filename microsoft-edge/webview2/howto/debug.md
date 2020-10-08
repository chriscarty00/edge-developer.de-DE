---
description: Erfahren Sie, wie Sie WebView2-Steuerelemente Debuggen.
title: Erste Schritte beim Debuggen von WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/21/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 78c0fb982de8ccce71a8df2b59447b55f64fdc2f
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "11052148"
---
# <span data-ttu-id="746bf-104">Erste Schritte beim Debuggen von WebView2-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="746bf-104">Get started debugging WebView2 applications</span></span>  

<span data-ttu-id="746bf-105">Das Ziel des Microsoft Edge WebView2-Steuerelements besteht darin, die besten Features und Tools für die Entwicklung von Web-und systemeigenen Anwendungen zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="746bf-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native application development features and tools.</span></span>  <span data-ttu-id="746bf-106">Wenn Sie Ihre WebView2-Anwendung entwickeln, sollten Sie Ihre Anwendung debuggen.</span><span class="sxs-lookup"><span data-stu-id="746bf-106">When you develop your WebView2 application, you should debug your application.</span></span>  <span data-ttu-id="746bf-107">In diesem Artikel werden die verschiedenen Tools erläutert, die Sie verwenden können, um Ihren Web-und systemeigenen Code in ihrer WebView2-Anwendung zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="746bf-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 application.</span></span>  

## [<span data-ttu-id="746bf-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="746bf-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="746bf-109">Verwenden Sie die [Microsoft Edge (Chrom)-Entwickler Tools][DevtoolsGuideChromiumMain] zum Debuggen von Webinhalten, die in WebView2-Steuerelementen angezeigt werden, auf die gleiche Weise, wie Sie für eine andere in Microsoft Edge angezeigte Webseite debuggen können.</span><span class="sxs-lookup"><span data-stu-id="746bf-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="746bf-110">Um das devtools zu öffnen, setzen Sie den Fokus auf das WebView-Steuerelement, und verwenden Sie dann eine der folgenden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="746bf-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="746bf-111">Wählen Sie aus `F12` .</span><span class="sxs-lookup"><span data-stu-id="746bf-111">Select `F12`.</span></span>  
*   <span data-ttu-id="746bf-112">Wählen Sie aus `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="746bf-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="746bf-113">Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie aus `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="746bf-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  

<span data-ttu-id="746bf-114">Weitere Informationen finden Sie unter [Übersicht über devtools][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="746bf-114">For more information, see [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="DevTools-Debuggen" lightbox="./media/f12.png":::
   <span data-ttu-id="746bf-116">DevTools-Debuggen</span><span class="sxs-lookup"><span data-stu-id="746bf-116">DevTools debugging</span></span>  
:::image-end:::  

## [<span data-ttu-id="746bf-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="746bf-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="746bf-118">Visual Studio bietet verschiedene Debugging-Tools für Web-und systemeigenen Code in WebView2-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="746bf-118">Visual Studio provides various debugging tools for web and native code in WebView2 applications.</span></span>  <span data-ttu-id="746bf-119">Im Abschnitt Visual Studio liegt der Hauptfokus auf dem Debuggen von WebView-Steuerelementen, doch die anderen Methoden zum Debuggen in Visual Studio sind wie gewohnt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="746bf-119">In the Visual Studio section, the primary focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="746bf-120">Mit dem folgenden Verfahren können Sie Web-und systemeigenen Code nur in Win32-Anwendungen oder Office-Add-ins Debuggen.</span><span class="sxs-lookup"><span data-stu-id="746bf-120">Use the following process to debug web and native code in Win32 applications or Office Add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="746bf-121">Wenn Sie die Anwendung in Visual Studio debuggen, wobei der systemeigene Debugger angefügt ist, `F12` kann die Auswahl den systemeigenen Debugger anstelle der Entwickler Tools auslösen.</span><span class="sxs-lookup"><span data-stu-id="746bf-121">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="746bf-122">Wählen Sie aus `Ctrl` + `Shift` + `I` , oder verwenden Sie das Kontextmenü \ (mit der rechten Maustaste auf \), um die Situation zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="746bf-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="746bf-123">Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Anforderungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="746bf-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="746bf-124">Zum Debuggen von Skripts muss die app in Visual Studio gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="746bf-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="746bf-125">Sie können keinen Debugger an einen ausgeführten WebView2-Prozess anfügen.</span><span class="sxs-lookup"><span data-stu-id="746bf-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="746bf-126">Installieren Sie Visual Studio 2019, Version 16,4 Preview 2 oder höher.</span><span class="sxs-lookup"><span data-stu-id="746bf-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  

<span data-ttu-id="746bf-127">Installieren und Einrichten der Skriptdebugger Tools in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="746bf-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="746bf-128">Führen Sie die folgenden Aktionen aus, um die Komponente **JavaScript-Diagnose** in der **Desktop Entwicklung mit C++** zu installieren.</span><span class="sxs-lookup"><span data-stu-id="746bf-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  

    1. <span data-ttu-id="746bf-129">Geben Sie in der Windows-Explorer-Leiste ein `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="746bf-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1. <span data-ttu-id="746bf-130">Wählen Sie **Visual Studio-Installationsprogramm** aus, um es zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="746bf-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1. <span data-ttu-id="746bf-131">Wählen Sie im Visual Studio-Installationsprogramm in der installierten Version die Schaltfläche **mehr** aus, und wählen Sie dann **ändern**aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1. <span data-ttu-id="746bf-132">Wählen Sie in Visual Studio unter **Arbeits auslasten**die Einstellung **Desktop Entwicklung in C++** aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="DevTools-Debuggen" lightbox="./media/workloads.png":::
            <span data-ttu-id="746bf-134">Bildschirm ' Ändern von Arbeitslasten ' in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="746bf-134">Visual Studio Modifying Workloads Screen</span></span> :::image-end:::  
        
    1.  <span data-ttu-id="746bf-135">Wählen Sie **einzelne Komponenten**aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="746bf-136">Geben Sie im Suchfeld ein `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="746bf-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="746bf-137">Wählen Sie die **JavaScript-Diagnose** Einstellung aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="746bf-138">Wählen Sie **ändern**aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="DevTools-Debuggen" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="746bf-140">Visual Studio-Registerkarte ' einzelne Komponenten ändern '</span><span class="sxs-lookup"><span data-stu-id="746bf-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="746bf-141">Aktivieren Sie das Skriptdebugging für WebView2-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="746bf-141">Enable script debugging for WebView2 applications.</span></span>  
    1.  <span data-ttu-id="746bf-142">Öffnen Sie in Ihrem WebView2-Projekt das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="746bf-143">Wählen Sie unter den **Konfigurationseigenschaften**die Option **Debuggen**aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="746bf-144">Wählen Sie unter dem **Debuggertyp**die Option **JavaScript (WebView2)** aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="DevTools-Debuggen" lightbox="./media/enbjs.png":::
           <span data-ttu-id="746bf-146">Visual Studio-Konfigurationseigenschaft " **Debuggen** "</span><span class="sxs-lookup"><span data-stu-id="746bf-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="746bf-147">Führen Sie die folgenden Aktionen aus, um Ihre WebView2-Anwendung zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="746bf-147">Complete the following actions to debug your WebView2 application.</span></span>  

1.  <span data-ttu-id="746bf-148">Wenn Sie einen Haltepunkt im Quellcode festlegen möchten, zeigen Sie auf die linke Seite der Zeile, und wählen Sie einen Haltepunkt aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="746bf-149">Der JS/TS-Debug-Adapter führt keine Quell Pfadzuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="746bf-150">Sie müssen exakt denselben Pfad öffnen, der Ihrem WebView2 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="746bf-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="DevTools-Debuggen" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="746bf-152">Visual Studio-Haltepunkt hinzufügen</span><span class="sxs-lookup"><span data-stu-id="746bf-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="746bf-153">Zum Ausführen des Debuggers wählen Sie die Bit-Größe der Plattform aus, und wählen Sie dann die grüne Schaltfläche Wiedergabe neben dem **lokalen Windows-Debugger**aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="746bf-154">Die Anwendung wird ausgeführt, und der Debugger stellt eine Verbindung mit dem ersten WebView2-Prozess her, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="746bf-154">The application runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text="DevTools-Debuggen" lightbox="./media/run.png"::: 
       <span data-ttu-id="746bf-156">**Lokaler Windows-Debugger** in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="746bf-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="746bf-157">Suchen Sie in der **Debug-Konsole**die Ausgabe des Debuggers.</span><span class="sxs-lookup"><span data-stu-id="746bf-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text="DevTools-Debuggen" lightbox="./media/console.png"::: 
       <span data-ttu-id="746bf-159">Visual Studio- **Debug-Konsole**</span><span class="sxs-lookup"><span data-stu-id="746bf-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
## [<span data-ttu-id="746bf-160">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="746bf-160">Visual Studio Code</span></span>](#tab/visualstudiocode)  

<span data-ttu-id="746bf-161">Verwenden Sie Microsoft Visual Studio-Code zum Debuggen von Skripts, die in WebView2-Steuerelementen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="746bf-161">Use Microsoft Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

<span data-ttu-id="746bf-162">Führen Sie in Visual Studio-Code die folgenden Aktionen aus, um den Code zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="746bf-162">In Visual Studio Code, complete the following actions to debug your code.</span></span> 

1.  <span data-ttu-id="746bf-163">Für Ihr Projekt ist eine Datei erforderlich `launch.json` .</span><span class="sxs-lookup"><span data-stu-id="746bf-163">Your project is required to have a `launch.json` file.</span></span>  <span data-ttu-id="746bf-164">Wenn Ihr Projekt keine Datei enthält `launch.json` , kopieren Sie den folgenden Codeausschnitt, und erstellen Sie eine neue `launch.json` Datei.</span><span class="sxs-lookup"><span data-stu-id="746bf-164">If your project doesn't have a `launch.json` file, copy the following code snippet and create a new `launch.json` file.</span></span>  
        
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",
        "env": {
            // Customize for your application location if needed
            "Path": "%path%;e:/path/to/your/application/location; "
        },
        "useWebView": true,
    ```  
        
1.  <span data-ttu-id="746bf-165">Wenn Sie einen Haltepunkt im Quellcode festlegen möchten, zeigen Sie auf die Zeile, und wählen Sie</span><span class="sxs-lookup"><span data-stu-id="746bf-165">To set a breakpoint in your source code, hover on the line, and select</span></span> `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="DevTools-Debuggen" lightbox="./media/breakpointvs.png":::
       <span data-ttu-id="746bf-167">Der Haltepunkt wird in Visual Studio-Code gesetzt</span><span class="sxs-lookup"><span data-stu-id="746bf-167">Breakpoint is set in Visual Studio Code</span></span>  
    :::image-end:::
    
    > [!NOTE]
    > <span data-ttu-id="746bf-168">Da Visual Studio-Code keine Quell Zuordnung ausführt, stellen Sie sicher, dass Sie Haltepunkte in derselben Datei festlegen, die von WebView2 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="746bf-168">Because Visual Studio Code does not perform source mapping, ensure you set breakpoints in the same file that WebView2 uses.</span></span>  <span data-ttu-id="746bf-169">Wenn die Pfade nicht übereinstimmen, wird der ausgeführte Code nicht vom Visual Studio-Code am Haltepunkt angehalten.</span><span class="sxs-lookup"><span data-stu-id="746bf-169">If the paths do not match, Visual Studio Code does not pause the running code at the breakpoint.</span></span>  
    
1.  <span data-ttu-id="746bf-170">Führen Sie den Code aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-170">Run the code.</span></span>  
    1.  <span data-ttu-id="746bf-171">Wählen Sie auf der Registerkarte **Ausführen** im Dropdownmenü die Option Startkonfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-171">On the **Run** tab, choose the launch configuration from the dropdown menu.</span></span>  
    1.  <span data-ttu-id="746bf-172">Wenn Sie mit dem Debuggen der Anwendung beginnen möchten, wählen Sie Debuggen starten (das grüne Dreieck neben der Dropdownliste Startkonfiguration) aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-172">To start debugging your application, choose Start Debugging, which is the green triangle next to the launch configuration drop down.</span></span>  
        
        :::image type="complex" source="./media/runvs.png" alt-text="DevTools-Debuggen" lightbox="./media/runvs.png":::
           <span data-ttu-id="746bf-174">Visual Studio-Registerkarte "Code ausführen"</span><span class="sxs-lookup"><span data-stu-id="746bf-174">Visual Studio Code Run tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="746bf-175">Öffnen Sie die **Debug-Konsole** , um die Debug-Ausgabe und die Fehler anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="746bf-175">Open **Debug Console** to view the debug output and errors.</span></span>  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text="DevTools-Debuggen" lightbox="./media/resultsvs.png":::
       <span data-ttu-id="746bf-177">Visual Studio-Code Debug-Konsole</span><span class="sxs-lookup"><span data-stu-id="746bf-177">Visual Studio Code Debug Console</span></span>  
    :::image-end:::  
    
<span data-ttu-id="746bf-178">**Erweiterte Einstellungen**:</span><span class="sxs-lookup"><span data-stu-id="746bf-178">**Advanced Settings**:</span></span>  

*   <span data-ttu-id="746bf-179">Gezieltes WebView Debuggen</span><span class="sxs-lookup"><span data-stu-id="746bf-179">Targeted Webview debugging.</span></span> 

    <span data-ttu-id="746bf-180">In einigen WebView2-Anwendungen können Sie mehr als ein WebView2-Steuerelement verwenden.</span><span class="sxs-lookup"><span data-stu-id="746bf-180">In some WebView2 applications, you may use more than one WebView2 control.</span></span> <span data-ttu-id="746bf-181">So wählen Sie das WebView2-Steuerelement aus, das in dieser Situation gedebuggt werden soll Sie können das gezielte WebView2 Debuggen verwenden.</span><span class="sxs-lookup"><span data-stu-id="746bf-181">To pick the WebView2 control to debug in this situation you can use targeted webview2 debugging</span></span> 
    
    <span data-ttu-id="746bf-182">Öffnen `launch.json` und führen Sie die folgenden Aktionen aus, um ein gezieltes WebView-Debugging zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="746bf-182">Open `launch.json` and complete the following actions to use targeted Webview debugging.</span></span>  
    
    1.  <span data-ttu-id="746bf-183">Überprüfen Sie, ob der `useWebview` Parameter auf festgesetzt ist `true` .</span><span class="sxs-lookup"><span data-stu-id="746bf-183">Confirm that the `useWebview` parameter is set to `true`.</span></span>  
    1.  <span data-ttu-id="746bf-184">Fügen Sie den `urlFilter` Parameter hinzu.</span><span class="sxs-lookup"><span data-stu-id="746bf-184">Add the `urlFilter` parameter.</span></span>  <span data-ttu-id="746bf-185">Wenn das WebView2-Steuerelement zu einer URL navigiert, `urlFilter` wird der Parameterwert verwendet, um Zeichenfolgen zu vergleichen, die in der URL angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="746bf-185">When the WebView2 control navigates to a URL, the `urlFilter` parameter value is used to compare strings that appear in the URL.</span></span>  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    <span data-ttu-id="746bf-186">Wenn Sie Ihre Anwendung debuggen, müssen Sie möglicherweise den Code vom Anfang des Rendering Prozesses aus durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="746bf-186">When debugging your application, you may need to step through the code from the beginning of the rendering process.</span></span> <span data-ttu-id="746bf-187">Wenn Sie Webseiten auf Websites Rendern und keinen Zugriff auf den Quellcode haben, können Sie die Option verwenden, da Webseiten nicht `?=value`  erkannte Parameter ignorieren.</span><span class="sxs-lookup"><span data-stu-id="746bf-187">If you are rendering webpages on sites and you don't have access to the source code, you can use the `?=value` option, because webpages ignore unrecognized parameters.</span></span>   
    
    > [!IMPORTANT]
    > <span data-ttu-id="746bf-188">Nachdem die erste Übereinstimmung in der URL gefunden wurde, wird der Debugger angehalten.</span><span class="sxs-lookup"><span data-stu-id="746bf-188">After the first match is found in the URL, the debugger stops.</span></span>  <span data-ttu-id="746bf-189">Zwei WebView2-Steuerelemente können nicht gleichzeitig gedebuggt werden, da der CDP-Port von allen WebView2-Steuerelementen freigegeben wird und eine einzelne Portnummer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="746bf-189">You cannot debug two WebView2 controls at the same time because the CDP port is shared by all WebView2 controls, and uses a single port number.</span></span>  
    
*   <span data-ttu-id="746bf-190">Debuggen von ausgeführten Prozessen</span><span class="sxs-lookup"><span data-stu-id="746bf-190">Debug running processes</span></span>  
    
    <span data-ttu-id="746bf-191">Möglicherweise müssen Sie den Debugger an die ausgeführten WebView2-Prozesse anfügen.</span><span class="sxs-lookup"><span data-stu-id="746bf-191">You may need to attach the debugger to running WebView2 processes.</span></span> <span data-ttu-id="746bf-192">Aktualisieren Sie dazu `launch.json` den `request` Parameter in `attach` .</span><span class="sxs-lookup"><span data-stu-id="746bf-192">To do that, in `launch.json`, update the `request` parameter to `attach`.</span></span>
        
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
        
    <span data-ttu-id="746bf-193">Das WebView2-Steuerelement muss den CDP-Port öffnen, um das Debuggen des WebView2-Steuerelements zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="746bf-193">Your WebView2 control must open the CDP port to allow debugging of the WebView2 control.</span></span>  <span data-ttu-id="746bf-194">Ihr Code muss erstellt werden, um sicherzustellen, dass nur ein WebView2-Steuerelement einen CDP-Port (Chrome Developer Protocol) geöffnet hat, bevor der Debugger gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="746bf-194">Your code must be built to ensure that only one WebView2 control has a Chrome Developer Protocol (CDP) port open, before starting the debugger.</span></span>  
    
*   <span data-ttu-id="746bf-195">Debug-Ablaufverfolgungsoptionen</span><span class="sxs-lookup"><span data-stu-id="746bf-195">Debug tracing options</span></span>  
    
    <span data-ttu-id="746bf-196">Fügen Sie den zu `trace` launch.jsden Parameter hinzu, um die Debug-Ablaufverfolgung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="746bf-196">Add the `trace` parameter to launch.json to enable debug tracing.</span></span>  
    
    1.  <span data-ttu-id="746bf-197">Parameter hinzufügen `trace` .</span><span class="sxs-lookup"><span data-stu-id="746bf-197">Add `trace` parameter.</span></span>  
        
 
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text="DevTools-Debuggen" lightbox="./media/tracelog.png":::
                 <span data-ttu-id="746bf-199">Speichern der Debug-Ausgabe in einer Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="746bf-199">Save debug output to a log file</span></span>  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text="DevTools-Debuggen" lightbox="./media/verbose.png":::
                 <span data-ttu-id="746bf-201">Visual Studio-Code Debug-Ausgabe mit aktivierter ausführlicher Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="746bf-201">Visual Studio Code Debug Output with verbose tracing turned on</span></span>  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   <span data-ttu-id="746bf-202">Debuggen von Office-Add-ins</span><span class="sxs-lookup"><span data-stu-id="746bf-202">Debug Office Add-ins.</span></span>
    
    <span data-ttu-id="746bf-203">Wenn Sie Office-Add-ins Debuggen, öffnen Sie den Add-in-Quellcode in einer separaten Instanz von Visual Studio-Code.</span><span class="sxs-lookup"><span data-stu-id="746bf-203">If you're debugging Office Add-ins, open the add-in source code in a separate instance of Visual Studio Code.</span></span>  <span data-ttu-id="746bf-204">Öffnen Sie launch.jsin ihrer WebView2-Anwendung, und fügen Sie den folgenden Codeausschnitt hinzu, um den Debugger an das Office-Add-in anzufügen.</span><span class="sxs-lookup"><span data-stu-id="746bf-204">Open launch.json in your WebView2 application and add the following code snippet to attach the debugger to the Office add-in.</span></span>
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   <span data-ttu-id="746bf-205">Problembehandlung des Debuggers</span><span class="sxs-lookup"><span data-stu-id="746bf-205">Troubleshooting the debugger</span></span>  
    
    <span data-ttu-id="746bf-206">Bei Verwendung des Debuggers können die folgenden Szenarien auftreten.</span><span class="sxs-lookup"><span data-stu-id="746bf-206">You may encounter the following scenarios when using the debugger.</span></span>  

    *   <span data-ttu-id="746bf-207">Der Debugger wird nicht am Haltepunkt angehalten, und Sie haben die Debug-Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="746bf-207">The debugger doesn't stop at the breakpoint, and you have debug output.</span></span>  <span data-ttu-id="746bf-208">Um das Problem zu beheben, stellen Sie sicher, dass die Datei mit dem Haltepunkt dieselbe Datei ist, die vom WebView2-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="746bf-208">To solve the issue, confirm that the file with the breakpoint is the same file that's used by the WebView2 control.</span></span>  <span data-ttu-id="746bf-209">Der Debugger führt keine Quell Pfadzuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="746bf-209">The debugger doesn't perform source path mapping.</span></span>  
    *   <span data-ttu-id="746bf-210">Sie können nicht an einen ausgeführten Prozess anfügen, und Sie erhalten einen Timeoutfehler.</span><span class="sxs-lookup"><span data-stu-id="746bf-210">You can't attach to a running process, and you get a timeout error.</span></span>  <span data-ttu-id="746bf-211">Um das Problem zu beheben, stellen Sie sicher, dass das WebView2-Steuerelement den CDP-Port geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="746bf-211">To solve the issue, confirm that the WebView2 control opened the CDP port.</span></span>  <span data-ttu-id="746bf-212">Stellen Sie sicher, dass Ihr  `additionalBrowserArguments`  Wert in der Registrierung richtig ist, oder die Optionen richtig sind.</span><span class="sxs-lookup"><span data-stu-id="746bf-212">Ensure your `additionalBrowserArguments` value in the registry is correct, or the options are correct.</span></span>  <span data-ttu-id="746bf-213">Weitere Informationen finden Sie unter [additionalBrowserArguments for dotnet] [Webview2ReferenceDotnet09515MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] und [additionalBrowserArguments für Win32] [Webview2ReferenceWin3209538Webview2IdlParameters].</span><span class="sxs-lookup"><span data-stu-id="746bf-213">For more information, see [additionalBrowserArguments for dotnet][Webview2ReferenceDotnet09515MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] and [additionalBrowserArguments for Win32][Webview2ReferenceWin3209538Webview2IdlParameters].</span></span>  
    
* * *  


* * *  

## <span data-ttu-id="746bf-214">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="746bf-214">See also</span></span>  

*   <span data-ttu-id="746bf-215">Informationen zum Einstieg in die Verwendung von WebView2 finden Sie unter [WebView2 erste Schritte][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="746bf-215">To get started using WebView2, see [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="746bf-216">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie im [WebView2Samples][GithubMicrosoftedgeWebview2samples] -Repo auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="746bf-216">For a comprehensive example of WebView2 capabilities, see the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="746bf-217">Ausführlichere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="746bf-217">For more detailed information about WebView2 APIs, see [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="746bf-218">Weitere Informationen zu WebView2 finden Sie unter [WebView2-Ressourcen][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="746bf-218">For more information about WebView2, see [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="746bf-219">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="746bf-219">Getting in touch with the Microsoft Edge WebView team</span></span>  

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

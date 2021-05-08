---
description: Erfahren Sie, wie Sie WebView2-Steuerelemente debuggen.
title: Erste Schritte beim Debuggen von WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: f895634d5e005bb07579d9a5f41c6a988cd78a33
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536536"
---
# <a name="get-started-debugging-webview2-apps"></a><span data-ttu-id="788e5-104">Erste Schritte beim Debuggen von WebView2-Apps</span><span class="sxs-lookup"><span data-stu-id="788e5-104">Get started debugging WebView2 apps</span></span>  

<span data-ttu-id="788e5-105">Das Ziel des Microsoft Edge WebView2-Steuerelements besteht in der Kombination der besten Features und Tools für die Web- und native App-Entwicklung.</span><span class="sxs-lookup"><span data-stu-id="788e5-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native app development features and tools.</span></span>  <span data-ttu-id="788e5-106">Wenn Sie Ihre WebView2-App entwickeln, sollten Sie Ihre App debuggen.</span><span class="sxs-lookup"><span data-stu-id="788e5-106">When you develop your WebView2 app, you should debug your app.</span></span>  <span data-ttu-id="788e5-107">In diesem Artikel werden die verschiedenen Tools beschrieben, die zum Debuggen ihres Web- und systemeigenen Codes in Ihrer WebView2-App verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="788e5-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 app.</span></span>  

## [<a name="microsoft-edge-devtools"></a><span data-ttu-id="788e5-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="788e5-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="788e5-109">Verwenden [Microsoft Edge (Chromium)-Entwicklertools][DevtoolsGuideChromiumMain] zum Debuggen von Webinhalten, die in WebView2-Steuerelementen angezeigt werden, auf die gleiche Weise wie für eine andere Webseite, die in webView2-Steuerelementen angezeigt Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="788e5-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="788e5-110">Zum Öffnen der DevTools legen Sie den Fokus auf das WebView-Steuerelement, und verwenden Sie dann eine der folgenden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="788e5-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="788e5-111">Wählen Sie `F12` aus.</span><span class="sxs-lookup"><span data-stu-id="788e5-111">Select `F12`.</span></span>  
*   <span data-ttu-id="788e5-112">Wählen Sie `Ctrl` + `Shift` + `I` aus.</span><span class="sxs-lookup"><span data-stu-id="788e5-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="788e5-113">Öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie `Inspect` aus.</span><span class="sxs-lookup"><span data-stu-id="788e5-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  
    
<span data-ttu-id="788e5-114">Weitere Informationen finden Sie unter [DevTools overview][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="788e5-114">For more information, navigate to [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="DevTools-Debugging" lightbox="./media/f12.png":::
   <span data-ttu-id="788e5-116">DevTools-Debugging</span><span class="sxs-lookup"><span data-stu-id="788e5-116">DevTools debugging</span></span>  
:::image-end:::  

## [<a name="visual-studio"></a><span data-ttu-id="788e5-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="788e5-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="788e5-118">Visual Studio bietet verschiedene Debuggingtools für Web- und systemeigenen Code in WebView2-Apps.</span><span class="sxs-lookup"><span data-stu-id="788e5-118">Visual Studio provides various debugging tools for web and native code in WebView2 apps.</span></span>  <span data-ttu-id="788e5-119">Im Abschnitt Visual Studio liegt der Hauptfokus auf dem Debuggen von WebView-Steuerelementen, die anderen Methoden des Debuggens in Visual Studio sind jedoch wie gewohnt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="788e5-119">In the Visual Studio section, the primary focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="788e5-120">Verwenden Sie den folgenden Prozess, um Web- und systemeigenen Code nur in Win32-Apps oder Office-Add-Ins zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="788e5-120">Use the following process to debug web and native code in Win32 apps or Office Add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="788e5-121">Wenn Sie Ihre App in Visual Studio mit dem systemeigenen Debugger debuggen, kann die Auswahl den systemeigenen Debugger anstelle von `F12` Entwicklertools auslösen.</span><span class="sxs-lookup"><span data-stu-id="788e5-121">When you debug your app in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="788e5-122">Wählen `Ctrl` + `Shift` + `I` Sie aus, oder verwenden Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), um die Situation zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="788e5-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="788e5-123">Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Anforderungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="788e5-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="788e5-124">Zum Debuggen von Skripts muss die App innerhalb eines Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="788e5-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="788e5-125">Sie können keinen Debugger an einen ausgeführten WebView2-Prozess anfügen.</span><span class="sxs-lookup"><span data-stu-id="788e5-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="788e5-126">Installieren Visual Studio 2019, Version 16.4 Preview 2 oder höher.</span><span class="sxs-lookup"><span data-stu-id="788e5-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  
    
<span data-ttu-id="788e5-127">Installieren und Einrichten der Skriptdebuggertools in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="788e5-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="788e5-128">Führen Sie die folgenden Aktionen aus, um die **#A0** in der **Desktopentwicklung mit C++ zu installieren.**</span><span class="sxs-lookup"><span data-stu-id="788e5-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  
    
    1.  <span data-ttu-id="788e5-129">Geben Sie in Windows Explorerleiste `Visual Studio Installer` ein.</span><span class="sxs-lookup"><span data-stu-id="788e5-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1.  <span data-ttu-id="788e5-130">Wählen **Visual Studio-Installer,** um es zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="788e5-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1.  <span data-ttu-id="788e5-131">Wählen Sie Visual Studio-Installer in der installierten Version die Schaltfläche **Mehr** aus, und wählen Sie dann **Ändern aus.**</span><span class="sxs-lookup"><span data-stu-id="788e5-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1.  <span data-ttu-id="788e5-132">Wählen Visual Studio unter **Arbeitsauslastungen**die Einstellung **Desktopentwicklung in C++** aus.</span><span class="sxs-lookup"><span data-stu-id="788e5-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Visual Studio Ändern des Bildschirms für Arbeitsauslastungen" lightbox="./media/workloads.png":::
            <span data-ttu-id="788e5-134">Visual Studio Ändern des Bildschirms für Arbeitsauslastungen</span><span class="sxs-lookup"><span data-stu-id="788e5-134">Visual Studio Modifying Workloads Screen</span></span>
        :::image-end:::  
        
    1.  <span data-ttu-id="788e5-135">Wählen **Sie Einzelne Komponenten aus.**</span><span class="sxs-lookup"><span data-stu-id="788e5-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="788e5-136">Geben Sie im Suchfeld `JavaScript diagnostics` ein.</span><span class="sxs-lookup"><span data-stu-id="788e5-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="788e5-137">Wählen Sie die **JavaScript-Diagnoseeinstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="788e5-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="788e5-138">Wählen Sie **Ändern**aus.</span><span class="sxs-lookup"><span data-stu-id="788e5-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio Ändern der Registerkarte "Einzelne Komponenten"" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="788e5-140">Visual Studio Ändern der Registerkarte "Einzelne Komponenten"</span><span class="sxs-lookup"><span data-stu-id="788e5-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="788e5-141">Aktivieren sie das Skriptdebubuing für WebView2-Apps.</span><span class="sxs-lookup"><span data-stu-id="788e5-141">Enable script debugging for WebView2 apps.</span></span>  
    1.  <span data-ttu-id="788e5-142">Öffnen Sie in Ihrem WebView2-Projekt das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Eigenschaften aus.**</span><span class="sxs-lookup"><span data-stu-id="788e5-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="788e5-143">Wählen Sie **unter Konfigurationseigenschaften** **Debuggen aus.**</span><span class="sxs-lookup"><span data-stu-id="788e5-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="788e5-144">Wählen Sie **unter Debuggertyp** **JavaScript (WebView2)** aus.</span><span class="sxs-lookup"><span data-stu-id="788e5-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Visual Studio Debugkonfigurationseigenschaft" lightbox="./media/enbjs.png":::
           <span data-ttu-id="788e5-146">Visual Studio **Debugkonfigurationseigenschaft**</span><span class="sxs-lookup"><span data-stu-id="788e5-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="788e5-147">Führen Sie die folgenden Aktionen aus, um Ihre WebView2-App zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="788e5-147">Complete the following actions to debug your WebView2 app.</span></span>  

1.  <span data-ttu-id="788e5-148">Wenn Sie einen Haltepunkt im Quellcode festlegen, zeigen Sie links neben der Zeilennummer, und wählen Sie einen Haltepunkt aus.</span><span class="sxs-lookup"><span data-stu-id="788e5-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="788e5-149">Der JS/TS-Debugadapter führt keine Quellpfadzuordnung durch.</span><span class="sxs-lookup"><span data-stu-id="788e5-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="788e5-150">Sie müssen den exakt gleichen Pfad öffnen, der Mit WebView2 verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="788e5-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio haltepunkt hinzufügen" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="788e5-152">Visual Studio haltepunkt hinzufügen</span><span class="sxs-lookup"><span data-stu-id="788e5-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="788e5-153">Wählen Sie zum Ausführen des Debuggers die Bitgröße der Plattform aus, und wählen Sie dann die grüne Wiedergabeschaltfläche neben **Local Windows Debugger aus.**</span><span class="sxs-lookup"><span data-stu-id="788e5-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="788e5-154">Die App wird ausgeführt, und der Debugger stellt eine Verbindung mit dem ersten erstellten WebView2-Prozess sicher.</span><span class="sxs-lookup"><span data-stu-id="788e5-154">The app runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Visual Studio Lokaler Windows Debugger" lightbox="./media/run.png"::: 
       <span data-ttu-id="788e5-156">Visual Studio Local **Windows Debugger**</span><span class="sxs-lookup"><span data-stu-id="788e5-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="788e5-157">Suchen Sie **in der Debugkonsole**nach der Ausgabe des Debuggers.</span><span class="sxs-lookup"><span data-stu-id="788e5-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio Debugkonsole" lightbox="./media/console.png"::: 
       <span data-ttu-id="788e5-159">Visual Studio Debug **console**</span><span class="sxs-lookup"><span data-stu-id="788e5-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
## [<a name="visual-studio-code"></a><span data-ttu-id="788e5-160">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="788e5-160">Visual Studio Code</span></span>](#tab/visualstudiocode)  

<span data-ttu-id="788e5-161">Verwenden Microsoft Visual Studio Code zum Debuggen von Skripts, die in WebView2-Steuerelementen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="788e5-161">Use Microsoft Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

<span data-ttu-id="788e5-162">Führen Visual Studio Code die folgenden Aktionen aus, um Den Code zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="788e5-162">In Visual Studio Code, complete the following actions to debug your code.</span></span> 

1.  <span data-ttu-id="788e5-163">Ihr Projekt muss über eine Datei `launch.json` verfügen.</span><span class="sxs-lookup"><span data-stu-id="788e5-163">Your project is required to have a `launch.json` file.</span></span>  <span data-ttu-id="788e5-164">Wenn Ihr Projekt keine Datei enthält, kopieren Sie den `launch.json` folgenden Codeausschnitt, und erstellen Sie eine neue `launch.json` Datei.</span><span class="sxs-lookup"><span data-stu-id="788e5-164">If your project doesn't have a `launch.json` file, copy the following code snippet and create a new `launch.json` file.</span></span>  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",
        "env": {
            // Customize for your app location if needed
            "Path": "%path%;e:/path/to/your/app/location; "
        },
        "useWebView": true,
        // The following two lines setup source path mapping, where `url` is the start page of your app, and `webRoot` is the top level directory with all your code files.
        "url": "file:///${workspaceFolder}/path/to/your/toplevel/foo.html",
        "webRoot": "${workspaceFolder}/path/to/your/assets"
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="788e5-165">Visual Studio Code Die Zuordnung des Quellpfads erfordert nun die URL, sodass Ihre App jetzt beim Starten einen Befehlszeilenparameter empfängt.</span><span class="sxs-lookup"><span data-stu-id="788e5-165">Visual Studio Code source path mapping now requires the URL, so your app now receives a command-line parameter when it starts.</span></span>  <span data-ttu-id="788e5-166">Sie können den Parameter bei Bedarf `url` sicher ignorieren.</span><span class="sxs-lookup"><span data-stu-id="788e5-166">You may safely ignore the `url` parameter if needed.</span></span>  
    
1.  <span data-ttu-id="788e5-167">Zum Festlegen eines Haltepunkts im Quellcode zeigen Sie auf die Zeile, und wählen Sie</span><span class="sxs-lookup"><span data-stu-id="788e5-167">To set a breakpoint in your source code, hover on the line, and select</span></span> `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="Der Haltepunkt wird in Visual Studio Code" lightbox="./media/breakpointvs.png":::
       <span data-ttu-id="788e5-169">Der Haltepunkt wird in Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="788e5-169">Breakpoint is set in Visual Studio Code</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="788e5-170">Führen Sie den Code aus.</span><span class="sxs-lookup"><span data-stu-id="788e5-170">Run the code.</span></span>  
    1.  <span data-ttu-id="788e5-171">Wählen Sie **auf der** Registerkarte Ausführen im Dropdownmenü die Startkonfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="788e5-171">On the **Run** tab, choose the launch configuration from the dropdown menu.</span></span>  
    1.  <span data-ttu-id="788e5-172">Wenn Sie mit dem Debuggen Ihrer App beginnen möchten, wählen Sie Debuggen starten aus. Dabei handelt es sich um das grüne Dreieck neben der Startkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="788e5-172">To start debugging your app, choose Start Debugging, which is the green triangle next to the launch configuration drop down.</span></span>  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Visual Studio Code Registerkarte "Ausführen"" lightbox="./media/runvs.png":::
           <span data-ttu-id="788e5-174">Visual Studio Code Registerkarte "Ausführen"</span><span class="sxs-lookup"><span data-stu-id="788e5-174">Visual Studio Code Run tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="788e5-175">Öffnen **Sie die Debugkonsole,** um die Debugausgabe und Fehler anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="788e5-175">Open **Debug Console** to view the debug output and errors.</span></span>  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Visual Studio Code Debugkonsole" lightbox="./media/resultsvs.png":::
       <span data-ttu-id="788e5-177">Visual Studio Code Debugkonsole</span><span class="sxs-lookup"><span data-stu-id="788e5-177">Visual Studio Code Debug Console</span></span>  
    :::image-end:::  
    
<span data-ttu-id="788e5-178">**Erweiterte Einstellungen**:</span><span class="sxs-lookup"><span data-stu-id="788e5-178">**Advanced Settings**:</span></span>  

*   <span data-ttu-id="788e5-179">Gezieltes Webview-Debugging.</span><span class="sxs-lookup"><span data-stu-id="788e5-179">Targeted Webview debugging.</span></span> 
    
    <span data-ttu-id="788e5-180">In einigen WebView2-Apps können Sie mehrere WebView2-Steuerelemente verwenden.</span><span class="sxs-lookup"><span data-stu-id="788e5-180">In some WebView2 apps, you may use more than one WebView2 control.</span></span> <span data-ttu-id="788e5-181">Zum Auswählen des zu debuggenden WebView2-Steuerelements in dieser Situation können Sie das gezielte Webview2-Debuggen verwenden.</span><span class="sxs-lookup"><span data-stu-id="788e5-181">To pick the WebView2 control to debug in this situation you can use targeted webview2 debugging</span></span> 
    
    <span data-ttu-id="788e5-182">Öffnen `launch.json` Und führen Sie die folgenden Aktionen aus, um das gezielte Webview-Debugging zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="788e5-182">Open `launch.json` and complete the following actions to use targeted Webview debugging.</span></span>  
    
    1.  <span data-ttu-id="788e5-183">Vergewissern Sie `useWebview` sich, dass der Parameter auf festgelegt `true` ist.</span><span class="sxs-lookup"><span data-stu-id="788e5-183">Confirm that the `useWebview` parameter is set to `true`.</span></span>  
    1.  <span data-ttu-id="788e5-184">Fügen Sie den Parameter `urlFilter` hinzu.</span><span class="sxs-lookup"><span data-stu-id="788e5-184">Add the `urlFilter` parameter.</span></span>  <span data-ttu-id="788e5-185">Wenn das WebView2-Steuerelement zu einer URL navigiert, wird der Parameterwert zum Vergleichen von Zeichenfolgen verwendet, `urlFilter` die in der URL angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="788e5-185">When the WebView2 control navigates to a URL, the `urlFilter` parameter value is used to compare strings that appear in the URL.</span></span>  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    <span data-ttu-id="788e5-186">Beim Debuggen Ihrer App müssen Sie den Code möglicherweise von Beginn des Renderingprozesses aus durchschritten.</span><span class="sxs-lookup"><span data-stu-id="788e5-186">When debugging your app, you may need to step through the code from the beginning of the rendering process.</span></span> <span data-ttu-id="788e5-187">Wenn Sie Webseiten auf Websites rendern und keinen Zugriff auf den Quellcode haben, können Sie die Option verwenden, da Webseiten unbekannte Parameter `?=value`  ignorieren.</span><span class="sxs-lookup"><span data-stu-id="788e5-187">If you are rendering webpages on sites and you don't have access to the source code, you can use the `?=value` option, because webpages ignore unrecognized parameters.</span></span>   
    
    > [!IMPORTANT]
    > <span data-ttu-id="788e5-188">Nachdem die erste Übereinstimmung in der URL gefunden wurde, wird der Debugger beendet.</span><span class="sxs-lookup"><span data-stu-id="788e5-188">After the first match is found in the URL, the debugger stops.</span></span>  <span data-ttu-id="788e5-189">Sie können zwei WebView2-Steuerelemente nicht gleichzeitig debuggen, da der CDP-Port von allen WebView2-Steuerelementen gemeinsam genutzt wird und eine einzelne Portnummer verwendet.</span><span class="sxs-lookup"><span data-stu-id="788e5-189">You cannot debug two WebView2 controls at the same time because the CDP port is shared by all WebView2 controls, and uses a single port number.</span></span>  
    
*   <span data-ttu-id="788e5-190">Debuggen ausgeführter Prozesse</span><span class="sxs-lookup"><span data-stu-id="788e5-190">Debug running processes</span></span>  
    
    <span data-ttu-id="788e5-191">Möglicherweise müssen Sie den Debugger an die Ausführung von WebView2-Prozessen anfügen.</span><span class="sxs-lookup"><span data-stu-id="788e5-191">You may need to attach the debugger to running WebView2 processes.</span></span> <span data-ttu-id="788e5-192">Aktualisieren Sie dazu in `launch.json` den Parameter `request` auf `attach` .</span><span class="sxs-lookup"><span data-stu-id="788e5-192">To do that, in `launch.json`, update the `request` parameter to `attach`.</span></span>
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    <span data-ttu-id="788e5-193">Ihr WebView2-Steuerelement muss den CDP-Port öffnen, um das Debuggen des WebView2-Steuerelements zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="788e5-193">Your WebView2 control must open the CDP port to allow debugging of the WebView2 control.</span></span>  <span data-ttu-id="788e5-194">Ihr Code muss so erstellt werden, dass nur ein WebView2-Steuerelement über einen geöffneten Chrome Developer Protocol (CDP)-Port verfügt, bevor der Debugger gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="788e5-194">Your code must be built to ensure that only one WebView2 control has a Chrome Developer Protocol (CDP) port open, before starting the debugger.</span></span>  
    
*   <span data-ttu-id="788e5-195">Debuggen von Ablaufverfolgungsoptionen</span><span class="sxs-lookup"><span data-stu-id="788e5-195">Debug tracing options</span></span>  
    
    <span data-ttu-id="788e5-196">Fügen Sie den `trace` Parameter hinzu, launch.jsaktiviert werden soll, um die Debugablaufverfolgung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="788e5-196">Add the `trace` parameter to launch.json to enable debug tracing.</span></span>  
    
    1.  <span data-ttu-id="788e5-197">`trace`Add-Parameter.</span><span class="sxs-lookup"><span data-stu-id="788e5-197">Add `trace` parameter.</span></span>  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Speichern Sie die Debugausgabe in einer Protokolldatei." lightbox="./media/tracelog.png":::
                 <span data-ttu-id="788e5-199">Speichern der Debugausgabe in einer Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="788e5-199">Save debug output to a log file</span></span>  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Ausführliche Ausgabe" lightbox="./media/verbose.png":::
                 <span data-ttu-id="788e5-201">Visual Studio Code Debuggen der Ausgabe mit aktivierter ausführlicher Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="788e5-201">Visual Studio Code Debug Output with verbose tracing turned on</span></span>  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   <span data-ttu-id="788e5-202">Debuggen Office Add-Ins.</span><span class="sxs-lookup"><span data-stu-id="788e5-202">Debug Office Add-ins.</span></span>  
    
    <span data-ttu-id="788e5-203">Öffnen Sie beim Debuggen Office Add-Ins den Add-In-Quellcode in einer separaten Instanz Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="788e5-203">If you're debugging Office Add-ins, open the add-in source code in a separate instance of Visual Studio Code.</span></span>  <span data-ttu-id="788e5-204">Öffnen launch.jsin Ihrer WebView2-App, und fügen Sie den folgenden Codeausschnitt hinzu, um den Debugger an das Office anfügen.</span><span class="sxs-lookup"><span data-stu-id="788e5-204">Open launch.json in your WebView2 app and add the following code snippet to attach the debugger to the Office add-in.</span></span>
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   <span data-ttu-id="788e5-205">Problembehandlung beim Debugger</span><span class="sxs-lookup"><span data-stu-id="788e5-205">Troubleshooting the debugger</span></span>  
    
    <span data-ttu-id="788e5-206">Bei Verwendung des Debuggers können die folgenden Szenarien auftreten.</span><span class="sxs-lookup"><span data-stu-id="788e5-206">You may encounter the following scenarios when using the debugger.</span></span>  
    
    *   <span data-ttu-id="788e5-207">Der Debugger wird nicht am Haltepunkt beendet, und Sie haben eine Debugausgabe.</span><span class="sxs-lookup"><span data-stu-id="788e5-207">The debugger doesn't stop at the breakpoint, and you have debug output.</span></span>  <span data-ttu-id="788e5-208">Um das Problem zu beheben, vergewissern Sie sich, dass die Datei mit dem Haltepunkt dieselbe Datei ist, die vom WebView2-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="788e5-208">To solve the issue, confirm that the file with the breakpoint is the same file that's used by the WebView2 control.</span></span>  <span data-ttu-id="788e5-209">Der Debugger führt keine Quellpfadzuordnung durch.</span><span class="sxs-lookup"><span data-stu-id="788e5-209">The debugger doesn't perform source path mapping.</span></span>  
    *   <span data-ttu-id="788e5-210">Sie können keinen laufenden Prozess anfügen, und Es wird ein Timeoutfehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="788e5-210">You can't attach to a running process, and you get a timeout error.</span></span>  <span data-ttu-id="788e5-211">Um das Problem zu beheben, vergewissern Sie sich, dass das WebView2-Steuerelement den CDP-Port geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="788e5-211">To solve the issue, confirm that the WebView2 control opened the CDP port.</span></span>  <span data-ttu-id="788e5-212">Stellen Sie  `additionalBrowserArguments`  sicher, dass der Wert in der Registrierung korrekt ist oder die Optionen richtig sind.</span><span class="sxs-lookup"><span data-stu-id="788e5-212">Ensure your `additionalBrowserArguments` value in the registry is correct, or the options are correct.</span></span>  <span data-ttu-id="788e5-213">Weitere Informationen finden Sie unter [additionalBrowserArguments for dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] und [additionalBrowserArguments for Win32][Webview2ReferenceWin32Webview2IdlParameters].</span><span class="sxs-lookup"><span data-stu-id="788e5-213">For more information, navigate to [additionalBrowserArguments for dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] and [additionalBrowserArguments for Win32][Webview2ReferenceWin32Webview2IdlParameters].</span></span>  
    
* * *  

## <a name="see-also"></a><span data-ttu-id="788e5-214">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="788e5-214">See also</span></span>  

*   <span data-ttu-id="788e5-215">Navigieren Sie zu [WebView2 Getting Started Guides,][Webview2MainGettingStarted]um mit WebView2 zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="788e5-215">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="788e5-216">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie im [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samples] GitHub.</span><span class="sxs-lookup"><span data-stu-id="788e5-216">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="788e5-217">Weitere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="788e5-217">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="788e5-218">Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="788e5-218">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="788e5-219">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="788e5-219">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "CoreWebView2EnvironmentOptions.AdditionalBrowserArguments Property (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment – Globale | Microsoft Docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

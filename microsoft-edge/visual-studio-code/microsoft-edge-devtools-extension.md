---
description: Verwenden von Elementen für Microsoft Edge (Chromium) aus Visual Studio Code
title: Elemente für Microsoft Edge (Chromium) aus Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, vs code, visual studio code, elements
ms.openlocfilehash: 83bac187fa2a9b1766a52f3f2cd176f171846e02
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398455"
---
# <a name="microsoft-edge-devtools-for-visual-studio-code-extension"></a><span data-ttu-id="0966f-104">Microsoft Edge DevTools für Visual Studio Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="0966f-104">Microsoft Edge DevTools for Visual Studio Code extension</span></span>  

<span data-ttu-id="0966f-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="0966f-105">Use</span></span> <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] --><span data-ttu-id="0966f-106">diese Erweiterung für den Zugriff in Microsoft Edge DevTools innerhalb [Microsoft Visual Studio Code .][VisualstudioCode]</span><span class="sxs-lookup"><span data-stu-id="0966f-106">this extension to access in Microsoft Edge DevTools inside [Microsoft Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="0966f-107">Sie haben Zugriff auf die **Elemente** **und** Netzwerktools in Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="0966f-107">You have access to the **Elements** and **Network** tools in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="0966f-108">Sie können eine Instanz der Datei entweder starten oder Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0966f-108">You may either launch or attach to an instance of Microsoft Edge.</span></span>  <span data-ttu-id="0966f-109">Nachdem Sie eine Verbindung hergestellt haben, können Sie die Laufzeit-HTML-Struktur anzeigen, das Layout ändern, Formatierungsprobleme beheben und den Netzwerkdatenverkehr überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0966f-109">After you connect you may display the runtime HTML structure, alter the layout, fix styling issues, and inspect network traffic.</span></span>  

## <a name="elements-tool"></a><span data-ttu-id="0966f-110">Elementtool</span><span class="sxs-lookup"><span data-stu-id="0966f-110">Elements tool</span></span>  

<span data-ttu-id="0966f-111">Standardmäßig startet die Erweiterung eine Browserinstanz in einem eindeutigen Fenster und bietet Ihnen die **Elements-Funktionalität** Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="0966f-111">By default, the extension launches a browser instance in a unique window and gives you the **Elements** functionality of Microsoft Edge DevTools.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools für Visual Studio Code, die mit einem vollständigen Browserfenster ausgeführt werden" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   <span data-ttu-id="0966f-113">Microsoft Edge DevTools für Visual Studio Code, die mit einem vollständigen Browserfenster ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="0966f-113">Microsoft Edge DevTools for Visual Studio Code running with a full browser window</span></span>  
:::image-end:::  

<span data-ttu-id="0966f-114">In den Erweiterungseinstellungen können Sie weitere Funktionen wie **headless Mode** und **Network aktivieren.**</span><span class="sxs-lookup"><span data-stu-id="0966f-114">In the extension settings, you may enable more functionality like **Headless Mode** and **Network**.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Aktivieren (oder Deaktivieren) des kopflosen Modus und der Netzwerkprüfung in den Erweiterungseinstellungen" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   <span data-ttu-id="0966f-116">Aktivieren des kopflosen Modus \(oder Deaktivieren\) und Netzwerkprüfung in den Erweiterungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="0966f-116">Enabling \(or disabling\) headless mode and Network inspection in the extension settings</span></span>  
:::image-end:::  

## <a name="headless-mode"></a><span data-ttu-id="0966f-117">Kopfloser Modus</span><span class="sxs-lookup"><span data-stu-id="0966f-117">Headless Mode</span></span>  

<span data-ttu-id="0966f-118">Im kopflosen Modus startet diese Erweiterung keine vollständige Browserinstanz zum Debuggen.</span><span class="sxs-lookup"><span data-stu-id="0966f-118">In headless mode, this extension does not launch a full browser instance to debug.</span></span>  <span data-ttu-id="0966f-119">Es wird eine Instanz im Hintergrund ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0966f-119">It runs an instance in the background.</span></span>  <span data-ttu-id="0966f-120">Möglicherweise müssen Sie im Editor bleiben und mit dem eingebetteten Browser interagieren.</span><span class="sxs-lookup"><span data-stu-id="0966f-120">You may have to stay inside the editor and interact with the embedded browser.</span></span>  <span data-ttu-id="0966f-121">Ein zusätzliches Browsersymbol wird nicht in der Taskleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0966f-121">An extra browser icon is not be displayed in your task bar.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools für Visual Studio Code, die ohne Kopf ausgeführt werden" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   <span data-ttu-id="0966f-123">Microsoft Edge DevTools für Visual Studio Code, die mit einem kopflosen Browser ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="0966f-123">Microsoft Edge DevTools for Visual Studio Code running with a headless browser</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="0966f-124">Unter macOS sollten Sie den Kopflosenmodus als bevorzugten Modus aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0966f-124">On macOS, you should turn on headless mode as your preferred mode.</span></span>  <span data-ttu-id="0966f-125">Die Verwendung des Kopflosenmodus sollte ein Problem lösen, bei dem das Browserfenster meldet, dass es sich um handelt, wenn das Fenster nicht sichtbar `Not Active` ist.</span><span class="sxs-lookup"><span data-stu-id="0966f-125">Using headless mode should solve an issue where, if the window is not visible, the browser window reports that it is `Not Active`.</span></span>  

## <a name="network-tool"></a><span data-ttu-id="0966f-126">Network-Tool</span><span class="sxs-lookup"><span data-stu-id="0966f-126">Network tool</span></span>  

<span data-ttu-id="0966f-127">Wenn Sie auch den Netzwerkdatenverkehr Ihrer Anwendung überprüfen möchten, öffnen Sie die Einstellungen, und aktivieren Sie **die** Registerkarte Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0966f-127">If you also want to inspect the network traffic of your application, open the settings and turn on the **Network** tab.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Netzwerkprüfung in Microsoft Edge DevTools für Visual Studio Code" lightbox="./media/edge-devtools-for-vscode-network.png":::
    <span data-ttu-id="0966f-129">Netzwerkprüfung in Microsoft Edge DevTools für Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="0966f-129">Network inspection in Microsoft Edge DevTools for Visual Studio Code</span></span>  
:::image-end:::  

## <a name="launching-microsoft-edge-from-the-extension"></a><span data-ttu-id="0966f-130">Starten Microsoft Edge aus der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="0966f-130">Launching Microsoft Edge From the extension</span></span>  

<span data-ttu-id="0966f-131">Navigieren Sie zu Microsoft Edge Tools in der **Aktivitätsleiste**.</span><span class="sxs-lookup"><span data-stu-id="0966f-131">Navigate to Microsoft Edge Tools in the **Activity Bar**.</span></span>  <span data-ttu-id="0966f-132">Neben der Stelle, Microsoft Edge **Tools: Targets steht,** gibt es ein Pluszeichen, das den Browser für Ihre App öffnet.</span><span class="sxs-lookup"><span data-stu-id="0966f-132">Next to where it says **Microsoft Edge Tools: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="0966f-133">Wenn Sie die **Option about:blank** auswählen, müssen Sie zu Ihrer Web-App im Browser navigieren, damit sie im Bereich Elemente in der Visual Studio Code. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0966f-133">If you choose the **about:blank** option, you must navigate to your web app in the browser for it to appear in the **Elements** panel in Visual Studio Code.</span></span>  

## <a name="launching-microsoft-edge-from-the-debug-view"></a><span data-ttu-id="0966f-134">Starten Microsoft Edge aus der Debugansicht</span><span class="sxs-lookup"><span data-stu-id="0966f-134">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="0966f-135">Wenn Sie die Verwendung der Debugansicht in Visual Studio Code gewohnt sind, greifen Sie Microsoft Edge DevTools darauf zu.</span><span class="sxs-lookup"><span data-stu-id="0966f-135">If you are accustomed to using the Debug view in Visual Studio Code, access Microsoft Edge DevTools from it.</span></span>  

1.  <span data-ttu-id="0966f-136">Navigieren Visual Studio Code zur Debugansicht</span><span class="sxs-lookup"><span data-stu-id="0966f-136">In Visual Studio Code, navigate to the Debug view</span></span> 
    *   <span data-ttu-id="0966f-137">Wählen `Ctrl` + `Shift` + `D` Sie unter Windows/Linux \( `Command` + `Shift` + `D` unter macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-137">Select `Ctrl`+`Shift`+`D` on Windows/Linux  \(`Command`+`Shift`+`D` on macOS\).</span></span>  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  <span data-ttu-id="0966f-138">Wenn sie keine Konfigurationen in Visual Studio Code, führen Sie eine der folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-138">If you do not have any configurations in Visual Studio Code, complete one of the following actions.</span></span>  
>     *   <span data-ttu-id="0966f-139">Wählen Sie `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-139">Select `F5`.</span></span>  
>     *   <span data-ttu-id="0966f-140">Wählen Sie **die Schaltfläche** Wiedergabe \(grün\) aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-140">Choose the **Play** \(green\) button.</span></span>  
> 1.  <span data-ttu-id="0966f-141">Wählen Sie im Dropdownmenü **Edge** aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-141">In the dropdown, choose **Edge** in the dropdown.</span></span>  
> 1.  <span data-ttu-id="0966f-142">Es `launch.json` sollte eine Datei angezeigt werden, die die folgende Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="0966f-142">A `launch.json` file should be displayed that contains the following configuration.</span></span>  
>     
>     ```json
>     {
>       "version": "0.2.0",
>       "configurations": [
>         {
>           "name": "Launch Microsoft Edge and open the Edge DevTools",
>           "request": "launch",
>           "type": "vscode-edge-devtools.debug",
>           "url": "http://localhost:8080"
>         }
>       ]
>     }
>     ```  
>     
> <span data-ttu-id="0966f-143">Führen Sie nach dem Laden der richtigen Konfiguration die folgende Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-143">After you load the correct configuration, complete the following action.</span></span>  

1.  <span data-ttu-id="0966f-144">Führen Sie zum Starten des **Elements-Visual Studio Code** eine der folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-144">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="0966f-145">Wählen Sie `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-145">Select `F5`.</span></span>  
    *   <span data-ttu-id="0966f-146">Wählen Sie **die Schaltfläche** Wiedergabe \(grün\) aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-146">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="0966f-147">Jetzt können Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="0966f-147">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="0966f-148">Greifen Sie auf einen Screencast Ihres Browsers zu.</span><span class="sxs-lookup"><span data-stu-id="0966f-148">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="0966f-149">Überprüfen Sie das DOM und die Formatierung der Komponenten auf Ihrer Seite.</span><span class="sxs-lookup"><span data-stu-id="0966f-149">Inspect the DOM and the styling of the components on your page.</span></span>  

## <a name="attaching-to-microsoft-edge"></a><span data-ttu-id="0966f-150">Anfügen an Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0966f-150">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="0966f-151">Führen Sie die folgenden Schritte aus, um einen Browser zu öffnen und die Instanz Visual Studio Code anfügen.</span><span class="sxs-lookup"><span data-stu-id="0966f-151">To open a browser and attach the instance to Visual Studio Code, complete the following steps.</span></span> 

1.  <span data-ttu-id="0966f-152">Um eine Instanz von Microsoft Edge \(Chromium\) zu öffnen, kopieren Und führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-152">To open an instance of Microsoft Edge \(Chromium\), copy and run the following command.</span></span>  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="0966f-153">Kopieren Sie nach dem Starten der Instanz den folgenden Codeausschnitt, und fügen Sie ihn in Die Datei `launch.json` ein.</span><span class="sxs-lookup"><span data-stu-id="0966f-153">After the instance launches, copy and paste the following code snippet into your `launch.json` file.</span></span>  
    
    ```json
    {
        "type": "vscode-edge-devtools.debug",
        "request": "attach",
        "name": "Attach to Microsoft Edge and open the developer tools",
        "url": "http://localhost:3000/",
        "webRoot": "${workspaceFolder}/out",
        "port": 9222
    }
    ```  
    
1.  <span data-ttu-id="0966f-154">Öffnen Visual Studio Code sie das Dropdownmenü **Debugger,** und wählen Sie An Microsoft Edge anhängen aus, und öffnen Sie **die Entwicklertools**.</span><span class="sxs-lookup"><span data-stu-id="0966f-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span></span>  
1.  <span data-ttu-id="0966f-155">Führen Sie zum Starten des **Elements-Visual Studio Code** eine der folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-155">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="0966f-156">Wählen Sie `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-156">Select `F5`.</span></span>  
    *   <span data-ttu-id="0966f-157">Wählen Sie **die Schaltfläche** Wiedergabe \(grün\) aus.</span><span class="sxs-lookup"><span data-stu-id="0966f-157">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="0966f-158">Jetzt können Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="0966f-158">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="0966f-159">Greifen Sie auf einen Screencast Ihres Browsers zu.</span><span class="sxs-lookup"><span data-stu-id="0966f-159">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="0966f-160">Überprüfen Sie das DOM und die Formatierung der Komponenten auf Ihrer Seite.</span><span class="sxs-lookup"><span data-stu-id="0966f-160">Inspect the DOM and the styling of the components on your page.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-for-visual-studio-code-extension-team"></a><span data-ttu-id="0966f-161">In Kontakt mit dem Microsoft Edge DevTools for Visual Studio Code Extension Team</span><span class="sxs-lookup"><span data-stu-id="0966f-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span></span>  

<span data-ttu-id="0966f-162">Senden Sie Ihr Feedback, [indem Sie ein Problem][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] gegen das GitHub [der][GithubMicrosoftVscodeEdgeDevtools] Erweiterung einreichen.</span><span class="sxs-lookup"><span data-stu-id="0966f-162">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="0966f-163">Wenn Sie helfen möchten,</span><span class="sxs-lookup"><span data-stu-id="0966f-163">If you want to help make</span></span> <!--the Microsoft Edge DevTools for Visual Studio Code --><span data-ttu-id="0966f-164">diese Erweiterung besser, Ihre Beiträge sind willkommen.</span><span class="sxs-lookup"><span data-stu-id="0966f-164">this extension better, your contributions are welcome.</span></span>  <span data-ttu-id="0966f-165">Finden Sie alles, was Sie benötigen, um im GitHub [der][GithubMicrosoftVscodeEdgeDevtools] Erweiterung zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="0966f-165">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Neues Problem – microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code"  

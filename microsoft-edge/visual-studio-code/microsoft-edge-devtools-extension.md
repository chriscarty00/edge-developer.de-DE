---
description: Verwenden von Elementen für Microsoft Edge (Chrom) aus Visual Studio-Code
title: Elemente für Microsoft Edge (Chrom) aus Visual Studio-Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, vs-Code, Visual Studio-Code, Elemente
ms.openlocfilehash: 81488c08a76a16b80a415cbd17cd0617df916f54
ms.sourcegitcommit: 1cfcf2c8970a6c2221cfbf09a23d36b08bd60690
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "11135490"
---
# <span data-ttu-id="7ee21-104">Microsoft Edge-devtools für Visual Studio-Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="7ee21-104">Microsoft Edge DevTools for Visual Studio Code extension</span></span>  

<span data-ttu-id="7ee21-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="7ee21-105">Use</span></span> <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] --><span data-ttu-id="7ee21-106">Diese Erweiterung für den Zugriff auf Microsoft Edge devtools in [Visual Studio-Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="7ee21-106">this extension to access in Microsoft Edge DevTools inside [Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="7ee21-107">Sie haben Zugriff auf die **Elemente** und **Netzwerk** Tools in Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="7ee21-107">You have access to the **Elements** and **Network** tools in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="7ee21-108">Sie können eine Instanz von Microsoft Edge entweder starten oder anfügen.</span><span class="sxs-lookup"><span data-stu-id="7ee21-108">You may either launch or attach to an instance of Microsoft Edge.</span></span>  <span data-ttu-id="7ee21-109">Nachdem Sie eine Verbindung hergestellt haben, können Sie die HTML-Laufzeitstruktur anzeigen, das Layout ändern, Styling-Probleme beheben und den Netzwerkdatenverkehr überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7ee21-109">After you connect you may display the runtime HTML structure, alter the layout, fix styling issues, and inspect network traffic.</span></span>  

## <span data-ttu-id="7ee21-110">Elemente-Tool</span><span class="sxs-lookup"><span data-stu-id="7ee21-110">Elements tool</span></span>  

<span data-ttu-id="7ee21-111">Standardmäßig startet die Erweiterung eine Browserinstanz in einem eindeutigen Fenster und gibt Ihnen **die Funktionen von** Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="7ee21-111">By default, the extension launches a browser instance in a unique window and gives you the **Elements** functionality of Microsoft Edge DevTools.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge-devtools für Visual Studio-Code, der mit einem vollständigen Browserfenster ausgeführt wird" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   <span data-ttu-id="7ee21-113">Microsoft Edge-devtools für Visual Studio-Code, der mit einem vollständigen Browserfenster ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="7ee21-113">Microsoft Edge DevTools for Visual Studio Code running with a full browser window</span></span>  
:::image-end:::  

<span data-ttu-id="7ee21-114">In den Erweiterungseinstellungen können Sie mehr Funktionen wie headless- **Modus** und **Netzwerk**aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7ee21-114">In the extension settings, you may enable more functionality like **Headless Mode** and **Network**.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Aktivieren (oder deaktivieren) des Headless-Modus und Netzwerkprüfung in den Erweiterungseinstellungen" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   <span data-ttu-id="7ee21-116">Aktivieren von \ (oder deaktivieren \) Headless-Modus und Netzwerkprüfung in den Erweiterungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="7ee21-116">Enabling \(or disabling\) headless mode and Network inspection in the extension settings</span></span>  
:::image-end:::  

## <span data-ttu-id="7ee21-117">Headless-Modus</span><span class="sxs-lookup"><span data-stu-id="7ee21-117">Headless Mode</span></span>  

<span data-ttu-id="7ee21-118">Im Headless-Modus wird mit dieser Erweiterung keine vollständige Browserinstanz zum Debuggen gestartet.</span><span class="sxs-lookup"><span data-stu-id="7ee21-118">In headless mode, this extension does not launch a full browser instance to debug.</span></span>  <span data-ttu-id="7ee21-119">Sie führt eine Instanz im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="7ee21-119">It runs an instance in the background.</span></span>  <span data-ttu-id="7ee21-120">Möglicherweise müssen Sie im Editor bleiben und mit dem eingebetteten Browser interagieren.</span><span class="sxs-lookup"><span data-stu-id="7ee21-120">You may have to stay inside the editor and interact with the embedded browser.</span></span>  <span data-ttu-id="7ee21-121">In der Taskleiste wird kein zusätzliches Browser Symbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7ee21-121">An extra browser icon is not be displayed in your task bar.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge-devtools für Visual Studio-Code, der mit einem headless ausgeführt wird" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   <span data-ttu-id="7ee21-123">Microsoft Edge-devtools für Visual Studio-Code, der mit einem headless-Browser ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="7ee21-123">Microsoft Edge DevTools for Visual Studio Code running with a headless browser</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="7ee21-124">Unter macOS sollten Sie den Modus "headless" als bevorzugten Modus aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7ee21-124">On macOS, you should turn on headless mode as your preferred mode.</span></span>  <span data-ttu-id="7ee21-125">Bei Verwendung des Headless-Modus sollte ein Problem gelöst werden, bei dem das Fenster im Browserfenster, wenn es nicht sichtbar ist `Not Active` .</span><span class="sxs-lookup"><span data-stu-id="7ee21-125">Using headless mode should solve an issue where, if the window is not visible, the browser window reports that it is `Not Active`.</span></span>  

## <span data-ttu-id="7ee21-126">Netzwerktool</span><span class="sxs-lookup"><span data-stu-id="7ee21-126">Network tool</span></span>  

<span data-ttu-id="7ee21-127">Wenn Sie auch den Netzwerkdatenverkehr Ihrer Anwendung prüfen möchten, öffnen Sie die Einstellungen, und aktivieren Sie die Registerkarte **Netzwerk** .</span><span class="sxs-lookup"><span data-stu-id="7ee21-127">If you also want to inspect the network traffic of your application, open the settings and turn on the **Network** tab.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Netzwerk Inspektion in Microsoft Edge devtools for Visual Studio-Code" lightbox="./media/edge-devtools-for-vscode-network.png":::
    <span data-ttu-id="7ee21-129">Netzwerk Inspektion in Microsoft Edge devtools for Visual Studio-Code</span><span class="sxs-lookup"><span data-stu-id="7ee21-129">Network inspection in Microsoft Edge DevTools for Visual Studio Code</span></span>  
:::image-end:::  

## <span data-ttu-id="7ee21-130">Starten von Microsoft Edge aus der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="7ee21-130">Launching Microsoft Edge From the extension</span></span>  

<span data-ttu-id="7ee21-131">Navigieren Sie in der **Aktivitäts Leiste**zu Microsoft Edge Tools.</span><span class="sxs-lookup"><span data-stu-id="7ee21-131">Navigate to Microsoft Edge Tools in the **Activity Bar**.</span></span>  <span data-ttu-id="7ee21-132">Neben der Position, an der **Microsoft Edge Tools: Targets steht,** gibt es ein Pluszeichen, mit dem der Browser für Ihre APP geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7ee21-132">Next to where it says **Microsoft Edge Tools: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="7ee21-133">Wenn Sie die Option **about: blank** auswählen, müssen Sie im Browser zu Ihrer Web-App navigieren, damit Sie im Visual Studio-Code im Panel **Elemente** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7ee21-133">If you choose the **about:blank** option, you must navigate to your web app in the browser for it to appear in the **Elements** panel in Visual Studio Code.</span></span>  

## <span data-ttu-id="7ee21-134">Starten von Microsoft Edge aus der Ansicht "Debuggen"</span><span class="sxs-lookup"><span data-stu-id="7ee21-134">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="7ee21-135">Wenn Sie es gewohnt sind, die Debugansicht in Visual Studio-Code zu verwenden, greifen Sie auf Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="7ee21-135">If you are accustomed to using the Debug view in Visual Studio Code, access Microsoft Edge DevTools from it.</span></span>  

1.  <span data-ttu-id="7ee21-136">Navigieren Sie in Visual Studio-Code zur Debug-Ansicht.</span><span class="sxs-lookup"><span data-stu-id="7ee21-136">In Visual Studio Code, navigate to the Debug view</span></span> 
    *   <span data-ttu-id="7ee21-137">Wählen Sie `Ctrl` + `Shift` + `D` unter Windows/Linux \ ( `Command` + `Shift` + `D` unter macOS).</span><span class="sxs-lookup"><span data-stu-id="7ee21-137">Select `Ctrl`+`Shift`+`D` on Windows/Linux  \(`Command`+`Shift`+`D` on macOS\).</span></span>  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  <span data-ttu-id="7ee21-138">Wenn Sie keine Konfigurationen in Visual Studio-Code haben, führen Sie eine der folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="7ee21-138">If you do not have any configurations in Visual Studio Code, complete one of the following actions.</span></span>  
>     *   <span data-ttu-id="7ee21-139">Wählen Sie aus `F5` .</span><span class="sxs-lookup"><span data-stu-id="7ee21-139">Select `F5`.</span></span>  
>     *   <span data-ttu-id="7ee21-140">Wählen Sie die Schaltfläche " **Wiedergabe** \ (grün \)" aus.</span><span class="sxs-lookup"><span data-stu-id="7ee21-140">Choose the **Play** \(green\) button.</span></span>  
> 1.  <span data-ttu-id="7ee21-141">Wählen Sie im Dropdownmenü die Option **Edge** in der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="7ee21-141">In the dropdown, choose **Edge** in the dropdown.</span></span>  
> 1.  <span data-ttu-id="7ee21-142">`launch.json`Es sollte eine Datei mit der folgenden Konfiguration angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7ee21-142">A `launch.json` file should be displayed that contains the following configuration.</span></span>  
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
> <span data-ttu-id="7ee21-143">Nachdem Sie die richtige Konfiguration geladen haben, führen Sie die folgende Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="7ee21-143">After you load the correct configuration, complete the following action.</span></span>  

1.  <span data-ttu-id="7ee21-144">Führen Sie eine der folgenden Aktionen aus, um das **Element** Tool aus Visual Studio-Code zu starten.</span><span class="sxs-lookup"><span data-stu-id="7ee21-144">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="7ee21-145">Wählen Sie aus `F5` .</span><span class="sxs-lookup"><span data-stu-id="7ee21-145">Select `F5`.</span></span>  
    *   <span data-ttu-id="7ee21-146">Wählen Sie die Schaltfläche " **Wiedergabe** \ (grün \)" aus.</span><span class="sxs-lookup"><span data-stu-id="7ee21-146">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="7ee21-147">Nun können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="7ee21-147">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="7ee21-148">Greifen Sie auf einen Screencast Ihres Browsers zu.</span><span class="sxs-lookup"><span data-stu-id="7ee21-148">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="7ee21-149">Überprüfen Sie das DOM und die Formatierung der Komponenten auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="7ee21-149">Inspect the DOM and the styling of the components on your page.</span></span>  

## <span data-ttu-id="7ee21-150">Anfügen an Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7ee21-150">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="7ee21-151">Führen Sie die folgenden Schritte aus, um einen Browser zu öffnen und die Instanz an Visual Studio-Code anzufügen.</span><span class="sxs-lookup"><span data-stu-id="7ee21-151">To open a browser and attach the instance to Visual Studio Code, complete the following steps.</span></span> 

1.  <span data-ttu-id="7ee21-152">Wenn Sie eine Instanz von Microsoft Edge \ (Chrom \) öffnen möchten, kopieren Sie den folgenden Befehl, und führen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7ee21-152">To open an instance of Microsoft Edge \(Chromium\), copy and run the following command.</span></span>  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="7ee21-153">Nachdem die Instanz gestartet wurde, kopieren Sie den folgenden Codeausschnitt in Ihre Datei, und fügen Sie ihn ein `launch.json` .</span><span class="sxs-lookup"><span data-stu-id="7ee21-153">After the instance launches, copy and paste the following code snippet into your `launch.json` file.</span></span>  
    
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
    
1.  <span data-ttu-id="7ee21-154">Öffnen Sie in Visual Studio-Code das Dropdownmenü **Debugger** , und wählen Sie **an Microsoft Edge anfügen aus, und öffnen Sie die Entwicklertools**.</span><span class="sxs-lookup"><span data-stu-id="7ee21-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span></span>  
1.  <span data-ttu-id="7ee21-155">Führen Sie eine der folgenden Aktionen aus, um das **Element** Tool aus Visual Studio-Code zu starten.</span><span class="sxs-lookup"><span data-stu-id="7ee21-155">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="7ee21-156">Wählen Sie aus `F5` .</span><span class="sxs-lookup"><span data-stu-id="7ee21-156">Select `F5`.</span></span>  
    *   <span data-ttu-id="7ee21-157">Wählen Sie die Schaltfläche " **Wiedergabe** \ (grün \)" aus.</span><span class="sxs-lookup"><span data-stu-id="7ee21-157">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="7ee21-158">Nun können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="7ee21-158">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="7ee21-159">Greifen Sie auf einen Screencast Ihres Browsers zu.</span><span class="sxs-lookup"><span data-stu-id="7ee21-159">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="7ee21-160">Überprüfen Sie das DOM und die Formatierung der Komponenten auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="7ee21-160">Inspect the DOM and the styling of the components on your page.</span></span>  
    
## <span data-ttu-id="7ee21-161">Kontaktieren des Microsoft Edge devtools for Visual Studio-Code Erweiterungs Teams</span><span class="sxs-lookup"><span data-stu-id="7ee21-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span></span>  

<span data-ttu-id="7ee21-162">Senden Sie Ihr Feedback, indem Sie [ein Problem][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] mit dem [GitHub-Repo][GithubMicrosoftVscodeEdgeDevtools] der Erweiterung einreichen.</span><span class="sxs-lookup"><span data-stu-id="7ee21-162">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="7ee21-163">Wenn Sie helfen möchten,</span><span class="sxs-lookup"><span data-stu-id="7ee21-163">If you want to help make</span></span> <!--the Microsoft Edge DevTools for Visual Studio Code --><span data-ttu-id="7ee21-164">Diese Erweiterung besser, ihre Beiträge sind willkommen.</span><span class="sxs-lookup"><span data-stu-id="7ee21-164">this extension better, your contributions are welcome.</span></span>  <span data-ttu-id="7ee21-165">Finden Sie alles, was Sie für den Einstieg in das [GitHub-Repo][GithubMicrosoftVscodeEdgeDevtools] der Erweiterung benötigen.</span><span class="sxs-lookup"><span data-stu-id="7ee21-165">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio-Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio-Code"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Neues Problem-Microsoft/vscode-Edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge-Tools für vs-Code"  

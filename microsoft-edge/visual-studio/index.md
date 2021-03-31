---
description: Microsoft Edge (Chromium) und Visual Studio
title: Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, vs, visual studio, debugger
ms.openlocfilehash: 562952ef238c05922e468501706ab75e1976273d
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387275"
---
# <a name="visual-studio"></a><span data-ttu-id="0189e-104">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0189e-104">Visual Studio</span></span>  

<span data-ttu-id="0189e-105">Microsoft [Visual Studio][MicrosoftVisualstudioVs] ist eine integrierte Entwicklungsumgebung \(IDE\).</span><span class="sxs-lookup"><span data-stu-id="0189e-105">Microsoft [Visual Studio][MicrosoftVisualstudioVs] is an integrated development environment \(IDE\).</span></span>   <span data-ttu-id="0189e-106">Verwenden Sie sie, um Ihre Web-Apps zu bearbeiten, zu debuggen, zu erstellen und zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0189e-106">Use it to edit, debug, build, and publish your web apps.</span></span>  <span data-ttu-id="0189e-107">Es handelt sich um ein funktionsreiches Programm, das für viele Aspekte Ihrer Webentwicklung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0189e-107">It is a feature-rich program that may be used for many aspects of your web development.</span></span>  <span data-ttu-id="0189e-108">Neben dem Standard-Editor und Debugger, den die meisten IDEs bereitstellen, enthält Visual Studio die folgenden Features, um Ihren Entwicklungsprozess zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="0189e-108">Over and above the standard editor and debugger that most IDEs provide, Visual Studio includes the following features to ease your development process.</span></span>  

*   <span data-ttu-id="0189e-109">Compiler</span><span class="sxs-lookup"><span data-stu-id="0189e-109">compilers</span></span>  
*   <span data-ttu-id="0189e-110">Codevollständigungstools</span><span class="sxs-lookup"><span data-stu-id="0189e-110">code completion tools</span></span>  
*   <span data-ttu-id="0189e-111">Grafische Designer</span><span class="sxs-lookup"><span data-stu-id="0189e-111">graphical designers</span></span>  
*   <span data-ttu-id="0189e-112">viele weitere</span><span class="sxs-lookup"><span data-stu-id="0189e-112">many more</span></span>  
    
<span data-ttu-id="0189e-113">Wenn Sie die Datei noch nicht Visual Studio, navigieren Sie zu [Download Visual Studio,][MicrosoftVisualstudioDownloads] um sie herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="0189e-113">If you are not already using Visual Studio, navigate to [Download Visual Studio][MicrosoftVisualstudioDownloads] to download it.</span></span>  

<span data-ttu-id="0189e-114">Derzeit unterstützt Visual Studio 2019 das Debuggen von JavaScript in Microsoft Edge für Ihr ASP.NET Framework und ASP.NET Core-Apps.</span><span class="sxs-lookup"><span data-stu-id="0189e-114">Currently, Visual Studio 2019 supports debugging JavaScript in Microsoft Edge for your ASP.NET Framework and ASP.NET Core apps.</span></span>  <span data-ttu-id="0189e-115">Führen Sie die folgenden Schritte aus, um Visual Studio Microsoft Edge zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="0189e-115">Complete the following steps to use Visual Studio to debug Microsoft Edge.</span></span>  

## <a name="launch-microsoft-edge"></a><span data-ttu-id="0189e-116">Starten von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0189e-116">Launch Microsoft Edge</span></span>  

<span data-ttu-id="0189e-117">Visual Studio den folgenden Workflow mithilfe einer einzelnen Schaltfläche ab.</span><span class="sxs-lookup"><span data-stu-id="0189e-117">Visual Studio completes the following workflow using a single button.</span></span>  

1.  <span data-ttu-id="0189e-118">Erstellt Ihre ASP.NET und ASP.NET Core-App.</span><span class="sxs-lookup"><span data-stu-id="0189e-118">Builds your ASP.NET and ASP.NET Core app.</span></span>  
1.  <span data-ttu-id="0189e-119">Startet den Webserver.</span><span class="sxs-lookup"><span data-stu-id="0189e-119">Starts your web server.</span></span>  
1.  <span data-ttu-id="0189e-120">Startet Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0189e-120">Launches Microsoft Edge.</span></span>  
1.  <span data-ttu-id="0189e-121">Verbindet den Visual Studio Debugger.</span><span class="sxs-lookup"><span data-stu-id="0189e-121">Connects the Visual Studio debugger.</span></span>  
    
<span data-ttu-id="0189e-122">Mit dem vereinfachten Workflow können Sie JavaScript debuggen, das in Microsoft Edge direkt über Ihre IDE ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0189e-122">The simplified workflow allows you to debug JavaScript that run in Microsoft Edge directly from your IDE.</span></span>  

### <a name="create-a-new-aspnet-core-web-app"></a><span data-ttu-id="0189e-123">Erstellen einer neuen ASP.NET Core Web App</span><span class="sxs-lookup"><span data-stu-id="0189e-123">Create a new ASP.NET Core web app</span></span>  

<span data-ttu-id="0189e-124">Öffnen Visual Studio 2019, und wählen **Sie Erstellen eines neuen Projekts aus.**</span><span class="sxs-lookup"><span data-stu-id="0189e-124">Open Visual Studio 2019 and choose **Create a new project**.</span></span>  <span data-ttu-id="0189e-125">Wählen Sie auf dem nächsten Bildschirm **ASP.NET Core Web app**Next  >  **aus.**</span><span class="sxs-lookup"><span data-stu-id="0189e-125">On the next screen, choose **ASP.NET Core Web app** > **Next**.</span></span>  

:::image type="complex" source="./media/create-new-project.png" alt-text="Erstellen einer neuen ASP.NET Core Web App" lightbox="./media/create-new-project.png":::
   <span data-ttu-id="0189e-127">Erstellen einer neuen ASP.NET Core Web App</span><span class="sxs-lookup"><span data-stu-id="0189e-127">Create a new ASP.NET Core Web app</span></span>  
:::image-end:::  

<span data-ttu-id="0189e-128">Geben Sie **einen Projektnamen** für Ihr neues Projekt an, und wählen Sie **Erstellen aus.**</span><span class="sxs-lookup"><span data-stu-id="0189e-128">Provide a **Project name** for your new project and choose **Create**.</span></span>  <span data-ttu-id="0189e-129">Wählen Sie für die Zwecke des Beispiels **React.js** als Vorlage aus, und wählen Sie **Erstellen aus.**</span><span class="sxs-lookup"><span data-stu-id="0189e-129">For the purposes of the example, choose **React.js** as the template, and choose **Create**.</span></span>  <span data-ttu-id="0189e-130">Die React.js-Vorlage  gibt an, wie React.js in eine ASP.NET Core-App integriert wird.</span><span class="sxs-lookup"><span data-stu-id="0189e-130">The **React.js** template specifies how to integrate React.js with an ASP.NET Core app.</span></span>  

### <a name="launch-microsoft-edge-from-visual-studio"></a><span data-ttu-id="0189e-131">Starten von Microsoft Edge von Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0189e-131">Launch Microsoft Edge from Visual Studio</span></span>  

<span data-ttu-id="0189e-132">Öffnen Sie nach dem Erstellen Des Projekts `ClientApp/src/components/Counter.js` .</span><span class="sxs-lookup"><span data-stu-id="0189e-132">After you create your project, open `ClientApp/src/components/Counter.js`.</span></span>  <span data-ttu-id="0189e-133">Wenn Sie nun javaScript Visual Studio, wählen Sie das Dropdown neben der grünen Schaltfläche **Play** und **IIS Express aus.**</span><span class="sxs-lookup"><span data-stu-id="0189e-133">Now, to use Visual Studio to debug JavaScript, choose the dropdown next to the green **Play** button and **IIS Express**.</span></span>  

:::image type="complex" source="./media/vs-dropdown.png" alt-text="Das Dropdown neben der grünen Schaltfläche Play und IIS Express" lightbox="./media/vs-dropdown.png":::
   <span data-ttu-id="0189e-135">Das Dropdown neben der grünen **Schaltfläche "Play"** und **"IIS Express"**</span><span class="sxs-lookup"><span data-stu-id="0189e-135">The dropdown next to the green **Play** button and **IIS Express**</span></span>  
:::image-end:::  

<span data-ttu-id="0189e-136">Wählen **Sie Skriptdebubuing**  >  **aktiviert aus.**</span><span class="sxs-lookup"><span data-stu-id="0189e-136">Choose **Script Debugging** > **Enabled**.</span></span>  

:::image type="complex" source="./media/enable-script-debugging.png" alt-text="Aktivieren des Skriptdebudings in Visual Studio" lightbox="./media/enable-script-debugging.png":::
   <span data-ttu-id="0189e-138">Aktivieren des Skriptdebudings in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0189e-138">Turn on script debugging in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="0189e-139">Wählen Sie in derselben Dropdownliste Webbrowser **>** dem Vorschaukanal von Microsoft Edge aus, den Sie Visual Studio starten möchten, z. B. Microsoft Edge Canary, Dev oder Beta.</span><span class="sxs-lookup"><span data-stu-id="0189e-139">In the same dropdown, choose **Web Browser** > the preview channel of Microsoft Edge that you want Visual Studio to launch, such as Microsoft Edge Canary, Dev, or Beta.</span></span>  <span data-ttu-id="0189e-140">Wenn Sie noch keinen der Microsoft Edge-Vorschaukanäle verwenden, navigieren Sie zu [Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload] herunterladen, um einen herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="0189e-140">If you are not already using one of the Microsoft Edge preview channels, navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload] to download one.</span></span>  

:::image type="complex" source="./media/set-web-browser.png" alt-text="Wählen Sie den Vorschaukanal von Microsoft Edge aus, den Visual Studio starten möchten" lightbox="./media/set-web-browser.png":::
   <span data-ttu-id="0189e-142">Wählen Sie den Vorschaukanal von Microsoft Edge aus, den Visual Studio starten möchten</span><span class="sxs-lookup"><span data-stu-id="0189e-142">Choose the preview channel of Microsoft Edge that you want Visual Studio to launch</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="0189e-143">Wenn Sie Microsoft Edge \(EdgeHTML\) auswählen, wird Visual Studio Microsoft Edge \(Chromium\) gestartet.</span><span class="sxs-lookup"><span data-stu-id="0189e-143">If you choose Microsoft Edge \(EdgeHTML\), Visual Studio launches it instead of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="0189e-144">Installieren Sie einen der Vorschaukanäle von [Microsoft Edge,][MicrosoftedgeinsiderDownload] oder stellen Sie sicher, dass die auf Ihrem Computer installierte Version von Microsoft Edge Microsoft Edge \(Chromium\) und nicht Microsoft Edge \(EdgeHTML\) ist.</span><span class="sxs-lookup"><span data-stu-id="0189e-144">[Install the one of the preview channels of Microsoft Edge][MicrosoftedgeinsiderDownload] or ensure that the version of Microsoft Edge installed on your machine is Microsoft Edge \(Chromium\) and not Microsoft Edge \(EdgeHTML\).</span></span>  

<span data-ttu-id="0189e-145">Nachdem Visual Studio richtig konfiguriert ist, wählen Sie die grüne Schaltfläche **Wiedergabe** aus.</span><span class="sxs-lookup"><span data-stu-id="0189e-145">Now that Visual Studio is correctly configured, choose the green **Play** button.</span></span>  <span data-ttu-id="0189e-146">Visual Studio Sie Ihre App, starten Sie den Webserver, starten Sie Microsoft Edge, und navigieren Sie zu oder zu dem Port, der `https://localhost:44362/` in angegeben `launchSettings.json` ist.</span><span class="sxs-lookup"><span data-stu-id="0189e-146">Visual Studio builds your app, start the web server, launch Microsoft Edge, and navigate to `https://localhost:44362/` or whatever port is specified in `launchSettings.json`.</span></span>  

:::image type="complex" source="./media/edge-launch.png" alt-text="Microsoft Edge wird von Visual Studio" lightbox="./media/edge-launch.png":::
   <span data-ttu-id="0189e-148">Microsoft Edge wird von Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0189e-148">Microsoft Edge launches from Visual Studio</span></span>  
:::image-end:::  

### <a name="debug-javascript-running-in-microsoft-edge"></a><span data-ttu-id="0189e-149">Debuggen von JavaScript, das in Microsoft Edge ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="0189e-149">Debug JavaScript running in Microsoft Edge</span></span>  

<span data-ttu-id="0189e-150">Wechseln Sie zurück zu Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0189e-150">Switch back to Visual Studio.</span></span>  <span data-ttu-id="0189e-151">Wählen Sie in die Rinne neben der Linie aus, um einen Haltepunkt für Zeile `Counter.js` 13 zu setzen.</span><span class="sxs-lookup"><span data-stu-id="0189e-151">In `Counter.js`, to set a breakpoint on Line 13, choose the gutter next to the line.</span></span>  

:::image type="complex" source="./media/set-breakpoint.png" alt-text="Wählen Sie die Rinne neben Zeile 13 in Counter.js, um einen Haltepunkt in Visual Studio" lightbox="./media/set-breakpoint.png":::
   <span data-ttu-id="0189e-153">Wählen Sie die Rinne neben Zeile 13 in aus, um einen `Counter.js` Haltepunkt in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0189e-153">Choose the gutter next to Line 13 in `Counter.js` to set a breakpoint in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="0189e-154">Wechseln Sie nun zurück zur Instanz von Microsoft Edge, die Visual Studio wurde.</span><span class="sxs-lookup"><span data-stu-id="0189e-154">Now switch back to the instance of Microsoft Edge that Visual Studio launched.</span></span>  <span data-ttu-id="0189e-155">Wählen Sie **im** NavMenu auf der linken Seite der Webseite den Zähler aus.</span><span class="sxs-lookup"><span data-stu-id="0189e-155">Choose on **Counter** in the NavMenu on the left of the webpage.</span></span>  <span data-ttu-id="0189e-156">Wählen Sie jetzt **Erhöhen aus.**</span><span class="sxs-lookup"><span data-stu-id="0189e-156">Now choose **Increment**.</span></span>  

:::image type="complex" source="./media/edge-counter.png" alt-text="The Counter page in our ASP.NET Core web app" lightbox="./media/edge-counter.png":::
   <span data-ttu-id="0189e-158">The Counter page in our ASP.NET Core web app</span><span class="sxs-lookup"><span data-stu-id="0189e-158">The Counter page in our ASP.NET Core web app</span></span>  
:::image-end:::  

<span data-ttu-id="0189e-159">Der JavaScript-Debugger in Visual Studio den haltepunkt, den Sie in festgelegt `Counter.js` haben.</span><span class="sxs-lookup"><span data-stu-id="0189e-159">The JavaScript debugger in Visual Studio hits the breakpoint you set in `Counter.js`.</span></span>  <span data-ttu-id="0189e-160">Visual Studio die Laufzeit von JavaScript, das in Microsoft Edge ausgeführt wird, an, und Sie können das Skript zeile für Zeile durchschritten.</span><span class="sxs-lookup"><span data-stu-id="0189e-160">Visual Studio now pauses the runtime of the JavaScript running in Microsoft Edge and you may step through the script line-by-line.</span></span>  

:::image type="complex" source="./media/hit-breakpoint.png" alt-text="Visual Studio hält JavaScript an, das in Microsoft Edge ausgeführt wird" lightbox="./media/hit-breakpoint.png":::
   <span data-ttu-id="0189e-162">Visual Studio hält JavaScript an, das in Microsoft Edge ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="0189e-162">Visual Studio pauses JavaScript running in Microsoft Edge</span></span>  
:::image-end:::  

<span data-ttu-id="0189e-163">Das Beispiel war nur eine geringfügige Demonstration der funktionalität, die in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0189e-163">The example was just a minor demonstration of the functionality available in Visual Studio.</span></span>  <span data-ttu-id="0189e-164">Weitere Informationen zu den Funktionen in Visual Studio 2019 finden Sie [in Visual Studio Dokumentation][VisualStudioWindowsIndex].</span><span class="sxs-lookup"><span data-stu-id="0189e-164">For more information about the functionality in Visual Studio 2019, navigate to [Visual Studio documentation][VisualStudioWindowsIndex].</span></span>  

## <a name="attach-to-microsoft-edge"></a><span data-ttu-id="0189e-165">An Microsoft Edge anfügen</span><span class="sxs-lookup"><span data-stu-id="0189e-165">Attach to Microsoft Edge</span></span>  

<span data-ttu-id="0189e-166">Zuvor mussten Sie Microsoft Edge von einem Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0189e-166">Previously, you had to launch Microsoft Edge from Visual Studio.</span></span>  <span data-ttu-id="0189e-167">Jetzt können Sie den Visual Studio an eine bereits ausgeführte Instanz von Microsoft Edge anfügen.</span><span class="sxs-lookup"><span data-stu-id="0189e-167">Now, you are able to attach the Visual Studio debugger to an already running instance of Microsoft Edge.</span></span>  

<span data-ttu-id="0189e-168">Stellen Sie zunächst sicher, dass keine Instanzen von Microsoft Edge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0189e-168">First, ensure that there are no running instances of Microsoft Edge.</span></span>  <span data-ttu-id="0189e-169">Führen Sie nun über die Befehlszeile den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="0189e-169">Now, from your command line, run the following command.</span></span>  

```console
start msedge –remote-debugging-port=9222
```  

<span data-ttu-id="0189e-170">Öffnen Visual Studio sie das Menü **Debuggen,** und wählen Sie An Prozess anfügen **aus,** oder wählen Sie `Ctrl` + `Alt` + `P` aus.</span><span class="sxs-lookup"><span data-stu-id="0189e-170">From Visual Studio, open the **Debug** menu and choose **Attach to Process** or select `Ctrl`+`Alt`+`P`.</span></span>  

:::image type="complex" source="./media/attach-to-process.png" alt-text="Wählen Sie An Prozess anfügen in Visual Studio" lightbox="./media/attach-to-process.png":::
   <span data-ttu-id="0189e-172">Wählen **Sie An Prozess anfügen** in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0189e-172">Choose **Attach to Process** in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="0189e-173">Legen Sie **im Dialogfeld An Prozess** anfügen **den** Verbindungstyp auf **Chrome devtools-Protokollwebsocket (keine Authentifizierung) ein.**</span><span class="sxs-lookup"><span data-stu-id="0189e-173">From the **Attach to Process** dialog, set **Connection type** to **Chrome devtools protocol websocket (no authentication)**.</span></span>  <span data-ttu-id="0189e-174">Geben Sie **im Textfeld Verbinden** des Ziels ein, und wählen Sie `http://localhost:9222/` `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="0189e-174">In the **Connecting target** textbox, type `http://localhost:9222/` and select `Enter`.</span></span>  <span data-ttu-id="0189e-175">Überprüfen Sie die Liste der geöffneten Registerkarten in Microsoft Edge, die im **Dialogfeld An** Prozess anfügen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0189e-175">Review the list of open tabs you have in Microsoft Edge listed out in the **Attach to Process** dialog.</span></span>  

:::image type="complex" source="./media/attach-to-process-dialog.png" alt-text="Konfigurieren des Dialogfelds An Prozess anfügen in Visual Studio" lightbox="./media/attach-to-process-dialog.png":::
   <span data-ttu-id="0189e-177">Konfigurieren des **Dialogfelds An Prozess anfügen** in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0189e-177">Configure the **Attach to Process** dialog in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="0189e-178">Wählen **Sie Select...** > das Kontrollkästchen neben **JavaScript (Microsoft Edge – Chromium) aus.**</span><span class="sxs-lookup"><span data-stu-id="0189e-178">Choose **Select...** > the checkbox next to **JavaScript (Microsoft Edge – Chromium)**.</span></span>  <span data-ttu-id="0189e-179">Um Registerkarten hinzuzufügen, zu neuen Registerkarten zu navigieren und Registerkarten zu schließen und die änderungen anzuzeigen, die im Dialogfeld **An** Prozess anfügen angezeigt werden, wählen Sie die **Schaltfläche Aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="0189e-179">To add tabs, navigate to new tabs, and close tabs and display the changes reflected in the **Attach to Process** dialog, choose the **Refresh** button.</span></span>  <span data-ttu-id="0189e-180">Wählen Sie die Registerkarte aus, die Sie debuggen möchten, und wählen Sie **Anhängen aus.**</span><span class="sxs-lookup"><span data-stu-id="0189e-180">Choose the tab you want to debug and choose **Attach**.</span></span>  

<span data-ttu-id="0189e-181">Der Visual Studio Debugger ist jetzt an Microsoft Edge angefügt.</span><span class="sxs-lookup"><span data-stu-id="0189e-181">The Visual Studio debugger is now attached to Microsoft Edge.</span></span>  <span data-ttu-id="0189e-182">Sie können die Ausführung von JavaScript anhalten, Haltepunkte festlegen und Anweisungen direkt `console.log()` im Fenster Debugausgabe in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0189e-182">You may pause the running of JavaScript, set breakpoints, and review `console.log()` statements directly in the Debug Output window in Visual Studio.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-visual-studio-team"></a><span data-ttu-id="0189e-183">Kontakt mit dem Microsoft Visual Studio Team</span><span class="sxs-lookup"><span data-stu-id="0189e-183">Getting in touch with the Microsoft Visual Studio team</span></span>  

<span data-ttu-id="0189e-184">Die Microsoft Visual Studio- und Microsoft Edge-Teams möchten mehr darüber erfahren, wie Sie mit JavaScript in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0189e-184">The Microsoft Visual Studio and Microsoft Edge teams wants to learn more about how you work with JavaScript in Visual Studio.</span></span>  <span data-ttu-id="0189e-185">Um Ihr Feedback zu senden, wählen Sie das **Symbol** Feedback senden in Visual Studio oder tweet @VisualStudio [und @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].</span><span class="sxs-lookup"><span data-stu-id="0189e-185">To send your feedback, choose the **Send Feedback** icon in Visual Studio or tweet [@VisualStudio and @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].</span></span>  

:::image type="complex" source="./media/feedback-icon.png" alt-text="Das Symbol Feedback senden in Visual Studio" lightbox="./media/feedback-icon.png":::
   <span data-ttu-id="0189e-187">Das **Symbol Feedback** senden in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0189e-187">The **Send Feedback** icon in Visual Studio</span></span>  
:::image-end:::  

<!-- links -->  

[VisualStudioWindowsIndex]: /visualstudio/windows/index "Visual Studio Dokumentation | Microsoft Docs"  

[MicrosoftVisualstudioDownloads]: https://visualstudio.microsoft.com/downloads "Download Visual Studio"  
[MicrosoftVisualstudioVs]: https://visualstudio.microsoft.com/vs "Visual Studio IDE"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[TwitterIntentTweetViualstudioEdgdevtools]: https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools "Tweet zu @VisualStudio und @EdgeDevTools | Twitter"  

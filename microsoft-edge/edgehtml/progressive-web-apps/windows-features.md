---
description: Progressives verbessern ihrer PWA für Windows mit nativen App-Features
title: Anpassen der PWA-EdgeHTML für Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Progressive Web-Apps, PWA, Edge, Windows, WinRT, UWP, EdgeHTML
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 59612d8292d4c4d4d7073b843386364d1ac55c5d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233990"
---
# <span data-ttu-id="c4ced-104">Anpassen der PWA-EdgeHTML für Windows</span><span class="sxs-lookup"><span data-stu-id="c4ced-104">Tailor your PWA (EdgeHTML) for Windows</span></span>  

<span data-ttu-id="c4ced-105">PWAs, die unter Windows 10 installiert sind, [nutzen alle Vorteile][PwaIndexWindows10] der Ausführung als [universelle Windows-Plattform \ (UWP \)][WindowsUWPGetStartedGuide] -apps, einschließlich Schutz durch die Sicherheit der Windows-App-Sandbox und Vollzugriff auf die [Windows-Runtime \ (WinRT \))][UwpApiIndex] -APIs, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="c4ced-105">PWAs installed on Windows 10 enjoy [all the benefits][PwaIndexWindows10] of running as [Universal Windows Platform \(UWP\)][WindowsUWPGetStartedGuide] apps, including protection through Windows app sandboxing security and full access to [Windows Runtime \(WinRT\))][UwpApiIndex] APIs, including those for:</span></span>  

*   <span data-ttu-id="c4ced-106">Steuern von Gerätefunktionen \ (wie Kamera, Mikrofon, GPS \)</span><span class="sxs-lookup"><span data-stu-id="c4ced-106">Controlling device features \(such as camera, microphone, GPS\)</span></span>  
*   <span data-ttu-id="c4ced-107">Zugriff auf Benutzer Ressourcen \ (wie Kalender, Kontakte, Dokumente, Musik \)</span><span class="sxs-lookup"><span data-stu-id="c4ced-107">Accessing user resources \(such as calendar, contacts, documents, music\)</span></span>  
*   <span data-ttu-id="c4ced-108">Starten/Navigieren in ihrer App mithilfe von Cortana-Sprachbefehlen</span><span class="sxs-lookup"><span data-stu-id="c4ced-108">Launching / navigating your app through Cortana voice commands</span></span>  
*   <span data-ttu-id="c4ced-109">Integration in das Windows-Betriebssystem \ (über das Windows-Aktions Center, die Desktop-Taskleiste und Kontextmenüs \)</span><span class="sxs-lookup"><span data-stu-id="c4ced-109">Integrating with the Windows OS \(through the Windows Action Center, desktop taskbar, and context menus\)</span></span>  
    
<span data-ttu-id="c4ced-110">Dies sind nur einige der zusätzlichen Möglichkeiten für Ihre PWA \ (EdgeHTML \) unter Windows.</span><span class="sxs-lookup"><span data-stu-id="c4ced-110">These are only a few of the added possibilities for your PWA \(EdgeHTML\) on Windows.</span></span>  

<span data-ttu-id="c4ced-111">In diesem Artikel wird gezeigt, wie Sie Ihre PWA \ (EdgeHTML \) als Windows 10-App installieren, ausführen und verbessern, während Sie dennoch die browserübergreifende und plattformübergreifende Kompatibilität sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-111">This article shows you how to install, run, and enhance your PWA \(EdgeHTML\) as a Windows 10 app, while still ensuring cross-browser and cross-platform compatibility.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="c4ced-112">Die Beispiele und Schritte in diesem Artikel erfordern Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="c4ced-112">The examples and steps in this article require Visual Studio 2017.</span></span> <span data-ttu-id="c4ced-113">Die in diesem Artikel verwendete Vorlage wird in Visual Studio 2019 nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="c4ced-113">Visual Studio 2019 does not include the template used in this article.</span></span> <span data-ttu-id="c4ced-114">Informationen zum Herunterladen von Visual Studio 2017 finden Sie unter [Visual Studio-Downloads-2017, 2015 & vorherigen Versionen][PreviousVSDownloads] .</span><span class="sxs-lookup"><span data-stu-id="c4ced-114">To download Visual Studio 2017, see [Visual Studio Downloads - 2017, 2015 & Previous Versions][PreviousVSDownloads]</span></span>  


## <span data-ttu-id="c4ced-115">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c4ced-115">Prerequisites</span></span>  

*   <span data-ttu-id="c4ced-116">Eine vorhandene PWA \ (oder gehostete Web-App \), entweder eine Live-oder eine localhost-Website.</span><span class="sxs-lookup"><span data-stu-id="c4ced-116">An existing PWA \(or hosted web app\), either a live or localhost site.</span></span>  <span data-ttu-id="c4ced-117">In diesem Leitfaden wird das Beispiel PWA aus [Erste Schritte mit progressiven Web-Apps][PwaGetStarted]verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4ced-117">This guide uses the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted].</span></span>  
*   <span data-ttu-id="c4ced-118">Laden Sie die \ (Free \) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].</span><span class="sxs-lookup"><span data-stu-id="c4ced-118">Download the \(free\) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].</span></span>  <span data-ttu-id="c4ced-119">Sie können auch die Editionen Professional, Enterprise oder [Preview][MicrosoftVisualStudioPreview] verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4ced-119">You are also able to use the Professional, Enterprise, or [Preview][MicrosoftVisualStudioPreview] editions.</span></span>  <span data-ttu-id="c4ced-120">Wählen Sie im Visual Studio-Installationsprogramm die folgenden Arbeitsauslastungen aus:</span><span class="sxs-lookup"><span data-stu-id="c4ced-120">From the Visual Studio Installer, choose the following Workloads:</span></span>  
    *   **<span data-ttu-id="c4ced-121">Entwicklung der universellen Windows-Plattform</span><span class="sxs-lookup"><span data-stu-id="c4ced-121">Universal Windows Platform development</span></span>**  
        
## <span data-ttu-id="c4ced-122">Einrichten und Ausführen der universellen Windows-App</span><span class="sxs-lookup"><span data-stu-id="c4ced-122">Set up and run your Universal Windows app</span></span>  

<span data-ttu-id="c4ced-123">Eine PWA \ (EdgeHTML \), die als Windows 10-App installiert ist, wird unabhängig vom Browser in einem eigenständigen \ ( `WWAHost.exe` Prozess \)-Fenster ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4ced-123">A PWA \(EdgeHTML\) installed as a Windows 10 app runs independently from the browser, in a standalone \(`WWAHost.exe` process\) window.</span></span>  <span data-ttu-id="c4ced-124">Für die Aktivierung wird einfach ein einfacher app-Wrapper benötigt, der Ihre gehostete Web-App enthält, die Sie mit der Visual Studio-Projektvorlage schnell einrichten können `Progressive Web App (Universal Windows)` .</span><span class="sxs-lookup"><span data-stu-id="c4ced-124">Enabling this simply requires a lightweight app wrapper that contains your hosted web app, which you are able to quickly set up using the Visual Studio `Progressive Web App (Universal Windows)` project template.</span></span>  <span data-ttu-id="c4ced-125">\ (Alle Ihre APP-Logik, einschließlich des Sendens von systemeigenen Windows-Runtime-API-Anforderungen, erfolgt weiterhin in Ihrem ursprünglichen Web App-Code. \)</span><span class="sxs-lookup"><span data-stu-id="c4ced-125">\(All your app logic, including sending native Windows Runtime API requests, still happens in your original web app code.\)</span></span>  

<span data-ttu-id="c4ced-126">Richten Sie Ihre Entwicklungsumgebung für die Windows-app in Visual Studio ein.</span><span class="sxs-lookup"><span data-stu-id="c4ced-126">Set up your Windows app development environment in Visual Studio.</span></span>  

1.  <span data-ttu-id="c4ced-127">Aktivieren Sie in den Windows-Einstellungen den [Entwicklermodus][WindowsUWPGetStartedEnable].</span><span class="sxs-lookup"><span data-stu-id="c4ced-127">In your Windows Settings, turn on [Developer mode][WindowsUWPGetStartedEnable].</span></span>  <span data-ttu-id="c4ced-128">\ (Geben `developer mode` Sie die Windows-Suchfunktion ein, um Sie zu finden. \)</span><span class="sxs-lookup"><span data-stu-id="c4ced-128">\(Type `developer mode` in the Windows searchbar to find it.\)</span></span>  
1.  <span data-ttu-id="c4ced-129">Starten Sie Visual Studio, und wählen Sie **Neues Projekt erstellen...** aus.</span><span class="sxs-lookup"><span data-stu-id="c4ced-129">Launch Visual Studio and select **Create a new project...**.</span></span>  
1.  <span data-ttu-id="c4ced-130">Wählen Sie **JavaScript**  >  **Windows Universal** aus, und wählen Sie **Progressive Web App (universelle Windows)** aus der Liste der Projekttypen in Visual Studio 2017 aus.</span><span class="sxs-lookup"><span data-stu-id="c4ced-130">Choose **Javascript** > **Windows Universal** and select **Progressive Web App (Universal Windows)** from the list of project types in Visual Studio 2017.</span></span>  
1.  <span data-ttu-id="c4ced-131">Wählen Sie die standardmäßige Windows 10 `Target version` \ (neueste Version) und `Minimum version` \ (Build 10586 oder höher \) aus, und wählen Sie **OK**aus.</span><span class="sxs-lookup"><span data-stu-id="c4ced-131">Select the default Windows 10 `Target version` \(most recent release\) and `Minimum version` \(build 10586 or higher\) and choose **OK**.</span></span>  
    
    ![Visual Studio-Auswahldialogfeld für UWP-Projektziel-Builds](media/vs-target-min-version.png)  
    
    <span data-ttu-id="c4ced-133">Das neue Projekt wird geladen, wenn der Paket-appxmanifest-Designer geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="c4ced-133">Your new project loads with the package.appxmanifest designer open.</span></span>  <span data-ttu-id="c4ced-134">Hier konfigurieren Sie die Details Ihrer APP, einschließlich Paketidentität, Paketabhängigkeiten, erforderliche Funktionen, visuelle Elemente und Erweiterbarkeitspunkte.</span><span class="sxs-lookup"><span data-stu-id="c4ced-134">This is where you configure the details of your app, including package identity, package dependencies, required capabilities, visual elements, and extensibility points.</span></span>  <span data-ttu-id="c4ced-135">Hierbei handelt es sich um eine leicht konfigurierbare, temporäre Version des App-paketmanifests, das während der APP-Entwicklung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4ced-135">This is an easily configurable, temporary version of the app package manifest used during app development.</span></span>  
    <span data-ttu-id="c4ced-136">Wenn Sie Ihr App-Projekt erstellen, [generiert Visual Studio eine AppxManifest.xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] -Datei aus diesen Metadaten, die zum Installieren und Ausführen der APP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4ced-136">When you build your app project, [Visual Studio generates an AppxManifest.xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] file from this metadata, which is used to install and run your app.</span></span>  <span data-ttu-id="c4ced-137">Wenn Sie Ihre Datei aktualisieren, müssen Sie `package.appxmanifest` das Projekt neu erstellen, damit beide in ihrer zur Laufzeit wiedergegeben werden `AppxManifest.xml` .</span><span class="sxs-lookup"><span data-stu-id="c4ced-137">Whenever you update your `package.appxmanifest` file, be sure to rebuild the project so both are reflected in your `AppxManifest.xml` at runtime.</span></span>  
    
1.  <span data-ttu-id="c4ced-138">Geben Sie im Manifest-Designer- **Anwendungs** Bereich die URL ihrer PWA als `Start page` .</span><span class="sxs-lookup"><span data-stu-id="c4ced-138">In the manifest designer **Application** panel, enter the URL of your PWA as the `Start page`.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c4ced-139">Dienstmitarbeiter werden für alle HTTPS \ (Secure, Remote \)-URLs unterstützt, die als `StartPage` .</span><span class="sxs-lookup"><span data-stu-id="c4ced-139">Service workers are supported for all https \(secure, remote\) urls specified as the `StartPage`.</span></span>  <span data-ttu-id="c4ced-140">Dienstmitarbeiter werden standardmäßig nicht für Webanwendungen unterstützt, die eine lokale Startseite angeben.</span><span class="sxs-lookup"><span data-stu-id="c4ced-140">Service workers are not supported by default for web apps that specify a local start page.</span></span>  <span data-ttu-id="c4ced-141">Um die Unterstützung der Dienstmitarbeiter für diese Fälle zu aktivieren, fügen Sie dem Manifest einen expliziten [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) -Eintrag hinzu, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="c4ced-141">To enable service worker support for these cases, add an explicit [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) entry to the manifest, for example:</span></span> `<uap:Rule Match="http://web-platform.test/" Type="include" uap5:ServiceWorker="true"/>`  
    
    ![Anwendungsbereich des Pakets. appxmanifest-Designer](media/vs-manifest-application.png)  
    
    <span data-ttu-id="c4ced-143">Sie können auch das `Display name` und `Description` nach Belieben ändern.</span><span class="sxs-lookup"><span data-stu-id="c4ced-143">You are able to also modify the `Display name` and `Description` as you like.</span></span>  
1.  <span data-ttu-id="c4ced-144">Speichern Sie diese Datei \ (oder ein anderes 512x512-Bild Ihrer Wahl) auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="c4ced-144">Save this file \(or another 512x512 image of your choosing\) to your desktop.</span></span>  
    <span data-ttu-id="c4ced-145">Klicken Sie dann im Manifest-Designer **Visual Assets** Panel auf die `Source` Schaltfläche Feld **...** , wählen Sie Sie als Quelldatei aus, und klicken Sie auf **generieren**.</span><span class="sxs-lookup"><span data-stu-id="c4ced-145">Then, in the manifest designer **Visual Assets** panel, click on the `Source` field **...** button, select it as your source file, and click **Generate**.</span></span>  <span data-ttu-id="c4ced-146">\ (Klicken Sie dann auf **OK** , um die Standardplatzhalter-Bilder zu überschreiben \).</span><span class="sxs-lookup"><span data-stu-id="c4ced-146">\(Then click **OK** to overwrite the default placeholder images\).</span></span>  
    
    ![Bereich "visuelle Objekte" des Pakets. appxmanifest-Designer](media/vs-manifest-visual-assets.png)  
    
    <span data-ttu-id="c4ced-148">Dadurch werden die grundlegenden visuellen Ressourcen zum Installieren, ausführen, starten und Verteilen Ihrer APP im Store generiert.</span><span class="sxs-lookup"><span data-stu-id="c4ced-148">This generates the basic visual assets for installing, running, launching, and distributing your app in the store.</span></span>  
    <span data-ttu-id="c4ced-149">Wenn rote `X` Fehlermeldungen angezeigt werden, die auf fehlende Bilder hindeuten, können Sie auf die Schaltfläche.. **.** klicken, um eine Datei aus den generierten Bildern manuell auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-149">If you see any red \(`X`\) errors indicating missing images, you are able to click on the **...** buttons to manually select a file from the generated images.</span></span>  
1.  <span data-ttu-id="c4ced-150">Ersetzen Sie im Bereich Manifest-Designer- **Inhalts-URIs** `http://example.com` durch den Speicherort Ihrer PWA \ (so `Rule`  =  `include` und `WinRT Access`  =  `All` \).</span><span class="sxs-lookup"><span data-stu-id="c4ced-150">In the manifest designer **Content URIs** panel, replace `http://example.com` with the location of your PWA \(such that `Rule` = `include` and `WinRT Access` = `All`\).</span></span>  
    <span data-ttu-id="c4ced-151">Dadurch wird Ihre PWA-Berechtigung zum Senden systemeigener Windows-Runtime \ (WinRT \)-API-Anforderungen gewährt, wenn Sie als Windows 10-app ausgeführt wird, die ein wenig später abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="c4ced-151">This grants your PWA permission to send native Windows Runtime \(WinRT\) API requests when running as a Windows 10 app, which is covered a bit later.</span></span>   <span data-ttu-id="c4ced-152">Wenn für ihre eigentliche PWA kein WinRT-Zugriff erforderlich ist, können Sie den `WinRT Access` Wert auf ändern `None` .</span><span class="sxs-lookup"><span data-stu-id="c4ced-152">If your actual PWA does not require WinRT access, you are able to switch the `WinRT Access` value to `None`.</span></span>  <span data-ttu-id="c4ced-153">Achten Sie auf jeden Fall darauf, die Standard `http://example.com` Zeichenfolge mit dem URI ihrer PWA zu unterteilen, oder die APP kann zur Laufzeit nicht ordnungsgemäß geladen werden.</span><span class="sxs-lookup"><span data-stu-id="c4ced-153">Either way, be sure to sub out the default `http://example.com` string with the URI of your PWA, or your app is not able to properly load at runtime.</span></span>  
    <span data-ttu-id="c4ced-154">Sie können Ihre PWA als Windows 10-app ausführen und Debuggen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-154">You are ready to run and debug your PWA as a Windows 10 app.</span></span>  <span data-ttu-id="c4ced-155">Wenn Sie eine localhost-Website verwenden, um diesen Leitfaden zu durchlaufen, stellen Sie sicher, dass Sie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4ced-155">If you are using a localhost site to step through this guide, make sure it is running.</span></span>  <span data-ttu-id="c4ced-156">Dann</span><span class="sxs-lookup"><span data-stu-id="c4ced-156">Then,</span></span>  
1.  <span data-ttu-id="c4ced-157">Erstellen Sie \ ( `Ctrl` + `Shift` + `F5` \), und führen `F5` Sie das PWA-Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="c4ced-157">Build \(`Ctrl`+`Shift`+`F5`\) and Run \(`F5`\) your PWA project.</span></span>  <span data-ttu-id="c4ced-158">Ihre Website sollte nun in einem eigenständigen App-Fenster gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="c4ced-158">Your website should now launch in a standalone app window.</span></span>  <span data-ttu-id="c4ced-159">Es handelt sich nicht nur um eine gehostete Web-App; Sie wird als Progressive Web-App auf Windows 10 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4ced-159">Not only is it a hosted web app; it is running as a Progressive Web App installed on Windows 10!</span></span>  
    
    ![PWA wird in einem WWAHost.exe Fenster ausgeführt](media/wwahost.png)  
    
## <span data-ttu-id="c4ced-161">Debuggen Ihrer PWA \ (EdgeHTML \) als Windows-App</span><span class="sxs-lookup"><span data-stu-id="c4ced-161">Debug your PWA \(EdgeHTML\) as a Windows app</span></span>  

<span data-ttu-id="c4ced-162">Da es sich bei einer PWA \ (EdgeHTML \) einfach um eine progressiv erweiterte gehostete Web-App handelt, können Sie Ihren serverseitigen Code wie jede andere Web-App mit der üblichen IDE und dem normalen Workflow Debuggen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-162">Because a PWA \(EdgeHTML\) is simply a progressively enhanced hosted web app, you are able to debug your server-side code the same as any web app, using your usual IDE and workflow.</span></span>  <span data-ttu-id="c4ced-163">Die von Ihnen bereitgestellten Änderungen werden in Ihrer installierten PWA-Version wiedergegeben, wenn Sie Sie das nächste Mal starten \ (Sie müssen das universelle Windows-App-Paket nicht erneut bereitstellen).</span><span class="sxs-lookup"><span data-stu-id="c4ced-163">The changes you deploy live are reflected in your installed PWA the next time you launch it \(no need to redeploy your Universal Windows app package\).</span></span>

<span data-ttu-id="c4ced-164">Für das clientseitige Debuggen in Ihrer Windows 10-App müssen Sie über die `Microsoft Edge DevTools Preview` App verfügen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-164">For client-side debugging within your Windows 10 app, you must have the `Microsoft Edge DevTools Preview` app.</span></span>  <span data-ttu-id="c4ced-165">Diese eigenständige App umfasst die gesamte Funktionalität des ursprünglichen in-Browser- [Microsoft Edge-devtools][DevToolsGuide] \ (einschließlich [PWA-Tools][DevToolsGuideServiceWorkers]\) sowie die grundlegende Unterstützung für [Remotedebuggen][DevToolsProtocol01ClientsEdgePreview] sowie eine [Debug-Zielauswahl][DevToolsGuideMicrosoftStoreApp] zum Anfügen an eine beliebige ausgeführte Instanz des EdgeHTML-Moduls, einschließlich Add-Ins für Office, Cortana, App-Webansichten und natürlich PWAs, die unter Windows ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c4ced-165">This standalone app includes all the functionality of the original in-browser [Microsoft Edge DevTools][DevToolsGuide] \(including [PWA tools][DevToolsGuideServiceWorkers]\), plus basic [remote debugging][DevToolsProtocol01ClientsEdgePreview] support and a [Debug Target chooser][DevToolsGuideMicrosoftStoreApp] for attaching to any running instance of the EdgeHTML engine, including add-ins for Office, Cortana, app webviews, and of course, PWAs running on Windows.</span></span>  

<span data-ttu-id="c4ced-166">Hier erfahren Sie, wie Sie das Debuggen für Ihre PWA \ (EdgeHTML \) einrichten.</span><span class="sxs-lookup"><span data-stu-id="c4ced-166">Here is how to set up debugging for your PWA \(EdgeHTML\).</span></span>  

1.  <span data-ttu-id="c4ced-167">Installieren Sie die [Microsoft Edge devtools Preview][MicrosoftStoreEdgeDevtoolsPreview] -App aus dem Microsoft Store, wenn Sie Sie nicht bereits haben.</span><span class="sxs-lookup"><span data-stu-id="c4ced-167">Install the [Microsoft Edge DevTools Preview][MicrosoftStoreEdgeDevtoolsPreview] app from the Microsoft Store if you do not already have it.</span></span>  
1.  <span data-ttu-id="c4ced-168">Starten Sie die devtools-APP, während ihre PWA-Website ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4ced-168">With your PWA site up and running, launch the DevTools app.</span></span>  
1.  <span data-ttu-id="c4ced-169">Starten Sie in Visual Studio Ihre Windows 10-App mit `Start Without Debugging` dem `Ctrl` + `F5` Befehl ().</span><span class="sxs-lookup"><span data-stu-id="c4ced-169">From Visual Studio, launch your Windows 10 app with the `Start Without Debugging` (`Ctrl`+`F5`) command.</span></span>  <span data-ttu-id="c4ced-170">\ (Die devtools-APP wird nicht ordnungsgemäß angefügt, wenn der Visual Studio-Debugger aktiv ist. \)</span><span class="sxs-lookup"><span data-stu-id="c4ced-170">\(The DevTools app does not attach properly if the Visual Studio debugger is active.\)</span></span>  
1.  <span data-ttu-id="c4ced-171">Klicken Sie in der devtools-app in der lokalen Debug-Zielauswahl auf die Schaltfläche **Aktualisieren** .</span><span class="sxs-lookup"><span data-stu-id="c4ced-171">In the DevTools app, click the **Refresh** button in the Local debug target chooser.</span></span>  <span data-ttu-id="c4ced-172">Ihre PWA \ (EdgeHTML \)-Website sollte nun aufgelistet sein.</span><span class="sxs-lookup"><span data-stu-id="c4ced-172">Your PWA \(EdgeHTML\) site should now be listed.</span></span>  <span data-ttu-id="c4ced-173">\ (Wenn Sie auch in einem Browserfenster ausgeführt wird, handelt es sich um die letzte Instanz dieser Website in der Liste. \)</span><span class="sxs-lookup"><span data-stu-id="c4ced-173">\(If it is also running in a browser window, it is the last instance of that site in the list.\)</span></span>  
1.  <span data-ttu-id="c4ced-174">Klicken Sie auf Ihren PWA \ (EdgeHTML \)-Website Eintrag, um eine neue Registerkarte für devtools-Instanzen zu öffnen und das Debuggen zu starten.</span><span class="sxs-lookup"><span data-stu-id="c4ced-174">Click on your PWA \(EdgeHTML\) site listing to open a new DevTools instance tab and start debugging.</span></span>  
    
    ![Lokale Debug-Zielauswahl in der Microsoft Edge devtools-App](media/devtools-local.png)  
    
1.  <span data-ttu-id="c4ced-176">Sie können überprüfen, ob devtools an Ihre PWA-running-as-Windows-App angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="c4ced-176">You are able to verify that DevTools is attached to your PWA-running-as-Windows-app.</span></span>  <span data-ttu-id="c4ced-177">Geben Sie in der devtools- **Konsole**Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="c4ced-177">In the DevTools **Console**, type:</span></span>  
    
    ```shell
    window.Windows
    ```  
    
    <span data-ttu-id="c4ced-178">Dadurch wird das globale `Windows Runtime` Objekt zurückgegeben, das alle [WinRT-Namespaces der obersten Ebene](#find-windows-runtime-winrt-apis)enthält.</span><span class="sxs-lookup"><span data-stu-id="c4ced-178">This returns the global `Windows Runtime` object containing all of the [top-level WinRT namespaces](#find-windows-runtime-winrt-apis).</span></span>  <span data-ttu-id="c4ced-179">Hierbei handelt es sich um Ihren PWA \ (EdgeHTML \)-Einstiegsbereich für die [universelle Windows-Plattform][WindowsUWPIndex], der nur für Web-Apps verfügbar gemacht wird, die als Windows 10-apps ausgeführt werden (die außerhalb des Browsers ausgeführt werden, in einem `WWAHost.exe` Prozess).</span><span class="sxs-lookup"><span data-stu-id="c4ced-179">This is your PWA \(EdgeHTML\) entrypoint to the [Universal Windows Platform][WindowsUWPIndex], and only exposed to web apps that run as Windows 10 apps (running outside the browser, in a `WWAHost.exe` process).</span></span>  
    
## <span data-ttu-id="c4ced-180">Suchen von Windows-Runtime-APIs (WinRT)</span><span class="sxs-lookup"><span data-stu-id="c4ced-180">Find Windows Runtime (WinRT) APIs</span></span>  

<span data-ttu-id="c4ced-181">Als installierte Windows-App verfügt Ihre [PWA \ (EdgeHTML \) über vollen Zugriff auf systemeigene Windows-Runtime-APIs][WindowsRuntime]. Ermitteln Sie, was Sie verwenden müssen, rufen Sie die erforderlichen Berechtigungen ab, und verwenden Sie die Feature-Erkennung, um diese API-Anforderung in unterstützten Umgebungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="c4ced-181">As an installed Windows app, your [PWA \(EdgeHTML\) has full access to native Windows Runtime APIs][WindowsRuntime]; identify what you need to use, obtain the requisite permissions, and employ feature detection to send that API request on supported environments.</span></span>  <span data-ttu-id="c4ced-182">Gehen Sie durch diesen Vorgang, um eine progressive Verbesserung für Windows-Desktopbenutzer ihrer PWA hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-182">Walk through this process to add a progressive enhancement for Windows desktop users of your PWA.</span></span>  

<span data-ttu-id="c4ced-183">Es gibt eine Reihe von Möglichkeiten, die universellen Windows-Plattform-APIs zu identifizieren, die Sie für Ihre Windows-PWA benötigen, einschließlich Durchsuchen der umfassenden [UWP-Dokumente auf Windows dev Center] [UWP/API/], herunterladen und Ausführen von [UWP-Codebeispielen](#uwp-code-samples) in Visual Studio und Durchsuchen von Codeausschnitten für allgemeine Aufgaben für PWAs unter Windows.</span><span class="sxs-lookup"><span data-stu-id="c4ced-183">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for PWAs on Windows.</span></span>

<span data-ttu-id="c4ced-184">Es gibt eine Reihe von Möglichkeiten, die für Ihre Windows-PWA benötigten APIs für die universelle Windows-Plattform zu identifizieren, einschließlich Durchsuchen der umfassenden [UWP-Dokumente auf Windows dev Center] [UWP/API/], herunterladen und Ausführen von [UWP-Codebeispielen](#uwp-code-samples) in Visual Studio und Durchsuchen von Codeausschnitten für allgemeine Aufgaben für [PWAs unter Windows 10 (EdgeHTML)][PwaIndexWindows10].</span><span class="sxs-lookup"><span data-stu-id="c4ced-184">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for [PWAs on Windows 10 (EdgeHTML)][PwaIndexWindows10].</span></span>  

<span data-ttu-id="c4ced-185">Insgesamt arbeiten WinRT-APIs in JavaScript auf die gleiche Weise wie in C#, daher können Sie die allgemeine [Dokumentation zur universellen Windows-Plattform][WindowsUWPIndex] und die [API-Referenz][UwpApiIndex] für die Verwendung befolgen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-185">Overall, WinRT APIs work in JavaScript the same way they do in C#, so you may follow the general [Universal Windows Platform documentation][WindowsUWPIndex] and [API Reference][UwpApiIndex] for usage.</span></span>  <span data-ttu-id="c4ced-186">Beachten Sie jedoch die folgenden Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="c4ced-186">However, please note the following differences:</span></span>  

*   <span data-ttu-id="c4ced-187">WinRT-Features in JavaScript verwenden [unterschiedliche Konventionen][ScriptingJsinrtUsingWinRTCasingConventions] für die Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="c4ced-187">WinRT features in JavaScript use  [different casing conventions][ScriptingJsinrtUsingWinRTCasingConventions]</span></span>  
*   <span data-ttu-id="c4ced-188">[Ereignisse werden als Zeichenfolgenbezeichner dargestellt][ScriptingJsinrtHandlingWinRTEvents] , die an Klassen `addEventListener` / `removeEventListener` Methoden übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4ced-188">[Events are represented as string identifiers][ScriptingJsinrtHandlingWinRTEvents] passed to class `addEventListener`/`removeEventListener` methods</span></span>  
*   <span data-ttu-id="c4ced-189">[Asynchrone Methoden][ScriptingJsinrtUsingWinRT] verwenden das JavaScript-Promise-Modell</span><span class="sxs-lookup"><span data-stu-id="c4ced-189">[Asynchronous methods][ScriptingJsinrtUsingWinRT] use the JavaScript Promise model</span></span>  
*   <span data-ttu-id="c4ced-190">APIs im `Windows.UI.Xaml` Namespace werden für JavaScript-apps nicht unterstützt, die stattdessen den [EdgeHTML][DevGuideWhatsNew] Engine Web Rendering Stack \ (HTML, CSS \) verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4ced-190">APIs in the `Windows.UI.Xaml` namespace are not supported for JavaScript apps, which instead use the [EdgeHTML][DevGuideWhatsNew] engine web rendering stack \(HTML, CSS\)</span></span>  
    
<span data-ttu-id="c4ced-191">Weitere Informationen finden Sie unter [Verwenden der Windows-Runtime in JavaScript][WindowRuntimeUsingJavascript].</span><span class="sxs-lookup"><span data-stu-id="c4ced-191">For more details, see [Using the Windows Runtime in JavaScript][WindowRuntimeUsingJavascript].</span></span>  

### <span data-ttu-id="c4ced-192">UWP-Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="c4ced-192">UWP code samples</span></span>  

<span data-ttu-id="c4ced-193">Schauen Sie sich die [universelle Windows-Plattform \ (UWP \) Code Beispiele][MicrosoftDeveloperWindowsSamples] Repo an, um JavaScript-Beispiele für allgemeine Windows 10-App-Szenarien zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-193">Check out the [Universal Windows Platform \(UWP\) Code Samples][MicrosoftDeveloperWindowsSamples] repo to browse JavaScript examples for common Windows 10 app scenarios.</span></span>  <span data-ttu-id="c4ced-194">Obwohl die JS-Versionen dieser Beispiele die [WinJS][GithubWinjsWinjs] -Bibliothek verwenden, um die Beispielvorlage zu strukturieren, ist WinJS für das Senden der WinRT-API-Anforderungen, die in diesen Beispielen demonstriert werden, nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4ced-194">Although the JS versions of these samples use the [WinJS][GithubWinjsWinjs] library to structure the sample template, WinJS is not required for sending the WinRT API requests demonstrated in these samples.</span></span>  

> [!NOTE]
> <span data-ttu-id="c4ced-195">Wenn Sie das [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] Ereignis für die APP Abhören müssen, können Sie dies mit der folgenden systemeigenen WinRT-API tun:</span><span class="sxs-lookup"><span data-stu-id="c4ced-195">If you need to listen for the [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] event for the app, you are able to do this using the following native WinRT API:</span></span>  
> 
> **<span data-ttu-id="c4ced-196">Verwenden Sie diese</span><span class="sxs-lookup"><span data-stu-id="c4ced-196">Use this</span></span>**  
> 
> ```javascript
> Windows.UI.WebUI.WebUIApplication.addEventListener("activated", function (activatedEventArgs) {
>     // Check activatedEventArgs.kind and respond as needed
> });
> ```  
> 
> <span data-ttu-id="c4ced-197">... im Gegensatz zu dieser Art von WinJS-Anforderung, die in den Beispielen verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="c4ced-197">... as opposed this type of WinJS request used in the samples:</span></span>  
> 
> **<span data-ttu-id="c4ced-198">Nicht so</span><span class="sxs-lookup"><span data-stu-id="c4ced-198">Not this</span></span>**  
> 
> ```javascript
>     var page = WinJS.UI.Pages.define("/html/scenario1-launched.html", {
>         ready: function (element, options) {
>             // Check options.activationKind and respond as needed
>         }
>     });
> ```  

## <span data-ttu-id="c4ced-199">Senden von WinRT-API-Anforderungen aus ihrer PWA (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="c4ced-199">Send WinRT API requests from your PWA (EdgeHTML)</span></span>  

<span data-ttu-id="c4ced-200">Nehmen Sie an diesem Punkt an, dass Sie ein benutzerdefiniertes Kontextmenü für Windows-Benutzer unserer PWA \ (EdgeHTML \) hinzufügen und die benötigten APIs im [Windows. UI. Popups][UwpApiWindowsUiPopups] -Namespace identifiziert haben möchten.</span><span class="sxs-lookup"><span data-stu-id="c4ced-200">At this point, pretend you want to add a custom context menu for Windows users of our PWA \(EdgeHTML\) and have identified the APIs you need in the [Windows.UI.Popups][UwpApiWindowsUiPopups] namespace.</span></span>  

<span data-ttu-id="c4ced-201">Um alle WinRT-APIs-Anforderungen aus unserer PWA \ (EdgeHTML \) zu senden, müssen Sie zuerst [die erforderlichen Berechtigungen](#set-application-content-uri-rules-acurs) \ (oder Anwendungsinhalts-URI-Regeln \) in Ihrer Windows-App-Paketmanifest \ ( `.appxmanifest` \)-Datei erstellen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-201">In order to send any WinRT APIs requests from our PWA \(EdgeHTML\), you first need to [establish the requisite permissions](#set-application-content-uri-rules-acurs) \(or, Application Content URI Rules\) in your Windows app package manifest \(`.appxmanifest`\) file.</span></span>  

<span data-ttu-id="c4ced-202">Wenn eine dieser API-Anforderungen den Zugriff auf Benutzer Ressourcen wie Bilder oder Musik oder auf Gerätefeatures wie die Kamera oder das Mikrofon beinhaltet, müssen Sie dem App-Paketmanifest auch [App-Funktionsdeklarationen](#app-capability-declarations) hinzufügen, damit Windows den Benutzer zur Genehmigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="c4ced-202">If any of these API requests involve access to user resources like pictures or music, or to device features like the camera or microphone, you also need to add [app capability declarations](#app-capability-declarations) to the app package manifest in order for Windows to prompt the user for permission.</span></span>  <span data-ttu-id="c4ced-203">Wenn Sie später Ihre PWA \ (EdgeHTML \) im Microsoft Store veröffentlichen, werden diese erforderlichen [App-Berechtigungen][MicrosoftSupportWindowsAppPermissions] auch in Ihrem Store-Eintrag angegeben.</span><span class="sxs-lookup"><span data-stu-id="c4ced-203">If you later publish your PWA \(EdgeHTML\) to the Microsoft Store, these required [App permissions][MicrosoftSupportWindowsAppPermissions] are also noted in your store listing.</span></span>  

#### <span data-ttu-id="c4ced-204">Einrichten von Anwendungsinhalts-URI-Regeln (ACURs)</span><span class="sxs-lookup"><span data-stu-id="c4ced-204">Set Application Content URI Rules (ACURs)</span></span>  

<span data-ttu-id="c4ced-205">Über ACURs (auch als URL-Zulassungsliste bezeichnet) können Sie die URLs Ihres PWA \ (EdgeHTML \) direkten Zugriffs auf Windows-Runtime-APIs angeben.</span><span class="sxs-lookup"><span data-stu-id="c4ced-205">Through ACURs, otherwise known as a URL allow list, you are able to give the URLs of your PWA \(EdgeHTML\) direct access to Windows Runtime APIs.</span></span>  <span data-ttu-id="c4ced-206">Auf der Windows-Betriebssystemebene sind die richtigen Richtlinien Grenzen so eingestellt, dass Code, der auf Ihrem Webserver gehostet wird, direkt Platt Form-API-Anforderungen senden kann.</span><span class="sxs-lookup"><span data-stu-id="c4ced-206">At the Windows OS level, the right policy bounds are set to allow code hosted on your web server to directly send platform API requests.</span></span>  <span data-ttu-id="c4ced-207">Sie definieren diese Grenzen in der APP-Paket Manifestdatei, wenn Sie Ihre PWA-URLs als angeben `ApplicationContentUriRules` .</span><span class="sxs-lookup"><span data-stu-id="c4ced-207">You define these bounds in the app package manifest file when you specify your PWA URLs as `ApplicationContentUriRules`.</span></span>  

<span data-ttu-id="c4ced-208">Ihre Regeln sollten die Startseite für Ihre APP und alle anderen Seiten enthalten, die als App-Seiten enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-208">Your rules should include the start page for your app and any other pages you want included as app pages.</span></span>  <span data-ttu-id="c4ced-209">Wenn der Benutzer zu einer URL navigiert, die nicht in ihren Regeln enthalten ist, öffnet Windows die Ziel-URL im Microsoft Edge-Browser und nicht das eigenständige PWA \ (EdgeHTML \)-Fenster \ ( `WWAHost.exe` Prozess \).</span><span class="sxs-lookup"><span data-stu-id="c4ced-209">If your user navigates to a URL that is not included in your rules, Windows opens the target URL in the Microsoft Edge browser rather than your standalone PWA \(EdgeHTML\) window \(`WWAHost.exe` process\).</span></span>  <span data-ttu-id="c4ced-210">Sie können auch bestimmte URLs ausschließen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-210">You may also exclude specific URLs.</span></span>  

<span data-ttu-id="c4ced-211">Es gibt mehrere Möglichkeiten, eine URL `Match` in ihren Regeln anzugeben:</span><span class="sxs-lookup"><span data-stu-id="c4ced-211">There are several ways to specify a URL `Match` in your rules:</span></span>  

*   <span data-ttu-id="c4ced-212">Ein exakter Hostname</span><span class="sxs-lookup"><span data-stu-id="c4ced-212">An exact hostname</span></span>  
*   <span data-ttu-id="c4ced-213">Ein Hostname, für den ein URI mit einer Unterdomäne dieses Hostnamens einbezogen oder ausgeschlossen wird</span><span class="sxs-lookup"><span data-stu-id="c4ced-213">A hostname for which a URI with any subdomain of that hostname is included or excluded</span></span>  
*   <span data-ttu-id="c4ced-214">Ein exakter URI</span><span class="sxs-lookup"><span data-stu-id="c4ced-214">An exact URI</span></span>  
*   <span data-ttu-id="c4ced-215">Ein exakter URI mit einer Abfrageeigenschaft</span><span class="sxs-lookup"><span data-stu-id="c4ced-215">An exact URI containing a query property</span></span>  
*   <span data-ttu-id="c4ced-216">Ein Teilpfad und ein Platzhalter für die Angabe einer bestimmten Dateierweiterung für eine Einbeziehungsregel</span><span class="sxs-lookup"><span data-stu-id="c4ced-216">A partial path and a wildcard to indicate a particular file extension for an include rule</span></span>  
*   <span data-ttu-id="c4ced-217">Relative Pfade für Ausschlussregeln</span><span class="sxs-lookup"><span data-stu-id="c4ced-217">Relative paths for exclude rules</span></span>  
    
<span data-ttu-id="c4ced-218">Hier sind einige Beispiele für ACURs in einer `.appxmanifest` Datei:</span><span class="sxs-lookup"><span data-stu-id="c4ced-218">Here are a few examples of ACURs in a `.appxmanifest` file:</span></span>  

```xml
<Application
Id="App"
StartPage="https://contoso.com/home">
<uap:ApplicationContentUriRules>
    <uap:Rule Type="include" Match="https://contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="include" Match="https://*.contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="exclude" Match="https://contoso.com/excludethispage.aspx" />
</uap:ApplicationContentUriRules>
```  

<span data-ttu-id="c4ced-219">In der ACURs für Ihre APP definierte URLs können über das `WindowsRuntimeAccess` Attribut, das die folgenden Werte akzeptiert, die Berechtigung für die Windows-Runtime erhalten:</span><span class="sxs-lookup"><span data-stu-id="c4ced-219">URLs defined within the ACURs for your app are able to be granted permission to the Windows Runtime through the `WindowsRuntimeAccess` attribute, which accepts the following values:</span></span>  

*   `all`<span data-ttu-id="c4ced-220">: Remote-JavaScript-Code hat Zugriff auf alle WinRT-APIs und alle lokalen Paketkomponenten.</span><span class="sxs-lookup"><span data-stu-id="c4ced-220">: Remote JavaScript code has access to all WinRT APIs and any local packaged components.</span></span>  <span data-ttu-id="c4ced-221">Der [Windows \ (WinRT \))-][UwpApiIndex] Namespace wird injiziert und im Skriptmodul dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c4ced-221">The [Windows \(WinRT\))][UwpApiIndex] namespace is injected and present in the script engine.</span></span>  
*   `allowForWeb`<span data-ttu-id="c4ced-222">: Der Remote Zugriff auf JavaScript-Code ist auf lokale verpackte Komponenten, einschließlich benutzerdefinierter C++/c #-Komponenten, limitiert.</span><span class="sxs-lookup"><span data-stu-id="c4ced-222">: Remote JavaScript code access is limited to local packaged components, including custom C++/C# components.</span></span>  
*   `none`<span data-ttu-id="c4ced-223">Standard.</span><span class="sxs-lookup"><span data-stu-id="c4ced-223">: Default.</span></span>  <span data-ttu-id="c4ced-224">Die angegebene URL hat keinen Plattformzugriff.</span><span class="sxs-lookup"><span data-stu-id="c4ced-224">The specified URL has no platform access.</span></span>  
    
<span data-ttu-id="c4ced-225">In diesem Lernprogramm haben Sie bereits die einzige ACUR-Version festgesetzt, die Sie benötigen \ (Schritt 6 des vorherigen [Einrichten und Ausführen des App](#set-up-and-run-your-universal-windows-app) -Abschnitts \) für ihre Einzelseiten-app.</span><span class="sxs-lookup"><span data-stu-id="c4ced-225">In this tutorial, you already set the only ACUR that you need \(Step 6 of the previous [Set up and run your app](#set-up-and-run-your-universal-windows-app) section\) for your single-page app.</span></span>  <span data-ttu-id="c4ced-226">Sie können dies über den Bereich " **Inhalts-URIs** " des Visual Studio- `package.appxmanifest` Designers bestätigen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-226">You are able to confirm this from the **Content URIs** panel of the Visual Studio `package.appxmanifest` designer.</span></span>  

![Bereich ' Inhalts-URI ' im Visual Studio-appxmanifest-Designer](media/vs-appxmanifest-editor-acurs.png)  

<span data-ttu-id="c4ced-228">Sie können auch den unformatierten XML-Code ihres Manifests anzeigen, indem Sie `package.appxmanifest` im Visual Studio-Projektmappen-Explorer mit der rechten Maustaste auf die Datei klicken und " **Code anzeigen** \ ( `F7` \)" auswählen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-228">You are also able to view the raw XML of your manifest by right-clicking your `package.appxmanifest` file in Visual Studio Solution Explorer and selecting **View Code** \(`F7`\).</span></span>  <span data-ttu-id="c4ced-229">Wenn Sie wieder zur Entwurfsansicht wechseln möchten, wählen Sie **Ansicht-Designer** \ ( `Shift` + `F7` \) aus.</span><span class="sxs-lookup"><span data-stu-id="c4ced-229">To toggle back to the Designer view, select **View Designer** \(`Shift`+`F7`\).</span></span>  

#### <span data-ttu-id="c4ced-230">Deklarationen von App-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c4ced-230">App capability declarations</span></span>  

<span data-ttu-id="c4ced-231">Wenn Ihre APP programmgesteuerten Zugriff auf Benutzer Ressourcen wie Bilder oder Musik oder auf Geräte wie eine Kamera oder ein Mikrofon benötigt, müssen Sie die entsprechenden [Deklarationen][WindowsUwpPackagingAppCapabilities] für die App-Funktion in Ihre APP-Paket Manifestdatei aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-231">If your app needs programmatic access to user resources like pictures or music, or to devices like a camera or a microphone, you must include the corresponding [App capability declarations][WindowsUwpPackagingAppCapabilities] in your app package manifest file.</span></span>  <span data-ttu-id="c4ced-232">Es gibt drei Kategorien von App Funktionsdeklarationen:</span><span class="sxs-lookup"><span data-stu-id="c4ced-232">There are three app capability declaration categories:</span></span>  

*   <span data-ttu-id="c4ced-233">[Funktionen zur allgemeinen Verwendung][WindowsUwpPackagingAppCapabilitiesGeneralUse], die auf die meisten allgemeinen App-Szenarien zutreffen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-233">[General-use capabilities][WindowsUwpPackagingAppCapabilitiesGeneralUse] that apply to most common app scenarios.</span></span>  
*   <span data-ttu-id="c4ced-234">[Gerätefunktionen][WindowsUwpPackagingAppCapabilitiesDevice], die Ihrer App den Zugriff auf Peripheriegeräte und interne Geräte ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-234">[Device capabilities][WindowsUwpPackagingAppCapabilitiesDevice] that allow your app to access peripheral and internal devices.</span></span>  
*   <span data-ttu-id="c4ced-235">[Funktionen zur Sondernutzung][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] , die Unternehmensszenarien unterstützen und ein Microsoft Store-Unternehmenskonto erfordern.</span><span class="sxs-lookup"><span data-stu-id="c4ced-235">[Special-use capabilities][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] that support enterprise scenarios and require a Microsoft Store company account.</span></span>  <span data-ttu-id="c4ced-236">Weitere Informationen zu Unternehmenskonten finden Sie unter [Kontotypen, Standorte und Gebühren][WindowsUwpPublishAccountTypesLocationsFees].</span><span class="sxs-lookup"><span data-stu-id="c4ced-236">For more info about company accounts, see [Account types, locations, and fees][WindowsUwpPublishAccountTypesLocationsFees].</span></span>
    
<span data-ttu-id="c4ced-237">Auf der Microsoft Store-App-Seite werden alle Funktionen aufgeführt, die Sie in Ihrem App-Paketmanifest deklarieren, daher müssen Sie unbedingt nur die Funktionen angeben, die Ihre APP tatsächlich verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4ced-237">Your Microsoft Store app page lists all the capabilities you declare in your app package manifest, so be sure to only specify the capabilities that your app actually uses.</span></span>

<span data-ttu-id="c4ced-238">Einige Funktionen bieten apps Zugriff auf vertrauliche Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c4ced-238">Some capabilities provide apps access to sensitive resources.</span></span>  <span data-ttu-id="c4ced-239">Diese Ressourcen gelten als vertraulich, weil jede Person auf die persönlichen Daten des Benutzers zugreifen oder dem Nutzer Geld kosten kann.</span><span class="sxs-lookup"><span data-stu-id="c4ced-239">These resources are considered sensitive because each is able to access the user's personal data or cost the user money.</span></span>  <span data-ttu-id="c4ced-240">Mit den Datenschutzeinstellungen, die von der Windows 10- [Einstellungs][BingResultsWindows10Settings] -App verwaltet werden, können Benutzer den Zugriff auf vertrauliche Ressourcen dynamisch steuern.</span><span class="sxs-lookup"><span data-stu-id="c4ced-240">Privacy settings, managed by the Windows 10 [Settings][BingResultsWindows10Settings] app, let the user dynamically control access to sensitive resources.</span></span>  <span data-ttu-id="c4ced-241">Daher ist es wichtig, dass Ihre APP nicht davon ausgeht, dass eine vertrauliche Ressource immer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c4ced-241">Thus, it is important that your app does not assume a sensitive resource is always available.</span></span>  <span data-ttu-id="c4ced-242">Weitere Informationen zum Zugriff auf sensible Ressourcen finden Sie unter [Richtlinien für Apps mit Berücksichtigung von Datenschutz][WindowsUwpSecurityIndex].</span><span class="sxs-lookup"><span data-stu-id="c4ced-242">For more info about accessing sensitive resources, see [Guidelines for privacy-aware apps][WindowsUwpSecurityIndex].</span></span>  

<span data-ttu-id="c4ced-243">Sie fordern Zugriff an, indem Sie Funktionen im Paketmanifest für Ihre APP deklarieren.</span><span class="sxs-lookup"><span data-stu-id="c4ced-243">You request access by declaring capabilities in the package manifest for your app.</span></span>  <span data-ttu-id="c4ced-244">In Visual Studio können Sie dies über den Bereich " **Funktionen** " des Package. appxmanifest-Designers tun.</span><span class="sxs-lookup"><span data-stu-id="c4ced-244">In Visual Studio, you are able to do this from the **Capabilities** panel of the package.appxmanifest designer.</span></span>  

![Bereich "Funktionen" im Visual Studio-appxmanifest-Designer](media/vs-appxmanifest-editor-capabilities.png)  

<span data-ttu-id="c4ced-246">In diesem Lernprogramm ist nur die standardmäßige Internet-Funktion \ (Client \) erforderlich, daher ist keine weitere Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4ced-246">In this tutorial, only the default Internet \(Client\) capability is required, so no further action is needed.</span></span>  

### <span data-ttu-id="c4ced-247">Verwenden der Feature-Erkennung zum Aufrufen von WinRT</span><span class="sxs-lookup"><span data-stu-id="c4ced-247">Use feature detection to invoke WinRT</span></span>  

<span data-ttu-id="c4ced-248">Damit Sie für Ihre PWA-Zielgruppe auf allen Plattformen eine qualitativ hochwertige Baseline erzielen können, verbessern Sie mit der WinRT-Feature-Erkennung schrittweise ihre PWA-Funktionalität für Windows.</span><span class="sxs-lookup"><span data-stu-id="c4ced-248">To ensure a quality baseline experience for your PWA audience across all platforms, you progressively enhance your PWA experience on Windows using WinRT feature detection.</span></span>  <span data-ttu-id="c4ced-249">Auf diese Weise können Sie sicherstellen, dass Ihr Windows-spezifischer Code nur in einem Kontext ausgeführt wird, in dem WinRT-APIs verfügbar und anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="c4ced-249">This way, you are able to be sure your Windows-specific code is only run in a context where WinRT APIs are available and applicable.</span></span>  

<span data-ttu-id="c4ced-250">Die Funktionserkennung kann so einfach sein wie die Suche nach dem `Windows` Objekt \ (dem EntryPoint zum [WinRT-Namespace][UwpApiIndex]\) wie unten:</span><span class="sxs-lookup"><span data-stu-id="c4ced-250">Feature detection may be as simple as looking for the `Windows` object \(the entrypoint to the [WinRT namespace][UwpApiIndex]\) as below:</span></span>  

```javascript
if(window.Windows){
    /*Run code that sends Windows API requests */
}
```  

<span data-ttu-id="c4ced-251">Da jedoch nicht alle Windows-APIs für alle [Windows 10-Gerätetypen][UwpExtensionSdkDeviceFamiliesOverview]verfügbar sind, ist es im Allgemeinen nützlich, eine spezifischere Funktionserkennung zu verwenden, um den Namespace der API-Anforderung, die Sie senden, weiter zu qualifizieren:</span><span class="sxs-lookup"><span data-stu-id="c4ced-251">However, given that not all Windows APIs are available on all [Windows 10 device types][UwpExtensionSdkDeviceFamiliesOverview], it is generally useful to use more specific feature detection to further qualify the namespace of the API request you are sending:</span></span>  

```javascript
if(window.Windows && Windows.Media.SpeechRecognition){
    /*Run code that sends Windows API requests */
}
```  

<span data-ttu-id="c4ced-252">Mit diesem Hintergrund können Sie einige WinRT-Code hinzufügen, um ein benutzerdefiniertes Kontextmenü zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="c4ced-252">With that background, you are ready to add some WinRT code to implement a custom context menu.</span></span>  <span data-ttu-id="c4ced-253">Wenn Sie das Beispiel PWA aus [Erste Schritte mit Progressive Web Apps][PwaGetStarted]verwenden:</span><span class="sxs-lookup"><span data-stu-id="c4ced-253">If you are using the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted]:</span></span>

1.  <span data-ttu-id="c4ced-254">Öffnen Sie Visual Studio für Ihr PWA-Websiteprojekt.</span><span class="sxs-lookup"><span data-stu-id="c4ced-254">Open Visual Studio to your PWA site project.</span></span>  
1.  <span data-ttu-id="c4ced-255">Öffnen Sie im Projektmappen-Explorer die `views\layout.pug` Datei, und fügen Sie die folgende Zeile direkt unter dem `script` Verweis für Ihren Dienstmitarbeiter hinzu:</span><span class="sxs-lookup"><span data-stu-id="c4ced-255">In Solution Explorer, open the `views\layout.pug` file and add the following line, right below the `script` reference for your service worker:</span></span>
    
    ```xml
    script(src='/javascripts/site.js')
    ```  
    
1.  <span data-ttu-id="c4ced-256">Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf den `javascripts` Ordner, und **fügen**Sie  >  **neue Datei hinzu.**</span><span class="sxs-lookup"><span data-stu-id="c4ced-256">In Solution Explorer, right-click on the `javascripts` folder and **Add** > **New File...**.</span></span>
1.  <span data-ttu-id="c4ced-257">Benennen Sie Ihre Datei: `site.js` , und kopieren Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="c4ced-257">Name your file: `site.js`, and copy in the following code:</span></span>
    
    ```javascript
    if (window.Windows && Windows.UI.Popups) {
        document.addEventListener('contextmenu', function (e) {

            // Build the context menu
            var menu = new Windows.UI.Popups.PopupMenu();
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 1", null, 1));
            menu.commands.append(new Windows.UI.Popups.UICommandSeparator);
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 2", null, 2));

            // Convert from webpage to WinRT coordinates
            function pageToWinRT(pageX, pageY) {
                var zoomFactor = document.documentElement.msContentZoomFactor;
                return {
                    x: (pageX - window.pageXOffset) * zoomFactor,
                    y: (pageY - window.pageYOffset) * zoomFactor
                };
            }

            // When the menu is invoked, execute the requested command
            menu.showAsync(pageToWinRT(e.pageX, e.pageY)).done(function (invokedCommand) {
                if (invokedCommand !== null) {
                    switch (invokedCommand.id) {
                        case 1:
                            console.log('Option 1 selected');
                            // Invoke code for option 1
                            break;
                        case 2:
                            console.log('Option 2 selected');
                            // Invoke code for option 2
                            break;
                        default:
                            break;
                    }
                } else {
                    // The command is null if no command was invoked.
                    console.log("Context menu dismissed");
                }
            });
        }, false);
    }
    ```
    
1.  <span data-ttu-id="c4ced-258">Vergleichen Sie das Verhalten des Kontextmenüs, wenn Sie Ihre PWA im Browser ausführen \ ( `F5` aus dem PWA-Websiteprojekt \) versus im Windows-App-Fenster \ ( `F5` aus ihrem universellen Windows-App-Projekt \).</span><span class="sxs-lookup"><span data-stu-id="c4ced-258">Compare the context menu behavior when you run your PWA in the browser \(`F5` from your PWA site project\) versus from inside the Windows app window \(`F5` from your Universal Windows app project\).</span></span>  <span data-ttu-id="c4ced-259">Klicken Sie im Browser mit der rechten Maustaste auf das Standardkontextmenü von Microsoft Edge, während während des `WWAHost.exe` Prozesses das benutzerdefinierte Menü nun angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4ced-259">In the browser, right-clicking gives you the Microsoft Edge default context menu, whereas in the `WWAHost.exe` process, your custom menu now appears.</span></span>  
    
    | <span data-ttu-id="c4ced-260">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c4ced-260">Microsoft Edge</span></span> | <span data-ttu-id="c4ced-261">Windows 10-App</span><span class="sxs-lookup"><span data-stu-id="c4ced-261">Windows 10 app</span></span> |  
    |:--- |:---- |  
    | ![Browser-Standardkontextmenü](media/browser-context-menu.png) | ![Benutzerdefiniertes App-Kontextmenü](media/app-context-menu.png) |  
    
<span data-ttu-id="c4ced-264">Wir hoffen, dass Sie jetzt ein solides Fundament haben, um Ihre PWAs unter Windows schrittweise zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="c4ced-264">Hopefully you now have a solid foundation for progressively enhancing your PWAs on Windows.</span></span>  <span data-ttu-id="c4ced-265">Wenn Sie auf Fragen stoßen oder etwas unklar ist, senden Sie uns bitte einen Kommentar!</span><span class="sxs-lookup"><span data-stu-id="c4ced-265">If you run into questions or anything is unclear, please send a comment!</span></span>  

## <span data-ttu-id="c4ced-266">Vertiefung</span><span class="sxs-lookup"><span data-stu-id="c4ced-266">Going further</span></span>

<span data-ttu-id="c4ced-267">Das [Windows dev Center][MicrosoftDeveloperWindowsApps] ist Ihre vollständige Referenz für alle Phasen des Windows-App-Aufbaus, von den [ersten Schritten][MicrosoftDeveloperWindowsAppsGetStarted]bis zum [entwerfen][MicrosoftDeveloperWindowsAppsDesign], [entwickeln][MicrosoftDeveloperWindowsAppsDevelop]und [veröffentlichen][MicrosoftDeveloperStorePublishApps] im Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="c4ced-267">The [Windows Dev Center][MicrosoftDeveloperWindowsApps] is your complete reference for all stages of Windows app building, from [getting started][MicrosoftDeveloperWindowsAppsGetStarted], to [designing][MicrosoftDeveloperWindowsAppsDesign], [developing][MicrosoftDeveloperWindowsAppsDevelop], and [publishing][MicrosoftDeveloperStorePublishApps] to the Microsoft Store.</span></span>  

<span data-ttu-id="c4ced-268">Eine allgemeine Übersicht über die universelle Windows-Plattform \ (UWP \) und wie Sie auf unterschiedliche Windows 10-Gerätefamilien abzielen, finden Sie unter [Einführung in die universelle Windows-Plattform][WindowsUWPGetStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="c4ced-268">For a general overview on the Universal Windows Platform \(UWP\) and how to target different Windows 10 device families, see [Intro to the Universal Windows Platform][WindowsUWPGetStartedGuide].</span></span>  

<span data-ttu-id="c4ced-269">Und wenn Sie fertig sind, gehen Sie wie folgt vor, um [Ihre PWA an den Microsoft Store](./microsoft-store.md)zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="c4ced-269">And when you are ready, here is how \(and why!\) to [Submit your PWA to the Microsoft Store](./microsoft-store.md).</span></span>  

<!-- links -->  

[PwaGetStarted]: ./get-started.md "Erste Schritte mit Progressive Web-Apps | Microsoft docs"  
[PwaIndexWindows10]: ./index.md#pwas-on-windows-10-edgehtml "PWAs unter Windows 10 (EdgeHTML) – Progressive Web-Apps unter Windows | Microsoft docs"  
[DevToolsGuide]: ../devtools-guide/index.md "Microsoft Edge (EdgeHTML)-Entwickler Tools | Microsoft docs"  
[DevToolsGuideMicrosoftStoreApp]: ../devtools-guide/index.md#microsoft-store-app "Microsoft Store-App – Microsoft Edge (EdgeHTML) Developer Tools | Microsoft docs"  
[DevToolsGuideServiceWorkers]: ../devtools-guide/service-workers.md "Dienstmitarbeiter | Microsoft docs"  
[DevToolsProtocol01ClientsEdgePreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge devtools Preview – devtools-Protokoll Clients | Microsoft docs"  
[DevGuideWhatsNew]: ../dev-guide/whats-new.md "Neuerungen in EdgeHTML | Microsoft docs"  
[WindowsRuntime]: ../windows-runtime/index.md "Windows-Runtime (WinRT) für JavaScript | Microsoft docs"  
[WindowRuntimeUsingJavascript]: ../windows-runtime/using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript | Microsoft docs"  

[ScriptingJsinrtHandlingWinRTEvents]: /scripting/jswinrt/handling-windows-runtime-events-in-javascript "Behandeln von Windows-Runtime-Ereignissen in JavaScript | Microsoft docs"  
[ScriptingJsinrtUsingWinRT]: /scripting/jswinrt/using-windows-runtime-asynchronous-methods "Verwenden von asynchronen Methoden für die Windows-Runtime | Microsoft docs"  
[ScriptingJsinrtUsingWinRTCasingConventions]:  /scripting/jswinrt/using-the-windows-runtime-in-javascript#casing-conventions-with-windows-runtime-features "Konventionen für die Groß-/Kleinschreibung mit Windows-Runtime-Features – unter Verwendung der Windows-Runtime in JavaScript | Microsoft docs"  
[UwpApiIndex]: /uwp/api/index "Windows UWP-Namespaces | Microsoft docs"  
[UwpApiWindowsUiPopups]: /uwp/api/windows.ui.popups "Windows. UI. Popups-Namespace | Microsoft docs"  
[UwpApiWindowsUiWebuiWebapplicationActivated]: /uwp/api/windows.ui.webui.webuiapplication.activated "WebUIApplication. Activated-Ereignis | Microsoft docs"  
[UwpExtensionSdkDeviceFamiliesOverview]: /uwp/extension-sdks/device-families-overview "Übersicht über Gerätefamilien | Microsoft docs"  
[UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest]: /uwp/schemas/appxpackage/uapmanifestschema/generate-package-manifest "So generiert Visual Studio ein App-Paketmanifest | Microsoft docs"  
[WindowsUWPIndex]: /windows/uwp/index "Dokumentation zur universellen Windows-Plattform | Microsoft docs"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide "Was ist eine APP für die universelle Windows-Plattform (UWP)? | Microsoft docs"  
[WindowsUWPGetStartedEnable]: /windows/uwp/get-started/enable-your-device-for-development "Aktivieren Ihres Geräts für die Entwicklung | Microsoft docs"  
[WindowsUwpSecurityIndex]: /windows/uwp/security/index "Sicherheit | Microsoft docs"  
[WindowsUwpPublishAccountTypesLocationsFees]: /windows/uwp/publish/account-types-locations-and-fees "Kontotypen, Standorte und Gebühren | Microsoft docs"  
[WindowsUwpPackagingAppCapabilitiesSpecialRestricted]: /windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities "Eingeschränkte Funktionen | Microsoft docs"  
[WindowsUwpPackagingAppCapabilitiesDevice]: /windows/uwp/packaging/app-capability-declarations#device-capabilities "Gerätefunktionen | Microsoft docs"  
[WindowsUwpPackagingAppCapabilitiesGeneralUse]: /windows/uwp/packaging/app-capability-declarations#general-use-capabilities "Funktionen zur allgemeinen Nutzung | Microsoft docs"  
[WindowsUwpPackagingAppCapabilities]: /windows/uwp/packaging/app-capability-declarations "App-Funktionsdeklarationen | Microsoft docs"  

[BingResultsWindows10Settings]: https://binged.it/2lOGSH0 "Windows 10-Einstellungen – Bing"  
[GithubWinjsWinjs]: https://github.com/winjs/winjs "winjs/winjs | GitHub"  
[MicrosoftDeveloperStorePublishApps]: https://developer.microsoft.com/store/publish-apps/index "Veröffentlichen von Windows-apps und-spielen"  
[MicrosoftDeveloperWindowsApps]: https://developer.microsoft.com/windows/apps/index "Dokumentation zur universellen Windows-Plattform"  
[MicrosoftDeveloperWindowsAppsDesign]: https://developer.microsoft.com/windows/apps/design/index "Entwerfen und Codieren von Windows-apps"  
[MicrosoftDeveloperWindowsAppsDevelop]: https://developer.microsoft.com/windows/apps/develop/index "Entwickeln von UWP-apps"  
[MicrosoftDeveloperWindowsAppsGetStarted]: https://developer.microsoft.com/windows/apps/getstarted/index "Erste Schritte mit Windows 10-apps"  
[MicrosoftDeveloperWindowsSamples]: https://developer.microsoft.com/windows/samples "Code Beispiele"  
[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge devtools Preview"  
[MicrosoftSupportWindowsAppPermissions]: https://support.microsoft.com/help/10557/windows-10-app-permissions "App-Berechtigungen"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Downloads"  
[MicrosoftVisualStudioPreview]: https://visualstudio.microsoft.com/vs/preview "Visual Studio Preview"  
[PreviousVSDownloads]: https://visualstudio.microsoft.com/vs/older-downloads/ "Visual Studio-Downloads"  

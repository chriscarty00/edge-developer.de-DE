---
description: Progressives verbessern ihrer PWA für Windows mit nativen App-Features
title: Anpassen der PWA-EdgeHTML für Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Progressive Web-Apps, PWA, Edge, Windows, WinRT, UWP, EdgeHTML
ms.openlocfilehash: 8ba682b03182194a773568254b66c3616bf4c3e2
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882786"
---
# <span data-ttu-id="c625c-104">Anpassen der PWA-EdgeHTML für Windows</span><span class="sxs-lookup"><span data-stu-id="c625c-104">Tailor your PWA (EdgeHTML) for Windows</span></span>  

<span data-ttu-id="c625c-105">PWAs, die unter Windows 10 installiert sind, [nutzen alle Vorteile][PwaIndexWindows10] der Ausführung als [universelle Windows-Plattform \ (UWP \)][WindowsUWPGetStartedGuide] -apps, einschließlich Schutz durch die Sicherheit der Windows-App-Sandbox und Vollzugriff auf die [Windows-Runtime \ (WinRT \))][UwpApiIndex] -APIs, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="c625c-105">PWAs installed on Windows 10 enjoy [all the benefits][PwaIndexWindows10] of running as [Universal Windows Platform \(UWP\)][WindowsUWPGetStartedGuide] apps, including protection through Windows app sandboxing security and full access to [Windows Runtime \(WinRT\))][UwpApiIndex] APIs, including those for:</span></span>  

*   <span data-ttu-id="c625c-106">Steuern von Gerätefunktionen \ (wie Kamera, Mikrofon, GPS \)</span><span class="sxs-lookup"><span data-stu-id="c625c-106">Controlling device features \(such as camera, microphone, GPS\)</span></span>  
*   <span data-ttu-id="c625c-107">Zugriff auf Benutzer Ressourcen \ (wie Kalender, Kontakte, Dokumente, Musik \)</span><span class="sxs-lookup"><span data-stu-id="c625c-107">Accessing user resources \(such as calendar, contacts, documents, music\)</span></span>  
*   <span data-ttu-id="c625c-108">Starten/Navigieren in ihrer App mithilfe von Cortana-Sprachbefehlen</span><span class="sxs-lookup"><span data-stu-id="c625c-108">Launching / navigating your app through Cortana voice commands</span></span>  
*   <span data-ttu-id="c625c-109">Integration in das Windows-Betriebssystem \ (über das Windows-Aktions Center, die Desktop-Taskleiste und Kontextmenüs \)</span><span class="sxs-lookup"><span data-stu-id="c625c-109">Integrating with the Windows OS \(through the Windows Action Center, desktop taskbar, and context menus\)</span></span>  

<span data-ttu-id="c625c-110">... und dies sind nur einige der zusätzlichen Möglichkeiten für Ihre PWA \ (EdgeHTML \) unter Windows!</span><span class="sxs-lookup"><span data-stu-id="c625c-110">... and these are only a few of the added possibilities for your PWA \(EdgeHTML\) on Windows!</span></span>  

<span data-ttu-id="c625c-111">In diesem Leitfaden wird gezeigt, wie Sie Ihre PWA \ (EdgeHTML \) als Windows 10-App installieren, ausführen und verbessern und gleichzeitig die browserübergreifende und plattformübergreifende Kompatibilität sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="c625c-111">This guide shows you how to install, run, and enhance your PWA \(EdgeHTML\) as a Windows 10 app, while still ensuring cross-browser and cross-platform compatibility.</span></span>  

## <span data-ttu-id="c625c-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c625c-112">Prerequisites</span></span>  

*   <span data-ttu-id="c625c-113">Eine vorhandene PWA \ (oder gehostete Web-App \), entweder eine Live-oder eine localhost-Website.</span><span class="sxs-lookup"><span data-stu-id="c625c-113">An existing PWA \(or hosted web app\), either a live or localhost site.</span></span>  <span data-ttu-id="c625c-114">In diesem Leitfaden wird das Beispiel PWA aus [Erste Schritte mit progressiven Web-Apps][PwaGetStarted]verwendet.</span><span class="sxs-lookup"><span data-stu-id="c625c-114">This guide uses the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted].</span></span>  
*   <span data-ttu-id="c625c-115">Laden Sie die \ (Free \) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].</span><span class="sxs-lookup"><span data-stu-id="c625c-115">Download the \(free\) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].</span></span>  <span data-ttu-id="c625c-116">Sie können auch die Editionen Professional, Enterprise oder [Preview][MicrosoftVisualStudioPreview] verwenden.</span><span class="sxs-lookup"><span data-stu-id="c625c-116">You are also able to use the Professional, Enterprise, or [Preview][MicrosoftVisualStudioPreview] editions.</span></span>  <span data-ttu-id="c625c-117">Wählen Sie im Visual Studio-Installationsprogramm die folgenden Arbeitsauslastungen aus:</span><span class="sxs-lookup"><span data-stu-id="c625c-117">From the Visual Studio Installer, choose the following Workloads:</span></span>  
    *   **<span data-ttu-id="c625c-118">Entwicklung der universellen Windows-Plattform</span><span class="sxs-lookup"><span data-stu-id="c625c-118">Universal Windows Platform development</span></span>**  

## <span data-ttu-id="c625c-119">Einrichten und Ausführen der universellen Windows-App</span><span class="sxs-lookup"><span data-stu-id="c625c-119">Set up and run your Universal Windows app</span></span>  

<span data-ttu-id="c625c-120">Eine PWA \ (EdgeHTML \), die als Windows 10-App installiert ist, wird unabhängig vom Browser in einem eigenständigen \ ( `WWAHost.exe` Prozess \)-Fenster ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c625c-120">A PWA \(EdgeHTML\) installed as a Windows 10 app runs independently from the browser, in a standalone \(`WWAHost.exe` process\) window.</span></span>  <span data-ttu-id="c625c-121">Für die Aktivierung wird einfach ein einfacher app-Wrapper benötigt, der Ihre gehostete Web-App enthält, die Sie mit der Visual Studio-Projektvorlage schnell einrichten können `Progressive Web App (Universal Windows)` .</span><span class="sxs-lookup"><span data-stu-id="c625c-121">Enabling this simply requires a lightweight app wrapper that contains your hosted web app, which you are able to quickly set up using the Visual Studio `Progressive Web App (Universal Windows)` project template.</span></span>  <span data-ttu-id="c625c-122">\ (Alle Ihre APP-Logik, einschließlich des Sendens von systemeigenen Windows-Runtime-API-Anforderungen, erfolgt weiterhin in Ihrem ursprünglichen Web App-Code. \)</span><span class="sxs-lookup"><span data-stu-id="c625c-122">\(All your app logic, including sending native Windows Runtime API requests, still happens in your original web app code.\)</span></span>  

<span data-ttu-id="c625c-123">Richten Sie Ihre Entwicklungsumgebung für die Windows-app in Visual Studio ein.</span><span class="sxs-lookup"><span data-stu-id="c625c-123">Set up your Windows app development environment in Visual Studio.</span></span>  

1.  <span data-ttu-id="c625c-124">Aktivieren Sie in den Windows-Einstellungen den [Entwicklermodus][WindowsUWPGetStartedEnable].</span><span class="sxs-lookup"><span data-stu-id="c625c-124">In your Windows Settings, turn on [Developer mode][WindowsUWPGetStartedEnable].</span></span>  <span data-ttu-id="c625c-125">\ (Geben `developer mode` Sie die Windows-Suchfunktion ein, um Sie zu finden. \)</span><span class="sxs-lookup"><span data-stu-id="c625c-125">\(Type `developer mode` in the Windows searchbar to find it.\)</span></span>  
1.  <span data-ttu-id="c625c-126">Starten Sie Visual Studio, und **Erstellen Sie ein neues Projekt...**</span><span class="sxs-lookup"><span data-stu-id="c625c-126">Launch Visual Studio and **Create a new project...**</span></span>  
1.  <span data-ttu-id="c625c-127">Wählen Sie die Projektvorlage für die C#- **Windows-Anwendungsverpackung** aus.</span><span class="sxs-lookup"><span data-stu-id="c625c-127">Select the C# **Windows Application Packaging Project** template.</span></span>  <span data-ttu-id="c625c-128">Wenn Sie eine frühere Version von Visual Studio verwenden, suchen Sie die entsprechende Vorlage unter **Hosted Web App (Universal Windows)** oder **Progressive Web App (universelle Windows)**.</span><span class="sxs-lookup"><span data-stu-id="c625c-128">If you are using a previous version of Visual Studio, find the equivalent template under **Hosted Web App (Universal Windows)** or **Progressive Web App (Universal Windows)**.</span></span>  
1.  <span data-ttu-id="c625c-129">Wählen Sie die standardmäßige Windows 10 `Target version` \ (neueste Version) und `Minimum version` \ (Build 10586 oder höher \) aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c625c-129">Select the default Windows 10 `Target version` \(most recent release\) and `Minimum version` \(build 10586 or higher\) and click **OK**.</span></span>  

    ![Visual Studio-Auswahldialogfeld für UWP-Projektziel-Builds](media/vs-target-min-version.png)  

    <span data-ttu-id="c625c-131">Das neue Projekt wird geladen, wenn der Paket-appxmanifest-Designer geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="c625c-131">Your new project loads with the package.appxmanifest designer open.</span></span>  <span data-ttu-id="c625c-132">Hier konfigurieren Sie die Details Ihrer APP, einschließlich Paketidentität, Paketabhängigkeiten, erforderliche Funktionen, visuelle Elemente und Erweiterbarkeitspunkte.</span><span class="sxs-lookup"><span data-stu-id="c625c-132">This is where you configure the details of your app, including package identity, package dependencies, required capabilities, visual elements, and extensibility points.</span></span>  <span data-ttu-id="c625c-133">Hierbei handelt es sich um eine leicht konfigurierbare, temporäre Version des App-paketmanifests, das während der APP-Entwicklung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c625c-133">This is an easily configurable, temporary version of the app package manifest used during app development.</span></span>  
    <span data-ttu-id="c625c-134">Wenn Sie Ihr App-Projekt erstellen, [generiert Visual Studio eine AppxManifest.xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] -Datei aus diesen Metadaten, die zum Installieren und Ausführen der APP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c625c-134">When you build your app project, [Visual Studio generates an AppxManifest.xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] file from this metadata, which is used to install and run your app.</span></span>  <span data-ttu-id="c625c-135">Wenn Sie Ihre Datei aktualisieren, müssen Sie `package.appxmanifest` das Projekt neu erstellen, damit beide in ihrer zur Laufzeit wiedergegeben werden `AppxManifest.xml` .</span><span class="sxs-lookup"><span data-stu-id="c625c-135">Whenever you update your `package.appxmanifest` file, be sure to rebuild the project so both are reflected in your `AppxManifest.xml` at runtime.</span></span>  

1.  <span data-ttu-id="c625c-136">Geben Sie im Manifest-Designer- **Anwendungs** Bereich die URL ihrer PWA als `Start page` .</span><span class="sxs-lookup"><span data-stu-id="c625c-136">In the manifest designer **Application** panel, enter the URL of your PWA as the `Start page`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c625c-137">Dienstmitarbeiter werden für alle HTTPS \ (Secure, Remote \)-URLs unterstützt, die als `StartPage` .</span><span class="sxs-lookup"><span data-stu-id="c625c-137">Service workers are supported for all https \(secure, remote\) urls specified as the `StartPage`.</span></span>  <span data-ttu-id="c625c-138">Dienstmitarbeiter werden standardmäßig nicht für Webanwendungen unterstützt, die eine lokale Startseite angeben.</span><span class="sxs-lookup"><span data-stu-id="c625c-138">Service workers are not supported by default for web apps that specify a local start page.</span></span>  <span data-ttu-id="c625c-139">Um die Unterstützung der Dienstmitarbeiter für diese Fälle zu aktivieren, fügen Sie dem Manifest einen expliziten [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) -Eintrag hinzu, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="c625c-139">To enable service worker support for these cases, add an explicit [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) entry to the manifest, for example:</span></span> `<uap:Rule Match="http://web-platform.test/" Type="include" uap5:ServiceWorker="true"/>`  
    
    ![Anwendungsbereich des Pakets. appxmanifest-Designer](media/vs-manifest-application.png)  
    
    <span data-ttu-id="c625c-141">Sie können auch das `Display name` und `Description` nach Belieben ändern.</span><span class="sxs-lookup"><span data-stu-id="c625c-141">You are able to also modify the `Display name` and `Description` as you like.</span></span>  
1.  <span data-ttu-id="c625c-142">Speichern Sie diese Datei \ (oder ein anderes 512x512-Bild Ihrer Wahl) auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="c625c-142">Save this file \(or another 512x512 image of your choosing\) to your desktop.</span></span>  
    <span data-ttu-id="c625c-143">Klicken Sie dann im Manifest-Designer **Visual Assets** Panel auf die `Source` Schaltfläche Feld **...** , wählen Sie Sie als Quelldatei aus, und klicken Sie auf **generieren**.</span><span class="sxs-lookup"><span data-stu-id="c625c-143">Then, in the manifest designer **Visual Assets** panel, click on the `Source` field **...** button, select it as your source file, and click **Generate**.</span></span>  <span data-ttu-id="c625c-144">\ (Klicken Sie dann auf **OK** , um die Standardplatzhalter-Bilder zu überschreiben \).</span><span class="sxs-lookup"><span data-stu-id="c625c-144">\(Then click **OK** to overwrite the default placeholder images\).</span></span>  
    
    ![Bereich "visuelle Objekte" des Pakets. appxmanifest-Designer](media/vs-manifest-visual-assets.png)  
    
    <span data-ttu-id="c625c-146">Dadurch werden die grundlegenden visuellen Ressourcen zum Installieren, ausführen, starten und Verteilen Ihrer APP im Store generiert.</span><span class="sxs-lookup"><span data-stu-id="c625c-146">This generates the basic visual assets for installing, running, launching, and distributing your app in the store.</span></span>  
    <span data-ttu-id="c625c-147">Wenn rote `X` Fehlermeldungen angezeigt werden, die auf fehlende Bilder hindeuten, können Sie auf die Schaltfläche.. **.** klicken, um eine Datei aus den generierten Bildern manuell auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c625c-147">If you see any red \(`X`\) errors indicating missing images, you are able to click on the **...** buttons to manually select a file from the generated images.</span></span>  
1.  <span data-ttu-id="c625c-148">Ersetzen Sie im Bereich Manifest-Designer- **Inhalts-URIs** `http://example.com` durch den Speicherort Ihrer PWA \ (so `Rule`  =  `include` und `WinRT Access`  =  `All` \).</span><span class="sxs-lookup"><span data-stu-id="c625c-148">In the manifest designer **Content URIs** panel, replace `http://example.com` with the location of your PWA \(such that `Rule` = `include` and `WinRT Access` = `All`\).</span></span>  
    <span data-ttu-id="c625c-149">Dadurch wird Ihre PWA-Berechtigung zum Senden systemeigener Windows-Runtime \ (WinRT \)-API-Anforderungen gewährt, wenn Sie als Windows 10-app ausgeführt wird, die ein wenig später abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="c625c-149">This grants your PWA permission to send native Windows Runtime \(WinRT\) API requests when running as a Windows 10 app, which is covered a bit later.</span></span>   <span data-ttu-id="c625c-150">Wenn für ihre eigentliche PWA kein WinRT-Zugriff erforderlich ist, können Sie den `WinRT Access` Wert auf ändern `None` .</span><span class="sxs-lookup"><span data-stu-id="c625c-150">If your actual PWA does not require WinRT access, you are able to switch the `WinRT Access` value to `None`.</span></span>  <span data-ttu-id="c625c-151">Achten Sie auf jeden Fall darauf, die Standard `http://example.com` Zeichenfolge mit dem URI ihrer PWA zu unterteilen, oder die APP kann zur Laufzeit nicht ordnungsgemäß geladen werden.</span><span class="sxs-lookup"><span data-stu-id="c625c-151">Either way, be sure to sub out the default `http://example.com` string with the URI of your PWA, or your app is not able to properly load at runtime.</span></span>  
    <span data-ttu-id="c625c-152">Sie können Ihre PWA als Windows 10-app ausführen und Debuggen.</span><span class="sxs-lookup"><span data-stu-id="c625c-152">You are ready to run and debug your PWA as a Windows 10 app.</span></span>  <span data-ttu-id="c625c-153">Wenn Sie eine localhost-Website verwenden, um diesen Leitfaden zu durchlaufen, stellen Sie sicher, dass Sie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c625c-153">If you are using a localhost site to step through this guide, make sure it is running.</span></span>  <span data-ttu-id="c625c-154">Dann</span><span class="sxs-lookup"><span data-stu-id="c625c-154">Then,</span></span>  
1.  <span data-ttu-id="c625c-155">Erstellen Sie \ ( `Ctrl` + `Shift` + `F5` \), und führen `F5` Sie das PWA-Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="c625c-155">Build \(`Ctrl`+`Shift`+`F5`\) and Run \(`F5`\) your PWA project.</span></span>  <span data-ttu-id="c625c-156">Ihre Website sollte nun in einem eigenständigen App-Fenster gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="c625c-156">Your website should now launch in a standalone app window.</span></span>  <span data-ttu-id="c625c-157">Es handelt sich nicht nur um eine gehostete Web-App; Sie wird als Progressive Web-App auf Windows 10 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c625c-157">Not only is it a hosted web app; it is running as a Progressive Web App installed on Windows 10!</span></span>  

    ![PWA wird in einem WWAHost.exe Fenster ausgeführt](media/wwahost.png)  

## <span data-ttu-id="c625c-159">Debuggen Ihrer PWA \ (EdgeHTML \) als Windows-App</span><span class="sxs-lookup"><span data-stu-id="c625c-159">Debug your PWA \(EdgeHTML\) as a Windows app</span></span>  

<span data-ttu-id="c625c-160">Da es sich bei einer PWA \ (EdgeHTML \) einfach um eine progressiv erweiterte gehostete Web-App handelt, können Sie Ihren serverseitigen Code wie jede andere Web-App mit der üblichen IDE und dem normalen Workflow Debuggen.</span><span class="sxs-lookup"><span data-stu-id="c625c-160">Because a PWA \(EdgeHTML\) is simply a progressively enhanced hosted web app, you are able to debug your server-side code the same as any web app, using your usual IDE and workflow.</span></span>  <span data-ttu-id="c625c-161">Die von Ihnen bereitgestellten Änderungen werden in Ihrer installierten PWA-Version wiedergegeben, wenn Sie Sie das nächste Mal starten \ (Sie müssen das universelle Windows-App-Paket nicht erneut bereitstellen).</span><span class="sxs-lookup"><span data-stu-id="c625c-161">The changes you deploy live are reflected in your installed PWA the next time you launch it \(no need to redeploy your Universal Windows app package\).</span></span>

<span data-ttu-id="c625c-162">Für das clientseitige Debuggen in Ihrer Windows 10-App müssen Sie über die `Microsoft Edge DevTools Preview` App verfügen.</span><span class="sxs-lookup"><span data-stu-id="c625c-162">For client-side debugging within your Windows 10 app, you must have the `Microsoft Edge DevTools Preview` app.</span></span>  <span data-ttu-id="c625c-163">Diese eigenständige App umfasst die gesamte Funktionalität des ursprünglichen in-Browser- [Microsoft Edge-devtools][DevToolsGuide] \ (einschließlich [PWA-Tools][DevToolsGuideServiceWorkers]\) sowie die grundlegende Unterstützung für [Remotedebuggen][DevToolsProtocol01ClientsEdgePreview] sowie eine [Debug-Zielauswahl][DevToolsGuideMicrosoftStoreApp] zum Anfügen an eine beliebige ausgeführte Instanz des EdgeHTML-Moduls, einschließlich Add-Ins für Office, Cortana, App-Webansichten und natürlich PWAs, die unter Windows ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c625c-163">This standalone app includes all the functionality of the original in-browser [Microsoft Edge DevTools][DevToolsGuide] \(including [PWA tools][DevToolsGuideServiceWorkers]\), plus basic [remote debugging][DevToolsProtocol01ClientsEdgePreview] support and a [Debug Target chooser][DevToolsGuideMicrosoftStoreApp] for attaching to any running instance of the EdgeHTML engine, including add-ins for Office, Cortana, app webviews, and of course, PWAs running on Windows.</span></span>  

<span data-ttu-id="c625c-164">Hier erfahren Sie, wie Sie das Debuggen für Ihre PWA \ (EdgeHTML \) einrichten.</span><span class="sxs-lookup"><span data-stu-id="c625c-164">Here is how to set up debugging for your PWA \(EdgeHTML\).</span></span>  

1.  <span data-ttu-id="c625c-165">Installieren Sie die [Microsoft Edge devtools Preview][MicrosoftStoreEdgeDevtoolsPreview] -App aus dem Microsoft Store, wenn Sie Sie nicht bereits haben.</span><span class="sxs-lookup"><span data-stu-id="c625c-165">Install the [Microsoft Edge DevTools Preview][MicrosoftStoreEdgeDevtoolsPreview] app from the Microsoft Store if you do not already have it.</span></span>  
1.  <span data-ttu-id="c625c-166">Starten Sie die devtools-APP, während ihre PWA-Website ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c625c-166">With your PWA site up and running, launch the DevTools app.</span></span>  
1.  <span data-ttu-id="c625c-167">Starten Sie in Visual Studio Ihre Windows 10-App mit `Start Without Debugging` dem `Ctrl` + `F5` Befehl ().</span><span class="sxs-lookup"><span data-stu-id="c625c-167">From Visual Studio, launch your Windows 10 app with the `Start Without Debugging` (`Ctrl`+`F5`) command.</span></span>  <span data-ttu-id="c625c-168">\ (Die devtools-APP wird nicht ordnungsgemäß angefügt, wenn der Visual Studio-Debugger aktiv ist. \)</span><span class="sxs-lookup"><span data-stu-id="c625c-168">\(The DevTools app does not attach properly if the Visual Studio debugger is active.\)</span></span>  
1.  <span data-ttu-id="c625c-169">Klicken Sie in der devtools-app in der lokalen Debug-Zielauswahl auf die Schaltfläche **Aktualisieren** .</span><span class="sxs-lookup"><span data-stu-id="c625c-169">In the DevTools app, click the **Refresh** button in the Local debug target chooser.</span></span>  <span data-ttu-id="c625c-170">Ihre PWA \ (EdgeHTML \)-Website sollte nun aufgelistet sein.</span><span class="sxs-lookup"><span data-stu-id="c625c-170">Your PWA \(EdgeHTML\) site should now be listed.</span></span>  <span data-ttu-id="c625c-171">\ (Wenn Sie auch in einem Browserfenster ausgeführt wird, handelt es sich um die letzte Instanz dieser Website in der Liste. \)</span><span class="sxs-lookup"><span data-stu-id="c625c-171">\(If it is also running in a browser window, it is the last instance of that site in the list.\)</span></span>  
1.  <span data-ttu-id="c625c-172">Klicken Sie auf Ihren PWA \ (EdgeHTML \)-Website Eintrag, um eine neue Registerkarte für devtools-Instanzen zu öffnen und das Debuggen zu starten.</span><span class="sxs-lookup"><span data-stu-id="c625c-172">Click on your PWA \(EdgeHTML\) site listing to open a new DevTools instance tab and start debugging.</span></span>  
    
    ![Lokale Debug-Zielauswahl in der Microsoft Edge devtools-App](media/devtools-local.png)  
    
1.  <span data-ttu-id="c625c-174">Sie können überprüfen, ob devtools an Ihre PWA-running-as-Windows-App angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="c625c-174">You are able to verify that DevTools is attached to your PWA-running-as-Windows-app.</span></span>  <span data-ttu-id="c625c-175">Geben Sie in der devtools- **Konsole**Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="c625c-175">In the DevTools **Console**, type:</span></span>  
    
    ```shell
    window.Windows
    ```  
    
    <span data-ttu-id="c625c-176">Dadurch wird das globale `Windows Runtime` Objekt zurückgegeben, das alle [WinRT-Namespaces der obersten Ebene](#find-windows-runtime-winrt-apis)enthält.</span><span class="sxs-lookup"><span data-stu-id="c625c-176">This returns the global `Windows Runtime` object containing all of the [top-level WinRT namespaces](#find-windows-runtime-winrt-apis).</span></span>  <span data-ttu-id="c625c-177">Hierbei handelt es sich um Ihren PWA \ (EdgeHTML \)-Einstiegsbereich für die [universelle Windows-Plattform][WindowsUWPIndex], der nur für Web-Apps verfügbar gemacht wird, die als Windows 10-apps ausgeführt werden (die außerhalb des Browsers ausgeführt werden, in einem `WWAHost.exe` Prozess).</span><span class="sxs-lookup"><span data-stu-id="c625c-177">This is your PWA \(EdgeHTML\) entrypoint to the [Universal Windows Platform][WindowsUWPIndex], and only exposed to web apps that run as Windows 10 apps (running outside the browser, in a `WWAHost.exe` process).</span></span>  
    
## <span data-ttu-id="c625c-178">Suchen von Windows-Runtime \ (WinRT \)-APIs</span><span class="sxs-lookup"><span data-stu-id="c625c-178">Find Windows Runtime \(WinRT\) APIs</span></span>  

<span data-ttu-id="c625c-179">Als installierte Windows-App verfügt Ihre [PWA \ (EdgeHTML \) über vollen Zugriff auf systemeigene Windows-Runtime-APIs][WindowsRuntime]. Ermitteln Sie, was Sie verwenden müssen, rufen Sie die erforderlichen Berechtigungen ab, und verwenden Sie die Feature-Erkennung, um diese API-Anforderung in unterstützten Umgebungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="c625c-179">As an installed Windows app, your [PWA \(EdgeHTML\) has full access to native Windows Runtime APIs][WindowsRuntime]; identify what you need to use, obtain the requisite permissions, and employ feature detection to send that API request on supported environments.</span></span>  <span data-ttu-id="c625c-180">Gehen Sie durch diesen Vorgang, um eine progressive Verbesserung für Windows-Desktopbenutzer ihrer PWA hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c625c-180">Walk through this process to add a progressive enhancement for Windows desktop users of your PWA.</span></span>  

<span data-ttu-id="c625c-181">Es gibt eine Reihe von Möglichkeiten, die universellen Windows-Plattform-APIs zu identifizieren, die Sie für Ihre Windows-PWA benötigen, einschließlich Durchsuchen der umfassenden [UWP-Dokumente auf Windows dev Center] [UWP/API/], herunterladen und Ausführen von [UWP-Codebeispielen](#uwp-code-samples) in Visual Studio und Durchsuchen von Codeausschnitten für allgemeine Aufgaben für PWAs unter Windows.</span><span class="sxs-lookup"><span data-stu-id="c625c-181">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for PWAs on Windows.</span></span>

<span data-ttu-id="c625c-182">Es gibt eine Reihe von Möglichkeiten, die für Ihre Windows-PWA benötigten APIs für die universelle Windows-Plattform zu identifizieren, einschließlich Durchsuchen der umfassenden [UWP-Dokumente auf Windows dev Center] [UWP/API/], herunterladen und Ausführen von [UWP-Codebeispielen](#uwp-code-samples) in Visual Studio und Durchsuchen von Codeausschnitten für allgemeine Aufgaben für [PWAs unter Windows 10 (EdgeHTML)][PwaIndexWindows10].</span><span class="sxs-lookup"><span data-stu-id="c625c-182">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for [PWAs on Windows 10 (EdgeHTML)][PwaIndexWindows10].</span></span>  

<span data-ttu-id="c625c-183">Insgesamt arbeiten WinRT-APIs in JavaScript auf die gleiche Weise wie in C#, daher können Sie die allgemeine [Dokumentation zur universellen Windows-Plattform][WindowsUWPIndex] und die [API-Referenz][UwpApiIndex] für die Verwendung befolgen.</span><span class="sxs-lookup"><span data-stu-id="c625c-183">Overall, WinRT APIs work in JavaScript the same way they do in C#, so you may follow the general [Universal Windows Platform documentation][WindowsUWPIndex] and [API Reference][UwpApiIndex] for usage.</span></span>  <span data-ttu-id="c625c-184">Beachten Sie jedoch die folgenden Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="c625c-184">However, please note the following differences:</span></span>  

*   <span data-ttu-id="c625c-185">WinRT-Features in JavaScript verwenden [unterschiedliche Konventionen][ScriptingJsinrtUsingWinRTCasingConventions] für die Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="c625c-185">WinRT features in JavaScript use  [different casing conventions][ScriptingJsinrtUsingWinRTCasingConventions]</span></span>  
*   <span data-ttu-id="c625c-186">[Ereignisse werden als Zeichenfolgenbezeichner dargestellt][ScriptingJsinrtHandlingWinRTEvents] , die an Klassen `addEventListener` / `removeEventListener` Methoden übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c625c-186">[Events are represented as string identifiers][ScriptingJsinrtHandlingWinRTEvents] passed to class `addEventListener`/`removeEventListener` methods</span></span>  
*   <span data-ttu-id="c625c-187">[Asynchrone Methoden][ScriptingJsinrtUsingWinRT] verwenden das JavaScript-Promise-Modell</span><span class="sxs-lookup"><span data-stu-id="c625c-187">[Asynchronous methods][ScriptingJsinrtUsingWinRT] use the JavaScript Promise model</span></span>  
*   <span data-ttu-id="c625c-188">APIs im `Windows.UI.Xaml` Namespace werden für JavaScript-apps nicht unterstützt, die stattdessen den [EdgeHTML][DevGuideWhatsNew] Engine Web Rendering Stack \ (HTML, CSS \) verwenden.</span><span class="sxs-lookup"><span data-stu-id="c625c-188">APIs in the `Windows.UI.Xaml` namespace are not supported for JavaScript apps, which instead use the [EdgeHTML][DevGuideWhatsNew] engine web rendering stack \(HTML, CSS\)</span></span>  

<span data-ttu-id="c625c-189">Weitere Informationen finden Sie unter [Verwenden der Windows-Runtime in JavaScript][WindowRuntimeUsingJavascript].</span><span class="sxs-lookup"><span data-stu-id="c625c-189">For more details, see [Using the Windows Runtime in JavaScript][WindowRuntimeUsingJavascript].</span></span>  

### <span data-ttu-id="c625c-190">UWP-Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="c625c-190">UWP code samples</span></span>  

<span data-ttu-id="c625c-191">Schauen Sie sich die [universelle Windows-Plattform \ (UWP \) Code Beispiele][MicrosoftDeveloperWindowsSamples] Repo an, um JavaScript-Beispiele für allgemeine Windows 10-App-Szenarien zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="c625c-191">Check out the [Universal Windows Platform \(UWP\) Code Samples][MicrosoftDeveloperWindowsSamples] repo to browse JavaScript examples for common Windows 10 app scenarios.</span></span>  <span data-ttu-id="c625c-192">Obwohl die JS-Versionen dieser Beispiele die [WinJS][GithubWinjsWinjs] -Bibliothek verwenden, um die Beispielvorlage zu strukturieren, ist WinJS für das Senden der WinRT-API-Anforderungen, die in diesen Beispielen demonstriert werden, nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c625c-192">Although the JS versions of these samples use the [WinJS][GithubWinjsWinjs] library to structure the sample template, WinJS is not required for sending the WinRT API requests demonstrated in these samples.</span></span>  

> [!NOTE]
> <span data-ttu-id="c625c-193">Wenn Sie das [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] Ereignis für die APP Abhören müssen, können Sie dies mit der folgenden systemeigenen WinRT-API tun:</span><span class="sxs-lookup"><span data-stu-id="c625c-193">If you need to listen for the [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] event for the app, you are able to do this using the following native WinRT API:</span></span>  
> 
> **<span data-ttu-id="c625c-194">Verwenden Sie diese</span><span class="sxs-lookup"><span data-stu-id="c625c-194">Use this</span></span>**  
> 
> ```javascript
> Windows.UI.WebUI.WebUIApplication.addEventListener("activated", function (activatedEventArgs) {
>     // Check activatedEventArgs.kind and respond as needed
> });
> ```  
> 
> <span data-ttu-id="c625c-195">... im Gegensatz zu dieser Art von WinJS-Anforderung, die in den Beispielen verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="c625c-195">... as opposed this type of WinJS request used in the samples:</span></span>  
> 
> **<span data-ttu-id="c625c-196">Nicht so</span><span class="sxs-lookup"><span data-stu-id="c625c-196">Not this</span></span>**  
> 
> ```javascript
>     var page = WinJS.UI.Pages.define("/html/scenario1-launched.html", {
>         ready: function (element, options) {
>             // Check options.activationKind and respond as needed
>         }
>     });
> ```  

## <span data-ttu-id="c625c-197">Senden von WinRT-API-Anforderungen aus ihrer PWA (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="c625c-197">Send WinRT API requests from your PWA (EdgeHTML)</span></span>  

<span data-ttu-id="c625c-198">Nehmen Sie an diesem Punkt an, dass Sie ein benutzerdefiniertes Kontextmenü für Windows-Benutzer unserer PWA \ (EdgeHTML \) hinzufügen und die benötigten APIs im [Windows. UI. Popups][UwpApiWindowsUiPopups] -Namespace identifiziert haben möchten.</span><span class="sxs-lookup"><span data-stu-id="c625c-198">At this point, pretend you want to add a custom context menu for Windows users of our PWA \(EdgeHTML\) and have identified the APIs you need in the [Windows.UI.Popups][UwpApiWindowsUiPopups] namespace.</span></span>  

<span data-ttu-id="c625c-199">Um alle WinRT-APIs-Anforderungen aus unserer PWA \ (EdgeHTML \) zu senden, müssen Sie zuerst [die erforderlichen Berechtigungen](#set-application-content-uri-rules-acurs) \ (oder Anwendungsinhalts-URI-Regeln \) in Ihrer Windows-App-Paketmanifest \ ( `.appxmanifest` \)-Datei erstellen.</span><span class="sxs-lookup"><span data-stu-id="c625c-199">In order to send any WinRT APIs requests from our PWA \(EdgeHTML\), you first need to [establish the requisite permissions](#set-application-content-uri-rules-acurs) \(or, Application Content URI Rules\) in your Windows app package manifest \(`.appxmanifest`\) file.</span></span>  

<span data-ttu-id="c625c-200">Wenn eine dieser API-Anforderungen den Zugriff auf Benutzer Ressourcen wie Bilder oder Musik oder auf Gerätefeatures wie die Kamera oder das Mikrofon beinhaltet, müssen Sie dem App-Paketmanifest auch [App-Funktionsdeklarationen](#app-capability-declarations) hinzufügen, damit Windows den Benutzer zur Genehmigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="c625c-200">If any of these API requests involve access to user resources like pictures or music, or to device features like the camera or microphone, you also need to add [app capability declarations](#app-capability-declarations) to the app package manifest in order for Windows to prompt the user for permission.</span></span>  <span data-ttu-id="c625c-201">Wenn Sie später Ihre PWA \ (EdgeHTML \) im Microsoft Store veröffentlichen, werden diese erforderlichen [App-Berechtigungen][MicrosoftSupportWindowsAppPermissions] auch in Ihrem Store-Eintrag angegeben.</span><span class="sxs-lookup"><span data-stu-id="c625c-201">If you later publish your PWA \(EdgeHTML\) to the Microsoft Store, these required [App permissions][MicrosoftSupportWindowsAppPermissions] are also noted in your store listing.</span></span>  

#### <span data-ttu-id="c625c-202">Einrichten von Anwendungsinhalts-URI-Regeln (ACURs)</span><span class="sxs-lookup"><span data-stu-id="c625c-202">Set Application Content URI Rules (ACURs)</span></span>  

<span data-ttu-id="c625c-203">Über ACURs (auch als URL-Zulassungsliste bezeichnet) können Sie die URLs Ihres PWA \ (EdgeHTML \) direkten Zugriffs auf Windows-Runtime-APIs angeben.</span><span class="sxs-lookup"><span data-stu-id="c625c-203">Through ACURs, otherwise known as a URL allow list, you are able to give the URLs of your PWA \(EdgeHTML\) direct access to Windows Runtime APIs.</span></span>  <span data-ttu-id="c625c-204">Auf der Windows-Betriebssystemebene sind die richtigen Richtlinien Grenzen so eingestellt, dass Code, der auf Ihrem Webserver gehostet wird, direkt Platt Form-API-Anforderungen senden kann.</span><span class="sxs-lookup"><span data-stu-id="c625c-204">At the Windows OS level, the right policy bounds are set to allow code hosted on your web server to directly send platform API requests.</span></span>  <span data-ttu-id="c625c-205">Sie definieren diese Grenzen in der APP-Paket Manifestdatei, wenn Sie Ihre PWA-URLs als angeben `ApplicationContentUriRules` .</span><span class="sxs-lookup"><span data-stu-id="c625c-205">You define these bounds in the app package manifest file when you specify your PWA URLs as `ApplicationContentUriRules`.</span></span>  

<span data-ttu-id="c625c-206">Ihre Regeln sollten die Startseite für Ihre APP und alle anderen Seiten enthalten, die als App-Seiten enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="c625c-206">Your rules should include the start page for your app and any other pages you want included as app pages.</span></span>  <span data-ttu-id="c625c-207">Wenn der Benutzer zu einer URL navigiert, die nicht in ihren Regeln enthalten ist, öffnet Windows die Ziel-URL im Microsoft Edge-Browser und nicht das eigenständige PWA \ (EdgeHTML \)-Fenster \ ( `WWAHost.exe` Prozess \).</span><span class="sxs-lookup"><span data-stu-id="c625c-207">If your user navigates to a URL that is not included in your rules, Windows opens the target URL in the Microsoft Edge browser rather than your standalone PWA \(EdgeHTML\) window \(`WWAHost.exe` process\).</span></span>  <span data-ttu-id="c625c-208">Sie können auch bestimmte URLs ausschließen.</span><span class="sxs-lookup"><span data-stu-id="c625c-208">You may also exclude specific URLs.</span></span>  

<span data-ttu-id="c625c-209">Es gibt mehrere Möglichkeiten, eine URL `Match` in ihren Regeln anzugeben:</span><span class="sxs-lookup"><span data-stu-id="c625c-209">There are several ways to specify a URL `Match` in your rules:</span></span>  

*   <span data-ttu-id="c625c-210">Ein exakter Hostname</span><span class="sxs-lookup"><span data-stu-id="c625c-210">An exact hostname</span></span>  
*   <span data-ttu-id="c625c-211">Ein Hostname, für den ein URI mit einer Unterdomäne dieses Hostnamens einbezogen oder ausgeschlossen wird</span><span class="sxs-lookup"><span data-stu-id="c625c-211">A hostname for which a URI with any subdomain of that hostname is included or excluded</span></span>  
*   <span data-ttu-id="c625c-212">Ein exakter URI</span><span class="sxs-lookup"><span data-stu-id="c625c-212">An exact URI</span></span>  
*   <span data-ttu-id="c625c-213">Ein exakter URI mit einer Abfrageeigenschaft</span><span class="sxs-lookup"><span data-stu-id="c625c-213">An exact URI containing a query property</span></span>  
*   <span data-ttu-id="c625c-214">Ein Teilpfad und ein Platzhalter für die Angabe einer bestimmten Dateierweiterung für eine Einbeziehungsregel</span><span class="sxs-lookup"><span data-stu-id="c625c-214">A partial path and a wildcard to indicate a particular file extension for an include rule</span></span>  
*   <span data-ttu-id="c625c-215">Relative Pfade für Ausschlussregeln</span><span class="sxs-lookup"><span data-stu-id="c625c-215">Relative paths for exclude rules</span></span>  

<span data-ttu-id="c625c-216">Hier sind einige Beispiele für ACURs in einer `.appxmanifest` Datei:</span><span class="sxs-lookup"><span data-stu-id="c625c-216">Here are a few examples of ACURs in a `.appxmanifest` file:</span></span>  

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

<span data-ttu-id="c625c-217">In der ACURs für Ihre APP definierte URLs können über das `WindowsRuntimeAccess` Attribut, das die folgenden Werte akzeptiert, die Berechtigung für die Windows-Runtime erhalten:</span><span class="sxs-lookup"><span data-stu-id="c625c-217">URLs defined within the ACURs for your app are able to be granted permission to the Windows Runtime through the `WindowsRuntimeAccess` attribute, which accepts the following values:</span></span>  

*   `all`<span data-ttu-id="c625c-218">: Remote-JavaScript-Code hat Zugriff auf alle WinRT-APIs und alle lokalen Paketkomponenten.</span><span class="sxs-lookup"><span data-stu-id="c625c-218">: Remote JavaScript code has access to all WinRT APIs and any local packaged components.</span></span>  <span data-ttu-id="c625c-219">Der [Windows \ (WinRT \))-][UwpApiIndex] Namespace wird injiziert und im Skriptmodul dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c625c-219">The [Windows \(WinRT\))][UwpApiIndex] namespace is injected and present in the script engine.</span></span>  
*   `allowForWeb`<span data-ttu-id="c625c-220">: Der Remote Zugriff auf JavaScript-Code ist auf lokale verpackte Komponenten, einschließlich benutzerdefinierter C++/c #-Komponenten, limitiert.</span><span class="sxs-lookup"><span data-stu-id="c625c-220">: Remote JavaScript code access is limited to local packaged components, including custom C++/C# components.</span></span>  
*   `none`<span data-ttu-id="c625c-221">Standard.</span><span class="sxs-lookup"><span data-stu-id="c625c-221">: Default.</span></span>  <span data-ttu-id="c625c-222">Die angegebene URL hat keinen Plattformzugriff.</span><span class="sxs-lookup"><span data-stu-id="c625c-222">The specified URL has no platform access.</span></span>  

<span data-ttu-id="c625c-223">In diesem Lernprogramm haben Sie bereits die einzige ACUR-Version festgesetzt, die Sie benötigen \ (Schritt 6 des vorherigen [Einrichten und Ausführen des App](#set-up-and-run-your-universal-windows-app) -Abschnitts \) für ihre Einzelseiten-app.</span><span class="sxs-lookup"><span data-stu-id="c625c-223">In this tutorial, you already set the only ACUR that you need \(Step 6 of the previous [Set up and run your app](#set-up-and-run-your-universal-windows-app) section\) for your single-page app.</span></span>  <span data-ttu-id="c625c-224">Sie können dies über den Bereich " **Inhalts-URIs** " des Visual Studio- `package.appxmanifest` Designers bestätigen.</span><span class="sxs-lookup"><span data-stu-id="c625c-224">You are able to confirm this from the **Content URIs** panel of the Visual Studio `package.appxmanifest` designer.</span></span>  

![Bereich ' Inhalts-URI ' im Visual Studio-appxmanifest-Designer](media/vs-appxmanifest-editor-acurs.png)  

<span data-ttu-id="c625c-226">Sie können auch den unformatierten XML-Code ihres Manifests anzeigen, indem Sie `package.appxmanifest` im Visual Studio-Projektmappen-Explorer mit der rechten Maustaste auf die Datei klicken und " **Code anzeigen** \ ( `F7` \)" auswählen.</span><span class="sxs-lookup"><span data-stu-id="c625c-226">You are also able to view the raw XML of your manifest by right-clicking your `package.appxmanifest` file in Visual Studio Solution Explorer and selecting **View Code** \(`F7`\).</span></span>  <span data-ttu-id="c625c-227">Wenn Sie wieder zur Entwurfsansicht wechseln möchten, wählen Sie **Ansicht-Designer** \ ( `Shift` + `F7` \) aus.</span><span class="sxs-lookup"><span data-stu-id="c625c-227">To toggle back to the Designer view, select **View Designer** \(`Shift`+`F7`\).</span></span>  

#### <span data-ttu-id="c625c-228">Deklarationen von App-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c625c-228">App capability declarations</span></span>  

<span data-ttu-id="c625c-229">Wenn Ihre APP programmgesteuerten Zugriff auf Benutzer Ressourcen wie Bilder oder Musik oder auf Geräte wie eine Kamera oder ein Mikrofon benötigt, müssen Sie die entsprechenden [Deklarationen][WindowsUwpPackagingAppCapabilities] für die App-Funktion in Ihre APP-Paket Manifestdatei aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="c625c-229">If your app needs programmatic access to user resources like pictures or music, or to devices like a camera or a microphone, you must include the corresponding [App capability declarations][WindowsUwpPackagingAppCapabilities] in your app package manifest file.</span></span>  <span data-ttu-id="c625c-230">Es gibt drei Kategorien von App Funktionsdeklarationen:</span><span class="sxs-lookup"><span data-stu-id="c625c-230">There are three app capability declaration categories:</span></span>  

*   <span data-ttu-id="c625c-231">[Funktionen zur allgemeinen Verwendung][WindowsUwpPackagingAppCapabilitiesGeneralUse], die auf die meisten allgemeinen App-Szenarien zutreffen.</span><span class="sxs-lookup"><span data-stu-id="c625c-231">[General-use capabilities][WindowsUwpPackagingAppCapabilitiesGeneralUse] that apply to most common app scenarios.</span></span>  
*   <span data-ttu-id="c625c-232">[Gerätefunktionen][WindowsUwpPackagingAppCapabilitiesDevice], die Ihrer App den Zugriff auf Peripheriegeräte und interne Geräte ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c625c-232">[Device capabilities][WindowsUwpPackagingAppCapabilitiesDevice] that allow your app to access peripheral and internal devices.</span></span>  
*   <span data-ttu-id="c625c-233">[Funktionen zur Sondernutzung][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] , die Unternehmensszenarien unterstützen und ein Microsoft Store-Unternehmenskonto erfordern.</span><span class="sxs-lookup"><span data-stu-id="c625c-233">[Special-use capabilities][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] that support enterprise scenarios and require a Microsoft Store company account.</span></span>  <span data-ttu-id="c625c-234">Weitere Informationen zu Unternehmenskonten finden Sie unter [Kontotypen, Standorte und Gebühren][WindowsUwpPublishAccountTypesLocationsFees].</span><span class="sxs-lookup"><span data-stu-id="c625c-234">For more info about company accounts, see [Account types, locations, and fees][WindowsUwpPublishAccountTypesLocationsFees].</span></span>

<span data-ttu-id="c625c-235">Auf der Microsoft Store-App-Seite werden alle Funktionen aufgeführt, die Sie in Ihrem App-Paketmanifest deklarieren, daher müssen Sie unbedingt nur die Funktionen angeben, die Ihre APP tatsächlich verwendet.</span><span class="sxs-lookup"><span data-stu-id="c625c-235">Your Microsoft Store app page lists all the capabilities you declare in your app package manifest, so be sure to only specify the capabilities that your app actually uses.</span></span>

<span data-ttu-id="c625c-236">Einige Funktionen bieten apps Zugriff auf vertrauliche Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c625c-236">Some capabilities provide apps access to sensitive resources.</span></span>  <span data-ttu-id="c625c-237">Diese Ressourcen gelten als vertraulich, weil jede Person auf die persönlichen Daten des Benutzers zugreifen oder dem Nutzer Geld kosten kann.</span><span class="sxs-lookup"><span data-stu-id="c625c-237">These resources are considered sensitive because each is able to access the user's personal data or cost the user money.</span></span>  <span data-ttu-id="c625c-238">Mit den Datenschutzeinstellungen, die von der Windows 10- [Einstellungs][BingResultsWindows10Settings] -App verwaltet werden, können Benutzer den Zugriff auf vertrauliche Ressourcen dynamisch steuern.</span><span class="sxs-lookup"><span data-stu-id="c625c-238">Privacy settings, managed by the Windows 10 [Settings][BingResultsWindows10Settings] app, let the user dynamically control access to sensitive resources.</span></span>  <span data-ttu-id="c625c-239">Daher ist es wichtig, dass Ihre APP nicht davon ausgeht, dass eine vertrauliche Ressource immer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c625c-239">Thus, it is important that your app does not assume a sensitive resource is always available.</span></span>  <span data-ttu-id="c625c-240">Weitere Informationen zum Zugriff auf sensible Ressourcen finden Sie unter [Richtlinien für Apps mit Berücksichtigung von Datenschutz][WindowsUwp|::ref2::|Index].</span><span class="sxs-lookup"><span data-stu-id="c625c-240">For more info about accessing sensitive resources, see [Guidelines for privacy-aware apps][WindowsUwp|::ref2::|Index].</span></span>  

<span data-ttu-id="c625c-241">Sie fordern Zugriff an, indem Sie Funktionen im Paketmanifest für Ihre APP deklarieren.</span><span class="sxs-lookup"><span data-stu-id="c625c-241">You request access by declaring capabilities in the package manifest for your app.</span></span>  <span data-ttu-id="c625c-242">In Visual Studio können Sie dies über den Bereich " **Funktionen** " des Package. appxmanifest-Designers tun.</span><span class="sxs-lookup"><span data-stu-id="c625c-242">In Visual Studio, you are able to do this from the **Capabilities** panel of the package.appxmanifest designer.</span></span>  

![Bereich "Funktionen" im Visual Studio-appxmanifest-Designer](media/vs-appxmanifest-editor-capabilities.png)  

<span data-ttu-id="c625c-244">In diesem Lernprogramm ist nur die standardmäßige Internet-Funktion \ (Client \) erforderlich, daher ist keine weitere Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c625c-244">In this tutorial, only the default Internet \(Client\) capability is required, so no further action is needed.</span></span>  

### <span data-ttu-id="c625c-245">Verwenden der Feature-Erkennung zum Aufrufen von WinRT</span><span class="sxs-lookup"><span data-stu-id="c625c-245">Use feature detection to invoke WinRT</span></span>  

<span data-ttu-id="c625c-246">Damit Sie für Ihre PWA-Zielgruppe auf allen Plattformen eine qualitativ hochwertige Baseline erzielen können, verbessern Sie mit der WinRT-Feature-Erkennung schrittweise ihre PWA-Funktionalität für Windows.</span><span class="sxs-lookup"><span data-stu-id="c625c-246">To ensure a quality baseline experience for your PWA audience across all platforms, you progressively enhance your PWA experience on Windows using WinRT feature detection.</span></span>  <span data-ttu-id="c625c-247">Auf diese Weise können Sie sicherstellen, dass Ihr Windows-spezifischer Code nur in einem Kontext ausgeführt wird, in dem WinRT-APIs verfügbar und anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="c625c-247">This way, you are able to be sure your Windows-specific code is only run in a context where WinRT APIs are available and applicable.</span></span>  

<span data-ttu-id="c625c-248">Die Funktionserkennung kann so einfach sein wie die Suche nach dem `Windows` Objekt \ (dem EntryPoint zum [WinRT-Namespace][UwpApiIndex]\) wie unten:</span><span class="sxs-lookup"><span data-stu-id="c625c-248">Feature detection may be as simple as looking for the `Windows` object \(the entrypoint to the [WinRT namespace][UwpApiIndex]\) as below:</span></span>  

```javascript
if(window.Windows){
    /*Run code that sends Windows API requests */
}
```  

<span data-ttu-id="c625c-249">Da jedoch nicht alle Windows-APIs für alle [Windows 10-Gerätetypen][UwpExtensionSdkDeviceFamiliesOverview]verfügbar sind, ist es im Allgemeinen nützlich, eine spezifischere Funktionserkennung zu verwenden, um den Namespace der API-Anforderung, die Sie senden, weiter zu qualifizieren:</span><span class="sxs-lookup"><span data-stu-id="c625c-249">However, given that not all Windows APIs are available on all [Windows 10 device types][UwpExtensionSdkDeviceFamiliesOverview], it is generally useful to use more specific feature detection to further qualify the namespace of the API request you are sending:</span></span>  

```javascript
if(window.Windows && Windows.Media.SpeechRecognition){
    /*Run code that sends Windows API requests */
}
```  

<span data-ttu-id="c625c-250">Mit diesem Hintergrund können Sie einige WinRT-Code hinzufügen, um ein benutzerdefiniertes Kontextmenü zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="c625c-250">With that background, you are ready to add some WinRT code to implement a custom context menu.</span></span>  <span data-ttu-id="c625c-251">Wenn Sie das Beispiel PWA aus [Erste Schritte mit Progressive Web Apps][PwaGetStarted]verwenden:</span><span class="sxs-lookup"><span data-stu-id="c625c-251">If you are using the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted]:</span></span>

1.  <span data-ttu-id="c625c-252">Öffnen Sie Visual Studio für Ihr PWA-Websiteprojekt.</span><span class="sxs-lookup"><span data-stu-id="c625c-252">Open Visual Studio to your PWA site project.</span></span>

1.  <span data-ttu-id="c625c-253">Öffnen Sie im Projektmappen-Explorer die `views\layout.pug` Datei, und fügen Sie die folgende Zeile direkt unter dem `script` Verweis für Ihren Dienstmitarbeiter hinzu:</span><span class="sxs-lookup"><span data-stu-id="c625c-253">In Solution Explorer, open the `views\layout.pug` file and add the following line, right below the `script` reference for your service worker:</span></span>
    
    ```xml
    script(src='/javascripts/site.js')
    ```  

1.  <span data-ttu-id="c625c-254">Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf den `javascripts` Ordner, und **fügen**Sie  >  **neue Datei hinzu.**</span><span class="sxs-lookup"><span data-stu-id="c625c-254">In Solution Explorer, right-click on the `javascripts` folder and **Add** > **New File...**.</span></span>

1.  <span data-ttu-id="c625c-255">Benennen Sie Ihre Datei: `site.js` , und kopieren Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="c625c-255">Name your file: `site.js`, and copy in the following code:</span></span>
    
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

1.  <span data-ttu-id="c625c-256">Vergleichen Sie das Verhalten des Kontextmenüs, wenn Sie Ihre PWA im Browser ausführen \ ( `F5` aus dem PWA-Websiteprojekt \) versus im Windows-App-Fenster \ ( `F5` aus ihrem universellen Windows-App-Projekt \).</span><span class="sxs-lookup"><span data-stu-id="c625c-256">Compare the context menu behavior when you run your PWA in the browser \(`F5` from your PWA site project\) versus from inside the Windows app window \(`F5` from your Universal Windows app project\).</span></span>  <span data-ttu-id="c625c-257">Klicken Sie im Browser mit der rechten Maustaste auf das Standardkontextmenü von Microsoft Edge, während während des `WWAHost.exe` Prozesses das benutzerdefinierte Menü nun angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c625c-257">In the browser, right-clicking gives you the Microsoft Edge default context menu, whereas in the `WWAHost.exe` process, your custom menu now appears.</span></span>  

    | <span data-ttu-id="c625c-258">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c625c-258">Microsoft Edge</span></span> | <span data-ttu-id="c625c-259">Windows 10-App</span><span class="sxs-lookup"><span data-stu-id="c625c-259">Windows 10 app</span></span> |  
    |:--- |:---- |  
    | ![Browser-Standardkontextmenü](media/browser-context-menu.png) | ![Benutzerdefiniertes App-Kontextmenü](media/app-context-menu.png) |  

<span data-ttu-id="c625c-262">Wir hoffen, dass Sie jetzt ein solides Fundament haben, um Ihre PWAs unter Windows schrittweise zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="c625c-262">Hopefully you now have a solid foundation for progressively enhancing your PWAs on Windows.</span></span>  <span data-ttu-id="c625c-263">Wenn Sie auf Fragen stoßen oder etwas unklar ist, senden Sie uns bitte einen Kommentar!</span><span class="sxs-lookup"><span data-stu-id="c625c-263">If you run into questions or anything is unclear, please send a comment!</span></span>  

## <span data-ttu-id="c625c-264">Vertiefung</span><span class="sxs-lookup"><span data-stu-id="c625c-264">Going further</span></span>

<span data-ttu-id="c625c-265">Das [Windows dev Center][MicrosoftDeveloperWindowsApps] ist Ihre vollständige Referenz für alle Phasen des Windows-App-Aufbaus, von den [ersten Schritten][MicrosoftDeveloperWindowsAppsGetStarted]bis zum [entwerfen][MicrosoftDeveloperWindowsAppsDesign], [entwickeln][MicrosoftDeveloperWindowsAppsDevelop]und [veröffentlichen][MicrosoftDeveloperStorePublishApps] im Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="c625c-265">The [Windows Dev Center][MicrosoftDeveloperWindowsApps] is your complete reference for all stages of Windows app building, from [getting started][MicrosoftDeveloperWindowsAppsGetStarted], to [designing][MicrosoftDeveloperWindowsAppsDesign], [developing][MicrosoftDeveloperWindowsAppsDevelop], and [publishing][MicrosoftDeveloperStorePublishApps] to the Microsoft Store.</span></span>  

<span data-ttu-id="c625c-266">Eine allgemeine Übersicht über die universelle Windows-Plattform \ (UWP \) und wie Sie auf unterschiedliche Windows 10-Gerätefamilien abzielen, finden Sie unter [Einführung in die universelle Windows-Plattform][WindowsUWPGetStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="c625c-266">For a general overview on the Universal Windows Platform \(UWP\) and how to target different Windows 10 device families, see [Intro to the Universal Windows Platform][WindowsUWPGetStartedGuide].</span></span>  

<span data-ttu-id="c625c-267">Und wenn Sie fertig sind, gehen Sie wie folgt vor, um [Ihre PWA an den Microsoft Store](./microsoft-store.md)zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="c625c-267">And when you are ready, here is how \(and why!\) to [Submit your PWA to the Microsoft Store](./microsoft-store.md).</span></span>  

<!-- image links -->  

<!-- links -->  

[PwaGetStarted]: ./get-started.md "Erste Schritte mit Progressive Web-Apps"  
[PwaIndexWindows10]: ./index.md#pwas-on-windows-10-edgehtml "PWAs unter Windows 10 (EdgeHTML) – Progressive Web-Apps unter Windows"  
[DevToolsGuide]: ../devtools-guide.md "Microsoft Edge (EdgeHTML)-Entwickler Tools"  
[DevToolsGuideMicrosoftStoreApp]: ../devtools-guide.md#microsoft-store-app "Microsoft Store-App – Microsoft Edge (EdgeHTML)-Entwickler Tools"  
[DevToolsGuideServiceWorkers]: ../devtools-guide/service-workers.md "Dienstmitarbeiter"  
[DevToolsProtocol01ClientsEdgePreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge devtools Preview – devtools-Protokoll Clients"  
[DevGuideWhatsNew]: ../dev-guide/whats-new.md "Neuerungen in EdgeHTML"  
[WindowsRuntime]: ../windows-runtime/index.md "Windows-Runtime (WinRT) für JavaScript"  
[WindowRuntimeUsingJavascript]: ../windows-runtime/using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript"  

[ScriptingJsinrtHandlingWinRTEvents]: /scripting/jswinrt/handling-windows-runtime-events-in-javascript "Behandeln von Windows-Runtime-Ereignissen in JavaScript"  
[ScriptingJsinrtUsingWinRT]: /scripting/jswinrt/using-windows-runtime-asynchronous-methods "Verwenden von asynchronen Windows-Runtime-Methoden"  
[ScriptingJsinrtUsingWinRTCasingConventions]:  /scripting/jswinrt/using-the-windows-runtime-in-javascript#casing-conventions-with-windows-runtime-features "Konventionen für die Groß-/Kleinschreibung mit Windows-Runtime-Features – verwenden der Windows-Runtime in JavaScript"  
[UwpApiIndex]: /uwp/api/index "Windows UWP-Namespaces"  
[UwpApiWindowsUiPopups]: /uwp/api/windows.ui.popups "Windows. UI. Popups-Namespace"  
[UwpApiWindowsUiWebuiWebapplicationActivated]: /uwp/api/windows.ui.webui.webuiapplication.activated "WebUIApplication. Activated-Ereignis"  
[UwpExtensionSdkDeviceFamiliesOverview]: /uwp/extension-sdks/device-families-overview "Übersicht über Gerätefamilien"  
[UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest]: /uwp/schemas/appxpackage/uapmanifestschema/generate-package-manifest "So generiert Visual Studio ein App-Paketmanifest"  
[WindowsUWPIndex]: /windows/uwp/index "Dokumentation zur universellen Windows-Plattform"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide "Was ist eine APP für die universelle Windows-Plattform (UWP)?"  
[WindowsUWPGetStartedEnable]: /windows/uwp/get-started/enable-your-device-for-development "Aktivieren Ihres Geräts für die Entwicklung"  
[WindowsUwpSecurityIndex]: /windows/uwp/security/index "Sicherheits"  
[WindowsUwpPublishAccountTypesLocationsFees]: /windows/uwp/publish/account-types-locations-and-fees "Kontotypen, Standorte und Gebühren"  
[WindowsUwpPackagingAppCapabilitiesSpecialRestricted]: /windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities "Eingeschränkte Funktionen"  
[WindowsUwpPackagingAppCapabilitiesDevice]: /windows/uwp/packaging/app-capability-declarations#device-capabilities "Gerätefunktionen"  
[WindowsUwpPackagingAppCapabilitiesGeneralUse]: /windows/uwp/packaging/app-capability-declarations#general-use-capabilities "Funktionen zur allgemeinen Nutzung"  
[WindowsUwpPackagingAppCapabilities]: /windows/uwp/packaging/app-capability-declarations "App-Funktionsdeklarationen"  

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

---
description: Dieser Leitfaden enthält eine Übersicht über die Grundlagen und Tools von PWA für das Erstellen von progressiven Web-Apps unter Windows.
title: Erste Schritte mit Progressive Web-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Progressive Web-Apps, PWA, Edge, Windows, PWABuilder, Web-Manifest, Service Worker, Push
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9a76399616ab7645b82242b94dd4757b73b37f60
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233572"
---
# <span data-ttu-id="32384-104">Erste Schritte mit Progressive Web-Apps</span><span class="sxs-lookup"><span data-stu-id="32384-104">Get started with Progressive Web Apps</span></span>  

<span data-ttu-id="32384-105">Progressive Web-Apps \ (PWAs \) sind einfach Webanwendungen, die mit systemeigenen App-ähnlichen Features auf unterstützenden Plattformen und Browser Modulen, wie Start-from-Homescreen-Installation, Offline-Unterstützung und Push-Benachrichtigungen, [zunehmend verbessert][WikiProgressiveEnhancement] werden.</span><span class="sxs-lookup"><span data-stu-id="32384-105">Progressive Web Apps \(PWAs\) are simply web apps that are [progressively enhanced][WikiProgressiveEnhancement] with native app-like features on supporting platforms and browser engines, such as launch-from-homescreen installation, offline support, and push notifications.</span></span>  <span data-ttu-id="32384-106">Unter Windows 10 mit dem Microsoft Edge \ (EdgeHTML \)-Modul genießen PWAs den zusätzlichen Vorteil, dass Sie unabhängig vom Browserfenster als [universelle Windows-Plattform][WindowsUwpGetStartedWhat] -apps ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="32384-106">On Windows 10 with the Microsoft Edge \(EdgeHTML\) engine, PWAs enjoy the added advantage of running independently of the browser window as [Universal Windows Platform][WindowsUwpGetStartedWhat] apps.</span></span>  

<span data-ttu-id="32384-107">Dieser Leitfaden bietet Ihnen einen Überblick über die Grundlagen von PWA, indem Sie eine einfache `localhost` Web-App als PWA mit Microsoft Visual Studio und einigen PWA Builder-Dienstprogrammen erstellen.</span><span class="sxs-lookup"><span data-stu-id="32384-107">This guide gives you an overview of PWA basics by building a simple `localhost` web app as a PWA using Microsoft Visual Studio and some PWA Builder utilities.</span></span>  <span data-ttu-id="32384-108">Das fertige Produkt funktioniert ähnlich in jedem Browser, der PWAs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32384-108">The finished product works similarly across any browser that supports PWAs.</span></span>  

> [!TIP]
> <span data-ttu-id="32384-109">Wenn Sie eine vorhandene Website schnell in eine PWA-Datei konvertieren und für Windows 10 und andere APP-Plattformen verpacken möchten, überprüfen Sie den [PWA-Generator][PwaBuilder].</span><span class="sxs-lookup"><span data-stu-id="32384-109">For a quick way to convert an existing site to a PWA and package it for Windows 10 and other app platforms, review [PWA Builder][PwaBuilder].</span></span>  

## <span data-ttu-id="32384-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="32384-110">Prerequisites</span></span>  

<span data-ttu-id="32384-111">Sie können PWAs mit jeder Webentwicklungs-IDE erstellen.</span><span class="sxs-lookup"><span data-stu-id="32384-111">You may build PWAs with any web development IDE.</span></span>  <span data-ttu-id="32384-112">Im folgenden finden Sie nur die Voraussetzungen für diesen Leitfaden, der Sie durch die Unterstützung von PWA-Tools im Windows Developer-Ökosystem führt.</span><span class="sxs-lookup"><span data-stu-id="32384-112">The following are only prerequisites for this guide, which walks you through PWA tooling support in the Windows developer ecosystem.</span></span>  

*   <span data-ttu-id="32384-113">Laden Sie die \ (Free \) [Visual Studio Community 2017][VisualStudioDownloads].</span><span class="sxs-lookup"><span data-stu-id="32384-113">Download the \(free\) [Visual Studio Community 2017][VisualStudioDownloads].</span></span>  <span data-ttu-id="32384-114">Sie können auch die Editionen Professional, Enterprise oder [Preview][VisualStudioPreview] verwenden.</span><span class="sxs-lookup"><span data-stu-id="32384-114">You may also use the Professional, Enterprise, or [Preview][VisualStudioPreview] editions.</span></span>  <span data-ttu-id="32384-115">Wählen Sie im Visual Studio-Installationsprogramm die folgenden Arbeitsauslastungen aus.</span><span class="sxs-lookup"><span data-stu-id="32384-115">From the Visual Studio Installer, choose the following Workloads.</span></span>  
    
    *   **<span data-ttu-id="32384-116">Entwicklung der universellen Windows-Plattform</span><span class="sxs-lookup"><span data-stu-id="32384-116">Universal Windows Platform development</span></span>**  
    *   **<span data-ttu-id="32384-117">Node.js Entwicklung</span><span class="sxs-lookup"><span data-stu-id="32384-117">Node.js development</span></span>**  

## <span data-ttu-id="32384-118">Einrichten einer einfachen Web-App</span><span class="sxs-lookup"><span data-stu-id="32384-118">Set up a basic web app</span></span>  

<span data-ttu-id="32384-119">Verwenden Sie aus Gründen der Einfachheit die Visual Studio [Node.js-und Express-App][VisualStudioNodeJsTutorial] -Vorlage, um `localhost` Web-App zu erstellen, die eine `index.html` Seite bedient.</span><span class="sxs-lookup"><span data-stu-id="32384-119">For the sake of simplicity, use the Visual Studio [Node.js and Express app][VisualStudioNodeJsTutorial] template to create `localhost` web app that serves up an `index.html` page.</span></span>  <span data-ttu-id="32384-120">Stellen Sie sich dies als Platzhalter für die überzeugend umfassende Web-App vor, die Sie als PWA entwickeln.</span><span class="sxs-lookup"><span data-stu-id="32384-120">Imagine this as a placeholder for the compelling, full-featured web app that you are developing as a PWA.</span></span>  

1.  <span data-ttu-id="32384-121">Starten Sie Visual Studio, und starten Sie ein neues Projekt.</span><span class="sxs-lookup"><span data-stu-id="32384-121">Launch Visual Studio, and start a new project.</span></span>  
    *   <span data-ttu-id="32384-122">**Datei**  >  **Neu**  >  **Project...**</span><span class="sxs-lookup"><span data-stu-id="32384-122">**File** > **New** > **Project...**</span></span>  
    *   `Ctrl`+`Shift`+`N`  
1.  <span data-ttu-id="32384-123">Wählen Sie unter **JavaScript**die Option **Basic Node.js Express 4-Anwendung**aus.</span><span class="sxs-lookup"><span data-stu-id="32384-123">Under **JavaScript**, select **Basic Node.js Express 4 Application**.</span></span>  <span data-ttu-id="32384-124">Geben Sie den Namen und den Speicherort ein, und wählen Sie **OK**aus.</span><span class="sxs-lookup"><span data-stu-id="32384-124">Set the name and location and choose **OK**.</span></span>  
    
    ![Auswählen der Projektvorlage "Node.js Express 4" in Visual Studio][ImageVsNodejsExpressTemplate]  
    
1.  <span data-ttu-id="32384-126">Nachdem das neue Projekt geladen wurde, wählen Sie **Build** \ ( `Ctrl` + `Shift` + `B` \) aus, und starten Sie das **Debuggen** `F5` .</span><span class="sxs-lookup"><span data-stu-id="32384-126">Once your new project loads, choose **Build** \(`Ctrl`+`Shift`+`B`\) and **Start Debugging** \(`F5`\).</span></span>  <span data-ttu-id="32384-127">Überprüfen Sie, ob die `index.html` Datei beim Durchsuchen geladen wird `http://localhost:1337` .</span><span class="sxs-lookup"><span data-stu-id="32384-127">Verify that your `index.html` file loads when you browse to `http://localhost:1337`.</span></span>  
    
    ![Ausführen der neuen Website auf localhost][ImageVsNodejsExpressIndex]  

## <span data-ttu-id="32384-129">Umwandeln Ihrer APP in eine PWA</span><span class="sxs-lookup"><span data-stu-id="32384-129">Turn your app into a PWA</span></span>  

<span data-ttu-id="32384-130">Jetzt ist es an der Zeit, die Grund [Legenden PWA-Anforderungen][PwaEdgehtmlIndexRequirements] für Ihre Web-App zu *vernetzen: ein Web App-Manifest*, *https* und *Dienstmitarbeiter*.</span><span class="sxs-lookup"><span data-stu-id="32384-130">Now it is time to wire up the basic [PWA requirements][PwaEdgehtmlIndexRequirements] for your web app: a *Web App Manifest*, *HTTPS* and *Service Workers*.</span></span>  

### <span data-ttu-id="32384-131">Web App-Manifest</span><span class="sxs-lookup"><span data-stu-id="32384-131">Web App Manifest</span></span>  

<span data-ttu-id="32384-132">Bei einem [Web App-Manifest][MDNWebAppManifest] handelt es sich um eine JSON-Metadatendatei, die Ihre APP beschreibt, einschließlich Name, Autor, Eintrags Seiten-URL und einem oder mehreren Symbolen.</span><span class="sxs-lookup"><span data-stu-id="32384-132">A [Web App Manifest][MDNWebAppManifest] is a JSON metadata file describing your app, including the name, author, entry page URL, and one or more icons.</span></span>  <span data-ttu-id="32384-133">Da es sich um ein [standardbasiertes Schema][W3cWebAppManifest]handelt, müssen Sie nur ein einzelnes Web App-Manifest für die PWA-Datei bereitstellen, die Sie auf einer beliebigen Plattform-, Betriebssystem-und Gerätekombination installieren, die PWAs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32384-133">Because it follows a [standards-based schema][W3cWebAppManifest], you must only supply a single web app manifest for the PWA that you are installing on any platform, OS, and device combination that supports PWAs.</span></span>  <span data-ttu-id="32384-134">Im Windows-Ökosystem signalisiert Ihr Web App-Manifest dem Bing Web-Indexer, dass Ihre PWA ein Kandidat für die automatische Inklusion in den [Microsoft Store][PwaEdgehtmlMicrosoftStore]ist, wo Sie fast 700 Millionen aktive monatliche Benutzer als Windows 10-App erreichen kann.</span><span class="sxs-lookup"><span data-stu-id="32384-134">In the Windows ecosystem, your web app manifest signals to the Bing web indexer that your PWA is a candidate for automatic inclusion in the [Microsoft Store][PwaEdgehtmlMicrosoftStore], where it may reach nearly 700 million active monthly users as a Windows 10 app.</span></span>  

<span data-ttu-id="32384-135">Wenn es sich um eine vorhandene Live Website handelt, können Sie ein Web App-Manifest mit dem [PWA-Generator][PwaBuilder]generieren.</span><span class="sxs-lookup"><span data-stu-id="32384-135">If this were an existing live site, you may generate a web app manifest using [PWA Builder][PwaBuilder].</span></span>  <span data-ttu-id="32384-136">Da es sich immer noch um ein unveröffentlichtes Projekt handelt, kopieren Sie ein Beispiel Manifest.</span><span class="sxs-lookup"><span data-stu-id="32384-136">Since it is still an unpublished project, copy a sample manifest.</span></span>  

1.  <span data-ttu-id="32384-137">Klicken Sie im Visual Studio- *Projektmappen-Explorer*mit der rechten Maustaste auf den *öffentlichen* Ordner, und wählen Sie neue Datei **Hinzufügen**  >  **...** aus, wobei Sie `manifest.json` den Namen des Elements angeben.</span><span class="sxs-lookup"><span data-stu-id="32384-137">In the Visual Studio *Solution Explorer*, right-click the *public* folder and select **Add** > **New File...**, specifying `manifest.json` as the item name.</span></span>  
1.  <span data-ttu-id="32384-138">Kopieren Sie `manifest.json` den folgenden Code in der Datei.</span><span class="sxs-lookup"><span data-stu-id="32384-138">In the `manifest.json` file, copy the following code.</span></span>  

    ```json
    {
        "dir": "ltr",
        "lang": "en-us",
        "name": "My Sample PWA",
        "scope": "/",
        "display": "browser",
        "start_url": "https://PLACEHOLDER-FOR-PWA-URL",
        "short_name": "SamplePWA",
        "theme_color": "transparent",
        "description": "A sample PWA for testing purposes",
        "orientation": "any",
        "background_color": "transparent",
        "related_applications": [],
        "prefer_related_applications": false,
        "icons": []
    }
    ```  
    
    <span data-ttu-id="32384-139">In einer echten PWA besteht der nächste Schritt darin, *Namen*, *start_url*, *SHORT_NAME*, *Beschreibung*und *Symbole* anzupassen \ (im nächsten Schritt werden die Symbole behandelt).</span><span class="sxs-lookup"><span data-stu-id="32384-139">In a real PWA, the next step is to customize *name*, *start_url*, *short_name*, *description*, and *icons* \(icons are covered in the next step\).</span></span>  
    
    <span data-ttu-id="32384-140">Weitere Informationen zu den verschiedenen Mitglieds Werten und zugehörigen Zwecken finden Sie im [Web App-Manifest-][MDNWebAppManifest] Referenz.</span><span class="sxs-lookup"><span data-stu-id="32384-140">To learn more about the different member values and associated purposes, see the [Web App Manifest][MDNWebAppManifest] reference.</span></span>  
    
1.  <span data-ttu-id="32384-141">Als nächstes füllen Sie das leere `icons` Array mit tatsächlichen Bildpfaden mithilfe des PWA Builder App-Bild Generators aus.</span><span class="sxs-lookup"><span data-stu-id="32384-141">Next, fill in the empty `icons` array with actual image paths by using the PWA Builder App Image Generator.</span></span>  
    
    1.  <span data-ttu-id="32384-142">Laden Sie dieses [Beispiel 512x512 PWA-Bild][ImagePwa]mithilfe eines Webbrowsers herunter.</span><span class="sxs-lookup"><span data-stu-id="32384-142">Using a web browser, download this [sample 512x512 PWA image][ImagePwa].</span></span>  
    1.  <span data-ttu-id="32384-143">Wechseln Sie zum [Bild Generator][PwaBuilderAppImageGenerator]der PWA Builder-APP, und wählen Sie das Bild aus, das `pwa.png` Sie gerade als **Eingabebild** gespeichert haben, und wählen Sie dann die Schaltfläche **herunterladen** aus.</span><span class="sxs-lookup"><span data-stu-id="32384-143">Go to the PWA Builder [App Image Generator][PwaBuilderAppImageGenerator], and select the `pwa.png` image you just saved as the **Input Image** and then choose the **Download** button.</span></span>  
    1.  <span data-ttu-id="32384-144">**Öffnen** und **extrahieren** Sie die ZIP-Datei.</span><span class="sxs-lookup"><span data-stu-id="32384-144">**Open** and **Extract** the zip file.</span></span>  
    1.  <span data-ttu-id="32384-145">Klicken Sie im Visual Studio-Projektmappen-Explorer mit der rechten Maustaste auf den `public` Ordner, und öffnen Sie den **Ordner im Datei-Explorer**.</span><span class="sxs-lookup"><span data-stu-id="32384-145">In the Visual Studio Solution Explorer, right-click the `public` folder and **Open Folder in File Explorer**.</span></span>  <span data-ttu-id="32384-146">Erstellen Sie einen **neuen Ordner** mit dem Namen `images` .</span><span class="sxs-lookup"><span data-stu-id="32384-146">Create a **New folder** named `images`.</span></span>  
    1.  <span data-ttu-id="32384-147">Kopieren Sie alle Plattformordner \ ( `android` ,, usw `chrome` `windows10` . \) aus dem extrahierten zip in den `images` Ordner, und schließen Sie das Fenster "Datei-Explorer".</span><span class="sxs-lookup"><span data-stu-id="32384-147">Copy all of the platform folders \(`android`, `chrome`, `windows10`, and so on\) from your extracted zip to the `images` folder and close the file explorer window.</span></span>  <span data-ttu-id="32384-148">Fügen Sie die Ordner Ihrem Visual Studio-Projekt hinzu (Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf `images` Ordner, und wählen Sie vorhandenen Ordner **Hinzufügen**  >  **...** für jeden der Ordner \) aus.</span><span class="sxs-lookup"><span data-stu-id="32384-148">Add the folders to your Visual Studio project \(in Solution Explorer, right-click `images` folder and select **Add** > **Existing folder...** for each of the folders\).</span></span>  
    1.  <span data-ttu-id="32384-149">Öffnen Sie die Datei aus dem extrahierten ZIP-Datei (mit Visual Studio oder einem beliebigen Editor) `icons.json` , und kopieren `"icons": [...]` Sie das Array in die `manifest.json` Datei Ihres Projekts.</span><span class="sxs-lookup"><span data-stu-id="32384-149">Open \(with Visual Studio or any editor\) the `icons.json` file from the extracted zip and copy the `"icons": [...]` array into the `manifest.json` file of your project.</span></span>  

1.  <span data-ttu-id="32384-150">Nun müssen Sie Ihr Web App-Manifest mit Ihrer APP verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="32384-150">Now you must associate your web app manifest with your app.</span></span>  <span data-ttu-id="32384-151">Öffnen `layout.pug` Sie die Datei \ (in `views` Ordner \) für die Bearbeitung, und fügen Sie diese Zeile direkt hinter dem Stylesheet-Link hinzu.</span><span class="sxs-lookup"><span data-stu-id="32384-151">Open the `layout.pug` file \(in `views` folder\) for editing, and add this line right after the stylesheet link.</span></span>  <span data-ttu-id="32384-152">\ (Es handelt sich einfach um die Kurzform für den Knoten [Mops][PugAttributes] für `<link rel='manifest' href='/manifest.json'>` \).</span><span class="sxs-lookup"><span data-stu-id="32384-152">\(It is simply the Node [pug][PugAttributes] template shorthand for `<link rel='manifest' href='/manifest.json'>`\).</span></span>  
    
    ```html
    link(rel='manifest', href='/manifest.json')
    ```  
    
<span data-ttu-id="32384-153">Mit all dem, was an Ort und Stelle ist, dient Ihre Web-App nun einer Manifesten und Homescreen-fähigen APP-Ikone!</span><span class="sxs-lookup"><span data-stu-id="32384-153">With all that in place, your web app is now serving up a manifest and homescreen-ready app icons!</span></span>  <span data-ttu-id="32384-154">Führen Sie Ihre APP aus `F5` , und laden Sie das Manifest ein.</span><span class="sxs-lookup"><span data-stu-id="32384-154">Try running your app \(`F5`\) and loading up the manifest.</span></span>  

![Web App-Manifest wird von localhost geladen][ImageVsNodejsExpressManifest]  

<span data-ttu-id="32384-156">Und eines ihrer Symbole.</span><span class="sxs-lookup"><span data-stu-id="32384-156">And one of your icons.</span></span>  

![Square71x71Logo-App-Logo wird von localhost geladen][ImageVsNodejsExpressIcon]  

<span data-ttu-id="32384-158">Wenn Sie die APP Live veröffentlichen \ (mit einem tatsächlichen `start_url` \), wird Sie von der Bing-Suchmaschine nun als Kandidat für [das automatische Verpacken und die Übermittlung an den Microsoft Store][PwaEdgehtmlMicrosoftStore] als installierbare Windows 10-App bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="32384-158">If you publish the app live \(with an actual `start_url`\), the Bing search engine now identifies it as a candidate for [automatic packaging and submission to the Microsoft Store][PwaEdgehtmlMicrosoftStore] as an installable Windows 10 app.</span></span>  <span data-ttu-id="32384-159">Stellen Sie sicher, dass Ihre manifest.json [-Datei die Qualitäts Signale für Progressive Web-Apps][WindowsBlogsPwaEdge] enthält, für die Bing Scans einschließlich der folgenden Elemente umfasst.</span><span class="sxs-lookup"><span data-stu-id="32384-159">Ensure that your manifest.json file includes the [Quality signals for Progressive Web Apps][WindowsBlogsPwaEdge] for which Bing scans including the following items.</span></span>   

*   `name`  
*   `description`  
*   <span data-ttu-id="32384-160">Mindestens ein Symbol 512px quadratisch oder größer \ (um sicherzustellen, dass eine Bildquelle mit einer genügenden Auflösung für die automatische Generierung des Begrüßungsbildschirms Ihrer APP, des Store-Eintrags, der Kachel Abbildung usw. angezeigt wird).</span><span class="sxs-lookup"><span data-stu-id="32384-160">At least one icon 512px square or larger \(to ensure an image source of sufficient resolution for auto-generating the splash screen of your app, store listing, tile image, and so on\).</span></span>  

<span data-ttu-id="32384-161">Darüber hinaus können Sie [https](#https), [Servicemitarbeiter](#service-workers)und die [Microsoft Store-Richtlinien][LegalWindowsAgrementsMicrosoftStorePolicies]einhalten.</span><span class="sxs-lookup"><span data-stu-id="32384-161">In addition, use [HTTPS](#https), [service workers](#service-workers), and comply with [Microsoft Store Policies][LegalWindowsAgrementsMicrosoftStorePolicies].</span></span>  

### <span data-ttu-id="32384-162">HTTPS</span><span class="sxs-lookup"><span data-stu-id="32384-162">HTTPS</span></span>  

<span data-ttu-id="32384-163">[Dienstmitarbeiter][MDNServiceWorkerApi] und andere wichtige PWA-Technologien, die mit Servicemitarbeitern arbeiten, wie etwa die [Cache][MDNCache]-, [Push][MDNPushApi]-und [Hintergrund-Synchronisierungs][MDNSyncManager] -APIs, funktionieren nur über sichere Verbindungen, was [https][WikiHttps] für Live-Websites oder `localhost` für Debugging-Zwecke bedeutet.</span><span class="sxs-lookup"><span data-stu-id="32384-163">[Service Workers][MDNServiceWorkerApi] and other key PWA technologies that work with service workers \(such as the [Cache][MDNCache], [Push][MDNPushApi], and [Background Sync][MDNSyncManager] APIs\) only work across secure connections, which means [HTTPS][WikiHttps] for live sites or `localhost` for debugging purposes.</span></span>  

<span data-ttu-id="32384-164">Wenn Sie [diese Web-App als Live Website veröffentlichen][VisualStudioNodejsTutorialPublishAzureAppService] \ (beispielsweisedurch Einrichten eines [Azure Free-Kontos][AzureCreateFreeAccount]\), müssen Sie sicherstellen, dass Ihr Server für HTTPS konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="32384-164">If you [publish this web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService] \(for example, by setting up an [Azure free account][AzureCreateFreeAccount]\), you must ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="32384-165">Wenn Sie den [Microsoft Azure-App-Dienst][AzureWebApps] zum Hosten Ihrer Website verwenden, wird diese standardmäßig über HTTPS bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="32384-165">If you use the [Microsoft Azure App Service][AzureWebApps] to host your site, it is served over HTTPS by default.</span></span>  

<span data-ttu-id="32384-166">Für dieses Handbuch verwenden Sie weiterhin die Verwendung `http://localhost` als Platzhalter für eine Live-Website, die für Sie bereitgestellt wird `https://` .</span><span class="sxs-lookup"><span data-stu-id="32384-166">For this guide, continue using `http://localhost` as a placeholder for a live site served over `https://`.</span></span>  

### <span data-ttu-id="32384-167">Service Workers</span><span class="sxs-lookup"><span data-stu-id="32384-167">Service Workers</span></span>  

<span data-ttu-id="32384-168">Service Mitarbeiter sind die Schlüsseltechnologien hinter PWAs.</span><span class="sxs-lookup"><span data-stu-id="32384-168">Service Workers is the key technology behind PWAs.</span></span> <span data-ttu-id="32384-169">Dienstmitarbeiter fungieren als Proxy zwischen PWA und dem Netzwerk, damit Ihre Website als installierte systemeigene App fungieren kann, die Offlineszenarien bedient, auf Server-Push-Benachrichtigungen reagiert und Hintergrundaufgaben ausführt.</span><span class="sxs-lookup"><span data-stu-id="32384-169">Service Workers act as a proxy between your PWA and the network to enable your website to function as an installed native app that serves up offline scenarios, responds to server push notifications, and runs background tasks.</span></span>  <span data-ttu-id="32384-170">Service Mitarbeiter erschließen auch neue Leistungs Strategien.</span><span class="sxs-lookup"><span data-stu-id="32384-170">Service workers also open up new performance strategies.</span></span>  <span data-ttu-id="32384-171">Sie müssen keine vollständige Web-App implementieren, um den Service Worker-Cache für optimierte Seiten Ladeleistung für Ihre Website zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="32384-171">You are not required to implement a full web app to use the service worker cache for fine-tuned page load performance for your website.</span></span>  

<span data-ttu-id="32384-172">Dienstmitarbeiter sind ereignisgesteuerte Hintergrund Threads, die von JavaScript-Dateien ausgeführt werden, die zusammen mit den regulären Skripts, die Ihre Web-App antreiben, bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="32384-172">Service workers are event-driven background threads that run from JavaScript files served up alongside the regular scripts that power your web app.</span></span>  <span data-ttu-id="32384-173">Da Dienstmitarbeiter nicht auf dem Hauptbenutzeroberflächen Thread ausgeführt werden, verfügen Dienstmitarbeiter nicht über DOM-Zugriff, obwohl der [UI-Thread][MDNWorkerPrototypePostMessage] und ein [Worker-Thread][MDNDedicatedWorkerGlobalScopePostMessage] mithilfe von `postMessage()` und `onmessage` Ereignishandlern kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="32384-173">Because Service workers do not run on the main UI thread, service workers do not have DOM access, though the [UI thread][MDNWorkerPrototypePostMessage] and a [worker thread][MDNDedicatedWorkerGlobalScopePostMessage] is able to communicate using `postMessage()` and `onmessage` event handlers.</span></span>  

<span data-ttu-id="32384-174">Sie ordnen eine Dienstmitarbeiter Ihrer APP zu, indem Sie Sie auf dem URL-Ursprung ihrer Website registrieren \ (oder einem angegebenen Pfad darin \).</span><span class="sxs-lookup"><span data-stu-id="32384-174">You associate a service worker with your app by registering it to the URL origin of your site \(or a specified path within it\).</span></span>  <span data-ttu-id="32384-175">Nach der Registrierung wird die Service Worker-Datei dann auf dem Benutzer Computer heruntergeladen, installiert und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="32384-175">Once registered, the service worker file is then downloaded, installed, and activated on the user machine.</span></span>  <span data-ttu-id="32384-176">Weitere Informationen finden Sie im MDN Web docs-Handbuch mit einer umfassenden Anleitung zur [Verwendung von Servicemitarbeitern][MDNUsingServiceWorkers] und einer detaillierten [Service Worker-API][MDNServiceWorkerApi] -Referenz.</span><span class="sxs-lookup"><span data-stu-id="32384-176">For more, MDN web docs has a comprehensive guide on [Using Service Workers][MDNUsingServiceWorkers] and a detailed [Service Worker API][MDNServiceWorkerApi] reference.</span></span>  

<span data-ttu-id="32384-177">Verwenden Sie für dieses Lernprogramm das Worker-Skript für Offline Seiten Dienst in [PWA Builder][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="32384-177">For this tutorial, use the Offline page service worker script on [PWA Builder][PwaBuilderServiceWorker].</span></span>  <span data-ttu-id="32384-178">Beginnen Sie, indem Sie das Skript mit mehr Funktionalität entsprechend Ihren Leistungsanforderungen, Netzwerkbandbreite usw. anpassen.</span><span class="sxs-lookup"><span data-stu-id="32384-178">Start by customizing the script with more functionality according to your performance requirements, network bandwidth, and so on.</span></span>  <span data-ttu-id="32384-179">Überprüfen Sie das von Mozilla bereitgestellte [Service Worker Cookbook][ServiceWorkerCookbook]  für eine Reihe nützlicher Ideen für die Zwischenspeicherung von Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="32384-179">Review the [Service Worker Cookbook][ServiceWorkerCookbook]  provided by Mozilla for a number of useful service worker caching ideas.</span></span>  

1.  <span data-ttu-id="32384-180">Öffnen Sie [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] den \ (Standard \) **Offline Page** Service Worker, und klicken Sie auf die Schaltfläche **Dienstmitarbeiter herunterladen** .</span><span class="sxs-lookup"><span data-stu-id="32384-180">Open [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] and select the \(default\) **Offline page** service worker and click the **Download service worker** button.</span></span>  
1.  <span data-ttu-id="32384-181">Öffnen Sie den Ordner "Download", und kopieren Sie die beiden folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="32384-181">Open the download folder and copy the following two files</span></span>  

    *   <span data-ttu-id="32384-182">ServiceWorker1\pwabuilder-sw-register.js</span><span class="sxs-lookup"><span data-stu-id="32384-182">ServiceWorker1\pwabuilder-sw-register.js</span></span>  
    *   <span data-ttu-id="32384-183">ServiceWorker1\pwabuilder-sw.js</span><span class="sxs-lookup"><span data-stu-id="32384-183">ServiceWorker1\pwabuilder-sw.js</span></span>  
    
    <span data-ttu-id="32384-184">Speichern Sie die Dateien im `public` Ordner Ihres Visual Studio Web App-Projekts.</span><span class="sxs-lookup"><span data-stu-id="32384-184">Save the files to the `public` folder of your Visual Studio web app project.</span></span>  <span data-ttu-id="32384-185">\ (In Visual Studio können Sie den `Ctrl` + `O` Datei-Explorer in Ihrem Projekt öffnen und zu dem `public` Ordner navigieren \).</span><span class="sxs-lookup"><span data-stu-id="32384-185">\(From Visual Studio, use `Ctrl`+`O` to open file explorer to your project and navigate to the `public` folder\).</span></span>  
    
    <span data-ttu-id="32384-186">Öffnen Sie im Projektmappen-Explorer die `public/pwabuilder-sw.js` Datei, und ändern Sie den Wert von in `offlineFallbackPage` `offline.html` .</span><span class="sxs-lookup"><span data-stu-id="32384-186">In Solution Explorer, open the `public/pwabuilder-sw.js` file, and change the value of `offlineFallbackPage` to `offline.html`.</span></span>  
    
    ```javascript
    const offlineFallbackPage = "offline.html";
    ```
    
    <span data-ttu-id="32384-187">Es lohnt sich, den Code in diesen beiden Dateien zu überprüfen, um zu erfahren, wie ein Dienstmitarbeiter registriert wird, der eine bestimmte Seite zwischenspeichert \ ( `offline.html` \), und wenn ein Netzwerkabruf fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="32384-187">It is worth reviewing the code in both of these files, to get the gist of how to register a service worker that caches a designated page \(`offline.html`\) and serves it when a network fetch fails.</span></span>  <span data-ttu-id="32384-188">Als Nächstes erstellen Sie eine einfache `offline.html` Seite als Platzhalter für die Offlinefunktionen Ihrer APP.</span><span class="sxs-lookup"><span data-stu-id="32384-188">Next, create a simple `offline.html` page as a placeholder for the offline functionality of your app.</span></span>  
    
1.  <span data-ttu-id="32384-189">Öffnen Sie im Projektmappen-Explorer die `views/layout.pug` Datei, und fügen Sie die folgende Zeile unter Ihren Link-Tags hinzu.</span><span class="sxs-lookup"><span data-stu-id="32384-189">In Solution Explorer, open the `views/layout.pug` file, and add the following line below your link tags.</span></span>  
    
    ```html
    script(src='/pwabuilder-sw-register.js' type='module')
    ```  
    
    <span data-ttu-id="32384-190">Ihre Website lädt und führt Ihr Registrierungsskript für Dienstmitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="32384-190">Your site loads and runs your service worker registration script.</span></span>  
    
1.  <span data-ttu-id="32384-191">Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf den `public` Ordner, und wählen Sie \*\*\*\*  >  **neue Datei**hinzufügen aus.  Benennen Sie `offline.html` die Datei, und fügen Sie einen `<title>` und einige Textinhalte hinzu, beispielsweise den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="32384-191">In Solution Explorer, right-click on the `public` folder and select **Add** > **New File...**.  Name it `offline.html`, and add a `<title>` and some body content, for example the following code.</span></span>  
    
    ```html
    <!DOCTYPE html>
    
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title>Offline mode</title>
    </head>
    <body>
        You are now offline.
    </body>
    </html>
    ```  
    
    <span data-ttu-id="32384-192">An diesem Punkt sollte Ihr `public` Ordner über drei neue Dateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="32384-192">At this point, your `public` folder should have three new files.</span></span>  
    
    ![Dateien, die dem öffentlichen Ordner der Projektmappe hinzugefügt wurden][ImageVsNodejsExpressPublic]  
    
1.  <span data-ttu-id="32384-194">Öffnen Sie im Projektmappen-Explorer die `routes\index.js` Datei, und fügen Sie den folgenden Code direkt vor dem letzten Befehl \ ( `module.exports = router;` \) hinzu.</span><span class="sxs-lookup"><span data-stu-id="32384-194">In Solution Explorer, open the `routes\index.js` file, and add the following code just before the final command \(`module.exports = router;`\).</span></span>  
    
    ```javascript
    router.get('/offline.html', function (req, res) {
        res.sendFile('public/offline.html');
    });
    ```  
    
    <span data-ttu-id="32384-195">Dadurch wird Ihre APP angewiesen, die `offline.html` Datei zu bedienen \ (wenn Ihr Dienstmitarbeiter Sie für den Offlinecache abruft \).</span><span class="sxs-lookup"><span data-stu-id="32384-195">This instructs your app to serve the `offline.html` file \(when your service worker fetches it for the offline cache\).</span></span>  
    
1.  <span data-ttu-id="32384-196">Testen Sie Ihre PWA!</span><span class="sxs-lookup"><span data-stu-id="32384-196">Test out your PWA!</span></span>  <span data-ttu-id="32384-197">Erstellen Sie \ ( `Ctrl` + `Shift` + `B` \), und führen `F5` Sie \ (\) Ihre Web-App aus, um Microsoft Edge zu starten und Ihre Seite zu öffnen `localhost` .</span><span class="sxs-lookup"><span data-stu-id="32384-197">Build \(`Ctrl`+`Shift`+`B`\) and Run \(`F5`\) your web app to launch Microsoft Edge and open your `localhost` page.</span></span>  <span data-ttu-id="32384-198">Führen Sie dann die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="32384-198">Then complete the following steps.</span></span>  
    
    1.  <span data-ttu-id="32384-199">Öffnen Sie die Edge \*\*\*\* `Ctrl` + `Shift` + `J` -devtools-Konsole, und überprüfen Sie, ob der Dienstmitarbeiter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="32384-199">Open the Edge DevTools **Console** \(`Ctrl`+`Shift`+`J`\) and verify the Service worker was registered.</span></span>  
    1.  <span data-ttu-id="32384-200">Erweitern Sie im **Debugger** -Panel das **Service Worker** -Steuerelement, und klicken Sie auf ihren Ursprung.</span><span class="sxs-lookup"><span data-stu-id="32384-200">In the **Debugger** panel, expand the **Service Workers** control and click on your origin.</span></span>  <span data-ttu-id="32384-201">Überprüfen Sie in der **Übersicht der Dienstmitarbeiter**, ob Ihr Dienstmitarbeiter aktiviert ist und ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32384-201">In the **Service Worker Overview**, verify your service worker is activated and running.</span></span>  
        
        ![Übersicht über den Edge devtools Service Worker][ImageDevtoolsSwOverview]  
        
    1.  <span data-ttu-id="32384-203">Erweitern Sie das **Cache** -Steuerelement, und überprüfen Sie, ob die `offline.html` Seite zwischengespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="32384-203">Expand the **Cache** control and verify that the `offline.html` page is cached.</span></span>  
        
        ![Edge devtools Service Worker-Cache][ImageDevtoolsSwCache]  
        
1.  <span data-ttu-id="32384-205">Zeit, ihre PWA als offline-app zu testen!</span><span class="sxs-lookup"><span data-stu-id="32384-205">Time to try your PWA as an offline app!</span></span>  <span data-ttu-id="32384-206">Beenden Sie in Visual Studio das **Debuggen** \ ( `Shift` + `F5` \) Ihre Web-App, und öffnen Sie dann Microsoft Edge \ (oder aktualisieren \) an die localhost-Adresse Ihrer Website.</span><span class="sxs-lookup"><span data-stu-id="32384-206">In Visual Studio, **Stop Debugging** \(`Shift`+`F5`\) your web app, then open Microsoft Edge \(or refresh\) to the localhost address of your website.</span></span>  <span data-ttu-id="32384-207">Es sollte nun die `offline.html` Seite laden (Dank ihres Service-Worker-und Offline-Caches \)!</span><span class="sxs-lookup"><span data-stu-id="32384-207">It should now load the `offline.html` page \(thanks to your service worker and offline cache\)!</span></span>  
    
    ![offline.html http://localhost:1337 in Microsoft Edge geladen][ImageOfflineHtml]  

## <span data-ttu-id="32384-209">Hinzufügen von Push-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="32384-209">Add push notifications</span></span>  

<span data-ttu-id="32384-210">Machen Sie Ihre PWA-App-ähnlicher, indem Sie clientseitige Unterstützung für Push-Benachrichtigungen hinzufügen, indem Sie die [Push-API][MDNPushApi] verwenden, um einen Messagingdienst zu abonnieren, und die [Benachrichtigungs-API][MDNNotificationsApi] , um beim Empfang einer Nachricht eine Popupnachricht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="32384-210">Make your PWA more app-like by adding client-side support for push notifications using the [Push API][MDNPushApi] to subscribe to a messaging service and the [Notifications API][MDNNotificationsApi] to display a toast message upon receiving a message.</span></span>  <span data-ttu-id="32384-211">Wie bei Service Mitarbeitern sind dies standardbasierte APIs, die browserübergreifend funktionieren, sodass Sie den Code nur einmal schreiben müssen, damit er überall funktioniert, PWAs unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="32384-211">As with Service Workers, these are standards-based APIs that work cross-browser, so you only have to write the code once for it to work everywhere PWAs are supported.</span></span>  <span data-ttu-id="32384-212">Verwenden Sie auf der Serverseite die Open-Source-Bibliothek [Web-Push][NPMWebPush] , um die Unterschiede bei der Bereitstellung von Push-Nachrichten in verschiedenen Browsern zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="32384-212">On the server side, use the [Web-Push][NPMWebPush] open-source library to handle the differences involved in delivering push messages to various browsers.</span></span>  

<span data-ttu-id="32384-213">Im folgenden wird das Push Rich-Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] von Mozilla angepasst, das für eine Reihe anderer nützlicher Web-Push-und Service-Worker-Rezepte interessant ist.</span><span class="sxs-lookup"><span data-stu-id="32384-213">The following is adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which is worth checking out for a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="32384-214">Schritt 1: Installieren der NPM Web-Push-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="32384-214">Step 1 - Install the NPM web-push library</span></span>  

<span data-ttu-id="32384-215">Klicken Sie im Visual Studio-Projektmappen-Explorer mit der rechten Maustaste auf das Projekt, und **Öffnen Sie Node.js interaktives Fenster**.  Geben Sie den folgenden Code ein.</span><span class="sxs-lookup"><span data-stu-id="32384-215">In Visual Studio Solution Explorer, right-click your project and **Open Node.js Interactive Window...**.  In it, type the following code.</span></span>  

```javascript
.npm install web-push
```  

<span data-ttu-id="32384-216">Dadurch wird die [Web-Push-][NPMWebPush] Bibliothek installiert.</span><span class="sxs-lookup"><span data-stu-id="32384-216">This installs the [Web-Push][NPMWebPush] library.</span></span>  <span data-ttu-id="32384-217">Öffnen Sie dann Ihre `index.js` Datei, und fügen Sie die folgende Zeile oben in der Datei nach den anderen Anforderungs Anweisungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="32384-217">Then, open up your `index.js` file, and add the following line to the top of your file after the other requirement statements.</span></span>  

```javascript
var webpush = require('web-push');
```  

### <span data-ttu-id="32384-218">Schritt 2: Generieren von VAPID-Schlüsseln für Ihren Server</span><span class="sxs-lookup"><span data-stu-id="32384-218">Step 2 - Generate VAPID keys for your server</span></span>  

<span data-ttu-id="32384-219">Als nächstes müssen Sie VAPID \ (freiwillige Application Server Identification \)-Schlüssel für Ihren Server generieren, um Push-Nachrichten an den PWA-Client zu senden.</span><span class="sxs-lookup"><span data-stu-id="32384-219">Next you must generate VAPID \(Voluntary Application Server Identification\) keys for your server to send push messages to the PWA client.</span></span>  <span data-ttu-id="32384-220">Sie müssen dies nur einmal tun \ (das heißt, Ihr Server erfordert nur ein einzelnes Paar VAPID-Schlüssel \).</span><span class="sxs-lookup"><span data-stu-id="32384-220">You only have to do this once \(that is, your server only requires a single pair of VAPID keys\).</span></span>  <span data-ttu-id="32384-221">Geben Sie im interaktiven Node.js Fenster den folgenden Code ein.</span><span class="sxs-lookup"><span data-stu-id="32384-221">In the Node.js Interactive Window, type the following code.</span></span>  

```javascript
var webpush = require('web-push');
webpush.generateVAPIDKeys();
```  

<span data-ttu-id="32384-222">Die Ausgabe sollte zu einem JSON-Objekt führen, das einen öffentlichen und einen privaten Schlüssel enthält, die Sie in Ihre Serverlogik kopieren.</span><span class="sxs-lookup"><span data-stu-id="32384-222">The output should result in a JSON object containing a public and private key, which you copy into your server logic.</span></span>  

<span data-ttu-id="32384-223">`index.js`Fügen Sie in der Datei unmittelbar vor der letzten \ ( `module.exports = router` \)-Zeile den folgenden Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="32384-223">In your `index.js` file, just before the final  \(`module.exports = router`\) line, add the following code.</span></span>  

```javascript
const vapidKeys = {
    publicKey: '',
    privateKey: ''
};

webpush.setVapidDetails(
    'mailto:pwa@example.com',
    vapidKeys.publicKey,
    vapidKeys.privateKey
);
```  

<span data-ttu-id="32384-224">Kopieren `publicKey` Sie die `privateKey` soeben generierten und-Werte.</span><span class="sxs-lookup"><span data-stu-id="32384-224">Copy the `publicKey` and `privateKey` values that you just generated.</span></span>  <span data-ttu-id="32384-225">Gerne können `mailto` Sie auch die Adresse anpassen \ (obwohl dies nicht erforderlich ist, um dieses Beispiel auszuführen \).</span><span class="sxs-lookup"><span data-stu-id="32384-225">Feel free to customize the `mailto` address as well \(though it is not required in order to run this sample\).</span></span>  

<span data-ttu-id="32384-226">Der [Mozilla Services Engineering-Blog][MozillaServicesSendingVapidWebPushNotificationsPush] hat einen netten Explainer auf VAPID und webpush, wenn Sie an den Details darüber interessiert sind, wie es hinter den Kulissen funktioniert.</span><span class="sxs-lookup"><span data-stu-id="32384-226">The [Mozilla Services engineering blog][MozillaServicesSendingVapidWebPushNotificationsPush] has a nice explainer on VAPID and WebPush if you are interested in the details of how it works behind the scenes.</span></span>  

### <span data-ttu-id="32384-227">Schritt 3 – behandeln von Push-bezogenen Server Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32384-227">Step 3 - Handle push-related server requests</span></span>  

<span data-ttu-id="32384-228">Richten Sie nun Routen für die Verarbeitung von Push-bezogenen Anforderungen vom PWA-Client ein, einschließlich der Bereitstellung des öffentlichen VAPID-Schlüssels und der Registrierung des Clients für den Empfang von Pushs.</span><span class="sxs-lookup"><span data-stu-id="32384-228">Now set up routes for handling push-related requests from the PWA client, including serving up the VAPID public key and registering the client to receive pushes.</span></span>  

<span data-ttu-id="32384-229">In einem realen Szenario stammt eine Push-Benachrichtigung wahrscheinlich von einem Ereignis in ihrer Serverlogik.</span><span class="sxs-lookup"><span data-stu-id="32384-229">In a real scenario, a push notification likely originates from an event in your server logic.</span></span>  <span data-ttu-id="32384-230">Um die Dinge hier zu vereinfachen, müssen Sie der PWA-Startseite eine Schaltfläche " **Push-Benachrichtigung** " hinzufügen, um Pushs von unserem Server zu generieren, und einen `/sendNotification` Endpunkt \ (Server Route \) für die Verarbeitung dieser Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="32384-230">To simplify things here, you must add a **Push Notification** button to our PWA homepage for generating pushes from our server, and a `/sendNotification` endpoint \(server route\)for handling those requests.</span></span>  

<span data-ttu-id="32384-231">`index.js`Fügen Sie in Ihrer Datei unmittelbar nach dem VAPID-Initialisierungscode, den Sie in [Schritt 2] [#Step-2---generieren-VAPID-Schlüssel-für-Server] hinzugefügt haben, die folgenden Routen an.</span><span class="sxs-lookup"><span data-stu-id="32384-231">In your `index.js` file, append the following routes just after the VAPID initialization code you added in [Step 2][#step-2---generate-vapid-keys-for-your-server].</span></span>  

```javascript
router.get('/vapidPublicKey', function (req, res) {
    res.send(vapidKeys.publicKey);
});

router.post('/register', function (req, res) {
    // A real world application stores the subscription info.
    res.sendStatus(201);
});

router.post('/sendNotification', function (req, res) {
    const subscription = req.body.subscription;
    const payload = 'payload';
    const options = null;
    
    webpush.sendNotification(subscription, payload, options)
        .then(function () {
            res.sendStatus(201);
        })
        .catch(function (error) {
            res.sendStatus(500);
            console.log(error);
        });
});
```  

<span data-ttu-id="32384-232">Mit dem serverseitigen Code in Kraft, in Push-Benachrichtigungen auf dem PWA-Client.</span><span class="sxs-lookup"><span data-stu-id="32384-232">With the server-side code in place, plumb in push notifications on the PWA client.</span></span>  

### <span data-ttu-id="32384-233">Schritt 4 – Abonnieren von Push-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="32384-233">Step 4 - Subscribe to push notifications</span></span>  

<span data-ttu-id="32384-234">Als Teil ihrer Rolle als PWA-Netzwerk Proxys behandeln Dienstmitarbeiter Push-Ereignisse und Popup Benachrichtigungs Interaktionen.</span><span class="sxs-lookup"><span data-stu-id="32384-234">As part of their role as PWA network proxies, service workers handle push events and toast notification interactions.</span></span>  <span data-ttu-id="32384-235">Wie bei der ersten Einrichtung von \ (oder der Registrierung \) eines Dienst Mitarbeiters, erfolgt die Anmeldung der PWA to Server-Push-Benachrichtigungen im Hauptbenutzeroberflächen Thread der PWA und erfordert eine Netzwerkverbindung.</span><span class="sxs-lookup"><span data-stu-id="32384-235">However, as it is with first setting up \(or registering\) a service worker, subscribing the PWA to server push notifications happens on the main UI thread of the PWA and requires network connectivity.</span></span>  <span data-ttu-id="32384-236">Für das Abonnieren von Push-Benachrichtigungen ist eine Active Service Worker-Registrierung erforderlich, daher müssen Sie zuerst überprüfen, ob Ihr Dienstmitarbeiter installiert und aktiv ist, bevor Sie versuchen, ihn für Push-Benachrichtigungen zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="32384-236">Subscribing to push notifications requires an active service worker registration, so you must first verify that your service worker is installed and active before trying to subscribe it to push notifications.</span></span>  

<span data-ttu-id="32384-237">Bevor ein neues Pushabonnement erstellt wird, überprüfen Sie, ob der Benutzer die PWA-Berechtigung zum Empfangen von Benachrichtigungen gewährt hat.</span><span class="sxs-lookup"><span data-stu-id="32384-237">Before a new push subscription is created, Microsoft Edge check if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="32384-238">Wenn dies nicht der Fall ist, wird der Benutzer vom Browser zur Genehmigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="32384-238">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="32384-239">Wenn die Berechtigung verweigert wird, wird die Anforderung `registration.pushManager.subscribe` ausgelöst `DOMException` , sodass Sie Sie behandeln müssen.</span><span class="sxs-lookup"><span data-stu-id="32384-239">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, so you must handle it.</span></span>  <span data-ttu-id="32384-240">Weitere Informationen zur Berechtigungsverwaltung finden Sie unter [Push-Benachrichtigungen in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="32384-240">For more on permission management, see [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="32384-241">Fügen Sie in der `pwabuilder-sw-register.js` Datei den folgenden Code ein.</span><span class="sxs-lookup"><span data-stu-id="32384-241">In your `pwabuilder-sw-register.js` file, append the following code.</span></span>  

```javascript
// Subscribe this PWA to push notifications from the server
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(async function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                // Otherwise subscribe with the server public key
                const response = await fetch('./vapidPublicKey');
                const vapidPublicKey = await response.text();
                const convertedVapidKey = urlBase64ToUint8Array(vapidPublicKey);
                
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: convertedVapidKey
                });
            });
    }).then(function (subscription) {
        // Send the subscription details to the server
        fetch('./register', {
            method: 'post',
            headers: {
                'Content-type': 'application/json'
            },
            body: JSON.stringify({
                subscription: subscription
            }),
        });
        
        // Create a button to mimic server pushes for testing purposes
        var button = document.createElement('input');
        button.type = 'button';
        button.id = 'notify';
        button.value = 'Send Notification';
        document.body.appendChild(button);
        document.getElementById('notify').addEventListener('click', function () {
            fetch('./sendNotification', {
                method: 'post',
                headers: {
                    'Content-type': 'application/json'
                },
                body: JSON.stringify({
                    subscription: subscription
                }),
            });
        });
    });

// Utility function for browser interoperability
function urlBase64ToUint8Array(base64String) {
    var padding = '='.repeat((4 - base64String.length % 4) % 4);
    var base64 = (base64String + padding)
        .replace(/\-/g, '+')
        .replace(/_/g, '/');
        
    var rawData = window.atob(base64);
    var outputArray = new Uint8Array(rawData.length);
    
    for (var i = 0; i < rawData.length; ++i) {
        outputArray[i] = rawData.charCodeAt(i);
    }
    return outputArray;
}
```  

<span data-ttu-id="32384-242">Lesen Sie die MDN-Dokumentation auf der [pushmanager][MDNPushManager] -Oberfläche und in den NPM-Dokumenten in der [Web-Push-][NPMWebPushUsage] Bibliothek, um weitere Informationen zur Funktionsweise der APIs und verschiedene verwandte Optionen zu finden.</span><span class="sxs-lookup"><span data-stu-id="32384-242">Review the MDN documentation on the [PushManager][MDNPushManager] interface and NPM docs on the [Web-Push][NPMWebPushUsage] library for more details on how the APIs work and various related options.</span></span>  

### <span data-ttu-id="32384-243">Schritt 5 – Einrichten von Push-und notificationclick-Ereignishandlern</span><span class="sxs-lookup"><span data-stu-id="32384-243">Step 5 - Set up push and notificationclick event handlers</span></span>  

<span data-ttu-id="32384-244">Bei der Einrichtung des Push-Abonnements erfolgt der Rest der Arbeit im Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="32384-244">With our push subscription set up, the remainder of the work happens in the service worker.</span></span>  <span data-ttu-id="32384-245">Zunächst müssen Sie einen Handler für vom Server gesendete Push-Ereignisse einrichten und mit einer Popupbenachrichtigung Antworten \ (wenn die Berechtigung erteilt wurde \), die die pushdaten-Nutzlast anzeigt.</span><span class="sxs-lookup"><span data-stu-id="32384-245">First you must set up a handler for server-sent push events, and respond with a toast notification \(if permission was granted\) displaying the push data payload.</span></span>  <span data-ttu-id="32384-246">Als Nächstes fügen Sie einen Click-Handler für den Toast hinzu, um die Benachrichtigung zu schließen und durch eine Liste der derzeit geöffneten Fenster zu sortieren, um die beabsichtigte PWA-Clientseite zu öffnen, zu fokussieren oder zu öffnen und zu fokussieren.</span><span class="sxs-lookup"><span data-stu-id="32384-246">Next you add a click handler for the toast to dismiss the notification and sort through a list of currently open windows to open, focus, or open and focus the intended PWA client page.</span></span>  

<span data-ttu-id="32384-247">Fügen Sie in der `pwabuilder-sw.js` Datei die folgenden Handler ein.</span><span class="sxs-lookup"><span data-stu-id="32384-247">In your `pwabuilder-sw.js` file, append the following handlers.</span></span>  

```javascript
//Respond to a server push with a user notification
self.addEventListener('push', function (event) {
    if ("granted" === Notification.permission) {
        var payload = event.data ? event.data.text() : 'no payload';
        const promiseChain = self.registration.showNotification('Sample PWA', {
            body: payload,
            icon: 'images/windows10/Square44x44Logo.scale-100.png'
        });
        //Ensure the toast notification is displayed before exiting this function
        event.waitUntil(promiseChain);
    }
});
    
//Respond to the user clicking the toast notification
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This looks to see if the current is already open and focuses it
    event.waitUntil(clients.matchAll({
        type: 'window'
    }).then(function (clientList) {
        for (var i = 0; i < clientList.length; i++) {
            var client = clientList[i];
            if (client.url == 'http://localhost:1337/' && 'focus' in client)
                return client.focus();
        }
        if (clients.openWindow)
            return clients.openWindow('/');
    }));
});
```  

### <span data-ttu-id="32384-248">Schritt 6 – probieren Sie es aus</span><span class="sxs-lookup"><span data-stu-id="32384-248">Step 6 - Try it out</span></span>  

<span data-ttu-id="32384-249">Zeit zum Testen von Push-Benachrichtigungen in ihrer PWA!</span><span class="sxs-lookup"><span data-stu-id="32384-249">Time to test push notifications in your PWA!</span></span>  

1.  <span data-ttu-id="32384-250">Führen `F5` Sie im Browser \ (\) PWA aus.</span><span class="sxs-lookup"><span data-stu-id="32384-250">Run \(`F5`\) your PWA in the browser.</span></span>  <span data-ttu-id="32384-251">Da Sie den Service Worker-Code \ ( `pwabuilder-sw.js` \) geändert haben, müssen Sie den devtools-Debugger \ ( `F12` \) im **Service Worker** -Übersichts Panel öffnen und die Registrierung der Dienstmitarbeiter **aufheben** und \ ( `F5` \) die Seite neu laden, um Sie erneut zu registrieren \ (oder klicken Sie auf **Aktualisieren**\).</span><span class="sxs-lookup"><span data-stu-id="32384-251">Because you modified the service worker code \(`pwabuilder-sw.js`\), you must open the DevTools Debugger \(`F12`\) to the **Service Worker Overview** panel and **Unregister** the service worker and reload \(`F5`\) the page to re-register it \(or you click **Update**\).</span></span>  <span data-ttu-id="32384-252">In einem Produktionsszenario überprüft der Browser regelmäßig, ob Updates für Dienstmitarbeiter vorhanden sind, und installiert die Updates im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="32384-252">In a production scenario, the browser checks regularly check for service worker updates and install the updates in the background.</span></span>  <span data-ttu-id="32384-253">Sie sollten Sie hier für sofortige Ergebnisse zwingen.</span><span class="sxs-lookup"><span data-stu-id="32384-253">You should force it here for immediate results.</span></span>  
    
    <span data-ttu-id="32384-254">Wenn Ihr Servicemitarbeiter aktiviert und versucht, ihre PWA-Benachrichtigung für Push-Benachrichtigungen zu abonnieren, wird unten auf der Seite ein Dialogfeld "Berechtigung" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="32384-254">As your service worker activates and attempts to subscribe your PWA to push notifications, you should see a permission dialog at the bottom of the page.</span></span>  
    
    ![Dialogfeld ' Berechtigung ' zum Aktivieren von Benachrichtigungen][ImageNotificationPermission]  
    
    <span data-ttu-id="32384-256">Wählen Sie **Ja** aus, um Popupbenachrichtigungen für Ihre PWA zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="32384-256">Choose **Yes** to enable toast notifications for your PWA.</span></span>  
    
1.  <span data-ttu-id="32384-257">Wählen Sie im Bereich Service Worker Overview die Schaltfläche  **drücken** aus.</span><span class="sxs-lookup"><span data-stu-id="32384-257">From the Service Worker Overview pane, try choosing the  **Push** button.</span></span>  <span data-ttu-id="32384-258">Es sollte eine Popupbenachrichtigung mit der Nutzlast \ (hart codierte "Test Push Message from devtools" \) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="32384-258">A toast notification with the \(hard-coded "Test push message from DevTools"\) payload should appear.</span></span>  
    
    ![Pushen einer Benachrichtigung von devtools][ImageDevtoolsPush]  
    
1.  <span data-ttu-id="32384-260">Wählen Sie als nächstes die Schaltfläche " **Benachrichtigung senden** " auf der Startseite Ihrer PWA aus.</span><span class="sxs-lookup"><span data-stu-id="32384-260">Next try choosing the **Send Notification** button on the homepage of your PWA.</span></span>  <span data-ttu-id="32384-261">Dieses Mal wird ein Toast mit der Nutzlast Ihres Servers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="32384-261">This time a toast with the payload from your server appears.</span></span>  
    
    ![Pushen einer Benachrichtigung vom PWA-Server][ImagePwaPush]  
    
    <span data-ttu-id="32384-263">Wenn Sie nicht auf \ (oder aktivieren \) einer Popupbenachrichtigung klicken, wird diese nach einigen Sekunden geschlossen und in Ihrem Windows-Wartungs Center in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="32384-263">If you do not click \(or activate\) a toast notification, it is dismissed after several seconds and queue up in your Windows Action Center.</span></span>  
    
    ![Benachrichtigungen im Windows-Wartungs Center][ImageWindowsActionCenter]  
    
    <span data-ttu-id="32384-265">Sie haben die Grundlagen von PWA-Push-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="32384-265">You have the basics of PWA push notifications.</span></span>  <span data-ttu-id="32384-266">In einer echten App werden die nächsten Schritte auf eine Weise implementiert, um Pushabonnements zu verwalten und zu speichern sowie Nutzdaten, die über das Netzwerk gesendet werden, ordnungsgemäß zu [verschlüsseln][NPMWebPushEncrypt] .</span><span class="sxs-lookup"><span data-stu-id="32384-266">In a real app, the next steps are implemented in a way to manage and store push subscriptions and to properly [encrypt][NPMWebPushEncrypt] payload data being sent across the wire.</span></span>  
    
## <span data-ttu-id="32384-267">Vertiefung</span><span class="sxs-lookup"><span data-stu-id="32384-267">Going further</span></span>  

<span data-ttu-id="32384-268">Dieser Leitfaden zeigt die grundlegende Anatomie einer progressiven Web-App und Microsoft PWA-Entwicklungstools, einschließlich Visual Studio, PWA Builder und Edge-devtools.</span><span class="sxs-lookup"><span data-stu-id="32384-268">This guide demonstrated the basic anatomy of a Progressive Web App and Microsoft PWA development tools including Visual Studio, PWA Builder, and Edge DevTools.</span></span>  

<span data-ttu-id="32384-269">Natürlich gibt es noch viel mehr, was dazu führt, dass [eine tolle PWA][PwaEdgehtmlIndexRequirements] über das hinausgeht, was Sie hier lesen, einschließlich des reaktionsfähigen Designs, der Deep-Linking-Funktion, der [browserübergreifenden Tests][BrowserStackTestEdgeBrowser] und anderer [bewährter Methoden][Webhint] \ (ganz zu schweigen von Ihrer APP-Funktionalität! \), doch dieser Leitfaden hat Ihnen hoffentlich eine fundierte Einführung in die Grundlagen von</span><span class="sxs-lookup"><span data-stu-id="32384-269">Of course, there is a lot more that goes into [making a great PWA][PwaEdgehtmlIndexRequirements] beyond what you read here, including responsive design, deep-linking, [cross-browser testing][BrowserStackTestEdgeBrowser] and other [best practices][Webhint] \(not to mention your app functionality!\), but hopefully this guide gave you a solid introduction of PWA basics and some ideas on getting started.</span></span>  <span data-ttu-id="32384-270">Wenn Sie weitere Fragen zur PWA-Entwicklung mit Windows oder Visual Studio haben, geben Sie bitte einen Kommentar ab!</span><span class="sxs-lookup"><span data-stu-id="32384-270">If you have further questions on PWA development with Windows or with Visual Studio, please leave a comment!</span></span>  

<span data-ttu-id="32384-271">Sehen Sie sich die anderen PWA-Leitfäden an, um zu erfahren, wie Sie die Kundenbindung erhöhen und eine nahtlosere, Betriebssystem integrierte App-Umgebung bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="32384-271">Review the other PWA guides to learn how to increase customer engagement and provide a more seamless, OS-integrated app experience.</span></span>  

*   <span data-ttu-id="32384-272">[Anpassen von Windows][PwaEdgehtmlWindowsFeatures]</span><span class="sxs-lookup"><span data-stu-id="32384-272">[Windows tailoring][PwaEdgehtmlWindowsFeatures].</span></span> <span data-ttu-id="32384-273">Mithilfe der einfachen Feature-Erkennung können Sie Ihre PWA für Windows 10-Kunden schrittweise über Native Windows-Runtime \ (WinRT \)-APIs verbessern, beispielsweise für die Anpassung der kachelbenachrichtigungen für Windows- **Startmenü** und für die Taskleiste Jumplists und \ (nach Berechtigung), die mit Benutzer Ressourcen wie Fotos, Musik und Kalender arbeiten.</span><span class="sxs-lookup"><span data-stu-id="32384-273">Using simple feature detection, you may progressively enhance your PWA for Windows 10 customers through native Windows Runtime \(WinRT\) APIs, such as those for customizing Windows **Start** menu tile notifications and taskbar jumplists, and \(upon permission\) working with user resources, such as photos, music, and calendar.</span></span>  
*   <span data-ttu-id="32384-274">[PWAs im Microsoft Store][PwaEdgehtmlMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="32384-274">[PWAs in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  <span data-ttu-id="32384-275">Erfahren Sie mehr über die Vorteile der App Store-Verteilung und wie Sie Ihre PWA übermitteln.</span><span class="sxs-lookup"><span data-stu-id="32384-275">Learn more about the benefits of app store distribution and how to submit your PWA.</span></span>  

## <span data-ttu-id="32384-276">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="32384-276">See also</span></span>  

*   <span data-ttu-id="32384-277">[Progressive Web-Apps auf MDN Web docs][MDNProgressiveWebApps] – exzellenter Leitfaden für Progressive Web-Apps.</span><span class="sxs-lookup"><span data-stu-id="32384-277">[Progressive Web Apps on MDN web docs][MDNProgressiveWebApps] - Excellent guide on Progressive Web Apps.</span></span>  
*   <span data-ttu-id="32384-278">[Progressive Web-Apps auf Web. dev][WebDevProgressiveWebApps] – exzellenter Leitfaden für Progressive Web-Apps.</span><span class="sxs-lookup"><span data-stu-id="32384-278">[Progressive Web Apps on web.dev][WebDevProgressiveWebApps] - Excellent guide on Progressive Web Apps.</span></span>  
*   <span data-ttu-id="32384-279">[Progressive Web-Apps rockt][ProgressiveWebApps] – zeigt Beispiele für PWAs in der realen Welt.</span><span class="sxs-lookup"><span data-stu-id="32384-279">[Progressive Web Apps rocks][ProgressiveWebApps] - Showcases real-world examples of PWAs.</span></span>  
*   <span data-ttu-id="32384-280">[Hacker-Nachrichten Leser als Progressive Web-Apps][HackerNewsProgressiveWebApps] – vergleicht unterschiedliche Frameworks und Leistungsmuster für die Implementierung einer Stichprobe \ (Hacker Newsreader \) PWA.</span><span class="sxs-lookup"><span data-stu-id="32384-280">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  

<!-- image links -->  

[ImageDevtoolsPush]: ./media/devtools-push.png  
[ImageDevtoolsSwCache]: ./media/devtools-cache.png  
[ImageDevtoolsSwOverview]: ./media/devtools-sw-overview.png  
[ImageNotificationPermission]: ./media/notification-permission.png  
[ImageOfflineHtml]: ./media/offline-html.png  
[ImagePwa]: ./media/pwa.png  
[ImagePwaPush]: ./media/pwa-push.png  
[ImageVsNodejsExpressIcon]: ./media/vs-nodejs-express-icon.png  
[ImageVsNodejsExpressIndex]: ./media/vs-nodejs-express-index.png  
[ImageVsNodejsExpressManifest]: ./media/vs-nodejs-express-manifest.png  
[ImageVsNodejsExpressPublic]: ./media/vs-nodejs-express-public.png  
[ImageVsNodejsExpressTemplate]: ./media/vs-nodejs-express-template.png  
[ImageWindowsActionCenter]: ./media/windows-action-center.png  

<!-- links -->  

[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Anforderungen – Progressive Web-Apps \ (EdgeHTML \) unter Windows | Microsoft docs"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps/microsoft-store.md "Progressive Web-Apps \ (EdgeHTML \) im Microsoft Store | Microsoft docs"  
[PwaEdgehtmlWindowsFeatures]: ../progressive-web-apps/windows-features.md "Anpassen ihrer PWA \ (EdgeHTML \) für Windows | Microsoft docs"  

[LegalWindowsAgrementsMicrosoftStorePolicies]: /legal/windows/agreements/store-policies "Microsoft Store-Richtlinien | Microsoft docs"  

[VisualStudioNodeJsTutorial]: /visualstudio/nodejs/tutorial-nodejs "Lernprogramm: Erstellen einer Node.js-und Express-app in Visual Studio | Microsoft docs"  
[VisualStudioNodejsTutorialPublishAzureAppService]: /visualstudio/nodejs/tutorial-nodejs#optional-publish-to-azure-app-service "Veröffentlichen im Azure-App-Dienst – erstellen einer Node.js-und Express-app in Visual Studio | Microsoft docs"  

[WindowsUwpGetStartedWhat]: /windows/uwp/get-started/whats-a-uwp "Was ist eine universelle Windows-Plattform \ (UWP \)-app?  | Microsoft docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Erstellen eines Azure Free-Kontos | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Web-Apps | Microsoft Azure"  

<!--[DeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote/ "page not found"  -->  

[WindowsBlogsPwaEdge]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#4UOdrDJj3124VIkc.97 "Willkommene Progressive Web-Apps für Microsoft Edge und Windows 10 | Windows-Blogs"  
[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Web-Benachrichtigungen in Microsoft Edge | Windows-Blogs"  

[VisualStudioDownloads]: https://www.visualstudio.com/downloads "Downloads | Visual Studio"  
[VisualStudioFree]: https://visualstudio.microsoft.com/free-developer-offers "﻿Kostenlose Entwickler Software & Services | Visual Studio"  
[VisualStudioPreview]: https://www.visualstudio.com/vs/preview "Visual Studio Preview"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "﻿Kostenlose Tests für Microsoft Edge-Browser unter Windows 10 | BrowserStack"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Hacker-Nachrichten Leser als Progressive Web-Apps"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/DedicatedWorkerGlobalScope/postMessage "DedicatedWorkerGlobalScope. PostMessage \ (\) | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Progressive Web-Apps \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "Pushmanager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker-API | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "Synchronisierungs-Manager | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Verwenden von Service Mitarbeitern | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Web App-Manifest | MDN"  
[MDNWorkerPrototypePostMessage]: https://developer.mozilla.org/docs/Web/API/Worker/postMessage "Worker. Prototype. PostMessage \ (\) | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Senden von VAPID identifizierten webpush-Benachrichtigungen über den Push-Dienst von Mozilla | Mozilla-Dienste"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Push | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, Payload, contentEncoding)-Web-Push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Verwendung-Web-Push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Progressive Web-Apps"  

[PugAttributes]: https://pugjs.org/language/attributes.html "Attribute | Mops"  

[PwaBuilder]: https://www.pwabuilder.com "PWA-Generator"  
[PwaBuilderAppImageGenerator]: https://www.pwabuilder.com/imageGenerator "App-Bild Generator"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Dienstmitarbeiter | PWA-Generator"  

[ServiceWorkerCookbook]: https://serviceworke.rs "ServiceWorker Cookbook"  
[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich-Demo | ServiceWorker Cookbook"  

[W3cWebAppManifest]: https://www.w3.org/TR/appmanifest "Web App-Manifest | W3C"  

[Webhint]: https://sonarwhal.com "webhint, das Hinweis Modul für bewährte Webmethoden" 
 
[MDNWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Verwenden von Web Workern" 

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Progressive Web-Apps | Web. dev"  

[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS | Wikipedia"  
[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Progressive Verbesserung | Wikipedia"  

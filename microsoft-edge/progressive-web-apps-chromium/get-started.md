---
description: In diesem Handbuch erhalten Sie eine Übersicht über die Grundlagen und Tools von PWA zum Erstellen von Progressive Web Apps (Chromium) unter Windows.
title: Erste Schritte mit Progressive Web Apps (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: progressive Web-Apps, PWA, Edge, Windows, PWABuilder, Webmanifest, Service worker, Push
ms.openlocfilehash: 6ff24b2e9219b2f3755bb2e8f6db137dc7a721ec
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398133"
---
# <a name="get-started-with-progressive-web-apps-chromium"></a><span data-ttu-id="db4a7-104">Erste Schritte mit Progressive Web Apps (Chromium)</span><span class="sxs-lookup"><span data-stu-id="db4a7-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="db4a7-105">Progressive Web Apps \(PWAs\) sind Web-Apps, die [schrittweise erweitert werden.][WikiProgressiveEnhancement]</span><span class="sxs-lookup"><span data-stu-id="db4a7-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement].</span></span>  <span data-ttu-id="db4a7-106">Die progressiven Verbesserungen umfassen app- like Features, z. B. Installation, Offlineunterstützung und Pushbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-106">The progressive enhancements include app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="db4a7-107">Sie können ihre PWA auch für App-Stores packen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-107">You may also package your PWA for app stores.</span></span>  <span data-ttu-id="db4a7-108">Zu den möglichen App-Stores gehören der Microsoft Store, Google Play, der Mac App Store und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="db4a7-108">Possible app stores include the Microsoft Store, Google Play, Mac App Store, and more.</span></span>  <span data-ttu-id="db4a7-109">Der Microsoft Store ist der kommerzielle App Store in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="db4a7-109">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="db4a7-110">Im folgenden Handbuch erhalten Sie eine Übersicht über die Grundlagen von PWA, indem Sie eine einfache Web-App erstellen und als PWA erweitern.</span><span class="sxs-lookup"><span data-stu-id="db4a7-110">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="db4a7-111">Das fertige Projekt funktioniert in modernen Browsern.</span><span class="sxs-lookup"><span data-stu-id="db4a7-111">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="db4a7-112">Sie können [PWABuilder verwenden,][PwaBuilder] um eine neue PWA zu erstellen, Ihre vorhandene PWA zu verbessern oder Ihre PWA für App-Stores zu packen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-112">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="db4a7-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="db4a7-113">Prerequisites</span></span>  

*   <span data-ttu-id="db4a7-114">Verwenden [Visual Studio Code zum][VisualstudioCodeMain] Bearbeiten des PWA-Quellcodes.</span><span class="sxs-lookup"><span data-stu-id="db4a7-114">Use [Visual Studio Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="db4a7-115">Verwenden [Node.js][NodejsMain] als lokaler Webserver.</span><span class="sxs-lookup"><span data-stu-id="db4a7-115">Use [Node.js][NodejsMain] as your local web server.</span></span>  
    
## <a name="create-a-basic-web-app"></a><span data-ttu-id="db4a7-116">Erstellen einer einfachen Web-App</span><span class="sxs-lookup"><span data-stu-id="db4a7-116">Create a basic web app</span></span>  

<span data-ttu-id="db4a7-117">Führen Sie zum Erstellen einer leeren Web-App die Schritte unter [Node Express App Generator aus,][ExpressjsApplicationGenerator]und nennen Sie Ihre App `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="db4a7-117">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="db4a7-118">Führen Sie in der Eingabeaufforderung die folgenden Befehle aus.</span><span class="sxs-lookup"><span data-stu-id="db4a7-118">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="db4a7-119">Die Befehle erstellen eine leere Web-App und installieren abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="db4a7-119">The commands create an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="db4a7-120">Sie haben jetzt eine einfache, funktionale Web-App.</span><span class="sxs-lookup"><span data-stu-id="db4a7-120">You now have a simple, functional web app.</span></span>  <span data-ttu-id="db4a7-121">Führen Sie den folgenden Befehl aus, um Ihre Web-App zu starten.</span><span class="sxs-lookup"><span data-stu-id="db4a7-121">To start your web app, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="db4a7-122">Navigieren Sie nun, `http://localhost:3000` um Ihre neue Web-App zu sehen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-122">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Ausführen des neuen PWA auf localhost" lightbox="./media/vs-nodejs-express-index.png":::
   <span data-ttu-id="db4a7-124">Ausführen des neuen PWA auf localhost</span><span class="sxs-lookup"><span data-stu-id="db4a7-124">Running your new PWA on localhost</span></span>
:::image-end:::

## <a name="get-started-building-a-pwa"></a><span data-ttu-id="db4a7-125">Erste Schritte beim Erstellen einer PWA</span><span class="sxs-lookup"><span data-stu-id="db4a7-125">Get started building a PWA</span></span>  

<span data-ttu-id="db4a7-126">Da Sie nun über eine einfache Web-App verfügen, erweitern Sie sie als PWA, indem Sie die drei Anforderungen für PWAs hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-126">Now that you have a simple web app, extend it as a PWA by adding the three requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="db4a7-127">: [HTTPS](#step-1---use-https), [ein Web-App-Manifest](#step-2---create-a-web-app-manifest)und ein [Service Worker](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="db4a7-127">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <a name="step-1---use-https"></a><span data-ttu-id="db4a7-128">Schritt 1 : Verwenden von HTTPS</span><span class="sxs-lookup"><span data-stu-id="db4a7-128">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="db4a7-129">Wichtige Teile der PWA-Plattform, z. B. [Service Workers,][MDNServiceWorkerApi]erfordern die Verwendung von HTTPS.</span><span class="sxs-lookup"><span data-stu-id="db4a7-129">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="db4a7-130">Wenn Ihr PWA live geht, müssen Sie es in einer HTTPS-URL veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-130">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="db4a7-131">Zum Debuggen ermöglicht Microsoft Edge auch `http://localhost` die Verwendung der PWA-APIs.</span><span class="sxs-lookup"><span data-stu-id="db4a7-131">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="db4a7-132">[Veröffentlichen Sie Ihre Web-App als Livewebsite,][VisualStudioNodejsTutorialPublishAzureAppService]stellen Sie jedoch sicher, dass Ihr Server für HTTPS konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="db4a7-132">[Publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService], but ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="db4a7-133">Sie können beispielsweise ein kostenloses [Azure-Konto erstellen.][AzureCreateFreeAccount]</span><span class="sxs-lookup"><span data-stu-id="db4a7-133">For example, you may create an [Azure free account][AzureCreateFreeAccount].</span></span>  <span data-ttu-id="db4a7-134">Hosten Sie Ihre Website im [Microsoft Azure App Service,][AzureWebApps] und sie wird standardmäßig über HTTPS bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="db4a7-134">Host your site on the [Microsoft Azure App Service][AzureWebApps] and it is served over HTTPS by default.</span></span>  

<span data-ttu-id="db4a7-135">Verwenden Sie die folgende Anleitung, `http://localhost` um Ihre PWA zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-135">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <a name="step-2---create-a-web-app-manifest"></a><span data-ttu-id="db4a7-136">Schritt 2 : Erstellen eines Web-App-Manifests</span><span class="sxs-lookup"><span data-stu-id="db4a7-136">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="db4a7-137">Ein [Web App-Manifest][MDNWebAppManifest] ist eine JSON-Datei, die Metadaten zu Ihrer App enthält, z. B. Name, Beschreibung, Symbole und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="db4a7-137">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="db4a7-138">So fügen Sie der Web-App ein App-Manifest hinzu:</span><span class="sxs-lookup"><span data-stu-id="db4a7-138">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="db4a7-139">Wählen Visual Studio Code die Option **Datei**öffnen Ordner  >  **aus,** und wählen Sie das `MySamplePwa` Verzeichnis aus, das Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="db4a7-139">In Visual Studio Code, choose **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="db4a7-140">Wählen `Ctrl` + `N` Sie diese Option aus, um eine neue Datei zu erstellen, und fügen Sie den folgenden Codeausschnitt ein.</span><span class="sxs-lookup"><span data-stu-id="db4a7-140">Select `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
    ```json
    {
        "lang": "en-us",
        "name": "My Sample PWA",
        "short_name": "SamplePWA",
        "description": "A sample PWA for testing purposes",
        "start_url": "/",
        "background_color": "#2f3d58",
        "theme_color": "#2f3d58",        
        "orientation": "any",
        "display": "standalone",
        "icons": [
            {
                "src": "/icon512.png",
                "sizes": "512x512"
            }
        ]
    }
    ```  
    
1.  <span data-ttu-id="db4a7-141">Speichern Sie die Datei unter `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="db4a7-141">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="db4a7-142">Fügen Sie ein 512x512-App-Symbolbild mit dem Namen `icon512.png` zu `/MySamplePwa/public/images` hinzu.</span><span class="sxs-lookup"><span data-stu-id="db4a7-142">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="db4a7-143">Sie können das [Beispielbild zu][ImagePwa] Testzwecken verwenden.</span><span class="sxs-lookup"><span data-stu-id="db4a7-143">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="db4a7-144">Öffnen Visual Studio `/public/index.html` Code, und fügen Sie den folgenden Codeausschnitt innerhalb des Tags `<head>` hinzu.</span><span class="sxs-lookup"><span data-stu-id="db4a7-144">In Visual Studio Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <a name="step-3---add-a-service-worker"></a><span data-ttu-id="db4a7-145">Schritt 3 : Hinzufügen eines Dienstmitarbeiters</span><span class="sxs-lookup"><span data-stu-id="db4a7-145">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="db4a7-146">Servicemitarbeiter sind die Schlüsseltechnologie für PWAs und ermöglichen Szenarien wie Offlineunterstützung, erweiterte Zwischenspeicherung und Ausführen von Hintergrundaufgaben, die zuvor auf systemeigene Apps beschränkt waren.</span><span class="sxs-lookup"><span data-stu-id="db4a7-146">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="db4a7-147">Servicemitarbeiter sind Hintergrundaufgaben, die Netzwerkanforderungen von Ihrer Web-App abfangen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-147">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="db4a7-148">Service workers attempt to complete tasks, even when your PWA is not running.</span><span class="sxs-lookup"><span data-stu-id="db4a7-148">Service workers attempt to complete tasks, even when your PWA is not running.</span></span>  <span data-ttu-id="db4a7-149">Zu den Aufgaben gehören die folgenden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-149">Tasks include the following actions.</span></span>  

*   <span data-ttu-id="db4a7-150">Serving requested resources from a cache</span><span class="sxs-lookup"><span data-stu-id="db4a7-150">Serving requested resources from a cache</span></span>  
*   <span data-ttu-id="db4a7-151">Senden von Pushbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="db4a7-151">Sending push notifications</span></span>  
*   <span data-ttu-id="db4a7-152">Ausführen von Aufgaben zum Abrufen von Hintergrundinformationen</span><span class="sxs-lookup"><span data-stu-id="db4a7-152">Running background fetch tasks</span></span>  
*   <span data-ttu-id="db4a7-153">Ungültige Symbole</span><span class="sxs-lookup"><span data-stu-id="db4a7-153">Badging icons</span></span>  
*   <span data-ttu-id="db4a7-154">und mehr</span><span class="sxs-lookup"><span data-stu-id="db4a7-154">and more</span></span>  
    
<span data-ttu-id="db4a7-155">Dienstmitarbeiter werden in einer speziellen JavaScript-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="db4a7-155">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="db4a7-156">Weitere Informationen finden Sie unter [Using Service Workers][MDNUsingServiceWorkers] and Service Worker [API][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="db4a7-156">For more information, navigate to [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="db4a7-157">Verwenden Sie zum Erstellen eines Dienstmitarbeiters in Ihrem Projekt das **Rezept cache-first network** service worker von [PWA Builder][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="db4a7-157">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="db4a7-158">Navigieren Sie [zu pwabuilder.com/serviceworker,][PwaBuilderServiceWorker]wählen Sie **den Cache-First-Netzwerkdienstmitarbeiter** aus, und wählen Sie die **Schaltfläche Herunterladen** aus.</span><span class="sxs-lookup"><span data-stu-id="db4a7-158">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="db4a7-159">Die heruntergeladene Datei enthält die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="db4a7-159">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  <span data-ttu-id="db4a7-160">Kopieren Sie die heruntergeladenen Dateien `public` in den Ordner in Ihrem Web-App-Projekt.</span><span class="sxs-lookup"><span data-stu-id="db4a7-160">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
1.  <span data-ttu-id="db4a7-161">Öffnen Visual Studio Code, und fügen Sie den `/public/index.html` folgenden Codeausschnitt innerhalb des Tags `<head>` hinzu.</span><span class="sxs-lookup"><span data-stu-id="db4a7-161">In Visual Studio Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="db4a7-162">Ihre Web-App verfügt jetzt über einen Dienstmitarbeiter, der die Cache-First-Strategie verwendet.</span><span class="sxs-lookup"><span data-stu-id="db4a7-162">Your web app now has a service worker that uses the cache-first strategy.</span></span>  <span data-ttu-id="db4a7-163">Der neue Dienstmitarbeiter ruft ressourcen zuerst aus dem Cache und nur bei Bedarf aus dem Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="db4a7-163">You new service worker fetches resources from the cache first, and from the network only as needed.</span></span>  <span data-ttu-id="db4a7-164">Zwischengespeicherte Ressourcen umfassen Bilder, JavaScript, CSS und HTML.</span><span class="sxs-lookup"><span data-stu-id="db4a7-164">Cached resources include images, JavaScript, CSS, and HTML.</span></span>

<span data-ttu-id="db4a7-165">Verwenden Sie die folgenden Schritte, um zu bestätigen, dass Ihr Dienstmitarbeiter ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db4a7-165">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="db4a7-166">Navigieren Sie zu Ihrer Web-App mithilfe `http://localhost:3000` von .</span><span class="sxs-lookup"><span data-stu-id="db4a7-166">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="db4a7-167">Wenn Ihre Web-App nicht verfügbar ist, führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="db4a7-167">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="db4a7-168">Wählen Sie in Microsoft Edge aus, `F12` um die Microsoft Edge DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-168">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="db4a7-169">Wählen **Sie Anwendung**und dann Service Workers **aus,** um die Servicemitarbeiter anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="db4a7-169">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="db4a7-170">Wenn der Dienstmitarbeiter nicht angezeigt wird, aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="db4a7-170">If the service worker is not displayed, refresh the page.</span></span>  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Übersicht über Microsoft Edge DevTools Service Worker" lightbox="./media/devtools-sw-overview.png":::
       <span data-ttu-id="db4a7-172">Übersicht über Microsoft Edge DevTools Service Worker</span><span class="sxs-lookup"><span data-stu-id="db4a7-172">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="db4a7-173">Zeigen Sie den Dienstarbeitscache an, indem Sie **Cachespeicher erweitern,** und wählen Sie **pwabuilder-precache aus.**</span><span class="sxs-lookup"><span data-stu-id="db4a7-173">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="db4a7-174">Alle vom Dienstmitarbeiter zwischengespeicherten Ressourcen sollten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="db4a7-174">All of the resources cached by the service worker should be displayed.</span></span>  <span data-ttu-id="db4a7-175">Zu den ressourcen, die vom Dienstmitarbeiter zwischengespeichert werden, gehören das App-Symbol, das App-Manifest, css und die JavaScript-Dateien.</span><span class="sxs-lookup"><span data-stu-id="db4a7-175">The resources cached by the service worker include the app icon, app manifest, CSS, and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Dienstarbeitscache in Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       <span data-ttu-id="db4a7-177">Dienstarbeitscache in Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="db4a7-177">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="db4a7-178">Testen Sie PWA als Offline-App.</span><span class="sxs-lookup"><span data-stu-id="db4a7-178">Try your PWA as an offline app.</span></span>  <span data-ttu-id="db4a7-179">Wählen Sie in Microsoft Edge DevTools \( \) Netzwerk aus, und ändern Sie dann `F12` den **Onlinestatus** in **Offline**. </span><span class="sxs-lookup"><span data-stu-id="db4a7-179">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Festlegen des Offlinemodus der App in Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       <span data-ttu-id="db4a7-181">Festlegen des Offlinemodus der App in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="db4a7-181">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="db4a7-182">Aktualisieren Sie Ihre App, und sie sollte den Offlinemechanismus für die Verwendung der Ressourcen Ihrer App aus dem Cache anzeigen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-182">Refresh your app and it should display the offline mechanism for serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Offline ausgeführter PWA" lightbox="./media/vs-nodejs-express-index.png":::
       <span data-ttu-id="db4a7-184">Offline ausgeführter PWA</span><span class="sxs-lookup"><span data-stu-id="db4a7-184">PWA running offline</span></span>
    :::image-end:::
    
## <a name="add-push-notifications-to-your-pwa"></a><span data-ttu-id="db4a7-185">Hinzufügen von Pushbenachrichtigungen zu Ihrem PWA</span><span class="sxs-lookup"><span data-stu-id="db4a7-185">Add push notifications to your PWA</span></span>  

<span data-ttu-id="db4a7-186">Sie können PWAs erstellen, die Pushbenachrichtigungen unterstützen, indem Sie die folgenden Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-186">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="db4a7-187">Abonnieren eines Messagingdiensts mithilfe der [Push-API][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="db4a7-187">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="db4a7-188">Anzeigen einer Popupnachricht beim Empfangen einer Nachricht vom Dienst mithilfe der [Benachrichtigungs-API][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="db4a7-188">Display a toast message when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  
    
<span data-ttu-id="db4a7-189">Genau wie bei Service Workers sind die Pushbenachrichtigungs-APIs standardbasierte APIs.</span><span class="sxs-lookup"><span data-stu-id="db4a7-189">Just like with Service Workers, the push notification APIs are standards-based APIs.</span></span>  <span data-ttu-id="db4a7-190">Die Pushbenachrichtigungs-APIs funktionieren browserübergreifend, daher sollte Ihr Code überall funktionieren, wo PWAs unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="db4a7-190">The push notification APIs work across browsers, so your code should work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="db4a7-191">Weitere Informationen zum Senden von Pushnachrichten an verschiedene Browser auf Ihrem Server finden Sie unter [Web-Push][NPMWebPush].</span><span class="sxs-lookup"><span data-stu-id="db4a7-191">For more information about delivering push messages to different browsers on your server, navigate to [Web-Push][NPMWebPush].</span></span>  

<span data-ttu-id="db4a7-192">Die folgenden Schritte wurden aus dem Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] von Mozilla angepasst, das eine Reihe anderer nützlicher Web-Push- und Servicearbeitsrezepte bietet.</span><span class="sxs-lookup"><span data-stu-id="db4a7-192">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <a name="step-1---generate-vapid-keys"></a><span data-ttu-id="db4a7-193">Schritt 1 : Generieren von VAPID-Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="db4a7-193">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="db4a7-194">Pushbenachrichtigungen erfordern VAPID \(Voluntary Application Server Identification\)-Schlüssel, um Pushnachrichten an den PWA-Client zu senden.</span><span class="sxs-lookup"><span data-stu-id="db4a7-194">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="db4a7-195">Es sind mehrere VAPID-Schlüsselgeneratoren online verfügbar \(z. B. [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="db4a7-195">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="db4a7-196">Nach der Generierung sollten Sie ein JSON-Objekt mit einem öffentlichen und einem privaten Schlüssel erhalten.</span><span class="sxs-lookup"><span data-stu-id="db4a7-196">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="db4a7-197">Speichern Sie die Schlüssel für spätere Schritte im folgenden Lernprogramm.</span><span class="sxs-lookup"><span data-stu-id="db4a7-197">Save the keys for later steps in the following tutorial.</span></span>  <span data-ttu-id="db4a7-198">Weitere Informationen zu VAPID und WebPush finden Sie unter Senden von VAPID identifizierten [WebPush-Benachrichtigungen mithilfe des Mozilla-Pushdiensts.][MozillaServicesSendingVapidWebPushNotificationsPush]</span><span class="sxs-lookup"><span data-stu-id="db4a7-198">For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <a name="step-2---subscribe-to-push-notifications"></a><span data-ttu-id="db4a7-199">Schritt 2 – Abonnieren von Pushbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="db4a7-199">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="db4a7-200">Servicemitarbeiter verarbeiten Pushereignisse und Popupbenachrichtigungsinteraktionen in Ihrem PWA.</span><span class="sxs-lookup"><span data-stu-id="db4a7-200">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="db4a7-201">Stellen Sie sicher, dass die folgenden Bedingungen erfüllt sind, um die PWA auf Server-Pushbenachrichtigungen zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="db4a7-201">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="db4a7-202">Ihr PWA ist installiert, aktiv und registriert</span><span class="sxs-lookup"><span data-stu-id="db4a7-202">Your PWA is installed, active, and registered</span></span>  
*   <span data-ttu-id="db4a7-203">Ihr Code zum Abschließen der Abonnementaufgabe befindet sich im Hauptbenutzeroberflächenthread des PWA</span><span class="sxs-lookup"><span data-stu-id="db4a7-203">Your code to complete the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="db4a7-204">Sie verfügen über Netzwerkkonnektivität</span><span class="sxs-lookup"><span data-stu-id="db4a7-204">You have network connectivity</span></span>  
    
<span data-ttu-id="db4a7-205">Bevor ein neues Pushabonnement erstellt wird, überprüft Microsoft Edge, ob der Benutzer die PWA-Berechtigung zum Empfangen von Benachrichtigungen erteilt hat.</span><span class="sxs-lookup"><span data-stu-id="db4a7-205">Before a new push subscription is created, Microsoft Edge verifies if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="db4a7-206">Andern falls nicht, wird der Benutzer vom Browser zur Berechtigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="db4a7-206">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="db4a7-207">Wenn die Berechtigung verweigert wird, wird von der Anforderung ein `registration.pushManager.subscribe` `DOMException` ausgelöst, der verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="db4a7-207">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="db4a7-208">Weitere Informationen zur Berechtigungsverwaltung finden Sie unter [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="db4a7-208">For more on permission management, navigate to [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="db4a7-209">Fügen Sie `pwabuilder-sw-register.js` in Ihrer Datei den folgenden Codeausschnitt an.</span><span class="sxs-lookup"><span data-stu-id="db4a7-209">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

```javascript
// Ask the user for permission to send push notifications.
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                const vapidPublicKey = "PASTE YOUR PUBLIC VAPID KEY HERE";             
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: urlBase64ToUint8Array(vapidPublicKey)
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

<span data-ttu-id="db4a7-210">Weitere Informationen finden Sie unter [PushManager][MDNPushManager] und [Web-Push.][NPMWebPushUsage]</span><span class="sxs-lookup"><span data-stu-id="db4a7-210">For more information, navigate to [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <a name="step-3---listen-for-push-notifications"></a><span data-ttu-id="db4a7-211">Schritt 3 – Abhören auf Pushbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="db4a7-211">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="db4a7-212">Nachdem ein Abonnement in Ihrem PWA erstellt wurde, fügen Sie dem Dienstmitarbeiter Handler hinzu, um auf Pushereignisse zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="db4a7-212">After a subscription is created in your PWA, add handlers to the service worker to respond to push events.</span></span>  <span data-ttu-id="db4a7-213">Das Pushereignis wird vom Server gesendet, um Popupbenachrichtigungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-213">Push event are sent from the server to display toast notifications.</span></span>  <span data-ttu-id="db4a7-214">Popupbenachrichtigungen zeigen Daten für eine empfangene Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="db4a7-214">Toast notifications display data for a received message.</span></span>  <span data-ttu-id="db4a7-215">Zum Ausführen der folgenden Aufgaben müssen Sie einen Handler `click` hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-215">To complete the following tasks, you must add a `click` handler.</span></span>  

*   <span data-ttu-id="db4a7-216">Schließen der Popupbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="db4a7-216">Dismiss the toast notification</span></span>  
*   <span data-ttu-id="db4a7-217">Öffnen, Fokussieren oder Öffnen und Fokussieren von geöffneten Fenstern</span><span class="sxs-lookup"><span data-stu-id="db4a7-217">Open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="db4a7-218">Öffnen und Fokussieren eines neuen Fensters zum Anzeigen einer PWA-Clientseite</span><span class="sxs-lookup"><span data-stu-id="db4a7-218">Open and focus a new window to display a PWA client page</span></span>  
    
<span data-ttu-id="db4a7-219">Fügen Sie `pwabuilder-sw.js` in Ihrer Datei die folgenden Handler hinzu.</span><span class="sxs-lookup"><span data-stu-id="db4a7-219">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

```javascript
// Respond to a server push with a user notification.
self.addEventListener('push', function (event) {
    if (Notification.permission === "granted") {
        const notificationText = event.data.text();
        const showNotification = self.registration.showNotification('Sample PWA', {
            body: notificationText,
            icon: 'images/icon512.png'
        });
        // Ensure the toast notification is displayed before exiting the function.
        event.waitUntil(showNotification);
    }
});

// Respond to the user selecting the toast notification.
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This attempts to display the current notification if it is already open and then focuses on it.
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

### <a name="step-4---try-it-out"></a><span data-ttu-id="db4a7-220">Schritt 4 – Ausprobieren</span><span class="sxs-lookup"><span data-stu-id="db4a7-220">Step 4 - Try it out</span></span>  

<span data-ttu-id="db4a7-221">Führen Sie die folgenden Schritte aus, um Pushbenachrichtigungen für Ihre PWA zu testen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-221">To test push notifications for your PWA, complete the following steps.</span></span>  

1.  <span data-ttu-id="db4a7-222">Navigieren Sie zu Ihrem PWA unter `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="db4a7-222">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="db4a7-223">Wenn Ihr Servicemitarbeiter aktiviert wird und versucht, Ihre PWA für Pushbenachrichtigungen zu abonnieren, fordert Microsoft Edge Sie auf, Ihrem PWA das Anzeigen von Benachrichtigungen zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="db4a7-223">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="db4a7-224">Wählen Sie **Zulassen**aus.</span><span class="sxs-lookup"><span data-stu-id="db4a7-224">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Berechtigungsdialogfeld zum Aktivieren von Benachrichtigungen" lightbox="./media/notification-permission.png":::
       <span data-ttu-id="db4a7-226">Berechtigungsdialogfeld zum Aktivieren von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="db4a7-226">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="db4a7-227">Simulieren sie eine serverseitige Pushbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="db4a7-227">Simulate a server-side push notification.</span></span>  <span data-ttu-id="db4a7-228">Wenn Ihr PWA `http://localhost:3000` in Ihrem Browser geöffnet ist, wählen Sie `F12` aus, um die DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="db4a7-228">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="db4a7-229">Wählen **Sie Application**Service  >  **Worker**Push  >  **aus,** um eine Test-Pushbenachrichtigung an Ihre PWA zu senden.</span><span class="sxs-lookup"><span data-stu-id="db4a7-229">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="db4a7-230">Eine Pushbenachrichtigung sollte in der Nähe der Taskleiste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="db4a7-230">A push notification should display near the taskbar.</span></span>  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Pushen einer Benachrichtigung von DevTools" lightbox="./media/devtools-push.png":::
             <span data-ttu-id="db4a7-232">Pushen einer Benachrichtigung von DevTools</span><span class="sxs-lookup"><span data-stu-id="db4a7-232">Push a notification from DevTools</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="db4a7-233">Wenn Sie keine Popupbenachrichtigung \(oder aktivieren\) auswählen, wird sie nach einigen Sekunden automatisch vom System geschlossen und im Windows Action Center in eine Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="db4a7-233">If you do not select \(or activate\) a toast notification, the system automatically dismisses it after several seconds and queues it in your Windows Action Center.</span></span>  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Benachrichtigungen im Windows Action Center" lightbox="./media/windows-action-center.png":::
             <span data-ttu-id="db4a7-235">Benachrichtigungen im Windows Action Center</span><span class="sxs-lookup"><span data-stu-id="db4a7-235">Notifications in Windows Action Center</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="db4a7-236">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="db4a7-236">Next steps</span></span>  

<span data-ttu-id="db4a7-237">Die folgenden Schritte umfassen zusätzliche Aufgaben, mit deren Hilfe Sie das Erstellen von echten PWAs verstehen können.</span><span class="sxs-lookup"><span data-stu-id="db4a7-237">The following steps include additional tasks to help you understand building real-world PWAs.</span></span>  

*   <span data-ttu-id="db4a7-238">Verwalten und Speichern von Pushabonnements</span><span class="sxs-lookup"><span data-stu-id="db4a7-238">Manage and store push subscriptions</span></span>  
*   <span data-ttu-id="db4a7-239">[Verschlüsseln von][NPMWebPushEncrypt] Nutzlastdaten</span><span class="sxs-lookup"><span data-stu-id="db4a7-239">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*   <span data-ttu-id="db4a7-240">Dynamisches Design</span><span class="sxs-lookup"><span data-stu-id="db4a7-240">Responsive design</span></span>  
*   <span data-ttu-id="db4a7-241">Tiefenverknüpfung</span><span class="sxs-lookup"><span data-stu-id="db4a7-241">Deep-linking</span></span>  
*   [<span data-ttu-id="db4a7-242">Browserübergreifende Tests</span><span class="sxs-lookup"><span data-stu-id="db4a7-242">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*   <span data-ttu-id="db4a7-243">Implementieren von Validierungs- und Testmethoden wie [Webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="db4a7-243">Implement validation and testing practices such as [Webhint][Webhint]</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="db4a7-244">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="db4a7-244">See also</span></span>  

*   [<span data-ttu-id="db4a7-245">Progressive Web Apps in MDN-Web-Dokumenten</span><span class="sxs-lookup"><span data-stu-id="db4a7-245">Progressive Web Apps on MDN web docs</span></span>][MDNProgressiveWebApps]  
*   [<span data-ttu-id="db4a7-246">Progressive Web Apps auf web.dev</span><span class="sxs-lookup"><span data-stu-id="db4a7-246">Progressive Web Apps on web.dev</span></span>][WebDevProgressiveWebApps]  
*   <span data-ttu-id="db4a7-247">[Hacker News-Leser als Progressive Web Apps][HackerNewsProgressiveWebApps] – Vergleicht verschiedene Frameworks und Leistungsmuster für die Implementierung eines Beispiels \(Hacker News Reader\) PWA.</span><span class="sxs-lookup"><span data-stu-id="db4a7-247">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  
*   [<span data-ttu-id="db4a7-248">Legendenbusting PWAs</span><span class="sxs-lookup"><span data-stu-id="db4a7-248">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="db4a7-249">Eine progressive Roadmap für Ihre Progressive Web App</span><span class="sxs-lookup"><span data-stu-id="db4a7-249">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="db4a7-250">Offline-POSTs mit progressiven Web-Apps</span><span class="sxs-lookup"><span data-stu-id="db4a7-250">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="db4a7-251">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="db4a7-251">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="db4a7-252">Wetten im Web</span><span class="sxs-lookup"><span data-stu-id="db4a7-252">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="db4a7-253">Benennung progressiver Web-Apps</span><span class="sxs-lookup"><span data-stu-id="db4a7-253">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="db4a7-254">Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 1)</span><span class="sxs-lookup"><span data-stu-id="db4a7-254">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="db4a7-255">Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 2)</span><span class="sxs-lookup"><span data-stu-id="db4a7-255">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="db4a7-256">Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 3)</span><span class="sxs-lookup"><span data-stu-id="db4a7-256">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Bereitstellen einer Node.js in Azure mit Visual Studio Code | Microsoft Docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Erstellen von kostenlosen Azure-| Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Web Apps | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Webbenachrichtigungen in Microsoft Edge | Windows-Blogs"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Kostenlose Microsoft Edge-Browsertests unter Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Eine progressive Roadmap für Ihre Progressive Web App"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Legendenbusting PWAs – Die neue Edge Edition"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Expressanwendungsgenerator | Express" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Benennung progressiver Web-Apps"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Hacker News-Leser als Progressive Web Apps"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Wetten im Web"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API-| MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Progressive Web apps \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API-| MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager-| MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Dienstarbeits-API-| MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Verwenden von Service Workers | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Web App Manifest | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Offline-POSTs mit progressiven Web-Apps"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Senden von VON VAPID identifizierten WebPush-Benachrichtigungen über mozillas Pushdienst-| Mozilla Services"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Push-| npm"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "encrypt(userPublicKey, userAuth, payload, contentEncoding) – Web-Push-| NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Verwendung – Web-Push-| NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Progressive Web Apps"  

[PwaBuilder]: https://www.pwabuilder.com "PWA Builder"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Service Worker | PWA Builder"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich Demo | ServiceWorker Cookbook"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 3)"  

[VapidkeysMain]: https://vapidkeys.com "Secure VAPID Key Generator | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Progressive Web Apps | web.dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Progressive | Wikipedia"  

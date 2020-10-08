---
description: Dieser Leitfaden enthält eine Übersicht über die Grundlagen und Tools von PWA für das Erstellen von Progressive Web-Apps (Chrom) unter Windows.
title: Erste Schritte mit Progressive Web-Apps (Chrom)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Progressive Web-Apps, PWA, Edge, Windows, PWABuilder, Web-Manifest, Service Worker, Push
ms.openlocfilehash: 065ced3afa8ecd4165325fd4f10a673d86c72fa7
ms.sourcegitcommit: be76feed0d616a96c77ea2748a9f0d6c0c06284b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/07/2020
ms.locfileid: "11103924"
---
# <span data-ttu-id="05e90-104">Erste Schritte mit Progressive Web-Apps (Chrom)</span><span class="sxs-lookup"><span data-stu-id="05e90-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="05e90-105">Progressive Web-Apps \ (PWAs \) sind Web-Apps, die [schrittweise verbessert][WikiProgressiveEnhancement]werden.</span><span class="sxs-lookup"><span data-stu-id="05e90-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement].</span></span>  <span data-ttu-id="05e90-106">Zu den fortschrittlichen Erweiterungen gehören App-ähnliche Features wie Installation, Offline Support und Push-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="05e90-106">The progressive enhancements include app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="05e90-107">Sie können auch Ihre PWA für App-Stores verpacken.</span><span class="sxs-lookup"><span data-stu-id="05e90-107">You may also package your PWA for app stores.</span></span>  <span data-ttu-id="05e90-108">Zu den möglichen App Stores gehören der Microsoft Store, Google Play, Mac App Store und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="05e90-108">Possible app stores include the Microsoft Store, Google Play, Mac App Store, and more.</span></span>  <span data-ttu-id="05e90-109">Der Microsoft Store ist der in Windows 10 integrierte kommerzielle App Store.</span><span class="sxs-lookup"><span data-stu-id="05e90-109">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="05e90-110">Das folgende Handbuch bietet Ihnen einen Überblick über die Grundlagen von PWA, indem Sie eine einfache Web-App erstellen und diese als PWA erweitern.</span><span class="sxs-lookup"><span data-stu-id="05e90-110">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="05e90-111">Das fertige Projekt funktioniert in modernen Browsern.</span><span class="sxs-lookup"><span data-stu-id="05e90-111">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="05e90-112">Sie können [PWABuilder][PwaBuilder] verwenden, um eine neue PWA zu erstellen, Ihre vorhandene PWA zu erweitern oder Ihre PWA für App-Stores zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="05e90-112">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <span data-ttu-id="05e90-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="05e90-113">Prerequisites</span></span>  

*   <span data-ttu-id="05e90-114">Verwenden Sie [Visual Studio-Code][VisualstudioCodeMain] zum Bearbeiten Ihres PWA-Quellcodes.</span><span class="sxs-lookup"><span data-stu-id="05e90-114">Use [Visual Studio Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="05e90-115">Verwenden Sie [Node.js][NodejsMain] als lokalen Webserver.</span><span class="sxs-lookup"><span data-stu-id="05e90-115">Use [Node.js][NodejsMain] as your local web server.</span></span>  

## <span data-ttu-id="05e90-116">Erstellen einer einfachen Web-App</span><span class="sxs-lookup"><span data-stu-id="05e90-116">Create a basic web app</span></span>  

<span data-ttu-id="05e90-117">Wenn Sie eine leere Web-App erstellen möchten, führen Sie die Schritte im [Knoten Express-App-Generator][ExpressjsApplicationGenerator]aus, und benennen Sie Ihre APP `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="05e90-117">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="05e90-118">Führen Sie in der Eingabeaufforderung die folgenden Befehle aus.</span><span class="sxs-lookup"><span data-stu-id="05e90-118">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="05e90-119">Die Befehle erstellen eine leere Web-App und installieren alle Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="05e90-119">The commands create an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="05e90-120">Sie verfügen jetzt über eine einfache, funktionelle Web-App.</span><span class="sxs-lookup"><span data-stu-id="05e90-120">You now have a simple, functional web app.</span></span>  <span data-ttu-id="05e90-121">Führen Sie den folgenden Befehl aus, um die Web-App zu starten.</span><span class="sxs-lookup"><span data-stu-id="05e90-121">To start your web app, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="05e90-122">Navigieren Sie nun zu `http://localhost:3000` ihrer neuen Web-App, um Sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="05e90-122">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Ausführen ihrer neuen PWA auf localhost" lightbox="./media/vs-nodejs-express-index.png":::
   <span data-ttu-id="05e90-124">Ausführen ihrer neuen PWA auf localhost</span><span class="sxs-lookup"><span data-stu-id="05e90-124">Running your new PWA on localhost</span></span>
:::image-end:::

## <span data-ttu-id="05e90-125">Erste Schritte beim Erstellen einer PWA</span><span class="sxs-lookup"><span data-stu-id="05e90-125">Get started building a PWA</span></span>  

<span data-ttu-id="05e90-126">Nachdem Sie nun über eine einfache Web App verfügen, können Sie Sie als PWA erweitern, indem Sie die drei Anforderungen für PWAs hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="05e90-126">Now that you have a simple web app, extend it as a PWA by adding the three requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="05e90-127">: [Https](#step-1---use-https), ein [Web App-Manifest](#step-2---create-a-web-app-manifest)und ein [Dienstmitarbeiter](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="05e90-127">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <span data-ttu-id="05e90-128">Schritt 1 – Verwenden von HTTPS</span><span class="sxs-lookup"><span data-stu-id="05e90-128">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="05e90-129">Wichtige Teile der PWA-Plattform, wie [Dienstmitarbeiter][MDNServiceWorkerApi], erfordern die Verwendung von HTTPS.</span><span class="sxs-lookup"><span data-stu-id="05e90-129">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="05e90-130">Wenn Ihre PWA live geschaltet wird, müssen Sie Sie in einer HTTPS-URL veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="05e90-130">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="05e90-131">Zu Debugging-Zwecken ermöglicht Microsoft Edge auch `http://localhost` die Verwendung der PWA-APIs.</span><span class="sxs-lookup"><span data-stu-id="05e90-131">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="05e90-132">[Veröffentlichen Sie Ihre Web-App als Live-Website][VisualStudioNodejsTutorialPublishAzureAppService], stellen Sie sicher, dass Ihr Server für HTTPS konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="05e90-132">[Publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService], but ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="05e90-133">So können Sie beispielsweise ein [Azure Free-Konto][AzureCreateFreeAccount]erstellen.</span><span class="sxs-lookup"><span data-stu-id="05e90-133">For example, you may create an [Azure free account][AzureCreateFreeAccount].</span></span>  <span data-ttu-id="05e90-134">Hosten Sie Ihre Website im [Microsoft Azure-App-Dienst][AzureWebApps] , und Sie wird standardmäßig über HTTPS bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="05e90-134">Host your site on the [Microsoft Azure App Service][AzureWebApps] and it is served over HTTPS by default.</span></span>  

<span data-ttu-id="05e90-135">Das folgende Handbuch wird `http://localhost` zum Erstellen ihrer PWA-Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="05e90-135">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <span data-ttu-id="05e90-136">Schritt 2: Erstellen eines Web App-Manifests</span><span class="sxs-lookup"><span data-stu-id="05e90-136">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="05e90-137">Bei einem [Web App-Manifest][MDNWebAppManifest] handelt es sich um eine JSON-Datei, die Metadaten zu ihrer app enthält, wie Name, Beschreibung, Symbole und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="05e90-137">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="05e90-138">So fügen Sie ein App-Manifest zur Web-App hinzu:</span><span class="sxs-lookup"><span data-stu-id="05e90-138">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="05e90-139">Wählen Sie im Visual Studio-Code **Datei**  >  **Ordner öffnen** aus, und wählen Sie das Verzeichnis aus, das `MySamplePwa` Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="05e90-139">In Visual Studio Code, choose **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="05e90-140">Wählen Sie aus, `Ctrl` + `N` um eine neue Datei zu erstellen, und fügen Sie den folgenden Codeausschnitt ein.</span><span class="sxs-lookup"><span data-stu-id="05e90-140">Select `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="05e90-141">Speichern Sie die Datei als `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="05e90-141">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="05e90-142">Fügen Sie ein 512x512-App-Symbolbild mit dem Namen hinzu `icon512.png` `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="05e90-142">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="05e90-143">Sie können das [Beispielbild][ImagePwa] für Testzwecke verwenden.</span><span class="sxs-lookup"><span data-stu-id="05e90-143">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="05e90-144">Öffnen Sie in Visual Studio-Code, `/public/index.html` und fügen Sie den folgenden Code Ausschnitt innerhalb des `<head>` Tags hinzu.</span><span class="sxs-lookup"><span data-stu-id="05e90-144">In Visual Studio Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <span data-ttu-id="05e90-145">Schritt 3: Hinzufügen eines Dienst Mitarbeiters</span><span class="sxs-lookup"><span data-stu-id="05e90-145">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="05e90-146">Dienstmitarbeiter sind die Schlüsseltechnologie hinter PWAs und ermöglichen Szenarien wie offline Support, erweiterte Zwischenspeicherung und Ausführen von Hintergrundaufgaben, die zuvor auf systemeigene apps reduziert wurden.</span><span class="sxs-lookup"><span data-stu-id="05e90-146">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="05e90-147">Dienstmitarbeiter sind Hintergrundaufgaben, die Netzwerkanforderungen aus Ihrer Web-App abfangen.</span><span class="sxs-lookup"><span data-stu-id="05e90-147">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="05e90-148">Dienstmitarbeiter versuchen, Aufgaben abzuschließen, selbst wenn Ihre PWA nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05e90-148">Service workers attempt to complete tasks, even when your PWA is not running.</span></span>  <span data-ttu-id="05e90-149">Aufgaben umfassen die folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="05e90-149">Tasks include the following actions.</span></span>  

*   <span data-ttu-id="05e90-150">Servieren von angeforderten Ressourcen aus einem Cache</span><span class="sxs-lookup"><span data-stu-id="05e90-150">Serving requested resources from a cache</span></span>  
*   <span data-ttu-id="05e90-151">Senden von Pushbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="05e90-151">Sending push notifications</span></span>  
*   <span data-ttu-id="05e90-152">Ausführen von Hintergrund Abruf Aufgaben</span><span class="sxs-lookup"><span data-stu-id="05e90-152">Running background fetch tasks</span></span>  
*   <span data-ttu-id="05e90-153">Badges-Symbole</span><span class="sxs-lookup"><span data-stu-id="05e90-153">Badging icons</span></span>  
*   <span data-ttu-id="05e90-154">und vieles mehr</span><span class="sxs-lookup"><span data-stu-id="05e90-154">and more</span></span>  

<span data-ttu-id="05e90-155">Dienstmitarbeiter werden in einer speziellen JavaScript-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="05e90-155">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="05e90-156">Weitere Informationen finden Sie unter [Verwenden von Dienst Mitarbeitern][MDNUsingServiceWorkers] und [Service Worker-API][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="05e90-156">For more information, navigate to [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="05e90-157">Um einen Dienstmitarbeiter in Ihrem Projekt zu erstellen, verwenden Sie das **Cache-First-Netzwerkdienst-Worker-** Rezept aus dem [PWA-Generator][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="05e90-157">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="05e90-158">Navigieren Sie zu [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], wählen Sie den **Cache-First-Netzwerk** Dienstmitarbeiter aus, und klicken Sie auf die Schaltfläche **herunterladen** .</span><span class="sxs-lookup"><span data-stu-id="05e90-158">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="05e90-159">Die heruntergeladene Datei enthält die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="05e90-159">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  <span data-ttu-id="05e90-160">Kopieren Sie die heruntergeladenen Dateien `public` in den Ordner in Ihrem Web App-Projekt.</span><span class="sxs-lookup"><span data-stu-id="05e90-160">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
    
1.  <span data-ttu-id="05e90-161">Öffnen Sie in Visual Studio-Code `/public/index.html` den folgenden Codeausschnitt, und fügen Sie ihn in das `<head>` Tag ein.</span><span class="sxs-lookup"><span data-stu-id="05e90-161">In Visual Studio Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="05e90-162">Ihre Web-App verfügt nun über einen Dienstmitarbeiter, der die Cache-First-Strategie verwendet.</span><span class="sxs-lookup"><span data-stu-id="05e90-162">Your web app now has a service worker that uses the cache-first strategy.</span></span>  <span data-ttu-id="05e90-163">Der neue Dienstmitarbeiter ruft zunächst Ressourcen aus dem Cache und nur nach Bedarf aus dem Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="05e90-163">You new service worker fetches resources from the cache first, and from the network only as needed.</span></span>  <span data-ttu-id="05e90-164">Zu den zwischengespeicherten Ressourcen gehören Bilder, JavaScript, CSS und HTML.</span><span class="sxs-lookup"><span data-stu-id="05e90-164">Cached resources include images, JavaScript, CSS, and HTML.</span></span>

<span data-ttu-id="05e90-165">Führen Sie die folgenden Schritte aus, um zu überprüfen, ob Ihre Dienstmitarbeiter ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="05e90-165">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="05e90-166">Navigieren Sie mithilfe von zu Ihrer Web-App `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="05e90-166">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="05e90-167">Wenn Ihre Web-App nicht verfügbar ist, führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="05e90-167">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="05e90-168">Wählen Sie in Microsoft Edge aus, `F12` um den Microsoft Edge-devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="05e90-168">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="05e90-169">Wählen Sie **Anwendung**und dann **Servicemitarbeiter** aus, um die Servicemitarbeiter anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="05e90-169">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="05e90-170">Wenn der Dienstmitarbeiter nicht angezeigt wird, aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="05e90-170">If the service worker is not displayed, refresh the page.</span></span>  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Ausführen ihrer neuen PWA auf localhost" lightbox="./media/devtools-sw-overview.png":::
       <span data-ttu-id="05e90-172">Übersicht über den Microsoft Edge devtools Service Worker</span><span class="sxs-lookup"><span data-stu-id="05e90-172">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="05e90-173">Zeigen Sie den Service Worker-Cache an, indem Sie den **Cachespeicher** erweitern und **pwabuilder-precache**auswählen.</span><span class="sxs-lookup"><span data-stu-id="05e90-173">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="05e90-174">Alle vom Dienstmitarbeiter zwischengespeicherten Ressourcen sollten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="05e90-174">All of the resources cached by the service worker should be displayed.</span></span>  <span data-ttu-id="05e90-175">Zu den vom Dienstmitarbeiter zwischengespeicherten Ressourcen gehören das App-Symbol, das App-Manifest, CSS-und JavaScript-Dateien.</span><span class="sxs-lookup"><span data-stu-id="05e90-175">The resources cached by the service worker include the app icon, app manifest, CSS, and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Ausführen ihrer neuen PWA auf localhost" lightbox="./media/devtools-cache.png":::
       <span data-ttu-id="05e90-177">Service Worker-Cache in Microsoft Edge devtools (F12)</span><span class="sxs-lookup"><span data-stu-id="05e90-177">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="05e90-178">Testen Sie Ihre PWA als offline-app.</span><span class="sxs-lookup"><span data-stu-id="05e90-178">Try your PWA as an offline app.</span></span>  <span data-ttu-id="05e90-179">Klicken Sie in Microsoft Edge devtools \ ( `F12` \) auf **Netzwerk** , und ändern Sie dann den **Online** Status in **Offline**.</span><span class="sxs-lookup"><span data-stu-id="05e90-179">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Ausführen ihrer neuen PWA auf localhost" lightbox="./media/devtools-offline.png":::
       <span data-ttu-id="05e90-181">Festlegen der APP auf den Offlinemodus in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="05e90-181">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="05e90-182">Aktualisieren Sie Ihre APP, und es sollte den Offline Mechanismus anzeigen, um die Ressourcen ihrer App aus dem Cache zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="05e90-182">Refresh your app and it should display the offline mechanism for serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Ausführen ihrer neuen PWA auf localhost" lightbox="./media/vs-nodejs-express-index.png":::
       <span data-ttu-id="05e90-184">PWA, die offline ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="05e90-184">PWA running offline</span></span>
    :::image-end:::
    
## <span data-ttu-id="05e90-185">Hinzufügen von Push-Benachrichtigungen zu ihrer PWA</span><span class="sxs-lookup"><span data-stu-id="05e90-185">Add push notifications to your PWA</span></span>  

<span data-ttu-id="05e90-186">Sie können PWAs erstellen, die Push-Benachrichtigungen unterstützen, indem Sie die folgenden Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="05e90-186">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="05e90-187">Abonnieren eines Messagingdiensts mithilfe der [Push-API][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="05e90-187">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="05e90-188">Anzeigen einer Popupnachricht, wenn eine Nachricht vom Dienst mithilfe der [Benachrichtigungs-API][MDNNotificationsApi] empfangen wird</span><span class="sxs-lookup"><span data-stu-id="05e90-188">Display a toast message when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  
    
<span data-ttu-id="05e90-189">Genau wie bei Service Mitarbeitern sind die Push-Benachrichtigungs-APIs standardbasierte APIs.</span><span class="sxs-lookup"><span data-stu-id="05e90-189">Just like with Service Workers, the push notification APIs are standards-based APIs.</span></span>  <span data-ttu-id="05e90-190">Die Push-Benachrichtigungs-APIs funktionieren in Browsern, sodass Ihr Code überall funktionieren kann, wenn PWAs unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="05e90-190">The push notification APIs work across browsers, so your code should work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="05e90-191">Weitere Informationen zum Bereitstellen von Push-Nachrichten an verschiedene Browser auf dem Server finden Sie unter [Web-Push][NPMWebPush].</span><span class="sxs-lookup"><span data-stu-id="05e90-191">For more information about delivering push messages to different browsers on your server, navigate to [Web-Push][NPMWebPush].</span></span>  

<span data-ttu-id="05e90-192">Die folgenden Schritte wurden von der Push Rich-Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] , die von Mozilla bereitgestellt wurde, mit einer Reihe anderer nützlicher Web Push-und Service-Worker-Rezepte angepasst.</span><span class="sxs-lookup"><span data-stu-id="05e90-192">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="05e90-193">Schritt 1: Generieren von VAPID-Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="05e90-193">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="05e90-194">Push-Benachrichtigungen erfordern VAPID \ (freiwillige Application Server Identification \)-Schlüssel, um Push-Nachrichten an den PWA-Client zu senden.</span><span class="sxs-lookup"><span data-stu-id="05e90-194">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="05e90-195">Es stehen mehrere VAPID-Schlüsselgeneratoren online zur Verfügung \ (beispielsweise [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="05e90-195">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="05e90-196">Nach der Generierung sollten Sie ein JSON-Objekt mit einem öffentlichen und einem privaten Schlüssel abrufen.</span><span class="sxs-lookup"><span data-stu-id="05e90-196">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="05e90-197">Speichern Sie die Schlüssel für spätere Schritte im folgenden Lernprogramm.</span><span class="sxs-lookup"><span data-stu-id="05e90-197">Save the keys for later steps in the following tutorial.</span></span>  <span data-ttu-id="05e90-198">Informationen zu VAPID und webpush finden Sie unter [Senden von VAPID identifizierten webpush-Benachrichtigungen mit dem Mozilla Push-Dienst][MozillaServicesSendingVapidWebPushNotificationsPush].</span><span class="sxs-lookup"><span data-stu-id="05e90-198">For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <span data-ttu-id="05e90-199">Schritt 2 – abonnieren von Push-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="05e90-199">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="05e90-200">Dienstmitarbeiter behandeln Push-Ereignisse und Popup Benachrichtigungs Interaktionen in ihrer PWA.</span><span class="sxs-lookup"><span data-stu-id="05e90-200">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="05e90-201">Stellen Sie sicher, dass die folgenden Bedingungen erfüllt sind, um die PWA to Server-Push-Benachrichtigungen zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="05e90-201">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="05e90-202">Ihre PWA ist installiert, aktiv und registriert</span><span class="sxs-lookup"><span data-stu-id="05e90-202">Your PWA is installed, active, and registered</span></span>  
*   <span data-ttu-id="05e90-203">Der Code zum Abschließen der Abonnement Aufgabe befindet sich im Hauptbenutzeroberflächen Thread der PWA</span><span class="sxs-lookup"><span data-stu-id="05e90-203">Your code to complete the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="05e90-204">Sie verfügen über Netzwerkkonnektivität</span><span class="sxs-lookup"><span data-stu-id="05e90-204">You have network connectivity</span></span>  
    
<span data-ttu-id="05e90-205">Bevor ein neues Push-Abonnement erstellt wird, überprüft Microsoft Edge, ob der Benutzer die PWA-Berechtigung zum Empfangen von Benachrichtigungen gewährt hat.</span><span class="sxs-lookup"><span data-stu-id="05e90-205">Before a new push subscription is created, Microsoft Edge verifies if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="05e90-206">Wenn dies nicht der Fall ist, wird der Benutzer vom Browser zur Genehmigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="05e90-206">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="05e90-207">Wenn die Berechtigung verweigert wird, wird die Anforderung zum Auslösen `registration.pushManager.subscribe` einer `DOMException` , die verarbeitet werden muss, ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="05e90-207">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="05e90-208">Weitere Informationen zur Berechtigungsverwaltung finden Sie unter [Push-Benachrichtigungen in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="05e90-208">For more on permission management, navigate to [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="05e90-209">Fügen Sie in `pwabuilder-sw-register.js` der Datei den folgenden Codeausschnitt an.</span><span class="sxs-lookup"><span data-stu-id="05e90-209">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

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

<span data-ttu-id="05e90-210">Wenn Sie weitere Informationen wünschen, navigieren Sie zu [pushmanager][MDNPushManager] und [Web-Push][NPMWebPushUsage].</span><span class="sxs-lookup"><span data-stu-id="05e90-210">For more information, navigate to [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <span data-ttu-id="05e90-211">Schritt 3 – überwachen von Push-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="05e90-211">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="05e90-212">Nachdem ein Abonnement in ihrer PWA erstellt wurde, fügen Sie dem Dienstmitarbeiter Handler hinzu, um auf Push-Ereignisse zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="05e90-212">After a subscription is created in your PWA, add handlers to the service worker to respond to push events.</span></span>  <span data-ttu-id="05e90-213">Das Push-Ereignis wird vom Server gesendet, um Popupbenachrichtigungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="05e90-213">Push event are sent from the server to display toast notifications.</span></span>  <span data-ttu-id="05e90-214">Popupbenachrichtigungen zeigen Daten für eine empfangene Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="05e90-214">Toast notifications display data for a received message.</span></span>  <span data-ttu-id="05e90-215">Wenn Sie die folgenden Aufgaben ausführen möchten, müssen Sie einen Click-Handler hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="05e90-215">To complete the following tasks, you must add a click handler.</span></span>  

*   <span data-ttu-id="05e90-216">Schließen der Popupbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="05e90-216">Dismiss the toast notification</span></span>  
*   <span data-ttu-id="05e90-217">Öffnen, fokussieren oder öffnen und fokussieren offener Fenster</span><span class="sxs-lookup"><span data-stu-id="05e90-217">Open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="05e90-218">Öffnen und fokussieren eines neuen Fensters, um eine PWA-Clientseite anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="05e90-218">Open and focus a new window to display a PWA client page</span></span>  
    
<span data-ttu-id="05e90-219">`pwabuilder-sw.js`Fügen Sie in der Datei die folgenden Handler hinzu.</span><span class="sxs-lookup"><span data-stu-id="05e90-219">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

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

### <span data-ttu-id="05e90-220">Schritt 4 – probieren Sie es aus</span><span class="sxs-lookup"><span data-stu-id="05e90-220">Step 4 - Try it out</span></span>  

<span data-ttu-id="05e90-221">Führen Sie die folgenden Schritte aus, um Push-Benachrichtigungen für Ihre PWA zu testen.</span><span class="sxs-lookup"><span data-stu-id="05e90-221">To test push notifications for your PWA, complete the following steps.</span></span>  

1.  <span data-ttu-id="05e90-222">Navigieren Sie zu ihrer PWA unter `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="05e90-222">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="05e90-223">Wenn Ihr Dienstmitarbeiter ihre PWA-Benachrichtigung für Push-Benachrichtigungen aktiviert und versucht, Sie zu abonnieren, werden Sie von Microsoft Edge dazu aufgefordert, zulassen, dass Ihre PWA-Benachrichtigungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="05e90-223">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="05e90-224">Wählen Sie **zulassen**aus.</span><span class="sxs-lookup"><span data-stu-id="05e90-224">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Ausführen ihrer neuen PWA auf localhost" lightbox="./media/notification-permission.png":::
       <span data-ttu-id="05e90-226">Dialogfeld ' Berechtigung ' zum Aktivieren von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="05e90-226">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="05e90-227">Simulieren Sie eine serverseitige Push-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="05e90-227">Simulate a server-side push notification.</span></span>  <span data-ttu-id="05e90-228">Wenn Ihre PWA `http://localhost:3000` in Ihrem Browser geöffnet ist, wählen Sie aus, `F12` um die devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="05e90-228">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="05e90-229">Wählen Sie **Application**  >  **Service Worker**  >  **Push** aus, um eine Test-Push-Benachrichtigung an Ihre PWA zu senden.</span><span class="sxs-lookup"><span data-stu-id="05e90-229">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  
    :::row:::
       :::column span="":::
          <span data-ttu-id="05e90-230">Eine Push-Benachrichtigung sollte in der Nähe der Taskleiste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="05e90-230">A push notification should display near the taskbar.</span></span>  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Ausführen ihrer neuen PWA auf localhost" lightbox="./media/devtools-push.png":::
             <span data-ttu-id="05e90-232">Pushen einer Benachrichtigung von devtools</span><span class="sxs-lookup"><span data-stu-id="05e90-232">Push a notification from DevTools</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="05e90-233">Wenn Sie keine Popupbenachrichtigung \ (oder aktivieren \) auswählen, wird das System nach einigen Sekunden automatisch geschlossen und in Ihrem Windows-Wartungs Center in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="05e90-233">If you do not select \(or activate\) a toast notification, the system automatically dismisses it after several seconds and queues it in your Windows Action Center.</span></span>  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Ausführen ihrer neuen PWA auf localhost" lightbox="./media/windows-action-center.png":::
             <span data-ttu-id="05e90-235">Benachrichtigungen im Windows-Wartungs Center</span><span class="sxs-lookup"><span data-stu-id="05e90-235">Notifications in Windows Action Center</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="05e90-236">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="05e90-236">Next steps</span></span>  

<span data-ttu-id="05e90-237">Die folgenden Schritte umfassen zusätzliche Aufgaben, mit denen Sie den Aufbau von PWAs in der realen Welt verstehen können.</span><span class="sxs-lookup"><span data-stu-id="05e90-237">The following steps include additional tasks to help you understand building real-world PWAs.</span></span>  

*   <span data-ttu-id="05e90-238">Verwalten und Speichern von Pushabonnement-Abonnements</span><span class="sxs-lookup"><span data-stu-id="05e90-238">Manage and store push subscriptions</span></span>  
*   <span data-ttu-id="05e90-239">[Verschlüsseln][NPMWebPushEncrypt] von Nutzdaten</span><span class="sxs-lookup"><span data-stu-id="05e90-239">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*   <span data-ttu-id="05e90-240">Dynamisches Design</span><span class="sxs-lookup"><span data-stu-id="05e90-240">Responsive design</span></span>  
*   <span data-ttu-id="05e90-241">Deep-Linking</span><span class="sxs-lookup"><span data-stu-id="05e90-241">Deep-linking</span></span>  
*   [<span data-ttu-id="05e90-242">Browserübergreifende Tests</span><span class="sxs-lookup"><span data-stu-id="05e90-242">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*   <span data-ttu-id="05e90-243">Implementieren von Validierungs-und Testmethoden wie [webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="05e90-243">Implement validation and testing practices such as [Webhint][Webhint]</span></span>  
   
## <span data-ttu-id="05e90-244">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="05e90-244">See also</span></span>  

*   [<span data-ttu-id="05e90-245">Progressive Web-Apps auf MDN Web docs</span><span class="sxs-lookup"><span data-stu-id="05e90-245">Progressive Web Apps on MDN web docs</span></span>][MDNProgressiveWebApps]  
*   [<span data-ttu-id="05e90-246">Progressive Web-Apps auf Web. dev</span><span class="sxs-lookup"><span data-stu-id="05e90-246">Progressive Web Apps on web.dev</span></span>][WebDevProgressiveWebApps]  
*   <span data-ttu-id="05e90-247">[Hacker-Nachrichten Leser als Progressive Web-Apps][HackerNewsProgressiveWebApps] – vergleicht unterschiedliche Frameworks und Leistungsmuster für die Implementierung einer Stichprobe \ (Hacker Newsreader \) PWA.</span><span class="sxs-lookup"><span data-stu-id="05e90-247">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  
*   [<span data-ttu-id="05e90-248">Mythos Zerschlagung PWAs</span><span class="sxs-lookup"><span data-stu-id="05e90-248">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="05e90-249">Eine progressive Roadmap für Ihre Progressive Web-App</span><span class="sxs-lookup"><span data-stu-id="05e90-249">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="05e90-250">Offline Beiträge mit progressiven Web-Apps</span><span class="sxs-lookup"><span data-stu-id="05e90-250">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="05e90-251">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="05e90-251">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="05e90-252">Wetten im Web</span><span class="sxs-lookup"><span data-stu-id="05e90-252">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="05e90-253">Benennen von progressiven Web-Apps</span><span class="sxs-lookup"><span data-stu-id="05e90-253">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="05e90-254">Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 1)</span><span class="sxs-lookup"><span data-stu-id="05e90-254">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="05e90-255">Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 2)</span><span class="sxs-lookup"><span data-stu-id="05e90-255">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="05e90-256">Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 3)</span><span class="sxs-lookup"><span data-stu-id="05e90-256">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Bereitstelleneiner Node.js-App für Azure mit Visual Studio-Code | Microsoft docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Erstellen eines Azure Free-Kontos | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Web-Apps | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Web-Benachrichtigungen in Microsoft Edge | Windows-Blogs"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio-Code"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "﻿Kostenlose Tests für Microsoft Edge-Browser unter Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Eine progressive Roadmap für Ihre Progressive Web-App"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Mythos Zerschlagung PWAs – die neue Edge-Edition"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Express-Anwendungsgenerator | Express" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Benennen von progressiven Web-Apps"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Hacker-Nachrichten Leser als Progressive Web-Apps"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Wetten im Web"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Progressive Web-Apps \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "Pushmanager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker-API | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Verwenden von Service Mitarbeitern | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Web App-Manifest | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Offline Beiträge mit progressiven Web-Apps"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Senden von VAPID identifizierten webpush-Benachrichtigungen über den Push-Dienst von Mozilla | Mozilla-Dienste"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Push | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, Payload, contentEncoding)-Web-Push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Verwendung-Web-Push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Progressive Web-Apps"  

[PwaBuilder]: https://www.pwabuilder.com "PWA-Generator"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Dienstmitarbeiter | PWA-Generator"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich-Demo | ServiceWorker Cookbook"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 3)"  

[VapidkeysMain]: https://vapidkeys.com "Secure VAPID-Schlüssel Generator | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Progressive Web-Apps | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Progressive Verbesserung | Wikipedia"  

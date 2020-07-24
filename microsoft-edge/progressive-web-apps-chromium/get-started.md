---
description: Dieser Leitfaden enthält eine Übersicht über die Grundlagen und Tools von PWA für das Erstellen von progressiven Web-Apps unter Windows.
title: Erste Schritte mit Progressive Web-Apps (Chrom)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Progressive Web-Apps, PWA, Edge, Windows, PWABuilder, Web-Manifest, Service Worker, Push
ms.openlocfilehash: a9a0cad2d771e52b783053e36f0f23dec5d8e70c
ms.sourcegitcommit: 515522959f517e194f93a27f5d360690600edd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894710"
---
# <span data-ttu-id="22e46-104">Erste Schritte mit Progressive Web-Apps (Chrom)</span><span class="sxs-lookup"><span data-stu-id="22e46-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="22e46-105">Progressive Web-Apps \ (PWAs \) sind Web-Apps, die mit App-ähnlichen Features wie Installation, Offline-Unterstützung und Push-Benachrichtigungen [schrittweise verbessert][WikiProgressiveEnhancement] werden.</span><span class="sxs-lookup"><span data-stu-id="22e46-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement] with app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="22e46-106">Sie können auch Ihre PWA für App-Stores, einschließlich des Microsoft Store, sowie Google Play, Mac App Store und vieles mehr verpacken.</span><span class="sxs-lookup"><span data-stu-id="22e46-106">You may also packaged your PWA for app stores, including the Microsoft Store as well as Google Play, Mac App Store and more.</span></span>  <span data-ttu-id="22e46-107">Der Microsoft Store ist der in Windows 10 integrierte kommerzielle App Store.</span><span class="sxs-lookup"><span data-stu-id="22e46-107">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="22e46-108">Das folgende Handbuch bietet Ihnen einen Überblick über die Grundlagen von PWA, indem Sie eine einfache Web-App erstellen und diese als PWA erweitern.</span><span class="sxs-lookup"><span data-stu-id="22e46-108">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="22e46-109">Das fertige Projekt funktioniert in modernen Browsern.</span><span class="sxs-lookup"><span data-stu-id="22e46-109">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="22e46-110">Sie können [PWABuilder][PwaBuilder] verwenden, um eine neue PWA zu erstellen, Ihre vorhandene PWA zu erweitern oder Ihre PWA für App-Stores zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="22e46-110">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <span data-ttu-id="22e46-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="22e46-111">Prerequisites</span></span>  

*   <span data-ttu-id="22e46-112">Verwenden Sie [vs-Code][VisualstudioCodeMain] zum Bearbeiten Ihres PWA-Quellcodes.</span><span class="sxs-lookup"><span data-stu-id="22e46-112">Use [VS Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="22e46-113">Verwenden Sie [Node.js][NodejsMain] als lokalen Webserver.</span><span class="sxs-lookup"><span data-stu-id="22e46-113">Use [Node.js][NodejsMain] as your local web server.</span></span>  

## <span data-ttu-id="22e46-114">Einrichten einer einfachen Web-App</span><span class="sxs-lookup"><span data-stu-id="22e46-114">Set up a basic web app</span></span>  

<span data-ttu-id="22e46-115">Wenn Sie eine leere Web-App erstellen möchten, führen Sie die Schritte im [Knoten Express-App-Generator][ExpressjsApplicationGenerator]aus, und benennen Sie Ihre APP `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="22e46-115">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="22e46-116">Führen Sie in der Eingabeaufforderung die folgenden Befehle aus.</span><span class="sxs-lookup"><span data-stu-id="22e46-116">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="22e46-117">Die Befehle erstellen eine leere Web-App und installieren alle Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="22e46-117">The commands creates an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="22e46-118">Sie haben jetzt eine einfache, funktionelle Web-App.</span><span class="sxs-lookup"><span data-stu-id="22e46-118">Now you have a simple, functional web app.</span></span>  <span data-ttu-id="22e46-119">Führen Sie den folgenden Befehl aus, um ihn zu starten.</span><span class="sxs-lookup"><span data-stu-id="22e46-119">To start it, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="22e46-120">Navigieren Sie nun zu `http://localhost:3000` ihrer neuen Web-App, um Sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22e46-120">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Ausführen ihrer neuen PWA auf localhost":::
   <span data-ttu-id="22e46-122">Ausführen ihrer neuen PWA auf localhost</span><span class="sxs-lookup"><span data-stu-id="22e46-122">Running your new PWA on localhost</span></span>
:::image-end:::

## <span data-ttu-id="22e46-123">Erste Schritte beim Erstellen einer PWA</span><span class="sxs-lookup"><span data-stu-id="22e46-123">Get started building a PWA</span></span>  

<span data-ttu-id="22e46-124">Nachdem Sie nun über eine einfache Web App verfügen, können Sie Sie als PWA erweitern, indem Sie die drei Anforderungen für PWAs hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="22e46-124">Now that you have a simple web app, extend it as a PWA by adding the 3 requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="22e46-125">: [Https](#step-1---use-https), ein [Web App-Manifest](#step-2---create-a-web-app-manifest)und ein [Dienstmitarbeiter](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="22e46-125">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <span data-ttu-id="22e46-126">Schritt 1 – Verwenden von HTTPS</span><span class="sxs-lookup"><span data-stu-id="22e46-126">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="22e46-127">Wichtige Teile der PWA-Plattform, wie [Dienstmitarbeiter][MDNServiceWorkerApi], erfordern die Verwendung von HTTPS.</span><span class="sxs-lookup"><span data-stu-id="22e46-127">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="22e46-128">Wenn Ihre PWA live geschaltet wird, müssen Sie Sie in einer HTTPS-URL veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="22e46-128">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="22e46-129">Zu Debugging-Zwecken ermöglicht Microsoft Edge auch `http://localhost` die Verwendung der PWA-APIs.</span><span class="sxs-lookup"><span data-stu-id="22e46-129">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="22e46-130">Wenn Sie [Ihre Web-App als Live Website veröffentlichen][VisualStudioNodejsTutorialPublishAzureAppService] \ (beispielsweisedurch Einrichten eines [Azure Free-Kontos][AzureCreateFreeAccount]\), müssen Sie sicherstellen, dass Ihr Server für HTTPS konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="22e46-130">If you [publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService] \(for example, by setting up an [Azure free account][AzureCreateFreeAccount]\), you must ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="22e46-131">Wenn Sie den [Microsoft Azure-App-Dienst][AzureWebApps] zum Hosten Ihrer Website verwenden, wird diese standardmäßig über HTTPS bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="22e46-131">If you use the [Microsoft Azure App Service][AzureWebApps] to host your site, it is served over HTTPS by default.</span></span>  

<span data-ttu-id="22e46-132">Das folgende Handbuch wird `http://localhost` zum Erstellen ihrer PWA-Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="22e46-132">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <span data-ttu-id="22e46-133">Schritt 2: Erstellen eines Web App-Manifests</span><span class="sxs-lookup"><span data-stu-id="22e46-133">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="22e46-134">Bei einem [Web App-Manifest][MDNWebAppManifest] handelt es sich um eine JSON-Datei, die Metadaten zu ihrer app enthält, wie Name, Beschreibung, Symbole und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="22e46-134">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="22e46-135">So fügen Sie ein App-Manifest zur Web-App hinzu:</span><span class="sxs-lookup"><span data-stu-id="22e46-135">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="22e46-136">**Klicken Sie**im vs-Code auf  >  **Ordner öffnen** , und wählen Sie das Verzeichnis aus, das `MySamplePwa` Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="22e46-136">In VS Code, go **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="22e46-137">Drücken Sie, `Ctrl` + `N` um eine neue Datei zu erstellen, und fügen Sie den folgenden Codeausschnitt ein.</span><span class="sxs-lookup"><span data-stu-id="22e46-137">Press `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="22e46-138">Speichern Sie die Datei als `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="22e46-138">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="22e46-139">Fügen Sie ein 512x512-App-Symbolbild mit dem Namen hinzu `icon512.png` `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="22e46-139">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="22e46-140">Sie können das [Beispielbild][ImagePwa] für Testzwecke verwenden.</span><span class="sxs-lookup"><span data-stu-id="22e46-140">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="22e46-141">Öffnen Sie im vs-Code, `/public/index.html` und fügen Sie den folgenden Code Ausschnitt innerhalb des `<head>` Tags hinzu.</span><span class="sxs-lookup"><span data-stu-id="22e46-141">In VS Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <span data-ttu-id="22e46-142">Schritt 3: Hinzufügen eines Dienst Mitarbeiters</span><span class="sxs-lookup"><span data-stu-id="22e46-142">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="22e46-143">Dienstmitarbeiter sind die Schlüsseltechnologie hinter PWAs und ermöglichen Szenarien wie offline Support, erweiterte Zwischenspeicherung und Ausführen von Hintergrundaufgaben, die zuvor auf systemeigene apps reduziert wurden.</span><span class="sxs-lookup"><span data-stu-id="22e46-143">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="22e46-144">Dienstmitarbeiter sind Hintergrundaufgaben, die Netzwerkanforderungen aus Ihrer Web-App abfangen.</span><span class="sxs-lookup"><span data-stu-id="22e46-144">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="22e46-145">Sie führen Aufgaben aus, auch wenn Ihre PWA nicht ausgeführt wird, beispielsweise das Servieren von angeforderten Ressourcen aus einem Cache, Senden von Push-Benachrichtigungen, Ausführen von Hintergrund-FETCH-Aufgaben, Badges-Symbolen usw.</span><span class="sxs-lookup"><span data-stu-id="22e46-145">They perform tasks, even when your PWA is not running, such as serving requested resources from a cache, sending push notifications, running background fetch tasks, badging icons, and so on.</span></span>  <span data-ttu-id="22e46-146">Dienstmitarbeiter werden in einer speziellen JavaScript-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="22e46-146">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="22e46-147">Weitere Informationen finden Sie unter [Verwenden von Servicemitarbeitern][MDNUsingServiceWorkers] und [Service Worker-API][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="22e46-147">For more information, see [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="22e46-148">Um einen Dienstmitarbeiter in Ihrem Projekt zu erstellen, verwenden Sie das **Cache-First-Netzwerkdienst-Worker-** Rezept aus dem [PWA-Generator][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="22e46-148">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="22e46-149">Navigieren Sie zu [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], wählen Sie den **Cache-First-Netzwerk** Dienstmitarbeiter aus, und klicken Sie auf die Schaltfläche **herunterladen** .</span><span class="sxs-lookup"><span data-stu-id="22e46-149">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="22e46-150">Die heruntergeladene Datei enthält die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="22e46-150">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  <span data-ttu-id="22e46-151">Kopieren Sie die heruntergeladenen Dateien `public` in den Ordner in Ihrem Web App-Projekt.</span><span class="sxs-lookup"><span data-stu-id="22e46-151">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
    
1.  <span data-ttu-id="22e46-152">Öffnen Sie im vs-Code `/public/index.html` den folgenden Codeausschnitt, und fügen Sie ihn in das `<head>` Tag ein.</span><span class="sxs-lookup"><span data-stu-id="22e46-152">In VS Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="22e46-153">Ihre Web-App verfügt nun über einen Dienstmitarbeiter, der die Cache-First-Strategie verwendet, die Ressourcen wie Bilder, JS, CSS und HTML zuerst aus dem Cache abruft und nach Bedarf zurück zum Netzwerk fällt.</span><span class="sxs-lookup"><span data-stu-id="22e46-153">Your web app now has a service worker that uses the cache-first strategy, which fetches resources like images, JS, CSS, and HTML from the cache first, and falls back to the network as needed.</span></span>  

<span data-ttu-id="22e46-154">Führen Sie die folgenden Schritte aus, um zu überprüfen, ob Ihre Dienstmitarbeiter ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="22e46-154">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="22e46-155">Navigieren Sie mithilfe von zu Ihrer Web-App `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="22e46-155">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="22e46-156">Wenn Ihre Web-App nicht verfügbar ist, führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="22e46-156">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="22e46-157">Wählen Sie in Microsoft Edge aus, `F12` um den Microsoft Edge-devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="22e46-157">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="22e46-158">Wählen Sie **Anwendung**und dann **Servicemitarbeiter** aus, um die Servicemitarbeiter anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22e46-158">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="22e46-159">Wenn der Dienstmitarbeiter nicht angezeigt wird, müssen Sie möglicherweise die Seite aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="22e46-159">If you do not see the service worker, you may need to refresh the page.</span></span>  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Übersicht über den Microsoft Edge devtools Service Worker":::
       <span data-ttu-id="22e46-161">Übersicht über den Microsoft Edge devtools Service Worker</span><span class="sxs-lookup"><span data-stu-id="22e46-161">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="22e46-162">Zeigen Sie den Service Worker-Cache an, indem Sie den **Cachespeicher** erweitern und **pwabuilder-precache**auswählen.</span><span class="sxs-lookup"><span data-stu-id="22e46-162">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="22e46-163">Sie sollten alle Ressourcen sehen, die vom Dienstmitarbeiter zwischengespeichert wurden, wie etwa das App-Symbol, App-Manifest, CSS-und JavaScript-Dateien.</span><span class="sxs-lookup"><span data-stu-id="22e46-163">You should see all the resources cached by the service worker, such as the app icon, app manifest, CSS and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Service Worker-Cache in Microsoft Edge devtools":::
       <span data-ttu-id="22e46-165">Service Worker-Cache in Microsoft Edge devtools (F12)</span><span class="sxs-lookup"><span data-stu-id="22e46-165">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="22e46-166">Testen Sie Ihre PWA als offline-app.</span><span class="sxs-lookup"><span data-stu-id="22e46-166">Try your PWA as an offline app.</span></span>  <span data-ttu-id="22e46-167">Klicken Sie in Microsoft Edge devtools \ ( `F12` \) auf **Netzwerk** , und ändern Sie dann den **Online** Status in **Offline**.</span><span class="sxs-lookup"><span data-stu-id="22e46-167">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Festlegen der APP auf den Offlinemodus in Microsoft Edge devtools":::
       <span data-ttu-id="22e46-169">Festlegen der APP auf den Offlinemodus in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="22e46-169">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="22e46-170">Aktualisieren Sie Ihre APP, und Sie sollten Sie offline arbeiten sehen, indem Sie die Ressourcen ihrer App aus dem Cache servieren.</span><span class="sxs-lookup"><span data-stu-id="22e46-170">Refresh your app and you should see it working offline by serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA, die offline ausgeführt wird":::
       <span data-ttu-id="22e46-172">PWA, die offline ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="22e46-172">PWA running offline</span></span>
    :::image-end:::
    
## <span data-ttu-id="22e46-173">Hinzufügen von Push-Benachrichtigungen zu ihrer PWA</span><span class="sxs-lookup"><span data-stu-id="22e46-173">Add push notifications to your PWA</span></span>  

<span data-ttu-id="22e46-174">Sie können PWAs erstellen, die Push-Benachrichtigungen unterstützen, indem Sie die folgenden Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="22e46-174">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="22e46-175">Abonnieren eines Messagingdiensts mithilfe der [Push-API][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="22e46-175">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="22e46-176">Anzeigen von Popupmeldungen, wenn eine Nachricht vom Dienst mithilfe der [Benachrichtigungs-API][MDNNotificationsApi] empfangen wird</span><span class="sxs-lookup"><span data-stu-id="22e46-176">Display a toast messages when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  

<span data-ttu-id="22e46-177">Wie bei Service Mitarbeitern sind dies standardbasierte APIs, die in Browsern funktionieren, sodass Sie den Code nur einmal schreiben müssen, damit er überall funktioniert, wo PWAs unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="22e46-177">As with Service Workers, these are standards-based APIs that work across browsers, so you only have to write the code once for it to work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="22e46-178">Weitere Informationen zum Übermitteln von Push-Nachrichten an verschiedene Browser auf dem Server finden Sie in der [Web-Push][NPMWebPush] -Open-Source-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="22e46-178">For more information on delivering push messages to different browsers on your server, use the [Web-Push][NPMWebPush] open-source library.</span></span>  

<span data-ttu-id="22e46-179">Die folgenden Schritte wurden von der Push Rich-Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] , die von Mozilla bereitgestellt wurde, mit einer Reihe anderer nützlicher Web Push-und Service-Worker-Rezepte angepasst.</span><span class="sxs-lookup"><span data-stu-id="22e46-179">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="22e46-180">Schritt 1: Generieren von VAPID-Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="22e46-180">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="22e46-181">Push-Benachrichtigungen erfordern VAPID \ (freiwillige Application Server Identification \)-Schlüssel, um Push-Nachrichten an den PWA-Client zu senden.</span><span class="sxs-lookup"><span data-stu-id="22e46-181">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="22e46-182">Es stehen mehrere VAPID-Schlüsselgeneratoren online zur Verfügung \ (beispielsweise [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="22e46-182">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="22e46-183">Nach der Generierung sollten Sie ein JSON-Objekt mit einem öffentlichen und einem privaten Schlüssel abrufen.</span><span class="sxs-lookup"><span data-stu-id="22e46-183">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="22e46-184">Speichern Sie die Schlüssel für die nachfolgenden Schritte im folgenden Lernprogramm.</span><span class="sxs-lookup"><span data-stu-id="22e46-184">Save the keys for subsequent steps in the following tutorial.</span></span>  <span data-ttu-id="22e46-185">Informationen dazu, wie VAPID und webpush funktionieren, finden Sie unter [Senden von VAPID identifizierten webpush-Benachrichtigungen über den Push-Dienst von Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].</span><span class="sxs-lookup"><span data-stu-id="22e46-185">For information on how VAPID and WebPush works, see [Sending VAPID identified WebPush Notifications via Mozilla's Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <span data-ttu-id="22e46-186">Schritt 2 – abonnieren von Push-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="22e46-186">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="22e46-187">Dienstmitarbeiter behandeln Push-Ereignisse und Popup Benachrichtigungs Interaktionen in ihrer PWA.</span><span class="sxs-lookup"><span data-stu-id="22e46-187">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="22e46-188">Stellen Sie sicher, dass die folgenden Bedingungen erfüllt sind, um die PWA to Server-Push-Benachrichtigungen zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="22e46-188">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="22e46-189">Ihre PWA ist installiert, aktiv und registriert</span><span class="sxs-lookup"><span data-stu-id="22e46-189">Your PWA is installed, active and registered</span></span>  
*   <span data-ttu-id="22e46-190">Ihr Code, der die Abonnement Aufgabe ausführt, befindet sich im Hauptbenutzeroberflächen Thread der PWA</span><span class="sxs-lookup"><span data-stu-id="22e46-190">Your code that performs the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="22e46-191">Sie verfügen über Netzwerkkonnektivität</span><span class="sxs-lookup"><span data-stu-id="22e46-191">You have network connectivity</span></span>  

<span data-ttu-id="22e46-192">Bevor ein neues Push-Abonnement erstellt wird, überprüft Microsoft Edge, ob der Benutzer die PWA-Berechtigung zum Empfangen von Benachrichtigungen gewährt hat.</span><span class="sxs-lookup"><span data-stu-id="22e46-192">Before a new push subscription is created, Microsoft Edge checks if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="22e46-193">Wenn dies nicht der Fall ist, wird der Benutzer vom Browser zur Genehmigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="22e46-193">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="22e46-194">Wenn die Berechtigung verweigert wird, wird die Anforderung zum Auslösen `registration.pushManager.subscribe` einer `DOMException` , die verarbeitet werden muss, ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="22e46-194">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="22e46-195">Weitere Informationen zur Berechtigungsverwaltung finden Sie unter [Push-Benachrichtigungen in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="22e46-195">For more on permission management, see [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="22e46-196">Fügen Sie in `pwabuilder-sw-register.js` der Datei den folgenden Codeausschnitt an.</span><span class="sxs-lookup"><span data-stu-id="22e46-196">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

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

<span data-ttu-id="22e46-197">Weitere Informationen finden Sie unter [pushmanager][MDNPushManager] und [Web-Push][NPMWebPushUsage].</span><span class="sxs-lookup"><span data-stu-id="22e46-197">For more information, see [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <span data-ttu-id="22e46-198">Schritt 3 – überwachen von Push-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="22e46-198">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="22e46-199">Nachdem nun ein Abonnement in ihrer PWA eingerichtet wurde, fügen Sie dem Dienstmitarbeiter Handler hinzu, um auf Push-Ereignisse zu reagieren \ (vom Server gesendet \), um Popupbenachrichtigungen mit den Daten einer empfangenen Nachricht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22e46-199">Now that a subscription is set up in your PWA, add handlers to the service worker to respond to push events \(sent from the server\) to display toast notifications with the data of a received message.</span></span>  <span data-ttu-id="22e46-200">Sie müssen einen Click-Handler hinzufügen, um die folgenden Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="22e46-200">You must add a click handler to perform the any of the following tasks.</span></span>  
*   <span data-ttu-id="22e46-201">Schließen der Popupbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="22e46-201">dismiss the toast notification</span></span>  
*   <span data-ttu-id="22e46-202">Öffnen, fokussieren oder öffnen und fokussieren offener Fenster</span><span class="sxs-lookup"><span data-stu-id="22e46-202">open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="22e46-203">Öffnen und fokussieren eines neuen Fensters, um eine PWA-Clientseite anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="22e46-203">open and focus a new window to display a PWA client page</span></span>  

<span data-ttu-id="22e46-204">`pwabuilder-sw.js`Fügen Sie in der Datei die folgenden Handler hinzu.</span><span class="sxs-lookup"><span data-stu-id="22e46-204">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

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
    
    // This looks to see if the current notification is already open and focuses it.
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

### <span data-ttu-id="22e46-205">Schritt 4 – probieren Sie es aus</span><span class="sxs-lookup"><span data-stu-id="22e46-205">Step 4 - Try it out</span></span>  

<span data-ttu-id="22e46-206">Führen Sie die folgenden Schritte aus, um Push-Benachrichtigungen in ihrer PWA zu testen.</span><span class="sxs-lookup"><span data-stu-id="22e46-206">Perform the following steps to test push notifications in your PWA.</span></span>  

1.  <span data-ttu-id="22e46-207">Navigieren Sie zu ihrer PWA unter `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="22e46-207">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="22e46-208">Wenn Ihr Dienstmitarbeiter ihre PWA-Benachrichtigung für Push-Benachrichtigungen aktiviert und versucht, Sie zu abonnieren, werden Sie von Microsoft Edge dazu aufgefordert, zulassen, dass Ihre PWA-Benachrichtigungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="22e46-208">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="22e46-209">Wählen Sie **zulassen**aus.</span><span class="sxs-lookup"><span data-stu-id="22e46-209">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Dialogfeld ' Berechtigung ' zum Aktivieren von Benachrichtigungen":::
       <span data-ttu-id="22e46-211">Dialogfeld ' Berechtigung ' zum Aktivieren von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="22e46-211">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
    
1.  <span data-ttu-id="22e46-212">Simulieren Sie eine serverseitige Push-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="22e46-212">Simulate a server-side push notification.</span></span>  <span data-ttu-id="22e46-213">Wenn Ihre PWA `http://localhost:3000` in Ihrem Browser geöffnet ist, wählen Sie aus, `F12` um die devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="22e46-213">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="22e46-214">Wählen Sie **Application**  >  **Service Worker**  >  **Push** aus, um eine Test-Push-Benachrichtigung an Ihre PWA zu senden.</span><span class="sxs-lookup"><span data-stu-id="22e46-214">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  <span data-ttu-id="22e46-215">Es sollte eine Push-Benachrichtigung in der Nähe der Taskleiste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="22e46-215">You should see a push notification appear near the taskbar.</span></span>  
    
    :::image type="complex" source="./media/devtools-push.png" alt-text="Pushen einer Benachrichtigung von devtools":::
       <span data-ttu-id="22e46-217">Pushen einer Benachrichtigung von devtools</span><span class="sxs-lookup"><span data-stu-id="22e46-217">Push a notification from DevTools</span></span>
    :::image-end:::
     
    <span data-ttu-id="22e46-218">Wenn Sie keine Popupbenachrichtigung \ (oder Activate \) auswählen, wird Sie nach einigen Sekunden geschlossen und in Ihrem Windows-Wartungs Center in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="22e46-218">If you do not select \(or activate\) a toast notification, it is dismissed after several seconds and queues up in your Windows Action Center.</span></span>  
    
    :::image type="complex" source="./media/windows-action-center.png" alt-text="Benachrichtigungen im Windows-Wartungs Center":::
       <span data-ttu-id="22e46-220">Benachrichtigungen im Windows-Wartungs Center</span><span class="sxs-lookup"><span data-stu-id="22e46-220">Notifications in Windows Action Center</span></span>
    :::image-end:::
    
    
## <span data-ttu-id="22e46-221">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="22e46-221">Next steps</span></span>  

<span data-ttu-id="22e46-222">Im folgenden finden Sie eine Liste weiterer Aufgaben, die Sie beim Erstellen von PWAs in der realen Welt kennenlernen sollten:</span><span class="sxs-lookup"><span data-stu-id="22e46-222">The following is a list of additional tasks to learn when building real-world PWAs:</span></span>  

*  <span data-ttu-id="22e46-223">Verwalten und Speichern von Pushabonnement-Abonnements</span><span class="sxs-lookup"><span data-stu-id="22e46-223">Manage and store push subscriptions</span></span>  
*  <span data-ttu-id="22e46-224">[Verschlüsseln][NPMWebPushEncrypt] von Nutzdaten</span><span class="sxs-lookup"><span data-stu-id="22e46-224">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*  <span data-ttu-id="22e46-225">Dynamisches Design</span><span class="sxs-lookup"><span data-stu-id="22e46-225">Responsive design</span></span>  
*  <span data-ttu-id="22e46-226">Deep-Linking</span><span class="sxs-lookup"><span data-stu-id="22e46-226">Deep-linking</span></span>  
*  [<span data-ttu-id="22e46-227">Browserübergreifende Tests</span><span class="sxs-lookup"><span data-stu-id="22e46-227">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*  <span data-ttu-id="22e46-228">Implementieren bewährter Methoden wie [webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="22e46-228">Implement best practices such as [Webhint][Webhint]</span></span>  

## <span data-ttu-id="22e46-229">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="22e46-229">See also</span></span>  

*   <span data-ttu-id="22e46-230">[Progressive Web-Apps auf MDN Web docs][MDNProgressiveWebApps].</span><span class="sxs-lookup"><span data-stu-id="22e46-230">[Progressive Web Apps on MDN web docs][MDNProgressiveWebApps].</span></span>  
*   <span data-ttu-id="22e46-231">[Progressive Web-Apps auf Web. dev][WebDevProgressiveWebApps].</span><span class="sxs-lookup"><span data-stu-id="22e46-231">[Progressive Web Apps on web.dev][WebDevProgressiveWebApps].</span></span>  
*   <span data-ttu-id="22e46-232">[Hacker-Nachrichten Leser als Progressive Web-Apps][HackerNewsProgressiveWebApps] – vergleicht unterschiedliche Frameworks und Leistungsmuster für die Implementierung einer Stichprobe \ (Hacker Newsreader \) PWA.</span><span class="sxs-lookup"><span data-stu-id="22e46-232">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  

<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Bereitstelleneiner Node.js-App für Azure mit vs-Code | Microsoft docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Erstellen eines Azure Free-Kontos | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Web-Apps | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Web-Benachrichtigungen in Microsoft Edge | Windows-Blogs"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio-Code"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "﻿Kostenlose Tests für Microsoft Edge-Browser unter Windows 10 | BrowserStack"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Express-Anwendungsgenerator | Express" 

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Hacker-Nachrichten Leser als Progressive Web-Apps"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Progressive Web-Apps \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "Pushmanager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker-API | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Verwenden von Service Mitarbeitern | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Web App-Manifest | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Senden von VAPID identifizierten webpush-Benachrichtigungen über den Push-Dienst von Mozilla | Mozilla-Dienste"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Push | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, Payload, contentEncoding)-Web-Push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Verwendung-Web-Push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Progressive Web-Apps"  

[PwaBuilder]: https://www.pwabuilder.com "PWA-Generator"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Dienstmitarbeiter | PWA-Generator"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich-Demo | ServiceWorker Cookbook"  

[VapidkeysMain]: https://vapidkeys.com "Secure VAPID-Schlüssel Generator | VapidKeys" 

[Webhint]: https://sonarwhal.com "webhint, das Hinweis Modul für bewährte Webmethoden"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Progressive Web-Apps | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Progressive Verbesserung | Wikipedia"  

---
description: Progressive Web-Apps (Chrom) werden nativ unter Windows 10 ausgeführt.  Hier finden Sie alles, was Sie als Web-Entwickler wissen müssen.
title: Progressive Web-Apps unter Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: Progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: a13f39dc3b3e0d47ad07b0e447556dc14093e71b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231216"
---
# <span data-ttu-id="46535-105">Übersicht über Progressive Web-Apps unter Windows</span><span class="sxs-lookup"><span data-stu-id="46535-105">Progressive Web Apps on Windows overview</span></span>  

<span data-ttu-id="46535-106">[Progressive Web-Apps][MDNApps] \(PWAs \) bieten Zugriff auf Open Web-Technologien für die plattformübergreifende Interoperabilität und bieten ihren Benutzern eine systemeigene, App-ähnliche Benutzeroberfläche, die auf Ihre Geräte zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="46535-106">[Progressive Web Apps][MDNApps] \(PWAs\) provide access to open web technologies for cross-platform interoperability and provide your users with a native, app-like experience customized for their devices.</span></span>  <span data-ttu-id="46535-107">PWAs sind Websites, die [schrittweise verbessert][AListApartUnderstandingProgressiveEnhancement] werden, um wie Native apps auf unterstützenden Plattformen zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="46535-107">PWAs are websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="46535-108">Die Eigenschaften einer PWA vereinen das Beste aus Web- und nativen Apps.</span><span class="sxs-lookup"><span data-stu-id="46535-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search.png":::
        ### [<span data-ttu-id="46535-109">Erkennbar</span><span class="sxs-lookup"><span data-stu-id="46535-109">Discoverable</span></span>][MDNPwaAdvantagesDiscoverable]
        <span data-ttu-id="46535-110">Aus Websuche-Ergebnissen und unterstützenden App-Stores</span><span class="sxs-lookup"><span data-stu-id="46535-110">From web search results and supporting app stores</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package.png":::
        ### [<span data-ttu-id="46535-111">Installierbar</span><span class="sxs-lookup"><span data-stu-id="46535-111">Installable</span></span>][MDNPwaAdvantagesInstallable]
        <span data-ttu-id="46535-112">Anheften und starten über den Startbildschirm, Startmenü, Taskleiste usw.</span><span class="sxs-lookup"><span data-stu-id="46535-112">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification.png":::
        ### [<span data-ttu-id="46535-113">Wieder einbinden</span><span class="sxs-lookup"><span data-stu-id="46535-113">Re-engageable</span></span>][MDNPwaAdvantagesReEngageable]
        <span data-ttu-id="46535-114">Senden von Push-Benachrichtigungen, auch wenn die APP nicht aktiv ist</span><span class="sxs-lookup"><span data-stu-id="46535-114">Send push notifications, even when the app is not active</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline.png":::
        ### [<span data-ttu-id="46535-115">Netzwerk unabhängig</span><span class="sxs-lookup"><span data-stu-id="46535-115">Network Independent</span></span>][MDNPwaAdvantagesNetworkIndependent]
        <span data-ttu-id="46535-116">Funktioniert offline und unter günstigen Netzwerkbedingungen</span><span class="sxs-lookup"><span data-stu-id="46535-116">Works offline and in low-network conditions</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive.png":::
        ### [<span data-ttu-id="46535-117">Progressive</span><span class="sxs-lookup"><span data-stu-id="46535-117">Progressive</span></span>][MDNPwaAdvantagesProgressive]
        <span data-ttu-id="46535-118">Die Erfahrung skaliert nach oben (oder unten) mit Gerätefunktionen</span><span class="sxs-lookup"><span data-stu-id="46535-118">Experience scales up (or down) with device capabilities</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security.png":::
        ### [<span data-ttu-id="46535-119">Sicher</span><span class="sxs-lookup"><span data-stu-id="46535-119">Safe</span></span>][MDNPwaAdvantagesSafe]
        <span data-ttu-id="46535-120">Bietet einen sicheren HTTPS-Endpunkt und andere Sicherheitsvorkehrungen für Benutzer</span><span class="sxs-lookup"><span data-stu-id="46535-120">Provides a secure HTTPS endpoint and other user safeguards</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive.png":::
        ### [<span data-ttu-id="46535-121">Dynamisch</span><span class="sxs-lookup"><span data-stu-id="46535-121">Responsive</span></span>][MDNPwaAdvantagesResponsive]
        <span data-ttu-id="46535-122">Passt sich der Bildschirmgröße des Benutzers oder der Ausrichtung und Eingabemethode an.</span><span class="sxs-lookup"><span data-stu-id="46535-122">Adapts to the user's screen size or orientation and input method</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link.png":::
        ### [<span data-ttu-id="46535-123">Linkbar</span><span class="sxs-lookup"><span data-stu-id="46535-123">Linkable</span></span>][MDNPwaAdvantagesLinkable]
        <span data-ttu-id="46535-124">Freigeben und starten von einem Standardhyperlink</span><span class="sxs-lookup"><span data-stu-id="46535-124">Share and launch from a standard hyperlink</span></span>
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


<span data-ttu-id="46535-125">Erstellen Sie Ihre vorhandene Website in eine PWA, um die Interaktion mit ihren Benutzern zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="46535-125">Build \(or convert\) your existing website to a PWA to enhance your engagement with your users.</span></span>  <span data-ttu-id="46535-126">Zu den Verbesserungen gehören Push-Benachrichtigungen, App-ähnliche Integration und Offlineunterstützung.</span><span class="sxs-lookup"><span data-stu-id="46535-126">Enhancements include push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="46535-127">Bauen Sie Ihre Zielgruppe im geöffneten Web weiter auf, damit die Benutzer ihre PWA-Suche und Link Freigabe entdecken können.</span><span class="sxs-lookup"><span data-stu-id="46535-127">Continue to build your audience on the open web for users to discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="46535-128">Das beste daran ist, dass Ihre APP mit dem Webservercode aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="46535-128">Best of all, your app is updated in using your web server code.</span></span>  

## <span data-ttu-id="46535-129">PWAs auf Microsoft Edge (Chrom)</span><span class="sxs-lookup"><span data-stu-id="46535-129">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="46535-130">Wenn Sie eine progressive Web App für Webstandard-APIs erstellen, kann Ihre Anwendung plattformübergreifend und auf Geräten bereitgestellt werden und die gerätespezifischen Funktionen wie verfügbar nutzen.</span><span class="sxs-lookup"><span data-stu-id="46535-130">When you build a Progressive Web App targeting web standard APIs, your application may be deployed across platforms and devices and take advantage of the device-specific capabilities as available.</span></span>  <span data-ttu-id="46535-131">PWAs in Microsoft Edge \(Chrom \) fügen Sie Ihrer Website die folgenden Vorteile hinzu.</span><span class="sxs-lookup"><span data-stu-id="46535-131">PWAs in Microsoft Edge \(Chromium\) add the following advantages to your website.</span></span>  

*   <span data-ttu-id="46535-132">Ihre APP ist auf einer auf Standards basierenden Web-Plattform aufgebaut.</span><span class="sxs-lookup"><span data-stu-id="46535-132">Your app is built on a standards-based web platform.</span></span>  
*   <span data-ttu-id="46535-133">Ermöglicht es Ihren Benutzern, Ihre APP direkt aus dem Browser zu installieren.</span><span class="sxs-lookup"><span data-stu-id="46535-133">Enables your users to install your app directly from the browser.</span></span>  
*   <span data-ttu-id="46535-134">Ermöglicht es Ihren Benutzern, Ihre APP ohne Store-basierte Bereitstellung oder Registrierung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="46535-134">Enables your users to install your app without a Store-based deployment or registration.</span></span>  
    
<span data-ttu-id="46535-135">Desktop-PWAs werden auf allen Plattformen unterstützt, die Microsoft Edge \(Chrom \) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="46535-135">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available.</span></span> <span data-ttu-id="46535-136">Microsoft Edge \(Chrom \) steht unter Windows 7, Windows 10 und macOS zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="46535-136">Microsoft Edge \(Chromium\) is available on Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="46535-137">Die folgenden Vorteile sind im Lieferumfang enthalten.</span><span class="sxs-lookup"><span data-stu-id="46535-137">The following benefits are included.</span></span>  

*   <span data-ttu-id="46535-138">Anwendungen können über das Symbol " **Installieren** " in der Navigationsleiste direkt im Browser installiert werden.</span><span class="sxs-lookup"><span data-stu-id="46535-138">Applications may be installed directly from within the browser using the **Install** icon in the navigation bar.</span></span>  
    
    :::image type="complex" source="./media/install_pwa_icon.png" alt-text="Installieren des Anwendungs Flyouts und-Symbols" lightbox="./media/install_pwa_icon.png":::
       <span data-ttu-id="46535-140">Installieren des Anwendungs Flyouts und-Symbols</span><span class="sxs-lookup"><span data-stu-id="46535-140">Install application flyout and icon</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="46535-141">Anwendungen können auch über das Menü **Einstellungen**-  >  **apps** installiert, ausgeführt und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="46535-141">Applications may also be installed, run, and managed from the **Settings** > **Apps** menu</span></span>  
    
    :::image type="complex" source="./media/app_menus.png" alt-text="Menüelemente des Programms unter Einstellungen" lightbox="./media/app_menus.png":::
       <span data-ttu-id="46535-143">Menüelemente des Programms unter "Einstellungen"</span><span class="sxs-lookup"><span data-stu-id="46535-143">Application menu items under settings</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="46535-144">Web-Benachrichtigungen sind in das Windows-Benachrichtigungssystem integriert.</span><span class="sxs-lookup"><span data-stu-id="46535-144">Web Notifications are integrated into the Windows notification system</span></span>  
*   <span data-ttu-id="46535-145">Shared Cookie Store mit dem Browserprofil, das die APP installiert hat</span><span class="sxs-lookup"><span data-stu-id="46535-145">Shared cookie store with the browser profile that installed the app</span></span>  
*   <span data-ttu-id="46535-146">Zugriff auf andere Browser Features über das Menü " **Einstellungen" und "mehr** \( `...` \)", einschließlich Zertifikatüberprüfung, Websiteberechtigungen, nach Verfolgungs Schutz und Browsererweiterungen</span><span class="sxs-lookup"><span data-stu-id="46535-146">Access to other browser features using the **Setting and more** \(`...`\) menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>  
*   <span data-ttu-id="46535-147">Vollzugriff auf [Microsoft Edge devtools][DevtoolsProgressiveWebApps] zum Debuggen Ihrer APP</span><span class="sxs-lookup"><span data-stu-id="46535-147">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="46535-148">Um PWAs speziell für Windows 10 anzupassen, die WinRT-API-Anforderungen mit JavaScript erstellen, navigieren Sie zu [spezifische Dokumentation zu den EdgeHTML PWA-Features] [PwaEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="46535-148">To tailor PWAs specifically for Windows 10 that make WinRT API requests using JavaScript, navigate to [documentation specific to the EdgeHTML PWA features][PwaEdgehtmlIndex].</span></span>  <span data-ttu-id="46535-149">Erfahren Sie mehr über das Testen ihrer PWA unter Windows 10 und deren Verteilung im Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="46535-149">Learn more about testing your PWA on Windows 10 and distributing it in the Microsoft Store.</span></span>  

> [!NOTE]
> <span data-ttu-id="46535-150">Weitere Informationen zu PWA-Vorteilen, bevorstehenden Features und kurzen Demos finden Sie unter [Erstellen von 2020-PWA-Sitzungen][BuildVideo].</span><span class="sxs-lookup"><span data-stu-id="46535-150">For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session][BuildVideo].</span></span> 

## <span data-ttu-id="46535-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46535-151">Requirements</span></span>  

<span data-ttu-id="46535-152">Damit Sie als PWA ausgeführt werden kann, sollte Ihre vom Server gehostete Web-App die folgenden Mindestanforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="46535-152">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="46535-153">HTTPS</span><span class="sxs-lookup"><span data-stu-id="46535-153">HTTPS</span></span>][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="46535-154">Schützt Ihre Benutzer, indem eine sichere Verbindung für die Server-oder App-Kommunikation bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="46535-154">Protects your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="46535-155">Dienstmitarbeiter und andere PWA-Technologien funktionieren nur mit Webressourcen, die über eine sichere Verbindung bereitgestellt werden \(oder `localhost` zu Debugging-Zwecken \).</span><span class="sxs-lookup"><span data-stu-id="46535-155">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="46535-156">Service Workers</span><span class="sxs-lookup"><span data-stu-id="46535-156">Service Workers</span></span>][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="46535-157">Verwendet Dienst Arbeitsthreads, um als Netzwerk Proxys zwischen Ihrem Server und der Client-App zu fungieren.</span><span class="sxs-lookup"><span data-stu-id="46535-157">Uses Service Worker threads to act as network proxies between your server and client app.</span></span>  <span data-ttu-id="46535-158">Dienst Arbeitsthreads bieten Offlineunterstützung, Zwischenspeicherung von Ressourcen, Push-Benachrichtigungen, Synchronisierung von Hintergrunddaten und Optimierungen bei der Seiten Ladeleistung.</span><span class="sxs-lookup"><span data-stu-id="46535-158">Service Worker threads provide offline support, resource caching, push notifications, background data sync, and  page-load performance optimizations.</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="46535-159">Web App-Manifest</span><span class="sxs-lookup"><span data-stu-id="46535-159">Web App Manifest</span></span>][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="46535-160">Stellt eine JSON-basierte Metadatendatei bereit, die wichtige Informationen zu Ihrer Web-App beschreibt, damit Windows 10 und andere Hostplattformen ihren PWA-Benutzern eine installierbare, systemeigene App-ähnliche Benutzeroberfläche bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="46535-160">Provides a JSON-based metadata file that describes key information about your web app, so that Windows 10 and other host platforms provide your PWA users with an installable, native app-like experience.</span></span>  <span data-ttu-id="46535-161">Zu den wichtigsten Informationen zählen Symbole, Sprache und URL-Einstiegspunkt.</span><span class="sxs-lookup"><span data-stu-id="46535-161">Key information includes icons, language, and URL entry point.</span></span> 
   :::column-end:::
:::row-end:::  

<span data-ttu-id="46535-162">Um eine tolle PWA zu sein, muss Ihre APP auch die folgenden Voraussetzungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="46535-162">To be a great PWA, your app must also meet the following requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="46535-163">Browserübergreifende Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="46535-163">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="46535-164">Stellen Sie sicher, dass Ihre PWA-Funktion in verschiedenen Browsern und Umgebungen [getestet][MicrosoftDeveloperEdgeToolsRemote] wird.</span><span class="sxs-lookup"><span data-stu-id="46535-164">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="46535-165">Dynamisches Design</span><span class="sxs-lookup"><span data-stu-id="46535-165">Responsive design</span></span>][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="46535-166">Verwendet flüssige Layouts und flexible Bilder.</span><span class="sxs-lookup"><span data-stu-id="46535-166">Employs fluid layouts and flexible images.</span></span>  <span data-ttu-id="46535-167">Das reaktionsfähige Design umfasst die folgenden Elemente, die ihre UX an das Gerät Ihres Benutzers anpassen.</span><span class="sxs-lookup"><span data-stu-id="46535-167">Responsive design includes the following elements that adapt your UX to your user's device.</span></span>  
      
      *   <span data-ttu-id="46535-168">CSS- [Raster][MDNCssGridLayout]</span><span class="sxs-lookup"><span data-stu-id="46535-168">CSS [grid][MDNCssGridLayout]</span></span>  
      *   [<span data-ttu-id="46535-169">Flexbox</span><span class="sxs-lookup"><span data-stu-id="46535-169">flexbox</span></span>][MDNCssFlexibleBoxLayout]  
      *   <span data-ttu-id="46535-170">CSS- [Raster][MDNCssGridLayout] und [Flexbox][MDNCssFlexibleBoxLayout]</span><span class="sxs-lookup"><span data-stu-id="46535-170">CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout]</span></span>  
      *   [<span data-ttu-id="46535-171">Medienabfragen</span><span class="sxs-lookup"><span data-stu-id="46535-171">media queries</span></span>][MDNMediaQueries]  
      *   [<span data-ttu-id="46535-172">reaktionsfähige Bilder</span><span class="sxs-lookup"><span data-stu-id="46535-172">responsive images</span></span>][MDNResponsiveImages]  
      
      <span data-ttu-id="46535-173">Verwendet [Geräte Emulations Tools][DevToolsGuideDeviceModeTestingOtherBrowsers] aus dem Browser, um lokal zu testen oder eine Remote Debugsitzung für [Windows][DevtoolsRemoteDebuggingWindows] oder [Android][DevtoolsRemoteDebuggingIndex] zu erstellen, um direkt auf einem Zielgerät zu testen.</span><span class="sxs-lookup"><span data-stu-id="46535-173">Uses [device emulation tools][DevToolsGuideDeviceModeTestingOtherBrowsers] from your browser to locally test, or create a remote debugging session on [Windows][DevtoolsRemoteDebuggingWindows] or [Android][DevtoolsRemoteDebuggingIndex] to test directly on a target device.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="46535-174">Deep-Linking</span><span class="sxs-lookup"><span data-stu-id="46535-174">Deep linking</span></span>][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="46535-175">Leitet jede Seite Ihrer Website an eine eindeutige URL weiter, damit vorhandene Benutzer Ihnen helfen können, ein noch größeres Publikum durch Social Media Sharing zu engagieren.</span><span class="sxs-lookup"><span data-stu-id="46535-175">Routes each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="46535-176">Validierungs-und Testmethoden</span><span class="sxs-lookup"><span data-stu-id="46535-176">Validation and testing practices</span></span>][Webhint]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="46535-177">Verwendet Code Quality Tools wie [webhint][Webhint] Linter, um die Effizienz, Robustheit, Sicherheit und Barrierefreiheit Ihrer APP zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="46535-177">Uses code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="46535-178">Chrome PWA-Checkliste</span><span class="sxs-lookup"><span data-stu-id="46535-178">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="46535-179">Überprüft Ihre PWA mit der Google-Baseline PWA-Checkliste.</span><span class="sxs-lookup"><span data-stu-id="46535-179">Verifies your PWA against the Google baseline PWA checklist.</span></span>  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> <span data-ttu-id="46535-180">Wenn Sie Ihre PWA in eine [Microsoft Store][MicrosoftDeveloperStore] -Anwendung umwandeln möchten, navigieren Sie zu [Progressive Web Apps (EdgeHTML) im Microsoft Store] [PwaEdgehtmlMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="46535-180">To turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] application, navigate to [Progressive Web Apps (EdgeHTML) in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  
  
## <span data-ttu-id="46535-181">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="46535-181">See also</span></span>  

*   [<span data-ttu-id="46535-182">Mythos Zerschlagung PWAs</span><span class="sxs-lookup"><span data-stu-id="46535-182">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="46535-183">Eine progressive Roadmap für Ihre Progressive Web-App</span><span class="sxs-lookup"><span data-stu-id="46535-183">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="46535-184">Offline Beiträge mit progressiven Web-Apps</span><span class="sxs-lookup"><span data-stu-id="46535-184">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="46535-185">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="46535-185">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="46535-186">Wetten im Web</span><span class="sxs-lookup"><span data-stu-id="46535-186">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="46535-187">Benennen von progressiven Web-Apps</span><span class="sxs-lookup"><span data-stu-id="46535-187">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="46535-188">Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 1)</span><span class="sxs-lookup"><span data-stu-id="46535-188">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="46535-189">Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 2)</span><span class="sxs-lookup"><span data-stu-id="46535-189">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="46535-190">Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 3)</span><span class="sxs-lookup"><span data-stu-id="46535-190">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- links -->  

[DevtoolsRemoteDebuggingIndex]: ../devtools-guide-chromium/remote-debugging/index.md "Erste Schritte mit dem Remotedebuggen von Android-Geräten | Microsoft docs"  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Erste Schritte mit dem Remote Debuggen von Windows 10-Geräten | Microsoft docs"  
[DevToolsGuideDeviceModeTestingOtherBrowsers]: ../devtools-guide-chromium/device-mode/testing-other-browsers.md "Emulieren und Testen anderer Browser | Microsoft docs"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps/index.md "Debuggen von progressiven Web-Apps | Microsoft docs"  
<!--[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "What's new in EdgeHTML 17 | Microsoft Docs"  -->  
<!--[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "What's New in EdgeHTML 14 | Microsoft Docs"  -->  
[PwaEdgehtmlIndex]: .. /edgehtml/Progressive-Web-Apps/Index.MD "Progressive Web-Apps (edgehtml) unter Windows | Microsoft docs "  
[PwaEdgehtmlMicrosoftStore]: .. /edgehtml/Progressive-Web-Apps/Microsoft-Store.MD "Progressive Web-Apps im Microsoft Store | Microsoft docs "
<!--PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps/microsoft-store.md#criteria-for-automatic-submission "Criteria for automatic submission - Progressive Web Apps in the Microsoft Store"  -->  

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Übersicht über Windows Push Notification Services (WNS) | Microsoft docs"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Entwerfen für Xbox und TV | Microsoft docs"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Überlegungen zur Benutzeroberfläche für UWP-Geräte | Microsoft docs"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Was ist eine APP für die universelle Windows-Plattform (UWP)? | Microsoft docs"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Unterstützen Ihrer APP mit Hintergrundaufgaben | Microsoft docs"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Veröffentlichen von Windows-apps und-spielen | Microsoft docs"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Öffnen eines entwicklerkontos | Microsoft docs"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Willkommene Progressive Web-Apps für Microsoft Edge und Windows 10 – Windows-Blogs"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "Hintergrund Synchronisierungs-API – Status der Microsoft Edge-Plattform"  
[MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Web Application Manifest – Status der Microsoft Edge-Plattform"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Sofortiges testen"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Gemischte Realität für Entwickler"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Neuen Microsoft Edge-Browser herunterladen"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Aktivieren oder Deaktivieren der Fokus Unterstützung in Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Ändern von Benachrichtigungseinstellungen in Windows 10"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Grundlegendes zur progressiven Optimierung – eine Liste auseinander"  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "Apps | MDN"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Cross-Browser-Tests | MDN"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "CSS-Layout für flexibles Feld | MDN"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "CSS-Raster Layout | MDN"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "FETCH-API | MDN"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Medienabfragen | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API | MDN"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Auffindbar – Vorteile von Progressive Web App"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Installierbare Vorteile für Progressive Web App"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Vorteile von Linkable-Progressive Web App"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Netzwerk unabhängig – Vorteile von Progressive Web App"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Vorteile für Progressive Web App"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Wieder einbinden – Vorteile von Progressive Web App"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Vorteile von responsive-Progressive Web App"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Vorteile von Safe-Progressive Web App"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Reaktionsfähige Bilder | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker-API | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "Synchronisierungs-Manager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Web App-Manifest | MDN"  

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "PWA-Video"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Eine progressive Roadmap für Ihre Progressive Web-App"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Mythos Zerschlagung PWAs – die neue Edge-Edition"  

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Benennen von progressiven Web-Apps"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Wetten im Web"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Offline Beiträge mit progressiven Web-Apps"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 3)"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Was macht eine gute Progressive Web-App aus? | Web. dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Deep Linking – Wikipedia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS – Wikipedia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Responsive Web Design – Wikipedia"  

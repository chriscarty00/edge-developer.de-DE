---
description: Progressive Web Apps (Chromium) werden nativ auf Windows 10.  Hier finden Sie alles, was Sie als Webentwickler wissen müssen.
title: Progressive Web Apps auf Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: Progressive Web Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: f1f5370af0710927f66c8231274fe307cb3ee2a4
ms.sourcegitcommit: 7f7922dbb6af87ecac1378d18359125770c5b8e5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536809"
---
# <a name="progressive-web-apps-on-windows-overview"></a><span data-ttu-id="157c2-105">Progressive Web Apps on Windows Overview</span><span class="sxs-lookup"><span data-stu-id="157c2-105">Progressive Web Apps on Windows overview</span></span>  

<span data-ttu-id="157c2-106">[Progressive Web Apps][MDNApps] \(PWAs\) bieten Zugriff auf offene Webtechnologien für die plattformübergreifende Interoperabilität und bieten Ihren Benutzern eine systemeigene, app- like-Erfahrung, die für ihre Geräte angepasst ist.</span><span class="sxs-lookup"><span data-stu-id="157c2-106">[Progressive Web Apps][MDNApps] \(PWAs\) provide access to open web technologies for cross-platform interoperability and provide your users with a native, app-like experience customized for their devices.</span></span>  <span data-ttu-id="157c2-107">PWAs sind Websites, die [schrittweise erweitert][AListApartUnderstandingProgressiveEnhancement] werden, um wie systemeigene Apps auf unterstützenden Plattformen zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="157c2-107">PWAs are websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="157c2-108">Die Eigenschaften einer PWA vereinen das Beste aus Web- und nativen Apps.</span><span class="sxs-lookup"><span data-stu-id="157c2-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification-small.png":::  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="discoverablemdnpwaadvantagesdiscoverable"></a><span data-ttu-id="157c2-109">[Discoverable][MDNPwaAdvantagesDiscoverable]</span><span class="sxs-lookup"><span data-stu-id="157c2-109">[Discoverable][MDNPwaAdvantagesDiscoverable]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="installablemdnpwaadvantagesinstallable"></a><span data-ttu-id="157c2-110">[Installierbar][MDNPwaAdvantagesInstallable]</span><span class="sxs-lookup"><span data-stu-id="157c2-110">[Installable][MDNPwaAdvantagesInstallable]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="re-engageablemdnpwaadvantagesreengageable"></a><span data-ttu-id="157c2-111">[Re-engageable][MDNPwaAdvantagesReEngageable]</span><span class="sxs-lookup"><span data-stu-id="157c2-111">[Re-engageable][MDNPwaAdvantagesReEngageable]</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        <span data-ttu-id="157c2-112">Aus Websuchergebnissen und unterstützenden App-Stores</span><span class="sxs-lookup"><span data-stu-id="157c2-112">From web search results and supporting app stores</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="157c2-113">Anheften und Starten vom Startbildschirm, Startmenü, Taskleiste und so weiter</span><span class="sxs-lookup"><span data-stu-id="157c2-113">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="157c2-114">Senden von Pushbenachrichtigungen, auch wenn die App nicht aktiv ist</span><span class="sxs-lookup"><span data-stu-id="157c2-114">Send push notifications, even when the app is not active</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security-small.png":::  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="network-independentmdnpwaadvantagesnetworkindependent"></a><span data-ttu-id="157c2-115">[Netzwerkunabhängig][MDNPwaAdvantagesNetworkIndependent]</span><span class="sxs-lookup"><span data-stu-id="157c2-115">[Network Independent][MDNPwaAdvantagesNetworkIndependent]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="progressivemdnpwaadvantagesprogressive"></a><span data-ttu-id="157c2-116">[Progressiv][MDNPwaAdvantagesProgressive]</span><span class="sxs-lookup"><span data-stu-id="157c2-116">[Progressive][MDNPwaAdvantagesProgressive]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="safemdnpwaadvantagessafe"></a><span data-ttu-id="157c2-117">[Sicher][MDNPwaAdvantagesSafe]</span><span class="sxs-lookup"><span data-stu-id="157c2-117">[Safe][MDNPwaAdvantagesSafe]</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        <span data-ttu-id="157c2-118">Funktioniert offline und unter Bedingungen mit geringem Netzwerk</span><span class="sxs-lookup"><span data-stu-id="157c2-118">Works offline and in low-network conditions</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="157c2-119">Die Benutzererfahrung wird mit den Gerätefunktionen nach oben (oder nach unten) skaliert.</span><span class="sxs-lookup"><span data-stu-id="157c2-119">Experience scales up (or down) with device capabilities</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="157c2-120">Bietet einen sicheren HTTPS-Endpunkt und andere Benutzerschutzmechanismen</span><span class="sxs-lookup"><span data-stu-id="157c2-120">Provides a secure HTTPS endpoint and other user safeguards</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link-small.png":::  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="responsivemdnpwaadvantagesresponsive"></a><span data-ttu-id="157c2-121">[Dynamisch][MDNPwaAdvantagesResponsive]</span><span class="sxs-lookup"><span data-stu-id="157c2-121">[Responsive][MDNPwaAdvantagesResponsive]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="linkablemdnpwaadvantageslinkable"></a><span data-ttu-id="157c2-122">[Linkable][MDNPwaAdvantagesLinkable]</span><span class="sxs-lookup"><span data-stu-id="157c2-122">[Linkable][MDNPwaAdvantagesLinkable]</span></span>  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        <span data-ttu-id="157c2-123">Passt sich an die Bildschirmgröße oder Ausrichtung und Eingabemethode des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="157c2-123">Adapts to the user's screen size or orientation and input method</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="157c2-124">Freigeben und Starten über einen Standardlink</span><span class="sxs-lookup"><span data-stu-id="157c2-124">Share and launch from a standard hyperlink</span></span>  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  

<span data-ttu-id="157c2-125">Erstellen Sie \(oder konvertieren\) Ihre vorhandene Website in PWA, um Ihr Engagement mit Ihren Benutzern zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="157c2-125">Build \(or convert\) your existing website to a PWA to enhance your engagement with your users.</span></span>  <span data-ttu-id="157c2-126">Zu den Verbesserungen gehören Pushbenachrichtigungen, app-like integration und offline support.</span><span class="sxs-lookup"><span data-stu-id="157c2-126">Enhancements include push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="157c2-127">Erstellen Sie weiterhin Ihre Zielgruppe im geöffneten Web, damit Benutzer Ihre PWA Suchen und Teilen von Links ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="157c2-127">Continue to build your audience on the open web for users to discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="157c2-128">Das Beste ist, dass Ihre App mithilfe des Webservercodes aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="157c2-128">Best of all, your app is updated in using your web server code.</span></span>  

## <a name="pwas-on-microsoft-edge-chromium"></a><span data-ttu-id="157c2-129">PWAs on Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="157c2-129">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="157c2-130">Wenn Sie eine Progressive Web App für Webstandard-APIs erstellen, kann Ihre App plattform- und geräteübergreifend bereitgestellt werden und die gerätespezifischen Funktionen nutzen.</span><span class="sxs-lookup"><span data-stu-id="157c2-130">When you build a Progressive Web App targeting web standard APIs, your app may be deployed across platforms and devices and take advantage of the device-specific capabilities as available.</span></span>  <span data-ttu-id="157c2-131">PWAs in Microsoft Edge \(Chromium\) fügen Ihrer Website die folgenden Vorteile hinzu.</span><span class="sxs-lookup"><span data-stu-id="157c2-131">PWAs in Microsoft Edge \(Chromium\) add the following advantages to your website.</span></span>  

*   <span data-ttu-id="157c2-132">Ihre App basiert auf einer standardbasierten Webplattform.</span><span class="sxs-lookup"><span data-stu-id="157c2-132">Your app is built on a standards-based web platform.</span></span>  
*   <span data-ttu-id="157c2-133">Ermöglicht Es Ihren Benutzern, Ihre App direkt über den Browser zu installieren.</span><span class="sxs-lookup"><span data-stu-id="157c2-133">Allows your users to install your app directly from the browser.</span></span>  
*   <span data-ttu-id="157c2-134">Ermöglicht Benutzern die Installation Ihrer App ohne Store Bereitstellung oder Registrierung.</span><span class="sxs-lookup"><span data-stu-id="157c2-134">Allows your users to install your app without a Store-based deployment or registration.</span></span>  
    
<span data-ttu-id="157c2-135">Desktop-PWAs werden auf allen Plattformen unterstützt, Microsoft Edge \(Chromium\) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="157c2-135">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available.</span></span> <span data-ttu-id="157c2-136">Microsoft Edge \(Chromium\) ist unter Windows 7, Windows 10 und macOS verfügbar.</span><span class="sxs-lookup"><span data-stu-id="157c2-136">Microsoft Edge \(Chromium\) is available on Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="157c2-137">Die folgenden Vorteile sind enthalten.</span><span class="sxs-lookup"><span data-stu-id="157c2-137">The following benefits are included.</span></span>  

*   <span data-ttu-id="157c2-138">Apps können direkt im Browser mithilfe \*\*\*\* des Installationssymbols in der Navigationsleiste installiert werden.</span><span class="sxs-lookup"><span data-stu-id="157c2-138">Apps may be installed directly from within the browser using the **Install** icon in the navigation bar.</span></span>  
    
    :::image type="complex" source="./media/install-progressive-web-app-icon.png" alt-text="Installieren von App-Flyout und Symbol" lightbox="./media/install-progressive-web-app-icon.png":::
       <span data-ttu-id="157c2-140">Installieren von App-Flyout und Symbol</span><span class="sxs-lookup"><span data-stu-id="157c2-140">Install app flyout and icon</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="157c2-141">Apps können auch im Menü apps installiert, ausgeführt **und Einstellungen**  >  **verwaltet** werden.</span><span class="sxs-lookup"><span data-stu-id="157c2-141">Apps may also be installed, run, and managed from the **Settings** > **Apps** menu</span></span>  
    
    :::image type="complex" source="./media/app-menus.png" alt-text="App-Menüelemente unter Einstellungen" lightbox="./media/app-menus.png":::
       <span data-ttu-id="157c2-143">App-Menüelemente unter Einstellungen</span><span class="sxs-lookup"><span data-stu-id="157c2-143">App menu items under settings</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="157c2-144">Webbenachrichtigungen sind in das Benachrichtigungssystem Windows integriert</span><span class="sxs-lookup"><span data-stu-id="157c2-144">Web Notifications are integrated into the Windows notification system</span></span>  
*   <span data-ttu-id="157c2-145">Freigegebener Cookiespeicher mit dem Browserprofil, das die App installiert hat</span><span class="sxs-lookup"><span data-stu-id="157c2-145">Shared cookie store with the browser profile that installed the app</span></span>  
*   <span data-ttu-id="157c2-146">Zugriff auf andere Browserfeatures mithilfe des Menüs **Einstellung** und mehr \( \) einschließlich Zertifikatüberprüfung, Websiteberechtigungen, Nachverfolgungsschutz `...` und Browsererweiterungen</span><span class="sxs-lookup"><span data-stu-id="157c2-146">Access to other browser features using the **Setting and more** \(`...`\) menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>  
*   <span data-ttu-id="157c2-147">Vollzugriff auf [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] zum Debuggen Ihrer App</span><span class="sxs-lookup"><span data-stu-id="157c2-147">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  
    
> [!NOTE]
> <span data-ttu-id="157c2-148">Weitere Informationen zu PWA, bevorstehenden Features und kurzen Demos finden Sie unter [Build 2020 PWA Session][BuildVideo].</span><span class="sxs-lookup"><span data-stu-id="157c2-148">For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session][BuildVideo].</span></span> 

## <a name="requirements"></a><span data-ttu-id="157c2-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="157c2-149">Requirements</span></span>  

<span data-ttu-id="157c2-150">Um als PWA ausführen zu können, sollte Ihre vom Server gehostete Web-App die folgenden Mindestanforderungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="157c2-150">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="157c2-151">HTTPS</span><span class="sxs-lookup"><span data-stu-id="157c2-151">HTTPS</span></span>][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="157c2-152">Schützt Ihre Benutzer, indem sie eine sichere Verbindung für die Server- oder App-Kommunikation bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="157c2-152">Protects your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="157c2-153">Service Workers und andere PWA funktionieren nur mit Webressourcen, die über eine sichere Verbindung \(oder aus `localhost` Debugzwecken) bedient werden\).</span><span class="sxs-lookup"><span data-stu-id="157c2-153">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="157c2-154">Service Workers</span><span class="sxs-lookup"><span data-stu-id="157c2-154">Service Workers</span></span>][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="157c2-155">Verwendet Service Worker-Threads, um als Netzwerk-Proxys zwischen Ihrem Server und Ihrer Client-App zu fungieren.</span><span class="sxs-lookup"><span data-stu-id="157c2-155">Uses Service Worker threads to act as network proxies between your server and client app.</span></span>  <span data-ttu-id="157c2-156">Service Worker-Threads bieten Offlineunterstützung, Ressourcen zwischenspeichern, Pushbenachrichtigungen, Hintergrunddatensynchronisierung und Leistungsoptimierungen beim Seitenladen.</span><span class="sxs-lookup"><span data-stu-id="157c2-156">Service Worker threads provide offline support, resource caching, push notifications, background data sync, and  page-load performance optimizations.</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="157c2-157">Web-App-Manifest</span><span class="sxs-lookup"><span data-stu-id="157c2-157">Web App Manifest</span></span>][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="157c2-158">Stellt eine JSON-basierte Metadatendatei bereit, in der wichtige Informationen zu Ihrer Web-App beschrieben werden, sodass Windows 10 und andere Hostplattformen Ihren PWA-Benutzern eine installierbare, systemeigene app-bezogene Besensung bieten.</span><span class="sxs-lookup"><span data-stu-id="157c2-158">Provides a JSON-based metadata file that describes key information about your web app, so that Windows 10 and other host platforms provide your PWA users with an installable, native app-like experience.</span></span>  <span data-ttu-id="157c2-159">Wichtige Informationen umfassen Symbole, Sprache und URL-Einstiegspunkt.</span><span class="sxs-lookup"><span data-stu-id="157c2-159">Key information includes icons, language, and URL entry point.</span></span> 
   :::column-end:::
:::row-end:::  

<span data-ttu-id="157c2-160">Um ein großartiges PWA, muss Ihre App auch die folgenden Anforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="157c2-160">To be a great PWA, your app must also meet the following requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="157c2-161">Browserübergreifende Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="157c2-161">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="157c2-162">Stellen Sie PWA, indem Sie [tests][MicrosoftDeveloperEdgeToolsRemote] in verschiedenen Browsern und Umgebungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="157c2-162">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="157c2-163">Dynamisches Design</span><span class="sxs-lookup"><span data-stu-id="157c2-163">Responsive design</span></span>][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="157c2-164">Verwendet flüssige Layouts und flexible Bilder.</span><span class="sxs-lookup"><span data-stu-id="157c2-164">Employs fluid layouts and flexible images.</span></span>  <span data-ttu-id="157c2-165">Das responsive Design umfasst die folgenden Elemente, die Ihre UX an das Gerät Ihres Benutzers anpassen.</span><span class="sxs-lookup"><span data-stu-id="157c2-165">Responsive design includes the following elements that adapt your UX to your user's device.</span></span>  
      
      *   <span data-ttu-id="157c2-166">[CSS-Raster][MDNCssGridLayout]</span><span class="sxs-lookup"><span data-stu-id="157c2-166">CSS [grid][MDNCssGridLayout]</span></span>  
      *   [<span data-ttu-id="157c2-167">flexbox</span><span class="sxs-lookup"><span data-stu-id="157c2-167">flexbox</span></span>][MDNCssFlexibleBoxLayout]  
      *   <span data-ttu-id="157c2-168">[CSS-Raster][MDNCssGridLayout] und [Flexbox][MDNCssFlexibleBoxLayout]</span><span class="sxs-lookup"><span data-stu-id="157c2-168">CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout]</span></span>  
      *   [<span data-ttu-id="157c2-169">Medienabfragen</span><span class="sxs-lookup"><span data-stu-id="157c2-169">media queries</span></span>][MDNMediaQueries]  
      *   [<span data-ttu-id="157c2-170">Reaktionsschnelle Bilder</span><span class="sxs-lookup"><span data-stu-id="157c2-170">responsive images</span></span>][MDNResponsiveImages]  
          
      <span data-ttu-id="157c2-171">Verwendet [Geräteemulationstools][DevToolsGuideDeviceModeTestingOtherBrowsers] aus Ihrem Browser, um lokal zu testen oder eine Remotedebugsitzung auf [Windows][DevtoolsRemoteDebuggingWindows] oder [Android][DevtoolsRemoteDebuggingIndex] zu erstellen, um direkt auf einem Zielgerät zu testen.</span><span class="sxs-lookup"><span data-stu-id="157c2-171">Uses [device emulation tools][DevToolsGuideDeviceModeTestingOtherBrowsers] from your browser to locally test, or create a remote debugging session on [Windows][DevtoolsRemoteDebuggingWindows] or [Android][DevtoolsRemoteDebuggingIndex] to test directly on a target device.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="157c2-172">Tiefe Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="157c2-172">Deep linking</span></span>][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="157c2-173">Leitet jede Seite Ihrer Website an eine eindeutige URL weiter, sodass vorhandene Benutzer Ihnen helfen können, eine noch breitere Zielgruppe über die Freigabe sozialer Medien zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="157c2-173">Routes each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="157c2-174">Validierungs- und Testmethoden</span><span class="sxs-lookup"><span data-stu-id="157c2-174">Validation and testing practices</span></span>][Webhint]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="157c2-175">Verwendet Codequalitätstools wie den [Webhint-Linter,][Webhint] um die Effizienz, Robustheit, Sicherheit und Barrierefreiheit Ihrer App zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="157c2-175">Uses code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="157c2-176">Chromium PWA Prüfliste</span><span class="sxs-lookup"><span data-stu-id="157c2-176">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="157c2-177">Überprüft Ihre PWA anhand der Google-PWA Prüfliste.</span><span class="sxs-lookup"><span data-stu-id="157c2-177">Verifies your PWA against the Google baseline PWA checklist.</span></span>  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> <span data-ttu-id="157c2-178">Um Ihre PWA in eine [Microsoft Store][MicrosoftDeveloperStore] zu verwandeln, navigieren Sie zu [Progressive Web Apps im Microsoft Store][PwaChromiumMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="157c2-178">To turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] app, navigate to [Progressive Web Apps in the Microsoft Store][PwaChromiumMicrosoftStore].</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="157c2-179">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="157c2-179">See also</span></span>  

*   [<span data-ttu-id="157c2-180">Legendenbusting PWAs</span><span class="sxs-lookup"><span data-stu-id="157c2-180">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="157c2-181">Eine progressive Roadmap für Ihre Progressive Web App</span><span class="sxs-lookup"><span data-stu-id="157c2-181">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="157c2-182">Offline-POSTs mit progressiven Web-Apps</span><span class="sxs-lookup"><span data-stu-id="157c2-182">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="157c2-183">PWA F&A</span><span class="sxs-lookup"><span data-stu-id="157c2-183">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="157c2-184">Wetten im Web</span><span class="sxs-lookup"><span data-stu-id="157c2-184">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="157c2-185">Benennung progressiver Web-Apps</span><span class="sxs-lookup"><span data-stu-id="157c2-185">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="157c2-186">Entwerfen und Erstellen einer progressiven Web-App ohne Framework (Teil 1)</span><span class="sxs-lookup"><span data-stu-id="157c2-186">Designing And Building A Progressive Web App Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart1]  
*   [<span data-ttu-id="157c2-187">Entwerfen und Erstellen einer progressiven Web-App ohne Framework (Teil 2)</span><span class="sxs-lookup"><span data-stu-id="157c2-187">Designing And Building A Progressive Web App Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart2]  
*   [<span data-ttu-id="157c2-188">Entwerfen und Erstellen einer progressiven Web-App ohne Framework (Teil 3)</span><span class="sxs-lookup"><span data-stu-id="157c2-188">Designing And Building A Progressive Web App Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart3]  
    
<!-- links -->  

[DevtoolsRemoteDebuggingIndex]: ../devtools-guide-chromium/remote-debugging/index.md "Erste Schritte mit remote debuggen von Android-Geräten | Microsoft Docs"  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Erste Schritte remote debugging Windows 10 Devices | Microsoft Docs"  
[DevToolsGuideDeviceModeTestingOtherBrowsers]: ../devtools-guide-chromium/device-mode/testing-other-browsers.md "Emulieren und Testen anderer | Microsoft Docs"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps/index.md "Debuggen von Progressive Web Apps | Microsoft Docs"  
[PwaChromiumMicrosoftStore]: ./microsoft-store.md "Veröffentlichen Sie Ihre Progressive Web App im Microsoft Store | Microsoft Docs"

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Windows Übersicht Notification Services (WNS) | Microsoft Docs"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Entwerfen für Xbox- und | Microsoft Docs"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Überlegungen zur Benutzeroberfläche für UWP-| Microsoft Docs"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Was ist eine Universelle Windows (UWP)-App? | Microsoft Docs"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Unterstützen Sie Ihre App mit Hintergrundaufgaben | Microsoft Docs"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Veröffentlichen Windows Apps und | Microsoft Docs"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Öffnen eines Entwicklerkontos | Microsoft Docs"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Willkommen bei Progressive Web Apps zum Microsoft Edge und Windows 10 - Windows Blogs"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "Hintergrundsynchronisierungs-API – Microsoft Edge Plattformstatus"  
[MicrosoftDeveloperEdgePlatformStatusWebAppManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Web-App-Manifest – Microsoft Edge Plattformstatus"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Sofortige Tests"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Mixed Reality für Entwickler"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Download New Microsoft Edge Browser"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Aktivieren oder Deaktivieren der Fokushilfe in Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Ändern von Benachrichtigungseinstellungen in Windows 10"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA F&A"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Grundlegendes zur progressiven Verbesserung – Eine Liste getrennt"  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "apps | MDN"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Browserübergreifende Tests | MDN"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "CSS Flexible Box Layout | MDN"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "CSS Grid Layout | MDN"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Abrufen von API-| MDN"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Medienabfragen | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API-| MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API-| MDN"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Discoverable – Vorteile progressiver Web-Apps"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Installierbar – Vorteile der progressiven Web-App"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Linkable – Vorteile progressiver Web-Apps"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Netzwerkunabhängig – Vorteile der progressiven Web-App"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Progressive – Progressive Web-App-Vorteile"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Re-engageable – Vorteile der progressiven Web-App"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Reaktionsfähig – Progressive Web-App-Vorteile"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Sicher – Vorteile der progressiven Web-App"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Reaktionsschnelle Bilder | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Dienstarbeits-API-| MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager-| MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Web App Manifest | MDN"  

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "PWA Video"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Eine progressive Roadmap für Ihre Progressive Web App"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Legendenbusting PWAs – Die neue Edge Edition"  

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Benennung progressiver Web-Apps"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Wetten im Web"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Offline-POSTs mit progressiven Web-Apps"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 1)"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 2)"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 3)"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Was macht eine gute Progressive Web App aus? | web.dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Tiefe Verknüpfung – Wikipedia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS – Wikipedia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Responsive Web Design – Wikipedia"  

---
description: Progressive Web-Apps werden nativ unter Windows 10 ausgeführt.  Hier finden Sie alles, was Sie als Web-Entwickler wissen müssen.
title: Progressive Web-Apps unter Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/17/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: Progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 482f498e246ee265424f7b80ff3cd67f78501ee2
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583035"
---
# <span data-ttu-id="a068c-105">Progressive Web-Apps unter Windows</span><span class="sxs-lookup"><span data-stu-id="a068c-105">Progressive Web Apps on Windows</span></span>  

<span data-ttu-id="a068c-106">Bei [fortschrittlichen Web-Apps][MDNApps] \ (oder einfach PWAs \) müssen Sie nicht zwischen der Verwendung von Open Web Technologies für die plattformübergreifende Interoperabilität und der Bereitstellung von benutzerdefinierten App-ähnlichen Funktionen für Ihre Geräte entscheiden.</span><span class="sxs-lookup"><span data-stu-id="a068c-106">With [Progressive Web Apps][MDNApps] \(or simply PWAs\), you do not have to decide between using open web technologies for cross-platform interoperability and providing your users with a native app-like experience customized for their devices.</span></span>  <span data-ttu-id="a068c-107">PWAs sind nur Websites, die [schrittweise verbessert][AListApartUnderstandingProgressiveEnhancement] werden, um wie Native apps auf unterstützenden Plattformen zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="a068c-107">PWAs are just websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="a068c-108">Die Eigenschaften einer PWA vereinen das Beste aus Web- und nativen Apps.</span><span class="sxs-lookup"><span data-stu-id="a068c-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        ![Erkennbares Symbol][ImageISearch]
        ### [<span data-ttu-id="a068c-110">Erkennbar</span><span class="sxs-lookup"><span data-stu-id="a068c-110">Discoverable</span></span>][MDNPwaAdvantagesDiscoverable]
        <span data-ttu-id="a068c-111">Aus Websuche-Ergebnissen und unterstützenden App-Stores</span><span class="sxs-lookup"><span data-stu-id="a068c-111">From web search results and supporting app stores</span></span>
    :::column-end:::
    :::column:::
        ![Installierbares Symbol][ImageIPackage]
        ### [<span data-ttu-id="a068c-113">Installierbar</span><span class="sxs-lookup"><span data-stu-id="a068c-113">Installable</span></span>][MDNPwaAdvantagesInstallable]
        <span data-ttu-id="a068c-114">Anheften und starten über den Startbildschirm, Startmenü, Taskleiste usw.</span><span class="sxs-lookup"><span data-stu-id="a068c-114">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>
    :::column-end:::
    :::column:::
        ![Symbol für erneutes einbinden][ImageIPushNotification]
        ### [<span data-ttu-id="a068c-116">Wieder einbinden</span><span class="sxs-lookup"><span data-stu-id="a068c-116">Re-engageable</span></span>][MDNPwaAdvantagesReEngageable]
        <span data-ttu-id="a068c-117">Senden von Push-Benachrichtigungen, auch wenn die APP nicht aktiv ist</span><span class="sxs-lookup"><span data-stu-id="a068c-117">Send push notifications, even when the app is not active</span></span>
    :::column-end:::
    :::column:::
        ![Netzwerk unabhängiges Symbol][ImageIOffline]
        ### [<span data-ttu-id="a068c-119">Netzwerk unabhängig</span><span class="sxs-lookup"><span data-stu-id="a068c-119">Network Independent</span></span>][MDNPwaAdvantagesNetworkIndependent]
        <span data-ttu-id="a068c-120">Funktioniert offline und unter günstigen Netzwerkbedingungen</span><span class="sxs-lookup"><span data-stu-id="a068c-120">Works offline and in low-network conditions</span></span>
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Progressives Symbol][ImageIProgressive]
        ### [<span data-ttu-id="a068c-122">Progressive</span><span class="sxs-lookup"><span data-stu-id="a068c-122">Progressive</span></span>][MDNPwaAdvantagesProgressive]
        <span data-ttu-id="a068c-123">Die Erfahrung skaliert nach oben (oder unten) mit Gerätefunktionen</span><span class="sxs-lookup"><span data-stu-id="a068c-123">Experience scales up (or down) with device capabilities</span></span>
    :::column-end:::
    :::column:::
        ![Sicheres Symbol][ImageISecurity]
        ### [<span data-ttu-id="a068c-125">Sicher</span><span class="sxs-lookup"><span data-stu-id="a068c-125">Safe</span></span>][MDNPwaAdvantagesSafe]
        <span data-ttu-id="a068c-126">Bietet einen sicheren HTTPS-Endpunkt und andere Sicherheitsvorkehrungen für Benutzer</span><span class="sxs-lookup"><span data-stu-id="a068c-126">Provides a secure HTTPS endpoint and other user safeguards</span></span>
    :::column-end:::
    :::column:::
        ![Symbol "reagiert"][ImageIResponsive]
        ### [<span data-ttu-id="a068c-128">Dynamisch</span><span class="sxs-lookup"><span data-stu-id="a068c-128">Responsive</span></span>][MDNPwaAdvantagesResponsive]
        <span data-ttu-id="a068c-129">Passt sich der Bildschirmgröße des Benutzers oder der Ausrichtung und Eingabemethode an.</span><span class="sxs-lookup"><span data-stu-id="a068c-129">Adapts to the user's screen size or orientation and input method</span></span>
    :::column-end:::
    :::column:::
        ![Verknüpfungssymbol][ImageILink]
        ### [<span data-ttu-id="a068c-131">Linkbar</span><span class="sxs-lookup"><span data-stu-id="a068c-131">Linkable</span></span>][MDNPwaAdvantagesLinkable]
        <span data-ttu-id="a068c-132">Freigeben und starten von einem Standardhyperlink</span><span class="sxs-lookup"><span data-stu-id="a068c-132">Share and launch from a standard hyperlink</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="a068c-133">Durch das Erstellen oder Konvertieren Ihrer vorhandenen Website in eine PWA können Sie Ihre vorhandene Zielgruppe mithilfe von Push-Benachrichtigungen, App-ähnlicher Integration und Offlineunterstützung besser nutzen.</span><span class="sxs-lookup"><span data-stu-id="a068c-133">By building or converting your existing site to a PWA, you engage better with your existing audience using push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="a068c-134">Gleichzeitig sollten Sie Ihre Zielgruppe im geöffneten Web weiterentwickeln, da Benutzer ihre PWA-Suche und Link Freigabe entdecken.</span><span class="sxs-lookup"><span data-stu-id="a068c-134">At the same time, you should continue to build your audience on the open web, as users discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="a068c-135">Das beste daran ist, dass Sie Ihre APP aktualisieren können, indem Sie einfach Ihren Webservercode aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a068c-135">Best of all, you may update your app by simply updating your web server code.</span></span>  

## <span data-ttu-id="a068c-136">PWAs auf Microsoft Edge (Chrom)</span><span class="sxs-lookup"><span data-stu-id="a068c-136">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="a068c-137">Wenn Sie eine progressive Web App für Webstandard-APIs erstellen, kann Ihre Anwendung plattformübergreifend und auf Geräten bereitgestellt werden und die gerätespezifischen Funktionen wie verfügbar nutzen.</span><span class="sxs-lookup"><span data-stu-id="a068c-137">When you build a Progressive Web App targeting web standard APIs, your application may be deployed across platforms and devices and take advantage of the device specific capabilities as available.</span></span>  <span data-ttu-id="a068c-138">PWAs in Microsoft Edge \ (Chrom \) sind vollständig auf der Grundlage einer webplattforms-Perspektive und ermöglichen Benutzern, die APP direkt aus dem Browser zu installieren, ohne dass eine Store-basierte Bereitstellung oder Registrierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a068c-138">PWAs in Microsoft Edge \(Chromium\) are completely standards-based from a web platform perspective and enable users to install the app directly from within the browser without the need for Store-based deployment or registration.</span></span>  <span data-ttu-id="a068c-139">Desktop-PWAs werden auf allen Plattformen unterstützt, die Microsoft Edge \ (Chrom \) zur Verfügung steht, einschließlich Windows 7, Windows 10 und macOS.</span><span class="sxs-lookup"><span data-stu-id="a068c-139">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available, including Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="a068c-140">Weitere Vorteile sind:</span><span class="sxs-lookup"><span data-stu-id="a068c-140">Other benefits include:</span></span>  

*   <span data-ttu-id="a068c-141">Anwendungen können direkt im Browser über das Symbol " **Installieren** " in der Navigationsleiste installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a068c-141">Applications may be installed directly from within the browser via the **Install** icon in the navigation bar.</span></span>  
    
    ![Installieren des Anwendungs Flyouts und-Symbols][ImageInstallPwa]  
    
*   <span data-ttu-id="a068c-143">Anwendungen können auch über das Menü **Einstellungen**-  >  **apps** installiert, ausgeführt und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a068c-143">Applications may also be installed, run and managed from the **Settings** > **Apps** menu</span></span>  
    
    ![Menüelemente des Programms unter "Einstellungen"][ImageAppMenus]  

*   <span data-ttu-id="a068c-145">Web-Benachrichtigungen sind in das Windows-Benachrichtigungssystem integriert.</span><span class="sxs-lookup"><span data-stu-id="a068c-145">Web Notifications are integrated into the Windows notification system</span></span>
*   <span data-ttu-id="a068c-146">Shared Cookie Store mit dem Browserprofil, das die APP installiert hat</span><span class="sxs-lookup"><span data-stu-id="a068c-146">Shared cookie store with the browser profile that installed the app</span></span>
*   <span data-ttu-id="a068c-147">Zugriff auf andere Browser Features über das `...` Menü, einschließlich Zertifikatüberprüfung, Websiteberechtigungen, nach Verfolgungs Schutz und Browsererweiterungen</span><span class="sxs-lookup"><span data-stu-id="a068c-147">Access to other browser features via the `...` menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>
*   <span data-ttu-id="a068c-148">Vollzugriff auf [Microsoft Edge devtools][DevtoolsProgressiveWebApps] zum Debuggen Ihrer APP</span><span class="sxs-lookup"><span data-stu-id="a068c-148">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="a068c-149">Informationen zum Anpassen von PWAs speziell für Windows 10, die WinRT-API-Anforderungen mithilfe von JavaScript erstellen, finden Sie in der [Dokumentation zu den EdgeHTML-PWA-Features][PwaEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="a068c-149">To tailor PWAs specifically for Windows 10 that make WinRT API requests using JavaScript, see the [documentation specific to the EdgeHTML PWA features][PwaEdgehtmlIndex].</span></span>  <span data-ttu-id="a068c-150">Erfahren Sie mehr über das Testen ihrer PWA unter Windows 10 und deren Verteilung im Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="a068c-150">Learn more about testing your PWA on Windows 10 and distributing it in the Microsoft Store.</span></span>  

## <span data-ttu-id="a068c-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a068c-151">Requirements</span></span>  

<span data-ttu-id="a068c-152">Damit Sie als PWA ausgeführt werden kann, sollte Ihre vom Server gehostete Web-App die folgenden Mindestanforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="a068c-152">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

|  | <span data-ttu-id="a068c-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a068c-153">Requirement</span></span> | <span data-ttu-id="a068c-154">Details</span><span class="sxs-lookup"><span data-stu-id="a068c-154">Details</span></span> | 
|:--- |:--- |:--- |  
| <span data-ttu-id="a068c-155">X</span><span class="sxs-lookup"><span data-stu-id="a068c-155">X</span></span> | [<span data-ttu-id="a068c-156">HTTPS</span><span class="sxs-lookup"><span data-stu-id="a068c-156">HTTPS</span></span>][WikiHttps] | <span data-ttu-id="a068c-157">Schützen Sie Ihre Benutzer, indem Sie eine sichere Verbindung für die Server-oder App-Kommunikation bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a068c-157">Protect your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="a068c-158">Dienstmitarbeiter und andere PWA-Technologien funktionieren nur mit Webressourcen, die über eine sichere Verbindung bereitgestellt werden \ (oder `localhost` zu Debugging-Zwecken \).</span><span class="sxs-lookup"><span data-stu-id="a068c-158">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  |  
| <span data-ttu-id="a068c-159">X</span><span class="sxs-lookup"><span data-stu-id="a068c-159">X</span></span> | [<span data-ttu-id="a068c-160">Dienstmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="a068c-160">Service Workers</span></span>][MDNServiceWorkerApi] | <span data-ttu-id="a068c-161">Verwenden Sie Dienst Arbeitsthreads, um als Netzwerk Proxys zwischen Ihrem Server und der Client-App zu fungieren, um Offline-Unterstützung, Zwischenspeicherung von Ressourcen, Push-Benachrichtigungen, Synchronisierung von Hintergrunddaten und Optimierungen beim Laden von Seiten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a068c-161">Use Service Worker threads to act as network proxies between your server and client app in order to provide offline support, resource caching, push notifications, background data sync, and  page load perf optimizations.</span></span>  |  
| <span data-ttu-id="a068c-162">X</span><span class="sxs-lookup"><span data-stu-id="a068c-162">X</span></span> | [<span data-ttu-id="a068c-163">Web App-Manifest</span><span class="sxs-lookup"><span data-stu-id="a068c-163">Web App Manifest</span></span>][MDNWebAppManifest] | <span data-ttu-id="a068c-164">Stellen Sie eine JSON-basierte Metadatendatei bereit, die wichtige Informationen zu Ihrer Web-App beschreibt \ (wie Symbole, Sprache und URL-Einstiegspunkt \), damit Windows 10 und andere Hostplattformen ihren PWA-Benutzern eine installierbare, systemeigene App-ähnliche Benutzeroberfläche bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="a068c-164">Provide a JSON-based metadata file describing key information about your web app \(such as icons, language, and URL entry point\), so that Windows 10 and other host platforms are able to provide your PWA users with an installable, native app-like experience.</span></span>  |  

<span data-ttu-id="a068c-165">Um eine tolle PWA zu sein, muss Ihre APP auch die folgenden Voraussetzungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="a068c-165">To be a great PWA, your app must also meet the following requirements.</span></span>  

|  | <span data-ttu-id="a068c-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a068c-166">Requirement</span></span> | <span data-ttu-id="a068c-167">Details</span><span class="sxs-lookup"><span data-stu-id="a068c-167">Details</span></span> | 
|:--- |:--- |:--- |  
| <span data-ttu-id="a068c-168">X</span><span class="sxs-lookup"><span data-stu-id="a068c-168">X</span></span> | [<span data-ttu-id="a068c-169">Browserübergreifende Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="a068c-169">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting] | <span data-ttu-id="a068c-170">Stellen Sie sicher, dass Ihre PWA-Funktion in verschiedenen Browsern und Umgebungen [getestet][MicrosoftDeveloperEdgeToolsRemote] wird.</span><span class="sxs-lookup"><span data-stu-id="a068c-170">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  |  
| <span data-ttu-id="a068c-171">X</span><span class="sxs-lookup"><span data-stu-id="a068c-171">X</span></span> | [<span data-ttu-id="a068c-172">Dynamisches Design</span><span class="sxs-lookup"><span data-stu-id="a068c-172">Responsive design</span></span>][WikiResponsiveWebDesign] | <span data-ttu-id="a068c-173">Verwenden Sie flüssige Layouts und flexible Bilder mit CSS- [Raster][MDNCssGridLayout], [Flexbox][MDNCssFlexibleBoxLayout], CSS- [Raster][MDNCssGridLayout] und [Flexbox][MDNCssFlexibleBoxLayout] , [medienabfragen][MDNMediaQueries]und reaktionsfähigen [Bildern][MDNResponsiveImages] , um Ihre UX an das Gerät Ihres Benutzers anzupassen.</span><span class="sxs-lookup"><span data-stu-id="a068c-173">Employ fluid layouts and flexible images with CSS [grid][MDNCssGridLayout], [flexbox][MDNCssFlexibleBoxLayout], CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout] , [media queries][MDNMediaQueries], and [responsive images][MDNResponsiveImages] to adapt your UX to your user's device.</span></span>  <span data-ttu-id="a068c-174">Verwenden Sie die [Geräte-Emulations Tools][DevToolsGuide|::ref1::|] Ihres Browsers, um lokal zu testen, oder richten Sie eine [Remote Debugsitzung][DevToolsProtocolClientsEdgeDevToolsPreview] ein, um direkt auf einem Zielgerät zu testen.</span><span class="sxs-lookup"><span data-stu-id="a068c-174">Use [device emulation tools][DevToolsGuide|::ref1::|] from your browser to test locally, or set up a [remote debugging session][DevToolsProtocolClientsEdgeDevToolsPreview] to test directly on a target device.</span></span>  |  
| <span data-ttu-id="a068c-175">X</span><span class="sxs-lookup"><span data-stu-id="a068c-175">X</span></span> | [<span data-ttu-id="a068c-176">Deep-Linking</span><span class="sxs-lookup"><span data-stu-id="a068c-176">Deep linking</span></span>][WikiDeepLinking] | <span data-ttu-id="a068c-177">Leiten Sie jede Seite Ihrer Website an eine eindeutige URL weiter, damit vorhandene Benutzer Ihnen helfen können, ein noch größeres Publikum durch Social Media Sharing zu engagieren.</span><span class="sxs-lookup"><span data-stu-id="a068c-177">Route each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  |  
| <span data-ttu-id="a068c-178">X</span><span class="sxs-lookup"><span data-stu-id="a068c-178">X</span></span> | [<span data-ttu-id="a068c-179">Bewährte Verfahren</span><span class="sxs-lookup"><span data-stu-id="a068c-179">Best practices</span></span>][Webhint] | <span data-ttu-id="a068c-180">Verwenden Sie Code Quality Tools wie [webhint][Webhint] Linter, um die Effizienz, Robustheit, Sicherheit und Barrierefreiheit Ihrer APP zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="a068c-180">Use code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  |  
| <span data-ttu-id="a068c-181">X</span><span class="sxs-lookup"><span data-stu-id="a068c-181">X</span></span> | [<span data-ttu-id="a068c-182">Chrome PWA-Checkliste</span><span class="sxs-lookup"><span data-stu-id="a068c-182">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist] | <span data-ttu-id="a068c-183">Überprüfen Sie Ihre PWA mit der Google-Baseline-PWA-Checkliste.</span><span class="sxs-lookup"><span data-stu-id="a068c-183">Check your PWA against the Google baseline PWA checklist.</span></span>  |  

<span data-ttu-id="a068c-184">Wenn Sie Ihre PWA in eine [Microsoft Store][MicrosoftDeveloperStore] -Anwendung umwandeln möchten, wechseln Sie zur Dokumentation zur [Progressive Web Apps (EdgeHTML)][PwaEdgehtmlMicrosoftStore] .</span><span class="sxs-lookup"><span data-stu-id="a068c-184">If you want to turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] application, head to the [Progressive Web Apps (EdgeHTML)][PwaEdgehtmlMicrosoftStore] documentation.</span></span>  

## <span data-ttu-id="a068c-185">Aktuelle Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="a068c-185">Current availability</span></span>  

<span data-ttu-id="a068c-186">Browser Modul-Unterstützung für Progressive Web App-Anforderungen für eine Reihe von Architekturkomponenten, wobei die Netzwerkinfrastruktur, die der [Fetch-API][MDNFetchApi]zugrunde liegt, am bedeutendsten ist.</span><span class="sxs-lookup"><span data-stu-id="a068c-186">Browser engine support for Progressive Web App requests for a number of architectural components, the most significant being the networking infrastructure underlying the [Fetch API][MDNFetchApi].</span></span>  

<span data-ttu-id="a068c-187">Für Microsoft Edge \ (Chromium \) enthält die Browser Plattform vollständige Unterstützung für diese Features, die auf allen Geräten funktionieren, auf denen Microsoft Edge \ (Chrom \) unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a068c-187">For Microsoft Edge \(Chromium\), the browser platform includes full support for these features that work across devices where Microsoft Edge \(Chromium\) is supported.</span></span>  

<!-- image links -->  

[ImageISearch]: media/i_search.png  
[ImageIPackage]: media/i_package.png  
[ImageIPushNotification]: media/i_push-notification.png  
[ImageIOffline]: media/i_offline.png  
[ImageIProgressive]: media/i_progressive.png  
[ImageISecurity]: media/i_security.png  
[ImageIResponsive]: media/i_responsive.png  
[ImageILink]: media/i_link.png  

[ImageInstallPwa]: ./media/Install_PWA.png  
[ImageAppMenus]: ./media/App_menus.png  

<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge devtools Preview – devtools-Protokoll Clients"  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Emulation"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps.md "Debuggen von progressiven Web-Apps"  
[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "Neuerungen in EdgeHTML 17"  
[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "Neuerungen in EdgeHTML 14"  
[PwaEdgehtmlIndex]: ../progressive-web-apps-edgehtml/index.md "Progressive Web-Apps (EdgeHTML) unter Windows"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps-edgehtml/microsoft-store.md "Progressive Web-Apps im Microsoft Store"
<!--PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps-edgehtml/microsoft-store.md#criteria-for-automatic-submission "Criteria for automatic submission - Progressive Web Apps in the Microsoft Store"  -->  

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Windows-Push-Benachrichtigungsdienste \ (WNS \) – Übersicht"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Entwerfen für Xbox und Fernsehgeräte"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Überlegungen zur Benutzeroberfläche für UWP-Geräte"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Was ist eine APP für die universelle Windows-Plattform (UWP)?"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Unterstützen Ihrer APP mit Hintergrundaufgaben"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Veröffentlichen von Windows-apps und-spielen"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Öffnen eines entwicklerkontos"  

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

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Was macht eine gute Progressive Web-App aus? | Web. dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Deep Linking – Wikipedia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS – Wikipedia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Responsive Web Design – Wikipedia"  

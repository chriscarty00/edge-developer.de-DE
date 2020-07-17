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
ms.openlocfilehash: 90740bac07ebfd74f89e2524e6955621e1b09b05
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882807"
---
# Progressive Web-Apps unter Windows  

Bei [fortschrittlichen Web-Apps][MDNApps] \ (oder einfach PWAs \) müssen Sie nicht zwischen der Verwendung von Open Web Technologies für die plattformübergreifende Interoperabilität und der Bereitstellung von benutzerdefinierten App-ähnlichen Funktionen für Ihre Geräte entscheiden.  PWAs sind nur Websites, die [schrittweise verbessert][AListApartUnderstandingProgressiveEnhancement] werden, um wie Native apps auf unterstützenden Plattformen zu funktionieren.  Die Eigenschaften einer PWA vereinen das Beste aus Web- und nativen Apps.  

:::row:::
    :::column:::
        ![Erkennbares Symbol][ImageISearch]
        ### [Erkennbar][MDNPwaAdvantagesDiscoverable]
        Aus Websuche-Ergebnissen und unterstützenden App-Stores
    :::column-end:::
    :::column:::
        ![Installierbares Symbol][ImageIPackage]
        ### [Installierbar][MDNPwaAdvantagesInstallable]
        Anheften und starten über den Startbildschirm, Startmenü, Taskleiste usw.
    :::column-end:::
    :::column:::
        ![Symbol für erneutes einbinden][ImageIPushNotification]
        ### [Wieder einbinden][MDNPwaAdvantagesReEngageable]
        Senden von Push-Benachrichtigungen, auch wenn die APP nicht aktiv ist
    :::column-end:::
    :::column:::
        ![Netzwerk unabhängiges Symbol][ImageIOffline]
        ### [Netzwerk unabhängig][MDNPwaAdvantagesNetworkIndependent]
        Funktioniert offline und unter günstigen Netzwerkbedingungen
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Progressives Symbol][ImageIProgressive]
        ### [Progressive][MDNPwaAdvantagesProgressive]
        Die Erfahrung skaliert nach oben (oder unten) mit Gerätefunktionen
    :::column-end:::
    :::column:::
        ![Sicheres Symbol][ImageISecurity]
        ### [Sicher][MDNPwaAdvantagesSafe]
        Bietet einen sicheren HTTPS-Endpunkt und andere Sicherheitsvorkehrungen für Benutzer
    :::column-end:::
    :::column:::
        ![Symbol "reagiert"][ImageIResponsive]
        ### [Dynamisch][MDNPwaAdvantagesResponsive]
        Passt sich der Bildschirmgröße des Benutzers oder der Ausrichtung und Eingabemethode an.
    :::column-end:::
    :::column:::
        ![Verknüpfungssymbol][ImageILink]
        ### [Linkbar][MDNPwaAdvantagesLinkable]
        Freigeben und starten von einem Standardhyperlink
    :::column-end:::
:::row-end:::

Durch das Erstellen oder Konvertieren Ihrer vorhandenen Website in eine PWA können Sie Ihre vorhandene Zielgruppe mithilfe von Push-Benachrichtigungen, App-ähnlicher Integration und Offlineunterstützung besser nutzen.  Gleichzeitig sollten Sie Ihre Zielgruppe im geöffneten Web weiterentwickeln, da Benutzer ihre PWA-Suche und Link Freigabe entdecken.  Das beste daran ist, dass Sie Ihre APP aktualisieren können, indem Sie einfach Ihren Webservercode aktualisieren.  

## PWAs auf Microsoft Edge (Chrom)  

Wenn Sie eine progressive Web App für Webstandard-APIs erstellen, kann Ihre Anwendung plattformübergreifend und auf Geräten bereitgestellt werden und die gerätespezifischen Funktionen wie verfügbar nutzen.  PWAs in Microsoft Edge \ (Chrom \) sind vollständig auf der Grundlage einer webplattforms-Perspektive und ermöglichen Benutzern, die APP direkt aus dem Browser zu installieren, ohne dass eine Store-basierte Bereitstellung oder Registrierung erforderlich ist.  Desktop-PWAs werden auf allen Plattformen unterstützt, die Microsoft Edge \ (Chrom \) zur Verfügung steht, einschließlich Windows 7, Windows 10 und macOS.  Weitere Vorteile sind:  

*   Anwendungen können direkt im Browser über das Symbol " **Installieren** " in der Navigationsleiste installiert werden.  
    
    ![Installieren des Anwendungs Flyouts und-Symbols][ImageInstallPwa]  
    
*   Anwendungen können auch über das Menü **Einstellungen**-  >  **apps** installiert, ausgeführt und verwaltet werden.  
    
    ![Menüelemente des Programms unter "Einstellungen"][ImageAppMenus]  

*   Web-Benachrichtigungen sind in das Windows-Benachrichtigungssystem integriert.
*   Shared Cookie Store mit dem Browserprofil, das die APP installiert hat
*   Zugriff auf andere Browser Features über das `...` Menü, einschließlich Zertifikatüberprüfung, Websiteberechtigungen, nach Verfolgungs Schutz und Browsererweiterungen
*   Vollzugriff auf [Microsoft Edge devtools][DevtoolsProgressiveWebApps] zum Debuggen Ihrer APP  

> [!IMPORTANT]
> Informationen zum Anpassen von PWAs speziell für Windows 10, die WinRT-API-Anforderungen mithilfe von JavaScript erstellen, finden Sie in der [Dokumentation zu den EdgeHTML-PWA-Features][PwaEdgehtmlIndex].  Erfahren Sie mehr über das Testen ihrer PWA unter Windows 10 und deren Verteilung im Microsoft Store.  

> [!NOTE]
> Schauen Sie sich die [Build 2020 PWA-Sitzung][BuildVideo] an, um einen Überblick über die Vorteile von PWA, bevorstehende Features und kurze Demos zu finden. 

## Anforderungen  

Damit Sie als PWA ausgeführt werden kann, sollte Ihre vom Server gehostete Web-App die folgenden Mindestanforderungen erfüllen:  

| Anforderung | Details | 
|:--- |:--- |  
| [HTTPS][WikiHttps] | Schützen Sie Ihre Benutzer, indem Sie eine sichere Verbindung für die Server-oder App-Kommunikation bereitstellen.  Dienstmitarbeiter und andere PWA-Technologien funktionieren nur mit Webressourcen, die über eine sichere Verbindung bereitgestellt werden \ (oder `localhost` zu Debugging-Zwecken \).  |  
| [Service Workers][MDNServiceWorkerApi] | Verwenden Sie Dienst Arbeitsthreads, um als Netzwerk Proxys zwischen Ihrem Server und der Client-App zu fungieren, um Offline-Unterstützung, Zwischenspeicherung von Ressourcen, Push-Benachrichtigungen, Synchronisierung von Hintergrunddaten und Optimierungen beim Laden von Seiten zu ermöglichen.  |  
| [Web App-Manifest][MDNWebAppManifest] | Stellen Sie eine JSON-basierte Metadatendatei bereit, die wichtige Informationen zu Ihrer Web-App beschreibt \ (wie Symbole, Sprache und URL-Einstiegspunkt \), damit Windows 10 und andere Hostplattformen ihren PWA-Benutzern eine installierbare, systemeigene App-ähnliche Benutzeroberfläche bereitstellen können.  |  

Um eine tolle PWA zu sein, muss Ihre APP auch die folgenden Voraussetzungen erfüllen.  

| Anforderung | Details | 
|:--- |:--- |  
| [Browserübergreifende Kompatibilität][MDNCrossBrowserTesting] | Stellen Sie sicher, dass Ihre PWA-Funktion in verschiedenen Browsern und Umgebungen [getestet][MicrosoftDeveloperEdgeToolsRemote] wird.  |  
| [Dynamisches Design][WikiResponsiveWebDesign] | Verwenden Sie flüssige Layouts und flexible Bilder mit CSS- [Raster][MDNCssGridLayout], [Flexbox][MDNCssFlexibleBoxLayout], CSS- [Raster][MDNCssGridLayout] und [Flexbox][MDNCssFlexibleBoxLayout] , [medienabfragen][MDNMediaQueries]und reaktionsfähigen [Bildern][MDNResponsiveImages] , um Ihre UX an das Gerät Ihres Benutzers anzupassen.  Verwenden Sie die [Geräte-Emulations Tools][DevToolsGuide|::ref1::|] Ihres Browsers, um lokal zu testen, oder richten Sie eine [Remote Debugsitzung][DevToolsProtocolClientsEdgeDevToolsPreview] ein, um direkt auf einem Zielgerät zu testen.  |  
| [Deep-Linking][WikiDeepLinking] | Leiten Sie jede Seite Ihrer Website an eine eindeutige URL weiter, damit vorhandene Benutzer Ihnen helfen können, ein noch größeres Publikum durch Social Media Sharing zu engagieren.  |  
| [Bewährte Verfahren][Webhint] | Verwenden Sie Code Quality Tools wie [webhint][Webhint] Linter, um die Effizienz, Robustheit, Sicherheit und Barrierefreiheit Ihrer APP zu optimieren.  |  
| [Chrome PWA-Checkliste][WebDevGoodPwaChecklist] | Überprüfen Sie Ihre PWA mit der Google-Baseline-PWA-Checkliste.  |  

Wenn Sie Ihre PWA in eine [Microsoft Store][MicrosoftDeveloperStore] -Anwendung umwandeln möchten, wechseln Sie zur Dokumentation zur [Progressive Web Apps (EdgeHTML)][PwaEdgehtmlMicrosoftStore] .  
  

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

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "PWA-Video"

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Was macht eine gute Progressive Web-App aus? | Web. dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Deep Linking – Wikipedia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS – Wikipedia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Responsive Web Design – Wikipedia"  

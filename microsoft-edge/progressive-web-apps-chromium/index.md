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
# Übersicht über Progressive Web-Apps unter Windows  

[Progressive Web-Apps][MDNApps] \ (PWAs \) bieten Zugriff auf Open Web-Technologien für die plattformübergreifende Interoperabilität und bieten ihren Benutzern eine systemeigene, App-ähnliche Benutzeroberfläche, die auf Ihre Geräte zugeschnitten ist.  PWAs sind Websites, die [schrittweise verbessert][AListApartUnderstandingProgressiveEnhancement] werden, um wie Native apps auf unterstützenden Plattformen zu funktionieren.  Die Eigenschaften einer PWA vereinen das Beste aus Web- und nativen Apps.  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search.png":::
        ### [Erkennbar][MDNPwaAdvantagesDiscoverable]
        Aus Websuche-Ergebnissen und unterstützenden App-Stores
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package.png":::
        ### [Installierbar][MDNPwaAdvantagesInstallable]
        Anheften und starten über den Startbildschirm, Startmenü, Taskleiste usw.
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification.png":::
        ### [Wieder einbinden][MDNPwaAdvantagesReEngageable]
        Senden von Push-Benachrichtigungen, auch wenn die APP nicht aktiv ist
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline.png":::
        ### [Netzwerk unabhängig][MDNPwaAdvantagesNetworkIndependent]
        Funktioniert offline und unter günstigen Netzwerkbedingungen
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive.png":::
        ### [Progressive][MDNPwaAdvantagesProgressive]
        Die Erfahrung skaliert nach oben (oder unten) mit Gerätefunktionen
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security.png":::
        ### [Sicher][MDNPwaAdvantagesSafe]
        Bietet einen sicheren HTTPS-Endpunkt und andere Sicherheitsvorkehrungen für Benutzer
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive.png":::
        ### [Dynamisch][MDNPwaAdvantagesResponsive]
        Passt sich der Bildschirmgröße des Benutzers oder der Ausrichtung und Eingabemethode an.
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link.png":::
        ### [Linkbar][MDNPwaAdvantagesLinkable]
        Freigeben und starten von einem Standardhyperlink
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


Erstellen Sie Ihre vorhandene Website in eine PWA, um die Interaktion mit ihren Benutzern zu verbessern.  Zu den Verbesserungen gehören Push-Benachrichtigungen, App-ähnliche Integration und Offlineunterstützung.  Bauen Sie Ihre Zielgruppe im geöffneten Web weiter auf, damit die Benutzer ihre PWA-Suche und Link Freigabe entdecken können.  Das beste daran ist, dass Ihre APP mit dem Webservercode aktualisiert wird.  

## PWAs auf Microsoft Edge (Chrom)  

Wenn Sie eine progressive Web App für Webstandard-APIs erstellen, kann Ihre Anwendung plattformübergreifend und auf Geräten bereitgestellt werden und die gerätespezifischen Funktionen wie verfügbar nutzen.  PWAs in Microsoft Edge \ (Chrom \) fügen Sie Ihrer Website die folgenden Vorteile hinzu.  

*   Ihre APP ist auf einer auf Standards basierenden Web-Plattform aufgebaut.  
*   Ermöglicht es Ihren Benutzern, Ihre APP direkt aus dem Browser zu installieren.  
*   Ermöglicht es Ihren Benutzern, Ihre APP ohne Store-basierte Bereitstellung oder Registrierung zu installieren.  
    
Desktop-PWAs werden auf allen Plattformen unterstützt, die Microsoft Edge \ (Chrom \) verfügbar ist. Microsoft Edge \ (Chrom \) steht unter Windows 7, Windows 10 und macOS zur Verfügung.  Die folgenden Vorteile sind im Lieferumfang enthalten.  

*   Anwendungen können über das Symbol " **Installieren** " in der Navigationsleiste direkt im Browser installiert werden.  
    
    :::image type="complex" source="./media/install_pwa_icon.png" alt-text="Installieren des Anwendungs Flyouts und-Symbols" lightbox="./media/install_pwa_icon.png":::
       Installieren des Anwendungs Flyouts und-Symbols  
    :::image-end:::  
    
*   Anwendungen können auch über das Menü **Einstellungen**-  >  **apps** installiert, ausgeführt und verwaltet werden.  
    
    :::image type="complex" source="./media/app_menus.png" alt-text="Menüelemente des Programms unter Einstellungen" lightbox="./media/app_menus.png":::
       Menüelemente des Programms unter "Einstellungen"  
    :::image-end:::  
    
*   Web-Benachrichtigungen sind in das Windows-Benachrichtigungssystem integriert.  
*   Shared Cookie Store mit dem Browserprofil, das die APP installiert hat  
*   Zugriff auf andere Browser Features über das Menü " **Einstellungen" und "mehr** \ ( `...` \)", einschließlich Zertifikatüberprüfung, Websiteberechtigungen, nach Verfolgungs Schutz und Browsererweiterungen  
*   Vollzugriff auf [Microsoft Edge devtools][DevtoolsProgressiveWebApps] zum Debuggen Ihrer APP  
    
> [!IMPORTANT]
> Um PWAs speziell für Windows 10 anzupassen, die WinRT-API-Anforderungen mit JavaScript erstellen, navigieren Sie zu [spezifische Dokumentation zu den EdgeHTML PWA-Features] [PwaEdgehtmlIndex].  Erfahren Sie mehr über das Testen ihrer PWA unter Windows 10 und deren Verteilung im Microsoft Store.  

> [!NOTE]
> Weitere Informationen zu PWA-Vorteilen, bevorstehenden Features und kurzen Demos finden Sie unter [Erstellen von 2020-PWA-Sitzungen][BuildVideo]. 

## Anforderungen  

Damit Sie als PWA ausgeführt werden kann, sollte Ihre vom Server gehostete Web-App die folgenden Mindestanforderungen erfüllen:  

:::row:::
   :::column span="1":::
      [HTTPS][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      Schützt Ihre Benutzer, indem eine sichere Verbindung für die Server-oder App-Kommunikation bereitgestellt wird.  Dienstmitarbeiter und andere PWA-Technologien funktionieren nur mit Webressourcen, die über eine sichere Verbindung bereitgestellt werden \ (oder `localhost` zu Debugging-Zwecken \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Service Workers][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      Verwendet Dienst Arbeitsthreads, um als Netzwerk Proxys zwischen Ihrem Server und der Client-App zu fungieren.  Dienst Arbeitsthreads bieten Offlineunterstützung, Zwischenspeicherung von Ressourcen, Push-Benachrichtigungen, Synchronisierung von Hintergrunddaten und Optimierungen bei der Seiten Ladeleistung.    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Web App-Manifest][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      Stellt eine JSON-basierte Metadatendatei bereit, die wichtige Informationen zu Ihrer Web-App beschreibt, damit Windows 10 und andere Hostplattformen ihren PWA-Benutzern eine installierbare, systemeigene App-ähnliche Benutzeroberfläche bereitstellen.  Zu den wichtigsten Informationen zählen Symbole, Sprache und URL-Einstiegspunkt. 
   :::column-end:::
:::row-end:::  

Um eine tolle PWA zu sein, muss Ihre APP auch die folgenden Voraussetzungen erfüllen.  

:::row:::
   :::column span="1":::
      [Browserübergreifende Kompatibilität][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      Stellen Sie sicher, dass Ihre PWA-Funktion in verschiedenen Browsern und Umgebungen [getestet][MicrosoftDeveloperEdgeToolsRemote] wird.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Dynamisches Design][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      Verwendet flüssige Layouts und flexible Bilder.  Das reaktionsfähige Design umfasst die folgenden Elemente, die ihre UX an das Gerät Ihres Benutzers anpassen.  
      
      *   CSS- [Raster][MDNCssGridLayout]  
      *   [Flexbox][MDNCssFlexibleBoxLayout]  
      *   CSS- [Raster][MDNCssGridLayout] und [Flexbox][MDNCssFlexibleBoxLayout]  
      *   [Medienabfragen][MDNMediaQueries]  
      *   [reaktionsfähige Bilder][MDNResponsiveImages]  
      
      Verwendet [Geräte Emulations Tools][DevToolsGuideDeviceModeTestingOtherBrowsers] aus dem Browser, um lokal zu testen oder eine Remote Debugsitzung für [Windows][DevtoolsRemoteDebuggingWindows] oder [Android][DevtoolsRemoteDebuggingIndex] zu erstellen, um direkt auf einem Zielgerät zu testen.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Deep-Linking][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      Leitet jede Seite Ihrer Website an eine eindeutige URL weiter, damit vorhandene Benutzer Ihnen helfen können, ein noch größeres Publikum durch Social Media Sharing zu engagieren.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Validierungs-und Testmethoden][Webhint]  
   :::column-end:::
   :::column span="2":::
      Verwendet Code Quality Tools wie [webhint][Webhint] Linter, um die Effizienz, Robustheit, Sicherheit und Barrierefreiheit Ihrer APP zu optimieren.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Chrome PWA-Checkliste][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      Überprüft Ihre PWA mit der Google-Baseline PWA-Checkliste.  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> Wenn Sie Ihre PWA in eine [Microsoft Store][MicrosoftDeveloperStore] -Anwendung umwandeln möchten, navigieren Sie zu [Progressive Web Apps (EdgeHTML) im Microsoft Store] [PwaEdgehtmlMicrosoftStore].  
  
## Weitere Informationen  

*   [Mythos Zerschlagung PWAs][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Eine progressive Roadmap für Ihre Progressive Web-App][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Offline Beiträge mit progressiven Web-Apps][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Wetten im Web][JoretegBlogBettingWeb]  
*   [Benennen von progressiven Web-Apps][Fberriman20170626NamingProgressiveWebApps]  
*   [Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Entwerfen und Erstellen einer progressiven Web-Anwendung ohne Framework (Teil 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
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

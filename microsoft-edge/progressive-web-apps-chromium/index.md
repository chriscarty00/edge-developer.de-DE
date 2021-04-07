---
description: Progressive Web Apps (Chromium) werden nativ unter Windows 10 ausgeführt.  Hier finden Sie alles, was Sie als Webentwickler wissen müssen.
title: Progressive Web Apps unter Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: be832ee5c0ad395dae7b4946c41da157ab5cd9ba
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480188"
---
# <a name="progressive-web-apps-on-windows-overview"></a>Übersicht über progressive Web-Apps unter Windows  

[Progressive Web Apps][MDNApps] \(PWAs\) bieten Zugriff auf offene Webtechnologien für die plattformübergreifende Interoperabilität und bieten Ihren Benutzern eine systemeigene, app- like-Erfahrung, die für ihre Geräte angepasst ist.  PWAs sind Websites, die [schrittweise erweitert][AListApartUnderstandingProgressiveEnhancement] werden, um wie systemeigene Apps auf unterstützenden Plattformen zu funktionieren.  Die Eigenschaften einer PWA vereinen das Beste aus Web- und nativen Apps.  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search-small.png":::
        ### <a name="discoverablemdnpwaadvantagesdiscoverable"></a>[Discoverable][MDNPwaAdvantagesDiscoverable]
        Aus Websuchergebnissen und unterstützenden App-Stores
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package-small.png":::
        ### <a name="installablemdnpwaadvantagesinstallable"></a>[Installierbar][MDNPwaAdvantagesInstallable]
        Anheften und Starten vom Startbildschirm, Startmenü, Taskleiste und so weiter
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification-small.png":::
        ### <a name="re-engageablemdnpwaadvantagesreengageable"></a>[Re-engageable][MDNPwaAdvantagesReEngageable]
        Senden von Pushbenachrichtigungen, auch wenn die App nicht aktiv ist
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline-small.png":::
        ### <a name="network-independentmdnpwaadvantagesnetworkindependent"></a>[Netzwerkunabhängig][MDNPwaAdvantagesNetworkIndependent]
        Funktioniert offline und unter Bedingungen mit geringem Netzwerk
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive-small.png":::
        ### <a name="progressivemdnpwaadvantagesprogressive"></a>[Progressiv][MDNPwaAdvantagesProgressive]
        Die Benutzererfahrung wird mit den Gerätefunktionen nach oben (oder nach unten) skaliert.
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security-small.png":::
        ### <a name="safemdnpwaadvantagessafe"></a>[Sicher][MDNPwaAdvantagesSafe]
        Bietet einen sicheren HTTPS-Endpunkt und andere Benutzerschutzmechanismen
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive-small.png":::
        ### <a name="responsivemdnpwaadvantagesresponsive"></a>[Dynamisch][MDNPwaAdvantagesResponsive]
        Passt sich an die Bildschirmgröße oder Ausrichtung und Eingabemethode des Benutzers an.
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link-small.png":::
        ### <a name="linkablemdnpwaadvantageslinkable"></a>[Linkable][MDNPwaAdvantagesLinkable]
        Freigeben und Starten über einen Standardlink
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


Erstellen Sie \(oder konvertieren\) Ihre vorhandene Website in eine PWA, um Ihr Engagement mit Ihren Benutzern zu verbessern.  Zu den Verbesserungen gehören Pushbenachrichtigungen, app-like integration und offline support.  Erstellen Sie weiterhin Ihre Zielgruppe im geöffneten Web, damit Benutzer Ihre PWA durch Suchen und Teilen von Links entdecken können.  Das Beste ist, dass Ihre App mithilfe des Webservercodes aktualisiert wird.  

## <a name="pwas-on-microsoft-edge-chromium"></a>PWAs auf Microsoft Edge (Chromium)  

Wenn Sie eine Progressive Web App für Webstandard-APIs erstellen, kann Ihre App plattform- und geräteübergreifend bereitgestellt werden und die gerätespezifischen Funktionen nutzen.  PWAs in Microsoft Edge \(Chromium\) fügen Ihrer Website die folgenden Vorteile hinzu.  

*   Ihre App basiert auf einer standardbasierten Webplattform.  
*   Ermöglicht Es Benutzern, Ihre App direkt über den Browser zu installieren.  
*   Ermöglicht Benutzern die Installation Ihrer App ohne Store-basierte Bereitstellung oder Registrierung.  
    
Desktop-PWAs werden auf allen Plattformen unterstützt, die Microsoft Edge \(Chromium\) verfügbar ist. Microsoft Edge \(Chromium\) ist unter Windows 7, Windows 10 und macOS verfügbar.  Die folgenden Vorteile sind enthalten.  

*   Apps können direkt im Browser mithilfe **** des Installationssymbols in der Navigationsleiste installiert werden.  
    
    :::image type="complex" source="./media/install-progressive-web-app-icon.png" alt-text="Installieren von App-Flyout und Symbol" lightbox="./media/install-progressive-web-app-icon.png":::
       Installieren von App-Flyout und Symbol  
    :::image-end:::  
    
*   Apps können auch im Menü Einstellungen **** apps installiert, ausgeführt und  >  **** verwaltet werden.  
    
    :::image type="complex" source="./media/app-menus.png" alt-text="App-Menüelemente unter Einstellungen" lightbox="./media/app-menus.png":::
       App-Menüelemente unter Einstellungen  
    :::image-end:::  
    
*   Webbenachrichtigungen sind in das Windows-Benachrichtigungssystem integriert  
*   Freigegebener Cookiespeicher mit dem Browserprofil, das die App installiert hat  
*   Zugriff auf andere Browserfeatures mithilfe des Menüs **Einstellung** und mehr \( \) einschließlich Zertifikatüberprüfung, Websiteberechtigungen, Nachverfolgungsschutz `...` und Browsererweiterungen  
*   Vollzugriff auf [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] zum Debuggen Ihrer App  
    
> [!NOTE]
> Weitere Informationen zu PWA-Vorteilen, bevorstehenden Features und kurzen Demos finden Sie unter [Build 2020 PWA session][BuildVideo]. 

## <a name="requirements"></a>Anforderungen  

Um als PWA ausgeführt zu werden, sollte Ihre vom Server gehostete Web-App die folgenden Mindestanforderungen enthalten.  

:::row:::
   :::column span="1":::
      [HTTPS][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      Schützt Ihre Benutzer, indem sie eine sichere Verbindung für die Server- oder App-Kommunikation bereitstellen.  Service Workers und andere PWA-Technologien funktionieren nur mit Webressourcen, die über eine sichere Verbindung \(oder aus `localhost` Debugzwecken) bedient werden\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Service Workers][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      Verwendet Service Worker-Threads, um als Netzwerk-Proxys zwischen Ihrem Server und Ihrer Client-App zu fungieren.  Service Worker-Threads bieten Offlineunterstützung, Ressourcen zwischenspeichern, Pushbenachrichtigungen, Hintergrunddatensynchronisierung und Leistungsoptimierungen beim Seitenladen.    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Web-App-Manifest][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      Stellt eine JSON-basierte Metadatendatei bereit, in der wichtige Informationen zu Ihrer Web-App beschrieben werden, sodass Windows 10 und andere Hostplattformen ihren PWA-Benutzern eine installierbare, systemeigene app-bezogene Besensung bieten.  Wichtige Informationen umfassen Symbole, Sprache und URL-Einstiegspunkt. 
   :::column-end:::
:::row-end:::  

Um ein großartiges PWA zu sein, muss Ihre App auch die folgenden Anforderungen erfüllen.  

:::row:::
   :::column span="1":::
      [Browserübergreifende Kompatibilität][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      Stellen Sie sicher, dass Ihr PWA funktioniert, [indem Sie][MicrosoftDeveloperEdgeToolsRemote] tests in verschiedenen Browsern und Umgebungen durchführen.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Dynamisches Design][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      Verwendet flüssige Layouts und flexible Bilder.  Das responsive Design umfasst die folgenden Elemente, die Ihre UX an das Gerät Ihres Benutzers anpassen.  
      
      *   [CSS-Raster][MDNCssGridLayout]  
      *   [flexbox][MDNCssFlexibleBoxLayout]  
      *   [CSS-Raster][MDNCssGridLayout] und [Flexbox][MDNCssFlexibleBoxLayout]  
      *   [Medienabfragen][MDNMediaQueries]  
      *   [Reaktionsschnelle Bilder][MDNResponsiveImages]  
      
      Verwendet [Geräteemulationstools][DevToolsGuideDeviceModeTestingOtherBrowsers] aus Ihrem Browser, um lokal zu testen oder eine Remotedebubuingsitzung unter [Windows][DevtoolsRemoteDebuggingWindows] oder [Android][DevtoolsRemoteDebuggingIndex] zu erstellen, um direkt auf einem Zielgerät zu testen.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Tiefe Verknüpfung][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      Leitet jede Seite Ihrer Website an eine eindeutige URL weiter, sodass vorhandene Benutzer Ihnen helfen können, eine noch breitere Zielgruppe über die Freigabe sozialer Medien zu erreichen.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Validierungs- und Testmethoden][Webhint]  
   :::column-end:::
   :::column span="2":::
      Verwendet Codequalitätstools wie den [Webhint-Linter,][Webhint] um die Effizienz, Robustheit, Sicherheit und Barrierefreiheit Ihrer App zu optimieren.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Chromium-PWA-Prüfliste][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      Überprüft Ihre PWA anhand der Google-Basis-PWA-Prüfliste.  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> Um Ihre PWA in eine [Microsoft Store-App zu][MicrosoftDeveloperStore] verwandeln, navigieren Sie zu [Progressive Web Apps im Microsoft Store][PwaChromiumMicrosoftStore].  
  
## <a name="see-also"></a>Weitere Informationen  

*   [Legendenbusting PWAs][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Eine progressive Roadmap für Ihre Progressive Web App][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Offline-POSTs mit progressiven Web-Apps][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Wetten im Web][JoretegBlogBettingWeb]  
*   [Benennung progressiver Web-Apps][Fberriman20170626NamingProgressiveWebApps]  
*   [Entwerfen und Erstellen einer progressiven Web-App ohne Framework (Teil 1)][Smashingmagazine201907ProgressiveWebAppFrameworkPart1]  
*   [Entwerfen und Erstellen einer progressiven Web-App ohne Framework (Teil 2)][Smashingmagazine201907ProgressiveWebAppFrameworkPart2]  
*   [Entwerfen und Erstellen einer progressiven Web-App ohne Framework (Teil 3)][Smashingmagazine201907ProgressiveWebAppFrameworkPart3]  
    
<!-- links -->  

[DevtoolsRemoteDebuggingIndex]: ../devtools-guide-chromium/remote-debugging/index.md "Erste Schritte mit remote debuggen von Android-Geräten | Microsoft Docs"  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Erste Schritte mit remote debugging Windows 10 Devices | Microsoft Docs"  
[DevToolsGuideDeviceModeTestingOtherBrowsers]: ../devtools-guide-chromium/device-mode/testing-other-browsers.md "Emulieren und Testen anderer | Microsoft Docs"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps/index.md "Debuggen von Progressive Web Apps | Microsoft Docs"  
[PwaChromiumMicrosoftStore]: ./microsoft-store.md "Veröffentlichen Sie Ihre Progressive Web App im Microsoft Store | Microsoft Docs"



[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Windows Push Notification Services (WNS) | Microsoft Docs"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Entwerfen für Xbox- und | Microsoft Docs"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Überlegungen zur Benutzeroberfläche für UWP-| Microsoft Docs"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Was ist eine App für die universelle Windows-Plattform (UWP)? | Microsoft Docs"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Unterstützen Sie Ihre App mit Hintergrundaufgaben | Microsoft Docs"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Veröffentlichen von Windows-Apps und | Microsoft Docs"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Öffnen eines Entwicklerkontos | Microsoft Docs"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Willkommen bei Progressive Web Apps für Microsoft Edge und Windows 10 – Windows Blogs"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "Hintergrundsynchronisierungs-API – Microsoft Edge Platform Status"  
[MicrosoftDeveloperEdgePlatformStatusWebAppManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Web-App-Manifest – Microsoft Edge-Plattformstatus"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Sofortige Tests"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Mixed Reality für Entwickler"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Herunterladen des neuen Microsoft Edge-Browsers"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Aktivieren oder Deaktivieren der Fokushilfe in Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Ändern von Benachrichtigungseinstellungen in Windows 10"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

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

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "PWA-Video"  

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

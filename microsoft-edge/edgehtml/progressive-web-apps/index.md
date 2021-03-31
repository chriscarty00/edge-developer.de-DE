---
description: Progressive Web-Apps werden nativ unter Windows 10 ausgeführt.  Hier finden Sie alles, was Sie als Web-Entwickler wissen müssen.
title: Progressive Web Apps (EdgeHTML) unter Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: Progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 87996f6be7c1963c01a476b307a31e689e3880d4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233944"
---
# Progressive Web Apps (EdgeHTML) unter Windows  

Mit [Progressive Web-Apps][MDNApps] \(oder einfach PWAs \) müssen Sie nicht zwischen der Verwendung offener Webtechnologien für die plattformübergreifende Interoperabilität und dem Bereitstelleneiner systemeigenen App-ähnlichen Benutzeroberfläche für Ihr Gerät entscheiden.  Das liegt daran, dass PWAs nur Websites sind, die [schrittweise verbessert][AListApartUnderstandingProgressiveEnhancement] werden, um wie Native apps auf unterstützenden Plattformen zu funktionieren.  Die Eigenschaften einer PWA vereinen das Beste aus Web- und nativen Apps.  

:::row:::
    :::column:::
        ![Erkennbares Symbol][ImageISearch]
        ### [Erkennbar][MDNPwaAdvantagesDiscoverable]
        Aus Websuche-Ergebnissen und unterstützenden App-Stores
    :::column-end:::
    :::column:::
        ![Installierbares Symbol][ImageIPackage]
        ### [Installierbar][MDNPwaAdvantagesInstallable]
        Anheften und starten vom Startbildschirm aus  
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
        Erfahrungs Skalen \(nach oben oder unten \) mit Gerätefunktionen  
    :::column-end:::
    :::column:::
        ![Sicheres Symbol][ImageISecurity]
        ### [Sicher][MDNPwaAdvantagesSafe]
        Bietet einen sicheren HTTPS-Endpunkt und andere Sicherheitsvorkehrungen für Benutzer  
    :::column-end:::
    :::column:::
        ![Symbol "reagiert"][ImageIResponsive]
        ### [Dynamisch][MDNPwaAdvantagesResponsive]
        Anpassung an Bildschirmgröße/-Ausrichtung und Eingabemethode des Benutzers  
    :::column-end:::
    :::column:::
        ![Verknüpfungssymbol][ImageILink]
        ### [Linkbar][MDNPwaAdvantagesLinkable]
        Freigeben und starten von einem Standardhyperlink  
    :::column-end:::
:::row-end:::

Durch das Erstellen oder Konvertieren Ihrer vorhandenen Website in eine PWA sind Sie in der Lage, Ihre vorhandene Zielgruppe mithilfe von Push-Benachrichtigungen und Offlineunterstützung besser zu engagieren.  Gleichzeitig sind Sie in der Lage, Ihre Zielgruppe im geöffneten Web weiter zu entwickeln, da Benutzer ihre PWA durchsuchen und Link Freigabe entdecken.  

## PWAs unter Windows 10 (EdgeHTML)  

> [!NOTE]
> Mit dem Wechsel zu Microsoft Edge (Chrom) von EdgeHTML sind die zugrunde liegenden Webplattformen, die von PWAs verwendet werden, nicht identisch.  Edge (Chrom)-PWAs werden im Browser installiert und ausgeführt.  Edge (EdgeHTML) PWAs ausführen als universelle Windows-Plattform (UWP)-Anwendungen und verwenden die ältere EdgeHTML-Webplattform.  Wenn Sie Windows 10-API-Zugriff für Ihre PWA benötigen, ist diese EdgeHTML-Dokumentation für Sie.  Wenn Sie über plattformübergreifende Unterstützung ohne Windows-spezifischen API-Zugriff verfügen, wenden Sie sich bitte an die [Microsoft Edge (Chrom) PWA-Dokumentation][PwaChromiumIndex].  

Wenn Sie eine progressive Web-App erstellen, um Windows 10 zu nutzen, können Sie Ihre PWA über den [Microsoft Store][MicrosoftDeveloperStore]verteilen, die gesamte Windows 10-Installationsbasis mit 600 Millionen aktiven monatlichen Benutzern ist Ihre potenzielle App-Zielgruppe!  Anwendungen, die auf diese Weise entwickelt wurden, werden als [universelle Windows-Plattform][WindowsUWPGetStartedGuide] -apps ausgeführt und verfügen über Native wie Zugriff auf die WinRT-APIs.  Beachten Sie, dass die Webplattform, die Ihren Code wiedergibt, bei der Verwendung der WinRT-APIs EdgeHTML ist, damit Sie die Funktionserkennung verwenden können, bevor Sie Windows-spezifische APIs aufrufen, um sicherzustellen, dass Ihre PWA weiterhin plattformübergreifend ausgeführt werden kann, auf denen Microsoft Edge \(Chromium \) PWAs verfügbar sind.  

[Hier][PwaEdgehtmlGetStarted] erfahren Sie, wie Sie Ihre Web-App in eine PWA \(EdgeHTML \) konvertieren, Sie unter Windows 10 testen und im Microsoft Store verteilen.  

## Anforderungen  

Damit Sie als PWA ausgeführt werden kann, erfordert ihre vom Server gehostete Web-App mindestens Folgendes:  

*   [Https][WikiHttps].  Schützen Sie Ihre Benutzer, indem Sie eine sichere Verbindung für die Kommunikation zwischen Servern und apps bereitstellen.  Dienstmitarbeiter und andere PWA-Technologien funktionieren nur mit Webressourcen, die über eine sichere Verbindung bereitgestellt werden \(oder `localhost` zu Debugging-Zwecken \).  
  
*   [Dienstmitarbeiter][MDNServiceWorkerApi].  Verwenden Sie Dienst Arbeitsthreads, um als Netzwerk Proxys zwischen Ihrem Server und der Client-App zu fungieren, um Offline-Unterstützung, Zwischenspeicherung von Ressourcen, Push-Benachrichtigungen, Synchronisierung von Hintergrunddaten und Optimierungen beim Laden von Seiten zu ermöglichen.  

*   [Web App-Manifest][MDNWebAppManifest].  Stellen Sie eine JSON-basierte Metadatendatei bereit, die wichtige Informationen zu Ihrer Web-App beschreibt \(wie Symbole, Sprache und URL-Einstiegspunkt \), damit Windows 10 und andere Hostplattformen ihren PWA-Benutzern eine installierbare, systemeigene App-ähnliche Benutzeroberfläche bereitstellen können.  Wenn Sie Ihre Website mit einem Web App-Manifest verknüpfen, kann Sie über den Bing-Indizierungsdienst [automatisch in den Microsoft Store aufgenommen][PwaEdgehtmlMicrosoftStoreImportingBing] werden.  

Um eine tolle PWA zu sein, benötigt Ihre APP auch:  

*   [Browserübergreifende Kompatibilität][MDNCrossBrowserTesting]  Stellen Sie sicher, dass Ihre PWA-Funktion in verschiedenen Browsern und Umgebungen [getestet][MicrosoftDeveloperEdgeToolsRemote] wird.  Unter Windows 10 sollten Sie sicherstellen, dass Sie Ihre APP sowohl im Microsoft Edge-Browser als auch in der vollständigen PWA-Umgebung testen: als installierte eigenständige Windows 10-App \(powered by the EdgeHTML Engine \).  
  
*   [Ansprechenden Entwurf][WikiResponsiveWebDesign].  Verwenden Sie flüssige Layouts und flexible Bilder mit CSS- [Raster][MDNCssGridLayout] und/oder [Flexbox][MDNCssFlexibleBoxLayout], [medienabfragen][MDNMediaQueries]und [responsive Images[MDNResponsiveImages] , um Ihre UX an das Gerät Ihres Benutzers anzupassen.  Verwenden Sie die Geräte- [Emulations Tools][DevToolsGuideEmulation] Ihres Browsers, um lokal zu testen, oder richten Sie eine [Remote Debugsitzung][DevToolsProtocolClientsEdgeDevToolsPreview] ein, um direkt auf einem Zielgerät zu testen.  Unter Windows 10 können PWAs \(EdgeHTML \) auch auf die [Formfaktoren zugeschnitten][WindowsUWPDesignDevicesIndex] werden, die über den Desktop, das Smartphone und das Tablet hinausgehen, einschließlich: [Xbox und TV][WindowsUWPDesignDevicesDesigningTv], [Surface Hub][MicrosoftDeveloperWindowsSurfaceHub]und [Windows Mixed Reality][MicrosoftDeveloperWindowsMixedReality] -Geräte.  
  
*   [Deep-Linking][WikiDeepLinking].  Leiten Sie jede Seite Ihrer Website an eine eindeutige URL weiter, damit vorhandene Benutzer Ihnen helfen können, ein noch größeres Publikum durch Social Media Sharing zu engagieren.  

*   [Bewährte Methoden][Webhint].  Verwenden Sie Code Quality Tools wie [webhint][Webhint] Linter, um die Effizienz, Robustheit, Sicherheit und Barrierefreiheit Ihrer APP zu optimieren.  

Um Ihre Progressive Web-App an den [Microsoft Store][MicrosoftDeveloperStore]zu übermitteln, müssen Sie über Folgendes verfügen:  

*   Ein [Microsoft-Entwicklerkonto][WindowsUWPPublishDeveloperAccount]  
*   Abgeschlossene [Schritte zum Veröffentlichen einer Windows-App][WindowsUWPPublishIndex]  

In den nächsten Monaten werden vorhandene PWAs im Web, die [bestimmte Kriterien][PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission] erfüllen, automatisch von der Bing-Suchmaschine in den Microsoft Store indiziert \(wo Entwickler diese direkt für Ihre Windows 10-Zielgruppe verwalten können).  

Weitere Informationen finden Sie [im Microsoft Store unter PWAs (EdgeHTML)][PwaEdgehtmlMicrosoftStore] .  

## Aktuelle Verfügbarkeit  

Die Browser Modul Unterstützung für Progressive Web-Apps erfordert eine Reihe von architektonischen Komponenten, wobei die Netzwerkinfrastruktur, die der [Fetch-API][MDNFetchApi]zugrunde liegt, am bedeutendsten ist.  Die PWA-Unterstützung im EdgeHTML-Modul wurde in der Windows 10 1809-Version abgeschlossen.  Weitere Verbesserungen an Webstandards seit dieser Zeit werden nicht in das EdgeHTML-Modul übernommen, daher sollten Sie Kompatibilitätstests ausführen und die Funktionserkennung für eine ordnungsgemäße Fallback-Funktion verwenden, wenn das Feature, das Ihre PWA-Funktion auf der EdgeHTML-Plattform nicht unterstützt.  

Für die bevorstehende Microsoft Edge-Version (Chrom) in 2020 bietet die Browser Plattform vollständige Unterstützung für diese Features, die auf allen Geräten funktionieren, auf denen der Chrom-Browser unterstützt wird.  

In EdgeHTML und Windows ist der aktuelle Status der auf Standards basierenden PWA-Technologien zu finden:  

| Technologie | Zweck | Verfügbarkeit | Verwendungshinweise |  
|:--- |:--- |:--- |:--- |  
| [Webanwendungs Manifest][MDNWebAppManifest] | Stellt App-Metadaten für das Hostbetriebssystem bereit, um die Installation und die App Store-Heraufstufung zu ermöglichen.  Für PWAs im Microsoft Store erforderlich.  | [In der Entwicklung][MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest] | Im Moment können Sie den [PWA-Generator][|::ref1::|] verwenden, um ein W3C-kompatibles JSON-Manifest zu generieren und Ihre APP für verschiedene Betriebssystemplattformen zu verpacken.  Für Windows übersetzt PWA Builder Ihr JSON-Manifest in das `.appxmanifest` von Windows 10-apps benötigte Format \(XML \).  |  
| [FETCH-API][MDNFetchApi] | Bietet asynchrone Netzwerke \(Anforderungen, Antworten \) für Seitenressourcen |[EdgeHTML 14 +][DevGuideWhatsNewEdgeHtml14] /Build 14393 + | Die Syntax der [Service Worker-API][MDNServiceWorkerApi] basiert auf FETCH-basierten Netzwerk-APIs.  Sie können die [Fetch-API][MDNFetchApi] auch allgemeiner als eine moderne Alternative zu verwenden `XMLHttpRequest` .  |  
| [Service Worker-API][MDNServiceWorkerApi] | Bietet ein offline fähiges Web-App-Modell/Netzwerkproxy, in dem ereignisgesteuerte Skripts unabhängig von Webseiten ausgeführt werden.  | [EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /Build 17133 + | Experimentelle Unterstützung \(hinter `Enable Service Workers` Flag \) ausgeliefert in EdgeHTML 16.  Standardmäßig aktiviert in EdgeHTML 17 + Builds.  |  
| [Cache-API][MDNCache] | Bietet einen Speichermechanismus für Netzwerkanforderung/-Antwort-Paare | [EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /Build 17133 + | Siehe oben in der [Service Worker-API-][MDNServiceWorkerApi] Hinweis.  |  
| [Push-API][MDNPushApi] | Ermöglicht einem Dienstmitarbeiter das Abonnieren von Push-Benachrichtigungen |[EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /Build 17133 +| Siehe oben in der [Service Worker-API-][MDNServiceWorkerApi] Hinweis.  Für Windows 10-apps \(einschließlich PWAs \) ist der [Windows-Push-Benachrichtigungsdienst \(WNS \)][WindowsUWPControlsPatternTilesNotificationsWns] erforderlich, um Push-Benachrichtigungen zu senden, die die W3C [-Push-API][MDNPushApi]unterstützen.  |  
| [Benachrichtigungs-API][MDNNotificationsApi] | Ermöglicht einem Dienstmitarbeiter, dem Benutzer eine Systembenachrichtigung bei der Push-Nachricht anzuzeigen | [EdgeHTML 14 +][DevGuideWhatsNewEdgeHtml14] /Build 14393 + | Web-Benachrichtigungen in EdgeHTML sind vollständig in das Windows 10- [Wartungs Center][MicrosoftSupportWindowsNotificationSettings]integriert, in dem Benutzer App-Benachrichtigungen verwalten und [ruhige Stunden][MicrosoftSupportWindowsFocusAssist]einstellen können.  |  
| [Hintergrund-Synchronisierungs-API][MDNSyncManager] | Stellt eine API bereit, mit der ein Dienstmitarbeiter benachrichtigt wird, dass der Benutzer wieder online ist, und regelmäßige Ereignisse zum Synchronisieren von lokalen Daten mit dem Server plant | [In der Entwicklung][MicrosoftDeveloperEdgePlatformStatusBackgroundSync] | Im Moment können Sie die systemeigene [WinRT-BackgroundTask-API][WindowsUWPLaunchResumeBackgroundTasks] verwenden, um Hintergrundaufgaben für Ihre PWA zu implementieren, wenn Sie als Windows 10-app ausgeführt wird.  |  

Hier ist der aktuelle Status des Microsoft Store-Supports für PWAs unter Windows 10:  

| Store-Übermittlungsmethode | Status | Details |  
|:--- |:--- |:--- |  
| Handbuch \(Entwickler initiiert \) | Verfügbar | Schauen Sie sich [PWAs (EdgeHTML) im Microsoft Store][PwaEdgehtmlMicrosoftStore] an, um zu beginnen.  |  
| Automatisch \(automatisch indiziert mit Bing \) | Bald verfügbar | Wir untersuchen [derzeit][WindowsBlogsWelcomingPWAsEdgeWindows] den PWA-Onboarding-Prozess mit einer begrenzten Teilmenge von App-Partnern.  In den nächsten Monaten begrüßt Microsoft PWAs über das Mainstream-Web zum Microsoft Store.  Lesen Sie den [automatischen PWA-Import mit Bing][PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission] , um mehr über die Microsoft Store-Anforderungen für automatisch generierte PWA-Auflistungen zu erfahren.  |  

<!-- image links -->  

[ImageISearch]: media/i_search.png  
[ImageIPackage]: media/i_package.png  
[ImageIPushNotification]: media/i_push-notification.png  
[ImageIOffline]: media/i_offline.png  
[ImageIProgressive]: media/i_progressive.png  
[ImageISecurity]: media/i_security.png  
[ImageIResponsive]: media/i_responsive.png  
[ImageILink]: media/i_link.png  

<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge devtools Preview – devtools-Protokoll Clients | Microsoft docs"  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Emulation | Microsoft docs"  
[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "Neuerungen in EdgeHTML 17 | Microsoft docs"  
[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "Neuerungen in EdgeHTML 14 | Microsoft docs"  
[PwaChromiumIndex]: ../../progressive-web-apps-chromium/index.md "Progressive Web-Apps (Chrom) unter Windows | Microsoft docs"  
[PwaEdgehtmlGetStarted]: ../progressive-web-apps/get-started.md "Erste Schritte mit Progressive Web Apps (EdgeHTML) | Microsoft docs"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps/microsoft-store.md "Progressive Web-Apps im Microsoft Store | Microsoft docs"
[PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps/microsoft-store.md#criteria-for-automatic-submission "Kriterien für die automatische Übermittlung – Progressive Web-Apps im Microsoft Store | Microsoft docs"  
[PwaEdgehtmlMicrosoftStoreImportingBing]: ./microsoft-store.md#automatic-pwa-importing-with-bing "Automatischer PWA-Import mit Bing-Progressive Web Apps (EdgeHTML) im Microsoft Store | Microsoft docs"  


[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Windows-Push-Benachrichtigungsdienste \(WNS \) – Übersicht"  
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
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images- "reaktionsfähige Bilder | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker-API | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "Synchronisierungs-Manager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Web App-Manifest | MDN"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Deep Linking – Wikipedia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS – Wikipedia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Responsive Web Design – Wikipedia"  

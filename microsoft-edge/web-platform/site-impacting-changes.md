---
description: Enthält eine Zusammenfassung von änderungen mit großen Auswirkungen, die sich auf die Websitekompatibilität auswirken können
title: Websitekompatibilität – Auswirkungen von Änderungen an Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/27/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibility, web platform
ms.openlocfilehash: 7db00ced1db767d3ec092c33369cbed1845ac65e
ms.sourcegitcommit: dfc6bc1bad5fc9d38b6eb3bcacf9ebb317b3bdf2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "11586204"
---
# <a name="site-compatibility-impacting-changes-coming-to-microsoft-edge"></a>Websitekompatibilität – Auswirkungen von Änderungen an Microsoft Edge  

Die Webplattform ist eine Sammlung von Technologien, die zum Erstellen von Webseiten verwendet werden.  Die Technologien umfassen HTML, CSS, JavaScript und viele andere offene Standards.  Die Webplattform wird ständig weiterentwickelt, um die Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern.  In einigen Fällen können Sich Änderungen auf die Funktionalität vorhandener Webseiten auswirken.  Weitere Informationen zu bevorstehenden Änderungen Chromium Projektwebplattform finden Sie unter [Chrome Platform Status Release timeline][ChromestatusFeaturesSchedule].  

Microsoft Edge übernehmen nahezu alle upstream-Änderungen an der Webplattform aus dem Chromium Projekt.  Zu den Gründen gehören Funktions- und Kompatibilitätsgründe.  Microsoft hat weiterhin die volle Kontrolle über Microsoft Edge Browser und kann Änderungen zurückweisen oder zurückweisen.  Das Microsoft Edge entscheiden, ob die Änderung den Browserbenutzern vorteile.  In der folgenden Microsoft Edge werden Featurebereiche Chromium Änderungen am Timing oder Verhalten aufgeführt.  In der Tabelle werden auch die wichtigsten Änderungen hervorgehoben, die das Microsoft Edge verfolgt.  

Lesen Sie diesen Artikel häufig.  Das Microsoft Edge aktualisiert diesen Artikel, wenn das Denken sich weiterentwickelt, Zeitachsen verfestigen und neue Änderungen angekündigt werden.  

| Änderung | Stable-Kanal | Experimentation | Weitere Informationen |  
|:--- |:--- |:--- |:--- |
| Cookies standardmäßig `SameSite=Lax` auf und `SameSite=None-requires-Secure` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v82, Dev v82 | Diese Änderung geschieht im Chromium Projekt, auf dem Microsoft Edge basiert.  Weitere Informationen, einschließlich der geplanten Zeitachse von Google für diese Änderung, finden Sie unter [Chrome Platform Status.][ChromestatusFeature5088147346030592]  |  
| Referrer Policy: Default to `strict-origin-when-cross-origin` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v79, Dev v79 | Diese Änderung geschieht im Chromium Projekt, auf dem Microsoft Edge basiert.  Weitere Informationen, einschließlich der geplanten Zeitachse von Google für diese Änderung, finden Sie unter [Chrome Platform Status.][ChromestatusFeature6251880185331712]  |  
| Nicht synchrone `XmlHttpRequest` Seitenentlassung | [Chrome+1](#release-comments) \(Edge v83\) |  | Diese Änderung geschieht im Chromium Projekt, auf dem Microsoft Edge basiert.  Mit Chrome bietet Microsoft Edge eine Gruppenrichtlinie, um diese Änderung bis Edge v88 zu deaktivieren.  Weitere Informationen, einschließlich der geplanten Zeitachse von Google für diese Änderung, finden Sie unter [Chrome Platform Status.][ChromestatusFeature4664843055398912]  |  
| Anzeigen einer subtilen Aufforderung für Benachrichtigungsberechtigungsanforderungen | Edge v84 |  | Stille Benachrichtigungsanforderungen zeigen ein subtiles Anforderungssymbol in der Adressleiste für Websitebenachrichtigungsberechtigungen an, die mithilfe der oder DER API angefordert werden, und ersetzt die vollständige oder standardmäßige `Notifications` `Push` Berechtigungs-Flyout-Eingabeaufforderungs-UI.  Dieses Feature ist derzeit für alle Benutzer aktiviert.  Navigieren Sie zu , um stille Benachrichtigungsanforderungen abmelden zu `edge://settings/content/notifications` .  In Der Zukunft kann das Microsoft Edge das erneute Aktivieren der vollständigen Flyoutbenachrichtigungsaufforderung in einigen Szenarien prüfen.  |  
| TLS/1.0 und TLS/1.1 standardmäßig deaktivieren | Edge v84 |  | Die [SSLMinVersion-Gruppenrichtlinie][DeployedgeMicrosoftEdgePoliciesSslversionmin] ermöglicht die erneute Aktivierung von TLS/1.0 und TLS/1.1. die Richtlinie bleibt bis Edge v90 verfügbar.  |  
| Blockieren gemischter Inhaltsdownloads | [Chrome+1](#release-comments) \(Edge v86\)  |  | Diese Änderung geschieht im Chromium Projekt, auf dem Microsoft Edge basiert.  Weitere Informationen, einschließlich der geplanten Zeitachse von Google für diese Änderung, finden Sie im [Google-Sicherheitsblogeintrag][GoogleBlogSecurity20200206].  Der Microsoft-Rolloutzeitplan für Dateitypen, die gewarnt oder blockiert werden sollen, ist für eine Version nach Chrome geplant.  |  
| Veralteter AppCache | [Chrome+1](#release-comments) \(Edge v86\)  |  | Diese Änderung geschieht im Chromium Projekt, auf dem Microsoft Edge basiert.  Weitere Informationen finden Sie in der [WebDev-Dokumentation][WebDevAppCacheRemoval].  Der Microsoft-Rolloutzeitplan für die Veraltetkeit ist für eine Version nach Chrome geplant.  Durch das [Anfordern eines AppCache OriginTrial-Tokens][ChromeDevelopersOrigintrialsAppCacheOriginTrial] können Websites die veraltete API bis Edge v90 weiterhin verwenden.  |  
| Entfernen von Adobe Flash | Edge v88  |  | Diese Änderung geschieht im Chromium Projekt, auf dem Microsoft Edge basiert.  Weitere Informationen finden Sie unter [Adobe Flash Chromium Roadmap][ChromiumFlashRoadmapSupportRemoved].  | 
| Deaktivieren und Entfernen von FTP | Edge v88  | Edge Beta v87 | In Edge Beta v87 ist die #A0 standardmäßig deaktiviert. In Edge Stable v87 bleibt es aktiviert.  In Edge v88 wird die FTP-Unterstützung vollständig entfernt.  Diese Änderung geschieht im Chromium Projekt, auf dem Microsoft Edge basiert.  Weitere Informationen finden Sie unter [Chrome Platform Status Entry][ChromestatusFeature6246151319715840].  Unternehmen mit Websites, die weiterhin FTP-Unterstützung benötigen, können FTP weiterhin verwenden, indem sie die Website so konfigurieren, dass sie den [IE-Modus verwendet.][DeployedgeEdgeIeMode]  | 
| AutomatischesUpgrade von Bildern mit gemischten Inhalten | Edge v88  |  | Nicht sichere \(HTTP\)-Verweise auf Bilder werden automatisch auf HTTPS aktualisiert. Wenn das Bild nicht über HTTPS verfügbar ist, schlägt der Bilddownload fehl. Es [steht eine Gruppenrichtlinie][DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls] zur Verfügung, um dieses Feature zu steuern. Diese Änderung geschieht im Chromium Projekt, auf dem Microsoft Edge basiert. Weitere Informationen finden Sie unter [Chrome Platform Status][ChromestatusFeature4926989725073408].  | 
| HTTP-Authentifizierung nicht zulässig, wenn Drittanbietercookies blockiert werden  | Edge v87  |  | Ab Edge v87 ist die HTTP-Authentifizierung auch nicht zulässig, wenn Cookies für Drittanbieteranforderungen blockiert werden, indem sie entweder die [BlockThirdPartyCookies-Richtlinie][DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies] oder den Umschalter in `edge://settings` verwenden. Diese Änderung kann sich Enterprise downloaden von Websitelisten für den [Internet Explorer-Modus][DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy] auswirken, wenn für den Endpunkt, der die Liste hostet, die Verwendung der HTTP-Authentifizierung erforderlich ist.  Fügen Sie der [CookieAllowedForURLs-Richtlinie][DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls] ein übereinstimmendes URL-Muster hinzu, um die Verwendung von Cookies und der HTTP-Authentifizierung für Enterprise Mode Site List-Downloads zu ermöglichen.  |
| Entfernen von 3DES in TLS  | Edge v93  |  | Ab Edge v93 wird die Unterstützung TLS_RSA_WITH_3DES_EDE_CBC_SHA Verschlüsselungssuite entfernt. Diese Änderung geschieht im Chromium Projekt, auf dem Microsoft Edge basiert. Weitere Informationen finden Sie unter [Chrome Platform Status][ChromestatusFeature6678134168485888]. Darüber hinaus steht in Edge v93 eine Kompatibilitätsrichtlinie zur Verfügung, um Szenarien zu unterstützen, die die Kompatibilität mit veralteten Servern beibehalten müssen. Diese Kompatibilitätsrichtlinie ist veraltet und funktioniert in Edge v95 nicht mehr. Stellen Sie sicher, dass Sie zuvor die Server mit Auswirkungen aktualisieren. |

##### <a name="release-comments"></a>Veröffentlichungskommentare  

:::row:::
   :::column span="1":::
      Chrome+1  
   :::column-end:::
   :::column span="2":::
      Basierend auf Benutzer- und Entwicklerfeedback wird die angegebene Funktion oder Änderung eine Version nach Chrome versendet.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome oder Chrome+1  
   :::column-end:::
   :::column span="2":::
      Basierend auf Benutzer- und Entwicklerfeedback wird das angegebene Feature oder die Änderung gleichzeitig oder eine Version nach Chrome versendet.  
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedgeEdgeIeMode]: /deployedge/edge-ie-mode "Informationen zum IE-| Microsoft Docs"  
[DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy]: /deployedge/edge-ie-mode-policies#configure-using-the-use-the-enterprise-mode-ie-website-list-policy "Konfigurieren mithilfe der Listenrichtlinie Enterprise IE-Website für den Enterprise - Konfigurieren von Richtlinien für den IE-Modus | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies]: /deployedge/microsoft-edge-policies#blockthirdpartycookies "BlockThirdPartyCookies - Microsoft Edge - Richtlinien | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]: /deployedge/microsoft-edge-policies#cookiesallowedforurls "CookiesAllowedForUrls - Microsoft Edge - Richtlinien | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls - Microsoft Edge - Richtlinien | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin - Microsoft Edge - Richtlinien | Microsoft Docs"  

[ChromestatusFeaturesSchedule]: https://www.chromestatus.com/features/schedule "Veröffentlichungszeitachse | Status der Chrome-Plattform"  
[ChromestatusFeature4664843055398912]: https://chromestatus.com/feature/4664843055398912 "Synchronisierung von XHR bei Seitenentlassung nicht | Status der Chrome-Plattform"  
[ChromestatusFeature4926989725073408]: https://chromestatus.com/feature/4926989725073408 "Autoupgrade Image Mixed Content | Status der Chrome-Plattform"  
[ChromestatusFeature5088147346030592]: https://chromestatus.com/feature/5088147346030592 "Cookies standardmäßig auf SameSite=Lax | Status der Chrome-Plattform"  
[ChromestatusFeature6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Veraltete FTP-| Status der Chrome-Plattform"  
[ChromestatusFeature6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Referrer policy: Default to strict-origin-when-cross-cross-origin | Status der Chrome-Plattform"  
[ChromestatusFeature6678134168485888]: https://chromestatus.com/feature/6678134168485888 "Entfernen von 3DES in TLS-| Status der Chrome-Plattform"

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Flashunterstützung aus Chromium entfernt (Ziel: Chrome 88+ - Jan 2021) – Flash Roadmap | Chromium Projekte"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "AppCache OriginTrial-Token | Chrome Developers"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Schützen von Benutzern vor unsicheren Downloads in Google Chrome - Google Online Security Blog" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Vorbereiten der AppCache-| web.dev"  

<!--todo:  cleanup links  -->  

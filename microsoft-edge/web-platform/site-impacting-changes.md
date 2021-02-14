---
description: Enthält eine Zusammenfassung der wichtigsten Änderungen, die sich auf die Websitekompatibilität auswirken können.
title: Websitekompatibilität – Auswirkungen von Änderungen an Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Kompatibilität, Webplattform
ms.openlocfilehash: 64cdb417e6bd0aa648c7e1225bb6dc522f3873ce
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327505"
---
# Websitekompatibilität – Auswirkungen von Änderungen an Microsoft Edge  

Das Web entwickelt sich ständig weiter, um Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern.  In einigen Fällen sind Änderungen möglicherweise erheblich genug, um die Funktionalität vorhandener Seiten zu verändern.  Die folgende Tabelle enthält eine Zusammenfassung besonders betroffener Änderungen, die das Microsoft Edge-Team derzeit verfolgt.  Lesen Sie diesen Artikel häufig. Das Microsoft Edge-Team aktualisiert die folgende Seite, wenn das Denken weiterentwickelt wird, Zeitachsen sich verfestigen und neue Änderungen angekündigt werden.  

| Änderung | Stable-Kanal | Experimentation | Weitere Informationen |  
|:--- |:--- |:--- |:--- |
| Cookies standardmäßig auf `SameSite=Lax` und `SameSite=None-requires-Secure` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v82, Dev v82 | Diese Änderung geschieht im Chromium-Projekt, auf dem Microsoft Edge basiert.  For more information, including the planned timeline by Google for this change, navigate to the [Chrome Platform Status entry][ChromePlatformStatus5088147346030592].  |  
| Verweiserrichtlinie: Standard: `strict-origin-when-cross-origin` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v79, Dev v79 | Diese Änderung geschieht im Chromium-Projekt, auf dem Microsoft Edge basiert.  For more information, including the planned timeline by Google for this change, navigate to the [Chrome Platform Status entry][ChromePlatformStatus6251880185331712].  |  
| Synchrone `XmlHttpRequest` Seitenentlassung nicht zu unterschreiben | [Chrome+1](#release-comments) \(Edge v83\) |  | Diese Änderung geschieht im Chromium-Projekt, auf dem Microsoft Edge basiert.  Mit Chrome bietet Microsoft Edge eine Gruppenrichtlinie, um diese Änderung bis Edge v88 zu deaktivieren.  For more information, including the planned timeline by Google for this change, navigate to the [Chrome Platform Status entry][ChromePlatformStatus4664843055398912].  |  
| Dezente Aufforderung für Benachrichtigungsberechtigungsanforderungen anzeigen | Edge v84 |  | Bei stillen Benachrichtigungsanforderungen wird in der Adressleiste ein dezentes Anforderungssymbol für Websitebenachrichtigungsberechtigungen angezeigt, die mithilfe der ODER-API angefordert wurden, und ersetzt dabei die vollständige oder standardmäßige `Notifications` `Push` Berechtigungs-Flyout-Eingabeaufforderung.  Dieses Feature ist derzeit für alle Benutzer aktiviert.  Um stille Benachrichtigungsanforderungen abmelden zu können, navigieren Sie zu `edge://settings/content/notifications` .  In zukunft kann das Microsoft Edge-Team in einigen Szenarien die erneute Aktivierung der vollständigen Flyoutbenachrichtigungsaufforderung ins Spiel kommen.  |  
| TLS/1.0 und TLS/1.1 standardmäßig deaktivieren | Edge v84 |  | Die [#A0][DeployedgeMicrosoftEdgePoliciesSslversionmin] ermöglicht die erneute Aktivierung von TLS/1.0 und TLS/1.1. Die Richtlinie bleibt bis Edge v90 verfügbar.  |  
| Blockieren von Downloads gemischter Inhalte | [Chrome+1](#release-comments) \(Edge v86\)  |  | Diese Änderung geschieht im Chromium-Projekt, auf dem Microsoft Edge basiert.  For more information, including the planned timeline by Google for this change, navigate to the [Google security blog entry][GoogleBlogSecurity20200206].  Der Microsoft-Einführungszeitplan für Dateitypen, die gewarnt oder blockiert werden sollen, ist für eine Version nach Chrome geplant.  |  
| Veralteter AppCache | [Chrome+1](#release-comments) \(Edge v86\)  |  | Diese Änderung geschieht im Chromium-Projekt, auf dem Microsoft Edge basiert.  Weitere Informationen finden Sie in der [WebDev-Dokumentation.][WebDevAppCacheRemoval]  Der Microsoft-Rolloutzeitplan für das Veraltete ist für eine Version nach Chrome geplant.  Durch das [Anfordern eines AppCache OriginTrial-Tokens][ChromeDevelopersOrigintrialsAppCacheOriginTrial] können Websites die veraltete API bis Edge v90 weiterhin verwenden.  |  
| Entfernen von Adobe Flash | Edge v88  |  | Diese Änderung geschieht im Chromium-Projekt, auf dem Microsoft Edge basiert.  For more information, navigate to the [Adobe Flash Chromium Roadmap][ChromiumFlashRoadmapSupportRemoved].  | 
| Deaktivieren und Entfernen von FTP | Edge v88  | Edge Beta v87 | In Edge Beta v87 ist die #A0 standardmäßig deaktiviert. in Edge Stable v87 bleibt es aktiviert.  In Edge v88 wurde die FTP-Unterstützung vollständig entfernt.  Diese Änderung geschieht im Chromium-Projekt, auf dem Microsoft Edge basiert.  Weitere Informationen finden Sie unter ["Chrome Platform Status Entry".][ChromePlatformStatus6246151319715840]  Unternehmen mit Websites, die weiterhin FTP-Unterstützung benötigen, können FTP weiterhin verwenden, indem sie die Website für die Verwendung des [IE-Modus konfigurieren.][DeployedgeEdgeIeMode]  | 
| AutomatischesUpgrade von Bildern mit gemischten Inhalten | Edge v88  |  | Nicht sichere \(HTTP\)-Verweise auf Bilder werden automatisch auf HTTPS aktualisiert. Wenn das Image nicht über HTTPS verfügbar ist, schlägt der Imagedownload fehl. Es [ist eine Gruppenrichtlinie][DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls] verfügbar, um dieses Feature zu steuern. Diese Änderung geschieht im Chromium-Projekt, auf dem Microsoft Edge basiert. For more information, navigate to the [Chrome Platform Status entry][ChromePlatformStatus4926989725073408].  | 
| DIE HTTP-Authentifizierung ist nicht zulässig, wenn Cookies von Drittanbietern blockiert werden  | Edge v87  |  | Ab Edge v87 ist die HTTP-Authentifizierung auch nicht zulässig, wenn Cookies für Drittanbieteranforderungen blockiert werden, entweder mithilfe der Richtlinie ["BlockThirdPartyCookies"][DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies] oder über die Seite "Edgeeinstellungen". Diese Änderung kann sich auf Downloads von Websitelisten im Unternehmensmodus für [den Internet][DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy] Explorer-Modus auswirken, wenn für den Endpunkt, der die Liste hostet, die Verwendung der HTTP-Authentifizierung erforderlich ist.  Fügen Sie der Richtlinie ["CookiesAllowedForURLs"][DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls] ein übereinstimmendes URL-Muster hinzu, um die Verwendung von Cookies und der HTTP-Authentifizierung für Websitelistendownloads im Unternehmensmodus zu ermöglichen.  |   

##### Anmerkungen zur Version  

:::row:::
   :::column span="1":::
      Chrome+1  
   :::column-end:::
   :::column span="2":::
      Basierend auf Benutzer- und Entwicklerfeedback wird die angegebene Funktion oder Änderung eine Version nach Chrome veröffentlicht.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome oder Chrome+1  
   :::column-end:::
   :::column span="2":::
      Basierend auf Benutzer- und Entwicklerfeedback wird das angegebene Feature oder die Änderung gleichzeitig oder in einer Version nach Chrome veröffentlicht.  
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedgeEdgeIeMode]: /deployedge/edge-ie-mode "Informationen zum IE-| Microsoft Docs"  
[DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy]: /deployedge/edge-ie-mode-policies#configure-using-the-use-the-enterprise-mode-ie-website-list-policy "Konfigurieren mithilfe der Websitelistenrichtlinie "Unternehmensmodus-IE verwenden" – Konfigurieren von Richtlinien für den | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies]: /deployedge/microsoft-edge-policies#blockthirdpartycookies "BlockThirdPartyCookies – Microsoft Edge – Richtlinien | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]: /deployedge/microsoft-edge-policies#cookiesallowedforurls "CookiesAllowedForUrls – Microsoft Edge – Richtlinien | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls - Microsoft Edge – Richtlinien | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin – Microsoft Edge – Richtlinien | Microsoft Docs"  

[ChromePlatformStatus4664843055398912]: https://chromestatus.com/feature/4664843055398912 "Synchronisierung von XHR bei Seitenentlassung von JavaScript-| Chrome Platform Status"  
[ChromePlatformStatus4926989725073408]: https://chromestatus.com/feature/4926989725073408 "AutomatischesUpgrade von Gemischten Bildinhalten | Chrome Platform Status"  
[ChromePlatformStatus5088147346030592]: https://chromestatus.com/feature/5088147346030592 "Cookies standardmäßig auf SameSite=Lax | Chrome Platform Status"  
[ChromePlatformStatus6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Veraltete FTP-| Chrome Platform Status"  
[ChromePlatformStatus6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Referrer Policy: Default to strict-origin-when-cross-origin | Chrome Platform Status"  

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Flashunterstützung von Chromium entfernt (Ziel: Chrome 88+ – Jan 2021) – Flash Roadmap | Chromium-Projekte"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "AppCache OriginTrial token | Chrome Developers"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Schützen von Benutzern vor unsicheren Downloads in Google Chrome – Google Online Security Blog" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Vorbereiten des Entfernens von AppCache | web.dev"  

<!--todo:  cleanup links  -->  

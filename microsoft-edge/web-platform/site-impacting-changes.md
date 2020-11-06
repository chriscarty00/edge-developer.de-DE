---
description: Enthält eine Zusammenfassung der Änderungen mit hoher Auswirkung, die sich auf die Website Kompatibilität auswirken können.
title: Website Kompatibilität – Auswirkungen von Änderungen an Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Kompatibilität, Web-Plattform
ms.openlocfilehash: bb4d67bf1ab6274a10a83ee750fa9db52ab85464
ms.sourcegitcommit: 4497b399a6ddfa34163b7d3db4f76423d4da3c12
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/05/2020
ms.locfileid: "11156348"
---
# Website Kompatibilität – Auswirkungen von Änderungen an Microsoft Edge  

Das Web entwickelt sich ständig weiter, um Benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern.  In einigen Fällen können Änderungen erheblich genug sein, um die Funktionalität vorhandener Seiten zu beeinflussen.  In der folgenden Tabelle sind besonders wichtige Änderungen zusammengefasst, die vom Microsoft Edge-Team zurzeit nachverfolgt werden.  Lesen Sie diesen Artikel häufig; das Microsoft Edge-Team aktualisiert die folgende Seite, wenn sich das Denken entwickelt, Zeitpläne verfestigen und neue Änderungen angekündigt werden.  

| Änderung | Stable-Kanal | Experimentation | Weitere Informationen |  
|:--- |:--- |:--- |:--- |
| Cookies standardmäßig auf `SameSite=Lax` und `SameSite=None-requires-Secure` | [Chrome + 1](#release-comments) \ (Edge V86 \)  | Canary V82, dev V82 | Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Um weitere Informationen zu erhalten, einschließlich der geplanten Zeitachse von Google für diese Änderung, navigieren Sie zum [Chrome Platform-Status Eintrag][ChromePlatformStatus5088147346030592].  |  
| Referrer-Richtlinie: standardmäßig `strict-origin-when-cross-origin` | [Chrome + 1](#release-comments) \ (Edge V86 \)  | Canary V79, dev V79 | Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Um weitere Informationen zu erhalten, einschließlich der geplanten Zeitachse von Google für diese Änderung, navigieren Sie zum [Chrome Platform-Status Eintrag][ChromePlatformStatus6251880185331712].  |  
| Synchrone `XmlHttpRequest` in Seiten Kündigung nicht zulassen | [Chrome + 1](#release-comments) \ (Edge v83 \) |  | Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Passend zu Chrome bietet Microsoft Edge eine Gruppenrichtlinie zum Deaktivieren dieser Änderung bis zum Edge-V88.  Um weitere Informationen zu erhalten, einschließlich der geplanten Zeitachse von Google für diese Änderung, navigieren Sie zum [Chrome Platform-Status Eintrag][ChromePlatformStatus4664843055398912].  |  
| Subtile Aufforderung zur Anzeige von Benachrichtigungs Berechtigungsanforderungen | Edge-v84 |  | Für ruhige Benachrichtigungsanforderungen wird in der Adressleiste für Website Benachrichtigungs Berechtigungen, die mit der oder-API angefordert werden, ein Symbol für subtile Anforderung angezeigt `Notifications` `Push` , das die Benutzeroberfläche für das vollständige oder standardmäßige Berechtigungs Flyout  Dieses Feature ist derzeit für alle Benutzer aktiviert.  Navigieren Sie zu, um die leisen Benachrichtigungsanforderungen zu deaktivieren `edge://settings/content/notifications` .  In Zukunft kann das Microsoft Edge-Team in einigen Szenarien das erneute Aktivieren der vollständigen Eingabeaufforderung für Flyout-Benachrichtigungen untersuchen.  |  
| Standardmäßiges Deaktivieren von TLS/1.0 und TLS/1.1 | Edge-v84 |  | Die [SSLMinVersion][DeployedEdgePoliciesSSLMinVersion] -Gruppenrichtlinie ermöglicht die erneute Aktivierung von TLS/1.0 und TLS/1.1; die Richtlinie bleibt verfügbar, bis Edge V90.  |  
| Blockieren von Downloads für gemischten Inhalt | [Chrome + 1](#release-comments) \ (Edge V86 \)  |  | Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Weitere Informationen, einschließlich der geplanten Zeitachse von Google für diese Änderung, finden Sie im [Blogeintrag Google Security][GoogleBlogSecurity20200206].  Der Microsoft-Rollout-Zeitplan für Dateitypen, die gewarnt oder blockiert werden sollen, ist für eine Version nach Chrome geplant.  |  
| Deprecated AppCache | [Chrome + 1](#release-comments) \ (Edge V86 \)  |  | Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Weitere Informationen finden Sie in der [WebDev-Dokumentation][WebDevAppCacheRemoval].  Der Microsoft-Rollout-Zeitplan für die deprecated-Version ist für eine Version nach Chrome geplant.  Durch Anfordern eines [AppCache-OriginTrial-Tokens][AppCacheOriginTrial] können Websites die veraltete API weiter verwenden, bis Edge-V90.  |  
| Entfernen von Adobe Flash | Edge-V88  |  | Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Wenn Sie weitere Informationen wünschen, navigieren Sie zur [Adobe Flash Chrom-Roadmap][ChromiumFlashRoadmapSupportRemoved].  | 
| Deaktivieren und Entfernen von FTP | Edge-V88  | Edge Beta-V87 | In Edge Beta V87 ist die FTP-Unterstützung standardmäßig deaktiviert; in Edge stable V87 bleibt die Funktion aktiviert.  In Edge V88 wird die FTP-Unterstützung vollständig entfernt.  Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Wenn Sie weitere Informationen wünschen, navigieren Sie zum [Chrome Platform-Status Eintrag][ChromePlatformStatus6246151319715840].  Unternehmen, die über Websites verfügen, die weiterhin FTP-Unterstützung benötigen, können FTP weiterhin verwenden, indem Sie die Website für die Verwendung des [IE-Modus](https://docs.microsoft.com/deployedge/edge-ie-mode)konfigurieren.  |   

##### Kommentare freigeben  

:::row:::
   :::column span="1":::
      Chrome + 1
   :::column-end:::
   :::column span="2":::
      Basierend auf dem Feedback von Benutzern und Entwicklern werden die angegebenen Features oder Änderungen in einer Version nach Chrome ausgeliefert.
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrom oder Chrom + 1
   :::column-end:::
   :::column span="2":::
      Auf der Grundlage des Feedbacks von Benutzern und Entwicklern wird die angegebene Funktion oder der Wechsel zur gleichen Zeit oder eine Version nach Chrome geliefert.
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedEdgePoliciesSSLMinVersion]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin – Microsoft Edge – Richtlinien | Microsoft docs"  

[ChromePlatformStatus4664843055398912]: https://www.chromestatus.com/feature/4664843055398912 "Synchronisierungs-XMLHttpRequest in Seite Entlassung deaktivieren JavaScript | Chrome-Platt Form Status"  
[ChromePlatformStatus5088147346030592]: https://www.chromestatus.com/feature/5088147346030592 "Cookies sind standardmäßig SameSite = Lax | Chrome-Platt Form Status"  
[ChromePlatformStatus6251880185331712]: https://www.chromestatus.com/feature/6251880185331712 "Referrer-Richtlinie: standardmäßig auf Strict-Origin-wann-Cross-Origin | Chrome-Platt Form Status"  
[ChromePlatformStatus6246151319715840]: https://chromestatus.com/feature/6246151319715840 "FTP-Unterstützung veraltet | Chrome-Platt Form Status"

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Flash-Unterstützung aus Chrom entfernt (Ziel: Chrom 88 +-Jan 2021) – Flash-Roadmap | Chromium-Projekte"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Schützen von Benutzern vor unsicheren Downloads in Google Chrome – Google Online Security-Blog" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal/ "AppCache entfernen"
[AppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "AppCache-OriginTrial-Token"

<!--todo:  cleanup links  -->  

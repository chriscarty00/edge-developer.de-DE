---
description: Auf dieser Seite finden Sie eine Zusammenfassung der Änderungen mit hoher Auswirkung, die sich auf die Website Kompatibilität auswirken könnten.
title: Website Kompatibilität – Auswirkungen von Änderungen an Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Kompatibilität, Web-Plattform
ms.openlocfilehash: f6c19258c1e82e1ce90a21f6efc04496100c3401
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843977"
---
# Website Kompatibilität – Auswirkungen von Änderungen an Microsoft Edge  

Das Web entwickelt sich ständig weiter, um die Benutzerfreundlichkeit, die Sicherheit und den Datenschutz zu verbessern.  In einigen Fällen können Änderungen erheblich genug sein, um die Funktionalität vorhandener Seiten zu beeinflussen.  In der nachstehenden Tabelle werden besonders stark wirkende Änderungen zusammengefasst, die vom Microsoft Edge-Team zurzeit nachverfolgt werden.  Bitte schauen Sie häufig zurück. das Microsoft Edge-Team aktualisiert die folgende Seite, wenn sich das Denken entwickelt, Zeitpläne verfestigen und neue Änderungen angekündigt werden.  

| Änderung | Stable-Kanal | Experimentation | Weitere Informationen |  
|:--- |:--- |:--- |:--- |
| Cookies standardmäßig auf `SameSite=Lax` | [Chrom oder Chrom + 1](#release-comments)  | Canary V82, dev V82 | Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Weitere Informationen, einschließlich der geplanten Zeitachse von Google für diese Änderung, finden Sie unter [Chrome Platform-Status Eintrag][ChromePlatformStatus5088147346030592].  |  
| Referrer-Richtlinie: standardmäßig `strict-origin-when-cross-origin` | [Chrom oder Chrom + 1](#release-comments)  | Canary V79, dev V79 | Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Weitere Informationen, einschließlich der geplanten Zeitachse von Google für diese Änderung, finden Sie unter [Chrome Platform-Status Eintrag][ChromePlatformStatus6251880185331712].  |  
| Synchrones XmlHttpRequest bei Seitenbeendigung nicht zulassen | [Chrome + 1](#release-comments) \ (Edge v83 \) |  | Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Passend zu Chrome bietet Microsoft Edge eine Gruppenrichtlinie, um diese Änderung bis zum Edge 88 zu deaktivieren.  Weitere Informationen, einschließlich der geplanten Zeitachse von Google für diese Änderung, finden Sie unter [Chrome Platform-Status Eintrag][ChromePlatformStatus4664843055398912].  |  
| Subtile Aufforderung zur Anzeige von Benachrichtigungs Berechtigungsanforderungen |  | Canary v83, dev v83 | Benutzer können jetzt in ruhige Benachrichtigungsanforderungen einwählen `edge://settings/content/notifications` .  Wenn diese Einstellung aktiviert ist, zeigt Microsoft Edge ein Symbol für subtile Anforderungen in der Adressleiste für Websites an, die zum Senden von Benutzern in Zukunft Benachrichtigungen über die `Notifications` oder `Push` -API anfordern.  Dieses subtile Symbol ersetzt die Eingabeaufforderung für das Flyout.  Ein Experiment in Canary und dev macht dieses Verhalten für einige Benutzer auf allen Websites, die Benachrichtigungen anfordern, standardmäßig aktiviert.  Benutzer können sich in entscheiden `edge://settings/content/notifications` .  In Zukunft kann das Microsoft Edge-Team die Anzeige der Flyout-Aufforderung in bestimmten Situationen basierend auf Benutzerverhalten und anderen Eingaben untersuchen.  |  
| Standardmäßiges Deaktivieren von TLS/1.0 und TLS/1.1 | Edge-v84 |  | Um die Auswirkungen auf Websites zu ermitteln, können Sie die `edge://flags/#display-legacy-tls-warnings` Kennzeichnung festlegen, damit Microsoft Edge beim Laden von Seiten, für die Legacy-TLS-Protokolle erforderlich sind, eine nicht blockierende "nicht sichere" Benachrichtigung anzeigt.  Die [SSLMinVersion][DeployedEdgePoliciesSSLMinVersion] -Gruppenrichtlinie ermöglicht die erneute Aktivierung von TLS/1.0 und TLS/1.1; die Richtlinie bleibt verfügbar, bis Edge 88.  |  
| Blockieren von Downloads für gemischten Inhalt | [Chrome + 1](#release-comments) \ (Edge V85 \)  |  | Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Weitere Informationen, einschließlich der geplanten Zeitachse von Google für diese Änderung, finden Sie im [Google Security-Blogeintrag][GoogleBlogSecurity20200206].  Der Microsoft-Rollout-Zeitplan für Dateitypen, die gewarnt oder blockiert werden sollen, ist für eine Version nach Chrome geplant.  |  
| Deprecated AppCache | [Chrome + 1](#release-comments) \ (Edge V86 \)  |  | Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Weitere Informationen finden Sie in der [WebDev-Dokumentation][WebDevAppCacheRemoval].  Der Microsoft-Rollout-Zeitplan für die deprecated-Version ist für eine Version nach Chrome geplant.  Durch Anfordern eines [AppCache-OriginTrial-Tokens][AppCacheOriginTrial] können Websites die veraltete API weiter verwenden, bis Edge-V90. |  
| Entfernen von Adobe Flash | Edge-V88  |  | Diese Änderung findet im Chromium-Projekt statt, auf dem Microsoft Edge basiert.  Weitere Informationen finden Sie in der [Roadmap für Adobe Flash Chrom][ChromiumFlashRoadmapSupportRemoved].  | 
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


<!-- image links -->  

<!-- links -->  

[DeployedEdgePoliciesSSLMinVersion]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin – Microsoft Edge – Richtlinien"  

[ChromePlatformStatus4664843055398912]: https://www.chromestatus.com/feature/4664843055398912 "Synchronisierungs-XMLHttpRequest in Seite Entlassung deaktivieren JavaScript – Chrome-Platt Form Status"  
[ChromePlatformStatus5088147346030592]: https://www.chromestatus.com/feature/5088147346030592 "Cookies standardmäßig auf SameSite = Lax-Chrome Platform-Status"  
[ChromePlatformStatus6251880185331712]: https://www.chromestatus.com/feature/6251880185331712 "Referrer-Richtlinie: standardmäßig zu Strict-Origin-when-Cross-Origin-Chrome-Platt Form Status"  

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Flash-Unterstützung aus Chrom entfernt (Ziel: Chrom 88 +-Jan 2021) – Flash-Roadmap | Chromium-Projekte"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Schützen von Benutzern vor unsicheren Downloads in Google Chrome – Google Online Security-Blog" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal/ "AppCache entfernen"
[AppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "AppCache-OriginTrial-Token"

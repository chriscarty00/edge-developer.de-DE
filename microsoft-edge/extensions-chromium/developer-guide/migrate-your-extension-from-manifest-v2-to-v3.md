---
description: Informationen zum Aktualisieren der Erweiterung von Manifest V2 auf V3
title: Vorbereiten der Aktualisierung Ihrer Erweiterungen von Manifest V2 auf V3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, extensions development, edge extensions, browser extensions, addons, developer, manifest v3, migrate to manifest v3
ms.openlocfilehash: 5aa1aa7446a312d581bacc4fa19ba7362c6c2a3e
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564616"
---
# <a name="prepare-to-update-your-extensions-from-manifest-v2-to-v3"></a>Vorbereiten der Aktualisierung Ihrer Erweiterungen von Manifest v2 auf v3  

In diesem Dokument werden wichtige Änderungen aufgeführt, die im Rahmen von Manifest v3 implementiert werden, der nächsten Version der Chromium Extensions-Plattform.  Das Microsoft Edge-Erweiterungsteam aktualisiert dieses Dokument im Verlauf der Implementierung.  Ausführliche Anleitungen zum Migrieren Ihrer Erweiterung zu Manifest v3 finden Sie unter [Migrieren zu Manifest V3][ChromeDeveloperDocsExtensionsMv3Mv3MigrationChecklist].  

## <a name="remotely-hosted-code"></a>Remote gehosteter Code  

Heute werden Teile des Erweiterungscodes remote gehostet und nicht als Teil des Erweiterungspakets während des Überprüfungsprozesses enthalten.  Dies bietet zwar Flexibilität zum Ändern von Code ohne erneutes Übermitteln der Erweiterung an den Speicher, der Code kann jedoch nach der Installation ausgenutzt werden.  Um [sicherzustellen, Microsoft Edge Add-Ons][MicrosoftMicrosoftedgeAddons] überprüfte Erweiterungen auflistet, wird vom Microsoft Edge-Erweiterungsteam die Verwendung von remote gehosteten Code durch Erweiterungen nicht unterstützt.  Diese Änderung macht Erweiterungen sicherer.  Entwickler müssen den von der Erweiterung verwendeten Code zur Überprüfung packen und übermitteln.  Alternativ können Sie die Funktion `eval()` in einer [Sandkastenumgebung verwenden.][ChromeDeveloperDocsExtensionsMv2Sandboxingeval]  

## <a name="run-time-host-permissions"></a>Laufzeithostberechtigungen  

Bei der Installation können Erweiterungen deckende Berechtigungen für den Zugriff auf alle Websites und Inhalte anfordern.  Diese Berechtigungen ermöglichen es Erweiterungen, mit minimalem Eingriff zu arbeiten und ein Risiko für den Datenschutz und die Sicherheit der Benutzer zu schaffen.  Zur Verbesserung der Transparenz stellt das Microsoft Edge-Erweiterungsteam Steuerelemente für Benutzer zur Verfügung, um den Zugriff auf Websites zur Laufzeit zu erlauben oder einzuschränken.  

## <a name="cross-origin-requests-in-content-scripts"></a>Ursprungsübergreifende Anforderungen in Inhaltsskripts  

Heute fordern Inhaltsskripts Zugriff auf jeden Beliebigen Ursprung an, einschließlich Ursprüngen, die von der Website nicht zulässig sind.  Das Verhalten bricht ursprungsübergreifende Prinzipien.  In Zukunft erfordert das Microsoft Edge-Erweiterungsteam, dass Inhaltsskripts die gleichen Berechtigungen wie die Webseite besitzen, auf der die Skripts eingeschleiert werden, wodurch ein potenzielles Sicherheitslückenschlupf geschlossen wird.  Zum Ausführen von ursprungsübergreifenden Anforderungen müssen Sie Hintergrundskripts verwenden, um Antworten zurück an Inhaltsskripts weiter zu geben.  Diese Änderungen sind verfügbar und hinter einem Flag.  Weitere Informationen finden Sie in diesem [Dokument.][ChromiumHomeChromiumSecurityExtensionContentScriptFetches]  

## <a name="web-request-api"></a>Webanforderungs-API  

Das Microsoft Edge-Erweiterungsteam ersetzt [die Webanforderungs-API][ChromeDeveloperDocsExtensionsReferenceWebrequest] durch [die Deklarative Net Request-API,][ChromeDeveloperDocsExtensionsReferenceDeclarativenetrequest]aber die Beobachtungsfunktionen der Webanforderungs-API bleiben erhalten.  Mit Ausnahme bestimmter Szenarien, in denen beobachtungsspezifische Funktionen der Webanforderungs-API für die Erweiterung erforderlich sind, empfiehlt das Microsoft Edge-Erweiterungsteam, nur die DNR-APIs zu verwenden.  Das Microsoft Edge-Erweiterungsteam ist davon überzeugt, dass diese Änderung positive Auswirkungen auf Erweiterungen haben wird, die funktionsreiche deklarative Funktionen verwenden.  Wenn mehr Erweiterungen auf die DNR-APIs umstellen, wird diese Änderung den Datenschutz der Benutzer verbessern, wodurch das Vertrauen in die Verwendung von Erweiterungen verbessert wird.  
Unternehmen können weiterhin das Blockierungsverhalten der Webanforderungs-API für Erweiterungen verwenden, die über Unternehmensrichtlinien verwaltet werden.  Weitere Informationen zu Erweiterungsrichtlinien finden Sie unter [Microsoft Edge – Policies][DeployedgeMicrosoftEdgePoliciesExtensions].  

## <a name="background-service-workers"></a>Hintergrunddienstmitarbeiter  
 
Servicemitarbeiter stehen für Tests auf Canary zur Verfügung.  Informationen zum Migrieren Ihrer Erweiterungen von Hintergrundseiten zu Servicemitarbeitern finden Sie unter Migrieren von [Hintergrundseiten zu Service Workers][ChromeDeveloperDocsExtensionsMv3MigratingToServiceWorkers].  Das Microsoft Edge-Erweiterungsteam evaluiert und untersucht die Auswirkungen, die diese Änderung für Entwickler und Benutzer mit sich bringt.  Das Microsoft Edge-Erweiterungsteam fügt zusätzliche Details zur Künftigen Änderung dieses Dokuments hinzu.  

## <a name="when-are-these-changes-available-in-microsoft-edge"></a>Wann sind diese Änderungen in Microsoft Edge  

Die aktuelle deklarative Net Request API-Implementierung ist in unseren Stable- und Betakanälen verfügbar.  Testen Sie die Änderungen, und geben Sie Feedback.  Das Microsoft Edge-Erweiterungsteam trägt zur Entwicklung bei und untersucht weitere Änderungen.  

| Kanalname | Details |  
|:--- |:--- |  
| Microsoft Edge 84 Stable | Die DNR-API steht zum Testen zur Verfügung. |  
| Microsoft Edge 85 Beta | Unterstützung für Kopfzeilenänderung ist verfügbar|  

Wenn die Änderungen an Chromium vorgenommen werden, teilt das Microsoft Edge-Erweiterungsteam Zeitachsen, sodass Sie Ihren Code aktualisieren und Erweiterungen erneut im Store veröffentlichen können.  

Das Microsoft Edge-Erweiterungsteam veröffentlicht weiterhin Updates im Blog.  Sie können Ihr Feedback zu den Änderungen über Tech [Community.][MicrosoftTechcommunityT5ArticlesManifestV3ChnagesAreNowAvailableInMicrosoftEdgeMP1780254]

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesExtensions]: /deployedge/microsoft-edge-policies#extensions "Erweiterungen – Microsoft Edge – Richtlinien | Microsoft Docs"  

[MicrosoftMicrosoftedgeAddons]: https://microsoftedge.microsoft.com/addons "Microsoft Edge-Add-Ons"  

[MicrosoftTechcommunityT5ArticlesManifestV3ChnagesAreNowAvailableInMicrosoftEdgeMP1780254]: https://techcommunity.microsoft.com/t5/articles/manifest-v3-changes-are-now-available-in-microsoft-edge/m-p/1780254 "Manifest-V3-Änderungen sind jetzt in Microsoft Edge | Microsoft Tech Community"  

[ChromeDeveloperDocsExtensionsMv2Sandboxingeval]: https://developer.chrome.com/docs/extensions/mv2/sandboxingEval "Verwenden von eval in Chrome-Erweiterungen | Chrome Developers"  
[ChromeDeveloperDocsExtensionsMv3MigratingToServiceWorkers]:  https://developer.chrome.com/docs/extensions/mv3/migrating_to_service_workers "Migrieren von Hintergrundseiten zu Servicemitarbeitern | Chrome Developers"  
[ChromeDeveloperDocsExtensionsMv3Mv3MigrationChecklist]: https://developer.chrome.com/docs/extensions/mv3/mv3-migration-checklist "Checkliste für die Manifest-V3| Chrome Developers"    

[ChromeDeveloperDocsExtensionsReferenceDeclarativenetrequest]: https://developer.chrome.com/docs/extensions/reference/declarativeNetRequest "chrome.declarativeNetRequest | Chrome Developers"  
[ChromeDeveloperDocsExtensionsReferenceWebrequest]: https://developer.chrome.com/docs/extensions/reference/webRequest "chrome.webRequest | Chrome Developers"  

[ChromiumHomeChromiumSecurityExtensionContentScriptFetches]: https://www.chromium.org/Home/chromium-security/extension-content-script-fetches "Änderungen an ursprungsübergreifenden Anforderungen in Chrome-Erweiterungsinhaltsskripts | Die Chromium Projekte"  

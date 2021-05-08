---
description: Informationen zum Aktualisieren der Erweiterung von Manifest V2 auf V3
title: Vorbereiten der Aktualisierung Ihrer Erweiterungen von Manifest V2 auf V3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, extensions development, edge extensions, browser extensions, addons, developer, manifest v3, migrate to manifest v3
ms.openlocfilehash: 262a5cab54dd23f596791c93ec1238619e247333
ms.sourcegitcommit: 1ad087b00df16fd7718a5d95226de57e29b335e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "11117829"
---
# Vorbereiten der Aktualisierung Ihrer Erweiterungen von Manifest v2 auf v3 

In diesem Dokument werden wichtige Änderungen aufgeführt, die im Rahmen von Manifest v3 implementiert werden, der nächsten Version der Chromium Extensions-Plattform. Dieses Dokument wird im Verlauf der Implementierung aktualisiert. Ausführliche Anleitungen zum Migrieren Ihrer Erweiterung zu Manifest v3 finden Sie unter [Migrieren zu Manifest V3][Google_Migrate_to_MV3]. 

## Remote gehosteter Code  

Heute können Erweiterungen Teile ihres Codes remote hosten und nicht als Teil des Erweiterungspakets während des Überprüfungsprozesses enthalten. Dies bietet zwar Flexibilität zum Ändern von Code ohne erneutes Übermitteln der Erweiterung an den Speicher, der Code kann jedoch nach der Installation ausgenutzt werden. Um [sicherzustellen, Microsoft Edge Add-Ons][EdgeAddons] überprüfte Erweiterungen auflistet, wird die Verwendung von remote gehosteten Code durch Erweiterungen nicht zugelassen. Diese Änderung macht Erweiterungen sicherer. Entwickler müssen den von der Erweiterung verwendeten Code zur Überprüfung packen und übermitteln. Alternativ können Entwickler die eval()-Funktion in einer [Sandkastenumgebung verwenden.][sandboxingEval] 

## Laufzeithostberechtigungen  

Bei der Installation können Erweiterungen deckende Berechtigungen für den Zugriff auf alle Websites und Inhalte anfordern. Diese Berechtigungen ermöglichen es Erweiterungen, mit minimalem Eingriff zu arbeiten und ein Risiko für den Datenschutz und die Sicherheit der Benutzer zu schaffen. Um die Transparenz zu verbessern, stellen wir Steuerelemente für Benutzer zur Verfügung, um den Zugriff auf Websites zur Laufzeit zu erlauben oder einzuschränken. 

## Ursprungsübergreifende Anforderungen in Inhaltsskripts  

Heute können Inhaltsskripts Zugriff auf jeden Beliebigen Ursprung anfordern, einschließlich Ursprüngen, die von der Website nicht zulässig sind. Dieses Verhalten bricht ursprungsübergreifende Prinzipien. In Zukunft müssen Inhaltsskripts über die gleichen Berechtigungen wie die Seite verfügen, in die sie eingeschleiert werden, um ein potenzielles Sicherheitslückenschlupf zu schließen. Zum Ausführen von ursprungsübergreifenden Anforderungen müssen Sie Hintergrundskripts verwenden, um Antworten zurück an Inhaltsskripts weiter zu geben. Diese Änderungen sind verfügbar und hinter einem Flag. Weitere Informationen finden Sie in diesem [Dokument.][CORS] 

## Webanforderungs-API  

Wir ersetzen die [Webanforderungs-API][WebRequestAPI] durch [die deklarative Net Request-API,][DeclarativeNetRequestAPI]behalten aber weiterhin die Beobachtungsfunktionen der Webanforderungs-API bei. Außer in bestimmten Szenarien, in denen beobachtungsspezifische Funktionen der Webanforderungs-API für die Erweiterung erforderlich sind, wird empfohlen, nur die DNR-APIs zu verwenden. Wir sind davon überzeugt, dass sich diese Änderung positiv auf Erweiterungen auswirken wird, die deklarative Funktionen mit funktionsreichen Funktionen verwenden. Wenn mehr Erweiterungen auf die DNR-APIs umstellen, wird diese Änderung den Datenschutz der Benutzer verbessern, wodurch das Vertrauen in die Verwendung von Erweiterungen verbessert wird.
Unternehmen können weiterhin das Blockierungsverhalten der Webanforderungs-API für Erweiterungen verwenden, die über Unternehmensrichtlinien verwaltet werden. Weitere Informationen zu Erweiterungsrichtlinien finden Sie unter [Microsoft Edge – Policies][MicrosoftEdgePolicies]. 

## Hintergrunddienstmitarbeiter  
 
Servicemitarbeiter stehen für Tests auf Canary zur Verfügung. Informationen zum Migrieren Ihrer Erweiterungen von Hintergrundseiten zu Servicemitarbeitern finden Sie unter Migrieren von [Hintergrundseiten zu Service Workers][ServiceWorkers]. Wir bewerten die & die Auswirkungen, die diese Änderung für Entwickler und Benutzer mit sich bringt. In Zukunft fügen wir diesem Dokument weitere Details zu dieser Änderung hinzu. 

## Wann werden diese Änderungen in der Microsoft Edge?

Die aktuelle deklarative Net Request API-Implementierung ist in unseren Stable- und Betakanälen verfügbar. Entwickler können diese Änderungen testen und Feedback geben. Wir werden zur Entwicklung beitragen und weitere Änderungen untersuchen. 

| Kanalname | Beschreibung |
|:--- |:--- |  
| Microsoft Edge 84 Stable | Die DNR-API steht zum Testen zur Verfügung. |  
| Microsoft Edge 85 Beta | Unterstützung für Kopfzeilenänderung ist verfügbar| 

Wenn die Änderungen an Chromium vorgenommen werden, teilen wir Zeitachsen, damit Entwickler ihren Code aktualisieren und Erweiterungen für den Store erneut veröffentlichen können. 

Wir veröffentlichen weiterhin Updates in unserem Blog. Sie können Ihr Feedback zu diesen Änderungen über [TechCommunity bereitstellen.][TechCommunity]

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/ "Microsoft Edge Add-Ons"  
[MicrosoftBlog]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration/  
[MicrosoftEdgePolicies]: https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions 

[TechCommunity]: https://techcommunity.microsoft.com/t5/articles/manifest-v3-changes-are-now-available-in-microsoft-edge/m-p/1780254 "Tech-Community"  


[Google_Migrate_to_MV3]: https://developer.chrome.com/extensions/migrating_to_manifest_v3   
[SandboxingEval]: https://developer.chrome.com/apps/sandboxingEval "Verwenden von eval in Chrome Extensions. Sicher."
[CORS]: https://www.chromium.org/Home/chromium-security/extension-content-script-fetches "Änderungen an ursprungsübergreifenden Anforderungen in Erweiterungsinhaltsskripts"
[WebRequestAPI]: https://developer.chrome.com/extensions/webRequest "Webanforderungs-API"  
[DeclarativeNetRequestAPI]: https://developer.chrome.com/extensions/declarativeNetRequest/ "Deklarative Net Request API"
[ServiceWorkers]:  https://developers.chrome.com/extensions/migrating_to_service_workers



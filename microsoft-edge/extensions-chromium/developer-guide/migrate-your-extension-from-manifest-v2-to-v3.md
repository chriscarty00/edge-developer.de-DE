---
description: Informationen zum Aktualisieren ihrer Erweiterung von Manifest v2 auf V3
title: Vorbereiten der Aktualisierung Ihrer Erweiterungen von Manifest v2 auf V3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Edge-Erweiterungen, Browsererweiterungen, Addons, Entwickler, Manifest v3, Migrieren zu Manifest v3
ms.openlocfilehash: 262a5cab54dd23f596791c93ec1238619e247333
ms.sourcegitcommit: 1ad087b00df16fd7718a5d95226de57e29b335e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "11117829"
---
# Vorbereiten der Aktualisierung Ihrer Erweiterungen von Manifest v2 auf V3 

In diesem Dokument sind wichtige Änderungen aufgeführt, die als Teil von Manifest v3, der nächsten Version der Chrom-Erweiterungs Plattform, implementiert werden. Wir aktualisieren dieses Dokument, während die Implementierung fortschreitet. Ausführliche Anleitungen zum Migrieren ihrer Erweiterung zu Manifest V3 finden Sie unter [Migrieren zu Manifest V3][Google_Migrate_to_MV3]. 

## Remote gehosteter Code  

Heute können Erweiterungen Teile Ihres Codes Remote hosten und diese während des Überprüfungsprozesses nicht als Teil des Erweiterungspakets einbeziehen. Dies bietet zwar Flexibilität beim Ändern von Code, ohne die Erweiterung erneut an den Store zu übermitteln, aber der Code kann nach der Installation ausgenutzt werden. Um sicherzustellen, dass [Microsoft Edge-Add-ons][EdgeAddons] überprüfte Erweiterungen auflistet, werden von der Verwendung von Remote gehostetem Code keine Erweiterungen zugelassen. Durch diese Änderung sind Erweiterungen sicherer. Entwickler müssen den gesamten Code, der von der Erweiterung verwendet wird, für die Validierung Verpacken und übermitteln. Alternativ können Entwickler die Funktion eval () in einer Sandbox- [Umgebung][sandboxingEval]verwenden. 

## Laufzeithost Berechtigungen  

Bei der Installationszeit können Erweiterungen für den Zugriff auf alle Websites und Inhalte pauschal Berechtigungen anfordern. Diese Berechtigungen ermöglichen es Erweiterungen, mit minimalem Eingriff zu arbeiten, und ein Risiko für den Datenschutz und die Sicherheit der Benutzer zu schaffen. Zur Verbesserung der Transparenz stellen wir Steuerelemente bereit, mit denen Benutzer den Zugriff auf Websites zur Laufzeit zulassen oder einschränken können. 

## Ursprungs übergreifende Anforderungen in Inhalts Skripts  

Heute können Inhalts Skripts Zugriff auf beliebige Herkunft einschließlich der Herkunft anfordern, die von der Website nicht gestattet ist. Dieses Verhalten verstößt über die Prinzipien des Kreuz Ursprungs. In diesem Fall müssen Inhalts Skripts die gleichen Berechtigungen wie die Seite aufweisen, in die Sie injiziert werden, und ein potenzielles Sicherheitslücke schließen. Zum Durchführen von Cross-Origin-Anforderungen müssen Sie hintergrundskripts verwenden, um Antworten an Inhalts Skripts zurückzuleiten. Diese Änderungen stehen hinter einer Kennzeichnung zur Verfügung. Wenn Sie weitere Informationen wünschen, navigieren Sie zu diesem [Dokument][CORS]. 

## Web Request-API  

Wir ersetzen die [Webanforderungs-API][WebRequestAPI] durch [deklarative net Request-API][DeclarativeNetRequestAPI], behalten aber weiterhin die beobachtungsfunktionen der Webanforderungs-API bei. Außer in einigen bestimmten Szenarien, in denen beobachtungsfunktionen der Webanforderungs-API für die Erweiterung erforderlich sind, wird empfohlen, nur die nur-APIs zu verwenden. Wir sind der Meinung, dass diese Änderung positive Auswirkungen auf Erweiterungen haben wird, die funktionsreiche deklarative Funktionen verwenden. Da sich mehr Erweiterungen auf die "More"-APIs umstellen, verbessert diese Änderung den Datenschutz der Benutzer, was zur Verbesserung des Vertrauens bei der Verwendung von Erweiterungen beiträgt.
Unternehmen können weiterhin das Blockierungsverhalten der Web Request-API für Erweiterungen verwenden, die über Unternehmensrichtlinien verwaltet werden. Weitere Informationen zu Erweiterungs Richtlinien finden Sie unter [Microsoft Edge – Richtlinien][MicrosoftEdgePolicies]. 

## Mitarbeiter des Hintergrund Diensts  
 
Service Mitarbeiter stehen für die Prüfung in Canary zur Verfügung. Wenn Sie Ihre Erweiterungen von Hintergrundseiten zu Servicemitarbeitern migrieren möchten, lesen Sie [Migrieren von Hintergrundseiten zu Dienst Mitarbeitern][ServiceWorkers]. Wir evaluieren & untersuchen, welche Auswirkungen diese Änderung sowohl auf Entwickler als auch auf Benutzer hat. Wir werden weitere Einzelheiten zu dieser Änderung dieses Dokuments in Zukunft hinzufügen. 

## Wann werden diese Änderungen in Microsoft Edge zur Verfügung stehen?

Die aktuelle deklarative net Request-API-Implementierung steht in unseren stable-und Beta-Kanälen zur Verfügung. Entwickler können diese Änderungen testen und Feedback bereitstellen. Wir werden zur Entwicklung beitragen und weitere Änderungen untersuchen. 

| Kanal Name | Beschreibung |
|:--- |:--- |  
| Microsoft Edge 84 stable | Die frei handapi steht zum Testen zur Verfügung. |  
| Microsoft Edge 85 Beta | Unterstützung für Kopfzeilen Änderung verfügbar| 

Wenn die Änderungen an Chrom vorgenommen wurden, geben wir Zeitpläne frei, damit Entwickler ihren Code aktualisieren und Erweiterungen im Store erneut veröffentlichen können. 

Wir veröffentlichen weiterhin Updates auf unserem Blog. Sie können Ihr Feedback zu diesen Änderungen über [TechCommunity][TechCommunity]bereitstellen.

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/ "Microsoft Edge-Add-ons"  
[MicrosoftBlog]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration/  
[MicrosoftEdgePolicies]: https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions 

[TechCommunity]: https://techcommunity.microsoft.com/t5/articles/manifest-v3-changes-are-now-available-in-microsoft-edge/m-p/1780254 "Tech Community"  


[Google_Migrate_to_MV3]: https://developer.chrome.com/extensions/migrating_to_manifest_v3   
[SandboxingEval]: https://developer.chrome.com/apps/sandboxingEval "Verwenden von eval in Chrome-Erweiterungen. Sicher."
[CORS]: https://www.chromium.org/Home/chromium-security/extension-content-script-fetches "Änderungen an Ursprungs übergreifenden Anforderungen in Erweiterungs Inhalts Skripts"
[WebRequestAPI]: https://developer.chrome.com/extensions/webRequest "Web Request-API"  
[DeclarativeNetRequestAPI]: https://developer.chrome.com/extensions/declarativeNetRequest/ "Deklarative net-Anforderungs-API"
[ServiceWorkers]:  https://developers.chrome.com/extensions/migrating_to_service_workers



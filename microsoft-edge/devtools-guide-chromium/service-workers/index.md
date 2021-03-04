---
description: Alles über Service Worker-Verbesserungen und deren Verwendung.
title: Verbesserungen bei Service Worker
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, service worker, PWA
ms.openlocfilehash: 2f32155d1d28d1e65ad29abfe58a414f3e3c6ed7
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387277"
---
# <a name="service-worker-improvements"></a>Verbesserungen bei Service Worker  

Dieser Artikel enthält Informationen zu Verbesserungen an [][MdnServiceWorkerApi] Entwicklertools für die Arbeit mit Servicemitarbeitern und den Netzwerkanforderungen, die jeweils übergeben werden.  Die **Verbesserungen bei den Dienstmitarbeitern** finden Sie in den Tools **Netzwerk,** **Anwendung** **und** Quellen.  Die Verbesserungen vereinfachen die folgenden Aufgaben.  

*   Debuggen basierend auf Service Worker-Zeitachsen.  
    *   Der Anfang einer Anforderung und die Dauer des Bootstrap.  
    *   Aktualisieren auf Dienstmitarbeiterregistrierung.  
    *   Die Laufzeit einer Anforderung mithilfe des [Fetch-Ereignishandlers.][MdnFetchEvent]  
    *   Die Laufzeit aller Abrufereignisse zum Laden eines Clients.  
*   Erkunden Sie die Laufzeitdetails von Fetch-Ereignishandlern, Installieren von Ereignishandlern und Aktivieren von Ereignishandlern.  
*   Schritt in und aus fetch-Ereignishandler mit [Seitenskriptinformationen](#sources).  
    
Die Erfahrungen umfassen drei verschiedene Entwicklertools.  

1.  Das [Netzwerktool.](#network)  Wählen Sie eine Netzwerkanforderung aus, die über einen Servicemitarbeiter ausgeführt wird, und greifen Sie im Timing-Tool auf die entsprechende Zeitachse des **Servicemitarbeiters** zu.  
1.  Das [Application-Tool.](#application)  Navigieren Sie zum Tool Service Workers, um die **Servicemitarbeiter zu** debuggen.  
1.  Das [Tool Sources.](#sources)  Greifen Sie auf Seitenskriptinformationen zu, wenn Sie in fetch-Ereignishandler treten.  
    
## <a name="network"></a>Network  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Dienstarbeitszeitachse im Netzwerktool" lightbox="../media/sw-network-timeline.msft.png":::
   Netzwerkansicht  
:::image-end:::  

Führen Sie eine der folgenden Aktionen aus, um auf die Debugfeatures des Dienstmitarbeiters im **Netzwerktool** zu zugreifen.  

*   Zugriff direkt im **Netzwerktool.**  
*   Gestartet im **Anwendungstool.**  
    
### <a name="request-routing"></a>Anforderungsrouting  

Um das Anforderungsrouting zu vereinfachen, werden auf Zeitachsen jetzt das Start-up des Dienstmitarbeiters und die `respondWith` Abrufereignisse angezeigt.  Führen Sie die folgenden Aktionen aus, um eine Netzwerkanforderung zu debuggen und zu visualisieren, die über einen Dienstmitarbeiter übergeben wurde.  

1.  Wählen Sie die Netzwerkanforderung aus, die über einen Servicemitarbeiter gegangen ist.  
1.  Öffnen Sie das **Timing-Tool.**  
    
### <a name="fetch-events"></a>Abrufen von Ereignissen  

Um mehr über die Abrufereignisse zu erfahren, wählen Sie den Dropdownpfeil links `respondWith` neben der `respondWith` aus.  Verwenden Sie die entsprechenden Dropdownpfeile, um weitere Details zu **der ursprünglichen** Anforderung und der empfangenen Antwort zu finden. ****  

## <a name="application"></a>Application  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Anwendungsansicht" lightbox="../media/sw-application-timeline.msft.png":::
   Anwendungsansicht  
:::image-end:::  

### <a name="service-worker-update-timeline"></a>Zeitachse der Dienstarbeitsmitarbeiteraktualisierung  

Das Microsoft Edge DevTools-Team hat eine Zeitachse im **Anwendungstool** hinzugefügt, um den Updatelebenszyklus des Servicemitarbeiters widerspiegeln zu können.  Es werden die Installations- und Aktivierungsereignisse angezeigt.  Jedes der Ereignisse verfügt über einen entsprechenden Dropdownpfeil, um Weitere Details zu erhalten.  

### <a name="request-routing-and-fetch-events"></a>Routing- und Abrufereignisse anfordern  

Sie können nun über das Netzwerktool in der Konsolenschubleiste auf die Zeitachsen des Dienstarbeitsmitarbeiters zugreifen. ****  Das Feature bietet Vorteile für die Leistung, minimiert die Benutzeroberflächenduplizierung und bietet eine umfassendere Debugoberfläche.  

1.  Öffnen Sie den Servicemitarbeiter, den Sie debuggen möchten.  
1.  Wählen Sie die **Schaltfläche Netzwerk** aus, um die [Anforderungsroutingerfahrung zu öffnen.](#network)  
1.  Verwenden Sie **die respondWith-Dropdowns** zum Abrufen von Ereignisanforderungs- und Antwortinformationen.  

Das **Netzwerktool** zeigt die Netzwerkanforderungen an, die durch den Servicemitarbeiter gegangen sind, den Sie debuggen.  Der automatische Filter ist eine Möglichkeit, die Untersuchung zu einent einengt.

## <a name="sources"></a>Quellen  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="DOM-Ansicht" lightbox="../media/sw-sources.msft.png":::
   DOM-Ansicht  
:::image-end:::  

Um weitere Stapelinformationen zu finden, legen Sie im Abrufhandler einen Haltepunkt ein.  Die Details führen dazu, wo die Ressource im Seitenskript angefordert wird.  Wenn der Debugger innerhalb eines Abrufhandlers angehalten wird, werden im Bereich rechts eine kombinierte Stapelinformationen angezeigt.  Danach können Sie sich in den Stapelframes bewegen.  

### <a name="future-work"></a>Zukünftige Arbeit  

Das Microsoft Edge DevTools-Team plant die Weiterentwicklung des Cachedetails und untersucht weitere Möglichkeiten zur Verbesserung der Debugerfahrung von Dienstmitarbeitern für [Entwickler von progressiven][MdnProgressiveWebApps] Webanwendungen.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Progressive Web Apps (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Dienstarbeits-API-| MDN"  

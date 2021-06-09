---
description: Alles über Service Worker-Verbesserungen und die Verwendung der einzelnen.
title: Verbesserungen für Service Worker
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, f12-Tools, Devtools, Service Worker, PWA
ms.openlocfilehash: c00b7c7fd18d4bb3d413369ec1464c0cb0255311
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597145"
---
# <a name="service-worker-improvements"></a>Verbesserungen für Service Worker  

In diesem Artikel erfahren Sie mehr über Verbesserungen an Entwicklertools für die Arbeit mit [Service-Workern][MdnServiceWorkerApi] und die Netzwerkanforderungen, die jeweils durchgehen.  Die Verbesserungen für **Service Worker** sind in den Tools **"Netzwerk",** **"Anwendung"** und **"Quellen"** enthalten.  Die Verbesserungen vereinfachen die folgenden Aufgaben.  

*   Debuggen basierend auf Service Worker-Zeitachsen.  
    *   Der Anfang einer Anforderung und die Dauer des Bootstrap.  
    *   Aktualisieren sie auf die Service Worker-Registrierung.  
    *   Die Laufzeit einer Anforderung mithilfe des [Fetch-Ereignishandlers.][MdnFetchEvent]  
    *   Die Laufzeit aller Abrufereignisse zum Laden eines Clients.  
*   Erkunden Sie die Laufzeitdetails zum Abrufen von Ereignishandlern, Installieren von Ereignishandlern und Aktivieren von Ereignishandlern.  
*   Treten Sie mit [Seitenskriptinformationen](#sources)in den Ereignishandler ein und aus dem Abruf.  
    
Die Umgebung umfasst drei verschiedene Entwicklertools.  

1.  Das [Netzwerktool.](#network)  Wählen Sie eine Netzwerkanforderung aus, die über einen Service Worker ausgeführt wird, und greifen Sie im **Timing-Tool** auf die entsprechende Zeitachse des Service Worker zu.  
1.  Das [Anwendungstool.](#application)  Navigieren Sie zum Debuggen der Service Worker zum **Service Worker-Tool.**  
1.  Das [Tool "Quellen".](#sources)  Greifen Sie auf Seitenskriptinformationen zu, wenn Sie in das Abrufen von Ereignishandlern eintreten.  
    
## <a name="network"></a>Network  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Zeitachse für Service Worker im Netzwerktool" lightbox="../media/sw-network-timeline.msft.png":::
   Netzwerkansicht  
:::image-end:::  

Führen Sie eine der folgenden Aktionen aus, um auf die Debugfeatures von Service Workern im **Netzwerktool** zuzugreifen.  

*   Zugriff direkt im **Netzwerktool.**  
*   Gestartet im **Anwendungstool.**  
    
### <a name="request-routing"></a>Anforderungsrouting  

Um das Anforderungsrouting einfacher visualisieren zu können, zeigen zeitachsen jetzt das Service Worker-Start-Up und die `respondWith` Abrufereignisse an.  Führen Sie die folgenden Aktionen aus, um eine Netzwerkanforderung zu debuggen und zu visualisieren, die an einen Service Worker übergeben wurde.  

1.  Wählen Sie die Netzwerkanforderung aus, die über einen Service Worker gesendet wurde.  
1.  Öffnen Sie das **Timing-Tool.**  
    
### <a name="fetch-events"></a>Abrufen von Ereignissen  

Um mehr über die Abrufereignisse zu `respondWith` erfahren, wählen Sie den Dropdownpfeil links neben der `respondWith` .  Verwenden Sie die entsprechenden Dropdownpfeile, um weitere Details über die **ursprüngliche Anforderung** und **die empfangene Antwort**zu finden.  

## <a name="application"></a>Anwendung  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Anwendungsansicht" lightbox="../media/sw-application-timeline.msft.png":::
   Anwendungsansicht  
:::image-end:::  

### <a name="service-worker-update-timeline"></a>Zeitachse für Dienstmitarbeiteraktualisierungen  

Das Microsoft Edge DevTools-Team hat eine Zeitachse im **Anwendungstool** hinzugefügt, um den Aktualisierungslebenszyklus des Service Worker widerzuspiegeln.  Es zeigt die Installations- und Aktivierungsereignisse an.  Jedes Ereignis verfügt über einen entsprechenden Dropdownpfeil, um Ihnen weitere Details zu geben.  

### <a name="request-routing-and-fetch-events"></a>Anfordern des Routings und Abrufen von Ereignissen  

Sie können jetzt über das **Netzwerktool** in der Konsolenschublade auf die Zeitachsen der Service worker zugreifen.  Das Feature bietet Vorteile für die Leistung, minimiert die Duplizierung der Benutzeroberfläche und erstellt eine umfassendere Debugumgebung.  

1.  Öffnen Sie den Dienstmitarbeiter, den Sie debuggen.  
1.  Klicken Sie auf die Schaltfläche **"Netzwerk",** um die [Anforderungsweiterleitung](#network)zu öffnen.  
1.  Verwenden Sie die **Dropdowns "respondWith"** zum Abrufen von Ereignisanforderungs- und Antwortinformationen.  

Das **Netzwerktool** zeigt die Netzwerkanforderungen an, die den Dienstmitarbeiter durchlaufen haben, den Sie debuggen.  Mit dem automatischen Filter können Sie Ihre Untersuchung eingrenzen.

## <a name="sources"></a>Quellen  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="DOM-Struktur" lightbox="../media/sw-sources.msft.png":::
   DOM-Struktur  
:::image-end:::  

Um weitere Stapelinformationen zu finden, legen Sie einen Haltepunkt im Fetch-Handler fest.  Die Details führen dazu, wo die Ressource im Seitenskript angefordert wird.  Wenn der Debugger innerhalb eines Abrufhandlers angehalten wird, werden im Bereich auf der rechten Seite kombinierte Stapelinformationen angezeigt.  Danach können Sie sich in den Stapelframes bewegen.  

### <a name="future-work"></a>Zukünftige Arbeit  

Das Microsoft Edge DevTools-Team plant, das Cachedetail weiter zu entwickeln, und untersucht weitere Möglichkeiten, um das Debuggen von Service Workern für [Progressive Webanwendungsentwickler][MdnProgressiveWebApps] zu verbessern.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | Mdn"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Progressive Web Apps (PWAs) | Mdn"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Dienstmitarbeiter-API-| Mdn"  

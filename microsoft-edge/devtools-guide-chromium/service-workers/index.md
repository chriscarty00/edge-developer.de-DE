---
description: Informationen zu den Verbesserungen der Dienstmitarbeiter und zur Verwendung der einzelnen Dienste.
title: Verbesserungen der Dienstmitarbeiter
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Service Worker, PWA
ms.openlocfilehash: 4e1b43235ccd7b108d2aadd1c803aa3276fa1265
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190034"
---
# Verbesserungen der Dienstmitarbeiter  

In diesem Artikel werden die Verbesserungen an [Servicemitarbeitern][MdnServiceWorkerApi] und die Netzwerkanforderungen erläutert, die jeweils durchlaufen werden.  Die **Verbesserungen der Dienstmitarbeiter** befinden sich in den Tools **Netzwerk**, **Anwendung**und **Quellen** .  Die Verbesserungen umfassen die folgenden Aufgaben.  

*   Debuggen basierend auf den Zeitrahmen für Dienstmitarbeiter.  
    *   Der Anfang einer Anforderung und die Dauer des Bootstrap.  
    *   Aktualisieren Sie die Service Worker-Registrierung.  
    *   Die Laufzeit einer Anforderung mit dem [Fetch-Ereignis][MdnFetchEvent] Handler.  
    *   Die Laufzeit aller FETCH-Ereignisse zum Laden eines Clients.  
*   Erkunden Sie die Laufzeitdetails von FETCH-Ereignishandlern, installieren Sie Ereignishandler, und aktivieren Sie Ereignishandler.  
*   Ein-und Auschecken des FETCH-Ereignishandlers mit [Seitenskript Informationen](#sources)  

Die Erfahrungen umfassen drei verschiedene Entwicklertools.  

1.  Das [Netzwerk](#network) Tool.  Wählen Sie eine Netzwerkanforderung aus, die über einen Dienstmitarbeiter ausgeführt wird, und greifen Sie im Tool **Zeitmessung** auf die entsprechende Zeitachse des Dienst Mitarbeiters zu.  
1.  Das [Anwendungs](#application) Tool.  Navigieren Sie zum Debuggen der Dienstmitarbeiter zum Tool **Dienstmitarbeiter** .  
1.  Das Tool " [Quellen](#sources) ".  Zugriffsseiten-Skript Informationen, wenn Sie zu Fetch-Ereignishandlern springen.  

## Network  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Service Worker-Zeitachse im Netzwerktool" lightbox="../media/sw-network-timeline.msft.png":::
   Netzwerkansicht  
:::image-end:::  

Führen Sie eine der folgenden Aktionen aus, um auf die Features des Dienstmitarbeiter Debuggens im Tool **Netzwerk** zuzugreifen.  

*   Direkter Zugriff auf das **Netzwerk** Tool.  
*   Im **Anwendungs** Tool gestartet.  
    
### Routing anfordern  

Um die Visualisierung von Anforderungs Routing zu vereinfachen, werden in den Zeitplänen nun die Start-und die FETCH-Ereignisse für den Dienstmitarbeiter angezeigt `respondWith` .  Führen Sie die folgenden Aktionen aus, um eine Netzwerkanforderung zu Debuggen und zu visualisieren, die von einem Dienstmitarbeiter durchgeführt wurde.  

1.  Wählen Sie die Netzwerkanforderung aus, die von einem Dienstmitarbeiter durchlaufen wurde.  
1.  Öffnen Sie das Tool **Anzeige** Dauer.  
    
### Abrufen von Ereignissen  

Wenn Sie mehr über die `respondWith` Fetch-Ereignisse erfahren möchten, wählen Sie den Dropdownpfeil links neben dem aus `respondWith` .  Wenn Sie weitere Details zur **ursprünglichen Anforderung** und **Antwort erhalten**möchten, verwenden Sie die entsprechenden Dropdownpfeile.  

## Application  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Anwendungsansicht" lightbox="../media/sw-application-timeline.msft.png":::
   Anwendungsansicht  
:::image-end:::  

### Zeitachsen Update für Dienstmitarbeiter  

Das Microsoft Edge devtools-Team hat im **Anwendungs** Tool eine Zeitachse hinzugefügt, um den Update-Lebenszyklus des Dienst Mitarbeiters wiederzugeben.  Sie zeigt die Installations-und Aktivierungsereignisse an.  Jedes der Ereignisse verfügt über einen entsprechenden Dropdownpfeil, um weitere Informationen zu erhalten.  

### Anfordern von Routing-und FETCH-Ereignissen  

Sie können nun über das Tool **Netzwerk** im Konsolen Einzug auf die Zeitpläne für Dienstmitarbeiter zugreifen.  Das Feature profitiert von der Leistung, minimiert die Duplizierung von Benutzeroberflächen und erstellt ein umfassenderes Debugging.  

1.  Öffnen Sie den zu debuggenden Dienstmitarbeiter.  
1.  Wählen Sie die Schaltfläche **Netzwerk** aus, um die [Anforderungs Routing-Umgebung](#network)zu öffnen.  
1.  Verwenden Sie die **respondWith** -Dropdownlisten für Fetch Event Request-und Response-Informationen.  

Das Tool **Netzwerk** zeigt die Netzwerkanforderungen an, die durch den Dienstmitarbeiter durchlaufen wurden, den Sie Debuggen.  Der automatische Filter ist eine Möglichkeit, ihre Exploration zu verkleinern.

## Quellen  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="DOM-Ansicht" lightbox="../media/sw-sources.msft.png":::
   DOM-Ansicht  
:::image-end:::  

Wenn Sie weitere Stapel Informationen finden möchten, legen Sie im FETCH-Handler einen Unterbrechungspunkt fest.  Die Details führen zu dem Ort, an dem die Ressource im Seitenskript angefordert wird.  Wenn der Debugger in einem Fetch-Handler angehalten wird, wird im Bereich auf der rechten Seite eine kombinierte Stapel Informationen angezeigt.  Anschließend können Sie in den Stapelrahmen navigieren.  

### Zukünftige Arbeit  

Das Microsoft Edge devtools-Team plant, die Cache Details weiter zu entwickeln und untersucht mehr Möglichkeiten zur Verbesserung der Service Worker-Debugging-Erfahrung für Entwickler von [progressiven Webanwendungen][MdnProgressiveWebApps] .  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Progressive Web-Apps (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker-API | MDN"  

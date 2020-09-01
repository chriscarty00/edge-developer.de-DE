---
title: Debuggen von Hintergrunddiensten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 1fecd6f9c1dceb39482bf8c4ade71918e32dec00
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983288"
---
<!-- Copyright Kayce Basques 
   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0
       
   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# Debuggen von Hintergrunddiensten mit Microsoft Edge devtools   



Der Abschnitt " **Hintergrunddienste** " von Microsoft Edge devtools ist eine Sammlung von Tools für die JavaScript-APIs, mit deren Hilfe Ihre Website Updates senden und empfangen kann, auch wenn ein Benutzer die Website nicht geöffnet hat.  
Ein Hintergrunddienst ähnelt einem [Hintergrundprozess] [WikiBackgroundProcess].  
Microsoft Edge devtools berücksichtigt jede der folgenden APIs als Hintergrunddienst:  

*   [Hintergrund Abruf](#background-fetch)  
*   [Hintergrundsynchronisierung](#background-sync)  
*   [Benachrichtigungen](#notifications)  
*   [Push-Nachrichten](#push-messages)  
    
Microsoft Edge devtools kann Hintergrunddienst Ereignisse für 3 Tage protokollieren, auch wenn devtools nicht geöffnet ist.  
Auf diese Weise können Sie sicherstellen, dass Ereignisse wie erwartet gesendet und empfangen werden.  Sie können auch die Details zu den einzelnen Ereignissen prüfen.  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich "Push-Messaging"" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   Anzeigen der Details eines Ereignisses im Bereich " **Push-Messaging** "  
:::image-end:::  

## Hintergrund Abruf   

Die *Background FETCH-API** ermöglicht es einem **Dienstmitarbeiter** , große Ressourcen wie Filme oder Podcasts als Hintergrunddienst zuverlässig herunterzuladen.  So protokollieren Sie das Hintergrund-FETCH-Ereignis für 3 Tage, auch wenn devtools nicht geöffnet ist:  

<!--Todo: add background fetch api section when available -->  

1.  [Öffnen Sie devtools][OpenDevTools].  
1.  Öffnen Sie den **Anwendungs** Panel.  
1.  Öffnen des Bereichs " **Hintergrund Abruf** "  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Der Bereich "Fetch-Hintergrund"" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       Der Bereich " **Fetch-Hintergrund** "  
    :::image-end:::  
    
1.  Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).  
   Nach dem Auslösen einiger Hintergrund Abruf Aktivitäten protokolliert devtools die Ereignisse in der Tabelle.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Ereignisprotokoll im Bereich "Fetch-Hintergrund"" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       Ereignisprotokoll im Bereich " **Fetch-Hintergrund** "  
    :::image-end:::  
    
1.  Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Hintergrund Abruf Bereich" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       Anzeigen der Details eines Ereignisses im **Hintergrund Abruf** Bereich  
    :::image-end:::  
    
## Hintergrundsynchronisierung   

Die **Hintergrund Synchronisierungs-API** ermöglicht es einem Offline **Dienstmitarbeiter** , Daten an einen Server zu senden, nachdem eine zuverlässige Internetverbindung wiederhergestellt wurde.  So protokollieren Sie Hintergrund Synchronisierungsereignisse für 3 Tage, auch wenn devtools nicht geöffnet ist:  

<!--Todo: add background sync api section when available -->  

1.  [Öffnen Sie devtools][OpenDevTools].  
1.  Öffnen Sie den **Anwendungs** Panel.  
1.  Öffnen des Bereichs " **Hintergrundsynchronisierung** "  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Der Bereich "Hintergrundsynchronisierung"" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       Der Bereich " **Hintergrundsynchronisierung** "  
    :::image-end:::  
    
1.  Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).  
   Nach dem Auslösen einiger Hintergrund Synchronisierungsaktivitäten protokolliert devtools die Ereignisse in der Tabelle.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Ereignisprotokoll im Bereich "Hintergrundsynchronisierung"" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       Ereignisprotokoll im Bereich " **Hintergrundsynchronisierung** "  
    :::image-end:::  
    
1.  Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich "Hintergrundsynchronisierung"" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       Anzeigen der Details eines Ereignisses im Bereich " **Hintergrundsynchronisierung** "  
    :::image-end:::  
    
## Benachrichtigungen 

Nachdem ein **Dienstmitarbeiter** eine Push- [Nachricht][MDNPush] von einem Server erhalten hat, verwendet der Dienstmitarbeiter die [Benachrichtigungs-API][MDNNotifications] , um die Daten für einen Benutzer anzuzeigen.  So protokollieren Sie Benachrichtigungen für 3 Tage, auch wenn devtools nicht geöffnet ist:  

1.  [Öffnen Sie devtools][OpenDevTools].  
1.  Öffnen Sie den **Anwendungs** Panel.  
1.  Öffnen Sie den Bereich **Benachrichtigungen** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Der Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       Der Bereich " **Benachrichtigungen** "  
    :::image-end:::  
    
1.  Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).  
   Nach dem Auslösen einiger Benachrichtigungs Aktivitäten protokolliert devtools die Ereignisse in der Tabelle.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Ereignisprotokoll im Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       Ereignisprotokoll im Bereich " **Benachrichtigungen** "  
    :::image-end:::  
    
1.  Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       Anzeigen der Details eines Ereignisses im Bereich " **Benachrichtigungen** "  
    :::image-end:::  
    
## Push-Nachrichten 

Um eine Push-Benachrichtigung für einen Benutzer anzuzeigen, muss ein **Dienstmitarbeiter** zuerst die [Push-Nachrichten-API][MDNPush] verwenden, um Daten von einem Server zu empfangen.  Wenn der Dienstmitarbeiter bereit ist, die Benachrichtigung anzuzeigen, wird die Benachrichtigungs [-API][MDNNotifications]verwendet.  So protokollieren Sie Push-Nachrichten für 3 Tage, auch wenn devtools nicht geöffnet ist:  

1.  [Öffnen Sie devtools][OpenDevTools].  
1.  Öffnen Sie den **Anwendungs** Panel.  
1.  Öffnen Sie den Bereich **Push-Messaging** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Der Bereich "Push-Messaging"" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       Der Bereich " **Push-Messaging** "  
    :::image-end:::  
    
1.  Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).  
    Nach dem Auslösen einiger Push-Nachrichten Aktivitäten protokolliert devtools die Ereignisse in der Tabelle.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Ereignisprotokoll im Bereich "Push-Messaging"" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       Ereignisprotokoll im Bereich " **Push-Messaging** "  
    :::image-end:::  
    
1.  Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich "Push-Messaging"" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       Anzeigen der Details eines Ereignisses im Bereich " **Push-Messaging** "  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open.md "Open Microsoft Edge (Chrom) Developer Tools | Microsoft docs"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "Hintergrundprozess – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  
[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

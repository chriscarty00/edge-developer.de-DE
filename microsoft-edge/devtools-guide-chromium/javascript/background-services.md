---
title: Debuggen von Hintergrunddiensten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 0ac2a057307a939069cbb3b48ecd38c9de71e5db
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581831"
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
Auf diese Weise können Sie sicherstellen, dass Ereignisse wie erwartet gesendet und empfangen werden.  Sie können auch die Details zu den einzelnen Ereignissen überprüfen.  

> ##### Abbildung1  
> Anzeigen der Details eines Ereignisses im Bereich "Push-Messaging"  
> ![Anzeigen der Details eines Ereignisses im Bereich "Push-Messaging"][PushDetails]  

## Hintergrund Abruf   

Die *Background FETCH-API** ermöglicht es einem **Dienstmitarbeiter** , große Ressourcen wie Filme oder Podcasts als Hintergrunddienst zuverlässig herunterzuladen.  So protokollieren Sie das Hintergrund-FETCH-Ereignis für 3 Tage, auch wenn devtools nicht geöffnet ist:  

<!--Todo: add background fetch api section when available -->  

1.  [Öffnen Sie devtools][OpenDevTools].  
1.  Öffnen Sie den **Anwendungs** Panel.  
1.  Öffnen des Bereichs " **Hintergrund Abruf** "  
    
    > ##### Abbildung2  
    > Der Bereich "Fetch-Hintergrund"  
    > ![Der Bereich "Fetch-Hintergrund"][FetchEmpty]  
    
1.  Klicken Sie auf **Datensatz** aufzeichnen ![ ][ImageRecordIcon] .  
   Nach dem Auslösen einiger Hintergrund Abruf Aktivitäten protokolliert devtools die Ereignisse in der Tabelle.  
    
    > ##### Abbildung 3  
    > Ereignisprotokoll im Bereich "Fetch-Hintergrund"  
    > ![Ereignisprotokoll im Bereich "Fetch-Hintergrund"][FetchLog]  
    
1.  Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.  
    
    > ##### Abbildung4  
    > Anzeigen der Details eines Ereignisses im Bereich "Fetch im Hintergrund"  
    > ![Anzeigen der Details eines Ereignisses im Bereich "Fetch im Hintergrund"][FetchDetails]  

## Hintergrundsynchronisierung   

Die **Hintergrund Synchronisierungs-API** ermöglicht es einem Offline **Dienstmitarbeiter** , Daten an einen Server zu senden, nachdem eine zuverlässige Internetverbindung wiederhergestellt wurde.  So protokollieren Sie Hintergrund Synchronisierungsereignisse für 3 Tage, auch wenn devtools nicht geöffnet ist:  

<!--Todo: add background sync api section when available -->  

1.  [Öffnen Sie devtools][OpenDevTools].  
1.  Öffnen Sie den **Anwendungs** Panel.  
1.  Öffnen des Bereichs " **Hintergrundsynchronisierung** "  
    
    > ##### Abbildung5  
    > Der Bereich "Hintergrundsynchronisierung"  
    > ![Der Bereich "Hintergrundsynchronisierung"][SyncEmpty]  
    
1.  Klicken Sie auf **Datensatz** aufzeichnen ![ ][ImageRecordIcon] .  
   Nach dem Auslösen einiger Hintergrund Synchronisierungsaktivitäten protokolliert devtools die Ereignisse in der Tabelle.  
    
    > ##### Abbildung6  
    > Ereignisprotokoll im Bereich "Hintergrundsynchronisierung"  
    > ![Ereignisprotokoll im Bereich "Hintergrundsynchronisierung"][SyncLog]  
    
1.  Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.  
    
    > ##### Abbildung7  
    > Anzeigen der Details eines Ereignisses im Hintergrund Synchronisierungsbereich  
    > ![Anzeigen der Details eines Ereignisses im Hintergrund Synchronisierungsbereich][SyncDetails]  
    
## Benachrichtigungen 

Nachdem ein **Dienstmitarbeiter** eine Push- [Nachricht][MDNPush] von einem Server erhalten hat, verwendet der Dienstmitarbeiter die [Benachrichtigungs-API][MDNNotifications] , um die Daten für einen Benutzer anzuzeigen.  So protokollieren Sie Benachrichtigungen für 3 Tage, auch wenn devtools nicht geöffnet ist:  

1.  [Öffnen Sie devtools][OpenDevTools].  
1.  Öffnen Sie den **Anwendungs** Panel.  
1.  Öffnen Sie den Bereich **Benachrichtigungen** .  
    
    > ##### Abbildung8  
    > Der Bereich "Benachrichtigungen"  
    > ![Der Bereich "Benachrichtigungen"][NotificationsEmpty]  
    
1.  Klicken Sie auf **Datensatz** aufzeichnen ![ ][ImageRecordIcon] .  
   Nach dem Auslösen einiger Benachrichtigungs Aktivitäten protokolliert devtools die Ereignisse in der Tabelle.  
    
    > ##### Abbildung 9  
    > Ereignisprotokoll im Bereich "Benachrichtigungen"  
    > ![Ereignisprotokoll im Bereich "Benachrichtigungen"][NotificationsLog]  
    
1.  Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.  
    
    > ##### Abbildung 10  
    > Anzeigen der Details eines Ereignisses im Bereich "Benachrichtigungen"  
    > ![Anzeigen der Details eines Ereignisses im Bereich "Benachrichtigungen"][NotificationsDetails]  
    
## Push-Nachrichten 

Um eine Push-Benachrichtigung für einen Benutzer anzuzeigen, muss ein **Dienstmitarbeiter** zuerst die [Push-Nachrichten-API][MDNPush] verwenden, um Daten von einem Server zu empfangen.  Wenn der Dienstmitarbeiter bereit ist, die Benachrichtigung anzuzeigen, wird die Benachrichtigungs [-API][MDNNotifications]verwendet.  So protokollieren Sie Push-Nachrichten für 3 Tage, auch wenn devtools nicht geöffnet ist:  

1.  [Öffnen Sie devtools][OpenDevTools].  
1.  Öffnen Sie den **Anwendungs** Panel.  
1.  Öffnen Sie den Bereich **Push-Messaging** .  
    
    > ##### Abbildung 11  
    > Der Bereich "Push-Messaging"  
    > ![Der Bereich "Push-Messaging"][PushEmpty]  

1.  Klicken Sie auf **Datensatz** aufzeichnen ![ ][ImageRecordIcon] .  
    Nach dem Auslösen einiger Push-Nachrichten Aktivitäten protokolliert devtools die Ereignisse in der Tabelle.  
    
    > ##### Abbildung 12  
    > Ereignisprotokoll im Bereich "Push-Messaging"  
    > ![Ereignisprotokoll im Bereich "Push-Messaging"][PushLog]  

1.  Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.  
    
    > ##### Abbildung 13  
    > Anzeigen der Details eines Ereignisses im Bereich "Push-Messaging"  
    > ![Anzeigen der Details eines Ereignisses im Bereich "Push-Messaging"][PushDetails2]  
    
 



<!-- image links -->  

[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[PushDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging.msft.png "Abbildung 1: Anzeigen der Details eines Ereignisses im Bereich "Push-Messaging""  
[FetchEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch-empty.msft.png "Abbildung 2: der Bereich "Fetch im Hintergrund""  
[FetchLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch.msft.png "Abbildung 3: ein Protokoll von Ereignissen im Bereich "Fetch im Hintergrund""  
[FetchDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch-details.msft.png "Abbildung 4: Anzeigen der Details eines Ereignisses im Bereich "Fetch im Hintergrund""  
[SyncEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync-empty.msft.png "Abbildung 5: der Bereich "Hintergrundsynchronisierung""  
[SyncLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync.msft.png "Abbildung 6: ein Protokoll von Ereignissen im Hintergrund Synchronisierungsbereich"  
[SyncDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync-details.msft.png "Abbildung 7: Anzeigen der Details eines Ereignisses im Hintergrund Synchronisierungsbereich"  
[NotificationsEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications-empty.msft.png "Abbildung 8: der Bereich "Benachrichtigungen""  
[NotificationsLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications.msft.png "Abbildung 9: ein Protokoll von Ereignissen im Bereich "Benachrichtigungen""  
[NotificationsDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications-details.msft.png "Abbildung 10: Anzeigen der Details eines Ereignisses im Bereich "Benachrichtigungen""  
[PushEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging-empty.msft.png "Abbildung 11: der Bereich "Push-Messaging""  
[PushLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging.msft.png "Abbildung 12: ein Protokoll von Ereignissen im Bereich "Push-Messaging""  
[PushDetails2]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging-details.msft.png "Abbildung 13: Anzeigen der Details eines Ereignisses im Bereich "Push-Messaging""  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open.md "Öffnen von Microsoft Edge (Chrom)-Entwickler Tools"  

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

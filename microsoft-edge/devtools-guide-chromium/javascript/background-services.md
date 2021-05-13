---
description: Debuggen von Hintergrund-Abruf, Hintergrundsynchronisierung, Benachrichtigungen und Pushnachrichten mit Microsoft Edge DevTools.
title: Debuggen von Hintergrunddiensten mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 4f5f52bcde976cea8432e3160a792438e5603e21
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564196"
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
# <a name="debug-background-services-with-microsoft-edge-devtools"></a>Debuggen von Hintergrunddiensten mit Microsoft Edge DevTools  

Der **Abschnitt Hintergrunddienste** von Microsoft Edge DevTools ist eine Sammlung von Tools für die JavaScript-APIs, mit denen Ihre Website Updates senden und empfangen kann, auch wenn ein Benutzer Ihre Website nicht geöffnet hat.  
Ein Hintergrunddienst ähnelt einem [Hintergrundprozess][WikiBackgroundProcess].  
Microsoft Edge DevTools betrachtet jede der folgenden APIs als Hintergrunddienst:  

*   [Hintergrund-Abruf](#background-fetch)  
*   [Hintergrundsynchronisierung](#background-sync)  
*   [Benachrichtigungen](#notifications)  
*   [Pushnachrichten](#push-messages)  
    
Microsoft Edge DevTools protokolliert möglicherweise Hintergrunddienstereignisse für 3 Tage, auch wenn DevTools nicht geöffnet ist.  
Das Protokoll für Hintergrunddienstereignisse kann Ihnen dabei helfen, sicherzustellen, dass Ereignisse wie erwartet gesendet und empfangen werden.  Sie können auch die Details der einzelnen Ereignisse überprüfen.  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Der Bereich Push Messaging" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   Der **Bereich Push Messaging**  
:::image-end:::  

## <a name="background-fetch"></a>Hintergrund-Abruf  

Die **Background Fetch-API** ermöglicht es einem **Servicemitarbeiter,** große Ressourcen wie Filme oder Podcasts zuverlässig als Hintergrunddienst herunterzuladen.  So protokollieren Sie das Background Fetch-Ereignis für 3 Tage, auch wenn DevTools nicht geöffnet ist:  

<!--Todo: add background fetch api section when available -->  

1.  [Öffnen Sie DevTools][OpenDevTools].  
1.  Öffnen Sie das **Anwendungstool.**  
1.  Öffnen Sie **den Bereich Hintergrund-Abruf.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Der Hintergrund-Abrufbereich" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       Der **Hintergrund-Abrufbereich**  
    :::image-end:::  
    
1.  Wählen **Sie Record** \( Record ![ ](../media/record-icon.msft.png) \).  
   Nach dem Auslösen einiger Background Fetch-Aktivität protokolliert DevTools die Ereignisse in der Tabelle.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Ein Protokoll mit Ereignissen im Hintergrund-Abrufbereich" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       Ein Protokoll mit Ereignissen im **Hintergrund-Abrufbereich**  
    :::image-end:::  
    
1.  Wählen Sie ein Ereignis aus, um seine Details im Bereich unterhalb der Tabelle anzuzeigen.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich Hintergrund-Abruf" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       Anzeigen der Details eines Ereignisses im **Bereich Hintergrund-Abruf**  
    :::image-end:::  
    
## <a name="background-sync"></a>Hintergrundsynchronisierung  

Die **Hintergrundsynchronisierungs-API** ermöglicht es einem **Offlinedienstmitarbeiter,** Daten an einen Server zu senden, sobald eine zuverlässige Internetverbindung wie hergestellt wurde.  So protokollieren Sie Hintergrundsynchronisierungsereignisse für 3 Tage, auch wenn DevTools nicht geöffnet ist:  

<!--Todo: add background sync api section when available -->  

1.  [Öffnen Sie DevTools][OpenDevTools].  
1.  Öffnen Sie das **Anwendungstool.**  
1.  Öffnen Sie **den Bereich Hintergrundsynchronisierung.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Der Bereich Hintergrundsynchronisierung" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       Der **Bereich Hintergrundsynchronisierung**  
    :::image-end:::  
    
1.  Wählen **Sie Record** \( Record ![ ](../media/record-icon.msft.png) \).  
   Nachdem einige Hintergrundsynchronisierungsaktivitäten ausgelöst wurden, protokolliert DevTools die Ereignisse in der Tabelle.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Ein Ereignisprotokoll im Bereich Hintergrundsynchronisierung" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       Ein Ereignisprotokoll im **Bereich Hintergrundsynchronisierung**  
    :::image-end:::  
    
1.  Wählen Sie ein Ereignis aus, um seine Details im Bereich unterhalb der Tabelle anzuzeigen.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich Hintergrundsynchronisierung" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       Anzeigen der Details eines Ereignisses im **Bereich Hintergrundsynchronisierung**  
    :::image-end:::  
    
## <a name="notifications"></a>Benachrichtigungen  

Nachdem ein **Dienstmitarbeiter** eine [Pushnachricht][MDNPush] von einem Server empfangen hat, verwendet der Dienstmitarbeiter die [Notifications-API,][MDNNotifications] um die Daten einem Benutzer anzuzeigen.  So protokollieren Sie Benachrichtigungen für 3 Tage, auch wenn DevTools nicht geöffnet ist:  

1.  [Öffnen Sie DevTools][OpenDevTools].  
1.  Öffnen Sie das **Anwendungstool.**  
1.  Öffnen Sie den **Bereich Benachrichtigungen.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Der Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       Der **Bereich "Benachrichtigungen"**  
    :::image-end:::  
    
1.  Wählen **Sie Record** \( Record ![ ](../media/record-icon.msft.png) \).  
   Nachdem einige Benachrichtigungsaktivitäten ausgelöst wurden, protokolliert DevTools die Ereignisse in der Tabelle.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Ein Ereignisprotokoll im Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       Ein Ereignisprotokoll im Bereich **"Benachrichtigungen"**  
    :::image-end:::  
    
1.  Wählen Sie ein Ereignis aus, um seine Details im Bereich unterhalb der Tabelle anzuzeigen.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich Benachrichtigungen" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       Anzeigen der Details eines Ereignisses im Bereich **Benachrichtigungen**  
    :::image-end:::  
    
## <a name="push-messages"></a>Pushnachrichten  

Um einem Benutzer eine Pushbenachrichtigung **** anzeigen zu können, muss ein Dienstmitarbeiter zunächst die [Pushnachrichten-API][MDNPush] verwenden, um Daten von einem Server zu empfangen.  Wenn der Dienstmitarbeiter bereit ist, die Benachrichtigung anzuzeigen, verwendet er die [Benachrichtigungs-API][MDNNotifications].  So protokollieren Sie Pushnachrichten für 3 Tage, auch wenn DevTools nicht geöffnet ist:  

1.  [Öffnen Sie DevTools][OpenDevTools].  
1.  Öffnen Sie das **Anwendungstool.**  
1.  Öffnen Sie den **Pushnachrichtenbereich.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Öffnen des Pushnachrichtenbereichs" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       Öffnen des **Pushnachrichtenbereichs**  
    :::image-end:::  
    
1.  Wählen **Sie Record** \( Record ![ ](../media/record-icon.msft.png) \).  
    Nachdem einige Pushnachrichtenaktivitäten ausgelöst wurden, protokolliert DevTools die Ereignisse in der Tabelle.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Ein Ereignisprotokoll im Pushnachrichtenbereich" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       Ein Ereignisprotokoll im **Pushnachrichtenbereich**  
    :::image-end:::  
    
1.  Wählen Sie ein Ereignis aus, um die Details im Bereich unterhalb der Tabelle anzuzeigen.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Pushnachrichtenbereich" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       Anzeigen der Details eines Ereignisses im **Pushnachrichtenbereich**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open/index.md "Öffnen Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API-| MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API-| MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "Hintergrundprozess – Wikipedia"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  
[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

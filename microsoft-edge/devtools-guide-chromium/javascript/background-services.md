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





# <span data-ttu-id="d564f-103">Debuggen von Hintergrunddiensten mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="d564f-103">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="d564f-104">Der Abschnitt " **Hintergrunddienste** " von Microsoft Edge devtools ist eine Sammlung von Tools für die JavaScript-APIs, mit deren Hilfe Ihre Website Updates senden und empfangen kann, auch wenn ein Benutzer die Website nicht geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="d564f-104">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="d564f-105">Ein Hintergrunddienst ähnelt einem [Hintergrundprozess] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="d564f-105">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="d564f-106">Microsoft Edge devtools berücksichtigt jede der folgenden APIs als Hintergrunddienst:</span><span class="sxs-lookup"><span data-stu-id="d564f-106">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="d564f-107">Hintergrund Abruf</span><span class="sxs-lookup"><span data-stu-id="d564f-107">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="d564f-108">Hintergrundsynchronisierung</span><span class="sxs-lookup"><span data-stu-id="d564f-108">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="d564f-109">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="d564f-109">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="d564f-110">Push-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="d564f-110">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="d564f-111">Microsoft Edge devtools kann Hintergrunddienst Ereignisse für 3 Tage protokollieren, auch wenn devtools nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="d564f-111">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="d564f-112">Auf diese Weise können Sie sicherstellen, dass Ereignisse wie erwartet gesendet und empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="d564f-112">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="d564f-113">Sie können auch die Details zu den einzelnen Ereignissen prüfen.</span><span class="sxs-lookup"><span data-stu-id="d564f-113">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich "Push-Messaging"" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="d564f-115">Anzeigen der Details eines Ereignisses im Bereich " **Push-Messaging** "</span><span class="sxs-lookup"><span data-stu-id="d564f-115">View the details of an event in the **Push Messaging** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="d564f-116">Hintergrund Abruf</span><span class="sxs-lookup"><span data-stu-id="d564f-116">Background Fetch</span></span>   

<span data-ttu-id="d564f-117">Die *Background FETCH-API*\* ermöglicht es einem **Dienstmitarbeiter** , große Ressourcen wie Filme oder Podcasts als Hintergrunddienst zuverlässig herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="d564f-117">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="d564f-118">So protokollieren Sie das Hintergrund-FETCH-Ereignis für 3 Tage, auch wenn devtools nicht geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="d564f-118">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="d564f-119">[Öffnen Sie devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="d564f-119">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="d564f-120">Öffnen Sie den **Anwendungs** Panel.</span><span class="sxs-lookup"><span data-stu-id="d564f-120">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="d564f-121">Öffnen des Bereichs " **Hintergrund Abruf** "</span><span class="sxs-lookup"><span data-stu-id="d564f-121">Open the **Background Fetch** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Der Bereich "Fetch-Hintergrund"" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="d564f-123">Der Bereich " **Fetch-Hintergrund** "</span><span class="sxs-lookup"><span data-stu-id="d564f-123">The **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d564f-124">Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d564f-124">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="d564f-125">Nach dem Auslösen einiger Hintergrund Abruf Aktivitäten protokolliert devtools die Ereignisse in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d564f-125">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Ereignisprotokoll im Bereich "Fetch-Hintergrund"" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="d564f-127">Ereignisprotokoll im Bereich " **Fetch-Hintergrund** "</span><span class="sxs-lookup"><span data-stu-id="d564f-127">A log of events in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d564f-128">Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d564f-128">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Hintergrund Abruf Bereich" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="d564f-130">Anzeigen der Details eines Ereignisses im **Hintergrund Abruf** Bereich</span><span class="sxs-lookup"><span data-stu-id="d564f-130">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d564f-131">Hintergrundsynchronisierung</span><span class="sxs-lookup"><span data-stu-id="d564f-131">Background Sync</span></span>   

<span data-ttu-id="d564f-132">Die **Hintergrund Synchronisierungs-API** ermöglicht es einem Offline **Dienstmitarbeiter** , Daten an einen Server zu senden, nachdem eine zuverlässige Internetverbindung wiederhergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d564f-132">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="d564f-133">So protokollieren Sie Hintergrund Synchronisierungsereignisse für 3 Tage, auch wenn devtools nicht geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="d564f-133">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="d564f-134">[Öffnen Sie devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="d564f-134">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="d564f-135">Öffnen Sie den **Anwendungs** Panel.</span><span class="sxs-lookup"><span data-stu-id="d564f-135">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="d564f-136">Öffnen des Bereichs " **Hintergrundsynchronisierung** "</span><span class="sxs-lookup"><span data-stu-id="d564f-136">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Der Bereich "Hintergrundsynchronisierung"" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="d564f-138">Der Bereich " **Hintergrundsynchronisierung** "</span><span class="sxs-lookup"><span data-stu-id="d564f-138">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d564f-139">Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d564f-139">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="d564f-140">Nach dem Auslösen einiger Hintergrund Synchronisierungsaktivitäten protokolliert devtools die Ereignisse in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d564f-140">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Ereignisprotokoll im Bereich "Hintergrundsynchronisierung"" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="d564f-142">Ereignisprotokoll im Bereich " **Hintergrundsynchronisierung** "</span><span class="sxs-lookup"><span data-stu-id="d564f-142">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d564f-143">Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d564f-143">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich "Hintergrundsynchronisierung"" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="d564f-145">Anzeigen der Details eines Ereignisses im Bereich " **Hintergrundsynchronisierung** "</span><span class="sxs-lookup"><span data-stu-id="d564f-145">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d564f-146">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="d564f-146">Notifications</span></span> 

<span data-ttu-id="d564f-147">Nachdem ein **Dienstmitarbeiter** eine Push- [Nachricht][MDNPush] von einem Server erhalten hat, verwendet der Dienstmitarbeiter die [Benachrichtigungs-API][MDNNotifications] , um die Daten für einen Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d564f-147">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="d564f-148">So protokollieren Sie Benachrichtigungen für 3 Tage, auch wenn devtools nicht geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="d564f-148">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="d564f-149">[Öffnen Sie devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="d564f-149">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="d564f-150">Öffnen Sie den **Anwendungs** Panel.</span><span class="sxs-lookup"><span data-stu-id="d564f-150">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="d564f-151">Öffnen Sie den Bereich **Benachrichtigungen** .</span><span class="sxs-lookup"><span data-stu-id="d564f-151">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Der Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="d564f-153">Der Bereich " **Benachrichtigungen** "</span><span class="sxs-lookup"><span data-stu-id="d564f-153">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d564f-154">Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d564f-154">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="d564f-155">Nach dem Auslösen einiger Benachrichtigungs Aktivitäten protokolliert devtools die Ereignisse in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d564f-155">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Ereignisprotokoll im Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="d564f-157">Ereignisprotokoll im Bereich " **Benachrichtigungen** "</span><span class="sxs-lookup"><span data-stu-id="d564f-157">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d564f-158">Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d564f-158">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="d564f-160">Anzeigen der Details eines Ereignisses im Bereich " **Benachrichtigungen** "</span><span class="sxs-lookup"><span data-stu-id="d564f-160">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d564f-161">Push-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="d564f-161">Push Messages</span></span> 

<span data-ttu-id="d564f-162">Um eine Push-Benachrichtigung für einen Benutzer anzuzeigen, muss ein **Dienstmitarbeiter** zuerst die [Push-Nachrichten-API][MDNPush] verwenden, um Daten von einem Server zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d564f-162">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="d564f-163">Wenn der Dienstmitarbeiter bereit ist, die Benachrichtigung anzuzeigen, wird die Benachrichtigungs [-API][MDNNotifications]verwendet.</span><span class="sxs-lookup"><span data-stu-id="d564f-163">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="d564f-164">So protokollieren Sie Push-Nachrichten für 3 Tage, auch wenn devtools nicht geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="d564f-164">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="d564f-165">[Öffnen Sie devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="d564f-165">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="d564f-166">Öffnen Sie den **Anwendungs** Panel.</span><span class="sxs-lookup"><span data-stu-id="d564f-166">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="d564f-167">Öffnen Sie den Bereich **Push-Messaging** .</span><span class="sxs-lookup"><span data-stu-id="d564f-167">Open the **Push Messaging** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Der Bereich "Push-Messaging"" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="d564f-169">Der Bereich " **Push-Messaging** "</span><span class="sxs-lookup"><span data-stu-id="d564f-169">The **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d564f-170">Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d564f-170">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="d564f-171">Nach dem Auslösen einiger Push-Nachrichten Aktivitäten protokolliert devtools die Ereignisse in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d564f-171">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Ereignisprotokoll im Bereich "Push-Messaging"" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="d564f-173">Ereignisprotokoll im Bereich " **Push-Messaging** "</span><span class="sxs-lookup"><span data-stu-id="d564f-173">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d564f-174">Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d564f-174">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich "Push-Messaging"" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="d564f-176">Anzeigen der Details eines Ereignisses im Bereich " **Push-Messaging** "</span><span class="sxs-lookup"><span data-stu-id="d564f-176">View the details of an event in the **Push Messaging** pane</span></span>  
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
> <span data-ttu-id="d564f-181">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d564f-181">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d564f-182">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d564f-182">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="d564f-184">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d564f-184">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

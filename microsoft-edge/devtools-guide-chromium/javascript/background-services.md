---
description: Debuggen von Hintergrund-FETCH-, Hintergrund-Sync-, Benachrichtigungs-und Push-Nachrichten mit Microsoft Edge-devtools
title: Debuggen von Hintergrunddiensten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 1724bd3a5e45734555650c3d46e377161a3a7c65
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992869"
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





# <span data-ttu-id="619bd-104">Debuggen von Hintergrunddiensten mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="619bd-104">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="619bd-105">Der Abschnitt " **Hintergrunddienste** " von Microsoft Edge devtools ist eine Sammlung von Tools für die JavaScript-APIs, mit deren Hilfe Ihre Website Updates senden und empfangen kann, auch wenn ein Benutzer die Website nicht geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="619bd-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="619bd-106">Ein Hintergrunddienst ähnelt einem [Hintergrundprozess] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="619bd-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="619bd-107">Microsoft Edge devtools berücksichtigt jede der folgenden APIs als Hintergrunddienst:</span><span class="sxs-lookup"><span data-stu-id="619bd-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="619bd-108">Hintergrund Abruf</span><span class="sxs-lookup"><span data-stu-id="619bd-108">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="619bd-109">Hintergrundsynchronisierung</span><span class="sxs-lookup"><span data-stu-id="619bd-109">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="619bd-110">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="619bd-110">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="619bd-111">Push-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="619bd-111">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="619bd-112">Microsoft Edge devtools kann Hintergrunddienst Ereignisse für 3 Tage protokollieren, auch wenn devtools nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="619bd-112">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="619bd-113">Auf diese Weise können Sie sicherstellen, dass Ereignisse wie erwartet gesendet und empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="619bd-113">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="619bd-114">Sie können auch die Details zu den einzelnen Ereignissen prüfen.</span><span class="sxs-lookup"><span data-stu-id="619bd-114">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich "Push-Messaging"" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="619bd-116">Anzeigen der Details eines Ereignisses im Bereich " **Push-Messaging** "</span><span class="sxs-lookup"><span data-stu-id="619bd-116">View the details of an event in the **Push Messaging** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="619bd-117">Hintergrund Abruf</span><span class="sxs-lookup"><span data-stu-id="619bd-117">Background Fetch</span></span>   

<span data-ttu-id="619bd-118">Die *Background FETCH-API*\* ermöglicht es einem **Dienstmitarbeiter** , große Ressourcen wie Filme oder Podcasts als Hintergrunddienst zuverlässig herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="619bd-118">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="619bd-119">So protokollieren Sie das Hintergrund-FETCH-Ereignis für 3 Tage, auch wenn devtools nicht geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="619bd-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="619bd-120">[Öffnen Sie devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="619bd-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="619bd-121">Öffnen Sie den **Anwendungs** Panel.</span><span class="sxs-lookup"><span data-stu-id="619bd-121">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="619bd-122">Öffnen des Bereichs " **Hintergrund Abruf** "</span><span class="sxs-lookup"><span data-stu-id="619bd-122">Open the **Background Fetch** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Der Bereich "Fetch-Hintergrund"" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="619bd-124">Der Bereich " **Fetch-Hintergrund** "</span><span class="sxs-lookup"><span data-stu-id="619bd-124">The **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="619bd-125">Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="619bd-125">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="619bd-126">Nach dem Auslösen einiger Hintergrund Abruf Aktivitäten protokolliert devtools die Ereignisse in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="619bd-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Ereignisprotokoll im Bereich "Fetch-Hintergrund"" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="619bd-128">Ereignisprotokoll im Bereich " **Fetch-Hintergrund** "</span><span class="sxs-lookup"><span data-stu-id="619bd-128">A log of events in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="619bd-129">Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="619bd-129">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Hintergrund Abruf Bereich" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="619bd-131">Anzeigen der Details eines Ereignisses im **Hintergrund Abruf** Bereich</span><span class="sxs-lookup"><span data-stu-id="619bd-131">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="619bd-132">Hintergrundsynchronisierung</span><span class="sxs-lookup"><span data-stu-id="619bd-132">Background Sync</span></span>   

<span data-ttu-id="619bd-133">Die **Hintergrund Synchronisierungs-API** ermöglicht es einem Offline **Dienstmitarbeiter** , Daten an einen Server zu senden, nachdem eine zuverlässige Internetverbindung wiederhergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="619bd-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="619bd-134">So protokollieren Sie Hintergrund Synchronisierungsereignisse für 3 Tage, auch wenn devtools nicht geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="619bd-134">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="619bd-135">[Öffnen Sie devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="619bd-135">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="619bd-136">Öffnen Sie den **Anwendungs** Panel.</span><span class="sxs-lookup"><span data-stu-id="619bd-136">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="619bd-137">Öffnen des Bereichs " **Hintergrundsynchronisierung** "</span><span class="sxs-lookup"><span data-stu-id="619bd-137">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Der Bereich "Hintergrundsynchronisierung"" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="619bd-139">Der Bereich " **Hintergrundsynchronisierung** "</span><span class="sxs-lookup"><span data-stu-id="619bd-139">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="619bd-140">Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="619bd-140">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="619bd-141">Nach dem Auslösen einiger Hintergrund Synchronisierungsaktivitäten protokolliert devtools die Ereignisse in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="619bd-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Ereignisprotokoll im Bereich "Hintergrundsynchronisierung"" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="619bd-143">Ereignisprotokoll im Bereich " **Hintergrundsynchronisierung** "</span><span class="sxs-lookup"><span data-stu-id="619bd-143">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="619bd-144">Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="619bd-144">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich "Hintergrundsynchronisierung"" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="619bd-146">Anzeigen der Details eines Ereignisses im Bereich " **Hintergrundsynchronisierung** "</span><span class="sxs-lookup"><span data-stu-id="619bd-146">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="619bd-147">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="619bd-147">Notifications</span></span> 

<span data-ttu-id="619bd-148">Nachdem ein **Dienstmitarbeiter** eine Push- [Nachricht][MDNPush] von einem Server erhalten hat, verwendet der Dienstmitarbeiter die [Benachrichtigungs-API][MDNNotifications] , um die Daten für einen Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="619bd-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="619bd-149">So protokollieren Sie Benachrichtigungen für 3 Tage, auch wenn devtools nicht geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="619bd-149">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="619bd-150">[Öffnen Sie devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="619bd-150">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="619bd-151">Öffnen Sie den **Anwendungs** Panel.</span><span class="sxs-lookup"><span data-stu-id="619bd-151">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="619bd-152">Öffnen Sie den Bereich **Benachrichtigungen** .</span><span class="sxs-lookup"><span data-stu-id="619bd-152">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Der Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="619bd-154">Der Bereich " **Benachrichtigungen** "</span><span class="sxs-lookup"><span data-stu-id="619bd-154">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="619bd-155">Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="619bd-155">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="619bd-156">Nach dem Auslösen einiger Benachrichtigungs Aktivitäten protokolliert devtools die Ereignisse in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="619bd-156">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Ereignisprotokoll im Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="619bd-158">Ereignisprotokoll im Bereich " **Benachrichtigungen** "</span><span class="sxs-lookup"><span data-stu-id="619bd-158">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="619bd-159">Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="619bd-159">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="619bd-161">Anzeigen der Details eines Ereignisses im Bereich " **Benachrichtigungen** "</span><span class="sxs-lookup"><span data-stu-id="619bd-161">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="619bd-162">Push-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="619bd-162">Push Messages</span></span> 

<span data-ttu-id="619bd-163">Um eine Push-Benachrichtigung für einen Benutzer anzuzeigen, muss ein **Dienstmitarbeiter** zuerst die [Push-Nachrichten-API][MDNPush] verwenden, um Daten von einem Server zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="619bd-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="619bd-164">Wenn der Dienstmitarbeiter bereit ist, die Benachrichtigung anzuzeigen, wird die Benachrichtigungs [-API][MDNNotifications]verwendet.</span><span class="sxs-lookup"><span data-stu-id="619bd-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="619bd-165">So protokollieren Sie Push-Nachrichten für 3 Tage, auch wenn devtools nicht geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="619bd-165">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="619bd-166">[Öffnen Sie devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="619bd-166">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="619bd-167">Öffnen Sie den **Anwendungs** Panel.</span><span class="sxs-lookup"><span data-stu-id="619bd-167">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="619bd-168">Öffnen Sie den Bereich **Push-Messaging** .</span><span class="sxs-lookup"><span data-stu-id="619bd-168">Open the **Push Messaging** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Der Bereich "Push-Messaging"" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="619bd-170">Der Bereich " **Push-Messaging** "</span><span class="sxs-lookup"><span data-stu-id="619bd-170">The **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="619bd-171">Klicken Sie auf **Datensatz** \ ( ![ Datensatz ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="619bd-171">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="619bd-172">Nach dem Auslösen einiger Push-Nachrichten Aktivitäten protokolliert devtools die Ereignisse in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="619bd-172">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Ereignisprotokoll im Bereich "Push-Messaging"" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="619bd-174">Ereignisprotokoll im Bereich " **Push-Messaging** "</span><span class="sxs-lookup"><span data-stu-id="619bd-174">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="619bd-175">Klicken Sie auf ein Ereignis, um dessen Details in dem Bereich unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="619bd-175">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich "Push-Messaging"" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="619bd-177">Anzeigen der Details eines Ereignisses im Bereich " **Push-Messaging** "</span><span class="sxs-lookup"><span data-stu-id="619bd-177">View the details of an event in the **Push Messaging** pane</span></span>  
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
> <span data-ttu-id="619bd-182">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="619bd-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="619bd-183">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="619bd-183">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="619bd-185">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="619bd-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

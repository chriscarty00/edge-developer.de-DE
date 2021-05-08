---
description: Debuggen von Hintergrund-Abruf, Hintergrundsynchronisierung, Benachrichtigungen und Pushnachrichten mit Microsoft Edge DevTools.
title: Debuggen von Hintergrunddiensten mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 15023098c547d31bf46bd387f849b365c13b38f6
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439528"
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

# <a name="debug-background-services-with-microsoft-edge-devtools"></a><span data-ttu-id="d7bf9-104">Debuggen von Hintergrunddiensten mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d7bf9-104">Debug Background Services with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="d7bf9-105">Der **Abschnitt Hintergrunddienste** von Microsoft Edge DevTools ist eine Sammlung von Tools für die JavaScript-APIs, mit denen Ihre Website Updates senden und empfangen kann, auch wenn die Website für einen Benutzer nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="d7bf9-106">Ein Hintergrunddienst ähnelt einem [Hintergrundprozess][WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="d7bf9-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="d7bf9-107">Microsoft Edge DevTools betrachtet jede der folgenden APIs als Hintergrunddienst:</span><span class="sxs-lookup"><span data-stu-id="d7bf9-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="d7bf9-108">Hintergrund-Abruf</span><span class="sxs-lookup"><span data-stu-id="d7bf9-108">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="d7bf9-109">Hintergrundsynchronisierung</span><span class="sxs-lookup"><span data-stu-id="d7bf9-109">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="d7bf9-110">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="d7bf9-110">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="d7bf9-111">Pushnachrichten</span><span class="sxs-lookup"><span data-stu-id="d7bf9-111">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="d7bf9-112">Microsoft Edge DevTools protokolliert möglicherweise Hintergrunddienstereignisse für 3 Tage, auch wenn DevTools nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-112">Microsoft Edge DevTools may log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="d7bf9-113">Das Protokoll für Hintergrunddienstereignisse kann Ihnen dabei helfen, sicherzustellen, dass Ereignisse wie erwartet gesendet und empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-113">The background service events log may help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="d7bf9-114">Sie können auch die Details der einzelnen Ereignisse überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-114">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Der Bereich Push Messaging" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="d7bf9-116">Der **Bereich Push Messaging**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-116">The **Push Messaging** pane</span></span>  
:::image-end:::  

## <a name="background-fetch"></a><span data-ttu-id="d7bf9-117">Hintergrund-Abruf</span><span class="sxs-lookup"><span data-stu-id="d7bf9-117">Background Fetch</span></span>  

<span data-ttu-id="d7bf9-118">Die **Background Fetch-API** ermöglicht es einem **Servicemitarbeiter,** große Ressourcen wie Filme oder Podcasts zuverlässig als Hintergrunddienst herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-118">The **Background Fetch API** enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="d7bf9-119">So protokollieren Sie das Background Fetch-Ereignis für 3 Tage, auch wenn DevTools nicht geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="d7bf9-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="d7bf9-120">[Öffnen Sie DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="d7bf9-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="d7bf9-121">Öffnen Sie das **Anwendungstool.**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-121">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="d7bf9-122">Öffnen Sie **den Bereich Hintergrund-Abruf.**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-122">Open the **Background Fetch** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Der Hintergrund-Abrufbereich" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="d7bf9-124">Der **Hintergrund-Abrufbereich**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-124">The **Background Fetch** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7bf9-125">Wählen **Sie Record** \( Record ![ ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="d7bf9-125">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
   <span data-ttu-id="d7bf9-126">Nach dem Auslösen einiger Background Fetch-Aktivität protokolliert DevTools die Ereignisse in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Ein Protokoll mit Ereignissen im Hintergrund-Abrufbereich" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="d7bf9-128">Ein Protokoll mit Ereignissen im **Hintergrund-Abrufbereich**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-128">A log of events in the **Background Fetch** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7bf9-129">Wählen Sie ein Ereignis aus, um seine Details im Bereich unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-129">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich Hintergrund-Abruf" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="d7bf9-131">Anzeigen der Details eines Ereignisses im **Bereich Hintergrund-Abruf**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-131">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <a name="background-sync"></a><span data-ttu-id="d7bf9-132">Hintergrundsynchronisierung</span><span class="sxs-lookup"><span data-stu-id="d7bf9-132">Background Sync</span></span>  

<span data-ttu-id="d7bf9-133">Die **Hintergrundsynchronisierungs-API** ermöglicht es einem **Offlinedienstmitarbeiter,** Daten an einen Server zu senden, sobald eine zuverlässige Internetverbindung wie hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="d7bf9-134">So protokollieren Sie Hintergrundsynchronisierungsereignisse für 3 Tage, auch wenn DevTools nicht geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="d7bf9-134">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="d7bf9-135">[Öffnen Sie DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="d7bf9-135">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="d7bf9-136">Öffnen Sie das **Anwendungstool.**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-136">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="d7bf9-137">Öffnen Sie **den Bereich Hintergrundsynchronisierung.**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-137">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Der Bereich Hintergrundsynchronisierung" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="d7bf9-139">Der **Bereich Hintergrundsynchronisierung**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-139">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7bf9-140">Wählen **Sie Record** \( Record ![ ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="d7bf9-140">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
   <span data-ttu-id="d7bf9-141">Nachdem einige Hintergrundsynchronisierungsaktivitäten ausgelöst wurden, protokolliert DevTools die Ereignisse in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Ein Ereignisprotokoll im Bereich Hintergrundsynchronisierung" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="d7bf9-143">Ein Ereignisprotokoll im **Bereich Hintergrundsynchronisierung**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-143">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7bf9-144">Wählen Sie ein Ereignis aus, um seine Details im Bereich unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-144">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich Hintergrundsynchronisierung" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="d7bf9-146">Anzeigen der Details eines Ereignisses im **Bereich Hintergrundsynchronisierung**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-146">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <a name="notifications"></a><span data-ttu-id="d7bf9-147">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="d7bf9-147">Notifications</span></span>  

<span data-ttu-id="d7bf9-148">Nachdem ein **Dienstmitarbeiter** eine [Pushnachricht][MDNPush] von einem Server empfangen hat, verwendet der Dienstmitarbeiter die [Notifications-API,][MDNNotifications] um die Daten einem Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="d7bf9-149">So protokollieren Sie Benachrichtigungen für 3 Tage, auch wenn DevTools nicht geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="d7bf9-149">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="d7bf9-150">[Öffnen Sie DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="d7bf9-150">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="d7bf9-151">Öffnen Sie das **Anwendungstool.**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-151">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="d7bf9-152">Öffnen Sie den **Bereich Benachrichtigungen.**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-152">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Der Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="d7bf9-154">Der **Bereich "Benachrichtigungen"**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-154">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7bf9-155">Wählen **Sie Record** \( Record ![ ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="d7bf9-155">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
   <span data-ttu-id="d7bf9-156">Nachdem einige Benachrichtigungsaktivitäten ausgelöst wurden, protokolliert DevTools die Ereignisse in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-156">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Ein Ereignisprotokoll im Bereich "Benachrichtigungen"" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="d7bf9-158">Ein Ereignisprotokoll im Bereich **"Benachrichtigungen"**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-158">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7bf9-159">Wählen Sie ein Ereignis aus, um seine Details im Bereich unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-159">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Bereich Benachrichtigungen" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="d7bf9-161">Anzeigen der Details eines Ereignisses im Bereich **Benachrichtigungen**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-161">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <a name="push-messages"></a><span data-ttu-id="d7bf9-162">Pushnachrichten</span><span class="sxs-lookup"><span data-stu-id="d7bf9-162">Push Messages</span></span>  

<span data-ttu-id="d7bf9-163">Um einem Benutzer eine Pushbenachrichtigung \*\*\*\* anzeigen zu können, muss ein Dienstmitarbeiter zunächst die [Pushnachrichten-API][MDNPush] verwenden, um Daten von einem Server zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="d7bf9-164">Wenn der Dienstmitarbeiter bereit ist, die Benachrichtigung anzuzeigen, verwendet er die [Benachrichtigungs-API][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="d7bf9-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="d7bf9-165">So protokollieren Sie Pushnachrichten für 3 Tage, auch wenn DevTools nicht geöffnet ist:</span><span class="sxs-lookup"><span data-stu-id="d7bf9-165">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="d7bf9-166">[Öffnen Sie DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="d7bf9-166">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="d7bf9-167">Öffnen Sie das **Anwendungstool.**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-167">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="d7bf9-168">Öffnen Sie den **Pushnachrichtenbereich.**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-168">Open the **Push Messaging** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Öffnen des Pushnachrichtenbereichs" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="d7bf9-170">Öffnen des **Pushnachrichtenbereichs**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-170">Open the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7bf9-171">Wählen **Sie Record** \( Record ![ ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="d7bf9-171">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
    <span data-ttu-id="d7bf9-172">Nachdem einige Pushnachrichtenaktivitäten ausgelöst wurden, protokolliert DevTools die Ereignisse in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-172">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Ein Ereignisprotokoll im Pushnachrichtenbereich" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="d7bf9-174">Ein Ereignisprotokoll im **Pushnachrichtenbereich**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-174">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d7bf9-175">Wählen Sie ein Ereignis aus, um die Details im Bereich unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-175">Choose an event to view the details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Anzeigen der Details eines Ereignisses im Pushnachrichtenbereich" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="d7bf9-177">Anzeigen der Details eines Ereignisses im **Pushnachrichtenbereich**</span><span class="sxs-lookup"><span data-stu-id="d7bf9-177">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="d7bf9-178">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="d7bf9-178">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open/index.md "Öffnen Sie Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Benachrichtigungs-API-| MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API-| MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "Hintergrundprozess – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="d7bf9-183">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-183">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d7bf9-184">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-184">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="d7bf9-186">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d7bf9-186">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

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
# <span data-ttu-id="a95ad-104">Verbesserungen der Dienstmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="a95ad-104">Service Worker improvements</span></span>  

<span data-ttu-id="a95ad-105">In diesem Artikel werden die Verbesserungen an [Servicemitarbeitern][MdnServiceWorkerApi] und die Netzwerkanforderungen erläutert, die jeweils durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="a95ad-105">This article teaches you about improvements to [service workers][MdnServiceWorkerApi] and the network requests that pass through each one.</span></span>  <span data-ttu-id="a95ad-106">Die **Verbesserungen der Dienstmitarbeiter** befinden sich in den Tools **Netzwerk**, **Anwendung**und **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="a95ad-106">The **service worker improvements** are in the **Network**, **Application**, and **Sources** tools.</span></span>  <span data-ttu-id="a95ad-107">Die Verbesserungen umfassen die folgenden Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="a95ad-107">The improvements include the following tasks.</span></span>  

*   <span data-ttu-id="a95ad-108">Debuggen basierend auf den Zeitrahmen für Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="a95ad-108">Debug based on Service Worker timelines.</span></span>  
    *   <span data-ttu-id="a95ad-109">Der Anfang einer Anforderung und die Dauer des Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="a95ad-109">The start of a request and duration of the bootstrap.</span></span>  
    *   <span data-ttu-id="a95ad-110">Aktualisieren Sie die Service Worker-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="a95ad-110">Update to Service worker registration.</span></span>  
    *   <span data-ttu-id="a95ad-111">Die Laufzeit einer Anforderung mit dem [Fetch-Ereignis][MdnFetchEvent] Handler.</span><span class="sxs-lookup"><span data-stu-id="a95ad-111">The runtime of a request using the [fetch event][MdnFetchEvent] handler.</span></span>  
    *   <span data-ttu-id="a95ad-112">Die Laufzeit aller FETCH-Ereignisse zum Laden eines Clients.</span><span class="sxs-lookup"><span data-stu-id="a95ad-112">The runtime of all fetch events for loading a client.</span></span>  
*   <span data-ttu-id="a95ad-113">Erkunden Sie die Laufzeitdetails von FETCH-Ereignishandlern, installieren Sie Ereignishandler, und aktivieren Sie Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="a95ad-113">Explore the runtime details of fetch event handlers, install event handlers, and activate event handlers.</span></span>  
*   <span data-ttu-id="a95ad-114">Ein-und Auschecken des FETCH-Ereignishandlers mit [Seitenskript Informationen](#sources)</span><span class="sxs-lookup"><span data-stu-id="a95ad-114">Step into and out of fetch event handler with [page script information](#sources).</span></span>  

<span data-ttu-id="a95ad-115">Die Erfahrungen umfassen drei verschiedene Entwicklertools.</span><span class="sxs-lookup"><span data-stu-id="a95ad-115">The experiences span three different developer tools.</span></span>  

1.  <span data-ttu-id="a95ad-116">Das [Netzwerk](#network) Tool.</span><span class="sxs-lookup"><span data-stu-id="a95ad-116">The [Network](#network) tool.</span></span>  <span data-ttu-id="a95ad-117">Wählen Sie eine Netzwerkanforderung aus, die über einen Dienstmitarbeiter ausgeführt wird, und greifen Sie im Tool **Zeitmessung** auf die entsprechende Zeitachse des Dienst Mitarbeiters zu.</span><span class="sxs-lookup"><span data-stu-id="a95ad-117">Choose a network request that runs through a service worker and access the corresponding timeline of the service worker in the **Timing** tool.</span></span>  
1.  <span data-ttu-id="a95ad-118">Das [Anwendungs](#application) Tool.</span><span class="sxs-lookup"><span data-stu-id="a95ad-118">The [Application](#application) tool.</span></span>  <span data-ttu-id="a95ad-119">Navigieren Sie zum Debuggen der Dienstmitarbeiter zum Tool **Dienstmitarbeiter** .</span><span class="sxs-lookup"><span data-stu-id="a95ad-119">To debug the service workers, navigate to the **Service Workers** tool.</span></span>  
1.  <span data-ttu-id="a95ad-120">Das Tool " [Quellen](#sources) ".</span><span class="sxs-lookup"><span data-stu-id="a95ad-120">The [Sources](#sources) tool.</span></span>  <span data-ttu-id="a95ad-121">Zugriffsseiten-Skript Informationen, wenn Sie zu Fetch-Ereignishandlern springen.</span><span class="sxs-lookup"><span data-stu-id="a95ad-121">Access page script information when stepping into fetch event handlers.</span></span>  

## <span data-ttu-id="a95ad-122">Network</span><span class="sxs-lookup"><span data-stu-id="a95ad-122">Network</span></span>  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Service Worker-Zeitachse im Netzwerktool" lightbox="../media/sw-network-timeline.msft.png":::
   <span data-ttu-id="a95ad-124">Netzwerkansicht</span><span class="sxs-lookup"><span data-stu-id="a95ad-124">Network view</span></span>  
:::image-end:::  

<span data-ttu-id="a95ad-125">Führen Sie eine der folgenden Aktionen aus, um auf die Features des Dienstmitarbeiter Debuggens im Tool **Netzwerk** zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a95ad-125">To access the service worker debugging features in the **Network** tool, complete one of the following actions.</span></span>  

*   <span data-ttu-id="a95ad-126">Direkter Zugriff auf das **Netzwerk** Tool.</span><span class="sxs-lookup"><span data-stu-id="a95ad-126">Access directly in the **Network** tool.</span></span>  
*   <span data-ttu-id="a95ad-127">Im **Anwendungs** Tool gestartet.</span><span class="sxs-lookup"><span data-stu-id="a95ad-127">Started in the **Application** tool.</span></span>  
    
### <span data-ttu-id="a95ad-128">Routing anfordern</span><span class="sxs-lookup"><span data-stu-id="a95ad-128">Request routing</span></span>  

<span data-ttu-id="a95ad-129">Um die Visualisierung von Anforderungs Routing zu vereinfachen, werden in den Zeitplänen nun die Start-und die FETCH-Ereignisse für den Dienstmitarbeiter angezeigt `respondWith` .</span><span class="sxs-lookup"><span data-stu-id="a95ad-129">To make request routing easier to visualize, timelines now display the service worker start-up and the `respondWith` fetch events.</span></span>  <span data-ttu-id="a95ad-130">Führen Sie die folgenden Aktionen aus, um eine Netzwerkanforderung zu Debuggen und zu visualisieren, die von einem Dienstmitarbeiter durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a95ad-130">To debug and visualize a network request that passed through a service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="a95ad-131">Wählen Sie die Netzwerkanforderung aus, die von einem Dienstmitarbeiter durchlaufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a95ad-131">Choose the network request that went through a service worker.</span></span>  
1.  <span data-ttu-id="a95ad-132">Öffnen Sie das Tool **Anzeige** Dauer.</span><span class="sxs-lookup"><span data-stu-id="a95ad-132">Open the **Timing** tool.</span></span>  
    
### <span data-ttu-id="a95ad-133">Abrufen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="a95ad-133">Fetch events</span></span>  

<span data-ttu-id="a95ad-134">Wenn Sie mehr über die `respondWith` Fetch-Ereignisse erfahren möchten, wählen Sie den Dropdownpfeil links neben dem aus `respondWith` .</span><span class="sxs-lookup"><span data-stu-id="a95ad-134">To learn more about the `respondWith` fetch events, choose the dropdown arrow to the left of the `respondWith`.</span></span>  <span data-ttu-id="a95ad-135">Wenn Sie weitere Details zur **ursprünglichen Anforderung** und **Antwort erhalten**möchten, verwenden Sie die entsprechenden Dropdownpfeile.</span><span class="sxs-lookup"><span data-stu-id="a95ad-135">To find more details about the **Original Request** and **Response Received**, use the corresponding dropdown arrows.</span></span>  

## <span data-ttu-id="a95ad-136">Application</span><span class="sxs-lookup"><span data-stu-id="a95ad-136">Application</span></span>  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Anwendungsansicht" lightbox="../media/sw-application-timeline.msft.png":::
   <span data-ttu-id="a95ad-138">Anwendungsansicht</span><span class="sxs-lookup"><span data-stu-id="a95ad-138">Application view</span></span>  
:::image-end:::  

### <span data-ttu-id="a95ad-139">Zeitachsen Update für Dienstmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="a95ad-139">Service worker update timeline</span></span>  

<span data-ttu-id="a95ad-140">Das Microsoft Edge devtools-Team hat im **Anwendungs** Tool eine Zeitachse hinzugefügt, um den Update-Lebenszyklus des Dienst Mitarbeiters wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="a95ad-140">The Microsoft Edge DevTools team added a timeline in the **Application** tool to reflect the update lifecycle of the service worker.</span></span>  <span data-ttu-id="a95ad-141">Sie zeigt die Installations-und Aktivierungsereignisse an.</span><span class="sxs-lookup"><span data-stu-id="a95ad-141">It displays the installation and activation events.</span></span>  <span data-ttu-id="a95ad-142">Jedes der Ereignisse verfügt über einen entsprechenden Dropdownpfeil, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a95ad-142">Each of the events has a corresponding dropdown arrow to give you more details.</span></span>  

### <span data-ttu-id="a95ad-143">Anfordern von Routing-und FETCH-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="a95ad-143">Request routing and fetch events</span></span>  

<span data-ttu-id="a95ad-144">Sie können nun über das Tool **Netzwerk** im Konsolen Einzug auf die Zeitpläne für Dienstmitarbeiter zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a95ad-144">You may now access the service worker timelines through the **Network** tool in the console drawer.</span></span>  <span data-ttu-id="a95ad-145">Das Feature profitiert von der Leistung, minimiert die Duplizierung von Benutzeroberflächen und erstellt ein umfassenderes Debugging.</span><span class="sxs-lookup"><span data-stu-id="a95ad-145">The feature benefits performance, minimizes UI duplication, and creates a more comprehensive debugging experience.</span></span>  

1.  <span data-ttu-id="a95ad-146">Öffnen Sie den zu debuggenden Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="a95ad-146">Open the service worker you are debugging.</span></span>  
1.  <span data-ttu-id="a95ad-147">Wählen Sie die Schaltfläche **Netzwerk** aus, um die [Anforderungs Routing-Umgebung](#network)zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a95ad-147">Choose the **Network** button to open up the [request routing experience](#network).</span></span>  
1.  <span data-ttu-id="a95ad-148">Verwenden Sie die **respondWith** -Dropdownlisten für Fetch Event Request-und Response-Informationen.</span><span class="sxs-lookup"><span data-stu-id="a95ad-148">Use the **respondWith** dropdowns for fetch event request and response information.</span></span>  

<span data-ttu-id="a95ad-149">Das Tool **Netzwerk** zeigt die Netzwerkanforderungen an, die durch den Dienstmitarbeiter durchlaufen wurden, den Sie Debuggen.</span><span class="sxs-lookup"><span data-stu-id="a95ad-149">The **Network** tool displays the network requests that went through the service worker you are debugging.</span></span>  <span data-ttu-id="a95ad-150">Der automatische Filter ist eine Möglichkeit, ihre Exploration zu verkleinern.</span><span class="sxs-lookup"><span data-stu-id="a95ad-150">The automatic filter is a way to narrow down your exploration.</span></span>

## <span data-ttu-id="a95ad-151">Quellen</span><span class="sxs-lookup"><span data-stu-id="a95ad-151">Sources</span></span>  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="DOM-Ansicht" lightbox="../media/sw-sources.msft.png":::
   <span data-ttu-id="a95ad-153">DOM-Ansicht</span><span class="sxs-lookup"><span data-stu-id="a95ad-153">DOM view</span></span>  
:::image-end:::  

<span data-ttu-id="a95ad-154">Wenn Sie weitere Stapel Informationen finden möchten, legen Sie im FETCH-Handler einen Unterbrechungspunkt fest.</span><span class="sxs-lookup"><span data-stu-id="a95ad-154">To find more stack information, set a break point in the fetch handler.</span></span>  <span data-ttu-id="a95ad-155">Die Details führen zu dem Ort, an dem die Ressource im Seitenskript angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="a95ad-155">The details lead to where the resource is requested in the page script.</span></span>  <span data-ttu-id="a95ad-156">Wenn der Debugger in einem Fetch-Handler angehalten wird, wird im Bereich auf der rechten Seite eine kombinierte Stapel Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a95ad-156">When the debugger pauses inside a fetch handler, a combined stack information is displayed in the panel to the right.</span></span>  <span data-ttu-id="a95ad-157">Anschließend können Sie in den Stapelrahmen navigieren.</span><span class="sxs-lookup"><span data-stu-id="a95ad-157">After that, you may move around in the stack frames.</span></span>  

### <span data-ttu-id="a95ad-158">Zukünftige Arbeit</span><span class="sxs-lookup"><span data-stu-id="a95ad-158">Future work</span></span>  

<span data-ttu-id="a95ad-159">Das Microsoft Edge devtools-Team plant, die Cache Details weiter zu entwickeln und untersucht mehr Möglichkeiten zur Verbesserung der Service Worker-Debugging-Erfahrung für Entwickler von [progressiven Webanwendungen][MdnProgressiveWebApps] .</span><span class="sxs-lookup"><span data-stu-id="a95ad-159">The Microsoft Edge DevTools team plans to further develop the cache detail and are investigating more ways to improve the service worker debugging experience for [Progressive Web Application][MdnProgressiveWebApps] developers.</span></span>  

## <span data-ttu-id="a95ad-160">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="a95ad-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Progressive Web-Apps (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker-API | MDN"  

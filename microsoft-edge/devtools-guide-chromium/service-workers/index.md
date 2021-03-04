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
# <a name="service-worker-improvements"></a><span data-ttu-id="0e356-104">Verbesserungen bei Service Worker</span><span class="sxs-lookup"><span data-stu-id="0e356-104">Service Worker improvements</span></span>  

<span data-ttu-id="0e356-105">Dieser Artikel enthält Informationen zu Verbesserungen an [][MdnServiceWorkerApi] Entwicklertools für die Arbeit mit Servicemitarbeitern und den Netzwerkanforderungen, die jeweils übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e356-105">This article teaches you about improvements to developer tools for working with [service workers][MdnServiceWorkerApi] and the network requests that pass through each one.</span></span>  <span data-ttu-id="0e356-106">Die **Verbesserungen bei den Dienstmitarbeitern** finden Sie in den Tools **Netzwerk,** **Anwendung** **und** Quellen.</span><span class="sxs-lookup"><span data-stu-id="0e356-106">The **service worker improvements** are in the **Network**, **Application**, and **Sources** tools.</span></span>  <span data-ttu-id="0e356-107">Die Verbesserungen vereinfachen die folgenden Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="0e356-107">The improvements simplify the following tasks.</span></span>  

*   <span data-ttu-id="0e356-108">Debuggen basierend auf Service Worker-Zeitachsen.</span><span class="sxs-lookup"><span data-stu-id="0e356-108">Debug based on Service Worker timelines.</span></span>  
    *   <span data-ttu-id="0e356-109">Der Anfang einer Anforderung und die Dauer des Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="0e356-109">The start of a request and duration of the bootstrap.</span></span>  
    *   <span data-ttu-id="0e356-110">Aktualisieren auf Dienstmitarbeiterregistrierung.</span><span class="sxs-lookup"><span data-stu-id="0e356-110">Update to Service worker registration.</span></span>  
    *   <span data-ttu-id="0e356-111">Die Laufzeit einer Anforderung mithilfe des [Fetch-Ereignishandlers.][MdnFetchEvent]</span><span class="sxs-lookup"><span data-stu-id="0e356-111">The runtime of a request using the [fetch event][MdnFetchEvent] handler.</span></span>  
    *   <span data-ttu-id="0e356-112">Die Laufzeit aller Abrufereignisse zum Laden eines Clients.</span><span class="sxs-lookup"><span data-stu-id="0e356-112">The runtime of all fetch events for loading a client.</span></span>  
*   <span data-ttu-id="0e356-113">Erkunden Sie die Laufzeitdetails von Fetch-Ereignishandlern, Installieren von Ereignishandlern und Aktivieren von Ereignishandlern.</span><span class="sxs-lookup"><span data-stu-id="0e356-113">Explore the runtime details of fetch event handlers, install event handlers, and activate event handlers.</span></span>  
*   <span data-ttu-id="0e356-114">Schritt in und aus fetch-Ereignishandler mit [Seitenskriptinformationen](#sources).</span><span class="sxs-lookup"><span data-stu-id="0e356-114">Step into and out of fetch event handler with [page script information](#sources).</span></span>  
    
<span data-ttu-id="0e356-115">Die Erfahrungen umfassen drei verschiedene Entwicklertools.</span><span class="sxs-lookup"><span data-stu-id="0e356-115">The experiences span three different developer tools.</span></span>  

1.  <span data-ttu-id="0e356-116">Das [Netzwerktool.](#network)</span><span class="sxs-lookup"><span data-stu-id="0e356-116">The [Network](#network) tool.</span></span>  <span data-ttu-id="0e356-117">Wählen Sie eine Netzwerkanforderung aus, die über einen Servicemitarbeiter ausgeführt wird, und greifen Sie im Timing-Tool auf die entsprechende Zeitachse des **Servicemitarbeiters** zu.</span><span class="sxs-lookup"><span data-stu-id="0e356-117">Choose a network request that runs through a service worker and access the corresponding timeline of the service worker in the **Timing** tool.</span></span>  
1.  <span data-ttu-id="0e356-118">Das [Application-Tool.](#application)</span><span class="sxs-lookup"><span data-stu-id="0e356-118">The [Application](#application) tool.</span></span>  <span data-ttu-id="0e356-119">Navigieren Sie zum Tool Service Workers, um die **Servicemitarbeiter zu** debuggen.</span><span class="sxs-lookup"><span data-stu-id="0e356-119">To debug the service workers, navigate to the **Service Workers** tool.</span></span>  
1.  <span data-ttu-id="0e356-120">Das [Tool Sources.](#sources)</span><span class="sxs-lookup"><span data-stu-id="0e356-120">The [Sources](#sources) tool.</span></span>  <span data-ttu-id="0e356-121">Greifen Sie auf Seitenskriptinformationen zu, wenn Sie in fetch-Ereignishandler treten.</span><span class="sxs-lookup"><span data-stu-id="0e356-121">Access page script information when stepping into fetch event handlers.</span></span>  
    
## <a name="network"></a><span data-ttu-id="0e356-122">Network</span><span class="sxs-lookup"><span data-stu-id="0e356-122">Network</span></span>  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Dienstarbeitszeitachse im Netzwerktool" lightbox="../media/sw-network-timeline.msft.png":::
   <span data-ttu-id="0e356-124">Netzwerkansicht</span><span class="sxs-lookup"><span data-stu-id="0e356-124">Network view</span></span>  
:::image-end:::  

<span data-ttu-id="0e356-125">Führen Sie eine der folgenden Aktionen aus, um auf die Debugfeatures des Dienstmitarbeiters im **Netzwerktool** zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0e356-125">To access the service worker debugging features in the **Network** tool, complete one of the following actions.</span></span>  

*   <span data-ttu-id="0e356-126">Zugriff direkt im **Netzwerktool.**</span><span class="sxs-lookup"><span data-stu-id="0e356-126">Access directly in the **Network** tool.</span></span>  
*   <span data-ttu-id="0e356-127">Gestartet im **Anwendungstool.**</span><span class="sxs-lookup"><span data-stu-id="0e356-127">Started in the **Application** tool.</span></span>  
    
### <a name="request-routing"></a><span data-ttu-id="0e356-128">Anforderungsrouting</span><span class="sxs-lookup"><span data-stu-id="0e356-128">Request routing</span></span>  

<span data-ttu-id="0e356-129">Um das Anforderungsrouting zu vereinfachen, werden auf Zeitachsen jetzt das Start-up des Dienstmitarbeiters und die `respondWith` Abrufereignisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e356-129">To make request routing easier to visualize, timelines now display the service worker start-up and the `respondWith` fetch events.</span></span>  <span data-ttu-id="0e356-130">Führen Sie die folgenden Aktionen aus, um eine Netzwerkanforderung zu debuggen und zu visualisieren, die über einen Dienstmitarbeiter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0e356-130">To debug and visualize a network request that passed through a service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="0e356-131">Wählen Sie die Netzwerkanforderung aus, die über einen Servicemitarbeiter gegangen ist.</span><span class="sxs-lookup"><span data-stu-id="0e356-131">Choose the network request that went through a service worker.</span></span>  
1.  <span data-ttu-id="0e356-132">Öffnen Sie das **Timing-Tool.**</span><span class="sxs-lookup"><span data-stu-id="0e356-132">Open the **Timing** tool.</span></span>  
    
### <a name="fetch-events"></a><span data-ttu-id="0e356-133">Abrufen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="0e356-133">Fetch events</span></span>  

<span data-ttu-id="0e356-134">Um mehr über die Abrufereignisse zu erfahren, wählen Sie den Dropdownpfeil links `respondWith` neben der `respondWith` aus.</span><span class="sxs-lookup"><span data-stu-id="0e356-134">To learn more about the `respondWith` fetch events, choose the dropdown arrow to the left of the `respondWith`.</span></span>  <span data-ttu-id="0e356-135">Verwenden Sie die entsprechenden Dropdownpfeile, um weitere Details zu **der ursprünglichen** Anforderung und der empfangenen Antwort zu finden. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0e356-135">To find more details about the **Original Request** and **Response Received**, use the corresponding dropdown arrows.</span></span>  

## <a name="application"></a><span data-ttu-id="0e356-136">Application</span><span class="sxs-lookup"><span data-stu-id="0e356-136">Application</span></span>  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Anwendungsansicht" lightbox="../media/sw-application-timeline.msft.png":::
   <span data-ttu-id="0e356-138">Anwendungsansicht</span><span class="sxs-lookup"><span data-stu-id="0e356-138">Application view</span></span>  
:::image-end:::  

### <a name="service-worker-update-timeline"></a><span data-ttu-id="0e356-139">Zeitachse der Dienstarbeitsmitarbeiteraktualisierung</span><span class="sxs-lookup"><span data-stu-id="0e356-139">Service worker update timeline</span></span>  

<span data-ttu-id="0e356-140">Das Microsoft Edge DevTools-Team hat eine Zeitachse im **Anwendungstool** hinzugefügt, um den Updatelebenszyklus des Servicemitarbeiters widerspiegeln zu können.</span><span class="sxs-lookup"><span data-stu-id="0e356-140">The Microsoft Edge DevTools team added a timeline in the **Application** tool to reflect the update lifecycle of the service worker.</span></span>  <span data-ttu-id="0e356-141">Es werden die Installations- und Aktivierungsereignisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e356-141">It displays the installation and activation events.</span></span>  <span data-ttu-id="0e356-142">Jedes der Ereignisse verfügt über einen entsprechenden Dropdownpfeil, um Weitere Details zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0e356-142">Each of the events has a corresponding dropdown arrow to give you more details.</span></span>  

### <a name="request-routing-and-fetch-events"></a><span data-ttu-id="0e356-143">Routing- und Abrufereignisse anfordern</span><span class="sxs-lookup"><span data-stu-id="0e356-143">Request routing and fetch events</span></span>  

<span data-ttu-id="0e356-144">Sie können nun über das Netzwerktool in der Konsolenschubleiste auf die Zeitachsen des Dienstarbeitsmitarbeiters zugreifen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0e356-144">You may now access the service worker timelines through the **Network** tool in the console drawer.</span></span>  <span data-ttu-id="0e356-145">Das Feature bietet Vorteile für die Leistung, minimiert die Benutzeroberflächenduplizierung und bietet eine umfassendere Debugoberfläche.</span><span class="sxs-lookup"><span data-stu-id="0e356-145">The feature benefits performance, minimizes UI duplication, and creates a more comprehensive debugging experience.</span></span>  

1.  <span data-ttu-id="0e356-146">Öffnen Sie den Servicemitarbeiter, den Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="0e356-146">Open the service worker you are debugging.</span></span>  
1.  <span data-ttu-id="0e356-147">Wählen Sie die **Schaltfläche Netzwerk** aus, um die [Anforderungsroutingerfahrung zu öffnen.](#network)</span><span class="sxs-lookup"><span data-stu-id="0e356-147">Choose the **Network** button to open up the [request routing experience](#network).</span></span>  
1.  <span data-ttu-id="0e356-148">Verwenden Sie **die respondWith-Dropdowns** zum Abrufen von Ereignisanforderungs- und Antwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="0e356-148">Use the **respondWith** dropdowns for fetch event request and response information.</span></span>  

<span data-ttu-id="0e356-149">Das **Netzwerktool** zeigt die Netzwerkanforderungen an, die durch den Servicemitarbeiter gegangen sind, den Sie debuggen.</span><span class="sxs-lookup"><span data-stu-id="0e356-149">The **Network** tool displays the network requests that went through the service worker you are debugging.</span></span>  <span data-ttu-id="0e356-150">Der automatische Filter ist eine Möglichkeit, die Untersuchung zu einent einengt.</span><span class="sxs-lookup"><span data-stu-id="0e356-150">The automatic filter is a way to narrow down your exploration.</span></span>

## <a name="sources"></a><span data-ttu-id="0e356-151">Quellen</span><span class="sxs-lookup"><span data-stu-id="0e356-151">Sources</span></span>  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="DOM-Ansicht" lightbox="../media/sw-sources.msft.png":::
   <span data-ttu-id="0e356-153">DOM-Ansicht</span><span class="sxs-lookup"><span data-stu-id="0e356-153">DOM view</span></span>  
:::image-end:::  

<span data-ttu-id="0e356-154">Um weitere Stapelinformationen zu finden, legen Sie im Abrufhandler einen Haltepunkt ein.</span><span class="sxs-lookup"><span data-stu-id="0e356-154">To find more stack information, set a break point in the fetch handler.</span></span>  <span data-ttu-id="0e356-155">Die Details führen dazu, wo die Ressource im Seitenskript angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="0e356-155">The details lead to where the resource is requested in the page script.</span></span>  <span data-ttu-id="0e356-156">Wenn der Debugger innerhalb eines Abrufhandlers angehalten wird, werden im Bereich rechts eine kombinierte Stapelinformationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e356-156">When the debugger pauses inside a fetch handler, a combined stack information is displayed in the panel to the right.</span></span>  <span data-ttu-id="0e356-157">Danach können Sie sich in den Stapelframes bewegen.</span><span class="sxs-lookup"><span data-stu-id="0e356-157">After that, you may move around in the stack frames.</span></span>  

### <a name="future-work"></a><span data-ttu-id="0e356-158">Zukünftige Arbeit</span><span class="sxs-lookup"><span data-stu-id="0e356-158">Future work</span></span>  

<span data-ttu-id="0e356-159">Das Microsoft Edge DevTools-Team plant die Weiterentwicklung des Cachedetails und untersucht weitere Möglichkeiten zur Verbesserung der Debugerfahrung von Dienstmitarbeitern für [Entwickler von progressiven][MdnProgressiveWebApps] Webanwendungen.</span><span class="sxs-lookup"><span data-stu-id="0e356-159">The Microsoft Edge DevTools team plans to further develop the cache detail and are investigating more ways to improve the service worker debugging experience for [Progressive Web Application][MdnProgressiveWebApps] developers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0e356-160">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="0e356-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Progressive Web Apps (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Dienstarbeits-API-| MDN"  

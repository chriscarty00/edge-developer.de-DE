---
description: Verwenden des Netzwerk Panels zum Überwachen und Anzeigen von Seitenressourcen Anforderungen
title: DevTools-Netzwerk
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Netzwerk, Ladezeit, http, HTTPS, Browser-Cache, har
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 261226c7210d978f11290816c81355bb0142dee9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234044"
---
# <span data-ttu-id="90f86-104">Network</span><span class="sxs-lookup"><span data-stu-id="90f86-104">Network</span></span>

<span data-ttu-id="90f86-105">Verwenden Sie das **Netzwerk** Panel, um die über den Draht gesendeten Anfragen und Antworten zu überwachen, zu überprüfen und zu profilieren.</span><span class="sxs-lookup"><span data-stu-id="90f86-105">Use the **Network** panel to monitor, inspect and profile the requests and responses sent over the wire.</span></span> <span data-ttu-id="90f86-106">Damit haben Sie folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="90f86-106">With it, you can:</span></span>

 - <span data-ttu-id="90f86-107">Durch [Suchen eines Datensatzes aller Ressourcenanforderungen](#network-summary) , die von der Seite vorgenommen wurden</span><span class="sxs-lookup"><span data-stu-id="90f86-107">[Browse a record of all the resource requests](#network-summary) made by the page</span></span>
 - <span data-ttu-id="90f86-108">[Messen der Ladezeit Ihrer Website](#summary-bar) für neue und wiederkehrende Benutzer</span><span class="sxs-lookup"><span data-stu-id="90f86-108">[Measure the load time of your site](#summary-bar) for new and returning users</span></span> 
 - <span data-ttu-id="90f86-109">Über [Prüfen der Überschriften, Nachrichtentexte, Parameter und Cookies](#request-details) , die zwischen Ihrer Seite und dem Netzwerk ausgetauscht wurden</span><span class="sxs-lookup"><span data-stu-id="90f86-109">[Inspect the headers, message bodies, parameters, and cookies](#request-details) exchanged between your page and the network</span></span>
 - <span data-ttu-id="90f86-110">[Ermitteln der Netzwerkereignisse](#timings) , die zu Engpässen beim Laden der Website führen</span><span class="sxs-lookup"><span data-stu-id="90f86-110">[Identify the network events causing bottlenecks](#timings) in the load time of your site</span></span>

![Das Microsoft Edge devtools-Netzwerk Panel](./media/network.png)

## <span data-ttu-id="90f86-112">Netzwerk Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="90f86-112">Network summary</span></span>

<span data-ttu-id="90f86-113">Wenn Sie devtools öffnen, ist die Netzwerkprofil Erstellung standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="90f86-113">When you open  DevTools, network profiling is turned on by default.</span></span> <span data-ttu-id="90f86-114">Der gesamte Netzwerkdatenverkehr von der Registerkarte "aktiver Browser" wird in der Liste "Netzwerk Zusammenfassung" aufgezeichnet, auch wenn Sie in einem anderen devtools als dem *Netzwerk*arbeiten.</span><span class="sxs-lookup"><span data-stu-id="90f86-114">All the network traffic from your active browser tab is recorded in the network summary list, even while you are working in a different  DevTools panel than *Network*.</span></span>

![In-Progress-Netzwerkprofil Erstellungs Indikator](./media/network_profile_indicator.png)

### <span data-ttu-id="90f86-116">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="90f86-116">Toolbar</span></span>

<span data-ttu-id="90f86-117">Die Symbolleiste bietet Steuerelemente zum profilieren und Filtern der Netzwerkaktivität Ihrer Seite.</span><span class="sxs-lookup"><span data-stu-id="90f86-117">The toolbar provides controls for profiling and filtering the network activity of your page.</span></span> 

![Netzwerk Profiler-Symbolleiste](./media/network_toolbar.png)

1. <span data-ttu-id="90f86-119">**Starten/Beenden der Profilerstellungssitzung**: Standardmäßig ist die Netzwerkprofil Erstellung aktiviert, und der Netzwerkdatenverkehr wird in der Liste " [**Netzwerk Profiler**](#network-request-list) " protokolliert.</span><span class="sxs-lookup"><span data-stu-id="90f86-119">**Start / Stop profiling session**: By default, network profiling is turned on, and network traffic will be logged in the [**Network profiler**](#network-request-list) list.</span></span> <span data-ttu-id="90f86-120">Mit der Schaltfläche **Stopp** () können Sie die Netzwerkaufzeichnung deaktivieren `Ctrl+E` .</span><span class="sxs-lookup"><span data-stu-id="90f86-120">You can turn off network capture with the **Stop** (`Ctrl+E`) button.</span></span>

2. <span data-ttu-id="90f86-121">**Als har exportieren**: Sie können die aktuelle Netzwerkprofil Erstellungs Sitzung ( `Ctrl+S` ) als JSON-formatierte [http-Archivdatei (har)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) speichern.</span><span class="sxs-lookup"><span data-stu-id="90f86-121">**Export as HAR**: You can save the current network profiling session (`Ctrl+S`) as a JSON-formatted [HTTP Archive (HAR)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) file.</span></span> 

3. <span data-ttu-id="90f86-122">**Inhaltstyp Filter**: Filtern Sie die Liste der Netzwerkanforderungen nach bestimmten Inhaltsanforderungen (*Dokumente, Stylesheets, Bilder, Skripts, Medien, Schriftarten, XMLHttpRequest usw*.).</span><span class="sxs-lookup"><span data-stu-id="90f86-122">**Content type filter**: Filter the network request list by specific content requests (*Documents, Style sheets, Images, Scripts, Media, Fonts, XHR, Other*).</span></span> <span data-ttu-id="90f86-123">Standardmäßig werden alle Inhaltstypen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90f86-123">By default all content types are shown.</span></span>

4. <span data-ttu-id="90f86-124">**Suchen**: Filtern ( `Ctrl+F` ) Sie die Netzwerk Anforderungsliste nach Eintragsnamen (Ressourcenpfade), die eine angegebene Suchzeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="90f86-124">**Find**: Filter (`Ctrl+F`) the network request list by entry names (resource paths) containing a specified search string.</span></span>

5. <span data-ttu-id="90f86-125">**Immer vom Server aktualisieren**: Wenn Sie diese Schaltfläche drücken, wird das Laden von Seitenressourcen aus dem Netzwerk und nicht vom Browsercache erzwungen.</span><span class="sxs-lookup"><span data-stu-id="90f86-125">**Always refresh from server**: Depressing this button will force page resources to load from the network rather than the browser cache.</span></span> <span data-ttu-id="90f86-126">Sie können die Seite aus dem Netzwerk ein einziges Mal aktualisieren, indem Sie auf klicken `Ctrl+F5` .</span><span class="sxs-lookup"><span data-stu-id="90f86-126">You can refresh the page from  network a single time by pressing `Ctrl+F5`.</span></span>

6. <span data-ttu-id="90f86-127">**Bypass Service Worker für alle Netzwerkanforderungen**: Deaktivieren Sie Ihre registrierten Servicemitarbeiter als Netzwerk Proxys.</span><span class="sxs-lookup"><span data-stu-id="90f86-127">**Bypass Service Worker for all network requests**: Disable your registered service workers as network proxies.</span></span> 

7. <span data-ttu-id="90f86-128">Schaltflächen Löschen</span><span class="sxs-lookup"><span data-stu-id="90f86-128">Clear buttons</span></span>

   - <span data-ttu-id="90f86-129">**Cache löschen**: entfernt alle im Browsercache gespeicherten Ressourcen (und emuliert eine erstmalige Benutzeroberfläche beim Laden der Seite).</span><span class="sxs-lookup"><span data-stu-id="90f86-129">**Clear cache**: Removes all resources stored in the browser cache (and emulates a first-time experience loading the page).</span></span>
   - <span data-ttu-id="90f86-130">**Cookies löschen**: entfernt alle Cookies für die angegebene Domäne (und emuliert eine erstmalige Nutzung der Website).</span><span class="sxs-lookup"><span data-stu-id="90f86-130">**Clear cookies**: Removes all cookies for the given domain (and emulates a first-time experience of the site).</span></span>
   - <span data-ttu-id="90f86-131">**Einträge beim Navigieren löschen: der**aufgezeichnete Datenverkehr wird bei der Seitennavigation gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90f86-131">**Clear entries on navigate**: Recorded traffic is cleared upon page navigation.</span></span> <span data-ttu-id="90f86-132">Dies ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="90f86-132">This is turned on by default.</span></span>
   - <span data-ttu-id="90f86-133">**Sitzung löschen**: Löscht alle Netzwerk Anforderungs Einträge aus der **Netzwerk Zusammenfassungs** Liste.</span><span class="sxs-lookup"><span data-stu-id="90f86-133">**Clear session**: Clears all network request entries from the **Network summary** list.</span></span>

### <span data-ttu-id="90f86-134">Liste der Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="90f86-134">Network request list</span></span>

<span data-ttu-id="90f86-135">Der gesamte Netzwerkdatenverkehr wird in einer Liste aufgezeichnet (bis zum Zeitpunkt der Navigation, manuelles Löschen oder devtools geschlossen).</span><span class="sxs-lookup"><span data-stu-id="90f86-135">All network traffic is recorded to a list (until cleared upon navigation, manually cleared, or  DevTools are closed).</span></span> <span data-ttu-id="90f86-136">Wenn Sie auf einen Eintrag klicken, wird eine [detailliertere Ansicht der Anfrage](#request-details)geöffnet.</span><span class="sxs-lookup"><span data-stu-id="90f86-136">Clicking on any entry will open a more [detailed view of the request](#request-details).</span></span>

![Liste der Netzwerkanforderungen](./media/network_request_list.png)

<span data-ttu-id="90f86-138">Die Netzwerk Anforderungsliste enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="90f86-138">The network request list includes the following info:</span></span> 

<span data-ttu-id="90f86-139">Spalte</span><span class="sxs-lookup"><span data-stu-id="90f86-139">Column</span></span> | <span data-ttu-id="90f86-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90f86-140">Description</span></span> 
:------------ | :------------- 
**<span data-ttu-id="90f86-141">Name</span><span class="sxs-lookup"><span data-stu-id="90f86-141">Name</span></span>** | <span data-ttu-id="90f86-142">Name und URL-Pfad der Anforderung</span><span class="sxs-lookup"><span data-stu-id="90f86-142">Name and URL path of the request</span></span>
**<span data-ttu-id="90f86-143">Protokoll</span><span class="sxs-lookup"><span data-stu-id="90f86-143">Protocol</span></span>** |  <span data-ttu-id="90f86-144">Der Typ des Protokolls für die Anforderung (wie *https; HTTP/2*)</span><span class="sxs-lookup"><span data-stu-id="90f86-144">Type of protocol for the request (such as *HTTPS, HTTP/2*)</span></span>
**<span data-ttu-id="90f86-145">Methode</span><span class="sxs-lookup"><span data-stu-id="90f86-145">Method</span></span>** |    <span data-ttu-id="90f86-146">Für die Anforderung verwendete [http-Methode](https://developer.mozilla.org/docs/Web/HTTP/Methods)</span><span class="sxs-lookup"><span data-stu-id="90f86-146">[HTTP method](https://developer.mozilla.org/docs/Web/HTTP/Methods) used for the request</span></span>
**<span data-ttu-id="90f86-147">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="90f86-147">Result</span></span>** |    <span data-ttu-id="90f86-148">[HTTP-Antwortstatus](https://developer.mozilla.org/docs/Web/HTTP/Status)  Code</span><span class="sxs-lookup"><span data-stu-id="90f86-148">[HTTP response status](https://developer.mozilla.org/docs/Web/HTTP/Status)  code</span></span>
**<span data-ttu-id="90f86-149">Inhaltstyp</span><span class="sxs-lookup"><span data-stu-id="90f86-149">Content type</span></span>** |  <span data-ttu-id="90f86-150">Art des angeforderten Mediums ([MIME-Typ](https://en.wikipedia.org/wiki/Media_type))</span><span class="sxs-lookup"><span data-stu-id="90f86-150">Type of media requested ([MIME type](https://en.wikipedia.org/wiki/Media_type))</span></span>
**<span data-ttu-id="90f86-151">Empfangen</span><span class="sxs-lookup"><span data-stu-id="90f86-151">Received</span></span>** | <span data-ttu-id="90f86-152">Die Größe der Antwort, wie Sie vom Server bereitgestellt wurde (wird nicht für zwischengespeicherte Antworten berechnet)</span><span class="sxs-lookup"><span data-stu-id="90f86-152">Size of the response as delivered by the server (not calculated for cached responses)</span></span>
**<span data-ttu-id="90f86-153">Zeit</span><span class="sxs-lookup"><span data-stu-id="90f86-153">Time</span></span>** |  <span data-ttu-id="90f86-154">Zeit zum Laden der Serverantwort (nicht für zwischengespeicherte Antworten berechnet)</span><span class="sxs-lookup"><span data-stu-id="90f86-154">Time to load the server response (not calculated for cached responses)</span></span>
**<span data-ttu-id="90f86-155">Initiator</span><span class="sxs-lookup"><span data-stu-id="90f86-155">Initiator</span></span>** | <span data-ttu-id="90f86-156">Subsystem, das für das Initiieren der Anforderung verantwortlich ist (wie *Parser, Redirect, Skript usw*.)</span><span class="sxs-lookup"><span data-stu-id="90f86-156">Subsystem responsible for initiating the request (such as *Parser, Redirect, Script, Other*)</span></span>
**<span data-ttu-id="90f86-157">Zeitachse</span><span class="sxs-lookup"><span data-stu-id="90f86-157">Timeline</span></span>** | <span data-ttu-id="90f86-158">Visuelle Zeitachse für die Netzwerkereignisse der Anforderung (wie *verzögert, auflösen (DNS), verbinden (TCP), SSL, senden, warten (TTFB), herunterladen*).</span><span class="sxs-lookup"><span data-stu-id="90f86-158">Visual timeline for the network events of the request (such as *Stalled, Resolving(DNS), Connecting(TCP), SSL, Sending, Waiting(TTFB), Downloading*).</span></span> <span data-ttu-id="90f86-159">Wenn Sie den Mauszeiger über das Diagramm bewegen, erhalten Sie eine genauere Unterbrechung der Netzwerk [Anzeige](#timings)dauern.</span><span class="sxs-lookup"><span data-stu-id="90f86-159">Hovering over the chart provides the more granular breakdown of network [network timings](#timings)).</span></span>

### <span data-ttu-id="90f86-160">Zusammenfassungs Leiste</span><span class="sxs-lookup"><span data-stu-id="90f86-160">Summary bar</span></span>

<span data-ttu-id="90f86-161">Die Leiste am unteren Rand des **Netzwerk** Panels fasst die Gesamtzahl der HTTP-Netzwerkfehler,-Anforderungen,-Datenübertragungen und-Ladezeiten während der Netzwerkprofil Erstellungs Sitzung zusammen (d. h., seit devtools geöffnet wurden und den Netzwerkdatenverkehr aufzeichnen).</span><span class="sxs-lookup"><span data-stu-id="90f86-161">The bar at the bottom of **Network** panel summarizes the total number of HTTP network errors, requests, data transfered, and load times during the network profiling session (i.e., since  DevTools were opened and recording network traffic).</span></span>

![Netzwerk Zusammenfassungs Leiste](./media/network_summary_bar.png)

<span data-ttu-id="90f86-163">**Verstrichene Zeit** bedeutet die Zeit zwischen dem Start der Profilerstellungssitzung und dem Zeitpunkt, zu dem die letzte Ressource aus dem Netzwerk heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="90f86-163">**Elapsed time** means the time between the start of the profiling session and when the last resource was downloaded from the network.</span></span> <span data-ttu-id="90f86-164">Ressourcen, die aus dem Browser-Cache abgerufen werden, werden dieser Nummer nicht Zeit gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="90f86-164">Resources fetched from the browser cache do not accrue time to this number.</span></span> 

<span data-ttu-id="90f86-165">**DOM Load Time** bezeichnet die Zeit zwischen dem Beginn der Profilerstellungssitzung und dem Zeitpunkt, zu dem das [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) -Ereignis ausgelöst wurde, um anzugeben, dass die Struktur des Seitendokuments geladen und analysiert wurde (aber nicht unbedingt alle Stylesheets, Bilder oder unter Frames).</span><span class="sxs-lookup"><span data-stu-id="90f86-165">**DOM load time** means the time between the start of the profiling session and when the [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) event was fired to indicate that the structure of the page document has been loaded and parsed (though not necessarily any stylesheets, images or subframes).</span></span>

<span data-ttu-id="90f86-166">**"Seitenladezeit"** bedeutet die Zeit zwischen dem Start der Profilerstellungssitzung und dem Zeitpunkt, zu dem das [Load](https://developer.mozilla.org/docs/Web/Events/load) -Ereignis ausgelöst wurde, um anzugeben, dass das Seiten Dokument (und alle zugehörigen Ressourcen) vollständig geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="90f86-166">**Page load time** time means the time between the start of the profiling session and when the [load](https://developer.mozilla.org/docs/Web/Events/load) event was fired to indicate that the page document (and all its resources) has been fully loaded.</span></span>

## <span data-ttu-id="90f86-167">Details anfordern</span><span class="sxs-lookup"><span data-stu-id="90f86-167">Request details</span></span>

<span data-ttu-id="90f86-168">Wenn Sie auf einen Eintrag in der [**Netzwerk Zusammenfassungs**](#network-summary) Liste klicken, wird der Bereich [**Anforderungsdetails**](#request-details) mit weiteren Informationen auf den folgenden Registerkarten geöffnet.</span><span class="sxs-lookup"><span data-stu-id="90f86-168">Clicking on any entry in the [**Network summary**](#network-summary) list will open the [**Request details**](#request-details) pane with further information in each of the following tabs.</span></span>

![Bereich ' Netzwerk Anforderungsdetails '](./media/network_request_details.png)

### <span data-ttu-id="90f86-170">Header</span><span class="sxs-lookup"><span data-stu-id="90f86-170">Headers</span></span>
<span data-ttu-id="90f86-171">Zeigt die [http-Header](https://developer.mozilla.org/docs/Web/HTTP/Headers) an, die vom Server gesendet und empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="90f86-171">Displays the [HTTP headers](https://developer.mozilla.org/docs/Web/HTTP/Headers) sent to and received from the server.</span></span> <span data-ttu-id="90f86-172">Klicken Sie mit der rechten Maustaste auf einen beliebigen kopfzeileneintrag, um ihn ( `Ctrl+C` ) in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="90f86-172">Right-click on any header entry to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="90f86-173">Sie können auch eine Mehrfachauswahl von Einträgen durchführen, indem Sie die Taste gedrückt halten `Shift` oder alle auswählen ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="90f86-173">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

### <span data-ttu-id="90f86-174">Textkörper</span><span class="sxs-lookup"><span data-stu-id="90f86-174">Body</span></span>
<span data-ttu-id="90f86-175">Zeigt die Textkörper Daten (sofern verfügbar) der Anforderungs-und Antwort Nutzlast an.</span><span class="sxs-lookup"><span data-stu-id="90f86-175">Displays the body data (if available) of the request and response payloads.</span></span>

<span data-ttu-id="90f86-176">Bildinhalte werden mit Bemaßungen und Größendaten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90f86-176">Image content is displayed with dimensions and size data.</span></span>

<span data-ttu-id="90f86-177">Text Inhalte werden in einem (schreibgeschützten) Editor mit Optionen zum Formatieren von minimierte-Inhalten mit **Pretty Print** und/oder **Word Wrap** angezeigt, um die Lesbarkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="90f86-177">Text content appears in a (read-only) editor with options to format minified content with **Pretty print** and/or **Word wrap** for easier readability.</span></span>

![Registerkarte "Text" im Bereich "Anforderungsdetails"](./media/network_details_body.png)

### <span data-ttu-id="90f86-179">Parameter</span><span class="sxs-lookup"><span data-stu-id="90f86-179">Parameters</span></span>
<span data-ttu-id="90f86-180">Zeigt Abfragezeichenfolgenparameter für Get-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="90f86-180">Displays query string parameters for GET requests.</span></span> <span data-ttu-id="90f86-181">Während die Parameter von Post-Anforderungen in den Kopfzeilen gesendet werden, werden Sie von Get-Anforderungen in die URL eingefügt.</span><span class="sxs-lookup"><span data-stu-id="90f86-181">While the parameters of POST requests are sent in the headers, GET requests include them in the URL.</span></span> <span data-ttu-id="90f86-182">Sie sind hier ausgebrochen, um einfacher zu lesen.</span><span class="sxs-lookup"><span data-stu-id="90f86-182">They're broken out here for easier reading.</span></span>

<span data-ttu-id="90f86-183">Klicken Sie mit der rechten Maustaste auf eine beliebige Zeile, um Sie ( `Ctrl+C` ) in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="90f86-183">Right-click on any row to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="90f86-184">Sie können auch eine Mehrfachauswahl von Einträgen durchführen, indem Sie die Taste gedrückt halten `Shift` oder alle auswählen ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="90f86-184">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

### <span data-ttu-id="90f86-185">Cookies</span><span class="sxs-lookup"><span data-stu-id="90f86-185">Cookies</span></span>
<span data-ttu-id="90f86-186">Zeigt Cookies an, die als Schlüssel-Wert-Paare gesendet oder empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="90f86-186">Displays cookies that are sent or received as key/value pairs.</span></span>

<span data-ttu-id="90f86-187">Klicken Sie mit der rechten Maustaste auf eine beliebige Zeile, um Sie ( `Ctrl+C` ) in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="90f86-187">Right-click on any row to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="90f86-188">Sie können auch eine Mehrfachauswahl von Einträgen durchführen, indem Sie die Taste gedrückt halten `Shift` oder alle auswählen ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="90f86-188">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

<span data-ttu-id="90f86-189">Sie können die gespeicherten Cookies für die angegebene Domäne über die [Symbolleiste](#network-summary) löschen (Schaltfläche "**Cookies löschen** ").</span><span class="sxs-lookup"><span data-stu-id="90f86-189">You can clear the stored cookies for the given domain from the [Toolbar](#network-summary) (**Clear cookies** button).</span></span> 

### <span data-ttu-id="90f86-190">Timings</span><span class="sxs-lookup"><span data-stu-id="90f86-190">Timings</span></span>

<span data-ttu-id="90f86-191">Die Registerkarte **Anzeige** Dauer enthält eine Zeitachse mit Netzwerkereignissen, die am Laden der ausgewählten Ressource beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="90f86-191">The **Timings** tab provides a timeline of network events involved in the loading of the selected resource.</span></span> <span data-ttu-id="90f86-192">Dies ähnelt den Informationen, die in der Spalte " *Zeitachse* " der [Netzwerk Anforderungsliste](#network-request-list)enthalten sind, enthält aber auch die Ereignisse, die zu der Anforderung führen, die über den Draht gesendet wird\*\*, wie etwa die Wartezeit in der Anforderungswarteschlange, die DNS-Auflösung und das Einrichten der TCP-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="90f86-192">This is similar to the information found in the *Timeline* column of the [Network request list](#network-request-list), but also includes the events leading up to the request being sent over the wire, such as time spent waiting (*Stalled*) in the request queue, DNS resolution, and establishing the TCP connection.</span></span> 

![Registerkarte "Anzeigedauern" im Bereich "Anforderungsdetails"](./media/network_details_timings.png)

<span data-ttu-id="90f86-194">Umleitungen zu/von anderen Ressourcen werden notiert, und durch Klicken auf den Link wird der Fokus auf diese Ressource im Bereich Netzwerk [Anforderungsdetails](#request details) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="90f86-194">Redirections to/from other resources are noted, and clicking on the link will set focus to that resource in the network [request details](#request details) pane.</span></span>

<span data-ttu-id="90f86-195">Resouces, die aus dem Cache geladen werden, sind von der Netzwerklatenz nicht betroffen, daher wird *kein Diagramm für Netzwerk Anzeigedauern* angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90f86-195">Resouces loaded from the cache are not affected by network latency, so no network *Timings* chart will display.</span></span>

![Umgeleitete Ressource, die aus dem Cache geladen wurde](./media/network_details_timings_cache_redirect.png)

<span data-ttu-id="90f86-197">Hier sind die verschiedenen Netzwerkereignisse, die für eine bestimmte Ressource möglicherweise in chronologischer Reihenfolge angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="90f86-197">Here are the different network events you might see for a given resource, in chronological order:</span></span>

#### <span data-ttu-id="90f86-198">Blockiert</span><span class="sxs-lookup"><span data-stu-id="90f86-198">Stalled</span></span>

<span data-ttu-id="90f86-199">Zeit, die auf eine verfügbare Netzwerkverbindung in der Anforderungswarteschlange wartet.</span><span class="sxs-lookup"><span data-stu-id="90f86-199">Time spent waiting for an available network connection in the request queue.</span></span> <span data-ttu-id="90f86-200">Für HTTP 1.0/1.1 ermöglicht Microsoft Edge maximal sechs (6) gleichzeitige TCP-Verbindungen pro Hostname.</span><span class="sxs-lookup"><span data-stu-id="90f86-200">For HTTP 1.0/1.1, Microsoft Edge allows a maximum of six (6) simultaneous TCP connections per hostname.</span></span> 

#### <span data-ttu-id="90f86-201">Auflösen (DNS)</span><span class="sxs-lookup"><span data-stu-id="90f86-201">Resolving (DNS)</span></span>

<span data-ttu-id="90f86-202">Zeit, die die IP-Adresse für den Hostnamen der Ressource im DNS ([Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System)) nachschlagen soll.</span><span class="sxs-lookup"><span data-stu-id="90f86-202">Time spent looking up the IP address for the hostname of the resource in the DNS ([Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System)).</span></span>

#### <span data-ttu-id="90f86-203">Verbinden (TCP)</span><span class="sxs-lookup"><span data-stu-id="90f86-203">Connecting (TCP)</span></span>

<span data-ttu-id="90f86-204">Zeit, die für das Einrichten der TCP-Verbindung ([Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)) aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="90f86-204">Time spent establishing the TCP ([Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)) connection.</span></span>

#### <span data-ttu-id="90f86-205">SSL</span><span class="sxs-lookup"><span data-stu-id="90f86-205">SSL</span></span>

<span data-ttu-id="90f86-206">Zeit, die für die Aushandlung einer SSL-Verbindung ([Secure Sockets Layer](https://en.wikipedia.org/wiki/Transport_Layer_Security)) mit dem [Proxy Server](https://en.wikipedia.org/wiki/Proxy_server) für den Host aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="90f86-206">Time spent negotiating a SSL ([Secure Sockets Layer](https://en.wikipedia.org/wiki/Transport_Layer_Security))  connection with the [proxy server](https://en.wikipedia.org/wiki/Proxy_server) for the host.</span></span>

#### <span data-ttu-id="90f86-207">Senden</span><span class="sxs-lookup"><span data-stu-id="90f86-207">Sending</span></span>

<span data-ttu-id="90f86-208">Der Zeitaufwand für das Senden der Ressourcenanforderung.</span><span class="sxs-lookup"><span data-stu-id="90f86-208">Time spent sending the resource request.</span></span>

#### <span data-ttu-id="90f86-209">Warten (TTFB)</span><span class="sxs-lookup"><span data-stu-id="90f86-209">Waiting (TTFB)</span></span>

<span data-ttu-id="90f86-210">Die Wartezeit für das erste Byte der Antwort vom Hostserver ("Time to First Byte" oder *TTFB*).</span><span class="sxs-lookup"><span data-stu-id="90f86-210">Time spent waiting for the first byte of the response from the host server ("time to first byte", or *TTFB*).</span></span>

#### <span data-ttu-id="90f86-211">Herunterladen</span><span class="sxs-lookup"><span data-stu-id="90f86-211">Downloading</span></span>

<span data-ttu-id="90f86-212">Die Zeit, die beim Lesen der Antwort vom Server aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="90f86-212">Time spent reading the response from the server.</span></span>

## <span data-ttu-id="90f86-213">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="90f86-213">Shortcuts</span></span>

| <span data-ttu-id="90f86-214">Aktion</span><span class="sxs-lookup"><span data-stu-id="90f86-214">Action</span></span>                         | <span data-ttu-id="90f86-215">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="90f86-215">Shortcut</span></span>     |
|:-------------------------------|:-------------|
| <span data-ttu-id="90f86-216">Starten/Beenden der Profilerstellungssitzung</span><span class="sxs-lookup"><span data-stu-id="90f86-216">Start / Stop profiling session</span></span> | `Ctrl` + `E` |
| <span data-ttu-id="90f86-217">Als har exportieren</span><span class="sxs-lookup"><span data-stu-id="90f86-217">Export as HAR</span></span>                  | `Ctrl` + `S` |
| <span data-ttu-id="90f86-218">Suchen</span><span class="sxs-lookup"><span data-stu-id="90f86-218">Find</span></span>                           | `Ctrl` + `F` |
| <span data-ttu-id="90f86-219">Kopieren</span><span class="sxs-lookup"><span data-stu-id="90f86-219">Copy</span></span>                           | `Ctrl` + `C` |

## <span data-ttu-id="90f86-220">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="90f86-220">Known Issues</span></span>

### <span data-ttu-id="90f86-221">Der Netzwerk Sammlungs-Agent konnte nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="90f86-221">The network collection agent failed to start.</span></span>

<span data-ttu-id="90f86-222">Wenn diese Fehlermeldung angezeigt wird: Fehler beim **Starten des Netzwerk Sammlungs-Agents** im Netzwerktool, führen Sie die folgenden Schritte aus, um eine Problemumgehung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="90f86-222">If you see this error message: **The network collection agent failed to start** in the Network tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="90f86-223">Drücken Sie `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="90f86-223">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="90f86-224">Geben Sie im Dialogfeld Ausführen den **Dienst "Services. msc**" ein.</span><span class="sxs-lookup"><span data-stu-id="90f86-224">In the Run dialog, enter **services.msc**.</span></span>
![Bekannte Probleme-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="90f86-226">Suchen Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst** , und klicken Sie mit der rechten Maustaste darauf.</span><span class="sxs-lookup"><span data-stu-id="90f86-226">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![Bekannte Probleme-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="90f86-228">Starten Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst**erneut.</span><span class="sxs-lookup"><span data-stu-id="90f86-228">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![Bekannte Probleme-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="90f86-230">Schließen Sie die Microsoft Edge-Entwickler Tools und die Registerkarte. Öffnen Sie eine neue Registerkarte, navigieren Sie zu Ihrer Seite, und drücken Sie `F12` .</span><span class="sxs-lookup"><span data-stu-id="90f86-230">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="90f86-231">Neben **Netzwerk** und Netzwerkanforderungen für Ihre Webseite sollte nun ein Play-Signal angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="90f86-231">You should now see a Play badge next to **Network** and the network requests for your webpage.</span></span>
![Bekannte Probleme-4](./media/known_issues_4-network.PNG)

<span data-ttu-id="90f86-233">Gibt es immer noch Probleme?</span><span class="sxs-lookup"><span data-stu-id="90f86-233">Still running into problems?</span></span> <span data-ttu-id="90f86-234">Senden Sie uns Ihr Feedback über das Symbol **Feedback senden** !</span><span class="sxs-lookup"><span data-stu-id="90f86-234">Please send us your feedback using the **Send feedback** icon!</span></span> 

![Bekannte Probleme-5](./media/known_issues_5.PNG)

### <span data-ttu-id="90f86-236">Fehler beim Beenden des Netzwerk Sammlungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="90f86-236">The network collection agent failed to stop.</span></span>

<span data-ttu-id="90f86-237">Wenn diese Fehlermeldung angezeigt wird: Fehler beim **Beenden des Netzwerk Sammlungs-Agents** im Netzwerktool, führen Sie die folgenden Schritte aus, um eine Problemumgehung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="90f86-237">If you see this error message: **The network collection agent failed to stop** in the Network tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="90f86-238">Drücken Sie `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="90f86-238">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="90f86-239">Geben Sie im Dialogfeld Ausführen den **Dienst "Services. msc**" ein.</span><span class="sxs-lookup"><span data-stu-id="90f86-239">In the Run dialog, enter **services.msc**.</span></span>
![Bekannte Probleme-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="90f86-241">Suchen Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst** , und klicken Sie mit der rechten Maustaste darauf.</span><span class="sxs-lookup"><span data-stu-id="90f86-241">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![Bekannte Probleme-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="90f86-243">Starten Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst**erneut.</span><span class="sxs-lookup"><span data-stu-id="90f86-243">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![Bekannte Probleme-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="90f86-245">Schließen Sie die Microsoft Edge-Entwickler Tools und die Registerkarte. Öffnen Sie eine neue Registerkarte, navigieren Sie zu Ihrer Seite, und drücken Sie `F12` .</span><span class="sxs-lookup"><span data-stu-id="90f86-245">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="90f86-246">Neben **Netzwerk** und Netzwerkanforderungen für Ihre Webseite sollte nun ein Play-Signal angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="90f86-246">You should now see a Play badge next to **Network** and the network requests for your webpage.</span></span>
![Bekannte Probleme-4](./media/known_issues_4-network.PNG)

<span data-ttu-id="90f86-248">Gibt es immer noch Probleme?</span><span class="sxs-lookup"><span data-stu-id="90f86-248">Still running into problems?</span></span> <span data-ttu-id="90f86-249">Senden Sie uns Ihr Feedback über das Symbol **Feedback senden** !</span><span class="sxs-lookup"><span data-stu-id="90f86-249">Please send us your feedback using the **Send feedback** icon!</span></span> 

![Bekannte Probleme-5](./media/known_issues_5.PNG)

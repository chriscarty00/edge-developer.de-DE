---
title: Anzeigen von Anwendungs Cache Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: fc1800fc54e5fb0d7998c62ce163ece7a461dd82
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931211"
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

# <span data-ttu-id="cd06a-103">Anzeigen von Anwendungs Cache Daten mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="cd06a-103">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="cd06a-104">Die Anwendungs Cache-API wird [aus der Web-Plattform entfernt][HTMLStandardOfflineWebApplications].</span><span class="sxs-lookup"><span data-stu-id="cd06a-104">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="cd06a-105">Dieser Leitfaden zeigt Ihnen, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um [Anwendungs Cache][MDNWebAPIsWindowApplicationCache] Ressourcen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cd06a-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <span data-ttu-id="cd06a-106">Anzeigen von Anwendungs Cache Daten</span><span class="sxs-lookup"><span data-stu-id="cd06a-106">View Application Cache data</span></span>  

1.  <span data-ttu-id="cd06a-107">Wählen Sie die Registerkarte **Quellen** aus, um das **Quellen** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cd06a-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="cd06a-108">Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="cd06a-108">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="cd06a-110">Bereich ' **Manifest** '</span><span class="sxs-lookup"><span data-stu-id="cd06a-110">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="cd06a-111">Erweitern Sie den Abschnitt **Anwendungscache** , und wählen Sie einen Cache aus, um die Ressourcen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cd06a-111">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Der Anwendungs Cache Bereich" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="cd06a-113">Der **Anwendungs Cache** Bereich</span><span class="sxs-lookup"><span data-stu-id="cd06a-113">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="cd06a-114">Jede Zeile der Tabelle stellt eine zwischengespeicherte Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="cd06a-114">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="cd06a-115">Die Spalte **Typ** steht [für die Kategorie der Ressource][MDNHTMLResourcesInAnApplicationCache].</span><span class="sxs-lookup"><span data-stu-id="cd06a-115">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="cd06a-116">Kategorie</span><span class="sxs-lookup"><span data-stu-id="cd06a-116">Category</span></span> | <span data-ttu-id="cd06a-117">Details</span><span class="sxs-lookup"><span data-stu-id="cd06a-117">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="cd06a-118">Diese Ressource wurde explizit im Manifest aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd06a-118">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="cd06a-119">Die URL ist ein Fallback für eine andere Ressource.</span><span class="sxs-lookup"><span data-stu-id="cd06a-119">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="cd06a-120">Die URL der anderen Ressource ist in devtools nicht aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd06a-120">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="cd06a-121">Das `manifest` Attribut der Ressource gibt an, dass der Cache das übergeordnete Element der Ressource ist.</span><span class="sxs-lookup"><span data-stu-id="cd06a-121">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="cd06a-122">Das Manifest hat angegeben, dass die Ressource aus dem Netzwerk stammen muss.</span><span class="sxs-lookup"><span data-stu-id="cd06a-122">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="cd06a-123">Am unteren Rand der Tabelle befinden sich Statussymbole, die Ihre Netzwerkverbindung und den Status des **Anwendungscaches**angeben.</span><span class="sxs-lookup"><span data-stu-id="cd06a-123">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="cd06a-124">Der **Anwendungs Cache** kann die folgenden Zustände aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cd06a-124">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="cd06a-125">Status</span><span class="sxs-lookup"><span data-stu-id="cd06a-125">State</span></span> | <span data-ttu-id="cd06a-126">Details</span><span class="sxs-lookup"><span data-stu-id="cd06a-126">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="cd06a-127">Das Manifest wird abgerufen und auf Updates überprüft.</span><span class="sxs-lookup"><span data-stu-id="cd06a-127">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="cd06a-128">Ressourcen werden dem Cache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd06a-128">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="cd06a-129">Der Cache hat keine neuen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="cd06a-129">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="cd06a-130">Der Cache wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cd06a-130">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="cd06a-131">Eine neue Version des Caches ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cd06a-131">A new version of the cache is available.</span></span> |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Offline-Webanwendungen – HTML-Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressourcen in einem Anwendungscache | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-Web-APIs | MDN"  

> [!NOTE]
> <span data-ttu-id="cd06a-136">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd06a-136">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cd06a-137">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd06a-137">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="cd06a-139">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cd06a-139">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

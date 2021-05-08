---
description: Anzeigen von Anwendungscachedaten aus dem Anwendungsbereich von Microsoft Edge DevTools.
title: Anzeigen von Anwendungscachedaten mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: cbe6623aa3132db4d01cd6b440702eb157525eed
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519142"
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

# <a name="view-application-cache-data-with-microsoft-edge-devtools"></a><span data-ttu-id="df7d1-104">Anzeigen von Anwendungscachedaten mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="df7d1-104">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="df7d1-105">Die Anwendungscache-API [wird von der Webplattform entfernt.][HTMLStandardOfflineWebApplications]</span><span class="sxs-lookup"><span data-stu-id="df7d1-105">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="df7d1-106">In diesem Handbuch erfahren Sie, wie Sie [Microsoft Edge DevTools verwenden,][MicrosoftEdgeDevTools] um Anwendungscacheressourcen [zu][MDNWebAPIsWindowApplicationCache] überprüfen.</span><span class="sxs-lookup"><span data-stu-id="df7d1-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <a name="view-application-cache-data"></a><span data-ttu-id="df7d1-107">Anzeigen von Anwendungscachedaten</span><span class="sxs-lookup"><span data-stu-id="df7d1-107">View Application Cache data</span></span>  

1.  <span data-ttu-id="df7d1-108">Wählen Sie oben in DevTools das **Tool Anwendung** aus.</span><span class="sxs-lookup"><span data-stu-id="df7d1-108">At the top of DevTools, choose the **Application** tool.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="df7d1-110">Der **Manifestbereich**</span><span class="sxs-lookup"><span data-stu-id="df7d1-110">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="df7d1-111">Erweitern Sie den **Abschnitt Anwendungscache,** und wählen Sie einen Cache aus, um die Ressourcen anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="df7d1-111">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Der Bereich Anwendungscache" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="df7d1-113">Der **Bereich Anwendungscache**</span><span class="sxs-lookup"><span data-stu-id="df7d1-113">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="df7d1-114">Jede Zeile der Tabelle stellt eine zwischengespeicherte Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="df7d1-114">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="df7d1-115">Die **Spalte Type** stellt die Kategorie der Ressource [dar.][MDNHTMLResourcesInAnApplicationCache]</span><span class="sxs-lookup"><span data-stu-id="df7d1-115">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="df7d1-116">Kategorie</span><span class="sxs-lookup"><span data-stu-id="df7d1-116">Category</span></span> | <span data-ttu-id="df7d1-117">Details</span><span class="sxs-lookup"><span data-stu-id="df7d1-117">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="df7d1-118">Diese Ressource wurde explizit im Manifest aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="df7d1-118">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="df7d1-119">Die URL ist ein Fallback für eine andere Ressource.</span><span class="sxs-lookup"><span data-stu-id="df7d1-119">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="df7d1-120">Die URL der anderen Ressource ist in DevTools nicht aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="df7d1-120">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="df7d1-121">Das `manifest` Attribut für die Ressource gibt an, dass der Cache das übergeordnete Element der Ressource ist.</span><span class="sxs-lookup"><span data-stu-id="df7d1-121">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="df7d1-122">Das Manifest hat angegeben, dass die Ressource aus dem Netzwerk stammen muss.</span><span class="sxs-lookup"><span data-stu-id="df7d1-122">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="df7d1-123">Am unteren Rand der Tabelle befinden sich Statussymbole, die Ihre Netzwerkverbindung und den Status des **Anwendungscaches angeben.**</span><span class="sxs-lookup"><span data-stu-id="df7d1-123">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="df7d1-124">Der **Anwendungscache** kann die folgenden Zustände haben.</span><span class="sxs-lookup"><span data-stu-id="df7d1-124">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="df7d1-125">Status</span><span class="sxs-lookup"><span data-stu-id="df7d1-125">State</span></span> | <span data-ttu-id="df7d1-126">Details</span><span class="sxs-lookup"><span data-stu-id="df7d1-126">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="df7d1-127">Das Manifest wird abgerufen und auf Updates überprüft.</span><span class="sxs-lookup"><span data-stu-id="df7d1-127">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="df7d1-128">Dem Cache werden Ressourcen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="df7d1-128">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="df7d1-129">Der Cache hat keine neuen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="df7d1-129">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="df7d1-130">Der Cache wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="df7d1-130">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="df7d1-131">Eine neue Version des Caches ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="df7d1-131">A new version of the cache is available.</span></span> |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Offlinewebanwendungen – HTML Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressourcen in einem Anwendungscache | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache – Web-APIs | MDN"  

> [!NOTE]
> <span data-ttu-id="df7d1-136">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df7d1-136">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="df7d1-137">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="df7d1-137">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="df7d1-139">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="df7d1-139">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

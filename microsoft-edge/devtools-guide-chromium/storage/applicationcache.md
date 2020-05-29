---
title: Anzeigen von Anwendungs Cache Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 6ce3087e9c719efbcf4d9ebceb860edd0ed0c3b6
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612095"
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





# <span data-ttu-id="bd695-103">Anzeigen von Anwendungs Cache Daten mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="bd695-103">View Application Cache Data With Microsoft Edge DevTools</span></span>   



> [!WARNING]
> <span data-ttu-id="bd695-104">Die Anwendungs Cache-API wird [aus der Web-Plattform entfernt][HTMLStandardOfflineWebApplications].</span><span class="sxs-lookup"><span data-stu-id="bd695-104">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="bd695-105">Dieser Leitfaden zeigt Ihnen, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um [Anwendungs Cache][MDNWebAPIsWindowApplicationCache] Ressourcen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="bd695-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <span data-ttu-id="bd695-106">Anzeigen von Anwendungs Cache Daten</span><span class="sxs-lookup"><span data-stu-id="bd695-106">View Application Cache Data</span></span>   

1.  <span data-ttu-id="bd695-107">Wählen Sie die Registerkarte **Quellen** aus, um das **Quellen** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bd695-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="bd695-108">Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bd695-108">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="bd695-109">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="bd695-109">Figure 1</span></span>  
    > <span data-ttu-id="bd695-110">Bereich ' Manifest '</span><span class="sxs-lookup"><span data-stu-id="bd695-110">The Manifest pane</span></span>  
    > ![Bereich ' Manifest '][ImageManifestPane]  

1.  <span data-ttu-id="bd695-112">Erweitern Sie den Abschnitt **Anwendungscache** , und klicken Sie auf einen Cache, um die Ressourcen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bd695-112">Expand the **Application Cache** section and click a cache to view the resources.</span></span>  
    
    > ##### <span data-ttu-id="bd695-113">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="bd695-113">Figure 2</span></span>  
    > <span data-ttu-id="bd695-114">Der Anwendungs Cache Bereich</span><span class="sxs-lookup"><span data-stu-id="bd695-114">The Application Cache pane</span></span>  
    > ![Der Anwendungs Cache Bereich][ImageApplicationCachePane]  

<span data-ttu-id="bd695-116">Jede Zeile der Tabelle stellt eine zwischengespeicherte Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="bd695-116">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="bd695-117">Die Spalte **Typ** steht [für die Kategorie der Ressource][MDNHTMLResourcesInAnApplicationCache].</span><span class="sxs-lookup"><span data-stu-id="bd695-117">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="bd695-118">Kategorie</span><span class="sxs-lookup"><span data-stu-id="bd695-118">Category</span></span> | <span data-ttu-id="bd695-119">Details</span><span class="sxs-lookup"><span data-stu-id="bd695-119">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="bd695-120">Diese Ressource wurde explizit im Manifest aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd695-120">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="bd695-121">Die URL ist ein Fallback für eine andere Ressource.</span><span class="sxs-lookup"><span data-stu-id="bd695-121">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="bd695-122">Die URL der anderen Ressource ist in devtools nicht aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd695-122">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="bd695-123">Das `manifest` Attribut für die Ressource hat angegeben, dass dieser Cache das übergeordnete Element der Ressource ist.</span><span class="sxs-lookup"><span data-stu-id="bd695-123">The `manifest` attribute on the resource indicated that this cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="bd695-124">Das Manifest hat angegeben, dass diese Ressource aus dem Netzwerk stammen muss.</span><span class="sxs-lookup"><span data-stu-id="bd695-124">The manifest specified that this resource must come from the network.</span></span> |  

<span data-ttu-id="bd695-125">Am unteren Rand der Tabelle befinden sich Statussymbole, die Ihre Netzwerkverbindung und den Status des Anwendungscaches angeben.</span><span class="sxs-lookup"><span data-stu-id="bd695-125">At the bottom of the table there are status icons indicating your network connection and the status of the Application Cache.</span></span>  <span data-ttu-id="bd695-126">Der Anwendungs Cache kann die folgenden Zustände aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bd695-126">The Application Cache may have the following states.</span></span>  

| <span data-ttu-id="bd695-127">Status</span><span class="sxs-lookup"><span data-stu-id="bd695-127">State</span></span> | <span data-ttu-id="bd695-128">Details</span><span class="sxs-lookup"><span data-stu-id="bd695-128">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="bd695-129">Das Manifest wird abgerufen und auf Updates überprüft.</span><span class="sxs-lookup"><span data-stu-id="bd695-129">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="bd695-130">Ressourcen werden dem Cache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bd695-130">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="bd695-131">Der Cache hat keine neuen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="bd695-131">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="bd695-132">Der Cache wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bd695-132">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="bd695-133">Eine neue Version des Caches ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bd695-133">A new version of the cache is available.</span></span> |  

<!--   -->  



<!-- image links -->  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Abbildung 1: der Bereich "Manifest""  
[ImageApplicationCachePane]: /microsoft-edge/devtools-guide-chromium/media/storage-cache-pane-cache-storage-resources.msft.png "Abbildung 2: Anwendungs Cache Bereich"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Offline-Webanwendungen – HTML-Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressourcen in einem Anwendungscache | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-Web-APIs | MDN"  

> [!NOTE]
> <span data-ttu-id="bd695-140">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd695-140">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bd695-141">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="bd695-141">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="bd695-143">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bd695-143">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

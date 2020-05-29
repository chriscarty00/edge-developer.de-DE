---
title: Anzeigen von Cache Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 82356777f209b86f88de1ee53b212947d969ff8a
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612074"
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





# <span data-ttu-id="0dab9-103">Anzeigen von Cache Daten mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="0dab9-103">View Cache Data With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="0dab9-104">Dieser Leitfaden zeigt, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um [Cache][MDNCache] Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0dab9-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="0dab9-105">Wenn Sie versuchen, http- [Cache][MDNHTTPCaching] -Daten zu überprüfen, ist dies nicht die gewünschte Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="0dab9-105">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  
<span data-ttu-id="0dab9-106">Suchen Sie in der Spalte **Größe** des **Netzwerkprotokolls**nach den Informationen.</span><span class="sxs-lookup"><span data-stu-id="0dab9-106">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="0dab9-107">Siehe [Protokoll Netzwerkaktivität][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="0dab9-107">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="0dab9-108">Anzeigen von Cachedaten</span><span class="sxs-lookup"><span data-stu-id="0dab9-108">View cache data</span></span>   

1.  <span data-ttu-id="0dab9-109">Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0dab9-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="0dab9-110">Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0dab9-110">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="0dab9-111">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="0dab9-111">Figure 1</span></span>  
    > <span data-ttu-id="0dab9-112">Bereich ' Manifest '</span><span class="sxs-lookup"><span data-stu-id="0dab9-112">The Manifest pane</span></span>  
    > ![Bereich ' Manifest '][ImageManifestPane]  

1.  <span data-ttu-id="0dab9-114">Erweitern Sie den Abschnitt **Cache Speicher** , um verfügbare Caches anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0dab9-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    > ##### <span data-ttu-id="0dab9-115">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="0dab9-115">Figure 2</span></span>  
    > <span data-ttu-id="0dab9-116">Verfügbare Caches</span><span class="sxs-lookup"><span data-stu-id="0dab9-116">Available caches</span></span>  
    > ![Verfügbare Caches][ImageCache]  

1.  <span data-ttu-id="0dab9-118">Wählen Sie einen Cache aus, um den Inhalt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0dab9-118">Select a cache to view the contents.</span></span>  
    
    > ##### <span data-ttu-id="0dab9-119">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="0dab9-119">Figure 3</span></span>  
    > <span data-ttu-id="0dab9-120">Anzeigen des Inhalts eines Caches</span><span class="sxs-lookup"><span data-stu-id="0dab9-120">Viewing the contents of a cache</span></span>  
    > ![Anzeigen des Inhalts eines Caches][ImageCacheView]  

1.  <span data-ttu-id="0dab9-122">Wählen Sie eine Ressource aus, um die HTTP-Header im Abschnitt unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0dab9-122">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    > ##### <span data-ttu-id="0dab9-123">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="0dab9-123">Figure 4</span></span>  
    > <span data-ttu-id="0dab9-124">Anzeigen der HTTP-Header einer Ressource</span><span class="sxs-lookup"><span data-stu-id="0dab9-124">Viewing the HTTP headers of a resource</span></span>  
    > ![Anzeigen der HTTP-Header einer Ressource][ImageViewCacheResource]  

1.  <span data-ttu-id="0dab9-126">Wählen Sie **Vorschau** aus, um den Inhalt einer Ressource anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0dab9-126">Select **Preview** to view the content of a resource.</span></span>  
    
    > ##### <span data-ttu-id="0dab9-127">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="0dab9-127">Figure 5</span></span>  
    > <span data-ttu-id="0dab9-128">Anzeigen des Inhalts einer Ressource</span><span class="sxs-lookup"><span data-stu-id="0dab9-128">Viewing the content of a resource</span></span>  
    > ![Anzeigen des Inhalts einer Ressource][ImageCacheContent]  

## <span data-ttu-id="0dab9-130">Aktualisieren einer Ressource</span><span class="sxs-lookup"><span data-stu-id="0dab9-130">Refresh a resource</span></span>   

1.  <span data-ttu-id="0dab9-131">[Anzeigen der Daten für einen Cache](#view-cache-data)</span><span class="sxs-lookup"><span data-stu-id="0dab9-131">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="0dab9-132">Wählen Sie die Ressource aus, die Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0dab9-132">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="0dab9-133">DevTools hebt die Markierung hervor, um anzugeben, dass Sie markiert ist.</span><span class="sxs-lookup"><span data-stu-id="0dab9-133">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="0dab9-134">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="0dab9-134">Figure 6</span></span>  
    > <span data-ttu-id="0dab9-135">Auswählen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="0dab9-135">Selecting a resource</span></span>  
    > ![Auswählen einer Ressource][ImageCacheSelected]  

1.  <span data-ttu-id="0dab9-137">Wählen **Sie Aktualisierung aktualisieren aus** ![ ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="0dab9-137">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  

## <span data-ttu-id="0dab9-138">Filtern von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0dab9-138">Filter resources</span></span>   

1.  <span data-ttu-id="0dab9-139">[Anzeigen der Daten für einen Cache](#view-cache-data)</span><span class="sxs-lookup"><span data-stu-id="0dab9-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="0dab9-140">Verwenden Sie das Textfeld nach **Pfad filtern** , um alle Ressourcen zu filtern, die nicht dem von Ihnen bereitgestellten Pfad entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0dab9-140">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    > ##### <span data-ttu-id="0dab9-141">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="0dab9-141">Figure 7</span></span>  
    > <span data-ttu-id="0dab9-142">Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="0dab9-142">Filtering out resources that do not match the specified path</span></span>  
    > ![Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen][ImageCacheFilter]  

## <span data-ttu-id="0dab9-144">Löschen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="0dab9-144">Delete a resource</span></span>   

1.  <span data-ttu-id="0dab9-145">[Anzeigen der Daten für einen Cache](#view-cache-data)</span><span class="sxs-lookup"><span data-stu-id="0dab9-145">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="0dab9-146">Wählen Sie die Ressource aus, die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="0dab9-146">Select the resource that you want to delete.</span></span>  <span data-ttu-id="0dab9-147">DevTools hebt die Markierung hervor, um anzugeben, dass Sie markiert ist.</span><span class="sxs-lookup"><span data-stu-id="0dab9-147">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="0dab9-148">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="0dab9-148">Figure 8</span></span>  
    > <span data-ttu-id="0dab9-149">Auswählen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="0dab9-149">Selecting a resource</span></span>  
    > ![Auswählen einer Ressource][ImageCacheSelected2]  

1.  <span data-ttu-id="0dab9-151">Wählen Sie **ausgewählte** löschen ausgewählt löschen aus ![ ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="0dab9-151">Select **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="0dab9-152">Löschen aller Cachedaten</span><span class="sxs-lookup"><span data-stu-id="0dab9-152">Delete all cache data</span></span>   

1.  <span data-ttu-id="0dab9-153">Öffnen Sie die **Anwendung**  >  **Clear Storage**.</span><span class="sxs-lookup"><span data-stu-id="0dab9-153">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="0dab9-154">Stellen Sie sicher, dass das Kontrollkästchen **Cache Speicher** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0dab9-154">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="0dab9-155">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="0dab9-155">Figure 9</span></span>  
    > <span data-ttu-id="0dab9-156">Das Kontrollkästchen " **Cache Speicher** "</span><span class="sxs-lookup"><span data-stu-id="0dab9-156">The **Cache Storage** checkbox</span></span>  
    > ![Das Kontrollkästchen "Cache Speicher"][ImageCacheCheckbox]  

1.  <span data-ttu-id="0dab9-158">Wählen Sie **Website Daten löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="0dab9-158">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="0dab9-159">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="0dab9-159">Figure 10</span></span>  
    > <span data-ttu-id="0dab9-160">Schaltfläche " **Website Daten löschen** "</span><span class="sxs-lookup"><span data-stu-id="0dab9-160">The **Clear Site Data** button</span></span>  
    > ![Schaltfläche "Website Daten löschen"][ImageCacheClearSite]  

<!--  -->  



<!-- image links -->  

[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Abbildung 1: der Bereich "Manifest""  
[ImageCache]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage.msft.png "Abbildung 2: verfügbare Caches"  
[ImageCacheView]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-root-headers.msft.png "Abbildung 3: Anzeigen des Inhalts eines Caches"  
[ImageViewCacheResource]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-index-headers.msft.png "Abbildung 4: Anzeigen der HTTP-Header einer Ressource"  
[ImageCacheContent]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-js-preview.msft.png "Abbildung 5: Anzeigen des Inhalts einer Ressource"  
[ImageCacheSelected]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-refresh.msft.png "Abbildung 6: Auswählen einer Ressource"  
[ImageCacheFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-filter.msft.png "Abbildung 7: Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen"  
[ImageCacheSelected2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-delete-selected.msft.png "Abbildung 8: Auswählen einer Ressource"  
[ImageCacheCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox.msft.png "Abbildung 9: das Kontrollkästchen "Cache Speicher""  
[ImageCacheClearSite]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png "Abbildung 10: die Schaltfläche "Website Daten löschen""  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/network/index#log-network-activity  "Protokollieren von Netzwerkaktivitäten"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "HTTP-Caching | MDN"  

> [!NOTE]
> <span data-ttu-id="0dab9-176">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0dab9-176">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0dab9-177">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/cache) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="0dab9-177">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="0dab9-179">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0dab9-179">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
title: Anzeigen von Cache Daten mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 7e7b4326204ce10732972c89b70c966e4bb665fb
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983850"
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





# <span data-ttu-id="fc1cb-103">Anzeigen von Cachedaten mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="fc1cb-103">View cache data with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="fc1cb-104">Dieser Leitfaden zeigt, wie Sie [Microsoft Edge devtools][MicrosoftEdgeDevTools] verwenden, um [Cache][MDNCache] Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="fc1cb-105">Wenn Sie versuchen, http- [Cache][MDNHTTPCaching] -Daten zu überprüfen, ist dies nicht die gewünschte Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-105">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="fc1cb-106">Suchen Sie in der Spalte **Größe** des **Netzwerkprotokolls**nach den Informationen.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-106">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="fc1cb-107">Siehe [Protokoll Netzwerkaktivität][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="fc1cb-107">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="fc1cb-108">Anzeigen von Cachedaten</span><span class="sxs-lookup"><span data-stu-id="fc1cb-108">View cache data</span></span>   

1.  <span data-ttu-id="fc1cb-109">Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="fc1cb-110">Der Bereich **Manifest** wird normalerweise standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-110">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="fc1cb-112">Bereich ' **Manifest** '</span><span class="sxs-lookup"><span data-stu-id="fc1cb-112">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fc1cb-113">Erweitern Sie den Abschnitt **Cache Speicher** , um verfügbare Caches anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-113">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Verfügbare Caches" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="fc1cb-115">Verfügbare Caches</span><span class="sxs-lookup"><span data-stu-id="fc1cb-115">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fc1cb-116">Wählen Sie einen Cache aus, um den Inhalt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-116">Select a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Anzeigen des Inhalts eines Caches" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="fc1cb-118">Anzeigen des Inhalts eines Caches</span><span class="sxs-lookup"><span data-stu-id="fc1cb-118">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fc1cb-119">Wählen Sie eine Ressource aus, um die HTTP-Header im Abschnitt unterhalb der Tabelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-119">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Anzeigen der HTTP-Header einer Ressource" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="fc1cb-121">Anzeigen der HTTP-Header einer Ressource</span><span class="sxs-lookup"><span data-stu-id="fc1cb-121">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fc1cb-122">Wählen Sie **Vorschau** aus, um den Inhalt einer Ressource anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-122">Select **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Anzeigen des Inhalts einer Ressource" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="fc1cb-124">Anzeigen des Inhalts einer Ressource</span><span class="sxs-lookup"><span data-stu-id="fc1cb-124">View the content of a resource</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="fc1cb-125">Aktualisieren einer Ressource</span><span class="sxs-lookup"><span data-stu-id="fc1cb-125">Refresh a resource</span></span>   

1.  <span data-ttu-id="fc1cb-126">[Anzeigen der Daten für einen Cache](#view-cache-data)</span><span class="sxs-lookup"><span data-stu-id="fc1cb-126">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="fc1cb-127">Wählen Sie die Ressource aus, die Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-127">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="fc1cb-128">DevTools hebt die Markierung hervor, um anzugeben, dass Sie markiert ist.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-128">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Auswählen einer Ressource" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="fc1cb-130">Auswählen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="fc1cb-130">Select a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fc1cb-131">Wählen Sie **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-131">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="fc1cb-132">Filtern von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fc1cb-132">Filter resources</span></span>   

1.  <span data-ttu-id="fc1cb-133">[Anzeigen der Daten für einen Cache](#view-cache-data)</span><span class="sxs-lookup"><span data-stu-id="fc1cb-133">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="fc1cb-134">Verwenden Sie das Textfeld nach **Pfad filtern** , um alle Ressourcen zu filtern, die nicht dem von Ihnen bereitgestellten Pfad entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-134">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="fc1cb-136">Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="fc1cb-136">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="fc1cb-137">Löschen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="fc1cb-137">Delete a resource</span></span>   

1.  <span data-ttu-id="fc1cb-138">[Anzeigen der Daten für einen Cache](#view-cache-data)</span><span class="sxs-lookup"><span data-stu-id="fc1cb-138">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="fc1cb-139">Wählen Sie die Ressource aus, die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-139">Select the resource that you want to delete.</span></span>  <span data-ttu-id="fc1cb-140">DevTools hebt die Markierung hervor, um anzugeben, dass Sie markiert ist.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-140">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Auswählen einer Ressource" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="fc1cb-142">Auswählen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="fc1cb-142">Select a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fc1cb-143">Wählen Sie " **Ausgewählte löschen** " aus ![ ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="fc1cb-143">Select **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="fc1cb-144">Löschen aller Cachedaten</span><span class="sxs-lookup"><span data-stu-id="fc1cb-144">Delete all cache data</span></span>   

1.  <span data-ttu-id="fc1cb-145">Öffnen Sie die **Anwendung**  >  **Clear Storage**.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-145">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="fc1cb-146">Stellen Sie sicher, dass das Kontrollkästchen **Cache Speicher** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-146">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Das Kontrollkästchen "Cache Speicher"" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="fc1cb-148">Das Kontrollkästchen " **Cache Speicher** "</span><span class="sxs-lookup"><span data-stu-id="fc1cb-148">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fc1cb-149">Wählen Sie **Website Daten löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-149">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Schaltfläche "Website Daten löschen"" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="fc1cb-151">Schaltfläche " **Website Daten löschen** "</span><span class="sxs-lookup"><span data-stu-id="fc1cb-151">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
<!--  
  


-->  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Protokoll Netzwerkaktivität | Microsoft docs"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "HTTP-Caching | MDN"  

> [!NOTE]
> <span data-ttu-id="fc1cb-156">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-156">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fc1cb-157">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/cache) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc1cb-157">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="fc1cb-159">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fc1cb-159">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

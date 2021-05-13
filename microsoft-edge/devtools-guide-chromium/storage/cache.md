---
description: Anzeigen von Cachedaten aus dem Anwendungsbereich von Microsoft Edge DevTools.
title: Anzeigen von Cachedaten mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 1f66419014682a316fa565c5ef2ab704f652637f
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564686"
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
# <a name="view-cache-data-with-microsoft-edge-devtools"></a><span data-ttu-id="48ba8-104">Anzeigen von Cachedaten mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="48ba8-104">View cache data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="48ba8-105">In diesem Handbuch erfahren Sie, wie Sie [Microsoft Edge DevTools verwenden,][MicrosoftEdgeDevTools] um [Cachedaten zu][MDNCache] überprüfen.</span><span class="sxs-lookup"><span data-stu-id="48ba8-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="48ba8-106">Wenn Sie versuchen, HTTP-Cachedaten [zu][MDNHTTPCaching] überprüfen, ist dies nicht die von Ihnen personenbezogene Anleitung.</span><span class="sxs-lookup"><span data-stu-id="48ba8-106">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="48ba8-107">Suchen Sie in der Spalte **Größe** des Netzwerkprotokolls **nach den Informationen.**</span><span class="sxs-lookup"><span data-stu-id="48ba8-107">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="48ba8-108">Navigieren Sie zu [Netzwerkaktivität protokollieren.][DevtoolsNetworkLogActivity]</span><span class="sxs-lookup"><span data-stu-id="48ba8-108">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <a name="view-cache-data"></a><span data-ttu-id="48ba8-109">Anzeigen von Cachedaten</span><span class="sxs-lookup"><span data-stu-id="48ba8-109">View cache data</span></span>  

1.  <span data-ttu-id="48ba8-110">Wählen Sie die **Registerkarte Anwendung** aus, um den Bereich **Anwendung zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="48ba8-110">Choose the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="48ba8-111">Der **Manifestbereich** wird in der Regel standardmäßig geöffnet.</span><span class="sxs-lookup"><span data-stu-id="48ba8-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="48ba8-113">Der **Manifestbereich**</span><span class="sxs-lookup"><span data-stu-id="48ba8-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="48ba8-114">Erweitern Sie den **Abschnitt Cache Storage,** um verfügbare Caches anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="48ba8-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Verfügbare Caches" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="48ba8-116">Verfügbare Caches</span><span class="sxs-lookup"><span data-stu-id="48ba8-116">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="48ba8-117">Wählen Sie einen Cache aus, um den Inhalt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="48ba8-117">Choose a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Anzeigen des Inhalts eines Caches" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="48ba8-119">Anzeigen des Inhalts eines Caches</span><span class="sxs-lookup"><span data-stu-id="48ba8-119">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="48ba8-120">Wählen Sie eine Ressource aus, um die HTTP-Header im Abschnitt unterhalb der Tabelle anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="48ba8-120">Choose a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Anzeigen der HTTP-Header einer Ressource" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="48ba8-122">Anzeigen der HTTP-Header einer Ressource</span><span class="sxs-lookup"><span data-stu-id="48ba8-122">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="48ba8-123">Wählen **Sie Vorschau** aus, um den Inhalt einer Ressource anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="48ba8-123">Choose **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Anzeigen des Inhalts einer Ressource" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="48ba8-125">Anzeigen des Inhalts einer Ressource</span><span class="sxs-lookup"><span data-stu-id="48ba8-125">View the content of a resource</span></span>  
    :::image-end:::  
    
## <a name="refresh-a-resource"></a><span data-ttu-id="48ba8-126">Aktualisieren einer Ressource</span><span class="sxs-lookup"><span data-stu-id="48ba8-126">Refresh a resource</span></span>  

1.  <span data-ttu-id="48ba8-127">[Anzeigen der Daten für einen Cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="48ba8-127">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="48ba8-128">Wählen Sie die Ressource aus, die Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="48ba8-128">Choose the resource that you want to refresh.</span></span>  <span data-ttu-id="48ba8-129">DevTools hebt es hervor, um anzugeben, dass es ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="48ba8-129">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Auswählen einer ressource, die aktualisiert werden soll" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="48ba8-131">Auswählen einer ressource, die aktualisiert werden soll</span><span class="sxs-lookup"><span data-stu-id="48ba8-131">Choose a resource to refresh</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="48ba8-132">Wählen **Sie Aktualisieren** \( Aktualisieren ![ ](../media/refresh-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="48ba8-132">Choose **Refresh** \(![Refresh](../media/refresh-icon.msft.png)\).</span></span>  
    
## <a name="filter-resources"></a><span data-ttu-id="48ba8-133">Filtern von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="48ba8-133">Filter resources</span></span>  

1.  <span data-ttu-id="48ba8-134">[Anzeigen der Daten für einen Cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="48ba8-134">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="48ba8-135">Verwenden Sie **das Textfeld Nach Pfad** filtern, um Ressourcen herausfiltern, die nicht mit dem von Ihnen zur Verfügung stellten Pfad übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="48ba8-135">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="48ba8-137">Filtern von Ressourcen, die nicht mit dem angegebenen Pfad übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="48ba8-137">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <a name="delete-a-resource"></a><span data-ttu-id="48ba8-138">Löschen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="48ba8-138">Delete a resource</span></span>  

1.  <span data-ttu-id="48ba8-139">[Anzeigen der Daten für einen Cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="48ba8-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="48ba8-140">Wählen Sie die Ressource aus, die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="48ba8-140">Choose the resource that you want to delete.</span></span>  <span data-ttu-id="48ba8-141">DevTools hebt es hervor, um anzugeben, dass es ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="48ba8-141">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Auswählen einer zu löschende Ressource" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="48ba8-143">Auswählen einer zu löschende Ressource</span><span class="sxs-lookup"><span data-stu-id="48ba8-143">Choose a resource to delete</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="48ba8-144">Wählen **Sie Ausgewählte \(** ![ Ausgewähltes Löschen ](../media/delete-icon.msft.png) \) löschen aus.</span><span class="sxs-lookup"><span data-stu-id="48ba8-144">Choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
## <a name="delete-all-cache-data"></a><span data-ttu-id="48ba8-145">Löschen aller Cachedaten</span><span class="sxs-lookup"><span data-stu-id="48ba8-145">Delete all cache data</span></span>  

1.  <span data-ttu-id="48ba8-146">Öffnen **Sie Application**Clear  >  **Storage**.</span><span class="sxs-lookup"><span data-stu-id="48ba8-146">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="48ba8-147">Stellen Sie sicher, dass **Storage** Cache aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="48ba8-147">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Das Kontrollkästchen Storage Cache" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="48ba8-149">Das **Kontrollkästchen Storage** Cache</span><span class="sxs-lookup"><span data-stu-id="48ba8-149">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="48ba8-150">Wählen **Sie Websitedaten löschen aus.**</span><span class="sxs-lookup"><span data-stu-id="48ba8-150">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Die Schaltfläche Websitedaten löschen" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="48ba8-152">Die **Schaltfläche Websitedaten** löschen</span><span class="sxs-lookup"><span data-stu-id="48ba8-152">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="48ba8-153">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="48ba8-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Protokollieren von Netzwerkaktivitäts| Microsoft Docs"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "HTTP-Zwischenspeicherung | MDN"  

> [!NOTE]
> <span data-ttu-id="48ba8-158">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48ba8-158">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="48ba8-159">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/cache) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="48ba8-159">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="48ba8-161">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="48ba8-161">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

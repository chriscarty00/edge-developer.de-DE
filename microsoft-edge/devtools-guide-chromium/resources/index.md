---
description: Organisieren Sie Ressourcen nach Frame, Domäne, Typ oder anderen Kriterien.
title: Anzeigen von Seitenressourcen mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 4f90927cc4044c722d9a62ab4b0427aa2753e4c5
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993590"
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





# <span data-ttu-id="512a4-104">Anzeigen von Seitenressourcen mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="512a4-104">View page resources with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="512a4-105">In diesem Leitfaden lernen Sie, wie Sie Microsoft Edge devtools verwenden, um die Ressourcen einer Webseite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="512a4-105">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="512a4-106">Ressourcen sind die Dateien, die eine Seite benötigt, um ordnungsgemäß angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="512a4-106">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="512a4-107">Beispiele für Ressourcen sind CSS-, JavaScript-und HTML-Dateien sowie Bilder.</span><span class="sxs-lookup"><span data-stu-id="512a4-107">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="512a4-108">In diesem Leitfaden wird davon ausgegangen, dass Sie mit den Grundlagen der [Webentwicklung][MDNLearnWebDevelopment] und der [Microsoft Edge-devtools][MicrosoftEdgeDevTools]vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="512a4-108">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="512a4-109">Öffnen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="512a4-109">Open resources</span></span>   

<span data-ttu-id="512a4-110">Wenn Sie den Namen der Ressource kennen, die Sie überprüfen möchten, bietet das **Befehlsmenü** eine schnelle Möglichkeit zum Öffnen der Ressource.</span><span class="sxs-lookup"><span data-stu-id="512a4-110">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="512a4-111">Drücken Sie `Control` + `P` \ (Windows \) oder `Command` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="512a4-111">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="512a4-112">Das Dialogfeld **Datei öffnen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="512a4-112">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="512a4-114">Dialogfeld ' **Datei öffnen** '</span><span class="sxs-lookup"><span data-stu-id="512a4-114">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="512a4-115">Wählen Sie die Datei aus der Dropdownliste aus, oder geben Sie den Dateinamen ein, und drücken Sie `Enter` im Feld AutoVervollständigen, sobald die richtige Datei hervorgehoben ist.</span><span class="sxs-lookup"><span data-stu-id="512a4-115">Select the file from the dropdown, or start typing the filename and press `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Geben Sie im Dialogfeld "Datei öffnen" einen Dateinamen ein." lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="512a4-117">Geben Sie im Dialogfeld " **Datei öffnen** " einen Dateinamen ein.</span><span class="sxs-lookup"><span data-stu-id="512a4-117">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="512a4-118">Öffnen von Ressourcen im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="512a4-118">Open resources in the Network panel</span></span>   

<span data-ttu-id="512a4-119">Weitere Informationen finden Sie unter [Überprüfen der Details einer Ressource][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="512a4-119">See [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Überprüfen einer Ressource im Netzwerk Panel" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="512a4-121">Überprüfen einer Ressource im **Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="512a4-121">Inspect a resource in the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="512a4-122">Anzeigen von Ressourcen im Netzwerk Panel von anderen Panels</span><span class="sxs-lookup"><span data-stu-id="512a4-122">Reveal resources in the Network panel from other panels</span></span>   

<span data-ttu-id="512a4-123">Im Abschnitt [Ressourcen durchsuchen](#browse-resources) wird gezeigt, wie Sie Ressourcen aus verschiedenen Teilen der devtools-Benutzeroberfläche anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="512a4-123">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="512a4-124">Wenn Sie jemals eine Ressource im **Netzwerk** Panel überprüfen möchten, klicken Sie mit der rechten Maustaste auf die Ressource, und wählen Sie **in der Netzwerksteuerung**anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="512a4-124">If you ever want to inspect a resource in the **Network** panel, right-click the resource and select **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Im Netzwerk Panel anzeigen" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="512a4-126">Im Netzwerk Panel anzeigen</span><span class="sxs-lookup"><span data-stu-id="512a4-126">Reveal in Network panel</span></span>**  
:::image-end:::  

## <span data-ttu-id="512a4-127">Ressourcen durchsuchen</span><span class="sxs-lookup"><span data-stu-id="512a4-127">Browse resources</span></span>   

### <span data-ttu-id="512a4-128">Durchsuchen von Ressourcen im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="512a4-128">Browse resources in the Network panel</span></span>   

<span data-ttu-id="512a4-129">Siehe [Protokoll Netzwerkaktivität][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="512a4-129">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Seitenressourcen im Netzwerkprotokoll" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="512a4-131">Seitenressourcen im **Netzwerk** Protokoll</span><span class="sxs-lookup"><span data-stu-id="512a4-131">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <span data-ttu-id="512a4-132">Durchsuchen nach Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="512a4-132">Browse by directory</span></span>   

<span data-ttu-id="512a4-133">So zeigen Sie die Ressourcen einer Seite an, die nach Verzeichnis geordnet ist:</span><span class="sxs-lookup"><span data-stu-id="512a4-133">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="512a4-134">Klicken Sie auf die Registerkarte **Quellen** , um das **Quellen** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="512a4-134">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="512a4-135">Klicken Sie auf das **Seiten** Register, um die Ressourcen der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="512a4-135">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="512a4-136">Der **Seiten** Bereich wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="512a4-136">The **Page** pane opens.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Seitenbereich" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="512a4-138">**Seiten** Bereich</span><span class="sxs-lookup"><span data-stu-id="512a4-138">The **Page** pane</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="512a4-139">Nachfolgend finden Sie eine Aufschlüsselung der nicht offensichtlichen Elemente in der vorherigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="512a4-139">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="512a4-140">Seitenelement</span><span class="sxs-lookup"><span data-stu-id="512a4-140">Page item</span></span> | <span data-ttu-id="512a4-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="512a4-141">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="512a4-142">Der Haupt Kontext des Dokument [Browsers][MDNInlineFrame]</span><span class="sxs-lookup"><span data-stu-id="512a4-142">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="512a4-143">Die Domäne.</span><span class="sxs-lookup"><span data-stu-id="512a4-143">The domain.</span></span>  <span data-ttu-id="512a4-144">Alle darunter geschachtelten Ressourcen stammen aus dieser Domäne.</span><span class="sxs-lookup"><span data-stu-id="512a4-144">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="512a4-145">Beispielsweise ist die vollständige URL der `comlink.global.j` Datei wahrscheinlich `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="512a4-145">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="512a4-146">Ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="512a4-146">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="512a4-147">Das HTML-Hauptdokument.</span><span class="sxs-lookup"><span data-stu-id="512a4-147">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="512a4-148">Ein Service Worker-Laufzeitkontext.</span><span class="sxs-lookup"><span data-stu-id="512a4-148">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="512a4-149">Klicken Sie auf eine Ressource, um Sie im **Editor**anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="512a4-149">Click a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Anzeigen einer Datei im Editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="512a4-151">Anzeigen einer Datei im **Editor**</span><span class="sxs-lookup"><span data-stu-id="512a4-151">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="512a4-152">Nach Dateiname suchen</span><span class="sxs-lookup"><span data-stu-id="512a4-152">Browse by filename</span></span>   

<span data-ttu-id="512a4-153">Standardmäßig werden im **Seiten** Bereich Ressourcen nach Verzeichnis gruppiert.</span><span class="sxs-lookup"><span data-stu-id="512a4-153">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="512a4-154">So deaktivieren Sie diese Gruppierung und zeigen die Ressourcen für jede Domäne als flache Liste an:</span><span class="sxs-lookup"><span data-stu-id="512a4-154">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="512a4-155">Öffnen des **Seiten** Bereichs</span><span class="sxs-lookup"><span data-stu-id="512a4-155">Open the **Page** pane.</span></span>  <span data-ttu-id="512a4-156">Siehe [Verzeichnis durchsuchen](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="512a4-156">See [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="512a4-157">Klicken Sie auf **Weitere Optionen** `...` , und deaktivieren Sie " **Gruppieren nach"**.</span><span class="sxs-lookup"><span data-stu-id="512a4-157">Click **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Die Option "Gruppieren nach"" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="512a4-159">Die Option **"Gruppieren nach"**</span><span class="sxs-lookup"><span data-stu-id="512a4-159">The **Group By Folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="512a4-160">Ressourcen sind nach Dateityp geordnet.</span><span class="sxs-lookup"><span data-stu-id="512a4-160">Resources are organized by file type.</span></span>  <span data-ttu-id="512a4-161">Innerhalb der einzelnen Dateitypen werden die Ressourcen alphabetisch geordnet.</span><span class="sxs-lookup"><span data-stu-id="512a4-161">Within each file type the resources are organized alphabetically.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Seitenbereich nach Deaktivierung des Ordners "Gruppieren nach"" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="512a4-163">**Seiten** Bereich nach Deaktivierung des **Ordners "Gruppieren nach"**</span><span class="sxs-lookup"><span data-stu-id="512a4-163">The **Page** pane after disabling **Group By Folder**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="512a4-164">Nach Dateityp suchen</span><span class="sxs-lookup"><span data-stu-id="512a4-164">Browse by file type</span></span>   

<span data-ttu-id="512a4-165">So gruppieren Sie Ressourcen basierend auf Ihrem Dateityp zusammen:</span><span class="sxs-lookup"><span data-stu-id="512a4-165">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="512a4-166">Klicken Sie auf die Registerkarte **Anwendung** .  Das **Anwendungs** Fenster wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="512a4-166">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="512a4-167">Standardmäßig wird der Bereich **Manifest** in der Regel zuerst geöffnet.</span><span class="sxs-lookup"><span data-stu-id="512a4-167">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Anwendungs Panel" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="512a4-169">**Anwendungs** Panel</span><span class="sxs-lookup"><span data-stu-id="512a4-169">The **Application** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="512a4-170">Scrollen Sie nach unten zum Bereich **Frames** .</span><span class="sxs-lookup"><span data-stu-id="512a4-170">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Der Bereich "Frames"" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="512a4-172">Der Bereich " **Frames** "</span><span class="sxs-lookup"><span data-stu-id="512a4-172">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="512a4-173">Erweitern Sie die Abschnitte, an denen Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="512a4-173">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="512a4-174">Klicken Sie auf eine Ressource, um Sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="512a4-174">Click a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Anzeigen einer Ressource im Anwendungs Panel" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="512a4-176">Anzeigen einer Ressource im **Anwendungs** Panel</span><span class="sxs-lookup"><span data-stu-id="512a4-176">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="512a4-177">Dateien nach Typ im Netzwerk Panel durchsuchen</span><span class="sxs-lookup"><span data-stu-id="512a4-177">Browse files by type in the Network panel</span></span>   

<span data-ttu-id="512a4-178">Siehe [Filtern nach Ressourcentyp][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="512a4-178">See [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtern nach CSS im Netzwerkprotokoll" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="512a4-180">Filtern nach CSS im **Netzwerk** Protokoll</span><span class="sxs-lookup"><span data-stu-id="512a4-180">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

<!--  
  


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Nach Ressourcentyp Filtern – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Überprüfen Sie die Details der Ressource – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Protokollieren von Netzwerkaktivitäten – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<IFRAME->: das Inline Frame-Element | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Web-Entwicklung kennenlernen | MDN"  

> [!NOTE]
> <span data-ttu-id="512a4-187">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="512a4-187">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="512a4-188">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/resources/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="512a4-188">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="512a4-190">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="512a4-190">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

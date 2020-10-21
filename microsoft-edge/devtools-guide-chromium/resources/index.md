---
description: Organisieren Sie Ressourcen nach Frame, Domäne, Typ oder anderen Kriterien.
title: Anzeigen von Seitenressourcen mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: a243a400dd85b587a8f299a6b8bc3d3d463796b0
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125398"
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

# <span data-ttu-id="0da6f-104">Anzeigen von Seitenressourcen mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="0da6f-104">View page resources with Microsoft Edge DevTools</span></span>  

  

<span data-ttu-id="0da6f-105">In diesem Leitfaden lernen Sie, wie Sie Microsoft Edge devtools verwenden, um die Ressourcen einer Webseite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0da6f-105">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="0da6f-106">Ressourcen sind die Dateien, die eine Seite benötigt, um ordnungsgemäß angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="0da6f-106">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="0da6f-107">Beispiele für Ressourcen sind CSS-, JavaScript-und HTML-Dateien sowie Bilder.</span><span class="sxs-lookup"><span data-stu-id="0da6f-107">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="0da6f-108">In diesem Leitfaden wird davon ausgegangen, dass Sie mit den Grundlagen der [Webentwicklung][MDNLearnWebDevelopment] und der [Microsoft Edge-devtools][MicrosoftEdgeDevTools]vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="0da6f-108">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="0da6f-109">Öffnen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0da6f-109">Open resources</span></span>  

<span data-ttu-id="0da6f-110">Wenn Sie den Namen der Ressource kennen, die Sie überprüfen möchten, bietet das **Befehlsmenü** eine schnelle Möglichkeit zum Öffnen der Ressource.</span><span class="sxs-lookup"><span data-stu-id="0da6f-110">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="0da6f-111">Wählen Sie `Control` + `P` \ (Windows, Linux \) oder `Command` + `P` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="0da6f-111">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="0da6f-112">Das Dialogfeld **Datei öffnen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0da6f-112">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="0da6f-114">Dialogfeld ' **Datei öffnen** '</span><span class="sxs-lookup"><span data-stu-id="0da6f-114">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0da6f-115">Wählen Sie die Datei aus der Dropdownliste aus, oder beginnen Sie mit der Eingabe des Datei namens, und wählen Sie `Enter` im Feld AutoVervollständigen die richtige Datei hervorgehoben aus.</span><span class="sxs-lookup"><span data-stu-id="0da6f-115">Select the file from the dropdown, or start typing the filename and select `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="0da6f-117">Geben Sie im Dialogfeld " **Datei öffnen** " einen Dateinamen ein.</span><span class="sxs-lookup"><span data-stu-id="0da6f-117">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="0da6f-118">Öffnen von Ressourcen im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="0da6f-118">Open resources in the Network panel</span></span>  

<span data-ttu-id="0da6f-119">Navigieren Sie, um [die Details einer Ressource zu überprüfen][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="0da6f-119">Navigate to [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="0da6f-121">Überprüfen einer Ressource im **Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="0da6f-121">Inspect a resource in the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="0da6f-122">Anzeigen von Ressourcen im Netzwerk Panel von anderen Panels</span><span class="sxs-lookup"><span data-stu-id="0da6f-122">Reveal resources in the Network panel from other panels</span></span>  

<span data-ttu-id="0da6f-123">Im Abschnitt [Ressourcen durchsuchen](#browse-resources) wird gezeigt, wie Sie Ressourcen aus verschiedenen Teilen der devtools-Benutzeroberfläche anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="0da6f-123">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="0da6f-124">Wenn Sie jemals eine Ressource im **Netzwerk** Panel überprüfen möchten, klicken Sie mit der rechten Maustaste auf die Ressource, und wählen Sie **im Netzwerk Panel**anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="0da6f-124">If you ever want to inspect a resource in the **Network** panel, right-click the resource and choose **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="0da6f-126">Im Netzwerk Panel anzeigen</span><span class="sxs-lookup"><span data-stu-id="0da6f-126">Reveal in Network panel</span></span>**  
:::image-end:::  

## <span data-ttu-id="0da6f-127">Ressourcen durchsuchen</span><span class="sxs-lookup"><span data-stu-id="0da6f-127">Browse resources</span></span>  

### <span data-ttu-id="0da6f-128">Durchsuchen von Ressourcen im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="0da6f-128">Browse resources in the Network panel</span></span>  

<span data-ttu-id="0da6f-129">Navigieren Sie zur [Protokoll Netzwerkaktivität][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="0da6f-129">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="0da6f-131">Seitenressourcen im **Netzwerk** Protokoll</span><span class="sxs-lookup"><span data-stu-id="0da6f-131">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <span data-ttu-id="0da6f-132">Durchsuchen nach Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="0da6f-132">Browse by directory</span></span>  

<span data-ttu-id="0da6f-133">So zeigen Sie die Ressourcen einer Seite an, die nach Verzeichnis geordnet ist:</span><span class="sxs-lookup"><span data-stu-id="0da6f-133">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="0da6f-134">Klicken Sie auf die Registerkarte **Quellen** , um das **Quellen** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0da6f-134">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="0da6f-135">Klicken Sie auf das **Seiten** Register, um die Ressourcen der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0da6f-135">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="0da6f-136">Der **Seiten** Bereich wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0da6f-136">The **Page** pane opens.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="0da6f-138">**Seiten** Bereich</span><span class="sxs-lookup"><span data-stu-id="0da6f-138">The **Page** pane</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="0da6f-139">Nachfolgend finden Sie eine Aufschlüsselung der nicht offensichtlichen Elemente in der vorherigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="0da6f-139">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="0da6f-140">Seitenelement</span><span class="sxs-lookup"><span data-stu-id="0da6f-140">Page item</span></span> | <span data-ttu-id="0da6f-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0da6f-141">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="0da6f-142">Der Haupt Kontext des Dokument [Browsers][MDNInlineFrame]</span><span class="sxs-lookup"><span data-stu-id="0da6f-142">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="0da6f-143">Die Domäne.</span><span class="sxs-lookup"><span data-stu-id="0da6f-143">The domain.</span></span>  <span data-ttu-id="0da6f-144">Alle darunter geschachtelten Ressourcen stammen aus dieser Domäne.</span><span class="sxs-lookup"><span data-stu-id="0da6f-144">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="0da6f-145">Beispielsweise ist die vollständige URL der `comlink.global.j` Datei wahrscheinlich `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="0da6f-145">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="0da6f-146">Ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="0da6f-146">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="0da6f-147">Das HTML-Hauptdokument.</span><span class="sxs-lookup"><span data-stu-id="0da6f-147">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="0da6f-148">Ein Service Worker-Laufzeitkontext.</span><span class="sxs-lookup"><span data-stu-id="0da6f-148">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="0da6f-149">Klicken Sie auf eine Ressource, um Sie im **Editor**anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0da6f-149">Click a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="0da6f-151">Anzeigen einer Datei im **Editor**</span><span class="sxs-lookup"><span data-stu-id="0da6f-151">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="0da6f-152">Nach Dateiname suchen</span><span class="sxs-lookup"><span data-stu-id="0da6f-152">Browse by filename</span></span>  

<span data-ttu-id="0da6f-153">Standardmäßig werden im **Seiten** Bereich Ressourcen nach Verzeichnis gruppiert.</span><span class="sxs-lookup"><span data-stu-id="0da6f-153">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="0da6f-154">So deaktivieren Sie diese Gruppierung und zeigen die Ressourcen für jede Domäne als flache Liste an:</span><span class="sxs-lookup"><span data-stu-id="0da6f-154">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="0da6f-155">Öffnen des **Seiten** Bereichs</span><span class="sxs-lookup"><span data-stu-id="0da6f-155">Open the **Page** pane.</span></span>  <span data-ttu-id="0da6f-156">Navigieren Sie nach [Verzeichnis durchsuchen](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="0da6f-156">Navigate to [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="0da6f-157">Wählen Sie **Weitere Optionen** aus `...` , und deaktivieren Sie " **Gruppieren nach"**.</span><span class="sxs-lookup"><span data-stu-id="0da6f-157">Choose **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="0da6f-159">Die Option **"Gruppieren nach"**</span><span class="sxs-lookup"><span data-stu-id="0da6f-159">The **Group By Folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="0da6f-160">Ressourcen sind nach Dateityp geordnet.</span><span class="sxs-lookup"><span data-stu-id="0da6f-160">Resources are organized by file type.</span></span>  <span data-ttu-id="0da6f-161">Innerhalb der einzelnen Dateitypen werden die Ressourcen alphabetisch geordnet.</span><span class="sxs-lookup"><span data-stu-id="0da6f-161">Within each file type the resources are organized alphabetically.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="0da6f-163">**Seiten** Bereich nach Deaktivierung des **Ordners "Gruppieren nach"**</span><span class="sxs-lookup"><span data-stu-id="0da6f-163">The **Page** pane after disabling **Group By Folder**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="0da6f-164">Nach Dateityp suchen</span><span class="sxs-lookup"><span data-stu-id="0da6f-164">Browse by file type</span></span>  

<span data-ttu-id="0da6f-165">So gruppieren Sie Ressourcen basierend auf Ihrem Dateityp zusammen:</span><span class="sxs-lookup"><span data-stu-id="0da6f-165">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="0da6f-166">Klicken Sie auf die Registerkarte **Anwendung** .  Das **Anwendungs** Fenster wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0da6f-166">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="0da6f-167">Standardmäßig wird der Bereich **Manifest** in der Regel zuerst geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0da6f-167">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="0da6f-169">**Anwendungs** Panel</span><span class="sxs-lookup"><span data-stu-id="0da6f-169">The **Application** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0da6f-170">Scrollen Sie nach unten zum Bereich **Frames** .</span><span class="sxs-lookup"><span data-stu-id="0da6f-170">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="0da6f-172">Der Bereich " **Frames** "</span><span class="sxs-lookup"><span data-stu-id="0da6f-172">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0da6f-173">Erweitern Sie die Abschnitte, an denen Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="0da6f-173">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="0da6f-174">Klicken Sie auf eine Ressource, um Sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0da6f-174">Click a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="0da6f-176">Anzeigen einer Ressource im **Anwendungs** Panel</span><span class="sxs-lookup"><span data-stu-id="0da6f-176">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="0da6f-177">Dateien nach Typ im Netzwerk Panel durchsuchen</span><span class="sxs-lookup"><span data-stu-id="0da6f-177">Browse files by type in the Network panel</span></span>  

<span data-ttu-id="0da6f-178">Navigieren Sie zu [Filter nach Ressourcentyp][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="0da6f-178">Navigate to [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Dialogfeld ' Datei öffnen '" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="0da6f-180">Filtern nach CSS im **Netzwerk** Protokoll</span><span class="sxs-lookup"><span data-stu-id="0da6f-180">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

## <span data-ttu-id="0da6f-181">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="0da6f-181">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Nach Ressourcentyp Filtern – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Überprüfen Sie die Details der Ressource – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Protokollieren von Netzwerkaktivitäten – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<IFRAME->: das Inline Frame-Element | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Web-Entwicklung kennenlernen | MDN"  

> [!NOTE]
> <span data-ttu-id="0da6f-188">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0da6f-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0da6f-189">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/resources/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="0da6f-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="0da6f-191">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0da6f-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

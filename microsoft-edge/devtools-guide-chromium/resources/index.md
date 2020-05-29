---
title: Anzeigen von Seitenressourcen mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 0977d0a9132c19742c3337f9dc0c3e1240508a3d
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611917"
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





# <span data-ttu-id="e119e-103">Anzeigen von Seitenressourcen mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="e119e-103">View Page Resources With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="e119e-104">In diesem Leitfaden lernen Sie, wie Sie Microsoft Edge devtools verwenden, um die Ressourcen einer Webseite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e119e-104">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="e119e-105">Ressourcen sind die Dateien, die eine Seite benötigt, um ordnungsgemäß angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="e119e-105">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="e119e-106">Beispiele für Ressourcen sind CSS-, JavaScript-und HTML-Dateien sowie Bilder.</span><span class="sxs-lookup"><span data-stu-id="e119e-106">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="e119e-107">In diesem Leitfaden wird davon ausgegangen, dass Sie mit den Grundlagen der [Webentwicklung][MDNLearnWebDevelopment] und der [Microsoft Edge-devtools][MicrosoftEdgeDevTools]vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="e119e-107">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="e119e-108">Öffnen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e119e-108">Open resources</span></span>   

<span data-ttu-id="e119e-109">Wenn Sie den Namen der Ressource kennen, die Sie überprüfen möchten, bietet das **Befehlsmenü** eine schnelle Möglichkeit zum Öffnen der Ressource.</span><span class="sxs-lookup"><span data-stu-id="e119e-109">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="e119e-110">Drücken Sie `Control` + `P` \ (Windows \) oder `Command` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="e119e-110">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="e119e-111">Das Dialogfeld **Datei öffnen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e119e-111">The **Open File** dialog opens.</span></span>  
    
    > ##### <span data-ttu-id="e119e-112">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="e119e-112">Figure 1</span></span>  
    > <span data-ttu-id="e119e-113">Dialogfeld ' **Datei öffnen** '</span><span class="sxs-lookup"><span data-stu-id="e119e-113">The **Open File** dialog</span></span>  
    > ![Dialogfeld ' Datei öffnen '][ImageOpenFile]  
    
1.  <span data-ttu-id="e119e-115">Wählen Sie die Datei aus der Dropdownliste aus, oder geben Sie den Dateinamen ein, und drücken Sie `Enter` im Feld AutoVervollständigen, sobald die richtige Datei hervorgehoben ist.</span><span class="sxs-lookup"><span data-stu-id="e119e-115">Select the file from the dropdown, or start typing the filename and press `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    > ##### <span data-ttu-id="e119e-116">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="e119e-116">Figure 2</span></span>  
    > <span data-ttu-id="e119e-117">Eingeben eines Datei namens im Dialogfeld " **Datei öffnen** "</span><span class="sxs-lookup"><span data-stu-id="e119e-117">Typing a filename in the **Open File** dialog</span></span>  
    > ![Eingeben eines Datei namens im Dialogfeld "Datei öffnen"][ImageFileSearch]  
    
### <span data-ttu-id="e119e-119">Öffnen von Ressourcen im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="e119e-119">Open resources in the Network panel</span></span>   

<span data-ttu-id="e119e-120">Weitere Informationen finden Sie unter [Überprüfen der Details einer Ressource][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="e119e-120">See [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

> ##### <span data-ttu-id="e119e-121">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="e119e-121">Figure 3</span></span>  
> <span data-ttu-id="e119e-122">Überprüfen einer Ressource im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="e119e-122">Inspecting a resource in the Network panel</span></span>  
> ![Überprüfen einer Ressource im Netzwerk Panel][ImageNetworkResponse]  

### <span data-ttu-id="e119e-124">Anzeigen von Ressourcen im Netzwerk Panel von anderen Panels</span><span class="sxs-lookup"><span data-stu-id="e119e-124">Reveal resources in the Network panel from other panels</span></span>   

<span data-ttu-id="e119e-125">Im Abschnitt [Ressourcen durchsuchen](#browse-resources) wird gezeigt, wie Sie Ressourcen aus verschiedenen Teilen der devtools-Benutzeroberfläche anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="e119e-125">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="e119e-126">Wenn Sie jemals eine Ressource im **Netzwerk** Panel überprüfen möchten, klicken Sie mit der rechten Maustaste auf die Ressource, und wählen Sie **in der Netzwerksteuerung**anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="e119e-126">If you ever want to inspect a resource in the **Network** panel, right-click the resource and select **Reveal in Network panel**.</span></span>  

> ##### <span data-ttu-id="e119e-127">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="e119e-127">Figure 4</span></span>  
> <span data-ttu-id="e119e-128">Die Option " **im Netzwerk anzeigen"**</span><span class="sxs-lookup"><span data-stu-id="e119e-128">The **Reveal in Network panel** option</span></span>  
> ![Im Netzwerk Panel anzeigen][ImageRevealNetwork]  

## <span data-ttu-id="e119e-130">Ressourcen durchsuchen</span><span class="sxs-lookup"><span data-stu-id="e119e-130">Browse resources</span></span>   

### <span data-ttu-id="e119e-131">Durchsuchen von Ressourcen im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="e119e-131">Browse resources in the Network panel</span></span>   

<span data-ttu-id="e119e-132">Siehe [Protokoll Netzwerkaktivität][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="e119e-132">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

> ##### <span data-ttu-id="e119e-133">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="e119e-133">Figure 5</span></span>  
> <span data-ttu-id="e119e-134">Seitenressourcen im Netzwerkprotokoll</span><span class="sxs-lookup"><span data-stu-id="e119e-134">Page resources in the Network Log</span></span>  
> ![Seitenressourcen im Netzwerkprotokoll][ImageNetworkLog]  

### <span data-ttu-id="e119e-136">Durchsuchen nach Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="e119e-136">Browse by directory</span></span>   

<span data-ttu-id="e119e-137">So zeigen Sie die Ressourcen einer Seite an, die nach Verzeichnis geordnet ist:</span><span class="sxs-lookup"><span data-stu-id="e119e-137">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="e119e-138">Klicken Sie auf die Registerkarte **Quellen** , um das **Quellen** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e119e-138">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="e119e-139">Klicken Sie auf das **Seiten** Register, um die Ressourcen der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e119e-139">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="e119e-140">Der **Seiten** Bereich wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e119e-140">The **Page** pane opens.</span></span>  
    
    > ##### <span data-ttu-id="e119e-141">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="e119e-141">Figure 6</span></span>  
    > <span data-ttu-id="e119e-142">**Seiten** Bereich</span><span class="sxs-lookup"><span data-stu-id="e119e-142">The **Page** pane</span></span>  
    > ![Seitenbereich][ImagePage]  
    
    <span data-ttu-id="e119e-144">Nachfolgend finden Sie eine Aufschlüsselung der nicht offensichtlichen Elemente in [Abbildung 6](#figure-6):</span><span class="sxs-lookup"><span data-stu-id="e119e-144">Here is a breakdown of the non-obvious items in [Figure 6](#figure-6):</span></span>  
    
    | <span data-ttu-id="e119e-145">Seitenelement</span><span class="sxs-lookup"><span data-stu-id="e119e-145">Page item</span></span> | <span data-ttu-id="e119e-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e119e-146">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="e119e-147">Der Haupt Kontext des Dokument [Browsers][MDNInlineFrame]</span><span class="sxs-lookup"><span data-stu-id="e119e-147">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="e119e-148">Die Domäne.</span><span class="sxs-lookup"><span data-stu-id="e119e-148">The domain.</span></span>  <span data-ttu-id="e119e-149">Alle darunter geschachtelten Ressourcen stammen aus dieser Domäne.</span><span class="sxs-lookup"><span data-stu-id="e119e-149">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="e119e-150">Beispielsweise ist die vollständige URL der `comlink.global.j` Datei wahrscheinlich `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="e119e-150">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="e119e-151">Ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e119e-151">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="e119e-152">Das HTML-Hauptdokument.</span><span class="sxs-lookup"><span data-stu-id="e119e-152">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="e119e-153">Ein Service Worker-Laufzeitkontext.</span><span class="sxs-lookup"><span data-stu-id="e119e-153">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="e119e-154">Klicken Sie auf eine Ressource, um Sie im **Editor**anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e119e-154">Click a resource to view it in the **Editor**.</span></span>  
    
    > ##### <span data-ttu-id="e119e-155">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="e119e-155">Figure 7</span></span>  
    > <span data-ttu-id="e119e-156">Anzeigen einer Datei im **Editor**</span><span class="sxs-lookup"><span data-stu-id="e119e-156">Viewing a file in the **Editor**</span></span>  
    > ![Anzeigen einer Datei im Editor][ImageSourcesView]  
    
### <span data-ttu-id="e119e-158">Nach Dateiname suchen</span><span class="sxs-lookup"><span data-stu-id="e119e-158">Browse by filename</span></span>   

<span data-ttu-id="e119e-159">Standardmäßig werden im **Seiten** Bereich Ressourcen nach Verzeichnis gruppiert.</span><span class="sxs-lookup"><span data-stu-id="e119e-159">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="e119e-160">So deaktivieren Sie diese Gruppierung und zeigen die Ressourcen für jede Domäne als flache Liste an:</span><span class="sxs-lookup"><span data-stu-id="e119e-160">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="e119e-161">Öffnen des **Seiten** Bereichs</span><span class="sxs-lookup"><span data-stu-id="e119e-161">Open the **Page** pane.</span></span>  <span data-ttu-id="e119e-162">Siehe [Verzeichnis durchsuchen](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="e119e-162">See [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="e119e-163">Klicken Sie auf **Weitere Optionen** `...` , und deaktivieren Sie " **Gruppieren nach"**.</span><span class="sxs-lookup"><span data-stu-id="e119e-163">Click **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    > ##### <span data-ttu-id="e119e-164">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="e119e-164">Figure 8</span></span>  
    > <span data-ttu-id="e119e-165">Die Option **"Gruppieren nach"**</span><span class="sxs-lookup"><span data-stu-id="e119e-165">The **Group By Folder** option</span></span>  
    > ![Die Option "Gruppieren nach"][ImageGroupByFolder]  
    
    <span data-ttu-id="e119e-167">Ressourcen sind nach Dateityp geordnet.</span><span class="sxs-lookup"><span data-stu-id="e119e-167">Resources are organized by file type.</span></span>  <span data-ttu-id="e119e-168">Innerhalb der einzelnen Dateitypen werden die Ressourcen alphabetisch geordnet.</span><span class="sxs-lookup"><span data-stu-id="e119e-168">Within each file type the resources are organized alphabetically.</span></span>  
    
    > ##### <span data-ttu-id="e119e-169">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="e119e-169">Figure 9</span></span>  
    > <span data-ttu-id="e119e-170">**Seiten** Bereich nach Deaktivierung des **Ordners "Gruppieren nach"**</span><span class="sxs-lookup"><span data-stu-id="e119e-170">The **Page** pane after disabling **Group By Folder**</span></span>  
    > ![Seitenbereich nach Deaktivierung des Ordners "Gruppieren nach"][ImageFileNames]  
    
### <span data-ttu-id="e119e-172">Nach Dateityp suchen</span><span class="sxs-lookup"><span data-stu-id="e119e-172">Browse by file type</span></span>   

<span data-ttu-id="e119e-173">So gruppieren Sie Ressourcen basierend auf Ihrem Dateityp zusammen:</span><span class="sxs-lookup"><span data-stu-id="e119e-173">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="e119e-174">Klicken Sie auf die Registerkarte **Anwendung** .  Das **Anwendungs** Fenster wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e119e-174">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="e119e-175">Standardmäßig wird der Bereich **Manifest** in der Regel zuerst geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e119e-175">By default the **Manifest** pane usually opens first.</span></span>  
    
    > ##### <span data-ttu-id="e119e-176">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="e119e-176">Figure 10</span></span>  
    > <span data-ttu-id="e119e-177">**Anwendungs** Panel</span><span class="sxs-lookup"><span data-stu-id="e119e-177">The **Application** panel</span></span>  
    > ![Anwendungs Panel][ImageApplication]  
    
1.  <span data-ttu-id="e119e-179">Scrollen Sie nach unten zum Bereich **Frames** .</span><span class="sxs-lookup"><span data-stu-id="e119e-179">Scroll down to the **Frames** pane.</span></span>  
    
    > ##### <span data-ttu-id="e119e-180">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="e119e-180">Figure 11</span></span>  
    > <span data-ttu-id="e119e-181">Der Bereich " **Frames** "</span><span class="sxs-lookup"><span data-stu-id="e119e-181">The **Frames** pane</span></span>  
    > ![Der Bereich "Frames"][ImageFrames]  
    
1.  <span data-ttu-id="e119e-183">Erweitern Sie die Abschnitte, an denen Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="e119e-183">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="e119e-184">Klicken Sie auf eine Ressource, um Sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e119e-184">Click a resource to view it.</span></span>  
    
    > ##### <span data-ttu-id="e119e-185">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="e119e-185">Figure 12</span></span>  
    > <span data-ttu-id="e119e-186">Anzeigen einer Ressource im **Anwendungs** Panel</span><span class="sxs-lookup"><span data-stu-id="e119e-186">Viewing a resource in the **Application** panel</span></span>  
    > ![Anzeigen einer Ressource im Anwendungs Panel][ImageApplicationView]  

#### <span data-ttu-id="e119e-188">Dateien nach Typ im Netzwerk Panel durchsuchen</span><span class="sxs-lookup"><span data-stu-id="e119e-188">Browse files by type in the Network panel</span></span>   

<span data-ttu-id="e119e-189">Siehe [Filtern nach Ressourcentyp][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="e119e-189">See [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

> ##### <span data-ttu-id="e119e-190">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="e119e-190">Figure 13</span></span>  
> <span data-ttu-id="e119e-191">Filtern nach CSS im Netzwerkprotokoll</span><span class="sxs-lookup"><span data-stu-id="e119e-191">Filtering for CSS in the Network Log</span></span>  
> ![Filtern nach CSS im Netzwerkprotokoll][ImageCSS]  

<!--  -->  



<!-- image links -->  

[ImageOpenFile]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-empty.msft.png "Abbildung 1: Dialogfeld "Datei öffnen""  
[ImageFileSearch]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-file-search.msft.png "Abbildung 2: Eingeben eines Datei namens in das Dialogfeld "Datei öffnen""  
[ImageNetworkResponse]: /microsoft-edge/devtools-guide-chromium/media/resources-network-response.msft.png "Abbildung 3: Überprüfen einer Ressource im * * Netzwerk * *-Panel"  
[ImageRevealNetwork]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-reveal-in-network-panel.msft.png "Abbildung 4: Anzeigen in der Netzwerksteuerung"  
[ImageNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources.msft.png "Abbildung 5: Seitenressourcen im Netzwerkprotokoll"  
[ImagePage]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-empty.msft.png "Abbildung 6: der Seitenbereich"  
[ImageSourcesView]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource.msft.png "Abbildung 7: Anzeigen einer Datei im Editor"  
[ImageGroupByFolder]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource-group-by-folder.msft.png "Abbildung 8: die Option "Gruppieren nach""  
[ImageFileNames]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png "Abbildung 9: der Seitenbereich nach dem Deaktivieren des Ordners "Gruppieren nach""  
[ImageApplication]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner.msft.png "Abbildung 10: Anwendungs Panel"  
[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-frames-expanded.msft.png "Abbildung 11: der Bereich "Frames""  
[ImageApplicationView]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-expanded-resources.msft.png "Abbildung 12: Anzeigen einer Ressource im Anwendungs Panel"  
[ImageCSS]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources-filter-css.msft.png "Abbildung 13: Filtern nach CSS im Netzwerkprotokoll"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevtoolsNetworkFilterByResourceType]: /microsoft-edge/devtools-guide-chromium/network/index#filter-by-resource-type "Nach Ressourcentyp Filtern – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools"  
[DevtoolsNetworkInspectDetailsResource]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Überprüfen der Details der Ressource – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Protokollieren von Netzwerkaktivitäten – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<IFRAME->: das Inline Frame-Element | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Web-Entwicklung kennenlernen | MDN"  

> [!NOTE]
> <span data-ttu-id="e119e-212">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e119e-212">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e119e-213">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/resources/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e119e-213">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="e119e-215">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e119e-215">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

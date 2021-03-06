---
description: Organisieren Sie Ressourcen nach Frame, Domäne, Typ oder anderen Kriterien.
title: Anzeigen von Seitenressourcen mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 75063b23f23c25ff4fe2e7f6e044a2de9a7b1ccd
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398224"
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

# <a name="view-page-resources-with-microsoft-edge-devtools"></a><span data-ttu-id="25674-104">Anzeigen von Seitenressourcen mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="25674-104">View page resources with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="25674-105">In diesem Handbuch erfahren Sie, wie Sie Microsoft Edge DevTools zum Anzeigen der Ressourcen einer Webseite verwenden.</span><span class="sxs-lookup"><span data-stu-id="25674-105">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="25674-106">Ressourcen sind die Dateien, die eine Seite benötigt, um ordnungsgemäß angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="25674-106">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="25674-107">Beispiele für Ressourcen sind CSS-, JavaScript- und HTML-Dateien sowie Bilder.</span><span class="sxs-lookup"><span data-stu-id="25674-107">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="25674-108">In diesem Handbuch wird davon ausgegangen, [][MDNLearnWebDevelopment] dass Sie mit den Grundlagen der Webentwicklung und [Microsoft Edge DevTools vertraut sind.][MicrosoftEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="25674-108">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="open-resources"></a><span data-ttu-id="25674-109">Öffnen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="25674-109">Open resources</span></span>  

<span data-ttu-id="25674-110">Wenn Sie den Namen der Ressource kennen, die \*\*\*\* Sie überprüfen möchten, bietet das Befehlsmenü eine schnelle Möglichkeit zum Öffnen der Ressource.</span><span class="sxs-lookup"><span data-stu-id="25674-110">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="25674-111">Wählen `Control` + `P` Sie \(Windows, Linux\) oder `Command` + `P` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="25674-111">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="25674-112">Das **Dialogfeld Datei öffnen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="25674-112">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Dialogfeld Datei öffnen" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="25674-114">Dialogfeld **Datei** öffnen</span><span class="sxs-lookup"><span data-stu-id="25674-114">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="25674-115">Wählen Sie die Datei aus dem Dropdownmenü aus, oder beginnen Sie mit der Eingabe des Dateinamens, und wählen Sie aus, sobald die richtige Datei `Enter` im Feld autoComplete hervorgehoben ist.</span><span class="sxs-lookup"><span data-stu-id="25674-115">Choose the file from the dropdown, or start typing the filename and select `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Geben Sie einen Dateinamen im Dialogfeld Datei öffnen ein." lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="25674-117">Geben Sie einen Dateinamen im Dialogfeld **Datei öffnen** ein.</span><span class="sxs-lookup"><span data-stu-id="25674-117">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <a name="open-resources-in-the-network-tool"></a><span data-ttu-id="25674-118">Öffnen von Ressourcen im Netzwerktool</span><span class="sxs-lookup"><span data-stu-id="25674-118">Open resources in the Network tool</span></span>  

<span data-ttu-id="25674-119">Navigieren Sie zu [Überprüfen der Details einer Ressource][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="25674-119">Navigate to [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Überprüfen einer Ressource im Netzwerktool" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="25674-121">Überprüfen einer Ressource im **Netzwerktool**</span><span class="sxs-lookup"><span data-stu-id="25674-121">Inspect a resource in the **Network** tool</span></span>  
:::image-end:::  

### <a name="reveal-resources-in-the-network-tool-from-other-panels"></a><span data-ttu-id="25674-122">Aufschluss über Ressourcen im Netzwerktool in anderen Panels</span><span class="sxs-lookup"><span data-stu-id="25674-122">Reveal resources in the Network tool from other panels</span></span>  

<span data-ttu-id="25674-123">Im [Abschnitt Ressourcen durchsuchen](#browse-resources) unten erfahren Sie, wie Sie Ressourcen aus verschiedenen Teilen der DevTools-Benutzeroberfläche anzeigen.</span><span class="sxs-lookup"><span data-stu-id="25674-123">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="25674-124">Wenn Sie jemals eine Ressource \*\*\*\* im Netzwerktool überprüfen möchten, zeigen Sie auf die Ressource, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie Im Netzwerkbereich einblenden **aus.**</span><span class="sxs-lookup"><span data-stu-id="25674-124">If you ever want to inspect a resource in the **Network** tool,  hover on the resource, open the contextual menu \(right-click\), and choose **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Anzeige im Netzwerkbereich" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="25674-126">Anzeige im Netzwerkbereich</span><span class="sxs-lookup"><span data-stu-id="25674-126">Reveal in Network panel</span></span>**  
:::image-end:::  

## <a name="browse-resources"></a><span data-ttu-id="25674-127">Durchsuchen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="25674-127">Browse resources</span></span>  

### <a name="browse-resources-in-the-network-panel"></a><span data-ttu-id="25674-128">Durchsuchen von Ressourcen im Netzwerkbereich</span><span class="sxs-lookup"><span data-stu-id="25674-128">Browse resources in the Network panel</span></span>  

<span data-ttu-id="25674-129">Navigieren Sie zu [Netzwerkaktivität protokollieren.][DevtoolsNetworkLogActivity]</span><span class="sxs-lookup"><span data-stu-id="25674-129">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Seitenressourcen im Netzwerkprotokoll" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="25674-131">Seitenressourcen im **Netzwerkprotokoll**</span><span class="sxs-lookup"><span data-stu-id="25674-131">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <a name="browse-by-directory"></a><span data-ttu-id="25674-132">Durchsuchen nach Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="25674-132">Browse by directory</span></span>  

<span data-ttu-id="25674-133">So zeigen Sie die Ressourcen einer nach Verzeichnis organisierten Seite an:</span><span class="sxs-lookup"><span data-stu-id="25674-133">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="25674-134">Wählen Sie das **Tool Quellen** aus, um den Bereich **Quellen zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="25674-134">Choose the **Sources** tool to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="25674-135">Wählen Sie den **Bereich** Seite aus, um die Ressourcen der Seite anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="25674-135">Choose the **Page** panel to show the resources of the page.</span></span>  <span data-ttu-id="25674-136">Der **Bereich Seite** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="25674-136">The **Page** pane opens.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Seitenbereich" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="25674-138">**Seitenbereich**</span><span class="sxs-lookup"><span data-stu-id="25674-138">The **Page** panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="25674-139">Hier ist eine Aufschlüsselung der nicht offensichtlichen Elemente in der vorherigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="25674-139">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="25674-140">Seitenelement</span><span class="sxs-lookup"><span data-stu-id="25674-140">Page item</span></span> | <span data-ttu-id="25674-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25674-141">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="25674-142">Der Hauptkontext [für das Durchsuchen von Dokumenten][MDNInlineFrame].</span><span class="sxs-lookup"><span data-stu-id="25674-142">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="25674-143">Die Domäne.</span><span class="sxs-lookup"><span data-stu-id="25674-143">The domain.</span></span>  <span data-ttu-id="25674-144">Alle ressourcen, die unter ihr geschachtelt sind, stammen aus dieser Domäne.</span><span class="sxs-lookup"><span data-stu-id="25674-144">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="25674-145">Die vollständige URL der Datei ist z. B. `comlink.global.j` wahrscheinlich `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="25674-145">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="25674-146">Ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="25674-146">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="25674-147">Das Haupt-HTML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="25674-147">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="25674-148">Ein Laufzeitkontext eines Dienstarbeitsmitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="25674-148">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="25674-149">Wählen Sie eine Ressource aus, um sie im **Editor anzeigen zu können.**</span><span class="sxs-lookup"><span data-stu-id="25674-149">Choose a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Anzeigen einer Datei im Editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="25674-151">Anzeigen einer Datei im **Editor**</span><span class="sxs-lookup"><span data-stu-id="25674-151">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <a name="browse-by-filename"></a><span data-ttu-id="25674-152">Durchsuchen nach Dateiname</span><span class="sxs-lookup"><span data-stu-id="25674-152">Browse by filename</span></span>  

<span data-ttu-id="25674-153">Standardmäßig werden im **Seitenbereich** Ressourcen nach Verzeichnis gruppen.</span><span class="sxs-lookup"><span data-stu-id="25674-153">By default the **Page** panel groups resources by directory.</span></span>  <span data-ttu-id="25674-154">So deaktivieren Sie diese Gruppierung, und zeigen Sie die Ressourcen für jede Domäne als flache Liste an:</span><span class="sxs-lookup"><span data-stu-id="25674-154">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="25674-155">Öffnen Sie den **Seitenbereich.**</span><span class="sxs-lookup"><span data-stu-id="25674-155">Open the **Page** panel.</span></span>  <span data-ttu-id="25674-156">Navigieren Sie [zu Durchsuchen nach Verzeichnis](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="25674-156">Navigate to [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="25674-157">Wählen **Sie Weitere Optionen aus,** und deaktivieren Sie `...` **"Nach Ordner" gruppieren.**</span><span class="sxs-lookup"><span data-stu-id="25674-157">Choose **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Die Option "Gruppe nach Ordner"" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="25674-159">Die **Option "Gruppe nach Ordner"**</span><span class="sxs-lookup"><span data-stu-id="25674-159">The **Group By Folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="25674-160">Ressourcen sind nach Dateityp organisiert.</span><span class="sxs-lookup"><span data-stu-id="25674-160">Resources are organized by file type.</span></span>  <span data-ttu-id="25674-161">Innerhalb jedes Dateityps sind die Ressourcen alphabetisch angeordnet.</span><span class="sxs-lookup"><span data-stu-id="25674-161">Within each file type the resources are organized alphabetically.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Der Seitenbereich nach der Deaktivierung von "Gruppe nach Ordner"" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="25674-163">Der **Seitenbereich** nach der Deaktivierung **von "Gruppe nach Ordner"**</span><span class="sxs-lookup"><span data-stu-id="25674-163">The **Page** panel after disabling **Group By Folder**</span></span>  
    :::image-end:::  
    
### <a name="browse-by-file-type"></a><span data-ttu-id="25674-164">Durchsuchen nach Dateityp</span><span class="sxs-lookup"><span data-stu-id="25674-164">Browse by file type</span></span>  

<span data-ttu-id="25674-165">So gruppieren Sie Ressourcen basierend auf ihrem Dateityp:</span><span class="sxs-lookup"><span data-stu-id="25674-165">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="25674-166">Wählen Sie die **Registerkarte Anwendung** aus.  Das **Tool Anwendung** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="25674-166">Choose the **Application** tab.  The **Application** tool opens.</span></span>  <span data-ttu-id="25674-167">Standardmäßig wird der **Manifestbereich** in der Regel zuerst geöffnet.</span><span class="sxs-lookup"><span data-stu-id="25674-167">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Das Anwendungstool" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="25674-169">Das **Anwendungstool**</span><span class="sxs-lookup"><span data-stu-id="25674-169">The **Application** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="25674-170">Scrollen Sie \*\*\*\* nach unten zum Frames-Bereich.</span><span class="sxs-lookup"><span data-stu-id="25674-170">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Der Bereich Frames" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="25674-172">Der **Bereich Frames**</span><span class="sxs-lookup"><span data-stu-id="25674-172">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="25674-173">Erweitern Sie die Abschnitte, an denen Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="25674-173">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="25674-174">Wählen Sie eine Ressource aus, um sie anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="25674-174">Choose a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Anzeigen einer Ressource im Anwendungsbereich" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="25674-176">Anzeigen einer Ressource im **Anwendungsbereich**</span><span class="sxs-lookup"><span data-stu-id="25674-176">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <a name="browse-files-by-type-in-the-network-panel"></a><span data-ttu-id="25674-177">Durchsuchen von Dateien nach Typ im Netzwerkbereich</span><span class="sxs-lookup"><span data-stu-id="25674-177">Browse files by type in the Network panel</span></span>  

<span data-ttu-id="25674-178">Navigieren Sie [zu Filtern nach Ressourcentyp][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="25674-178">Navigate to [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtern nach CSS im Netzwerkprotokoll" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="25674-180">Filtern nach CSS im **Netzwerkprotokoll**</span><span class="sxs-lookup"><span data-stu-id="25674-180">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="25674-181">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="25674-181">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtern nach Ressourcentyp – Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspect the details of the resource - Inspect network activity in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Protokollnetzwerkaktivität – Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools | Microsoft Docs"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: Das Inlineframe-Element | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Erfahren Sie mehr über | MDN"  

> [!NOTE]
> <span data-ttu-id="25674-188">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25674-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="25674-189">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/resources/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="25674-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="25674-191">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="25674-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
description: Die neuesten experimentellen Features in Microsoft Edge DevTools
title: Experimentelle Funktionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, experiment
ms.openlocfilehash: b366cfeccafe874bc9e76d3b66659122c5d07c69
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398679"
---
# <a name="experimental-features"></a><span data-ttu-id="c8dab-104">Experimentelle Funktionen</span><span class="sxs-lookup"><span data-stu-id="c8dab-104">Experimental features</span></span>  

<span data-ttu-id="c8dab-105">Microsoft Edge DevTools bieten Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.</span><span class="sxs-lookup"><span data-stu-id="c8dab-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="c8dab-106">Sie können testen und [Feedback geben,](#providing-feedback-on-experimental-features) bevor jedes Feature veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="c8dab-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="c8dab-107">Obwohl experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, können Sie die neuesten experimentellen Features über den Microsoft Edge Canary-Kanal erhalten.</span><span class="sxs-lookup"><span data-stu-id="c8dab-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="c8dab-108">Aktivieren experimenteller Features</span><span class="sxs-lookup"><span data-stu-id="c8dab-108">Turn on experimental features</span></span>  

<span data-ttu-id="c8dab-109">Führen Sie die folgenden Schritte aus, um \(oder off\) experimentelle Features in Microsoft Edge zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c8dab-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="c8dab-110">[Öffnen Sie DevTools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="c8dab-110">[Open DevTools][DevtoolsOpenMain].</span></span>  
    *   <span data-ttu-id="c8dab-111">Wählen `Control` + `Shift` + `I` Sie \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="c8dab-112">Weitere Informationen finden Sie unter [Microsoft Edge DevTools-Tastenkombinationen.][DevToolsShortcuts]</span><span class="sxs-lookup"><span data-stu-id="c8dab-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="c8dab-113">Öffnen Sie den [Bereich][DevToolsCustomizeIndexSettings] Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="c8dab-114">Wählen Sie `Shift` + `?` aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="c8dab-115">Weitere Informationen finden Sie unter [Microsoft Edge DevTools-Tastenkombinationen.][DevToolsShortcuts]</span><span class="sxs-lookup"><span data-stu-id="c8dab-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="c8dab-116">Klicken Sie auf der linken Seite des **Einstellungsbereichs** auf den Abschnitt **Experimente.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Die Seite Experimente unter Einstellungen" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="c8dab-118">Die **Seite Experimente** unter **Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="c8dab-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8dab-119">Scrollen Sie **auf** der Seite Experimente durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben jedem Feature, das Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="c8dab-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="c8dab-120">Schließen Sie Microsoft Edge DevTools, und öffnen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="c8dab-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="c8dab-121">Experimentelle Features werden ständig aktualisiert und können Leistungsprobleme verursachen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="c8dab-122">Um ein experimentelles Feature zu deaktivieren, öffnen Sie die Seite **Experimente,** und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c8dab-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="c8dab-123">Hervorgehobene experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="c8dab-123">Highlighted experimental features</span></span>  

<span data-ttu-id="c8dab-124">In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c8dab-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="c8dab-125">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="c8dab-125">Experimental feature</span></span> | <span data-ttu-id="c8dab-126">Microsoft Edge-Version</span><span class="sxs-lookup"><span data-stu-id="c8dab-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="c8dab-127">Aktivieren von Webhint</span><span class="sxs-lookup"><span data-stu-id="c8dab-127">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="c8dab-128">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="c8dab-128">85 or later</span></span> |  
| [<span data-ttu-id="c8dab-129">Aktivieren der Netzwerkkonsole</span><span class="sxs-lookup"><span data-stu-id="c8dab-129">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="c8dab-130">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="c8dab-130">85 or later</span></span> |  
| [<span data-ttu-id="c8dab-131">Source Order Viewer</span><span class="sxs-lookup"><span data-stu-id="c8dab-131">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="c8dab-132">86 oder höher</span><span class="sxs-lookup"><span data-stu-id="c8dab-132">86 or later</span></span> |  
| [<span data-ttu-id="c8dab-133">Aktivieren des Tastenkombinationen-Editors</span><span class="sxs-lookup"><span data-stu-id="c8dab-133">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="c8dab-134">87 oder höher</span><span class="sxs-lookup"><span data-stu-id="c8dab-134">87 or later</span></span> |  
| [<span data-ttu-id="c8dab-135">Aktivieren zusammengesetzter Layer in der 3D-Ansicht</span><span class="sxs-lookup"><span data-stu-id="c8dab-135">Enable Composited Layers in 3D View</span></span>](#enable-composited-layers-in-3d-view) | <span data-ttu-id="c8dab-136">87 oder höher</span><span class="sxs-lookup"><span data-stu-id="c8dab-136">87 or later</span></span> |  
| [<span data-ttu-id="c8dab-137">Aktivieren des neuen Schriftart-Editor-Tools im Bereich Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="c8dab-137">Enable new Font Editor tool within the Styles pane</span></span>](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="c8dab-138">89 oder höher</span><span class="sxs-lookup"><span data-stu-id="c8dab-138">89 or later</span></span> |  
| [<span data-ttu-id="c8dab-139">Aktivieren neuer CSS Flexbox-Debuggingfeatures</span><span class="sxs-lookup"><span data-stu-id="c8dab-139">Enable new CSS Flexbox debugging features</span></span>](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="c8dab-140">89 oder höher</span><span class="sxs-lookup"><span data-stu-id="c8dab-140">89 or later</span></span> |  
| [<span data-ttu-id="c8dab-141">Aktivieren und Aktivieren von Registerkartenmenüs für Schaltflächen zum Öffnen von weiteren Tools</span><span class="sxs-lookup"><span data-stu-id="c8dab-141">Enable + button tab menus to open more tools</span></span>](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="c8dab-142">89 oder höher</span><span class="sxs-lookup"><span data-stu-id="c8dab-142">89 or later</span></span> |  
| [<span data-ttu-id="c8dab-143">Registerkarte Willkommen aktivieren</span><span class="sxs-lookup"><span data-stu-id="c8dab-143">Enable Welcome tab</span></span>](#enable-welcome-tool) | <span data-ttu-id="c8dab-144">89 oder höher</span><span class="sxs-lookup"><span data-stu-id="c8dab-144">89 or later</span></span> |  

### <a name="enable-new-css-grid-debugging-features"></a><span data-ttu-id="c8dab-145">Aktivieren neuer FEATURES für das CSS-Rasterdebuding</span><span class="sxs-lookup"><span data-stu-id="c8dab-145">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="c8dab-146">Dieses experimentelle Feature bietet eine Reihe neuer Visualisierungen, mit deren Hilfe Sie CSS-Rasterlayouts debuggen können.</span><span class="sxs-lookup"><span data-stu-id="c8dab-146">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="c8dab-147">Aktivieren Sie dieses [Experiment,](#turn-on-experimental-features) und laden Sie DevTools neu, um eine Vorschau der neuesten experimentellen Features anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-147">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="c8dab-148">Dieses Experiment ist standardmäßig in Microsoft Edge, Version 87 oder höher, aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c8dab-148">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <a name="viewing-on-hover-grid-overlays-with-the-inspect-tool"></a><span data-ttu-id="c8dab-149">Anzeigen von On-Hover-Rasterüberlagerungen mit dem Inspect-Tool</span><span class="sxs-lookup"><span data-stu-id="c8dab-149">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="c8dab-150">Das **Tool Inspect** bietet eine schnelle Möglichkeit, CSS Grid Layouts in einer Website zu identifizieren und zu visualisieren, indem Sie mit der Maus auf sie zeigen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-150">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="c8dab-151">Wählen Sie in der oberen linken Ecke von DevTools das Symbol **Inspect** ![ \( Inspect ](../media/inspect-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-151">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="c8dab-152">Zeigen Sie dann auf ein `Grid` Element auf der Webseite, die Sie debuggen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-152">Then, hover on a `Grid` element on the webpage you are debugging.</span></span>  <span data-ttu-id="c8dab-153">Gliederungen werden um das Raster herum angezeigt, und die Schraffur gibt die Position von Gitterlücken an, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c8dab-153">Outlines are displayed around the grid, and hatching indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Anzeigen von Rastern mit dem Inspect-Tool" lightbox="../media/grid-inspect.msft.png":::
   <span data-ttu-id="c8dab-155">Anzeigen von Rastern mit dem **Inspect-Tool**</span><span class="sxs-lookup"><span data-stu-id="c8dab-155">Viewing grids with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="viewing-persistent-grid-overlays"></a><span data-ttu-id="c8dab-156">Anzeigen von beständigen Rasterüberlagerungen</span><span class="sxs-lookup"><span data-stu-id="c8dab-156">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="c8dab-157">In Microsoft Edge, Version 86 oder höher, bietet das experimentelle CSS-Rasterfeature auch die Möglichkeit, dauerhafte Grid-Überlagerungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c8dab-157">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="c8dab-158">Die beständigen Überlagerungen bieten verschiedene Vorteile.</span><span class="sxs-lookup"><span data-stu-id="c8dab-158">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="c8dab-159">Die beständigen Überlagerungen bleiben auf der Seite sichtbar, wenn Sie einen Bildlauf durchführen, die Maus bewegen und andere Features der DevTools verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8dab-159">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="c8dab-160">Mehrere dauerhafte Überlagerungen können gleichzeitig aktiviert werden, sodass Sie mehrere Rasterlayouts gleichzeitig überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="c8dab-160">Multiple persistent overlays may be turned on at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="c8dab-161">Dauerhafte Überlagerungen bieten viele Konfigurationsoptionen, z. B. Ausblenden oder Anzeigen von Namen im Rasterbereich, Rasterlücken, Titelgrößen und so weiter.</span><span class="sxs-lookup"><span data-stu-id="c8dab-161">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  
    
<span data-ttu-id="c8dab-162">Die beiden Möglichkeiten zum Umschalten einer beständigen Rasterüberlagerung.</span><span class="sxs-lookup"><span data-stu-id="c8dab-162">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="c8dab-163">Wählen Sie **das Ovalsymbol Raster** neben einem Grid-Element aus, das in der DOM-Struktur des **Elements-Tools angezeigt** wird.</span><span class="sxs-lookup"><span data-stu-id="c8dab-163">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Gitternetz-Ovalsymbol im Elementtool" lightbox="../media/grid-adorner.msft.png":::
       <span data-ttu-id="c8dab-165">Gitternetz-Ovalsymbol im **Elementtool**</span><span class="sxs-lookup"><span data-stu-id="c8dab-165">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="c8dab-166">Öffnen Sie das **neue Layoutpanel** im Elementtool, und aktivieren Sie das Kontrollkästchen neben jedem Grid-Element, das Hervorgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8dab-166">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Layoutbereich in DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="c8dab-168">**Layoutbereich** in DevTools</span><span class="sxs-lookup"><span data-stu-id="c8dab-168">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <a name="configuring-persistent-overlays"></a><span data-ttu-id="c8dab-169">Konfigurieren von beständigen Überlagerungen</span><span class="sxs-lookup"><span data-stu-id="c8dab-169">Configuring persistent overlays</span></span>  

<span data-ttu-id="c8dab-170">In Microsoft Edge, Version 86 oder höher, befindet sich das neue **Layoutpanel** im **Elementtool** neben den **Formatvorlagen** und **berechneten** Panels.</span><span class="sxs-lookup"><span data-stu-id="c8dab-170">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** panels.</span></span>  <span data-ttu-id="c8dab-171">Im **Layoutbereich** werden Konfigurationsoptionen für dauerhafte Überlagerungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c8dab-171">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Feature zum Debuggen von CSS-Rastern" lightbox="../media/experiments-grid.msft.png":::
   <span data-ttu-id="c8dab-173">Feature zum Debuggen von CSS-Rastern</span><span class="sxs-lookup"><span data-stu-id="c8dab-173">CSS grid debugging feature</span></span>  
:::image-end:::  

### <a name="enable-support-to-move-tabs-between-panels"></a><span data-ttu-id="c8dab-174">Aktivieren der Unterstützung zum Verschieben von Registerkarten zwischen Panels</span><span class="sxs-lookup"><span data-stu-id="c8dab-174">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="c8dab-175">Normalerweise können Tools wie **Elemente** und **Netzwerk** nur im Hauptbereich geöffnet werden, der sich am oberen Rand der DevTools befindet.</span><span class="sxs-lookup"><span data-stu-id="c8dab-175">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="c8dab-176">Tools wie **3D-Ansicht** und **Probleme,** die normalerweise nur im **Drawer-Bereich** geöffnet werden, der sich am unteren Rand der DevTools befindet.</span><span class="sxs-lookup"><span data-stu-id="c8dab-176">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="c8dab-177">Nachdem Sie das Experiment auswählen, können Sie Tools zwischen dem oberen und unteren Bereich verschieben.</span><span class="sxs-lookup"><span data-stu-id="c8dab-177">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="c8dab-178">Um ein Tool zu verschieben, zeigen Sie auf die Registerkarte, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Nach** oben oder **Nach unten verschieben aus.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-178">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="c8dab-179">Mit diesem Experiment können Sie Ihr DevTools-Layout anpassen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-179">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="c8dab-180">Wählen Sie aus, um den **Bereich "Drawer" ein- oder** auszublenden. `Escape`</span><span class="sxs-lookup"><span data-stu-id="c8dab-180">To display or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Verschieben von Tools zwischen Panels" lightbox="../media/experiments-move-panels.msft.png":::
   <span data-ttu-id="c8dab-182">Verschieben von Tools zwischen Panels</span><span class="sxs-lookup"><span data-stu-id="c8dab-182">Moving tools between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-webhint"></a><span data-ttu-id="c8dab-183">Aktivieren von Webhint</span><span class="sxs-lookup"><span data-stu-id="c8dab-183">Enable webhint</span></span>  

<span data-ttu-id="c8dab-184">[webhint][WebhintMain] ist ein Open-Source-Tool, das Feedback in Echtzeit für Websites und lokale Webseiten liefert.</span><span class="sxs-lookup"><span data-stu-id="c8dab-184">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="c8dab-185">Die Art des Feedbacks, das [von webhint bereitgestellt wird.][WebhintMain]</span><span class="sxs-lookup"><span data-stu-id="c8dab-185">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="c8dab-186">Bedienungshilfen</span><span class="sxs-lookup"><span data-stu-id="c8dab-186">accessibility</span></span>  
*   <span data-ttu-id="c8dab-187">Browserübergreifende Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="c8dab-187">cross-browser compatibility</span></span>  
*   <span data-ttu-id="c8dab-188">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="c8dab-188">security</span></span>  
*   <span data-ttu-id="c8dab-189">Leistung</span><span class="sxs-lookup"><span data-stu-id="c8dab-189">performance</span></span>  
*   <span data-ttu-id="c8dab-190">Progressive Web Apps (PWAs)</span><span class="sxs-lookup"><span data-stu-id="c8dab-190">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="c8dab-191">Andere häufige Probleme bei der Webentwicklung</span><span class="sxs-lookup"><span data-stu-id="c8dab-191">other common web development issues</span></span>  
    
<span data-ttu-id="c8dab-192">Das [Webhint-Experiment][WebhintMain] zeigt das Webhint-Feedback im Bereich [Probleme][DevtoolsIssues] an.</span><span class="sxs-lookup"><span data-stu-id="c8dab-192">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="c8dab-193">Wählen Sie ein Problem zum Anzeigen der Lösungsdokumentation und eine Liste der betroffenen Ressourcen auf Ihrer Website aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-193">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="c8dab-194">Wählen Sie einen Ressourcenlink aus, um den relevanten **Bereich Netzwerk,** **Quellen**oder **Elemente** in DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-194">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="Webhintfeedback im Problembereich" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="c8dab-196">Webhintfeedback im **Problembereich**</span><span class="sxs-lookup"><span data-stu-id="c8dab-196">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a><span data-ttu-id="c8dab-197">Aktivieren der Netzwerkkonsole</span><span class="sxs-lookup"><span data-stu-id="c8dab-197">Enable Network Console</span></span>  

<span data-ttu-id="c8dab-198">**Die Netzwerkkonsole** ist der Arbeitstitel eines Experiments zum Erstellen synthetischer Netzwerkanforderungen über HTTP.</span><span class="sxs-lookup"><span data-stu-id="c8dab-198">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="c8dab-199">Sie können das **Netzwerkkonsolenexperiment** verwenden, um Web-API-Anforderungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="c8dab-199">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="c8dab-200">Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.</span><span class="sxs-lookup"><span data-stu-id="c8dab-200">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="c8dab-201">Führen Sie die folgenden Schritte aus, um die **Netzwerkkonsole**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8dab-201">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="c8dab-202">Öffnen Sie den **Netzwerkbereich.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-202">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="c8dab-203">Suchen Sie die Netzwerkanforderung, die Sie ändern und erneut senden möchten.</span><span class="sxs-lookup"><span data-stu-id="c8dab-203">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="c8dab-204">Öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen **Sie Bearbeiten und Wiedergabe aus.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-204">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="c8dab-205">Wenn die **Netzwerkkonsole geöffnet** wird, bearbeiten Sie die Netzwerkanforderungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-205">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="c8dab-206">Wählen Sie **Senden**aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-206">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Netzwerkkonsole in der Konsolenschubschubschube" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="c8dab-208">**Netzwerkkonsole** in der **Konsolenschubschubschube**</span><span class="sxs-lookup"><span data-stu-id="c8dab-208">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="source-order-viewer"></a><span data-ttu-id="c8dab-209">Source Order Viewer</span><span class="sxs-lookup"><span data-stu-id="c8dab-209">Source Order Viewer</span></span>  

<span data-ttu-id="c8dab-210">**Source Order Viewer** ist ein Experiment, das die Reihenfolge der Elemente in der Webseitenquelle anzeigt.</span><span class="sxs-lookup"><span data-stu-id="c8dab-210">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="c8dab-211">Die Anzeigereihenfolge auf dem Bildschirm kann sich von der Reihenfolge der Quelle unterscheiden, wodurch Bildschirmlese- und Tastaturbenutzer verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="c8dab-211">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="c8dab-212">Verwenden Sie **das Experiment Source Order Viewer,** um die Unterschiede zwischen der Anzeigereihenfolge auf dem Bildschirm und der Reihenfolge der Quelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="c8dab-212">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="c8dab-213">Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.</span><span class="sxs-lookup"><span data-stu-id="c8dab-213">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="c8dab-214">Führen Sie die folgenden Schritte aus, um die **Quellauftragsanzeige**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8dab-214">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="c8dab-215">Öffnen Sie das **Elementtool.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-215">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="c8dab-216">Öffnen Sie **den Bereich** Barrierefreiheit im Bereich "Drawer\(bottom\)".</span><span class="sxs-lookup"><span data-stu-id="c8dab-216">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="c8dab-217">Aktivieren Sie **im Abschnitt Quellauftragsanzeige** das Kontrollkästchen **Quellreihenfolge** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-217">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="c8dab-218">Markieren Sie jedes HTML-Element, um eine Überlagerung anzuzeigen, die die Reihenfolge in der Webseitenquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="c8dab-218">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Quellauftragsanzeige im Bereich Barrierefreiheit" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="c8dab-220">**Quellauftragsanzeige** im Bereich **Barrierefreiheit**</span><span class="sxs-lookup"><span data-stu-id="c8dab-220">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-keyboard-shortcut-editor"></a><span data-ttu-id="c8dab-221">Aktivieren des Tastenkombinationen-Editors</span><span class="sxs-lookup"><span data-stu-id="c8dab-221">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="c8dab-222">Wenn das **Experiment Tastenkombinationen-Editor** aktivieren aktiviert ist, können Sie Tastenkombinationen für alle Aktionen in devTools anpassen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-222">With the **Enable keyboard shortcut editor** experiment turned on, you may customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="c8dab-223">Führen Sie die folgenden Schritte aus, um die Tastenkombination für eine bestimmte Aktion anzupassen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-223">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="c8dab-224">[Öffnen Sie DevTools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="c8dab-224">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="c8dab-225">Öffnen [Sie Einstellungen][DevToolsCustomizeIndexSettings].</span><span class="sxs-lookup"><span data-stu-id="c8dab-225">Open [Settings][DevToolsCustomizeIndexSettings].</span></span>  
    *   <span data-ttu-id="c8dab-226">Wählen Sie `Shift` + `?` aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-226">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="c8dab-227">Navigieren Sie zur **Seite Verknüpfungen.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-227">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="c8dab-228">Wählen Sie die Aktion aus, die Sie anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="c8dab-228">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="c8dab-229">Wählen Sie **das Symbol** Bearbeiten \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-229">Choose the **Edit** \(![EditKeyboardShortcut](../media/edit-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Wählen Sie auf der Seite Verknüpfungen unter Einstellungen die anzupassende Aktion aus." lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="c8dab-231">Wählen Sie auf der Seite Verknüpfungen unter Einstellungen die anzupassende **Aktion** [aus.][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="c8dab-231">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeIndexSettings]</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8dab-232">Wählen Sie auf der Tastatur die Tasten aus, die an die Aktion gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8dab-232">On the keyboard, select the keys to bind to the action.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Auswählen der Schlüssel, die Sie der Aktion zuweisen möchten" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="c8dab-234">Auswählen der Schlüssel, die Sie der Aktion zuweisen möchten</span><span class="sxs-lookup"><span data-stu-id="c8dab-234">Choose the keys you want to assign to the action</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8dab-235">Zum Speichern der neuen Tastenkombination wählen Sie das Häkchen \(</span><span class="sxs-lookup"><span data-stu-id="c8dab-235">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="c8dab-237">\) symbol.</span><span class="sxs-lookup"><span data-stu-id="c8dab-237">\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Wählen Sie das Häkchensymbol aus, um die neue Tastenkombination zu speichern." lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="c8dab-239">Wählen Sie das Häkchensymbol aus, um die neue Tastenkombination zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c8dab-239">Choose the checkmark icon to save your new keyboard shortcut</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8dab-240">Wählen Sie die neue Tastenkombination aus, um die Aktion in den DevTools auszulösen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-240">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="c8dab-241">Auf der **Seite Verknüpfungen** zeigt **das** Symbol Benutzerdefinierte Tastenkombination \( ![ CustomKeyboardShortcut \) die von Ihnen ](../media/custom-keyboard-shortcut-icon.msft.png) angepassten Tastenkombinationen an.</span><span class="sxs-lookup"><span data-stu-id="c8dab-241">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut](../media/custom-keyboard-shortcut-icon.msft.png)\) icon displays keyboard shortcuts you customized.</span></span>  <span data-ttu-id="c8dab-242">Um alle Verknüpfungen zurückzusetzen, wählen Sie **Standardverknüpfungen wiederherstellen aus.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-242">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="c8dab-243">Wenn Sie Ihre Änderungen beim Bearbeiten der Tastenkombinationen für eine Aktion verwerfen möchten, wählen Sie das Symbol X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-243">To discard your changes while you edit the keyboard shortcuts for an action, choose the X \(![XKeyboardShortcut](../media/discard-changes-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="c8dab-244">Zum Entfernen von Verknüpfungen für eine bestimmte Aktion wählen Sie **das** Symbol Verknüpfung löschen \( ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-244">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut](../media/delete-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="c8dab-245">Wenn Sie mehrere Verknüpfungen für eine Aktion hinzufügen möchten, wählen **Sie Verknüpfung hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-245">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>  

> [!NOTE]
> <span data-ttu-id="c8dab-246">Wenn eine Tastenkombination derzeit einer anderen Aktion zugewiesen ist, können Sie sie nicht für eine neue Aktion speichern.</span><span class="sxs-lookup"><span data-stu-id="c8dab-246">If a keyboard shortcut is currently assigned to another action, you may not save it for a new action.</span></span>  <span data-ttu-id="c8dab-247">Sie müssen zuerst die Tastenkombination für die vorherige Aktion löschen und dann der neuen Aktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-247">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a><span data-ttu-id="c8dab-248">Aktivieren zusammengesetzter Layer in der 3D-Ansicht</span><span class="sxs-lookup"><span data-stu-id="c8dab-248">Enable Composited Layers in 3D View</span></span>  

<span data-ttu-id="c8dab-249">Sie können layer jetzt zusammen mit z-Indizes und dem Dokumentobjektmodell \(DOM\) visualisieren.</span><span class="sxs-lookup"><span data-stu-id="c8dab-249">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="c8dab-250">Dieses Feature hilft Ihnen beim Debuggen, ohne Kontexte so oft zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="c8dab-250">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="c8dab-251">Sie haben festgestellt, dass die Reduzierung des Kontextwechsels ein großer Problempunkt war.</span><span class="sxs-lookup"><span data-stu-id="c8dab-251">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="c8dab-252">Es ist nicht immer klar, wie sich der von Ihnen geschriebene Code auf Ihre Web-App auswirkt.</span><span class="sxs-lookup"><span data-stu-id="c8dab-252">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="c8dab-253">Für ein umfassendes visuelles Debugging werden jetzt die 3D-Ansicht und die zusammengesetzten Ebenen kombiniert.</span><span class="sxs-lookup"><span data-stu-id="c8dab-253">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="c8dab-254">Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.</span><span class="sxs-lookup"><span data-stu-id="c8dab-254">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="c8dab-255">Führen Sie die folgenden **Schritte aus,** um zusammengesetzte Layer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8dab-255">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="c8dab-256">Wählen Sie in der Schublade das **3D-Ansichtstool** aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-256">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="c8dab-257">Öffnen Sie den **Bereich Zusammengesetzte Ebenen.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-257">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="c8dab-258">Alle dargestellten Ebenen der App werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c8dab-258">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="c8dab-259">Testen Sie dieses Feature mit Ihren eigenen Web-Apps.</span><span class="sxs-lookup"><span data-stu-id="c8dab-259">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Bereich „Zusammengesetzte Ebenen“" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="c8dab-261">Bereich **Zusammengesetzte Ebenen**</span><span class="sxs-lookup"><span data-stu-id="c8dab-261">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a><span data-ttu-id="c8dab-262">Aktivieren des neuen Schriftart-Editor-Tools im Bereich Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="c8dab-262">Enable new Font Editor tool within the Styles pane</span></span>  

<span data-ttu-id="c8dab-263">Sie können nun den neuen visuellen [Schriftarten-Editor verwenden,][DevtoolsInspectStylesEditFonts] um Schriftarten zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c8dab-263">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="c8dab-264">Verwenden Sie sie, um Schriftarten und Schriftartmerkmale zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c8dab-264">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="c8dab-265">Der visuelle **Schriftarten-Editor** hilft Ihnen beim Ausführen der folgenden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-265">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="c8dab-266">Wechseln zwischen Einheiten für unterschiedliche Schriftarteigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8dab-266">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="c8dab-267">Wechseln zwischen Schlüsselwörtern für unterschiedliche Schriftarteigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8dab-267">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="c8dab-268">Einheiten konvertieren</span><span class="sxs-lookup"><span data-stu-id="c8dab-268">Convert units</span></span>  
*   <span data-ttu-id="c8dab-269">Generieren von genauem CSS-Code</span><span class="sxs-lookup"><span data-stu-id="c8dab-269">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="c8dab-270">Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.</span><span class="sxs-lookup"><span data-stu-id="c8dab-270">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="c8dab-271">Führen Sie die folgenden Schritte aus, um den neuen **visuellen Schriftart-Editor**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8dab-271">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="c8dab-272">Öffnen Sie das **Elementtool.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-272">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="c8dab-273">Öffnen Sie den **Bereich Formatvorlagen.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-273">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="c8dab-274">Wählen Sie das **Symbol Schriftart-Editor** aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-274">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="c8dab-275">Weitere Informationen zum neuen visuellen Schriftarten-Editor **finden**Sie unter Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich [Formatvorlagen in DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="c8dab-275">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Der visuelle Schriftarten-Editor-Bereich wird hervorgehoben" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="c8dab-277">Der visuelle **Schriftarten-Editor-Bereich** wird hervorgehoben</span><span class="sxs-lookup"><span data-stu-id="c8dab-277">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-new-css-flexbox-debugging-features"></a><span data-ttu-id="c8dab-278">Aktivieren neuer CSS Flexbox-Debuggingfeatures</span><span class="sxs-lookup"><span data-stu-id="c8dab-278">Enable new CSS Flexbox debugging features</span></span>  

<span data-ttu-id="c8dab-279">Dieses experimentelle Feature bietet viele neue Visualisierungen, mit deren Hilfe Sie CSS-Flexbox-Layouts debuggen können.</span><span class="sxs-lookup"><span data-stu-id="c8dab-279">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="c8dab-280">Um eine Vorschau der neuesten experimentellen Features anzuzeigen, [aktivieren Sie dieses Experiment,](#turn-on-experimental-features) und laden Sie DevTools neu.</span><span class="sxs-lookup"><span data-stu-id="c8dab-280">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="c8dab-281">Anzeigen von beständigen Überlagerungen in Flexbox-Layouts mit dem Inspect-Tool</span><span class="sxs-lookup"><span data-stu-id="c8dab-281">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="c8dab-282">Das **Inspect-Tool** bietet eine schnelle Möglichkeit, CSS-Flexbox-Layouts in einer Website zu identifizieren und zu visualisieren, indem Sie mit der Maus auf sie zeigen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-282">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="c8dab-283">Wählen Sie in der oberen linken Ecke von DevTools das Symbol **Inspect** ![ \( Inspect ](../media/inspect-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-283">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="c8dab-284">Zeigen Sie dann beim Debuggen der Website auf einen Flexcontainer, um Gliederungen um den flex-Container zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-284">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Anzeigen von Flexbox-Containern mit dem Inspect-Tool" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="c8dab-286">Anzeigen von Flexbox-Containern mit dem **Inspect-Tool**</span><span class="sxs-lookup"><span data-stu-id="c8dab-286">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="c8dab-287">Anzeigen von beständigen Überlagerungen in Flexboxlayouts</span><span class="sxs-lookup"><span data-stu-id="c8dab-287">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="c8dab-288">In Microsoft Edge, Version 89 oder höher, bietet das experimentelle FEATURE CSS Flexbox auch die Möglichkeit, dauerhafte Überlagerungen für Flexbox-Layouts zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c8dab-288">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="c8dab-289">Dauerhafte Überlagerungen bieten die folgenden Vorteile.</span><span class="sxs-lookup"><span data-stu-id="c8dab-289">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="c8dab-290">Dauerhafte Überlagerungen bleiben auf der Webseite sichtbar, wenn Sie einen Bildlauf durchführen, die Maus bewegen und andere Features der DevTools verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8dab-290">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="c8dab-291">Mehrere dauerhafte Überlagerungen können gleichzeitig verwendet werden, damit Sie mehrere Flexbox-Layouts gleichzeitig überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="c8dab-291">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="c8dab-292">Dauerhafte Überlagerungen bieten Farbkonfigurationsoptionen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-292">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="c8dab-293">Verwenden Sie eine der folgenden Aktionen, um dauerhafte Überlagerungen im Flexbox-Layout umschalten zu können.</span><span class="sxs-lookup"><span data-stu-id="c8dab-293">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="c8dab-294">Wählen Sie **das Ovalsymbol Flexbox** neben einem beliebigen Flexbox-Container aus, der in der DOM-Struktur des **Elements-Tools angezeigt** wird.</span><span class="sxs-lookup"><span data-stu-id="c8dab-294">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="c8dab-295">Öffnen Sie das **neue Layoutpanel** im **Elementtool,** und aktivieren Sie das Kontrollkästchen neben jedem Flexbox-Container, den Sie hervorheben möchten.</span><span class="sxs-lookup"><span data-stu-id="c8dab-295">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Flexsymbole und Layoutbereich in DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="c8dab-297">Flexsymbole **und Layoutbereich** in DevTools</span><span class="sxs-lookup"><span data-stu-id="c8dab-297">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="c8dab-298">Konfigurieren von beständigen Überlagerungen</span><span class="sxs-lookup"><span data-stu-id="c8dab-298">Configure persistent overlays</span></span>  

<span data-ttu-id="c8dab-299">Verwenden Sie den **Layoutbereich,** um Optionen für dauerhafte Überlagerungen für CSS-Raster oder Flexbox-Layouts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c8dab-299">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="c8dab-300">Der **Layoutbereich** befindet sich im **Elementtool** neben den **Formatvorlagen-** und **Berechneten** Fensterausschnitten.</span><span class="sxs-lookup"><span data-stu-id="c8dab-300">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Layoutbereich" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="c8dab-302">Layoutbereich</span><span class="sxs-lookup"><span data-stu-id="c8dab-302">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable--button-tab-menus-to-open-more-tools"></a><span data-ttu-id="c8dab-303">Aktivieren und Aktivieren von Registerkartenmenüs für Schaltflächen zum Öffnen von weiteren Tools</span><span class="sxs-lookup"><span data-stu-id="c8dab-303">Enable + button tab menus to open more tools</span></span>  

<span data-ttu-id="c8dab-304">Sie können nun weitere Tools mit dem neuen **Symbol Weitere Tools** \( `+` \) öffnen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-304">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="c8dab-305">Nachdem Sie die \*\*\*\* Registerkartenmenüs +aktivieren aktiviert haben, um weitere Tools zu öffnen und DevTools neu zu laden, wird rechts neben der Registerkartengruppe am oberen Rand der DevTools ein Pluszeichen \( `+` \) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c8dab-305">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="c8dab-306">Wenn Sie eine Liste anderer Tools anzeigen möchten, die Sie der Registerkartenleiste hinzufügen können, wählen Sie das neue Symbol Weitere **Tools** \( `+` \) aus.</span><span class="sxs-lookup"><span data-stu-id="c8dab-306">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Weitere Tools im oberen Bereich" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="c8dab-308">**Weitere Tools** im oberen Bereich</span><span class="sxs-lookup"><span data-stu-id="c8dab-308">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a><span data-ttu-id="c8dab-309">Aktivieren des Willkommenstools</span><span class="sxs-lookup"><span data-stu-id="c8dab-309">Enable Welcome tool</span></span>

<span data-ttu-id="c8dab-310">Dieses Experiment ersetzt das **Neue** Tool durch das neue **Willkommenstool.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-310">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="c8dab-311">Es wird ein aktualisiertes Design für den folgenden Inhalt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c8dab-311">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="c8dab-312">Links zu Entwickler-Dokumenten</span><span class="sxs-lookup"><span data-stu-id="c8dab-312">Links to developer docs</span></span>  
*   <span data-ttu-id="c8dab-313">die neuesten Features</span><span class="sxs-lookup"><span data-stu-id="c8dab-313">the latest features</span></span>  
*   <span data-ttu-id="c8dab-314">Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="c8dab-314">release notes</span></span>  
*   <span data-ttu-id="c8dab-315">Option zum Kontaktieren des Microsoft Edge DevTools-Teams</span><span class="sxs-lookup"><span data-stu-id="c8dab-315">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="c8dab-316">Das **Willkommenstool** wird nach jedem Update auf Microsoft Edge automatisch geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c8dab-316">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="c8dab-317">Um die Anzeige \*\*\*\* des Willkommenstools nach jedem Update zu verhindern, aktivieren Sie das Kontrollkästchen neben Registerkarte Öffnen nach jedem Update **unter** dem **Titel Willkommenstool.**</span><span class="sxs-lookup"><span data-stu-id="c8dab-317">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="c8dab-318">Wenn Sie das ursprüngliche **Tool What's New** bevorzugen, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings]  >  **Experimente,** und entfernen Sie das Kontrollkästchen neben **Registerkarte Willkommen aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="c8dab-318">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Willkommenstool" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="c8dab-320">**Willkommenstool**</span><span class="sxs-lookup"><span data-stu-id="c8dab-320">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="c8dab-321">Frühere experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="c8dab-321">Previous experimental features</span></span>  

*   <span data-ttu-id="c8dab-322">[Die 3D-Ansicht][Devtools3dViewIndex] ist jetzt in Microsoft Edge, Version 83 oder höher, standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c8dab-322">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="c8dab-323">[Aktivieren Der Support zum Verschieben von Registerkarten][DevtoolsMoveTabs] zwischen Panels ist jetzt verfügbar und in Microsoft Edge, Version 85 oder höher, standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c8dab-323">[Turn on support to move tabs between panels][DevtoolsMoveTabs] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="c8dab-324">[Tastenkombinationen anpassen ist][DevtoolsCustomKeyboardShortcuts] jetzt verfügbar und in Microsoft Edge, Version 86 oder höher, standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c8dab-324">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="c8dab-325">[Emulation: Der duale][DevtoolsDeviceModeDualScreenAndFoldables] Bildschirmmodus ist jetzt verfügbar und in Microsoft Edge, Version 89 oder höher, standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c8dab-325">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="c8dab-326">[In Microsoft Edge,][DevtoolsCssGrid] Version 89 oder höher, sind neue FEATURES für das CSS-Rasterdebuding jetzt verfügbar und standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c8dab-326">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="c8dab-327">Bereitstellen von Feedback zu experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="c8dab-327">Providing feedback on experimental features</span></span>  

<span data-ttu-id="c8dab-328">So geben Sie Feedback zu Microsoft Edge DevTools-Experimenten oder zu anderen DevTools-Bezogenen.</span><span class="sxs-lookup"><span data-stu-id="c8dab-328">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="c8dab-329">Senden Sie Ihr Feedback mit dem **Symbol** Feedback senden in den DevTools</span><span class="sxs-lookup"><span data-stu-id="c8dab-329">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="c8dab-330">Tweet bei [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="c8dab-330">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol Feedback senden in den Microsoft Edge-Entwicklungstools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="c8dab-332">Das Symbol **Feedback senden** in den Microsoft Edge-Entwicklungstools</span><span class="sxs-lookup"><span data-stu-id="c8dab-332">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "3D-Ansicht | Microsoft Docs"  
[DevtoolsCssGrid]: ../css/grid.md "Inspect CSS Grid in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsMoveTabs]: ../customize/index.md "Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simulieren mobiler Geräte mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich Formatvorlagen in DevTools | Microsoft Docs"  
[DevtoolsIssues]: ../issues/index.md "Erkennen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool „Probleme“ | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Microsoft Edge DevTools-Tastenkombinationen | Microsoft Docs"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools-| Microsoft Docs"  
[DevtoolsOpenMain]: ../open/index.md "Öffnen Sie Microsoft Edge DevTools | Microsoft Docs"  

[DualScreenWebIndex]: /dual-screen/web/index "Dualscreen-Weberfahrungen | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Laden Sie den Surface Duo-Emulator | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Arbeiten mit der Naht – Einführung in duale Bildschirmgeräte | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface Duo-Emulators | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Css-Medienbildschirm-Spannfunktion für die Erkennung von | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "Die getWindowSegments-JavaScript-API für Dual-Screen-| Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Remotedesktopclients | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxis fold | Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emulieren von Dualscreen- und faltbaren Geräten in Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  

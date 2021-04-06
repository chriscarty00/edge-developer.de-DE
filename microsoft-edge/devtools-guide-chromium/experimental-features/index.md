---
description: Die neuesten experimentellen Features in Microsoft Edge DevTools
title: Experimentelle Features
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, experiment
no-loc:
- Enable webhint
- Enable Network Console
- Source Order Viewer
- Enable Composited Layers in 3D View
- Enable new Font Editor tool within the Styles pane
- Enable new CSS Flexbox debugging features
- Enable + button tab menus to open more tools
- Enable Welcome tab
- 3D View
- Turn on support to move tabs between panels
- Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code
- Edit keyboard shortcuts for any action in the DevTools
- Turn on new CSS grid debugging features
- 'Emulation: Support dual screen mode'
ms.openlocfilehash: c76830cb8bbcc597aa026f58e1926cd2f9bc2d62
ms.sourcegitcommit: 2ddfd98d1e871be9c61380a8ca57da398d38bd54
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "11439584"
---
# <a name="experimental-features"></a><span data-ttu-id="93899-104">Experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="93899-104">Experimental features</span></span>  

<span data-ttu-id="93899-105">Microsoft Edge DevTools bieten Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.</span><span class="sxs-lookup"><span data-stu-id="93899-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="93899-106">Sie können testen und [Feedback geben,](#providing-feedback-on-experimental-features) bevor jedes Feature veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="93899-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="93899-107">Obwohl experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, können Sie die neuesten experimentellen Features über den Microsoft Edge Canary-Kanal erhalten.</span><span class="sxs-lookup"><span data-stu-id="93899-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="93899-108">Aktivieren experimenteller Features</span><span class="sxs-lookup"><span data-stu-id="93899-108">Turn on experimental features</span></span>  

<span data-ttu-id="93899-109">Führen Sie die folgenden Schritte aus, um \(oder off\) experimentelle Features in Microsoft Edge zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="93899-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="93899-110">[Öffnen Sie DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="93899-110">[Open DevTools][DevtoolsOpenIndex].</span></span>  
    *   <span data-ttu-id="93899-111">Wählen `Control` + `Shift` + `I` Sie \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="93899-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="93899-112">Weitere Informationen finden Sie unter [Microsoft Edge DevTools-Tastenkombinationen.][DevtoolsShortcutsIndex]</span><span class="sxs-lookup"><span data-stu-id="93899-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="93899-113">Öffnen Sie den [Bereich][DevToolsCustomizeIndexSettings] Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="93899-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="93899-114">Wählen Sie `Shift` + `?` aus.</span><span class="sxs-lookup"><span data-stu-id="93899-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="93899-115">Weitere Informationen finden Sie unter [Microsoft Edge DevTools-Tastenkombinationen.][DevtoolsShortcutsIndex]</span><span class="sxs-lookup"><span data-stu-id="93899-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="93899-116">Klicken Sie auf der linken Seite des **Einstellungsbereichs** auf den Abschnitt **Experimente.**</span><span class="sxs-lookup"><span data-stu-id="93899-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Die Seite Experimente unter Einstellungen" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="93899-118">Die **Seite Experimente** unter **Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="93899-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="93899-119">Scrollen Sie **auf** der Seite Experimente durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben jedem Feature, das Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="93899-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="93899-120">Schließen Sie Microsoft Edge DevTools, und öffnen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="93899-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="93899-121">Experimentelle Features werden ständig aktualisiert und können Leistungsprobleme verursachen.</span><span class="sxs-lookup"><span data-stu-id="93899-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="93899-122">Um ein experimentelles Feature zu deaktivieren, öffnen Sie die Seite **Experimente,** und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="93899-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="93899-123">Hervorgehobene experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="93899-123">Highlighted experimental features</span></span>  

<span data-ttu-id="93899-124">In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="93899-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="93899-125">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="93899-125">Experimental feature</span></span> | <span data-ttu-id="93899-126">Microsoft Edge-Version</span><span class="sxs-lookup"><span data-stu-id="93899-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [Enable webhint](#enable-webhint) | <span data-ttu-id="93899-127">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="93899-127">85 or later</span></span> |  
| [Enable Network Console](#enable-network-console) | <span data-ttu-id="93899-128">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="93899-128">85 or later</span></span> |  
| [Source Order Viewer](#source-order-viewer) | <span data-ttu-id="93899-129">86 oder höher</span><span class="sxs-lookup"><span data-stu-id="93899-129">86 or later</span></span> |  
| [Enable Composited Layers in 3D View](#enable-composited-layers-in-3d-view) | <span data-ttu-id="93899-130">87 oder höher</span><span class="sxs-lookup"><span data-stu-id="93899-130">87 or later</span></span> |  
| [Enable new Font Editor tool within the Styles pane](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="93899-131">89 oder höher</span><span class="sxs-lookup"><span data-stu-id="93899-131">89 or later</span></span> |  
| [Enable new CSS Flexbox debugging features](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="93899-132">89 oder höher</span><span class="sxs-lookup"><span data-stu-id="93899-132">89 or later</span></span> |  
| [Enable + button tab menus to open more tools](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="93899-133">89 oder höher</span><span class="sxs-lookup"><span data-stu-id="93899-133">89 or later</span></span> |  
| [Enable Welcome tab](#enable-welcome-tab) | <span data-ttu-id="93899-134">89 oder höher</span><span class="sxs-lookup"><span data-stu-id="93899-134">89 or later</span></span> |  

### Enable webhint  

<span data-ttu-id="93899-135">[webhint][WebhintMain] ist ein Open-Source-Tool, das Feedback in Echtzeit für Websites und lokale Webseiten liefert.</span><span class="sxs-lookup"><span data-stu-id="93899-135">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="93899-136">Die Art des Feedbacks, das [von webhint bereitgestellt wird.][WebhintMain]</span><span class="sxs-lookup"><span data-stu-id="93899-136">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="93899-137">Bedienungshilfen</span><span class="sxs-lookup"><span data-stu-id="93899-137">accessibility</span></span>  
*   <span data-ttu-id="93899-138">Browserübergreifende Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="93899-138">cross-browser compatibility</span></span>  
*   <span data-ttu-id="93899-139">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="93899-139">security</span></span>  
*   <span data-ttu-id="93899-140">Leistung</span><span class="sxs-lookup"><span data-stu-id="93899-140">performance</span></span>  
*   <span data-ttu-id="93899-141">Progressive Web Apps (PWAs)</span><span class="sxs-lookup"><span data-stu-id="93899-141">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="93899-142">Andere häufige Probleme bei der Webentwicklung</span><span class="sxs-lookup"><span data-stu-id="93899-142">other common web development issues</span></span>  
    
<span data-ttu-id="93899-143">Das [Webhint-Experiment][WebhintMain] zeigt das Webhint-Feedback im Bereich [Probleme][DevtoolsIssuesIndex] an.</span><span class="sxs-lookup"><span data-stu-id="93899-143">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssuesIndex] panel.</span></span>  <span data-ttu-id="93899-144">Wählen Sie ein Problem zum Anzeigen der Lösungsdokumentation und eine Liste der betroffenen Ressourcen auf Ihrer Website aus.</span><span class="sxs-lookup"><span data-stu-id="93899-144">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="93899-145">Wählen Sie einen Ressourcenlink aus, um den relevanten **Bereich Netzwerk,** **Quellen**oder **Elemente** in DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="93899-145">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="Webhintfeedback im Problembereich" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="93899-147">Webhintfeedback im **Problembereich**</span><span class="sxs-lookup"><span data-stu-id="93899-147">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Enable Network Console  

<span data-ttu-id="93899-148">**Die Netzwerkkonsole** ist der Arbeitstitel eines Experiments zum Erstellen synthetischer Netzwerkanforderungen über HTTP.</span><span class="sxs-lookup"><span data-stu-id="93899-148">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="93899-149">Sie können das **Netzwerkkonsolenexperiment** verwenden, um Web-API-Anforderungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="93899-149">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="93899-150">Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.</span><span class="sxs-lookup"><span data-stu-id="93899-150">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="93899-151">Führen Sie die folgenden Schritte aus, um die **Netzwerkkonsole**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="93899-151">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="93899-152">Öffnen Sie den **Netzwerkbereich.**</span><span class="sxs-lookup"><span data-stu-id="93899-152">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="93899-153">Suchen Sie die Netzwerkanforderung, die Sie ändern und erneut senden möchten.</span><span class="sxs-lookup"><span data-stu-id="93899-153">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="93899-154">Öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen **Sie Bearbeiten und Wiedergabe aus.**</span><span class="sxs-lookup"><span data-stu-id="93899-154">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="93899-155">Wenn die **Netzwerkkonsole geöffnet** wird, bearbeiten Sie die Netzwerkanforderungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="93899-155">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="93899-156">Wählen Sie **Senden**aus.</span><span class="sxs-lookup"><span data-stu-id="93899-156">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Netzwerkkonsole in der Konsolenschubschubschube" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="93899-158">**Netzwerkkonsole** in der **Konsolenschubschubschube**</span><span class="sxs-lookup"><span data-stu-id="93899-158">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Source Order Viewer  

<span data-ttu-id="93899-159">**Source Order Viewer** ist ein Experiment, das die Reihenfolge der Elemente in der Webseitenquelle anzeigt.</span><span class="sxs-lookup"><span data-stu-id="93899-159">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="93899-160">Die Anzeigereihenfolge auf dem Bildschirm kann sich von der Reihenfolge der Quelle unterscheiden, wodurch Bildschirmlese- und Tastaturbenutzer verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="93899-160">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="93899-161">Verwenden Sie das Experiment, um die Unterschiede zwischen der Anzeigereihenfolge auf dem Bildschirm und **Source Order Viewer** der Reihenfolge der Quelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="93899-161">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="93899-162">Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.</span><span class="sxs-lookup"><span data-stu-id="93899-162">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="93899-163">Führen Sie **Source Order Viewer** zur Verwendung die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="93899-163">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="93899-164">Öffnen Sie das **Elementtool.**</span><span class="sxs-lookup"><span data-stu-id="93899-164">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="93899-165">Öffnen Sie **den Bereich** Barrierefreiheit im Bereich "Drawer\(bottom\)".</span><span class="sxs-lookup"><span data-stu-id="93899-165">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="93899-166">Aktivieren Sie **Source Order Viewer** im Abschnitt das Kontrollkästchen **Quellreihenfolge** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="93899-166">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="93899-167">Markieren Sie jedes HTML-Element, um eine Überlagerung anzuzeigen, die die Reihenfolge in der Webseitenquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="93899-167">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Source Order Viewer in the Accessibility pane" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Source Order Viewer** in the **Accessibility** pane  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Enable Composited Layers in 3D View  

<span data-ttu-id="93899-169">Sie können layer jetzt zusammen mit z-Indizes und dem Dokumentobjektmodell \(DOM\) visualisieren.</span><span class="sxs-lookup"><span data-stu-id="93899-169">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="93899-170">Dieses Feature hilft Ihnen beim Debuggen, ohne Kontexte so oft zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="93899-170">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="93899-171">Sie haben festgestellt, dass die Reduzierung des Kontextwechsels ein großer Problempunkt war.</span><span class="sxs-lookup"><span data-stu-id="93899-171">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="93899-172">Es ist nicht immer klar, wie sich der von Ihnen geschriebene Code auf Ihre Web-App auswirkt.</span><span class="sxs-lookup"><span data-stu-id="93899-172">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="93899-173">Für ein umfassendes visuelles Debuggen werden nun 3D View die und zusammengesetzte Ebenen kombiniert.</span><span class="sxs-lookup"><span data-stu-id="93899-173">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="93899-174">Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.</span><span class="sxs-lookup"><span data-stu-id="93899-174">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="93899-175">Führen Sie die folgenden **Schritte aus,** um zusammengesetzte Layer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="93899-175">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="93899-176">Wählen Sie in der Schublade das **3D View** Tool aus.</span><span class="sxs-lookup"><span data-stu-id="93899-176">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="93899-177">Öffnen Sie den **Bereich Zusammengesetzte Ebenen.**</span><span class="sxs-lookup"><span data-stu-id="93899-177">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="93899-178">Alle dargestellten Ebenen der App werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="93899-178">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="93899-179">Testen Sie dieses Feature mit Ihren eigenen Web-Apps.</span><span class="sxs-lookup"><span data-stu-id="93899-179">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Bereich Zusammengesetzte Ebenen" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="93899-181">Bereich **Zusammengesetzte Ebenen**</span><span class="sxs-lookup"><span data-stu-id="93899-181">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Enable new Font Editor tool within the Styles pane  

<span data-ttu-id="93899-182">Sie können nun den neuen visuellen [Schriftarten-Editor verwenden,][DevtoolsInspectStylesEditFonts] um Schriftarten zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="93899-182">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="93899-183">Verwenden Sie sie, um Schriftarten und Schriftartmerkmale zu definieren.</span><span class="sxs-lookup"><span data-stu-id="93899-183">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="93899-184">Der visuelle **Schriftarten-Editor** hilft Ihnen beim Ausführen der folgenden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="93899-184">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="93899-185">Wechseln zwischen Einheiten für unterschiedliche Schriftarteigenschaften</span><span class="sxs-lookup"><span data-stu-id="93899-185">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="93899-186">Wechseln zwischen Schlüsselwörtern für unterschiedliche Schriftarteigenschaften</span><span class="sxs-lookup"><span data-stu-id="93899-186">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="93899-187">Konvertieren von Einheiten</span><span class="sxs-lookup"><span data-stu-id="93899-187">Convert units</span></span>  
*   <span data-ttu-id="93899-188">Generieren von genauem CSS-Code</span><span class="sxs-lookup"><span data-stu-id="93899-188">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="93899-189">Nachdem Sie das Experiment aktivieren, stellen Sie sicher, dass Sie die DevTools neu starten.</span><span class="sxs-lookup"><span data-stu-id="93899-189">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="93899-190">Führen Sie die folgenden Schritte aus, um den neuen **visuellen Schriftart-Editor**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="93899-190">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="93899-191">Öffnen Sie das **Elementtool.**</span><span class="sxs-lookup"><span data-stu-id="93899-191">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="93899-192">Öffnen Sie den **Bereich Formatvorlagen.**</span><span class="sxs-lookup"><span data-stu-id="93899-192">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="93899-193">Wählen Sie das **Symbol Schriftart-Editor** aus.</span><span class="sxs-lookup"><span data-stu-id="93899-193">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="93899-194">Weitere Informationen zum neuen visuellen Schriftarten-Editor **finden**Sie unter Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich [Formatvorlagen in DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="93899-194">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Der visuelle Schriftarten-Editor-Bereich wird hervorgehoben" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="93899-196">Der visuelle **Schriftarten-Editor-Bereich** wird hervorgehoben</span><span class="sxs-lookup"><span data-stu-id="93899-196">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable new CSS Flexbox debugging features  

<span data-ttu-id="93899-197">Dieses experimentelle Feature bietet viele neue Visualisierungen, mit deren Hilfe Sie CSS-Flexbox-Layouts debuggen können.</span><span class="sxs-lookup"><span data-stu-id="93899-197">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="93899-198">Um eine Vorschau der neuesten experimentellen Features anzuzeigen, [aktivieren Sie dieses Experiment,](#turn-on-experimental-features) und laden Sie DevTools neu.</span><span class="sxs-lookup"><span data-stu-id="93899-198">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="93899-199">Anzeigen von beständigen Überlagerungen in Flexbox-Layouts mit dem Inspect-Tool</span><span class="sxs-lookup"><span data-stu-id="93899-199">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="93899-200">Das **Inspect-Tool** bietet eine schnelle Möglichkeit, CSS-Flexbox-Layouts in einer Website zu identifizieren und zu visualisieren, indem Sie mit der Maus auf sie zeigen.</span><span class="sxs-lookup"><span data-stu-id="93899-200">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="93899-201">Wählen Sie in der oberen linken Ecke von DevTools das Symbol **Inspect** ![ \( Inspect ](../media/inspect-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="93899-201">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="93899-202">Zeigen Sie dann beim Debuggen der Website auf einen Flexcontainer, um Gliederungen um den flex-Container zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="93899-202">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Anzeigen von Flexbox-Containern mit dem Inspect-Tool" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="93899-204">Anzeigen von Flexbox-Containern mit dem **Inspect-Tool**</span><span class="sxs-lookup"><span data-stu-id="93899-204">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="93899-205">Anzeigen von beständigen Überlagerungen in Flexboxlayouts</span><span class="sxs-lookup"><span data-stu-id="93899-205">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="93899-206">In Microsoft Edge, Version 89 oder höher, bietet das experimentelle FEATURE CSS Flexbox auch die Möglichkeit, dauerhafte Überlagerungen für Flexbox-Layouts zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="93899-206">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="93899-207">Dauerhafte Überlagerungen bieten die folgenden Vorteile.</span><span class="sxs-lookup"><span data-stu-id="93899-207">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="93899-208">Dauerhafte Überlagerungen bleiben auf der Webseite sichtbar, wenn Sie einen Bildlauf durchführen, die Maus bewegen und andere Features der DevTools verwenden.</span><span class="sxs-lookup"><span data-stu-id="93899-208">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="93899-209">Mehrere dauerhafte Überlagerungen können gleichzeitig verwendet werden, damit Sie mehrere Flexbox-Layouts gleichzeitig überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="93899-209">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="93899-210">Dauerhafte Überlagerungen bieten Farbkonfigurationsoptionen.</span><span class="sxs-lookup"><span data-stu-id="93899-210">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="93899-211">Verwenden Sie eine der folgenden Aktionen, um dauerhafte Überlagerungen im Flexbox-Layout umschalten zu können.</span><span class="sxs-lookup"><span data-stu-id="93899-211">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="93899-212">Wählen Sie **das Ovalsymbol Flexbox** neben einem beliebigen Flexbox-Container aus, der in der DOM-Struktur des **Elements-Tools angezeigt** wird.</span><span class="sxs-lookup"><span data-stu-id="93899-212">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="93899-213">Öffnen Sie das **neue Layoutpanel** im **Elementtool,** und aktivieren Sie das Kontrollkästchen neben jedem Flexbox-Container, den Sie hervorheben möchten.</span><span class="sxs-lookup"><span data-stu-id="93899-213">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Flexsymbole und Layoutbereich in DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="93899-215">Flexsymbole **und Layoutbereich** in DevTools</span><span class="sxs-lookup"><span data-stu-id="93899-215">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="93899-216">Konfigurieren von beständigen Überlagerungen</span><span class="sxs-lookup"><span data-stu-id="93899-216">Configure persistent overlays</span></span>  

<span data-ttu-id="93899-217">Verwenden Sie den **Layoutbereich,** um Optionen für dauerhafte Überlagerungen für CSS-Raster oder Flexbox-Layouts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="93899-217">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="93899-218">Der **Layoutbereich** befindet sich im **Elementtool** neben den **Formatvorlagen-** und **Berechneten** Fensterausschnitten.</span><span class="sxs-lookup"><span data-stu-id="93899-218">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Layoutbereich" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="93899-220">Layoutbereich</span><span class="sxs-lookup"><span data-stu-id="93899-220">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable + button tab menus to open more tools  

<span data-ttu-id="93899-221">Sie können nun weitere Tools mit dem neuen **Symbol Weitere Tools** \( `+` \) öffnen.</span><span class="sxs-lookup"><span data-stu-id="93899-221">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="93899-222">Nachdem Sie das Experiment aktivieren und DevTools neu laden, wird rechts neben der Registerkartengruppe am oberen Rand der DevTools ein Pluszeichen **Enable + button tab menus to open more tools** \( `+` \) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="93899-222">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="93899-223">Wenn Sie eine Liste anderer Tools anzeigen möchten, die Sie der Registerkartenleiste hinzufügen können, wählen Sie das neue Symbol Weitere **Tools** \( `+` \) aus.</span><span class="sxs-lookup"><span data-stu-id="93899-223">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Weitere Tools im oberen Bereich" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="93899-225">**Weitere Tools** im oberen Bereich</span><span class="sxs-lookup"><span data-stu-id="93899-225">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable Welcome tab

<span data-ttu-id="93899-226">Dieses Experiment ersetzt das **Neue** Tool durch das neue **Willkommenstool.**</span><span class="sxs-lookup"><span data-stu-id="93899-226">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="93899-227">Es wird ein aktualisiertes Design für den folgenden Inhalt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="93899-227">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="93899-228">Links zu Entwickler-Dokumenten</span><span class="sxs-lookup"><span data-stu-id="93899-228">Links to developer docs</span></span>  
*   <span data-ttu-id="93899-229">die neuesten Features</span><span class="sxs-lookup"><span data-stu-id="93899-229">the latest features</span></span>  
*   <span data-ttu-id="93899-230">Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="93899-230">release notes</span></span>  
*   <span data-ttu-id="93899-231">Option zum Kontaktieren des Microsoft Edge DevTools-Teams</span><span class="sxs-lookup"><span data-stu-id="93899-231">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="93899-232">Das **Willkommenstool** wird nach jedem Update auf Microsoft Edge automatisch geöffnet.</span><span class="sxs-lookup"><span data-stu-id="93899-232">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="93899-233">Um die Anzeige \*\*\*\* des Willkommenstools nach jedem Update zu verhindern, aktivieren Sie das Kontrollkästchen neben Registerkarte Öffnen nach jedem Update **unter** dem **Titel Willkommenstool.**</span><span class="sxs-lookup"><span data-stu-id="93899-233">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="93899-234">Wenn Sie das ursprüngliche **Tool What's New** bevorzugen, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings]  >  **Experimente,** und entfernen Sie das Kontrollkästchen neben **Enable Welcome tab** .</span><span class="sxs-lookup"><span data-stu-id="93899-234">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Willkommenstool" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="93899-236">**Willkommenstool**</span><span class="sxs-lookup"><span data-stu-id="93899-236">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="93899-237">Frühere experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="93899-237">Previous experimental features</span></span>  

*   <span data-ttu-id="93899-238">[3D View][Devtools3dViewIndex] ist jetzt in Microsoft Edge, Version 83 oder höher, verfügbar und standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="93899-238">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="93899-239">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex] ist jetzt in Microsoft Edge, Version 85 oder höher, verfügbar und standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="93899-239">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="93899-240">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] ist jetzt in Microsoft Edge, Version 86 oder höher, verfügbar und standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="93899-240">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="93899-241">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] ist jetzt in Microsoft Edge, Version 89 oder höher, verfügbar und standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="93899-241">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="93899-242">[Turn on new CSS grid debugging features][DevtoolsCssGrid] ist jetzt in Microsoft Edge, Version 89 oder höher, verfügbar und standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="93899-242">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="93899-243">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] ist jetzt in Microsoft Edge, Version 90 oder höher, verfügbar und standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="93899-243">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 90 or later.</span></span>  

## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="93899-244">Bereitstellen von Feedback zu experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="93899-244">Providing feedback on experimental features</span></span>  

<span data-ttu-id="93899-245">So geben Sie Feedback zu Microsoft Edge DevTools-Experimenten oder zu anderen DevTools-Bezogenen.</span><span class="sxs-lookup"><span data-stu-id="93899-245">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="93899-246">Senden Sie Ihr Feedback mit dem **Symbol** Feedback senden in den DevTools</span><span class="sxs-lookup"><span data-stu-id="93899-246">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="93899-247">Tweet bei [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="93899-247">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol Feedback senden in den Microsoft Edge-Entwicklungstools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="93899-249">Das Symbol **Feedback senden** in den Microsoft Edge-Entwicklungstools</span><span class="sxs-lookup"><span data-stu-id="93899-249">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "3D-Ansicht | Microsoft Docs"  
[DevtoolsCssGrid]: ../css/grid.md "Inspect CSS Grid in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Tastenkombinationen für alle Aktionen in devTools bearbeiten | Microsoft Docs"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Tastenkombinationen in devTools mit Microsoft Visual Studio Code übereinstimmen | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simulieren mobiler Geräte mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich „Formatvorlagen“ in DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../issues/index.md "Erkennen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool „Probleme“ | Microsoft Docs"  
[DevtoolsOpenIndex]: ../open/index.md "Öffnen Sie Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Microsoft Edge DevTools-Tastenkombinationen | Microsoft Docs"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emulieren von Dualscreen- und faltbaren Geräten in Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  

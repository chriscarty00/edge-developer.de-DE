---
description: Das Tool "Neues" ist jetzt Willkommen, Visual Font Editor im Formatvorlagenbereich, CSS-Flexbox-Debugtools und vieles mehr.
title: Neues in DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: cfaee927d2d914cf0d816505ea2cf6b36a225d64
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313221"
---
# <span data-ttu-id="048e3-104">Neues in DevTools (Microsoft Edge 89)</span><span class="sxs-lookup"><span data-stu-id="048e3-104">What's New In DevTools (Microsoft Edge 89)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="048e3-105">What's New is now Welcome</span><span class="sxs-lookup"><span data-stu-id="048e3-105">What's New is now Welcome</span></span>  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="048e3-106">Das **Tool What's New** in den Microsoft Edge DevTools hat jetzt ein neues Erscheinungsbild und einen neuen Namen:  **Willkommen**.</span><span class="sxs-lookup"><span data-stu-id="048e3-106">The **What's New** tool in the Microsoft Edge DevTools now has a new appearance and a new name:  **Welcome**.</span></span>  <span data-ttu-id="048e3-107">Das **Willkommenstool** zeigt weiterhin die neuesten DevTools-News und -Updates an.</span><span class="sxs-lookup"><span data-stu-id="048e3-107">The **Welcome** tool still displays the latest DevTools news and updates.</span></span>  <span data-ttu-id="048e3-108">Es enthält jetzt auch Links zur Microsoft Edge DevTools-Dokumentation, Möglichkeiten zum Übermitteln von Feedback und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="048e3-108">It now also includes links to Microsoft Edge DevTools documentation, ways to submit feedback, and more.</span></span>  <span data-ttu-id="048e3-109">Zum Anzeigen des **Willkommenstools** nach jeder Aktualisierung von \*\*\*\* Microsoft Edge aktivieren Sie nach jeder Aktualisierung unter dem Titel das Kontrollkästchen neben der Registerkarte "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="048e3-109">To display the **Welcome** tool after each update to Microsoft Edge, choose the checkbox next to **Open tab after each update** under the title.</span></span>  <span data-ttu-id="048e3-110">Um das **Willkommenstool zu** schließen, wählen Sie das **X** auf der rechten Seite des Registerkartentitels aus.</span><span class="sxs-lookup"><span data-stu-id="048e3-110">To close the **Welcome** tool, choose the **X** on the right-side of the tab title.</span></span>  <span data-ttu-id="048e3-111">Wenn Sie das ursprüngliche Tool **"Was ist neu"** bevorzugen, navigieren Sie zu Einstellungsexperimente, und entfernen Sie das Kontrollkästchen neben der Registerkarte [][DevtoolsCustomizeIndexSettings]  >  \*\*\*\* **"Willkommen aktivieren".**</span><span class="sxs-lookup"><span data-stu-id="048e3-111">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="Das Willkommenstool ist hervorgehoben" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   <span data-ttu-id="048e3-113">Das **Willkommenstool** ist hervorgehoben</span><span class="sxs-lookup"><span data-stu-id="048e3-113">The **Welcome** tool is highlighted</span></span>  
:::image-end:::  

## <span data-ttu-id="048e3-114">Visual Font Editor im Formatvorlagenbereich</span><span class="sxs-lookup"><span data-stu-id="048e3-114">Visual Font Editor in the Styles pane</span></span>  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="048e3-115">Wenn Sie mit Schriftarten in CSS arbeiten, verwenden Sie den neuen visuellen [Schriftarten-Editor.][DevtoolsInspectStylesEditFonts]</span><span class="sxs-lookup"><span data-stu-id="048e3-115">When you work with fonts in CSS, use the new visual [Font Editor][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="048e3-116">Sie können Fallbackschriftarten definieren und Schieberegler verwenden, um Schriftgrad, Schriftgrad, Zeilenhöhe und Abstand zu definieren.</span><span class="sxs-lookup"><span data-stu-id="048e3-116">You may define fallback fonts, and use sliders to define font weight, size, line-height, and spacing.</span></span>  <span data-ttu-id="048e3-117">Mit **dem Schriftarten-Editor** können Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="048e3-117">The **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="048e3-118">Wechseln zwischen Einheiten für unterschiedliche Schriftarteigenschaften</span><span class="sxs-lookup"><span data-stu-id="048e3-118">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="048e3-119">Wechseln zwischen Schlüsselwörtern für unterschiedliche Schriftarteigenschaften</span><span class="sxs-lookup"><span data-stu-id="048e3-119">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="048e3-120">Einheiten konvertieren</span><span class="sxs-lookup"><span data-stu-id="048e3-120">Convert units</span></span>  
*   <span data-ttu-id="048e3-121">Generieren von genauem CSS-Code</span><span class="sxs-lookup"><span data-stu-id="048e3-121">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="048e3-122">Um dieses Experiment zu [][DevtoolsCustomizeIndexSettings]aktivieren, navigieren Sie zu Einstellungsexperimente, und aktivieren Sie das Kontrollkästchen neben "Neue Schriftarten-Editor-Tools  >  \*\*\*\* **im Formatvorlagenbereich aktivieren".**</span><span class="sxs-lookup"><span data-stu-id="048e3-122">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new Font Editor tools within Styles pane**.</span></span>  <span data-ttu-id="048e3-123">Weitere Informationen finden Sie unter "Bearbeiten von [CSS-Schriftartenformatvorlagen und -einstellungen" im Bereich "Formatvorlagen" in DevTools.][DevtoolsInspectStylesEditFonts]</span><span class="sxs-lookup"><span data-stu-id="048e3-123">For more information, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="048e3-124">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1093229][CR1093229].</span><span class="sxs-lookup"><span data-stu-id="048e3-124">To review the history of this feature in the Chromium open-source project, navigate to Issue [1093229][CR1093229].</span></span>  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="Der visuelle Schriftarten-Editor wird im Formatvorlagenbereich hervorgehoben." lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   <span data-ttu-id="048e3-126">Der visuelle **Schriftarten-Editor** wird im **Formatvorlagenbereich** hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="048e3-126">The visual **Font editor** is highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="048e3-127">CSS-Flexbox-Debugtools</span><span class="sxs-lookup"><span data-stu-id="048e3-127">CSS Flexbox debugging tools</span></span>  

<span data-ttu-id="048e3-128">Die Debugfeatures von Flexbox befinden sich in der aktiven Entwicklung.</span><span class="sxs-lookup"><span data-stu-id="048e3-128">Flexbox debugging features are in active development.</span></span>  <span data-ttu-id="048e3-129">Um das Experiment für die folgenden beiden [][DevtoolsCustomizeIndexSettings]Features zu aktivieren, navigieren Sie zu "Einstellungsexperimente", und aktivieren Sie das Kontrollkästchen neben "Neue  >  \*\*\*\* **CSS-Flexbox-Debugfeatures aktivieren".**</span><span class="sxs-lookup"><span data-stu-id="048e3-129">To turn on the experiment for the following two features, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new CSS Flexbox debugging features**.</span></span>  <span data-ttu-id="048e3-130">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problemen [1136394][CR1136394] und [1139949][CR1139949].</span><span class="sxs-lookup"><span data-stu-id="048e3-130">To review the history of this feature in the Chromium open-source project, navigate to Issues [1136394][CR1136394] and [1139949][CR1139949].</span></span>  

### <span data-ttu-id="048e3-131">Neue Flexbox (Flexbox)-Symbole helfen bei der Identifizierung und Anzeige von Flexcontainern</span><span class="sxs-lookup"><span data-stu-id="048e3-131">New Flexbox (flex) icon help identify and display flex containers</span></span>  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="048e3-132">Im **Elementtool** hilft Ihnen das neue Flexbox (Flex)-Symbol, Flexbox-Container in Ihrem Code zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="048e3-132">In the **Elements** tool, the new Flexbox (flex) icon helps you identify Flexbox containers in your code.</span></span>  <span data-ttu-id="048e3-133">Wählen Sie das Flexbox \(flex\)-Symbol aus, um den Überlagerungseffekt zu aktivieren oder zu deaktivieren, der einen Flexboxcontainer umriss.</span><span class="sxs-lookup"><span data-stu-id="048e3-133">Choose the Flexbox \(flex\) icon to turn on or off the overlay effect that outlines a Flexbox container.</span></span>  <span data-ttu-id="048e3-134">Sie können die Farbe der Überlagerung im **Layoutbereich** anpassen, der sich neben Formatvorlagen **und** **berechnet befindet.**</span><span class="sxs-lookup"><span data-stu-id="048e3-134">You may customize the color of the overlay in the **Layout** pane, which is located next to **Styles** and **Computed**.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="048e3-135">Um den Überlagerungseffekt, der den Container "Flexbox" umriss, ein- und auszuschalten, wählen Sie das Flexbox \( `flex` \)-Symbol aus.</span><span class="sxs-lookup"><span data-stu-id="048e3-135">To turn on and off the overlay effect that outlines the Flexbox container, choose the Flexbox \(`flex`\) icon.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="048e3-136">Sie können die Farbe der Überlagerung im **Layoutbereich** neben **Formatvorlagen** und berechnet **anpassen.**</span><span class="sxs-lookup"><span data-stu-id="048e3-136">You may customize the color of the overlay in the **Layout** pane next to **Styles** and **Computed**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Das Flexbox (Flex)-Symbol und die hervorgehobene Webseite" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         <span data-ttu-id="048e3-138">Das **Flexbox** \( `flex` \)-Symbol und die hervorgehobene Webseite</span><span class="sxs-lookup"><span data-stu-id="048e3-138">The **Flexbox** \(`flex`\) icon and webpage highlighted</span></span> :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Die im Layoutbereich hervorgehobenen Flexbox-Überlagerungen" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         <span data-ttu-id="048e3-140">Die **im Layoutbereich hervorgehobenen Flexbox-Überlagerungen** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="048e3-140">The **Flexbox overlays** highlighted in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="048e3-141">Anzeigen von Ausrichtungssymbolen und Gitternetzlinien, wenn sich die Layouts von Flexbox mithilfe von CSS-Eigenschaften ändern</span><span class="sxs-lookup"><span data-stu-id="048e3-141">Display alignment icons and gridlines when Flexbox layouts change using CSS properties</span></span>  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="048e3-142">Wenn Sie CSS für Ihr Flexboxlayout bearbeiten, \*\*\*\* werden bei automatischen CSS-Completes im Formatvorlagenbereich jetzt hilfreiche Symbole neben relevanten Flexbox-Eigenschaften angezeigt.</span><span class="sxs-lookup"><span data-stu-id="048e3-142">When you edit CSS for your Flexbox layout, CSS autocompletes in the **Styles** pane now displays helpful icons next to relevant Flexbox properties.</span></span>  <span data-ttu-id="048e3-143">Öffnen Sie zum Testen dieses neuen Features das **Elementtool,** und wählen Sie einen Flexcontainer aus.</span><span class="sxs-lookup"><span data-stu-id="048e3-143">To try this new feature, open the **Elements** tool and select a flex container.</span></span>  <span data-ttu-id="048e3-144">Fügen Sie dann eine Eigenschaft für den Container im Formatvorlagenbereich hinzu oder ändern Sie **sie.**</span><span class="sxs-lookup"><span data-stu-id="048e3-144">Then add or change a property on that container in the **Styles** pane.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="048e3-145">Im Menü "AutoVervollständigung" werden jetzt Symbole angezeigt, die die Auswirkung von Ausrichtungseigenschaften wie und `align-content` `align-items` angeben.</span><span class="sxs-lookup"><span data-stu-id="048e3-145">The autocomplete menu now displays icons that indicate the effect of alignment properties such as `align-content` and `align-items`.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="048e3-146">Darüber hinaus zeigt DevTools jetzt eine Leitlinie an, damit Sie die EIGENSCHAFT `align-items` CSS besser überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="048e3-146">Additionally, DevTools now displays a guiding line to help you better review the `align-items` CSS property.</span></span>  <span data-ttu-id="048e3-147">Die `gap` CSS-Eigenschaft wird ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="048e3-147">The `gap` CSS property is supported as well.</span></span>  <span data-ttu-id="048e3-148">In der folgenden Abbildung wird die Eigenschaft CSS festgelegt, und das Schraffierungsmuster für `gap` `gap: 12px;` jede Lücke wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="048e3-148">In the following figure, the `gap` CSS property is set to `gap: 12px;` and the hatching pattern for each gap is displayed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Das Menü "AutoVervollständigung" ist für CSS-Eigenschaften hervorgehoben, die mit ausrichtungs-" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         <span data-ttu-id="048e3-150">Menü "AutoVervollständigung" für CSS-Eigenschaften, die mit</span><span class="sxs-lookup"><span data-stu-id="048e3-150">Autocomplete menu highlighted for CSS properties that start with</span></span> `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Flexboxlücke in CSS-Eigenschaften und hervorgehobener Webseite" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         <span data-ttu-id="048e3-152">Flexbox `gap` in CSS-Eigenschaften und hervorgehobener Webseite</span><span class="sxs-lookup"><span data-stu-id="048e3-152">Flexbox `gap` in CSS properties and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="048e3-153">Schnelles Hinzufügen von Tools mit der neuen Schaltfläche "Weitere Tools"</span><span class="sxs-lookup"><span data-stu-id="048e3-153">Add tools quickly with new More Tools button</span></span>  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="048e3-154">Sie haben nun eine neue Möglichkeit, weitere Tools in den Microsoft Edge DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="048e3-154">You now have a new way to open more tools in the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="048e3-155">Nachdem Sie dieses Experiment aktivieren, wird das Symbol "Weitere **Tools"** rechts neben dem Hauptbereich als Pluszeichen ( `+` ) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="048e3-155">After you turn on this experiment, the **More Tools** icon displays as a plus sign (`+`) to the right of the main panel.</span></span>  <span data-ttu-id="048e3-156">Wenn Sie eine Liste mit anderen Tools anzeigen möchten, die dem Hauptbereich hinzugefügt werden, klicken Sie auf das Symbol "Weitere **Tools\(** `+` \)".</span><span class="sxs-lookup"><span data-stu-id="048e3-156">To display a list of other tools to add to the main panel, choose the **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="048e3-157">Um dieses Experiment zu [][DevtoolsCustomizeIndexSettings]aktivieren, navigieren Sie zu "Einstellungsexperimente", und aktivieren Sie dann das Kontrollkästchen neben den  >  \*\*\*\* Registerkartenmenüs "Aktivieren+ "Schaltfläche", um **weitere Tools zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="048e3-157">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**, and then choose the checkbox next to **Enable + button tab menus to open more tools**.</span></span>  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Weitere In DevTools hervorgehobene Tools" lightbox="../../media/2021/01/more-tools.msft.png":::
   <span data-ttu-id="048e3-159">**Weitere In** DevTools hervorgehobene Tools</span><span class="sxs-lookup"><span data-stu-id="048e3-159">**More Tools** highlighted in DevTools</span></span>  
:::image-end:::  

## <span data-ttu-id="048e3-160">Hilfstechnologien melden jetzt Position und Anzahl der CSS-Vorschläge.</span><span class="sxs-lookup"><span data-stu-id="048e3-160">Assistive technologies now announce position and count of CSS suggestions</span></span>  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

<span data-ttu-id="048e3-161">Wenn Sie CSS bearbeiten, erhalten Sie eine Dropdownliste mit Features.</span><span class="sxs-lookup"><span data-stu-id="048e3-161">When you edit CSS, you get a dropdown of features.</span></span>  <span data-ttu-id="048e3-162">Dieses Feature war für Benutzer von Hilfstechnologien nicht verfügbar, da es in Microsoft Edge, Version 89, angekündigt wurde.</span><span class="sxs-lookup"><span data-stu-id="048e3-162">This feature was not available to users of assistive technologies, since it is announced in Microsoft Edge version 89.</span></span>  <span data-ttu-id="048e3-163">Ein Benutzer von Hilfstechnologien kann nun im Formatvorlagenbereich durch die Vorschläge von **CSS** navigieren.</span><span class="sxs-lookup"><span data-stu-id="048e3-163">A user of assistive technologies may now navigate CSS suggestions in the **Styles** pane.</span></span>  <span data-ttu-id="048e3-164">In Microsoft Edge, Version 88 und früher, hat die als Benutzer angekündigte Hilfstechnologie beim Bearbeiten von CSS im Formatvorlagenbereich durch die Liste der Vorschläge `Suggestion` navigiert. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="048e3-164">In Microsoft Edge version 88 and earlier, assistive technology announced `Suggestion` as a user navigated through the list of suggestions when editing CSS in the **Styles** pane.</span></span>  <span data-ttu-id="048e3-165">In Microsoft Edge, Version 89, hört ein Benutzer der Hilfstechnologie jetzt die Position und Anzahl des aktuellen Vorschlags.</span><span class="sxs-lookup"><span data-stu-id="048e3-165">In Microsoft Edge version 89, a user of assistive technology now hears the position and count of the current suggestion.</span></span>  <span data-ttu-id="048e3-166">Jeder Vorschlag wird angekündigt, wenn der Benutzer durch die Liste der Vorschläge navigiert, z. B. Vorschlag 3 von 5.</span><span class="sxs-lookup"><span data-stu-id="048e3-166">Each suggestion is announced as the user navigates through the list of suggestions, such as Suggestion 3 of 5.</span></span>  <span data-ttu-id="048e3-167">Um mehr über das Schreiben von CSS in devTools zu erfahren, navigieren Sie zu [CSS ändern.][DevtoolsCssReferenceChangeCss]</span><span class="sxs-lookup"><span data-stu-id="048e3-167">To learn more about writing CSS in the DevTools, navigate to [Change CSS][DevtoolsCssReferenceChangeCss].</span></span>  <span data-ttu-id="048e3-168">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1157329][CR1157329].</span><span class="sxs-lookup"><span data-stu-id="048e3-168">To review the history of this feature in the Chromium open-source project, navigate to Issue [1157329][CR1157329].</span></span>  

<!--To view a video that displays and reads aloud several suggestions with this experiment turned on, navigate to [Voiceover announcing devtools options](https://youtu.be/9TcUpleEwwA) on YouTube.  -->  

<span data-ttu-id="048e3-169">Der folgende Videolink zeigt mehrere Vorschläge an und liest sie laut vor, wenn dieses Experiment aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="048e3-169">The following video link displays and reads aloud several suggestions with this experiment turned on.</span></span>  

> [!VIDEO https://youtu.be/9TcUpleEwwA]  

## <span data-ttu-id="048e3-170">Emulieren von Surface Duo und Samsung Fold</span><span class="sxs-lookup"><span data-stu-id="048e3-170">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

<span data-ttu-id="048e3-171">Testen Sie die Darstellung Ihrer Website oder App auf den folgenden Geräten in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="048e3-171">Test the appearance of your website or app on the following devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="048e3-172">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="048e3-172">Surface Duo</span></span>][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [<span data-ttu-id="048e3-173">Samsung Verknappung</span><span class="sxs-lookup"><span data-stu-id="048e3-173">Samsung Galaxy Fold</span></span>][SamsungUsMobileGalaxyFold]  
    
<span data-ttu-id="048e3-174">Aktivieren Sie **experimentelle Webplattformfeatures,** um auf das neue Feature für medienübergreifende [CSS-Medien][DualScreenWebCssMediaSpanning] zu zugreifen und die [JavaScript-API "getWindowSegments" zu erhalten.][DualScreenWebJavascriptGetwindowsegments]</span><span class="sxs-lookup"><span data-stu-id="048e3-174">Turn on **Experimental Web Platform features** to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [getWindowSegments JavaScript API][DualScreenWebJavascriptGetwindowsegments].</span></span>  <span data-ttu-id="048e3-175">Navigieren Sie zu dem Flag neben den Features der `edge://flags` **experimentellen Webplattform, und**schalten Sie es um.</span><span class="sxs-lookup"><span data-stu-id="048e3-175">Navigate to `edge://flags` and toggle the flag next to **Experimental Web Platform features**.</span></span>  <span data-ttu-id="048e3-176">Verwenden Sie die folgenden Features beim Emulieren des Geräts, um Ihre Website oder App für den dualen Bildschirm und die ausklappbaren [Geräte zu verbessern.][DevtoolsDeviceModeIndex]</span><span class="sxs-lookup"><span data-stu-id="048e3-176">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="048e3-177">[Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], d. h. wenn Ihre Website \(oder App\) auf beiden Bildschirmen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="048e3-177">[Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>  
*   <span data-ttu-id="048e3-178">[Rendern der Naht][DualScreenIntroductionHowToWorkWithSeam], die den Abstand zwischen den beiden Bildschirmen ist.</span><span class="sxs-lookup"><span data-stu-id="048e3-178">[Rendering the seam][DualScreenIntroductionHowToWorkWithSeam], which is the space between the two screens.</span></span>  
    
<span data-ttu-id="048e3-179">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1054281][CR1054281].</span><span class="sxs-lookup"><span data-stu-id="048e3-179">To review the history of this feature in the Chromium open-source project, navigate to Issue [1054281][CR1054281].</span></span>  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Emulieren des dualen Bildschirms" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   <span data-ttu-id="048e3-181">Emulieren des dualen Bildschirms</span><span class="sxs-lookup"><span data-stu-id="048e3-181">Emulate dual-screen</span></span>  
:::image-end:::  

## <span data-ttu-id="048e3-182">Microsoft Edge Developer Tools for Visual Studio Code Version 1.1.2</span><span class="sxs-lookup"><span data-stu-id="048e3-182">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.2</span></span>  

<span data-ttu-id="048e3-183">Die [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.2 for Microsoft Visual Studio Code hat die folgenden Änderungen seit der vorherigen Version.</span><span class="sxs-lookup"><span data-stu-id="048e3-183">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.2 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="048e3-184">Microsoft Visual Studio Code aktualisiert Erweiterungen automatisch.</span><span class="sxs-lookup"><span data-stu-id="048e3-184">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="048e3-185">Um manuell auf Version 1.1.2 zu aktualisieren, navigieren Sie zu ["Erweiterung manuell aktualisieren".][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="048e3-185">To manually update to version 1.1.2, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  

*   <span data-ttu-id="048e3-186">Schaltfläche **"Instanz schließen"** zu jedem Element in der Zielliste \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="048e3-186">Added a **Close instance** button to each item on the target list \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span></span>  
*   <span data-ttu-id="048e3-187">Microsoft [Edge DevTools][DevtoolsMain] Version von 84.0.522.63 auf [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span><span class="sxs-lookup"><span data-stu-id="048e3-187">Bumped [Microsoft Edge DevTools][DevtoolsMain] version from 84.0.522.63 to [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span></span>  
*   <span data-ttu-id="048e3-188">Enthaltener [Debugger für Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] als Abhängigkeit \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span><span class="sxs-lookup"><span data-stu-id="048e3-188">Included [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] as a dependency  \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span></span>  
*   <span data-ttu-id="048e3-189">Implementierte Einstellungsoption zum Ändern von Erweiterungsthemen \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span><span class="sxs-lookup"><span data-stu-id="048e3-189">Implemented settings option to change extension themes \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span></span>  
    
<span data-ttu-id="048e3-190">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="048e3-190">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

## <span data-ttu-id="048e3-191">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="048e3-191">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="048e3-192">Screenshot des Aufnahmeknotens über Viewport hinaus</span><span class="sxs-lookup"><span data-stu-id="048e3-192">Capture node screenshot beyond viewport</span></span>  

<span data-ttu-id="048e3-193">In Microsoft Edge, Version 89, sind Knotenscreenshots genauer und erfassen den vollständigen Knoten, auch wenn der Inhalt des Knotens nicht im Viewport sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="048e3-193">In Microsoft Edge version 89, node screenshots are more accurate, capturing the full node even if content from the node is not visible in the viewport.</span></span>  <span data-ttu-id="048e3-194">Zeigen Sie **im Tool "Elemente"** auf ein Element, öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie Screenshot des **Aufnahmeknotens aus.**</span><span class="sxs-lookup"><span data-stu-id="048e3-194">In the **Elements** tool, hover  on an element, open the contextual menu \(right-click\), and choose **Capture node screenshot**.</span></span>  <span data-ttu-id="048e3-195">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1003629][CR1003629].</span><span class="sxs-lookup"><span data-stu-id="048e3-195">To review the history of this feature in the Chromium open-source project, navigate to Issue [1003629][CR1003629].</span></span>  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Screenshot des Aufnahmeknotens im Kontextmenü im Tool "Elemente"" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   <span data-ttu-id="048e3-197">**Screenshot des Aufnahmeknotens** im Kontextmenü im Tool **"Elemente"**</span><span class="sxs-lookup"><span data-stu-id="048e3-197">**Capture node screenshot** highlighted on the context menu in the **Elements** tool</span></span>  
:::image-end:::  

### <span data-ttu-id="048e3-198">Elementtoolupdates</span><span class="sxs-lookup"><span data-stu-id="048e3-198">Elements tool updates</span></span>  

#### <span data-ttu-id="048e3-199">Unterstützung der Erzwingung des :target-CSS-Status</span><span class="sxs-lookup"><span data-stu-id="048e3-199">Support forcing the :target CSS state</span></span>  

<span data-ttu-id="048e3-200">Sie können jetzt DevTools [][MdnDocsWebCssTarget] verwenden, um die :target-CSS-Pseudoklasse zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="048e3-200">You may now use DevTools to force the [:target][MdnDocsWebCssTarget] CSS pseudo-class.</span></span>  <span data-ttu-id="048e3-201">Die Pseudoklasse wird ausgelöst, wenn ein eindeutiges Element \(das Zielelement\) über ein Element verfügt, das einem `:target` `id` Fragment der URL entspricht.</span><span class="sxs-lookup"><span data-stu-id="048e3-201">The `:target` pseudo-class is triggered when a unique element \(the target element\) has an `id` that matches a fragment of the URL.</span></span>  <span data-ttu-id="048e3-202">Beispielsweise löst die URL die Pseudoklasse für `http://www.example.com/index.html#section1` ein `:target` HTML-Element mit `id="section1"` aus.</span><span class="sxs-lookup"><span data-stu-id="048e3-202">For example, the `http://www.example.com/index.html#section1` URL triggers the `:target` pseudo-class on an HTML element with `id="section1"`.</span></span>  <span data-ttu-id="048e3-203">To try a demo with section 1 highlighted, navigate to [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span><span class="sxs-lookup"><span data-stu-id="048e3-203">To try a demo with section 1 highlighted, navigate to [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span></span>  <span data-ttu-id="048e3-204">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1156628][CR1156628].</span><span class="sxs-lookup"><span data-stu-id="048e3-204">To review the history of this feature in the Chromium open-source project, navigate to Issue [1156628][CR1156628].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Die Webseite ohne erzwungene CSS hervorgehoben" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         <span data-ttu-id="048e3-206">Webseite ohne erzwungene CSS hervorgehoben</span><span class="sxs-lookup"><span data-stu-id="048e3-206">Webpage highlighted with no forced CSS</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS forced and webpage highlighted" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` <span data-ttu-id="048e3-208">CSS erzwungen und Webseite hervorgehoben</span><span class="sxs-lookup"><span data-stu-id="048e3-208">CSS forced and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="048e3-209">Verwenden doppelter Elemente zum Kopieren von Elementen</span><span class="sxs-lookup"><span data-stu-id="048e3-209">Use Duplicate elements to copy elements</span></span>  

<span data-ttu-id="048e3-210">Verwenden Sie die neue **Verknüpfung "Duplicate"-Element,** um ein Element zu klonen.</span><span class="sxs-lookup"><span data-stu-id="048e3-210">Use the new **Duplicate element** shortcut to clone an element.</span></span>  <span data-ttu-id="048e3-211">Zeigen Sie **im Elementtool** auf ein Element, öffnen Sie das Kontextmenü \(rechtsklick\), wählen Sie **"Duplizieren" aus.**</span><span class="sxs-lookup"><span data-stu-id="048e3-211">In the **Elements** tool, hover on an element, open the contextual menu \(right-click\), choose **Duplicate element**.</span></span>  <span data-ttu-id="048e3-212">Unter dem ausgewählten Element wird ein neues Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="048e3-212">A new element is created under the selected element.</span></span>  <span data-ttu-id="048e3-213">Um das Element mit einer Tastenkombination zu duplizieren, wählen `Shift` + `Alt` + `Down Arrow` Sie \(Windows/Linux\) oder `Shift` + `Option` + `Down Arrow` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="048e3-213">To duplicate the element with a keyboard shortcut, select `Shift`+`Alt`+`Down Arrow` \(Windows/Linux\) or `Shift`+`Option`+`Down Arrow` \(macOS\).</span></span>  <span data-ttu-id="048e3-214">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1150797][CR1150797].</span><span class="sxs-lookup"><span data-stu-id="048e3-214">To review the history of this feature in the Chromium open-source project, navigate to Issue [1150797][CR1150797].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="Das Element "Duplicate" wird im Kontextmenü eines Elements im Tool "Elemente" hervorgehoben." lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   <span data-ttu-id="048e3-216">Das **Element "Duplicate"** wird im Kontextmenü eines Elements im Tool **"Elemente"** hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="048e3-216">The **Duplicate element** is highlighted in the context menu on an element in the **Elements** tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="048e3-217">Farbauswahl für benutzerdefinierte CSS-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="048e3-217">Color pickers for custom CSS properties</span></span>  

<span data-ttu-id="048e3-218">Im **Formatvorlagenbereich** werden nun Farbauswahlen für benutzerdefinierte CSS-Eigenschaften angezeigt.</span><span class="sxs-lookup"><span data-stu-id="048e3-218">The **Styles** pane now displays color pickers for custom CSS properties.</span></span>  <span data-ttu-id="048e3-219">Um die RGBA-, HSLA- und Hexadezimalformate des Farbwerts zu durchzyklen, halten Sie die Farbauswahl und `Shift` wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="048e3-219">To cycle through the RGBA, HSLA, and Hex formats of the color value, hold `Shift` and choose the color picker.</span></span>  <span data-ttu-id="048e3-220">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1147016][CR1147016].</span><span class="sxs-lookup"><span data-stu-id="048e3-220">To review the history of this feature in the Chromium open-source project, navigate to Issue [1147016][CR1147016].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Farbauswahl für benutzerdefinierte CSS-Eigenschaften" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   <span data-ttu-id="048e3-222">Farbauswahl für benutzerdefinierte CSS-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="048e3-222">Color pickers for custom CSS properties</span></span>  
:::image-end:::  

#### <span data-ttu-id="048e3-223">Kopieren von CSS-Klassen und -Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="048e3-223">Copy CSS classes and properties</span></span>  

<span data-ttu-id="048e3-224">Sie können jetzt mit ein paar neuen Optionen im Kontextmenü die CSS-Eigenschaften schneller kopieren.</span><span class="sxs-lookup"><span data-stu-id="048e3-224">You may now copy CSS properties quicker with a few new options in the contextual menu.</span></span>  <span data-ttu-id="048e3-225">Wählen Sie **im Tool "Elemente"** ein Element aus.</span><span class="sxs-lookup"><span data-stu-id="048e3-225">In the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="048e3-226">Um den Wert zu \*\*\*\* kopieren, zeigen Sie im Formatvorlagenbereich auf eine CSS-Klasse oder eine CSS-Eigenschaft, öffnen Sie ein Kontextmenü \(rechtsklick\), und wählen Sie die Kopieroption aus.</span><span class="sxs-lookup"><span data-stu-id="048e3-226">To copy the value, in the **Styles** pane, hover on a CSS class or a CSS property, open a contextual menu \(right-click\), and choose the copy option.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="048e3-227">Kopieren von Optionen für eine CSS-Klasse.</span><span class="sxs-lookup"><span data-stu-id="048e3-227">Copy options for a CSS class.</span></span>  
      
      | <span data-ttu-id="048e3-228">Option</span><span class="sxs-lookup"><span data-stu-id="048e3-228">Option</span></span> | <span data-ttu-id="048e3-229">Details</span><span class="sxs-lookup"><span data-stu-id="048e3-229">Details</span></span> |  
      |:--- |:--- |  
      | **<span data-ttu-id="048e3-230">Auswahl kopieren</span><span class="sxs-lookup"><span data-stu-id="048e3-230">Copy selector</span></span>** | <span data-ttu-id="048e3-231">Kopieren Sie den aktuellen Selektornamen.</span><span class="sxs-lookup"><span data-stu-id="048e3-231">Copy the current selector name.</span></span> |  
      | **<span data-ttu-id="048e3-232">Kopierregel</span><span class="sxs-lookup"><span data-stu-id="048e3-232">Copy rule</span></span>** | <span data-ttu-id="048e3-233">Kopieren Sie die Regel des aktuellen Selektors.</span><span class="sxs-lookup"><span data-stu-id="048e3-233">Copy the rule of the current selector.</span></span> |  
      | **<span data-ttu-id="048e3-234">Kopieren aller Deklarationen</span><span class="sxs-lookup"><span data-stu-id="048e3-234">Copy all declarations</span></span>** | <span data-ttu-id="048e3-235">Kopieren Sie alle Deklarationen unter der aktuellen Regel, einschließlich nicht gültiger Und Präfixeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="048e3-235">Copy all declarations under the current rule, including non-valid and prefixed properties.</span></span> |  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="048e3-236">Kopieren von Optionen für eine CSS-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="048e3-236">Copy options for a CSS property.</span></span>  
      
      | <span data-ttu-id="048e3-237">Option</span><span class="sxs-lookup"><span data-stu-id="048e3-237">Option</span></span> | <span data-ttu-id="048e3-238">Details</span><span class="sxs-lookup"><span data-stu-id="048e3-238">Details</span></span> |      
      |:--- |:--- |  
      | **<span data-ttu-id="048e3-239">Kopieren der Deklaration</span><span class="sxs-lookup"><span data-stu-id="048e3-239">Copy declaration</span></span>** | <span data-ttu-id="048e3-240">Kopieren Sie die Deklaration der aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="048e3-240">Copy the declaration of the current line.</span></span> |  
      | **<span data-ttu-id="048e3-241">Eigenschaft "Copy"</span><span class="sxs-lookup"><span data-stu-id="048e3-241">Copy property</span></span>** | <span data-ttu-id="048e3-242">Kopieren Sie die Eigenschaft der aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="048e3-242">Copy the property of the current line.</span></span> |  
      | **<span data-ttu-id="048e3-243">Kopierwert</span><span class="sxs-lookup"><span data-stu-id="048e3-243">Copy value</span></span>** | <span data-ttu-id="048e3-244">Kopieren Sie den Wert der aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="048e3-244">Copy the value of the current line.</span></span> |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Kopieren von Optionen für eine CSS-Klasse im Kontextmenü" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         <span data-ttu-id="048e3-246">Kopieren von Optionen für eine CSS-Klasse im Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="048e3-246">Copy options for a CSS class in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Kopieren von Optionen für eine CSS-Eigenschaft im Kontextmenü" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         <span data-ttu-id="048e3-248">Kopieren von Optionen für eine CSS-Eigenschaft im Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="048e3-248">Copy options for a CSS property in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="048e3-249">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1152391][CR1152391].</span><span class="sxs-lookup"><span data-stu-id="048e3-249">To review the history of this feature in the Chromium open-source project, navigate to Issue [1152391][CR1152391].</span></span>  

### <span data-ttu-id="048e3-250">Cookiesupdates</span><span class="sxs-lookup"><span data-stu-id="048e3-250">Cookies updates</span></span>  

#### <span data-ttu-id="048e3-251">Neue Option zum Anzeigen von URL-decodierten Cookies</span><span class="sxs-lookup"><span data-stu-id="048e3-251">New option to display URL-decoded cookies</span></span>  

<span data-ttu-id="048e3-252">Sie können jetzt den Wert für URL-decodierte Cookies im Bereich **"Cookies"** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="048e3-252">You may now opt to display the URL-decoded cookies value in the **Cookies** pane.</span></span>  <span data-ttu-id="048e3-253">Um das decodierte Cookie \*\*\*\* anzuzeigen, navigieren Sie zum Bereich "Anwendungscookies", wählen Sie ein beliebiges Cookie in der Liste aus, und aktivieren Sie das Kontrollkästchen neben  >  \*\*\*\* **decodierte URL anzeigen.**</span><span class="sxs-lookup"><span data-stu-id="048e3-253">To display the decoded cookie, navigate to **Application** > **Cookies** pane, choose any cookie on the list, and choose the checkbox next to **Show URL decoded**.</span></span>  <span data-ttu-id="048e3-254">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [997625][CR997625].</span><span class="sxs-lookup"><span data-stu-id="048e3-254">To review the history of this feature in the Chromium open-source project, navigate to Issue [997625][CR997625].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Option zum Anzeigen von URL-decodierten Cookies" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   <span data-ttu-id="048e3-256">Option zum Anzeigen von URL-decodierten Cookies</span><span class="sxs-lookup"><span data-stu-id="048e3-256">Option to display URL decoded cookies</span></span>  
:::image-end:::  

#### <span data-ttu-id="048e3-257">Filtern und Löschen sichtbarer Cookies</span><span class="sxs-lookup"><span data-stu-id="048e3-257">Filter and clear visible cookies</span></span>  

<span data-ttu-id="048e3-258">In Microsoft Edge version 88 or earlier, the **Application** tool only provided a way to clear all cookies with the **Clear all cookies** button.</span><span class="sxs-lookup"><span data-stu-id="048e3-258">In Microsoft Edge version 88 or earlier, the **Application** tool only provided a way to clear all cookies with the **Clear all cookies** button.</span></span>  <span data-ttu-id="048e3-259">In Microsoft Edge, Version 89, können Sie nun "Gefilterte Cookies **löschen"** auswählen, um nur die gefilterten Cookies zu löschen.</span><span class="sxs-lookup"><span data-stu-id="048e3-259">In Microsoft Edge version 89, you may now choose **Clear filtered cookies** to delete only the filtered cookies.</span></span>  <span data-ttu-id="048e3-260">Um Cookies zu filtern, navigieren Sie zu **"Anwendungscookies",**  >  \*\*\*\* und geben Sie das Textfeld **"Filter"** ein.</span><span class="sxs-lookup"><span data-stu-id="048e3-260">To filter cookies, navigate to **Application** > **Cookies**, and type in the **Filter** textbox.</span></span>  <span data-ttu-id="048e3-261">Um die angezeigten Cookies zu löschen, wählen Sie die Schaltfläche **"Gefilterte Cookies löschen"** aus.</span><span class="sxs-lookup"><span data-stu-id="048e3-261">To delete the displayed cookies, choose the **Clear filtered cookies** button.</span></span>  <span data-ttu-id="048e3-262">Löschen Sie den Filtertext, um alle anderen Cookies anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="048e3-262">To display all other cookies, clear the filter text.</span></span>  <span data-ttu-id="048e3-263">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [978059][CR978059].</span><span class="sxs-lookup"><span data-stu-id="048e3-263">To review the history of this feature in the Chromium open-source project, navigate to Issue [978059][CR978059].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Nur sichtbare Cookies löschen" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   <span data-ttu-id="048e3-265">Nur sichtbare Cookies löschen</span><span class="sxs-lookup"><span data-stu-id="048e3-265">Clear only visible cookies</span></span>  
:::image-end:::  

#### <span data-ttu-id="048e3-266">Neue Option zum Löschen von Drittanbietercookies im Speicherbereich</span><span class="sxs-lookup"><span data-stu-id="048e3-266">New option to clear third-party cookies in the Storage pane</span></span>  

<span data-ttu-id="048e3-267">DevTools löschen jetzt standardmäßig nur Cookies von Erstparteiern.</span><span class="sxs-lookup"><span data-stu-id="048e3-267">DevTools now clear only first-party cookies by default.</span></span>  <span data-ttu-id="048e3-268">Wenn Sie nur Websitedaten und Erstplatziertcookies löschen möchten, navigieren Sie zum **Anwendungsspeicher,** und wählen Sie  >  \*\*\*\* dann **"Websitedaten löschen" aus.**</span><span class="sxs-lookup"><span data-stu-id="048e3-268">To clear website data and first-party cookies only, navigate to **Application** > **Storage**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="048e3-269">Navigieren Sie zum Anwendungsspeicher, \*\*\*\* um Websitedaten und alle Cookies  >  **zu löschen.**</span><span class="sxs-lookup"><span data-stu-id="048e3-269">To clear website data and all cookies, navigate to **Application** > **Storage**.</span></span>  <span data-ttu-id="048e3-270">Aktivieren Sie das Kontrollkästchen neben **Cookies**von Drittanbietern, und wählen Sie dann **"Websitedaten löschen" aus.**</span><span class="sxs-lookup"><span data-stu-id="048e3-270">Choose the checkbox next to **including third-party cookies**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="048e3-271">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1012337][CR1012337].</span><span class="sxs-lookup"><span data-stu-id="048e3-271">To review the history of this feature in the Chromium open-source project, navigate to Issue [1012337][CR1012337].</span></span>  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Option zum Löschen von Cookies von Drittanbietern" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   <span data-ttu-id="048e3-273">Option zum Löschen von Cookies von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="048e3-273">Option to clear third-party cookies</span></span>  
:::image-end:::  

### <span data-ttu-id="048e3-274">Netzwerktoolupdates</span><span class="sxs-lookup"><span data-stu-id="048e3-274">Network tool updates</span></span>  

#### <span data-ttu-id="048e3-275">Netzwerkprotokolleinstellung für "Datensatz beibehalten"</span><span class="sxs-lookup"><span data-stu-id="048e3-275">Persist Record network log setting</span></span>  

<span data-ttu-id="048e3-276">In Microsoft Edge, Version 88 oder \*\*\*\* früher, setzen DevTools die Protokolleinstellung "Protokoll aufzeichnen" zurück, wenn eine Webseite aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="048e3-276">In Microsoft Edge version 88 or earlier, DevTools reset the **Record network log** setting when a webpage refreshes.</span></span>  <span data-ttu-id="048e3-277">In Microsoft Edge, Version 89, werden die Protokolleinstellungen des Datensatznetzwerks von DevTools **beibehalten.**</span><span class="sxs-lookup"><span data-stu-id="048e3-277">In Microsoft Edge version 89, DevTools now persist the **Record network log** setting.</span></span>  <span data-ttu-id="048e3-278">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1122580][CR1122580].</span><span class="sxs-lookup"><span data-stu-id="048e3-278">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122580][CR1122580].</span></span>  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Aufzeichnen des Netzwerkprotokolls" lightbox="../../media/2021/01/network-log.msft.png":::
   <span data-ttu-id="048e3-280">Aufzeichnen des Netzwerkprotokolls</span><span class="sxs-lookup"><span data-stu-id="048e3-280">Record network log</span></span>  
:::image-end:::  

#### <span data-ttu-id="048e3-281">Onlineoption ist jetzt keine Einschränkungsoption</span><span class="sxs-lookup"><span data-stu-id="048e3-281">Online option is now No throttling option</span></span>  

<span data-ttu-id="048e3-282">Die Netzwerkemulationsoption **Online** wurde jetzt in **"No Throttling" umbenannt.**</span><span class="sxs-lookup"><span data-stu-id="048e3-282">The network emulation option **Online** is now renamed to **No Throttling**.</span></span>  <span data-ttu-id="048e3-283">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1028078][CR1028078].</span><span class="sxs-lookup"><span data-stu-id="048e3-283">To review the history of this feature in the Chromium open-source project, navigate to Issue [1028078][CR1028078].</span></span>  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Keine Einschränkungsoption" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   <span data-ttu-id="048e3-285">**Keine Einschränkungsoption**</span><span class="sxs-lookup"><span data-stu-id="048e3-285">**No throttling** option</span></span>  
:::image-end:::  

### <span data-ttu-id="048e3-286">Neue Kopieroptionen im Konsolentool, im Quellentool und im Formatvorlagenbereich</span><span class="sxs-lookup"><span data-stu-id="048e3-286">New copy options in the Console tool, Sources tool, and Styles pane</span></span>

#### <span data-ttu-id="048e3-287">Kopieren eines Objekts im Konsolen- und Quellentool</span><span class="sxs-lookup"><span data-stu-id="048e3-287">Copy object in the Console and Sources tool</span></span>  

<span data-ttu-id="048e3-288">Sie können nun Objektwerte in die **Konsolen-** und **Quellentools** kopieren.</span><span class="sxs-lookup"><span data-stu-id="048e3-288">You may now copy object values in the **Console** and **Sources** tools.</span></span>  <span data-ttu-id="048e3-289">Die Möglichkeit, Objektwerte zu kopieren, ist beim Arbeiten mit großen Objekten hilfreich.</span><span class="sxs-lookup"><span data-stu-id="048e3-289">The ability to copy object values is useful when working with large objects.</span></span>  <span data-ttu-id="048e3-290">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problemen [1148353][CR1148353] und [1149859][CR1149859].</span><span class="sxs-lookup"><span data-stu-id="048e3-290">To review the history of this feature in the Chromium open-source project, navigate to Issues [1148353][CR1148353] and [1149859][CR1149859].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="048e3-291">Zeigen Sie **im Konsolentool** auf ein Objekt, öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie dann **"Objekt kopieren" aus.**</span><span class="sxs-lookup"><span data-stu-id="048e3-291">In the **Console** tool, hover on an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="048e3-292">Zeigen \*\*\*\* Sie im Tool Quellen auf einem Haltepunkt auf ein Objekt, markieren Sie im Popupfenster Objekt ein Objekt, öffnen Sie das Kontextmenü \(rechtsklick\ ), und wählen Sie dann Objekt kopieren aus. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="048e3-292">In the **Sources** tool, on a breakpoint, hover on an object, in the **Object** popup window, highlight an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Kopieren des Objekts in der Konsole" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         <span data-ttu-id="048e3-294">Kopieren des Objekts in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="048e3-294">Copy object in the **Console**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Objekt in "Sources" kopieren" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         <span data-ttu-id="048e3-296">Objekt in **"Sources" kopieren**</span><span class="sxs-lookup"><span data-stu-id="048e3-296">Copy object in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="048e3-297">Kopieren des Dateinamens im Bereich "Quellen" und "Formatvorlagen"</span><span class="sxs-lookup"><span data-stu-id="048e3-297">Copy file name in the Sources tool and Styles pane</span></span>  

<span data-ttu-id="048e3-298">Sie können jetzt einen Dateinamen über das Kontextmenü kopieren.</span><span class="sxs-lookup"><span data-stu-id="048e3-298">You may now copy a file name using the contextual menu.</span></span>  <span data-ttu-id="048e3-299">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [1155120][CR1155120].</span><span class="sxs-lookup"><span data-stu-id="048e3-299">To review the history of this feature in the Chromium open-source project, navigate to Issues [1155120][CR1155120].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="048e3-300">Zeigen Sie im Tool Quellen auf einen Dateinamen, öffnen Sie das Kontextmenü \(rechtsklick\ ), und wählen Sie dann Dateinamen **kopieren aus.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="048e3-300">In the **Sources** tool, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="048e3-301">Zeigen Sie **im** Elementtool > Formatvorlagenbereich auf einen Dateinamen, öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie dann "Dateinamen \*\*\*\* **kopieren" aus.**</span><span class="sxs-lookup"><span data-stu-id="048e3-301">In the **Elements** tool > **Styles** pane, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Kopieren des Dateinamens in "Quellen"" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         <span data-ttu-id="048e3-303">Kopieren des Dateinamens in **"Quellen"**</span><span class="sxs-lookup"><span data-stu-id="048e3-303">Copy file name in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Kopieren des Dateinamens im Formatvorlagenbereich" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         <span data-ttu-id="048e3-305">Kopieren des Dateinamens im **Formatvorlagenbereich**</span><span class="sxs-lookup"><span data-stu-id="048e3-305">Copy file name in **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="048e3-306">Updates für Framedetails</span><span class="sxs-lookup"><span data-stu-id="048e3-306">Updates to Frame details</span></span>  

#### <span data-ttu-id="048e3-307">Informationen zu Service Workers in Framedetails</span><span class="sxs-lookup"><span data-stu-id="048e3-307">Service Workers information in Frame details</span></span>  

<span data-ttu-id="048e3-308">DevTools listet jetzt einen dedizierten Dienstmitarbeiter unter dem übergeordneten Frame auf.</span><span class="sxs-lookup"><span data-stu-id="048e3-308">DevTools now lists a dedicated service worker under the parent frame.</span></span>  <span data-ttu-id="048e3-309">In der folgenden Abbildung werden Die Details des Dienstmitarbeiters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="048e3-309">In the following figure, service worker details are displayed.</span></span>  <span data-ttu-id="048e3-310">Um die Details des Dienstarbeitsmitarbeiters anzuzeigen, navigieren Sie zu **"Application**  >  **Frames**Service  >  `top`  >  **Workers",** und wählen Sie dann einen Dienstmitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="048e3-310">To display the service worker details, navigate to **Application** > **Frames** > `top` > **Service Workers** and then choose a service worker.</span></span>  <span data-ttu-id="048e3-311">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1122507][CR1122507].</span><span class="sxs-lookup"><span data-stu-id="048e3-311">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122507][CR1122507].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Informationen zu Service Workers in den Framesdetails" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   <span data-ttu-id="048e3-313">**Informationen zu Service Workers** in den **Framesdetails**</span><span class="sxs-lookup"><span data-stu-id="048e3-313">**Service Workers** information in the **Frames** details</span></span>  
:::image-end:::  

#### <span data-ttu-id="048e3-314">Messen von Speicherinformationen in Framedetails</span><span class="sxs-lookup"><span data-stu-id="048e3-314">Measure Memory information in Frame details</span></span>  

<span data-ttu-id="048e3-315">Der `performance.measureMemory()` STATUS der API wird nun im Abschnitt zur **API-Verfügbarkeit** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="048e3-315">The `performance.measureMemory()` API status is now displayed under the **API availability** section.</span></span>  <span data-ttu-id="048e3-316">Die neue `performance.measureMemory()` API schätzt die Speicherauslastung der gesamten Webseite.</span><span class="sxs-lookup"><span data-stu-id="048e3-316">The new `performance.measureMemory()` API estimates the memory usage of the entire webpage.</span></span>  <span data-ttu-id="048e3-317">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="048e3-317">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Messen des Arbeitsspeichers" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   <span data-ttu-id="048e3-319">Messen des Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="048e3-319">Measure Memory</span></span>  
:::image-end:::  

### <span data-ttu-id="048e3-320">Verworfene Frames im Leistungstool</span><span class="sxs-lookup"><span data-stu-id="048e3-320">Dropped frames in the Performance tool</span></span>  

<span data-ttu-id="048e3-321">Wenn Sie [die Lastleistung im Tool "Performance"][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]analysieren, markiert der Abschnitt **"Frames"** verworfene Frames als rot.</span><span class="sxs-lookup"><span data-stu-id="048e3-321">When you [analyze load performance in the Performance tool][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], the **Frames** section now marks dropped frames as red.</span></span>  <span data-ttu-id="048e3-322">Zeigen Sie zum Anzeigen der Framerate auf einen verworfenen Frame.</span><span class="sxs-lookup"><span data-stu-id="048e3-322">To display the frame rate, hover on a dropped frame.</span></span>  <span data-ttu-id="048e3-323">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1075865][CR1075865].</span><span class="sxs-lookup"><span data-stu-id="048e3-323">To review the history of this feature in the Chromium open-source project, navigate to Issue [1075865][CR1075865].</span></span>  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Verworfene Frames" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   <span data-ttu-id="048e3-325">Verworfene Frames</span><span class="sxs-lookup"><span data-stu-id="048e3-325">Dropped frames</span></span>  
:::image-end:::  

#### <span data-ttu-id="048e3-326">Neue Farbkontrastberechnung – Advanced Perceptual Contrast Algorithm (APCA)</span><span class="sxs-lookup"><span data-stu-id="048e3-326">New color contrast calculation - Advanced Perceptual Contrast Algorithm (APCA)</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="048e3-327">Der [Advanced Perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] ersetzt das [AA][W3cWaiWcag21QuickrefContrastMinimum] / [AAA-Richtlinienkontrastverhältnis][W3cWaiWcag21QuickrefContrastEnhanced] in der [Farbauswahl.][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]</span><span class="sxs-lookup"><span data-stu-id="048e3-327">The [Advanced Perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] replaces the [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced] guidelines contrast ratio in the [Color Picker][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].</span></span>  <span data-ttu-id="048e3-328">APCA ist eine neue Möglichkeit zum Berechnen des Kontrasts.</span><span class="sxs-lookup"><span data-stu-id="048e3-328">APCA is a new way to compute contrast.</span></span>  <span data-ttu-id="048e3-329">Sie basiert auf modernen Forschungen zur Farbwahrnehmung.</span><span class="sxs-lookup"><span data-stu-id="048e3-329">It is based on modern research on color perception.</span></span>  <span data-ttu-id="048e3-330">Im Vergleich zu AA/AAA-Richtlinien ist APCA kontextabhängiger.</span><span class="sxs-lookup"><span data-stu-id="048e3-330">Compared to AA/AAA guidelines, APCA is more context-dependent.</span></span>  <span data-ttu-id="048e3-331">Der Kontrast wird basierend auf den folgenden räumlichen Eigenschaften des Texts, der Farbe und des Kontexts berechnet.</span><span class="sxs-lookup"><span data-stu-id="048e3-331">The contrast is calculated based on the following spatial properties of the text, color, and context.</span></span>  

*   <span data-ttu-id="048e3-332">Räumliche Eigenschaften von Text, die Schriftgrad und Schriftgrad enthalten.</span><span class="sxs-lookup"><span data-stu-id="048e3-332">Spatial properties of text that include font weight and size.</span></span>  
*   <span data-ttu-id="048e3-333">Räumliche Eigenschaften der Farbe, die den wahrgenommenen Kontrast zwischen Text und Hintergrund enthalten.</span><span class="sxs-lookup"><span data-stu-id="048e3-333">Spatial properties of color that include perceived contrast between text and background.</span></span>  
*   <span data-ttu-id="048e3-334">Räumliche Eigenschaften des Kontexts, die Umgebungslicht, Umgebung und den beabsichtigten Zweck umfassen.</span><span class="sxs-lookup"><span data-stu-id="048e3-334">Spatial properties of context that include ambient light, surroundings, and intended purpose.</span></span>  
    
<span data-ttu-id="048e3-335">Um dieses Experiment zu [][DevtoolsCustomizeIndexSettings]aktivieren, navigieren Sie zu "Einstellungsexperimente", und aktivieren Sie das Kontrollkästchen neben "Neuen  >  \*\*\*\* **advanced Perceptual Contrast Algorithm (APCA)** aktivieren", der das vorherige Kontrastverhältnis und AA/AAA-Richtlinien ersetzt.</span><span class="sxs-lookup"><span data-stu-id="048e3-335">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable new Advanced Perceptual Contrast Algorithm (APCA) replacing previous contrast ratio and AA/AAA guidelines**.</span></span>  <span data-ttu-id="048e3-336">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1121900][CR1121900].</span><span class="sxs-lookup"><span data-stu-id="048e3-336">To review the history of this feature in the Chromium open-source project, navigate to Issue [1121900][CR1121900].</span></span>  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA in der Farbauswahl" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   <span data-ttu-id="048e3-338">APCA in der Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="048e3-338">APCA in the Color Picker</span></span>  
:::image-end:::  

## <span data-ttu-id="048e3-339">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="048e3-339">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="048e3-340">Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="048e3-340">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="048e3-341">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="048e3-341">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="048e3-342">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="048e3-342">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Neues in DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Anzeigen des Kontrastverhältnisses eines Textelements in der Farbauswahl – Barrierefreiheitsreferenz | Microsoft Docs"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Ändern von CSS – CSS-| Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools-| Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Testen auf ausklappbaren und dualen Bildschirmgeräten – Emulieren von Dualbildschirmen und ausklappbaren Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simulieren eines mobilen Viewports – Emulieren mobiler Geräte in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Leistung beim Laden eines Datensatzes – Referenz zur Leistungsanalyse | Microsoft Docs"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Bearbeiten von Css-Schriftartenformaten und -einstellungen im Formatvorlagenbereich in DevTools | Microsoft Docs"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Übersicht über microsoft Edge (Chromium)-Entwicklertools | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "So arbeiten Sie mit der Naht – Einführung in duale Bildschirmgeräte | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Feature für bildschirmübergreifende CSS-Medien für die Erkennung von | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "Die getWindowSegments-JavaScript-API für Dualbildschirmgeräte | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Abschnitt 1 : CSS :target demo for What's New in DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: Implementieren von Dropdownmenüs in Einstellungen zum Ändern von Designs | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: Debugger für Microsoft Edge als Abhängigkeits-| GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Aktualisieren der Edge DevTools-Version auf 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Hinzufügen einzelner Schließen-Schaltflächen zum Instanzenbereich | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Wählen Sie Schriftarteigenschaften und Hintergrundfarben aus, um ausreichend Kontrast für die Lesbarkeit von | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Vertrauenswürdige | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Neues Surface Duo| Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Preview Channels"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterungs-Marketplace-| Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  

<!--[CR174309]: https://crbug.com/174309 "Issue 174309: DevTools: Allow to customize keyboard shortcuts/key bindings | Chromium bugs"  -->  
<!--[CR772558]: https://crbug.com/772558 "Issue 772558: DevTools: Update to latest version of Lighthouse | Chromium bugs"  -->  
[CR978059]: https://crbug.com/978059 "Issue 978059: Deleting cookies when filtering them, delete all the cookies not just the filtered ones | Chromium bugs"  
[CR997625]: https://crbug.com/997625 "Issue 997625: New Feature Req | Need option to see url-decoded value in cookies | Chromium bugs"  
[CR1003629]: https://crbug.com/1003629 "Issue 1003629: Capture Node does not screenshot the node below the fold anymore. <span data-ttu-id="048e3-374">| Chromium bugs"</span><span class="sxs-lookup"><span data-stu-id="048e3-374">| Chromium bugs"</span></span>  
[CR1012337]: https://crbug.com/1012337 "Issue 1012337: Clear Site Data destroys Google session on non-Google sites | Chromium bugs"  
[CR1028078]: https://crbug.com/1028078 "Issue 1028078: Put Online and Offline next to each next to each in the list | Chromium bugs"  
[CR1054281]: https://crbug.com/1054281 "Issue 1054281: Feature Request: DevTools should emulate foldable and dual-screen devices | Chromium bugs"  
<!--[CR1073909]: https://crbug.com/1073909 "Issue 1073909: BLOCKED | Chromium bugs"  -->  
[CR1075865]: https://crbug.com/1075865 "Issue 1075865: Show dropped frames in devtools timeline | Chromium bugs"  
[CR1093229]: https://crbug.com/1093229 "Issue 1093229: DevTools: offer a specialized typeface editor UI | Chromium bugs"  
[CR1121900]: https://crbug.com/1121900 "Issue 1121900: DevTools: update contrast calculation logic per new spec | Chromium bugs"  
[CR1122507]: https://crbug.com/1122507 "Issue 1122507: Surface worker information in frame tree view | Chromium bugs"  
[CR1122580]: https://crbug.com/1122580 "Issue 1122580: Impossible to disable network recording on reload | Chromium bugs"  
<!--[CR1126824]: https://crbug.com/1126824 "Issue 1126824: ☂ Support Trust Token debugging in DevTools | Chromium bugs"  -->  
[CR1136394]: https://crbug.com/1136394 "Issue 1136394: Flexbox tooling | Chromium bugs"  
<!--[CR1137837]: https://crbug.com/1137837 "Issue 1137837: ☂ Improve Trusted Types support in DevTools | Chromium bugs"  -->  
[CR1139899]: https://crbug.com/1139899 "Issue 1139899: Report gated API availability in frame details view | Chromium bugs"  
[CR1139949]: https://crbug.com/1139949 "Issue 1139949: Flexbox overlay | Chromium bugs"  
<!--[CR1142804]: https://crbug.com/1142804 "Issue 1142804: Implement break-on-trusted-type-violation | Chromium bugs"  -->  
<!--[CR1144127]: https://crbug.com/1144127 "Issue 1144127: BLOCKED | Chromium bugs"  -->  
[CR1147016]: https://crbug.com/1147016 "Problem 1147016: Die Farbauswahl wird in der var()-Funktion nicht angezeigt. <span data-ttu-id="048e3-387">| Chromium bugs"</span><span class="sxs-lookup"><span data-stu-id="048e3-387">| Chromium bugs"</span></span>  
[CR1148353]: https://crbug.com/1148353 "Issue 1148353: Feature Request: Copy Object from the devtools console | Chromium bugs"  
[CR1149859]: https://crbug.com/1149859 "Issue 1149859: [feature request][Console] add copy object to clipboard item to contextual menu | Chromium bugs"  
[CR1150797]: https://crbug.com/1150797 "Issue 1150797: Add Duplicate element context menu in Element panel | Chromium bugs"  
<!--[CR1150883]: https://crbug.com/1150883 "Issue 1150883: Remove TT messages from the console but keep underlining in the sources tab | Chromium bugs"  -->  
<!--[CR1152290]: https://crbug.com/1152290 "Issue 1152290: Devtools support for QuicTransport | Chromium bugs"  -->  
[CR1152391]: https://crbug.com/1152391 "Issue 1152391: Support for copy CSS context menu in styles panel | Chromium bugs"  
[CR1155120]: https://crbug.com/1155120 "Issue 1155120: [FR]Support copy file name and line number | Chromium bugs"  
[CR1156628]: https://crbug.com/1156628 "Issue 1156628: DevTools: add support for :target in force element state feature | Chromium bugs"  
[CR1157329]: https://crbug.com/1157329 "Issue 1157329: Accessibility - Narrator: Narrator is not announcing the count and position for suggestions available for code in Styles tab | Chromium bugs"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "1-1-| Samsung US"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Kontrast (erweitert) – So erfüllen Sie WCAG (Kurzübersicht) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Kontrast (Minimum) – So erfüllen Sie WCAG (Kurzübersicht) | W3C"  

> [!NOTE]
> <span data-ttu-id="048e3-399">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="048e3-399">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="048e3-400">Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/updates/2021/01/devtools/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="048e3-400">The original page is found [here](https://developers.google.com/web/updates/2021/01/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="048e3-402">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="048e3-402">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Übergreifender Platzhalter"  

---
description: Passen Sie Tastenkombinationen mit Visual Studio-Code an, emulieren Sie Surface Duo und Samsung Galaxy Fold, Verbesserungen der CSS-Raster Überlagerung und vieles mehr.
title: Neuerungen in devtools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 0e759c18b5ef547bfd490f4d525930f92809a6a1
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2020
ms.locfileid: "11133911"
---
# <span data-ttu-id="17ec1-104">Neuerungen in devtools (Microsoft Edge 86)</span><span class="sxs-lookup"><span data-stu-id="17ec1-104">What's New In DevTools (Microsoft Edge 86)</span></span>  

## <span data-ttu-id="17ec1-105">Ankündigungen des Microsoft Edge devtools-Teams</span><span class="sxs-lookup"><span data-stu-id="17ec1-105">Announcements from the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <span data-ttu-id="17ec1-106">Zuordnen von Tastenkombinationen in devtools zu Visual Studio-Code</span><span class="sxs-lookup"><span data-stu-id="17ec1-106">Match keyboard shortcuts in DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="17ec1-107">In Microsoft Edge 86 können Sie die Tastenkombinationen im devtools mit ihren Tastenkombinationen in [Visual Studio-Code][VisualStudioCode]vergleichen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-107">In Microsoft Edge 86, you may match keyboard shortcuts in the DevTools to your shortcuts in [Visual Studio Code][VisualStudioCode].</span></span> 

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   <span data-ttu-id="17ec1-109">Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code</span><span class="sxs-lookup"><span data-stu-id="17ec1-109">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-110">Um dieses Feature zu aktivieren, navigieren Sie zum [Anpassen von Tastenkombinationen im Microsoft Edge-devtools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="17ec1-110">To activate this feature, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  

<span data-ttu-id="17ec1-111">Die Tastenkombination zum Anhalten oder Fortsetzen der Ausführung eines Skripts in [Visual Studio-Code][VisualStudioCodeShortcutsKeyboardWindows] lautet beispielsweise `F5` .</span><span class="sxs-lookup"><span data-stu-id="17ec1-111">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="17ec1-112">Mit der **devtools (Standardeinstellung)** ist dieselbe Verknüpfung in der devtools `F8` , aber wenn Sie die **Visual Studio-Code** Vorgabe auswählen, ist diese Verknüpfung nun auch `F5` .</span><span class="sxs-lookup"><span data-stu-id="17ec1-112">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8`, but when you choose the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="17ec1-113">Chrom Problem [#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="17ec1-113">Chromium issue [#174309][CR174309]</span></span>  

### <span data-ttu-id="17ec1-114">Emulieren von Surface Duo und Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="17ec1-114">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code":::
   <span data-ttu-id="17ec1-116">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="17ec1-116">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-117">Sie können jetzt das Aussehen und Verhalten Ihrer Website oder App auf zwei neuen Geräten testen:  [Surface Duo][MicrosoftSurfaceDevicesDuo] und [Samsung Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="17ec1-117">You are now able to test the look and feel of your website or app on two new devices:  [Surface Duo][MicrosoftSurfaceDevicesDuo] and [Samsung Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.</span></span>  

<span data-ttu-id="17ec1-118">Verwenden Sie beim [emulieren des Geräts][DevtoolsDeviceModeIndex]die folgenden Features, um Ihre Website oder App für Dual-Screen-und faltbare Geräte zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="17ec1-118">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="17ec1-119">Über [greifend][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], das heißt, wenn auf beiden Bildschirmen die Website \ (oder App \) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="17ec1-119">[Spanning][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>
*   <span data-ttu-id="17ec1-120">[Rendern der Naht][DualScreenIntroductionHowWorkSeam], also des Leerraums zwischen den beiden Bildschirmen</span><span class="sxs-lookup"><span data-stu-id="17ec1-120">[Rendering the seam][DualScreenIntroductionHowWorkSeam], which is the space between the two screens.</span></span>
*   <span data-ttu-id="17ec1-121">[Aktivieren von experimentellen Web-Platform-APIs][DevtoolsExperimentalFeaturesEnableExperimentalApis] für den Zugriff auf das neue [CSS mediascreen-Feature][DualScreenWebCssMediaSpanning] und die [JavaScript-getWindowSegments-API][DualScreenWebJavascriptGetwindowsegments].</span><span class="sxs-lookup"><span data-stu-id="17ec1-121">[Enabling experimental Web Platform APIs][DevtoolsExperimentalFeaturesEnableExperimentalApis] to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [JavaScript getWindowSegments API][DualScreenWebJavascriptGetwindowsegments].</span></span>  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   <span data-ttu-id="17ec1-123">Geräteemulation für Surface Duo</span><span class="sxs-lookup"><span data-stu-id="17ec1-123">Device emulation for Surface Duo</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-124">Um dieses experimentelle Feature zu aktivieren, navigieren Sie zu [experimentelle Features aktivieren][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] , und aktivieren Sie das Kontrollkästchen neben **Emulation: Dual-Screen-Modus unterstützen**.</span><span class="sxs-lookup"><span data-stu-id="17ec1-124">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Emulation: Support dual screen mode**.</span></span>  

<span data-ttu-id="17ec1-125">Wenn Sie weitere Informationen zu diesem Experiment erhalten möchten, navigieren Sie zu [Emulation: Unterstützung des dualen Bildschirms][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span><span class="sxs-lookup"><span data-stu-id="17ec1-125">For more information about this experiment, navigate to [Emulation: Support dual screen mode][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span></span>  

<span data-ttu-id="17ec1-126">Chromium-Problem: [#1054281][CR1054281]</span><span class="sxs-lookup"><span data-stu-id="17ec1-126">Chromium issue: [#1054281][CR1054281]</span></span>  

### <span data-ttu-id="17ec1-127">Verbesserungen der CSS-Raster Überlagerung und neue experimentelle Raster Features</span><span class="sxs-lookup"><span data-stu-id="17ec1-127">CSS grid overlay improvements and new experimental grid features</span></span>  

<span data-ttu-id="17ec1-128">Vielen Dank für ihr positives Feedback zu den verbesserten CSS-Raster Überlagerungen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-128">Thank you for the positive feedback about the improved CSS grid overlays.</span></span>  <span data-ttu-id="17ec1-129">Die CSS-Raster Überlagerungen sind nun standardmäßig aktiviert, und es ist nicht erforderlich, dass Sie ein Experiment aktivieren.</span><span class="sxs-lookup"><span data-stu-id="17ec1-129">The CSS grid overlays are now enabled by default and do not require you to turn on an experiment.</span></span>  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   <span data-ttu-id="17ec1-131">CSS-Raster Überlagerung für `article` Element</span><span class="sxs-lookup"><span data-stu-id="17ec1-131">CSS grid overlay for `article` element</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="17ec1-132">Weitere Informationen zu Raster Überlagerungen finden Sie unter [Debuggen von CSS-Raster Features][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span><span class="sxs-lookup"><span data-stu-id="17ec1-132">For more information about grid overlays, go to [CSS grid debugging features][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="17ec1-133">Das Microsoft Edge devtools-Team und das Chrome devtools-Team arbeiten an zusätzlichen Features zusammen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-133">The Microsoft Edge DevTools team and the Chrome DevTools team collaborate on additional features.</span></span>  <span data-ttu-id="17ec1-134">Zu den neuen Features gehören mehrere Overlays, die in einem neuen **Layoutbereich** im Bereich **Elemente** persistent und konfigurierbar sind.</span><span class="sxs-lookup"><span data-stu-id="17ec1-134">The new features include multiple overlays that are persistent and configurable from a new **Layout** pane on the **Elements** panel.</span></span>  

<span data-ttu-id="17ec1-135">Um dieses experimentelle Feature zu aktivieren, navigieren Sie zu [experimentelle Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] aktivieren, und aktivieren Sie das Kontrollkästchen neben **neue CSS-Raster Debuggen Features aktivieren (Konfigurationsoptionen, die im Bereich "Layout-Seitenleiste" in Elementen nach dem Neustart verfügbar sind)**.</span><span class="sxs-lookup"><span data-stu-id="17ec1-135">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)**.</span></span>  

<span data-ttu-id="17ec1-136">Weitere Informationen zu diesem Experiment finden Sie unter [Aktivieren neuer Features für das Debuggen von CSS-Rastern][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span><span class="sxs-lookup"><span data-stu-id="17ec1-136">For more information about this experiment, navigate to [Enable new CSS grid debugging features][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="17ec1-137">Chromium-Problem: [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="17ec1-137">Chromium issue: [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="17ec1-138">Von der Konsole kopierte Tabelle erhält die Formatierung</span><span class="sxs-lookup"><span data-stu-id="17ec1-138">Table copied from the Console preserves formatting</span></span>  

<span data-ttu-id="17ec1-139">In Microsoft Edge 85 oder früher ging die Formatierung einer Kopie `console.table` verloren.</span><span class="sxs-lookup"><span data-stu-id="17ec1-139">In Microsoft Edge 85 or earlier, the formatting of a copied `console.table` was lost.</span></span>  <span data-ttu-id="17ec1-140">Wenn Sie die Ausgabe aus der [Tabellen][DevtoolsConsoleApiTable] Konsolen-API kopiert und eingefügt haben, wurde nur der Text der Tabelle beibehalten.</span><span class="sxs-lookup"><span data-stu-id="17ec1-140">If you copied the output from the [table][DevtoolsConsoleApiTable] Console API, and pasted it, only the text of the table was kept.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` <span data-ttu-id="17ec1-142">Ausgabe der Konsolen-API in Microsoft Edge 85 oder früher</span><span class="sxs-lookup"><span data-stu-id="17ec1-142">Console API output in Microsoft Edge 85 or earlier</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="17ec1-144">Konsolen-API-Ausgabe von Microsoft Edge 85 oder früher in Visual Studio-Code eingefügt</span><span class="sxs-lookup"><span data-stu-id="17ec1-144">Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="17ec1-145">Wenn Sie in Microsoft Edge 86 oder höher eine Tabelle aus der **Konsole**kopieren, ist die Formatierung nun erhalten.</span><span class="sxs-lookup"><span data-stu-id="17ec1-145">In Microsoft Edge 86 or later, when you copy a table from the **Console**, the formatting is now preserved.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` <span data-ttu-id="17ec1-147">Ausgabe der Konsolen-API in Microsoft Edge 86 oder höher</span><span class="sxs-lookup"><span data-stu-id="17ec1-147">Console API output in Microsoft Edge 86 or later</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="17ec1-149">Konsolen-API-Ausgabe von Microsoft Edge 86 oder später eingefügt in Visual Studio-Code</span><span class="sxs-lookup"><span data-stu-id="17ec1-149">Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="17ec1-150">Chrom Problem: [#1115011] [CR1115011]</span><span class="sxs-lookup"><span data-stu-id="17ec1-150">Chromium issue: [#1115011][CR1115011]</span></span>  

### <span data-ttu-id="17ec1-151">Viewer für Quellreihenfolge für einfachere Tests zur Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="17ec1-151">Source Order Viewer for easier accessibility testing</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code":::
   <span data-ttu-id="17ec1-153">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="17ec1-153">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-154">Die neue Barrierefreiheits Hilfe zeigt die Reihenfolge der Elemente in der Quelle an.</span><span class="sxs-lookup"><span data-stu-id="17ec1-154">The new accessibility helper displays the order of elements in the source.</span></span>  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   <span data-ttu-id="17ec1-156">Aktivieren der **Quellreihenfolge anzeigen**</span><span class="sxs-lookup"><span data-stu-id="17ec1-156">Activate **Show source order**</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-157">Dieses Feature macht es einfacher, die Art und Weise zu testen, wie Sprachausgabe und Tastatur Benutzer Ihre Website oder App erleben.</span><span class="sxs-lookup"><span data-stu-id="17ec1-157">This feature makes it easier to test the way screen reader and keyboard users experience your website or app.</span></span>  <span data-ttu-id="17ec1-158">Bildschirmsprachausgaben und Tastaturnavigation hängen davon ab, ob Inhalte in einer bestimmten Reihenfolge im Quellcode Ihrer Website oder App gespeichert werden, damit Sie der gerenderten Seite entsprechen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-158">Screen readers and keyboard navigation depend on content being placed in a particular order in the source code of your website or app, so that it matches the rendered page.</span></span>  <span data-ttu-id="17ec1-159">In der Quellauftrags Anzeige werden potenzielle Unterschiede in der Reihenfolge zwischen der gerenderten Seite und dem Quellcode angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17ec1-159">The Source Order Viewer displays potential differences in order between the rendered page and the source code.</span></span>  

<span data-ttu-id="17ec1-160">Wenn Sie dieses experimentelle Feature aktivieren möchten, navigieren Sie zu [experimentelle Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] aktivieren, und aktivieren Sie das Kontrollkästchen neben **Quellauftrags Anzeige aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="17ec1-160">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Source Order Viewer**.</span></span>  

<span data-ttu-id="17ec1-161">Weitere Informationen zu diesem Experiment finden Sie unter [Aktivieren der Quellauftrags Anzeige][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span><span class="sxs-lookup"><span data-stu-id="17ec1-161">For more information about this experiment, navigate to [Enable Source Order Viewer][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span></span>  

<span data-ttu-id="17ec1-162">Chromium-Problem: [#1094406][CR1094406]</span><span class="sxs-lookup"><span data-stu-id="17ec1-162">Chromium issue: [#1094406][CR1094406]</span></span>  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <span data-ttu-id="17ec1-163">Markieren aller Suchergebnisse im elementtool</span><span class="sxs-lookup"><span data-stu-id="17ec1-163">Highlight all search results in Elements tool</span></span>  

<span data-ttu-id="17ec1-164">In Microsoft Edge 84 und 85 wurde das erste Suchergebnis im **Element** Panel nicht markiert.</span><span class="sxs-lookup"><span data-stu-id="17ec1-164">In Microsoft Edge 84 and 85, the first search result in the **Elements** panel did not highlight.</span></span>  <span data-ttu-id="17ec1-165">Die restlichen Suchergebnisse wurden richtig hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="17ec1-165">The remaining search results were highlighted correctly.</span></span>  

<span data-ttu-id="17ec1-166">Vielen Dank für Ihr Feedback und die Verbesserung von Chrom.</span><span class="sxs-lookup"><span data-stu-id="17ec1-166">Thank you for sending your feedback and helping improve Chromium.</span></span>  <span data-ttu-id="17ec1-167">Ihr Feedback hat ein Problem [#1103316][CR1103316] im Open-Source-Projekt Chromium aufgedeckt.</span><span class="sxs-lookup"><span data-stu-id="17ec1-167">Your feedback uncovered Issue [#1103316][CR1103316] in the open-source Chromium project.</span></span>  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   <span data-ttu-id="17ec1-169">Hervorgehobenes erstes Suchergebnis im **Element** Panel in Microsoft Edge 84 oder höher</span><span class="sxs-lookup"><span data-stu-id="17ec1-169">Highlighted first search result on **Elements** panel in Microsoft Edge 84 or later</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-170">Das Problem ist jetzt in allen Versionen von Microsoft Edge behoben.</span><span class="sxs-lookup"><span data-stu-id="17ec1-170">The issue is now fixed in all versions of Microsoft Edge.</span></span>  

<span data-ttu-id="17ec1-171">Chromium-Problem: [#1103316][CR1103316]</span><span class="sxs-lookup"><span data-stu-id="17ec1-171">Chromium issue: [#1103316][CR1103316]</span></span>  

## <span data-ttu-id="17ec1-172">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="17ec1-172">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="17ec1-173">Neues Medien Panel</span><span class="sxs-lookup"><span data-stu-id="17ec1-173">New Media panel</span></span>  

<span data-ttu-id="17ec1-174">DevTools zeigt nun Informationen zu Medienplayern im [Medien][DevtoolsMediaPanelIndex] Panel an.</span><span class="sxs-lookup"><span data-stu-id="17ec1-174">DevTools now displays media players information in the [Media][DevtoolsMediaPanelIndex] panel.</span></span>  

<span data-ttu-id="17ec1-175">Führen Sie den folgenden Schritt aus, um den neuen **Medien** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-175">To open the new **Media** panel, complete the following step.</span></span>  

1.  <span data-ttu-id="17ec1-176">Wählen Sie **anpassen und Steuern devtools** \ ( `...` \) > **Weitere Tools**  >  **Medien**aus.</span><span class="sxs-lookup"><span data-stu-id="17ec1-176">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/media-panel.msft.png":::
       <span data-ttu-id="17ec1-178">Neues **Medien** Panel</span><span class="sxs-lookup"><span data-stu-id="17ec1-178">New **Media** panel</span></span>  
    :::image-end:::  

<span data-ttu-id="17ec1-179">Vor dem neuen **Medien** Panel in devtools befanden sich die Protokollierungs-und Debuginformationen zu Videoplayern unter der Einstellung " **zuletzt verwendete Spieler** ".</span><span class="sxs-lookup"><span data-stu-id="17ec1-179">Before the new **Media** panel in DevTools, the logging and debug information about video players was located under the **Recent Players** setting.</span></span>  <span data-ttu-id="17ec1-180">Wenn Sie die Einstellung für **zuletzt verwendete Spieler** öffnen möchten, wechseln Sie zu `edge://media-internals` und wählen Sie den Reiter **Spieler** aus.</span><span class="sxs-lookup"><span data-stu-id="17ec1-180">To open the **Recent Players** setting, go to `edge://media-internals` and choose the **Players** tab.</span></span>  

<span data-ttu-id="17ec1-181">Zeigen Sie Liveinhalte an, und prüfen Sie potenzielle Probleme schneller, einschließlich der folgenden Beispiele.</span><span class="sxs-lookup"><span data-stu-id="17ec1-181">View live content and inspect potential issues more quickly, including the following examples.</span></span>  

*   <span data-ttu-id="17ec1-182">Warum werden Frames verworfen?</span><span class="sxs-lookup"><span data-stu-id="17ec1-182">Why frames are dropped?</span></span>  
*   <span data-ttu-id="17ec1-183">Warum wird JavaScript in einer unerwarteten Weise mit dem Spieler interagieren?</span><span class="sxs-lookup"><span data-stu-id="17ec1-183">Why JavaScript is interacting with the player in an unexpected way?</span></span>  

### <span data-ttu-id="17ec1-184">Aufzeichnen von Knoten Screenshots über das Kontextmenü des Elements Panels</span><span class="sxs-lookup"><span data-stu-id="17ec1-184">Capture node screenshots using the Elements panel context menu</span></span>  

<span data-ttu-id="17ec1-185">Sie können nun Knoten Screenshots über das Kontextmenü im Bereich " **Elemente** " erfassen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-185">You may now capture node screenshots using the context menu in the **Elements** panel.</span></span>  

<span data-ttu-id="17ec1-186">Wenn Sie beispielsweise einen Screenshot des Inhaltsverzeichnisses erstellen möchten, zeigen Sie auf das Element, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Screenshot des Knotens aufzeichnen**aus.</span><span class="sxs-lookup"><span data-stu-id="17ec1-186">For example, to take a screenshot of the table of contents, hover on the element, open the contextual menu \(right-click\), and select **Capture node screenshot**.</span></span>  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   <span data-ttu-id="17ec1-188">Screenshots des Knotens aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="17ec1-188">Capture node screenshots</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-189">Chromium-Problem: [#1100253][CR1100253]</span><span class="sxs-lookup"><span data-stu-id="17ec1-189">Chromium issue: [#1100253][CR1100253]</span></span>  

### <span data-ttu-id="17ec1-190">Probleme mit Tool Updates</span><span class="sxs-lookup"><span data-stu-id="17ec1-190">Issues tool updates</span></span>  

<span data-ttu-id="17ec1-191">Die warnungsleiste "Probleme" im **Konsolen** Bereich wird nun durch eine normale Nachricht ersetzt.</span><span class="sxs-lookup"><span data-stu-id="17ec1-191">The Issues warning bar on the **Console** panel is now replaced with a regular message.</span></span>  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   <span data-ttu-id="17ec1-193">Probleme in der Konsolen Nachricht</span><span class="sxs-lookup"><span data-stu-id="17ec1-193">Issues in console message</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-194">Probleme mit Cookies von Drittanbietern sind jetzt standardmäßig im **Problem** Tool ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="17ec1-194">Third-party cookie issues are now hidden by default in the **Issues** tool.</span></span>  <span data-ttu-id="17ec1-195">Aktivieren Sie das Kontrollkästchen neues **einbeziehen von Cookies von Drittanbietern** , um die Probleme anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-195">Enable the new **Include third-party cookie issues** checkbox to view the issues.</span></span>  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   <span data-ttu-id="17ec1-197">Kontrollkästchen für Cookies von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="17ec1-197">third-party cookie issues checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-198">Chrom Probleme: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span><span class="sxs-lookup"><span data-stu-id="17ec1-198">Chromium issues: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span></span>  

### <span data-ttu-id="17ec1-199">Emulieren fehlender lokaler Schriftarten</span><span class="sxs-lookup"><span data-stu-id="17ec1-199">Emulate missing local fonts</span></span>  

<span data-ttu-id="17ec1-200">Öffnen Sie das [Rendering-Tool][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] , und verwenden Sie das neue Feature **lokale Schriftarten deaktivieren** , um fehlende `local()` Quellen in Regeln zu emulieren `@font-face` .</span><span class="sxs-lookup"><span data-stu-id="17ec1-200">Open the [Rendering tool][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] and use the new **Disable local fonts** feature to emulate missing `local()` sources in `@font-face` rules.</span></span>  

<span data-ttu-id="17ec1-201">Wenn die Schriftart beispielsweise `Rubik` auf Ihrem Gerät installiert ist und von der `@font-face src` Regel als Schriftart verwendet wird `local()` , verwendet Microsoft Edge die lokale Schriftartdatei auf Ihrem Gerät.</span><span class="sxs-lookup"><span data-stu-id="17ec1-201">For example, when the `Rubik` font is installed on your device and the `@font-face src` rule uses it as a `local()` font, Microsoft Edge uses the local font file from your device.</span></span>  

<span data-ttu-id="17ec1-202">Wenn **lokale Schriftarten deaktivieren** aktiviert ist, ignoriert devtools die `local()` Schriftarten und ruft alle aus dem Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="17ec1-202">When **Disable local fonts** is enabled, DevTools ignores the `local()` fonts and fetches each from the network.</span></span>  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/disable-font.msft.png":::
   <span data-ttu-id="17ec1-204">Emulieren fehlender lokaler Schriftarten</span><span class="sxs-lookup"><span data-stu-id="17ec1-204">Emulate missing local fonts</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-205">Wenn Sie während der Entwicklung zwei unterschiedliche Kopien derselben Schriftart verwenden, wie beispielsweise die folgenden Beispiele.</span><span class="sxs-lookup"><span data-stu-id="17ec1-205">If you use two different copies of the same font during development, such as the following examples.</span></span>  

*   <span data-ttu-id="17ec1-206">Eine lokale Schriftart für Ihre Entwurfstools.</span><span class="sxs-lookup"><span data-stu-id="17ec1-206">A local font for your design tools.</span></span>  
*   <span data-ttu-id="17ec1-207">Eine Web-Schriftart für Ihren Code.</span><span class="sxs-lookup"><span data-stu-id="17ec1-207">A web font for your code.</span></span>  

<span data-ttu-id="17ec1-208">Verwenden Sie **lokale Schriftarten deaktivieren** , damit Sie die folgenden Aufgaben einfacher ausführen können.</span><span class="sxs-lookup"><span data-stu-id="17ec1-208">Use **Disable local fonts** to make it easier for you to complete the following tasks.</span></span>  

*   <span data-ttu-id="17ec1-209">Debuggen und Messen der Ladeleistung und Optimierung von Webschriftarten</span><span class="sxs-lookup"><span data-stu-id="17ec1-209">Debug and measure loading performance and optimization of web fonts.</span></span>  
*   <span data-ttu-id="17ec1-210">Überprüfen Sie die Genauigkeit Ihrer CSS `@font-face` -Regeln.</span><span class="sxs-lookup"><span data-stu-id="17ec1-210">Verify accuracy of your CSS `@font-face` rules.</span></span>  
*   <span data-ttu-id="17ec1-211">Entdecken Sie Unterschiede zwischen lokalen Versionen, die auf Ihrem Gerät installiert sind, und einer Web-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="17ec1-211">Discover differences between local versions installed on your device and a web font.</span></span>  

<span data-ttu-id="17ec1-212">Chromium-Problem: [#384968][CR384968]</span><span class="sxs-lookup"><span data-stu-id="17ec1-212">Chromium issue: [#384968][CR384968]</span></span>  

### <span data-ttu-id="17ec1-213">Emulieren inaktiver Benutzer</span><span class="sxs-lookup"><span data-stu-id="17ec1-213">Emulate inactive users</span></span>  

<span data-ttu-id="17ec1-214">Die [API für die Leerlauferkennung][WebDevIdleDetection] ermöglicht es Entwicklern, inaktive Benutzer zu erkennen und auf Leerlauf Zustandsänderungen zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="17ec1-214">The [Idle Detection API][WebDevIdleDetection] allows developers to detect inactive users and react on idle state changes.</span></span>  <span data-ttu-id="17ec1-215">Sie können jetzt devtools verwenden, um die Änderungen im Leerlaufzustand im **Sensor** Tool sowohl für den Benutzerzustand als auch für den Bildschirm Zustand zu emulieren, anstatt zu warten, bis der Zustand des tatsächlichen Ruhezustands geändert wird.</span><span class="sxs-lookup"><span data-stu-id="17ec1-215">You are now able to use DevTools to emulate idle state changes in the **Sensors** tool for both the user state and the screen state instead of waiting for the actual idle state to change.</span></span>  <span data-ttu-id="17ec1-216">Sie können das Tool **Sensoren** aus der [Schublade][DevtoolsCustomizeIndexDrawer]öffnen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-216">You may open the **Sensors** tool from the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   <span data-ttu-id="17ec1-218">Emulieren inaktiver Benutzer</span><span class="sxs-lookup"><span data-stu-id="17ec1-218">Emulate inactive users</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-219">Chromium-Problem: [#1090802][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="17ec1-219">Chromium issue: [#1090802][CR1090802]</span></span>  

### <span data-ttu-id="17ec1-220">Emulieren bevorzugt-reduzierte Daten</span><span class="sxs-lookup"><span data-stu-id="17ec1-220">Emulate prefers-reduced-data</span></span>  

> [!NOTE]
> <span data-ttu-id="17ec1-221">Wenn Sie dieses Feature in Microsoft Edge 86 aktivieren möchten, wechseln Sie zu, `edge://flags#enable-experimental-web-platform-features` und aktivieren Sie das Kennzeichen **experimentelle webplattforms-Features** .</span><span class="sxs-lookup"><span data-stu-id="17ec1-221">In Microsoft Edge 86, to enable this feature, go to `edge://flags#enable-experimental-web-platform-features` and turn on the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="17ec1-222">Die Emulations Option wird nur angezeigt, wenn das Flag aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="17ec1-222">The emulation option is only displayed if the flag is enabled.</span></span>  

<span data-ttu-id="17ec1-223">Die Abfrage " [bevorzugt reduzierte Daten][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] Medien" erkennt Benutzerinhalts Einstellungen für reduzierte Daten.</span><span class="sxs-lookup"><span data-stu-id="17ec1-223">The [prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] media query detects user content preferences for reduced data.</span></span>  <span data-ttu-id="17ec1-224">Wenn diese Option ausgewählt ist, erhält der Benutzer Alternativen Seiteninhalt, in dem geringere Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17ec1-224">If selected, the user receives alternate page content that uses less data.</span></span>  

<span data-ttu-id="17ec1-225">Sie können jetzt devtools verwenden, um die medienabfrage zu emulieren `prefers-reduced-data` .</span><span class="sxs-lookup"><span data-stu-id="17ec1-225">You may now use DevTools to emulate the `prefers-reduced-data` media query.</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   <span data-ttu-id="17ec1-227">Emulieren bevorzugt-reduzierte Daten</span><span class="sxs-lookup"><span data-stu-id="17ec1-227">Emulate prefers-reduced-data</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-228">Chromium-Problem: [#1096068][CR1096068]</span><span class="sxs-lookup"><span data-stu-id="17ec1-228">Chromium issue: [#1096068][CR1096068]</span></span>  

### <span data-ttu-id="17ec1-229">Unterstützung für neue JavaScript-Features</span><span class="sxs-lookup"><span data-stu-id="17ec1-229">Support for new JavaScript features</span></span>  

<span data-ttu-id="17ec1-230">DevTools haben nun die folgenden JavaScript-Sprachfeatures besser unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17ec1-230">DevTools now have better supported the following JavaScript language features.</span></span>  

| <span data-ttu-id="17ec1-231">JavaScript-Sprachfeature</span><span class="sxs-lookup"><span data-stu-id="17ec1-231">JavaScript language feature</span></span> | <span data-ttu-id="17ec1-232">Details</span><span class="sxs-lookup"><span data-stu-id="17ec1-232">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="17ec1-233">Logische Zuordnungs Operatoren</span><span class="sxs-lookup"><span data-stu-id="17ec1-233">Logical assignment operators</span></span>][V8FeaturesLogicalAssignment] | <span data-ttu-id="17ec1-234">DevTools unterstützt jetzt die logische Zuordnung mit dem neuen `&&=` `||=` und den `??=` Operatoren in den Panels **Console** und **Sources** .</span><span class="sxs-lookup"><span data-stu-id="17ec1-234">DevTools now supports logical assignment with the new `&&=`, `||=`, and `??=` operators in the **Console** and **Sources** panels.</span></span>  |  
| <span data-ttu-id="17ec1-235">Pretty-Print- [numerische Trenn][V8FeaturesNumericSeparators] Zeichen</span><span class="sxs-lookup"><span data-stu-id="17ec1-235">Pretty-print [numeric separators][V8FeaturesNumericSeparators]</span></span> | <span data-ttu-id="17ec1-236">DevTools nun richtig hübsch – druckt die numerischen Trennzeichen im **Quellen** Panel.</span><span class="sxs-lookup"><span data-stu-id="17ec1-236">DevTools now properly pretty-prints the numeric separators in the **Sources** panel.</span></span>  |  

<span data-ttu-id="17ec1-237">Probleme mit Chrom: [1086817][CR1086817], [1080569][CR1080569]</span><span class="sxs-lookup"><span data-stu-id="17ec1-237">Chromium issues: [1086817][CR1086817], [1080569][CR1080569]</span></span>  

### <span data-ttu-id="17ec1-238">Leuchtturm 6,2 im Leuchtturm-Panel</span><span class="sxs-lookup"><span data-stu-id="17ec1-238">Lighthouse 6.2 in the Lighthouse panel</span></span>  

<span data-ttu-id="17ec1-239">Auf dem **Leuchtturm** -Panel läuft nun Lighthouse 6,2.</span><span class="sxs-lookup"><span data-stu-id="17ec1-239">The **Lighthouse** panel is now running Lighthouse 6.2.</span></span>  <span data-ttu-id="17ec1-240">Eine vollständige Liste der Änderungen finden Sie in den [Anmerkungen zur Lighthouse-Version][GithubGooglechromeLighthouseV620].</span><span class="sxs-lookup"><span data-stu-id="17ec1-240">For a full list of changes, go to the [Lighthouse release notes][GithubGooglechromeLighthouseV620].</span></span>  

<span data-ttu-id="17ec1-241">Chromium-Problem: [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="17ec1-241">Chromium issue: [#772558][CR772558]</span></span>  

### <span data-ttu-id="17ec1-242">Deprecated of other Origins-Eintrag im Bereich "Dienstmitarbeiter"</span><span class="sxs-lookup"><span data-stu-id="17ec1-242">Deprecation of other origins listing in the Service Workers pane</span></span>  

<span data-ttu-id="17ec1-243">DevTools bietet nun einen Link im Bereich " **Dienstmitarbeiter** " \ (**Anwendungs** Bereich > Bereich " **Dienstmitarbeiter** \"), um die vollständige Liste der Servicemitarbeiter anderer Herkunft anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-243">DevTools now provides a link from the **Service workers** pane \(**Application** panel > **Service workers** pane\) to view the full list of service workers from other origins.</span></span>  <span data-ttu-id="17ec1-244">Wechseln Sie zu, um auf die Liste zuzugreifen, ohne das devtools zu öffnen `edge://service-worker-internals/?devtools` .</span><span class="sxs-lookup"><span data-stu-id="17ec1-244">To access the list without opening the DevTools, go to `edge://service-worker-internals/?devtools`.</span></span>  

<span data-ttu-id="17ec1-245">Zuvor devtools eine Liste angezeigt, die unter dem **Anwendungs** Bereich > Bereich " **Dienstmitarbeiter** " geschachtelt ist.</span><span class="sxs-lookup"><span data-stu-id="17ec1-245">Previously DevTools displayed a list nested under the **Application** panel > **Service workers** pane.</span></span>  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   <span data-ttu-id="17ec1-247">Link zu anderen Ursprüngen</span><span class="sxs-lookup"><span data-stu-id="17ec1-247">Link to other origins</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-248">Chromium-Problem: [#807440][CR807440]</span><span class="sxs-lookup"><span data-stu-id="17ec1-248">Chromium issue: [#807440][CR807440]</span></span>  

### <span data-ttu-id="17ec1-249">Anzeigen der Deckungs Zusammenfassung für gefilterte Elemente</span><span class="sxs-lookup"><span data-stu-id="17ec1-249">Show coverage summary for filtered items</span></span>  

<span data-ttu-id="17ec1-250">DevTools wird nun dynamisch neu berechnet und eine Zusammenfassung der Deckungs Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17ec1-250">DevTools now recalculate and display a summary of coverage information dynamically.</span></span>  <span data-ttu-id="17ec1-251">Die dynamische Anzeige wird ausgelöst, wenn Filter im [Coverage][DevtoolsCoverageIndex] -Tool angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="17ec1-251">The dynamic display is triggered when filters are applied in the [Coverage][DevtoolsCoverageIndex] tool.</span></span>  <span data-ttu-id="17ec1-252">Vor dem **Coverage** -Tool wird immer eine Zusammenfassung aller Deckungs Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17ec1-252">Before the **Coverage** tool always displayed a summary of all coverage information.</span></span>  

<span data-ttu-id="17ec1-253">In der ersten der folgenden Zahlen wird die Zusammenfassung zunächst angezeigt, `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` und in der zweiten der folgenden Zahlen wird die Zusammenfassung angezeigt, `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` nachdem die CSS-Filterung angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="17ec1-253">In the first of the following figures, the summary initially displays `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` and in the second of the following figures, the summary displays `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` after CSS filtering is applied.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         <span data-ttu-id="17ec1-255">Deckungs Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="17ec1-255">Coverage summary</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         <span data-ttu-id="17ec1-257">Deckungs Zusammenfassung für gefilterte Elemente</span><span class="sxs-lookup"><span data-stu-id="17ec1-257">Coverage summary for filtered items</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="17ec1-258">Chromium-Problem: [#1061385][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="17ec1-258">Chromium issue: [#1061385][CR1090802]</span></span>  

### <span data-ttu-id="17ec1-259">Neue Frame Detailansicht im Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="17ec1-259">New frame details view in Application panel</span></span>  

<span data-ttu-id="17ec1-260">DevTools zeigen nun eine detaillierte Ansicht für jeden Frame an.</span><span class="sxs-lookup"><span data-stu-id="17ec1-260">DevTools now show a detailed view for each frame.</span></span>  <span data-ttu-id="17ec1-261">Um darauf zuzugreifen, wählen Sie im **Anwendungs** Bereich unter dem Menü **Frames** einen Frame aus.</span><span class="sxs-lookup"><span data-stu-id="17ec1-261">To access it, choose a frame under the **Frames** menu in the **Application** panel.</span></span>  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/frame-details.msft.png":::
   <span data-ttu-id="17ec1-263">Neue Detailansicht für einen Frame im **Anwendungs** Bereich</span><span class="sxs-lookup"><span data-stu-id="17ec1-263">New detailed view for a frame in **Application** panel</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-264">Chromium-Problem: [#1093247][CR1093247]</span><span class="sxs-lookup"><span data-stu-id="17ec1-264">Chromium issue: [#1093247][CR1093247]</span></span>  

#### <span data-ttu-id="17ec1-265">Frame Details für geöffnete Fenster</span><span class="sxs-lookup"><span data-stu-id="17ec1-265">Frame details for opened windows</span></span>  

<span data-ttu-id="17ec1-266">Geöffnete Fenster und Popupfenster werden nun auch unter der Frame Struktur angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17ec1-266">Open windows and pop-up windows now display under the frame tree as well.</span></span>  <span data-ttu-id="17ec1-267">Die Detailansicht der geöffneten Fenster enthält zusätzliche Sicherheitsinformationen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-267">The detailed view of the opened windows includes additional security information.</span></span>  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/window-opener.msft.png":::
   <span data-ttu-id="17ec1-269">Neue Frame-Detailansicht für geöffnete Fenster</span><span class="sxs-lookup"><span data-stu-id="17ec1-269">New frame detailed view for opened windows</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-270">Chrom Problem: [#1107766] [CR1107766]</span><span class="sxs-lookup"><span data-stu-id="17ec1-270">Chromium issue: [#1107766][CR1107766]</span></span>  

#### <span data-ttu-id="17ec1-271">Sicherheits-und Isolierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="17ec1-271">Security and isolation information</span></span>  

<span data-ttu-id="17ec1-272">Sicherer Kontext, [Cross-Origin-embeder-Policy (COEP)][WebDevCoopCoep]und [Cross-Origin-Opener-Policy (Coop)][WebDevCoopCoep] werden jetzt in den Frame Details angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17ec1-272">Secure context, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep], and [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] are now displayed in the frame details.</span></span>  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/coep-coop.msft.png":::
   <span data-ttu-id="17ec1-274">Sicherheits-und Isolierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="17ec1-274">Security and isolation information</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-275">In Zukunft planen das Microsoft Edge devtools-Team und das Chrome devtools-Team, weitere Sicherheitsinformationen zu den Frame Details hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-275">In the future, the Microsoft Edge DevTools team and the Chrome DevTools team are planning to add more security information to the frame details.</span></span>  

<span data-ttu-id="17ec1-276">Chromium-Problem: [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="17ec1-276">Chromium issue: [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="17ec1-277">Elemente und Aktualisierungen des Netzwerk Panels</span><span class="sxs-lookup"><span data-stu-id="17ec1-277">Elements and Network panel updates</span></span>  

#### <span data-ttu-id="17ec1-278">Vorschlag für barrierefreie Farben im Bereich "Formatvorlagen"</span><span class="sxs-lookup"><span data-stu-id="17ec1-278">Accessible color suggestion in the Styles pane</span></span>  

<span data-ttu-id="17ec1-279">DevTools bietet jetzt Farbvorschläge für Text mit niedriger Farbkontrast.</span><span class="sxs-lookup"><span data-stu-id="17ec1-279">DevTools now provides color suggestions for low color contrast text.</span></span>  

<span data-ttu-id="17ec1-280">Im folgenden Beispiel `h1` ist Text mit geringem Kontrast.</span><span class="sxs-lookup"><span data-stu-id="17ec1-280">In the example below, `h1` has low contrast text.</span></span>  <span data-ttu-id="17ec1-281">Um das Problem zu beheben, öffnen Sie die Farbauswahl der `color` Eigenschaft im Bereich **Formatvorlagen** .</span><span class="sxs-lookup"><span data-stu-id="17ec1-281">To fix it, open the color picker of the `color` property in the **Styles** pane.</span></span>  <span data-ttu-id="17ec1-282">Nachdem Sie den Abschnitt **Kontrastverhältnis** erweitert haben, bietet devtools AA-und AAA-Farbvorschläge.</span><span class="sxs-lookup"><span data-stu-id="17ec1-282">After you expand the **Contrast ratio** section, DevTools provides AA and AAA color suggestions.</span></span>  <span data-ttu-id="17ec1-283">Wählen Sie die vorgeschlagene Farbe aus, um die Farbe anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="17ec1-283">Select the suggested color to apply the color.</span></span>  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   <span data-ttu-id="17ec1-285">Farbauswahl schlägt Vorschläge für AA-und AAA-Farben vor</span><span class="sxs-lookup"><span data-stu-id="17ec1-285">Color picker suggests AA and AAA color suggestions</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-286">Chromium-Problem: [#1093227][CR1093227]</span><span class="sxs-lookup"><span data-stu-id="17ec1-286">Chromium issue: [#1093227][CR1093227]</span></span>  

#### <span data-ttu-id="17ec1-287">Bereich ' Eigenschaften wiederherstellen ' im Bereich ' Elemente '</span><span class="sxs-lookup"><span data-stu-id="17ec1-287">Reinstate Properties pane in the Elements panel</span></span>  

<span data-ttu-id="17ec1-288">Der Bereich " **Eigenschaften** " ist "zurück".</span><span class="sxs-lookup"><span data-stu-id="17ec1-288">The **Properties** pane is back.</span></span>  <span data-ttu-id="17ec1-289">Es war [in Microsoft Edge 84 veraltet][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span><span class="sxs-lookup"><span data-stu-id="17ec1-289">It was [deprecated in Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span></span>  <span data-ttu-id="17ec1-290">Das Microsoft Edge devtools-Team und das Chrome devtools-Team planen Verbesserungen bei der Überprüfung von Eigenschaften von Elementen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-290">The Microsoft Edge DevTools team and the Chrome DevTools team are planning improvements for inspecting properties of elements.</span></span>  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/properties-pane.msft.png":::
   <span data-ttu-id="17ec1-292">Bereich ' **Eigenschaften** ' im Bereich ' **Elemente** '</span><span class="sxs-lookup"><span data-stu-id="17ec1-292">**Properties** pane in the **Elements** panel</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-293">Chromium-Problem:</span><span class="sxs-lookup"><span data-stu-id="17ec1-293">Chromium issue:</span></span>  <!--  [#1105205][CR1105205],  -->  <span data-ttu-id="17ec1-294">[#1116085] [CR1116085]</span><span class="sxs-lookup"><span data-stu-id="17ec1-294">[#1116085][CR1116085]</span></span>  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <span data-ttu-id="17ec1-295">AutoVervollständigen von benutzerdefinierten Schriftarten im Bereich "Formatvorlagen"</span><span class="sxs-lookup"><span data-stu-id="17ec1-295">Autocomplete custom fonts in the Styles pane</span></span>  

<span data-ttu-id="17ec1-296">Importierte Schrift Flächen werden jetzt der Liste der CSS-Autovervollständigung hinzugefügt, wenn die `font-family` Eigenschaft im Bereich " **Formatvorlagen** " bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="17ec1-296">Imported font faces are now added to the list of CSS autocompletion when editing the `font-family` property in the **Styles** pane.</span></span>  

<span data-ttu-id="17ec1-297">Wenn beispielsweise `monospace` eine benutzerdefinierte Schriftart auf dem lokalen Computer installiert ist, wird Sie in der Liste CSS-Vervollständigung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17ec1-297">For example, if `monospace` is a custom font installed on the local machine, it's displayed in the CSS completion list.</span></span> <span data-ttu-id="17ec1-298">In früheren Versionen von Microsoft Edge wurde die Schriftart nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17ec1-298">In previous versions of Microsoft Edge, the font wasn't displayed.</span></span>

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   <span data-ttu-id="17ec1-300">Benutzerdefinierte AutoVervollständigen-Schriftarten</span><span class="sxs-lookup"><span data-stu-id="17ec1-300">Autocomplete custom fonts</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-301">Chrom Problem: [#1106221] [CR1106221]</span><span class="sxs-lookup"><span data-stu-id="17ec1-301">Chromium issue: [#1106221][CR1106221]</span></span>  

#### <span data-ttu-id="17ec1-302">Konsistente Anzeige des Ressourcentyps in der Netzwerksteuerung</span><span class="sxs-lookup"><span data-stu-id="17ec1-302">Consistently display resource type in Network panel</span></span>  

<span data-ttu-id="17ec1-303">DevTools zeigt jetzt konsistent denselben Ressourcentyp wie die ursprüngliche Netzwerkanforderung an und fügt `/ Redirect` beim Umleiten \ (HTTP-Statuscode 302 \) den Wert der Spalte **Typ** an.</span><span class="sxs-lookup"><span data-stu-id="17ec1-303">DevTools now consistently display the same resource type as the original network request and appends `/ Redirect` to the **Type** column value when redirection \(HTTP status code 302\) happens.</span></span>  

<span data-ttu-id="17ec1-304">Zuvor hat devtools den Typ in `Other` Sometimes geändert.</span><span class="sxs-lookup"><span data-stu-id="17ec1-304">Previously DevTools changed the type to `Other` sometimes.</span></span>  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/network-redirect.msft.png":::
   <span data-ttu-id="17ec1-306">Anzeigen des Umleitungs Ressourcentyps</span><span class="sxs-lookup"><span data-stu-id="17ec1-306">Display redirect resource type</span></span>  
:::image-end:::  

<span data-ttu-id="17ec1-307">Chromium-Problem: [#997694][CR997694]</span><span class="sxs-lookup"><span data-stu-id="17ec1-307">Chromium issue: [#997694][CR997694]</span></span>  

#### <span data-ttu-id="17ec1-308">Löschen von Schaltflächen in den Elementen und Netzwerk Fenstern</span><span class="sxs-lookup"><span data-stu-id="17ec1-308">Clear buttons in the Elements and Network panels</span></span>  

<span data-ttu-id="17ec1-309">Die folgenden Textfelder verfügen nun über **klare** Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-309">The following text boxes now have **Clear** buttons.</span></span>  

*   <span data-ttu-id="17ec1-310">Die Felder ' Text filtern ' im Bereich ' **Formatvorlagen** ' und ' **Netzwerk** Bereich '</span><span class="sxs-lookup"><span data-stu-id="17ec1-310">The filter text boxes in the **Styles** pane and **Network** panel.</span></span>  
*   <span data-ttu-id="17ec1-311">Das Textfeld "Dom-Suche" im Dialogfeld " **Elemente** ".</span><span class="sxs-lookup"><span data-stu-id="17ec1-311">The DOM search text box in the **Elements** panel.</span></span>  

<span data-ttu-id="17ec1-312">Wählen Sie die Schaltfläche **Löschen** aus, um den eingegebenen Text zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-312">Choose the **Clear** button to remove any inputted text.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         <span data-ttu-id="17ec1-314">Löschen von Schaltflächen in den **Elementen** -Panels</span><span class="sxs-lookup"><span data-stu-id="17ec1-314">Clear buttons in the **Elements** panels</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         <span data-ttu-id="17ec1-316">Löschen von Schaltflächen in den  **Netzwerk** Panels</span><span class="sxs-lookup"><span data-stu-id="17ec1-316">Clear buttons in the  **Network** panels</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="17ec1-317">Chromium-Problem: [#1067184][CR1067184]</span><span class="sxs-lookup"><span data-stu-id="17ec1-317">Chromium issue: [#1067184][CR1067184]</span></span>  

## <span data-ttu-id="17ec1-318">Herunterladen der Microsoft Edge Preview-Kanäle</span><span class="sxs-lookup"><span data-stu-id="17ec1-318">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="17ec1-319">Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="17ec1-319">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="17ec1-320">Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="17ec1-320">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="17ec1-321">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="17ec1-321">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Symbol für devtools-Einstellungen"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Missbilligung des Bereichs "Eigenschaften" im Bereich "Elemente" – Neuerungen in devtools (Microsoft Edge 84) | Microsoft docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Features des CSS-Raster Debuggens – Neuerungen in devtools (Microsoft Edge 85) | Microsoft docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emulieren von mobilen Geräten in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Anpassen von Tastenkombinationen in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Aktivieren experimenteller APIs – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulation: Unterstützung des Dual-Screen-Modus – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Aktivieren der Quellauftrags Anzeige – experimentelle Features | Microsoft docs"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Emulation: Unterstützung des Dual-Screen-Modus – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Testen auf faltbaren und Dual-Screen-Geräten – experimentelle Funktionen | Microsoft docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Aktivieren von experimentellen Features – experimentelle Features | Microsoft docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "Tabelle-Console-API-Referenz | Microsoft docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Suchen Sie ungenutzten JavaScript-und CSS-Code mit der Registerkarte Coverage in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Schublade – Anpassen von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analysieren der Renderingleistung mit der Registerkarte "Rendering" – Referenz zur Leistungsanalyse | Microsoft docs"  
[DevtoolsMediaPanelIndex]: /microsoft-edge/devtools-guide-chromium/media-panel/index "Anzeigen und Debuggen von Medienplayer-Informationen | Microsoft docs"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Arbeiten mit der Naht – Einführung in Dual-Screen-Geräte | Microsoft docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "CSS mediascreen-Spanning-Funktion für Dual-Screen-Erkennung | Microsoft docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "Die getWindowSegments-JavaScript-API für Dual-Screen-Geräte | Microsoft docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Preview-Kanäle"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio-Code "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio-Code Tastenkombinationen für Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Das neue Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools Twitter-Konto"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chrom Fehler"  

[CR174309]: https://crbug.com/174309 "DevTools: zulassen der Anpassung von Tastenkombinationen/Tastenkombinationen | Chrom Fehler"
[CR384968]: https://crbug.com/384968 "Option zum ignorieren lokaler () Schriftarten | Chrom Fehler"  
[CR772558]: https://crbug.com/772558 "DevTools: Update auf die neueste Version von Lighthouse | Chrom Fehler"  
[CR807440]: https://crbug.com/807440 "Chrome sperrt mit einer hohen Anzahl von SWs | Chrom Fehler"  
[CR997694]: https://crbug.com/997694 "XMLHttpRequest-Anforderungen mit 302-Status werden nicht unter dem Filter \ "XMLHttpRequest \" im Netzwerk Panel angezeigt | Chrom Fehler"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Tabellentools | Chrom Fehler"  
[CR1051466]: https://crbug.com/1051466 "Unterstützen des Coop/COEP-Debuggens in devtools | Chrom Fehler"  
[CR1054281]: https://crbug.com/1054281 "Feature Request: devtools sollte faltbare und Dual-Screen-Geräte emulieren | Chrom Fehler"  
[CR1067184]: https://crbug.com/1067184 "Feature Request: Schaltfläche "Filter löschen" im Netzwerk &-Elemente-> Formatfilter Eingaben | Chrom Fehler"  
[CR1068116]: https://crbug.com/1068116 "☂ Bereich "Schiffs Probleme" | Chrom Fehler"  
[CR1080569]: https://crbug.com/1080569 "Acorn unterstützt keine logischen Zuweisungsoperatoren | Chrom Fehler"  
[CR1080589]: https://crbug.com/1080589 "Klassifizieren von Problemen durch Drittanbieter/First-Party | Chrom Fehler"  
[CR1086817]: https://crbug.com/1086817 "Acorn unterstützt keine numerischen Trennzeichen | Chrom Fehler"  
[CR1090802]: https://crbug.com/1090802 "Simulieren von Änderungen im Leerlaufzustand aus der Leerlauf Erkennungs-API | Chrom Fehler"  
[CR1093227]: https://crbug.com/1093227 "DevTools: empfehlen Sie die nächste barrierefreie Farbe | Chrom Fehler"  
[CR1093247]: https://crbug.com/1093247 "Anzeigen von Informationen zu Frames im Anwendungs Panel | Chrom Fehler"  
[CR1094406]: https://crbug.com/1094406 "Entwickler möchten eine Quellauftrags Anzeige für at https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: Unterstützung emuliert das Feature "bevorzugt-reduzierte Datenmedien" | Chrom Fehler"  
[CR1096481]: https://crbug.com/1096481 "Issues Banner Placement | Chrom Fehler"  
[CR1100253]: https://crbug.com/1100253 "Verknüpfung zum Hinzufügen eines Screenshot-Knotens im Kontextmenü des Elements | Chrom Fehler"  
[CR1103316]: https://crbug.com/1103316 "Beim ersten Suchergebnis wird die Element Suche nicht resolveNode (Text markieren usw.) | Chrom Fehler"  
[CR1103854]: https://crbug.com/1103854 "De-verschleiern von X-Client-Datenwerten in Developer Tools | Chrom Fehler"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: https://crbug.com/1106221 "Hinzufügen von importierten Schriftarten zur Autovervollständigung der Schriftartfamilie im Formatvorlagen-Panel | Chromium-Fehler "  
[CR1107766]: https://crbug.com/1107766 "zeigt Informationen zu Frames an, die von" Window. Open () "in der Frame Struktur generiert wurden | Chromium-Fehler "  
[CR1115011]: https://crbug.com/1115011 "beim Kopieren einer Tabelle aus der Konsole wird die Struktur der Tabelle nicht beibehalten | Chromium-Fehler "  
[CR1116085]: https://crbug.com/1116085 "Bitte bringen Sie den devtools-Eigenschafteninspektor zurück | Chromium-Fehler "  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "bevorzugt-reduzierte Datenmedien Abfragen Ebene 5 | W3C CSS-Arbeitsgruppen-Editor-Entwürfe"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v 6.2.0-GoogleChrome/Lighthouse | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Protokollpuffer | Google-Entwickler"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung USA"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Logische Zuordnung | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Numerische Trennzeichen | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Erstellen Ihrer Website \ "Cross-Origin isolated \" mit Coop und COEP | Web. dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Erkennen von inaktiven Benutzern mit der Leerlauf Erkennungs-API | Web. dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Vermeiden Sie nicht zusammengesetzte Animationen | Web. dev"  

> [!NOTE]
> <span data-ttu-id="17ec1-382">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17ec1-382">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="17ec1-383">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/updates/2020/08/devtools/index) gefunden und von [Jecelyn Yeen][JecelynYeen] \ (Developer Advocate, Chrome devtools \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="17ec1-383">The original page is found [here](https://developers.google.com/web/updates/2020/08/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="17ec1-385">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="17ec1-385">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

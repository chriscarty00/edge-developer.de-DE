---
description: Anpassen von Tastenkombinationen Visual Studio Code, Emulieren von Surface Duo und Samsung -Galaxis-Fold, Verbesserungen der CSS-Rasterüberlagerung und vieles mehr.
title: Neues in DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: ec2219e9ebdd5d79c61bcaa813f7784246b1f5d0
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564945"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-86"></a><span data-ttu-id="48ac5-104">Neues in DevTools (Microsoft Edge 86)</span><span class="sxs-lookup"><span data-stu-id="48ac5-104">What's New In DevTools (Microsoft Edge 86)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="48ac5-105">Ankündigungen des Microsoft Edge DevTools-Teams</span><span class="sxs-lookup"><span data-stu-id="48ac5-105">Announcements from the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <a name="match-keyboard-shortcuts-in-devtools-to-visual-studio-code"></a><span data-ttu-id="48ac5-106">Übereinstimmung von Tastenkombinationen in DevTools mit Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="48ac5-106">Match keyboard shortcuts in DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="48ac5-107">In Microsoft Edge 86 können Sie Tastenkombinationen in den DevTools mit Ihren Verknüpfungen in Microsoft Visual Studio [Code übereinstimmen.][VisualStudioCodeMain]</span><span class="sxs-lookup"><span data-stu-id="48ac5-107">In Microsoft Edge 86, you may match keyboard shortcuts in the DevTools to your shortcuts in [Microsoft Visual Studio Code][VisualStudioCodeMain].</span></span>  

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Übereinstimmung von Tastenkombinationen in devTools zu Visual Studio Code" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   <span data-ttu-id="48ac5-109">Übereinstimmung von Tastenkombinationen in devTools zu Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="48ac5-109">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-110">Navigieren Sie zum Aktivieren dieses Features zu [Tastenkombinationen anpassen im Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="48ac5-110">To activate this feature, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  

<span data-ttu-id="48ac5-111">Beispielsweise ist die Tastenkombination zum Anhalten oder Fortsetzen des Ausführens eines Skripts in [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] `F5` .</span><span class="sxs-lookup"><span data-stu-id="48ac5-111">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="48ac5-112">Mit der **Voreinstellung DevTools (Default)** ist dieselbe Verknüpfung in devTools , aber wenn Sie die voreingestellte Visual Studio Code auswählen, ist diese Verknüpfung `F8` jetzt auch \*\*\*\* `F5` .</span><span class="sxs-lookup"><span data-stu-id="48ac5-112">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8`, but when you choose the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="48ac5-113">Chromium Problem [#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="48ac5-113">Chromium issue [#174309][CR174309]</span></span>  

### <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a><span data-ttu-id="48ac5-114">Emulieren von Surface Duo und Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="48ac5-114">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="48ac5-116">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="48ac5-116">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-117">Sie können nun das Aussehen ihrer Website oder App auf zwei neuen Geräten testen: [Surface Duo][MicrosoftSurfaceDevicesDuo] und Samsung [Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="48ac5-117">You are now able to test the look and feel of your website or app on two new devices:  [Surface Duo][MicrosoftSurfaceDevicesDuo] and [Samsung Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.</span></span>  

<span data-ttu-id="48ac5-118">Um Ihre Website oder App für die Geräte mit dualem Bildschirm oder für die faltbare Geräte zu verbessern, verwenden Sie die folgenden Features bei der [Emulation des Geräts][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="48ac5-118">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="48ac5-119">[Aufteilung][DevtoolsDeviceModeDualScreenAndFoldables], das ist, wenn Ihre Website \(oder App\) auf beiden Bildschirmen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="48ac5-119">[Spanning][DevtoolsDeviceModeDualScreenAndFoldables], which is when your website \(or app\) appears across both screens.</span></span>
*   <span data-ttu-id="48ac5-120">[Rendering der Naht][DualScreenIntroductionHowWorkSeam], das ist der Abstand zwischen den beiden Bildschirmen.</span><span class="sxs-lookup"><span data-stu-id="48ac5-120">[Rendering the seam][DualScreenIntroductionHowWorkSeam], which is the space between the two screens.</span></span>
*   <span data-ttu-id="48ac5-121">Aktivieren experimenteller Webplattform-APIs für den Zugriff auf das neue Feature für die [Medienbildschirmübergreifende][DualScreenWebCssMediaSpanning] CSS und [die JavaScript getWindowSegments-API][DualScreenWebJavascriptGetwindowsegments].</span><span class="sxs-lookup"><span data-stu-id="48ac5-121">Enabling experimental Web Platform APIs to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [JavaScript getWindowSegments API][DualScreenWebJavascriptGetwindowsegments].</span></span>  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Geräteemulation für Surface Duo" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   <span data-ttu-id="48ac5-123">Geräteemulation für Surface Duo</span><span class="sxs-lookup"><span data-stu-id="48ac5-123">Device emulation for Surface Duo</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-124">Navigieren Sie zum Aktivieren dieses experimentellen Features zu [Aktivieren experimenteller Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **Emulation: Support dual screen mode**.</span><span class="sxs-lookup"><span data-stu-id="48ac5-124">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Emulation: Support dual screen mode**.</span></span>  

<span data-ttu-id="48ac5-125">Weitere Informationen zu diesem Feature finden Sie unter [Emulieren von Dualscreen-][DevtoolsDeviceModeDualScreenAndFoldables]und faltbaren Geräten in Microsoft Edge DevTools .</span><span class="sxs-lookup"><span data-stu-id="48ac5-125">For more information about this feature, navigate to [Emulate dual-screen and foldable devices in Microsoft Edge DevTools][DevtoolsDeviceModeDualScreenAndFoldables].</span></span>  

<span data-ttu-id="48ac5-126">Chromium Problem: [#1054281][CR1054281]</span><span class="sxs-lookup"><span data-stu-id="48ac5-126">Chromium issue: [#1054281][CR1054281]</span></span>  

### <a name="css-grid-overlay-improvements-and-new-experimental-grid-features"></a><span data-ttu-id="48ac5-127">Verbesserungen der CSS-Rasterüberlagerung und neue experimentelle Rasterfeatures</span><span class="sxs-lookup"><span data-stu-id="48ac5-127">CSS grid overlay improvements and new experimental grid features</span></span>  

<span data-ttu-id="48ac5-128">Vielen Dank für das positive Feedback zu den verbesserten CSS-Rasterüberlagerungen.</span><span class="sxs-lookup"><span data-stu-id="48ac5-128">Thank you for the positive feedback about the improved CSS grid overlays.</span></span>  <span data-ttu-id="48ac5-129">Die CSS-Rasterüberlagerungen sind jetzt standardmäßig aktiviert und erfordern nicht, dass Sie ein Experiment aktivieren.</span><span class="sxs-lookup"><span data-stu-id="48ac5-129">The CSS grid overlays are now enabled by default and do not require you to turn on an experiment.</span></span>  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="CSS-Rasterüberlagerung für artikelelement" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   <span data-ttu-id="48ac5-131">CSS-Rasterüberlagerung für `article` Element</span><span class="sxs-lookup"><span data-stu-id="48ac5-131">CSS grid overlay for `article` element</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="48ac5-132">Weitere Informationen zu Rasterüberlagerungen finden Sie unter [CSS-Rasterdebugfunktionen][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span><span class="sxs-lookup"><span data-stu-id="48ac5-132">For more information about grid overlays, navigate to [CSS grid debugging features][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="48ac5-133">Das Microsoft Edge DevTools-Team und das Chrome DevTools-Team arbeiten an weiteren Features zusammen.</span><span class="sxs-lookup"><span data-stu-id="48ac5-133">The Microsoft Edge DevTools team and the Chrome DevTools team collaborate on additional features.</span></span>  <span data-ttu-id="48ac5-134">Die neuen Features umfassen mehrere Überlagerungen, die dauerhaft und aus einem neuen **Layoutbereich** im Elementtool **konfigurierbar** sind.</span><span class="sxs-lookup"><span data-stu-id="48ac5-134">The new features include multiple overlays that are persistent and configurable from a new **Layout** pane on the **Elements** tool.</span></span>  

<span data-ttu-id="48ac5-135">Navigieren Sie zum Aktivieren dieses experimentellen Features zu [Aktivieren von experimentellen Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben Neue CSS-Raster-Debuggingfeatures aktivieren (Konfigurationsoptionen sind im Seitenleistenbereich Layout in Elementen nach dem Neustart **verfügbar)**.</span><span class="sxs-lookup"><span data-stu-id="48ac5-135">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)**.</span></span>  

<span data-ttu-id="48ac5-136">Weitere Informationen zu diesem Feature finden Sie unter [Inspect CSS Grid in Microsoft Edge DevTools][DevtoolsCssGrid].</span><span class="sxs-lookup"><span data-stu-id="48ac5-136">For more information about this feature, navigate to [Inspect CSS Grid in Microsoft Edge DevTools][DevtoolsCssGrid].</span></span>  

<span data-ttu-id="48ac5-137">Chromium Problem: [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="48ac5-137">Chromium issue: [#1047356][CR1047356]</span></span>  

### <a name="table-copied-from-the-console-preserves-formatting"></a><span data-ttu-id="48ac5-138">Aus der Konsole kopierte Tabelle behält die Formatierung bei</span><span class="sxs-lookup"><span data-stu-id="48ac5-138">Table copied from the Console preserves formatting</span></span>  

<span data-ttu-id="48ac5-139">In Microsoft Edge 85 oder früheren Versionen ist die Formatierung eines kopierten `console.table` Textes verloren gegangen.</span><span class="sxs-lookup"><span data-stu-id="48ac5-139">In Microsoft Edge 85 or earlier, the formatting of a copied `console.table` was lost.</span></span>  <span data-ttu-id="48ac5-140">Wenn Sie die Ausgabe aus der [Konsolen-API der Tabelle][DevtoolsConsoleApiTable] kopiert und eingeschrieben haben, wurde nur der Text der Tabelle beibehalten.</span><span class="sxs-lookup"><span data-stu-id="48ac5-140">If you copied the output from the [table][DevtoolsConsoleApiTable] Console API, and pasted it, only the text of the table was kept.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Table Console API output in Microsoft Edge 85 or earlier" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` <span data-ttu-id="48ac5-142">Konsolen-API-Ausgabe in Microsoft Edge 85 oder früher</span><span class="sxs-lookup"><span data-stu-id="48ac5-142">Console API output in Microsoft Edge 85 or earlier</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Table Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="48ac5-144">Konsolen-API-Ausgabe von Microsoft Edge 85 oder früher in Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="48ac5-144">Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="48ac5-145">In Microsoft Edge 86 oder höher wird die Formatierung \*\*\*\* beibehalten, wenn Sie eine Tabelle aus der Konsole kopieren.</span><span class="sxs-lookup"><span data-stu-id="48ac5-145">In Microsoft Edge 86 or later, when you copy a table from the **Console**, the formatting is now preserved.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Table Console API Output in Microsoft Edge 86 oder höher" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` <span data-ttu-id="48ac5-147">Konsolen-API-Ausgabe in Microsoft Edge 86 oder höher</span><span class="sxs-lookup"><span data-stu-id="48ac5-147">Console API output in Microsoft Edge 86 or later</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Table Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="48ac5-149">Konsolen-API-Ausgabe aus Microsoft Edge 86 oder höher, die in Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="48ac5-149">Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="48ac5-150">Chromium Problem: [#1115011][CR1115011]</span><span class="sxs-lookup"><span data-stu-id="48ac5-150">Chromium issue: [#1115011][CR1115011]</span></span>  

### <a name="source-order-viewer-for-easier-accessibility-testing"></a><span data-ttu-id="48ac5-151">Source Order Viewer für einfachere Barrierefreiheitstests</span><span class="sxs-lookup"><span data-stu-id="48ac5-151">Source Order Viewer for easier accessibility testing</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="48ac5-153">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="48ac5-153">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-154">Die neue Barrierefreiheitshilfe zeigt die Reihenfolge der Elemente in der Quelle an.</span><span class="sxs-lookup"><span data-stu-id="48ac5-154">The new accessibility helper displays the order of elements in the source.</span></span>  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Aktivieren der Quellreihenfolge anzeigen" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   <span data-ttu-id="48ac5-156">Aktivieren **der Quellreihenfolge anzeigen**</span><span class="sxs-lookup"><span data-stu-id="48ac5-156">Activate **Show source order**</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-157">Mit diesem Feature können Sie leichter testen, wie Bildschirmlese- und Tastaturbenutzer Ihre Website oder App nutzen.</span><span class="sxs-lookup"><span data-stu-id="48ac5-157">This feature makes it easier to test the way screen reader and keyboard users experience your website or app.</span></span>  <span data-ttu-id="48ac5-158">Bildschirmlesegeräte und Tastaturnavigation hängen davon ab, dass Inhalte im Quellcode Ihrer Website oder App in einer bestimmten Reihenfolge platziert werden, sodass sie der gerenderten Seite entspricht.</span><span class="sxs-lookup"><span data-stu-id="48ac5-158">Screen readers and keyboard navigation depend on content being placed in a particular order in the source code of your website or app, so that it matches the rendered page.</span></span>  <span data-ttu-id="48ac5-159">Der Quellauftragsanzeige zeigt potenzielle Unterschiede in der Reihenfolge zwischen der gerenderten Seite und dem Quellcode an.</span><span class="sxs-lookup"><span data-stu-id="48ac5-159">The Source Order Viewer displays potential differences in order between the rendered page and the source code.</span></span>  

<span data-ttu-id="48ac5-160">Navigieren Sie zum Aktivieren dieses experimentellen Features zu [Aktivieren experimenteller Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **Source Order Viewer**aktivieren.</span><span class="sxs-lookup"><span data-stu-id="48ac5-160">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Source Order Viewer**.</span></span>  

<span data-ttu-id="48ac5-161">Weitere Informationen zu diesem Experiment finden Sie unter [Source Order Viewer][DevtoolsExperimentalFeaturesSourceOrderViewer].</span><span class="sxs-lookup"><span data-stu-id="48ac5-161">For more information about this experiment, navigate to [Source Order Viewer][DevtoolsExperimentalFeaturesSourceOrderViewer].</span></span>  

<span data-ttu-id="48ac5-162">Chromium Problem: [#1094406][CR1094406]</span><span class="sxs-lookup"><span data-stu-id="48ac5-162">Chromium issue: [#1094406][CR1094406]</span></span>  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Microsoft Edge DevTools in Traditional Chinese" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Microsoft Edge DevTools in Japanese" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <a name="highlight-all-search-results-in-elements-tool"></a><span data-ttu-id="48ac5-163">Hervorheben aller Suchergebnisse im Elementtool</span><span class="sxs-lookup"><span data-stu-id="48ac5-163">Highlight all search results in Elements tool</span></span>  

<span data-ttu-id="48ac5-164">In Microsoft Edge 84 und 85 wurde das erste Suchergebnis im **Elementtool** nicht hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="48ac5-164">In Microsoft Edge 84 and 85, the first search result in the **Elements** tool did not highlight.</span></span>  <span data-ttu-id="48ac5-165">Die restlichen Suchergebnisse wurden korrekt hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="48ac5-165">The remaining search results were highlighted correctly.</span></span>  

<span data-ttu-id="48ac5-166">Vielen Dank für Das Senden Ihres Feedbacks und die Verbesserung Chromium.</span><span class="sxs-lookup"><span data-stu-id="48ac5-166">Thank you for sending your feedback and helping improve Chromium.</span></span>  <span data-ttu-id="48ac5-167">Ihr Feedback deckte Problem [#1103316][CR1103316] im Open-Source-Chromium auf.</span><span class="sxs-lookup"><span data-stu-id="48ac5-167">Your feedback uncovered Issue [#1103316][CR1103316] in the open-source Chromium project.</span></span>  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Hervorgehobenes erstes Suchergebnis im Elementbereich in Microsoft Edge 84 oder höher" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   <span data-ttu-id="48ac5-169">Hervorgehobenes erstes Suchergebnis im **Elementtool** in Microsoft Edge 84 oder höher</span><span class="sxs-lookup"><span data-stu-id="48ac5-169">Highlighted first search result on **Elements** tool in Microsoft Edge 84 or later</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-170">Das Problem wurde jetzt in allen Versionen von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="48ac5-170">The issue is now fixed in all versions of Microsoft Edge.</span></span>  

<span data-ttu-id="48ac5-171">Chromium Problem: [#1103316][CR1103316]</span><span class="sxs-lookup"><span data-stu-id="48ac5-171">Chromium issue: [#1103316][CR1103316]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="48ac5-172">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="48ac5-172">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-media-tool"></a><span data-ttu-id="48ac5-173">Tool für neue Medien</span><span class="sxs-lookup"><span data-stu-id="48ac5-173">New Media tool</span></span>  

<span data-ttu-id="48ac5-174">DevTools zeigt jetzt Media Player-Informationen im Tool [Media][DevtoolsMediaPanelIndex] an.</span><span class="sxs-lookup"><span data-stu-id="48ac5-174">DevTools now displays media players information in the [Media][DevtoolsMediaPanelIndex] tool.</span></span>  

<span data-ttu-id="48ac5-175">Führen Sie den folgenden Schritt aus, um das neue **Medientool** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="48ac5-175">To open the new **Media** tool, complete the following step.</span></span>  

1.  <span data-ttu-id="48ac5-176">Wählen **Sie Anpassen und Steuern devTools** \( `...` \) > Weitere **Tools**  >  **Media aus.**</span><span class="sxs-lookup"><span data-stu-id="48ac5-176">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Tool für neue Medien" lightbox="../../media/2020/08/media-panel.msft.png":::
       <span data-ttu-id="48ac5-178">Tool **für neue Medien**</span><span class="sxs-lookup"><span data-stu-id="48ac5-178">New **Media** tool</span></span>  
    :::image-end:::  

<span data-ttu-id="48ac5-179">Vor dem neuen **Medientool** in DevTools befanden sich die Protokollierungs- und Debuginformationen zu Video playern unter der **Einstellung Zuletzt verwendeter Player.**</span><span class="sxs-lookup"><span data-stu-id="48ac5-179">Before the new **Media** tool in DevTools, the logging and debug information about video players was located under the **Recent Players** setting.</span></span>  <span data-ttu-id="48ac5-180">Navigieren Sie zum Öffnen der Einstellung Zuletzt **verwendeter Spieler,** `edge://media-internals` und wählen Sie das Tool **Spieler** aus.</span><span class="sxs-lookup"><span data-stu-id="48ac5-180">To open the **Recent Players** setting, navigate to `edge://media-internals` and choose the **Players** tool.</span></span>  

<span data-ttu-id="48ac5-181">Zeigen Sie Liveinhalte an, und untersuchen Sie potenzielle Probleme schneller, einschließlich der folgenden Beispiele.</span><span class="sxs-lookup"><span data-stu-id="48ac5-181">View live content and inspect potential issues more quickly, including the following examples.</span></span>  

*   <span data-ttu-id="48ac5-182">Warum werden Frames verworfen?</span><span class="sxs-lookup"><span data-stu-id="48ac5-182">Why frames are dropped?</span></span>  
*   <span data-ttu-id="48ac5-183">Warum interagiert JavaScript unerwartet mit dem Spieler?</span><span class="sxs-lookup"><span data-stu-id="48ac5-183">Why JavaScript is interacting with the player in an unexpected way?</span></span>  

### <a name="capture-node-screenshots-using-the-elements-tool-context-menu"></a><span data-ttu-id="48ac5-184">Erfassen von Knoten-Screenshots mithilfe des Kontextmenüs des Elements-Tools</span><span class="sxs-lookup"><span data-stu-id="48ac5-184">Capture node screenshots using the Elements tool context menu</span></span>  

<span data-ttu-id="48ac5-185">Sie können jetzt Knoten-Screenshots mithilfe des Kontextmenüs im **Elementtool** erfassen.</span><span class="sxs-lookup"><span data-stu-id="48ac5-185">You may now capture node screenshots using the context menu in the **Elements** tool.</span></span>  

<span data-ttu-id="48ac5-186">Um beispielsweise einen Screenshot des Inhaltsverzeichnisses zu erstellen, zeigen Sie auf das Element, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie Screenshot des Knotens **erfassen aus.**</span><span class="sxs-lookup"><span data-stu-id="48ac5-186">For example, to take a screenshot of the table of contents, hover on the element, open the contextual menu \(right-click\), and select **Capture node screenshot**.</span></span>  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Screenshots des Aufnahmeknotens" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   <span data-ttu-id="48ac5-188">Screenshots des Aufnahmeknotens</span><span class="sxs-lookup"><span data-stu-id="48ac5-188">Capture node screenshots</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-189">Chromium Problem: [#1100253][CR1100253]</span><span class="sxs-lookup"><span data-stu-id="48ac5-189">Chromium issue: [#1100253][CR1100253]</span></span>  

### <a name="issues-tool-updates"></a><span data-ttu-id="48ac5-190">Probleme mit Toolupdates</span><span class="sxs-lookup"><span data-stu-id="48ac5-190">Issues tool updates</span></span>  

<span data-ttu-id="48ac5-191">Die Warnmeldungsleiste Probleme im **Konsolentool** wird jetzt durch eine reguläre Meldung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="48ac5-191">The Issues warning bar on the **Console** tool is now replaced with a regular message.</span></span>  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Probleme in Konsolennachrichten" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   <span data-ttu-id="48ac5-193">Probleme in Konsolennachrichten</span><span class="sxs-lookup"><span data-stu-id="48ac5-193">Issues in console message</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-194">Cookieprobleme von Drittanbietern werden jetzt standardmäßig im **Problemtool** ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="48ac5-194">Third-party cookie issues are now hidden by default in the **Issues** tool.</span></span>  <span data-ttu-id="48ac5-195">Aktivieren Sie das neue **Kontrollkästchen Cookieprobleme von** Drittanbietern enthalten, um die Probleme anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="48ac5-195">Enable the new **Include third-party cookie issues** checkbox to view the issues.</span></span>  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Kontrollkästchen für Cookieprobleme von Drittanbietern" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   <span data-ttu-id="48ac5-197">Kontrollkästchen für Cookieprobleme von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="48ac5-197">third-party cookie issues checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-198">Chromium Probleme: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span><span class="sxs-lookup"><span data-stu-id="48ac5-198">Chromium issues: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span></span>  

### <a name="emulate-missing-local-fonts"></a><span data-ttu-id="48ac5-199">Emulieren fehlender lokaler Schriftarten</span><span class="sxs-lookup"><span data-stu-id="48ac5-199">Emulate missing local fonts</span></span>  

<span data-ttu-id="48ac5-200">Öffnen Sie [das Renderingtool,][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] und verwenden Sie das neue Feature Lokale **Schriftarten** deaktivieren, um fehlende `local()` Quellen in Regeln zu `@font-face` emulieren.</span><span class="sxs-lookup"><span data-stu-id="48ac5-200">Open the [Rendering tool][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] and use the new **Disable local fonts** feature to emulate missing `local()` sources in `@font-face` rules.</span></span>  

<span data-ttu-id="48ac5-201">Wenn die Schriftart beispielsweise auf Ihrem Gerät installiert ist und von der Regel als Schriftart verwendet wird, verwendet Microsoft Edge die lokale Schriftartdatei `Rubik` `@font-face src` von Ihrem `local()` Gerät.</span><span class="sxs-lookup"><span data-stu-id="48ac5-201">For example, when the `Rubik` font is installed on your device and the `@font-face src` rule uses it as a `local()` font, Microsoft Edge uses the local font file from your device.</span></span>  

<span data-ttu-id="48ac5-202">Wenn **Lokale Schriftarten deaktivieren** aktiviert ist, ignoriert DevTools die Schriftarten und ruft jede Schriftart aus dem Netzwerk `local()` ab.</span><span class="sxs-lookup"><span data-stu-id="48ac5-202">When **Disable local fonts** is enabled, DevTools ignores the `local()` fonts and fetches each from the network.</span></span>  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Emulieren fehlender lokaler Schriftarten" lightbox="../../media/2020/08/disable-font.msft.png":::
   <span data-ttu-id="48ac5-204">Emulieren fehlender lokaler Schriftarten</span><span class="sxs-lookup"><span data-stu-id="48ac5-204">Emulate missing local fonts</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-205">Wenn Sie während der Entwicklung zwei unterschiedliche Kopien derselben Schriftart verwenden, z. B. die folgenden Beispiele.</span><span class="sxs-lookup"><span data-stu-id="48ac5-205">If you use two different copies of the same font during development, such as the following examples.</span></span>  

*   <span data-ttu-id="48ac5-206">Eine lokale Schriftart für Ihre Designtools.</span><span class="sxs-lookup"><span data-stu-id="48ac5-206">A local font for your design tools.</span></span>  
*   <span data-ttu-id="48ac5-207">Eine Webschriftart für Ihren Code.</span><span class="sxs-lookup"><span data-stu-id="48ac5-207">A web font for your code.</span></span>  

<span data-ttu-id="48ac5-208">Verwenden **Sie Lokale Schriftarten deaktivieren,** um ihnen das Ausführen der folgenden Aufgaben zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="48ac5-208">Use **Disable local fonts** to make it easier for you to complete the following tasks.</span></span>  

*   <span data-ttu-id="48ac5-209">Debuggen und Messen der Ladeleistung und Optimierung von Webschriftarten.</span><span class="sxs-lookup"><span data-stu-id="48ac5-209">Debug and measure loading performance and optimization of web fonts.</span></span>  
*   <span data-ttu-id="48ac5-210">Überprüfen Sie die Genauigkeit Ihrer `@font-face` CSS-Regeln.</span><span class="sxs-lookup"><span data-stu-id="48ac5-210">Verify accuracy of your CSS `@font-face` rules.</span></span>  
*   <span data-ttu-id="48ac5-211">Ermitteln Sie Unterschiede zwischen lokalen Versionen, die auf Ihrem Gerät installiert sind, und einer Webschriftart.</span><span class="sxs-lookup"><span data-stu-id="48ac5-211">Discover differences between local versions installed on your device and a web font.</span></span>  

<span data-ttu-id="48ac5-212">Chromium Problem: [#384968][CR384968]</span><span class="sxs-lookup"><span data-stu-id="48ac5-212">Chromium issue: [#384968][CR384968]</span></span>  

### <a name="emulate-inactive-users"></a><span data-ttu-id="48ac5-213">Emulieren inaktiver Benutzer</span><span class="sxs-lookup"><span data-stu-id="48ac5-213">Emulate inactive users</span></span>  

<span data-ttu-id="48ac5-214">Die [Idle Detection-API][WebDevIdleDetection] ermöglicht Es Entwicklern, inaktive Benutzer zu erkennen und auf Änderungen des Leerlaufzustands zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="48ac5-214">The [Idle Detection API][WebDevIdleDetection] allows developers to detect inactive users and react on idle state changes.</span></span>  <span data-ttu-id="48ac5-215">Sie können devTools nun verwenden, um Änderungen des Leerlaufzustands im Tool **Sensoren** sowohl für den Benutzerstatus als auch für den Bildschirmzustand zu emulieren, anstatt auf die Änderung des tatsächlichen Leerlaufzustands zu warten.</span><span class="sxs-lookup"><span data-stu-id="48ac5-215">You are now able to use DevTools to emulate idle state changes in the **Sensors** tool for both the user state and the screen state instead of waiting for the actual idle state to change.</span></span>  <span data-ttu-id="48ac5-216">Sie können das Tool **"Sensors"** in der [Drawer öffnen.][DevtoolsCustomizeIndexDrawer]</span><span class="sxs-lookup"><span data-stu-id="48ac5-216">You may open the **Sensors** tool from the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Emulieren inaktiver Benutzer" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   <span data-ttu-id="48ac5-218">Emulieren inaktiver Benutzer</span><span class="sxs-lookup"><span data-stu-id="48ac5-218">Emulate inactive users</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-219">Chromium Problem: [#1090802][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="48ac5-219">Chromium issue: [#1090802][CR1090802]</span></span>  

### <a name="emulate-prefers-reduced-data"></a><span data-ttu-id="48ac5-220">Emulieren von prefers-reduced-data</span><span class="sxs-lookup"><span data-stu-id="48ac5-220">Emulate prefers-reduced-data</span></span>  

> [!NOTE]
> <span data-ttu-id="48ac5-221">Navigieren Microsoft Edge 86, um dieses Feature zu aktivieren, zu und aktivieren Sie das Flag für Features der `edge://flags#enable-experimental-web-platform-features` **Experimentellen** Webplattform.</span><span class="sxs-lookup"><span data-stu-id="48ac5-221">In Microsoft Edge 86, to enable this feature, navigate to `edge://flags#enable-experimental-web-platform-features` and turn on the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="48ac5-222">Die Emulationsoption wird nur angezeigt, wenn das Flag aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="48ac5-222">The emulation option is only displayed if the flag is enabled.</span></span>  

<span data-ttu-id="48ac5-223">Die [Prefers-reduced-Data Media-Abfrage][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] erkennt Benutzerinhaltseinstellungen für reduzierte Daten.</span><span class="sxs-lookup"><span data-stu-id="48ac5-223">The [prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] media query detects user content preferences for reduced data.</span></span>  <span data-ttu-id="48ac5-224">Wenn diese Option ausgewählt ist, erhält der Benutzer alternative Seiteninhalte, die weniger Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="48ac5-224">If selected, the user receives alternate page content that uses less data.</span></span>  

<span data-ttu-id="48ac5-225">Sie können jetzt DevTools verwenden, um die `prefers-reduced-data` Medienabfrage zu emulieren.</span><span class="sxs-lookup"><span data-stu-id="48ac5-225">You may now use DevTools to emulate the `prefers-reduced-data` media query.</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Emulieren von prefers-reduced-data" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   <span data-ttu-id="48ac5-227">Emulieren von prefers-reduced-data</span><span class="sxs-lookup"><span data-stu-id="48ac5-227">Emulate prefers-reduced-data</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-228">Chromium Problem: [#1096068][CR1096068]</span><span class="sxs-lookup"><span data-stu-id="48ac5-228">Chromium issue: [#1096068][CR1096068]</span></span>  

### <a name="support-for-new-javascript-features"></a><span data-ttu-id="48ac5-229">Unterstützung für neue JavaScript-Features</span><span class="sxs-lookup"><span data-stu-id="48ac5-229">Support for new JavaScript features</span></span>  

<span data-ttu-id="48ac5-230">DevTools haben jetzt die folgenden JavaScript-Sprachfeatures besser unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48ac5-230">DevTools now have better supported the following JavaScript language features.</span></span>  

| <span data-ttu-id="48ac5-231">JavaScript-Sprachfeature</span><span class="sxs-lookup"><span data-stu-id="48ac5-231">JavaScript language feature</span></span> | <span data-ttu-id="48ac5-232">Details</span><span class="sxs-lookup"><span data-stu-id="48ac5-232">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="48ac5-233">Logische Zuweisungsoperatoren</span><span class="sxs-lookup"><span data-stu-id="48ac5-233">Logical assignment operators</span></span>][V8FeaturesLogicalAssignment] | <span data-ttu-id="48ac5-234">DevTools unterstützt jetzt die logische Zuordnung mit den neuen `&&=` Operatoren `||=` , und in `??=` den **Konsolen-** und **Quellentools.**</span><span class="sxs-lookup"><span data-stu-id="48ac5-234">DevTools now supports logical assignment with the new `&&=`, `||=`, and `??=` operators in the **Console** and **Sources** tools.</span></span>  |  
| <span data-ttu-id="48ac5-235">Ziemlich gedruckte [numerische Trennzeichen][V8FeaturesNumericSeparators]</span><span class="sxs-lookup"><span data-stu-id="48ac5-235">Pretty-print [numeric separators][V8FeaturesNumericSeparators]</span></span> | <span data-ttu-id="48ac5-236">DevTools druckt nun die numerischen Trennzeichen im Tool **Sources ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="48ac5-236">DevTools now properly pretty-prints the numeric separators in the **Sources** tool.</span></span>  |  

<span data-ttu-id="48ac5-237">Chromium: [1086817][CR1086817], [1080569][CR1080569]</span><span class="sxs-lookup"><span data-stu-id="48ac5-237">Chromium issues: [1086817][CR1086817], [1080569][CR1080569]</span></span>  

### <a name="lighthouse-62-in-the-lighthouse-panel"></a><span data-ttu-id="48ac5-238">Leuchttürme 6.2 im Bereich "Leuchttürme"</span><span class="sxs-lookup"><span data-stu-id="48ac5-238">Lighthouse 6.2 in the Lighthouse panel</span></span>  

<span data-ttu-id="48ac5-239">Das **Tool "Leuchtturm"** wird jetzt mit "6.2" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48ac5-239">The **Lighthouse** tool is now running Lighthouse 6.2.</span></span>  <span data-ttu-id="48ac5-240">Eine vollständige Liste der Änderungen finden Sie in den [Anmerkungen zur Veröffentlichung von "Leuchttürme".][GithubGooglechromeLighthouseV620]</span><span class="sxs-lookup"><span data-stu-id="48ac5-240">For a full list of changes, navigate to the [Lighthouse release notes][GithubGooglechromeLighthouseV620].</span></span>  

<span data-ttu-id="48ac5-241">Chromium Problem: [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="48ac5-241">Chromium issue: [#772558][CR772558]</span></span>  

### <a name="deprecation-of-other-origins-listing-in-the-service-workers-pane"></a><span data-ttu-id="48ac5-242">Veraltetes Auflisten anderer Ursprünge im Bereich "Service Workers"</span><span class="sxs-lookup"><span data-stu-id="48ac5-242">Deprecation of other origins listing in the Service Workers pane</span></span>  

<span data-ttu-id="48ac5-243">DevTools stellt nun einen Link aus dem Bereich Service **workers** **\(** Anwendungstool > Dienstmitarbeiterbereich\) zur Verfügung, um die vollständige Liste der Servicemitarbeiter anderer Ursprünge anzuzeigen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="48ac5-243">DevTools now provides a link from the **Service workers** pane \(**Application** tool > **Service workers** pane\) to view the full list of service workers from other origins.</span></span>  <span data-ttu-id="48ac5-244">Navigieren Sie zu, um auf die Liste zu zugreifen, ohne die DevTools zu `edge://service-worker-internals/?devtools` öffnen.</span><span class="sxs-lookup"><span data-stu-id="48ac5-244">To access the list without opening the DevTools, navigate to `edge://service-worker-internals/?devtools`.</span></span>  

<span data-ttu-id="48ac5-245">Zuvor hat DevTools eine Liste angezeigt, die unter dem Anwendungstool **>** **Dienstmitarbeiterbereich geschachtelt** ist.</span><span class="sxs-lookup"><span data-stu-id="48ac5-245">Previously DevTools displayed a list nested under the **Application** tool > **Service workers** pane.</span></span>  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Link zu anderen Ursprüngen" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   <span data-ttu-id="48ac5-247">Link zu anderen Ursprüngen</span><span class="sxs-lookup"><span data-stu-id="48ac5-247">Link to other origins</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-248">Chromium Problem: [#807440][CR807440]</span><span class="sxs-lookup"><span data-stu-id="48ac5-248">Chromium issue: [#807440][CR807440]</span></span>  

### <a name="show-coverage-summary-for-filtered-items"></a><span data-ttu-id="48ac5-249">Anzeigen der Abdeckungszusammenfassung für gefilterte Elemente</span><span class="sxs-lookup"><span data-stu-id="48ac5-249">Show coverage summary for filtered items</span></span>  

<span data-ttu-id="48ac5-250">DevTools berechnet nun neu und zeigt dynamisch eine Zusammenfassung der Abdeckungsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="48ac5-250">DevTools now recalculate and display a summary of coverage information dynamically.</span></span>  <span data-ttu-id="48ac5-251">Die dynamische Anzeige wird ausgelöst, wenn Filter im [Coverage-Tool angewendet][DevtoolsCoverageIndex] werden.</span><span class="sxs-lookup"><span data-stu-id="48ac5-251">The dynamic display is triggered when filters are applied in the [Coverage][DevtoolsCoverageIndex] tool.</span></span>  <span data-ttu-id="48ac5-252">Bevor das **Coverage-Tool** immer eine Zusammenfassung aller Abdeckungsinformationen angezeigt hat.</span><span class="sxs-lookup"><span data-stu-id="48ac5-252">Before the **Coverage** tool always displayed a summary of all coverage information.</span></span>  

<span data-ttu-id="48ac5-253">In der ersten der folgenden Abbildungen wird zunächst die Zusammenfassung angezeigt, und in der zweiten der folgenden Abbildungen wird die Zusammenfassung angezeigt, nachdem die `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` CSS-Filterung angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="48ac5-253">In the first of the following figures, the summary initially displays `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` and in the second of the following figures, the summary displays `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` after CSS filtering is applied.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Zusammenfassung der Abdeckung" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         <span data-ttu-id="48ac5-255">Zusammenfassung der Abdeckung</span><span class="sxs-lookup"><span data-stu-id="48ac5-255">Coverage summary</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Abdeckungszusammenfassung für gefilterte Elemente" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         <span data-ttu-id="48ac5-257">Abdeckungszusammenfassung für gefilterte Elemente</span><span class="sxs-lookup"><span data-stu-id="48ac5-257">Coverage summary for filtered items</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="48ac5-258">Chromium Problem: [#1061385][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="48ac5-258">Chromium issue: [#1061385][CR1090802]</span></span>  

### <a name="new-frame-details-view-in-application-panel"></a><span data-ttu-id="48ac5-259">Neue Framedetailseansicht im Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="48ac5-259">New frame details view in Application panel</span></span>  

<span data-ttu-id="48ac5-260">DevTools zeigt jetzt eine detaillierte Ansicht für jeden Frame an.</span><span class="sxs-lookup"><span data-stu-id="48ac5-260">DevTools now show a detailed view for each frame.</span></span>  <span data-ttu-id="48ac5-261">Um darauf zu zugreifen, wählen Sie im Anwendungstool unter dem Menü **Frames** einen **Frame** aus.</span><span class="sxs-lookup"><span data-stu-id="48ac5-261">To access it, choose a frame under the **Frames** menu in the **Application** tool.</span></span>  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Neue Detailansicht für einen Frame im Anwendungsbereich" lightbox="../../media/2020/08/frame-details.msft.png":::
   <span data-ttu-id="48ac5-263">Neue Detailansicht für einen Frame im **Anwendungstool**</span><span class="sxs-lookup"><span data-stu-id="48ac5-263">New detailed view for a frame in **Application** tool</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-264">Chromium Problem: [#1093247][CR1093247]</span><span class="sxs-lookup"><span data-stu-id="48ac5-264">Chromium issue: [#1093247][CR1093247]</span></span>  

#### <a name="frame-details-for-opened-windows"></a><span data-ttu-id="48ac5-265">Framedetails für geöffnete Fenster</span><span class="sxs-lookup"><span data-stu-id="48ac5-265">Frame details for opened windows</span></span>  

<span data-ttu-id="48ac5-266">Geöffnete Fenster und Popupfenster werden nun auch unter der Framestruktur angezeigt.</span><span class="sxs-lookup"><span data-stu-id="48ac5-266">Open windows and pop-up windows now display under the frame tree as well.</span></span>  <span data-ttu-id="48ac5-267">Die detaillierte Ansicht der geöffneten Fenster enthält zusätzliche Sicherheitsinformationen.</span><span class="sxs-lookup"><span data-stu-id="48ac5-267">The detailed view of the opened windows includes additional security information.</span></span>  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Neue Frame-Detailansicht für geöffnete Fenster" lightbox="../../media/2020/08/window-opener.msft.png":::
   <span data-ttu-id="48ac5-269">Neue Frame-Detailansicht für geöffnete Fenster</span><span class="sxs-lookup"><span data-stu-id="48ac5-269">New frame detailed view for opened windows</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-270">Chromium Problem: [#1107766][CR1107766]</span><span class="sxs-lookup"><span data-stu-id="48ac5-270">Chromium issue: [#1107766][CR1107766]</span></span>  

#### <a name="security-and-isolation-information"></a><span data-ttu-id="48ac5-271">Sicherheits- und Isolationsinformationen</span><span class="sxs-lookup"><span data-stu-id="48ac5-271">Security and isolation information</span></span>  

<span data-ttu-id="48ac5-272">Sicherer Kontext, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep]und [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] werden nun in den Framedetails angezeigt.</span><span class="sxs-lookup"><span data-stu-id="48ac5-272">Secure context, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep], and [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] are now displayed in the frame details.</span></span>  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Sicherheits- und Isolationsinformationen" lightbox="../../media/2020/08/coep-coop.msft.png":::
   <span data-ttu-id="48ac5-274">Sicherheits- und Isolationsinformationen</span><span class="sxs-lookup"><span data-stu-id="48ac5-274">Security and isolation information</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-275">In Zukunft planen das Microsoft Edge DevTools-Team und das Chrome DevTools-Team, den Framedetails weitere Sicherheitsinformationen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="48ac5-275">In the future, the Microsoft Edge DevTools team and the Chrome DevTools team are planning to add more security information to the frame details.</span></span>  

<span data-ttu-id="48ac5-276">Chromium Problem: [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="48ac5-276">Chromium issue: [#1051466][CR1051466]</span></span>  

### <a name="elements-and-network-panel-updates"></a><span data-ttu-id="48ac5-277">Updates für Elemente und Netzwerkpanels</span><span class="sxs-lookup"><span data-stu-id="48ac5-277">Elements and Network panel updates</span></span>  

#### <a name="accessible-color-suggestion-in-the-styles-pane"></a><span data-ttu-id="48ac5-278">Barrierefreier Farbvorschlag im Bereich Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="48ac5-278">Accessible color suggestion in the Styles pane</span></span>  

<span data-ttu-id="48ac5-279">DevTools bietet nun Farbvorschläge für Text mit geringem Farbkontrast.</span><span class="sxs-lookup"><span data-stu-id="48ac5-279">DevTools now provides color suggestions for low color contrast text.</span></span>  

<span data-ttu-id="48ac5-280">Im folgenden Beispiel hat `h1` Text mit geringem Kontrast.</span><span class="sxs-lookup"><span data-stu-id="48ac5-280">In the example below, `h1` has low contrast text.</span></span>  <span data-ttu-id="48ac5-281">Um dies zu beheben, öffnen Sie die Farbauswahl der `color` Eigenschaft im **Bereich Formatvorlagen.**</span><span class="sxs-lookup"><span data-stu-id="48ac5-281">To fix it, open the color picker of the `color` property in the **Styles** pane.</span></span>  <span data-ttu-id="48ac5-282">Nachdem Sie den Abschnitt **Kontrastverhältnis** erweitert haben, stellt DevTools AA- und AAA-Farbvorschläge zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="48ac5-282">After you expand the **Contrast ratio** section, DevTools provides AA and AAA color suggestions.</span></span>  <span data-ttu-id="48ac5-283">Wählen Sie die vorgeschlagene Farbe aus, um die Farbe anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="48ac5-283">Choose the suggested color to apply the color.</span></span>  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Farbauswahl schlägt AA- und AAA-Farbvorschläge vor" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   <span data-ttu-id="48ac5-285">Farbauswahl schlägt AA- und AAA-Farbvorschläge vor</span><span class="sxs-lookup"><span data-stu-id="48ac5-285">Color picker suggests AA and AAA color suggestions</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-286">Chromium Problem: [#1093227][CR1093227]</span><span class="sxs-lookup"><span data-stu-id="48ac5-286">Chromium issue: [#1093227][CR1093227]</span></span>  

#### <a name="reinstate-properties-pane-in-the-elements-panel"></a><span data-ttu-id="48ac5-287">Bereich Eigenschaften im Elementbereich neu festlegen</span><span class="sxs-lookup"><span data-stu-id="48ac5-287">Reinstate Properties pane in the Elements panel</span></span>  

<span data-ttu-id="48ac5-288">Der **Bereich** Eigenschaften ist zurück.</span><span class="sxs-lookup"><span data-stu-id="48ac5-288">The **Properties** pane is back.</span></span>  <span data-ttu-id="48ac5-289">In [84 wurde Microsoft Edge veraltet.][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]</span><span class="sxs-lookup"><span data-stu-id="48ac5-289">It was [deprecated in Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span></span>  <span data-ttu-id="48ac5-290">Das Microsoft Edge DevTools-Team und das Chrome DevTools-Team planen Verbesserungen für die Überprüfung der Eigenschaften von Elementen.</span><span class="sxs-lookup"><span data-stu-id="48ac5-290">The Microsoft Edge DevTools team and the Chrome DevTools team are planning improvements for inspecting properties of elements.</span></span>  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Eigenschaftenbereich im Elementbereich" lightbox="../../media/2020/08/properties-pane.msft.png":::
   <span data-ttu-id="48ac5-292">**Eigenschaftenbereich** im **Elementtool**</span><span class="sxs-lookup"><span data-stu-id="48ac5-292">**Properties** pane in the **Elements** tool</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-293">Chromium Problem:</span><span class="sxs-lookup"><span data-stu-id="48ac5-293">Chromium issue:</span></span>  <!--  [#1105205][CR1105205],  -->  <span data-ttu-id="48ac5-294">[#1116085] [CR1116085]</span><span class="sxs-lookup"><span data-stu-id="48ac5-294">[#1116085][CR1116085]</span></span>  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Human-readable `X-Client-Data` header values" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <a name="autocomplete-custom-fonts-in-the-styles-pane"></a><span data-ttu-id="48ac5-295">Automatisches Kompletieren benutzerdefinierter Schriftarten im Bereich Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="48ac5-295">Autocomplete custom fonts in the Styles pane</span></span>  

<span data-ttu-id="48ac5-296">Importierte Schriftartengesichter werden nun der Liste der automatischen CSS-Vervollständigung hinzugefügt, wenn die Eigenschaft im `font-family` Bereich **Formatvorlagen bearbeitet** wird.</span><span class="sxs-lookup"><span data-stu-id="48ac5-296">Imported font faces are now added to the list of CSS autocompletion when editing the `font-family` property in the **Styles** pane.</span></span>  

<span data-ttu-id="48ac5-297">Wenn beispielsweise eine benutzerdefinierte Schriftart auf dem lokalen Computer installiert ist, wird `monospace` sie in der Css-Abschlussliste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="48ac5-297">For example, if `monospace` is a custom font installed on the local machine, it displays in the CSS completion list.</span></span>  <span data-ttu-id="48ac5-298">In früheren Versionen von Microsoft Edge wurde die Schriftart nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="48ac5-298">In previous versions of Microsoft Edge, the font was not displayed.</span></span>

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Automatisches Kompletieren benutzerdefinierter Schriftarten" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   <span data-ttu-id="48ac5-300">Automatisches Kompletieren benutzerdefinierter Schriftarten</span><span class="sxs-lookup"><span data-stu-id="48ac5-300">Autocomplete custom fonts</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-301">Chromium Problem: [#1106221][CR1106221]</span><span class="sxs-lookup"><span data-stu-id="48ac5-301">Chromium issue: [#1106221][CR1106221]</span></span>  

#### <a name="consistently-display-resource-type-in-network-panel"></a><span data-ttu-id="48ac5-302">Konsistenter Ressourcentyp im Netzwerkbereich anzeigen</span><span class="sxs-lookup"><span data-stu-id="48ac5-302">Consistently display resource type in Network panel</span></span>  

<span data-ttu-id="48ac5-303">DevTools zeigen jetzt konsistent denselben Ressourcentyp wie die ursprüngliche Netzwerkanforderung an und fügen den Wert der Spalte Type an, wenn die Umleitung `/ Redirect` \(HTTP-Statuscode 302\) erfolgt. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="48ac5-303">DevTools now consistently display the same resource type as the original network request and appends `/ Redirect` to the **Type** column value when redirection \(HTTP status code 302\) happens.</span></span>  

<span data-ttu-id="48ac5-304">Zuvor hat DevTools den Typ in manchmal `Other` geändert.</span><span class="sxs-lookup"><span data-stu-id="48ac5-304">Previously DevTools changed the type to `Other` sometimes.</span></span>  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Umleitungsressourcentyp anzeigen" lightbox="../../media/2020/08/network-redirect.msft.png":::
   <span data-ttu-id="48ac5-306">Umleitungsressourcentyp anzeigen</span><span class="sxs-lookup"><span data-stu-id="48ac5-306">Display redirect resource type</span></span>  
:::image-end:::  

<span data-ttu-id="48ac5-307">Chromium Problem: [#997694][CR997694]</span><span class="sxs-lookup"><span data-stu-id="48ac5-307">Chromium issue: [#997694][CR997694]</span></span>  

#### <a name="clear-buttons-in-the-elements-and-network-tools"></a><span data-ttu-id="48ac5-308">Löschen von Schaltflächen in den Elementen und Netzwerktools</span><span class="sxs-lookup"><span data-stu-id="48ac5-308">Clear buttons in the Elements and Network tools</span></span>  

<span data-ttu-id="48ac5-309">Die folgenden Textfelder verfügen jetzt über **Schaltflächen löschen.**</span><span class="sxs-lookup"><span data-stu-id="48ac5-309">The following text boxes now have **Clear** buttons.</span></span>  

*   <span data-ttu-id="48ac5-310">Die Filtertextfelder im **Bereich Formatvorlagen** und **im Netzwerktool.**</span><span class="sxs-lookup"><span data-stu-id="48ac5-310">The filter text boxes in the **Styles** pane and **Network** tool.</span></span>  
*   <span data-ttu-id="48ac5-311">Das Textfeld DOM-Suche im **Elementtool.**</span><span class="sxs-lookup"><span data-stu-id="48ac5-311">The DOM search text box in the **Elements** tool.</span></span>  

<span data-ttu-id="48ac5-312">Wählen Sie die **Schaltfläche Löschen** aus, um eingegebenen Text zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="48ac5-312">Choose the **Clear** button to remove any inputted text.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Löschen von Schaltflächen in den Elementen-Panels" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         <span data-ttu-id="48ac5-314">Löschen von Schaltflächen in den **Elements-Tools**</span><span class="sxs-lookup"><span data-stu-id="48ac5-314">Clear buttons in the **Elements** tools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Löschen von Schaltflächen in den Netzwerkpanels" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         <span data-ttu-id="48ac5-316">Löschen von Schaltflächen in den **Netzwerktools**</span><span class="sxs-lookup"><span data-stu-id="48ac5-316">Clear buttons in the  **Network** tools</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="48ac5-317">Chromium Problem: [#1067184][CR1067184]</span><span class="sxs-lookup"><span data-stu-id="48ac5-317">Chromium issue: [#1067184][CR1067184]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="48ac5-318">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="48ac5-318">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="48ac5-319">Wenn Sie sich auf Windows oder macOS befinden, sollten Sie die Microsoft Edge Vorschaukanäle [als][MicrosoftEdgePreviewChannels] Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="48ac5-319">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="48ac5-320">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="48ac5-320">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="48ac5-321">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="48ac5-321">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Veralteter Eigenschaftenbereich im Elementbereich – Neues in DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Features zum Debuggen von CSS-Rastern – Neues in DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsConsoleApiTable]: ../../../console/api.md#table "Tabelle – Konsolen-API-| Microsoft Docs"  
[DevtoolsCoverageIndex]: ../../../coverage/index.md "Suchen Sie nicht verwendeten JavaScript- und CSS-Code auf der Registerkarte Abdeckung in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]: ../../../css/grid.md "Inspect CSS Grid in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../../../customize/index.md#drawer "Drawer – Anpassen Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../../../device-mode/dual-screen-and-foldables.md "Emulieren von Dualscreen- und faltbaren Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: ../../../evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tool "Analysieren der Renderingleistung mit dem Renderingtool – Leistungsanalysereferenz | Microsoft Docs"  
<!--  [DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features/index.md#enable-experimental-apis "Enable experimental APIs - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: .. /.. /.. /experimental-features/index.md#emulation-support-dual-screen-mode "Emulation: Support dual screen mode - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#source-order-viewer "Source Order Viewer - Experimental features | Microsoft Docs"
<!--  [DevtoolsExperimentalFeaturesTestOnFoldableDualScreenDevices]: ../../../experimental-features/index.md#test-on-foldable-and-dual-screen-devices "Test on foldable and dual-screen devices - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features "Aktivieren experimenteller Features – Experimentelle Features | Microsoft Docs"  
[DevtoolsMediaPanelIndex]: .. /.. /.. /media-panel/index.md "Anzeigen und Debuggen von Media Player-| Microsoft Docs"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Arbeiten mit der Naht – Einführung in Geräten mit dualem Bildschirm | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Feature „CSS-Medienbildschirmaufteilung“ für die Erkennung von dualem Bildschirm | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "Die API „getWindowSegments JavaScript“ für Geräte mit dualem Bildschirm | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Code Tastenkombinationen für Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Das neue Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools, Twitter-Konto"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  

[CR174309]: https://crbug.com/174309 "DevTools: Ermöglicht das Anpassen von Tastenkombinationen/Tastenkombinationen | Chromium Fehler"
[CR384968]: https://crbug.com/384968 "Option zum Ignorieren von lokalen()Schriftarten | Chromium Fehler"  
[CR772558]: https://crbug.com/772558 "DevTools: Aktualisieren auf die neueste Version von &quot;| Chromium Fehler"  
[CR807440]: https://crbug.com/807440 "Chrome wird mit einer großen Anzahl von SWs | Chromium Fehler"  
[CR997694]: https://crbug.com/997694 "XHR-Anforderungen mit dem Status 302 werden im Netzwerkbereich nicht unter dem Filter \"xhr\" | Chromium Fehler"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Chromium Fehler"  
[CR1051466]: https://crbug.com/1051466 "Unterstützung des COOP/COEP-Debuggings in DevTools | Chromium Fehler"  
[CR1054281]: https://crbug.com/1054281 "Featureanforderung: DevTools sollte zusammenklappbare und duale Bildschirmgeräte emulieren, die | Chromium Fehler"  
[CR1067184]: https://crbug.com/1067184 "Featureanforderung: Filterschaltfläche löschen im Netzwerk & Elemente -> Formatfiltereingaben | Chromium Fehler"  
[CR1068116]: https://crbug.com/1068116 "☂ Problembereich | Chromium Fehler"  
[CR1080569]: https://crbug.com/1080569 "acorn unterstützt keine logischen Zuweisungsoperatoren | Chromium Fehler"  
[CR1080589]: https://crbug.com/1080589 "Klassifizieren von Problemen nach Drittanbieter-/erst-| Chromium Fehler"  
[CR1086817]: https://crbug.com/1086817 "acorn unterstützt keine numerischen Trennzeichen | Chromium Fehler"  
[CR1090802]: https://crbug.com/1090802 "Simulieren von Änderungen des Leerlaufzustands aus der Leerlauferkennungs-API | Chromium Fehler"  
[CR1093227]: https://crbug.com/1093227 "DevTools: Schlagen Sie die am nächsten barrierefreien | Chromium Fehler"  
[CR1093247]: https://crbug.com/1093247 "Anzeigen von Informationen zu Frames im Anwendungsbereich | Chromium Fehler"  
[CR1094406]: https://crbug.com/1094406 "Entwickler möchten eine Quellauftragsanzeige für AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: Unterstützt die Emulierung der Features &quot;prefers-reduced-data media&quot; | Chromium Fehler"  
[CR1096481]: https://crbug.com/1096481 "Probleme bei der Bannerplatzierung | Chromium Fehler"  
[CR1100253]: https://crbug.com/1100253 "Hinzufügen einer Verknüpfung mit einem Screenshotknoten im Elementkontextmenü | Chromium Fehler"  
[CR1103316]: https://crbug.com/1103316 "Elementesuche wird nicht aufgelöstNode (Hervorhebungstext usw.) im ersten Suchergebnis | Chromium Fehler"  
[CR1103854]: https://crbug.com/1103854 "Entverschleieren von X-Client-Data-Werten in Entwicklertools | Chromium Fehler"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: "Hinzufügen importierter Schriftarten zur automatischen Schriftfamilienvervollständigung https://crbug.com/1106221 im Formatvorlagenbereich | Chromium Fehler"  
[CR1107766]: "Anzeigen von Informationen zu Frames, die von https://crbug.com/1107766 'window.open()' in der Framestruktur generiert | Chromium Fehler"  
[CR1115011]: "Beim Kopieren einer Tabelle aus der Konsole wird die Struktur der Tabelle nicht | https://crbug.com/1115011 Chromium Fehler"  
[CR1116085]: "Rufen Sie den https://crbug.com/1116085 Inspektor für DevTools-Eigenschaften | Chromium Fehler"  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "prefers-reduced-data – Media Queries Level 5 | W3C CSS Working Group Editor Drafts"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v6.2.0 – GoogleChrome/| GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Protokollpuffer | Google Developers"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Logische Zuweisung | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Numerische Trennzeichen | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "So wird Ihre Website mithilfe von COOP und COEP isoliert\"Cross-Origin\" | web.dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Erkennen von inaktiven Benutzern mit dem Leerlauferkennungs-API-| web.dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Vermeiden sie nicht zusammengesetzte Animationen | web.dev"  

> [!NOTE]
> <span data-ttu-id="48ac5-380">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48ac5-380">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="48ac5-381">Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-86) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="48ac5-381">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-86) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="48ac5-383">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="48ac5-383">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  

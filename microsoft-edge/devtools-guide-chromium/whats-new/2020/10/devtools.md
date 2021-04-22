---
description: Neue CSS Grid-Debuggingtools, Webauthn-Tool, verschiebbare Tools und berechnete Seitenleisten.
title: Neues in DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 0f4e0aaeba55f584697d1817f7ea54044dfdd380
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514354"
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
# <a name="whats-new-in-devtools-microsoft-edge-87"></a><span data-ttu-id="3b520-104">Neues in DevTools (Microsoft Edge 87)</span><span class="sxs-lookup"><span data-stu-id="3b520-104">What's New In DevTools (Microsoft Edge 87)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="improving-devtools-localization"></a><span data-ttu-id="3b520-105">Verbessern der DevTools-Lokalisierung</span><span class="sxs-lookup"><span data-stu-id="3b520-105">Improving DevTools localization</span></span>  

<span data-ttu-id="3b520-106">Um Ihre Übersetzungsanforderungen zu erfüllen, konzentriert sich das Microsoft Edge DevTools-Team auf die Verbesserung der Übersetzungsqualität.</span><span class="sxs-lookup"><span data-stu-id="3b520-106">To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.</span></span>  <span data-ttu-id="3b520-107">Ab Microsoft Edge, Version 87, sind mehrere Zeichenfolgen und Begriffe gesperrt und ändern sich nicht, auch wenn die restlichen DevTools in anderen Sprachen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3b520-107">Starting in Microsoft Edge version 87, several strings and terms are locked and do not change even when the rest of the DevTools are displayed in other languages.</span></span>  <span data-ttu-id="3b520-108">Die Liste der betroffenen Zeichenfolgen und Begriffe umfasst Folgendes.</span><span class="sxs-lookup"><span data-stu-id="3b520-108">The list of affected strings and terms include the following.</span></span>  

*   <span data-ttu-id="3b520-109">Die Zeichenfolgen im **Tool "Leuchttürme".**</span><span class="sxs-lookup"><span data-stu-id="3b520-109">The strings in the **Lighthouse** tool.</span></span>  
*   <span data-ttu-id="3b520-110">Der Begriff `service worker` .</span><span class="sxs-lookup"><span data-stu-id="3b520-110">The term `service worker`.</span></span>  
*   <span data-ttu-id="3b520-111">Einige der **Netzwerktoolfilter** wie `URL` , , und `XHR` `JS` `CSS` .</span><span class="sxs-lookup"><span data-stu-id="3b520-111">Some of the **Network** tool filters such as `URL`, `XHR`, `JS`, and `CSS`.</span></span>  
*   <span data-ttu-id="3b520-112">Die [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] Console Utilities-API.</span><span class="sxs-lookup"><span data-stu-id="3b520-112">The [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] Console Utilities API.</span></span>  
    
<span data-ttu-id="3b520-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] ist jetzt in der [Konsole](/microsoft-edge/devtools-guide-chromium/console/index.md) für Benutzer in lokalisierten Versionen der DevTools verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3b520-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] is now available in the [Console](/microsoft-edge/devtools-guide-chromium/console/index.md) for users on localized versions of the DevTools.</span></span>   <span data-ttu-id="3b520-114">Vielen Dank an die globale Entwickler-Community, dass Sie die Lokalisierung von Microsoft Edge DevTools verbessert haben.</span><span class="sxs-lookup"><span data-stu-id="3b520-114">Thank you to the global developer community for helping improve localization of the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="3b520-115">Senden Sie [weiterhin Feedback zur Lokalisierungsqualität,](#getting-in-touch-with-microsoft-edge-devtools-team) um die Unterstützung für DevTools in allen Locales zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="3b520-115">Continue to [send feedback on localization quality](#getting-in-touch-with-microsoft-edge-devtools-team) to improve support for DevTools in all locales.</span></span>  <span data-ttu-id="3b520-116">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="3b520-116">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Netzwerktool mit nicht lokalisierten Filtern" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   <span data-ttu-id="3b520-118">**Netzwerkbereich** mit nicht lokalisierten Filtern</span><span class="sxs-lookup"><span data-stu-id="3b520-118">**Network** pane with non-localized filters</span></span>  
:::image-end:::  

## <a name="move-tools-between-top-and-bottom-panels"></a><span data-ttu-id="3b520-119">Verschieben von Tools zwischen oberen und unteren Panels</span><span class="sxs-lookup"><span data-stu-id="3b520-119">Move tools between top and bottom panels</span></span>  

<span data-ttu-id="3b520-120">DevTools unterstützt jetzt das Verschieben von Tools zwischen dem oberen und unteren Bereich.</span><span class="sxs-lookup"><span data-stu-id="3b520-120">DevTools now supports moving tools between the top and bottom panels.</span></span>  <span data-ttu-id="3b520-121">Passen Sie Ihre DevTools an, und verbessern Sie Ihre Produktivität, indem Sie eine beliebige Kombination von zwei Tools gleichzeitig anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3b520-121">Customize your DevTools and improve your productivity by viewing any combination of two tools at the same time.</span></span>  <span data-ttu-id="3b520-122">Zeigen Sie z. B. die **Elemente** und die **Sources-Tools** gleichzeitig an \(durch Verschieben des **Tools Sources** nach unten\).</span><span class="sxs-lookup"><span data-stu-id="3b520-122">For example, view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span></span>  <span data-ttu-id="3b520-123">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [#1075732][CR1075732].</span><span class="sxs-lookup"><span data-stu-id="3b520-123">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1075732][CR1075732].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="3b520-124">Um ein beliebiges oberstes Tool nach unten zu verschieben, zeigen Sie auf eine Registerkarte, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Nach unten verschieben aus.**</span><span class="sxs-lookup"><span data-stu-id="3b520-124">To move any top tool to the bottom, hover on a tab, open the contextual menu \(right-click\), and choose **Move to bottom**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Nach unten verschieben" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         <span data-ttu-id="3b520-126">Nach unten verschieben</span><span class="sxs-lookup"><span data-stu-id="3b520-126">Move to bottom</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="3b520-127">Um ein beliebiges unteres Tool nach oben zu verschieben, zeigen Sie auf eine Registerkarte, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Nach oben verschieben aus.**</span><span class="sxs-lookup"><span data-stu-id="3b520-127">To move any bottom tool to the top, hover on a tab, open the contextual menu \(right-click\), and choose **Move to top**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Nach oben verschieben" lightbox="../../media/2020/10/move-to-top.msft.png":::
         <span data-ttu-id="3b520-129">Nach oben verschieben</span><span class="sxs-lookup"><span data-stu-id="3b520-129">Move to top</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <a name="save-and-export-using-the-network-console"></a><span data-ttu-id="3b520-130">Speichern und Exportieren mithilfe der Netzwerkkonsole</span><span class="sxs-lookup"><span data-stu-id="3b520-130">Save and export using the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="3b520-132">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="3b520-132">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3b520-133">Das **Tool für die** Netzwerkkonsole hat nun die Kompatibilität mit den [Schemas Postman v2.1][PostmanSchemaJsonCollectionv210Index] und [OpenAPI v2][SwaggerSpecificationV2] verbessert.</span><span class="sxs-lookup"><span data-stu-id="3b520-133">The **Network Console** tool now has improved compatibility with the [Postman v2.1][PostmanSchemaJsonCollectionv210Index] and [OpenAPI v2][SwaggerSpecificationV2] schemas.</span></span>  <span data-ttu-id="3b520-134">Navigieren Sie zum Aktivieren des Experiments zu Aktivieren von [Experimentellen Features,][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **Netzwerkkonsole aktivieren.**</span><span class="sxs-lookup"><span data-stu-id="3b520-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span></span>  <span data-ttu-id="3b520-135">Weitere Informationen zur Netzwerkkonsole **finden**Sie unter [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span><span class="sxs-lookup"><span data-stu-id="3b520-135">For more information about the **Network Console**, navigate to [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span></span>  <span data-ttu-id="3b520-136">Dieses Experiment unterstützt nun die folgenden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="3b520-136">This experiment now supports the following actions.</span></span>  

*   <span data-ttu-id="3b520-137">Speichern und exportieren Sie Sammlungen und Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="3b520-137">Save and export Collections and Environments.</span></span>  
*   <span data-ttu-id="3b520-138">Bearbeiten und exportieren Sie Sätze von Umgebungsvariablen im **Netzwerkkonsolentool.**</span><span class="sxs-lookup"><span data-stu-id="3b520-138">Edit and export sets of environment variables within the **Network Console** tool.</span></span>  
    
<span data-ttu-id="3b520-139">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1093687][CR1093687].</span><span class="sxs-lookup"><span data-stu-id="3b520-139">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1093687][CR1093687].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Geben Sie den Namen für die neue Umgebung ein." lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         <span data-ttu-id="3b520-141">Geben Sie den Namen für die neue Umgebung ein.</span><span class="sxs-lookup"><span data-stu-id="3b520-141">Enter name for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Auswählen des Formats für die neue Umgebung" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         <span data-ttu-id="3b520-143">Auswählen des Formats für die neue Umgebung</span><span class="sxs-lookup"><span data-stu-id="3b520-143">Choose format for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-grid-tooling"></a><span data-ttu-id="3b520-144">Verbessertes CSS-Raster-Tool</span><span class="sxs-lookup"><span data-stu-id="3b520-144">Improved CSS Grid tooling</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="3b520-146">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="3b520-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3b520-147">Die Microsoft Edge DevTools unterstützen nun die folgenden Features zum Überprüfen, Anzeigen und Debuggen Ihrer CSS-Raster.</span><span class="sxs-lookup"><span data-stu-id="3b520-147">The Microsoft Edge DevTools now support the following features for inspecting, viewing, and debugging your CSS grids.</span></span>  

*   <span data-ttu-id="3b520-148">Zeigen Sie eine vereinfachte Rasterüberlagerung mit dem **Tool Inspect** an, oder erhalten Sie detailliertere Informationen mit beständigen Überlagerungen.</span><span class="sxs-lookup"><span data-stu-id="3b520-148">Display a simplified grid overlay using the **Inspect** tool, or get more detailed information with persistent overlays.</span></span>  
*   <span data-ttu-id="3b520-149">Wenn Sie dauerhafte Rasterüberlagerungen aktivieren möchten, wählen Sie das Rastersymbol neben einem Rastercontainerelement im **Tool Elemente** aus, oder wählen Sie das Raster im **Layouttool** aus.</span><span class="sxs-lookup"><span data-stu-id="3b520-149">To enable persistent grid overlays, choose the grid icon next to a grid container element in the **Elements** tool or choose the grid in the **Layout** tool.</span></span>  
*   <span data-ttu-id="3b520-150">Sie können dauerhafte Überlagerungen für mehrere Raster aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3b520-150">You may enable persistent overlays for multiple grids.</span></span>  
*   <span data-ttu-id="3b520-151">Mit dem **neuen Layout-Tool** können Sie Gitternetzüberlagerungen einfach umschalten und die Darstellung und den Inhalt für die einzelnen Einstellungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3b520-151">The new **Layout** tool allows you to easily toggle grid overlays and configure the appearance and the content for each.</span></span>  
    
<span data-ttu-id="3b520-152">Die Features sind standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3b520-152">The features are turned on by default.</span></span>  <span data-ttu-id="3b520-153">Weitere Informationen zu den Features finden Sie unter [CSS-Raster][DevtoolsCssGrid].</span><span class="sxs-lookup"><span data-stu-id="3b520-153">For more information about the features, navigate to [CSS grids][DevtoolsCssGrid].</span></span>  <span data-ttu-id="3b520-154">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1047356][CR1047356].</span><span class="sxs-lookup"><span data-stu-id="3b520-154">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1047356][CR1047356].</span></span>  <span data-ttu-id="3b520-155">Darüber hinaus arbeitet das Microsoft Edge DevTools-Team mit dem Chrome DevTools-Team und der Chromium-Community zusammen, um DevTools neue Features für flexbox-Tools hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3b520-155">Additionally, the Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new flexbox tooling features to DevTools.</span></span>  <span data-ttu-id="3b520-156">Informationen zu Updates für flexbox-Tools im Open-Source-Projekt Chromium finden Sie unter Issue [#1136394][CR1136394].</span><span class="sxs-lookup"><span data-stu-id="3b520-156">For updates on flexbox tooling in the Chromium open-source project, navigate to Issue [#1136394][CR1136394].</span></span>  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Layouttool mit Rastern" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   <span data-ttu-id="3b520-158">**Layouttool** mit Rastern</span><span class="sxs-lookup"><span data-stu-id="3b520-158">**Layout** tool with grids</span></span>  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a><span data-ttu-id="3b520-159">Anpassen von Tastaturkürzeln in den Einstellungen</span><span class="sxs-lookup"><span data-stu-id="3b520-159">Customize keyboard shortcuts in Settings</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="3b520-161">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="3b520-161">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3b520-162">Sie können nun die Tastenkombination für alle Aktionen in devTools anpassen.</span><span class="sxs-lookup"><span data-stu-id="3b520-162">You are now able to customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="3b520-163">Seit Microsoft Edge, Version 84, können Sie zwischen Visual Studio **Code** und **DevTools (Standard)-Voreinstellungen** für Tastenkombinationen [wählen.][DevtoolsCustomizeShortcuts]</span><span class="sxs-lookup"><span data-stu-id="3b520-163">Since Microsoft Edge version 84, you are able to choose between **Visual Studio Code** and **DevTools (default)** presets for [keyboard shortcuts][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="3b520-164">Ab Microsoft Edge, Version 87, \*\*\*\* können Sie das Experiment Tastenkombinationen-Editor aktivieren, um Tastenkombinationen [weiter anzupassen.][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]</span><span class="sxs-lookup"><span data-stu-id="3b520-164">Starting in Microsoft Edge version 87, you may turn on the **Enable keyboard shortcut editor** experiment to further [customize keyboard shortcuts][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="3b520-165">Navigieren Sie zum Aktivieren des Experiments zu Experimentelle Features [aktivieren,][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **Tastenkombinationen-Editor aktivieren.**</span><span class="sxs-lookup"><span data-stu-id="3b520-165">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="3b520-166">Weitere Informationen zum Anpassen und Bearbeiten von Tastenkombinationen finden Sie unter [Experimentelles Feature „Tastenkombinations-Editor aktivieren“][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="3b520-166">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  <span data-ttu-id="3b520-167">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="3b520-167">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Benutzerdefinierte Verknüpfung zum Anhalten eines Skripts" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   <span data-ttu-id="3b520-169">Benutzerdefinierte Verknüpfung zum Anhalten eines Skripts</span><span class="sxs-lookup"><span data-stu-id="3b520-169">Custom shortcut for pausing a script</span></span>  
:::image-end:::  

## <a name="introducing-the-microsoft-edge-tools-for-visual-studio-code-extension"></a><span data-ttu-id="3b520-170">Einführung in die Microsoft Edge Tools for Visual Studio Code extension</span><span class="sxs-lookup"><span data-stu-id="3b520-170">Introducing the Microsoft Edge Tools for Visual Studio Code extension</span></span>  

<span data-ttu-id="3b520-171">Die **Elemente für Visual Studio Code** und Netzwerk für Visual Studio **Codeerweiterungen** werden nun mit den neuen Microsoft Edge Developer Tools for Visual Studio [Code-Erweiterung][VisualStudioCodeMarketplaceMsEdgedevtools] zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="3b520-171">The **Elements for Visual Studio Code** and **Network for Visual Studio Code** extensions are now merged into the new [Microsoft Edge Developer Tools for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extension.</span></span>  <span data-ttu-id="3b520-172">Verwenden Sie die Microsoft Edge DevTools für die folgenden Aktivitäten, ohne Microsoft Visual Studio verlassen.</span><span class="sxs-lookup"><span data-stu-id="3b520-172">Use the Microsoft Edge DevTools for the following activities without leaving Microsoft Visual Studio Code.</span></span>  

*   <span data-ttu-id="3b520-173">Debuggen des DOM</span><span class="sxs-lookup"><span data-stu-id="3b520-173">Debug the DOM</span></span>  
*   <span data-ttu-id="3b520-174">Bearbeiten von CSS</span><span class="sxs-lookup"><span data-stu-id="3b520-174">Edit CSS</span></span>  
*   <span data-ttu-id="3b520-175">Überprüfen des Netzwerkdatenverkehrs</span><span class="sxs-lookup"><span data-stu-id="3b520-175">Inspect network traffic</span></span>  

<span data-ttu-id="3b520-176">Starten Sie mit der Erweiterung Microsoft Edge, stellen Sie eine Verbindung mit einer vorhandenen Instanz des Browsers oder verwenden Sie einen kopflosen Browser direkt von Ihrem Editor aus.</span><span class="sxs-lookup"><span data-stu-id="3b520-176">With the extension, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span></span>  <span data-ttu-id="3b520-177">Navigieren Sie zum Microsoft Edge Developer Tools for [Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repository auf GitHub, um Mitwirken und Ablegen von Problemen mit Ihrem Feedback zu dieser Erweiterung zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="3b520-177">To start contributing and filing issues with your feedback about this extension, navigate to the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Screenshot mit der Erweiterung im vollständigen Browsermodus" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         <span data-ttu-id="3b520-179">Screenshot mit der Erweiterung im vollständigen Browsermodus</span><span class="sxs-lookup"><span data-stu-id="3b520-179">Using the extension in full browser mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Verwenden der Erweiterung im Kopflosenmodus screenshot" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         <span data-ttu-id="3b520-181">Verwenden der Erweiterung im Kopflosenmodus screenshot</span><span class="sxs-lookup"><span data-stu-id="3b520-181">Using the extension in headless mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="3b520-182">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="3b520-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-webauthn-tool"></a><span data-ttu-id="3b520-183">Neues WebAuthn-Tool</span><span class="sxs-lookup"><span data-stu-id="3b520-183">New WebAuthn tool</span></span>  

<span data-ttu-id="3b520-184">In früheren Versionen von Microsoft Edge gab es keine systemeigene WebAuthn-Debuggingunterstützung.</span><span class="sxs-lookup"><span data-stu-id="3b520-184">In earlier versions of Microsoft Edge, there was no native WebAuthn debugging support.</span></span>  <span data-ttu-id="3b520-185">Sie benötigten physische Authentisierungsgeräte, um Ihre Webanwendung mit der [Webauthentifizierungs-API zu testen.][GithubW3cWebauthn]</span><span class="sxs-lookup"><span data-stu-id="3b520-185">You needed physical authenticators to test your web application with the [Web Authentication API][GithubW3cWebauthn].</span></span>  <span data-ttu-id="3b520-186">Mit dem neuen **WebAuthn-Tool** können Sie die folgenden Aktionen ausführen, ohne physische Authentisierungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3b520-186">With the new **WebAuthn** tool, you are able to do the following actions without the use of any physical authenticators.</span></span>

*   <span data-ttu-id="3b520-187">Emulieren von Authentatoren</span><span class="sxs-lookup"><span data-stu-id="3b520-187">Emulate authenticators</span></span>
*   <span data-ttu-id="3b520-188">Anpassen von Attributen von Authentatoren</span><span class="sxs-lookup"><span data-stu-id="3b520-188">Customize attributes of authenticators</span></span>
*   <span data-ttu-id="3b520-189">Überprüfen der Zustände von Authentatoren</span><span class="sxs-lookup"><span data-stu-id="3b520-189">Inspect states of authenticators</span></span>
    
<span data-ttu-id="3b520-190">Weitere Informationen zum **WebAuthn-Feature** finden Sie unter Emulieren von Authentatoren und Debuggen [von WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="3b520-190">For more information about the **WebAuthn** feature, navigate to [Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span></span>  

<span data-ttu-id="3b520-191">Sie können Authentatoren emulieren und die [Webauthentifizierungs-API][GithubW3cWebauthn] mit dem neuen [WebAuthn-Tool][DevtoolsWebauthnIndex] debuggen.</span><span class="sxs-lookup"><span data-stu-id="3b520-191">You are able to emulate authenticators and debug the [Web Authentication API][GithubW3cWebauthn] with the new [WebAuthn][DevtoolsWebauthnIndex] tool.</span></span>  <span data-ttu-id="3b520-192">Wählen Sie zum Öffnen des **WebAuthn-Tools** das Symbol **DevTools** anpassen \( \) > `...` Weitere **Tools**  >  **WebAuthn aus.**</span><span class="sxs-lookup"><span data-stu-id="3b520-192">To open the **WebAuthn** tool, choose **the Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  <span data-ttu-id="3b520-193">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1034663][CR1034663].</span><span class="sxs-lookup"><span data-stu-id="3b520-193">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1034663][CR1034663].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Öffnen des WebAuthn-Tools" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         <span data-ttu-id="3b520-195">Öffnen des **WebAuthn-Tools**</span><span class="sxs-lookup"><span data-stu-id="3b520-195">Open the **WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="WebAuthn-Tool" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         <span data-ttu-id="3b520-197">**WebAuthn-Tool**</span><span class="sxs-lookup"><span data-stu-id="3b520-197">**WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="elements-tool-updates"></a><span data-ttu-id="3b520-198">Aktualisierungen des Tools „Elemente“</span><span class="sxs-lookup"><span data-stu-id="3b520-198">Elements tool updates</span></span>  

#### <a name="view-the-computed-sidebar-pane-in-the-styles-pane"></a><span data-ttu-id="3b520-199">Anzeigen des Seitenleistenbereichs "Berechnet" im Bereich Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="3b520-199">View the Computed sidebar pane in the Styles pane</span></span>  

<span data-ttu-id="3b520-200">Schaltet den **Bereich Berechnet** im Bereich **Formatvorlagen** um.</span><span class="sxs-lookup"><span data-stu-id="3b520-200">Toggle the **Computed** pane in the **Styles** pane.</span></span>  <span data-ttu-id="3b520-201">Der **Bereich Berechnet** im Bereich **Formatvorlagen** ist standardmäßig reduziert.</span><span class="sxs-lookup"><span data-stu-id="3b520-201">The **Computed** pane in the **Styles** pane is collapsed by default.</span></span>  <span data-ttu-id="3b520-202">Um ihn umschalten zu können, wählen Sie die Schaltfläche aus.</span><span class="sxs-lookup"><span data-stu-id="3b520-202">To toggle it, choose the button.</span></span>  <span data-ttu-id="3b520-203">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1073899][CR1073899].</span><span class="sxs-lookup"><span data-stu-id="3b520-203">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1073899][CR1073899].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Öffnen des Seitenleistenbereichs "Berechnet"" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         <span data-ttu-id="3b520-205">Öffnen des **Seitenleistenbereichs "Berechnet"**</span><span class="sxs-lookup"><span data-stu-id="3b520-205">Open the **Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Berechneter Seitenleistenbereich" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         <span data-ttu-id="3b520-207">**Berechneter Seitenleistenbereich**</span><span class="sxs-lookup"><span data-stu-id="3b520-207">**Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="grouping-css-properties-in-the-computed-panel"></a><span data-ttu-id="3b520-208">Gruppieren von CSS-Eigenschaften im Berechneten Bereich</span><span class="sxs-lookup"><span data-stu-id="3b520-208">Grouping CSS properties in the Computed panel</span></span>  

<span data-ttu-id="3b520-209">Um die angewendete CSS mit weniger Bildlauf anzuzeigen, gruppieren Sie die CSS-Eigenschaften nach Kategorien im **Bereich Berechnet.**</span><span class="sxs-lookup"><span data-stu-id="3b520-209">To view your applied CSS with less scrolling, group the CSS properties by categories in the **Computed** pane.</span></span>  <span data-ttu-id="3b520-210">Sie können sich auch selektiv auf eine Reihe verwandter Eigenschaften konzentrieren, während Sie Ihre CSS überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3b520-210">You may also selectively focus on a set of related properties while you inspect your CSS.</span></span>  <span data-ttu-id="3b520-211">Wählen Sie **im Elementtool** ein Element aus.</span><span class="sxs-lookup"><span data-stu-id="3b520-211">From the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="3b520-212">Um die CSS-Eigenschaften \(oder ungroup\) zu gruppieren, aktivieren Sie das **Kontrollkästchen Gruppe.**</span><span class="sxs-lookup"><span data-stu-id="3b520-212">To group \(or ungroup\) the CSS properties, toggle the **Group** checkbox.</span></span>  <span data-ttu-id="3b520-213">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [#1096230][CR1096230], [#1084673][CR1084673]und [#1106251][CR1106251].</span><span class="sxs-lookup"><span data-stu-id="3b520-213">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1096230][CR1096230], [#1084673][CR1084673], and [#1106251][CR1106251].</span></span>  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Gruppieren von CSS-Eigenschaften" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   <span data-ttu-id="3b520-215">Gruppieren von CSS-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3b520-215">Grouping CSS properties</span></span>  
:::image-end:::  

### <a name="lighthouse-64-in-the-lighthouse-tool"></a><span data-ttu-id="3b520-216">Leuchttürme 6.4 im Tool "Leuchttürme"</span><span class="sxs-lookup"><span data-stu-id="3b520-216">Lighthouse 6.4 in the Lighthouse tool</span></span>  

<span data-ttu-id="3b520-217">Das **Tool "Leuchtturm"** wird jetzt mit "6.4" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b520-217">The **Lighthouse** tool is now running Lighthouse 6.4.</span></span>  <span data-ttu-id="3b520-218">Eine vollständige Liste der Änderungen finden Sie in den [Anmerkungen zur Veröffentlichung von "Leuchttürme".][GithubGoogleChromeLighthouseReleasesV641]</span><span class="sxs-lookup"><span data-stu-id="3b520-218">For a full list of changes, navigate to the [Lighthouse release notes][GithubGoogleChromeLighthouseReleasesV641].</span></span>  <span data-ttu-id="3b520-219">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#772558][CR772558].</span><span class="sxs-lookup"><span data-stu-id="3b520-219">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#772558][CR772558].</span></span>  

### <a name="performancemark-events-in-the-timings-section"></a><span data-ttu-id="3b520-220">performance.mark()-Ereignisse im Abschnitt Timings</span><span class="sxs-lookup"><span data-stu-id="3b520-220">performance.mark() events in the Timings section</span></span>  

<span data-ttu-id="3b520-221">Der **Abschnitt Timings einer** Aufzeichnung im Tool ["Leistung"][DevtoolsGuideChromiumEvaluatePerformanceReference] markiert nun `performance.mark()` Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="3b520-221">The **Timings section** of a recording in the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool now marks `performance.mark()` events.</span></span>  <span data-ttu-id="3b520-222">Um dieses Feature auszuprobieren und die Leistung Ihres JavaScript-Codes zu messen, fügen Sie `performance.mark()` Dem Code Ereignisse hinzu.</span><span class="sxs-lookup"><span data-stu-id="3b520-222">To try this feature and measure the performance of your JavaScript code, add `performance.mark()` events to your code.</span></span>  <span data-ttu-id="3b520-223">Der folgende Codeausschnitt fügt z. B. Markierungen vor und nach einer Schleife hinzu, die mithilfe von Schritten von 7 von 0 auf `for` 1000 iteriert wird.</span><span class="sxs-lookup"><span data-stu-id="3b520-223">For example, the following code snippet adds markers before and after a `for` loop that iterates from 0 to 1000 using increments of 7.</span></span>  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

<span data-ttu-id="3b520-224">Öffnen Sie dann das [Tool Leistung,][DevtoolsGuideChromiumEvaluatePerformanceReference] und navigieren Sie zum **Abschnitt Timings,** um Ihren JavaScript-Code zu aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="3b520-224">Then, open the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool and navigate to the **Timings section** to record your JavaScript code.</span></span>  <span data-ttu-id="3b520-225">Die `performance.mark()` hinzugefügten Ereignisse werden nun in der Aufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b520-225">The `performance.mark()` events you added are now displayed in the recording.</span></span>  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Performance.mark-Ereignisse" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` <span data-ttu-id="3b520-227">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="3b520-227">events</span></span>  
:::image-end:::  

### <a name="new-resource-type-and-url-filters-in-the-network-tool"></a><span data-ttu-id="3b520-228">Neue Ressourcentyp- und URL-Filter im Netzwerktool</span><span class="sxs-lookup"><span data-stu-id="3b520-228">New resource-type and url filters in the Network tool</span></span>  

<span data-ttu-id="3b520-229">Verwenden Sie das neue `resource-type` und `url` Schlüsselwörter im **Netzwerktool,** um Netzwerkanforderungen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="3b520-229">Use the new `resource-type` and `url` keywords in the **Network** tool to filter network requests.</span></span>  <span data-ttu-id="3b520-230">Verwenden Sie beispielsweise, `resource-type:image` um sich auf die Netzwerkanforderungen zu konzentrieren, die Bilder sind.</span><span class="sxs-lookup"><span data-stu-id="3b520-230">For example, use `resource-type:image` to focus on the network requests that are images.</span></span>  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="Ressourcentypfilter" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   <span data-ttu-id="3b520-232">Ressourcentypfilter</span><span class="sxs-lookup"><span data-stu-id="3b520-232">resource-type filter</span></span>  
:::image-end:::  

<span data-ttu-id="3b520-233">Um speziellere Schlüsselwörter wie und zu `resource-type` `url` ermitteln, navigieren Sie zu [Filtern von Anforderungen nach Eigenschaften][DevtoolsNetworkReferenceFilterRequestsProperties].</span><span class="sxs-lookup"><span data-stu-id="3b520-233">To discover more special keywords such as `resource-type` and `url`, navigate to [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span></span>  <span data-ttu-id="3b520-234">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [#1121141][CR1121141] und [#1104188][CR1104188].</span><span class="sxs-lookup"><span data-stu-id="3b520-234">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1121141][CR1121141] and [#1104188][CR1104188].</span></span>  

### <a name="frame-details-view-updates"></a><span data-ttu-id="3b520-235">Updates der Frame-Detailansicht</span><span class="sxs-lookup"><span data-stu-id="3b520-235">Frame details view updates</span></span>  

#### <a name="display-coep-and-coop-reporting-to-endpoint"></a><span data-ttu-id="3b520-236">Anzeigen der COEP- und COOP-Berichterstellung an den Endpunkt</span><span class="sxs-lookup"><span data-stu-id="3b520-236">Display COEP and COOP reporting to endpoint</span></span>  

<span data-ttu-id="3b520-237">Zeigen Sie die Endpunkte Cross-Origin Embedder Policy \(COEP\) und Cross-Origin Opener Policy \(COOP\) unter dem Abschnitt Sicherheit `reporting to` **& Isolation** an.</span><span class="sxs-lookup"><span data-stu-id="3b520-237">View the Cross-Origin Embedder Policy \(COEP\) and Cross-Origin Opener Policy \(COOP\) `reporting to` endpoint under the **Security & Isolation** section.</span></span>  <span data-ttu-id="3b520-238">Die [Berichts-API][MdnReportingApi] definiert `Report-To` einen neuen HTTP-Header, mit dem Sie die Serverendpunkte für den Browser zum Senden von Warnungen und Fehlern angeben können.</span><span class="sxs-lookup"><span data-stu-id="3b520-238">The [Reporting API][MdnReportingApi] defines `Report-To`, a new HTTP header, that gives you a way to specify the server endpoints for the browser to send warnings and errors.</span></span>  <span data-ttu-id="3b520-239">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="3b520-239">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Die Berichterstellung an den Endpunkt" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   <span data-ttu-id="3b520-241">Der `reporting to` Endpunkt</span><span class="sxs-lookup"><span data-stu-id="3b520-241">The `reporting to` endpoint</span></span>  
:::image-end:::  

#### <a name="display-coep-and-coop-report-only-mode"></a><span data-ttu-id="3b520-242">Anzeigen des NS-Berichtsmodus für COEP und COOP</span><span class="sxs-lookup"><span data-stu-id="3b520-242">Display COEP and COOP report-only mode</span></span>  

<span data-ttu-id="3b520-243">DevTools zeigt jetzt die `report-only` Bezeichnung für COEP und COOP an, die auf den Modus `report-only` festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="3b520-243">DevTools now display the `report-only` label for COEP and COOP that are set to `report-only` mode.</span></span>  <span data-ttu-id="3b520-244">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="3b520-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Bezeichnung für den Nur-Bericht-Modus" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   <span data-ttu-id="3b520-246">Die `report-only` Bezeichnung für den Modus</span><span class="sxs-lookup"><span data-stu-id="3b520-246">The `report-only` mode label</span></span>  
:::image-end:::  

### <a name="view-and-fix-color-contrast-issues-in-the-css-overview-tool"></a><span data-ttu-id="3b520-247">Anzeigen und Beheben von Farbkontrastproblemen im CSS-Übersichtstool</span><span class="sxs-lookup"><span data-stu-id="3b520-247">View and fix color contrast issues in the CSS Overview tool</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="3b520-249">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="3b520-249">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3b520-250">Das **Tool CSS Overview** zeigt nun eine Liste der Elemente auf Ihrer Seite an, die Probleme mit dem Farbkontrast haben.</span><span class="sxs-lookup"><span data-stu-id="3b520-250">The **CSS Overview** tool now displays a list of elements on your page that have color contrast issues.</span></span>  <span data-ttu-id="3b520-251">Die folgende Demoseite enthält ein Beispiel für ein Farbkontrastproblem.</span><span class="sxs-lookup"><span data-stu-id="3b520-251">The following demo page has an example of a color contrast issue.</span></span>  

[<span data-ttu-id="3b520-252">DEMO zu barrierefreien Farben (CSS Overview Accessible Colors)</span><span class="sxs-lookup"><span data-stu-id="3b520-252">CSS Overview Accessible Colors Demo</span></span>][GlitchCssOverviewAccessibleColorsDemo]  

<span data-ttu-id="3b520-253">Aktivieren Sie zum Aktivieren dieses Experiments unter **Einstellungen**Experimente das Kontrollkästchen  >  \*\*\*\* **CSS-Übersicht.**</span><span class="sxs-lookup"><span data-stu-id="3b520-253">To enable this experiment, under **Settings** > **Experiments**, choose the **CSS Overview** checkbox.</span></span>  <span data-ttu-id="3b520-254">Wenn Sie eine Liste der Elemente anzeigen möchten, bei der ein Farbkontrastproblem besteht, wählen Sie unter **Kontrastprobleme** **Text aus.**</span><span class="sxs-lookup"><span data-stu-id="3b520-254">To view a list of elements that have a color contrast issue, on **Contrast issues**, choose **Text**.</span></span>  <span data-ttu-id="3b520-255">Um das Element im **Elementtool zu** öffnen, wählen Sie ein Element in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="3b520-255">To open the element in the **Elements** tool, choose an element in the list.</span></span>  <span data-ttu-id="3b520-256">Zur Behebung von Kontrastproblemen stellen die Microsoft Edge DevTools [automatisch Farbvorschläge zur Verfügung.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]</span><span class="sxs-lookup"><span data-stu-id="3b520-256">To help fix contrast issues, the Microsoft Edge DevTools [automatically provide color suggestions][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span></span>  <span data-ttu-id="3b520-257">Navigieren Sie zum Überprüfen von Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu Problem [#1120316][CR1120316].</span><span class="sxs-lookup"><span data-stu-id="3b520-257">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1120316][CR1120316].</span></span>  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Probleme mit geringem Farbkontrast" lightbox="../../media/2020/10/css-overview.msft.png":::
   <span data-ttu-id="3b520-259">Probleme mit geringem Farbkontrast</span><span class="sxs-lookup"><span data-stu-id="3b520-259">Low color contrast issues</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="3b520-260">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="3b520-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="3b520-261">Wenn Sie unter Windows oder macOS sind, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="3b520-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="3b520-262">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="3b520-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="3b520-263">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="3b520-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Veralteter Eigenschaftenbereich im Elementtool – Neues in DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Features zum Debuggen von CSS-Rastern – Neues in DevTools (Microsoft Edge 85) | Microsoft Docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Barrierefreier Farbvorschlag im Bereich Formatvorlagen – Neues in DevTools (Microsoft Edge 86) | Microsoft Docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Zuletzt ausgewähltes Element oder JavaScript-Objekt – Api-Referenz für Konsolenprogramme | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Leistungsanalysereferenz | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Emulation: Unterstützung des dualen Bildschirmmodus – Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Aktivieren experimenteller APIs – Experimentelle | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Aktivieren des Tastenkombinationen-Editors – Experimentelle | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulation: Unterstützung des dualen Bildschirmmodus – Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Aktivieren der Netzwerkkonsole – Experimentelle | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Aktivieren der Quellauftragsanzeige – Experimentelle | Microsoft Docs"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Testen auf zusammenklappbaren geräten und dualen Bildschirmen – Experimentelle | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Aktivieren von Experimentellen Features – Experimentelle Features | Microsoft Docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "Tabelle – Konsolen-API-| Microsoft Docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Suchen Sie nicht verwendeten JavaScript- und CSS-Code auf der Registerkarte Abdeckung in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Überprüfen der CSS Grid-| Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Drawer – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analysieren der Renderingleistung mit der Registerkarte Rendering – Leistungsanalysereferenz | Microsoft Docs"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Anzeigen und Debuggen von Media Player-| Microsoft Docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Filtern von Anforderungen nach Eigenschaften – Netzwerkanalysereferenz | Microsoft Docs"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Emulieren von Authentifizierungsautoren und Debuggen von WebAuthn in Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  

[CR174309]: https://crbug.com/174309 "DevTools: Ermöglicht das Anpassen von Tastenkombinationen/Tastenkombinationen | Chromium-Fehler"
[CR772558]: https://crbug.com/772558 "DevTools: Aktualisieren auf die neueste Version von &quot;| Chromium-Fehler"  
[CR1034663]: https://crbug.com/1034663 "Erstellen eines Front-Ends für die WebAuthn Testing-API | Chromium-Fehler"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Chromium-Fehler"  
[CR1051466]: https://crbug.com/1051466 "Unterstützung des COOP/COEP-Debuggings in DevTools | Chromium-Fehler"  
[CR1073899]: https://crbug.com/1073899 "Registerkarte &quot;Berechnete Formatvorlage&quot; wird im reaktionsschnellen Modus | Chromium-Fehler"  
[CR1075732]: https://crbug.com/1075732 "DevTools-Personalisierung – Wechselregisterkarten | Chromium-Fehler"  
[CR1084673]: https://crbug.com/1084673 "DevTools: Verbessern Sie die Art und Weise, wie wir benutzerdefinierte CSS-Eigenschaften ((auch bekannt) präsentieren. CSS-Variablen) und deren Werte | Chromium-Fehler"  
[CR1093687]: https://crbug.com/1093687 "Erstellen eines Tools zum Erstellen und Wiedergeben synthetischer Netzwerkanforderungen | Chromium-Fehler"  
[CR1096230]: https://crbug.com/1096230 "Gruppieren von CSS-Eigenschaften nach Kategorien im Bereich &quot;Computed Styles&quot; | Chromium-Fehler"  
[CR1104188]: https://crbug.com/1104188 "Bei der Suche nach vollständigen URL-Adressen findet die Netzwerktoolsuche keine | Chromium-Fehler"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: Verbessern der Registerkarten für berechnete Formatvorlagen | Chromium-Fehler"  
[CR1120316]: https://crbug.com/1120316 "Hervorheben eines schlechten Kontrasts unter CSS Overview > Colors | Chromium-Bugs"  
[CR1121141]: https://crbug.com/1121141 "Filtern nach Ressourcentyp in Netzwerkprotokollen | Chromium-Fehler"  
[CR1121312]: https://crbug.com/1121312 "Einstellungen sollten aus dem Menü &quot;Weitere Tools&quot; entfernt | Chromium-Fehler"  
[CR1136394]: https://crbug.com/1136394 "Flexbox-| Chromium-Bugs"  
[CR1136655]: https://crbug.com/1136655 "Devtools: Lokalisierung V2 | Chromium-Fehler"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Berichterstellungs-API-| MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1 – GoogleChrome/| GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Webauthentifizierungs-| GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Hello! | Glitch"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Postman Collection Format v2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "OpenAPI-Spezifikations-| Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> <span data-ttu-id="3b520-316">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b520-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3b520-317">Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-87) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="3b520-317">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-87) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="3b520-319">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3b520-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

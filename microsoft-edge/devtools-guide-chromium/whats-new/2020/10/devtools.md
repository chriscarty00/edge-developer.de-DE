---
description: Neue CSS-Raster Debugging-Tools, webauthn-Tool, verschiebbare Tools und Bereich für berechnete Seitenleiste.
title: Neuerungen in devtools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: b972468ad21f3a64985a00aecbe29836032b3334
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190005"
---
# <span data-ttu-id="e889e-104">Neuerungen in devtools (Microsoft Edge 87)</span><span class="sxs-lookup"><span data-stu-id="e889e-104">What's New In DevTools (Microsoft Edge 87)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="e889e-105">Verbessern der devtools-Lokalisierung</span><span class="sxs-lookup"><span data-stu-id="e889e-105">Improving DevTools localization</span></span>  

<span data-ttu-id="e889e-106">Um Ihre Übersetzungsanforderungen zu erfüllen, konzentriert sich das Microsoft Edge devtools-Team auf die Verbesserung der Übersetzungsqualität.</span><span class="sxs-lookup"><span data-stu-id="e889e-106">To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.</span></span>  <span data-ttu-id="e889e-107">Ab Microsoft Edge, Version 87, sind mehrere Zeichenfolgen und Ausdrücke gesperrt und ändern sich auch dann nicht, wenn die restlichen devtools in anderen Sprachen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e889e-107">Starting in Microsoft Edge version 87, several strings and terms are locked and do not change even when the rest of the DevTools are displayed in other languages.</span></span>  <span data-ttu-id="e889e-108">Die Liste der betroffenen Zeichenfolgen und Begriffe enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e889e-108">The list of affected strings and terms include the following.</span></span>  

*   <span data-ttu-id="e889e-109">Die Zeichenfolgen im **Leuchtturm** -Tool.</span><span class="sxs-lookup"><span data-stu-id="e889e-109">The strings in the **Lighthouse** tool.</span></span>  
*   <span data-ttu-id="e889e-110">Der Ausdruck `service worker` .</span><span class="sxs-lookup"><span data-stu-id="e889e-110">The term `service worker`.</span></span>  
*   <span data-ttu-id="e889e-111">Einige der **Netzwerk** Tool Filter wie `URL` ,,, `XHR` `JS` und `CSS` .</span><span class="sxs-lookup"><span data-stu-id="e889e-111">Some of the **Network** tool filters such as `URL`, `XHR`, `JS`, and `CSS`.</span></span>  
*   <span data-ttu-id="e889e-112">Die API für die [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] -Konsolen Dienstprogramme</span><span class="sxs-lookup"><span data-stu-id="e889e-112">The [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] Console Utilities API.</span></span>  
    
<span data-ttu-id="e889e-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] steht jetzt in der [Konsole](/microsoft-edge/devtools-guide-chromium/console/index.md) für Benutzer mit lokalisierten Versionen von devtools zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e889e-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] is now available in the [Console](/microsoft-edge/devtools-guide-chromium/console/index.md) for users on localized versions of the DevTools.</span></span>   <span data-ttu-id="e889e-114">Vielen Dank an die globale Entwicklercommunity, um die Lokalisierung des Microsoft Edge-devtools zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="e889e-114">Thank you to the global developer community for helping improve localization of the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="e889e-115">Senden Sie weiterhin [Feedback zur Lokalisierungsqualität](#getting-in-touch-with-microsoft-edge-devtools-team) , um die Unterstützung für devtools in allen Gebietsschemas zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="e889e-115">Continue to [send feedback on localization quality](#getting-in-touch-with-microsoft-edge-devtools-team) to improve support for DevTools in all locales.</span></span>  <span data-ttu-id="e889e-116">Navigieren Sie zu Issue [#1136655][CR1136655], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-116">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Netzwerktool mit nicht lokalisierten Filtern" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   <span data-ttu-id="e889e-118">**Netzwerk** Bereich mit nicht lokalisierten Filtern</span><span class="sxs-lookup"><span data-stu-id="e889e-118">**Network** pane with non-localized filters</span></span>  
:::image-end:::  

## <span data-ttu-id="e889e-119">Verschieben von Tools zwischen dem oberen und unteren Bereich</span><span class="sxs-lookup"><span data-stu-id="e889e-119">Move tools between top and bottom panels</span></span>  

<span data-ttu-id="e889e-120">DevTools unterstützt jetzt das Verschieben von Tools zwischen dem oberen und unteren Bereich.</span><span class="sxs-lookup"><span data-stu-id="e889e-120">DevTools now supports moving tools between the top and bottom panels.</span></span>  <span data-ttu-id="e889e-121">Passen Sie Ihre devtools an, und verbessern Sie Ihre Produktivität, indem Sie eine beliebige Kombination aus zwei Tools gleichzeitig anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e889e-121">Customize your DevTools and improve your productivity by viewing any combination of two tools at the same time.</span></span>  <span data-ttu-id="e889e-122">So können Sie beispielsweise die **Elemente** und die **Quellen** Tools gleichzeitig anzeigen, indem Sie das **Quellen** Tool nach unten verschieben.</span><span class="sxs-lookup"><span data-stu-id="e889e-122">For example, view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span></span>  <span data-ttu-id="e889e-123">Navigieren Sie zu Issue [#1075732][CR1075732], um den Verlauf dieses Features im Open-Source-Projekt Chrom zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-123">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1075732][CR1075732].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e889e-124">Wenn Sie ein oberes Tool nach unten verschieben möchten, zeigen Sie auf eine Registerkarte, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **nach unten verschieben**aus.</span><span class="sxs-lookup"><span data-stu-id="e889e-124">To move any top tool to the bottom, hover on a tab, open the contextual menu \(right-click\), and choose **Move to bottom**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Nach unten verschieben" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         <span data-ttu-id="e889e-126">Nach unten verschieben</span><span class="sxs-lookup"><span data-stu-id="e889e-126">Move to bottom</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="e889e-127">Wenn Sie ein beliebiges Bottom-Tool nach oben verschieben möchten, zeigen Sie auf eine Registerkarte, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **nach oben verschieben**aus.</span><span class="sxs-lookup"><span data-stu-id="e889e-127">To move any bottom tool to the top, hover on a tab, open the contextual menu \(right-click\), and choose **Move to top**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Zum Anfang wechseln" lightbox="../../media/2020/10/move-to-top.msft.png":::
         <span data-ttu-id="e889e-129">Zum Anfang wechseln</span><span class="sxs-lookup"><span data-stu-id="e889e-129">Move to top</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="e889e-130">Speichern und Exportieren mithilfe der Netzwerk Konsole</span><span class="sxs-lookup"><span data-stu-id="e889e-130">Save and export using the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   <span data-ttu-id="e889e-132">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="e889e-132">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="e889e-133">Das **Netzwerkkonsolen** Tool bietet nun eine verbesserte Kompatibilität mit den Schemas " [Postman v 2.1][PostmanSchemaJsonCollectionv210Index] " und " [OpenAPI v2][SwaggerSpecificationV2] ".</span><span class="sxs-lookup"><span data-stu-id="e889e-133">The **Network Console** tool now has improved compatibility with the [Postman v2.1][PostmanSchemaJsonCollectionv210Index] and [OpenAPI v2][SwaggerSpecificationV2] schemas.</span></span>  <span data-ttu-id="e889e-134">Um das Experiment zu aktivieren, navigieren Sie zu [experimentelle Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] aktivieren, und aktivieren Sie das Kontrollkästchen neben **Netzwerk Konsole aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="e889e-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span></span>  <span data-ttu-id="e889e-135">Weitere Informationen zur **Netzwerk Konsole**finden Sie unter Aktivieren des [experimentellen Netzwerkkonsolen Features][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span><span class="sxs-lookup"><span data-stu-id="e889e-135">For more information about the **Network Console**, navigate to [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span></span>  <span data-ttu-id="e889e-136">Dieses Experiment unterstützt nun die folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="e889e-136">This experiment now supports the following actions.</span></span>  

*   <span data-ttu-id="e889e-137">Speichern und Exportieren von Sammlungen und Umgebungen</span><span class="sxs-lookup"><span data-stu-id="e889e-137">Save and export Collections and Environments.</span></span>  
*   <span data-ttu-id="e889e-138">Bearbeiten und exportieren Sie Gruppen von Umgebungsvariablen innerhalb des **Netzwerkkonsolen** Tools.</span><span class="sxs-lookup"><span data-stu-id="e889e-138">Edit and export sets of environment variables within the **Network Console** tool.</span></span>  
    
<span data-ttu-id="e889e-139">Navigieren Sie zu Issue [#1093687][CR1093687], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-139">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1093687][CR1093687].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Geben Sie den Namen für die neue Umgebung ein." lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         <span data-ttu-id="e889e-141">Geben Sie den Namen für die neue Umgebung ein.</span><span class="sxs-lookup"><span data-stu-id="e889e-141">Enter name for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Format für die neue Umgebung auswählen" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         <span data-ttu-id="e889e-143">Format für die neue Umgebung auswählen</span><span class="sxs-lookup"><span data-stu-id="e889e-143">Choose format for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="e889e-144">Verbesserte CSS-Raster Tools</span><span class="sxs-lookup"><span data-stu-id="e889e-144">Improved CSS Grid tooling</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   <span data-ttu-id="e889e-146">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="e889e-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="e889e-147">Die Microsoft Edge-devtools unterstützen nun die folgenden Features zum Überprüfen, anzeigen und Debuggen von CSS-Rastern.</span><span class="sxs-lookup"><span data-stu-id="e889e-147">The Microsoft Edge DevTools now support the following features for inspecting, viewing, and debugging your CSS grids.</span></span>  

*   <span data-ttu-id="e889e-148">Anzeigen einer vereinfachten Raster Überlagerung mit dem Tool "über **prüfen** " oder Abrufen detaillierter Informationen mit beständigen Overlays.</span><span class="sxs-lookup"><span data-stu-id="e889e-148">Display a simplified grid overlay using the **Inspect** tool, or get more detailed information with persistent overlays.</span></span>  
*   <span data-ttu-id="e889e-149">Wenn Sie persistente Raster Überlagerungen aktivieren möchten, wählen Sie das Rastersymbol neben einem Rastercontainer Element im Tool **Elemente** aus, oder wählen Sie das Raster im Tool **Layout** aus.</span><span class="sxs-lookup"><span data-stu-id="e889e-149">To enable persistent grid overlays, choose the grid icon next to a grid container element in the **Elements** tool or choose the grid in the **Layout** tool.</span></span>  
*   <span data-ttu-id="e889e-150">Sie können persistente Overlays für mehrere Raster aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e889e-150">You may enable persistent overlays for multiple grids.</span></span>  
*   <span data-ttu-id="e889e-151">Mit dem neuen **Layout** -Tool können Sie problemlos Raster Überlagerungen umschalten und die Darstellung und den Inhalt für jeden konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e889e-151">The new **Layout** tool allows you to easily toggle grid overlays and configure the appearance and the content for each.</span></span>  
    
<span data-ttu-id="e889e-152">Die Features sind standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e889e-152">The features are turned on by default.</span></span>  <span data-ttu-id="e889e-153">Wenn Sie weitere Informationen zu den Features erhalten möchten, navigieren Sie zu [CSS-Rastern][DevtoolsCssGrid].</span><span class="sxs-lookup"><span data-stu-id="e889e-153">For more information about the features, navigate to [CSS grids][DevtoolsCssGrid].</span></span>  <span data-ttu-id="e889e-154">Navigieren Sie zu Issue [#1047356][CR1047356], um den Verlauf dieses Features im Open-Source-Projekt Chrom zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-154">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1047356][CR1047356].</span></span>  <span data-ttu-id="e889e-155">Darüber hinaus kooperiert das Microsoft Edge devtools-Team mit der Chrome-devtools-Team-und Chrom-Community, um neue Flexbox-Tool Funktionen zu devtools hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e889e-155">Additionally, the Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new flexbox tooling features to DevTools.</span></span>  <span data-ttu-id="e889e-156">Informationen zu Updates für die Flexbox-Tools im Open-Source-Projekt von Chromium finden Sie unter Issue [#1136394][CR1136394].</span><span class="sxs-lookup"><span data-stu-id="e889e-156">For updates on flexbox tooling in the Chromium open-source project, navigate to Issue [#1136394][CR1136394].</span></span>  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Layout-Tool mit Rastern" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   <span data-ttu-id="e889e-158">**Layout** -Tool mit Rastern</span><span class="sxs-lookup"><span data-stu-id="e889e-158">**Layout** tool with grids</span></span>  
:::image-end:::  

## <span data-ttu-id="e889e-159">Anpassen von Tastenkombinationen in den Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e889e-159">Customize keyboard shortcuts in Settings</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   <span data-ttu-id="e889e-161">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="e889e-161">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="e889e-162">Sie können nun die Tastenkombination für jede Aktion im devtools anpassen.</span><span class="sxs-lookup"><span data-stu-id="e889e-162">You are now able to customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="e889e-163">Seit Microsoft Edge, Version 84, können Sie zwischen **Visual Studio-Code** und **devtools (Standard)** -Voreinstellungen für [Tastenkombinationen][DevtoolsCustomizeShortcuts]auswählen.</span><span class="sxs-lookup"><span data-stu-id="e889e-163">Since Microsoft Edge version 84, you are able to choose between **Visual Studio Code** and **DevTools (default)** presets for [keyboard shortcuts][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="e889e-164">Ab Microsoft Edge, Version 87, können Sie das Experiment zum **Aktivieren des Tasten Kombinations-Editors aktivieren** , um [Tastenkombinationen weiter anzupassen][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="e889e-164">Starting in Microsoft Edge version 87, you may turn on the **Enable keyboard shortcut editor** experiment to further [customize keyboard shortcuts][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="e889e-165">Um das Experiment zu aktivieren, navigieren Sie zu [experimentelle Features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] aktivieren, und aktivieren Sie das Kontrollkästchen neben **Tastenkombinationen-Editor aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="e889e-165">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="e889e-166">Weitere Informationen zum Anpassen und Bearbeiten von Tastenkombinationen finden Sie unter Aktivieren des Features für den [Tasten Kombinations-Editor][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="e889e-166">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  <span data-ttu-id="e889e-167">Navigieren Sie zu Issue [#174309][CR174309], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-167">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Benutzerdefinierte Tastenkombination zum Anhalten eines Skripts" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   <span data-ttu-id="e889e-169">Benutzerdefinierte Tastenkombination zum Anhalten eines Skripts</span><span class="sxs-lookup"><span data-stu-id="e889e-169">Custom shortcut for pausing a script</span></span>  
:::image-end:::  

## <span data-ttu-id="e889e-170">Einführung in die Microsoft Edge-Tools für die Visual Studio-Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="e889e-170">Introducing the Microsoft Edge Tools for Visual Studio Code extension</span></span>  

<span data-ttu-id="e889e-171">Die **Elemente für Visual Studio** -Code und **Netzwerk für Visual Studio-Code** Erweiterungen sind jetzt mit der neuen [Microsoft Edge Developer Tools for Visual Studio-Code][VisualStudioCodeMarketplaceMsEdgedevtools] Erweiterung verbunden.</span><span class="sxs-lookup"><span data-stu-id="e889e-171">The **Elements for Visual Studio Code** and **Network for Visual Studio Code** extensions are now merged into the new [Microsoft Edge Developer Tools for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extension.</span></span>  <span data-ttu-id="e889e-172">Verwenden Sie die Microsoft Edge-devtools für die folgenden Aktivitäten, ohne Visual Studio-Code zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="e889e-172">Use the Microsoft Edge DevTools for the following activities without leaving Visual Studio Code.</span></span>  

*   <span data-ttu-id="e889e-173">Debuggen des DOM</span><span class="sxs-lookup"><span data-stu-id="e889e-173">Debug the DOM</span></span>  
*   <span data-ttu-id="e889e-174">CSS bearbeiten</span><span class="sxs-lookup"><span data-stu-id="e889e-174">Edit CSS</span></span>  
*   <span data-ttu-id="e889e-175">Überprüfen des Netzwerkverkehrs</span><span class="sxs-lookup"><span data-stu-id="e889e-175">Inspect network traffic</span></span>  

<span data-ttu-id="e889e-176">Starten Sie mit der Erweiterung Microsoft Edge, stellen Sie eine Verbindung mit einer vorhandenen Instanz des Browsers her, oder verwenden Sie einen headless-Browser direkt in Ihrem Editor.</span><span class="sxs-lookup"><span data-stu-id="e889e-176">With the extension, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span></span>  <span data-ttu-id="e889e-177">Navigieren Sie zu den [Microsoft Edge-Entwickler Tools für Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] Repo auf GitHub, um mit Ihrem Feedback zu dieser Erweiterung Beiträge zu erstellen und Probleme zu melden.</span><span class="sxs-lookup"><span data-stu-id="e889e-177">To start contributing and filing issues with your feedback about this extension, navigate to the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Verwenden der Erweiterung im vollständigen Browsermodus-Screenshot" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         <span data-ttu-id="e889e-179">Verwenden der Erweiterung im vollständigen Browsermodus-Screenshot</span><span class="sxs-lookup"><span data-stu-id="e889e-179">Using the extension in full browser mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Verwenden der Erweiterung im Headless-Modus-Screenshot" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         <span data-ttu-id="e889e-181">Verwenden der Erweiterung im Headless-Modus-Screenshot</span><span class="sxs-lookup"><span data-stu-id="e889e-181">Using the extension in headless mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="e889e-182">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="e889e-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="e889e-183">Neues webauthn-Tool</span><span class="sxs-lookup"><span data-stu-id="e889e-183">New WebAuthn tool</span></span>  

<span data-ttu-id="e889e-184">In früheren Versionen von Microsoft Edge gab es keine Unterstützung für das Debuggen von webauthen im System.</span><span class="sxs-lookup"><span data-stu-id="e889e-184">In earlier versions of Microsoft Edge, there was no native WebAuthn debugging support.</span></span>  <span data-ttu-id="e889e-185">Sie haben physische Authentifikatoren benötigt, um Ihre Webanwendung mit der [Web-Authentifizierungs-API][GithubW3cWebauthn]zu testen.</span><span class="sxs-lookup"><span data-stu-id="e889e-185">You needed physical authenticators to test your web application with the [Web Authentication API][GithubW3cWebauthn].</span></span>  <span data-ttu-id="e889e-186">Mit dem neuen **webauthn** -Tool können Sie die folgenden Aktionen ausführen, ohne dass physische Authentifikatoren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e889e-186">With the new **WebAuthn** tool, you are able to do the following actions without the use of any physical authenticators.</span></span>

*   <span data-ttu-id="e889e-187">Emulieren von Authentifikatoren</span><span class="sxs-lookup"><span data-stu-id="e889e-187">Emulate authenticators</span></span>
*   <span data-ttu-id="e889e-188">Anpassen von Attributen von Authentifikatoren</span><span class="sxs-lookup"><span data-stu-id="e889e-188">Customize attributes of authenticators</span></span>
*   <span data-ttu-id="e889e-189">Überprüfen von Authentifizierungs Zuständen</span><span class="sxs-lookup"><span data-stu-id="e889e-189">Inspect states of authenticators</span></span>
    
<span data-ttu-id="e889e-190">Weitere Informationen zum **webauthn** -Feature finden Sie unter [emulieren von Authentifikatoren und Debuggen von webauthn in Microsoft Edge devtools][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="e889e-190">For more information about the **WebAuthn** feature, navigate to [Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span></span>  

<span data-ttu-id="e889e-191">Sie können Authentifikatoren emulieren und die [Web-Authentifizierungs-API][GithubW3cWebauthn] mit dem neuen [webauthn][DevtoolsWebauthnIndex] -Tool Debuggen.</span><span class="sxs-lookup"><span data-stu-id="e889e-191">You are able to emulate authenticators and debug the [Web Authentication API][GithubW3cWebauthn] with the new [WebAuthn][DevtoolsWebauthnIndex] tool.</span></span>  <span data-ttu-id="e889e-192">Um das **webauthn** -Tool zu öffnen, wählen Sie **das Symbol anpassen und Steuern devtools** \ ( `...` \) > **Weitere Tools**  >  **webauthn**aus.</span><span class="sxs-lookup"><span data-stu-id="e889e-192">To open the **WebAuthn** tool, choose **the Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  <span data-ttu-id="e889e-193">Navigieren Sie zu Issue [#1034663][CR1034663], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-193">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1034663][CR1034663].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Öffnen des webauthn-Tools" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         <span data-ttu-id="e889e-195">Öffnen des **webauthn** -Tools</span><span class="sxs-lookup"><span data-stu-id="e889e-195">Open the **WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Webauthn-Tool" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         <span data-ttu-id="e889e-197">**Webauthn** -Tool</span><span class="sxs-lookup"><span data-stu-id="e889e-197">**WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="e889e-198">Elemente-Tool-Updates</span><span class="sxs-lookup"><span data-stu-id="e889e-198">Elements tool updates</span></span>  

#### <span data-ttu-id="e889e-199">Anzeigen des Bereichs "berechnete Seitenleiste" im Bereich "Formatvorlagen"</span><span class="sxs-lookup"><span data-stu-id="e889e-199">View the Computed sidebar pane in the Styles pane</span></span>  

<span data-ttu-id="e889e-200">Umschalten des **berechneten** Bereichs im Bereich " **Formatvorlagen** "</span><span class="sxs-lookup"><span data-stu-id="e889e-200">Toggle the **Computed** pane in the **Styles** pane.</span></span>  <span data-ttu-id="e889e-201">Der **berechnete** Bereich im Bereich " **Formatvorlagen** " ist standardmäßig reduziert.</span><span class="sxs-lookup"><span data-stu-id="e889e-201">The **Computed** pane in the **Styles** pane is collapsed by default.</span></span>  <span data-ttu-id="e889e-202">Um Sie zu aktivieren, wählen Sie die Schaltfläche aus.</span><span class="sxs-lookup"><span data-stu-id="e889e-202">To toggle it, choose the button.</span></span>  <span data-ttu-id="e889e-203">Navigieren Sie zu Issue [#1073899][CR1073899], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-203">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1073899][CR1073899].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Öffnen des Bereichs "berechnete Seitenleiste"" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         <span data-ttu-id="e889e-205">Öffnen des Bereichs " **berechnete Seitenleiste** "</span><span class="sxs-lookup"><span data-stu-id="e889e-205">Open the **Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Bereich "berechnete Seitenleiste"" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         <span data-ttu-id="e889e-207">Bereich " **berechnete Seitenleiste** "</span><span class="sxs-lookup"><span data-stu-id="e889e-207">**Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="e889e-208">Gruppieren von CSS-Eigenschaften im berechneten Panel</span><span class="sxs-lookup"><span data-stu-id="e889e-208">Grouping CSS properties in the Computed panel</span></span>  

<span data-ttu-id="e889e-209">Wenn Sie das angewendete CSS mit einem geringeren Bildlauf anzeigen möchten, Gruppieren Sie die CSS-Eigenschaften nach Kategorien im **berechneten** Bereich.</span><span class="sxs-lookup"><span data-stu-id="e889e-209">To view your applied CSS with less scrolling, group the CSS properties by categories in the **Computed** pane.</span></span>  <span data-ttu-id="e889e-210">Sie können sich auch selektiv auf eine Reihe verwandter Eigenschaften konzentrieren, während Sie Ihr CSS untersuchen.</span><span class="sxs-lookup"><span data-stu-id="e889e-210">You may also selectively focus on a set of related properties while you inspect your CSS.</span></span>  <span data-ttu-id="e889e-211">Wählen Sie **im Element** -Tool ein Element aus.</span><span class="sxs-lookup"><span data-stu-id="e889e-211">From the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="e889e-212">Wenn Sie die CSS-Eigenschaften gruppieren oder die Gruppe aufheben möchten, aktivieren Sie das Kontrollkästchen **Gruppieren** .</span><span class="sxs-lookup"><span data-stu-id="e889e-212">To group \(or ungroup\) the CSS properties, toggle the **Group** checkbox.</span></span>  <span data-ttu-id="e889e-213">Navigieren Sie zu Problemen [#1096230][CR1096230], [#1084673][CR1084673]und [#1106251][CR1106251], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-213">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1096230][CR1096230], [#1084673][CR1084673], and [#1106251][CR1106251].</span></span>  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Gruppieren von CSS-Eigenschaften" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   <span data-ttu-id="e889e-215">Gruppieren von CSS-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e889e-215">Grouping CSS properties</span></span>  
:::image-end:::  

### <span data-ttu-id="e889e-216">Leuchtturm 6,4 im Leuchtturm-Tool</span><span class="sxs-lookup"><span data-stu-id="e889e-216">Lighthouse 6.4 in the Lighthouse tool</span></span>  

<span data-ttu-id="e889e-217">Das **Leuchtturm** -Tool läuft nun auf Lighthouse 6,4.</span><span class="sxs-lookup"><span data-stu-id="e889e-217">The **Lighthouse** tool is now running Lighthouse 6.4.</span></span>  <span data-ttu-id="e889e-218">Wenn Sie eine vollständige Liste der Änderungen finden möchten, navigieren Sie zu den [Anmerkungen zur Lighthouse-Version][GithubGoogleChromeLighthouseReleasesV641].</span><span class="sxs-lookup"><span data-stu-id="e889e-218">For a full list of changes, navigate to the [Lighthouse release notes][GithubGoogleChromeLighthouseReleasesV641].</span></span>  <span data-ttu-id="e889e-219">Navigieren Sie zu Issue [#772558][CR772558], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-219">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#772558][CR772558].</span></span>  

### <span data-ttu-id="e889e-220">Performance. Mark ()-Ereignisse im Abschnitt "Anzeigedauern"</span><span class="sxs-lookup"><span data-stu-id="e889e-220">performance.mark() events in the Timings section</span></span>  

<span data-ttu-id="e889e-221">Der **Abschnitt Timings** einer Aufzeichnung im [Leistungs][DevtoolsGuideChromiumEvaluatePerformanceReference] Tool markiert nun `performance.mark()` Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="e889e-221">The **Timings section** of a recording in the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool now marks `performance.mark()` events.</span></span>  <span data-ttu-id="e889e-222">Wenn Sie dieses Feature testen und die Leistung Ihres JavaScript-Codes messen möchten, fügen Sie `performance.mark()` Ihrem Code Ereignisse hinzu.</span><span class="sxs-lookup"><span data-stu-id="e889e-222">To try this feature and measure the performance of your JavaScript code, add `performance.mark()` events to your code.</span></span>  <span data-ttu-id="e889e-223">Mit dem folgenden Codeausschnitt werden beispielsweise Marker vor und nach einer Schleife hinzugefügt `for` , die mit Inkrementen von 7 von 0 bis 1000 durchläuft.</span><span class="sxs-lookup"><span data-stu-id="e889e-223">For example, the following code snippet adds markers before and after a `for` loop that iterates from 0 to 1000 using increments of 7.</span></span>  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

<span data-ttu-id="e889e-224">Öffnen Sie dann das Tool [Leistung][DevtoolsGuideChromiumEvaluatePerformanceReference] , und navigieren Sie zum **Abschnitt Anzeige** dauern, um Ihren JavaScript-Code aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="e889e-224">Then, open the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool and navigate to the **Timings section** to record your JavaScript code.</span></span>  <span data-ttu-id="e889e-225">Die `performance.mark()` von Ihnen hinzugefügten Ereignisse werden nun in der Aufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e889e-225">The `performance.mark()` events you added are now displayed in the recording.</span></span>  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Performance. Mark-Ereignisse" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` <span data-ttu-id="e889e-227">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e889e-227">events</span></span>  
:::image-end:::  

### <span data-ttu-id="e889e-228">Neue Ressourcentyp-und URL-Filter im Netzwerktool</span><span class="sxs-lookup"><span data-stu-id="e889e-228">New resource-type and url filters in the Network tool</span></span>  

<span data-ttu-id="e889e-229">Verwenden Sie die neuen `resource-type` und `url` Schlüsselwörter im **Netzwerk** Tool, um Netzwerkanforderungen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="e889e-229">Use the new `resource-type` and `url` keywords in the **Network** tool to filter network requests.</span></span>  <span data-ttu-id="e889e-230">Verwenden Sie beispielsweise, `resource-type:image` um sich auf die Netzwerkanforderungen zu konzentrieren, die Bilder sind.</span><span class="sxs-lookup"><span data-stu-id="e889e-230">For example, use `resource-type:image` to focus on the network requests that are images.</span></span>  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="Ressourcentypfilter" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   <span data-ttu-id="e889e-232">Ressourcentypfilter</span><span class="sxs-lookup"><span data-stu-id="e889e-232">resource-type filter</span></span>  
:::image-end:::  

<span data-ttu-id="e889e-233">Wenn Sie weitere spezielle Schlüsselwörter wie "und" entdecken möchten `resource-type` `url` , navigieren Sie zu [Filteranforderungen nach Eigenschaften][DevtoolsNetworkReferenceFilterRequestsProperties].</span><span class="sxs-lookup"><span data-stu-id="e889e-233">To discover more special keywords such as `resource-type` and `url`, navigate to [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span></span>  <span data-ttu-id="e889e-234">Navigieren Sie zu Problemen [#1121141][CR1121141] und [#1104188][CR1104188], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-234">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1121141][CR1121141] and [#1104188][CR1104188].</span></span>  

### <span data-ttu-id="e889e-235">Frame Details-Ansicht Updates</span><span class="sxs-lookup"><span data-stu-id="e889e-235">Frame details view updates</span></span>  

#### <span data-ttu-id="e889e-236">Anzeigen von COEP und Coop-Berichterstattung an Endpunkt</span><span class="sxs-lookup"><span data-stu-id="e889e-236">Display COEP and COOP reporting to endpoint</span></span>  

<span data-ttu-id="e889e-237">Zeigen Sie im `reporting to` Abschnitt **Sicherheits & Isolierung** die Richtlinie für die Cross-Origin-Einbettungs Richtlinie \ (COEP \) und die Cross-Origin-Opener-Richtlinie \ (Coop \) an.</span><span class="sxs-lookup"><span data-stu-id="e889e-237">View the Cross-Origin Embedder Policy \(COEP\) and Cross-Origin Opener Policy \(COOP\) `reporting to` endpoint under the **Security & Isolation** section.</span></span>  <span data-ttu-id="e889e-238">Die [Reporting-API][MdnReportingApi] definiert `Report-To` einen neuen HTTP-Header, der Ihnen die Möglichkeit gibt, die Server Endpunkte für den Browser anzugeben, um Warnungen und Fehler zu senden.</span><span class="sxs-lookup"><span data-stu-id="e889e-238">The [Reporting API][MdnReportingApi] defines `Report-To`, a new HTTP header, that gives you a way to specify the server endpoints for the browser to send warnings and errors.</span></span>  <span data-ttu-id="e889e-239">Navigieren Sie zu Issue [#1051466][CR1051466], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-239">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Der Bericht an den Endpunkt" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   <span data-ttu-id="e889e-241">Der `reporting to` Endpunkt</span><span class="sxs-lookup"><span data-stu-id="e889e-241">The `reporting to` endpoint</span></span>  
:::image-end:::  

#### <span data-ttu-id="e889e-242">Anzeigen des COEP-und Coop-Berichtsmodus</span><span class="sxs-lookup"><span data-stu-id="e889e-242">Display COEP and COOP report-only mode</span></span>  

<span data-ttu-id="e889e-243">DevTools zeigt jetzt die `report-only` Beschriftung für COEP und Coop an, die auf Mode festgesetzt sind `report-only` .</span><span class="sxs-lookup"><span data-stu-id="e889e-243">DevTools now display the `report-only` label for COEP and COOP that are set to `report-only` mode.</span></span>  <span data-ttu-id="e889e-244">Navigieren Sie zu Issue [#1051466][CR1051466], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Die Bezeichnung "nur Berichtsmodus"" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   <span data-ttu-id="e889e-246">Die `report-only` Beschriftung "Modus"</span><span class="sxs-lookup"><span data-stu-id="e889e-246">The `report-only` mode label</span></span>  
:::image-end:::  

### <span data-ttu-id="e889e-247">Anzeigen und Beheben von Problemen mit dem Farbkontrast im Tool "CSS-Übersicht"</span><span class="sxs-lookup"><span data-stu-id="e889e-247">View and fix color contrast issues in the CSS Overview tool</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   <span data-ttu-id="e889e-249">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="e889e-249">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="e889e-250">Das Tool **CSS-Übersicht** zeigt nun eine Liste der Elemente auf der Seite an, die Probleme mit dem Farbkontrast aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e889e-250">The **CSS Overview** tool now displays a list of elements on your page that have color contrast issues.</span></span>  <span data-ttu-id="e889e-251">Die folgende Demo Seite enthält ein Beispiel für ein Farbkontrast Problem.</span><span class="sxs-lookup"><span data-stu-id="e889e-251">The following demo page has an example of a color contrast issue.</span></span>  

[<span data-ttu-id="e889e-252">Demo für barrierefreie Farben für CSS-Übersicht</span><span class="sxs-lookup"><span data-stu-id="e889e-252">CSS Overview Accessible Colors Demo</span></span>][GlitchCssOverviewAccessibleColorsDemo]  

<span data-ttu-id="e889e-253">Um dieses Experiment zu aktivieren, wählen Sie unter **Einstellungen**  >  **Experimente**das Kontrollkästchen **CSS-Übersicht** aus.</span><span class="sxs-lookup"><span data-stu-id="e889e-253">To enable this experiment, under **Settings** > **Experiments**, choose the **CSS Overview** checkbox.</span></span>  <span data-ttu-id="e889e-254">Wenn Sie eine Liste der Elemente mit einem Farbkontrast Problem anzeigen möchten, wählen Sie in **Kontrast Problemen** **Text**aus.</span><span class="sxs-lookup"><span data-stu-id="e889e-254">To view a list of elements that have a color contrast issue, on **Contrast issues**, choose **Text**.</span></span>  <span data-ttu-id="e889e-255">Wenn Sie das Element im Tool **Elemente** öffnen möchten, wählen Sie ein Element in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="e889e-255">To open the element in the **Elements** tool, choose an element in the list.</span></span>  <span data-ttu-id="e889e-256">Um Kontrastprobleme zu beheben, bieten die Microsoft Edge-devtools [automatisch Farbvorschläge][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]an.</span><span class="sxs-lookup"><span data-stu-id="e889e-256">To help fix contrast issues, the Microsoft Edge DevTools [automatically provide color suggestions][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span></span>  <span data-ttu-id="e889e-257">Navigieren Sie zu Issue [#1120316][CR1120316], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e889e-257">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1120316][CR1120316].</span></span>  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Probleme mit niedriger Farbkontrast" lightbox="../../media/2020/10/css-overview.msft.png":::
   <span data-ttu-id="e889e-259">Probleme mit niedriger Farbkontrast</span><span class="sxs-lookup"><span data-stu-id="e889e-259">Low color contrast issues</span></span>  
:::image-end:::  

## <span data-ttu-id="e889e-260">Herunterladen der Microsoft Edge Preview-Kanäle</span><span class="sxs-lookup"><span data-stu-id="e889e-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="e889e-261">Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="e889e-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="e889e-262">Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e889e-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="e889e-263">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="e889e-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Missbilligung des Eigenschaftenbereichs im elementtool – Neuerungen in devtools (Microsoft Edge 84) | Microsoft docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Features des CSS-Raster Debuggens – Neuerungen in devtools (Microsoft Edge 85) | Microsoft docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Vorschlag für barrierefreie Farben im Bereich "Formatvorlagen" – Neuerungen in devtools (Microsoft Edge 86) | Microsoft docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emulieren von mobilen Geräten in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Zuletzt ausgewähltes Element oder JavaScript-Objekt – API-Referenz für Konsolen Dienstprogramme | Microsoft docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Anpassen von Tastenkombinationen in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referenz zur Leistungsanalyse | Microsoft docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Emulation: Unterstützung des Dual-Screen-Modus – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Aktivieren experimenteller APIs – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Aktivieren des Tasten Kombinations-Editors – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulation: Unterstützung des Dual-Screen-Modus – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Aktivieren der Netzwerk Konsole – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Aktivieren der Quellauftrags Anzeige – experimentelle Features | Microsoft docs"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Testen auf faltbaren und Dual-Screen-Geräten – experimentelle Funktionen | Microsoft docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Aktivieren von experimentellen Features – experimentelle Features | Microsoft docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "Tabelle-Console-API-Referenz | Microsoft docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Suchen Sie ungenutzten JavaScript-und CSS-Code mit der Registerkarte Coverage in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Überprüfen des CSS-Rasters | Microsoft docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Schublade – Anpassen von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – anpassen von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analysieren der Renderingleistung mit der Registerkarte "Rendering" – Referenz zur Leistungsanalyse | Microsoft docs"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Anzeigen und Debuggen von Medienplayer-Informationen | Microsoft docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Filtern von Anforderungen nach Eigenschaften-Netzwerkanalyse Referenz | Microsoft docs"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Emulieren von Authentifikatoren und Debuggen von webauthn in Microsoft Edge devtools | Microsoft docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Preview-Kanäle"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio-Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio-Code | Visual Studio-Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chrom Fehler"  

[CR174309]: https://crbug.com/174309 "DevTools: zulassen der Anpassung von Tastenkombinationen/Tastenkombinationen | Chrom Fehler"
[CR772558]: https://crbug.com/772558 "DevTools: Update auf die neueste Version von Lighthouse | Chrom Fehler"  
[CR1034663]: https://crbug.com/1034663 "Erstellen eines Front-End für die webauthn-Test-API | Chrom Fehler"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Tabellentools | Chrom Fehler"  
[CR1051466]: https://crbug.com/1051466 "Unterstützen des Coop/COEP-Debuggens in devtools | Chrom Fehler"  
[CR1073899]: https://crbug.com/1073899 "Die Registerkarte "berechnete Formatvorlage" verschwindet im reaktionsfähigen Modus | Chrom Fehler"  
[CR1075732]: https://crbug.com/1075732 "DevTools-Personalisierung – Movable Tabs | Chrom Fehler"  
[CR1084673]: https://crbug.com/1084673 "DevTools: verbessern Sie die Darstellung von benutzerdefinierten CSS-Eigenschaften (aka). CSS-Variablen) und deren Werte | Chrom Fehler"  
[CR1093687]: https://crbug.com/1093687 "Tool zum Erstellen und Wiedergeben von synthetischen Netzwerkanforderungen | Chrom Fehler"  
[CR1096230]: https://crbug.com/1096230 "Gruppieren von CSS-Eigenschaften nach Kategorien im Bereich "berechnete Formatvorlagen" | Chrom Fehler"  
[CR1104188]: https://crbug.com/1104188 "Bei der Suche nach vollständiger URL werden keine Ergebnisse gefunden. Chrom Fehler"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: Registerkarte "berechnete Formatvorlagen verbessern" | Chrom Fehler"  
[CR1120316]: https://crbug.com/1120316 "Ungültiger Kontrast unter CSS-Übersicht > Farben | Chrom Fehler"  
[CR1121141]: https://crbug.com/1121141 "Filtern nach Ressourcentyp in Netzwerkprotokoll zulassen | Chrom Fehler"  
[CR1121312]: https://crbug.com/1121312 "Einstellungen sollten aus dem Menü "Weitere Tools" entfernt werden | Chrom Fehler"  
[CR1136394]: https://crbug.com/1136394 "Flexbox-Tooling | Chrom Fehler"  
[CR1136655]: https://crbug.com/1136655 "Devtools: Lokalisierung v2 | Chrom Fehler"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Reporting-API | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v 6.4.1-GoogleChrome/Leuchtturm | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Web-Authentifizierung | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Hallo! | Glitch"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Postboten-Sammlungs Format v 2.1.0 | Postbote"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "OpenAPI-Spezifikation | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> <span data-ttu-id="e889e-316">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e889e-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e889e-317">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/updates/2020/10/devtools/index) gefunden und von [Jecelyn Yeen][JecelynYeen] \ (Developer Advocate, Chrome devtools \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e889e-317">The original page is found [here](https://developers.google.com/web/updates/2020/10/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="e889e-319">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e889e-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
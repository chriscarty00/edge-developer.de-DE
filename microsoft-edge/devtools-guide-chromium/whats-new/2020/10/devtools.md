---
description: Neue CSS-Raster-Debuggingtools, Webauthn-Tool, verschiebbare Tools und berechnete Sidebarpanels.
title: Neues in DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: cf3a685a1a4e9a3f13d2401a6294058a71dd5104
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313030"
---
# <span data-ttu-id="59f33-104">Neues in DevTools (Microsoft Edge 87)</span><span class="sxs-lookup"><span data-stu-id="59f33-104">What's New In DevTools (Microsoft Edge 87)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="59f33-105">Verbessern der Lokalisierung von DevTools</span><span class="sxs-lookup"><span data-stu-id="59f33-105">Improving DevTools localization</span></span>  

<span data-ttu-id="59f33-106">Um Ihre Übersetzungsanforderungen zu erfüllen, konzentriert sich das Microsoft Edge DevTools-Team auf die Verbesserung der Übersetzungsqualität.</span><span class="sxs-lookup"><span data-stu-id="59f33-106">To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.</span></span>  <span data-ttu-id="59f33-107">Ab Microsoft Edge, Version 87, sind mehrere Zeichenfolgen und Begriffe gesperrt und ändern sich nicht, auch wenn die restlichen DevTools in anderen Sprachen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="59f33-107">Starting in Microsoft Edge version 87, several strings and terms are locked and do not change even when the rest of the DevTools are displayed in other languages.</span></span>  <span data-ttu-id="59f33-108">Die Liste der betroffenen Zeichenfolgen und Begriffe enthält Folgendes.</span><span class="sxs-lookup"><span data-stu-id="59f33-108">The list of affected strings and terms include the following.</span></span>  

*   <span data-ttu-id="59f33-109">Die Zeichenfolgen im **Tool "2013".**</span><span class="sxs-lookup"><span data-stu-id="59f33-109">The strings in the **Lighthouse** tool.</span></span>  
*   <span data-ttu-id="59f33-110">Der Ausdruck `service worker` .</span><span class="sxs-lookup"><span data-stu-id="59f33-110">The term `service worker`.</span></span>  
*   <span data-ttu-id="59f33-111">Einige der **Netzwerktoolfilter,** z. B. `URL` , und `XHR` `JS` `CSS` .</span><span class="sxs-lookup"><span data-stu-id="59f33-111">Some of the **Network** tool filters such as `URL`, `XHR`, `JS`, and `CSS`.</span></span>  
*   <span data-ttu-id="59f33-112">Die [Konsolen-Hilfsprogramme-API "$0".][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]</span><span class="sxs-lookup"><span data-stu-id="59f33-112">The [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] Console Utilities API.</span></span>  
    
<span data-ttu-id="59f33-113">[0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] USD ist jetzt in der [Konsole](/microsoft-edge/devtools-guide-chromium/console/index.md) für Benutzer mit lokalisierten Versionen von DevTools verfügbar.</span><span class="sxs-lookup"><span data-stu-id="59f33-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] is now available in the [Console](/microsoft-edge/devtools-guide-chromium/console/index.md) for users on localized versions of the DevTools.</span></span>   <span data-ttu-id="59f33-114">Vielen Dank an die globale Entwickler-Community, die die Lokalisierung der Microsoft Edge DevTools verbessert hat.</span><span class="sxs-lookup"><span data-stu-id="59f33-114">Thank you to the global developer community for helping improve localization of the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="59f33-115">Senden Sie [weiterhin Feedback zur Lokalisierungsqualität,](#getting-in-touch-with-microsoft-edge-devtools-team) um die Unterstützung für DevTools in allen Locales zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="59f33-115">Continue to [send feedback on localization quality](#getting-in-touch-with-microsoft-edge-devtools-team) to improve support for DevTools in all locales.</span></span>  <span data-ttu-id="59f33-116">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="59f33-116">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Netzwerktool mit nicht lokalisierten Filtern" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   <span data-ttu-id="59f33-118">**Netzwerkbereich** mit nicht lokalisierten Filtern</span><span class="sxs-lookup"><span data-stu-id="59f33-118">**Network** pane with non-localized filters</span></span>  
:::image-end:::  

## <span data-ttu-id="59f33-119">Verschieben von Tools zwischen oberen und unteren Panels</span><span class="sxs-lookup"><span data-stu-id="59f33-119">Move tools between top and bottom panels</span></span>  

<span data-ttu-id="59f33-120">DevTools unterstützt jetzt das Verschieben von Tools zwischen dem oberen und unteren Bereich.</span><span class="sxs-lookup"><span data-stu-id="59f33-120">DevTools now supports moving tools between the top and bottom panels.</span></span>  <span data-ttu-id="59f33-121">Passen Sie Ihre DevTools an, und verbessern Sie Ihre Produktivität, indem Sie eine beliebige Kombination von zwei Tools gleichzeitig anzeigen.</span><span class="sxs-lookup"><span data-stu-id="59f33-121">Customize your DevTools and improve your productivity by viewing any combination of two tools at the same time.</span></span>  <span data-ttu-id="59f33-122">Beispielsweise können Sie die **Elemente und** **die** Quellentools gleichzeitig \*\*\*\* anzeigen \(durch Verschieben des Quellentools nach unten\).</span><span class="sxs-lookup"><span data-stu-id="59f33-122">For example, view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span></span>  <span data-ttu-id="59f33-123">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [#1075732][CR1075732].</span><span class="sxs-lookup"><span data-stu-id="59f33-123">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1075732][CR1075732].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="59f33-124">Um ein beliebiges oberstes Tool nach unten zu verschieben, zeigen Sie auf eine Registerkarte, öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **"Nach unten verschieben" aus.**</span><span class="sxs-lookup"><span data-stu-id="59f33-124">To move any top tool to the bottom, hover on a tab, open the contextual menu \(right-click\), and choose **Move to bottom**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Nach unten bewegen" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         <span data-ttu-id="59f33-126">Nach unten bewegen</span><span class="sxs-lookup"><span data-stu-id="59f33-126">Move to bottom</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="59f33-127">Um ein beliebiges unteres Tool nach oben zu verschieben, zeigen Sie auf eine Registerkarte, öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **"Nach oben" aus.**</span><span class="sxs-lookup"><span data-stu-id="59f33-127">To move any bottom tool to the top, hover on a tab, open the contextual menu \(right-click\), and choose **Move to top**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Nach oben" lightbox="../../media/2020/10/move-to-top.msft.png":::
         <span data-ttu-id="59f33-129">Nach oben</span><span class="sxs-lookup"><span data-stu-id="59f33-129">Move to top</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="59f33-130">Speichern und Exportieren mithilfe der Netzwerkkonsole</span><span class="sxs-lookup"><span data-stu-id="59f33-130">Save and export using the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="59f33-132">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="59f33-132">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="59f33-133">Das **Tool "Netzwerkkonsole"** hat nun die Kompatibilität mit den [Postman v2.1-][PostmanSchemaJsonCollectionv210Index] und [OpenAPI v2-Schemas][SwaggerSpecificationV2] verbessert.</span><span class="sxs-lookup"><span data-stu-id="59f33-133">The **Network Console** tool now has improved compatibility with the [Postman v2.1][PostmanSchemaJsonCollectionv210Index] and [OpenAPI v2][SwaggerSpecificationV2] schemas.</span></span>  <span data-ttu-id="59f33-134">Um das Experiment zu aktivieren, navigieren Sie zu "Experimentelle Funktionen [aktivieren",][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **"Netzwerkkonsole aktivieren".**</span><span class="sxs-lookup"><span data-stu-id="59f33-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span></span>  <span data-ttu-id="59f33-135">Weitere Informationen zur Netzwerkkonsole **finden**Sie unter ["Enable Network Console Experimental".][DevtoolsExperimentalFeaturesEnableNetworkConsole]</span><span class="sxs-lookup"><span data-stu-id="59f33-135">For more information about the **Network Console**, navigate to [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span></span>  <span data-ttu-id="59f33-136">Dieses Experiment unterstützt jetzt die folgenden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="59f33-136">This experiment now supports the following actions.</span></span>  

*   <span data-ttu-id="59f33-137">Speichern und Exportieren von Sammlungen und Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="59f33-137">Save and export Collections and Environments.</span></span>  
*   <span data-ttu-id="59f33-138">Bearbeiten und Exportieren von Gruppen von Umgebungsvariablen im **Tool "Netzwerkkonsole".**</span><span class="sxs-lookup"><span data-stu-id="59f33-138">Edit and export sets of environment variables within the **Network Console** tool.</span></span>  
    
<span data-ttu-id="59f33-139">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1093687][CR1093687].</span><span class="sxs-lookup"><span data-stu-id="59f33-139">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1093687][CR1093687].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Geben Sie den Namen für die neue Umgebung ein." lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         <span data-ttu-id="59f33-141">Geben Sie den Namen für die neue Umgebung ein.</span><span class="sxs-lookup"><span data-stu-id="59f33-141">Enter name for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Auswählen des Formats für die neue Umgebung" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         <span data-ttu-id="59f33-143">Auswählen des Formats für die neue Umgebung</span><span class="sxs-lookup"><span data-stu-id="59f33-143">Choose format for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="59f33-144">Verbesserte CSS-Raster-Tools</span><span class="sxs-lookup"><span data-stu-id="59f33-144">Improved CSS Grid tooling</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="59f33-146">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="59f33-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="59f33-147">Die Microsoft Edge DevTools unterstützen jetzt die folgenden Features zum Überprüfen, Anzeigen und Debuggen Ihrer CSS-Raster.</span><span class="sxs-lookup"><span data-stu-id="59f33-147">The Microsoft Edge DevTools now support the following features for inspecting, viewing, and debugging your CSS grids.</span></span>  

*   <span data-ttu-id="59f33-148">Zeigen Sie eine vereinfachte Rasterüberlagerung mithilfe des Tools **"Überprüfen"** an, oder erhalten Sie detailliertere Informationen mit beständigen Überlagerungen.</span><span class="sxs-lookup"><span data-stu-id="59f33-148">Display a simplified grid overlay using the **Inspect** tool, or get more detailed information with persistent overlays.</span></span>  
*   <span data-ttu-id="59f33-149">Um beständige Rasterüberlagerungen zu aktivieren, wählen Sie \*\*\*\* das Rastersymbol neben einem Rastercontainerelement im Elementtool oder das Raster im **Layouttool** aus.</span><span class="sxs-lookup"><span data-stu-id="59f33-149">To enable persistent grid overlays, choose the grid icon next to a grid container element in the **Elements** tool or choose the grid in the **Layout** tool.</span></span>  
*   <span data-ttu-id="59f33-150">Sie können beständige Überlagerungen für mehrere Raster aktivieren.</span><span class="sxs-lookup"><span data-stu-id="59f33-150">You may enable persistent overlays for multiple grids.</span></span>  
*   <span data-ttu-id="59f33-151">Mit dem **neuen Layouttool** können Sie Rasterüberlagerungen einfach umschalten und das Erscheinungsbild und den Inhalt für jedes Layout konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="59f33-151">The new **Layout** tool allows you to easily toggle grid overlays and configure the appearance and the content for each.</span></span>  
    
<span data-ttu-id="59f33-152">Die Features sind standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="59f33-152">The features are turned on by default.</span></span>  <span data-ttu-id="59f33-153">Weitere Informationen zu den Features finden Sie unter [CSS-Raster.][DevtoolsCssGrid]</span><span class="sxs-lookup"><span data-stu-id="59f33-153">For more information about the features, navigate to [CSS grids][DevtoolsCssGrid].</span></span>  <span data-ttu-id="59f33-154">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [#1047356][CR1047356].</span><span class="sxs-lookup"><span data-stu-id="59f33-154">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1047356][CR1047356].</span></span>  <span data-ttu-id="59f33-155">Darüber hinaus arbeitet das Microsoft Edge DevTools-Team mit dem Chrome DevTools-Team und der Chromium-Community zusammen, um DevTools neue Flexbox-Toolfunktionen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="59f33-155">Additionally, the Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new flexbox tooling features to DevTools.</span></span>  <span data-ttu-id="59f33-156">Um Updates für Flexboxtools im Open-Source-Projekt Chromium zu erhalten, navigieren Sie zu Problem [#1136394][CR1136394].</span><span class="sxs-lookup"><span data-stu-id="59f33-156">For updates on flexbox tooling in the Chromium open-source project, navigate to Issue [#1136394][CR1136394].</span></span>  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Layouttool mit Rastern" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   <span data-ttu-id="59f33-158">**Layouttool** mit Rastern</span><span class="sxs-lookup"><span data-stu-id="59f33-158">**Layout** tool with grids</span></span>  
:::image-end:::  

## <span data-ttu-id="59f33-159">Anpassen von Tastenkombinationen in den Einstellungen</span><span class="sxs-lookup"><span data-stu-id="59f33-159">Customize keyboard shortcuts in Settings</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="59f33-161">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="59f33-161">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="59f33-162">Sie können jetzt die Tastenkombination für jede Aktion in devTools anpassen.</span><span class="sxs-lookup"><span data-stu-id="59f33-162">You are now able to customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="59f33-163">Seit Microsoft Edge Version 84 können Sie zwischen Visual Studio **Code** und **DevTools (Standard)-Voreinstellungen** für Tastenkombinationen [wählen.][DevtoolsCustomizeShortcuts]</span><span class="sxs-lookup"><span data-stu-id="59f33-163">Since Microsoft Edge version 84, you are able to choose between **Visual Studio Code** and **DevTools (default)** presets for [keyboard shortcuts][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="59f33-164">Ab Microsoft Edge, Version 87, \*\*\*\* können Sie das Experiment "Tastenkombination-Editor aktivieren" aktivieren, um Tastenkombinationen [weiter anzupassen.][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]</span><span class="sxs-lookup"><span data-stu-id="59f33-164">Starting in Microsoft Edge version 87, you may turn on the **Enable keyboard shortcut editor** experiment to further [customize keyboard shortcuts][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="59f33-165">Um das Experiment zu aktivieren, navigieren Sie zu "Experimentelle Funktionen [aktivieren",][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **"Tastenkombination-Editor aktivieren".**</span><span class="sxs-lookup"><span data-stu-id="59f33-165">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="59f33-166">Weitere Informationen zum Anpassen und Bearbeiten von Tastenkombinationen finden Sie unter [Experimentelles Feature „Tastenkombinations-Editor aktivieren“][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="59f33-166">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  <span data-ttu-id="59f33-167">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="59f33-167">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Benutzerdefinierte Verknüpfung zum Anhalten eines Skripts" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   <span data-ttu-id="59f33-169">Benutzerdefinierte Verknüpfung zum Anhalten eines Skripts</span><span class="sxs-lookup"><span data-stu-id="59f33-169">Custom shortcut for pausing a script</span></span>  
:::image-end:::  

## <span data-ttu-id="59f33-170">Einführung in die Microsoft Edge Tools for Visual Studio Code extension</span><span class="sxs-lookup"><span data-stu-id="59f33-170">Introducing the Microsoft Edge Tools for Visual Studio Code extension</span></span>  

<span data-ttu-id="59f33-171">Die **Elemente für Visual Studio Code** und Network for Visual Studio **Code** werden jetzt mit den neuen Microsoft Edge Developer Tools for [Visual Studio Codeerweiterung][VisualStudioCodeMarketplaceMsEdgedevtools] zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="59f33-171">The **Elements for Visual Studio Code** and **Network for Visual Studio Code** extensions are now merged into the new [Microsoft Edge Developer Tools for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extension.</span></span>  <span data-ttu-id="59f33-172">Verwenden Sie die Microsoft Edge DevTools für die folgenden Aktivitäten, ohne Visual Studio verlassen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="59f33-172">Use the Microsoft Edge DevTools for the following activities without leaving Visual Studio Code.</span></span>  

*   <span data-ttu-id="59f33-173">Debuggen des DOM</span><span class="sxs-lookup"><span data-stu-id="59f33-173">Debug the DOM</span></span>  
*   <span data-ttu-id="59f33-174">Bearbeiten von CSS</span><span class="sxs-lookup"><span data-stu-id="59f33-174">Edit CSS</span></span>  
*   <span data-ttu-id="59f33-175">Überprüfen des Netzwerkdatenverkehrs</span><span class="sxs-lookup"><span data-stu-id="59f33-175">Inspect network traffic</span></span>  

<span data-ttu-id="59f33-176">Starten Sie mit der Erweiterung Microsoft Edge, stellen Sie eine Verbindung mit einer vorhandenen Instanz des Browsers oder verwenden Sie direkt in Ihrem Editor einen browserlosen Browser.</span><span class="sxs-lookup"><span data-stu-id="59f33-176">With the extension, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span></span>  <span data-ttu-id="59f33-177">Um probleme mit Ihrem Feedback zu dieser Erweiterung zu lösen, navigieren Sie zum [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] Repository auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="59f33-177">To start contributing and filing issues with your feedback about this extension, navigate to the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Screenshot der Erweiterung im vollständigen Browsermodus" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         <span data-ttu-id="59f33-179">Screenshot der Erweiterung im vollständigen Browsermodus</span><span class="sxs-lookup"><span data-stu-id="59f33-179">Using the extension in full browser mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Screenshot der Erweiterung im kopflosen Modus" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         <span data-ttu-id="59f33-181">Screenshot der Erweiterung im kopflosen Modus</span><span class="sxs-lookup"><span data-stu-id="59f33-181">Using the extension in headless mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="59f33-182">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="59f33-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="59f33-183">Neues WebAuthn-Tool</span><span class="sxs-lookup"><span data-stu-id="59f33-183">New WebAuthn tool</span></span>  

<span data-ttu-id="59f33-184">In früheren Versionen von Microsoft Edge gab es keine systemeigene WebAuthn-Debugunterstützung.</span><span class="sxs-lookup"><span data-stu-id="59f33-184">In earlier versions of Microsoft Edge, there was no native WebAuthn debugging support.</span></span>  <span data-ttu-id="59f33-185">Sie benötigten physische Authentatoren, um Ihre Webanwendung mit der [Webauthentifizierungs-API zu testen.][GithubW3cWebauthn]</span><span class="sxs-lookup"><span data-stu-id="59f33-185">You needed physical authenticators to test your web application with the [Web Authentication API][GithubW3cWebauthn].</span></span>  <span data-ttu-id="59f33-186">Mit dem neuen **Tool WebAuthn** können Sie die folgenden Aktionen ausführen, ohne physische Authentatoren zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="59f33-186">With the new **WebAuthn** tool, you are able to do the following actions without the use of any physical authenticators.</span></span>

*   <span data-ttu-id="59f33-187">Emulieren von Authentatoren</span><span class="sxs-lookup"><span data-stu-id="59f33-187">Emulate authenticators</span></span>
*   <span data-ttu-id="59f33-188">Anpassen von Attributen von Authentatoren</span><span class="sxs-lookup"><span data-stu-id="59f33-188">Customize attributes of authenticators</span></span>
*   <span data-ttu-id="59f33-189">Überprüfen der Zustände von Authentatoren</span><span class="sxs-lookup"><span data-stu-id="59f33-189">Inspect states of authenticators</span></span>
    
<span data-ttu-id="59f33-190">Weitere Informationen zum **Feature WebAuthn** finden Sie unter Emulieren von Authentatoren und Debuggen von [WebAuthn in Microsoft Edge DevTools.][DevtoolsWebauthnIndex]</span><span class="sxs-lookup"><span data-stu-id="59f33-190">For more information about the **WebAuthn** feature, navigate to [Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span></span>  

<span data-ttu-id="59f33-191">Sie können Authentatoren emulieren und die [Webauthentifizierungs-API][GithubW3cWebauthn] mit dem neuen [WebAuthn-Tool][DevtoolsWebauthnIndex] debuggen.</span><span class="sxs-lookup"><span data-stu-id="59f33-191">You are able to emulate authenticators and debug the [Web Authentication API][GithubW3cWebauthn] with the new [WebAuthn][DevtoolsWebauthnIndex] tool.</span></span>  <span data-ttu-id="59f33-192">Um das **Tool WebAuthn zu** öffnen, wählen Sie das Symbol **DevTools** anpassen und steuern \( \) aus, > Weitere Tools `...` \*\*\*\*  >  **WebAuthn**.</span><span class="sxs-lookup"><span data-stu-id="59f33-192">To open the **WebAuthn** tool, choose **the Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  <span data-ttu-id="59f33-193">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1034663][CR1034663].</span><span class="sxs-lookup"><span data-stu-id="59f33-193">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1034663][CR1034663].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Öffnen des WebAuthn-Tools" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         <span data-ttu-id="59f33-195">Öffnen des **WebAuthn-Tools**</span><span class="sxs-lookup"><span data-stu-id="59f33-195">Open the **WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Tool WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         <span data-ttu-id="59f33-197">**Tool WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="59f33-197">**WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="59f33-198">Elementtoolupdates</span><span class="sxs-lookup"><span data-stu-id="59f33-198">Elements tool updates</span></span>  

#### <span data-ttu-id="59f33-199">Anzeigen des Bereichs "Berechnete Randleiste" im Formatvorlagenbereich</span><span class="sxs-lookup"><span data-stu-id="59f33-199">View the Computed sidebar pane in the Styles pane</span></span>  

<span data-ttu-id="59f33-200">Schalten Sie den **berechneten Bereich** im **Formatvorlagenbereich** um.</span><span class="sxs-lookup"><span data-stu-id="59f33-200">Toggle the **Computed** pane in the **Styles** pane.</span></span>  <span data-ttu-id="59f33-201">Der **berechnete** Bereich **im** Formatvorlagenbereich ist standardmäßig reduziert.</span><span class="sxs-lookup"><span data-stu-id="59f33-201">The **Computed** pane in the **Styles** pane is collapsed by default.</span></span>  <span data-ttu-id="59f33-202">Um ihn umschalten zu können, klicken Sie auf die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="59f33-202">To toggle it, choose the button.</span></span>  <span data-ttu-id="59f33-203">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1073899][CR1073899].</span><span class="sxs-lookup"><span data-stu-id="59f33-203">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1073899][CR1073899].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Öffnen des Bereichs "Berechnete Seitenleiste"" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         <span data-ttu-id="59f33-205">Öffnen des **Bereichs "Berechnete Seitenleiste"**</span><span class="sxs-lookup"><span data-stu-id="59f33-205">Open the **Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Berechneter Randbereich" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         <span data-ttu-id="59f33-207">**Berechneter Randbereich**</span><span class="sxs-lookup"><span data-stu-id="59f33-207">**Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="59f33-208">Gruppieren von CSS-Eigenschaften im berechneten Bereich</span><span class="sxs-lookup"><span data-stu-id="59f33-208">Grouping CSS properties in the Computed panel</span></span>  

<span data-ttu-id="59f33-209">Um die angewendeten CSS mit weniger Bildlauf anzuzeigen, gruppieren Sie die CSS-Eigenschaften nach Kategorien im **Berechneten** Bereich.</span><span class="sxs-lookup"><span data-stu-id="59f33-209">To view your applied CSS with less scrolling, group the CSS properties by categories in the **Computed** pane.</span></span>  <span data-ttu-id="59f33-210">Sie können sich auch selektiv auf eine Reihe verwandter Eigenschaften konzentrieren, während Sie Ihre CSS überprüfen.</span><span class="sxs-lookup"><span data-stu-id="59f33-210">You may also selectively focus on a set of related properties while you inspect your CSS.</span></span>  <span data-ttu-id="59f33-211">Wählen Sie **im Tool "Elemente"** ein Element aus.</span><span class="sxs-lookup"><span data-stu-id="59f33-211">From the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="59f33-212">Um die CSS -Eigenschaften zu gruppieren (oder die Gruppierung zu aufheben), aktivieren Sie das **Kontrollkästchen Gruppe .**</span><span class="sxs-lookup"><span data-stu-id="59f33-212">To group \(or ungroup\) the CSS properties, toggle the **Group** checkbox.</span></span>  <span data-ttu-id="59f33-213">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [#1096230][CR1096230], [#1084673][CR1084673]und [#1106251][CR1106251].</span><span class="sxs-lookup"><span data-stu-id="59f33-213">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1096230][CR1096230], [#1084673][CR1084673], and [#1106251][CR1106251].</span></span>  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Gruppieren von CSS-Eigenschaften" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   <span data-ttu-id="59f33-215">Gruppieren von CSS-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59f33-215">Grouping CSS properties</span></span>  
:::image-end:::  

### <span data-ttu-id="59f33-216">1. Juni 6.4 im Tool "Wiedererbauen"</span><span class="sxs-lookup"><span data-stu-id="59f33-216">Lighthouse 6.4 in the Lighthouse tool</span></span>  

<span data-ttu-id="59f33-217">Das **Tool "2013"** wird nun mit Dement 6.4 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59f33-217">The **Lighthouse** tool is now running Lighthouse 6.4.</span></span>  <span data-ttu-id="59f33-218">Eine vollständige Liste der Änderungen finden Sie in den Anmerkungen zur [Veröffentlichung des Veröffentlichungsprojekts.][GithubGoogleChromeLighthouseReleasesV641]</span><span class="sxs-lookup"><span data-stu-id="59f33-218">For a full list of changes, navigate to the [Lighthouse release notes][GithubGoogleChromeLighthouseReleasesV641].</span></span>  <span data-ttu-id="59f33-219">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#772558][CR772558].</span><span class="sxs-lookup"><span data-stu-id="59f33-219">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#772558][CR772558].</span></span>  

### <span data-ttu-id="59f33-220">performance.mark()-Ereignisse im Abschnitt "Timings"</span><span class="sxs-lookup"><span data-stu-id="59f33-220">performance.mark() events in the Timings section</span></span>  

<span data-ttu-id="59f33-221">Im **Abschnitt "Timings"** einer Aufzeichnung im Tool ["Leistung"][DevtoolsGuideChromiumEvaluatePerformanceReference] werden jetzt Ereignisse `performance.mark()` markiert.</span><span class="sxs-lookup"><span data-stu-id="59f33-221">The **Timings section** of a recording in the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool now marks `performance.mark()` events.</span></span>  <span data-ttu-id="59f33-222">Um dieses Feature auszuprobieren und die Leistung Ihres JavaScript-Codes zu messen, fügen Sie `performance.mark()` Dem Code Ereignisse hinzu.</span><span class="sxs-lookup"><span data-stu-id="59f33-222">To try this feature and measure the performance of your JavaScript code, add `performance.mark()` events to your code.</span></span>  <span data-ttu-id="59f33-223">Der folgende Codeausschnitt fügt beispielsweise Markierungen vor und nach einer Schleife hinzu, die in Schritten von 7 von 0 bis `for` 1000 iteriert wird.</span><span class="sxs-lookup"><span data-stu-id="59f33-223">For example, the following code snippet adds markers before and after a `for` loop that iterates from 0 to 1000 using increments of 7.</span></span>  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

<span data-ttu-id="59f33-224">Öffnen Sie dann das [Leistungstool,][DevtoolsGuideChromiumEvaluatePerformanceReference] und navigieren Sie zum Abschnitt **"Timings",** um Ihren JavaScript-Code zu notiert.</span><span class="sxs-lookup"><span data-stu-id="59f33-224">Then, open the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool and navigate to the **Timings section** to record your JavaScript code.</span></span>  <span data-ttu-id="59f33-225">Die `performance.mark()` hinzugefügten Ereignisse werden nun in der Aufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="59f33-225">The `performance.mark()` events you added are now displayed in the recording.</span></span>  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Performance.mark-Ereignisse" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` <span data-ttu-id="59f33-227">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="59f33-227">events</span></span>  
:::image-end:::  

### <span data-ttu-id="59f33-228">Neue Ressourcentyp- und URL-Filter im Netzwerktool</span><span class="sxs-lookup"><span data-stu-id="59f33-228">New resource-type and url filters in the Network tool</span></span>  

<span data-ttu-id="59f33-229">Verwenden Sie die neuen `resource-type` und `url` Schlüsselwörter im **Netzwerktool,** um Netzwerkanforderungen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="59f33-229">Use the new `resource-type` and `url` keywords in the **Network** tool to filter network requests.</span></span>  <span data-ttu-id="59f33-230">Verwenden Sie dies beispielsweise, `resource-type:image` um sich auf die Netzwerkanforderungen zu konzentrieren, bei der es sich um Bilder handelt.</span><span class="sxs-lookup"><span data-stu-id="59f33-230">For example, use `resource-type:image` to focus on the network requests that are images.</span></span>  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="Ressourcentypfilter" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   <span data-ttu-id="59f33-232">Ressourcentypfilter</span><span class="sxs-lookup"><span data-stu-id="59f33-232">resource-type filter</span></span>  
:::image-end:::  

<span data-ttu-id="59f33-233">Um speziellere Schlüsselwörter wie und `resource-type` `url` zu ermitteln, navigieren Sie zu [Filteranforderungen nach Eigenschaften.][DevtoolsNetworkReferenceFilterRequestsProperties]</span><span class="sxs-lookup"><span data-stu-id="59f33-233">To discover more special keywords such as `resource-type` and `url`, navigate to [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span></span>  <span data-ttu-id="59f33-234">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [#1121141][CR1121141] und [#1104188][CR1104188].</span><span class="sxs-lookup"><span data-stu-id="59f33-234">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1121141][CR1121141] and [#1104188][CR1104188].</span></span>  

### <span data-ttu-id="59f33-235">Updates der Frame-Detailansicht</span><span class="sxs-lookup"><span data-stu-id="59f33-235">Frame details view updates</span></span>  

#### <span data-ttu-id="59f33-236">Anzeigen der COEP- und DERSRG-Berichterstellung für Endpunkte</span><span class="sxs-lookup"><span data-stu-id="59f33-236">Display COEP and COOP reporting to endpoint</span></span>  

<span data-ttu-id="59f33-237">Sehen Sie sich den Endpunkt "Cross-Origin Embedder Policy \(COEP\") und den Endpunkt "Cross-Origin Opener Policy \(ZUR\) " `reporting to` **Security & Isolation"** an.</span><span class="sxs-lookup"><span data-stu-id="59f33-237">View the Cross-Origin Embedder Policy \(COEP\) and Cross-Origin Opener Policy \(COOP\) `reporting to` endpoint under the **Security & Isolation** section.</span></span>  <span data-ttu-id="59f33-238">Die [Berichterstellungs-API][MdnReportingApi] definiert einen neuen HTTP-Header, mit dem Sie die Serverendpunkte für den Browser zum Senden von Warnungen und `Report-To` Fehlern angeben können.</span><span class="sxs-lookup"><span data-stu-id="59f33-238">The [Reporting API][MdnReportingApi] defines `Report-To`, a new HTTP header, that gives you a way to specify the server endpoints for the browser to send warnings and errors.</span></span>  <span data-ttu-id="59f33-239">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="59f33-239">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Die Berichterstellung an den Endpunkt" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   <span data-ttu-id="59f33-241">Der `reporting to` Endpunkt</span><span class="sxs-lookup"><span data-stu-id="59f33-241">The `reporting to` endpoint</span></span>  
:::image-end:::  

#### <span data-ttu-id="59f33-242">Anzeigen des Berichtsmodus "COEP" und "DESGOE"</span><span class="sxs-lookup"><span data-stu-id="59f33-242">Display COEP and COOP report-only mode</span></span>  

<span data-ttu-id="59f33-243">DevTools zeigen jetzt die Bezeichnung für COEP und HOC an, `report-only` die auf den Modus festgelegt `report-only` sind.</span><span class="sxs-lookup"><span data-stu-id="59f33-243">DevTools now display the `report-only` label for COEP and COOP that are set to `report-only` mode.</span></span>  <span data-ttu-id="59f33-244">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="59f33-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Bezeichnung für den Nur-Bericht-Modus" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   <span data-ttu-id="59f33-246">Die `report-only` Modusbezeichnung</span><span class="sxs-lookup"><span data-stu-id="59f33-246">The `report-only` mode label</span></span>  
:::image-end:::  

### <span data-ttu-id="59f33-247">Anzeigen und Beheben von Problemen mit dem Farbkontrast im Css-Übersichtstool</span><span class="sxs-lookup"><span data-stu-id="59f33-247">View and fix color contrast issues in the CSS Overview tool</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="59f33-249">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="59f33-249">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="59f33-250">Das **Tool "CSS-Übersicht"** zeigt nun eine Liste der Elemente auf Der Seite an, die Probleme mit dem Farbkontrast haben.</span><span class="sxs-lookup"><span data-stu-id="59f33-250">The **CSS Overview** tool now displays a list of elements on your page that have color contrast issues.</span></span>  <span data-ttu-id="59f33-251">Die folgende Demoseite enthält ein Beispiel für ein Problem mit dem Farbkontrast.</span><span class="sxs-lookup"><span data-stu-id="59f33-251">The following demo page has an example of a color contrast issue.</span></span>  

[<span data-ttu-id="59f33-252">Demo zu barrierefreien Farben in CSS (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="59f33-252">CSS Overview Accessible Colors Demo</span></span>][GlitchCssOverviewAccessibleColorsDemo]  

<span data-ttu-id="59f33-253">Um dieses Experiment \*\*\*\* zu aktivieren, aktivieren Sie unter "Einstellungsexperimente"  >  \*\*\*\* das **Kontrollkästchen "CSS-Übersicht".**</span><span class="sxs-lookup"><span data-stu-id="59f33-253">To enable this experiment, under **Settings** > **Experiments**, choose the **CSS Overview** checkbox.</span></span>  <span data-ttu-id="59f33-254">Wenn Sie eine Liste der Elemente anzeigen möchten, bei deren Farbkontrast ein Problem mit dem Farbkontrast besteht, wählen Sie bei Problemen mit dem **Kontrast** **Text aus.**</span><span class="sxs-lookup"><span data-stu-id="59f33-254">To view a list of elements that have a color contrast issue, on **Contrast issues**, choose **Text**.</span></span>  <span data-ttu-id="59f33-255">Um das Element im Tool **"Elemente" zu** öffnen, wählen Sie ein Element in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="59f33-255">To open the element in the **Elements** tool, choose an element in the list.</span></span>  <span data-ttu-id="59f33-256">Zur Behebung von Kontrastproblemen stellen die Microsoft Edge DevTools [automatisch Farbvorschläge zur Verfügung.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]</span><span class="sxs-lookup"><span data-stu-id="59f33-256">To help fix contrast issues, the Microsoft Edge DevTools [automatically provide color suggestions][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span></span>  <span data-ttu-id="59f33-257">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [#1120316][CR1120316].</span><span class="sxs-lookup"><span data-stu-id="59f33-257">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1120316][CR1120316].</span></span>  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Probleme mit geringem Farbkontrast" lightbox="../../media/2020/10/css-overview.msft.png":::
   <span data-ttu-id="59f33-259">Probleme mit geringem Farbkontrast</span><span class="sxs-lookup"><span data-stu-id="59f33-259">Low color contrast issues</span></span>  
:::image-end:::  

## <span data-ttu-id="59f33-260">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="59f33-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="59f33-261">Wenn Sie windows- oder macOS verwenden, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="59f33-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="59f33-262">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="59f33-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="59f33-263">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="59f33-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Veralteter Eigenschaftenbereich im Elementtool – Neues in DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Features für das Debuggen von CSS-Rastern – Neues in DevTools (Microsoft Edge 85) | Microsoft Docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Barrierefreie Farbvorschläge im Formatvorlagenbereich – Neues in DevTools (Microsoft Edge 86) | Microsoft Docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Zuletzt ausgewähltes Element oder JavaScript-Objekt – Console Utilities API Reference | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools-| Microsoft Docs"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Leistungsanalysereferenz | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Emulation: Unterstützung des Dualbildschirmmodus – Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Aktivieren experimenteller APIs – experimentelle | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Aktivieren des Editors für Tastenkombinationen – Experimentelle | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulation: Unterstützung des Dualbildschirmmodus – Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Aktivieren der Netzwerkkonsole – Experimentelle | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Aktivieren der Quellreihenfolgeanzeige – experimentelle Features | Microsoft Docs"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Testen auf ausklappbaren und dualen Bildschirmgeräten – Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Aktivieren von experimentellen Features – experimentelle Features | Microsoft Docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "Tabelle – Konsolen-API-| Microsoft Docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Suchen Sie nicht verwendeten JavaScript- und CSS-Code auf der Registerkarte "Abdeckung" in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Überprüfen der CSS-Raster-| Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Drawer – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analysieren der Renderingleistung mit der Registerkarte "Rendern" – Referenz zu | Microsoft Docs"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Anzeigen und Debuggen von Media Player-| Microsoft Docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Filtern von Anforderungen nach Eigenschaften – Netzwerkanalysereferenz | Microsoft Docs"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Emulieren von Authenatoren und Debuggen von WebAuthn in Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Preview Channels"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  

[CR174309]: https://crbug.com/174309 "DevTools: Anpassen von Tastenkombinationen/Tastenkombinationen | Chromium-Bugs"
[CR772558]: https://crbug.com/772558 "DevTools: Aktualisieren auf die neueste Version von | Chromium-Bugs"  
[CR1034663]: https://crbug.com/1034663 "Erstellen sie ein Front-End für die WebAuthn Testing-API| Chromium-Bugs"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Chromium-Bugs"  
[CR1051466]: https://crbug.com/1051466 "Unterstützen von DEBUGGING/COEP in DevTools | Chromium-Bugs"  
[CR1073899]: https://crbug.com/1073899 "Registerkarte für berechnete Stile wird im reaktionsschnellen Modus | Chromium-Bugs"  
[CR1075732]: https://crbug.com/1075732 "DevTools-Personalisierung – Wechselregisterkarten | Chromium-Bugs"  
[CR1084673]: https://crbug.com/1084673 "DevTools: Verbessern Sie die Art und Weise, wie wir benutzerdefinierte CSS-Eigenschaften (auch bekannt) präsentieren. CSS-Variablen) und deren Werte | Chromium-Bugs"  
[CR1093687]: https://crbug.com/1093687 "Erstellen eines Tools zum Erstellen und Wiedergeben synthetischer Netzwerkanforderungen | Chromium-Bugs"  
[CR1096230]: https://crbug.com/1096230 "Gruppieren von CSS-Eigenschaften nach Kategorien im Bereich "Berechnete Formatvorlagen" | Chromium-Bugs"  
[CR1104188]: https://crbug.com/1104188 "Bei der Suche nach vollständigen URL-Adressen findet die Netzwerktoolsuche keine | Chromium-Bugs"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: Verbessern der Registerkarte "Berechnete Formatvorlagen" | Chromium-Bugs"  
[CR1120316]: https://crbug.com/1120316 "Hervorheben des schlechten Kontrasts unter "CSS-Übersicht" > Farben | Chromium Bugs"  
[CR1121141]: https://crbug.com/1121141 "Filtern nach Ressourcentyp in Netzwerkprotokollen | Chromium-Bugs"  
[CR1121312]: https://crbug.com/1121312 "Einstellungen sollten aus dem Menü "Weitere Tools" entfernt | Chromium-Bugs"  
[CR1136394]: https://crbug.com/1136394 "Flexbox-| Chromium Bugs"  
[CR1136655]: https://crbug.com/1136655 "Devtools: Lokalisierung von V2-| Chromium-Bugs"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Berichterstellungs-API-| MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1 – GoogleChrome/| GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Webauthentifizierungs-| GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Hello! | Glitch"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Postman Collection Format v2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "OpenAPI Specification | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> <span data-ttu-id="59f33-316">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59f33-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="59f33-317">Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/updates/2020/10/devtools/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="59f33-317">The original page is found [here](https://developers.google.com/web/updates/2020/10/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="59f33-319">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="59f33-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen
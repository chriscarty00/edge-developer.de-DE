---
description: Verbesserungen der Barrierefreiheit, Verwendung des devtools in anderen Sprachen und vieles mehr.
title: Neuerungen in devtools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 8f82f46cd683433a37614bcf15745e1de9f31ffb
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015468"
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

# <span data-ttu-id="f90b1-104">Neuerungen in devtools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="f90b1-104">What's new in DevTools (Microsoft Edge 80)</span></span>  

## <span data-ttu-id="f90b1-105">Ankündigungen des Microsoft Edge devtools-Teams</span><span class="sxs-lookup"><span data-stu-id="f90b1-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="f90b1-106">In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise im Microsoft Edge devtools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="f90b1-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="f90b1-107">Schauen Sie sich diese an, um neue Features in den devtools, Visual Studio-Code Erweiterungen und vieles mehr zu testen.</span><span class="sxs-lookup"><span data-stu-id="f90b1-107">Check them out to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="f90b1-108">Wenn Sie über die neuesten und besten Funktionen Ihrer Entwicklertools auf dem Laufenden bleiben möchten, laden Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] herunter und [folgen Sie uns auf Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="f90b1-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="f90b1-109">Verbesserungen der Barrierefreiheit für devtools</span><span class="sxs-lookup"><span data-stu-id="f90b1-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="f90b1-110">Das devtools-Team hat 170-Änderungen zu chromium beigetragen, um Probleme mit der Farbkontrast-, Tastatur-und Bildschirmsprachausgabe in devtools zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f90b1-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="f90b1-111">Jeder Entwickler, der das Web erstellt, sollte in der Lage sein, das devtools zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f90b1-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="Das Tool "Leistung" im devtools mit den Verbesserungen der Tastaturnavigation und der Bildschirmsprachausgabe" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="f90b1-113">Das Tool " **Leistung** " im devtools mit den Verbesserungen der Tastaturnavigation und der Bildschirmsprachausgabe</span><span class="sxs-lookup"><span data-stu-id="f90b1-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-114">Möchten Sie erfahren, wie Sie Ihre Webseite für alle Benutzer barrierefrei gestalten können?</span><span class="sxs-lookup"><span data-stu-id="f90b1-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="f90b1-115">Laden Sie die [Barrierefreiheits Einblicke][AccessibilityInsights] und [webhint][WebhintBrowserExtension] -Erweiterungen für Microsoft Edge herunter, um zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="f90b1-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="f90b1-116">Wenn Sie Bildschirmsprachausgaben oder die Tastatur verwenden, um in der devtools zu navigieren, senden Sie Ihr Feedback, indem Sie uns über [tweeten][PostTweetEdgeDevTools] oder auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) klicken.</span><span class="sxs-lookup"><span data-stu-id="f90b1-116">If you use screen readers or the keyboard to navigate around the DevTools, send your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="f90b1-117">Chrom Problem [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="f90b1-117">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="f90b1-118">Verwenden des devtools in anderen Sprachen</span><span class="sxs-lookup"><span data-stu-id="f90b1-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="f90b1-119">Viele Entwickler verwenden andere Entwicklertools wie StackOverflow und Visual Studio-Code in ihrer Muttersprache, nicht nur in Englisch.</span><span class="sxs-lookup"><span data-stu-id="f90b1-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="f90b1-120">Wir freuen uns, die Lokalisierung für das devtools bekannt zu geben, das Sie nun in einer von 10 Sprachen außer Englisch verwenden können:</span><span class="sxs-lookup"><span data-stu-id="f90b1-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="f90b1-121">Chinesisch (vereinfacht \) –  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="f90b1-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f90b1-122">Chinesisch (traditionell \) –  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="f90b1-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="f90b1-123">Französisch – Fran&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="f90b1-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f90b1-124">Deutsch-Deutsch</span><span class="sxs-lookup"><span data-stu-id="f90b1-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="f90b1-125">Italienisch-Italiano</span><span class="sxs-lookup"><span data-stu-id="f90b1-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f90b1-126">Japanisch –  &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="f90b1-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="f90b1-127">Koreanisch –  &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="f90b1-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f90b1-128">Portugiesisch-Portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="f90b1-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="f90b1-129">Russisch –  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="f90b1-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f90b1-130">Spanisch-ESPA&#241;OL</span><span class="sxs-lookup"><span data-stu-id="f90b1-130">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文（简体）| Chinese (Traditional) - 中文（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="f90b1-131">Navigieren Sie zu `edge://flags` und setzen Sie das Kennzeichen **lokalisierte Entwickler Tools aktivieren** auf **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="f90b1-131">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="f90b1-132">Setzen Sie auch das Kennzeichen **Entwickler Tools Experimente** auf **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="f90b1-132">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="f90b1-133">Starten Sie Microsoft Edge neu, und öffnen Sie das devtools.</span><span class="sxs-lookup"><span data-stu-id="f90b1-133">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="f90b1-134">Die devtools entsprechen der Sprache, in der Sie Microsoft Edge verwenden `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="f90b1-134">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="Das devtools in Deutsch" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   <span data-ttu-id="f90b1-136">Das devtools in Deutsch</span><span class="sxs-lookup"><span data-stu-id="f90b1-136">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-137">Wenn Sie das devtools in einer anderen Sprache als den verfügbaren verwenden möchten, senden Sie uns eine [Tweet][PostTweetEdgeDevTools] oder klicken Sie auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="f90b1-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="f90b1-138">Chrom Problem [#941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="f90b1-138">Chromium issue [#941561][CR941561]</span></span>  

### <span data-ttu-id="f90b1-139">webhint Microsoft Edge-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="f90b1-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="f90b1-140">Mit der webhint Microsoft Edge-Erweiterung können Sie Ihre Webseite auf einfache Weise überprüfen und Feedback zu Barrierefreiheit, Browserkompatibilität, Sicherheit, Leistung und vielem mehr in der devtools erhalten.</span><span class="sxs-lookup"><span data-stu-id="f90b1-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="f90b1-141">Weitere Informationen finden Sie unter [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="f90b1-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="Die Registerkarte "Hinweise" im devtools, wenn die webhint-Browser Erweiterung installiert ist" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   <span data-ttu-id="f90b1-143">Die Registerkarte " **Hinweise** " im devtools, wenn die webhint-Browser Erweiterung installiert ist</span><span class="sxs-lookup"><span data-stu-id="f90b1-143">The **Hints** tab in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-144">[Testen Sie die webhint-Browser Erweiterung in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="f90b1-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="f90b1-145">Nachdem Sie die Erweiterung installiert haben, öffnen Sie das devtools, und wählen Sie die Registerkarte Hinweise aus.  Führen Sie von hier aus eine anpassbare Website Überprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="f90b1-145">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="f90b1-146">Besuchen Sie [webhint.IO][WebhintBrowserExtension] , um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f90b1-146">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <span data-ttu-id="f90b1-147">3D View</span><span class="sxs-lookup"><span data-stu-id="f90b1-147">3D View</span></span>  

<span data-ttu-id="f90b1-148">Verwenden Sie die **3D-Ansicht** , um Ihre Webanwendung zu debuggen, indem Sie durch das [Dokumentobjektmodell \ (DOM \)][MDNDocumentObjectModel] oder den Stapel Kontext des [z-Index][MDNZIndex] navigieren.</span><span class="sxs-lookup"><span data-stu-id="f90b1-148">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="Die 3D-Ansicht im devtools" lightbox="../../images/2019/12/3dview.msft.png":::
   <span data-ttu-id="f90b1-150">Die **3D-Ansicht** im devtools</span><span class="sxs-lookup"><span data-stu-id="f90b1-150">The **3D View** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-151">Wenn Sie auf die 3D-Ansicht zugreifen möchten, navigieren Sie zu `edge://flags` und stellen Sie sicher, dass das Kennzeichen **Entwickler Tools Experimente** auf **aktiviert**festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="f90b1-151">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="f90b1-152">Starten Sie Microsoft Edge neu, und öffnen Sie das devtools.</span><span class="sxs-lookup"><span data-stu-id="f90b1-152">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="f90b1-153">Drücken Sie `F1` im devtools oder wechseln Sie zu **Einstellungen**, navigieren Sie zu **Experimenten** , und aktivieren Sie das Kontrollkästchen **3D-Ansicht aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="f90b1-153">Press `F1` in the DevTools or go to **Settings**, navigate to **Experiments** section, and check the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="f90b1-154">Drücken Sie jetzt `Ctrl`  +  `Shift`  +  `P` , geben Sie in **3D-Ansicht** ein, und wählen Sie **3D-Ansicht**anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="f90b1-154">Now, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="f90b1-155">Wir arbeiten an der Benutzeroberfläche und fügen der 3D-Ansicht Weitere Funktionen hinzu, damit Sie uns Ihr [Feedback](#getting-in-touch-with-microsoft-edge-devtools-team)senden können.</span><span class="sxs-lookup"><span data-stu-id="f90b1-155">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="f90b1-156">Chrom Problem [#987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="f90b1-156">Chromium issue [#987787][CR987787]</span></span>

### <span data-ttu-id="f90b1-157">Visual Studio-Code Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="f90b1-157">Visual Studio Code extensions</span></span>  

<span data-ttu-id="f90b1-158">Das devtools-Team hat auch einige Erweiterungen für [Visual Studio-Code][VisualStudioCode] veröffentlicht, mit denen Sie die Leistung des devtools direkt aus Ihrem Text-Editor verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f90b1-158">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor.</span></span> <span data-ttu-id="f90b1-159">Schauen Sie sich die folgenden Erweiterungen an.</span><span class="sxs-lookup"><span data-stu-id="f90b1-159">Check out the following extensions.</span></span>  

#### <span data-ttu-id="f90b1-160">Elemente für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f90b1-160">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="f90b1-161">Verwenden Sie das elementtool in Visual Studio-Code, indem Sie die Visual Studio-Code Erweiterung " [Elemente für Microsoft Edge (Chrom)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] " hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f90b1-161">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="Das Tool ' Elemente ' in Visual Studio-Code mit den Elementen für Microsoft Edge Extension" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   <span data-ttu-id="f90b1-163">Das Tool ' **Elemente** ' in Visual Studio-Code mit den Elementen für Microsoft Edge Extension</span><span class="sxs-lookup"><span data-stu-id="f90b1-163">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-164">Weitere Informationen finden Sie unter [Elemente für die Microsoft Edge Visual Studio-Code Erweiterung][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="f90b1-164">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="f90b1-165">Debugger für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f90b1-165">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="f90b1-166">Debuggen Sie JavaScript in Microsoft Edge direkt aus Visual Studio-Code, wenn Sie den [Debugger für Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio-Code Erweiterung ausführen.</span><span class="sxs-lookup"><span data-stu-id="f90b1-166">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="Der Debugger für Microsoft Edge Extension in Visual Studio-Code" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   <span data-ttu-id="f90b1-168">Der Debugger für Microsoft Edge Extension in Visual Studio-Code</span><span class="sxs-lookup"><span data-stu-id="f90b1-168">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-169">Weitere Informationen finden Sie unter [Debuggen von Microsoft Edge aus Visual Studio-Code][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="f90b1-169">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="f90b1-170">Webhint</span><span class="sxs-lookup"><span data-stu-id="f90b1-170">webhint</span></span>  

<span data-ttu-id="f90b1-171">Die [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio-Code Erweiterung verwendet `webhint` , um Ihre Webseite zu verbessern, während Sie Sie schreiben!</span><span class="sxs-lookup"><span data-stu-id="f90b1-171">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="f90b1-172">Mit dieser Erweiterung wird die Diagnose für Ihre Arbeitsbereichsdateien basierend auf der Analyse ausgeführt und gemeldet `webhint` .</span><span class="sxs-lookup"><span data-stu-id="f90b1-172">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="Die webhint Visual Studio-Code Erweiterung, die eine TSX-Datei in Visual Studio-Code analysiert" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="f90b1-174">Die webhint Visual Studio-Code Erweiterung, die eine `.tsx` Datei in Visual Studio-Code analysiert</span><span class="sxs-lookup"><span data-stu-id="f90b1-174">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-175">[Erfahren Sie mehr über die Visual Studio-Code webhint-Erweiterung][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="f90b1-175">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="f90b1-176">Integration von Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f90b1-176">Visual Studio integration</span></span>
<span data-ttu-id="f90b1-177">Verwenden Sie in Visual Studio 2019, Version 16,2 oder höher, den Visual Studio-Debugger zum Debuggen von JavaScript, das in Microsoft Edge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f90b1-177">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="f90b1-178">[Laden Sie Visual Studio 2019 herunter][MicrosoftVisualStudioDownloads] , um dieses Feature auszuprobieren!</span><span class="sxs-lookup"><span data-stu-id="f90b1-178">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, dev oder Beta" lightbox="../../images/2019/12/vs.msft.png":::
   <span data-ttu-id="f90b1-180">Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, dev oder Beta</span><span class="sxs-lookup"><span data-stu-id="f90b1-180">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-181">[Lesen Sie unseren Blogbeitrag, um zu erfahren, wie Sie Microsoft Edge in Visual Studio debuggen][MicrosoftVisualStudioBlogDebugJavascript]können.</span><span class="sxs-lookup"><span data-stu-id="f90b1-181">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <span data-ttu-id="f90b1-182">Nachrichten zur Präventions Konsole</span><span class="sxs-lookup"><span data-stu-id="f90b1-182">Tracking prevention Console messages</span></span>  

<span data-ttu-id="f90b1-183">Die nach Verfolgungs Verhinderung ist ein einzigartiges Feature in Microsoft Edge, das Sie davor schützt, von Websites, die Sie noch nicht besucht haben, nachverfolgt</span><span class="sxs-lookup"><span data-stu-id="f90b1-183">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="f90b1-184">Die Standardeinstellung für die nach Verfolgungs Verhinderung ist der Modus "ausgeglichen", der Drittanbieter-Tracker und bekannte bösartige Tracker für eine Erfahrung blockiert, die Datenschutz und Web-Kompatibilität abgleicht.</span><span class="sxs-lookup"><span data-stu-id="f90b1-184">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="f90b1-185">Damit Sie mehr über die Kompatibilität Ihrer Webseite erfahren, wenn bestimmte Tracker blockiert sind, haben wir auch Warnmeldungen in der Konsole hinzugefügt, wenn ein Tracker blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="f90b1-185">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Nachrichten in der Konsole, wenn die nach Verfolgungs Prävention den Zugriff auf den Speicher für einen Tracker blockiert" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   <span data-ttu-id="f90b1-187">Nachrichten in der **Konsole** , wenn die nach Verfolgungs Prävention den Zugriff auf den Speicher für einen Tracker blockiert</span><span class="sxs-lookup"><span data-stu-id="f90b1-187">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-188">[Weitere Informationen finden Sie unter Verhinderung von Nachverfolgung und dem Gleichgewichtzwischen Datenschutz und Web-Kompatibilität][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="f90b1-188">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="f90b1-189">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="f90b1-189">Announcements from the Chromium project</span></span>  

<span data-ttu-id="f90b1-190">In den folgenden Abschnitten werden weitere in Microsoft Edge 80 verfügbare Features angekündigt, die zum Open-Source-Projekt Chromium beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="f90b1-190">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="f90b1-191">Unterstützung für Let-und Class-Deklarationen in der Konsole</span><span class="sxs-lookup"><span data-stu-id="f90b1-191">Support for let and class redeclarations in the Console</span></span>  

<span data-ttu-id="f90b1-192">Die **Konsole** unterstützt jetzt erneute Deklarationen von `let` und- `class` Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="f90b1-192">The **Console** now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="f90b1-193">Die Unfähigkeit, erneut zu deklarieren, war ein häufiges Ärgernis für Webentwickler, die die Konsole zum Experimentieren mit neuem JavaScript-Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="f90b1-193">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="f90b1-194">Das erneute Deklarieren einer `let` oder `class` -Anweisung in einem Skript außerhalb der Konsole oder in einer einzelnen Konsoleneingabe führt weiterhin zu einer `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="f90b1-194">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="f90b1-195">Bei der erneuten Deklaration einer lokalen Variablen mit `let` hat die Konsole beispielsweise einen Fehler ausgelöst:</span><span class="sxs-lookup"><span data-stu-id="f90b1-195">For example, previously, when re-declaring a local variable with `let`, the Console threw an error:</span></span>  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="Die Konsole in Microsoft Edge 79 zeigt, dass die Let-erneute Deklaration fehlschlägt" lightbox="../../images/2019/12/letbefore.msft.png":::
   <span data-ttu-id="f90b1-197">Die **Konsole** in Microsoft Edge 79, die zeigt, dass die Let-erneute Deklaration fehlschlägt</span><span class="sxs-lookup"><span data-stu-id="f90b1-197">The **Console** in Microsoft Edge 79 showing that the let re-declaration fails</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-198">Die Konsole ermöglicht nun die erneute Deklaration:</span><span class="sxs-lookup"><span data-stu-id="f90b1-198">Now, the Console allows the redeclaration:</span></span>  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="Die Konsole in Microsoft Edge 80 zeigt, dass die Let-erneute Deklaration erfolgreich ist" lightbox="../../images/2019/12/letafter.msft.png":::
   <span data-ttu-id="f90b1-200">Die **Konsole** in Microsoft Edge 80 zeigt, dass die Let-erneute Deklaration erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="f90b1-200">The **Console** in Microsoft Edge 80 showing that the let re-declaration succeeds</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-201">Chrom Problem [#1004193][CR1004193]</span><span class="sxs-lookup"><span data-stu-id="f90b1-201">Chromium issue [#1004193][CR1004193]</span></span>  

### <span data-ttu-id="f90b1-202">Verbessertes Webassembly-Debugging</span><span class="sxs-lookup"><span data-stu-id="f90b1-202">Improved WebAssembly debugging</span></span>  

<span data-ttu-id="f90b1-203">DevTools hat mit der Unterstützung des [Dwarf-Debugging-Standards][DwarfHome]begonnen, was mehr Unterstützung für die schrittweise Codierung, das Festlegen von Haltepunkten und das Auflösen von Stapelablaufverfolgungen in ihren Quellsprachen in devtools bedeutet.</span><span class="sxs-lookup"><span data-stu-id="f90b1-203">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### <span data-ttu-id="f90b1-204">Netzwerk Panel-Updates</span><span class="sxs-lookup"><span data-stu-id="f90b1-204">Network panel updates</span></span>  

#### <span data-ttu-id="f90b1-205">Anfordern von Initiator-Chains auf der Registerkarte "Initiator"</span><span class="sxs-lookup"><span data-stu-id="f90b1-205">Request Initiator Chains in the Initiator tab</span></span>  

<span data-ttu-id="f90b1-206">Sie können nun die Initiatoren und Abhängigkeiten einer Netzwerkanforderung als geschachtelte Liste anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f90b1-206">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="f90b1-207">Dies kann Ihnen helfen zu verstehen, warum eine Ressource angefordert wurde, oder welche Netzwerkaktivität eine bestimmte Ressource (wie ein Skript \) verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="f90b1-207">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Eine Anforderungs Initiator-Kette auf der Registerkarte "Initiator"" lightbox="../../images/2019/12/initiators.msft.png":::
   <span data-ttu-id="f90b1-209">Eine Anforderungs Initiator-Kette auf der Registerkarte " **Initiator** "</span><span class="sxs-lookup"><span data-stu-id="f90b1-209">A Request Initiator Chain in the **Initiator** tab</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-210">Klicken Sie nach dem [Protokollieren der Netzwerkaktivität in der Netzwerksteuerung][DevToolsNetworkIndex]auf eine Ressource, und wechseln Sie dann zur Registerkarte **Initiator** , um die **Anforderungs initiatorkette**anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="f90b1-210">After [logging network activity in the Network panel][DevToolsNetworkIndex], click a resource and then go to the **Initiator** tab to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="f90b1-211">Die **geprüfte Ressource** ist fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="f90b1-211">The **inspected resource** is bold.</span></span>  <span data-ttu-id="f90b1-212">Im obigen Screenshot `ai.2.min.js` befindet sich die geprüfte Ressource.</span><span class="sxs-lookup"><span data-stu-id="f90b1-212">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="f90b1-213">Die Ressourcen oberhalb der geprüften Ressource sind die **Initiatoren**.</span><span class="sxs-lookup"><span data-stu-id="f90b1-213">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="f90b1-214">Im obigen Screenshot `https://www.microsoftedgeinsider.com` ist der Initiator von `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="f90b1-214">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="f90b1-215">Mit anderen Worten: `https://www.microsoftedgeinsider.com` Ursache für die Netzwerkanforderung `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="f90b1-215">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="f90b1-216">Die Ressourcen unterhalb der geprüften Ressource sind die **Abhängigkeiten**.</span><span class="sxs-lookup"><span data-stu-id="f90b1-216">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="f90b1-217">Im obigen Screenshot `https://dc.services.visualstudio.com/v2/track` ist eine Abhängigkeit von `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="f90b1-217">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="f90b1-218">Mit anderen Worten: `ai.2.min.js` Ursache für die Netzwerkanforderung `https://dc.services.visualstudio.com/v2/track` .</span><span class="sxs-lookup"><span data-stu-id="f90b1-218">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="f90b1-219">Auf Initiator-und Abhängigkeitsinformationen kann auch zugegriffen werden, indem Sie `Shift` auf Netzwerkressourcen halten und dann darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="f90b1-219">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="f90b1-220">Weitere Informationen finden Sie unter [Anzeigen von Initiatoren und Abhängigkeiten][DevToolsNetworkReferenceViewInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="f90b1-220">See [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="f90b1-221">Chrom Problem [#842488][CR842488]</span><span class="sxs-lookup"><span data-stu-id="f90b1-221">Chromium issue [#842488][CR842488]</span></span>  

#### <span data-ttu-id="f90b1-222">Markieren der ausgewählten Netzwerkanforderung in der Übersicht</span><span class="sxs-lookup"><span data-stu-id="f90b1-222">Highlight the selected network request in the Overview</span></span>  

<span data-ttu-id="f90b1-223">Nachdem Sie auf eine Netzwerkressource klicken, um Sie zu überprüfen, fügt das Netzwerk Panel nun einen blauen Rahmen um die Ressource in der **Übersicht**ein.</span><span class="sxs-lookup"><span data-stu-id="f90b1-223">After you click a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="f90b1-224">Dies kann Ihnen helfen zu erkennen, ob die Netzwerkanforderung früher oder später als erwartet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f90b1-224">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="Der Übersichtsbereich, der die überprüfte Ressource markiert" lightbox="../../images/2019/12/overview.msft.png":::
   <span data-ttu-id="f90b1-226">Der Übersichtsbereich, der die **über** prüfte Ressource markiert</span><span class="sxs-lookup"><span data-stu-id="f90b1-226">The **Overview** pane highlighting the inspected resource</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-227">Chrom Problem [#988253][CR988253]</span><span class="sxs-lookup"><span data-stu-id="f90b1-227">Chromium issue [#988253][CR988253]</span></span>  

#### <span data-ttu-id="f90b1-228">URL-und Pfad Spalten im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="f90b1-228">URL and path columns in the Network panel</span></span>  

<span data-ttu-id="f90b1-229">Verwenden Sie die Spalten neuer **Pfad** und **URL** im **Netzwerk** Panel, um den absoluten Pfad oder die vollständige URL der einzelnen Netzwerkressourcen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f90b1-229">Use the new **Path** and **URL** columns in the **Network** panel to see the absolute path or full URL of each network resource.</span></span>  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="Die Spalten ' neuer Pfad ' und ' URL ' im Netzwerk Panel" lightbox="../../images/2019/12/columns.msft.png":::
   <span data-ttu-id="f90b1-231">Die Spalten ' neuer Pfad ' und ' URL ' im **Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="f90b1-231">The new Path and URL columns in the **Network** panel</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-232">Klicken Sie mit der rechten Maustaste auf die Tabelle Überschrift **Wasserfall** , und wählen Sie **Pfad** oder **URL** aus, um die neuen Spalten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f90b1-232">Right-click the **Waterfall** table header and select **Path** or **URL** to show the new columns.</span></span>  

<span data-ttu-id="f90b1-233">Chrom Problem [#993366][CR993366]</span><span class="sxs-lookup"><span data-stu-id="f90b1-233">Chromium issue [#993366][CR993366]</span></span>  

#### <span data-ttu-id="f90b1-234">Aktualisierte Benutzer-Agent-Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="f90b1-234">Updated User-Agent strings</span></span>  

<span data-ttu-id="f90b1-235">DevTools unterstützt das Festlegen einer benutzerdefinierten Benutzer-Agent-Zeichenfolge über die Registerkarte **Netzwerkbedingungen** .  Die Benutzer-Agent-Zeichenfolge wirkt `User-Agent` sich auf den an Netzwerkressourcen angefügten HTTP-Header und auch auf den Wert von aus `navigator.userAgent` .</span><span class="sxs-lookup"><span data-stu-id="f90b1-235">DevTools supports setting a custom User-Agent string through the **Network Conditions** tab.  The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="f90b1-236">Die vordefinierten Benutzer-Agent-Zeichenfolgen wurden so aktualisiert, dass Sie den modernen Browserversionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f90b1-236">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="Das Menü "Benutzer-Agent" auf der Registerkarte "Netzwerkbedingungen"" lightbox="../../images/2019/12/useragent.msft.png":::
   <span data-ttu-id="f90b1-238">Das Menü "Benutzer-Agent" auf der Registerkarte " **Netzwerkbedingungen** "</span><span class="sxs-lookup"><span data-stu-id="f90b1-238">The User Agent menu in the **Network Conditions** tab</span></span>  
:::image-end:::  

<span data-ttu-id="f90b1-239">Um auf **Netzwerkbedingungen**zuzugreifen, [Öffnen Sie das Befehlsmenü][DevToolsCommandMenuIndex] , und führen Sie den `Show Network Conditions` Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="f90b1-239">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="f90b1-240">Sie können auch [Benutzer-Agent-Zeichenfolgen im Gerätemodus einrichten][DevToolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="f90b1-240">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="f90b1-241">Chrom Problem [#1029031][CR1029031]</span><span class="sxs-lookup"><span data-stu-id="f90b1-241">Chromium issue [#1029031][CR1029031]</span></span>  

### <span data-ttu-id="f90b1-242">Audits-Panel-Updates</span><span class="sxs-lookup"><span data-stu-id="f90b1-242">Audits panel updates</span></span>  

#### <span data-ttu-id="f90b1-243">Neue Konfigurations-UI</span><span class="sxs-lookup"><span data-stu-id="f90b1-243">New configuration UI</span></span>  

<span data-ttu-id="f90b1-244">Die Benutzeroberfläche der Konfiguration verfügt über ein neues, reaktionsfähiges Design, und die Optionen für die Einschränkungs Konfiguration wurden vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="f90b1-244">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="f90b1-245">Weitere Informationen zu den Änderungen beim Einschränken der Benutzeroberfläche finden Sie unter [Drosselung des Überwachungs Panels][GitHubGoogleChromeDevToolsAuditsPanelThrottling] .</span><span class="sxs-lookup"><span data-stu-id="f90b1-245">See [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling] for more information on the throttling UI changes.</span></span>  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="Die neue Benutzeroberfläche für die Konfiguration" lightbox="../../images/2019/12/start.msft.png":::
   <span data-ttu-id="f90b1-247">Die neue Benutzeroberfläche für die Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f90b1-247">The new configuration UI</span></span>  
:::image-end:::  

### <span data-ttu-id="f90b1-248">Updates für Coverage-Registerkarten</span><span class="sxs-lookup"><span data-stu-id="f90b1-248">Coverage tab updates</span></span>  

#### <span data-ttu-id="f90b1-249">Pro-Funktion-oder pro-Block-Abdeckungs Modi</span><span class="sxs-lookup"><span data-stu-id="f90b1-249">Per-function or per-block coverage modes</span></span>  

<span data-ttu-id="f90b1-250">Die [Registerkarte Coverage][DevToolsCoverageIndex] enthält ein neues Dropdownmenü, in dem Sie angeben können, ob Codeabdeckungsdaten **pro Funktion** oder **pro Block**erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f90b1-250">The [Coverage tab][DevToolsCoverageIndex] has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="f90b1-251">**Pro-Block** -Abdeckung ist detaillierter, aber auch weitaus teurer zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="f90b1-251">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="f90b1-252">DevTools verwendet jetzt standardmäßig **pro Funktion** Coverage.</span><span class="sxs-lookup"><span data-stu-id="f90b1-252">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="f90b1-253">Je nachdem, ob Sie **pro Funktion** oder **pro Block** Modus verwenden, werden möglicherweise große Unterschiede bei der Codeabdeckung in HTML-Dateien angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f90b1-253">You may see large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="f90b1-254">Bei Verwendung des **pro-Funktions** Modus werden Inlineskripts in HTML-Dateien als Funktionen behandelt.</span><span class="sxs-lookup"><span data-stu-id="f90b1-254">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="f90b1-255">Wenn das Skript überhaupt ausgeführt wird, markiert devtools das gesamte Skript als verwendeten Code.</span><span class="sxs-lookup"><span data-stu-id="f90b1-255">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="f90b1-256">Nur wenn das Skript überhaupt nicht ausgeführt wird, kennzeichnet devtools das Skript als unbenutzten Code.</span><span class="sxs-lookup"><span data-stu-id="f90b1-256">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="Dropdownmenü "Coverage-Modus"" lightbox="../../images/2019/12/modes.msft.png":::
   <span data-ttu-id="f90b1-258">Dropdownmenü "Coverage-Modus"</span><span class="sxs-lookup"><span data-stu-id="f90b1-258">The coverage mode dropdown menu</span></span>  
:::image-end:::  

#### <span data-ttu-id="f90b1-259">Coverage muss nun durch ein Seiten-Reload initiiert werden</span><span class="sxs-lookup"><span data-stu-id="f90b1-259">Coverage must now be initiated by a page reload</span></span>  

<span data-ttu-id="f90b1-260">Das Umschalten der Codeabdeckung ohne das erneute Laden einer Seite wurde entfernt, da die Abdeckungsdaten unzuverlässig waren.</span><span class="sxs-lookup"><span data-stu-id="f90b1-260">Toggling code coverage without a page reload has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="f90b1-261">Beispielsweise kann eine Funktion als unbenutzt gemeldet werden, wenn die Laufzeit vor langer Zeit war und der V8-Garbage Collector Sie bereinigt hat.</span><span class="sxs-lookup"><span data-stu-id="f90b1-261">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="f90b1-262">Chrom Problem [#1004203][CR1004203]</span><span class="sxs-lookup"><span data-stu-id="f90b1-262">Chromium issue [#1004203][CR1004203]</span></span>  

## <span data-ttu-id="f90b1-263">Herunterladen der Microsoft Edge Preview-Kanäle</span><span class="sxs-lookup"><span data-stu-id="f90b1-263">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="f90b1-264">Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="f90b1-264">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="f90b1-265">Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="f90b1-265">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="f90b1-266">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="f90b1-266">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!--<<../../_shared/devtools-feedback.md>> -->

<!--<<../../_shared/canary.md>> -->

<!--<<../../_shared/discover.md>> -->

<!-- image links -->  

<!--[../../images/2019/12/wasm.msft.png]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevToolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Suchen Sie ungenutzten JavaScript-und CSS-Code mit der Registerkarte Coverage in Microsoft Edge devtools | Microsoft docs"  
[DevToolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simulieren eines mobilen Viewports – simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools | Microsoft docs"  
[DevToolsNetworkIndex]: /microsoft-edge/devtools-guide-chromium/network/index "Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#view-initiators-and-dependencies "Anzeigen von Initiatoren und Abhängigkeiten – Netzwerkanalyse Referenz | Microsoft docs"  
[DevGuideEdgeHtmlWhatsNew]: /microsoft-edge/dev-guide/whats-new "Neuerungen in EdgeHTML | Microsoft docs"  
[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Debugger für Microsoft Edge Visual Studio-Code Erweiterung | Microsoft docs"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Elemente für Microsoft Edge Visual Studio-Code Erweiterung | Microsoft docs"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Hinzufügen des Felds "Initiator" zur Registerkarte "Überschriften" | Chrom Fehler"  
[CR988253]: https://crbug.com/988253 "Fehler devtools-keine Zuordnung zwischen Netzwerkanforderung und Zeitachsendiagramm | Chrom Fehler"  
[CR993366]: https://crbug.com/993366 "Bitte zeigen Sie den Pfad Teil der URL in der Liste der Netzwerk Panel-Anfragen an | Chrom Fehler"  
[CR1004193]: https://crbug.com/1004193 "REPL-Modus für V8 | Chrom Fehler"  
[CR1004203]: https://crbug.com/1004203 "Erstellen von Code Coverage awesome | Chrom Fehler"  
[CR1029031]: https://crbug.com/1029031 "UA-Zeichenfolgen werden veraltet | Chrom Fehler" 
[CR963183]: https://crbug.com/963183 "DevTools sind nicht WCAG-kompatibel | Chrom Fehler"
[CR941561]: https://crbug.com/941561 "Lokalisierbarkeit der devtools | Chrom Fehler"
[CR987787]: https://crbug.com/987787 "Dom 3D-Ansicht | Chrom Fehler"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Einblicke in die Barrierefreiheit"  

[DwarfHome]: https://dwarfstd.org "Zwerge-Startseite"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "DevTools ' Audits Panel Drosselung-GoogleChrome/Lighthouse | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Neues Problem – MicrosoftDocs/Edge – Entwickler"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Preview-Kanäle"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider-Addons"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Debuggen von JavaScript in Microsoft Edge in Visual Studio | Visual Studio-Blog"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Herunterladen von Visual Studio 2019 für Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Dokumentobjektmodell (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Einen Tweet Posten"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools Twitter-Konto"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio-Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Debugger für Microsoft Edge – Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elemente für Microsoft Edge \ (Chrom \) – Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint – Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint-Browser Erweiterung | webhint-Dokumentation"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio-Code Erweiterung | webhint-Dokumentation"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Verbessern der nach Verfolgungs Vorbeugung in Microsoft Edge-Blogbeitrag"
[TheWebWeWant]: https://aka.ms/webwewant "Das gewünschte Web"

> [!NOTE]
> <span data-ttu-id="f90b1-306">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f90b1-306">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f90b1-307">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/updates/2019/12/devtools/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="f90b1-307">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="f90b1-309">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f90b1-309">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

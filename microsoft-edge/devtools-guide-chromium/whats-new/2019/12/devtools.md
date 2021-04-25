---
description: Verbesserungen bei der Barrierefreiheit mithilfe der DevTools in anderen Sprachen und mehr.
title: Neues in DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 1388cbf62bd341837d92c51ad137f3909e60e476
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514396"
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
# <a name="whats-new-in-devtools-microsoft-edge-80"></a><span data-ttu-id="4122c-104">Neues in DevTools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="4122c-104">What's new in DevTools (Microsoft Edge 80)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4122c-105">Ankündigungen des Microsoft Edge DevTools-Teams</span><span class="sxs-lookup"><span data-stu-id="4122c-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="4122c-106">Die folgenden Abschnitte sind eine Liste der Ankündigungen, die Sie möglicherweise vom Microsoft Edge DevTools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="4122c-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="4122c-107">Sehen Sie sich die Ankündigungen an, um neue Features in devTools, Microsoft Visual Studio Codeerweiterungen zu testen und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="4122c-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="4122c-108">Laden Sie die Microsoft Edge-Vorschaukanäle herunter, und folgen [][MicrosoftEdgePreviewChannels] Sie uns [auf Twitter,][EdgeDevToolsTwitterAccount]um über die neuesten und besten Features in Ihren Entwicklertools auf dem neuesten Stand zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="4122c-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="accessibility-improvements-to-the-devtools"></a><span data-ttu-id="4122c-109">Verbesserungen bei der Barrierefreiheit der DevTools</span><span class="sxs-lookup"><span data-stu-id="4122c-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="4122c-110">Das DevTools-Team hat 170 Änderungen an Chromium vorgenommen, um probleme mit hohem Farbkontrast, Tastatur und Bildschirmleseprogramm in den DevTools zu beheben.</span><span class="sxs-lookup"><span data-stu-id="4122c-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="4122c-111">Jeder Entwickler, der das Web aufbaut, sollte die DevTools verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4122c-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="Das Leistungstool in den DevTools mit verbesserungen bei der Tastaturnavigation und der Bildschirmleseausgabe" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="4122c-113">Das **Leistungstool** in den DevTools mit verbesserungen bei der Tastaturnavigation und der Bildschirmleseausgabe</span><span class="sxs-lookup"><span data-stu-id="4122c-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-114">Möchten Sie erfahren, wie Sie ihre Webseite für alle Benutzer zugänglich machen?</span><span class="sxs-lookup"><span data-stu-id="4122c-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="4122c-115">Laden Sie [die Accessibility Insights-][AccessibilityInsights] und [Webhint-Erweiterungen][WebhintBrowserExtension] für Microsoft Edge herunter, um zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="4122c-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="4122c-116">Wenn Sie Bildschirmlesegeräte oder die Tastatur verwenden, um [][PostTweetEdgeDevTools] die DevTools zu navigieren, senden Sie Ihr Feedback, indem Sie an uns twittern oder das Symbol Feedback [senden](#getting-in-touch-with-microsoft-edge-devtools-team) drücken!</span><span class="sxs-lookup"><span data-stu-id="4122c-116">If you use screen readers or the keyboard to navigate around the DevTools, send your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="4122c-117">[Chromium-#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="4122c-117">Chromium issue [#963183][CR963183]</span></span>  

### <a name="using-the-devtools-in-other-languages"></a><span data-ttu-id="4122c-118">Verwenden der DevTools in anderen Sprachen</span><span class="sxs-lookup"><span data-stu-id="4122c-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="4122c-119">Viele Entwickler verwenden andere Entwicklertools, z. B. StackOverflow und Visual Studio Code, in ihrer Sprache, nicht nur in Englisch.</span><span class="sxs-lookup"><span data-stu-id="4122c-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="4122c-120">Wir freuen uns, die Lokalisierung für die DevTools ankündigen zu können, die Sie jetzt in einer von 10 Sprachen neben Englisch verwenden können:</span><span class="sxs-lookup"><span data-stu-id="4122c-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="4122c-121">Chinesisch \(Vereinfacht\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="4122c-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4122c-122">Chinesisch \(Traditionell\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="4122c-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="4122c-123">Französisch – fran&#231;ais</span><span class="sxs-lookup"><span data-stu-id="4122c-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4122c-124">Deutsch – deutsch</span><span class="sxs-lookup"><span data-stu-id="4122c-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="4122c-125">Italienisch - italiano</span><span class="sxs-lookup"><span data-stu-id="4122c-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4122c-126">Japanisch - &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="4122c-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="4122c-127">Koreanisch - &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="4122c-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4122c-128">Portugiesisch – portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="4122c-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="4122c-129">Russisch – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="4122c-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4122c-130">Spanisch – espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="4122c-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="4122c-131">Navigieren Sie `edge://flags` zu, und legen Sie das **Flag Lokalisierte Entwicklertools aktivieren auf** Aktiviert **.**</span><span class="sxs-lookup"><span data-stu-id="4122c-131">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="4122c-132">Legen Sie außerdem das **Experiment-Flag Für Entwicklertools** auf **Aktiviert festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="4122c-132">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="4122c-133">Starten Sie Microsoft Edge neu, und öffnen Sie die DevTools.</span><span class="sxs-lookup"><span data-stu-id="4122c-133">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Select `F1` in the DevTools or navigate to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="4122c-134">Die DevTools entsprechen der Sprache, die Sie für Microsoft Edge in `edge://settings/languages` verwenden.</span><span class="sxs-lookup"><span data-stu-id="4122c-134">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="Die DevTools auf Deutsch" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   <span data-ttu-id="4122c-136">Die DevTools auf Deutsch</span><span class="sxs-lookup"><span data-stu-id="4122c-136">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-137">Wenn Sie devTools in einer anderen Sprache als die verfügbaren verwenden [möchten,][PostTweetEdgeDevTools] twittern Sie bei uns, oder wählen Sie das Symbol Feedback [senden](#getting-in-touch-with-microsoft-edge-devtools-team) aus.</span><span class="sxs-lookup"><span data-stu-id="4122c-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or choose the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="4122c-138">[Chromium-Problem #941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="4122c-138">Chromium issue [#941561][CR941561]</span></span>  

### <a name="webhint-microsoft-edge-extension"></a><span data-ttu-id="4122c-139">webhint Microsoft Edge-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="4122c-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="4122c-140">Mit der Webhint Microsoft Edge-Erweiterung können Sie Ihre Webseite ganz einfach überprüfen und Feedback zu Barrierefreiheit, Browserkompatibilität, Sicherheit, Leistung und mehr innerhalb der DevTools erhalten.</span><span class="sxs-lookup"><span data-stu-id="4122c-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="4122c-141">Weitere Informationen finden Sie unter [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="4122c-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="Das Hints-Tool in devTools, wenn die Webhint-Browsererweiterung installiert ist" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   <span data-ttu-id="4122c-143">Das **Hints-Tool** in devTools, wenn die Webhint-Browsererweiterung installiert ist</span><span class="sxs-lookup"><span data-stu-id="4122c-143">The **Hints** tool in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-144">[Testen Sie die Webhint-Browsererweiterung in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="4122c-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="4122c-145">Öffnen Sie nach der Installation der Erweiterung die DevTools, und wählen Sie das **Hints-Tool** aus.</span><span class="sxs-lookup"><span data-stu-id="4122c-145">Once you install the extension, open the DevTools and choose the **Hints** tool.</span></span>  <span data-ttu-id="4122c-146">Führen Sie von hier aus eine anpassbare Websitescan aus.</span><span class="sxs-lookup"><span data-stu-id="4122c-146">From here, run a customizable site scan.</span></span>  <span data-ttu-id="4122c-147">Weitere Informationen finden [Webhint.io][WebhintBrowserExtension] sie.</span><span class="sxs-lookup"><span data-stu-id="4122c-147">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <a name="3d-view"></a><span data-ttu-id="4122c-148">3D View</span><span class="sxs-lookup"><span data-stu-id="4122c-148">3D View</span></span>  

<span data-ttu-id="4122c-149">Verwenden Sie **die 3D-Ansicht,** um Ihre Webanwendung zu debuggen, indem Sie durch das [Dokumentobjektmodell \(DOM\)][MDNDocumentObjectModel] oder den [Z-Index-Stapelkontext][MDNZIndex] navigieren.</span><span class="sxs-lookup"><span data-stu-id="4122c-149">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="Die 3D-Ansicht in den DevTools" lightbox="../../images/2019/12/3dview.msft.png":::
   <span data-ttu-id="4122c-151">Die **3D-Ansicht** in den DevTools</span><span class="sxs-lookup"><span data-stu-id="4122c-151">The **3D View** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-152">Um auf die 3D-Ansicht zu zugreifen, navigieren Sie zu und stellen Sie sicher, dass das Experiment-Flag `edge://flags` **entwicklertools** auf **Aktiviert festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="4122c-152">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="4122c-153">Starten Sie Microsoft Edge neu, und öffnen Sie die DevTools.</span><span class="sxs-lookup"><span data-stu-id="4122c-153">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="4122c-154">Wählen `F1` Sie im Abschnitt DevTools aus, oder öffnen Sie den Abschnitt **Einstellungen**  >  **Experimente,** und aktivieren Sie das **Kontrollkästchen 3D-Ansicht** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4122c-154">Select `F1` in the DevTools or open the **Settings** > **Experiments** section, and turn on the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="4122c-155">Wählen Sie jetzt `Ctrl`  +  `Shift`  +  `P` , geben Sie in **3D-Ansicht ein,** und wählen **Sie 3D-Ansicht anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="4122c-155">Now, select `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="4122c-156">Wir arbeiten an der Benutzeroberfläche und fügen der 3D-Ansicht weitere Funktionen hinzu, senden Sie uns ihr [Feedback.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="4122c-156">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="4122c-157">[Chromium-#987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="4122c-157">Chromium issue [#987787][CR987787]</span></span>

### <a name="visual-studio-code-extensions"></a><span data-ttu-id="4122c-158">Visual Studio Codeerweiterungen</span><span class="sxs-lookup"><span data-stu-id="4122c-158">Visual Studio Code extensions</span></span>  

<span data-ttu-id="4122c-159">Das DevTools-Team hat auch einige Erweiterungen für Visual Studio [Code][VisualStudioCode] veröffentlicht, mit derEnt nen Sie die Leistung der DevTools direkt aus Ihrem Text-Editor nutzen können.</span><span class="sxs-lookup"><span data-stu-id="4122c-159">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor.</span></span> <span data-ttu-id="4122c-160">Sehen Sie sich die folgenden Erweiterungen an.</span><span class="sxs-lookup"><span data-stu-id="4122c-160">Check out the following extensions.</span></span>  

#### <a name="elements-for-microsoft-edge"></a><span data-ttu-id="4122c-161">Elemente für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4122c-161">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="4122c-162">Verwenden Sie das Element-Tool aus Visual Studio Code, indem Sie die [Erweiterung Elemente für Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio code hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4122c-162">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="Das Elementtool in Visual Studio Code mithilfe der Erweiterung Elemente für Microsoft Edge" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   <span data-ttu-id="4122c-164">Das **Elementtool** in Visual Studio Code mithilfe der Erweiterung Elemente für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4122c-164">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-165">Weitere Informationen finden Sie unter [Elemente für Microsoft Edge Visual Studio Codeerweiterung][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="4122c-165">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <a name="debugger-for-microsoft-edge"></a><span data-ttu-id="4122c-166">Debugger für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4122c-166">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="4122c-167">Mit dem [Debugger für Microsoft Edge Visual Studio][VisualStudioMarketplaceDebuggerEdge] Codeerweiterung debuggen Sie JavaScript, das in Microsoft Edge ausgeführt wird, direkt aus Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="4122c-167">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="Debugger für Microsoft Edge Extension in Visual Studio Code" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   <span data-ttu-id="4122c-169">Debugger für Microsoft Edge Extension in Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="4122c-169">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-170">Weitere Informationen finden Sie unter [Debuggen von Microsoft Edge aus Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="4122c-170">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <a name="webhint"></a><span data-ttu-id="4122c-171">Webhint</span><span class="sxs-lookup"><span data-stu-id="4122c-171">webhint</span></span>  

<span data-ttu-id="4122c-172">Die [Webhint Visual Studio][VisualStudioMarketplaceWebhintExtension] Codeerweiterung verwendet, um Ihre Webseite zu verbessern, während Sie sie `webhint` schreiben!</span><span class="sxs-lookup"><span data-stu-id="4122c-172">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="4122c-173">Diese Erweiterung wird ausgeführt und meldet Diagnosen für Ihre Arbeitsbereichsdateien basierend auf `webhint` der Analyse.</span><span class="sxs-lookup"><span data-stu-id="4122c-173">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="Das webhint Visual Studio Codeerweiterung, die eine .tsx-Datei in Visual Studio Code analysiert" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="4122c-175">Das webhint Visual Studio Codeerweiterung, die eine Datei `.tsx` in Visual Studio Code analysiert</span><span class="sxs-lookup"><span data-stu-id="4122c-175">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-176">[Erfahren Sie mehr über die Visual Studio Code-Webhint-Erweiterung][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="4122c-176">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <a name="visual-studio-integration"></a><span data-ttu-id="4122c-177">Visual Studio Integration</span><span class="sxs-lookup"><span data-stu-id="4122c-177">Visual Studio integration</span></span>  

<span data-ttu-id="4122c-178">Verwenden Visual Studio 2019, Version 16.2 oder höher, den Visual Studio-Debugger, um JavaScript zu debuggen, das in Microsoft Edge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4122c-178">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="4122c-179">[Laden Visual Studio 2019 herunter,][MicrosoftVisualStudioDownloads] um dieses Feature auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="4122c-179">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out.</span></span>  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, Dev oder Beta" lightbox="../../images/2019/12/vs.msft.png":::
   <span data-ttu-id="4122c-181">Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, Dev oder Beta</span><span class="sxs-lookup"><span data-stu-id="4122c-181">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-182">[Lesen Sie unseren Blogbeitrag, um zu erfahren, wie Sie Microsoft Edge von][MicrosoftVisualStudioBlogDebugJavascript]Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4122c-182">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <a name="tracking-prevention-console-messages"></a><span data-ttu-id="4122c-183">Nachverfolgen von Nachrichten der Verhinderungskonsole</span><span class="sxs-lookup"><span data-stu-id="4122c-183">Tracking prevention Console messages</span></span>  

<span data-ttu-id="4122c-184">Die Nachverfolgungsverhütung ist ein einzigartiges Feature in Microsoft Edge, das verhindert, dass Sie von einer Website nachverfolgt werden, bevor Sie sie besucht haben.</span><span class="sxs-lookup"><span data-stu-id="4122c-184">Tracking prevention is a unique feature in Microsoft Edge that blocks you from being tracked by a website before you visited it.</span></span>  <span data-ttu-id="4122c-185">Die Standardeinstellung für die Nachverfolgungsverhütung ist der Balanced-Modus, der Drittanbieter-Tracker und bekannte bösartige Tracker blockiert, um datenschutz- und webkompatibilität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="4122c-185">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="4122c-186">Damit Sie mehr Einblick in die Kompatibilität Ihrer Webseite erhalten, wenn bestimmte Tracker blockiert \*\*\*\* werden, hat das Microsoft Edge-Team Warnmeldungen in der Konsole hinzugefügt, wenn ein Tracker blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="4122c-186">To give you more insight into the compatibility of your web page when certain trackers are blocked, The Microsoft Edge team added warning messages in the **Console** when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Nachrichten in der Konsole beim Nachverfolgen der Verhinderung blockiert den Zugriff auf speicher für einen Tracker" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   <span data-ttu-id="4122c-188">Nachrichten in der **Konsole beim Nachverfolgen** der Verhinderung blockiert den Zugriff auf speicher für einen Tracker</span><span class="sxs-lookup"><span data-stu-id="4122c-188">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-189">[Lesen Sie mehr über die Nachverfolgung der Verhinderung und das Gleichgewicht zwischen Datenschutz und Webkompatibilität.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="4122c-189">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="4122c-190">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="4122c-190">Announcements from the Chromium project</span></span>  

<span data-ttu-id="4122c-191">In den folgenden Abschnitten werden zusätzliche Features angekündigt, die in Microsoft Edge 80 verfügbar sind und zum Open Source Chromium-Projekt beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="4122c-191">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <a name="support-for-let-and-class-redeclarations-in-the-console"></a><span data-ttu-id="4122c-192">Unterstützung von Let- und Klassen-Neudeklarationen in der Konsole</span><span class="sxs-lookup"><span data-stu-id="4122c-192">Support for let and class redeclarations in the Console</span></span>  

<span data-ttu-id="4122c-193">Die **Konsole** unterstützt jetzt Neudeklarationen von `let` und `class` Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="4122c-193">The **Console** now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="4122c-194">Die Unfähigkeit, eine erneute Deklaration zu erstellen, war für Webentwickler, die die Konsole verwenden, um mit neuem JavaScript-Code zu experimentieren, ein häufiges Unmut.</span><span class="sxs-lookup"><span data-stu-id="4122c-194">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="4122c-195">Das erneute Deklarieren einer oder einer Anweisung in einem Skript außerhalb der Konsole oder innerhalb einer einzelnen Konsoleneingabe führt `let` `class` weiterhin zu einer `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="4122c-195">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="4122c-196">Beim erneuten Deklarieren einer lokalen Variablen mit hat die Konsole beispielsweise `let` zuvor einen Fehler ausgegeben:</span><span class="sxs-lookup"><span data-stu-id="4122c-196">For example, previously, when re-declaring a local variable with `let`, the Console threw an error:</span></span>  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="Die Konsole in Microsoft Edge 79, die zeigt, dass die erneute Deklarierung fehlschlägt" lightbox="../../images/2019/12/letbefore.msft.png":::
   <span data-ttu-id="4122c-198">Die **Konsole** in Microsoft Edge 79, die zeigt, dass die erneute Deklaration fehlschlägt</span><span class="sxs-lookup"><span data-stu-id="4122c-198">The **Console** in Microsoft Edge 79 showing that the let re-declaration fails</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-199">Nun ermöglicht die Konsole die erneute Deklarierung:</span><span class="sxs-lookup"><span data-stu-id="4122c-199">Now, the Console allows the redeclaration:</span></span>  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="Die Konsole in Microsoft Edge 80, die zeigt, dass die erneute Deklarierung erfolgreich ist" lightbox="../../images/2019/12/letafter.msft.png":::
   <span data-ttu-id="4122c-201">Die **Konsole** in Microsoft Edge 80, die zeigt, dass die erneute Deklaration erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="4122c-201">The **Console** in Microsoft Edge 80 showing that the let re-declaration succeeds</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-202">[Chromium-#1004193][CR1004193]</span><span class="sxs-lookup"><span data-stu-id="4122c-202">Chromium issue [#1004193][CR1004193]</span></span>  

### <a name="improved-webassembly-debugging"></a><span data-ttu-id="4122c-203">Verbessertes WebAssembly-Debuggen</span><span class="sxs-lookup"><span data-stu-id="4122c-203">Improved WebAssembly debugging</span></span>  

<span data-ttu-id="4122c-204">DevTools hat damit begonnen, den [STANDARD FÜR DAS DEBUGGEN ZU UNTERSTÜTZEN,][DwarfHome]was bedeutet, dass mehr Unterstützung für das Schrittweise Festlegen von Code, das Festlegen von Haltepunkten und das Auflösen von Stapelverfolgungen in Ihren Quellsprachen in DevTools zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="4122c-204">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### <a name="network-panel-updates"></a><span data-ttu-id="4122c-205">Netzwerkbereichsupdates</span><span class="sxs-lookup"><span data-stu-id="4122c-205">Network panel updates</span></span>  

#### <a name="request-initiator-chains-in-the-initiator-panel"></a><span data-ttu-id="4122c-206">Anfordern von Initiatorketten im Initiatorbereich</span><span class="sxs-lookup"><span data-stu-id="4122c-206">Request Initiator Chains in the Initiator panel</span></span>  

<span data-ttu-id="4122c-207">Sie können jetzt die Initiatoren und Abhängigkeiten einer Netzwerkanforderung als geschachtelte Liste anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4122c-207">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="4122c-208">Dies hilft Ihnen möglicherweise zu verstehen, warum eine Ressource angefordert wurde oder welche Netzwerkaktivität eine bestimmte Ressource \(z. B. ein Skript\) verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="4122c-208">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Eine Anforderungsinitiatorkette im Initiatorbereich" lightbox="../../images/2019/12/initiators.msft.png":::
   <span data-ttu-id="4122c-210">Eine Anforderungsinitiatorkette im **Initiatorbereich**</span><span class="sxs-lookup"><span data-stu-id="4122c-210">A Request Initiator Chain in the **Initiator** panel</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-211">Wählen [Sie nach der][DevToolsNetworkIndex]Protokollierung der Netzwerkaktivität im Netzwerkbereich eine Ressource aus, und navigieren Sie dann zum Bereich **Initiator,** um die Anforderungsinitiatorkette **zu sehen:**</span><span class="sxs-lookup"><span data-stu-id="4122c-211">After [logging network activity in the Network panel][DevToolsNetworkIndex], choose a resource and then navigate to the **Initiator** panel to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="4122c-212">Die **überprüfte Ressource ist** fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="4122c-212">The **inspected resource** is bold.</span></span>  <span data-ttu-id="4122c-213">Im obigen Screenshot `ai.2.min.js` ist die überprüfte Ressource.</span><span class="sxs-lookup"><span data-stu-id="4122c-213">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="4122c-214">Die Ressourcen über der überprüften Ressource sind die **Initiatoren.**</span><span class="sxs-lookup"><span data-stu-id="4122c-214">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="4122c-215">Im obigen Screenshot `https://www.microsoftedgeinsider.com` ist der Initiator von `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="4122c-215">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="4122c-216">Mit anderen Worten, `https://www.microsoftedgeinsider.com` hat die Netzwerkanforderung für `ai.2.min.js` verursacht.</span><span class="sxs-lookup"><span data-stu-id="4122c-216">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="4122c-217">Die Ressourcen unterhalb der überprüften Ressource sind **die Abhängigkeiten**.</span><span class="sxs-lookup"><span data-stu-id="4122c-217">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="4122c-218">Im obigen Screenshot `https://dc.services.visualstudio.com/v2/track` ist eine Abhängigkeit von `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="4122c-218">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="4122c-219">Mit anderen Worten, `ai.2.min.js` hat die Netzwerkanforderung für `https://dc.services.visualstudio.com/v2/track` verursacht.</span><span class="sxs-lookup"><span data-stu-id="4122c-219">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="4122c-220">Der Zugriff auf Initiator- und Abhängigkeitsinformationen kann auch durch Halten und anschließendes Zeigen `Shift` auf Netzwerkressourcen möglich sein.</span><span class="sxs-lookup"><span data-stu-id="4122c-220">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="4122c-221">Navigieren Sie zu [Initiatoren und Abhängigkeiten anzeigen.][DevToolsNetworkReferenceViewInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="4122c-221">Navigate to [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="4122c-222">[Chromium-Problem #842488][CR842488]</span><span class="sxs-lookup"><span data-stu-id="4122c-222">Chromium issue [#842488][CR842488]</span></span>  

#### <a name="highlight-the-selected-network-request-in-the-overview"></a><span data-ttu-id="4122c-223">Hervorheben der ausgewählten Netzwerkanforderung in der Übersicht</span><span class="sxs-lookup"><span data-stu-id="4122c-223">Highlight the selected network request in the Overview</span></span>  

<span data-ttu-id="4122c-224">Nachdem Sie eine Netzwerkressource zum Überprüfen der Ressource auswählen, wird im Bereich Netzwerk nun ein blauer Rahmen um diese Ressource in der **Übersicht angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="4122c-224">After you choose a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="4122c-225">Dadurch können Sie erkennen, ob die Netzwerkanforderung früher oder später als erwartet vor sich geht.</span><span class="sxs-lookup"><span data-stu-id="4122c-225">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="Der Bereich Übersicht, in dem die überprüfte Ressource hervorgehoben wird" lightbox="../../images/2019/12/overview.msft.png":::
   <span data-ttu-id="4122c-227">Der **Bereich Übersicht,** in dem die überprüfte Ressource hervorgehoben wird</span><span class="sxs-lookup"><span data-stu-id="4122c-227">The **Overview** pane highlighting the inspected resource</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-228">[Chromium-#988253][CR988253]</span><span class="sxs-lookup"><span data-stu-id="4122c-228">Chromium issue [#988253][CR988253]</span></span>  

#### <a name="url-and-path-columns-in-the-network-panel"></a><span data-ttu-id="4122c-229">URL- und Pfadspalten im Netzwerkbereich</span><span class="sxs-lookup"><span data-stu-id="4122c-229">URL and path columns in the Network panel</span></span>  

<span data-ttu-id="4122c-230">Verwenden Sie die neuen **Pfad-** und **URL-Spalten** im **Netzwerktool,** um den absoluten Pfad oder die vollständige URL jeder Netzwerkressource anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4122c-230">Use the new **Path** and **URL** columns in the **Network** tool to display the absolute path or full URL of each network resource.</span></span>  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="Die neuen Pfad- und URL-Spalten im Netzwerkbereich" lightbox="../../images/2019/12/columns.msft.png":::
   <span data-ttu-id="4122c-232">Die neuen Pfad- und URL-Spalten im **Netzwerktool**</span><span class="sxs-lookup"><span data-stu-id="4122c-232">The new Path and URL columns in the **Network** tool</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-233">Um die neuen Spalten anzuzeigen, zeigen Sie auf die **Kopfzeile der Wasserfalltabelle,** öffnen Sie das Kontextmenü \(righ-click\), und wählen Sie **Pfad** oder **URL aus.**</span><span class="sxs-lookup"><span data-stu-id="4122c-233">To display the new columns, hover on the **Waterfall** table header, open the contextual menu \(righ-click\), and choose **Path** or **URL**.</span></span>  

<span data-ttu-id="4122c-234">[Chromium-#993366][CR993366]</span><span class="sxs-lookup"><span data-stu-id="4122c-234">Chromium issue [#993366][CR993366]</span></span>  

#### <a name="updated-user-agent-strings"></a><span data-ttu-id="4122c-235">Aktualisierte User-Agent Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="4122c-235">Updated User-Agent strings</span></span>  

<span data-ttu-id="4122c-236">DevTools unterstützt das Festlegen einer benutzerdefinierten User-Agent über den Bereich **Netzwerkbedingungen.**</span><span class="sxs-lookup"><span data-stu-id="4122c-236">DevTools supports setting a custom User-Agent string through the **Network Conditions** panel.</span></span>  <span data-ttu-id="4122c-237">Die User-Agent wirkt sich auf den an Netzwerkressourcen angefügten HTTP-Header und `User-Agent` auch auf den Wert von `navigator.userAgent` aus.</span><span class="sxs-lookup"><span data-stu-id="4122c-237">The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="4122c-238">Die vordefinierten User-Agent Zeichenfolgen wurden aktualisiert, um moderne Browserversionen wider zuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="4122c-238">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="Das Menü Benutzer-Agent im Bereich Netzwerkbedingungen" lightbox="../../images/2019/12/useragent.msft.png":::
   <span data-ttu-id="4122c-240">Das Menü Benutzer-Agent im Bereich **Netzwerkbedingungen**</span><span class="sxs-lookup"><span data-stu-id="4122c-240">The User Agent menu in the **Network Conditions** panel</span></span>  
:::image-end:::  

<span data-ttu-id="4122c-241">Öffnen Sie **zum Zugreifen auf**Netzwerkbedingungen das [Befehlsmenü,][DevToolsCommandMenuIndex] und führen Sie den Befehl `Show Network Conditions` aus.</span><span class="sxs-lookup"><span data-stu-id="4122c-241">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="4122c-242">Sie können auch [User-Agent zeichenfolgen im Gerätemodus festlegen.][DevToolsDeviceModeIndex]</span><span class="sxs-lookup"><span data-stu-id="4122c-242">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="4122c-243">[Chromium-#1029031][CR1029031]</span><span class="sxs-lookup"><span data-stu-id="4122c-243">Chromium issue [#1029031][CR1029031]</span></span>  

### <a name="audits-panel-updates"></a><span data-ttu-id="4122c-244">Überwachung von Panelupdates</span><span class="sxs-lookup"><span data-stu-id="4122c-244">Audits panel updates</span></span>  

#### <a name="new-configuration-ui"></a><span data-ttu-id="4122c-245">Neue Konfigurationsbenutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="4122c-245">New configuration UI</span></span>  

<span data-ttu-id="4122c-246">Die Konfigurationsbenutzeroberfläche verfügt über ein neues, reaktionsfähiges Design, und die Konfigurationsoptionen für die Einschränkung wurden vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="4122c-246">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="4122c-247">Weitere Informationen zu Den Änderungen der Einschränkungsbenutzeroberfläche finden Sie unter [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling].</span><span class="sxs-lookup"><span data-stu-id="4122c-247">For more information on the throttling UI changes, navigate to [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling].</span></span>  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="Die neue Konfigurationsbenutzeroberfläche" lightbox="../../images/2019/12/start.msft.png":::
   <span data-ttu-id="4122c-249">Die neue Konfigurationsbenutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="4122c-249">The new configuration UI</span></span>  
:::image-end:::  

### <a name="coverage-tool-updates"></a><span data-ttu-id="4122c-250">Updates des Abdeckungstools</span><span class="sxs-lookup"><span data-stu-id="4122c-250">Coverage tool updates</span></span>  

#### <a name="per-function-or-per-block-coverage-modes"></a><span data-ttu-id="4122c-251">Funktions- oder Blockabdeckungsmodi</span><span class="sxs-lookup"><span data-stu-id="4122c-251">Per-function or per-block coverage modes</span></span>  

<span data-ttu-id="4122c-252">Das [Coverage-Tool][DevToolsCoverageIndex] verfügt über ein neues Dropdownmenü, mit \*\*\*\* dem Sie angeben können, ob Codeabdeckungsdaten pro Funktion oder pro Block **erfasst werden sollen.**</span><span class="sxs-lookup"><span data-stu-id="4122c-252">The [Coverage][DevToolsCoverageIndex] tool has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="4122c-253">**Die Abdeckung pro** Block ist detaillierter, aber auch viel teurer zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="4122c-253">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="4122c-254">DevTools verwendet **jetzt standardmäßig die** Abdeckung pro Funktion.</span><span class="sxs-lookup"><span data-stu-id="4122c-254">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="4122c-255">Je nachdem, ob Sie pro Funktion oder \*\*\*\* pro Blockmodus verwenden, können Sie große Unterschiede bei der Codeabdeckung in **HTML-Dateien** feststellen.</span><span class="sxs-lookup"><span data-stu-id="4122c-255">You may notice large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="4122c-256">Bei Verwendung **pro Funktionsmodus** werden Inlineskripts in HTML-Dateien als Funktionen behandelt.</span><span class="sxs-lookup"><span data-stu-id="4122c-256">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="4122c-257">Wenn das Skript überhaupt ausgeführt wird, markiert DevTools das gesamte Skript als verwendeten Code.</span><span class="sxs-lookup"><span data-stu-id="4122c-257">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="4122c-258">Nur wenn das Skript überhaupt nicht ausgeführt wird, markieren DevTools das Skript als nicht verwendeten Code.</span><span class="sxs-lookup"><span data-stu-id="4122c-258">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="Dropdownmenü Abdeckungsmodus" lightbox="../../images/2019/12/modes.msft.png":::
   <span data-ttu-id="4122c-260">Dropdownmenü "Abdeckungsmodus"</span><span class="sxs-lookup"><span data-stu-id="4122c-260">The coverage mode dropdown menu</span></span>  
:::image-end:::  

#### <a name="coverage-must-now-be-initiated-by-a-page-refresh"></a><span data-ttu-id="4122c-261">Die Abdeckung muss jetzt durch eine Seitenaktualisierung initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="4122c-261">Coverage must now be initiated by a page refresh</span></span>  

<span data-ttu-id="4122c-262">Die Toggling-Codeabdeckung ohne Seitenaktualisierung wurde entfernt, da die Abdeckungsdaten unzuverlässig waren.</span><span class="sxs-lookup"><span data-stu-id="4122c-262">Toggling code coverage without a page refresh has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="4122c-263">Beispielsweise kann eine Funktion als nicht verwendet gemeldet werden, wenn die Laufzeit vor langer Zeit war und der V8-Garbage Collector sie bereinigt hat.</span><span class="sxs-lookup"><span data-stu-id="4122c-263">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="4122c-264">[Chromium-#1004203][CR1004203]</span><span class="sxs-lookup"><span data-stu-id="4122c-264">Chromium issue [#1004203][CR1004203]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="4122c-265">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="4122c-265">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="4122c-266">Wenn Sie unter Windows oder macOS sind, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="4122c-266">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="4122c-267">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="4122c-267">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="4122c-268">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="4122c-268">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft Docs"  
[DevToolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Suchen Sie nicht verwendeten JavaScript- und CSS-Code mit dem Coverage-Tool in Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simulieren eines mobilen Viewports – Simulieren mobiler Geräte mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsNetworkIndex]: /microsoft-edge/devtools-guide-chromium/network/index "Überprüfen der Netzwerkaktivitäten in Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#view-initiators-and-dependencies "Anzeigen von Initiatoren und Abhängigkeiten – Netzwerkanalysereferenz | Microsoft Docs"  
[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Debugger für Microsoft Edge Visual Studio Codeerweiterung | Microsoft Docs"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Elemente für Microsoft Edge Visual Studio Codeerweiterung | Microsoft Docs"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Fügen Sie das Feld Initiator der Registerkarte Kopfzeilen | Chromium-Bugs"  
[CR988253]: https://crbug.com/988253 "Bug DevTools – Keine Zuordnung zwischen Netzwerkanforderung und zeitachsendiagramm | Chromium-Bugs"  
[CR993366]: https://crbug.com/993366 "Bitte zeigen Sie den Pfadteil der URL in der Liste der Netzwerkpanelanforderungen | Chromium-Bugs"  
[CR1004193]: https://crbug.com/1004193 "REPL-Modus für V8-| Chromium-Bugs"  
[CR1004203]: https://crbug.com/1004203 "Machen Sie die Codeabdeckung | Chromium-Bugs"  
[CR1029031]: https://crbug.com/1029031 "UA-Zeichenfolgen werden veraltet | Chromium-Bugs" 
[CR963183]: https://crbug.com/963183 "DevTools sind nicht WCAG-kompatible | Chromium-Bugs"
[CR941561]: https://crbug.com/941561 "Lokalisierbarkeit der DevTools-| Chromium-Bugs"
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium-Bugs"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Einblicke in die Barrierefreiheit"  

[DwarfHome]: https://dwarfstd.org "Heim der Zwerge"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "DevTools' Audits Panel Throttling – GoogleChrome/| GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Neues Problem – MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Preview Channels"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Debuggen von JavaScript in Microsoft Edge von Visual Studio | Visual Studio Blog"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Download Visual Studio 2019 für Windows \& Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Document Object Model (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Veröffentlichen eines Tweets"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools, Twitter-Konto"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Debugger für Microsoft Edge – Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elemente für Microsoft Edge \(Chromium\) – Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint – Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint Browser Extension | Webhintdokumentation"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio Codeerweiterung | Webhintdokumentation"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Verbessern der Nachverfolgungsverhütung in Microsoft Edge-Blogbeitrag"
[TheWebWeWant]: https://aka.ms/webwewant "The Web We Want"

> [!NOTE]
> <span data-ttu-id="4122c-307">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4122c-307">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4122c-308">Die ursprüngliche Seite befindet sich [hier](https://developer.chrome.com/blog/new-in-devtools-80) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="4122c-308">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-80) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="4122c-310">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4122c-310">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

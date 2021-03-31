---
description: 3D-Ansicht, Visual Studio Integration in Microsoft Edge und vieles mehr.
title: Neues in DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 204a596e2497415eefeeb8aa819106635ff30caa
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408360"
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
# <a name="whats-new-in-devtools-microsoft-edge-81"></a><span data-ttu-id="57cf2-104">Neues in DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="57cf2-104">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="57cf2-105">Ankündigungen des Microsoft Edge DevTools-Teams</span><span class="sxs-lookup"><span data-stu-id="57cf2-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="57cf2-106">Die folgenden Abschnitte sind eine Liste der Ankündigungen, die Sie möglicherweise vom Microsoft Edge DevTools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="57cf2-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="57cf2-107">Sehen Sie sich die Ankündigungen an, um neue Features in devTools, Microsoft Visual Studio Codeerweiterungen zu testen und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="57cf2-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="57cf2-108">Laden Sie die Microsoft Edge-Vorschaukanäle herunter, und folgen [][MicrosoftEdgePreviewChannels] Sie uns [auf Twitter,][EdgeDevToolsTwitterAccount]um über die neuesten und besten Features in Ihren Entwicklertools auf dem neuesten Stand zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="57cf2-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="accessibility-improvements-to-the-devtools"></a><span data-ttu-id="57cf2-109">Verbesserungen bei der Barrierefreiheit der DevTools</span><span class="sxs-lookup"><span data-stu-id="57cf2-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="57cf2-110">Das DevTools-Team hat 170 Änderungen an Chromium vorgenommen, um probleme mit hohem Farbkontrast, Tastatur und Bildschirmleseprogramm in den DevTools zu beheben.</span><span class="sxs-lookup"><span data-stu-id="57cf2-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="57cf2-111">Jeder Entwickler, der das Web aufbaut, sollte die DevTools verwenden können.</span><span class="sxs-lookup"><span data-stu-id="57cf2-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="Das Leistungstool in den DevTools mit verbesserungen bei der Tastaturnavigation und der Bildschirmleseausgabe" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="57cf2-113">Das **Leistungstool** in den DevTools mit verbesserungen bei der Tastaturnavigation und der Bildschirmleseausgabe</span><span class="sxs-lookup"><span data-stu-id="57cf2-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-114">Möchten Sie erfahren, wie Sie ihre Webseite für alle Benutzer zugänglich machen?</span><span class="sxs-lookup"><span data-stu-id="57cf2-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="57cf2-115">Laden Sie [die Accessibility Insights-][AccessibilityInsights] und [Webhint-Erweiterungen][WebhintBrowserExtension] für Microsoft Edge herunter, um zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="57cf2-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="57cf2-116">Wenn Sie Bildschirmlesegeräte oder die Tastatur verwenden, um [][PostTweetEdgeDevTools] die DevTools zu navigieren, senden Sie uns Ihr Feedback, indem Sie an uns twittern oder das Symbol Feedback [senden](#getting-in-touch-with-microsoft-edge-devtools-team) drücken!</span><span class="sxs-lookup"><span data-stu-id="57cf2-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="57cf2-117">[Chromium-#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="57cf2-117">Chromium issue [#963183][CR963183]</span></span>  

### <a name="using-the-devtools-in-other-languages"></a><span data-ttu-id="57cf2-118">Verwenden der DevTools in anderen Sprachen</span><span class="sxs-lookup"><span data-stu-id="57cf2-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="57cf2-119">Viele Entwickler verwenden andere Entwicklertools, z. B. StackOverflow und Visual Studio Code, in ihrer Sprache, nicht nur in Englisch.</span><span class="sxs-lookup"><span data-stu-id="57cf2-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="57cf2-120">Wir freuen uns, die Lokalisierung für die DevTools ankündigen zu können, die Sie jetzt in einer von 10 Sprachen neben Englisch verwenden können:</span><span class="sxs-lookup"><span data-stu-id="57cf2-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="57cf2-121">Chinesisch \(Vereinfacht\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="57cf2-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="57cf2-122">Chinesisch \(Traditionell\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="57cf2-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="57cf2-123">Französisch – fran&#231;ais</span><span class="sxs-lookup"><span data-stu-id="57cf2-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="57cf2-124">Deutsch – deutsch</span><span class="sxs-lookup"><span data-stu-id="57cf2-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="57cf2-125">Italienisch - italiano</span><span class="sxs-lookup"><span data-stu-id="57cf2-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="57cf2-126">Japanisch - &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="57cf2-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="57cf2-127">Koreanisch - &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="57cf2-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="57cf2-128">Portugiesisch – portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="57cf2-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="57cf2-129">Russisch – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="57cf2-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="57cf2-130">Spanisch – espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="57cf2-130">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="57cf2-131">Die DevTools entsprechen automatisch der Sprache, die Sie für Microsoft Edge in `edge://settings/languages` verwenden.</span><span class="sxs-lookup"><span data-stu-id="57cf2-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="57cf2-132">Wenn Microsoft Edge in einer Sprache sein soll und Ihre DevTools auf Englisch bleiben sollen, wählen Sie in devTools aus, um Einstellungen zu öffnen und Die Browsersprache `F1` **übereinstimmen zu deaktivieren.** [][Settings]</span><span class="sxs-lookup"><span data-stu-id="57cf2-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, select `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="Die DevTools auf Deutsch" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   <span data-ttu-id="57cf2-134">Die DevTools auf Deutsch</span><span class="sxs-lookup"><span data-stu-id="57cf2-134">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-135">**Konsolennachrichten** werden nicht lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="57cf2-135">**Console** messages are not localized.</span></span>  <span data-ttu-id="57cf2-136">Nur die zeichenfolgen, die in der DevTools-Benutzeroberfläche verwendet werden, werden in der Sprache angezeigt, die Sie für Microsoft Edge verwenden.</span><span class="sxs-lookup"><span data-stu-id="57cf2-136">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="57cf2-137">Wenn Sie devTools in einer anderen Sprache als die verfügbaren verwenden [möchten,][PostTweetEdgeDevTools] twittern Sie bei uns, oder wählen Sie das Symbol Feedback [senden](#getting-in-touch-with-microsoft-edge-devtools-team) aus.</span><span class="sxs-lookup"><span data-stu-id="57cf2-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or choose the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="57cf2-138">[Chromium-Problem #941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="57cf2-138">Chromium issue [#941561][CR941561]</span></span>  

### <a name="webhint-microsoft-edge-extension"></a><span data-ttu-id="57cf2-139">webhint Microsoft Edge-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="57cf2-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="57cf2-140">Mit der Webhint Microsoft Edge-Erweiterung können Sie Ihre Webseite ganz einfach überprüfen und Feedback zu Barrierefreiheit, Browserkompatibilität, Sicherheit, Leistung und mehr innerhalb der DevTools erhalten.</span><span class="sxs-lookup"><span data-stu-id="57cf2-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="57cf2-141">Weitere Informationen finden Sie unter [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="57cf2-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="Das Hints-Tool in devTools, wenn die Webhint-Browsererweiterung installiert ist" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   <span data-ttu-id="57cf2-143">Das **Hints-Tool** in devTools, wenn die Webhint-Browsererweiterung installiert ist</span><span class="sxs-lookup"><span data-stu-id="57cf2-143">The **Hints** tool in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-144">[Testen Sie die Webhint-Browsererweiterung in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="57cf2-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="57cf2-145">Öffnen Sie nach der Installation der Erweiterung die DevTools, und wählen Sie das **Hints-Tool** aus.</span><span class="sxs-lookup"><span data-stu-id="57cf2-145">Once you install the extension, open the DevTools and choose the **Hints** tool.</span></span>  <span data-ttu-id="57cf2-146">Führen Sie von hier aus eine anpassbare Websitescan aus.</span><span class="sxs-lookup"><span data-stu-id="57cf2-146">From here, run a customizable site scan.</span></span>  <span data-ttu-id="57cf2-147">Weitere Informationen finden [Webhint.io][WebhintBrowserExtension] sie.</span><span class="sxs-lookup"><span data-stu-id="57cf2-147">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <a name="3d-view"></a><span data-ttu-id="57cf2-148">3D View</span><span class="sxs-lookup"><span data-stu-id="57cf2-148">3D View</span></span>  

<span data-ttu-id="57cf2-149">Verwenden Sie **die 3D-Ansicht,** um Ihre Webanwendung zu debuggen, indem Sie durch das [Dokumentobjektmodell \(DOM\)][MDNDocumentObjectModel] oder den [Z-Index-Stapelkontext][MDNZIndex] navigieren.</span><span class="sxs-lookup"><span data-stu-id="57cf2-149">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="Die 3D-Ansicht in den DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   <span data-ttu-id="57cf2-151">Die 3D-Ansicht in den DevTools</span><span class="sxs-lookup"><span data-stu-id="57cf2-151">The 3D View in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-152">Um auf die 3D-Ansicht zu zugreifen, wählen Sie , geben `Ctrl`  +  `Shift`  +  `P` Sie in **3D-Ansicht ein,** und wählen **Sie 3D-Ansicht anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="57cf2-152">To access the 3D View, select `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="57cf2-153">Das Microsoft Edge-Team arbeitet mit dem Chromium-Team auf der Benutzeroberfläche zusammen und fügt der 3D-Ansicht weitere Funktionen hinzu. Senden Sie daher Ihr [Feedback.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="57cf2-153">The Microsoft Edge team is working with the Chromium team on the UI and adding more functionality to the 3D View, so please send your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="57cf2-154">[Chromium-#987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="57cf2-154">Chromium issue [#987787][CR987787]</span></span>  

### <a name="visual-studio-code-extensions"></a><span data-ttu-id="57cf2-155">Visual Studio Codeerweiterungen</span><span class="sxs-lookup"><span data-stu-id="57cf2-155">Visual Studio Code extensions</span></span>  

<span data-ttu-id="57cf2-156">Das DevTools-Team hat auch einige Erweiterungen für Visual Studio [Code][VisualStudioCode] veröffentlicht, mit dem Sie die Leistung der DevTools direkt aus Ihrem Text-Editor nutzen können.</span><span class="sxs-lookup"><span data-stu-id="57cf2-156">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="57cf2-157">Sehen Sie sich die folgenden Erweiterungen an:</span><span class="sxs-lookup"><span data-stu-id="57cf2-157">Check out the extensions below:</span></span>  

#### <a name="elements-for-microsoft-edge"></a><span data-ttu-id="57cf2-158">Elemente für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="57cf2-158">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="57cf2-159">Verwenden Sie das Elementtool aus Visual Studio Code, indem Sie die Erweiterung Elemente für [Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="57cf2-159">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="Das Elementtool in Visual Studio Code mithilfe der Erweiterung Elemente für Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   <span data-ttu-id="57cf2-161">Das **Elementtool** in Visual Studio Code mithilfe der Erweiterung Elemente für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="57cf2-161">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-162">Weitere Informationen finden Sie unter [Elemente für Microsoft Edge Visual Studio Codeerweiterung][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="57cf2-162">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <a name="debugger-for-microsoft-edge"></a><span data-ttu-id="57cf2-163">Debugger für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="57cf2-163">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="57cf2-164">Mit dem [Debugger für Microsoft Edge Visual Studio][VisualStudioMarketplaceDebuggerEdge] Codeerweiterung debuggen Sie JavaScript, das in Microsoft Edge ausgeführt wird, direkt aus Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="57cf2-164">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="Debugger für Microsoft Edge Extension in Visual Studio Code" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   <span data-ttu-id="57cf2-166">Debugger für Microsoft Edge Extension in Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="57cf2-166">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-167">Weitere Informationen finden Sie unter [Debuggen von Microsoft Edge aus Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="57cf2-167">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <a name="webhint"></a><span data-ttu-id="57cf2-168">Webhint</span><span class="sxs-lookup"><span data-stu-id="57cf2-168">webhint</span></span>  

<span data-ttu-id="57cf2-169">Die [Webhint Visual Studio][VisualStudioMarketplaceWebhintExtension] Codeerweiterung verwendet, um Ihre Webseite zu verbessern, während `webhint` Sie sie schreiben.</span><span class="sxs-lookup"><span data-stu-id="57cf2-169">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you are writing it.</span></span>  <span data-ttu-id="57cf2-170">Diese Erweiterung wird ausgeführt und meldet Diagnosen für Ihre Arbeitsbereichsdateien basierend auf `webhint` der Analyse.</span><span class="sxs-lookup"><span data-stu-id="57cf2-170">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="Das webhint Visual Studio Codeerweiterung, die eine .tsx-Datei in Visual Studio Code analysiert" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="57cf2-172">Das webhint Visual Studio Codeerweiterung, die eine Datei `.tsx` in Visual Studio Code analysiert</span><span class="sxs-lookup"><span data-stu-id="57cf2-172">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-173">[Erfahren Sie mehr über die Visual Studio Code-Webhint-Erweiterung][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="57cf2-173">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <a name="visual-studio-integration"></a><span data-ttu-id="57cf2-174">Visual Studio Integration</span><span class="sxs-lookup"><span data-stu-id="57cf2-174">Visual Studio integration</span></span>  

<span data-ttu-id="57cf2-175">Verwenden Visual Studio 2019, Version 16.2 oder höher, den Visual Studio-Debugger, um JavaScript zu debuggen, das in Microsoft Edge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57cf2-175">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="57cf2-176">[Laden Visual Studio 2019 herunter,][MicrosoftVisualStudioDownloads] um dieses Feature auszuprobieren!</span><span class="sxs-lookup"><span data-stu-id="57cf2-176">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, Dev oder Beta" lightbox="../../images/2020/01/vs.msft.png":::
   <span data-ttu-id="57cf2-178">Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, Dev oder Beta</span><span class="sxs-lookup"><span data-stu-id="57cf2-178">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-179">[Erfahren Sie mehr über das Debuggen von Microsoft Edge von Visual Studio.][MicrosoftVisualStudio]</span><span class="sxs-lookup"><span data-stu-id="57cf2-179">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <a name="tracking-prevention-console-messages"></a><span data-ttu-id="57cf2-180">Nachverfolgen von Nachrichten der Verhinderungskonsole</span><span class="sxs-lookup"><span data-stu-id="57cf2-180">Tracking prevention Console messages</span></span>  

<span data-ttu-id="57cf2-181">Die Nachverfolgungsverhütung ist ein einzigartiges Feature in Microsoft Edge, das Sie davor schützt, von Websites nachverfolgt zu werden, die Sie zuvor noch nicht besucht haben.</span><span class="sxs-lookup"><span data-stu-id="57cf2-181">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you have not visited before.</span></span>  <span data-ttu-id="57cf2-182">Die Standardeinstellung für die Nachverfolgungsverhütung ist der Balanced-Modus, der Drittanbieter-Tracker und bekannte bösartige Tracker blockiert, um datenschutz- und webkompatibilität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="57cf2-182">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="57cf2-183">Um Ihnen mehr Einblick in die Kompatibilität Ihrer Webseite zu geben, wenn bestimmte Tracker blockiert werden, wurden Warnmeldungen in der **Konsole** hinzugefügt, wenn ein Tracker blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="57cf2-183">To give you more insight into the compatibility of your web page when certain trackers are blocked, warning messages were added in the **Console** when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Nachrichten in der Konsole beim Nachverfolgen der Verhinderung blockiert den Zugriff auf speicher für einen Tracker" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   <span data-ttu-id="57cf2-185">Nachrichten in der **Konsole beim Nachverfolgen** der Verhinderung blockiert den Zugriff auf speicher für einen Tracker</span><span class="sxs-lookup"><span data-stu-id="57cf2-185">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-186">[Lesen Sie mehr über die Nachverfolgung der Verhinderung und das Gleichgewicht zwischen Datenschutz und Webkompatibilität.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="57cf2-186">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="57cf2-187">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="57cf2-187">Announcements from the Chromium project</span></span>  

<span data-ttu-id="57cf2-188">In den folgenden Abschnitten werden zusätzliche Features angekündigt, die in Microsoft Edge 81 verfügbar sind und zum Open Source Chromium-Projekt beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="57cf2-188">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <a name="moto-g4-support-in-device-mode"></a><span data-ttu-id="57cf2-189">Unterstützung von "Moto G4" im Gerätemodus</span><span class="sxs-lookup"><span data-stu-id="57cf2-189">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="57cf2-190">Simulieren [Sie nach dem Aktivieren der Gerätesymbolleiste][DeviceToolbar]die Dimensionen eines G4-Ansichtsports von "Moto G4" aus der **Geräteliste.**</span><span class="sxs-lookup"><span data-stu-id="57cf2-190">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Simulieren eines G4-Ansichtsports von Moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   <span data-ttu-id="57cf2-192">Simulieren eines G4-Ansichtsports von "Moto G4"</span><span class="sxs-lookup"><span data-stu-id="57cf2-192">Simulating a Moto G4 viewport</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-193">Wählen [Sie Geräterahmen anzeigen aus,][DeviceFrame] um die Hardware von "Moto G4" um den Viewport zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="57cf2-193">Choose [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Anzeigen der Hardware von Moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   <span data-ttu-id="57cf2-195">Anzeigen der Hardware von "Moto G4"</span><span class="sxs-lookup"><span data-stu-id="57cf2-195">Showing the Moto G4 hardware</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-196">Verwandte Features:</span><span class="sxs-lookup"><span data-stu-id="57cf2-196">Related features:</span></span>  

*   <span data-ttu-id="57cf2-197">Öffnen Sie [das Befehlsmenü,][CommandMenu] und führen Sie den Befehl aus, um einen Screenshot des Viewports zu erstellen, der die `Capture screenshot` Hardware von "Moto G4" enthält (nachdem Sie **Geräterahmen anzeigen aktiviert haben).**</span><span class="sxs-lookup"><span data-stu-id="57cf2-197">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="57cf2-198">[Drosseln Sie das Netzwerk und die CPU,][ThrottleNetworkAndCpu] um die Browserbedingungen eines mobilen Benutzers genauer zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="57cf2-198">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="57cf2-199">[Chromium-#924693][CR924693]</span><span class="sxs-lookup"><span data-stu-id="57cf2-199">Chromium issue [#924693][CR924693]</span></span>  

### <a name="cookie-related-updates"></a><span data-ttu-id="57cf2-200">Cookiebezogene Updates</span><span class="sxs-lookup"><span data-stu-id="57cf2-200">Cookie-related updates</span></span>  

#### <a name="blocked-cookies-in-the-cookies-pane"></a><span data-ttu-id="57cf2-201">Blockierte Cookies im Bereich Cookies</span><span class="sxs-lookup"><span data-stu-id="57cf2-201">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="57cf2-202">Im Bereich Cookies im Bereich Anwendung werden nun blockierte Cookies mit gelbem Hintergrund angezeigt.</span><span class="sxs-lookup"><span data-stu-id="57cf2-202">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Blockierte Cookies im Bereich Cookies des Anwendungsbereichs" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   <span data-ttu-id="57cf2-204">Blockierte Cookies im Bereich Cookies des Anwendungsbereichs</span><span class="sxs-lookup"><span data-stu-id="57cf2-204">Blocked cookies in the Cookies pane of the Application panel</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-205">[Chromium-#1030258][CR1030258]</span><span class="sxs-lookup"><span data-stu-id="57cf2-205">Chromium issue [#1030258][CR1030258]</span></span>  <!-- inaccessible  -->  

#### <a name="cookie-priority-in-the-cookie-pane"></a><span data-ttu-id="57cf2-206">Cookiepriorität im Cookiebereich</span><span class="sxs-lookup"><span data-stu-id="57cf2-206">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="57cf2-207">Die Cookies-Tabellen in den **Netzwerk-** und **Anwendungstools** enthalten jetzt eine **Spalte Priorität.**</span><span class="sxs-lookup"><span data-stu-id="57cf2-207">The Cookies tables in the **Network** and **Application** tools now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="57cf2-208">Chrombasierte Browser wie Microsoft Edge sind die einzigen Browser, die die Cookiepriorität unterstützen.</span><span class="sxs-lookup"><span data-stu-id="57cf2-208">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="57cf2-209">[Chromium-Problem #1026879][CR1026879]</span><span class="sxs-lookup"><span data-stu-id="57cf2-209">Chromium issue [#1026879][CR1026879]</span></span>  

#### <a name="edit-all-cookie-values"></a><span data-ttu-id="57cf2-210">Bearbeiten aller Cookiewerte</span><span class="sxs-lookup"><span data-stu-id="57cf2-210">Edit all cookie values</span></span>  

<span data-ttu-id="57cf2-211">Alle Zellen in den Cookietabellen können jetzt bearbeitet werden, mit Ausnahme von Zellen in der **Spalte Größe,** da diese Spalte die Netzwerkgröße des Cookies in Bytes darstellt.</span><span class="sxs-lookup"><span data-stu-id="57cf2-211">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="57cf2-212">Eine Erläuterung der einzelnen Spalten finden Sie unter [Fields][CookiesFields].</span><span class="sxs-lookup"><span data-stu-id="57cf2-212">For an explanation of each column, navigate to [Fields][CookiesFields].</span></span>  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Bearbeiten eines Cookiewerts" lightbox="../../images/2020/01/editcookie.msft.png":::
   <span data-ttu-id="57cf2-214">Bearbeiten eines Cookiewerts</span><span class="sxs-lookup"><span data-stu-id="57cf2-214">Editing a cookie value</span></span>  
:::image-end:::  

#### <a name="copy-as-nodejs-fetch-to-include-cookie-data"></a><span data-ttu-id="57cf2-215">Kopieren als Node.js abrufen, um Cookiedaten zu enthalten</span><span class="sxs-lookup"><span data-stu-id="57cf2-215">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="57cf2-216">Wenn Sie einen Ausdruck abrufen möchten, der Cookiedaten enthält, zeigen Sie auf eine Netzwerkanforderung, öffnen Sie das Kontextmenü \(mit der rechten Maustaste\), und wählen Sie Kopieren als Node.js `fetch`   >  **aus.**</span><span class="sxs-lookup"><span data-stu-id="57cf2-216">To get a `fetch` expression that includes cookie data, hover on a network request, open the contextual menu \(right-click\), and choose **Copy** > **Copy as Node.js fetch**.</span></span>  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Kopieren als Node.js Abrufen" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   <span data-ttu-id="57cf2-218">Kopieren als Node.js Abrufen</span><span class="sxs-lookup"><span data-stu-id="57cf2-218">Copy as Node.js fetch</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-219">[Chromium-#1029826][CR1029826]</span><span class="sxs-lookup"><span data-stu-id="57cf2-219">Chromium issue [#1029826][CR1029826]</span></span>  

### <a name="more-accurate-web-app-manifest-icons"></a><span data-ttu-id="57cf2-220">Präzisere Web-App-Manifestsymbole</span><span class="sxs-lookup"><span data-stu-id="57cf2-220">More accurate web app manifest icons</span></span>  

<span data-ttu-id="57cf2-221">Zuvor hat der Manifestbereich im Anwendungsbereich eigene Anforderungen gesendet, um Web-App-Manifestsymbole anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="57cf2-221">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="57cf2-222">DevTools zeigt nun genau dasselbe Manifestsymbol an, das Microsoft Edge verwendet.</span><span class="sxs-lookup"><span data-stu-id="57cf2-222">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Symbole im Manifestbereich" lightbox="../../images/2020/01/manifesticons.msft.png":::
   <span data-ttu-id="57cf2-224">Symbole im Manifestbereich</span><span class="sxs-lookup"><span data-stu-id="57cf2-224">Icons in the Manifest pane</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-225">[Chromium-Problem #985402][CR985402]</span><span class="sxs-lookup"><span data-stu-id="57cf2-225">Chromium issue [#985402][CR985402]</span></span>  

### <a name="hover-on-css-content-properties-to-display-unescaped-values"></a><span data-ttu-id="57cf2-226">Zeigen Sie auf CSS-Inhaltseigenschaften, um nicht dargestellte Werte anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="57cf2-226">Hover on CSS content properties to display unescaped values</span></span>  

<span data-ttu-id="57cf2-227">Zeigen Sie auf den Wert einer `content` Eigenschaft, um die nicht dargestellte Version des Werts zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="57cf2-227">Hover on the value of a `content` property to display the unescaped version of the value.</span></span>  

<span data-ttu-id="57cf2-228">In dieser Demo [][CSSContentDemo] wird beispielsweise beim Überprüfen des Pseudoelements eine escapete Zeichenfolge im Bereich `p::after` **Formatvorlagen** angezeigt:</span><span class="sxs-lookup"><span data-stu-id="57cf2-228">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element an escaped string is displayed in the **Styles** pane:</span></span>  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="Die escapete Zeichenfolge" lightbox="../../images/2020/01/escapedstring.msft.png":::
   <span data-ttu-id="57cf2-230">Die escapete Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57cf2-230">The escaped string</span></span>  
:::image-end:::  

<span data-ttu-id="57cf2-231">Wenn Sie mit dem Mauszeiger auf den Wert zeigen, wird der `content` Wert ohneScaped angezeigt.</span><span class="sxs-lookup"><span data-stu-id="57cf2-231">When you hover on the `content` value, the unescaped value is displayed.</span></span>  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="Der Nicht-Scaped-Wert" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   <span data-ttu-id="57cf2-233">Der Nicht-Scaped-Wert</span><span class="sxs-lookup"><span data-stu-id="57cf2-233">The unescaped value</span></span>  
:::image-end:::  

### <a name="more-detailed-source-map-errors-in-the-console"></a><span data-ttu-id="57cf2-234">Ausführlichere Fehler bei der Quellzuordnung in der Konsole</span><span class="sxs-lookup"><span data-stu-id="57cf2-234">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="57cf2-235">Die Konsole bietet nun ausführlichere Informationen dazu, warum eine Quellzuordnung nicht geladen oder analysiert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="57cf2-235">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="57cf2-236">Zuvor hat sie lediglich einen Fehler bereitgestellt, ohne zu erläutern, was falsch gelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="57cf2-236">Previously it just provided an error without explaining what went wrong.</span></span>  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Fehler beim Laden einer Quellzuordnung in der Konsole" lightbox="../../images/2020/01/sourcemap.msft.png":::
   <span data-ttu-id="57cf2-238">Fehler beim Laden einer Quellzuordnung in der Konsole</span><span class="sxs-lookup"><span data-stu-id="57cf2-238">A source map loading error in the Console</span></span>  
:::image-end:::  

### <a name="setting-for-disabling-scrolling-past-the-end-of-a-file"></a><span data-ttu-id="57cf2-239">Einstellung zum Deaktivieren des Bildlaufs am Ende einer Datei</span><span class="sxs-lookup"><span data-stu-id="57cf2-239">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="57cf2-240">Öffnen [Sie Einstellungen,][Settings] und deaktivieren Sie dann **Einstellungsquellen**Zulassen des Bildlaufs am Ende der Datei, um das Standardverhalten der Benutzeroberfläche zu deaktivieren, mit dem Sie einen Bildlauf weit über das Ende einer Datei im Bereich  >    >   **Quellen** durchführen können.</span><span class="sxs-lookup"><span data-stu-id="57cf2-240">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Deaktivieren Zulassen des Bildlaufs am Ende der Datei" lightbox="../../images/2020/01/settings.msft.png":::
   <span data-ttu-id="57cf2-242">Deaktivieren Zulassen **des Bildlaufs über das Ende der Datei** in den Einstellungen</span><span class="sxs-lookup"><span data-stu-id="57cf2-242">Disabling **Allow scrolling past end of file** in Settings</span></span>  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="Der Bildlauf am Ende einer Datei ist jetzt im Bereich Quellen deaktiviert." lightbox="../../images/2020/01/scrollingsources.msft.png":::
   <span data-ttu-id="57cf2-244">Der Bildlauf am Ende einer Datei ist jetzt im Bereich Quellen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="57cf2-244">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="57cf2-245">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="57cf2-245">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="57cf2-246">Wenn Sie unter Windows oder macOS sind, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="57cf2-246">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="57cf2-247">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="57cf2-247">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="57cf2-248">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="57cf2-248">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simulieren eines mobilen Viewports – Simulieren mobiler Geräte mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Docs"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Geräterahmen anzeigen – Simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Docs"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit der Microsoft Edge DevTools-Befehlsmenüleiste | Microsoft Docs"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Drosseln des Netzwerks und der CPU – Simulieren mobiler Geräte mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Docs"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Microsoft Docs"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Felder – Anzeigen, Bearbeiten und Löschen von Cookies mit Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Debugger für Microsoft Edge Visual Studio Codeerweiterung"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Elemente für Microsoft Edge Visual Studio Codeerweiterung"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Preview Channels"  

[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Code"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Debugger für Microsoft Edge – Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elemente für Microsoft Edge \(Chromium\) – Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint – Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Verbessern der Nachverfolgungsverhütung in Microsoft Edge-Blogbeitrag"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Herunterladen Visual Studio 2019 für Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Tweet posten"  

[CR924693]: https://crbug.com/924693 "Featureanforderung: Hinzufügen von "Moto G4" zur Gerätemodusliste | Chromium-Bugs"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Chromium-Bugs"  
[CR1026879]: https://crbug.com/1026879 "Die Registerkarte Cookie in der Entwicklungskonsole zeigt keine Priorität mehr | Chromium-Bugs"  
[CR1029826]: https://crbug.com/1029826 "Netzwerkregisterkarte – > die rechte Option zum Anfordern von -> Copy -> kopieren, da beim Abrufen keine Cookies | Chromium-Bugs"  
[CR985402]: https://crbug.com/985402 "Fehlerzeichenfolgen des Web-App-Manifestsymbols sind verwirrend | Chromium-Bugs"  
[CR963183]: https://crbug.com/963183 "DevTools sind nicht WCAG-kompatible | Chromium-Bugs"  
[CR941561]: https://crbug.com/941561 "Lokalisierbarkeit der DevTools-| Chromium-Bugs"  
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium-Bugs"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demo für nicht angezeigte CSS-Inhalte"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Neues Problem – MicrosoftDocs/edge-developer"  

[TheWebWeWant]: https://aka.ms/webwewant "The Web We Want"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Einblicke in die Barrierefreiheit"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Document Object Model (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools, Twitter-Konto"  

[Webhint]: https://aka.ms/webhint "webhint"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Webhint Browser Extension | Webhintdokumentation"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio Codeerweiterung | Webhintdokumentation"  

> [!NOTE]
> <span data-ttu-id="57cf2-285">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57cf2-285">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="57cf2-286">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/updates/2020/01/devtools/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="57cf2-286">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="57cf2-288">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="57cf2-288">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
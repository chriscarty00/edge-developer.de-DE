---
description: Verbesserungen der Barrierefreiheit, Verwendung des devtools in anderen Sprachen und vieles mehr.
title: Neuerungen in devtools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: dcc6c97cfb355d654c596f4be29de6507174bebd
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993401"
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

# <span data-ttu-id="38cd1-104">Neuerungen in devtools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="38cd1-104">What's new in DevTools (Microsoft Edge 80)</span></span>  

## <span data-ttu-id="38cd1-105">Ankündigungen des Microsoft Edge devtools-Teams</span><span class="sxs-lookup"><span data-stu-id="38cd1-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="38cd1-106">In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise im Microsoft Edge devtools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="38cd1-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="38cd1-107">Schauen Sie sich diese an, um neue Features in den devtools, vs-Code Erweiterungen und mehr zu testen.</span><span class="sxs-lookup"><span data-stu-id="38cd1-107">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="38cd1-108">Wenn Sie über die neuesten und besten Funktionen Ihrer Entwicklertools auf dem Laufenden bleiben möchten, laden Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] herunter und [folgen Sie uns auf Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="38cd1-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="38cd1-109">Verbesserungen der Barrierefreiheit für devtools</span><span class="sxs-lookup"><span data-stu-id="38cd1-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="38cd1-110">Das devtools-Team hat 170-Änderungen zu chromium beigetragen, um Probleme mit der Farbkontrast-, Tastatur-und Bildschirmsprachausgabe in devtools zu beheben.</span><span class="sxs-lookup"><span data-stu-id="38cd1-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="38cd1-111">Jeder Entwickler, der das Web erstellt, sollte in der Lage sein, das devtools zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="38cd1-111">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="38cd1-112">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="38cd1-112">Figure 1</span></span>  
> <span data-ttu-id="38cd1-113">Das Tool "Leistung" im devtools mit den Verbesserungen der Tastaturnavigation und der Bildschirmsprachausgabe</span><span class="sxs-lookup"><span data-stu-id="38cd1-113">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![Das Tool "Leistung" im devtools mit den Verbesserungen der Tastaturnavigation und der Bildschirmsprachausgabe][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="38cd1-115">Möchten Sie erfahren, wie Sie Ihre Webseite für alle Benutzer barrierefrei gestalten können?</span><span class="sxs-lookup"><span data-stu-id="38cd1-115">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="38cd1-116">Laden Sie die [Barrierefreiheits Einblicke][AccessibilityInsights] und [webhint][WebhintBrowserExtension] -Erweiterungen für Microsoft Edge herunter, um zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="38cd1-116">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="38cd1-117">Wenn Sie Bildschirmsprachausgaben oder die Tastatur verwenden, um in der devtools zu navigieren, senden Sie uns Ihr Feedback, indem Sie uns [tweeten][PostTweetEdgeDevTools] oder auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) klicken.</span><span class="sxs-lookup"><span data-stu-id="38cd1-117">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="38cd1-118">Chrom Problem [#963183][crbug963183]</span><span class="sxs-lookup"><span data-stu-id="38cd1-118">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="38cd1-119">Verwenden des devtools in anderen Sprachen</span><span class="sxs-lookup"><span data-stu-id="38cd1-119">Using the DevTools in other languages</span></span>  

<span data-ttu-id="38cd1-120">Viele Entwickler verwenden andere Entwicklertools wie StackOverflow und vs-Code in ihrer Muttersprache, nicht nur in Englisch.</span><span class="sxs-lookup"><span data-stu-id="38cd1-120">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="38cd1-121">Wir freuen uns, die Lokalisierung für das devtools bekannt zu geben, das Sie nun in einer von 10 Sprachen außer Englisch verwenden können:</span><span class="sxs-lookup"><span data-stu-id="38cd1-121">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="38cd1-122">Chinesisch (vereinfacht \) –  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="38cd1-122">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="38cd1-123">Chinesisch (traditionell \) –  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="38cd1-123">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="38cd1-124">Französisch – Fran&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="38cd1-124">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="38cd1-125">Deutsch-Deutsch</span><span class="sxs-lookup"><span data-stu-id="38cd1-125">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="38cd1-126">Italienisch-Italiano</span><span class="sxs-lookup"><span data-stu-id="38cd1-126">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="38cd1-127">Japanisch –  &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="38cd1-127">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="38cd1-128">Koreanisch –  &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="38cd1-128">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="38cd1-129">Portugiesisch-Portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="38cd1-129">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="38cd1-130">Russisch –  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="38cd1-130">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="38cd1-131">Spanisch-ESPA&#241;OL</span><span class="sxs-lookup"><span data-stu-id="38cd1-131">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="38cd1-132">Navigieren Sie zu `edge://flags` und setzen Sie das Kennzeichen **lokalisierte Entwickler Tools aktivieren** auf **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="38cd1-132">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="38cd1-133">Setzen Sie auch das Kennzeichen **Entwickler Tools Experimente** auf **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="38cd1-133">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="38cd1-134">Starten Sie Microsoft Edge neu, und öffnen Sie das devtools.</span><span class="sxs-lookup"><span data-stu-id="38cd1-134">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="38cd1-135">Die devtools entsprechen der Sprache, in der Sie Microsoft Edge verwenden `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="38cd1-135">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

> ##### <span data-ttu-id="38cd1-136">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="38cd1-136">Figure 2</span></span>  
> <span data-ttu-id="38cd1-137">Das devtools in Deutsch</span><span class="sxs-lookup"><span data-stu-id="38cd1-137">The DevTools in German</span></span>  
> ![Das devtools in Deutsch][ImageLocalizedGerman]  

<span data-ttu-id="38cd1-139">Wenn Sie das devtools in einer anderen Sprache als den verfügbaren verwenden möchten, senden Sie uns eine [Tweet][PostTweetEdgeDevTools] oder klicken Sie auf das Symbol [Feedback senden](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="38cd1-139">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="38cd1-140">Chrom Problem [#941561][crbug941561]</span><span class="sxs-lookup"><span data-stu-id="38cd1-140">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="38cd1-141">webhint Microsoft Edge-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="38cd1-141">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="38cd1-142">Mit der webhint Microsoft Edge-Erweiterung können Sie Ihre Webseite auf einfache Weise überprüfen und Feedback zu Barrierefreiheit, Browserkompatibilität, Sicherheit, Leistung und vielem mehr in der devtools erhalten.</span><span class="sxs-lookup"><span data-stu-id="38cd1-142">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="38cd1-143">Weitere Informationen finden Sie unter [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="38cd1-143">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="38cd1-144">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="38cd1-144">Figure 3</span></span>  
> <span data-ttu-id="38cd1-145">Die Registerkarte "Hinweise" im devtools, wenn die webhint-Browser Erweiterung installiert ist</span><span class="sxs-lookup"><span data-stu-id="38cd1-145">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![Die Registerkarte "Hinweise" im devtools, wenn die webhint-Browser Erweiterung installiert ist][ImageHintsTabWebhintExtension]  

<span data-ttu-id="38cd1-147">[Testen Sie die webhint-Browser Erweiterung in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="38cd1-147">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="38cd1-148">Nachdem Sie die Erweiterung installiert haben, öffnen Sie das devtools, und wählen Sie die Registerkarte Hinweise aus.  Führen Sie von hier aus eine anpassbare Website Überprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="38cd1-148">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="38cd1-149">Besuchen Sie [webhint.IO][WebhintBrowserExtension] , um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="38cd1-149">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <span data-ttu-id="38cd1-150">3D View</span><span class="sxs-lookup"><span data-stu-id="38cd1-150">3D View</span></span>  

<span data-ttu-id="38cd1-151">Verwenden Sie die **3D-Ansicht** , um Ihre Webanwendung zu debuggen, indem Sie durch das [Dokumentobjektmodell \ (DOM \)][MDNDocumentObjectModel] oder den Stapel Kontext des [z-Index][MDNZIndex] navigieren.</span><span class="sxs-lookup"><span data-stu-id="38cd1-151">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="38cd1-152">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="38cd1-152">Figure 4</span></span>  
> <span data-ttu-id="38cd1-153">Die 3D-Ansicht im devtools</span><span class="sxs-lookup"><span data-stu-id="38cd1-153">The 3D View in the DevTools</span></span>  
> ![Die 3D-Ansicht im devtools][Image3DView]  

<span data-ttu-id="38cd1-155">Wenn Sie auf die 3D-Ansicht zugreifen möchten, navigieren Sie zu `edge://flags` und stellen Sie sicher, dass das Kennzeichen **Entwickler Tools Experimente** auf **aktiviert**festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="38cd1-155">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="38cd1-156">Starten Sie Microsoft Edge neu, und öffnen Sie das devtools.</span><span class="sxs-lookup"><span data-stu-id="38cd1-156">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="38cd1-157">Drücken Sie `F1` im devtools oder wechseln Sie zu **Einstellungen**, navigieren Sie zu **Experimenten** , und aktivieren Sie das Kontrollkästchen **3D-Ansicht aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="38cd1-157">Press `F1` in the DevTools or go to **Settings**, navigate to **Experiments** section, and check the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="38cd1-158">Drücken Sie jetzt `Ctrl`  +  `Shift`  +  `P` , geben Sie in **3D-Ansicht** ein, und wählen Sie **3D-Ansicht**anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="38cd1-158">Now, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="38cd1-159">Wir arbeiten an der Benutzeroberfläche und fügen der 3D-Ansicht Weitere Funktionen hinzu, damit Sie uns Ihr [Feedback](#getting-in-touch-with-microsoft-edge-devtools-team)senden können.</span><span class="sxs-lookup"><span data-stu-id="38cd1-159">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="38cd1-160">Chrom Problem [#987787][crbug987787]</span><span class="sxs-lookup"><span data-stu-id="38cd1-160">Chromium issue [#987787][crbug987787]</span></span>

### <span data-ttu-id="38cd1-161">Visual Studio-Code Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="38cd1-161">Visual Studio Code extensions</span></span>  

<span data-ttu-id="38cd1-162">Das devtools-Team hat auch einige Erweiterungen für [Visual Studio-Code \ (vs-Code \)][VisualStudioCode] veröffentlicht, mit denen Sie die Leistung des devtools direkt aus Ihrem Text-Editor verwenden können!</span><span class="sxs-lookup"><span data-stu-id="38cd1-162">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="38cd1-163">Schauen Sie sich die folgenden Erweiterungen an:</span><span class="sxs-lookup"><span data-stu-id="38cd1-163">Check out the extensions below:</span></span>  

#### <span data-ttu-id="38cd1-164">Elemente für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="38cd1-164">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="38cd1-165">Verwenden Sie das Elements-Tool aus dem vs-Code, indem Sie die [Elemente für Microsoft Edge \ (Chrom \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] vs-Code Erweiterung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="38cd1-165">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="38cd1-166">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="38cd1-166">Figure 5</span></span>  
> <span data-ttu-id="38cd1-167">Das Tool ' Elemente ' im vs-Code mit den Elementen für Microsoft Edge Extension</span><span class="sxs-lookup"><span data-stu-id="38cd1-167">The Elements tool in VS Code using the Elements for Microsoft Edge extension</span></span>  
> ![Das Tool ' Elemente ' im vs-Code mit den Elementen für Microsoft Edge Extension][ImageElementsVisualStudioCode]  

<span data-ttu-id="38cd1-169">Weitere Informationen finden Sie unter [Elemente für Microsoft Edge vs Code Extension][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="38cd1-169">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="38cd1-170">Debugger für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="38cd1-170">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="38cd1-171">Debuggen Sie mit dem [Debugger für Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] vs Code Extension JavaScript, das in Microsoft Edge ausgeführt wird, direkt von vs-Code!</span><span class="sxs-lookup"><span data-stu-id="38cd1-171">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="38cd1-172">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="38cd1-172">Figure 6</span></span>  
> <span data-ttu-id="38cd1-173">Der Debugger für Microsoft Edge Extension in vs-Code</span><span class="sxs-lookup"><span data-stu-id="38cd1-173">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![Der Debugger für Microsoft Edge Extension in vs-Code][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="38cd1-175">Weitere Informationen finden Sie unter [Debuggen von Microsoft Edge aus vs-Code][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="38cd1-175">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="38cd1-176">Webhint</span><span class="sxs-lookup"><span data-stu-id="38cd1-176">webhint</span></span>  

<span data-ttu-id="38cd1-177">Die [webhint][VisualStudioMarketplaceWebhintExtension] vs-Code Erweiterung verwendet `webhint` , um Ihre Webseite zu verbessern, während Sie Sie schreiben!</span><span class="sxs-lookup"><span data-stu-id="38cd1-177">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="38cd1-178">Mit dieser Erweiterung wird die Diagnose für Ihre Arbeitsbereichsdateien basierend auf der Analyse ausgeführt und gemeldet `webhint` .</span><span class="sxs-lookup"><span data-stu-id="38cd1-178">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="38cd1-179">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="38cd1-179">Figure 7</span></span>  
> <span data-ttu-id="38cd1-180">Die webhint vs-Code Erweiterung, die eine TSX-Datei im vs-Code analysiert</span><span class="sxs-lookup"><span data-stu-id="38cd1-180">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![Die webhint vs-Code Erweiterung, die eine TSX-Datei im vs-Code analysiert][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="38cd1-182">[Weitere Informationen zur Erweiterung des vs-Code webhints][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="38cd1-182">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="38cd1-183">Integration von Visual Studio</span><span class="sxs-lookup"><span data-stu-id="38cd1-183">Visual Studio integration</span></span>
<span data-ttu-id="38cd1-184">Verwenden Sie in Visual Studio 2019, Version 16,2 oder höher, den Visual Studio-Debugger zum Debuggen von JavaScript, das in Microsoft Edge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38cd1-184">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="38cd1-185">[Laden Sie Visual Studio 2019 herunter][MicrosoftVisualStudioDownloads] , um dieses Feature auszuprobieren!</span><span class="sxs-lookup"><span data-stu-id="38cd1-185">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="38cd1-186">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="38cd1-186">Figure 8</span></span>  
> <span data-ttu-id="38cd1-187">Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, dev oder Beta</span><span class="sxs-lookup"><span data-stu-id="38cd1-187">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, dev oder Beta][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="38cd1-189">[Lesen Sie unseren Blogbeitrag, um zu erfahren, wie Sie Microsoft Edge in Visual Studio debuggen][MicrosoftVisualStudioBlogDebugJavascript]können.</span><span class="sxs-lookup"><span data-stu-id="38cd1-189">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <span data-ttu-id="38cd1-190">Nachrichten zur Präventions Konsole</span><span class="sxs-lookup"><span data-stu-id="38cd1-190">Tracking prevention Console messages</span></span>  

<span data-ttu-id="38cd1-191">Die nach Verfolgungs Verhinderung ist ein einzigartiges Feature in Microsoft Edge, das Sie davor schützt, von Websites, die Sie noch nicht besucht haben, nachverfolgt</span><span class="sxs-lookup"><span data-stu-id="38cd1-191">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="38cd1-192">Die Standardeinstellung für die nach Verfolgungs Verhinderung ist der Modus "ausgeglichen", der Drittanbieter-Tracker und bekannte bösartige Tracker für eine Erfahrung blockiert, die Datenschutz und Web-Kompatibilität abgleicht.</span><span class="sxs-lookup"><span data-stu-id="38cd1-192">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="38cd1-193">Damit Sie mehr über die Kompatibilität Ihrer Webseite erfahren, wenn bestimmte Tracker blockiert sind, haben wir auch Warnmeldungen in der Konsole hinzugefügt, wenn ein Tracker blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="38cd1-193">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="38cd1-194">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="38cd1-194">Figure 9</span></span>  
> <span data-ttu-id="38cd1-195">Nachrichten in der Konsole, wenn die nach Verfolgungs Prävention den Zugriff auf den Speicher für einen Tracker blockiert</span><span class="sxs-lookup"><span data-stu-id="38cd1-195">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Nachrichten in der Konsole, wenn die nach Verfolgungs Prävention den Zugriff auf den Speicher für einen Tracker blockiert][ImageTrackingPrevention]  

<span data-ttu-id="38cd1-197">[Weitere Informationen finden Sie unter Verhinderung von Nachverfolgung und dem Gleichgewichtzwischen Datenschutz und Web-Kompatibilität][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="38cd1-197">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="38cd1-198">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="38cd1-198">Announcements from the Chromium project</span></span>  

<span data-ttu-id="38cd1-199">In den folgenden Abschnitten werden weitere in Microsoft Edge 80 verfügbare Features angekündigt, die zum Open-Source-Projekt Chromium beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="38cd1-199">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="38cd1-200">Unterstützung für Let-und Class-Deklarationen in der Konsole</span><span class="sxs-lookup"><span data-stu-id="38cd1-200">Support for let and class redeclarations in the Console</span></span>  

<span data-ttu-id="38cd1-201">Die Konsole unterstützt jetzt erneute Deklarationen von `let` und- `class` Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="38cd1-201">The Console now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="38cd1-202">Die Unfähigkeit, erneut zu deklarieren, war ein häufiges Ärgernis für Webentwickler, die die Konsole zum Experimentieren mit neuem JavaScript-Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="38cd1-202">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="38cd1-203">Das erneute Deklarieren einer `let` oder `class` -Anweisung in einem Skript außerhalb der Konsole oder in einer einzelnen Konsoleneingabe führt weiterhin zu einer `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="38cd1-203">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="38cd1-204">Bei der erneuten Deklaration einer lokalen Variablen mit `let` hat die Konsole beispielsweise einen Fehler ausgelöst:</span><span class="sxs-lookup"><span data-stu-id="38cd1-204">For example, previously, when redeclaring a local variable with `let`, the Console threw an error:</span></span>  

> ##### <span data-ttu-id="38cd1-205">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="38cd1-205">Figure 10</span></span>  
> <span data-ttu-id="38cd1-206">Die Konsole in Microsoft Edge 79 zeigt, dass die Let-erneute Deklaration fehlschlägt</span><span class="sxs-lookup"><span data-stu-id="38cd1-206">The Console in Microsoft Edge 79 showing that the let redeclaration fails</span></span>  
> ![Die Konsole in Microsoft Edge 79 zeigt, dass die Let-erneute Deklaration fehlschlägt][ImageConsoleRedeclarationFails]  

<span data-ttu-id="38cd1-208">Die Konsole ermöglicht nun die erneute Deklaration:</span><span class="sxs-lookup"><span data-stu-id="38cd1-208">Now, the Console allows the redeclaration:</span></span>  

> ##### <span data-ttu-id="38cd1-209">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="38cd1-209">Figure 11</span></span>  
> <span data-ttu-id="38cd1-210">Die Konsole in Microsoft Edge 80 zeigt, dass die Let-erneute Deklaration erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="38cd1-210">The Console in Microsoft Edge 80 showing that the let redeclaration succeeds</span></span>  
> ![Die Konsole in Microsoft Edge 80 zeigt, dass die Let-erneute Deklaration erfolgreich ist][ImageConsoleRedeclarationSucceeds]  

<span data-ttu-id="38cd1-212">Chrom Problem [#1004193][crbug1004193]</span><span class="sxs-lookup"><span data-stu-id="38cd1-212">Chromium issue [#1004193][crbug1004193]</span></span>  

### <span data-ttu-id="38cd1-213">Verbessertes Webassembly-Debugging</span><span class="sxs-lookup"><span data-stu-id="38cd1-213">Improved WebAssembly debugging</span></span>  

<span data-ttu-id="38cd1-214">DevTools hat mit der Unterstützung des [Dwarf-Debugging-Standards][DwarfHome]begonnen, was mehr Unterstützung für die schrittweise Codierung, das Festlegen von Haltepunkten und das Auflösen von Stapelablaufverfolgungen in ihren Quellsprachen in devtools bedeutet.</span><span class="sxs-lookup"><span data-stu-id="38cd1-214">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
> ##### Figure  
> The new DWARF-powered WebAssembly debugging  
> ![The new DWARF-powered WebAssembly debugging][ImageDwarfPoweredWebAssemblyDebugging]  
-->  

### <span data-ttu-id="38cd1-215">Netzwerk Panel-Updates</span><span class="sxs-lookup"><span data-stu-id="38cd1-215">Network panel updates</span></span>  

#### <span data-ttu-id="38cd1-216">Anfordern von Initiator-Chains auf der Registerkarte "Initiator"</span><span class="sxs-lookup"><span data-stu-id="38cd1-216">Request Initiator Chains in the Initiator tab</span></span>  

<span data-ttu-id="38cd1-217">Sie können nun die Initiatoren und Abhängigkeiten einer Netzwerkanforderung als geschachtelte Liste anzeigen.</span><span class="sxs-lookup"><span data-stu-id="38cd1-217">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="38cd1-218">Dies kann Ihnen helfen zu verstehen, warum eine Ressource angefordert wurde, oder welche Netzwerkaktivität eine bestimmte Ressource (wie ein Skript \) verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="38cd1-218">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

> ##### <span data-ttu-id="38cd1-219">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="38cd1-219">Figure 12</span></span>  
> <span data-ttu-id="38cd1-220">Eine Anforderungs Initiator-Kette auf der Registerkarte "Initiator"</span><span class="sxs-lookup"><span data-stu-id="38cd1-220">A Request Initiator Chain in the Initiator tab</span></span>  
> ![Eine Anforderungs Initiator-Kette auf der Registerkarte "Initiator"][ImageRequestInitiatorChain]  

<span data-ttu-id="38cd1-222">Klicken Sie nach dem [Protokollieren der Netzwerkaktivität in der Netzwerksteuerung][DevToolsNetworkIndex]auf eine Ressource, und wechseln Sie dann zur Registerkarte **Initiator** , um die **Anforderungs initiatorkette**anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="38cd1-222">After [logging network activity in the Network panel][DevToolsNetworkIndex], click a resource and then go to the **Initiator** tab to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="38cd1-223">Die **geprüfte Ressource** ist fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="38cd1-223">The **inspected resource** is bold.</span></span>  <span data-ttu-id="38cd1-224">Im obigen Screenshot `ai.2.min.js` befindet sich die geprüfte Ressource.</span><span class="sxs-lookup"><span data-stu-id="38cd1-224">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="38cd1-225">Die Ressourcen oberhalb der geprüften Ressource sind die **Initiatoren**.</span><span class="sxs-lookup"><span data-stu-id="38cd1-225">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="38cd1-226">Im obigen Screenshot `https://www.microsoftedgeinsider.com` ist der Initiator von `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="38cd1-226">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="38cd1-227">Mit anderen Worten: `https://www.microsoftedgeinsider.com` Ursache für die Netzwerkanforderung `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="38cd1-227">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="38cd1-228">Die Ressourcen unterhalb der geprüften Ressource sind die **Abhängigkeiten**.</span><span class="sxs-lookup"><span data-stu-id="38cd1-228">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="38cd1-229">Im obigen Screenshot `https://dc.services.visualstudio.com/v2/track` ist eine Abhängigkeit von `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="38cd1-229">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="38cd1-230">Mit anderen Worten: `ai.2.min.js` Ursache für die Netzwerkanforderung `https://dc.services.visualstudio.com/v2/track` .</span><span class="sxs-lookup"><span data-stu-id="38cd1-230">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="38cd1-231">Auf Initiator-und Abhängigkeitsinformationen kann auch zugegriffen werden, indem Sie `Shift` auf Netzwerkressourcen halten und dann darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="38cd1-231">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="38cd1-232">Weitere Informationen finden Sie unter [Anzeigen von Initiatoren und Abhängigkeiten][DevToolsNetworkReferenceViewInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="38cd1-232">See [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="38cd1-233">Chrom Problem [#842488][crbug842488]</span><span class="sxs-lookup"><span data-stu-id="38cd1-233">Chromium issue [#842488][crbug842488]</span></span>  

#### <span data-ttu-id="38cd1-234">Markieren der ausgewählten Netzwerkanforderung in der Übersicht</span><span class="sxs-lookup"><span data-stu-id="38cd1-234">Highlight the selected network request in the Overview</span></span>  

<span data-ttu-id="38cd1-235">Nachdem Sie auf eine Netzwerkressource klicken, um Sie zu überprüfen, fügt das Netzwerk Panel nun einen blauen Rahmen um die Ressource in der **Übersicht**ein.</span><span class="sxs-lookup"><span data-stu-id="38cd1-235">After you click a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="38cd1-236">Dies kann Ihnen helfen zu erkennen, ob die Netzwerkanforderung früher oder später als erwartet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38cd1-236">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

> ##### <span data-ttu-id="38cd1-237">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="38cd1-237">Figure 13</span></span>  
> <span data-ttu-id="38cd1-238">Der Übersichtsbereich, der die überprüfte Ressource markiert</span><span class="sxs-lookup"><span data-stu-id="38cd1-238">The Overview pane highlighting the inspected resource</span></span>  
> ![Der Übersichtsbereich, der die überprüfte Ressource markiert][ImageOverviewPaneInspectedResource]  

<span data-ttu-id="38cd1-240">Chrom Problem [#988253][crbug988253]</span><span class="sxs-lookup"><span data-stu-id="38cd1-240">Chromium issue [#988253][crbug988253]</span></span>  

#### <span data-ttu-id="38cd1-241">URL-und Pfad Spalten im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="38cd1-241">URL and path columns in the Network panel</span></span>  

<span data-ttu-id="38cd1-242">Verwenden Sie die Spalten neuer **Pfad** und **URL** im **Netzwerk** Panel, um den absoluten Pfad oder die vollständige URL der einzelnen Netzwerkressourcen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="38cd1-242">Use the new **Path** and **URL** columns in the **Network** panel to see the absolute path or full URL of each network resource.</span></span>  

> ##### <span data-ttu-id="38cd1-243">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="38cd1-243">Figure 14</span></span>  
> <span data-ttu-id="38cd1-244">Die Spalten ' neuer Pfad ' und ' URL ' im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="38cd1-244">The new Path and URL columns in the Network panel</span></span>  
> ![Die Spalten ' neuer Pfad ' und ' URL ' im Netzwerk Panel][ImagePathNetworkPanel]  

<span data-ttu-id="38cd1-246">Klicken Sie mit der rechten Maustaste auf die Tabelle Überschrift **Wasserfall** , und wählen Sie **Pfad** oder **URL** aus, um die neuen Spalten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="38cd1-246">Right-click the **Waterfall** table header and select **Path** or **URL** to show the new columns.</span></span>  

<span data-ttu-id="38cd1-247">Chrom Problem [#993366][crbug993366]</span><span class="sxs-lookup"><span data-stu-id="38cd1-247">Chromium issue [#993366][crbug993366]</span></span>  

#### <span data-ttu-id="38cd1-248">Aktualisierte Benutzer-Agent-Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="38cd1-248">Updated User-Agent strings</span></span>  

<span data-ttu-id="38cd1-249">DevTools unterstützt das Festlegen einer benutzerdefinierten Benutzer-Agent-Zeichenfolge über die Registerkarte **Netzwerkbedingungen** .  Die Benutzer-Agent-Zeichenfolge wirkt `User-Agent` sich auf den an Netzwerkressourcen angefügten HTTP-Header und auch auf den Wert von aus `navigator.userAgent` .</span><span class="sxs-lookup"><span data-stu-id="38cd1-249">DevTools supports setting a custom User-Agent string through the **Network Conditions** tab.  The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="38cd1-250">Die vordefinierten Benutzer-Agent-Zeichenfolgen wurden so aktualisiert, dass Sie den modernen Browserversionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="38cd1-250">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

> ##### <span data-ttu-id="38cd1-251">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="38cd1-251">Figure 15</span></span>  
> <span data-ttu-id="38cd1-252">Das Menü "Benutzer-Agent" auf der Registerkarte "Netzwerkbedingungen"</span><span class="sxs-lookup"><span data-stu-id="38cd1-252">The User Agent menu in the Network Conditions tab</span></span>  
> ![Das Menü "Benutzer-Agent" auf der Registerkarte "Netzwerkbedingungen"][ImageUserAgentNetworkConditionsTab]  

<span data-ttu-id="38cd1-254">Um auf **Netzwerkbedingungen**zuzugreifen, [Öffnen Sie das Befehlsmenü][DevToolsCommandMenuIndex] , und führen Sie den `Show Network Conditions` Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="38cd1-254">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="38cd1-255">Sie können auch [Benutzer-Agent-Zeichenfolgen im Gerätemodus einrichten][DevToolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="38cd1-255">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="38cd1-256">Chrom Problem [#1029031][crbug1029031]</span><span class="sxs-lookup"><span data-stu-id="38cd1-256">Chromium issue [#1029031][crbug1029031]</span></span>  

### <span data-ttu-id="38cd1-257">Audits-Panel-Updates</span><span class="sxs-lookup"><span data-stu-id="38cd1-257">Audits panel updates</span></span>  

#### <span data-ttu-id="38cd1-258">Neue Konfigurations-UI</span><span class="sxs-lookup"><span data-stu-id="38cd1-258">New configuration UI</span></span>  

<span data-ttu-id="38cd1-259">Die Benutzeroberfläche der Konfiguration verfügt über ein neues, reaktionsfähiges Design, und die Optionen für die Einschränkungs Konfiguration wurden vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="38cd1-259">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="38cd1-260">Weitere Informationen zu den Änderungen beim Einschränken der Benutzeroberfläche finden Sie unter [Drosselung des Überwachungs Panels][GitHubGoogleChromeDevToolsAuditsPanelThrottling] .</span><span class="sxs-lookup"><span data-stu-id="38cd1-260">See [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling] for more information on the throttling UI changes.</span></span>  

> ##### <span data-ttu-id="38cd1-261">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="38cd1-261">Figure 16</span></span>  
> <span data-ttu-id="38cd1-262">Die neue Benutzeroberfläche für die Konfiguration</span><span class="sxs-lookup"><span data-stu-id="38cd1-262">The new configuration UI</span></span>  
> ![Die neue Benutzeroberfläche für die Konfiguration][ImageConfigurationUI]  

### <span data-ttu-id="38cd1-264">Updates für Coverage-Registerkarten</span><span class="sxs-lookup"><span data-stu-id="38cd1-264">Coverage tab updates</span></span>  

#### <span data-ttu-id="38cd1-265">Pro-Funktion-oder pro-Block-Abdeckungs Modi</span><span class="sxs-lookup"><span data-stu-id="38cd1-265">Per-function or per-block coverage modes</span></span>  

<span data-ttu-id="38cd1-266">Die [Registerkarte Coverage][DevToolsCoverageIndex] enthält ein neues Dropdownmenü, in dem Sie angeben können, ob Codeabdeckungsdaten **pro Funktion** oder **pro Block**erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="38cd1-266">The [Coverage tab][DevToolsCoverageIndex] has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="38cd1-267">**Pro-Block** -Abdeckung ist detaillierter, aber auch weitaus teurer zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="38cd1-267">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="38cd1-268">DevTools verwendet jetzt standardmäßig **pro Funktion** Coverage.</span><span class="sxs-lookup"><span data-stu-id="38cd1-268">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="38cd1-269">Je nachdem, ob Sie **pro Funktion** oder **pro Block** Modus verwenden, werden möglicherweise große Unterschiede bei der Codeabdeckung in HTML-Dateien angezeigt.</span><span class="sxs-lookup"><span data-stu-id="38cd1-269">You may see large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="38cd1-270">Bei Verwendung des **pro-Funktions** Modus werden Inlineskripts in HTML-Dateien als Funktionen behandelt.</span><span class="sxs-lookup"><span data-stu-id="38cd1-270">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="38cd1-271">Wenn das Skript überhaupt ausgeführt wird, markiert devtools das gesamte Skript als verwendeten Code.</span><span class="sxs-lookup"><span data-stu-id="38cd1-271">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="38cd1-272">Nur wenn das Skript überhaupt nicht ausgeführt wird, kennzeichnet devtools das Skript als unbenutzten Code.</span><span class="sxs-lookup"><span data-stu-id="38cd1-272">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

> ##### <span data-ttu-id="38cd1-273">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="38cd1-273">Figure 17</span></span>  
> <span data-ttu-id="38cd1-274">Dropdownmenü "Coverage-Modus"</span><span class="sxs-lookup"><span data-stu-id="38cd1-274">The coverage mode dropdown menu</span></span>  
> ![Dropdownmenü "Coverage-Modus"][ImageCoverageMode]  

#### <span data-ttu-id="38cd1-276">Coverage muss nun durch ein Seiten-Reload initiiert werden</span><span class="sxs-lookup"><span data-stu-id="38cd1-276">Coverage must now be initiated by a page reload</span></span>  

<span data-ttu-id="38cd1-277">Das Umschalten der Codeabdeckung ohne das erneute Laden einer Seite wurde entfernt, da die Abdeckungsdaten unzuverlässig waren.</span><span class="sxs-lookup"><span data-stu-id="38cd1-277">Toggling code coverage without a page reload has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="38cd1-278">Beispielsweise kann eine Funktion als unbenutzt gemeldet werden, wenn die Laufzeit vor langer Zeit war und der V8-Garbage Collector Sie bereinigt hat.</span><span class="sxs-lookup"><span data-stu-id="38cd1-278">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="38cd1-279">Chrom Problem [#1004203][crbug1004203]</span><span class="sxs-lookup"><span data-stu-id="38cd1-279">Chromium issue [#1004203][crbug1004203]</span></span>  

## <span data-ttu-id="38cd1-280">Herunterladen der Microsoft Edge Preview-Kanäle</span><span class="sxs-lookup"><span data-stu-id="38cd1-280">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="38cd1-281">Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="38cd1-281">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="38cd1-282">Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="38cd1-282">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="38cd1-283">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="38cd1-283">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!--<<../../_shared/devtools-feedback.md>> -->

<!--<<../../_shared/canary.md>> -->

<!--<<../../_shared/discover.md>> -->

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2019/12/a11y-performance-tool.msft.gif "Abbildung 1: das Tool "Leistung" im devtools mit den Verbesserungen der Tastaturnavigation und der Bildschirmsprachausgabe"  
[ImageLocalizedGerman]: ../../images/2019/12/localized-devtools.msft.png "Abbildung 2: die devtools in Deutsch"  
[ImageHintsTabWebhintExtension]: ../../images/2019/12/webhint-browser-extension.msft.png "Abbildung 3: die Registerkarte "Hinweise" im Microsoft Edge-devtools, wenn die webhint-Browser Erweiterung installiert ist"  
[Image3DView]: ../../images/2019/12/3dview.msft.png "Abbildung 4: die 3D-Ansicht in der Microsoft Edge-devtools"  
[ImageElementsVisualStudioCode]: ../../images/2019/12/elements-for-edge.msft.png "Abbildung 5: das Tool "Elemente" im vs-Code mit den Elementen für Microsoft Edge Extension"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2019/12/vscode-debugger.msft.png "Abbildung 6: Debugger für Microsoft-Edge-Erweiterung in vs-Code"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2019/12/webhint-vscode-extension.msft.png "Abbildung 7: die webhint vs-Code Erweiterung, die eine TSX-Datei im vs-Code analysiert"  
[ImageVisualStudioLaunchWebApp]: ../../images/2019/12/vs.msft.png "Abbildung 8: Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, dev oder Beta"  
[ImageTrackingPrevention]: ../../images/2019/12/tracking-prevention.msft.png "Abbildung 9: Nachrichten in der Konsole, wenn die nach Verfolgungs Prävention den Zugriff auf den Speicher für einen Tracker blockiert"  
[ImageConsoleRedeclarationFails]: ../../images/2019/12/letbefore.msft.png "Abbildung 10: die Konsole in Microsoft Edge 79, die zeigt, dass die Let-erneute Deklaration fehlschlägt"  
[ImageConsoleRedeclarationSucceeds]: ../../images/2019/12/letafter.msft.png "Abbildung 11: die Konsole in Microsoft Edge 80, die zeigt, dass die Let-erneute Deklaration erfolgreich ist"  
[ImageRequestInitiatorChain]: ../../images/2019/12/initiators.msft.png "Abbildung 12: eine Anforderungs Initiator-Kette auf der Registerkarte "Initiator""  
[ImageOverviewPaneInspectedResource]: ../../images/2019/12/overview.msft.png "Abbildung 13: der Übersichtsbereich, der die überprüfte Ressource markiert"  
[ImagePathNetworkPanel]: ../../images/2019/12/columns.msft.png "Abbildung 14: die Spalten "neuer Pfad" und "URL" im Netzwerk Panel"  
[ImageUserAgentNetworkConditionsTab]: ../../images/2019/12/useragent.msft.png "Abbildung 15: das Menü "Benutzer-Agent" auf der Registerkarte "Netzwerkbedingungen""  
[ImageConfigurationUI]: ../../images/2019/12/start.msft.png "Abbildung 16: die neue Benutzeroberfläche für die Konfiguration"  
[ImageCoverageMode]: ../../images/2019/12/modes.msft.png "Abbildung 17: das Dropdownmenü "Coverage Mode""  

<!--[ImageDwarfPoweredWebAssemblyDebugging]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: ../../../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  
[DevToolsCoverageIndex]: ../../../coverage/index.md "Suchen von nicht verwendetem Javascript und CSS-Code mit der Registerkarte "Coverage" in Microsoft Edge devtools"  
[DevToolsDeviceModeIndex]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simulieren eines mobilen Viewports – simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools"  
[DevToolsNetworkIndex]: ../../../network/index.md "Überprüfen der Netzwerkaktivität in Microsoft Edge devtools"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: ../../../network/reference.md#view-initiators-and-dependencies "Anzeigen von Initiatoren und Abhängigkeiten – Netzwerkanalyse Referenz"  
[DevGuideEdgeHtmlWhatsNew]: ../../../../dev-guide/whats-new.md "Neuerungen in EdgeHTML"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Debugger für Microsoft Edge-vs-Code Erweiterung"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elemente für Microsoft Edge vs Code Extension"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[crbug842488]: https://crbug.com/842488 "842488-Hinzufügen des Felds "Initiator" zur Registerkarte "Kopfzeilen"-Monorail"  
[crbug988253]: https://crbug.com/988253 "988253-Fehler-devtools-keine Zuordnung zwischen Netzwerkanforderung und Zeitachsendiagramm-Monorail"  
[crbug993366]: https://crbug.com/993366 "993366-Bitte zeigen Sie den Pfad Teil der URL in der Liste der Netzwerk-Panel-Anfragen-Monorail"  
[crbug1004193]: https://crbug.com/1004193 "1004193-repl-Modus für V8-Monorail"  
[crbug1004203]: https://crbug.com/1004203 "1004203-Monorail"  
[crbug1029031]: https://crbug.com/1029031 "1029031-UA-Zeichenfolgen werden veraltet-Monorail" 
[crbug963183]: https://crbug.com/963183 "963183-devtools sind keine WCAG-kompatibel"
[crbug941561]: https://crbug.com/941561 "941561-Lokalisierbarkeit des devtools"
[crbug987787]: https://crbug.com/987787 "987787-Dom 3D-Ansicht"

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
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint vs-Code Erweiterung | webhint-Dokumentation"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Verbessern der nach Verfolgungs Vorbeugung in Microsoft Edge-Blogbeitrag"
[TheWebWeWant]: https://aka.ms/webwewant "Das gewünschte Web"

> [!NOTE]
> <span data-ttu-id="38cd1-340">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38cd1-340">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="38cd1-341">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/updates/2019/12/devtools/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="38cd1-341">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="38cd1-343">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="38cd1-343">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

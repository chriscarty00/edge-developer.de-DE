---
title: Neuerungen in devtools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: ac85f0d9f8a5f112e702968b9c0aeceb05312ac1
ms.sourcegitcommit: 7e3a876ccb1f0ff3d50d4e32f03af98f780e2930
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2020
ms.locfileid: "10591391"
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








# <span data-ttu-id="d2b4f-103">Neuerungen in devtools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="d2b4f-103">What's new in DevTools (Microsoft Edge 80)</span></span>   



## <span data-ttu-id="d2b4f-104">Ankündigungen des Microsoft Edge devtools-Teams</span><span class="sxs-lookup"><span data-stu-id="d2b4f-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="d2b4f-105">In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise im Microsoft Edge devtools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="d2b4f-106">Schauen Sie sich diese an, um neue Features in den devtools, vs-Code Erweiterungen und mehr zu testen.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-106">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="d2b4f-107">Wenn Sie über die neuesten und besten Funktionen Ihrer Entwicklertools auf dem Laufenden bleiben möchten, laden Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] herunter und [folgen Sie uns auf Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="d2b4f-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="d2b4f-108">Verbesserungen der Barrierefreiheit für devtools</span><span class="sxs-lookup"><span data-stu-id="d2b4f-108">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="d2b4f-109">Das devtools-Team hat 170-Änderungen zu chromium beigetragen, um Probleme mit der Farbkontrast-, Tastatur-und Bildschirmsprachausgabe in devtools zu beheben.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-109">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="d2b4f-110">Jeder Entwickler, der das Web erstellt, sollte in der Lage sein, das devtools zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-110">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="d2b4f-111">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="d2b4f-111">Figure 1</span></span>  
> <span data-ttu-id="d2b4f-112">Das Tool "Leistung" im devtools mit den Verbesserungen der Tastaturnavigation und der Bildschirmsprachausgabe</span><span class="sxs-lookup"><span data-stu-id="d2b4f-112">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![Das Tool "Leistung" im devtools mit den Verbesserungen der Tastaturnavigation und der Bildschirmsprachausgabe][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="d2b4f-114">Möchten Sie erfahren, wie Sie Ihre Webseite für alle Benutzer barrierefrei gestalten können?</span><span class="sxs-lookup"><span data-stu-id="d2b4f-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="d2b4f-115">Laden Sie die [Barrierefreiheits Einblicke][AccessibilityInsights] und [webhint][WebhintBrowserExtension] -Erweiterungen für Microsoft Edge herunter, um zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="d2b4f-116">Wenn Sie Bildschirmsprachausgaben oder die Tastatur verwenden, um in der devtools zu navigieren, senden Sie uns Ihr Feedback, indem Sie uns [tweeten][PostTweetEdgeDevTools] oder auf das [Feedback](#feedback) -Symbol klicken.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="d2b4f-117">Chrom Problem [#963183][crbug963183]</span><span class="sxs-lookup"><span data-stu-id="d2b4f-117">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="d2b4f-118">Verwenden des devtools in anderen Sprachen</span><span class="sxs-lookup"><span data-stu-id="d2b4f-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="d2b4f-119">Viele Entwickler verwenden andere Entwicklertools wie StackOverflow und vs-Code in ihrer Muttersprache, nicht nur in Englisch.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-119">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="d2b4f-120">Wir freuen uns, die Lokalisierung für das devtools bekannt zu geben, das Sie nun in einer von 10 Sprachen außer Englisch verwenden können:</span><span class="sxs-lookup"><span data-stu-id="d2b4f-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d2b4f-121">Chinesisch (vereinfacht \) –  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="d2b4f-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d2b4f-122">Chinesisch (traditionell \) –  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="d2b4f-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="d2b4f-123">Französisch – Fran&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="d2b4f-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d2b4f-124">Deutsch-Deutsch</span><span class="sxs-lookup"><span data-stu-id="d2b4f-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="d2b4f-125">Italienisch-Italiano</span><span class="sxs-lookup"><span data-stu-id="d2b4f-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d2b4f-126">Japanisch –  &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="d2b4f-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="d2b4f-127">Koreanisch –  &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="d2b4f-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d2b4f-128">Portugiesisch-Portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="d2b4f-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="d2b4f-129">Russisch –  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="d2b4f-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d2b4f-130">Spanisch-ESPA&#241;OL</span><span class="sxs-lookup"><span data-stu-id="d2b4f-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="d2b4f-131">Navigieren Sie zu `edge://flags` und setzen Sie das Kennzeichen **lokalisierte Entwickler Tools aktivieren** auf **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-131">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="d2b4f-132">Setzen Sie auch das Kennzeichen **Entwickler Tools Experimente** auf **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-132">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="d2b4f-133">Starten Sie Microsoft Edge neu, und öffnen Sie das devtools.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-133">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="d2b4f-134">Die devtools entsprechen der Sprache, in der Sie Microsoft Edge verwenden `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="d2b4f-134">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

> ##### <span data-ttu-id="d2b4f-135">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="d2b4f-135">Figure 2</span></span>  
> <span data-ttu-id="d2b4f-136">Das devtools in Deutsch</span><span class="sxs-lookup"><span data-stu-id="d2b4f-136">The DevTools in German</span></span>  
> ![Das devtools in Deutsch][ImageLocalizedGerman]  

<span data-ttu-id="d2b4f-138">Wenn Sie das devtools in einer anderen Sprache als den verfügbaren verwenden möchten, senden Sie uns eine [Tweet][PostTweetEdgeDevTools] oder klicken Sie auf das [Feedback](#feedback) -Symbol.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-138">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Feedback](#feedback) icon.</span></span>  

<span data-ttu-id="d2b4f-139">Chrom Problem [#941561][crbug941561]</span><span class="sxs-lookup"><span data-stu-id="d2b4f-139">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="d2b4f-140">webhint Microsoft Edge-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="d2b4f-140">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="d2b4f-141">Mit der webhint Microsoft Edge-Erweiterung können Sie Ihre Webseite auf einfache Weise überprüfen und Feedback zu Barrierefreiheit, Browserkompatibilität, Sicherheit, Leistung und vielem mehr in der devtools erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-141">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="d2b4f-142">Weitere Informationen finden Sie unter [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="d2b4f-142">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="d2b4f-143">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="d2b4f-143">Figure 3</span></span>  
> <span data-ttu-id="d2b4f-144">Die Registerkarte "Hinweise" im devtools, wenn die webhint-Browser Erweiterung installiert ist</span><span class="sxs-lookup"><span data-stu-id="d2b4f-144">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![Die Registerkarte "Hinweise" im devtools, wenn die webhint-Browser Erweiterung installiert ist][ImageHintsTabWebhintExtension]  

<span data-ttu-id="d2b4f-146">[Testen Sie die webhint-Browser Erweiterung in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="d2b4f-146">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="d2b4f-147">Nachdem Sie die Erweiterung installiert haben, öffnen Sie das devtools, und wählen Sie die Registerkarte Hinweise aus.  Führen Sie von hier aus eine anpassbare Website Überprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-147">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="d2b4f-148">Besuchen Sie [webhint.IO][WebhintBrowserExtension] , um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-148">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <span data-ttu-id="d2b4f-149">3D View</span><span class="sxs-lookup"><span data-stu-id="d2b4f-149">3D View</span></span>  

<span data-ttu-id="d2b4f-150">Verwenden Sie die **3D-Ansicht** , um Ihre Webanwendung zu debuggen, indem Sie durch das [Dokumentobjektmodell \ (DOM \)][MDNDocumentObjectModel] oder den Stapel Kontext des [z-Index][MDNZIndex] navigieren.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-150">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="d2b4f-151">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="d2b4f-151">Figure 4</span></span>  
> <span data-ttu-id="d2b4f-152">Die 3D-Ansicht im devtools</span><span class="sxs-lookup"><span data-stu-id="d2b4f-152">The 3D View in the DevTools</span></span>  
> ![Die 3D-Ansicht im devtools][Image3DView]  

<span data-ttu-id="d2b4f-154">Wenn Sie auf die 3D-Ansicht zugreifen möchten, navigieren Sie zu `edge://flags` und stellen Sie sicher, dass das Kennzeichen **Entwickler Tools Experimente** auf **aktiviert**festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-154">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="d2b4f-155">Starten Sie Microsoft Edge neu, und öffnen Sie das devtools.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-155">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="d2b4f-156">Drücken Sie `F1` im devtools oder wechseln Sie zu **Einstellungen**, navigieren Sie zu **Experimenten** , und aktivieren Sie das Kontrollkästchen **3D-Ansicht aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="d2b4f-156">Press `F1` in the DevTools or go to **Settings**, navigate to **Experiments** section, and check the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="d2b4f-157">Drücken Sie jetzt `Ctrl`  +  `Shift`  +  `P` , geben Sie in **3D-Ansicht** ein, und wählen Sie **3D-Ansicht**anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-157">Now, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="d2b4f-158">Wir arbeiten an der Benutzeroberfläche und fügen der 3D-Ansicht Weitere Funktionen hinzu, damit Sie uns Ihr [Feedback](#feedback)senden können.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-158">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#feedback).</span></span>  

<span data-ttu-id="d2b4f-159">Chrom Problem [#987787][crbug987787]</span><span class="sxs-lookup"><span data-stu-id="d2b4f-159">Chromium issue [#987787][crbug987787]</span></span>

### <span data-ttu-id="d2b4f-160">Visual Studio-Code Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="d2b4f-160">Visual Studio Code extensions</span></span>  

<span data-ttu-id="d2b4f-161">Das devtools-Team hat auch einige Erweiterungen für [Visual Studio-Code \ (vs-Code \)][VisualStudioCode] veröffentlicht, mit denen Sie die Leistung des devtools direkt aus Ihrem Text-Editor verwenden können!</span><span class="sxs-lookup"><span data-stu-id="d2b4f-161">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="d2b4f-162">Schauen Sie sich die folgenden Erweiterungen an:</span><span class="sxs-lookup"><span data-stu-id="d2b4f-162">Check out the extensions below:</span></span>  

#### <span data-ttu-id="d2b4f-163">Elemente für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d2b4f-163">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="d2b4f-164">Verwenden Sie das Elements-Tool aus dem vs-Code, indem Sie die [Elemente für Microsoft Edge \ (Chrom \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] vs-Code Erweiterung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-164">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="d2b4f-165">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="d2b4f-165">Figure 5</span></span>  
> <span data-ttu-id="d2b4f-166">Das Tool ' Elemente ' im vs-Code mit den Elementen für Microsoft Edge Extension</span><span class="sxs-lookup"><span data-stu-id="d2b4f-166">The Elements tool in VS Code using the Elements for Microsoft Edge extension</span></span>  
> ![Das Tool ' Elemente ' im vs-Code mit den Elementen für Microsoft Edge Extension][ImageElementsVisualStudioCode]  

<span data-ttu-id="d2b4f-168">Weitere Informationen finden Sie unter [Elemente für Microsoft Edge vs Code Extension][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="d2b4f-168">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="d2b4f-169">Debugger für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d2b4f-169">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="d2b4f-170">Debuggen Sie mit dem [Debugger für Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] vs Code Extension JavaScript, das in Microsoft Edge ausgeführt wird, direkt von vs-Code!</span><span class="sxs-lookup"><span data-stu-id="d2b4f-170">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="d2b4f-171">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="d2b4f-171">Figure 6</span></span>  
> <span data-ttu-id="d2b4f-172">Der Debugger für Microsoft Edge Extension in vs-Code</span><span class="sxs-lookup"><span data-stu-id="d2b4f-172">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![Der Debugger für Microsoft Edge Extension in vs-Code][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="d2b4f-174">Weitere Informationen finden Sie unter [Debuggen von Microsoft Edge aus vs-Code][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="d2b4f-174">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="d2b4f-175">webhint</span><span class="sxs-lookup"><span data-stu-id="d2b4f-175">webhint</span></span>  

<span data-ttu-id="d2b4f-176">Die [webhint][VisualStudioMarketplaceWebhintExtension] vs-Code Erweiterung verwendet `webhint` , um Ihre Webseite zu verbessern, während Sie Sie schreiben!</span><span class="sxs-lookup"><span data-stu-id="d2b4f-176">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="d2b4f-177">Mit dieser Erweiterung wird die Diagnose für Ihre Arbeitsbereichsdateien basierend auf der Analyse ausgeführt und gemeldet `webhint` .</span><span class="sxs-lookup"><span data-stu-id="d2b4f-177">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="d2b4f-178">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="d2b4f-178">Figure 7</span></span>  
> <span data-ttu-id="d2b4f-179">Die webhint vs-Code Erweiterung, die eine TSX-Datei im vs-Code analysiert</span><span class="sxs-lookup"><span data-stu-id="d2b4f-179">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![Die webhint vs-Code Erweiterung, die eine TSX-Datei im vs-Code analysiert][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="d2b4f-181">[Weitere Informationen zur Erweiterung des vs-Code webhints][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="d2b4f-181">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="d2b4f-182">Integration von Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d2b4f-182">Visual Studio integration</span></span>
<span data-ttu-id="d2b4f-183">Verwenden Sie in Visual Studio 2019, Version 16,2 oder höher, den Visual Studio-Debugger zum Debuggen von JavaScript, das in Microsoft Edge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-183">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="d2b4f-184">[Laden Sie Visual Studio 2019 herunter][MicrosoftVisualStudioDownloads] , um dieses Feature auszuprobieren!</span><span class="sxs-lookup"><span data-stu-id="d2b4f-184">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="d2b4f-185">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="d2b4f-185">Figure 8</span></span>  
> <span data-ttu-id="d2b4f-186">Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, dev oder Beta</span><span class="sxs-lookup"><span data-stu-id="d2b4f-186">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![Visual Studio mit der Option zum Starten Ihrer Web-App in Microsoft Edge Canary, dev oder Beta][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="d2b4f-188">[Lesen Sie unseren Blogbeitrag, um zu erfahren, wie Sie Microsoft Edge in Visual Studio debuggen][MicrosoftVisualStudioBlogDebugJavascript]können.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-188">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <span data-ttu-id="d2b4f-189">Nachrichten zur Präventions Konsole</span><span class="sxs-lookup"><span data-stu-id="d2b4f-189">Tracking prevention Console messages</span></span>  

<span data-ttu-id="d2b4f-190">Die nach Verfolgungs Verhinderung ist ein einzigartiges Feature in Microsoft Edge, das Sie davor schützt, von Websites, die Sie noch nicht besucht haben, nachverfolgt</span><span class="sxs-lookup"><span data-stu-id="d2b4f-190">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="d2b4f-191">Die Standardeinstellung für die nach Verfolgungs Verhinderung ist der Modus "ausgeglichen", der Drittanbieter-Tracker und bekannte bösartige Tracker für eine Erfahrung blockiert, die Datenschutz und Web-Kompatibilität abgleicht.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-191">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="d2b4f-192">Damit Sie mehr über die Kompatibilität Ihrer Webseite erfahren, wenn bestimmte Tracker blockiert sind, haben wir auch Warnmeldungen in der Konsole hinzugefügt, wenn ein Tracker blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-192">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="d2b4f-193">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="d2b4f-193">Figure 9</span></span>  
> <span data-ttu-id="d2b4f-194">Nachrichten in der Konsole, wenn die nach Verfolgungs Prävention den Zugriff auf den Speicher für einen Tracker blockiert</span><span class="sxs-lookup"><span data-stu-id="d2b4f-194">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Nachrichten in der Konsole, wenn die nach Verfolgungs Prävention den Zugriff auf den Speicher für einen Tracker blockiert][ImageTrackingPrevention]  

<span data-ttu-id="d2b4f-196">[Weitere Informationen finden Sie unter Verhinderung von Nachverfolgung und dem Gleichgewichtzwischen Datenschutz und Web-Kompatibilität][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="d2b4f-196">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="d2b4f-197">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="d2b4f-197">Announcements from the Chromium project</span></span>  

<span data-ttu-id="d2b4f-198">In den folgenden Abschnitten werden weitere in Microsoft Edge 80 verfügbare Features angekündigt, die zum Open-Source-Projekt Chromium beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-198">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="d2b4f-199">Unterstützung für Let-und Class-Deklarationen in der Konsole</span><span class="sxs-lookup"><span data-stu-id="d2b4f-199">Support for let and class redeclarations in the Console</span></span>   

<span data-ttu-id="d2b4f-200">Die Konsole unterstützt jetzt erneute Deklarationen von `let` und- `class` Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-200">The Console now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="d2b4f-201">Die Unfähigkeit, erneut zu deklarieren, war ein häufiges Ärgernis für Webentwickler, die die Konsole zum Experimentieren mit neuem JavaScript-Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-201">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="d2b4f-202">Das erneute Deklarieren einer `let` oder `class` -Anweisung in einem Skript außerhalb der Konsole oder in einer einzelnen Konsoleneingabe führt weiterhin zu einer `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="d2b4f-202">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="d2b4f-203">Bei der erneuten Deklaration einer lokalen Variablen mit `let` hat die Konsole beispielsweise einen Fehler ausgelöst:</span><span class="sxs-lookup"><span data-stu-id="d2b4f-203">For example, previously, when redeclaring a local variable with `let`, the Console threw an error:</span></span>  

> ##### <span data-ttu-id="d2b4f-204">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="d2b4f-204">Figure 10</span></span>  
> <span data-ttu-id="d2b4f-205">Die Konsole in Microsoft Edge 79 zeigt, dass die Let-erneute Deklaration fehlschlägt</span><span class="sxs-lookup"><span data-stu-id="d2b4f-205">The Console in Microsoft Edge 79 showing that the let redeclaration fails</span></span>  
> ![Die Konsole in Microsoft Edge 79 zeigt, dass die Let-erneute Deklaration fehlschlägt][ImageConsoleRedeclarationFails]  

<span data-ttu-id="d2b4f-207">Die Konsole ermöglicht nun die erneute Deklaration:</span><span class="sxs-lookup"><span data-stu-id="d2b4f-207">Now, the Console allows the redeclaration:</span></span>  

> ##### <span data-ttu-id="d2b4f-208">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="d2b4f-208">Figure 11</span></span>  
> <span data-ttu-id="d2b4f-209">Die Konsole in Microsoft Edge 80 zeigt, dass die Let-erneute Deklaration erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="d2b4f-209">The Console in Microsoft Edge 80 showing that the let redeclaration succeeds</span></span>  
> ![Die Konsole in Microsoft Edge 80 zeigt, dass die Let-erneute Deklaration erfolgreich ist][ImageConsoleRedeclarationSucceeds]  

<span data-ttu-id="d2b4f-211">Chrom Problem [#1004193][crbug1004193]</span><span class="sxs-lookup"><span data-stu-id="d2b4f-211">Chromium issue [#1004193][crbug1004193]</span></span>  

### <span data-ttu-id="d2b4f-212">Verbessertes Webassembly-Debugging</span><span class="sxs-lookup"><span data-stu-id="d2b4f-212">Improved WebAssembly debugging</span></span>   

<span data-ttu-id="d2b4f-213">DevTools hat mit der Unterstützung des [Dwarf-Debugging-Standards][DwarfHome]begonnen, was mehr Unterstützung für die schrittweise Codierung, das Festlegen von Haltepunkten und das Auflösen von Stapelablaufverfolgungen in ihren Quellsprachen in devtools bedeutet.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-213">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
> ##### Figure  
> The new DWARF-powered WebAssembly debugging  
> ![The new DWARF-powered WebAssembly debugging][ImageDwarfPoweredWebAssemblyDebugging]  
-->  

### <span data-ttu-id="d2b4f-214">Netzwerk Panel-Updates</span><span class="sxs-lookup"><span data-stu-id="d2b4f-214">Network panel updates</span></span>   

#### <span data-ttu-id="d2b4f-215">Anfordern von Initiator-Chains auf der Registerkarte "Initiator"</span><span class="sxs-lookup"><span data-stu-id="d2b4f-215">Request Initiator Chains in the Initiator tab</span></span>   

<span data-ttu-id="d2b4f-216">Sie können nun die Initiatoren und Abhängigkeiten einer Netzwerkanforderung als geschachtelte Liste anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-216">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="d2b4f-217">Dies kann Ihnen helfen zu verstehen, warum eine Ressource angefordert wurde, oder welche Netzwerkaktivität eine bestimmte Ressource (wie ein Skript \) verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-217">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

> ##### <span data-ttu-id="d2b4f-218">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="d2b4f-218">Figure 12</span></span>  
> <span data-ttu-id="d2b4f-219">Eine Anforderungs Initiator-Kette auf der Registerkarte "Initiator"</span><span class="sxs-lookup"><span data-stu-id="d2b4f-219">A Request Initiator Chain in the Initiator tab</span></span>  
> ![Eine Anforderungs Initiator-Kette auf der Registerkarte "Initiator"][ImageRequestInitiatorChain]  

<span data-ttu-id="d2b4f-221">Klicken Sie nach dem [Protokollieren der Netzwerkaktivität in der Netzwerksteuerung][DevToolsNetworkIndex]auf eine Ressource, und wechseln Sie dann zur Registerkarte **Initiator** , um die **Anforderungs initiatorkette**anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="d2b4f-221">After [logging network activity in the Network panel][DevToolsNetworkIndex], click a resource and then go to the **Initiator** tab to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="d2b4f-222">Die **geprüfte Ressource** ist fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-222">The **inspected resource** is bold.</span></span>  <span data-ttu-id="d2b4f-223">Im obigen Screenshot `ai.2.min.js` befindet sich die geprüfte Ressource.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-223">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="d2b4f-224">Die Ressourcen oberhalb der geprüften Ressource sind die **Initiatoren**.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-224">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="d2b4f-225">Im obigen Screenshot `https://www.microsoftedgeinsider.com` ist der Initiator von `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="d2b4f-225">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="d2b4f-226">Mit anderen Worten: `https://www.microsoftedgeinsider.com` Ursache für die Netzwerkanforderung `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="d2b4f-226">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="d2b4f-227">Die Ressourcen unterhalb der geprüften Ressource sind die **Abhängigkeiten**.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-227">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="d2b4f-228">Im obigen Screenshot `https://dc.services.visualstudio.com/v2/track` ist eine Abhängigkeit von `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="d2b4f-228">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="d2b4f-229">Mit anderen Worten: `ai.2.min.js` Ursache für die Netzwerkanforderung `https://dc.services.visualstudio.com/v2/track` .</span><span class="sxs-lookup"><span data-stu-id="d2b4f-229">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="d2b4f-230">Auf Initiator-und Abhängigkeitsinformationen kann auch zugegriffen werden, indem Sie `Shift` auf Netzwerkressourcen halten und dann darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-230">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="d2b4f-231">Weitere Informationen finden Sie unter [Anzeigen von Initiatoren und Abhängigkeiten][DevToolsNetworkReferenceViewInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="d2b4f-231">See [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="d2b4f-232">Chrom Problem [#842488][crbug842488]</span><span class="sxs-lookup"><span data-stu-id="d2b4f-232">Chromium issue [#842488][crbug842488]</span></span>  

#### <span data-ttu-id="d2b4f-233">Markieren der ausgewählten Netzwerkanforderung in der Übersicht</span><span class="sxs-lookup"><span data-stu-id="d2b4f-233">Highlight the selected network request in the Overview</span></span>   

<span data-ttu-id="d2b4f-234">Nachdem Sie auf eine Netzwerkressource klicken, um Sie zu überprüfen, fügt das Netzwerk Panel nun einen blauen Rahmen um die Ressource in der **Übersicht**ein.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-234">After you click a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="d2b4f-235">Dies kann Ihnen helfen zu erkennen, ob die Netzwerkanforderung früher oder später als erwartet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-235">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

> ##### <span data-ttu-id="d2b4f-236">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="d2b4f-236">Figure 13</span></span>  
> <span data-ttu-id="d2b4f-237">Der Übersichtsbereich, der die überprüfte Ressource markiert</span><span class="sxs-lookup"><span data-stu-id="d2b4f-237">The Overview pane highlighting the inspected resource</span></span>  
> ![Der Übersichtsbereich, der die überprüfte Ressource markiert][ImageOverviewPaneInspectedResource]  

<span data-ttu-id="d2b4f-239">Chrom Problem [#988253][crbug988253]</span><span class="sxs-lookup"><span data-stu-id="d2b4f-239">Chromium issue [#988253][crbug988253]</span></span>  

#### <span data-ttu-id="d2b4f-240">URL-und Pfad Spalten im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="d2b4f-240">URL and path columns in the Network panel</span></span>   

<span data-ttu-id="d2b4f-241">Verwenden Sie die Spalten neuer **Pfad** und **URL** im **Netzwerk** Panel, um den absoluten Pfad oder die vollständige URL der einzelnen Netzwerkressourcen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-241">Use the new **Path** and **URL** columns in the **Network** panel to see the absolute path or full URL of each network resource.</span></span>  

> ##### <span data-ttu-id="d2b4f-242">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="d2b4f-242">Figure 14</span></span>  
> <span data-ttu-id="d2b4f-243">Die Spalten ' neuer Pfad ' und ' URL ' im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="d2b4f-243">The new Path and URL columns in the Network panel</span></span>  
> ![Die Spalten ' neuer Pfad ' und ' URL ' im Netzwerk Panel][ImagePathNetworkPanel]  

<span data-ttu-id="d2b4f-245">Klicken Sie mit der rechten Maustaste auf die Tabelle Überschrift **Wasserfall** , und wählen Sie **Pfad** oder **URL** aus, um die neuen Spalten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-245">Right-click the **Waterfall** table header and select **Path** or **URL** to show the new columns.</span></span>  

<span data-ttu-id="d2b4f-246">Chrom Problem [#993366][crbug993366]</span><span class="sxs-lookup"><span data-stu-id="d2b4f-246">Chromium issue [#993366][crbug993366]</span></span>  

#### <span data-ttu-id="d2b4f-247">Aktualisierte Benutzer-Agent-Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="d2b4f-247">Updated User-Agent strings</span></span>   

<span data-ttu-id="d2b4f-248">DevTools unterstützt das Festlegen einer benutzerdefinierten Benutzer-Agent-Zeichenfolge über die Registerkarte **Netzwerkbedingungen** .  Die Benutzer-Agent-Zeichenfolge wirkt `User-Agent` sich auf den an Netzwerkressourcen angefügten HTTP-Header und auch auf den Wert von aus `navigator.userAgent` .</span><span class="sxs-lookup"><span data-stu-id="d2b4f-248">DevTools supports setting a custom User-Agent string through the **Network Conditions** tab.  The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="d2b4f-249">Die vordefinierten Benutzer-Agent-Zeichenfolgen wurden so aktualisiert, dass Sie den modernen Browserversionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-249">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

> ##### <span data-ttu-id="d2b4f-250">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="d2b4f-250">Figure 15</span></span>  
> <span data-ttu-id="d2b4f-251">Das Menü "Benutzer-Agent" auf der Registerkarte "Netzwerkbedingungen"</span><span class="sxs-lookup"><span data-stu-id="d2b4f-251">The User Agent menu in the Network Conditions tab</span></span>  
> ![Das Menü "Benutzer-Agent" auf der Registerkarte "Netzwerkbedingungen"][ImageUserAgentNetworkConditionsTab]  

<span data-ttu-id="d2b4f-253">Um auf **Netzwerkbedingungen**zuzugreifen, [Öffnen Sie das Befehlsmenü][DevToolsCommandMenuIndex] , und führen Sie den `Show Network Conditions` Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-253">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="d2b4f-254">Sie können auch [Benutzer-Agent-Zeichenfolgen im Gerätemodus einrichten][DevToolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="d2b4f-254">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="d2b4f-255">Chrom Problem [#1029031][crbug1029031]</span><span class="sxs-lookup"><span data-stu-id="d2b4f-255">Chromium issue [#1029031][crbug1029031]</span></span>  

### <span data-ttu-id="d2b4f-256">Audits-Panel-Updates</span><span class="sxs-lookup"><span data-stu-id="d2b4f-256">Audits panel updates</span></span>   

#### <span data-ttu-id="d2b4f-257">Neue Konfigurations-UI</span><span class="sxs-lookup"><span data-stu-id="d2b4f-257">New configuration UI</span></span>   

<span data-ttu-id="d2b4f-258">Die Benutzeroberfläche der Konfiguration verfügt über ein neues, reaktionsfähiges Design, und die Optionen für die Einschränkungs Konfiguration wurden vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-258">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="d2b4f-259">Weitere Informationen zu den Änderungen beim Einschränken der Benutzeroberfläche finden Sie unter [Drosselung des Überwachungs Panels][GitHubGoogleChromeDevToolsAuditsPanelThrottling] .</span><span class="sxs-lookup"><span data-stu-id="d2b4f-259">See [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling] for more information on the throttling UI changes.</span></span>  

> ##### <span data-ttu-id="d2b4f-260">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="d2b4f-260">Figure 16</span></span>  
> <span data-ttu-id="d2b4f-261">Die neue Benutzeroberfläche für die Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d2b4f-261">The new configuration UI</span></span>  
> ![Die neue Benutzeroberfläche für die Konfiguration][ImageConfigurationUI]  

### <span data-ttu-id="d2b4f-263">Updates für Coverage-Registerkarten</span><span class="sxs-lookup"><span data-stu-id="d2b4f-263">Coverage tab updates</span></span>   

#### <span data-ttu-id="d2b4f-264">Pro-Funktion-oder pro-Block-Abdeckungs Modi</span><span class="sxs-lookup"><span data-stu-id="d2b4f-264">Per-function or per-block coverage modes</span></span>   

<span data-ttu-id="d2b4f-265">Die [Registerkarte Coverage][DevToolsCoverageIndex] enthält ein neues Dropdownmenü, in dem Sie angeben können, ob Codeabdeckungsdaten **pro Funktion** oder **pro Block**erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-265">The [Coverage tab][DevToolsCoverageIndex] has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="d2b4f-266">**Pro-Block** -Abdeckung ist detaillierter, aber auch weitaus teurer zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-266">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="d2b4f-267">DevTools verwendet jetzt standardmäßig **pro Funktion** Coverage.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-267">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="d2b4f-268">Je nachdem, ob Sie **pro Funktion** oder **pro Block** Modus verwenden, werden möglicherweise große Unterschiede bei der Codeabdeckung in HTML-Dateien angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-268">You may see large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="d2b4f-269">Bei Verwendung des **pro-Funktions** Modus werden Inlineskripts in HTML-Dateien als Funktionen behandelt.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-269">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="d2b4f-270">Wenn das Skript überhaupt ausgeführt wird, markiert devtools das gesamte Skript als verwendeten Code.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-270">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="d2b4f-271">Nur wenn das Skript überhaupt nicht ausgeführt wird, kennzeichnet devtools das Skript als unbenutzten Code.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-271">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

> ##### <span data-ttu-id="d2b4f-272">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="d2b4f-272">Figure 17</span></span>  
> <span data-ttu-id="d2b4f-273">Dropdownmenü "Coverage-Modus"</span><span class="sxs-lookup"><span data-stu-id="d2b4f-273">The coverage mode dropdown menu</span></span>  
> ![Dropdownmenü "Coverage-Modus"][ImageCoverageMode]  

#### <span data-ttu-id="d2b4f-275">Coverage muss nun durch ein Seiten-Reload initiiert werden</span><span class="sxs-lookup"><span data-stu-id="d2b4f-275">Coverage must now be initiated by a page reload</span></span>   

<span data-ttu-id="d2b4f-276">Das Umschalten der Codeabdeckung ohne das erneute Laden einer Seite wurde entfernt, da die Abdeckungsdaten unzuverlässig waren.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-276">Toggling code coverage without a page reload has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="d2b4f-277">Beispielsweise kann eine Funktion als unbenutzt gemeldet werden, wenn die Laufzeit vor langer Zeit war und der V8-Garbage Collector Sie bereinigt hat.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-277">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="d2b4f-278">Chrom Problem [#1004203][crbug1004203]</span><span class="sxs-lookup"><span data-stu-id="d2b4f-278">Chromium issue [#1004203][crbug1004203]</span></span>  

## <span data-ttu-id="d2b4f-279">Feedback senden</span><span class="sxs-lookup"><span data-stu-id="d2b4f-279">Feedback</span></span>   



<span data-ttu-id="d2b4f-280">So besprechen Sie die neuen Features und Änderungen in diesem Beitrag oder alles, was mit devtools zu tun hat:</span><span class="sxs-lookup"><span data-stu-id="d2b4f-280">To discuss the new features and changes in this post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="d2b4f-281">Senden Sie Ihr Feedback über das **Feedback** -Symbol im devtools</span><span class="sxs-lookup"><span data-stu-id="d2b4f-281">Send your feedback using the **Feedback** icon in the DevTools</span></span>  

> ##### <span data-ttu-id="d2b4f-282">Abbildung 18</span><span class="sxs-lookup"><span data-stu-id="d2b4f-282">Figure 18</span></span>
> <span data-ttu-id="d2b4f-283">Das **Feedback** Symbol in der Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="d2b4f-283">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
> ![Das \* \* Feedback \* \*-Symbol in der Microsoft Edge-devtools][ImageFeedbackIcon]  

*   <span data-ttu-id="d2b4f-285">Tweet bei [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="d2b4f-285">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="d2b4f-286">Einen Vorschlag an [das gewünschte Web][TheWebWeWant] senden</span><span class="sxs-lookup"><span data-stu-id="d2b4f-286">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="d2b4f-287">Datei Fehler in diesem Dokument im [Edge-Entwickler-][GitHubMicrosoftDocsEdgeDeveloperNewIssue] Repository</span><span class="sxs-lookup"><span data-stu-id="d2b4f-287">File bugs on this document in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

## <span data-ttu-id="d2b4f-288">Herunterladen der Microsoft Edge Preview-Kanäle</span><span class="sxs-lookup"><span data-stu-id="d2b4f-288">Download the Microsoft Edge preview channels</span></span>   

<span data-ttu-id="d2b4f-289">Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-289">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="d2b4f-290">Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-290">The preview channels give you access to the latest DevTools features.</span></span>  

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
[ImageFeedbackIcon]: ../../images/2019/12/feedback-icon.msft.png "Abbildung 18: das * * Feedback * *-Symbol in der Microsoft Edge-devtools"

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
> <span data-ttu-id="d2b4f-348">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-348">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d2b4f-349">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/updates/2019/12/devtools/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools & Lighthouse) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d2b4f-349">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="d2b4f-351">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d2b4f-351">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

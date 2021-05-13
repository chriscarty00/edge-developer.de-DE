---
description: Eine umfassende Referenz zu Barrierefreiheitsfeatures in Microsoft Edge DevTools.
title: Referenz zur Barrierefreiheit
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: a82dec6ffd7e3fb44143ea103fc9756afcd1a161
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564574"
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
# <a name="accessibility-reference"></a><span data-ttu-id="41aff-104">Referenz zur Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="41aff-104">Accessibility reference</span></span>  

<span data-ttu-id="41aff-105">Diese Seite ist eine umfassende Referenz zu Barrierefreiheitsfeatures in Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="41aff-105">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="41aff-106">Es richtet sich an Webentwickler, die:</span><span class="sxs-lookup"><span data-stu-id="41aff-106">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="41aff-107">Verfügen Sie über grundlegende Kenntnisse von DevTools, z. B. wie Sie es öffnen.</span><span class="sxs-lookup"><span data-stu-id="41aff-107">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="41aff-108">Sind mit [Barrierefreiheitsgrundsätzen und bewährten Methoden vertraut.][MDNAccessibility]</span><span class="sxs-lookup"><span data-stu-id="41aff-108">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  
    
<span data-ttu-id="41aff-109">Dieser Verweis soll Ihnen dabei helfen, alle in DevTools verfügbaren Tools zu entdecken, mit deren Hilfe Sie die Barrierefreiheit einer Seite untersuchen können.</span><span class="sxs-lookup"><span data-stu-id="41aff-109">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="41aff-110">Wenn Sie Hilfe zum Navigieren in DevTools mit einer Hilfstechnologie wie einer Bildschirmlesehilfe suchen, navigieren Sie zu [Navigieren Microsoft Edge DevTools with Assistive Technology][DevtoolsAccessibilityNavigation].</span><span class="sxs-lookup"><span data-stu-id="41aff-110">If you are looking for help on navigating DevTools with an assistive technology like a screen reader, navigate to [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation].</span></span>  

## <a name="overview-of-accessibility-features-in-microsoft-edge-devtools"></a><span data-ttu-id="41aff-111">Übersicht über Barrierefreiheitsfeatures in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="41aff-111">Overview of accessibility features in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="41aff-112">In diesem Abschnitt wird erläutert, wie DevTools in Ihr allgemeines Toolkit für Barrierefreiheit passt.</span><span class="sxs-lookup"><span data-stu-id="41aff-112">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="41aff-113">Wenn Sie bestimmen, ob auf eine Seite zugegriffen werden kann, müssen Sie zwei allgemeine Fragen berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="41aff-113">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="41aff-114">Sind Sie in der Lage, mit einer Tastatur oder einer [Bildschirmleseausgabe auf der Seite zu navigieren?][MDNScreenReader]</span><span class="sxs-lookup"><span data-stu-id="41aff-114">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="41aff-115">Sind die Elemente der Seite für Bildschirmlesegeräte ordnungsgemäß gekennzeichnet?</span><span class="sxs-lookup"><span data-stu-id="41aff-115">Are the elements of the page properly marked up for screen readers?</span></span>  
    
<span data-ttu-id="41aff-116">Im Allgemeinen sollten DevTools Ihnen bei der Behebung von Fehlern im Zusammenhang mit fragen #2 helfen, da diese Fehler einfach automatisiert zu erkennen sind.</span><span class="sxs-lookup"><span data-stu-id="41aff-116">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="41aff-117">Fragen #1 ist genauso wichtig, aber leider hilft Ihnen DevTools dort nicht.</span><span class="sxs-lookup"><span data-stu-id="41aff-117">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="41aff-118">Die einzige Möglichkeit, Fehler im Zusammenhang mit fragen #1 zu finden, besteht in der Verwendung einer Seite mit einer Tastatur oder einer Bildschirmleseausgabe selbst.</span><span class="sxs-lookup"><span data-stu-id="41aff-118">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--To learn more, navigate to [How To Do An Accessibility Review][AccessibilityReview].  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <a name="audit-the-accessibility-of-a-page"></a><span data-ttu-id="41aff-119">Überwachen der Barrierefreiheit einer Seite</span><span class="sxs-lookup"><span data-stu-id="41aff-119">Audit the accessibility of a page</span></span>  

> [!NOTE]
> <span data-ttu-id="41aff-120">Das **Tool Überwachungen** stellt Links zu Inhalten zur Verfügung, die auf Websites von Drittanbietern gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="41aff-120">The **Audits** tool provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="41aff-121">Microsoft ist nicht verantwortlich und hat keine Kontrolle über den Inhalt dieser Websites und alle möglicherweise gesammelten Daten.</span><span class="sxs-lookup"><span data-stu-id="41aff-121">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="41aff-122">Verwenden Sie im Allgemeinen den Bereich Überwachungen, um zu ermitteln, ob:</span><span class="sxs-lookup"><span data-stu-id="41aff-122">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="41aff-123">Eine Seite ist für Bildschirmlesegeräte ordnungsgemäß gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="41aff-123">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="41aff-124">Die Textelemente auf einer Seite verfügen über ausreichende Kontrastverhältnisse.</span><span class="sxs-lookup"><span data-stu-id="41aff-124">The text elements on a page have sufficient contrast ratios.</span></span>  <span data-ttu-id="41aff-125">Navigieren Sie [zu Anzeigen des Kontrastverhältnisses eines Textelements in der Farbauswahl.](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker)</span><span class="sxs-lookup"><span data-stu-id="41aff-125">Navigate to [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="41aff-126">So überwachen Sie eine Seite:</span><span class="sxs-lookup"><span data-stu-id="41aff-126">To audit a page:</span></span>  

1.  <span data-ttu-id="41aff-127">Navigieren Sie zu der URL, die Sie überwachen möchten.</span><span class="sxs-lookup"><span data-stu-id="41aff-127">Navigate to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="41aff-128">Wählen Sie in DevTools das **Tool Überwachungen** aus.</span><span class="sxs-lookup"><span data-stu-id="41aff-128">In DevTools, choose the **Audits** tool.</span></span>  <span data-ttu-id="41aff-129">DevTools zeigt Ihnen verschiedene Konfigurationsoptionen.</span><span class="sxs-lookup"><span data-stu-id="41aff-129">DevTools shows you various configuration options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Konfigurieren von Überwachungen" lightbox="../media/accessibility-audits-pane.msft.png":::
       <span data-ttu-id="41aff-131">Konfigurieren von Überwachungen</span><span class="sxs-lookup"><span data-stu-id="41aff-131">Configure audits</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="41aff-132">Die Screenshots in diesem Abschnitt wurden mit Microsoft Edge Version 79 erstellt.</span><span class="sxs-lookup"><span data-stu-id="41aff-132">The screenshots in this section were taken with Microsoft Edge version 79.</span></span>  <span data-ttu-id="41aff-133">Sie können überprüfen, welche Version Sie unter `edge://version` ausführen.</span><span class="sxs-lookup"><span data-stu-id="41aff-133">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="41aff-134">Die **Benutzeroberfläche** des Überwachungsinstruments sieht in früheren Versionen von Microsoft Edge anders aus, der allgemeine Workflow ist jedoch identisch.</span><span class="sxs-lookup"><span data-stu-id="41aff-134">The **Audits** tool UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="41aff-135">Wählen **Sie für**Gerät Mobile **aus,** wenn Sie ein mobiles Gerät simulieren möchten.</span><span class="sxs-lookup"><span data-stu-id="41aff-135">For **Device**, choose **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="41aff-136">Mit dieser Option wird die Zeichenfolge des Benutzer-Agents geändert und die Größe des Viewports geändert.</span><span class="sxs-lookup"><span data-stu-id="41aff-136">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="41aff-137">Wenn die mobile Version der Seite anders als die Desktopversion angezeigt wird, kann diese Option erhebliche Auswirkungen auf die Ergebnisse Ihrer Überwachung haben.</span><span class="sxs-lookup"><span data-stu-id="41aff-137">If the mobile version of the page displays differently than the desktop version, this option may have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="41aff-138">Stellen Sie **im Abschnitt Überwachungen** sicher, dass **Barrierefreiheit** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="41aff-138">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="41aff-139">Deaktivieren Sie die anderen Kategorien, wenn Sie sie aus Ihrem Bericht ausschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="41aff-139">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="41aff-140">Lassen Sie sie aktiviert, wenn Sie andere Möglichkeiten zur Verbesserung der Qualität Ihrer Seite finden möchten.</span><span class="sxs-lookup"><span data-stu-id="41aff-140">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="41aff-141">Im **Abschnitt Einschränkung** können Sie das Netzwerk und die CPU drosseln, was bei der Analyse der Lastleistung hilfreich ist.</span><span class="sxs-lookup"><span data-stu-id="41aff-141">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="41aff-142">Diese Option sollte für Ihre Barrierefreiheitsnote irrelevant sein, sodass Sie die von Ihnen bevorzugten Optionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="41aff-142">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="41aff-143">Mit **dem Kontrollkästchen Storage** löschen können Sie den speicherplatz vor dem Laden der Seite löschen oder den Speicher zwischen Seitenlasten beibehalten.</span><span class="sxs-lookup"><span data-stu-id="41aff-143">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="41aff-144">Diese Option ist wahrscheinlich auch für die Barrierefreiheitsnote irrelevant, sodass Sie die von Ihnen bevorzugten Optionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="41aff-144">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="41aff-145">Wählen **Sie Überwachungen ausführen aus.**</span><span class="sxs-lookup"><span data-stu-id="41aff-145">Choose **Run Audits**.</span></span> <span data-ttu-id="41aff-146">Nach 10 bis 30 Sekunden stellt DevTools einen Bericht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="41aff-146">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="41aff-147">Ihr Bericht enthält verschiedene Tipps, wie Sie die Barrierefreiheit der Seite verbessern können.</span><span class="sxs-lookup"><span data-stu-id="41aff-147">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Ein Bericht" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       <span data-ttu-id="41aff-149">Ein Bericht</span><span class="sxs-lookup"><span data-stu-id="41aff-149">A report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="41aff-150">Wählen Sie eine Überwachung aus, um mehr darüber zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="41aff-150">Choose an audit to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Weitere Informationen zu einer Überwachung" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       <span data-ttu-id="41aff-152">Weitere Informationen zu einer Überwachung</span><span class="sxs-lookup"><span data-stu-id="41aff-152">More information about an audit</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="41aff-153">Wählen **Sie Weitere Informationen aus,** um die Dokumentation dieser Überwachung anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="41aff-153">Choose **Learn More** to view the documentation of that audit.</span></span>  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Anzeigen der Dokumentation einer Überwachung" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="41aff-155">Anzeigen der Dokumentation einer Überwachung</span><span class="sxs-lookup"><span data-stu-id="41aff-155">View the documentation of an audit</span></span>  
    :::image-end:::  
    
### <a name="see-also-axe-extension"></a><span data-ttu-id="41aff-156">Siehe auch: aXe-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="41aff-156">See also: aXe extension</span></span>  

<span data-ttu-id="41aff-157">Möglicherweise verwenden Sie lieber die [aXe-Erweiterung][ChromeWebStoreAxe] als das **Überwachungstool.**</span><span class="sxs-lookup"><span data-stu-id="41aff-157">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** tool.</span></span>  
<span data-ttu-id="41aff-158">Die Erweiterung aXe stellt im Allgemeinen dieselben Informationen zur Verfügung, da es sich um das zugrunde liegende Modul handelt, das die Überwachungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41aff-158">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="41aff-159">Die aXe-Erweiterung hat eine andere Benutzeroberfläche und beschreibt Prüfungen geringfügig anders.</span><span class="sxs-lookup"><span data-stu-id="41aff-159">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="41aff-160">Ein Vorteil der Erweiterung aXe gegenüber dem **Tool "Überwachungen"** besteht in der Möglichkeit, fehlerhafte Knoten zu prüfen und zu markieren.</span><span class="sxs-lookup"><span data-stu-id="41aff-160">One advantage that the aXe extension has over the **Audits** tool is that it enables you to inspect and highlight failing nodes.</span></span>  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Die Erweiterung aXe" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   <span data-ttu-id="41aff-162">Die Erweiterung aXe</span><span class="sxs-lookup"><span data-stu-id="41aff-162">The aXe extension</span></span>  
:::image-end:::  

## <a name="the-accessibility-panel"></a><span data-ttu-id="41aff-163">Der Bereich Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="41aff-163">The Accessibility panel</span></span>  

<span data-ttu-id="41aff-164">Im **Bereich** Barrierefreiheit werden die Barrierefreiheitsstruktur, ARIA-Attribute und berechneten Barrierefreiheitseigenschaften von DOM-Knoten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="41aff-164">The **Accessibility** panel is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="41aff-165">So öffnen Sie den **Bereich Barrierefreiheit:**</span><span class="sxs-lookup"><span data-stu-id="41aff-165">To open the **Accessibility** panel:</span></span>  

1.  <span data-ttu-id="41aff-166">Wählen Sie das **Elementtool** aus.</span><span class="sxs-lookup"><span data-stu-id="41aff-166">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="41aff-167">Wählen Sie **in der DOM-Struktur**das Element aus, das Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="41aff-167">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="41aff-168">Wählen Sie den **Bereich Barrierefreiheit** aus.</span><span class="sxs-lookup"><span data-stu-id="41aff-168">Choose the **Accessibility** panel.</span></span>  <span data-ttu-id="41aff-169">Dieser Bereich wird möglicherweise hinter der Schaltfläche **Weitere Registerkarten** ![ \( Weitere ](../media/more-tabs-icon.msft.png) Registerkarten \) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="41aff-169">This panel may be hidden behind the **More Tabs** \(![More Tabs](../media/more-tabs-icon.msft.png)\) button.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Überprüfen des h1-Elements der DevTools-Homepage im Bereich Barrierefreiheit" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="41aff-171">Überprüfen des `h1` Elements der DevTools-Homepage im **Bereich Barrierefreiheit**</span><span class="sxs-lookup"><span data-stu-id="41aff-171">Inspect the `h1` element of the DevTools homepage in the **Accessibility** panel</span></span>  
:::image-end:::  

### <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a><span data-ttu-id="41aff-172">Anzeigen der Position eines Elements in der Barrierefreiheitsstruktur</span><span class="sxs-lookup"><span data-stu-id="41aff-172">View the position of an element in the accessibility tree</span></span>  

<span data-ttu-id="41aff-173">Die [Barrierefreiheitsstruktur][MDNAccessibilityTree] ist eine Teilmenge der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="41aff-173">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="41aff-174">Es enthält nur Elemente aus der DOM-Struktur, die für die Anzeige des Inhalts einer Seite in einer Bildschirmleseausgabe relevant und nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="41aff-174">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="41aff-175">Überprüfen Sie die Position eines Elements in der Barrierefreiheitsstruktur im [Bereich Barrierefreiheit.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="41aff-175">Inspect the position of an element in the accessibility tree from the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Abschnitt "Barrierefreiheitsstruktur"" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="41aff-177">Abschnitt **"Barrierefreiheitsstruktur"**</span><span class="sxs-lookup"><span data-stu-id="41aff-177">The **Accessibility Tree** section</span></span>  
:::image-end:::  

### <a name="view-the-aria-attributes-of-an-element"></a><span data-ttu-id="41aff-178">Anzeigen der ARIA-Attribute eines Elements</span><span class="sxs-lookup"><span data-stu-id="41aff-178">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="41aff-179">ARIA-Attribute stellen sicher, dass die Bildschirmlesegeräte über alle Informationen verfügen, die sie benötigen, um den Inhalt einer Seite ordnungsgemäß darstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="41aff-179">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="41aff-180">Zeigen Sie die ARIA-Attribute eines Elements im Bereich [Barrierefreiheit](#the-accessibility-panel) an.</span><span class="sxs-lookup"><span data-stu-id="41aff-180">View the ARIA attributes of an element in the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Der Abschnitt "ARIA Attributes"" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="41aff-182">Der **Abschnitt "ARIA Attributes"**</span><span class="sxs-lookup"><span data-stu-id="41aff-182">The **ARIA Attributes** section</span></span>  
:::image-end:::  

### <a name="view-the-computed-accessibility-properties-of-an-element"></a><span data-ttu-id="41aff-183">Anzeigen der berechneten Barrierefreiheitseigenschaften eines Elements</span><span class="sxs-lookup"><span data-stu-id="41aff-183">View the computed accessibility properties of an element</span></span>  

> [!NOTE]
> <span data-ttu-id="41aff-184">Wenn Sie nach berechneten CSS-Eigenschaften suchen, navigieren Sie zu [Berechneter][DevtoolsCssReferenceViewActuallyAppliedElements] Bereich.</span><span class="sxs-lookup"><span data-stu-id="41aff-184">If you are looking for computed CSS properties, navigate to [Computed][DevtoolsCssReferenceViewActuallyAppliedElements] panel.</span></span>  

<span data-ttu-id="41aff-185">Einige Barrierefreiheitseigenschaften werden vom Browser dynamisch berechnet.</span><span class="sxs-lookup"><span data-stu-id="41aff-185">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="41aff-186">Diese Eigenschaften werden im Abschnitt **Berechnete Eigenschaften** im **Bereich** Barrierefreiheit angezeigt.</span><span class="sxs-lookup"><span data-stu-id="41aff-186">These properties are displayed in the **Computed Properties** section of the **Accessibility** panel.</span></span>  

<span data-ttu-id="41aff-187">Zeigen Sie die berechneten Barrierefreiheitseigenschaften eines Elements im Bereich [Barrierefreiheit](#the-accessibility-panel) an.</span><span class="sxs-lookup"><span data-stu-id="41aff-187">View the computed accessibility properties of an element in the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Der Abschnitt Berechnete Eigenschaften des Barrierefreiheitsbereichs" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="41aff-189">Der **Abschnitt Berechnete Eigenschaften** des **Barrierefreiheitsbereichs**</span><span class="sxs-lookup"><span data-stu-id="41aff-189">The **Computed Properties** section of the **Accessibility** panel</span></span>  
:::image-end:::  

## <a name="view-the-contrast-ratio-of-a-text-element-in-the-color-picker"></a><span data-ttu-id="41aff-190">Anzeigen des Kontrastverhältnisses eines Textelements in der Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="41aff-190">View the contrast ratio of a text element in the Color Picker</span></span>  

<span data-ttu-id="41aff-191">Einige Personen mit niedriger Sehkraft sehen Bereiche nicht als sehr hell oder sehr dunkel.</span><span class="sxs-lookup"><span data-stu-id="41aff-191">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="41aff-192">Alles wird in der Regel ungefähr mit der gleichen Helligkeit angezeigt, was es schwierig macht, Gliederungen und Kanten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="41aff-192">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="41aff-193">Das Kontrastverhältnis misst den Helligkeitsunterschied zwischen dem Vordergrund und dem Hintergrund des Texts.</span><span class="sxs-lookup"><span data-stu-id="41aff-193">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="41aff-194">Wenn Ihr Text ein niedriges Kontrastverhältnis hat, können diese Benutzer mit niedriger Sehkraft Ihre Website im wahrsten Sinne des Wortes als leeren Bildschirm sehen.</span><span class="sxs-lookup"><span data-stu-id="41aff-194">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="41aff-195">Mit der Farbauswahl können Sie überprüfen, ob Ihr Text die empfohlenen Kontrastverhältnisstufen erfüllt:</span><span class="sxs-lookup"><span data-stu-id="41aff-195">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="41aff-196">Wählen Sie das **Elementtool** aus.</span><span class="sxs-lookup"><span data-stu-id="41aff-196">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="41aff-197">Wählen Sie **in der DOM-Struktur**das Textelement aus, das Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="41aff-197">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Überprüfen eines Absatzes in der DOM-Struktur" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="41aff-199">Überprüfen eines Absatzes in der **DOM-Struktur**</span><span class="sxs-lookup"><span data-stu-id="41aff-199">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="41aff-200">Wählen Sie **im Bereich** Formatvorlagen das Farbfeld neben dem Wert des `color` Elements aus.</span><span class="sxs-lookup"><span data-stu-id="41aff-200">In the **Styles** panel, choose the color square next to the `color` value of the element.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Die Color-Eigenschaft des Elements" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="41aff-202">Die `color` Eigenschaft des Elements</span><span class="sxs-lookup"><span data-stu-id="41aff-202">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="41aff-203">Überprüfen Sie **den Abschnitt Kontrastverhältnis** der Farbauswahl.</span><span class="sxs-lookup"><span data-stu-id="41aff-203">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="41aff-204">Ein Häkchen bedeutet, dass das Element die [Mindestempfehlung erfüllt.][W3CContrastMinimum]</span><span class="sxs-lookup"><span data-stu-id="41aff-204">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="41aff-205">Zwei Häkchen bedeutet, dass es die erweiterte [Empfehlung erfüllt.][W3CContrastEnhanced]</span><span class="sxs-lookup"><span data-stu-id="41aff-205">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="Der Abschnitt Kontrastverhältnis der Farbauswahl zeigt 2 Häkchen und einen Wert von 13,97 an." lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="41aff-207">Der **Abschnitt Kontrastverhältnis** der Farbauswahl zeigt 2 Häkchen und einen Wert von</span><span class="sxs-lookup"><span data-stu-id="41aff-207">The **Contrast Ratio** section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="41aff-208">Weitere Informationen finden Sie im Abschnitt **Kontrastverhältnis.**</span><span class="sxs-lookup"><span data-stu-id="41aff-208">For more information, choose the **Contrast Ratio** section.</span></span>  <span data-ttu-id="41aff-209">Oben in der Farbauswahl wird in der visuellen Auswahl eine Linie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="41aff-209">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="41aff-210">Wenn die aktuelle Farbe Empfehlungen erfüllt, entspricht auch alles auf derselben Seite der Linie den Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="41aff-210">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="41aff-211">Wenn die aktuelle Farbe den Empfehlungen nicht gerecht wird, erfüllt auch nichts auf derselben Seite empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="41aff-211">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Die Kontrastverhältnislinie in der visuellen Auswahl" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="41aff-213">Die **Kontrastverhältnislinie** in der visuellen Auswahl</span><span class="sxs-lookup"><span data-stu-id="41aff-213">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="41aff-214">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="41aff-214">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Navigieren Microsoft Edge DevTools mit Hilfstechnologie | Microsoft Docs"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Nur das CSS anzeigen, das tatsächlich auf ein Element angewendet wird – CSS Reference | Microsoft Docs"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe – Web Accessibility Testing – Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Barrierefreiheitsstruktur (Accessibility Tree, AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Barrierefreiheit | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Bildschirmleseprogramm | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contrast (Enhanced) Level AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Kontrast (Minimum) Level AA | W3C"  

> [!NOTE]
> <span data-ttu-id="41aff-223">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41aff-223">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="41aff-224">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="41aff-224">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="41aff-226">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="41aff-226">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

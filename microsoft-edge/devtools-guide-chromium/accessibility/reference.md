---
description: Eine umfassende Referenz zu Barrierefreiheitsfeatures in Microsoft Edge devtools
title: Barrierefreiheits Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 39b0b8c36cea017b9976ea4e80e92ea93896a671
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993268"
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

# <span data-ttu-id="9f60b-104">Barrierefreiheits Referenz</span><span class="sxs-lookup"><span data-stu-id="9f60b-104">Accessibility reference</span></span>  

<span data-ttu-id="9f60b-105">Diese Seite ist eine umfassende Referenz zu Barrierefreiheitsfeatures in Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="9f60b-105">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="9f60b-106">Sie ist für Web-Entwickler gedacht, die:</span><span class="sxs-lookup"><span data-stu-id="9f60b-106">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="9f60b-107">Grundlegende Kenntnisse in devtools, beispielsweise zum Öffnen.</span><span class="sxs-lookup"><span data-stu-id="9f60b-107">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="9f60b-108">Sind mit [Grundsätzen der Barrierefreiheit und bewährten Methoden][MDNAccessibility]vertraut.</span><span class="sxs-lookup"><span data-stu-id="9f60b-108">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  
    
<span data-ttu-id="9f60b-109">Dieser Bezug soll Ihnen helfen, alle in devtools verfügbaren Tools zu finden, die Ihnen bei der Untersuchung der Barrierefreiheit einer Seite helfen.</span><span class="sxs-lookup"><span data-stu-id="9f60b-109">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="9f60b-110">Weitere Informationen finden Sie unter [Navigieren in Microsoft Edge devtools mit Hilfstechnologien][DevtoolsAccessibilityNavigation] , wenn Sie Hilfe beim Navigieren in devtools mit einer Hilfstechnologie wie einer Bildschirmsprachausgabe suchen.</span><span class="sxs-lookup"><span data-stu-id="9f60b-110">See [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation] if you are looking for help on navigating DevTools with an assistive technology like a screen reader.</span></span>  

## <span data-ttu-id="9f60b-111">Übersicht über Barrierefreiheitsfeatures in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="9f60b-111">Overview of accessibility features in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="9f60b-112">In diesem Abschnitt wird erläutert, wie sich devtools in Ihr gesamtes Barrierefreiheits-Toolkit einfügt.</span><span class="sxs-lookup"><span data-stu-id="9f60b-112">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="9f60b-113">Wenn Sie feststellen möchten, ob eine Seite barrierefrei ist, müssen Sie zwei allgemeine Fragen berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="9f60b-113">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="9f60b-114">Können Sie auf der Seite mit einer Tastatur oder einer [Sprachausgabe][MDNScreenReader]navigieren?</span><span class="sxs-lookup"><span data-stu-id="9f60b-114">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="9f60b-115">Sind die Elemente der Seite für Bildschirmsprachausgaben richtig markiert?</span><span class="sxs-lookup"><span data-stu-id="9f60b-115">Are the elements of the page properly marked up for screen readers?</span></span>  
    
<span data-ttu-id="9f60b-116">Im Allgemeinen sollte devtools Sie bei der Behebung von Fehlern in Bezug auf Fragen #2 unterstützen, da diese Fehler in automatisierter Weise leicht zu erkennen sind.</span><span class="sxs-lookup"><span data-stu-id="9f60b-116">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="9f60b-117">Frage #1 ist genauso wichtig, aber leider hilft Ihnen devtools nicht.</span><span class="sxs-lookup"><span data-stu-id="9f60b-117">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="9f60b-118">Die einzige Möglichkeit, Fehler im Zusammenhang mit der Frage #1 zu finden, besteht darin, eine Seite mit einer Tastatur oder einer Bildschirmsprachausgabe selbst zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f60b-118">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <span data-ttu-id="9f60b-119">Überwachen der Barrierefreiheit einer Seite</span><span class="sxs-lookup"><span data-stu-id="9f60b-119">Audit the accessibility of a page</span></span>  

> [!NOTE]
> <span data-ttu-id="9f60b-120">Das **Überwachungs** Panel enthält Links zu Inhalten, die auf Websites von Drittanbietern gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="9f60b-120">The **Audits** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="9f60b-121">Microsoft ist nicht verantwortlich und hat keine Kontrolle über den Inhalt dieser Websites und alle Daten, die möglicherweise erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="9f60b-121">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="9f60b-122">Im Allgemeinen können Sie mithilfe des Überwachungs Panels feststellen, ob:</span><span class="sxs-lookup"><span data-stu-id="9f60b-122">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="9f60b-123">Eine Seite ist für Bildschirmsprachausgaben richtig markiert.</span><span class="sxs-lookup"><span data-stu-id="9f60b-123">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="9f60b-124">Die Textelemente auf einer Seite verfügen über ein ausreichendes Kontrastverhältnis.</span><span class="sxs-lookup"><span data-stu-id="9f60b-124">The text elements on a page have sufficient contrast ratios.</span></span>  <span data-ttu-id="9f60b-125">Weitere Informationen finden Sie unter [Anzeigen des Kontrastverhältnisses eines Textelements in der Farbauswahl](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span><span class="sxs-lookup"><span data-stu-id="9f60b-125">See [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="9f60b-126">So überprüfen Sie eine Seite:</span><span class="sxs-lookup"><span data-stu-id="9f60b-126">To audit a page:</span></span>  

1.  <span data-ttu-id="9f60b-127">Wechseln Sie zu der URL, die Sie überwachen möchten.</span><span class="sxs-lookup"><span data-stu-id="9f60b-127">Go to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="9f60b-128">Klicken Sie in devtools auf die Registerkarte **Audits** .  DevTools zeigt Ihnen verschiedene Konfigurationsoptionen.</span><span class="sxs-lookup"><span data-stu-id="9f60b-128">In DevTools, click the **Audits** tab.  DevTools shows you various configuration options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Konfigurieren von Audits" lightbox="../media/accessibility-audits-pane.msft.png":::
       <span data-ttu-id="9f60b-130">Konfigurieren von Audits</span><span class="sxs-lookup"><span data-stu-id="9f60b-130">Configure audits</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="9f60b-131">Die Screenshots in diesem Abschnitt wurden mit Version 79 von Microsoft Edge übernommen.</span><span class="sxs-lookup"><span data-stu-id="9f60b-131">The screenshots in this section were taken with version 79 of Microsoft Edge.</span></span>  <span data-ttu-id="9f60b-132">Sie können überprüfen, welche Version Sie Ausführen `edge://version` .</span><span class="sxs-lookup"><span data-stu-id="9f60b-132">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="9f60b-133">Die Benutzeroberfläche des **Überwachungs** Panels sieht in früheren Versionen von Microsoft Edge anders aus, der allgemeine Workflow ist jedoch identisch.</span><span class="sxs-lookup"><span data-stu-id="9f60b-133">The **Audits** panel UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="9f60b-134">Wählen Sie für **Gerät**den Eintrag **Handy** aus, wenn Sie ein mobiles Gerät simulieren möchten.</span><span class="sxs-lookup"><span data-stu-id="9f60b-134">For **Device**, select **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="9f60b-135">Mit dieser Option wird die Zeichenfolge des Benutzer-Agents geändert und die Größe des Viewports geändert.</span><span class="sxs-lookup"><span data-stu-id="9f60b-135">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="9f60b-136">Wenn die Mobile Version der Seite anders als die Desktop Version angezeigt wird, kann sich diese Option erheblich auf die Ergebnisse ihrer Überwachung auswirken.</span><span class="sxs-lookup"><span data-stu-id="9f60b-136">If the mobile version of the page displays differently than the desktop version, this option could have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="9f60b-137">Stellen Sie im Abschnitt **Audits** sicher, dass die **Barrierefreiheit** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9f60b-137">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="9f60b-138">Deaktivieren Sie die anderen Kategorien, wenn Sie Sie aus dem Bericht ausschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="9f60b-138">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="9f60b-139">Lassen Sie sie aktiviert, wenn Sie andere Möglichkeiten entdecken möchten, um die Qualität Ihrer Seite zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="9f60b-139">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="9f60b-140">Im Abschnitt **Drosselung** können Sie das Netzwerk und die CPU Drosseln, was bei der Analyse der Auslastungs Leistung hilfreich ist.</span><span class="sxs-lookup"><span data-stu-id="9f60b-140">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="9f60b-141">Diese Option sollte für den Zugriff auf die Barrierefreiheit irrelevant sein, daher können Sie das, was Sie bevorzugen, verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f60b-141">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="9f60b-142">Mit dem Kontrollkästchen **Speicher löschen** können Sie den gesamten Speicher löschen, bevor Sie die Seite laden, oder den Speicherplatz zwischen den Seitenlasten bewahren.</span><span class="sxs-lookup"><span data-stu-id="9f60b-142">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="9f60b-143">Diese Option ist möglicherweise auch für das Ergebnis der Barrierefreiheit irrelevant, sodass Sie die von Ihnen bevorzugten Optionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="9f60b-143">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="9f60b-144">Klicken Sie auf **Überwachungen ausführen**.</span><span class="sxs-lookup"><span data-stu-id="9f60b-144">Click **Run Audits**.</span></span> <span data-ttu-id="9f60b-145">Nach 10 bis 30 Sekunden bietet devtools einen Bericht.</span><span class="sxs-lookup"><span data-stu-id="9f60b-145">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="9f60b-146">Ihr Bericht gibt Ihnen verschiedene Tipps, wie Sie die Barrierefreiheit der Seite verbessern können.</span><span class="sxs-lookup"><span data-stu-id="9f60b-146">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Einen Bericht" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       <span data-ttu-id="9f60b-148">Einen Bericht</span><span class="sxs-lookup"><span data-stu-id="9f60b-148">A report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9f60b-149">Klicken Sie auf eine Überwachung, um mehr darüber zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="9f60b-149">Click an audit to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Weitere Informationen zu einer Überwachung" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       <span data-ttu-id="9f60b-151">Weitere Informationen zu einer Überwachung</span><span class="sxs-lookup"><span data-stu-id="9f60b-151">More information about an audit</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9f60b-152">Klicken Sie auf **Weitere Informationen** , um die Dokumentation dieser Überwachung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9f60b-152">Click **Learn More** to view the documentation of that audit.</span></span>  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Anzeigen der Dokumentation einer Überwachung" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="9f60b-154">Anzeigen der Dokumentation einer Überwachung</span><span class="sxs-lookup"><span data-stu-id="9f60b-154">View the documentation of an audit</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="9f60b-155">Siehe auch: aXe Extension</span><span class="sxs-lookup"><span data-stu-id="9f60b-155">See also: aXe extension</span></span>  

<span data-ttu-id="9f60b-156">Möglicherweise bevorzugen Sie die [Axt-Erweiterung][ChromeWebStoreAxe] anstelle des **Überwachungs** Panels.</span><span class="sxs-lookup"><span data-stu-id="9f60b-156">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** panel.</span></span>  
<span data-ttu-id="9f60b-157">Die aXe-Erweiterung bietet im Allgemeinen dieselben Informationen, da es sich um das zugrunde liegende Modul handelt, das das Überwachungs Panel ausmacht.</span><span class="sxs-lookup"><span data-stu-id="9f60b-157">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="9f60b-158">Die aXe-Erweiterung hat eine andere Benutzeroberfläche und beschreibt die Überwachungen etwas anders.</span><span class="sxs-lookup"><span data-stu-id="9f60b-158">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="9f60b-159">Ein Vorteil, den die Axt-Erweiterung über das **Überwachungs** Panel hat, besteht darin, dass Sie fehlerhafte Knoten überprüfen und markieren können.</span><span class="sxs-lookup"><span data-stu-id="9f60b-159">One advantage that the aXe extension has over the **Audits** panel is that it enables you to inspect and highlight failing nodes.</span></span>  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Die Axt-Erweiterung" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   <span data-ttu-id="9f60b-161">Die Axt-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="9f60b-161">The aXe extension</span></span>  
:::image-end:::  

## <span data-ttu-id="9f60b-162">Der Bereich "Barrierefreiheit"</span><span class="sxs-lookup"><span data-stu-id="9f60b-162">The Accessibility pane</span></span>  

<span data-ttu-id="9f60b-163">Im Bereich " **Barrierefreiheit** " werden die Barrierefreiheits Struktur, Aria-Attribute und berechnete Barrierefreiheitseigenschaften von DOM-Knoten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9f60b-163">The **Accessibility** pane is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="9f60b-164">So öffnen Sie den Bereich **Barrierefreiheit** :</span><span class="sxs-lookup"><span data-stu-id="9f60b-164">To open the **Accessibility** pane:</span></span>  

1.  <span data-ttu-id="9f60b-165">Klicken Sie auf die Registerkarte **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="9f60b-165">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="9f60b-166">Wählen Sie in der **DOM-Struktur**das Element aus, das Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="9f60b-166">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="9f60b-167">Klicken Sie auf die Registerkarte **Barrierefreiheit** .  Diese Registerkarte ist möglicherweise hinter der Schaltfläche **weitere Registerkarten** \ ( ![ weitere Registerkarten ][ImageMoreTabsIcon] \) verborgen.</span><span class="sxs-lookup"><span data-stu-id="9f60b-167">Click the **Accessibility** tab.  This tab may be hidden behind the **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) button.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Überprüfen des H1-Elements der devtools-Homepage im Bereich "Barrierefreiheit"" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="9f60b-169">Überprüfen des `h1` Elements der devtools-Homepage im Bereich " **Barrierefreiheit** "</span><span class="sxs-lookup"><span data-stu-id="9f60b-169">Inspect the `h1` element of the DevTools homepage in the **Accessibility** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="9f60b-170">Anzeigen der Position eines Elements in der Barrierefreiheits Struktur</span><span class="sxs-lookup"><span data-stu-id="9f60b-170">View the position of an element in the accessibility tree</span></span>  

<span data-ttu-id="9f60b-171">Die [Barrierefreiheits Struktur][MDNAccessibilityTree] ist eine Teilmenge der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="9f60b-171">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="9f60b-172">Sie enthält nur Elemente aus der DOM-Struktur, die für die Anzeige des Inhalts einer Seite in einer Sprachausgabe relevant und nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="9f60b-172">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="9f60b-173">Überprüfen Sie die Position eines Elements in der Barrierefreiheits Struktur aus dem [Bereich Barrierefreiheit](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="9f60b-173">Inspect the position of an element in the accessibility tree from the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Abschnitt "Barrierefreiheits Struktur"" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="9f60b-175">Abschnitt " **Barrierefreiheits Struktur** "</span><span class="sxs-lookup"><span data-stu-id="9f60b-175">The **Accessibility Tree** section</span></span>  
:::image-end:::  

### <span data-ttu-id="9f60b-176">Anzeigen der Aria-Attribute eines Elements</span><span class="sxs-lookup"><span data-stu-id="9f60b-176">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="9f60b-177">Aria-Attribute stellen sicher, dass Bildschirmsprachausgaben alle Informationen enthalten, die Sie benötigen, um den Inhalt einer Seite ordnungsgemäß darzustellen.</span><span class="sxs-lookup"><span data-stu-id="9f60b-177">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="9f60b-178">Zeigen Sie die Aria-Attribute eines Elements im [Bereich "Barrierefreiheit"](#the-accessibility-pane)an.</span><span class="sxs-lookup"><span data-stu-id="9f60b-178">View the ARIA attributes of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Der Abschnitt "Aria-Attribute"" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="9f60b-180">Der Abschnitt " **Aria-Attribute** "</span><span class="sxs-lookup"><span data-stu-id="9f60b-180">The **ARIA Attributes** section</span></span>  
:::image-end:::  

### <span data-ttu-id="9f60b-181">Anzeigen der berechneten Barrierefreiheitseigenschaften eines Elements</span><span class="sxs-lookup"><span data-stu-id="9f60b-181">View the computed accessibility properties of an element</span></span>  

> [!NOTE]
> <span data-ttu-id="9f60b-182">Wenn Sie nach berechneten CSS-Eigenschaften suchen, lesen Sie die [Registerkarte berechnet][DevtoolsCssReferenceViewActuallyAppliedElements].</span><span class="sxs-lookup"><span data-stu-id="9f60b-182">If you are looking for computed CSS properties, see the [Computed tab][DevtoolsCssReferenceViewActuallyAppliedElements].</span></span>  

<span data-ttu-id="9f60b-183">Einige Barrierefreiheitseigenschaften werden vom Browser dynamisch berechnet.</span><span class="sxs-lookup"><span data-stu-id="9f60b-183">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="9f60b-184">Diese Eigenschaften werden im Abschnitt " **berechnete Eigenschaften** " des **Barrierefreiheits** Bereichs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9f60b-184">These properties are displayed in the **Computed Properties** section of the **Accessibility** pane.</span></span>  

<span data-ttu-id="9f60b-185">Zeigen Sie die berechneten Barrierefreiheitseigenschaften eines Elements im [Bereich "Barrierefreiheit"](#the-accessibility-pane)an.</span><span class="sxs-lookup"><span data-stu-id="9f60b-185">View the computed accessibility properties of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Abschnitt "berechnete Eigenschaften" im Bereich "Barrierefreiheit"" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="9f60b-187">Abschnitt " **berechnete Eigenschaften** " im Bereich " **Barrierefreiheit** "</span><span class="sxs-lookup"><span data-stu-id="9f60b-187">The **Computed Properties** section of the **Accessibility** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="9f60b-188">Anzeigen des Kontrastverhältnisses eines Textelements in der Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="9f60b-188">View the contrast ratio of a text element in the Color Picker</span></span>  

<span data-ttu-id="9f60b-189">Einige Personen mit Sehbehinderungen sehen keine Bereiche als sehr hell oder sehr dunkel.</span><span class="sxs-lookup"><span data-stu-id="9f60b-189">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="9f60b-190">Alles neigt dazu, bei ungefähr der gleichen Helligkeit zu erscheinen, wodurch es schwierig ist, Konturen und Kanten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="9f60b-190">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="9f60b-191">Das Kontrastverhältnis misst den Helligkeitsunterschied zwischen Vordergrund und Hintergrund des Texts.</span><span class="sxs-lookup"><span data-stu-id="9f60b-191">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="9f60b-192">Wenn Ihr Text ein kontrastarmes Verhältnis hat, können diese sehbehinderten Benutzer Ihre Website buchstäblich als einen leeren Bildschirm sehen.</span><span class="sxs-lookup"><span data-stu-id="9f60b-192">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="9f60b-193">Mit der Farbauswahl können Sie überprüfen, ob Ihr Text die empfohlenen Kontrast Raten erfüllt:</span><span class="sxs-lookup"><span data-stu-id="9f60b-193">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="9f60b-194">Klicken Sie auf die Registerkarte **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="9f60b-194">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="9f60b-195">Wählen Sie in der **DOM-Struktur**das Textelement aus, das Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="9f60b-195">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Überprüfen eines Absatzes in der DOM-Struktur" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="9f60b-197">Überprüfen eines Absatzes in der **DOM-Struktur**</span><span class="sxs-lookup"><span data-stu-id="9f60b-197">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9f60b-198">Klicken Sie im Bereich **Formatvorlagen** auf das Farbquadrat neben dem `color` Wert des Elements.</span><span class="sxs-lookup"><span data-stu-id="9f60b-198">In the **Styles** pane, click the color square next to the `color` value of the element.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Die Color-Eigenschaft des Elements" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="9f60b-200">Die `color` Eigenschaft des Elements</span><span class="sxs-lookup"><span data-stu-id="9f60b-200">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9f60b-201">Überprüfen Sie den Abschnitt **Kontrastverhältnis** der Farbauswahl.</span><span class="sxs-lookup"><span data-stu-id="9f60b-201">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="9f60b-202">Ein Häkchen bedeutet, dass das Element die [minimale Empfehlung][W3CContrastMinimum]erfüllt.</span><span class="sxs-lookup"><span data-stu-id="9f60b-202">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="9f60b-203">Zwei Kontrollkästchen bedeuten, dass die [Erweiterte Empfehlung][W3CContrastEnhanced]erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="9f60b-203">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="Der Abschnitt "Kontrastverhältnis" der Farbauswahl zeigt zwei Häkchen und einen Wert von 13,97." lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="9f60b-205">Der Abschnitt " **Kontrastverhältnis** " der Farbauswahl zeigt zwei Häkchen und einen Wert von</span><span class="sxs-lookup"><span data-stu-id="9f60b-205">The **Contrast Ratio** section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="9f60b-206">Klicken Sie auf den Abschnitt **Kontrastverhältnis** , um weitere Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9f60b-206">Click the **Contrast Ratio** section to see more information.</span></span>  <span data-ttu-id="9f60b-207">Eine Zeile wird in der visuellen Auswahl oben in der Farbauswahl angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9f60b-207">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="9f60b-208">Wenn die aktuelle Farbe Empfehlungen erfüllt, entspricht alles, was auf der gleichen Seite der Zeile steht, auch Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="9f60b-208">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="9f60b-209">Wenn die aktuelle Farbe keine Empfehlungen erfüllt, entspricht alles auf der gleichen Seite auch nicht den Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="9f60b-209">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Die Zeile "Kontrastverhältnis" in der visuellen Auswahl" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="9f60b-211">Die Zeile " **Kontrastverhältnis** " in der visuellen Auswahl</span><span class="sxs-lookup"><span data-stu-id="9f60b-211">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  
    
<!--## Feedback   -->  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Navigieren in Microsoft Edge devtools mit Hilfstechnologien | Microsoft docs"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Anzeigen nur des CSS, das tatsächlich auf ein Element angewendet wird-CSS-Referenz | Microsoft docs"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "Axe – Web-Barrierefreiheits Tests – Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Barrierefreiheits Struktur (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Barrierefreiheit | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Sprachausgabe | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Kontrast (erweitert) AAA-Ebene | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Kontrast (Mindest) Ebene AA | W3C"  

> [!NOTE]
> <span data-ttu-id="9f60b-220">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f60b-220">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9f60b-221">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="9f60b-221">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="9f60b-223">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9f60b-223">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
title: Barrierefreiheits Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 7417388023612b6e1ca651deba28e099e3c8e3d8
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581573"
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





# <span data-ttu-id="9ce0c-103">Barrierefreiheits Referenz</span><span class="sxs-lookup"><span data-stu-id="9ce0c-103">Accessibility Reference</span></span>   



<span data-ttu-id="9ce0c-104">Diese Seite ist eine umfassende Referenz zu Barrierefreiheitsfeatures in Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-104">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="9ce0c-105">Sie ist für Web-Entwickler gedacht, die:</span><span class="sxs-lookup"><span data-stu-id="9ce0c-105">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="9ce0c-106">Grundlegende Kenntnisse in devtools, beispielsweise zum Öffnen.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-106">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="9ce0c-107">Sind mit [Grundsätzen der Barrierefreiheit und bewährten Methoden][MDNAccessibility]vertraut.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-107">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  

<span data-ttu-id="9ce0c-108">Dieser Bezug soll Ihnen helfen, alle in devtools verfügbaren Tools zu finden, die Ihnen bei der Untersuchung der Barrierefreiheit einer Seite helfen.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-108">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="9ce0c-109">Weitere Informationen finden Sie unter [Navigieren in Microsoft Edge devtools mit Hilfstechnologien][DevtoolsAccessibilityNavigation] , wenn Sie Hilfe beim Navigieren in devtools mit einer Hilfstechnologie wie einer Bildschirmsprachausgabe suchen.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-109">See [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation] if you are looking for help on navigating DevTools with an assistive technology like a screen reader.</span></span>  

## <span data-ttu-id="9ce0c-110">Übersicht über Barrierefreiheitsfeatures in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="9ce0c-110">Overview of accessibility features in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="9ce0c-111">In diesem Abschnitt wird erläutert, wie sich devtools in Ihr gesamtes Barrierefreiheits-Toolkit einfügt.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-111">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="9ce0c-112">Wenn Sie feststellen möchten, ob eine Seite barrierefrei ist, müssen Sie zwei allgemeine Fragen berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="9ce0c-112">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="9ce0c-113">Können Sie auf der Seite mit einer Tastatur oder einer [Sprachausgabe][MDNScreenReader]navigieren?</span><span class="sxs-lookup"><span data-stu-id="9ce0c-113">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="9ce0c-114">Sind die Elemente der Seite für Bildschirmsprachausgaben richtig markiert?</span><span class="sxs-lookup"><span data-stu-id="9ce0c-114">Are the elements of the page properly marked up for screen readers?</span></span>  

<span data-ttu-id="9ce0c-115">Im Allgemeinen sollte devtools Sie bei der Behebung von Fehlern in Bezug auf Fragen #2 unterstützen, da diese Fehler in automatisierter Weise leicht zu erkennen sind.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-115">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="9ce0c-116">Frage #1 ist genauso wichtig, aber leider hilft Ihnen devtools nicht.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-116">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="9ce0c-117">Die einzige Möglichkeit, Fehler im Zusammenhang mit der Frage #1 zu finden, besteht darin, eine Seite mit einer Tastatur oder einer Bildschirmsprachausgabe selbst zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-117">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <span data-ttu-id="9ce0c-118">Überwachen der Barrierefreiheit einer Seite</span><span class="sxs-lookup"><span data-stu-id="9ce0c-118">Audit the accessibility of a page</span></span>   

> [!NOTE]
> <span data-ttu-id="9ce0c-119">Das **Überwachungs** Panel enthält Links zu Inhalten, die auf Websites von Drittanbietern gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-119">The **Audits** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="9ce0c-120">Microsoft ist nicht verantwortlich und hat keine Kontrolle über den Inhalt dieser Websites und alle Daten, die möglicherweise erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-120">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="9ce0c-121">Im Allgemeinen können Sie mithilfe des Überwachungs Panels feststellen, ob:</span><span class="sxs-lookup"><span data-stu-id="9ce0c-121">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="9ce0c-122">Eine Seite ist für Bildschirmsprachausgaben richtig markiert.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-122">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="9ce0c-123">Die Textelemente auf einer Seite verfügen über ein ausreichendes Kontrastverhältnis.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-123">The text elements on a page have sufficient contrast ratios.</span></span> <span data-ttu-id="9ce0c-124">Siehe auch [Anzeigen des Kontrastverhältnisses eines Textelements in der Farbauswahl](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span><span class="sxs-lookup"><span data-stu-id="9ce0c-124">See also [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="9ce0c-125">So überprüfen Sie eine Seite:</span><span class="sxs-lookup"><span data-stu-id="9ce0c-125">To audit a page:</span></span>  

1.  <span data-ttu-id="9ce0c-126">Wechseln Sie zu der URL, die Sie überwachen möchten.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-126">Go to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="9ce0c-127">Klicken Sie in devtools auf die Registerkarte **Audits** .  DevTools zeigt Ihnen verschiedene Konfigurationsoptionen.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-127">In DevTools, click the **Audits** tab.  DevTools shows you various configuration options.</span></span>  
    
    > ##### <span data-ttu-id="9ce0c-128">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="9ce0c-128">Figure 1</span></span>  
    > <span data-ttu-id="9ce0c-129">Konfigurieren von Audits</span><span class="sxs-lookup"><span data-stu-id="9ce0c-129">Configuring audits</span></span>  
    > ![Konfigurieren von Audits][ImageConfiguringAudits]  
    
    > [!NOTE]
    > <span data-ttu-id="9ce0c-131">Die Screenshots in diesem Abschnitt wurden mit Version 79 von Microsoft Edge übernommen.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-131">The screenshots in this section were taken with version 79 of Microsoft Edge.</span></span>  <span data-ttu-id="9ce0c-132">Sie können überprüfen, welche Version Sie Ausführen `edge://version` .</span><span class="sxs-lookup"><span data-stu-id="9ce0c-132">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="9ce0c-133">Die Benutzeroberfläche des **Überwachungs** Panels sieht in früheren Versionen von Microsoft Edge anders aus, der allgemeine Workflow ist jedoch identisch.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-133">The **Audits** panel UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="9ce0c-134">Wählen Sie für **Gerät**den Eintrag **Handy** aus, wenn Sie ein mobiles Gerät simulieren möchten.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-134">For **Device**, select **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="9ce0c-135">Mit dieser Option wird die Zeichenfolge des Benutzer-Agents geändert und die Größe des Viewports geändert.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-135">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="9ce0c-136">Wenn die Mobile Version der Seite anders als die Desktop Version angezeigt wird, kann sich diese Option erheblich auf die Ergebnisse ihrer Überwachung auswirken.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-136">If the mobile version of the page displays differently than the desktop version, this option could have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="9ce0c-137">Stellen Sie im Abschnitt **Audits** sicher, dass die **Barrierefreiheit** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-137">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="9ce0c-138">Deaktivieren Sie die anderen Kategorien, wenn Sie Sie aus dem Bericht ausschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-138">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="9ce0c-139">Lassen Sie sie aktiviert, wenn Sie andere Möglichkeiten entdecken möchten, um die Qualität Ihrer Seite zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-139">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="9ce0c-140">Im Abschnitt **Drosselung** können Sie das Netzwerk und die CPU Drosseln, was bei der Analyse der Auslastungs Leistung hilfreich ist.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-140">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="9ce0c-141">Diese Option sollte für den Zugriff auf die Barrierefreiheit irrelevant sein, daher können Sie das, was Sie bevorzugen, verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-141">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="9ce0c-142">Mit dem Kontrollkästchen **Speicher löschen** können Sie den gesamten Speicher löschen, bevor Sie die Seite laden, oder den Speicherplatz zwischen den Seitenlasten bewahren.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-142">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="9ce0c-143">Diese Option ist möglicherweise auch für das Ergebnis der Barrierefreiheit irrelevant, sodass Sie die von Ihnen bevorzugten Optionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-143">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="9ce0c-144">Klicken Sie auf **Überwachungen ausführen**.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-144">Click **Run Audits**.</span></span> <span data-ttu-id="9ce0c-145">Nach 10 bis 30 Sekunden bietet devtools einen Bericht.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-145">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="9ce0c-146">Ihr Bericht gibt Ihnen verschiedene Tipps, wie Sie die Barrierefreiheit der Seite verbessern können.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-146">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    > ##### <span data-ttu-id="9ce0c-147">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="9ce0c-147">Figure 2</span></span>  
    > <span data-ttu-id="9ce0c-148">Einen Bericht</span><span class="sxs-lookup"><span data-stu-id="9ce0c-148">A report</span></span>  
    > ![Einen Bericht][ImageReport]  
    
1.  <span data-ttu-id="9ce0c-150">Klicken Sie auf eine Überwachung, um mehr darüber zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-150">Click an audit to learn more about it.</span></span>  
    
    > ##### <span data-ttu-id="9ce0c-151">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="9ce0c-151">Figure 3</span></span>  
    > <span data-ttu-id="9ce0c-152">Weitere Informationen zu einer Überwachung</span><span class="sxs-lookup"><span data-stu-id="9ce0c-152">More information about an audit</span></span>  
    > ![Weitere Informationen zu einer Überwachung][ImageAttributes]  
    
1.  <span data-ttu-id="9ce0c-154">Klicken Sie auf **Weitere Informationen** , um die Dokumentation dieser Überwachung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-154">Click **Learn More** to view the documentation of that audit.</span></span>
    
    > ##### <span data-ttu-id="9ce0c-155">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="9ce0c-155">Figure 4</span></span>  
    > <span data-ttu-id="9ce0c-156">Anzeigen der Dokumentation einer Überwachung</span><span class="sxs-lookup"><span data-stu-id="9ce0c-156">Viewing the documentation of an audit</span></span>  
    > ![Anzeigen der Dokumentation einer Überwachung][ImageAuditDocumentation]  
    
### <span data-ttu-id="9ce0c-158">Siehe auch: aXe Extension</span><span class="sxs-lookup"><span data-stu-id="9ce0c-158">See also: aXe extension</span></span>   

<span data-ttu-id="9ce0c-159">Möglicherweise bevorzugen Sie die [Axt-Erweiterung][ChromeWebStoreAxe] anstelle des **Überwachungs** Panels.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-159">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** panel.</span></span>  
<span data-ttu-id="9ce0c-160">Die aXe-Erweiterung bietet im Allgemeinen dieselben Informationen, da es sich um das zugrunde liegende Modul handelt, das das Überwachungs Panel ausmacht.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-160">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="9ce0c-161">Die aXe-Erweiterung hat eine andere Benutzeroberfläche und beschreibt die Überwachungen etwas anders.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-161">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="9ce0c-162">Ein Vorteil, den die Axt-Erweiterung über das **Überwachungs** Panel hat, besteht darin, dass Sie fehlerhafte Knoten überprüfen und markieren können.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-162">One advantage that the aXe extension has over the **Audits** panel is that it enables you to inspect and highlight failing nodes.</span></span>  

> ##### <span data-ttu-id="9ce0c-163">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="9ce0c-163">Figure 5</span></span>  
> <span data-ttu-id="9ce0c-164">Die Axt-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="9ce0c-164">The aXe extension</span></span>  
> ![Die Axt-Erweiterung][ImageAxeExtension]  

## <span data-ttu-id="9ce0c-166">Der Bereich "Barrierefreiheit"</span><span class="sxs-lookup"><span data-stu-id="9ce0c-166">The Accessibility pane</span></span>   

<span data-ttu-id="9ce0c-167">Im Bereich " **Barrierefreiheit** " werden die Barrierefreiheits Struktur, Aria-Attribute und berechnete Barrierefreiheitseigenschaften von DOM-Knoten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-167">The **Accessibility** pane is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="9ce0c-168">So öffnen Sie den Bereich **Barrierefreiheit** :</span><span class="sxs-lookup"><span data-stu-id="9ce0c-168">To open the **Accessibility** pane:</span></span>  

1.  <span data-ttu-id="9ce0c-169">Klicken Sie auf die Registerkarte **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="9ce0c-169">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="9ce0c-170">Wählen Sie in der **DOM-Struktur**das Element aus, das Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-170">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="9ce0c-171">Klicken Sie auf die Registerkarte **Barrierefreiheit** .  Diese Registerkarte ist möglicherweise **More Tabs** hinter der ![ Schaltfläche weitere Registerkarten weitere Tabstopps verborgen ][ImageMoreTabsIcon] .</span><span class="sxs-lookup"><span data-stu-id="9ce0c-171">Click the **Accessibility** tab.  This tab may be hidden behind the **More Tabs** ![More Tabs][ImageMoreTabsIcon] button.</span></span>  

> ##### <span data-ttu-id="9ce0c-172">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="9ce0c-172">Figure 6</span></span>  
> <span data-ttu-id="9ce0c-173">Überprüfen des `h1` Elements der devtools-Homepage im Bereich " **Barrierefreiheit** "</span><span class="sxs-lookup"><span data-stu-id="9ce0c-173">Inspecting the `h1` element of the DevTools homepage in the **Accessibility** pane</span></span>  
> ![Überprüfen des H1-Elements der devtools-Homepage im Bereich "Barrierefreiheit"][ImageA11yPane]  

### <span data-ttu-id="9ce0c-175">Anzeigen der Position eines Elements in der Barrierefreiheits Struktur</span><span class="sxs-lookup"><span data-stu-id="9ce0c-175">View the position of an element in the accessibility tree</span></span>   

<span data-ttu-id="9ce0c-176">Die [Barrierefreiheits Struktur][MDNAccessibilityTree] ist eine Teilmenge der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-176">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="9ce0c-177">Sie enthält nur Elemente aus der DOM-Struktur, die für die Anzeige des Inhalts einer Seite in einer Sprachausgabe relevant und nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-177">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="9ce0c-178">Überprüfen Sie die Position eines Elements in der Barrierefreiheits Struktur aus dem [Bereich Barrierefreiheit](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="9ce0c-178">Inspect the position of an element in the accessibility tree from the [Accessibility pane](#the-accessibility-pane).</span></span>  

> ##### <span data-ttu-id="9ce0c-179">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="9ce0c-179">Figure 7</span></span>  
> <span data-ttu-id="9ce0c-180">Abschnitt "Barrierefreiheits Struktur"</span><span class="sxs-lookup"><span data-stu-id="9ce0c-180">The Accessibility Tree section</span></span>  
> ![Abschnitt "Barrierefreiheits Struktur"][ImageAllyTree]  

### <span data-ttu-id="9ce0c-182">Anzeigen der Aria-Attribute eines Elements</span><span class="sxs-lookup"><span data-stu-id="9ce0c-182">View the ARIA attributes of an element</span></span>   

<span data-ttu-id="9ce0c-183">Aria-Attribute stellen sicher, dass Bildschirmsprachausgaben alle Informationen enthalten, die Sie benötigen, um den Inhalt einer Seite ordnungsgemäß darzustellen.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-183">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="9ce0c-184">Zeigen Sie die Aria-Attribute eines Elements im [Bereich "Barrierefreiheit"](#the-accessibility-pane)an.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-184">View the ARIA attributes of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

> ##### <span data-ttu-id="9ce0c-185">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="9ce0c-185">Figure 8</span></span>  
> <span data-ttu-id="9ce0c-186">Der Abschnitt "Aria-Attribute"</span><span class="sxs-lookup"><span data-stu-id="9ce0c-186">The ARIA Attributes section</span></span>  
> ![Der Abschnitt "Aria-Attribute"][ImageAriaAttributesSection]  

### <span data-ttu-id="9ce0c-188">Anzeigen der berechneten Barrierefreiheitseigenschaften eines Elements</span><span class="sxs-lookup"><span data-stu-id="9ce0c-188">View the computed accessibility properties of an element</span></span>   

> [!NOTE]
> <span data-ttu-id="9ce0c-189">Wenn Sie nach berechneten CSS-Eigenschaften suchen, lesen Sie die [Registerkarte berechnet][DevtoolsCssReferenceViewActuallyAppliedElements].</span><span class="sxs-lookup"><span data-stu-id="9ce0c-189">If you are looking for computed CSS properties, see the [Computed tab][DevtoolsCssReferenceViewActuallyAppliedElements].</span></span>  

<span data-ttu-id="9ce0c-190">Einige Barrierefreiheitseigenschaften werden vom Browser dynamisch berechnet.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-190">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="9ce0c-191">Diese Eigenschaften werden im Abschnitt " **berechnete Eigenschaften** " des **Barrierefreiheits** Bereichs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-191">These properties are displayed in the **Computed Properties** section of the **Accessibility** pane.</span></span>  

<span data-ttu-id="9ce0c-192">Zeigen Sie die berechneten Barrierefreiheitseigenschaften eines Elements im [Bereich "Barrierefreiheit"](#the-accessibility-pane)an.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-192">View the computed accessibility properties of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

> ##### <span data-ttu-id="9ce0c-193">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="9ce0c-193">Figure 9</span></span>  
> <span data-ttu-id="9ce0c-194">Der Abschnitt "berechnete (Barrierefreiheits-) Eigenschaften"</span><span class="sxs-lookup"><span data-stu-id="9ce0c-194">The Computed (Accessibility) Properties section</span></span>  
> ![Der Abschnitt "berechnete (Barrierefreiheits-) Eigenschaften"][ImageComputedA11yPropertiesSection]  

## <span data-ttu-id="9ce0c-196">Anzeigen des Kontrastverhältnisses eines Textelements in der Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="9ce0c-196">View the contrast ratio of a text element in the Color Picker</span></span>   

<span data-ttu-id="9ce0c-197">Einige Personen mit Sehbehinderungen sehen keine Bereiche als sehr hell oder sehr dunkel.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-197">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="9ce0c-198">Alles neigt dazu, bei ungefähr der gleichen Helligkeit zu erscheinen, wodurch es schwierig ist, Konturen und Kanten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-198">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  
<span data-ttu-id="9ce0c-199">Das Kontrastverhältnis misst den Helligkeitsunterschied zwischen Vordergrund und Hintergrund des Texts.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-199">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="9ce0c-200">Wenn Ihr Text ein kontrastarmes Verhältnis hat, können diese sehbehinderten Benutzer Ihre Website buchstäblich als einen leeren Bildschirm sehen.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-200">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="9ce0c-201">Mit der Farbauswahl können Sie überprüfen, ob Ihr Text die empfohlenen Kontrast Raten erfüllt:</span><span class="sxs-lookup"><span data-stu-id="9ce0c-201">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="9ce0c-202">Klicken Sie auf die Registerkarte **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="9ce0c-202">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="9ce0c-203">Wählen Sie in der **DOM-Struktur**das Textelement aus, das Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-203">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    > ##### <span data-ttu-id="9ce0c-204">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="9ce0c-204">Figure 10</span></span>  
    > <span data-ttu-id="9ce0c-205">Überprüfen eines Absatzes in der DOM-Struktur</span><span class="sxs-lookup"><span data-stu-id="9ce0c-205">Inspecting a paragraph in the DOM Tree</span></span>  
    > ![Überprüfen eines Absatzes in der DOM-Struktur][ImageInspectDomTree]  
    
1.  <span data-ttu-id="9ce0c-207">Klicken Sie im Bereich **Formatvorlagen** auf das Farbquadrat neben dem `color` Wert des Elements.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-207">In the **Styles** pane, click the color square next to the `color` value of the element.</span></span>  
    
    > ##### <span data-ttu-id="9ce0c-208">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="9ce0c-208">Figure 11</span></span>  
    > <span data-ttu-id="9ce0c-209">Die `color` Eigenschaft des Elements</span><span class="sxs-lookup"><span data-stu-id="9ce0c-209">The `color` property of the element</span></span>  
    > ![Die Color-Eigenschaft des Elements][ImageColorElement]  
    
1.  <span data-ttu-id="9ce0c-211">Überprüfen Sie den Abschnitt **Kontrastverhältnis** der Farbauswahl.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-211">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="9ce0c-212">Ein Häkchen bedeutet, dass das Element die [minimale Empfehlung][W3CContrastMinimum]erfüllt.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-212">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="9ce0c-213">Zwei Kontrollkästchen bedeuten, dass die [Erweiterte Empfehlung][W3CContrastEnhanced]erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-213">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>
    
    > ##### <span data-ttu-id="9ce0c-214">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="9ce0c-214">Figure 12</span></span>  
    > <span data-ttu-id="9ce0c-215">Der Abschnitt "Kontrastverhältnis" der Farbauswahl zeigt zwei Häkchen und einen Wert von</span><span class="sxs-lookup"><span data-stu-id="9ce0c-215">The Contrast Ratio section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    > ![Der Abschnitt "Kontrastverhältnis" der Farbauswahl zeigt zwei Häkchen und einen Wert von 13,97.][ImageColorPickerContrastRatio]  
    
1.  <span data-ttu-id="9ce0c-217">Klicken Sie auf den Abschnitt **Kontrastverhältnis** , um weitere Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-217">Click the **Contrast Ratio** section to see more information.</span></span>  <span data-ttu-id="9ce0c-218">Eine Zeile wird in der visuellen Auswahl oben in der Farbauswahl angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-218">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="9ce0c-219">Wenn die aktuelle Farbe Empfehlungen erfüllt, entspricht alles, was auf der gleichen Seite der Zeile steht, auch Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-219">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="9ce0c-220">Wenn die aktuelle Farbe keine Empfehlungen erfüllt, entspricht alles auf der gleichen Seite auch nicht den Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-220">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    > ##### <span data-ttu-id="9ce0c-221">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="9ce0c-221">Figure 13</span></span>  
    > <span data-ttu-id="9ce0c-222">Die Zeile "Kontrastverhältnis" in der visuellen Auswahl</span><span class="sxs-lookup"><span data-stu-id="9ce0c-222">The Contrast Ratio Line in the visual picker</span></span>  
    > ![Die Zeile "Kontrastverhältnis" in der visuellen Auswahl][ImageContrastRatioLine]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  

[ImageConfiguringAudits]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-pane.msft.png "Abbildung 1: Konfigurieren von Audits"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-run-audits-result.msft.png "Abbildung 2: eine Zahl"  
[ImageAttributes]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-run-audits-result-issues-expanded.msft.png "Abbildung 3: Weitere Informationen zu einer Überwachung"  
[ImageAuditDocumentation]: /microsoft-edge/devtools-guide-chromium/media/accessibility-web-dev-accessibility-audits-learn-more.msft.png "Abbildung 4: Anzeigen der Dokumentation einer Überwachung"  
[ImageAxeExtension]: /microsoft-edge/devtools-guide-chromium/media/accessibility-devtools-extension-axe-panel.msft.png "Abbildung 5: die Axt-Erweiterung"  
[ImageA11yPane]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility.msft.png "Abbildung 6: Überprüfen des H1-Elements der devtools-Homepage im Bereich "Barrierefreiheit""  
[ImageAllyTree]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-tree.msft.png "Abbildung 7: Abschnitt "Barrierefreiheits Struktur""  
[ImageAriaAttributesSection]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-aria-attributes.msft.png "Abbildung 8: Abschnitt "Aria-Attribute""  
[ImageComputedA11yPropertiesSection]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-computed-properties.msft.png "Abbildung 9: der Abschnitt "berechnete Eigenschaften (Barrierefreiheit)""  
[ImageInspectDomTree]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-paragraph-highlight.msft.png "Abbildung 10: Überprüfen eines Absatzes in der DOM-Struktur"  
[ImageColorElement]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color.msft.png "Abbildung 11: die Color-Eigenschaft des Elements"  
[ImageColorPickerContrastRatio]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png "Abbildung 12: der Abschnitt "Kontrastverhältnis" der Farbauswahl zeigt zwei Häkchen und einen Wert von 13,97."  
[ImageContrastRatioLine]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png "Abbildung 13: die Zeile "Kontrastverhältnis" in der visuellen Auswahl"  
<!-- links -->  

[DevtoolsAccessibilityNavigation]: navigation.md "Navigieren in Microsoft Edge devtools mit Hilfstechnologien"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Anzeigen nur des CSS, das tatsächlich auf ein Element angewendet wird-CSS-Referenz"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "Axe – Web-Barrierefreiheits Tests – Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Barrierefreiheits Struktur (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Barrierefreiheit | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Sprachausgabe | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Kontrast (erweitert) AAA-Ebene | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Kontrast (Mindest) Ebene AA | W3C"  

> [!NOTE]
> <span data-ttu-id="9ce0c-245">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-245">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9ce0c-246">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="9ce0c-246">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="9ce0c-248">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9ce0c-248">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
description: Überprüfen und Ändern von Animationen mit dem Animations Inspektor für Microsoft Edge devtools
title: Überprüfen von Animationen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: fed686c07acd0648ac512dac131d85a317fb64eb
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124775"
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

# <span data-ttu-id="be023-104">Überprüfen von Animationen</span><span class="sxs-lookup"><span data-stu-id="be023-104">Inspect animations</span></span>  

<span data-ttu-id="be023-105">Überprüfen und Ändern von Animationen mit dem Animations Inspektor für Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="be023-105">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   <span data-ttu-id="be023-107">Animations Inspektor</span><span class="sxs-lookup"><span data-stu-id="be023-107">animation inspector</span></span>  
:::image-end:::  

### <span data-ttu-id="be023-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="be023-108">Summary</span></span>  

*   <span data-ttu-id="be023-109">Zeichnen Sie Animationen auf, indem Sie den Animations Inspektor öffnen.</span><span class="sxs-lookup"><span data-stu-id="be023-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="be023-110">Der Animations Inspektor erkennt und sortiert Animationen automatisch in Gruppen.</span><span class="sxs-lookup"><span data-stu-id="be023-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="be023-111">Überprüfen Sie Animationen, indem Sie Sie verlangsamen, jede einzelne wiedergeben oder den Quellcode anzeigen.</span><span class="sxs-lookup"><span data-stu-id="be023-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="be023-112">Sie können Animationen ändern, indem Sie den Offset für Anzeigedauer, Verzögerung, Dauer oder Keyframe ändern.</span><span class="sxs-lookup"><span data-stu-id="be023-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <span data-ttu-id="be023-113">Übersicht</span><span class="sxs-lookup"><span data-stu-id="be023-113">Overview</span></span>  

<span data-ttu-id="be023-114">Der Microsoft Edge devtools-Animations Inspektor hat zwei Hauptaufgaben.</span><span class="sxs-lookup"><span data-stu-id="be023-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="be023-115">Untersuchen von Animationen</span><span class="sxs-lookup"><span data-stu-id="be023-115">Inspecting animations.</span></span>  <span data-ttu-id="be023-116">Sie möchten den Quellcode für eine Animationsgruppe verlangsamen, wiedergeben oder überprüfen.</span><span class="sxs-lookup"><span data-stu-id="be023-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="be023-117">Ändern von Animationen</span><span class="sxs-lookup"><span data-stu-id="be023-117">Modifying animations.</span></span>  <span data-ttu-id="be023-118">Sie möchten die Zeitmessung, die Verzögerung, die Dauer oder den Keyframe-Offset einer Animationsgruppe ändern.</span><span class="sxs-lookup"><span data-stu-id="be023-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="be023-119">Bezier-und Keyframe-Bearbeitung werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be023-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="be023-120">Der Animations Inspektor unterstützt CSS-Animationen, CSS-Übergänge und Web-Animationen.</span><span class="sxs-lookup"><span data-stu-id="be023-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="be023-121">Animationen werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be023-121">animations are currently not supported.</span></span>  

### <span data-ttu-id="be023-122">Was ist eine Animationsgruppe?</span><span class="sxs-lookup"><span data-stu-id="be023-122">What is an Animation Group?</span></span>  

<span data-ttu-id="be023-123">Bei einer Animationsgruppe handelt es sich um eine Gruppe von Animationen, die möglicherweise miteinander in Beziehung stehen.</span><span class="sxs-lookup"><span data-stu-id="be023-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="be023-124">Derzeit hat das Web kein echtes Konzept einer Gruppen Animation, daher müssen Motion-Designer und-Entwickler einzelne Animationen zusammenstellen und verfassen, damit die Animationen als ein kohärenter visueller Effekt gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="be023-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="be023-125">Der Animations Inspektor prognostiziert, welche Animationen auf der Grundlage der Startzeit \ (ohne Verzögerungen usw.) zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="be023-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="be023-126">Der Animations Inspektor gruppiert auch die Animationen nebeneinander.</span><span class="sxs-lookup"><span data-stu-id="be023-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="be023-127">Mit anderen Worten: eine Gruppe von Animationen, die alle im gleichen Skriptblock ausgelöst werden, wird zusammen gruppiert.</span><span class="sxs-lookup"><span data-stu-id="be023-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="be023-128">Wenn eine Animation asynchron ist, wird Sie in eine separate Gruppe verschoben.</span><span class="sxs-lookup"><span data-stu-id="be023-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <span data-ttu-id="be023-129">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="be023-129">Get started</span></span>  

<span data-ttu-id="be023-130">Es gibt zwei Möglichkeiten, den Animations Inspektor zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="be023-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="be023-131">Öffnen des Menüs zum **anpassen und Steuern des devtools**</span><span class="sxs-lookup"><span data-stu-id="be023-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="be023-132">Navigieren Sie zum unter Menü **Weitere Tools** .</span><span class="sxs-lookup"><span data-stu-id="be023-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="be023-133">Auswählen von **Animationen**:</span><span class="sxs-lookup"><span data-stu-id="be023-133">Choose **Animations**:</span></span>  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           <span data-ttu-id="be023-135">**Animationen** mithilfe des Hauptmenüs</span><span class="sxs-lookup"><span data-stu-id="be023-135">**Animations** using Main Menu</span></span>  
    :::image-end:::  
        
*   <span data-ttu-id="be023-136">Öffnen des **Befehlsmenüs**</span><span class="sxs-lookup"><span data-stu-id="be023-136">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="be023-137">Geben Sie `Drawer: Show Animations` ein.</span><span class="sxs-lookup"><span data-stu-id="be023-137">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="be023-138">Der Animations Inspektor wird als Registerkarte neben dem Konsolen Einzug geöffnet.</span><span class="sxs-lookup"><span data-stu-id="be023-138">The Animation Inspector opens up as a tab next to the Console Drawer.</span></span>  <span data-ttu-id="be023-139">Da es sich bei dem Animations Inspektor um eine Schublade handelt, können Sie den Animations Inspektor in einem beliebigen devtools-Fenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="be023-139">Since the Animation Inspector is a Drawer tab, you may use the Animation Inspector from any DevTools panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   <span data-ttu-id="be023-141">Animations Inspektor leeren</span><span class="sxs-lookup"><span data-stu-id="be023-141">Empty Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="be023-142">Der Animations Inspektor ist in vier Hauptabschnitte unterteilt \ (oder Bereiche \).</span><span class="sxs-lookup"><span data-stu-id="be023-142">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="be023-143">Dieser Leitfaden bezieht sich auf jeden Bereich wie folgt:</span><span class="sxs-lookup"><span data-stu-id="be023-143">This guide refers to each pane as follows:</span></span>  

| <span data-ttu-id="be023-144">Index</span><span class="sxs-lookup"><span data-stu-id="be023-144">Index</span></span> | <span data-ttu-id="be023-145">Bereich</span><span class="sxs-lookup"><span data-stu-id="be023-145">Pane</span></span> | <span data-ttu-id="be023-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be023-146">Description</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="be023-147">1</span><span class="sxs-lookup"><span data-stu-id="be023-147">1</span></span> | **<span data-ttu-id="be023-148">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="be023-148">Controls</span></span>** | <span data-ttu-id="be023-149">Hier können Sie alle aktuell aufgenommenen Animationsgruppen löschen oder die Geschwindigkeit der aktuell ausgewählten Animationsgruppe ändern.</span><span class="sxs-lookup"><span data-stu-id="be023-149">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="be023-150">2</span><span class="sxs-lookup"><span data-stu-id="be023-150">2</span></span> | **<span data-ttu-id="be023-151">Übersicht</span><span class="sxs-lookup"><span data-stu-id="be023-151">Overview</span></span>** | <span data-ttu-id="be023-152">Wählen Sie hier eine Animationsgruppe aus, um Sie im **Detail** Bereich zu überprüfen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="be023-152">Select an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="be023-153">3</span><span class="sxs-lookup"><span data-stu-id="be023-153">3</span></span> | **<span data-ttu-id="be023-154">Zeitachse</span><span class="sxs-lookup"><span data-stu-id="be023-154">Timeline</span></span>** | <span data-ttu-id="be023-155">Pausieren und starten Sie eine Animation von hier aus, oder springen Sie zu einer bestimmten Stelle in der Animation.</span><span class="sxs-lookup"><span data-stu-id="be023-155">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="be023-156">4</span><span class="sxs-lookup"><span data-stu-id="be023-156">4</span></span> | **<span data-ttu-id="be023-157">Details</span><span class="sxs-lookup"><span data-stu-id="be023-157">Details</span></span>** | <span data-ttu-id="be023-158">Überprüfen und Ändern der aktuell ausgewählten Animationsgruppe</span><span class="sxs-lookup"><span data-stu-id="be023-158">Inspect and modify the currently selected Animation Group.</span></span> |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   <span data-ttu-id="be023-160">Animations Inspektor mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="be023-160">Annotated Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="be023-161">Wenn Sie eine Animation aufzeichnen möchten, führen Sie einfach die Interaktion aus, mit der die Animation ausgelöst wird, während der Animations Inspektor geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="be023-161">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="be023-162">Wenn beim Laden einer Seite eine Animation ausgelöst wird, laden Sie die Seite neu, wobei der Animations Inspektor geöffnet wird, um die Animation zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="be023-162">If an animation is triggered on page load, reload the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <span data-ttu-id="be023-163">Überprüfen von Animationen</span><span class="sxs-lookup"><span data-stu-id="be023-163">Inspect animations</span></span>  

<span data-ttu-id="be023-164">Nachdem Sie eine Animation aufgenommen haben, gibt es verschiedene Möglichkeiten, Sie wiederzugeben:</span><span class="sxs-lookup"><span data-stu-id="be023-164">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="be023-165">Zeigen Sie **mit der Maus** auf die Miniaturansicht im Übersichtsbereich, um eine Vorschau davon anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be023-165">Hover over the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="be023-166">Wählen **Sie im Übersichtsbereich die** Gruppe Animation aus, damit Sie im **Detail** Bereich angezeigt wird, und drücken Sie dann das Symbol **Wiedergabe** \ ( ![ Wiedergabe ][ImageReplayButtonIcon] -Symbol).</span><span class="sxs-lookup"><span data-stu-id="be023-166">Select the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and press the **replay** \(![replay icon][ImageReplayButtonIcon]\) icon.</span></span>  <span data-ttu-id="be023-167">Die Animation wird im Viewport wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="be023-167">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="be023-168">Klicken Sie auf die Symbole **Animationsgeschwindigkeit** \ ( ![ Animations Geschwindigkeits Symbole ][ImageAnimationSpeedButtonsIcon] \), um die Vorschau Geschwindigkeit der aktuell ausgewählten Animationsgruppe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="be023-168">Click on the **animation speed** \(![animation speed icons][ImageAnimationSpeedButtonsIcon]\) icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="be023-169">Sie können die rote vertikale Leiste verwenden, um Ihre aktuelle Position zu ändern.</span><span class="sxs-lookup"><span data-stu-id="be023-169">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="be023-170">Klicken Sie, und ziehen Sie den roten vertikalen Balken, um die Animation des Viewports zu schrubben.</span><span class="sxs-lookup"><span data-stu-id="be023-170">Click and drag the red vertical bar to scrub the viewport animation.</span></span>  
    
### <span data-ttu-id="be023-171">Anzeigen von Animations Details</span><span class="sxs-lookup"><span data-stu-id="be023-171">View animation details</span></span>  

<span data-ttu-id="be023-172">Nachdem Sie eine Animationsgruppe erfasst haben, klicken **Sie im Übersichtsbereich darauf** , um die Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be023-172">After you capture an Animation Group, click on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="be023-173">Im **Detail** Bereich wird jeder einzelnen Animation die Zeile a zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="be023-173">In the **Details** pane each individual animation is assigned the a row.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="be023-175">Animationsgruppen Details</span><span class="sxs-lookup"><span data-stu-id="be023-175">Animation Group details</span></span>  
:::image-end:::  

<span data-ttu-id="be023-176">Zeigen Sie mit der Maus auf eine Animation, um Sie im Viewport zu markieren.</span><span class="sxs-lookup"><span data-stu-id="be023-176">Hover over an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="be023-177">Klicken Sie auf die Animation, um Sie im **Element** Panel zu markieren.</span><span class="sxs-lookup"><span data-stu-id="be023-177">Click on the animation to select it in the **Elements** panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="be023-179">Zeigen Sie mit der Maus auf die Animation, um Sie im Viewport hervorzuheben</span><span class="sxs-lookup"><span data-stu-id="be023-179">Hover over the animation to highlight it in viewport</span></span>  
:::image-end:::  

<span data-ttu-id="be023-180">Der linke, dunklere Abschnitt einer Animation ist die Definition.</span><span class="sxs-lookup"><span data-stu-id="be023-180">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="be023-181">Der Rechte, verblasstere Abschnitt stellt Iterationen dar.</span><span class="sxs-lookup"><span data-stu-id="be023-181">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="be023-182">In der folgenden Abbildung stellen die Abschnitte zwei und drei beispielsweise Iterationen von Abschnitt eins dar.</span><span class="sxs-lookup"><span data-stu-id="be023-182">For example, in the following figure, sections two and three represent iterations of section one.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   <span data-ttu-id="be023-184">Diagramm der Animations Iterationen</span><span class="sxs-lookup"><span data-stu-id="be023-184">Diagram of animation iterations</span></span>  
:::image-end:::  

<span data-ttu-id="be023-185">Wenn für zwei Elemente dieselbe Animation angewendet wurde, weist der Animations Inspektor den Elementen dieselbe Farbe zu.</span><span class="sxs-lookup"><span data-stu-id="be023-185">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="be023-186">Die Farbe ist zufällig und hat keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="be023-186">The color is random and has no significance.</span></span>  <span data-ttu-id="be023-187">In der folgenden Abbildung finden Sie beispielsweise die beiden Elemente, `div.cwccw.earlier` und es werden die `div.cwccw.later` gleichen Animationen `spinrightleft` wie die `div.ccwcw.earlier` und- `div.ccwcw.later` Elemente angewendet.</span><span class="sxs-lookup"><span data-stu-id="be023-187">For example, in the following figure, the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   <span data-ttu-id="be023-189">Farbcodierte Animationen</span><span class="sxs-lookup"><span data-stu-id="be023-189">Color-coded animations</span></span>  
:::image-end:::  

## <span data-ttu-id="be023-190">Ändern von Animationen</span><span class="sxs-lookup"><span data-stu-id="be023-190">Modify animations</span></span>  

<span data-ttu-id="be023-191">Es gibt drei Möglichkeiten, wie Sie eine Animation mit dem Animations Inspektor ändern können.</span><span class="sxs-lookup"><span data-stu-id="be023-191">There are three ways you are able to modify an animation with the Animation Inspector.</span></span>  

*   <span data-ttu-id="be023-192">Animationsdauer.</span><span class="sxs-lookup"><span data-stu-id="be023-192">Animation duration.</span></span>  
*   <span data-ttu-id="be023-193">Keyframe-Anzeigedauern.</span><span class="sxs-lookup"><span data-stu-id="be023-193">Keyframe timings.</span></span>  
*   <span data-ttu-id="be023-194">Anfangszeit Verzögerung.</span><span class="sxs-lookup"><span data-stu-id="be023-194">Start time delay.</span></span>  
    
<span data-ttu-id="be023-195">In der folgenden Abbildung wird die ursprüngliche Animation dargestellt.</span><span class="sxs-lookup"><span data-stu-id="be023-195">In the following figure, the original animation is represented.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   <span data-ttu-id="be023-197">Ursprüngliche Animation vor der Änderung</span><span class="sxs-lookup"><span data-stu-id="be023-197">Original animation before modification</span></span>  
:::image-end:::  

<span data-ttu-id="be023-198">Wenn Sie die Dauer einer Animation ändern möchten, klicken Sie auf den ersten oder letzten Kreis, und ziehen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="be023-198">To change the duration of an animation, click and drag the first or last circle.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   <span data-ttu-id="be023-200">Geänderte Dauer</span><span class="sxs-lookup"><span data-stu-id="be023-200">Modified duration</span></span>  
:::image-end:::  

<span data-ttu-id="be023-201">Wenn die Animation Keyframe-Regeln definiert, werden diese als weiße innere Kreise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="be023-201">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="be023-202">Klicken Sie, und ziehen Sie eine der folgenden Schritte, um die Anzeigedauer des Keyframes zu ändern.</span><span class="sxs-lookup"><span data-stu-id="be023-202">Click and drag one of these to change the timing of the keyframe.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   <span data-ttu-id="be023-204">Geänderter Keyframe</span><span class="sxs-lookup"><span data-stu-id="be023-204">Modified keyframe</span></span>  
:::image-end:::  

<span data-ttu-id="be023-205">Wenn Sie einer Animation eine Verzögerung hinzufügen möchten, klicken Sie darauf, und ziehen Sie Sie mit Ausnahme der Kreise an eine beliebige Stelle.</span><span class="sxs-lookup"><span data-stu-id="be023-205">To add a delay to an animation, click and drag it anywhere except the circles.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   <span data-ttu-id="be023-207">Geänderte Verzögerung</span><span class="sxs-lookup"><span data-stu-id="be023-207">Modified delay</span></span>  
:::image-end:::  

## <span data-ttu-id="be023-208">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="be023-208">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="be023-209">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be023-209">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="be023-210">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="be023-210">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="be023-212">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="be023-212">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

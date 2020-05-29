---
title: Überprüfen von Animationen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 6466c7f0e1f8680a2429b565e8022d152d05d733
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568277"
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





# <span data-ttu-id="4fcf0-103">Überprüfen von Animationen</span><span class="sxs-lookup"><span data-stu-id="4fcf0-103">Inspect animations</span></span>   



<span data-ttu-id="4fcf0-104">Überprüfen und Ändern von Animationen mit dem Animations Inspektor für Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="4fcf0-104">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

> ##### <span data-ttu-id="4fcf0-105">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="4fcf0-105">Figure 1</span></span>  
> <span data-ttu-id="4fcf0-106">Animations Inspektor</span><span class="sxs-lookup"><span data-stu-id="4fcf0-106">Animation inspector</span></span>  
> ![Animations Inspektor][ImageAnimationInspector]  

### <span data-ttu-id="4fcf0-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4fcf0-108">Summary</span></span>  

*   <span data-ttu-id="4fcf0-109">Zeichnen Sie Animationen auf, indem Sie den Animations Inspektor öffnen.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="4fcf0-110">Der Animations Inspektor erkennt und sortiert Animationen automatisch in Gruppen.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="4fcf0-111">Überprüfen Sie Animationen, indem Sie Sie verlangsamen, jede einzelne wiedergeben oder den Quellcode anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="4fcf0-112">Sie können Animationen ändern, indem Sie den Offset für Anzeigedauer, Verzögerung, Dauer oder Keyframe ändern.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <span data-ttu-id="4fcf0-113">Übersicht</span><span class="sxs-lookup"><span data-stu-id="4fcf0-113">Overview</span></span>   

<span data-ttu-id="4fcf0-114">Der Microsoft Edge devtools-Animations Inspektor hat zwei Hauptaufgaben.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="4fcf0-115">Untersuchen von Animationen</span><span class="sxs-lookup"><span data-stu-id="4fcf0-115">Inspecting animations.</span></span>  <span data-ttu-id="4fcf0-116">Sie möchten den Quellcode für eine Animationsgruppe verlangsamen, wiedergeben oder überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="4fcf0-117">Ändern von Animationen</span><span class="sxs-lookup"><span data-stu-id="4fcf0-117">Modifying animations.</span></span>  <span data-ttu-id="4fcf0-118">Sie möchten die Zeitmessung, die Verzögerung, die Dauer oder den Keyframe-Offset einer Animationsgruppe ändern.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="4fcf0-119">Bezier-und Keyframe-Bearbeitung werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="4fcf0-120">Der Animations Inspektor unterstützt CSS-Animationen, CSS-Übergänge und Web-Animationen.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="4fcf0-121">Animationen werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-121">animations are currently not supported.</span></span>  

### <span data-ttu-id="4fcf0-122">Was ist eine Animationsgruppe?</span><span class="sxs-lookup"><span data-stu-id="4fcf0-122">What is an Animation Group?</span></span>  

<span data-ttu-id="4fcf0-123">Bei einer Animationsgruppe handelt es sich um eine Gruppe von Animationen, die möglicherweise miteinander in Beziehung stehen.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="4fcf0-124">Derzeit hat das Web kein echtes Konzept einer Gruppen Animation, daher müssen Motion-Designer und-Entwickler einzelne Animationen zusammenstellen und verfassen, damit die Animationen als ein kohärenter visueller Effekt gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="4fcf0-125">Der Animations Inspektor prognostiziert, welche Animationen auf der Grundlage der Startzeit \ (ohne Verzögerungen usw.) zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="4fcf0-126">Der Animations Inspektor gruppiert auch die Animationen nebeneinander.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="4fcf0-127">Mit anderen Worten: eine Gruppe von Animationen, die alle im gleichen Skriptblock ausgelöst werden, wird zusammen gruppiert.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="4fcf0-128">Wenn eine Animation asynchron ist, wird Sie in eine separate Gruppe verschoben.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <span data-ttu-id="4fcf0-129">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="4fcf0-129">Get started</span></span>  

<span data-ttu-id="4fcf0-130">Es gibt zwei Möglichkeiten, den Animations Inspektor zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="4fcf0-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="4fcf0-131">Öffnen des Menüs zum **anpassen und Steuern des devtools**</span><span class="sxs-lookup"><span data-stu-id="4fcf0-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="4fcf0-132">Navigieren Sie zum unter Menü **Weitere Tools** .</span><span class="sxs-lookup"><span data-stu-id="4fcf0-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="4fcf0-133">Wählen Sie **Animationen**aus:</span><span class="sxs-lookup"><span data-stu-id="4fcf0-133">Select **Animations**:</span></span>  
        
        > ##### <span data-ttu-id="4fcf0-134">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="4fcf0-134">Figure 2</span></span>  
        > <span data-ttu-id="4fcf0-135">Animationen über das Hauptmenü</span><span class="sxs-lookup"><span data-stu-id="4fcf0-135">Animations via Main Menu</span></span>  
        > ![Animationen über das Hauptmenü][ImageAnimationsViaMainMenu]  
        
*   <span data-ttu-id="4fcf0-137">Öffnen des **Befehlsmenüs**</span><span class="sxs-lookup"><span data-stu-id="4fcf0-137">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="4fcf0-138">Geben Sie `Drawer: Show Animations` ein.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-138">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="4fcf0-139">Der Animations Inspektor wird als Registerkarte neben dem Konsolen Einzug geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-139">The Animation Inspector opens up as a tab next to the Console Drawer.</span></span>  <span data-ttu-id="4fcf0-140">Da es sich bei dem Animations Inspektor um eine Schublade handelt, können Sie den Animations Inspektor in einem beliebigen devtools-Fenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-140">Since the Animation Inspector is a Drawer tab, you may use the Animation Inspector from any DevTools panel.</span></span>  

> ##### <span data-ttu-id="4fcf0-141">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="4fcf0-141">Figure 3</span></span>  
> <span data-ttu-id="4fcf0-142">Animations Inspektor leeren</span><span class="sxs-lookup"><span data-stu-id="4fcf0-142">Empty Animation Inspector</span></span>  
> ![Animations Inspektor leeren][ImageEmptyAnimationInspector]  

<span data-ttu-id="4fcf0-144">Der Animations Inspektor ist in vier Hauptabschnitte unterteilt \ (oder Bereiche \).</span><span class="sxs-lookup"><span data-stu-id="4fcf0-144">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="4fcf0-145">Dieser Leitfaden bezieht sich auf jeden Bereich wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4fcf0-145">This guide refers to each pane as follows:</span></span>  

| | <span data-ttu-id="4fcf0-146">Bereich</span><span class="sxs-lookup"><span data-stu-id="4fcf0-146">Pane</span></span> | <span data-ttu-id="4fcf0-147">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4fcf0-147">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="4fcf0-148">1</span><span class="sxs-lookup"><span data-stu-id="4fcf0-148">1</span></span> | **<span data-ttu-id="4fcf0-149">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="4fcf0-149">Controls</span></span>** | <span data-ttu-id="4fcf0-150">Hier können Sie alle aktuell aufgenommenen Animationsgruppen löschen oder die Geschwindigkeit der aktuell ausgewählten Animationsgruppe ändern.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-150">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="4fcf0-151">2</span><span class="sxs-lookup"><span data-stu-id="4fcf0-151">2</span></span> | **<span data-ttu-id="4fcf0-152">Übersicht</span><span class="sxs-lookup"><span data-stu-id="4fcf0-152">Overview</span></span>** | <span data-ttu-id="4fcf0-153">Wählen Sie hier eine Animationsgruppe aus, um Sie im **Detail** Bereich zu überprüfen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-153">Select an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="4fcf0-154">3</span><span class="sxs-lookup"><span data-stu-id="4fcf0-154">3</span></span> | **<span data-ttu-id="4fcf0-155">Zeitachse</span><span class="sxs-lookup"><span data-stu-id="4fcf0-155">Timeline</span></span>** | <span data-ttu-id="4fcf0-156">Pausieren und starten Sie eine Animation von hier aus, oder springen Sie zu einer bestimmten Stelle in der Animation.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-156">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="4fcf0-157">4</span><span class="sxs-lookup"><span data-stu-id="4fcf0-157">4</span></span> | **<span data-ttu-id="4fcf0-158">Details</span><span class="sxs-lookup"><span data-stu-id="4fcf0-158">Details</span></span>** | <span data-ttu-id="4fcf0-159">Überprüfen und Ändern der aktuell ausgewählten Animationsgruppe</span><span class="sxs-lookup"><span data-stu-id="4fcf0-159">Inspect and modify the currently selected Animation Group.</span></span> |  

> ##### <span data-ttu-id="4fcf0-160">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="4fcf0-160">Figure 4</span></span>  
> <span data-ttu-id="4fcf0-161">Animations Inspektor mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="4fcf0-161">Annotated Animation Inspector</span></span>  
> ![Animations Inspektor mit Anmerkungen][ImageAnnotatedAnimationInspector]  

<span data-ttu-id="4fcf0-163">Wenn Sie eine Animation aufzeichnen möchten, führen Sie einfach die Interaktion aus, mit der die Animation ausgelöst wird, während der Animations Inspektor geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-163">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="4fcf0-164">Wenn beim Laden einer Seite eine Animation ausgelöst wird, laden Sie die Seite neu, wobei der Animations Inspektor geöffnet wird, um die Animation zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-164">If an animation is triggered on page load, reload the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <span data-ttu-id="4fcf0-165">Überprüfen von Animationen</span><span class="sxs-lookup"><span data-stu-id="4fcf0-165">Inspect animations</span></span>   

<span data-ttu-id="4fcf0-166">Nachdem Sie eine Animation aufgenommen haben, gibt es verschiedene Möglichkeiten, Sie wiederzugeben:</span><span class="sxs-lookup"><span data-stu-id="4fcf0-166">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="4fcf0-167">Zeigen Sie **mit der Maus** auf die Miniaturansicht im Übersichtsbereich, um eine Vorschau davon anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-167">Hover over the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="4fcf0-168">Wählen Sie im Bereich " **Übersicht** " die Gruppe "Animation" aus, damit Sie im **Detail** Bereich angezeigt wird, und drücken Sie dann das Symbol Symbol **Wiedergabe wieder** geben ![ ][ImageReplayButtonIcon] .</span><span class="sxs-lookup"><span data-stu-id="4fcf0-168">Select the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and press the **replay** ![replay icon][ImageReplayButtonIcon] icon.</span></span>  <span data-ttu-id="4fcf0-169">Die Animation wird im Viewport wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-169">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="4fcf0-170">Klicken Sie auf **die Symbole für Animations** Geschwindigkeits ![ Geschwindigkeits Symbole ][ImageAnimationSpeedButtonsIcon] , um die Vorschau Geschwindigkeit der aktuell ausgewählten Animationsgruppe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-170">Click on the **animation speed** ![animation speed icons][ImageAnimationSpeedButtonsIcon] icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="4fcf0-171">Sie können die rote vertikale Leiste verwenden, um Ihre aktuelle Position zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-171">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="4fcf0-172">Klicken Sie, und ziehen Sie den roten vertikalen Balken, um die Animation des Viewports zu schrubben.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-172">Click and drag the red vertical bar to scrub the viewport animation.</span></span>  

### <span data-ttu-id="4fcf0-173">Anzeigen von Animations Details</span><span class="sxs-lookup"><span data-stu-id="4fcf0-173">View animation details</span></span>  

<span data-ttu-id="4fcf0-174">Nachdem Sie eine Animationsgruppe erfasst haben, klicken **Sie im Übersichtsbereich darauf** , um die Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-174">After you capture an Animation Group, click on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="4fcf0-175">Im **Detail** Bereich wird jeder einzelnen Animation die Zeile a zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-175">In the **Details** pane each individual animation is assigned the a row.</span></span>  

> ##### <span data-ttu-id="4fcf0-176">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="4fcf0-176">Figure 5</span></span>  
> <span data-ttu-id="4fcf0-177">Animationsgruppen Details</span><span class="sxs-lookup"><span data-stu-id="4fcf0-177">Animation Group details</span></span>  
> ![Animationsgruppen Details][ImageAnimationGroupDetails]  

<span data-ttu-id="4fcf0-179">Zeigen Sie mit der Maus auf eine Animation, um Sie im Viewport zu markieren.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-179">Hover over an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="4fcf0-180">Klicken Sie auf die Animation, um Sie im **Element** Panel zu markieren.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-180">Click on the animation to select it in the **Elements** panel.</span></span>  

> ##### <span data-ttu-id="4fcf0-181">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="4fcf0-181">Figure 6</span></span>  
> <span data-ttu-id="4fcf0-182">Zeigen Sie mit der Maus auf die Animation, um Sie im Viewport hervorzuheben</span><span class="sxs-lookup"><span data-stu-id="4fcf0-182">Hover over the animation to highlight it in viewport</span></span>  
> ![Zeigen Sie mit der Maus auf die Animation, um Sie im Viewport hervorzuheben][ImageHoverOverAnimationHighlightViewport]  

<span data-ttu-id="4fcf0-184">Der linke, dunklere Abschnitt einer Animation ist die Definition.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-184">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="4fcf0-185">Der Rechte, verblasstere Abschnitt stellt Iterationen dar.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-185">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="4fcf0-186">In [Abbildung 7](#figure-7)stellen beispielsweise Abschnitte zwei und drei Iterationen von Abschnitt eins dar.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-186">For example, in [Figure 7](#figure-7), sections two and three represent iterations of section one.</span></span>  

> ##### <span data-ttu-id="4fcf0-187">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="4fcf0-187">Figure 7</span></span>  
> <span data-ttu-id="4fcf0-188">Diagramm der Animations Iterationen</span><span class="sxs-lookup"><span data-stu-id="4fcf0-188">Diagram of animation iterations</span></span>  
> ![Diagramm der Animations Iterationen][ImageDiagramAnimationIterations]  

<span data-ttu-id="4fcf0-190">Wenn für zwei Elemente dieselbe Animation angewendet wurde, weist der Animations Inspektor den Elementen dieselbe Farbe zu.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-190">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="4fcf0-191">Die Farbe ist zufällig und hat keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-191">The color is random and has no significance.</span></span>  <span data-ttu-id="4fcf0-192">In [Abbildung 8](#figure-8) sind beispielsweise die beiden Elemente `div.cwccw.earlier` `div.cwccw.later` enthalten, und es wird dieselbe Animation `spinrightleft` wie für die `div.ccwcw.earlier` Elemente und verwendet `div.ccwcw.later` .</span><span class="sxs-lookup"><span data-stu-id="4fcf0-192">For example, in [Figure 8](#figure-8) the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

> ##### <span data-ttu-id="4fcf0-193">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="4fcf0-193">Figure 8</span></span>  
> <span data-ttu-id="4fcf0-194">Farbcodierte Animationen</span><span class="sxs-lookup"><span data-stu-id="4fcf0-194">Color-coded animations</span></span>  
> ![Farbcodierte Animationen][ImageColorCodedAnimations]  

## <span data-ttu-id="4fcf0-196">Ändern von Animationen</span><span class="sxs-lookup"><span data-stu-id="4fcf0-196">Modify animations</span></span>   

<span data-ttu-id="4fcf0-197">Es gibt drei Möglichkeiten, wie Sie eine Animation mit dem Animations Inspektor ändern können:</span><span class="sxs-lookup"><span data-stu-id="4fcf0-197">There are three ways you are able to modify an animation with the Animation Inspector:</span></span>  

*   <span data-ttu-id="4fcf0-198">Animationsdauer.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-198">Animation duration.</span></span>  
*   <span data-ttu-id="4fcf0-199">Keyframe-Anzeigedauern.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-199">Keyframe timings.</span></span>  
*   <span data-ttu-id="4fcf0-200">Anfangszeit Verzögerung.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-200">Start time delay.</span></span>  

<span data-ttu-id="4fcf0-201">In diesem Abschnitt wird angenommen, dass [Abbildung 9](#figure-9) die ursprüngliche Animation darstellt:</span><span class="sxs-lookup"><span data-stu-id="4fcf0-201">For this section suppose that [Figure 9](#figure-9) represents the original animation:</span></span>  

> ##### <span data-ttu-id="4fcf0-202">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="4fcf0-202">Figure 9</span></span>  
> <span data-ttu-id="4fcf0-203">Ursprüngliche Animation vor der Änderung</span><span class="sxs-lookup"><span data-stu-id="4fcf0-203">Original animation before modification</span></span>  
> ![Ursprüngliche Animation vor der Änderung][ImageOriginalAnimationBeforeModification]  

<span data-ttu-id="4fcf0-205">Wenn Sie die Dauer einer Animation ändern möchten, klicken Sie auf den ersten oder letzten Kreis, und ziehen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-205">To change the duration of an animation, click and drag the first or last circle.</span></span>  

> ##### <span data-ttu-id="4fcf0-206">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="4fcf0-206">Figure 10</span></span>  
> <span data-ttu-id="4fcf0-207">Geänderte Dauer</span><span class="sxs-lookup"><span data-stu-id="4fcf0-207">Modified duration</span></span>  
> ![Geänderte Dauer][ImageModifiedDuration]  

<span data-ttu-id="4fcf0-209">Wenn die Animation Keyframe-Regeln definiert, werden diese als weiße innere Kreise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-209">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="4fcf0-210">Klicken Sie, und ziehen Sie eine der folgenden Schritte, um die Anzeigedauer des Keyframes zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-210">Click and drag one of these to change the timing of the keyframe.</span></span>  

> ##### <span data-ttu-id="4fcf0-211">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="4fcf0-211">Figure 11</span></span>  
> <span data-ttu-id="4fcf0-212">Geänderter Keyframe</span><span class="sxs-lookup"><span data-stu-id="4fcf0-212">Modified keyframe</span></span>  
> ![Geänderter Keyframe][ImageModifiedKeyframe]  

<span data-ttu-id="4fcf0-214">Wenn Sie einer Animation eine Verzögerung hinzufügen möchten, klicken Sie darauf, und ziehen Sie Sie mit Ausnahme der Kreise an eine beliebige Stelle.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-214">To add a delay to an animation, click and drag it anywhere except the circles.</span></span>  

> ##### <span data-ttu-id="4fcf0-215">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="4fcf0-215">Figure 12</span></span>  
> <span data-ttu-id="4fcf0-216">Geänderte Verzögerung</span><span class="sxs-lookup"><span data-stu-id="4fcf0-216">Modified delay</span></span>  
> ![Geänderte Verzögerung][ImageModifiedDelay]  

<!--   -->  



<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: /microsoft-edge/devtools-guide-chromium/media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/replay-button-icon.msft.png  

[ImageAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-completed.msft.png "Abbildung 1: Animations Inspektor"  
[ImageAnimationsViaMainMenu]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-more-tools-animations.msft.png "Abbildung 2: Animationen über das Hauptmenü"  
[ImageEmptyAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations.msft.png "Abbildung 3: leeres Animations Inspektor"  
[ImageAnnotatedAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png "Abbildung 4: Inspektor für kommentierte Animationen"  
[ImageAnimationGroupDetails]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png "Abbildung 5: Details zur Animationsgruppe"  
[ImageHoverOverAnimationHighlightViewport]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png "Abbildung 6: zeigen Sie mit der Maus auf die Animation, um Sie im Viewport zu markieren."  
[ImageDiagramAnimationIterations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations-highlight.msft.png "Abbildung 7: Diagramm der Animations Iterationen"  
[ImageColorCodedAnimations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations.msft.png "Abbildung 8: farbcodierte Animationen"  
[ImageOriginalAnimationBeforeModification]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations.msft.png "Abbildung 9: ursprüngliche Animation vor der Änderung"  
[ImageModifiedDuration]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png "Abbildung 10: geänderte Dauer"  
[ImageModifiedKeyframe]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png "Abbildung 11: Geänderter Keyframe"  
[ImageModifiedDelay]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png "Abbildung 12: geänderte Verzögerung"  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="4fcf0-230">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4fcf0-231">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="4fcf0-233">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4fcf0-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

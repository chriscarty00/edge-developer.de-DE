---
description: Überprüfen und Ändern von Animationen mit dem Microsoft Edge DevTools Animation Inspector.
title: Überprüfen von Animationen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: a695517cb56da057e62293b5ca92b22058602f44
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564217"
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
# <a name="inspect-animations"></a><span data-ttu-id="05e40-104">Überprüfen von Animationen</span><span class="sxs-lookup"><span data-stu-id="05e40-104">Inspect animations</span></span>  

<span data-ttu-id="05e40-105">Überprüfen und Ändern von Animationen mit dem Microsoft Edge DevTools Animation Inspector.</span><span class="sxs-lookup"><span data-stu-id="05e40-105">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="Animationsinspektor" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   <span data-ttu-id="05e40-107">Animationsinspektor</span><span class="sxs-lookup"><span data-stu-id="05e40-107">animation inspector</span></span>  
:::image-end:::  

### <a name="summary"></a><span data-ttu-id="05e40-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="05e40-108">Summary</span></span>  

*   <span data-ttu-id="05e40-109">Erfassen Sie Animationen, indem Sie den Animationsinspektor öffnen.</span><span class="sxs-lookup"><span data-stu-id="05e40-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="05e40-110">Der Animationsinspektor erkennt und sortiert Animationen automatisch in Gruppen.</span><span class="sxs-lookup"><span data-stu-id="05e40-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="05e40-111">Überprüfen Sie Animationen, indem Sie die einzelnen Animationen verlangsamen, jeweils wiedergeben oder den Quellcode anzeigen.</span><span class="sxs-lookup"><span data-stu-id="05e40-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="05e40-112">Ändern Sie Animationen, indem Sie den Zeit-, Verzögerungs-, Dauer- oder Keyframeversatz ändern.</span><span class="sxs-lookup"><span data-stu-id="05e40-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <a name="overview"></a><span data-ttu-id="05e40-113">Übersicht</span><span class="sxs-lookup"><span data-stu-id="05e40-113">Overview</span></span>  

<span data-ttu-id="05e40-114">Der Microsoft Edge DevTools Animation Inspector hat zwei Hauptzwecke.</span><span class="sxs-lookup"><span data-stu-id="05e40-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="05e40-115">Überprüfen von Animationen.</span><span class="sxs-lookup"><span data-stu-id="05e40-115">Inspecting animations.</span></span>  <span data-ttu-id="05e40-116">Sie möchten den Quellcode für eine Animationsgruppe verlangsamen, wiedergeben oder überprüfen.</span><span class="sxs-lookup"><span data-stu-id="05e40-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="05e40-117">Ändern von Animationen.</span><span class="sxs-lookup"><span data-stu-id="05e40-117">Modifying animations.</span></span>  <span data-ttu-id="05e40-118">Sie möchten den Zeit-, Verzögerungs-, Dauer- oder Keyframeoffset einer Animationsgruppe ändern.</span><span class="sxs-lookup"><span data-stu-id="05e40-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="05e40-119">Die Bearbeitung von Bézier- und Keyframes wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05e40-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="05e40-120">Der Animationsinspektor unterstützt CSS-Animationen, CSS-Übergänge und Webanimationen.</span><span class="sxs-lookup"><span data-stu-id="05e40-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="05e40-121">Animationen werden derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05e40-121">animations are currently not supported.</span></span>  

### <a name="what-is-an-animation-group"></a><span data-ttu-id="05e40-122">Was ist eine Animationsgruppe?</span><span class="sxs-lookup"><span data-stu-id="05e40-122">What is an Animation Group?</span></span>  

<span data-ttu-id="05e40-123">Eine Animationsgruppe ist eine Gruppe von Animationen, die miteinander in Zusammenhang stehen können.</span><span class="sxs-lookup"><span data-stu-id="05e40-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="05e40-124">Derzeit verfügt das Web nicht über ein echtes Konzept einer Gruppenanimation, daher müssen Bewegungsdesigner und Entwickler einzelne Animationen verfassen und zeitigen, sodass die Animationen als ein zusammenhängender visueller Effekt gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="05e40-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="05e40-125">Der Animationsinspektor prognostiziert, welche Animationen basierend auf der Startzeit \(ohne Verzögerungen und so weiter\) verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="05e40-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="05e40-126">Der Animationsinspektor gruppen die Animationen auch nebeneinander.</span><span class="sxs-lookup"><span data-stu-id="05e40-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="05e40-127">Anders ausgedrückt: Eine Reihe von Animationen, die alle im gleichen Skriptblock ausgelöst werden, werden zusammen gruppieren.</span><span class="sxs-lookup"><span data-stu-id="05e40-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="05e40-128">Wenn eine Animation asynchron ist, wird sie in einer separaten Gruppe platziert.</span><span class="sxs-lookup"><span data-stu-id="05e40-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <a name="get-started"></a><span data-ttu-id="05e40-129">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="05e40-129">Get started</span></span>  

<span data-ttu-id="05e40-130">Es gibt zwei Möglichkeiten, den Animationsinspektor zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="05e40-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="05e40-131">Öffnen Sie **das Menü Anpassen und Steuern von DevTools**</span><span class="sxs-lookup"><span data-stu-id="05e40-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="05e40-132">Navigieren Sie zum **Untermenü Weitere** Tools.</span><span class="sxs-lookup"><span data-stu-id="05e40-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="05e40-133">Wählen Sie **Animationen**aus:</span><span class="sxs-lookup"><span data-stu-id="05e40-133">Choose **Animations**:</span></span>  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animationen mithilfe des Hauptmenüs" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           <span data-ttu-id="05e40-135">**Animationen** mithilfe des Hauptmenüs</span><span class="sxs-lookup"><span data-stu-id="05e40-135">**Animations** using Main Menu</span></span>  
        :::image-end:::  
        
*   <span data-ttu-id="05e40-136">Öffnen des **Befehlsmenüs**</span><span class="sxs-lookup"><span data-stu-id="05e40-136">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="05e40-137">Geben Sie `Drawer: Show Animations` ein.</span><span class="sxs-lookup"><span data-stu-id="05e40-137">Type `Drawer: Show Animations`.</span></span>  
        
<span data-ttu-id="05e40-138">Der Animationsinspektor wird neben dem **Konsolentool** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="05e40-138">The Animation Inspector opens next to the **Console** tool.</span></span>  <span data-ttu-id="05e40-139">Da der Animationsinspektor ein Drawer-Tool ist, können Sie den Animationsinspektor aus einem beliebigen DevTools-Bereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="05e40-139">Since the Animation Inspector is a Drawer tool, you may use the Animation Inspector from any DevTools panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Leerer Animationsinspektor" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   <span data-ttu-id="05e40-141">Leerer Animationsinspektor</span><span class="sxs-lookup"><span data-stu-id="05e40-141">Empty Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="05e40-142">Der Animationsinspektor ist in vier Hauptabschnitte \(oder Bereiche\) unterteilt.</span><span class="sxs-lookup"><span data-stu-id="05e40-142">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="05e40-143">Dieses Handbuch bezieht sich wie folgt auf jeden Bereich:</span><span class="sxs-lookup"><span data-stu-id="05e40-143">This guide refers to each pane as follows:</span></span>  

| <span data-ttu-id="05e40-144">Index</span><span class="sxs-lookup"><span data-stu-id="05e40-144">Index</span></span> | <span data-ttu-id="05e40-145">Bereich</span><span class="sxs-lookup"><span data-stu-id="05e40-145">Pane</span></span> | <span data-ttu-id="05e40-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05e40-146">Description</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="05e40-147">1</span><span class="sxs-lookup"><span data-stu-id="05e40-147">1</span></span> | **<span data-ttu-id="05e40-148">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="05e40-148">Controls</span></span>** | <span data-ttu-id="05e40-149">Hier können Sie alle aktuell erfassten Animationsgruppen löschen oder die Geschwindigkeit der aktuell ausgewählten Animationsgruppe ändern.</span><span class="sxs-lookup"><span data-stu-id="05e40-149">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="05e40-150">2</span><span class="sxs-lookup"><span data-stu-id="05e40-150">2</span></span> | **<span data-ttu-id="05e40-151">Übersicht</span><span class="sxs-lookup"><span data-stu-id="05e40-151">Overview</span></span>** | <span data-ttu-id="05e40-152">Wählen Sie hier eine Animationsgruppe aus, um sie im Detailbereich zu überprüfen **und zu** ändern.</span><span class="sxs-lookup"><span data-stu-id="05e40-152">Choose an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="05e40-153">3</span><span class="sxs-lookup"><span data-stu-id="05e40-153">3</span></span> | **<span data-ttu-id="05e40-154">Zeitachse</span><span class="sxs-lookup"><span data-stu-id="05e40-154">Timeline</span></span>** | <span data-ttu-id="05e40-155">Unterbrechen Und starten Sie eine Animation von hier aus, oder springen Sie zu einem bestimmten Punkt in der Animation.</span><span class="sxs-lookup"><span data-stu-id="05e40-155">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="05e40-156">4</span><span class="sxs-lookup"><span data-stu-id="05e40-156">4</span></span> | **<span data-ttu-id="05e40-157">Details</span><span class="sxs-lookup"><span data-stu-id="05e40-157">Details</span></span>** | <span data-ttu-id="05e40-158">Überprüfen und ändern Sie die aktuell ausgewählte Animationsgruppe.</span><span class="sxs-lookup"><span data-stu-id="05e40-158">Inspect and modify the currently selected Animation Group.</span></span> |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Animationsinspektor mit Anmerkungen" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   <span data-ttu-id="05e40-160">Animationsinspektor mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="05e40-160">Annotated Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="05e40-161">Führen Sie zum Erfassen einer Animation einfach die Interaktion aus, die die Animation auslöst, während der Animationsinspektor geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="05e40-161">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="05e40-162">Wenn eine Animation beim Laden der Seite ausgelöst wird, aktualisieren Sie die Seite, wenn der Animationsinspektor geöffnet ist, um die Animation zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="05e40-162">If an animation is triggered on page load, refresh the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <a name="inspect-animations"></a><span data-ttu-id="05e40-163">Überprüfen von Animationen</span><span class="sxs-lookup"><span data-stu-id="05e40-163">Inspect animations</span></span>  

<span data-ttu-id="05e40-164">Nachdem Sie eine Animation erfasst haben, gibt es einige Möglichkeiten, sie wieder zu wiedergeben:</span><span class="sxs-lookup"><span data-stu-id="05e40-164">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="05e40-165">Zeigen Sie auf die Miniaturansicht **im** Bereich Übersicht, um eine Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="05e40-165">Hover on the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="05e40-166">Wählen Sie die \*\*\*\* Animationsgruppe im Bereich Übersicht \(so, dass sie im **Detailbereich** angezeigt wird\) aus, und wählen Sie das Wiedergabesymbol **\(** ![ Wiedergabesymbol ](../media/replay-button-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="05e40-166">Choose the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and choose the **replay** \(![replay icon](../media/replay-button-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="05e40-167">Die Animation wird im Viewport wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="05e40-167">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="05e40-168">Wählen Sie **die Symbole für animationsgeschwindigkeit** \( Animationsgeschwindigkeit \) aus, um die Vorschaugeschwindigkeit der aktuell ausgewählten ![ ](../media/animation-speed-buttons-icon.msft.png) Animationsgruppe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="05e40-168">Choose the **animation speed** \(![animation speed icons](../media/animation-speed-buttons-icon.msft.png)\) icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="05e40-169">Sie können die rote vertikale Leiste verwenden, um Ihre aktuelle Position zu ändern.</span><span class="sxs-lookup"><span data-stu-id="05e40-169">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="05e40-170">Wählen Sie die rote vertikale Leiste aus, und ziehen Sie sie, um die Viewportanimation zu bereinigungen.</span><span class="sxs-lookup"><span data-stu-id="05e40-170">Choose and drag the red vertical bar to scrub the viewport animation.</span></span>  
    
### <a name="view-animation-details"></a><span data-ttu-id="05e40-171">Anzeigen von Animationsdetails</span><span class="sxs-lookup"><span data-stu-id="05e40-171">View animation details</span></span>  

<span data-ttu-id="05e40-172">Nachdem Sie eine Animationsgruppe erfasst haben, wählen Sie sie im Bereich **Übersicht** aus, um die Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="05e40-172">After you capture an Animation Group, choose on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="05e40-173">Im **Detailbereich** wird jeder einzelnen Animation die Zeile zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="05e40-173">In the **Details** pane each individual animation is assigned the a row.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Details zur Animationsgruppe" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="05e40-175">Details zur Animationsgruppe</span><span class="sxs-lookup"><span data-stu-id="05e40-175">Animation Group details</span></span>  
:::image-end:::  

<span data-ttu-id="05e40-176">Zeigen Sie auf eine Animation, um sie im Viewport zu markieren.</span><span class="sxs-lookup"><span data-stu-id="05e40-176">Hover on an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="05e40-177">Wählen Sie die Animation aus, um sie im **Elementtool auszuwählen.**</span><span class="sxs-lookup"><span data-stu-id="05e40-177">Choose the animation to select it in the **Elements** tool.</span></span>  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Zeigen Sie auf die Animation, um sie im Viewport zu markieren." lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="05e40-179">Zeigen Sie auf die Animation, um sie im Viewport zu markieren.</span><span class="sxs-lookup"><span data-stu-id="05e40-179">Hover on the animation to highlight it in viewport</span></span>  
:::image-end:::  

<span data-ttu-id="05e40-180">Der ganz links, dunklere Abschnitt einer Animation ist die Definition.</span><span class="sxs-lookup"><span data-stu-id="05e40-180">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="05e40-181">Der rechte, verblasste Abschnitt stellt Iterationen dar.</span><span class="sxs-lookup"><span data-stu-id="05e40-181">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="05e40-182">In der folgenden Abbildung stellen die Abschnitte 2 und 3 beispielsweise Iterationen von Abschnitt 1 dar.</span><span class="sxs-lookup"><span data-stu-id="05e40-182">For example, in the following figure, sections two and three represent iterations of section one.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagramm von Animationsiterationen" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   <span data-ttu-id="05e40-184">Diagramm von Animationsiterationen</span><span class="sxs-lookup"><span data-stu-id="05e40-184">Diagram of animation iterations</span></span>  
:::image-end:::  

<span data-ttu-id="05e40-185">Wenn zwei Elemente die gleiche Animation angewendet haben, weist der Animationsinspektor den Elementen dieselbe Farbe zu.</span><span class="sxs-lookup"><span data-stu-id="05e40-185">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="05e40-186">Die Farbe ist zufällig und hat keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="05e40-186">The color is random and has no significance.</span></span>  <span data-ttu-id="05e40-187">In der folgenden Abbildung werden z. B. die beiden Elemente mit derselben Animation `div.cwccw.earlier` `div.cwccw.later` \( \) angewendet, wie die `spinrightleft` `div.ccwcw.earlier` elemente `div.ccwcw.later` and.</span><span class="sxs-lookup"><span data-stu-id="05e40-187">For example, in the following figure, the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Farbcodete Animationen" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   <span data-ttu-id="05e40-189">Farbcodete Animationen</span><span class="sxs-lookup"><span data-stu-id="05e40-189">Color-coded animations</span></span>  
:::image-end:::  

## <a name="modify-animations"></a><span data-ttu-id="05e40-190">Ändern von Animationen</span><span class="sxs-lookup"><span data-stu-id="05e40-190">Modify animations</span></span>  

<span data-ttu-id="05e40-191">Es gibt drei Möglichkeiten, eine Animation mit dem Animationsinspektor zu ändern.</span><span class="sxs-lookup"><span data-stu-id="05e40-191">There are three ways you are able to modify an animation with the Animation Inspector.</span></span>  

*   <span data-ttu-id="05e40-192">Animationsdauer.</span><span class="sxs-lookup"><span data-stu-id="05e40-192">Animation duration.</span></span>  
*   <span data-ttu-id="05e40-193">Keyframe-Timings.</span><span class="sxs-lookup"><span data-stu-id="05e40-193">Keyframe timings.</span></span>  
*   <span data-ttu-id="05e40-194">Startzeitverzögerung.</span><span class="sxs-lookup"><span data-stu-id="05e40-194">Start time delay.</span></span>  
    
<span data-ttu-id="05e40-195">In der folgenden Abbildung wird die ursprüngliche Animation dargestellt.</span><span class="sxs-lookup"><span data-stu-id="05e40-195">In the following figure, the original animation is represented.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Originalanimation vor Änderung" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   <span data-ttu-id="05e40-197">Originalanimation vor Änderung</span><span class="sxs-lookup"><span data-stu-id="05e40-197">Original animation before modification</span></span>  
:::image-end:::  

<span data-ttu-id="05e40-198">Um die Dauer einer Animation zu ändern, wählen Sie den ersten oder letzten Kreis aus, und ziehen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="05e40-198">To change the duration of an animation, choose and drag the first or last circle.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Geänderte Dauer" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   <span data-ttu-id="05e40-200">Geänderte Dauer</span><span class="sxs-lookup"><span data-stu-id="05e40-200">Modified duration</span></span>  
:::image-end:::  

<span data-ttu-id="05e40-201">Wenn die Animation Keyframeregeln definiert, werden diese als weiße innere Kreise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="05e40-201">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="05e40-202">Wählen Sie einen dieser Elemente aus, und ziehen Sie ihn, um den Zeitpunkt des Keyframes zu ändern.</span><span class="sxs-lookup"><span data-stu-id="05e40-202">Choose and drag one of these to change the timing of the keyframe.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Geändertes Keyframe" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   <span data-ttu-id="05e40-204">Geändertes Keyframe</span><span class="sxs-lookup"><span data-stu-id="05e40-204">Modified keyframe</span></span>  
:::image-end:::  

<span data-ttu-id="05e40-205">Wenn Sie einer Animation eine Verzögerung hinzufügen möchten, wählen Sie sie aus, und ziehen Sie sie an eine beliebige Stelle mit Ausnahme der Kreise.</span><span class="sxs-lookup"><span data-stu-id="05e40-205">To add a delay to an animation, choose and drag it anywhere except the circles.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Geänderte Verzögerung" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   <span data-ttu-id="05e40-207">Geänderte Verzögerung</span><span class="sxs-lookup"><span data-stu-id="05e40-207">Modified delay</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="05e40-208">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="05e40-208">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="05e40-209">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05e40-209">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="05e40-210">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="05e40-210">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="05e40-212">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="05e40-212">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

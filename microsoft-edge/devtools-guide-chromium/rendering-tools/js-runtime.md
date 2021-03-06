---
description: Identifizieren Sie teure Funktionen mithilfe des Microsoft Edge DevTools-Speicherbereichs.
title: Beschleunigen der JavaScript-Laufzeit
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 682001ae8d265b342e5d6e0725f9f8ac4e298cf8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397601"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->

# <a name="speed-up-javascript-runtime"></a><span data-ttu-id="f9a8f-104">Beschleunigen der JavaScript-Laufzeit</span><span class="sxs-lookup"><span data-stu-id="f9a8f-104">Speed up JavaScript runtime</span></span>  

<span data-ttu-id="f9a8f-105">Identifizieren Sie teure Funktionen mithilfe des **Speicherbereichs.**</span><span class="sxs-lookup"><span data-stu-id="f9a8f-105">Identify expensive functions using the **Memory** panel.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Beispielprofile" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="f9a8f-107">Beispielprofile</span><span class="sxs-lookup"><span data-stu-id="f9a8f-107">Sample Profiles</span></span>  
:::image-end:::  

### <a name="summary"></a><span data-ttu-id="f9a8f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f9a8f-108">Summary</span></span>  

*   <span data-ttu-id="f9a8f-109">Zeichnen Sie genau auf, welche Funktionen aufgerufen wurden und wie viel Arbeitsspeicher die einzelnen Funktionen mit Demokation Sampling im **Speicherbereich** benötigen.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="f9a8f-110">Visualisieren Sie Ihre Profile als Flammendiagramm.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-110">Visualize your profiles as a flame chart.</span></span>  
    
## <a name="record-a-sampling-profile"></a><span data-ttu-id="f9a8f-111">Aufzeichnen eines Samplingprofils</span><span class="sxs-lookup"><span data-stu-id="f9a8f-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="f9a8f-112">Wenn Sie jank in Ihrem JavaScript bemerken, erfassen Sie ein Samplingprofil.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="f9a8f-113">Samplingprofile zeigen an, wo die Laufzeit für Funktionen auf Ihrer Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="f9a8f-114">Navigieren Sie zum **Speicherbereich** von DevTools.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-114">Navigate to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="f9a8f-115">Wählen Sie das **Optionsfeld Zuweisungsstichprobe** aus.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-115">Choose the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="f9a8f-116">Wählen Sie **Start**aus.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-116">Choose **Start**.</span></span>  
1.  <span data-ttu-id="f9a8f-117">Je nachdem, was Sie analysieren möchten, können Sie entweder die Seite aktualisieren, mit der Seite interagieren oder einfach die Seite ausführen lassen.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-117">Depending on what you are trying to analyze, you may either refresh the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="f9a8f-118">Wählen Sie die **Schaltfläche** Beenden aus, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-118">Choose the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="f9a8f-119">Sie können auch die [Console Utilities-API verwenden,][DevtoolsConsoleUtilities] um Profile über die Befehlszeile zu aufzeichnen und zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <a name="view-sampling-profile"></a><span data-ttu-id="f9a8f-120">Anzeigen des Samplingprofils</span><span class="sxs-lookup"><span data-stu-id="f9a8f-120">View Sampling Profile</span></span>  

<span data-ttu-id="f9a8f-121">Wenn Sie die Aufzeichnung abgeschlossen haben, \*\*\*\* füllt DevTools automatisch den Speicherbereich unter **SAMPLING PROFILES** mit den Daten aus Ihrer Aufzeichnung auf.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="f9a8f-122">Die Standardansicht ist **Heavy \(Bottom Up\)**.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="f9a8f-123">In dieser Ansicht können Sie überprüfen, welche Funktionen die Leistung am stärksten beeinträchtigen, und den anfordernden Pfad für jede Funktion untersuchen.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-123">This view allows you to review which functions had the most impact on performance and examine the requesting path for each function.</span></span>  

### <a name="change-sort-order"></a><span data-ttu-id="f9a8f-124">Sortierreihenfolge ändern</span><span class="sxs-lookup"><span data-stu-id="f9a8f-124">Change sort order</span></span>  

<span data-ttu-id="f9a8f-125">Wenn Sie die Sortierreihenfolge ändern möchten, wählen Sie das Dropdownmenü neben dem Symbol für ausgewählte Fokusfunktion **\(** ausgewählte Funktion im Fokus \) aus, und wählen Sie dann eine der ![ ][ImageFocusIcon] folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-125">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function][ImageFocusIcon]\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="f9a8f-126">**Diagramm**.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-126">**Chart**.</span></span>  <span data-ttu-id="f9a8f-127">Zeigt ein chronologisches Diagramm der Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-127">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Flammendiagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="f9a8f-129">Flammendiagramm</span><span class="sxs-lookup"><span data-stu-id="f9a8f-129">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="f9a8f-130">**Heavy \(Bottom Up\)**.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-130">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="f9a8f-131">Listet Funktionen nach Auswirkungen auf die Leistung auf und ermöglicht es Ihnen, die aufrufenden Pfade zu den Funktionen zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-131">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="f9a8f-132">Dies ist die Standardansicht.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-132">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Schweres Diagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="f9a8f-134">Schweres Diagramm</span><span class="sxs-lookup"><span data-stu-id="f9a8f-134">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="f9a8f-135">**Struktur \(Top Down\)**.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-135">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="f9a8f-136">Zeigt ein Gesamtbild der Anrufstruktur, beginnend am oberen Rand der Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-136">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Strukturdiagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="f9a8f-138">Strukturdiagramm</span><span class="sxs-lookup"><span data-stu-id="f9a8f-138">Tree chart</span></span>  
:::image-end:::  

### <a name="exclude-functions"></a><span data-ttu-id="f9a8f-139">Ausschließen von Funktionen</span><span class="sxs-lookup"><span data-stu-id="f9a8f-139">Exclude functions</span></span>  

<span data-ttu-id="f9a8f-140">Um eine Funktion aus Dem Samplingprofil auszuschließen, wählen Sie sie aus, und wählen Sie dann die Schaltfläche ausgewählte Funktion **ausschließen** \( ausgewählte Funktion ![ ausschließen ][ImageExcludeIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-140">To exclude a function from your Sampling Profile, select it and then select the **exclude selected function** \(![exclude selected function][ImageExcludeIcon]\) button.</span></span>  <span data-ttu-id="f9a8f-141">Die anfordernde Funktion \(parent\) der ausgeschlossenen Funktion \(child\) wird mit dem zugewiesenen Arbeitsspeicher belastet, der der ausgeschlossenen Funktion \(child\) zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-141">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="f9a8f-142">Wählen Sie **die Schaltfläche Alle Funktionen wiederherstellen** \( Alle Funktionen ![ wiederherstellen \) aus, um alle ausgeschlossenen Funktionen wieder in der ][ImageRestoreIcon] Aufzeichnung wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-142">Choose the **restore all functions** \(![restore all functions][ImageRestoreIcon]\) button to restore all excluded functions back into the recording.</span></span>  

## <a name="view-sampling-profile-as-chart"></a><span data-ttu-id="f9a8f-143">Anzeigen des Samplingprofils als Diagramm</span><span class="sxs-lookup"><span data-stu-id="f9a8f-143">View Sampling Profile as Chart</span></span>  

<span data-ttu-id="f9a8f-144">Die Diagrammansicht bietet eine visuelle Darstellung des Samplingprofils im Laufe der Zeit.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-144">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="f9a8f-145">Nachdem Sie [ein Samplingprofil aufgezeichnet haben,](#record-a-sampling-profile)zeigen Sie die Aufzeichnung als Flammendiagramm an, indem Sie [die Sortierreihenfolge in](#change-sort-order) Diagramm **ändern.**</span><span class="sxs-lookup"><span data-stu-id="f9a8f-145">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Flammendiagrammansicht" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="f9a8f-147">Flammendiagrammansicht</span><span class="sxs-lookup"><span data-stu-id="f9a8f-147">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="f9a8f-148">Das Flammendiagramm ist in zwei Teile unterteilt.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-148">The flame chart is split into two parts.</span></span>  

| <span data-ttu-id="f9a8f-149">index</span><span class="sxs-lookup"><span data-stu-id="f9a8f-149">index</span></span> | <span data-ttu-id="f9a8f-150">Bestandteil</span><span class="sxs-lookup"><span data-stu-id="f9a8f-150">Part</span></span> | <span data-ttu-id="f9a8f-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9a8f-151">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="f9a8f-152">1</span><span class="sxs-lookup"><span data-stu-id="f9a8f-152">1</span></span> | <span data-ttu-id="f9a8f-153">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f9a8f-153">Overview</span></span> | <span data-ttu-id="f9a8f-154">Eine Vogel-Augen-Ansicht der gesamten Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-154">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="f9a8f-155">Die Höhe der Balken entspricht der Tiefe der Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-155">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="f9a8f-156">Je höher die Leiste, desto tiefer die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-156">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="f9a8f-157">2</span><span class="sxs-lookup"><span data-stu-id="f9a8f-157">2</span></span> | <span data-ttu-id="f9a8f-158">Anrufstapel</span><span class="sxs-lookup"><span data-stu-id="f9a8f-158">Call Stacks</span></span> | <span data-ttu-id="f9a8f-159">Dies ist eine detaillierte Ansicht der Funktionen, die während der Aufzeichnung aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-159">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="f9a8f-160">Die horizontale Achse ist Zeit und vertikale Achse ist die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-160">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="f9a8f-161">Die Stapel sind von oben nach unten organisiert.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-161">The stacks are organized top-down.</span></span>  <span data-ttu-id="f9a8f-162">Die Funktion oben hat also die darunter genannte aufgerufen, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-162">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="f9a8f-163">Funktionen werden nach dem Zufallsprinzip gefärbt.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-163">Functions are colored randomly.</span></span>  <span data-ttu-id="f9a8f-164">Es besteht keine Korrelation mit den Farben, die in den anderen Panels verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-164">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="f9a8f-165">Funktionen sind jedoch bei Aufrufen immer gleich gefärbt, sodass Sie Muster in jeder Laufzeit beobachten können.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-165">However, functions are always colored the same across invocations so that you may observe patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Mit Anmerkungen versehenes Flammendiagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="f9a8f-167">Mit Anmerkungen versehenes Flammendiagramm</span><span class="sxs-lookup"><span data-stu-id="f9a8f-167">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="f9a8f-168">Eine hohe Aufrufliste ist nicht unbedingt wichtig, sondern bedeutet lediglich, dass viele Funktionen aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-168">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="f9a8f-169">Ein breiter Balken bedeutet jedoch, dass eine Funktion lange ge dauern hat, bis sie abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-169">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="f9a8f-170">Dies sind Kandidaten für die Optimierung.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-170">These are candidates for optimization.</span></span>  

### <a name="zoom-in-on-specific-parts-of-recording"></a><span data-ttu-id="f9a8f-171">Vergrößern bestimmter Teile der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="f9a8f-171">Zoom in on specific parts of recording</span></span>  

<span data-ttu-id="f9a8f-172">Wählen, halten und ziehen Sie die Maus nach links und rechts über die Übersicht, um bestimmte Teile der Anrufliste zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-172">Choose, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="f9a8f-173">Nach dem Zoomen zeigt die Aufrufliste automatisch den von Ihnen ausgewählten Teil der Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-173">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Diagramm verkleinert" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="f9a8f-175">Diagramm verkleinert</span><span class="sxs-lookup"><span data-stu-id="f9a8f-175">Chart zoomed</span></span>  
:::image-end:::  

### <a name="view-function-details"></a><span data-ttu-id="f9a8f-176">Anzeigen von Funktionsdetails</span><span class="sxs-lookup"><span data-stu-id="f9a8f-176">View function details</span></span>  

<span data-ttu-id="f9a8f-177">Wählen Sie eine Funktion aus, um die Definition im Bereich **Quellen anzeigen** zu können.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-177">Choose a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="f9a8f-178">Zeigen Sie auf eine Funktion, um den Namen und die Zeitdaten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-178">Hover on a function to display the name and timing data.</span></span>  <span data-ttu-id="f9a8f-179">Die folgenden Informationen werden bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-179">The following information is provided.</span></span>  

| <span data-ttu-id="f9a8f-180">Detail</span><span class="sxs-lookup"><span data-stu-id="f9a8f-180">Detail</span></span> | <span data-ttu-id="f9a8f-181">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9a8f-181">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="f9a8f-182">Name</span><span class="sxs-lookup"><span data-stu-id="f9a8f-182">Name</span></span>** | <span data-ttu-id="f9a8f-183">Der Name der Funktion.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-183">The name of the function.</span></span>  |  
| **<span data-ttu-id="f9a8f-184">Self size</span><span class="sxs-lookup"><span data-stu-id="f9a8f-184">Self size</span></span>** | <span data-ttu-id="f9a8f-185">Die Größe des aktuellen Aufrufs der Funktion, einschließlich nur der Anweisungen in der Funktion.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-185">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="f9a8f-186">Gesamtgröße</span><span class="sxs-lookup"><span data-stu-id="f9a8f-186">Total size</span></span>** | <span data-ttu-id="f9a8f-187">Die Größe des aktuellen Aufrufs dieser Funktion und aller von ihr aufgerufenen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-187">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="f9a8f-188">URL</span><span class="sxs-lookup"><span data-stu-id="f9a8f-188">URL</span></span>** | <span data-ttu-id="f9a8f-189">Die Position der Funktionsdefinition in Form von where ist der Name der Datei, in der die Funktion definiert ist, und die `base.js:261` `base.js` `261` Zeilennummer der Definition.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-189">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Anzeigen von Funktionsdetails im Diagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="f9a8f-191">Anzeigen von Funktionsdetails im Diagramm</span><span class="sxs-lookup"><span data-stu-id="f9a8f-191">View functions details in chart</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f9a8f-192">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="f9a8f-192">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Api-Referenz für Konsolenprogramme | Microsoft Docs"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "profile – Apireferenz für Konsolenprogramme | Microsoft Docs"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd – Api-Referenz für Konsolenprogramme | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="f9a8f-196">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f9a8f-197">Die ursprüngliche Seite [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) befindet sich hier und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) und [Meggin Kearney][MegginKearney] \(Tech Writer\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="f9a8f-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="f9a8f-199">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f9a8f-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

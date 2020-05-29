---
title: Beschleunigen der JavaScript-Laufzeit
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 0e198be3e1cef53590a24bfaa2382746ced299ed
ms.sourcegitcommit: 0342d99bf8d3212068890bab0e1e960afa507c02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611871"
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





# <span data-ttu-id="a0251-103">Beschleunigen der JavaScript-Laufzeit</span><span class="sxs-lookup"><span data-stu-id="a0251-103">Speed Up JavaScript Runtime</span></span>   




<span data-ttu-id="a0251-104">Ermitteln Sie mit dem **Speicher** Panel kostspielige Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a0251-104">Identify expensive functions using the **Memory** panel.</span></span>  

> ##### <span data-ttu-id="a0251-105">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="a0251-105">Figure 1</span></span>  
> <span data-ttu-id="a0251-106">Sampling-profile</span><span class="sxs-lookup"><span data-stu-id="a0251-106">Sampling Profiles</span></span>  
> ![Sampling-profile][ImageCpuProfile]  

### <span data-ttu-id="a0251-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a0251-108">Summary</span></span>  

*   <span data-ttu-id="a0251-109">Zeichnen Sie genau auf, welche Funktionen aufgerufen wurden und wie viel Arbeitsspeicher für die Zuweisungs Stichproben im **Speicher** Panel erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a0251-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="a0251-110">Visualisieren Sie Ihre Profile als Flammen Diagramm.</span><span class="sxs-lookup"><span data-stu-id="a0251-110">Visualize your profiles as a flame chart.</span></span>  

## <span data-ttu-id="a0251-111">Aufzeichnen eines Stichproben Profils</span><span class="sxs-lookup"><span data-stu-id="a0251-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="a0251-112">Wenn Sie Jank in Ihrem JavaScript bemerken, erfassen Sie ein Sampling-Profil.</span><span class="sxs-lookup"><span data-stu-id="a0251-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="a0251-113">Sampling-Profile zeigen an, wo die Laufzeit für Funktionen auf der Seite aufgewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0251-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="a0251-114">Wechseln Sie zum **Speicher** Panel von devtools.</span><span class="sxs-lookup"><span data-stu-id="a0251-114">Go to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="a0251-115">Aktivieren Sie das Optionsfeld **Zuweisungs Sampling** .</span><span class="sxs-lookup"><span data-stu-id="a0251-115">Select the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="a0251-116">Wählen Sie **Start**.</span><span class="sxs-lookup"><span data-stu-id="a0251-116">Select **Start**.</span></span>  
1.  <span data-ttu-id="a0251-117">Je nachdem, was Sie analysieren möchten, können Sie entweder die Seite neu laden, mit der Seite interagieren oder einfach die Seite ausführen lassen.</span><span class="sxs-lookup"><span data-stu-id="a0251-117">Depending on what you are trying to analyze, you may either reload the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="a0251-118">Wählen Sie die Schaltfläche **Beenden** aus, wenn Sie den Vorgang beendet haben.</span><span class="sxs-lookup"><span data-stu-id="a0251-118">Select the **Stop** button when you are finished.</span></span>  

> [!NOTE]
> <span data-ttu-id="a0251-119">Sie können auch die API für die [Konsolen Dienstprogramme][DevtoolsConsoleUtilities] zum Aufzeichnen und Gruppieren von Profilen über die Befehlszeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0251-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <span data-ttu-id="a0251-120">Sampling-Profil anzeigen</span><span class="sxs-lookup"><span data-stu-id="a0251-120">View Sampling Profile</span></span>  

<span data-ttu-id="a0251-121">Wenn Sie die Aufzeichnung abgeschlossen haben, füllt devtools den **Speicher** Panel automatisch unter **Sampling-profile** mit den Daten aus ihrer Aufzeichnung auf.</span><span class="sxs-lookup"><span data-stu-id="a0251-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="a0251-122">Die Standardansicht ist **schwer. \ (Bottom up \)**.</span><span class="sxs-lookup"><span data-stu-id="a0251-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="a0251-123">In dieser Ansicht können Sie sehen, welche Funktionen die meisten Auswirkungen auf die Leistung haben, und die Aufruf Pfade für diese Funktionen untersuchen.</span><span class="sxs-lookup"><span data-stu-id="a0251-123">This view enables you to see which functions had the most impact on performance and examine the calling paths to those functions.</span></span>  

### <span data-ttu-id="a0251-124">Ändern der Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="a0251-124">Change sort order</span></span>   

<span data-ttu-id="a0251-125">Wenn Sie die Sortierreihenfolge ändern möchten, wählen Sie das Dropdownmenü **neben dem Fokus ausgewählte Funktions** Symbol ausgewählte Funktion aus, ![ ][ImageFocusIcon] und wählen Sie dann eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="a0251-125">To change the sorting order, select the dropdown menu next to the **focus selected function** ![focus selected function][ImageFocusIcon] icon and then choose one of the following options.</span></span>

<span data-ttu-id="a0251-126">**Diagramm**aus.</span><span class="sxs-lookup"><span data-stu-id="a0251-126">**Chart**.</span></span>  <span data-ttu-id="a0251-127">Zeigt ein chronologisches Diagramm der Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="a0251-127">Displays a chronological chart of the recording.</span></span>  

> ##### <span data-ttu-id="a0251-128">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="a0251-128">Figure 2</span></span>  
> <span data-ttu-id="a0251-129">Flamm Diagramm</span><span class="sxs-lookup"><span data-stu-id="a0251-129">Flame chart</span></span>  
> ![Flamm Diagramm][ImageFlameChart]  

<span data-ttu-id="a0251-131">**Heavy \ (Bottom up \)**.</span><span class="sxs-lookup"><span data-stu-id="a0251-131">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="a0251-132">Listet Funktionen nach Auswirkungen auf die Leistung auf und ermöglicht Ihnen, die Aufruf Pfade zu den Funktionen zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="a0251-132">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="a0251-133">Dies ist die Standardansicht.</span><span class="sxs-lookup"><span data-stu-id="a0251-133">This is the default view.</span></span>  

> ##### <span data-ttu-id="a0251-134">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="a0251-134">Figure 3</span></span>  
> <span data-ttu-id="a0251-135">Schweres Diagramm</span><span class="sxs-lookup"><span data-stu-id="a0251-135">Heavy chart</span></span>  
> ![Schweres Diagramm][ImageHeavyChart]  

<span data-ttu-id="a0251-137">**Struktur \ (oben)**</span><span class="sxs-lookup"><span data-stu-id="a0251-137">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="a0251-138">Zeigt ein Gesamtbild der aufrufenden Struktur, beginnend am oberen Rand der Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="a0251-138">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

> ##### <span data-ttu-id="a0251-139">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="a0251-139">Figure 4</span></span>  
> <span data-ttu-id="a0251-140">Strukturdiagramm</span><span class="sxs-lookup"><span data-stu-id="a0251-140">Tree chart</span></span>  
> ![Strukturdiagramm][ImageTreeChart]  

### <span data-ttu-id="a0251-142">Ausschließen von Funktionen</span><span class="sxs-lookup"><span data-stu-id="a0251-142">Exclude functions</span></span>   

<span data-ttu-id="a0251-143">Wenn Sie eine Funktion aus Ihrem Stichproben Profil ausschließen möchten, wählen Sie Sie aus, um Sie zu markieren, und wählen Sie dann das Symbol ausgewählte **Funktion ausschließen aus** ![ ][ImageExcludeIcon] .</span><span class="sxs-lookup"><span data-stu-id="a0251-143">To exclude a function from your Sampling Profile, select it to select it and then select the **exclude selected function** ![exclude selected function][ImageExcludeIcon] icon.</span></span>  <span data-ttu-id="a0251-144">Die anfordernde Funktion \ (übergeordnete \) der ausgeschlossenen Funktion \ (untergeordnete \) wird mit dem zugewiesenen Arbeitsspeicher belastet, der der ausgeschlossenen Funktion zugeordnet ist (untergeordnete \).</span><span class="sxs-lookup"><span data-stu-id="a0251-144">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="a0251-145">Wählen Sie **das Symbol alle Funktionen** wiederherstellen alle Funktionen wiederherstellen aus ![ ][ImageRestoreIcon] , um alle ausgeschlossenen Funktionen wieder in die Aufzeichnung zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="a0251-145">Select the **restore all functions** ![restore all functions][ImageRestoreIcon] icon to restore all excluded functions back into the recording.</span></span>  

## <span data-ttu-id="a0251-146">Sampling-Profil als Diagramm anzeigen</span><span class="sxs-lookup"><span data-stu-id="a0251-146">View Sampling Profile as Chart</span></span>   

<span data-ttu-id="a0251-147">Die Diagrammansicht bietet eine visuelle Darstellung des Sampling-Profils über einen Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="a0251-147">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="a0251-148">Nachdem Sie [ein Stichproben Profil aufgezeichnet](#record-a-sampling-profile)haben, zeigen Sie die Aufzeichnung als Flammen Diagramm an, indem Sie [die Sortierreihenfolge](#change-sort-order) in **Diagramm**ändern.</span><span class="sxs-lookup"><span data-stu-id="a0251-148">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

> ##### <span data-ttu-id="a0251-149">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="a0251-149">Figure 5</span></span>  
> <span data-ttu-id="a0251-150">Ansicht "Flammen Diagramm"</span><span class="sxs-lookup"><span data-stu-id="a0251-150">Flame chart view</span></span>  
> ![Ansicht "Flammen Diagramm"][ImageFlameChartView]  

<span data-ttu-id="a0251-152">Das Flammen Diagramm ist in zwei Teile aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="a0251-152">The flame chart is split into two parts.</span></span>  

| | <span data-ttu-id="a0251-153">Bestandteil</span><span class="sxs-lookup"><span data-stu-id="a0251-153">Part</span></span> | <span data-ttu-id="a0251-154">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0251-154">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="a0251-155">1</span><span class="sxs-lookup"><span data-stu-id="a0251-155">1</span></span> | <span data-ttu-id="a0251-156">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a0251-156">Overview</span></span> | <span data-ttu-id="a0251-157">Eine Vogelperspektive der gesamten Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="a0251-157">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="a0251-158">Die Höhe der Balken entspricht der Tiefe der Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="a0251-158">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="a0251-159">Je höher die Leiste, desto tiefer die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="a0251-159">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="a0251-160">2</span><span class="sxs-lookup"><span data-stu-id="a0251-160">2</span></span> | <span data-ttu-id="a0251-161">Anruflisten</span><span class="sxs-lookup"><span data-stu-id="a0251-161">Call Stacks</span></span> | <span data-ttu-id="a0251-162">Hierbei handelt es sich um eine detaillierte Ansicht der Funktionen, die während der Aufzeichnung aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="a0251-162">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="a0251-163">Die horizontale Achse ist Zeit, und die vertikale Achse ist die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="a0251-163">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="a0251-164">Die Stapel werden oben nach unten angeordnet.</span><span class="sxs-lookup"><span data-stu-id="a0251-164">The stacks are organized top-down.</span></span>  <span data-ttu-id="a0251-165">So nennt sich die Funktion oben die untere und so weiter.</span><span class="sxs-lookup"><span data-stu-id="a0251-165">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="a0251-166">Funktionen werden nach dem Zufallsprinzip eingefärbt.</span><span class="sxs-lookup"><span data-stu-id="a0251-166">Functions are colored randomly.</span></span>  <span data-ttu-id="a0251-167">Es gibt keine Korrelation zu den in den anderen Bereichen verwendeten Farben.</span><span class="sxs-lookup"><span data-stu-id="a0251-167">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="a0251-168">Funktionen werden allerdings immer gleich über Aufrufe eingefärbt, sodass Sie in jeder Laufzeit Muster sehen können.</span><span class="sxs-lookup"><span data-stu-id="a0251-168">However, functions are always colored the same across invocations so that you are able to see patterns in each runtime.</span></span>  

> ##### <span data-ttu-id="a0251-169">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="a0251-169">Figure 6</span></span>  
> <span data-ttu-id="a0251-170">Flamm Diagramm mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="a0251-170">Annotated flame chart</span></span>  
> ![Flamm Diagramm mit Anmerkungen][ImageAnnotatedFlameChart]  

<span data-ttu-id="a0251-172">Eine hohe Aufrufliste ist nicht unbedingt wichtig, Sie bedeutet nur, dass viele Funktionen aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="a0251-172">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="a0251-173">Eine breite Leiste bedeutet aber, dass eine Funktion lange Zeit in Anspruch genommen hat.</span><span class="sxs-lookup"><span data-stu-id="a0251-173">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="a0251-174">Diese sind Kandidaten für die Optimierung.</span><span class="sxs-lookup"><span data-stu-id="a0251-174">These are candidates for optimization.</span></span>  

### <span data-ttu-id="a0251-175">Vergrößern bestimmter Teile der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="a0251-175">Zoom in on specific parts of recording</span></span>   

<span data-ttu-id="a0251-176">Wählen, halten und ziehen Sie die Maus nach links und rechts über die Übersicht, um bestimmte Teile der Anrufliste zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="a0251-176">Select, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="a0251-177">Nachdem Sie die Ansicht gezoomt haben, wird in der Aufrufliste automatisch der Teil der Aufzeichnung angezeigt, den Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="a0251-177">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

> ##### <span data-ttu-id="a0251-178">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="a0251-178">Figure 7</span></span>  
> <span data-ttu-id="a0251-179">Diagramm vergrößert</span><span class="sxs-lookup"><span data-stu-id="a0251-179">Chart zoomed</span></span>  
> ![Diagramm vergrößert][ImageFlameChartZoomed]  

### <span data-ttu-id="a0251-181">Anzeigen von Funktionsdetails</span><span class="sxs-lookup"><span data-stu-id="a0251-181">View function details</span></span>   

<span data-ttu-id="a0251-182">Wählen Sie eine Funktion aus, um die Definition im **Quellen** Panel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0251-182">Select on a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="a0251-183">Zeigen Sie mit der Maus auf eine Funktion, um die Namen-und Anzeigedauer Daten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a0251-183">Hover over a function to display the name and timing data.</span></span>  <span data-ttu-id="a0251-184">Die folgenden Informationen werden bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a0251-184">The following information is provided.</span></span>  

| <span data-ttu-id="a0251-185">Detail</span><span class="sxs-lookup"><span data-stu-id="a0251-185">Detail</span></span> | <span data-ttu-id="a0251-186">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0251-186">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="a0251-187">Name</span><span class="sxs-lookup"><span data-stu-id="a0251-187">Name</span></span>** | <span data-ttu-id="a0251-188">Der Name der Funktion.</span><span class="sxs-lookup"><span data-stu-id="a0251-188">The name of the function.</span></span>  |  
| **<span data-ttu-id="a0251-189">Selbst Größe</span><span class="sxs-lookup"><span data-stu-id="a0251-189">Self size</span></span>** | <span data-ttu-id="a0251-190">Die Größe des aktuellen Aufrufs der Funktion, einschließlich nur der Anweisungen in der Funktion.</span><span class="sxs-lookup"><span data-stu-id="a0251-190">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="a0251-191">Gesamtgröße</span><span class="sxs-lookup"><span data-stu-id="a0251-191">Total size</span></span>** | <span data-ttu-id="a0251-192">Die Größe des aktuellen Aufrufs dieser Funktion und der von ihr aufgerufenen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a0251-192">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="a0251-193">URL</span><span class="sxs-lookup"><span data-stu-id="a0251-193">URL</span></span>** | <span data-ttu-id="a0251-194">Die Position der Funktionsdefinition in Form von `base.js:261` Where `base.js` ist der Name der Datei, in der die Funktion definiert ist, und `261` die Nummer der Zeile der Definition.</span><span class="sxs-lookup"><span data-stu-id="a0251-194">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

> ##### <span data-ttu-id="a0251-195">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="a0251-195">Figure 8</span></span>  
> <span data-ttu-id="a0251-196">Anzeigen von Funktionsdetails in einem Diagramm</span><span class="sxs-lookup"><span data-stu-id="a0251-196">Viewing functions details in chart</span></span>  
> ![Anzeigen von Funktionsdetails in einem Diagramm][ImageFunctionsDetails]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageExcludeIcon]: /microsoft-edge/devtools-guide-chromium/media/exclude-icon.msft.png  
[ImageFocusIcon]: /microsoft-edge/devtools-guide-chromium/media/images/focus-icon.msft.png  
[ImageRestoreIcon]: /microsoft-edge/devtools-guide-chromium/media/images/restore-icon.msft.png  

[ImageCpuProfile]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png "Abbildung 1: Sampling-profile"  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png "Abbildung 2: Flammen Diagramm"  
[ImageHeavyChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png "Abbildung 3: schweres Diagramm"  
[ImageTreeChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png "Abbildung 4: Strukturdiagramm"  
[ImageFlameChartView]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png "Abbildung 5: Ansicht "Flammen Diagramm""  
[ImageAnnotatedFlameChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png "Abbildung 6: kommentiertes Flammen Diagramm"  
[ImageFlameChartZoomed]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png "Abbildung 7: Diagramm vergrößert"  
[ImageFunctionsDetails]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png "Abbildung 8: Anzeigen von Funktionsdetails in einem Diagramm"  

<!-- links -->  

[DevtoolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "API-Referenz für Konsolen Dienstprogramme"  
[DevtoolsConsoleUtilitiesProfile]: /microsoft-edge/devtools-guide-chromium/console/utilities#profile "API-Referenz für Profil-Console-Utilities"  
[DevtoolsConsoleUtilitiesProfileEnd]: /microsoft-edge/devtools-guide-chromium/console/utilities#profileend "API-Referenz zu profileEnd-Console Utilities"  

> [!NOTE]
> <span data-ttu-id="a0251-209">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0251-209">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a0251-210">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) gefunden und von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools & Lighthouse \) und [Meggin Kearney][MegginKearney] \ (Tech Writer \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="a0251-210">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="a0251-212">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a0251-212">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

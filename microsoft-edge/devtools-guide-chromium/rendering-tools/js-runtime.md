---
title: Beschleunigen der JavaScript-Laufzeit
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 801de4beeec29010ef63b2bcda950b57d4e544f7
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986185"
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

# <span data-ttu-id="83edc-103">Beschleunigen der JavaScript-Laufzeit</span><span class="sxs-lookup"><span data-stu-id="83edc-103">Speed up JavaScript runtime</span></span>  

<span data-ttu-id="83edc-104">Ermitteln Sie mit dem **Speicher** Panel kostspielige Funktionen.</span><span class="sxs-lookup"><span data-stu-id="83edc-104">Identify expensive functions using the **Memory** panel.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Beispielprofile" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="83edc-106">Beispielprofile</span><span class="sxs-lookup"><span data-stu-id="83edc-106">Sample Profiles</span></span>  
:::image-end:::  

### <span data-ttu-id="83edc-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="83edc-107">Summary</span></span>  

*   <span data-ttu-id="83edc-108">Zeichnen Sie genau auf, welche Funktionen aufgerufen wurden und wie viel Arbeitsspeicher für die Zuweisungs Stichproben im **Speicher** Panel erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="83edc-108">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="83edc-109">Visualisieren Sie Ihre Profile als Flammen Diagramm.</span><span class="sxs-lookup"><span data-stu-id="83edc-109">Visualize your profiles as a flame chart.</span></span>  
    
## <span data-ttu-id="83edc-110">Aufzeichnen eines Stichproben Profils</span><span class="sxs-lookup"><span data-stu-id="83edc-110">Record a Sampling Profile</span></span>  

<span data-ttu-id="83edc-111">Wenn Sie Jank in Ihrem JavaScript bemerken, erfassen Sie ein Sampling-Profil.</span><span class="sxs-lookup"><span data-stu-id="83edc-111">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="83edc-112">Sampling-Profile zeigen an, wo die Laufzeit für Funktionen auf der Seite aufgewendet wird.</span><span class="sxs-lookup"><span data-stu-id="83edc-112">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="83edc-113">Wechseln Sie zum **Speicher** Panel von devtools.</span><span class="sxs-lookup"><span data-stu-id="83edc-113">Go to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="83edc-114">Aktivieren Sie das Optionsfeld **Zuweisungs Sampling** .</span><span class="sxs-lookup"><span data-stu-id="83edc-114">Select the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="83edc-115">Wählen Sie **Start**.</span><span class="sxs-lookup"><span data-stu-id="83edc-115">Select **Start**.</span></span>  
1.  <span data-ttu-id="83edc-116">Je nachdem, was Sie analysieren möchten, können Sie entweder die Seite neu laden, mit der Seite interagieren oder einfach die Seite ausführen lassen.</span><span class="sxs-lookup"><span data-stu-id="83edc-116">Depending on what you are trying to analyze, you may either reload the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="83edc-117">Wählen Sie die Schaltfläche **Beenden** aus, wenn Sie den Vorgang beendet haben.</span><span class="sxs-lookup"><span data-stu-id="83edc-117">Select the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="83edc-118">Sie können auch die API für die [Konsolen Dienstprogramme][DevtoolsConsoleUtilities] zum Aufzeichnen und Gruppieren von Profilen über die Befehlszeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="83edc-118">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <span data-ttu-id="83edc-119">Sampling-Profil anzeigen</span><span class="sxs-lookup"><span data-stu-id="83edc-119">View Sampling Profile</span></span>  

<span data-ttu-id="83edc-120">Wenn Sie die Aufzeichnung abgeschlossen haben, füllt devtools den **Speicher** Panel automatisch unter **Sampling-profile** mit den Daten aus ihrer Aufzeichnung auf.</span><span class="sxs-lookup"><span data-stu-id="83edc-120">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="83edc-121">Die Standardansicht ist **schwer. \ (Bottom up \)**.</span><span class="sxs-lookup"><span data-stu-id="83edc-121">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="83edc-122">In dieser Ansicht können Sie sehen, welche Funktionen die meisten Auswirkungen auf die Leistung haben, und die Aufruf Pfade für diese Funktionen untersuchen.</span><span class="sxs-lookup"><span data-stu-id="83edc-122">This view enables you to see which functions had the most impact on performance and examine the calling paths to those functions.</span></span>  

### <span data-ttu-id="83edc-123">Ändern der Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="83edc-123">Change sort order</span></span>  

<span data-ttu-id="83edc-124">Wenn Sie die Sortierreihenfolge ändern möchten, wählen Sie das Dropdownmenü neben dem Symbol **Fokus ausgewählte** Funktion \ ( ![ ausgewählte Funktion auswählen ][ImageFocusIcon] \) aus, und wählen Sie dann eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="83edc-124">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function][ImageFocusIcon]\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="83edc-125">**Diagramm**aus.</span><span class="sxs-lookup"><span data-stu-id="83edc-125">**Chart**.</span></span>  <span data-ttu-id="83edc-126">Zeigt ein chronologisches Diagramm der Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="83edc-126">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Flamm Diagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="83edc-128">Flamm Diagramm</span><span class="sxs-lookup"><span data-stu-id="83edc-128">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="83edc-129">**Heavy \ (Bottom up \)**.</span><span class="sxs-lookup"><span data-stu-id="83edc-129">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="83edc-130">Listet Funktionen nach Auswirkungen auf die Leistung auf und ermöglicht Ihnen, die Aufruf Pfade zu den Funktionen zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="83edc-130">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="83edc-131">Dies ist die Standardansicht.</span><span class="sxs-lookup"><span data-stu-id="83edc-131">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Schweres Diagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="83edc-133">Schweres Diagramm</span><span class="sxs-lookup"><span data-stu-id="83edc-133">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="83edc-134">**Struktur \ (oben)**</span><span class="sxs-lookup"><span data-stu-id="83edc-134">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="83edc-135">Zeigt ein Gesamtbild der aufrufenden Struktur, beginnend am oberen Rand der Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="83edc-135">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Strukturdiagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="83edc-137">Strukturdiagramm</span><span class="sxs-lookup"><span data-stu-id="83edc-137">Tree chart</span></span>  
:::image-end:::  

### <span data-ttu-id="83edc-138">Ausschließen von Funktionen</span><span class="sxs-lookup"><span data-stu-id="83edc-138">Exclude functions</span></span>  

<span data-ttu-id="83edc-139">Wenn Sie eine Funktion aus Ihrem Stichproben Profil ausschließen möchten, wählen Sie Sie aus, und wählen Sie dann die Schaltfläche **ausgewählte Funktion ausschließen** \ ( ![ ausgewählte Funktion ausschließen ][ImageExcludeIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="83edc-139">To exclude a function from your Sampling Profile, select it and then select the **exclude selected function** \(![exclude selected function][ImageExcludeIcon]\) button.</span></span>  <span data-ttu-id="83edc-140">Die anfordernde Funktion \ (übergeordnete \) der ausgeschlossenen Funktion \ (untergeordnete \) wird mit dem zugewiesenen Arbeitsspeicher belastet, der der ausgeschlossenen Funktion zugeordnet ist (untergeordnete \).</span><span class="sxs-lookup"><span data-stu-id="83edc-140">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="83edc-141">Wählen Sie die Schaltfläche **alle Funktionen wieder** herstellen \ ( ![ alle Funktionen wiederherstellen ][ImageRestoreIcon] \) aus, um alle ausgeschlossenen Funktionen wieder in die Aufzeichnung zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="83edc-141">Select the **restore all functions** \(![restore all functions][ImageRestoreIcon]\) button to restore all excluded functions back into the recording.</span></span>  

## <span data-ttu-id="83edc-142">Sampling-Profil als Diagramm anzeigen</span><span class="sxs-lookup"><span data-stu-id="83edc-142">View Sampling Profile as Chart</span></span>  

<span data-ttu-id="83edc-143">Die Diagrammansicht bietet eine visuelle Darstellung des Sampling-Profils über einen Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="83edc-143">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="83edc-144">Nachdem Sie [ein Stichproben Profil aufgezeichnet](#record-a-sampling-profile)haben, zeigen Sie die Aufzeichnung als Flammen Diagramm an, indem Sie [die Sortierreihenfolge](#change-sort-order) in **Diagramm**ändern.</span><span class="sxs-lookup"><span data-stu-id="83edc-144">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Ansicht "Flammen Diagramm"" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="83edc-146">Ansicht "Flammen Diagramm"</span><span class="sxs-lookup"><span data-stu-id="83edc-146">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="83edc-147">Das Flammen Diagramm ist in zwei Teile aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="83edc-147">The flame chart is split into two parts.</span></span>  

| <span data-ttu-id="83edc-148">Index</span><span class="sxs-lookup"><span data-stu-id="83edc-148">index</span></span> | <span data-ttu-id="83edc-149">Bestandteil</span><span class="sxs-lookup"><span data-stu-id="83edc-149">Part</span></span> | <span data-ttu-id="83edc-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83edc-150">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="83edc-151">1</span><span class="sxs-lookup"><span data-stu-id="83edc-151">1</span></span> | <span data-ttu-id="83edc-152">Übersicht</span><span class="sxs-lookup"><span data-stu-id="83edc-152">Overview</span></span> | <span data-ttu-id="83edc-153">Eine Vogelperspektive der gesamten Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="83edc-153">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="83edc-154">Die Höhe der Balken entspricht der Tiefe der Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="83edc-154">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="83edc-155">Je höher die Leiste, desto tiefer die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="83edc-155">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="83edc-156">2</span><span class="sxs-lookup"><span data-stu-id="83edc-156">2</span></span> | <span data-ttu-id="83edc-157">Anruflisten</span><span class="sxs-lookup"><span data-stu-id="83edc-157">Call Stacks</span></span> | <span data-ttu-id="83edc-158">Hierbei handelt es sich um eine detaillierte Ansicht der Funktionen, die während der Aufzeichnung aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="83edc-158">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="83edc-159">Die horizontale Achse ist Zeit, und die vertikale Achse ist die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="83edc-159">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="83edc-160">Die Stapel werden oben nach unten angeordnet.</span><span class="sxs-lookup"><span data-stu-id="83edc-160">The stacks are organized top-down.</span></span>  <span data-ttu-id="83edc-161">So nennt sich die Funktion oben die untere und so weiter.</span><span class="sxs-lookup"><span data-stu-id="83edc-161">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="83edc-162">Funktionen werden nach dem Zufallsprinzip eingefärbt.</span><span class="sxs-lookup"><span data-stu-id="83edc-162">Functions are colored randomly.</span></span>  <span data-ttu-id="83edc-163">Es gibt keine Korrelation zu den in den anderen Bereichen verwendeten Farben.</span><span class="sxs-lookup"><span data-stu-id="83edc-163">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="83edc-164">Funktionen werden allerdings immer gleich über Aufrufe eingefärbt, sodass Sie in jeder Laufzeit Muster sehen können.</span><span class="sxs-lookup"><span data-stu-id="83edc-164">However, functions are always colored the same across invocations so that you are able to see patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Flamm Diagramm mit Anmerkungen" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="83edc-166">Flamm Diagramm mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="83edc-166">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="83edc-167">Eine hohe Aufrufliste ist nicht unbedingt wichtig, Sie bedeutet nur, dass viele Funktionen aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="83edc-167">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="83edc-168">Eine breite Leiste bedeutet aber, dass eine Funktion lange Zeit in Anspruch genommen hat.</span><span class="sxs-lookup"><span data-stu-id="83edc-168">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="83edc-169">Diese sind Kandidaten für die Optimierung.</span><span class="sxs-lookup"><span data-stu-id="83edc-169">These are candidates for optimization.</span></span>  

### <span data-ttu-id="83edc-170">Vergrößern bestimmter Teile der Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="83edc-170">Zoom in on specific parts of recording</span></span>  

<span data-ttu-id="83edc-171">Wählen, halten und ziehen Sie die Maus nach links und rechts über die Übersicht, um bestimmte Teile der Anrufliste zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="83edc-171">Select, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="83edc-172">Nachdem Sie die Ansicht gezoomt haben, wird in der Aufrufliste automatisch der Teil der Aufzeichnung angezeigt, den Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="83edc-172">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Diagramm vergrößert" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="83edc-174">Diagramm vergrößert</span><span class="sxs-lookup"><span data-stu-id="83edc-174">Chart zoomed</span></span>  
:::image-end:::  

### <span data-ttu-id="83edc-175">Anzeigen von Funktionsdetails</span><span class="sxs-lookup"><span data-stu-id="83edc-175">View function details</span></span>  

<span data-ttu-id="83edc-176">Wählen Sie eine Funktion aus, um die Definition im **Quellen** Panel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="83edc-176">Select on a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="83edc-177">Zeigen Sie mit der Maus auf eine Funktion, um die Namen-und Anzeigedauer Daten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="83edc-177">Hover over a function to display the name and timing data.</span></span>  <span data-ttu-id="83edc-178">Die folgenden Informationen werden bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="83edc-178">The following information is provided.</span></span>  

| <span data-ttu-id="83edc-179">Detail</span><span class="sxs-lookup"><span data-stu-id="83edc-179">Detail</span></span> | <span data-ttu-id="83edc-180">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83edc-180">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="83edc-181">Name</span><span class="sxs-lookup"><span data-stu-id="83edc-181">Name</span></span>** | <span data-ttu-id="83edc-182">Der Name der Funktion.</span><span class="sxs-lookup"><span data-stu-id="83edc-182">The name of the function.</span></span>  |  
| **<span data-ttu-id="83edc-183">Selbst Größe</span><span class="sxs-lookup"><span data-stu-id="83edc-183">Self size</span></span>** | <span data-ttu-id="83edc-184">Die Größe des aktuellen Aufrufs der Funktion, einschließlich nur der Anweisungen in der Funktion.</span><span class="sxs-lookup"><span data-stu-id="83edc-184">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="83edc-185">Gesamtgröße</span><span class="sxs-lookup"><span data-stu-id="83edc-185">Total size</span></span>** | <span data-ttu-id="83edc-186">Die Größe des aktuellen Aufrufs dieser Funktion und der von ihr aufgerufenen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="83edc-186">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="83edc-187">URL</span><span class="sxs-lookup"><span data-stu-id="83edc-187">URL</span></span>** | <span data-ttu-id="83edc-188">Die Position der Funktionsdefinition in Form von `base.js:261` Where `base.js` ist der Name der Datei, in der die Funktion definiert ist, und `261` die Nummer der Zeile der Definition.</span><span class="sxs-lookup"><span data-stu-id="83edc-188">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Anzeigen von Funktionsdetails in einem Diagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="83edc-190">Anzeigen von Funktionsdetails in einem Diagramm</span><span class="sxs-lookup"><span data-stu-id="83edc-190">View functions details in chart</span></span>  
:::image-end:::  

## <span data-ttu-id="83edc-191">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="83edc-191">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "API-Referenz für Konsolen Dienstprogramme | Microsoft docs"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "Profil-Console Utilities API Reference | Microsoft docs"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd-Console Utilities API Reference | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="83edc-195">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83edc-195">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="83edc-196">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) gefunden und von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) und [Meggin Kearney][MegginKearney] \ (Tech Writer \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="83edc-196">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="83edc-198">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83edc-198">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

---
description: Verwenden Sie die Zuordnungsinstrumentation auf der Zeitachse, um Objekte zu finden, die nicht ordnungsgemäß gesammelt werden, und behalten Sie weiterhin Arbeitsspeicher bei.
title: Verwenden der Zuordnungsinstrumentation auf der Zeitachse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: a02249840256b1e5a2469a253d765eb888527662
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564084"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->
# <a name="how-to-use-allocation-instrumentation-on-timeline"></a><span data-ttu-id="0c9ad-104">Verwenden der Zuordnungsinstrumentation auf der Zeitachse</span><span class="sxs-lookup"><span data-stu-id="0c9ad-104">How to use Allocation instrumentation on Timeline</span></span>  

<span data-ttu-id="0c9ad-105">Verwenden **Sie die Zuordnungsinstrumentation auf der** Zeitachse, um Objekte zu finden, die nicht ordnungsgemäß gesammelt werden, und behalten Sie weiterhin Arbeitsspeicher bei.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-105">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <a name="how-allocation-instrumentation-on-timeline-works"></a><span data-ttu-id="0c9ad-106">Funktionsweise der Zuweisungsinstrumentation auf der Zeitachse</span><span class="sxs-lookup"><span data-stu-id="0c9ad-106">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="0c9ad-107">**Die Zuordnungsinstrumentation auf der Zeitachse** kombiniert die detaillierten Snapshotinformationen des **Heap-Profilers** mit der inkrementellen Aktualisierung und Nachverfolgung des **Leistungsbereichs.**</span><span class="sxs-lookup"><span data-stu-id="0c9ad-107">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="0c9ad-108">Auf ähnliche Weise umfasst das Nachverfolgen der Heapzuweisung für Objekte das Starten einer Aufzeichnung, das Ausführen einer Abfolge von Aktionen und das Beenden der Aufzeichnung für die Analyse.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-108">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="0c9ad-109">**Die Zuordnungsinstrumentation auf der** Zeitachse nimmt in regelmäßigen Abständen Heapmomentaufnahmen während der Aufzeichnung \(so häufig wie alle 50 ms\) und eine letzte Momentaufnahme am Ende der Aufzeichnung auf.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-109">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms\) and one final snapshot at the end of the recording.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Zuordnungsinstrumentation auf der Zeitachse" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **<span data-ttu-id="0c9ad-111">Zuordnungsinstrumentation auf der Zeitachse</span><span class="sxs-lookup"><span data-stu-id="0c9ad-111">Allocation instrumentation on timeline</span></span>**  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="0c9ad-112">Die Zahl nach der ist eine Objekt-ID, die in den mehreren Momentaufnahmen, die während der `@` Aufzeichnungssitzung erstellt wurden, beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="0c9ad-113">Die ID des beständigen Objekts ermöglicht einen genauen Vergleich zwischen Heapzuständen.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-113">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="0c9ad-114">Objekte werden während der Garbage Collections verschoben, sodass das Anzeigen der Adresse eines Objekts keinen Sinn macht.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <a name="enable-allocation-instrumentation-on-timeline"></a><span data-ttu-id="0c9ad-115">Aktivieren der Zuordnungsinstrumentation auf der Zeitachse</span><span class="sxs-lookup"><span data-stu-id="0c9ad-115">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="0c9ad-116">Führen Sie die folgenden Aktionen aus, um mit der Verwendung der **Zuordnungsinstrumentation auf der Zeitachse zu beginnen.**</span><span class="sxs-lookup"><span data-stu-id="0c9ad-116">Complete the following actions to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="0c9ad-117">[Öffnen Sie devTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="0c9ad-117">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="0c9ad-118">Öffnen Sie **den Bereich** Arbeitsspeicher, wählen Sie das **Optionsfeld Zuordnungsinstrumentation auf der Zeitachse** aus.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="0c9ad-119">Start recording (Aufzeichnung starten.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-119">Start recording.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Profiler für Datensatzheapzuordnungen" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       <span data-ttu-id="0c9ad-121">Profiler für Datensatzheapzuordnungen</span><span class="sxs-lookup"><span data-stu-id="0c9ad-121">Record heap allocations profiler</span></span>  
    :::image-end:::  
    
## <a name="read-a-heap-allocation-timeline"></a><span data-ttu-id="0c9ad-122">Lesen einer Zeitachse für die Heapzuweisung</span><span class="sxs-lookup"><span data-stu-id="0c9ad-122">Read a heap allocation timeline</span></span>  

<span data-ttu-id="0c9ad-123">Die Zeitachse für die Heapzuordnung zeigt an, wo Objekte erstellt werden, und identifiziert den Aufbewahrungspfad.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-123">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="0c9ad-124">In der folgenden Abbildung geben die Balken oben an, wann neue Objekte im Heap gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-124">In the following figure, the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="0c9ad-125">Die Höhe der einzelnen Balken entspricht der Größe der zuletzt zugewiesenen Objekte, und die Farbe der Balken gibt an, ob diese Objekte noch in der letzten Heapmomentaufnahme gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-125">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="0c9ad-126">Blaue Balken zeigen Objekte an, die am Ende der Zeitachse noch live sind, graue Balken zeigen Objekte an, die während der Zeitachse zugewiesen wurden, aber seitdem garbage collected wurden.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-126">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Zuordnungsinstrumentation auf Zeitachsenmomentaufnahme" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   <span data-ttu-id="0c9ad-128">**Zuordnungsinstrumentation auf Zeitachsenmomentaufnahme**</span><span class="sxs-lookup"><span data-stu-id="0c9ad-128">**Allocation instrumentation on timeline** snapshot</span></span>  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple choose actions  -->  

<span data-ttu-id="0c9ad-129">Sie können die Schieberegler in der obigen Zeitachse verwenden, um in diese bestimmte Momentaufnahme zu zoomen und die Objekte zu überprüfen, die zu diesem Zeitpunkt kürzlich zugewiesen wurden:</span><span class="sxs-lookup"><span data-stu-id="0c9ad-129">You are able to use the sliders in the timeline above to zoom into that particular snapshot and review the objects that were recently allocated at that point:</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Zoomen in die Momentaufnahme" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   <span data-ttu-id="0c9ad-131">Zoomen in die Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="0c9ad-131">Zoom into snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="0c9ad-132">Wenn Sie ein bestimmtes Objekt im Heap auswählen, wird die Aufbewahrungsstruktur im unteren Teil der Heapmomentaufnahme angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-132">Choosing on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="0c9ad-133">Wenn Sie den Aufbewahrungspfad zum Objekt untersuchen, sollten Sie genügend Informationen erhalten, um zu verstehen, warum das Objekt nicht erfasst wurde, und Sie sollten die erforderlichen Codeänderungen vornehmen, um den unnötigen Verweis zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-133">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <a name="view-memory-allocation-by-function"></a><span data-ttu-id="0c9ad-134">Anzeigen der Speicherzuweisung nach Funktion</span><span class="sxs-lookup"><span data-stu-id="0c9ad-134">View memory allocation by function</span></span>  

<span data-ttu-id="0c9ad-135">Sie können die Speicherzuweisung über die JavaScript-Funktion anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-135">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="0c9ad-136">Weitere Informationen finden Sie unter Untersuchen der [Speicherzuordnung nach Funktion][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span><span class="sxs-lookup"><span data-stu-id="0c9ad-136">For more information, navigate to [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0c9ad-137">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="0c9ad-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Öffnen Microsoft Edge (Chromium) DevTools | Microsoft Docs"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Untersuchen der Speicherzuweisung nach Funktion – Beheben von Speicherproblemen | Microsoft Docs"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Herunterladen eines Microsoft Edge Kanals"  

> [!NOTE]
> <span data-ttu-id="0c9ad-141">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-141">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0c9ad-142">Die ursprüngliche Seite befindet sich [hier und](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) wird von [Meggin Kearney][MegginKearney] \(Technical Writer\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="0c9ad-142">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="0c9ad-144">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0c9ad-144">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  

---
title: Verwenden der Zuordnungs Instrumentation auf der Zeitachse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: d0a7a66a9f061d1a5d98e57269ffbcc0a0afefa4
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985748"
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





# <span data-ttu-id="14b9e-103">Verwenden der Zuordnungs Instrumentation auf der Zeitachse</span><span class="sxs-lookup"><span data-stu-id="14b9e-103">How to use Allocation instrumentation on timeline</span></span>  



<span data-ttu-id="14b9e-104">Verwenden Sie die **Zuweisungs Instrumentation auf der Zeitachse** , um Objekte zu finden, die nicht ordnungsgemäß von der Garbage Collection erfasst werden, und den Speicher weiterhin beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="14b9e-104">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <span data-ttu-id="14b9e-105">Funktionsweise der Zuordnungs Instrumentation auf der Zeitachse</span><span class="sxs-lookup"><span data-stu-id="14b9e-105">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="14b9e-106">Die **Zuweisungs Instrumentation auf Zeitachse** kombiniert die detaillierten Schnappschuss Informationen des **Heap-Profilers** mit der inkrementellen Aktualisierung und Nachverfolgung des **Leistungs** Panels.</span><span class="sxs-lookup"><span data-stu-id="14b9e-106">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="14b9e-107">Ebenso umfasst das Nachverfolgen der Heapzuordnung für Objekte das Starten einer Aufzeichnung, das Durchführen einer Abfolge von Aktionen und das Beenden der Aufzeichnung zur Analyse.</span><span class="sxs-lookup"><span data-stu-id="14b9e-107">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="14b9e-108">Bei der **Zuweisungs Instrumentation auf der Zeitachse** werden Heap-Snapshots in der gesamten Aufzeichnung (so häufig wie alle 50-ms! \) und ein letzter Snapshot am Ende der Aufzeichnung regelmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="14b9e-108">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms!\) and one final snapshot at the end of the recording.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Zuordnungs Instrumentation auf Zeitachse" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **<span data-ttu-id="14b9e-110">Zuordnungs Instrumentation auf Zeitachse</span><span class="sxs-lookup"><span data-stu-id="14b9e-110">Allocation instrumentation on timeline</span></span>**  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="14b9e-111">Die Zahl nach der `@` ist eine Objekt-ID, die über die verschiedenen Snapshots, die während der Aufzeichnungssitzung aufgenommen wurden, beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="14b9e-111">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="14b9e-112">Die persistente Objekt-ID ermöglicht einen präzisen Vergleich zwischen Heap Zuständen.</span><span class="sxs-lookup"><span data-stu-id="14b9e-112">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="14b9e-113">Objekte werden während Garbage Collections verschoben, daher ist es sinnlos, die Adresse eines Objekts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="14b9e-113">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <span data-ttu-id="14b9e-114">Aktivieren der Zuordnungs Instrumentation auf der Zeitachse</span><span class="sxs-lookup"><span data-stu-id="14b9e-114">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="14b9e-115">Führen Sie die folgenden Schritte aus, um die **Zuweisungs Instrumentation auf Zeitachse**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="14b9e-115">Follow these steps to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="14b9e-116">[Öffnen Sie das devtools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="14b9e-116">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="14b9e-117">Öffnen Sie den Bereich " **Speicher** ", und aktivieren Sie das Optionsfeld **Zuweisungs Instrumentation auf Zeitachse** .</span><span class="sxs-lookup"><span data-stu-id="14b9e-117">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="14b9e-118">Start recording (Aufzeichnung starten.</span><span class="sxs-lookup"><span data-stu-id="14b9e-118">Start recording.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Datensatz-Heapzuweisungen Profiler" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       <span data-ttu-id="14b9e-120">Datensatz-Heapzuweisungen Profiler</span><span class="sxs-lookup"><span data-stu-id="14b9e-120">Record heap allocations profiler</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="14b9e-121">Lesen einer Heap Zuordnungs Zeitachse</span><span class="sxs-lookup"><span data-stu-id="14b9e-121">Read a heap allocation timeline</span></span>  

<span data-ttu-id="14b9e-122">Die Zeitachse der Heapzuweisung zeigt an, wo Objekte erstellt werden, und identifiziert den Beibehaltungs Pfad.</span><span class="sxs-lookup"><span data-stu-id="14b9e-122">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="14b9e-123">In der folgenden Abbildung geben die Balken am oberen Rand an, wenn neue Objekte im Heap gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="14b9e-123">In the following figure, the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="14b9e-124">Die Höhe der einzelnen Balken entspricht der Größe der zuletzt zugeordneten Objekte, und die Farbe der Balken gibt an, ob diese Objekte weiterhin im endgültigen Heap-Snapshot enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="14b9e-124">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="14b9e-125">Blaue Balken zeigen Objekte an, die am Ende der Zeitachse weiterhin aktiv sind, und graue Balken zeigen Objekte an, die während der Zeitachse zugewiesen wurden, die aber seither als Garbage Collection erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="14b9e-125">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Zuordnungs Instrumentation auf der Zeitachse-Momentaufnahme" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   <span data-ttu-id="14b9e-127">**Zuordnungs Instrumentation auf der Zeitachse** -Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="14b9e-127">**Allocation instrumentation on timeline** snapshot</span></span>  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

<span data-ttu-id="14b9e-128">Sie können die Schieberegler in der obigen Zeitachse verwenden, um den jeweiligen Schnappschuss zu vergrößern und die Objekte anzuzeigen, die kürzlich zu diesem Zeitpunkt zugewiesen wurden:</span><span class="sxs-lookup"><span data-stu-id="14b9e-128">You are able to use the sliders in the timeline above to zoom into that particular snapshot and see the objects that were recently allocated at that point:</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Vergrößern des Schnappschusses" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   <span data-ttu-id="14b9e-130">Vergrößern des Schnappschusses</span><span class="sxs-lookup"><span data-stu-id="14b9e-130">Zoom into snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="14b9e-131">Wenn Sie auf ein bestimmtes Objekt im Heap klicken, wird im unteren Teil des Heap-Snapshots die Beibehaltungs Struktur angezeigt.</span><span class="sxs-lookup"><span data-stu-id="14b9e-131">Clicking on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="14b9e-132">Wenn Sie den Beibehaltungs Pfad für das Objekt untersuchen, sollten Sie genügend Informationen erhalten, um zu verstehen, warum das Objekt nicht erfasst wurde, und Sie sollten die erforderlichen Codeänderungen vornehmen, um den unnötigen Verweis zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="14b9e-132">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <span data-ttu-id="14b9e-133">Anzeigen der Speicherzuweisung nach Funktion</span><span class="sxs-lookup"><span data-stu-id="14b9e-133">View memory allocation by function</span></span>   

<span data-ttu-id="14b9e-134">Sie können die Speicherzuweisung nach JavaScript-Funktion anzeigen.</span><span class="sxs-lookup"><span data-stu-id="14b9e-134">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="14b9e-135">Weitere Informationen finden Sie unter [untersuchen der Speicherzuweisung nach Funktion][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] .</span><span class="sxs-lookup"><span data-stu-id="14b9e-135">See [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] for more information.</span></span>  

<!--
## Feedback   


-->  

<!-- links -->  

[DevToolsOpenIndex]: ../open.md "Öffnen Sie Microsoft Edge (Chrom) devtools | Microsoft docs"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Untersuchen der Speicherzuweisung nach Funktion – beheben von Speicherproblemen | Microsoft docs"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Herunterladen eines Microsoft Edge-Kanals"  

> [!NOTE]
> <span data-ttu-id="14b9e-139">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14b9e-139">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="14b9e-140">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) gefunden und von [Meggin Kearney][MegginKearney] (Technical Writer \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="14b9e-140">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="14b9e-142">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="14b9e-142">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

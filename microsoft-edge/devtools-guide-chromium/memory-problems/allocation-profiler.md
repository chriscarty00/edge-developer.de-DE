---
description: Use Allocation instrumentation on timeline to find objects that are not being properly garbage collected, and continue to retain memory.
title: How to Use Allocation Instrumentation on Timeline
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: 58a951c4241ae0fe7dce70f523a701694b8254f9
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993506"
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

# <span data-ttu-id="c51e1-104">How to use Allocation instrumentation on Timeline</span><span class="sxs-lookup"><span data-stu-id="c51e1-104">How to use Allocation instrumentation on Timeline</span></span>  

<span data-ttu-id="c51e1-105">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span><span class="sxs-lookup"><span data-stu-id="c51e1-105">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <span data-ttu-id="c51e1-106">How Allocation instrumentation on timeline works</span><span class="sxs-lookup"><span data-stu-id="c51e1-106">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="c51e1-107">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span><span class="sxs-lookup"><span data-stu-id="c51e1-107">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="c51e1-108">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span><span class="sxs-lookup"><span data-stu-id="c51e1-108">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="c51e1-109">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms\) and one final snapshot at the end of the recording.</span><span class="sxs-lookup"><span data-stu-id="c51e1-109">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms\) and one final snapshot at the end of the recording.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Allocation instrumentation on timeline" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **<span data-ttu-id="c51e1-111">Allocation instrumentation on timeline</span><span class="sxs-lookup"><span data-stu-id="c51e1-111">Allocation instrumentation on timeline</span></span>**  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="c51e1-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span><span class="sxs-lookup"><span data-stu-id="c51e1-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="c51e1-113">The persistent object ID enables precise comparison between heap states.</span><span class="sxs-lookup"><span data-stu-id="c51e1-113">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="c51e1-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span><span class="sxs-lookup"><span data-stu-id="c51e1-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <span data-ttu-id="c51e1-115">Enable Allocation Instrumentation on Timeline</span><span class="sxs-lookup"><span data-stu-id="c51e1-115">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="c51e1-116">Complete the following actions to begin using **Allocation instrumentation on timeline**.</span><span class="sxs-lookup"><span data-stu-id="c51e1-116">Complete the following actions to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="c51e1-117">[Open the DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="c51e1-117">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="c51e1-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span><span class="sxs-lookup"><span data-stu-id="c51e1-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="c51e1-119">Start recording.</span><span class="sxs-lookup"><span data-stu-id="c51e1-119">Start recording.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Allocation instrumentation on timeline" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       <span data-ttu-id="c51e1-121">Record heap allocations profiler</span><span class="sxs-lookup"><span data-stu-id="c51e1-121">Record heap allocations profiler</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c51e1-122">Read a heap allocation timeline</span><span class="sxs-lookup"><span data-stu-id="c51e1-122">Read a heap allocation timeline</span></span>  

<span data-ttu-id="c51e1-123">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span><span class="sxs-lookup"><span data-stu-id="c51e1-123">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="c51e1-124">In the following figure, the bars at the top indicate when new objects are found in the heap.</span><span class="sxs-lookup"><span data-stu-id="c51e1-124">In the following figure, the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="c51e1-125">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span><span class="sxs-lookup"><span data-stu-id="c51e1-125">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="c51e1-126">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span><span class="sxs-lookup"><span data-stu-id="c51e1-126">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Allocation instrumentation on timeline" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   <span data-ttu-id="c51e1-128">**Allocation instrumentation on timeline** snapshot</span><span class="sxs-lookup"><span data-stu-id="c51e1-128">**Allocation instrumentation on timeline** snapshot</span></span>  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

<span data-ttu-id="c51e1-129">You are able to use the sliders in the timeline above to zoom into that particular snapshot and see the objects that were recently allocated at that point:</span><span class="sxs-lookup"><span data-stu-id="c51e1-129">You are able to use the sliders in the timeline above to zoom into that particular snapshot and see the objects that were recently allocated at that point:</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Allocation instrumentation on timeline" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   <span data-ttu-id="c51e1-131">Zoom into snapshot</span><span class="sxs-lookup"><span data-stu-id="c51e1-131">Zoom into snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="c51e1-132">Clicking on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span><span class="sxs-lookup"><span data-stu-id="c51e1-132">Clicking on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="c51e1-133">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span><span class="sxs-lookup"><span data-stu-id="c51e1-133">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <span data-ttu-id="c51e1-134">View memory allocation by function</span><span class="sxs-lookup"><span data-stu-id="c51e1-134">View memory allocation by function</span></span>  

<span data-ttu-id="c51e1-135">You are able to view memory allocation by JavaScript function.</span><span class="sxs-lookup"><span data-stu-id="c51e1-135">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="c51e1-136">For more information, see [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span><span class="sxs-lookup"><span data-stu-id="c51e1-136">For more information, see [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span></span>  

## <span data-ttu-id="c51e1-137">Getting in touch with the Microsoft Edge DevTools team</span><span class="sxs-lookup"><span data-stu-id="c51e1-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open.md "Open Microsoft Edge (Chromium) DevTools | Microsoft Docs"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Investigate memory allocation by function - Fix Memory Problems | Microsoft Docs"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Download a Microsoft Edge Channel"  

> [!NOTE]
> <span data-ttu-id="c51e1-141">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c51e1-141">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c51e1-142">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="c51e1-142">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="c51e1-144">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c51e1-144">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

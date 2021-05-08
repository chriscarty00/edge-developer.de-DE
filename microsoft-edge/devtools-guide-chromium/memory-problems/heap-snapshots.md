---
description: Erfahren Sie, wie Sie Heapmomentaufnahmen mit dem Microsoft Edge DevTools-Heap-Profiler aufzeichnen und Speicherlecks finden.
title: Aufzeichnen von Heapmomentaufnahmen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: ce7a6f972bed386f96312808428bd74f1241668f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397804"
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
   limitations under the License.  -->

# <a name="how-to-record-heap-snapshots"></a><span data-ttu-id="175f5-104">Aufzeichnen von Heapmomentaufnahmen</span><span class="sxs-lookup"><span data-stu-id="175f5-104">How to record heap snapshots</span></span>  

<span data-ttu-id="175f5-105">Erfahren Sie, wie Sie Heapmomentaufnahmen mit dem Microsoft Edge DevTools-Heap-Profiler aufzeichnen und Speicherlecks finden.</span><span class="sxs-lookup"><span data-stu-id="175f5-105">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="175f5-106">Der Microsoft Edge DevTools-Heap-Profiler zeigt die Speicherverteilung durch die JavaScript-Objekte und zugehörigen DOM-Knoten Ihrer Seite an.</span><span class="sxs-lookup"><span data-stu-id="175f5-106">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="175f5-107">Verwenden Sie ihn, um JavaScript-Heap-\(JS-Heap\)-Momentaufnahmen zu erstellen, Speicherdiagramme zu analysieren, Momentaufnahmen zu vergleichen und Speicherverluste zu finden.</span><span class="sxs-lookup"><span data-stu-id="175f5-107">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="175f5-108">Navigieren Sie zu [Objekte Aufbewahrungsstruktur][DevtoolsMemoryProblems101ObjectsRetainingTree].</span><span class="sxs-lookup"><span data-stu-id="175f5-108">Navigate to [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <a name="take-a-snapshot"></a><span data-ttu-id="175f5-109">Erstellen einer Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="175f5-109">Take a snapshot</span></span>  

<span data-ttu-id="175f5-110">Wählen Sie **im Bereich** Arbeitsspeicher die Option **Momentaufnahme erstellen**und dann Start **aus.**</span><span class="sxs-lookup"><span data-stu-id="175f5-110">On the **Memory** panel, choose **Take snapshot**, then choose **Start**.</span></span>  <span data-ttu-id="175f5-111">Sie können auch `Ctrl` + `E` \(Windows, Linux\) oder `Cmd` + `E` \(macOS\) auswählen.</span><span class="sxs-lookup"><span data-stu-id="175f5-111">You may also select `Ctrl`+`E` \(Windows, Linux\) or `Cmd`+`E` \(macOS\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Auswählen des Profilerstellungstyps" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   <span data-ttu-id="175f5-113">Auswählen des Profilerstellungstyps</span><span class="sxs-lookup"><span data-stu-id="175f5-113">Choose profiling type</span></span>  
:::image-end:::  

<span data-ttu-id="175f5-114">**Momentaufnahmen** werden zunächst im Rendererprozessspeicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="175f5-114">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="175f5-115">Momentaufnahmen werden bei Bedarf an die DevTools übertragen, wenn Sie das Momentaufnahmesymbol zum Anzeigen auswählen.</span><span class="sxs-lookup"><span data-stu-id="175f5-115">Snapshots are transferred to the DevTools on demand, when you choose on the snapshot icon to view it.</span></span>  

<span data-ttu-id="175f5-116">Nachdem die Momentaufnahme in DevTools geladen und analysiert wurde, wird die Nummer unter dem Snapshottitel angezeigt und zeigt die Gesamtgröße der erreichbaren [JavaScript-Objekte an.][DevtoolsMemoryProblems101ObjectSizes]</span><span class="sxs-lookup"><span data-stu-id="175f5-116">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Gesamtgröße erreichbarer Objekte" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   <span data-ttu-id="175f5-118">Gesamtgröße erreichbarer Objekte</span><span class="sxs-lookup"><span data-stu-id="175f5-118">Total size of reachable objects</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="175f5-119">In Momentaufnahmen sind nur erreichbare Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="175f5-119">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="175f5-120">Außerdem beginnt das Erstellen einer Momentaufnahme immer mit einer Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="175f5-120">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <a name="clear-snapshots"></a><span data-ttu-id="175f5-121">Löschen von Momentaufnahmen</span><span class="sxs-lookup"><span data-stu-id="175f5-121">Clear snapshots</span></span>  

<span data-ttu-id="175f5-122">Wählen **Sie Alle Profile löschen** symbol, um Momentaufnahmen zu entfernen \(sowohl von DevTools als auch von jedem Speicher, der dem Rendererprozess zugeordnet ist\).</span><span class="sxs-lookup"><span data-stu-id="175f5-122">Choose **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Entfernen von Momentaufnahmen" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   <span data-ttu-id="175f5-124">Entfernen von Momentaufnahmen</span><span class="sxs-lookup"><span data-stu-id="175f5-124">Remove snapshots</span></span>  
:::image-end:::  

<span data-ttu-id="175f5-125">Durch das Schließen des DevTools-Fensters werden keine Profile aus dem Speicher gelöscht, der dem Rendererprozess zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="175f5-125">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="175f5-126">Beim erneuten Öffnen von DevTools werden alle zuvor aufgenommenen Momentaufnahmen wieder in der Liste der Momentaufnahmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="175f5-126">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="175f5-127">Probieren Sie dieses Beispiel für [gestreute Objekte aus,][GlitchDevtoolsMemoryExample03] und profilieren Sie es mithilfe des Heap-Profilers.</span><span class="sxs-lookup"><span data-stu-id="175f5-127">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="175f5-128">Eine Reihe von \(object\)-Elementzuordnungen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="175f5-128">A number of \(object\) item allocations are displayed.</span></span>  

## <a name="view-snapshots"></a><span data-ttu-id="175f5-129">Anzeigen von Momentaufnahmen</span><span class="sxs-lookup"><span data-stu-id="175f5-129">View snapshots</span></span>  

<span data-ttu-id="175f5-130">Zeigen Sie Momentaufnahmen aus unterschiedlichen Perspektiven für verschiedene Aufgaben an.</span><span class="sxs-lookup"><span data-stu-id="175f5-130">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="175f5-131">**Die Zusammenfassungsansicht** zeigt Objekte, die nach dem Konstruktornamen zusammengefasst sind.</span><span class="sxs-lookup"><span data-stu-id="175f5-131">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="175f5-132">Verwenden Sie es, um Objekte \(und die Speichernutzung\) basierend auf dem Typ nach Konstruktornamen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="175f5-132">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="175f5-133">Es ist besonders hilfreich, um **DOM-Lecks nachverfolgung zu verfolgen.**</span><span class="sxs-lookup"><span data-stu-id="175f5-133">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="175f5-134">**Vergleichsansicht**.</span><span class="sxs-lookup"><span data-stu-id="175f5-134">**Comparison view**.</span></span>  <span data-ttu-id="175f5-135">Zeigt den Unterschied zwischen zwei Momentaufnahmen an.</span><span class="sxs-lookup"><span data-stu-id="175f5-135">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="175f5-136">Verwenden Sie sie, um zwei \(oder mehr\) Speichermomentaufnahmen vor und nach einem Vorgang zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="175f5-136">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="175f5-137">Wenn Sie das Delta im frei werdenden Speicher und in der Referenzanzahl überprüfen, können Sie das Vorhandensein und die Ursache eines Speicherverlusts bestätigen.</span><span class="sxs-lookup"><span data-stu-id="175f5-137">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="175f5-138">**Containment-Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="175f5-138">**Containment view**.</span></span>  <span data-ttu-id="175f5-139">Ermöglicht die Untersuchung von Heapinhalten.</span><span class="sxs-lookup"><span data-stu-id="175f5-139">Allows exploration of heap contents.</span></span>  <span data-ttu-id="175f5-140">**Die Eindämmungsansicht** bietet eine bessere Ansicht der Objektstruktur und hilft dabei, Objekte zu analysieren, auf die im globalen Namespace \(window\) verwiesen wird, um herauszufinden, was Objekte um sich herum hält.</span><span class="sxs-lookup"><span data-stu-id="175f5-140">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="175f5-141">Verwenden Sie sie, um Verschlüsse zu analysieren und sich auf niedriger Ebene mit Ihren Objekten zu begnnen.</span><span class="sxs-lookup"><span data-stu-id="175f5-141">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="175f5-142">Um zwischen Ansichten zu wechseln, verwenden Sie die Auswahl oben in der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="175f5-142">To switch between views, use the selector at the top of the view.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Auswahl für Switchansichten" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   <span data-ttu-id="175f5-144">Auswahl für Switchansichten</span><span class="sxs-lookup"><span data-stu-id="175f5-144">Switch views selector</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="175f5-145">Nicht alle Eigenschaften werden im JavaScript-Heap gespeichert.</span><span class="sxs-lookup"><span data-stu-id="175f5-145">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="175f5-146">Eigenschaften, die mithilfe von Getters implementiert werden, die systemeigenen Code ausführen, werden nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="175f5-146">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="175f5-147">Außerdem werden werte, die keine Zeichenfolgen sind, z. B. Zahlen, nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="175f5-147">Also, non-string values such as numbers are not captured.</span></span>  

### <a name="summary-view"></a><span data-ttu-id="175f5-148">Zusammenfassungsansicht</span><span class="sxs-lookup"><span data-stu-id="175f5-148">Summary view</span></span>  

<span data-ttu-id="175f5-149">Zunächst wird in der Zusammenfassungsansicht eine Momentaufnahme geöffnet, in der Objektsummen angezeigt werden, die erweitert werden können, um Instanzen zu zeigen:</span><span class="sxs-lookup"><span data-stu-id="175f5-149">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Zusammenfassungsansicht" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   <span data-ttu-id="175f5-151">**Zusammenfassungsansicht**</span><span class="sxs-lookup"><span data-stu-id="175f5-151">**Summary** view</span></span>  
:::image-end:::  

<span data-ttu-id="175f5-152">Einträge auf oberster Ebene sind "Gesamtlinien".</span><span class="sxs-lookup"><span data-stu-id="175f5-152">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="175f5-153">Einträge auf oberster Ebene</span><span class="sxs-lookup"><span data-stu-id="175f5-153">Top-level entries</span></span> | <span data-ttu-id="175f5-154">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="175f5-154">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="175f5-155">Konstruktor</span><span class="sxs-lookup"><span data-stu-id="175f5-155">Constructor</span></span>** | <span data-ttu-id="175f5-156">Stellt alle Objekte dar, die mit diesem Konstruktor erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="175f5-156">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="175f5-157">Entfernung</span><span class="sxs-lookup"><span data-stu-id="175f5-157">Distance</span></span>** | <span data-ttu-id="175f5-158">zeigt den Abstand zum Stamm mithilfe des kürzesten einfachen Pfads von Knoten an.</span><span class="sxs-lookup"><span data-stu-id="175f5-158">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="175f5-159">Flache Größe</span><span class="sxs-lookup"><span data-stu-id="175f5-159">Shallow size</span></span>** | <span data-ttu-id="175f5-160">Zeigt die Summe der flachen Größen aller Objekte an, die von einer bestimmten Konstruktorfunktion erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="175f5-160">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="175f5-161">Die flache Größe ist die Größe des Arbeitsspeichers, der von einem Objekt gehalten wird \(im Allgemeinen haben Arrays und Zeichenfolgen größere flache Größen\).</span><span class="sxs-lookup"><span data-stu-id="175f5-161">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="175f5-162">Navigieren Sie zu [Objektgrößen][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="175f5-162">Navigate to [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="175f5-163">Beibehaltene Größe</span><span class="sxs-lookup"><span data-stu-id="175f5-163">Retained size</span></span>** | <span data-ttu-id="175f5-164">Zeigt die maximale beibehaltene Größe zwischen denselben Objekten an.</span><span class="sxs-lookup"><span data-stu-id="175f5-164">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="175f5-165">Die Größe des Arbeitsspeichers, den Sie frei machen können, nachdem ein Objekt gelöscht wurde \(und die Abhängigen werden nicht mehr erreichbar\) wird als beibehaltene Größe bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="175f5-165">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="175f5-166">Navigieren Sie zu [Objektgrößen][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="175f5-166">Navigate to [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="175f5-167">Nach dem Erweitern einer Gesamtlinie in der oberen Ansicht werden alle Instanzen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="175f5-167">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="175f5-168">Für jede Instanz werden die flachen und beibehaltenen Größen in den entsprechenden Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="175f5-168">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="175f5-169">Die Zahl nach dem Zeichen ist die eindeutige ID des Objekts, sodass Sie Heapmomentaufnahmen auf `@` Objektbasis vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="175f5-169">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="175f5-170">Denken Sie daran, dass gelbe Objekte JavaScript-Verweise und rote Objekte getrennte Knoten sind, auf die von einem mit einem gelben Hintergrund verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="175f5-170">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="175f5-171">Was entsprechen die verschiedenen Konstruktoreinträge \(Group\) im Heap-Profiler?</span><span class="sxs-lookup"><span data-stu-id="175f5-171">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Konstruktorgruppen" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   <span data-ttu-id="175f5-173">**Konstruktorgruppen**</span><span class="sxs-lookup"><span data-stu-id="175f5-173">**Constructor** groups</span></span>  
:::image-end:::  

| <span data-ttu-id="175f5-174">Konstruktor \(Group\)-Eintrag</span><span class="sxs-lookup"><span data-stu-id="175f5-174">Constructor \(group\) entry</span></span> | <span data-ttu-id="175f5-175">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="175f5-175">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="175f5-176">\(global property\)</span><span class="sxs-lookup"><span data-stu-id="175f5-176">\(global property\)</span></span>** | <span data-ttu-id="175f5-177">Die Zwischenobjekte zwischen einem globalen Objekt \(z. B. \) und einem Objekt, auf das `window` verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="175f5-177">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="175f5-178">Wenn ein Objekt mithilfe eines Konstruktors erstellt wird und von einem globalen Objekt gehalten wird, kann der `Person` Aufbewahrungspfad als dargestellt `[global] > \(global property\) > Person` werden.</span><span class="sxs-lookup"><span data-stu-id="175f5-178">If an object is created using a constructor `Person` and is held by a global object, the retaining path may be represented as `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="175f5-179">Dies steht im Gegensatz zur Norm, bei der Objekte direkt aufeinander verweisen.</span><span class="sxs-lookup"><span data-stu-id="175f5-179">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="175f5-180">Zwischenobjekte sind aus Leistungsgründen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="175f5-180">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="175f5-181">Globals werden regelmäßig geändert, und Eigenschaftenzugriffsoptimierungen sind für nicht-globale Objekte nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="175f5-181">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="175f5-182">\(roots\)</span><span class="sxs-lookup"><span data-stu-id="175f5-182">\(roots\)</span></span>** | <span data-ttu-id="175f5-183">Die Stammeinträge in der Aufbewahrungsstrukturansicht sind die Entitäten, die Verweise auf das ausgewählte Objekt haben.</span><span class="sxs-lookup"><span data-stu-id="175f5-183">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="175f5-184">Die Einträge können auch Verweise sein, die vom Modul zu modulspezifischen Zwecken erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="175f5-184">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="175f5-185">Das Modul verfügt über Caches, die auf Objekte verweisen, aber alle diese Verweise sind schwach und verhindern nicht, dass ein Objekt gesammelt wird, da keine wirklich starken Verweise vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="175f5-185">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="175f5-186">\(closure\)</span><span class="sxs-lookup"><span data-stu-id="175f5-186">\(closure\)</span></span>** | <span data-ttu-id="175f5-187">Eine Anzahl von Verweisen auf eine Gruppe von Objekten über Funktionsschließungen.</span><span class="sxs-lookup"><span data-stu-id="175f5-187">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="175f5-188">\(array, string, number, regexp\)</span><span class="sxs-lookup"><span data-stu-id="175f5-188">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="175f5-189">Eine Liste von Objekttypen mit Eigenschaften, die auf ein Array, eine Zeichenfolge, eine Zahl oder einen regulären Ausdruck verweisen.</span><span class="sxs-lookup"><span data-stu-id="175f5-189">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="175f5-190">\(kompilierter Code\)</span><span class="sxs-lookup"><span data-stu-id="175f5-190">\(compiled code\)</span></span>** | <span data-ttu-id="175f5-191">Alles im Zusammenhang mit kompilierten Code.</span><span class="sxs-lookup"><span data-stu-id="175f5-191">Everything related to compiled code.</span></span>  <span data-ttu-id="175f5-192">Skript ähnelt einer Funktion, entspricht jedoch einem `<script>` Textkörper.</span><span class="sxs-lookup"><span data-stu-id="175f5-192">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="175f5-193">SharedFunctionInfos \(SFI\) sind Objekte, die zwischen Funktionen und kompilierten Code stehen.</span><span class="sxs-lookup"><span data-stu-id="175f5-193">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="175f5-194">Funktionen haben in der Regel einen Kontext, sfIs nicht.</span><span class="sxs-lookup"><span data-stu-id="175f5-194">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="175f5-195">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**und so weiter.</span><span class="sxs-lookup"><span data-stu-id="175f5-195">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="175f5-196">Verweise auf Elemente oder Dokumentobjekte eines bestimmten Typs, auf die ihr Code verweist.</span><span class="sxs-lookup"><span data-stu-id="175f5-196">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <a name="comparison-view"></a><span data-ttu-id="175f5-197">Vergleichsansicht</span><span class="sxs-lookup"><span data-stu-id="175f5-197">Comparison view</span></span>  

<span data-ttu-id="175f5-198">Suchen Sie nach undichten Objekten, indem Sie mehrere Momentaufnahmen miteinander vergleichen.</span><span class="sxs-lookup"><span data-stu-id="175f5-198">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="175f5-199">Um zu überprüfen, ob ein bestimmter Anwendungsvorgang keine Lecks \(z. B. ein Paar direkter und umgekehrter Vorgänge, z. B. das Öffnen eines Dokuments und das anschließende Schließen, keine Undichte hinterlassen sollte\), können Sie das folgende Szenario befolgen:</span><span class="sxs-lookup"><span data-stu-id="175f5-199">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="175f5-200">Erstellen Sie eine Heapmomentaufnahme, bevor Sie einen Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="175f5-200">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="175f5-201">Führen Sie einen Vorgang \(interagieren Sie mit einer Seite in einer Weise aus, von der Sie glauben, dass ein Leck verursacht wird\).</span><span class="sxs-lookup"><span data-stu-id="175f5-201">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="175f5-202">Führen Sie einen umgekehrten Vorgang aus \(Führen Sie die entgegengesetzte Interaktion aus, und wiederholen Sie sie ein paar Mal\).</span><span class="sxs-lookup"><span data-stu-id="175f5-202">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="175f5-203">Erstellen Sie einen zweiten Heapsnapshot, und ändern Sie die Ansicht dieser in **Vergleich**, und vergleichen Sie sie mit **Snapshot 1**.</span><span class="sxs-lookup"><span data-stu-id="175f5-203">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  
    
<span data-ttu-id="175f5-204">In der **Vergleichsansicht** wird der Unterschied zwischen zwei Momentaufnahmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="175f5-204">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="175f5-205">Beim Erweitern eines Gesamteintrags werden hinzugefügte und gelöschte Objektinstanzen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="175f5-205">When expanding a total entry, added and deleted object instances are shown.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Vergleichsansicht" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   <span data-ttu-id="175f5-207">**Vergleichsansicht**</span><span class="sxs-lookup"><span data-stu-id="175f5-207">**Comparison** view</span></span>  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <a name="containment-view"></a><span data-ttu-id="175f5-208">Containment-Ansicht</span><span class="sxs-lookup"><span data-stu-id="175f5-208">Containment view</span></span>  

<span data-ttu-id="175f5-209">Die **Containment-Ansicht** ist im Wesentlichen eine "Vogelperspektive" der Objektstruktur Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="175f5-209">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="175f5-210">Es ermöglicht Ihnen, einen Blick in Funktionsschließungen zu werfen, interne Objekte des virtuellen Computers \(VM\) zu beobachten, die ihre JavaScript-Objekte zusammen stellen, und zu verstehen, wie viel Arbeitsspeicher Ihre Anwendung auf sehr niedriger Ebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="175f5-210">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="175f5-211">Einstiegspunkte für die Eindämmungsansicht</span><span class="sxs-lookup"><span data-stu-id="175f5-211">Containment view entry points</span></span> | <span data-ttu-id="175f5-212">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="175f5-212">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="175f5-213">DOMWindow-Objekte</span><span class="sxs-lookup"><span data-stu-id="175f5-213">DOMWindow objects</span></span>** | <span data-ttu-id="175f5-214">Globale Objekte für JavaScript-Code.</span><span class="sxs-lookup"><span data-stu-id="175f5-214">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="175f5-215">GC-Stamm</span><span class="sxs-lookup"><span data-stu-id="175f5-215">GC roots</span></span>** | <span data-ttu-id="175f5-216">Die tatsächlichen GC-Stammwurzeln, die vom Garbage of the VM verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="175f5-216">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="175f5-217">GC-Stammpunkte bestehen aus integrierten Objektzuordnungen, Symboltabellen, VM-Threadstapeln, Kompilierungscaches, Handlebereiche und globalen Handles.</span><span class="sxs-lookup"><span data-stu-id="175f5-217">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="175f5-218">Systemeigene Objekte</span><span class="sxs-lookup"><span data-stu-id="175f5-218">Native objects</span></span>** | <span data-ttu-id="175f5-219">Browserobjekte werden innerhalb des virtuellen JavaScript-Computers \(JavaScript VM\) "pushed", um Automatisierung zu ermöglichen, z. B. DOM-Knoten, CSS-Regeln.</span><span class="sxs-lookup"><span data-stu-id="175f5-219">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Containment-Ansicht" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   <span data-ttu-id="175f5-221">**Containment-Ansicht**</span><span class="sxs-lookup"><span data-stu-id="175f5-221">**Containment** view</span></span>  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="175f5-222">Ein Tipp zu Verschlüssen.</span><span class="sxs-lookup"><span data-stu-id="175f5-222">A tip about closures.</span></span>  <span data-ttu-id="175f5-223">Benennen Sie die Funktionen so, dass Sie problemlos zwischen Verschlüssen in der Momentaufnahme unterscheiden können.</span><span class="sxs-lookup"><span data-stu-id="175f5-223">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="175f5-224">In diesem Beispiel werden beispielsweise keine benannten Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="175f5-224">For example, this example does not use named functions.</span></span>  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function() { // this is NOT a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <span data-ttu-id="175f5-225">Der folgende Codeausschnitt verwendet benannte Funktionen.</span><span class="sxs-lookup"><span data-stu-id="175f5-225">The followingcode snippet uses named functions.</span></span>  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function lC() { // this IS a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <!--  
> :::image type="complex" source="../media/memory-problems-domleaks.msft.png" alt-text="Name functions to distinguish between closures" lightbox="../media/memory-problems-domleaks.msft.png":::
>    Name functions to distinguish between closures  
> :::image-end:::  
> -->  
> 
> > [!NOTE]
> > <span data-ttu-id="175f5-226">Probieren Sie dieses Beispiel [aus, warum `eval` es übl ist,][GlitchDevtoolsMemoryExample07] die Auswirkungen von Sperrungen auf den Speicher zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="175f5-226">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="175f5-227">Sie können auch daran interessiert sein, diesem Beispiel nachzu folgen, das Sie durch die Aufzeichnung von [Heapzuordnungen führt.][GlitchDevtoolsMemoryExample08]</span><span class="sxs-lookup"><span data-stu-id="175f5-227">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <a name="look-up-color-coding"></a><span data-ttu-id="175f5-228">Suchen nach Farbcodierung</span><span class="sxs-lookup"><span data-stu-id="175f5-228">Look up color coding</span></span>  

<span data-ttu-id="175f5-229">Eigenschaften und Eigenschaftswerte von Objekten haben unterschiedliche Typen und werden entsprechend gefärbt.</span><span class="sxs-lookup"><span data-stu-id="175f5-229">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="175f5-230">Jede Eigenschaft hat einen von vier Typen.</span><span class="sxs-lookup"><span data-stu-id="175f5-230">Each property has one of four types.</span></span>  

| <span data-ttu-id="175f5-231">Eigenschaftstyp</span><span class="sxs-lookup"><span data-stu-id="175f5-231">Property Type</span></span> | <span data-ttu-id="175f5-232">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="175f5-232">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="175f5-233">a: property</span><span class="sxs-lookup"><span data-stu-id="175f5-233">a: property</span></span>** | <span data-ttu-id="175f5-234">Eine reguläre Eigenschaft mit einem Namen, auf die über den `.` \(dot\)-Operator zugegriffen wird, oder über `[` `]` \(brackets\)-Notation, z. B. `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="175f5-234">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="175f5-235">0: Element</span><span class="sxs-lookup"><span data-stu-id="175f5-235">0: element</span></span>** | <span data-ttu-id="175f5-236">Eine reguläre Eigenschaft mit einem numerischen Index, auf die über `[` `]` die Notation \(brackets\) zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="175f5-236">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="175f5-237">a: context var</span><span class="sxs-lookup"><span data-stu-id="175f5-237">a: context var</span></span>** |  <span data-ttu-id="175f5-238">Eine Variable in einem Funktionskontext, auf die über den Variablennamen innerhalb einer Funktionsschließung zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="175f5-238">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="175f5-239">a: System-Prop</span><span class="sxs-lookup"><span data-stu-id="175f5-239">a: system prop</span></span>** | <span data-ttu-id="175f5-240">Eine Eigenschaft, die von der JavaScript-VM hinzugefügt wurde und nicht über JavaScript-Code zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="175f5-240">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="175f5-241">Objekte, die `System` nicht über einen entsprechenden JavaScript-Typ verfügen.</span><span class="sxs-lookup"><span data-stu-id="175f5-241">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="175f5-242">Jeder ist Teil der Objektsystemimplementierung der Javascript-VM.</span><span class="sxs-lookup"><span data-stu-id="175f5-242">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="175f5-243">V8 weist die meisten internen Objekte im gleichen Heap wie die JS-Objekte des Benutzers zu.</span><span class="sxs-lookup"><span data-stu-id="175f5-243">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="175f5-244">Dies sind also nur V8-Interne.</span><span class="sxs-lookup"><span data-stu-id="175f5-244">So these are just V8 internals.</span></span>  

## <a name="find-a-specific-object"></a><span data-ttu-id="175f5-245">Suchen eines bestimmten Objekts</span><span class="sxs-lookup"><span data-stu-id="175f5-245">Find a specific object</span></span>  

<span data-ttu-id="175f5-246">Um ein Objekt im gesammelten Heap zu finden, können Sie die Objekt-ID verwenden `Ctrl` + `F` und geben.</span><span class="sxs-lookup"><span data-stu-id="175f5-246">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <a name="uncover-dom-leaks"></a><span data-ttu-id="175f5-247">Aufdecken von DOM-Lecks</span><span class="sxs-lookup"><span data-stu-id="175f5-247">Uncover DOM leaks</span></span>  

<span data-ttu-id="175f5-248">Der Heapprofiler kann bidirektionale Abhängigkeiten zwischen browsereigenen Objekten \(DOM-Knoten, CSS-Regeln\) und JavaScript-Objekten widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="175f5-248">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="175f5-249">Dies hilft, ansonsten unsichtbare Lecks zu erkennen, die aufgrund vergessener getrennter DOM-Unterstrukturen passieren, die herumschlaufen.</span><span class="sxs-lookup"><span data-stu-id="175f5-249">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="175f5-250">DOM-Lecks können größer sein, als Sie denken.</span><span class="sxs-lookup"><span data-stu-id="175f5-250">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="175f5-251">Ziehen Sie das folgende Beispiel in Betracht.</span><span class="sxs-lookup"><span data-stu-id="175f5-251">Consider the following sample.</span></span>  <span data-ttu-id="175f5-252">Wann ist die #tree GC?</span><span class="sxs-lookup"><span data-stu-id="175f5-252">When is the #tree GC?</span></span>  

```javascript
var select = document.querySelector;
var treeRef = select("#tree");
var leafRef = select("#leaf");
var body = select("body");
body.removeChild(treeRef);
//#tree in not GC yet due to treeRef
treeRef = null;
//#tree is not GC yet due to indirect
//reference from leafRef
leafRef = null;
//#NOW able to be #tree GC
```  

<span data-ttu-id="175f5-253">Der behält einen Verweis auf das relevante übergeordnete Objekt \(parentNode\) bei und rekursiv bis , also nur, wenn leafRef nullifiziert wird, ist die GESAMTE Struktur unter einem Kandidaten für `#leaf` `#tree` `#tree` GC.</span><span class="sxs-lookup"><span data-stu-id="175f5-253">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="DOM-Unterstrukturen" lightbox="../media/memory-problems-tree-gc.msft.png":::
   <span data-ttu-id="175f5-255">DOM-Unterstrukturen</span><span class="sxs-lookup"><span data-stu-id="175f5-255">DOM subtrees</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="175f5-256">Beispiele: Probieren Sie dieses Beispiel für einen nicht mehr vorhandenen [DOM-Knoten][GlitchDevtoolsMemoryExample06] aus, um zu verstehen, wo und wie sie erkannt werden können.</span><span class="sxs-lookup"><span data-stu-id="175f5-256">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="175f5-257">Sie können sich auch dieses Beispiel dafür anschauen, dass [DOM-Lecks größer als erwartet sind.][GlitchDevtoolsMemoryExample09]</span><span class="sxs-lookup"><span data-stu-id="175f5-257">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="175f5-258">Weitere Informationen zu DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span><span class="sxs-lookup"><span data-stu-id="175f5-258">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="175f5-259">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="175f5-259">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Objektgrößen – Speicherterminologie | Microsoft Docs"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Struktur der Aufbewahrung von Objekten – Speicherterminologie | Microsoft Docs"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html - Microsoft Edge (Chromium) DevTools | Glitch"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "Speicher | Folien"  

> [!NOTE]
> <span data-ttu-id="175f5-269">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="175f5-269">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="175f5-270">Die ursprüngliche Seite befindet sich [hier und](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) wird von [Meggin Kearney][MegginKearney] \(Technical Writer\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="175f5-270">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="175f5-272">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="175f5-272">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

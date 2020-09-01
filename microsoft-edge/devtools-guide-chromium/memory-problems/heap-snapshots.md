---
title: Aufzeichnen von Heap-Snapshots
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: bd46489d8a8a3fddbff60618b4997784294cccff
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985439"
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





# <span data-ttu-id="9926f-103">Aufzeichnen von Heap-Snapshots</span><span class="sxs-lookup"><span data-stu-id="9926f-103">How to record heap snapshots</span></span>   



<span data-ttu-id="9926f-104">Erfahren Sie, wie Sie Heap-Snapshots mit dem Microsoft Edge devtools-Heap Profiler aufzeichnen und Speicherverluste finden.</span><span class="sxs-lookup"><span data-stu-id="9926f-104">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="9926f-105">Der Microsoft Edge devtools-Heap Profiler zeigt die Speicherverteilung nach den JavaScript-Objekten und den zugehörigen DOM-Knoten Ihrer Seite an.</span><span class="sxs-lookup"><span data-stu-id="9926f-105">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="9926f-106">Verwenden Sie es, um Snapshots des JavaScript-Heaps zu erstellen, Speicher Diagramme zu analysieren, Schnappschüsse zu vergleichen und Speicherverluste zu finden.</span><span class="sxs-lookup"><span data-stu-id="9926f-106">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="9926f-107">Siehe auch Objekte, die die [Struktur beibehalten][DevtoolsMemoryProblems101ObjectsRetainingTree].</span><span class="sxs-lookup"><span data-stu-id="9926f-107">See also [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <span data-ttu-id="9926f-108">Erstellen einer Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="9926f-108">Take a snapshot</span></span>  

<span data-ttu-id="9926f-109">Wählen Sie im **Speicher** Panel **Schnappschuss aufnehmen**und dann auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="9926f-109">On the **Memory** panel, choose **Take snapshot**, then click **Start**.</span></span>  <span data-ttu-id="9926f-110">Sie können auch `Ctrl` + `E` \ (Windows \) oder `Cmd` + `E` \ (macOS \) drücken.</span><span class="sxs-lookup"><span data-stu-id="9926f-110">You may also press `Ctrl`+`E` \(Windows\) or `Cmd`+`E` \(macOS\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Auswählen des Profil Erstellungs Typs" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   <span data-ttu-id="9926f-112">Auswählen des Profil Erstellungs Typs</span><span class="sxs-lookup"><span data-stu-id="9926f-112">Select profiling type</span></span>  
:::image-end:::  

<span data-ttu-id="9926f-113">**Snapshots** werden zunächst im Speicher des Renderer-Prozesses gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9926f-113">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="9926f-114">Schnappschüsse werden bei Bedarf an devtools übertragen, wenn Sie auf das Schnappschuss Symbol klicken, um es anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9926f-114">Snapshots are transferred to the DevTools on demand, when you click on the snapshot icon to view it.</span></span>  

<span data-ttu-id="9926f-115">Nachdem der Schnappschuss in devtools geladen und analysiert wurde, wird die Zahl unterhalb des Snapshot-Titels angezeigt und zeigt die [Gesamtgröße der erreichbaren JavaScript-Objekte an][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="9926f-115">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Gesamtgröße der erreichbaren Objekte" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   <span data-ttu-id="9926f-117">Gesamtgröße der erreichbaren Objekte</span><span class="sxs-lookup"><span data-stu-id="9926f-117">Total size of reachable objects</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9926f-118">In Schnappschüssen sind nur erreichbare Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="9926f-118">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="9926f-119">Außerdem beginnt das Erstellen eines Snapshots immer mit einer Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="9926f-119">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <span data-ttu-id="9926f-120">Löschen von Schnappschüssen</span><span class="sxs-lookup"><span data-stu-id="9926f-120">Clear snapshots</span></span>  

<span data-ttu-id="9926f-121">Klicken Sie auf Symbol " **alle Profile löschen** ", um Schnappschüsse zu entfernen \ (sowohl aus devtools als auch aus dem Speicher, der dem Renderer-Prozess zugeordnet ist).</span><span class="sxs-lookup"><span data-stu-id="9926f-121">Click **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Entfernen von Schnappschüssen" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   <span data-ttu-id="9926f-123">Entfernen von Schnappschüssen</span><span class="sxs-lookup"><span data-stu-id="9926f-123">Remove snapshots</span></span>  
:::image-end:::  

<span data-ttu-id="9926f-124">Beim Schließen des devtools-Fensters werden keine Profile aus dem Speicher gelöscht, der dem Renderer-Prozess zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9926f-124">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="9926f-125">Beim erneuten Öffnen von devtools werden alle zuvor aufgenommenen Schnappschüsse wieder in der Liste der Schnappschüsse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9926f-125">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="9926f-126">Probieren Sie dieses Beispiel für [verstreute Objekte][GlitchDevtoolsMemoryExample03] aus, und erstellen Sie ein Profil mit dem Heap Profiler.</span><span class="sxs-lookup"><span data-stu-id="9926f-126">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="9926f-127">Es sollte eine Anzahl von \ (Object \)-Element Zuweisungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9926f-127">You should see a number of \(object\) item allocations.</span></span>  

## <span data-ttu-id="9926f-128">Anzeigen von Schnappschüssen</span><span class="sxs-lookup"><span data-stu-id="9926f-128">View snapshots</span></span>  

<span data-ttu-id="9926f-129">Sie können Schnappschüsse aus unterschiedlichen Perspektiven für verschiedene Aufgaben anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9926f-129">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="9926f-130">**Zusammenfassungsansicht** zeigt Objekte, die nach dem Namen des Konstruktors gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="9926f-130">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="9926f-131">Verwenden Sie es, um Objekte \ (und die Speichernutzung \) basierend auf dem Typ nach konstruktornamen gruppiert zu jagen.</span><span class="sxs-lookup"><span data-stu-id="9926f-131">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="9926f-132">Dies ist besonders hilfreich für das **Aufspüren von Dom-Lecks**.</span><span class="sxs-lookup"><span data-stu-id="9926f-132">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="9926f-133">**Vergleichsansicht**.</span><span class="sxs-lookup"><span data-stu-id="9926f-133">**Comparison view**.</span></span>  <span data-ttu-id="9926f-134">Zeigt den Unterschied zwischen zwei Schnappschüssen an.</span><span class="sxs-lookup"><span data-stu-id="9926f-134">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="9926f-135">Verwenden Sie diese Funktion, um zwei \ (oder mehr \) Speicher-Snapshots von vor und nach einem Vorgang zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="9926f-135">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="9926f-136">Wenn Sie das Delta in freiem Arbeitsspeicher und Verweisanzahl prüfen, können Sie das vorhanden sein und die Ursache für einen Speicherverlust bestätigen.</span><span class="sxs-lookup"><span data-stu-id="9926f-136">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="9926f-137">**Einkapselungs Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="9926f-137">**Containment view**.</span></span>  <span data-ttu-id="9926f-138">Ermöglicht das Erforschen von Heap Inhalten.</span><span class="sxs-lookup"><span data-stu-id="9926f-138">Allows exploration of heap contents.</span></span>  <span data-ttu-id="9926f-139">Die **Einkapselungs Ansicht** bietet eine bessere Sicht auf die Objektstruktur und hilft, Objekte zu analysieren, auf die im globalen Namespace \ (Window \) verwiesen wird, um herauszufinden, welche Objekte in der Nähe sind.</span><span class="sxs-lookup"><span data-stu-id="9926f-139">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="9926f-140">Verwenden Sie es, um Verschlüsse zu analysieren und in Ihre Objekte auf einem niedrigeren Niveau zu tauchen.</span><span class="sxs-lookup"><span data-stu-id="9926f-140">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="9926f-141">Um zwischen den Ansichten zu wechseln, verwenden Sie die Auswahl oben in der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="9926f-141">To switch between views, use the selector at the top of the view.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Wechseln der Ansicht-Auswahl" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   <span data-ttu-id="9926f-143">Wechseln der Ansicht-Auswahl</span><span class="sxs-lookup"><span data-stu-id="9926f-143">Switch views selector</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9926f-144">Nicht alle Eigenschaften werden auf dem JavaScript-Heap gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9926f-144">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="9926f-145">Mit Gettern implementierte Eigenschaften, die systemeigenen Code ausführen, werden nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="9926f-145">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="9926f-146">Auch nicht-Zeichenfolgenwerte wie Zahlen werden nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="9926f-146">Also, non-string values such as numbers are not captured.</span></span>  

### <span data-ttu-id="9926f-147">Zusammenfassungsansicht</span><span class="sxs-lookup"><span data-stu-id="9926f-147">Summary view</span></span>  

<span data-ttu-id="9926f-148">Zunächst wird in der Zusammenfassungsansicht eine Momentaufnahme geöffnet, in der die Objektergebnisse angezeigt werden, die möglicherweise erweitert werden, um Instanzen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="9926f-148">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Zusammenfassungsansicht" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   <span data-ttu-id="9926f-150">Zusammenfassungsansicht</span><span class="sxs-lookup"><span data-stu-id="9926f-150">Summary view</span></span>  
:::image-end:::  

<span data-ttu-id="9926f-151">Einträge auf oberster Ebene sind "Total"-Zeilen.</span><span class="sxs-lookup"><span data-stu-id="9926f-151">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="9926f-152">Einträge auf oberster Ebene</span><span class="sxs-lookup"><span data-stu-id="9926f-152">Top-level entries</span></span> | <span data-ttu-id="9926f-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9926f-153">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="9926f-154">Konstruktor</span><span class="sxs-lookup"><span data-stu-id="9926f-154">Constructor</span></span>** | <span data-ttu-id="9926f-155">Stellt alle mit diesem Konstruktor erstellten Objekte dar.</span><span class="sxs-lookup"><span data-stu-id="9926f-155">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="9926f-156">Entfernung</span><span class="sxs-lookup"><span data-stu-id="9926f-156">Distance</span></span>** | <span data-ttu-id="9926f-157">zeigt den Abstand zum Stamm mithilfe des kürzesten einfachen Pfads von Knoten an.</span><span class="sxs-lookup"><span data-stu-id="9926f-157">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="9926f-158">Flache Größe</span><span class="sxs-lookup"><span data-stu-id="9926f-158">Shallow size</span></span>** | <span data-ttu-id="9926f-159">Zeigt die Summe der flachen Größen aller Objekte an, die von einer bestimmten Konstruktorfunktion erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9926f-159">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="9926f-160">Die flache Größe ist die Größe des Speichers, der für ein Objekt reserviert ist \ (im allgemeinen weisen Arrays und Zeichenfolgen größere flache Größen auf \).</span><span class="sxs-lookup"><span data-stu-id="9926f-160">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="9926f-161">Siehe auch [Objektgrößen][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="9926f-161">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="9926f-162">Beibehaltungs Größe</span><span class="sxs-lookup"><span data-stu-id="9926f-162">Retained size</span></span>** | <span data-ttu-id="9926f-163">Zeigt die maximale Beibehaltungs Größe für den gleichen Satz von Objekten an.</span><span class="sxs-lookup"><span data-stu-id="9926f-163">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="9926f-164">Die Größe des Arbeitsspeichers, der nach dem Löschen eines Objekts freigegeben werden kann \ (und die abhängigen Personen sind nicht mehr erreichbar \) wird als Beibehaltungs Größe bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9926f-164">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="9926f-165">Siehe auch [Objektgrößen][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="9926f-165">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="9926f-166">Nachdem Sie eine Gesamtzeile in der oberen Ansicht erweitert haben, werden alle Instanzen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9926f-166">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="9926f-167">Für jede Instanz werden die flachen und gespeicherten Größen in den entsprechenden Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9926f-167">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="9926f-168">Die Zahl hinter dem `@` Zeichen ist die eindeutige ID des Objekts, die es Ihnen ermöglicht, Heap-Schnappschüsse pro Objekt zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="9926f-168">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="9926f-169">Beachten Sie, dass gelbe Objekte JavaScript-Bezüge aufweisen und rote Objekte getrennte Knoten sind, auf die von einer mit einem gelben Hintergrund verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9926f-169">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="9926f-170">Was entsprechen die verschiedenen Konstruktoren \ (Group \)-Einträge im Heap Profiler?</span><span class="sxs-lookup"><span data-stu-id="9926f-170">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Konstruktorgruppen" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   <span data-ttu-id="9926f-172">Konstruktorgruppen</span><span class="sxs-lookup"><span data-stu-id="9926f-172">Constructor groups</span></span>  
:::image-end:::  

| <span data-ttu-id="9926f-173">Konstruktor \ (Gruppe \) Eintrag</span><span class="sxs-lookup"><span data-stu-id="9926f-173">Constructor \(group\) entry</span></span> | <span data-ttu-id="9926f-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9926f-174">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="9926f-175">\ (globale Eigenschaft \)</span><span class="sxs-lookup"><span data-stu-id="9926f-175">\(global property\)</span></span>** | <span data-ttu-id="9926f-176">Die zwischen Objekte zwischen einem globalen Objekt \ (wie `window` \) und einem Objekt, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9926f-176">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="9926f-177">Wenn ein Objekt mit einem Konstruktor erstellt `Person` und von einem globalen Objekt gehalten wird, sieht der Beibehaltungs Pfad wie folgt aus `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="9926f-177">If an object is created using a constructor `Person` and is held by a global object, the retaining path would look like `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="9926f-178">Dies steht im Gegensatz zur Norm, bei der sich Objekte direkt gegenseitig referenzieren.</span><span class="sxs-lookup"><span data-stu-id="9926f-178">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="9926f-179">Zwischen Objekte bestehen aus Leistungsgründen.</span><span class="sxs-lookup"><span data-stu-id="9926f-179">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="9926f-180">Globals werden regelmäßig geändert, und Eigenschaftenzugriffs Optimierungen erledigen eine gute Aufgabe für nicht-globale Objekte, die nicht für Globals gelten.</span><span class="sxs-lookup"><span data-stu-id="9926f-180">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="9926f-181">\ (Roots \)</span><span class="sxs-lookup"><span data-stu-id="9926f-181">\(roots\)</span></span>** | <span data-ttu-id="9926f-182">Die Stamm Einträge in der Beibehaltungs Strukturansicht sind die Entitäten, die auf das ausgewählte Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="9926f-182">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="9926f-183">Die Einträge können auch Verweise sein, die vom Modul für modulspezifische Zwecke erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9926f-183">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="9926f-184">Das Modul hat Zwischenspeicher, die auf Objekte verweisen, aber alle derartigen Bezüge sind schwach und verhindern nicht, dass ein Objekt gesammelt wird, da es keine wirklich starken Bezüge gibt.</span><span class="sxs-lookup"><span data-stu-id="9926f-184">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="9926f-185">\ (Closure \)</span><span class="sxs-lookup"><span data-stu-id="9926f-185">\(closure\)</span></span>** | <span data-ttu-id="9926f-186">Die Anzahl von Verweisen auf eine Gruppe von Objekten über Funktions Closures.</span><span class="sxs-lookup"><span data-stu-id="9926f-186">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="9926f-187">\ (Array, Zeichenfolge, Zahl, regexp \)</span><span class="sxs-lookup"><span data-stu-id="9926f-187">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="9926f-188">Eine Liste von Objekttypen mit Eigenschaften, die auf ein Array, eine Zeichenfolge, eine Zahl oder einen regulären Ausdruck verweisen.</span><span class="sxs-lookup"><span data-stu-id="9926f-188">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="9926f-189">\ (kompilierter Code \)</span><span class="sxs-lookup"><span data-stu-id="9926f-189">\(compiled code\)</span></span>** | <span data-ttu-id="9926f-190">Alles im Zusammenhang mit kompiliertem Code.</span><span class="sxs-lookup"><span data-stu-id="9926f-190">Everything related to compiled code.</span></span>  <span data-ttu-id="9926f-191">Das Skript ähnelt einer Funktion, entspricht aber einem `<script>` Textkörper.</span><span class="sxs-lookup"><span data-stu-id="9926f-191">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="9926f-192">SharedFunctionInfos \ (SFI \) sind Objekte, die zwischen Funktionen und kompiliertem Code stehen.</span><span class="sxs-lookup"><span data-stu-id="9926f-192">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="9926f-193">Funktionen haben in der Regel einen Kontext, während SFIs nicht.</span><span class="sxs-lookup"><span data-stu-id="9926f-193">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="9926f-194">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**usw.</span><span class="sxs-lookup"><span data-stu-id="9926f-194">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="9926f-195">Verweise auf Elemente oder Dokument Objekte eines bestimmten Typs, auf die der Code verweist.</span><span class="sxs-lookup"><span data-stu-id="9926f-195">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <span data-ttu-id="9926f-196">Vergleichsansicht</span><span class="sxs-lookup"><span data-stu-id="9926f-196">Comparison view</span></span>  

<span data-ttu-id="9926f-197">Suchen Sie durchgesickerte Objekte, indem Sie mehrere Schnappschüsse miteinander vergleichen.</span><span class="sxs-lookup"><span data-stu-id="9926f-197">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="9926f-198">Wenn Sie sicherstellen möchten, dass ein bestimmter Anwendungsvorgang keine Undichtigkeiten verursacht \ (beispielsweise in der Regel ein paar von direkten und umgekehrten Vorgängen, wie das Öffnen eines Dokuments und das anschließende Schließen des Dokuments), sollten Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="9926f-198">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="9926f-199">Erstellen Sie einen Heap-Snapshot, bevor Sie einen Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="9926f-199">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="9926f-200">Durchführen eines Vorgangs \ (Interaktion mit einer Seite auf eine Art und Weise, von der Sie glauben, dass Sie ein Leck verursacht).</span><span class="sxs-lookup"><span data-stu-id="9926f-200">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="9926f-201">Durchführen eines umgekehrten Vorgangs \ (die entgegengesetzte Interaktion ausführen und einige Male wiederholen \).</span><span class="sxs-lookup"><span data-stu-id="9926f-201">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="9926f-202">Nehmen Sie einen zweiten Heap-Snapshot auf, und ändern Sie die Ansicht dieser Person in einen **Vergleich**, und vergleichen Sie Sie mit **Snapshot 1**.</span><span class="sxs-lookup"><span data-stu-id="9926f-202">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  
    
<span data-ttu-id="9926f-203">In der **Vergleichs** Ansicht wird der Unterschied zwischen zwei Schnappschüssen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9926f-203">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="9926f-204">Wenn Sie einen Gesamteintrag erweitern, werden hinzugefügte und gelöschte Objektinstanzen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9926f-204">When expanding a total entry, added and deleted object instances are shown.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Vergleichsansicht" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   <span data-ttu-id="9926f-206">**Vergleichs** Ansicht</span><span class="sxs-lookup"><span data-stu-id="9926f-206">**Comparison** view</span></span>  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <span data-ttu-id="9926f-207">Einkapselungs Ansicht</span><span class="sxs-lookup"><span data-stu-id="9926f-207">Containment view</span></span>  

<span data-ttu-id="9926f-208">Die **Einkapselungs** Ansicht ist im Grunde eine "Vogelperspektive" der Objektstruktur Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9926f-208">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="9926f-209">Sie ermöglicht es Ihnen, in Funktions Verschlüssen zu spähen, die virtuellen computerinternen Objekte zu beobachten, die zusammen Ihre JavaScript-Objekte bilden, und zu verstehen, wie viel Arbeitsspeicher Ihre Anwendung auf einem sehr geringen Niveau verwendet.</span><span class="sxs-lookup"><span data-stu-id="9926f-209">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="9926f-210">Einstiegspunkte für die Eindämmungs Ansicht</span><span class="sxs-lookup"><span data-stu-id="9926f-210">Containment view entry points</span></span> | <span data-ttu-id="9926f-211">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9926f-211">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="9926f-212">DOMWindow-Objekte</span><span class="sxs-lookup"><span data-stu-id="9926f-212">DOMWindow objects</span></span>** | <span data-ttu-id="9926f-213">Globale Objekte für JavaScript-Code.</span><span class="sxs-lookup"><span data-stu-id="9926f-213">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="9926f-214">GC-Stämme</span><span class="sxs-lookup"><span data-stu-id="9926f-214">GC roots</span></span>** | <span data-ttu-id="9926f-215">Die tatsächlichen GC-Stämme, die vom Garbage des virtuellen Computers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9926f-215">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="9926f-216">GC-Stämme umfassen integrierte Objektzuordnungen, Symboltabellen, VM-Threadstapel, Kompilierungs Caches, handlebereiche und globale Handles.</span><span class="sxs-lookup"><span data-stu-id="9926f-216">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="9926f-217">Systemeigene Objekte</span><span class="sxs-lookup"><span data-stu-id="9926f-217">Native objects</span></span>** | <span data-ttu-id="9926f-218">Browser Objekte werden innerhalb des virtuellen JavaScript-Computers "geschoben" \ (JavaScript VM \), um die Automatisierung zu ermöglichen, beispielsweise DOM-Knoten, CSS-Regeln.</span><span class="sxs-lookup"><span data-stu-id="9926f-218">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Einkapselungs Ansicht" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   <span data-ttu-id="9926f-220">**Einkapselungs** Ansicht</span><span class="sxs-lookup"><span data-stu-id="9926f-220">**Containment** view</span></span>  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="9926f-221">Ein Tipp zu Closures.</span><span class="sxs-lookup"><span data-stu-id="9926f-221">A tip about closures.</span></span>  <span data-ttu-id="9926f-222">Benennen Sie die Funktionen, damit Sie problemlos zwischen den Closures im Schnappschuss unterscheiden können.</span><span class="sxs-lookup"><span data-stu-id="9926f-222">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="9926f-223">In diesem Beispiel werden beispielsweise keine benannten Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9926f-223">For example, this example does not use named functions.</span></span>  
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
> <span data-ttu-id="9926f-224">Das followingcode-Snippet verwendet benannte Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9926f-224">The followingcode snippet uses named functions.</span></span>  
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
> > <span data-ttu-id="9926f-225">Probieren Sie dieses Beispiel aus, [warum das `eval` böse ist][GlitchDevtoolsMemoryExample07] , um die Auswirkungen von Closures auf den Arbeitsspeicher zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="9926f-225">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="9926f-226">Möglicherweise sind Sie auch daran interessiert, es mit diesem Beispiel zu befolgen, das Sie durch das Aufzeichnen von [Heapzuweisungen][GlitchDevtoolsMemoryExample08]führt.</span><span class="sxs-lookup"><span data-stu-id="9926f-226">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <span data-ttu-id="9926f-227">Nachschlagen der Farbcodierung</span><span class="sxs-lookup"><span data-stu-id="9926f-227">Look up color coding</span></span>  

<span data-ttu-id="9926f-228">Eigenschaften und Eigenschaftswerte von Objekten haben unterschiedliche Typen und werden entsprechend eingefärbt.</span><span class="sxs-lookup"><span data-stu-id="9926f-228">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="9926f-229">Jede Eigenschaft hat einen von vier Typen.</span><span class="sxs-lookup"><span data-stu-id="9926f-229">Each property has one of four types.</span></span>  

| <span data-ttu-id="9926f-230">Eigenschaftstyp</span><span class="sxs-lookup"><span data-stu-id="9926f-230">Property Type</span></span> | <span data-ttu-id="9926f-231">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9926f-231">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="9926f-232">a: Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9926f-232">a: property</span></span>** | <span data-ttu-id="9926f-233">Eine reguläre Eigenschaft mit einem Namen, auf den über den `.` \ (dot \)-Operator zugegriffen wird, `[` `]` beispielsweise über die Notation \ (Brackets \) `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="9926f-233">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="9926f-234">0: Element</span><span class="sxs-lookup"><span data-stu-id="9926f-234">0: element</span></span>** | <span data-ttu-id="9926f-235">Eine reguläre Eigenschaft mit einem numerischen Index, auf die über `[` `]` \ (eckige Klammern \)-Notation zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="9926f-235">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="9926f-236">a: Kontext var</span><span class="sxs-lookup"><span data-stu-id="9926f-236">a: context var</span></span>** |  <span data-ttu-id="9926f-237">Eine Variable in einem Funktionskontext, auf die über den Variablennamen in einem Funktions Abschluss zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="9926f-237">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="9926f-238">a: System Prop</span><span class="sxs-lookup"><span data-stu-id="9926f-238">a: system prop</span></span>** | <span data-ttu-id="9926f-239">Eine von der JavaScript-VM hinzugefügte Eigenschaft, auf die über JavaScript-Code nicht zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="9926f-239">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="9926f-240">Objekte, `System` die als kein entsprechender JavaScript-Typ gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="9926f-240">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="9926f-241">Jede ist Teil der Objekt Systemimplementierung der JavaScript-VM.</span><span class="sxs-lookup"><span data-stu-id="9926f-241">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="9926f-242">V8 ordnet die meisten internen Objekte im gleichen Heap wie die JS-Objekte des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="9926f-242">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="9926f-243">Das sind also nur V8-Interna.</span><span class="sxs-lookup"><span data-stu-id="9926f-243">So these are just V8 internals.</span></span>  

## <span data-ttu-id="9926f-244">Suchen nach einem bestimmten Objekt</span><span class="sxs-lookup"><span data-stu-id="9926f-244">Find a specific object</span></span>  

<span data-ttu-id="9926f-245">Wenn Sie ein Objekt im gesammelten Heap suchen möchten, können Sie `Ctrl` + `F` die Objekt-ID verwenden und angeben.</span><span class="sxs-lookup"><span data-stu-id="9926f-245">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <span data-ttu-id="9926f-246">Aufdecken von Dom-Lecks</span><span class="sxs-lookup"><span data-stu-id="9926f-246">Uncover DOM leaks</span></span>  

<span data-ttu-id="9926f-247">Der Heap-Profiler hat die Möglichkeit, bidirektionale Abhängigkeiten zwischen Browser systemeigenen Objekten \ (DOM-Knoten, CSS-Regeln \) und JavaScript-Objekten wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="9926f-247">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="9926f-248">Dies hilft bei der Ermittlung von ansonsten unsichtbaren Lecks, die durch vergessene, freigegebene Dom-unter Bäume entstehen.</span><span class="sxs-lookup"><span data-stu-id="9926f-248">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="9926f-249">Dom-Lecks können größer sein, als Sie denken.</span><span class="sxs-lookup"><span data-stu-id="9926f-249">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="9926f-250">Sehen Sie sich das folgende Beispiel an:</span><span class="sxs-lookup"><span data-stu-id="9926f-250">Consider the following sample.</span></span>  <span data-ttu-id="9926f-251">Wann ist der #Tree GC?</span><span class="sxs-lookup"><span data-stu-id="9926f-251">When is the #tree GC?</span></span>  

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

<span data-ttu-id="9926f-252">Der `#leaf` verwaltet einen Verweis auf das relevante übergeordnete Element \ (parentNode \) und rekursiv bis zu `#tree` , sodass nur dann, wenn leafRef ungültig ist, die gesamte Struktur unter `#tree` einem Kandidaten für GC verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9926f-252">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Dom-Teilbäume" lightbox="../media/memory-problems-tree-gc.msft.png":::
   <span data-ttu-id="9926f-254">Dom-Teilbäume</span><span class="sxs-lookup"><span data-stu-id="9926f-254">DOM subtrees</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9926f-255">Beispiele: Probieren Sie dieses Beispiel eines [undichten DOM-Knotens][GlitchDevtoolsMemoryExample06] aus, um zu verstehen, wo er undicht sein kann und wie er erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="9926f-255">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="9926f-256">Sie können sich auch dieses Beispiel für [Undichtigkeiten von Dom anschauen, die größer als erwartet sind][GlitchDevtoolsMemoryExample09].</span><span class="sxs-lookup"><span data-stu-id="9926f-256">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="9926f-257">Weitere Informationen zu Dom-Lecks und Grundlagen der Speicheranalyse finden Sie unter Auschecken von [Speicherlecks bei der Suche nach dem Microsoft Edge-devtools][GonzaloRuizdeVillaMemory] von Gonzalo Ruiz de Villa.</span><span class="sxs-lookup"><span data-stu-id="9926f-257">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

<!--  
## Feedback   


-->  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Objektgrößen – Speicher Terminologie | Microsoft docs"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Objekte, die die Struktur des Arbeitsspeichers beibehalten | Microsoft docs"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html-Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html-Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html-Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html-Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html-Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html-Microsoft Edge (Chrom) devtools | Glitch"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "Arbeitsspeicher | Folien"  

> [!NOTE]
> <span data-ttu-id="9926f-267">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9926f-267">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9926f-268">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) gefunden und von [Meggin Kearney][MegginKearney] (Technical Writer \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="9926f-268">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="9926f-270">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9926f-270">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

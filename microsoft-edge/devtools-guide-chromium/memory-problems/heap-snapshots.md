---
title: Aufzeichnen von Heap-Snapshots
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: e6f64b219bc2b28d01780c28cc605d56a07cb491
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611678"
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





# <span data-ttu-id="7e74e-103">Aufzeichnen von Heap-Snapshots</span><span class="sxs-lookup"><span data-stu-id="7e74e-103">How to Record Heap Snapshots</span></span>   



<span data-ttu-id="7e74e-104">Erfahren Sie, wie Sie Heap-Snapshots mit dem Microsoft Edge devtools-Heap Profiler aufzeichnen und Speicherverluste finden.</span><span class="sxs-lookup"><span data-stu-id="7e74e-104">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="7e74e-105">Der Microsoft Edge devtools-Heap Profiler zeigt die Speicherverteilung nach den JavaScript-Objekten und den zugehörigen DOM-Knoten Ihrer Seite an.</span><span class="sxs-lookup"><span data-stu-id="7e74e-105">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="7e74e-106">Verwenden Sie es, um Snapshots des JavaScript-Heaps zu erstellen, Speicher Diagramme zu analysieren, Schnappschüsse zu vergleichen und Speicherverluste zu finden.</span><span class="sxs-lookup"><span data-stu-id="7e74e-106">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="7e74e-107">Siehe auch Objekte, die die [Struktur beibehalten][DevtoolsMemoryProblems101ObjectsRetainingTree].</span><span class="sxs-lookup"><span data-stu-id="7e74e-107">See also [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <span data-ttu-id="7e74e-108">Erstellen einer Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="7e74e-108">Take a snapshot</span></span>  

<span data-ttu-id="7e74e-109">Wählen Sie im **Speicher** Panel **Schnappschuss aufnehmen**und dann auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="7e74e-109">On the **Memory** panel, choose **Take snapshot**, then click **Start**.</span></span>  <span data-ttu-id="7e74e-110">Sie können auch `Ctrl` + `E` \ (Windows \) oder `Cmd` + `E` \ (macOS \) drücken.</span><span class="sxs-lookup"><span data-stu-id="7e74e-110">You may also press `Ctrl`+`E` \(Windows\) or `Cmd`+`E` \(macOS\).</span></span>  

> ##### <span data-ttu-id="7e74e-111">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="7e74e-111">Figure 1</span></span>  
> <span data-ttu-id="7e74e-112">Auswählen des Profil Erstellungs Typs</span><span class="sxs-lookup"><span data-stu-id="7e74e-112">Select profiling type</span></span>  
> ![Auswählen des Profil Erstellungs Typs][ImageProfilingType]  

<span data-ttu-id="7e74e-114">**Snapshots** werden zunächst im Speicher des Renderer-Prozesses gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7e74e-114">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="7e74e-115">Schnappschüsse werden bei Bedarf an devtools übertragen, wenn Sie auf das Schnappschuss Symbol klicken, um es anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-115">Snapshots are transferred to the DevTools on demand, when you click on the snapshot icon to view it.</span></span>  

<span data-ttu-id="7e74e-116">Nachdem der Schnappschuss in devtools geladen und analysiert wurde, wird die Zahl unterhalb des Snapshot-Titels angezeigt und zeigt die [Gesamtgröße der erreichbaren JavaScript-Objekte an][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="7e74e-116">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

> ##### <span data-ttu-id="7e74e-117">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="7e74e-117">Figure 2</span></span>  
> <span data-ttu-id="7e74e-118">Gesamtgröße der erreichbaren Objekte</span><span class="sxs-lookup"><span data-stu-id="7e74e-118">Total size of reachable objects</span></span>  
> ![Gesamtgröße der erreichbaren Objekte][ImageTotalSize]  

> [!NOTE]
> <span data-ttu-id="7e74e-120">In Schnappschüssen sind nur erreichbare Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="7e74e-120">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="7e74e-121">Außerdem beginnt das Erstellen eines Snapshots immer mit einer Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="7e74e-121">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <span data-ttu-id="7e74e-122">Löschen von Schnappschüssen</span><span class="sxs-lookup"><span data-stu-id="7e74e-122">Clear snapshots</span></span>  

<span data-ttu-id="7e74e-123">Klicken Sie auf Symbol " **alle Profile löschen** ", um Schnappschüsse zu entfernen \ (sowohl aus devtools als auch aus dem Speicher, der dem Renderer-Prozess zugeordnet ist).</span><span class="sxs-lookup"><span data-stu-id="7e74e-123">Click **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

> ##### <span data-ttu-id="7e74e-124">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="7e74e-124">Figure 3</span></span>  
> <span data-ttu-id="7e74e-125">Entfernen von Schnappschüssen</span><span class="sxs-lookup"><span data-stu-id="7e74e-125">Remove snapshots</span></span>  
> ![Entfernen von Schnappschüssen][ImageRemoveSnapshots]  

<span data-ttu-id="7e74e-127">Beim Schließen des devtools-Fensters werden keine Profile aus dem Speicher gelöscht, der dem Renderer-Prozess zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7e74e-127">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="7e74e-128">Beim erneuten Öffnen von devtools werden alle zuvor aufgenommenen Schnappschüsse wieder in der Liste der Schnappschüsse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7e74e-128">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="7e74e-129">Probieren Sie dieses Beispiel für [verstreute Objekte][GlitchDevtoolsMemoryExample03] aus, und erstellen Sie ein Profil mit dem Heap Profiler.</span><span class="sxs-lookup"><span data-stu-id="7e74e-129">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="7e74e-130">Es sollte eine Anzahl von \ (Object \)-Element Zuweisungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7e74e-130">You should see a number of \(object\) item allocations.</span></span>  

## <span data-ttu-id="7e74e-131">Anzeigen von Schnappschüssen</span><span class="sxs-lookup"><span data-stu-id="7e74e-131">View snapshots</span></span>  

<span data-ttu-id="7e74e-132">Sie können Schnappschüsse aus unterschiedlichen Perspektiven für verschiedene Aufgaben anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-132">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="7e74e-133">**Zusammenfassungsansicht** zeigt Objekte, die nach dem Namen des Konstruktors gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="7e74e-133">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="7e74e-134">Verwenden Sie es, um Objekte \ (und die Speichernutzung \) basierend auf dem Typ nach konstruktornamen gruppiert zu jagen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-134">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="7e74e-135">Dies ist besonders hilfreich für das **Aufspüren von Dom-Lecks**.</span><span class="sxs-lookup"><span data-stu-id="7e74e-135">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="7e74e-136">**Vergleichsansicht**.</span><span class="sxs-lookup"><span data-stu-id="7e74e-136">**Comparison view**.</span></span>  <span data-ttu-id="7e74e-137">Zeigt den Unterschied zwischen zwei Schnappschüssen an.</span><span class="sxs-lookup"><span data-stu-id="7e74e-137">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="7e74e-138">Verwenden Sie diese Funktion, um zwei \ (oder mehr \) Speicher-Snapshots von vor und nach einem Vorgang zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-138">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="7e74e-139">Wenn Sie das Delta in freiem Arbeitsspeicher und Verweisanzahl prüfen, können Sie das vorhanden sein und die Ursache für einen Speicherverlust bestätigen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-139">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="7e74e-140">**Einkapselungs Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="7e74e-140">**Containment view**.</span></span>  <span data-ttu-id="7e74e-141">Ermöglicht das Erforschen von Heap Inhalten.</span><span class="sxs-lookup"><span data-stu-id="7e74e-141">Allows exploration of heap contents.</span></span>  <span data-ttu-id="7e74e-142">Die **Einkapselungs Ansicht** bietet eine bessere Sicht auf die Objektstruktur und hilft, Objekte zu analysieren, auf die im globalen Namespace \ (Window \) verwiesen wird, um herauszufinden, welche Objekte in der Nähe sind.</span><span class="sxs-lookup"><span data-stu-id="7e74e-142">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="7e74e-143">Verwenden Sie es, um Verschlüsse zu analysieren und in Ihre Objekte auf einem niedrigeren Niveau zu tauchen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-143">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="7e74e-144">Um zwischen den Ansichten zu wechseln, verwenden Sie die Auswahl oben in der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="7e74e-144">To switch between views, use the selector at the top of the view.</span></span>  

> ##### <span data-ttu-id="7e74e-145">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="7e74e-145">Figure 4</span></span>  
> <span data-ttu-id="7e74e-146">Wechseln der Ansicht-Auswahl</span><span class="sxs-lookup"><span data-stu-id="7e74e-146">Switch views selector</span></span>  
> ![Wechseln der Ansicht-Auswahl][ImageSwitchViews]  

> [!NOTE]
> <span data-ttu-id="7e74e-148">Nicht alle Eigenschaften werden auf dem JavaScript-Heap gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7e74e-148">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="7e74e-149">Mit Gettern implementierte Eigenschaften, die systemeigenen Code ausführen, werden nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="7e74e-149">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="7e74e-150">Auch nicht-Zeichenfolgenwerte wie Zahlen werden nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="7e74e-150">Also, non-string values such as numbers are not captured.</span></span>  

### <span data-ttu-id="7e74e-151">Zusammenfassungsansicht</span><span class="sxs-lookup"><span data-stu-id="7e74e-151">Summary view</span></span>  

<span data-ttu-id="7e74e-152">Zunächst wird in der Zusammenfassungsansicht eine Momentaufnahme geöffnet, in der die Objektergebnisse angezeigt werden, die möglicherweise erweitert werden, um Instanzen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="7e74e-152">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

> ##### <span data-ttu-id="7e74e-153">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="7e74e-153">Figure 5</span></span>  
> <span data-ttu-id="7e74e-154">Zusammenfassungsansicht</span><span class="sxs-lookup"><span data-stu-id="7e74e-154">Summary view</span></span>  
> ![Zusammenfassungsansicht][ImageSummaryView]  

<span data-ttu-id="7e74e-156">Einträge auf oberster Ebene sind "Total"-Zeilen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-156">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="7e74e-157">Einträge auf oberster Ebene</span><span class="sxs-lookup"><span data-stu-id="7e74e-157">Top-level entries</span></span> | <span data-ttu-id="7e74e-158">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e74e-158">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="7e74e-159">Konstruktor</span><span class="sxs-lookup"><span data-stu-id="7e74e-159">Constructor</span></span>** | <span data-ttu-id="7e74e-160">Stellt alle mit diesem Konstruktor erstellten Objekte dar.</span><span class="sxs-lookup"><span data-stu-id="7e74e-160">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="7e74e-161">Entfernung</span><span class="sxs-lookup"><span data-stu-id="7e74e-161">Distance</span></span>** | <span data-ttu-id="7e74e-162">zeigt den Abstand zum Stamm mithilfe des kürzesten einfachen Pfads von Knoten an.</span><span class="sxs-lookup"><span data-stu-id="7e74e-162">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="7e74e-163">Flache Größe</span><span class="sxs-lookup"><span data-stu-id="7e74e-163">Shallow size</span></span>** | <span data-ttu-id="7e74e-164">Zeigt die Summe der flachen Größen aller Objekte an, die von einer bestimmten Konstruktorfunktion erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7e74e-164">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="7e74e-165">Die flache Größe ist die Größe des Speichers, der für ein Objekt reserviert ist \ (im allgemeinen weisen Arrays und Zeichenfolgen größere flache Größen auf \).</span><span class="sxs-lookup"><span data-stu-id="7e74e-165">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="7e74e-166">Siehe auch [Objektgrößen][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="7e74e-166">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="7e74e-167">Beibehaltungs Größe</span><span class="sxs-lookup"><span data-stu-id="7e74e-167">Retained size</span></span>** | <span data-ttu-id="7e74e-168">Zeigt die maximale Beibehaltungs Größe für den gleichen Satz von Objekten an.</span><span class="sxs-lookup"><span data-stu-id="7e74e-168">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="7e74e-169">Die Größe des Arbeitsspeichers, der nach dem Löschen eines Objekts freigegeben werden kann \ (und die abhängigen Personen sind nicht mehr erreichbar \) wird als Beibehaltungs Größe bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7e74e-169">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="7e74e-170">Siehe auch [Objektgrößen][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="7e74e-170">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="7e74e-171">Nachdem Sie eine Gesamtzeile in der oberen Ansicht erweitert haben, werden alle Instanzen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7e74e-171">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="7e74e-172">Für jede Instanz werden die flachen und gespeicherten Größen in den entsprechenden Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7e74e-172">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="7e74e-173">Die Zahl hinter dem `@` Zeichen ist die eindeutige ID des Objekts, die es Ihnen ermöglicht, Heap-Schnappschüsse pro Objekt zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-173">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="7e74e-174">Beachten Sie, dass gelbe Objekte JavaScript-Bezüge aufweisen und rote Objekte getrennte Knoten sind, auf die von einer mit einem gelben Hintergrund verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7e74e-174">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="7e74e-175">Was entsprechen die verschiedenen Konstruktoren \ (Group \)-Einträge im Heap Profiler?</span><span class="sxs-lookup"><span data-stu-id="7e74e-175">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

> ##### <span data-ttu-id="7e74e-176">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="7e74e-176">Figure 6</span></span>  
> <span data-ttu-id="7e74e-177">Konstruktorgruppen</span><span class="sxs-lookup"><span data-stu-id="7e74e-177">Constructor groups</span></span>  
> ![Konstruktorgruppen][ImageConstructorGroups]  

| <span data-ttu-id="7e74e-179">Konstruktor \ (Gruppe \) Eintrag</span><span class="sxs-lookup"><span data-stu-id="7e74e-179">Constructor \(group\) entry</span></span> | <span data-ttu-id="7e74e-180">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e74e-180">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="7e74e-181">\ (globale Eigenschaft \)</span><span class="sxs-lookup"><span data-stu-id="7e74e-181">\(global property\)</span></span>** | <span data-ttu-id="7e74e-182">Die zwischen Objekte zwischen einem globalen Objekt \ (wie `window` \) und einem Objekt, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7e74e-182">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="7e74e-183">Wenn ein Objekt mit einem Konstruktor erstellt `Person` und von einem globalen Objekt gehalten wird, sieht der Beibehaltungs Pfad wie folgt aus `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="7e74e-183">If an object is created using a constructor `Person` and is held by a global object, the retaining path would look like `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="7e74e-184">Dies steht im Gegensatz zur Norm, bei der sich Objekte direkt gegenseitig referenzieren.</span><span class="sxs-lookup"><span data-stu-id="7e74e-184">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="7e74e-185">Zwischen Objekte bestehen aus Leistungsgründen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-185">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="7e74e-186">Globals werden regelmäßig geändert, und Eigenschaftenzugriffs Optimierungen erledigen eine gute Aufgabe für nicht-globale Objekte, die nicht für Globals gelten.</span><span class="sxs-lookup"><span data-stu-id="7e74e-186">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="7e74e-187">\ (Roots \)</span><span class="sxs-lookup"><span data-stu-id="7e74e-187">\(roots\)</span></span>** | <span data-ttu-id="7e74e-188">Die Stamm Einträge in der Beibehaltungs Strukturansicht sind die Entitäten, die auf das ausgewählte Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-188">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="7e74e-189">Die Einträge können auch Verweise sein, die vom Modul für modulspezifische Zwecke erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7e74e-189">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="7e74e-190">Das Modul hat Zwischenspeicher, die auf Objekte verweisen, aber alle derartigen Bezüge sind schwach und verhindern nicht, dass ein Objekt gesammelt wird, da es keine wirklich starken Bezüge gibt.</span><span class="sxs-lookup"><span data-stu-id="7e74e-190">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="7e74e-191">\ (Closure \)</span><span class="sxs-lookup"><span data-stu-id="7e74e-191">\(closure\)</span></span>** | <span data-ttu-id="7e74e-192">Die Anzahl von Verweisen auf eine Gruppe von Objekten über Funktions Closures.</span><span class="sxs-lookup"><span data-stu-id="7e74e-192">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="7e74e-193">\ (Array, Zeichenfolge, Zahl, regexp \)</span><span class="sxs-lookup"><span data-stu-id="7e74e-193">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="7e74e-194">Eine Liste von Objekttypen mit Eigenschaften, die auf ein Array, eine Zeichenfolge, eine Zahl oder einen regulären Ausdruck verweisen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-194">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="7e74e-195">\ (kompilierter Code \)</span><span class="sxs-lookup"><span data-stu-id="7e74e-195">\(compiled code\)</span></span>** | <span data-ttu-id="7e74e-196">Alles im Zusammenhang mit kompiliertem Code.</span><span class="sxs-lookup"><span data-stu-id="7e74e-196">Everything related to compiled code.</span></span>  <span data-ttu-id="7e74e-197">Das Skript ähnelt einer Funktion, entspricht aber einem `<script>` Textkörper.</span><span class="sxs-lookup"><span data-stu-id="7e74e-197">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="7e74e-198">SharedFunctionInfos \ (SFI \) sind Objekte, die zwischen Funktionen und kompiliertem Code stehen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-198">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="7e74e-199">Funktionen haben in der Regel einen Kontext, während SFIs nicht.</span><span class="sxs-lookup"><span data-stu-id="7e74e-199">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="7e74e-200">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**usw.</span><span class="sxs-lookup"><span data-stu-id="7e74e-200">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="7e74e-201">Verweise auf Elemente oder Dokument Objekte eines bestimmten Typs, auf die der Code verweist.</span><span class="sxs-lookup"><span data-stu-id="7e74e-201">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <span data-ttu-id="7e74e-202">Vergleichsansicht</span><span class="sxs-lookup"><span data-stu-id="7e74e-202">Comparison view</span></span>  

<span data-ttu-id="7e74e-203">Suchen Sie durchgesickerte Objekte, indem Sie mehrere Schnappschüsse miteinander vergleichen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-203">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="7e74e-204">Wenn Sie sicherstellen möchten, dass ein bestimmter Anwendungsvorgang keine Undichtigkeiten verursacht \ (beispielsweise in der Regel ein paar von direkten und umgekehrten Vorgängen, wie das Öffnen eines Dokuments und das anschließende Schließen des Dokuments), sollten Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="7e74e-204">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="7e74e-205">Erstellen Sie einen Heap-Snapshot, bevor Sie einen Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-205">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="7e74e-206">Durchführen eines Vorgangs \ (Interaktion mit einer Seite auf eine Art und Weise, von der Sie glauben, dass Sie ein Leck verursacht).</span><span class="sxs-lookup"><span data-stu-id="7e74e-206">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="7e74e-207">Durchführen eines umgekehrten Vorgangs \ (die entgegengesetzte Interaktion ausführen und einige Male wiederholen \).</span><span class="sxs-lookup"><span data-stu-id="7e74e-207">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="7e74e-208">Nehmen Sie einen zweiten Heap-Snapshot auf, und ändern Sie die Ansicht dieser Person in einen **Vergleich**, und vergleichen Sie Sie mit **Snapshot 1**.</span><span class="sxs-lookup"><span data-stu-id="7e74e-208">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  

<span data-ttu-id="7e74e-209">In der **Vergleichs** Ansicht wird der Unterschied zwischen zwei Schnappschüssen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7e74e-209">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="7e74e-210">Wenn Sie einen Gesamteintrag erweitern, werden hinzugefügte und gelöschte Objektinstanzen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7e74e-210">When expanding a total entry, added and deleted object instances are shown.</span></span>  

> ##### <span data-ttu-id="7e74e-211">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="7e74e-211">Figure 7</span></span>  
> <span data-ttu-id="7e74e-212">Vergleichsansicht</span><span class="sxs-lookup"><span data-stu-id="7e74e-212">Comparison view</span></span>  
> ![Vergleichsansicht][ImageComparisonView]  

<!--todo: add HeapProfilingComparison section when available  -->  

### <span data-ttu-id="7e74e-214">Einkapselungs Ansicht</span><span class="sxs-lookup"><span data-stu-id="7e74e-214">Containment view</span></span>  

<span data-ttu-id="7e74e-215">Die **Einkapselungs** Ansicht ist im Grunde eine "Vogelperspektive" der Objektstruktur Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7e74e-215">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="7e74e-216">Sie ermöglicht es Ihnen, in Funktions Verschlüssen zu spähen, die virtuellen computerinternen Objekte zu beobachten, die zusammen Ihre JavaScript-Objekte bilden, und zu verstehen, wie viel Arbeitsspeicher Ihre Anwendung auf einem sehr geringen Niveau verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e74e-216">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="7e74e-217">Einstiegspunkte für die Eindämmungs Ansicht</span><span class="sxs-lookup"><span data-stu-id="7e74e-217">Containment view entry points</span></span> | <span data-ttu-id="7e74e-218">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e74e-218">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="7e74e-219">DOMWindow-Objekte</span><span class="sxs-lookup"><span data-stu-id="7e74e-219">DOMWindow objects</span></span>** | <span data-ttu-id="7e74e-220">Globale Objekte für JavaScript-Code.</span><span class="sxs-lookup"><span data-stu-id="7e74e-220">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="7e74e-221">GC-Stämme</span><span class="sxs-lookup"><span data-stu-id="7e74e-221">GC roots</span></span>** | <span data-ttu-id="7e74e-222">Die tatsächlichen GC-Stämme, die vom Garbage des virtuellen Computers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e74e-222">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="7e74e-223">GC-Stämme umfassen integrierte Objektzuordnungen, Symboltabellen, VM-Threadstapel, Kompilierungs Caches, handlebereiche und globale Handles.</span><span class="sxs-lookup"><span data-stu-id="7e74e-223">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="7e74e-224">Systemeigene Objekte</span><span class="sxs-lookup"><span data-stu-id="7e74e-224">Native objects</span></span>** | <span data-ttu-id="7e74e-225">Browser Objekte werden innerhalb des virtuellen JavaScript-Computers "geschoben" \ (JavaScript VM \), um die Automatisierung zu ermöglichen, beispielsweise DOM-Knoten, CSS-Regeln.</span><span class="sxs-lookup"><span data-stu-id="7e74e-225">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

> ##### <span data-ttu-id="7e74e-226">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="7e74e-226">Figure 8</span></span>  
> <span data-ttu-id="7e74e-227">Einkapselungs Ansicht</span><span class="sxs-lookup"><span data-stu-id="7e74e-227">Containment view</span></span>  
> ![Einkapselungs Ansicht][ImageContainmentView]  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="7e74e-229">Ein Tipp zu Closures.</span><span class="sxs-lookup"><span data-stu-id="7e74e-229">A tip about closures.</span></span>  <span data-ttu-id="7e74e-230">Benennen Sie die Funktionen, damit Sie problemlos zwischen den Closures im Schnappschuss unterscheiden können.</span><span class="sxs-lookup"><span data-stu-id="7e74e-230">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="7e74e-231">In diesem Beispiel werden beispielsweise keine benannten Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e74e-231">For example, this example does not use named functions.</span></span>  
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
> <span data-ttu-id="7e74e-232">In diesem Beispiel werden benannte Funktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="7e74e-232">This example uses named functions:</span></span>  
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
> > ##### old Figure 9  
> > Name functions to distinguish between closures  
> > ![Name functions to distinguish between closures][ImageDomLeaks]  
> -->  
> 
> > [!NOTE]
> > <span data-ttu-id="7e74e-233">Probieren Sie dieses Beispiel aus, [warum das `eval` böse ist][GlitchDevtoolsMemoryExample07] , um die Auswirkungen von Closures auf den Arbeitsspeicher zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="7e74e-233">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="7e74e-234">Möglicherweise sind Sie auch daran interessiert, es mit diesem Beispiel zu befolgen, das Sie durch das Aufzeichnen von [Heapzuweisungen][GlitchDevtoolsMemoryExample08]führt.</span><span class="sxs-lookup"><span data-stu-id="7e74e-234">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <span data-ttu-id="7e74e-235">Nachschlagen der Farbcodierung</span><span class="sxs-lookup"><span data-stu-id="7e74e-235">Look up color coding</span></span>  

<span data-ttu-id="7e74e-236">Eigenschaften und Eigenschaftswerte von Objekten haben unterschiedliche Typen und werden entsprechend eingefärbt.</span><span class="sxs-lookup"><span data-stu-id="7e74e-236">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="7e74e-237">Jede Eigenschaft hat einen von vier Typen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-237">Each property has one of four types.</span></span>  

| <span data-ttu-id="7e74e-238">Eigenschaftstyp</span><span class="sxs-lookup"><span data-stu-id="7e74e-238">Property Type</span></span> | <span data-ttu-id="7e74e-239">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e74e-239">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="7e74e-240">a: Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7e74e-240">a: property</span></span>** | <span data-ttu-id="7e74e-241">Eine reguläre Eigenschaft mit einem Namen, auf den über den `.` \ (dot \)-Operator zugegriffen wird, `[` `]` beispielsweise über die Notation \ (Brackets \) `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="7e74e-241">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="7e74e-242">0: Element</span><span class="sxs-lookup"><span data-stu-id="7e74e-242">0: element</span></span>** | <span data-ttu-id="7e74e-243">Eine reguläre Eigenschaft mit einem numerischen Index, auf die über `[` `]` \ (eckige Klammern \)-Notation zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="7e74e-243">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="7e74e-244">a: Kontext var</span><span class="sxs-lookup"><span data-stu-id="7e74e-244">a: context var</span></span>** |  <span data-ttu-id="7e74e-245">Eine Variable in einem Funktionskontext, auf die über den Variablennamen in einem Funktions Abschluss zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e74e-245">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="7e74e-246">a: System Prop</span><span class="sxs-lookup"><span data-stu-id="7e74e-246">a: system prop</span></span>** | <span data-ttu-id="7e74e-247">Eine von der JavaScript-VM hinzugefügte Eigenschaft, auf die über JavaScript-Code nicht zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e74e-247">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="7e74e-248">Objekte, `System` die als kein entsprechender JavaScript-Typ gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="7e74e-248">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="7e74e-249">Jede ist Teil der Objekt Systemimplementierung der JavaScript-VM.</span><span class="sxs-lookup"><span data-stu-id="7e74e-249">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="7e74e-250">V8 ordnet die meisten internen Objekte im gleichen Heap wie die JS-Objekte des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="7e74e-250">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="7e74e-251">Das sind also nur V8-Interna.</span><span class="sxs-lookup"><span data-stu-id="7e74e-251">So these are just V8 internals.</span></span>  

## <span data-ttu-id="7e74e-252">Suchen nach einem bestimmten Objekt</span><span class="sxs-lookup"><span data-stu-id="7e74e-252">Find a specific object</span></span>  

<span data-ttu-id="7e74e-253">Wenn Sie ein Objekt im gesammelten Heap suchen möchten, können Sie `Ctrl` + `F` die Objekt-ID verwenden und angeben.</span><span class="sxs-lookup"><span data-stu-id="7e74e-253">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <span data-ttu-id="7e74e-254">Aufdecken von Dom-Lecks</span><span class="sxs-lookup"><span data-stu-id="7e74e-254">Uncover DOM leaks</span></span>  

<span data-ttu-id="7e74e-255">Der Heap-Profiler hat die Möglichkeit, bidirektionale Abhängigkeiten zwischen Browser systemeigenen Objekten \ (DOM-Knoten, CSS-Regeln \) und JavaScript-Objekten wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="7e74e-255">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="7e74e-256">Dies hilft bei der Ermittlung von ansonsten unsichtbaren Lecks, die durch vergessene, freigegebene Dom-unter Bäume entstehen.</span><span class="sxs-lookup"><span data-stu-id="7e74e-256">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="7e74e-257">Dom-Lecks können größer sein, als Sie denken.</span><span class="sxs-lookup"><span data-stu-id="7e74e-257">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="7e74e-258">Sehen Sie sich das folgende Beispiel an:</span><span class="sxs-lookup"><span data-stu-id="7e74e-258">Consider the following sample.</span></span>  <span data-ttu-id="7e74e-259">Wann ist der #Tree GC?</span><span class="sxs-lookup"><span data-stu-id="7e74e-259">When is the #tree GC?</span></span>  

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

<span data-ttu-id="7e74e-260">Der `#leaf` verwaltet einen Verweis auf das relevante übergeordnete Element \ (parentNode \) und rekursiv bis zu `#tree` , sodass nur dann, wenn leafRef ungültig ist, die gesamte Struktur unter `#tree` einem Kandidaten für GC verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7e74e-260">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

> ##### <span data-ttu-id="7e74e-261">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="7e74e-261">Figure 9</span></span>  
> <span data-ttu-id="7e74e-262">Dom-Teilbäume</span><span class="sxs-lookup"><span data-stu-id="7e74e-262">DOM subtrees</span></span>  
> <span data-ttu-id="7e74e-263">! [Dom-Teilbäume] [ImageTreeGc]</span><span class="sxs-lookup"><span data-stu-id="7e74e-263">![DOM subtrees][ImageTreeGc]</span></span>  

> [!NOTE]
> <span data-ttu-id="7e74e-264">Beispiele: Probieren Sie dieses Beispiel eines [undichten DOM-Knotens][GlitchDevtoolsMemoryExample06] aus, um zu verstehen, wo er undicht sein kann und wie er erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="7e74e-264">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="7e74e-265">Sie können sich auch dieses Beispiel für [Undichtigkeiten von Dom anschauen, die größer als erwartet sind][GlitchDevtoolsMemoryExample09].</span><span class="sxs-lookup"><span data-stu-id="7e74e-265">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="7e74e-266">Weitere Informationen zu Dom-Lecks und Grundlagen der Speicheranalyse finden Sie unter Auschecken von [Speicherlecks bei der Suche nach dem Microsoft Edge-devtools][GonzaloRuizdeVillaMemory] von Gonzalo Ruiz de Villa.</span><span class="sxs-lookup"><span data-stu-id="7e74e-266">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

<!--## Feedback   -->  



<!-- image links -->  

[ImageProfilingType]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png "Abbildung 1: Auswählen des Profil Erstellungs Typs"  
[ImageTotalSize]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png "Abbildung 2: Gesamtgröße der erreichbaren Objekte"  
[ImageRemoveSnapshots]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png "Abbildung 3: Entfernen von Schnappschüssen"  
[ImageSwitchViews]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png "Abbildung 4: Wechseln der Ansicht-Auswahl"  
[ImageSummaryView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png "Abbildung 5: Zusammenfassungsansicht"  
[ImageConstructorGroups]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png "Abbildung 6: konstruktorgruppen"  
[ImageComparisonView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png "Abbildung 7: Vergleichsansicht"  
[ImageContainmentView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png "Abbildung 8: Kapselungs Ansicht"  
<!--[ImageDomLeaks]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-domleaks.msft.png "old Figure 9: Name functions to distinguish between closures"  -->  
[ImageTreeGc]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Memory-Problems-Tree-GC.msft.png "Abbildung 9: Dom-unter Strukturen"  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: /microsoft-edge/devtools-guide-chromium/memory-problems/memory-101#object-sizes "Objektgrößen – Arbeitsspeicher Terminologie"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: /microsoft-edge/devtools-guide-chromium/memory-problems/memory-101#objects-retaining-tree "Objekte, die die Struktur des Arbeitsspeichers beibehalten"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "Example-03. html – Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "Example-06. html – Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "Example-07. html – Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "Example-08. html – Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "Example-09. html – Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "Example-10. html – Microsoft Edge (Chrom) devtools | Glitch"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "Arbeitsspeicher | Folien"  

> [!NOTE]
> <span data-ttu-id="7e74e-285">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e74e-285">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7e74e-286">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) gefunden und von [Meggin Kearney][MegginKearney] (Technical Writer \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e74e-286">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="7e74e-288">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7e74e-288">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

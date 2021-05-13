---
description: In diesem Abschnitt werden allgemeine Begriffe beschrieben, die in der Speicheranalyse verwendet werden und für eine Vielzahl von Speicherprofilerstellungstools für verschiedene Sprachen gelten.
title: Arbeitsspeicherterminologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 58b3ecde157b1c551b6c0cd435049ce221555519
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564770"
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
# <a name="memory-terminology"></a><span data-ttu-id="7cd02-104">Arbeitsspeicherterminologie</span><span class="sxs-lookup"><span data-stu-id="7cd02-104">Memory terminology</span></span>  

<span data-ttu-id="7cd02-105">Dieser Artikel beschreibt allgemeine Begriffe, die in der Speicheranalyse verwendet werden, und gilt für verschiedene Speicherprofilerstellungstools für verschiedene Sprachen.</span><span class="sxs-lookup"><span data-stu-id="7cd02-105">This article describes common terms used in memory analysis, and is applicable to various memory profiling tools for different languages.</span></span>  

<span data-ttu-id="7cd02-106">Die hier beschriebenen Begriffe und Begriffe beziehen sich auf den [Speicherbereich][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="7cd02-106">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="7cd02-107">Wenn Sie jemals mit dem Java, .NET oder einem anderen Speicherprofiler gearbeitet haben, kann dieser Artikel eine Aktualisierung sein.</span><span class="sxs-lookup"><span data-stu-id="7cd02-107">If you have ever worked with either the Java, .NET, or some other memory profiler, then this article may be a refresher.</span></span>  

## <a name="object-sizes"></a><span data-ttu-id="7cd02-108">Objektgrößen</span><span class="sxs-lookup"><span data-stu-id="7cd02-108">Object sizes</span></span>  

<span data-ttu-id="7cd02-109">Stellen Sie sich Speicher als Diagramm mit grundtypen \(wie Zahlen und Zeichenfolgen\) und Objekten \(assoziative Arrays\) vor.</span><span class="sxs-lookup"><span data-stu-id="7cd02-109">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="7cd02-110">Es kann als Diagramm mit vielen verbundenen Punkten angezeigt werden, z. B. der folgenden Abbildung.</span><span class="sxs-lookup"><span data-stu-id="7cd02-110">It may display as a graph with many interconnected points such as following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Visuelle Darstellung des Arbeitsspeichers" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="7cd02-112">Visuelle Darstellung des Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="7cd02-112">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="7cd02-113">Ein Objekt kann auf zwei Arten Arbeitsspeicher haben:</span><span class="sxs-lookup"><span data-stu-id="7cd02-113">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="7cd02-114">Direkt durch das Objekt.</span><span class="sxs-lookup"><span data-stu-id="7cd02-114">Directly by the object.</span></span>  
*   <span data-ttu-id="7cd02-115">Implizit durch Das Halten von Verweisen auf andere Objekte und damit verhindern, dass diese Objekte automatisch von einem Garbage Collector verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="7cd02-115">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector.</span></span>  

<span data-ttu-id="7cd02-116">Bei der Arbeit mit dem [Speicherbereich][DevtoolsMemoryProblemsHeapSnapshots] in DevTools \(ein Tool zur Untersuchung von Speicherproblemen unter **Speicher**\) können Sie sich einige verschiedene Spalten mit Informationen anschauen.</span><span class="sxs-lookup"><span data-stu-id="7cd02-116">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="7cd02-117">Zwei, die sich abhingen, sind **Flache Größe** und **Beibehaltene Größe,** aber was stellen diese dar?</span><span class="sxs-lookup"><span data-stu-id="7cd02-117">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Flache und beibehaltene Größe" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="7cd02-119">Flache und beibehaltene Größe</span><span class="sxs-lookup"><span data-stu-id="7cd02-119">Shallow and Retained Size</span></span>  
:::image-end:::  

### <a name="shallow-size"></a><span data-ttu-id="7cd02-120">Flache Größe</span><span class="sxs-lookup"><span data-stu-id="7cd02-120">Shallow size</span></span>  

<span data-ttu-id="7cd02-121">Dies ist die Größe des Arbeitsspeichers, der vom Objekt gehalten wird.</span><span class="sxs-lookup"><span data-stu-id="7cd02-121">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="7cd02-122">Bei typischen JavaScript-Objekten ist etwas Arbeitsspeicher für die Beschreibung und das Speichern von unmittelbaren Werten reserviert.</span><span class="sxs-lookup"><span data-stu-id="7cd02-122">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="7cd02-123">In der Regel können nur Arrays und Zeichenfolgen eine erhebliche flache Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7cd02-123">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="7cd02-124">Zeichenfolgen und externe Arrays verfügen jedoch häufig über ihren Hauptspeicher im Rendererspeicher, was nur ein kleines Wrapperobjekt im JavaScript-Heap verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="7cd02-124">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="7cd02-125">Rendererspeicher ist der ganze Speicher des Prozesses, in dem eine überprüfte Seite gerendert wird: systemeigener Speicher + JS-Heapspeicher der Seite + JS-Heapspeicher aller dedizierten Mitarbeiter, die von der Seite gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="7cd02-125">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="7cd02-126">Dennoch kann selbst ein kleines Objekt indirekt einen großen Speicher enthalten, indem verhindert wird, dass andere Objekte durch den automatischen Garbage Collection-Prozess verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="7cd02-126">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <a name="retained-size"></a><span data-ttu-id="7cd02-127">Beibehaltene Größe</span><span class="sxs-lookup"><span data-stu-id="7cd02-127">Retained size</span></span>  

<span data-ttu-id="7cd02-128">Dies ist die Größe des Arbeitsspeichers, der freigegeben wird, nachdem das Objekt gelöscht wurde, zusammen mit den abhängigen Objekten, die aus Garbage Collector-Ursprüngen nicht erreichbar **gemacht wurden.**</span><span class="sxs-lookup"><span data-stu-id="7cd02-128">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots**.</span></span>  

<span data-ttu-id="7cd02-129">**Garbage Collector-Ursprünge** werden \*\*\*\* aus Handles erstellt, die \(entweder lokal oder global\) erstellt werden, wenn ein Verweis aus systemeigenem Code auf ein JavaScript-Objekt außerhalb von V8 erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7cd02-129">**Garbage Collector roots** are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="7cd02-130">Alle diese Handles finden Sie in einer Heapmomentaufnahme unter **GC roots**  >  **Handle scope** und GC **roots**  >  **Global handles**.</span><span class="sxs-lookup"><span data-stu-id="7cd02-130">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="7cd02-131">Die Beschreibung der Handles in dieser Dokumentation, ohne details zur Browserimplementierung zu machen, kann verwirrend sein.</span><span class="sxs-lookup"><span data-stu-id="7cd02-131">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="7cd02-132">Sowohl garbage collector roots als auch die Handles müssen Sie sich keine Sorgen machen.</span><span class="sxs-lookup"><span data-stu-id="7cd02-132">Both Garbage Collector roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="7cd02-133">Es gibt viele interne Garbage Collector-Ursprünge, von denen die meisten für die Benutzer nicht interessant sind.</span><span class="sxs-lookup"><span data-stu-id="7cd02-133">There are lots of internal Garbage Collector roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="7cd02-134">Aus Der Sicht der Anwendungen gibt es die folgenden Arten von Ursprüngen.</span><span class="sxs-lookup"><span data-stu-id="7cd02-134">From the applications standpoint, there are the following kinds of roots.</span></span>  

*   <span data-ttu-id="7cd02-135">Window global object \(in each iframe\).</span><span class="sxs-lookup"><span data-stu-id="7cd02-135">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="7cd02-136">In den Heapmomentaufnahmen gibt das Feld die Anzahl der Eigenschaftsverweise auf dem kürzesten `distance` Aufbewahrungspfad aus dem Fenster an.</span><span class="sxs-lookup"><span data-stu-id="7cd02-136">In the heap snapshots, the `distance` field indicates the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="7cd02-137">Die Dokument-DOM-Struktur, die aus allen systemeigenen DOM-Knoten besteht, die durch Durchlaufen des Dokuments erreichbar sind.</span><span class="sxs-lookup"><span data-stu-id="7cd02-137">The document DOM tree, consisting of all native DOM nodes that are reachable by traversing the document.</span></span>  <span data-ttu-id="7cd02-138">Nicht alle Knoten verfügen über JavaScript-Wrapper, aber wenn ein Knoten über einen Wrapper verfügt, ist der Knoten lebendig, während das Dokument lebendig ist.</span><span class="sxs-lookup"><span data-stu-id="7cd02-138">Not all of the nodes have JavaScript wrappers, but if a node has a wrapper, the node is alive while the document is alive.</span></span>  
*   <span data-ttu-id="7cd02-139">Manchmal werden Objekte im Debugkontext im **Tool Sources** und in der **Konsole**beibehalten, z. B. nach der Konsolenauswertung.</span><span class="sxs-lookup"><span data-stu-id="7cd02-139">Sometimes objects are retained by the debug context in the **Sources** tool and the **Console**, such as after Console evaluation.</span></span>  <span data-ttu-id="7cd02-140">Erstellen Sie Heapmomentaufnahmen mit einem geräumten **Konsolentool** und keine aktiven Haltepunkte im Debugger im **Sources-Tool.**</span><span class="sxs-lookup"><span data-stu-id="7cd02-140">Create heap snapshots with a cleared **Console** tool and no active breakpoints in the debugger in the **Sources** tool.</span></span>

>[!TIP]
> <span data-ttu-id="7cd02-141">Deaktivieren Sie vor dem Erstellen einer \*\*\*\* Heapmomentaufnahme im [Speichertool][DevtoolsMemoryProblemsHeapSnapshots] das Konsolentool, und deaktivieren Sie haltepunkte im **Tool Quellen.**</span><span class="sxs-lookup"><span data-stu-id="7cd02-141">Before taking a heap snapshot in the [Memory][DevtoolsMemoryProblemsHeapSnapshots] tool, clear the **Console** tool and deactivate breakpoints in the **Sources** tool.</span></span>  <span data-ttu-id="7cd02-142">Führen Sie die Methode **aus,** um das Konsolentool zu `clear()` löschen.</span><span class="sxs-lookup"><span data-stu-id="7cd02-142">To clear the **Console** tool, run the `clear()` method.</span></span>  

<span data-ttu-id="7cd02-143">Das Speicherdiagramm beginnt mit einem Stamm, der das Objekt des Browsers oder das Objekt eines Node.js `window` `Global` sein kann.</span><span class="sxs-lookup"><span data-stu-id="7cd02-143">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="7cd02-144">Sie können nicht steuern, wie das Stammobjekt gesammelt wird.</span><span class="sxs-lookup"><span data-stu-id="7cd02-144">You do not control how the root object is garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Sie können nicht steuern, wie das Stammobjekt als Garbage Collection erfasst wird." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="7cd02-146">Sie können nicht steuern, wie das Stammobjekt als Garbage Collection erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="7cd02-146">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="7cd02-147">Was vom Stamm aus nicht erreichbar ist, wird garbage collected.</span><span class="sxs-lookup"><span data-stu-id="7cd02-147">Whatever is not reachable from the root gets garbage collected.</span></span>  

> [!NOTE]
> <span data-ttu-id="7cd02-148">Sowohl die [Spalten "Flache Größe"](#shallow-size) [als auch "Beibehaltene Größe"](#retained-size) stellen Daten in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="7cd02-148">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <a name="objects-retaining-tree"></a><span data-ttu-id="7cd02-149">Aufbewahrungsstruktur für Objekte</span><span class="sxs-lookup"><span data-stu-id="7cd02-149">Objects retaining tree</span></span>  

<span data-ttu-id="7cd02-150">Der Heap ist ein Netzwerk von miteinander verbundenen Objekten.</span><span class="sxs-lookup"><span data-stu-id="7cd02-150">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="7cd02-151">In der mathematischen Welt wird diese Struktur als Diagramm **oder** Speicherdiagramm bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7cd02-151">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="7cd02-152">Ein Diagramm wird aus Knoten **erstellt,** die über Kanten verbunden **sind,** die beide Beschriftungen erhalten.</span><span class="sxs-lookup"><span data-stu-id="7cd02-152">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="7cd02-153">**Knoten** \(oder **Objekte**\) werden mit \*\*\*\* dem Namen der Konstruktorfunktion gekennzeichnet, die zum Erstellen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7cd02-153">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="7cd02-154">**Kanten** werden mit den Namen von Eigenschaften **gekennzeichnet.**</span><span class="sxs-lookup"><span data-stu-id="7cd02-154">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="7cd02-155">Erfahren [Sie, wie Sie ein Profil mit dem Heap Profiler aufzeichnen.][DevtoolsMemoryProblemsHeapSnapshots]</span><span class="sxs-lookup"><span data-stu-id="7cd02-155">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="7cd02-156">In der folgenden Abbildung sind einige der wichtigsten Dinge in der Heap Snapshot-Aufzeichnung im [Tool Speicher][DevtoolsMemoryProblemsHeapSnapshots] enthalten: der Abstand zum Garbage Collector-Stamm.</span><span class="sxs-lookup"><span data-stu-id="7cd02-156">In the following figure, some of the notable things in the Heap Snapshot recording in the [Memory][DevtoolsMemoryProblemsHeapSnapshots] tool include distance:  the distance from the Garbage Collector root.</span></span>  <span data-ttu-id="7cd02-157">Wenn sich fast alle Objekte desselben Typs in derselben Entfernung befinden und einige wenige sich in größerer Entfernung befinden, ist dies eine Untersuchung wert.</span><span class="sxs-lookup"><span data-stu-id="7cd02-157">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Abstand zum Stamm" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="7cd02-159">Abstand zum Stamm</span><span class="sxs-lookup"><span data-stu-id="7cd02-159">Distance from root</span></span>  
:::image-end:::  

## <a name="dominators"></a><span data-ttu-id="7cd02-160">Dominante</span><span class="sxs-lookup"><span data-stu-id="7cd02-160">Dominators</span></span>  

<span data-ttu-id="7cd02-161">Dominantor-Objekte bestehen aus einer Strukturstruktur, da jedes Objekt über genau einen Dominanter verfügt.</span><span class="sxs-lookup"><span data-stu-id="7cd02-161">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="7cd02-162">Einem #A0 eines Objekts fehlen möglicherweise direkte Verweise auf ein objekt, das es überragt. Das heißt, die Struktur des Dominantors ist keine spannende Struktur des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="7cd02-162">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="7cd02-163">In der folgenden Abbildung ist die folgende Anweisung true.</span><span class="sxs-lookup"><span data-stu-id="7cd02-163">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="7cd02-164">Knoten 1 überwiegen Knoten 2</span><span class="sxs-lookup"><span data-stu-id="7cd02-164">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="7cd02-165">Knoten 2 überwiegen die Knoten 3, 4 und 6</span><span class="sxs-lookup"><span data-stu-id="7cd02-165">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="7cd02-166">Knoten 3 überwiegen Knoten 5</span><span class="sxs-lookup"><span data-stu-id="7cd02-166">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="7cd02-167">Knoten 5 überwiegen Knoten 8</span><span class="sxs-lookup"><span data-stu-id="7cd02-167">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="7cd02-168">Knoten 6 überwiegen Knoten 7</span><span class="sxs-lookup"><span data-stu-id="7cd02-168">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Struktur der dominanten Struktur" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="7cd02-170">Struktur der dominanten Struktur</span><span class="sxs-lookup"><span data-stu-id="7cd02-170">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="7cd02-171">In der folgenden Abbildung ist Knoten der Dominante von , ist aber auch in jedem einfachen Pfad von `#3` `#10` Garbage Collector zu `#7` `#10` vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7cd02-171">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector to `#10`.</span></span>  <span data-ttu-id="7cd02-172">Daher ist ein Objekt B ein Dominanter eines Objekts A, wenn B in jedem einfachen Pfad vom Stamm zum Objekt A vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7cd02-172">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Animierte Dominantor-Illustration" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="7cd02-174">Animierte Dominantor-Illustration</span><span class="sxs-lookup"><span data-stu-id="7cd02-174">Animated dominator illustration</span></span>  
:::image-end:::  

## <a name="v8-specifics"></a><span data-ttu-id="7cd02-175">V8-Spezifische</span><span class="sxs-lookup"><span data-stu-id="7cd02-175">V8 specifics</span></span>  

<span data-ttu-id="7cd02-176">Beim Profilerstellungsspeicher ist es hilfreich zu verstehen, warum Heapmomentaufnahmen auf eine bestimmte Weise aussehen.</span><span class="sxs-lookup"><span data-stu-id="7cd02-176">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="7cd02-177">In diesem Abschnitt werden einige Speicherthemen beschrieben, die speziell dem **virtuellen V8-JavaScript-Computer** \(V8 VM oder VM\) zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7cd02-177">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <a name="javascript-object-representation"></a><span data-ttu-id="7cd02-178">JavaScript-Objektdarstellung</span><span class="sxs-lookup"><span data-stu-id="7cd02-178">JavaScript object representation</span></span>  

<span data-ttu-id="7cd02-179">Es gibt drei Grundtypen:</span><span class="sxs-lookup"><span data-stu-id="7cd02-179">There are three primitive types:</span></span>  

*   <span data-ttu-id="7cd02-180">Zahlen \(z. B. `3.14159...` \)</span><span class="sxs-lookup"><span data-stu-id="7cd02-180">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="7cd02-181">Booleans \( `true` oder `false` \)</span><span class="sxs-lookup"><span data-stu-id="7cd02-181">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="7cd02-182">Zeichenfolgen \(z. B. `"Werner Heisenberg"` \)</span><span class="sxs-lookup"><span data-stu-id="7cd02-182">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="7cd02-183">Grundtypen können nicht auf andere Werte verweisen und sind immer Blatt- oder Endknoten.</span><span class="sxs-lookup"><span data-stu-id="7cd02-183">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="7cd02-184">**Zahlen** können wie folgt gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="7cd02-184">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="7cd02-185">ein sofortiger ganzzahliger 31-Bit-Wert, der als **kleine ganze Zahlen** \(**SMI**s\) bezeichnet wird, oder</span><span class="sxs-lookup"><span data-stu-id="7cd02-185">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="7cd02-186">Heapobjekte, die als **Heapnummern bezeichnet werden.**</span><span class="sxs-lookup"><span data-stu-id="7cd02-186">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="7cd02-187">Heapnummern werden zum Speichern von Werten verwendet, die nicht in das SMI-Formular passen, z. B. **Doubles**oder wenn ein Wert geschachtelt werden **muss,** z. B. festlegen von Eigenschaften darauf.</span><span class="sxs-lookup"><span data-stu-id="7cd02-187">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="7cd02-188">**Zeichenfolgen** können in einer der beiden Dateien gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="7cd02-188">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="7cd02-189">der **VM-Heap**oder</span><span class="sxs-lookup"><span data-stu-id="7cd02-189">the **VM heap**, or</span></span>
*   <span data-ttu-id="7cd02-190">extern im **Speicher des Renderers**.</span><span class="sxs-lookup"><span data-stu-id="7cd02-190">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="7cd02-191">Ein **Wrapperobjekt** wird erstellt und für den Zugriff auf externen Speicher verwendet, in dem beispielsweise Skriptquellen und andere Inhalte gespeichert werden, die aus dem Web empfangen werden, anstatt in den VM-Heap kopiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="7cd02-191">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="7cd02-192">Der Arbeitsspeicher für neue JavaScript-Objekte wird über einen dedizierten JavaScript-Heap \(oder **VM-Heap\)** zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="7cd02-192">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="7cd02-193">Diese Objekte werden vom Garbage Collector in V8 verwaltet und bleiben daher am Leben, solange mindestens ein starker Verweis darauf besteht.</span><span class="sxs-lookup"><span data-stu-id="7cd02-193">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="7cd02-194">Alles, was sich nicht im JavaScript-Heap befindet, wird als **systemeigenes Objekt bezeichnet.**</span><span class="sxs-lookup"><span data-stu-id="7cd02-194">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="7cd02-195">Systemeigene Objekte werden im Gegensatz zu Heapobjekten nicht während ihrer gesamten Lebensdauer vom V8-Garbage Collector verwaltet und können nur über JavaScript mithilfe des JavaScript-Wrapperobjekts zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="7cd02-195">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="7cd02-196">**Cons string** ist ein Objekt, das aus Paaren von Zeichenfolgen besteht, die gespeichert und dann verbunden werden, und ist ein Ergebnis der Verkettung.</span><span class="sxs-lookup"><span data-stu-id="7cd02-196">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="7cd02-197">Die Verbindung der **Inhalte der Cons-Zeichenfolge** erfolgt nur nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="7cd02-197">The joining of the **cons string** contents occurs only as needed.</span></span>  <span data-ttu-id="7cd02-198">Wenn z. B. eine Teilzeichenfolge einer angeschlossenen Zeichenfolge erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="7cd02-198">For example, when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="7cd02-199">Wenn Sie z. B. und verketten, erhalten Sie eine Zeichenfolge, die das Ergebnis der `a` `b` `(a, b)` Verkettung darstellt.</span><span class="sxs-lookup"><span data-stu-id="7cd02-199">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="7cd02-200">Wenn Sie später mit diesem Ergebnis `d` verkettet sind, erhalten Sie eine weitere **Cons-Zeichenfolge:** `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="7cd02-200">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="7cd02-201">**Array** ist ein Objekt mit numerischen Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="7cd02-201">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="7cd02-202">**Arrays** werden in der V8 VM umfassend zum Speichern großer Datenmengen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7cd02-202">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="7cd02-203">Sätze von Schlüssel-Wert-Paaren, z. B. Wörterbücher, werden durch **Arrays gesichert.**</span><span class="sxs-lookup"><span data-stu-id="7cd02-203">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="7cd02-204">Ein typisches JavaScript-Objekt wird nur als einer von zwei **Arraytypen** gespeichert:</span><span class="sxs-lookup"><span data-stu-id="7cd02-204">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="7cd02-205">benannte Eigenschaften und</span><span class="sxs-lookup"><span data-stu-id="7cd02-205">named properties, and</span></span>  
*   <span data-ttu-id="7cd02-206">numerische Elemente</span><span class="sxs-lookup"><span data-stu-id="7cd02-206">numeric elements</span></span>  

<span data-ttu-id="7cd02-207">Bei einer kleinen Anzahl von Eigenschaften werden die Eigenschaften intern im JavaScript-Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7cd02-207">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="7cd02-208">**Map** ist ein Objekt, das sowohl den Objekttyp als auch das Layout beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7cd02-208">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="7cd02-209">Beispielsweise werden Karten verwendet, um implizite Objekthierarchien für den [schnellen Eigenschaftenzugriff zu beschreiben.][V8FastProperties]</span><span class="sxs-lookup"><span data-stu-id="7cd02-209">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <a name="object-groups"></a><span data-ttu-id="7cd02-210">Objektgruppen</span><span class="sxs-lookup"><span data-stu-id="7cd02-210">Object groups</span></span>  

<span data-ttu-id="7cd02-211">Jede **systemeigene Objektgruppe** besteht aus Objekten, die gegenseitige Verweise aufeinander enthalten.</span><span class="sxs-lookup"><span data-stu-id="7cd02-211">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="7cd02-212">Stellen Sie sich beispielsweise eine DOM-Unterstruktur vor, in der jeder Knoten eine Verknüpfung zum relativen übergeordneten Element und Links zum nächsten untergeordneten und nächsten gleichgeordneten Element hat und daher ein verbundenes Diagramm bildet.</span><span class="sxs-lookup"><span data-stu-id="7cd02-212">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="7cd02-213">Systemeigene Objekte werden nicht im JavaScript-Heap dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7cd02-213">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="7cd02-214">Die fehlende Darstellung ist der Grund, warum systemeigene Objekte die Größe Null haben.</span><span class="sxs-lookup"><span data-stu-id="7cd02-214">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="7cd02-215">Stattdessen werden Wrapperobjekte erstellt.</span><span class="sxs-lookup"><span data-stu-id="7cd02-215">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="7cd02-216">Jedes Wrapperobjekt enthält einen Verweis auf das entsprechende systemeigene Objekt zum Umleiten von Befehlen an dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="7cd02-216">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="7cd02-217">Eine Objektgruppe enthält wiederum Wrapperobjekte.</span><span class="sxs-lookup"><span data-stu-id="7cd02-217">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="7cd02-218">Dadurch wird jedoch kein unkollektierbarer Zyklus erstellt, da Garbage Collector intelligent genug ist, um Objektgruppen frei zu lassen, auf deren Wrapper nicht mehr verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7cd02-218">However, this does not create an uncollectable cycle, as Garbage Collector is smart enough to release object groups whose wrappers are no longer referenced.</span></span>  <span data-ttu-id="7cd02-219">Vergessen sie jedoch, einen einzelnen Wrapper zu veröffentlichen, enthält die gesamte Gruppe und die zugehörigen Wrapper.</span><span class="sxs-lookup"><span data-stu-id="7cd02-219">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7cd02-220">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="7cd02-220">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Aufzeichnen von Heapmomentaufnahmen | Microsoft Docs"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Schnelle Eigenschaften in V8-| V8"  

> [!NOTE]
> <span data-ttu-id="7cd02-223">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cd02-223">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7cd02-224">Die ursprüngliche Seite befindet sich [hier und](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) wird von [Meggin Kearney][MegginKearney] \(Technical Writer\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="7cd02-224">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="7cd02-226">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7cd02-226">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney

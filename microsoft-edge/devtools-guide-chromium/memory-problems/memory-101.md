---
description: In diesem Abschnitt werden allgemeine Begriffe beschrieben, die in der Speicheranalyse verwendet werden und für eine Vielzahl von Speicherprofilerstellungstools für verschiedene Sprachen gelten.
title: Speicherterminologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 1579374be29f0f419ded3bf88f5dea284f0bbb1a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397790"
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

# <a name="memory-terminology"></a><span data-ttu-id="45940-104">Speicherterminologie</span><span class="sxs-lookup"><span data-stu-id="45940-104">Memory terminology</span></span>  

<span data-ttu-id="45940-105">Dieser Artikel beschreibt allgemeine Begriffe, die in der Speicheranalyse verwendet werden, und gilt für verschiedene Speicherprofilerstellungstools für verschiedene Sprachen.</span><span class="sxs-lookup"><span data-stu-id="45940-105">This article describes common terms used in memory analysis, and is applicable to various memory profiling tools for different languages.</span></span>  

<span data-ttu-id="45940-106">Die hier beschriebenen Begriffe und Begriffe beziehen sich auf den [Speicherbereich][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="45940-106">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="45940-107">Wenn Sie jemals mit dem Java, .NET oder einem anderen Speicherprofiler gearbeitet haben, kann dieser Artikel eine Aktualisierung sein.</span><span class="sxs-lookup"><span data-stu-id="45940-107">If you have ever worked with either the Java, .NET, or some other memory profiler, then this article may be a refresher.</span></span>  

## <a name="object-sizes"></a><span data-ttu-id="45940-108">Objektgrößen</span><span class="sxs-lookup"><span data-stu-id="45940-108">Object sizes</span></span>  

<span data-ttu-id="45940-109">Stellen Sie sich Speicher als Diagramm mit grundtypen \(wie Zahlen und Zeichenfolgen\) und Objekten \(assoziative Arrays\) vor.</span><span class="sxs-lookup"><span data-stu-id="45940-109">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="45940-110">Es kann als Diagramm mit vielen verbundenen Punkten angezeigt werden, z. B. der folgenden Abbildung.</span><span class="sxs-lookup"><span data-stu-id="45940-110">It may display as a graph with many interconnected points such as following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Visuelle Darstellung des Arbeitsspeichers" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="45940-112">Visuelle Darstellung des Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="45940-112">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="45940-113">Ein Objekt kann auf zwei Arten Arbeitsspeicher haben:</span><span class="sxs-lookup"><span data-stu-id="45940-113">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="45940-114">Direkt durch das Objekt.</span><span class="sxs-lookup"><span data-stu-id="45940-114">Directly by the object.</span></span>  
*   <span data-ttu-id="45940-115">Implizit durch Das Halten von Verweisen auf andere Objekte und damit verhindern, dass diese Objekte automatisch von einem Garbage Collector verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="45940-115">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector.</span></span>  

<span data-ttu-id="45940-116">Bei der Arbeit mit dem [Speicherbereich][DevtoolsMemoryProblemsHeapSnapshots] in DevTools \(ein Tool zur Untersuchung von Speicherproblemen unter **Speicher**\) können Sie sich einige verschiedene Spalten mit Informationen anschauen.</span><span class="sxs-lookup"><span data-stu-id="45940-116">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="45940-117">Zwei, die sich abhingen, sind **Flache Größe** und **Beibehaltene Größe,** aber was stellen diese dar?</span><span class="sxs-lookup"><span data-stu-id="45940-117">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Flache und beibehaltene Größe" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="45940-119">Flache und beibehaltene Größe</span><span class="sxs-lookup"><span data-stu-id="45940-119">Shallow and Retained Size</span></span>  
:::image-end:::  

### <a name="shallow-size"></a><span data-ttu-id="45940-120">Flache Größe</span><span class="sxs-lookup"><span data-stu-id="45940-120">Shallow size</span></span>  

<span data-ttu-id="45940-121">Dies ist die Größe des Arbeitsspeichers, der vom Objekt gehalten wird.</span><span class="sxs-lookup"><span data-stu-id="45940-121">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="45940-122">Bei typischen JavaScript-Objekten ist etwas Arbeitsspeicher für die Beschreibung und das Speichern von unmittelbaren Werten reserviert.</span><span class="sxs-lookup"><span data-stu-id="45940-122">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="45940-123">In der Regel können nur Arrays und Zeichenfolgen eine erhebliche flache Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="45940-123">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="45940-124">Zeichenfolgen und externe Arrays verfügen jedoch häufig über ihren Hauptspeicher im Rendererspeicher, was nur ein kleines Wrapperobjekt im JavaScript-Heap verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="45940-124">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="45940-125">Rendererspeicher ist der ganze Speicher des Prozesses, in dem eine überprüfte Seite gerendert wird: systemeigener Speicher + JS-Heapspeicher der Seite + JS-Heapspeicher aller dedizierten Mitarbeiter, die von der Seite gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="45940-125">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="45940-126">Dennoch kann selbst ein kleines Objekt indirekt einen großen Speicher enthalten, indem verhindert wird, dass andere Objekte durch den automatischen Garbage Collection-Prozess verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="45940-126">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <a name="retained-size"></a><span data-ttu-id="45940-127">Beibehaltene Größe</span><span class="sxs-lookup"><span data-stu-id="45940-127">Retained size</span></span>  

<span data-ttu-id="45940-128">Dies ist die Größe des Arbeitsspeichers, der freigegeben wird, nachdem das Objekt gelöscht wurde, zusammen mit den abhängigen Objekten, die aus Garbage Collector-Ursprüngen nicht erreichbar **gemacht wurden.**</span><span class="sxs-lookup"><span data-stu-id="45940-128">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots**.</span></span>  

<span data-ttu-id="45940-129">**Garbage Collector-Ursprünge** werden \*\*\*\* aus Handles erstellt, die \(entweder lokal oder global\) erstellt werden, wenn ein Verweis aus systemeigenem Code auf ein JavaScript-Objekt außerhalb von V8 erfolgt.</span><span class="sxs-lookup"><span data-stu-id="45940-129">**Garbage Collector roots** are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="45940-130">Alle diese Handles finden Sie in einer Heapmomentaufnahme unter **GC roots**  >  **Handle scope** und GC **roots**  >  **Global handles**.</span><span class="sxs-lookup"><span data-stu-id="45940-130">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="45940-131">Die Beschreibung der Handles in dieser Dokumentation, ohne details zur Browserimplementierung zu machen, kann verwirrend sein.</span><span class="sxs-lookup"><span data-stu-id="45940-131">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="45940-132">Sowohl garbage collector roots als auch die Handles müssen Sie sich keine Sorgen machen.</span><span class="sxs-lookup"><span data-stu-id="45940-132">Both Garbage Collector roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="45940-133">Es gibt viele interne Garbage Collector-Ursprünge, von denen die meisten für die Benutzer nicht interessant sind.</span><span class="sxs-lookup"><span data-stu-id="45940-133">There are lots of internal Garbage Collector roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="45940-134">Aus Der Sicht der Anwendungen gibt es folgende Arten von Ursprüngen.</span><span class="sxs-lookup"><span data-stu-id="45940-134">From the applications standpoint there are following kinds of roots.</span></span>  

*   <span data-ttu-id="45940-135">Window global object \(in each iframe\).</span><span class="sxs-lookup"><span data-stu-id="45940-135">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="45940-136">In den Heapmomentaufnahmen ist ein Abstandsfeld enthalten, das die Anzahl der Eigenschaftsverweise auf dem kürzesten Aufbewahrungspfad vom Fenster aus ist.</span><span class="sxs-lookup"><span data-stu-id="45940-136">There is a distance field in the heap snapshots which is the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="45940-137">Dokument-DOM-Struktur, die aus allen systemeigenen DOM-Knoten besteht, die durch Durchlaufen des Dokuments erreichbar sind.</span><span class="sxs-lookup"><span data-stu-id="45940-137">Document DOM tree consisting of all native DOM nodes reachable by traversing the document.</span></span>  <span data-ttu-id="45940-138">Nicht alle Knoten verfügen möglicherweise über JS-Wrapper, aber wenn ein Knoten über einen Wrapper verfügt, ist er lebendig, während das Dokument noch am Leben ist.</span><span class="sxs-lookup"><span data-stu-id="45940-138">Not all of the nodes may have JS wrappers but if a node has a wrapper, it is alive while the document is alive.</span></span>  
*   <span data-ttu-id="45940-139">Manchmal können Objekte im Debuggerkontext im Bereich **Quellen** und in der **Konsole** \(z. B. nach der Konsolenauswertung\) beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="45940-139">Sometimes objects may be retained by the debugger context in the **Sources** panel and the **Console** \(for example after Console evaluation\).</span></span>  <span data-ttu-id="45940-140">Erstellen Sie Heapmomentaufnahmen mit einem geräumten **Konsolenbereich** und keine aktiven Haltepunkte im Debugger im **Bereich** Quellen.</span><span class="sxs-lookup"><span data-stu-id="45940-140">Create heap snapshots with a cleared **Console** panel and no active breakpoints in the debugger in the **Sources** panel.</span></span>

>[!TIP]
> <span data-ttu-id="45940-141">Deaktivieren Sie **den Konsolenbereich,** indem Sie Haltepunkte im Bereich Quellen ausführen und deaktivieren, bevor Sie eine `clear()` \*\*\*\* Heapmomentaufnahme im [Speicherbereich erstellen.][DevtoolsMemoryProblemsHeapSnapshots]</span><span class="sxs-lookup"><span data-stu-id="45940-141">Clear the **Console** panel by running `clear()` and deactivate breakpoints in the **Sources** panel before taking a heap snapshot in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>

<span data-ttu-id="45940-142">Das Speicherdiagramm beginnt mit einem Stamm, der das Objekt des Browsers oder das Objekt eines Node.js `window` `Global` sein kann.</span><span class="sxs-lookup"><span data-stu-id="45940-142">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="45940-143">Sie können nicht steuern, wie dieses Stammobjekt im Garbage Collection-Objekt gesammelt wird.</span><span class="sxs-lookup"><span data-stu-id="45940-143">You do not control how this root object is garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Sie können nicht steuern, wie das Stammobjekt als Garbage Collection erfasst wird." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="45940-145">Sie können nicht steuern, wie das Stammobjekt als Garbage Collection erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="45940-145">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="45940-146">Was vom Stamm aus nicht erreichbar ist, wird garbage collected.</span><span class="sxs-lookup"><span data-stu-id="45940-146">Whatever is not reachable from the root gets garbage collected.</span></span>  

> [!NOTE]
> <span data-ttu-id="45940-147">Sowohl die [Spalten "Flache Größe"](#shallow-size) [als auch "Beibehaltene Größe"](#retained-size) stellen Daten in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="45940-147">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <a name="objects-retaining-tree"></a><span data-ttu-id="45940-148">Aufbewahrungsstruktur für Objekte</span><span class="sxs-lookup"><span data-stu-id="45940-148">Objects retaining tree</span></span>  

<span data-ttu-id="45940-149">Der Heap ist ein Netzwerk von miteinander verbundenen Objekten.</span><span class="sxs-lookup"><span data-stu-id="45940-149">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="45940-150">In der mathematischen Welt wird diese Struktur als Diagramm **oder** Speicherdiagramm bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="45940-150">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="45940-151">Ein Diagramm wird aus Knoten **erstellt,** die über Kanten verbunden **sind,** die beide Beschriftungen erhalten.</span><span class="sxs-lookup"><span data-stu-id="45940-151">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="45940-152">**Knoten** \(oder **Objekte**\) werden mit \*\*\*\* dem Namen der Konstruktorfunktion gekennzeichnet, die zum Erstellen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="45940-152">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="45940-153">**Kanten** werden mit den Namen von Eigenschaften **gekennzeichnet.**</span><span class="sxs-lookup"><span data-stu-id="45940-153">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="45940-154">Erfahren [Sie, wie Sie ein Profil mit dem Heap Profiler aufzeichnen.][DevtoolsMemoryProblemsHeapSnapshots]</span><span class="sxs-lookup"><span data-stu-id="45940-154">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="45940-155">In der folgenden Abbildung sind einige der wichtigsten Dinge in der Heap Snapshot-Aufzeichnung im [Tool Speicher][DevtoolsMemoryProblemsHeapSnapshots] enthalten: der Abstand zum Garbage Collector-Stamm.</span><span class="sxs-lookup"><span data-stu-id="45940-155">In the following figure, some of the notable things in the Heap Snapshot recording in the [Memory][DevtoolsMemoryProblemsHeapSnapshots] tool include distance:  the distance from the Garbage Collector root.</span></span>  <span data-ttu-id="45940-156">Wenn sich fast alle Objekte desselben Typs in derselben Entfernung befinden und einige wenige sich in größerer Entfernung befinden, ist dies eine Untersuchung wert.</span><span class="sxs-lookup"><span data-stu-id="45940-156">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Abstand zum Stamm" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="45940-158">Abstand zum Stamm</span><span class="sxs-lookup"><span data-stu-id="45940-158">Distance from root</span></span>  
:::image-end:::  

## <a name="dominators"></a><span data-ttu-id="45940-159">Dominante</span><span class="sxs-lookup"><span data-stu-id="45940-159">Dominators</span></span>  

<span data-ttu-id="45940-160">Dominantor-Objekte bestehen aus einer Strukturstruktur, da jedes Objekt über genau einen Dominanter verfügt.</span><span class="sxs-lookup"><span data-stu-id="45940-160">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="45940-161">Einem #A0 eines Objekts fehlen möglicherweise direkte Verweise auf ein objekt, das es überragt. Das heißt, die Struktur des Dominantors ist keine spannende Struktur des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="45940-161">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="45940-162">In der folgenden Abbildung ist die folgende Anweisung true.</span><span class="sxs-lookup"><span data-stu-id="45940-162">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="45940-163">Knoten 1 überwiegen Knoten 2</span><span class="sxs-lookup"><span data-stu-id="45940-163">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="45940-164">Knoten 2 überwiegen die Knoten 3, 4 und 6</span><span class="sxs-lookup"><span data-stu-id="45940-164">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="45940-165">Knoten 3 überwiegen Knoten 5</span><span class="sxs-lookup"><span data-stu-id="45940-165">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="45940-166">Knoten 5 überwiegen Knoten 8</span><span class="sxs-lookup"><span data-stu-id="45940-166">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="45940-167">Knoten 6 überwiegen Knoten 7</span><span class="sxs-lookup"><span data-stu-id="45940-167">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Struktur der dominanten Struktur" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="45940-169">Struktur der dominanten Struktur</span><span class="sxs-lookup"><span data-stu-id="45940-169">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="45940-170">In der folgenden Abbildung ist Knoten der Dominante von , ist aber auch in jedem einfachen Pfad von `#3` `#10` Garbage Collector zu `#7` `#10` vorhanden.</span><span class="sxs-lookup"><span data-stu-id="45940-170">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector to `#10`.</span></span>  <span data-ttu-id="45940-171">Daher ist ein Objekt B ein Dominanter eines Objekts A, wenn B in jedem einfachen Pfad vom Stamm zum Objekt A vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="45940-171">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Animierte Dominantor-Illustration" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="45940-173">Animierte Dominantor-Illustration</span><span class="sxs-lookup"><span data-stu-id="45940-173">Animated dominator illustration</span></span>  
:::image-end:::  

## <a name="v8-specifics"></a><span data-ttu-id="45940-174">V8-Spezifische</span><span class="sxs-lookup"><span data-stu-id="45940-174">V8 specifics</span></span>  

<span data-ttu-id="45940-175">Beim Profilerstellungsspeicher ist es hilfreich zu verstehen, warum Heapmomentaufnahmen auf eine bestimmte Weise aussehen.</span><span class="sxs-lookup"><span data-stu-id="45940-175">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="45940-176">In diesem Abschnitt werden einige Speicherthemen beschrieben, die speziell dem **virtuellen V8-JavaScript-Computer** \(V8 VM oder VM\) zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="45940-176">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <a name="javascript-object-representation"></a><span data-ttu-id="45940-177">JavaScript-Objektdarstellung</span><span class="sxs-lookup"><span data-stu-id="45940-177">JavaScript object representation</span></span>  

<span data-ttu-id="45940-178">Es gibt drei Grundtypen:</span><span class="sxs-lookup"><span data-stu-id="45940-178">There are three primitive types:</span></span>  

*   <span data-ttu-id="45940-179">Zahlen \(z. B. `3.14159...` \)</span><span class="sxs-lookup"><span data-stu-id="45940-179">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="45940-180">Booleans \( `true` oder `false` \)</span><span class="sxs-lookup"><span data-stu-id="45940-180">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="45940-181">Zeichenfolgen \(z. B. `"Werner Heisenberg"` \)</span><span class="sxs-lookup"><span data-stu-id="45940-181">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="45940-182">Grundtypen können nicht auf andere Werte verweisen und sind immer Blatt- oder Endknoten.</span><span class="sxs-lookup"><span data-stu-id="45940-182">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="45940-183">**Zahlen** können wie folgt gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="45940-183">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="45940-184">ein sofortiger ganzzahliger 31-Bit-Wert, der als **kleine ganze Zahlen** \(**SMI**s\) bezeichnet wird, oder</span><span class="sxs-lookup"><span data-stu-id="45940-184">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="45940-185">Heapobjekte, die als **Heapnummern bezeichnet werden.**</span><span class="sxs-lookup"><span data-stu-id="45940-185">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="45940-186">Heapnummern werden zum Speichern von Werten verwendet, die nicht in das SMI-Formular passen, z. B. **Doubles**oder wenn ein Wert geschachtelt werden **muss,** z. B. festlegen von Eigenschaften darauf.</span><span class="sxs-lookup"><span data-stu-id="45940-186">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="45940-187">**Zeichenfolgen** können in einer der beiden Dateien gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="45940-187">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="45940-188">der **VM-Heap**oder</span><span class="sxs-lookup"><span data-stu-id="45940-188">the **VM heap**, or</span></span>
*   <span data-ttu-id="45940-189">extern im **Speicher des Renderers**.</span><span class="sxs-lookup"><span data-stu-id="45940-189">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="45940-190">Ein **Wrapperobjekt** wird erstellt und für den Zugriff auf externen Speicher verwendet, in dem beispielsweise Skriptquellen und andere Inhalte gespeichert werden, die aus dem Web empfangen werden, anstatt in den VM-Heap kopiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="45940-190">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="45940-191">Der Arbeitsspeicher für neue JavaScript-Objekte wird über einen dedizierten JavaScript-Heap \(oder **VM-Heap\)** zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="45940-191">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="45940-192">Diese Objekte werden vom Garbage Collector in V8 verwaltet und bleiben daher am Leben, solange mindestens ein starker Verweis darauf besteht.</span><span class="sxs-lookup"><span data-stu-id="45940-192">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="45940-193">Alles, was sich nicht im JavaScript-Heap befindet, wird als **systemeigenes Objekt bezeichnet.**</span><span class="sxs-lookup"><span data-stu-id="45940-193">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="45940-194">Systemeigene Objekte werden im Gegensatz zu Heapobjekten nicht während ihrer gesamten Lebensdauer vom V8-Garbage Collector verwaltet und können nur über JavaScript mithilfe des JavaScript-Wrapperobjekts zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="45940-194">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="45940-195">**Cons string** ist ein Objekt, das aus Paaren von Zeichenfolgen besteht, die gespeichert und dann verbunden werden, und ist ein Ergebnis der Verkettung.</span><span class="sxs-lookup"><span data-stu-id="45940-195">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="45940-196">Die Verbindung der **Inhalte der Cons-Zeichenfolge** erfolgt nur nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="45940-196">The joining of the **cons string** contents occurs only as needed.</span></span>  <span data-ttu-id="45940-197">Wenn z. B. eine Teilzeichenfolge einer angeschlossenen Zeichenfolge erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="45940-197">For example, when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="45940-198">Wenn Sie z. B. und verketten, erhalten Sie eine Zeichenfolge, die das Ergebnis der `a` `b` `(a, b)` Verkettung darstellt.</span><span class="sxs-lookup"><span data-stu-id="45940-198">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="45940-199">Wenn Sie später mit diesem Ergebnis `d` verkettet sind, erhalten Sie eine weitere **Cons-Zeichenfolge:** `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="45940-199">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="45940-200">**Array** ist ein Objekt mit numerischen Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="45940-200">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="45940-201">**Arrays** werden in der V8 VM umfassend zum Speichern großer Datenmengen verwendet.</span><span class="sxs-lookup"><span data-stu-id="45940-201">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="45940-202">Sätze von Schlüssel-Wert-Paaren, z. B. Wörterbücher, werden durch **Arrays gesichert.**</span><span class="sxs-lookup"><span data-stu-id="45940-202">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="45940-203">Ein typisches JavaScript-Objekt wird nur als einer von zwei **Arraytypen** gespeichert:</span><span class="sxs-lookup"><span data-stu-id="45940-203">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="45940-204">benannte Eigenschaften und</span><span class="sxs-lookup"><span data-stu-id="45940-204">named properties, and</span></span>  
*   <span data-ttu-id="45940-205">numerische Elemente</span><span class="sxs-lookup"><span data-stu-id="45940-205">numeric elements</span></span>  

<span data-ttu-id="45940-206">Bei einer kleinen Anzahl von Eigenschaften werden die Eigenschaften intern im JavaScript-Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="45940-206">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="45940-207">**Map** ist ein Objekt, das sowohl den Objekttyp als auch das Layout beschreibt.</span><span class="sxs-lookup"><span data-stu-id="45940-207">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="45940-208">Beispielsweise werden Karten verwendet, um implizite Objekthierarchien für den [schnellen Eigenschaftenzugriff zu beschreiben.][V8FastProperties]</span><span class="sxs-lookup"><span data-stu-id="45940-208">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <a name="object-groups"></a><span data-ttu-id="45940-209">Objektgruppen</span><span class="sxs-lookup"><span data-stu-id="45940-209">Object groups</span></span>  

<span data-ttu-id="45940-210">Jede **systemeigene Objektgruppe** besteht aus Objekten, die gegenseitige Verweise aufeinander enthalten.</span><span class="sxs-lookup"><span data-stu-id="45940-210">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="45940-211">Stellen Sie sich beispielsweise eine DOM-Unterstruktur vor, in der jeder Knoten eine Verknüpfung zum relativen übergeordneten Element und Links zum nächsten untergeordneten und nächsten gleichgeordneten Element hat und daher ein verbundenes Diagramm bildet.</span><span class="sxs-lookup"><span data-stu-id="45940-211">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="45940-212">Systemeigene Objekte werden nicht im JavaScript-Heap dargestellt.</span><span class="sxs-lookup"><span data-stu-id="45940-212">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="45940-213">Die fehlende Darstellung ist der Grund, warum systemeigene Objekte die Größe Null haben.</span><span class="sxs-lookup"><span data-stu-id="45940-213">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="45940-214">Stattdessen werden Wrapperobjekte erstellt.</span><span class="sxs-lookup"><span data-stu-id="45940-214">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="45940-215">Jedes Wrapperobjekt enthält einen Verweis auf das entsprechende systemeigene Objekt zum Umleiten von Befehlen an dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="45940-215">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="45940-216">Eine Objektgruppe enthält wiederum Wrapperobjekte.</span><span class="sxs-lookup"><span data-stu-id="45940-216">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="45940-217">Dadurch wird jedoch kein unkollektierbarer Zyklus erstellt, da Garbage Collector intelligent genug ist, um Objektgruppen frei zu lassen, auf deren Wrapper nicht mehr verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="45940-217">However, this does not create an uncollectable cycle, as Garbage Collector is smart enough to release object groups whose wrappers are no longer referenced.</span></span>  <span data-ttu-id="45940-218">Vergessen sie jedoch, einen einzelnen Wrapper zu veröffentlichen, enthält die gesamte Gruppe und die zugehörigen Wrapper.</span><span class="sxs-lookup"><span data-stu-id="45940-218">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="45940-219">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="45940-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Aufzeichnen von Heapmomentaufnahmen | Microsoft Docs"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Schnelle Eigenschaften in V8-| V8"  

> [!NOTE]
> <span data-ttu-id="45940-222">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45940-222">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="45940-223">Die ursprüngliche Seite befindet sich [hier und](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) wird von [Meggin Kearney][MegginKearney] \(Technical Writer\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="45940-223">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="45940-225">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="45940-225">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney

---
title: Speicher Terminologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: cb258135b7b3c931116d84b1e9b7a548a2b58a6d
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986251"
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

# <span data-ttu-id="7f32d-103">Speicher Terminologie</span><span class="sxs-lookup"><span data-stu-id="7f32d-103">Memory Terminology</span></span>  

<span data-ttu-id="7f32d-104">In diesem Abschnitt werden allgemeine Ausdrücke beschrieben, die in der Speicheranalyse verwendet werden, und Sie gelten für eine Vielzahl von Arbeitsspeicherprofil Tools für verschiedene Sprachen.</span><span class="sxs-lookup"><span data-stu-id="7f32d-104">This section describes common terms used in memory analysis, and is applicable to a variety of memory profiling tools for different languages.</span></span>  

<span data-ttu-id="7f32d-105">Die hier beschriebenen Begriffe und Begriffe beziehen sich auf das [Speicher Panel][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="7f32d-105">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="7f32d-106">Wenn Sie jemals mit dem Java-, .net-oder einem anderen Speicher Profiler gearbeitet haben, ist dies möglicherweise eine Auffrischung.</span><span class="sxs-lookup"><span data-stu-id="7f32d-106">If you have ever worked with either the Java, .NET, or some other memory profiler, then this may be a refresher.</span></span>  

## <span data-ttu-id="7f32d-107">Objektgrößen</span><span class="sxs-lookup"><span data-stu-id="7f32d-107">Object sizes</span></span>  

<span data-ttu-id="7f32d-108">Denken Sie an Arbeitsspeicher als ein Diagramm mit primitiven Typen \ (wie Zahlen und Zeichenfolgen \) und Objekten \ (assoziative Arrays \).</span><span class="sxs-lookup"><span data-stu-id="7f32d-108">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="7f32d-109">Sie wird möglicherweise visuell als Diagramm mit einer Reihe von miteinander verbundenen Punkten wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="7f32d-109">It might visually be represented as a graph with a number of interconnected points as follows:</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Visuelle Darstellung des Arbeitsspeichers" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="7f32d-111">Visuelle Darstellung des Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="7f32d-111">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="7f32d-112">Ein Objekt kann Speicher auf zwei Arten enthalten:</span><span class="sxs-lookup"><span data-stu-id="7f32d-112">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="7f32d-113">Direkt vom Objekt.</span><span class="sxs-lookup"><span data-stu-id="7f32d-113">Directly by the object.</span></span>  
*   <span data-ttu-id="7f32d-114">Implizit durch Speichern von Verweisen auf andere Objekte, wodurch verhindert wird, dass diese Objekte automatisch von einem Garbage Collector entfernt werden \ (**GC** für Short \).</span><span class="sxs-lookup"><span data-stu-id="7f32d-114">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector \(**GC** for short\).</span></span>  

<span data-ttu-id="7f32d-115">Bei der Arbeit mit dem [Speicher][DevtoolsMemoryProblemsHeapSnapshots] Bereich in devtools \ (ein Tool zur Untersuchung von Speicherproblemen, die unter " **Arbeits**Speicher" gefunden wurden) finden Sie möglicherweise einige verschiedene Informationsspalten.</span><span class="sxs-lookup"><span data-stu-id="7f32d-115">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="7f32d-116">Zwei, die sich hervorheben, sind eine **flache Größe** und eine **Beibehaltungs Größe**, doch was stellen diese dar?</span><span class="sxs-lookup"><span data-stu-id="7f32d-116">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Flache und gespeicherte Größe" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="7f32d-118">Flache und gespeicherte Größe</span><span class="sxs-lookup"><span data-stu-id="7f32d-118">Shallow and Retained Size</span></span>  
:::image-end:::  

### <span data-ttu-id="7f32d-119">Flache Größe</span><span class="sxs-lookup"><span data-stu-id="7f32d-119">Shallow size</span></span>  

<span data-ttu-id="7f32d-120">Dies ist die Größe des Speichers, der vom Objekt gehalten wird.</span><span class="sxs-lookup"><span data-stu-id="7f32d-120">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="7f32d-121">Typische JavaScript-Objekte verfügen über einen Speicherplatz, der für die Beschreibung reserviert ist, und zum Speichern unmittelbarer Werte.</span><span class="sxs-lookup"><span data-stu-id="7f32d-121">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="7f32d-122">In der Regel können nur Arrays und Zeichenfolgen eine beträchtliche flache Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7f32d-122">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="7f32d-123">Zeichenfolgen und externe Arrays verfügen jedoch häufig über Ihren Hauptspeicher im rendererspeicher, wodurch nur ein kleines Wrapperobjekt auf dem JavaScript-Heap verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="7f32d-123">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="7f32d-124">Der Renderer-Arbeitsspeicher ist der gesamte Arbeitsspeicher des Prozesses, in dem eine geprüfte Seite gerendert wird: nativer Arbeitsspeicher + js-Heapspeicher des Page + js-Heapspeichers aller dedizierten Arbeitskräfte, die von der Seite gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="7f32d-124">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="7f32d-125">Dennoch kann selbst ein kleines Objekt eine große Menge an Arbeitsspeicher indirekt aufnehmen, indem verhindert wird, dass andere Objekte vom automatischen Garbage Collection-Prozess verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="7f32d-125">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <span data-ttu-id="7f32d-126">Beibehaltungs Größe</span><span class="sxs-lookup"><span data-stu-id="7f32d-126">Retained size</span></span>  

<span data-ttu-id="7f32d-127">Hierbei handelt es sich um die Größe des Arbeitsspeichers, der freigegeben wird, sobald das Objekt zusammen mit den abhängigen Objekten gelöscht wird, die aus den **Garbage Collector-Stämmen** (GC-Stämme \) nicht erreichbar sind.</span><span class="sxs-lookup"><span data-stu-id="7f32d-127">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots** \(GC roots\) .</span></span>  

<span data-ttu-id="7f32d-128">**Garbage Collector-Stämme** \ (GC-Stämme \) bestehen aus **Handles** , die \ (entweder lokal oder Global \) erstellt werden, wenn Sie einen Verweis vom systemeigenen Code auf ein JavaScript-Objekt außerhalb von V8 erstellen.</span><span class="sxs-lookup"><span data-stu-id="7f32d-128">**Garbage Collector roots** \(GC roots\) are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="7f32d-129">Alle derartigen Handles befinden sich möglicherweise in einem Heap-Snapshot unter **GC-Roots**  >  -**Handles** und globalen **GC-Stamm**  >  **Handles**.</span><span class="sxs-lookup"><span data-stu-id="7f32d-129">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="7f32d-130">Die Beschreibung der Handles in dieser Dokumentation, ohne die Details der Browser Implementierung zu untertauchen, ist möglicherweise verwirrend.</span><span class="sxs-lookup"><span data-stu-id="7f32d-130">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="7f32d-131">Sowohl Garbage Collector (GC)-Stämme als auch die Ziehpunkte sind keine Grund zur Sorge.</span><span class="sxs-lookup"><span data-stu-id="7f32d-131">Both Garbage Collector (GC) roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="7f32d-132">Es gibt viele interne GC-Stämme, von denen die meisten nicht für die Benutzer interessant sind.</span><span class="sxs-lookup"><span data-stu-id="7f32d-132">There are lots of internal GC roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="7f32d-133">Aus Sicht der Anwendungen gibt es folgende Arten von Stämmen:</span><span class="sxs-lookup"><span data-stu-id="7f32d-133">From the applications standpoint there are following kinds of roots.</span></span>  

*   <span data-ttu-id="7f32d-134">Globales Window-Objekt \ (in jedem IFRAME \).</span><span class="sxs-lookup"><span data-stu-id="7f32d-134">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="7f32d-135">In den Heap-Schnappschüssen gibt es ein Entfernungs Feld, bei dem es sich um die Anzahl der Eigenschaftsverweise auf dem kürzesten Beibehaltungs Pfad aus dem Fenster handelt.</span><span class="sxs-lookup"><span data-stu-id="7f32d-135">There is a distance field in the heap snapshots which is the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="7f32d-136">Dokument-DOM-Struktur, bestehend aus allen systemeigenen DOM-Knoten, die durch Durchlaufen des Dokuments erreichbar sind.</span><span class="sxs-lookup"><span data-stu-id="7f32d-136">Document DOM tree consisting of all native DOM nodes reachable by traversing the document.</span></span>  <span data-ttu-id="7f32d-137">Nicht alle Knoten können js-Wrapper aufweisen, aber wenn ein Knoten über einen Wrapper verfügt, ist er lebendig, während das Dokument aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="7f32d-137">Not all of the nodes may have JS wrappers but if a node has a wrapper, it is alive while the document is alive.</span></span>  
*   <span data-ttu-id="7f32d-138">Manchmal werden Objekte im Debugger-Kontext im **Quellen** Panel und in der **Konsole** (beispielsweise nach der Konsolen Auswertung \) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7f32d-138">Sometimes objects may be retained by the debugger context in the **Sources** panel and the **Console** \(for example after Console evaluation\).</span></span>  <span data-ttu-id="7f32d-139">Erstellen Sie Heap-Schnappschüsse mit einem gelöschten **Konsolen** Panel und keine aktiven Haltepunkte im Debugger im **Quellen** Panel.</span><span class="sxs-lookup"><span data-stu-id="7f32d-139">Create heap snapshots with a cleared **Console** panel and no active breakpoints in the debugger in the **Sources** panel.</span></span>

>[!TIP]
> <span data-ttu-id="7f32d-140">Deaktivieren Sie die **Konsolen** Leiste, indem Sie die `clear()` Haltepunkte im **Quellen** Panel ausführen und deaktivieren, bevor Sie einen Heap-Schnappschuss im [Speicher Panel][DevtoolsMemoryProblemsHeapSnapshots]aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="7f32d-140">Clear the **Console** panel by running `clear()` and deactivate breakpoints in the **Sources** panel before taking a heap snapshot in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>

<span data-ttu-id="7f32d-141">Der Speicher Graph beginnt mit einem Stamm, der das Objekt des `window` Browsers oder das `Global` Objekt eines Node.js Moduls sein kann.</span><span class="sxs-lookup"><span data-stu-id="7f32d-141">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="7f32d-142">Sie steuern nicht, wie dieses Stammobjekt Garbage Collection (GGT) ist.</span><span class="sxs-lookup"><span data-stu-id="7f32d-142">You do not control how this root object is garbage collected (GCd).</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Sie können nicht steuern, wie das Stammobjekt als Garbage Collection erfasst wird." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="7f32d-144">Sie können nicht steuern, wie das Stammobjekt als Garbage Collection erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="7f32d-144">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="7f32d-145">Was nicht über den Stamm erreichbar ist, erhält Garbage Collection \ (GGT \).</span><span class="sxs-lookup"><span data-stu-id="7f32d-145">Whatever is not reachable from the root gets garbage collected \(GCd\).</span></span>  

> [!NOTE]
> <span data-ttu-id="7f32d-146">Die Spalten " [flache Größe](#shallow-size) " und " [Größe beibehalten](#retained-size) " stellen Daten in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="7f32d-146">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <span data-ttu-id="7f32d-147">Objekte, die die Struktur beibehalten</span><span class="sxs-lookup"><span data-stu-id="7f32d-147">Objects retaining tree</span></span>  

<span data-ttu-id="7f32d-148">Der Heap ist ein Netzwerk von miteinander verbundenen Objekten.</span><span class="sxs-lookup"><span data-stu-id="7f32d-148">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="7f32d-149">In der mathematischen Welt wird diese Struktur als **Diagramm** oder Speicher Diagramm bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7f32d-149">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="7f32d-150">Ein Diagramm wird aus **Knoten** erstellt, die über **Kanten**verbunden sind, wobei beide Bezeichnungen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7f32d-150">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="7f32d-151">**Knoten** \ (oder **Objekte**\) werden mit dem Namen der **Konstruktorfunktion** gekennzeichnet, die zum Erstellen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7f32d-151">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="7f32d-152">**Kanten** werden mit den Namen der **Eigenschaften**gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7f32d-152">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="7f32d-153">Erfahren Sie [, wie Sie ein Profil mit dem Heap Profiler aufzeichnen][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="7f32d-153">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="7f32d-154">In der folgenden Abbildung sind einige der auffälligen Dinge, die bei der Aufzeichnung des Heap-Schnappschusses im [Speicher Panel][DevtoolsMemoryProblemsHeapSnapshots] angezeigt werden können, Distance: der Abstand vom Garbage Collector \ (GC \)-Stammverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7f32d-154">In the following figure, some of the eye-catching things that you may see in the Heap Snapshot recording in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots] include distance:  the distance from the Garbage Collector \(GC\) root.</span></span>  <span data-ttu-id="7f32d-155">Wenn sich fast alle Objekte desselben Typs im gleichen Abstand befinden und einige wenige in größerer Entfernung sind, ist das eine Untersuchung Wert.</span><span class="sxs-lookup"><span data-stu-id="7f32d-155">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Abstand vom Stamm" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="7f32d-157">Abstand vom Stamm</span><span class="sxs-lookup"><span data-stu-id="7f32d-157">Distance from root</span></span>  
:::image-end:::  

## <span data-ttu-id="7f32d-158">Dominators</span><span class="sxs-lookup"><span data-stu-id="7f32d-158">Dominators</span></span>  

<span data-ttu-id="7f32d-159">Dominator-Objekte bestehen aus einer Struktur, da jedes Objekt genau einen Dominator hat.</span><span class="sxs-lookup"><span data-stu-id="7f32d-159">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="7f32d-160">Ein Dominator eines Objekts kann keine direkten Bezüge auf ein Objekt aufweisen, das es dominiert; Das bedeutet, dass die Struktur des Dominators keine Spanning-Struktur des Diagramms ist.</span><span class="sxs-lookup"><span data-stu-id="7f32d-160">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="7f32d-161">In der folgenden Abbildung ist die folgende Anweisung wahr.</span><span class="sxs-lookup"><span data-stu-id="7f32d-161">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="7f32d-162">Knoten 1 dominiert Knoten 2</span><span class="sxs-lookup"><span data-stu-id="7f32d-162">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="7f32d-163">Knoten 2 dominiert die Knoten 3, 4 und 6</span><span class="sxs-lookup"><span data-stu-id="7f32d-163">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="7f32d-164">Knoten 3 dominiert Knoten 5</span><span class="sxs-lookup"><span data-stu-id="7f32d-164">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="7f32d-165">Knoten 5 dominiert Knoten 8</span><span class="sxs-lookup"><span data-stu-id="7f32d-165">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="7f32d-166">Knoten 6 dominiert Knoten 7</span><span class="sxs-lookup"><span data-stu-id="7f32d-166">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Struktur des Dominators" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="7f32d-168">Struktur des Dominators</span><span class="sxs-lookup"><span data-stu-id="7f32d-168">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="7f32d-169">In der folgenden Abbildung `#3` ist der Knoten der Dominator von `#10` , aber er ist `#7` auch in jedem einfachen Pfad vom Garbage Collector \ (GC \) bis `#10` .</span><span class="sxs-lookup"><span data-stu-id="7f32d-169">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector \(GC\) to `#10`.</span></span>  <span data-ttu-id="7f32d-170">Daher ist ein Objekt b ein Dominator eines Objekts a, wenn b in jedem einfachen Pfad vom Stamm zum Objekt a vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7f32d-170">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Animierte Dominator-Illustration" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="7f32d-172">Animierte Dominator-Illustration</span><span class="sxs-lookup"><span data-stu-id="7f32d-172">Animated dominator illustration</span></span>  
:::image-end:::  

## <span data-ttu-id="7f32d-173">V8-Besonderheiten</span><span class="sxs-lookup"><span data-stu-id="7f32d-173">V8 specifics</span></span>  

<span data-ttu-id="7f32d-174">Bei der Profilerstellung von Arbeitsspeicher ist es hilfreich zu verstehen, warum Heap Momentaufnahmen auf eine bestimmte Weise aussehen.</span><span class="sxs-lookup"><span data-stu-id="7f32d-174">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="7f32d-175">In diesem Abschnitt werden einige speicherbezogene Themen beschrieben, die speziell der **virtuellen V8-JavaScript-Maschine** \ (V8 VM oder VM \) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7f32d-175">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <span data-ttu-id="7f32d-176">JavaScript-Objektdarstellung</span><span class="sxs-lookup"><span data-stu-id="7f32d-176">JavaScript object representation</span></span>  

<span data-ttu-id="7f32d-177">Es gibt drei primitive Typen:</span><span class="sxs-lookup"><span data-stu-id="7f32d-177">There are three primitive types:</span></span>  

*   <span data-ttu-id="7f32d-178">Zahlen \ (Beispiel `3.14159...` : \)</span><span class="sxs-lookup"><span data-stu-id="7f32d-178">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="7f32d-179">Boolesche Werte \ ( `true` oder `false` \)</span><span class="sxs-lookup"><span data-stu-id="7f32d-179">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="7f32d-180">Zeichenfolgen \ (Beispiel `"Werner Heisenberg"` : \)</span><span class="sxs-lookup"><span data-stu-id="7f32d-180">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="7f32d-181">Primitive können nicht auf andere Werte verweisen und sind immer Blatt-oder Endpunkt Knoten.</span><span class="sxs-lookup"><span data-stu-id="7f32d-181">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="7f32d-182">**Nummern** können entweder wie folgt gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="7f32d-182">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="7f32d-183">eine direkte 31-Bit-Ganzzahl, die als **kleine ganze Zahlen** (**SMI**s \) bezeichnet wird, oder</span><span class="sxs-lookup"><span data-stu-id="7f32d-183">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="7f32d-184">Heap-Objekte, die als **Heap-Nummern**bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="7f32d-184">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="7f32d-185">Heap-Nummern werden zum Speichern von Werten verwendet, die nicht in das SMI-Formular passen, wie etwa **Doubles**, oder wenn ein Wert **geschachtelt**werden muss, wie beispielsweise das Festlegen von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7f32d-185">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="7f32d-186">**Zeichenfolgen** können entweder in folgendem gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="7f32d-186">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="7f32d-187">der **VM-Heap**oder</span><span class="sxs-lookup"><span data-stu-id="7f32d-187">the **VM heap**, or</span></span>
*   <span data-ttu-id="7f32d-188">extern im **Speicher des Renderers**.</span><span class="sxs-lookup"><span data-stu-id="7f32d-188">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="7f32d-189">Ein **Wrapperobjekt** wird erstellt und für den Zugriff auf externen Speicher verwendet, wenn beispielsweise Skript Quellen und andere Inhalte, die aus dem Web empfangen werden, gespeichert werden, anstatt auf den VM-Heap kopiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="7f32d-189">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="7f32d-190">Der Arbeitsspeicher für neue JavaScript-Objekte wird von einem dedizierten JavaScript-Heap zugeordnet \ (oder **VM-Heap**\).</span><span class="sxs-lookup"><span data-stu-id="7f32d-190">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="7f32d-191">Diese Objekte werden vom Garbage Collector in V8 verwaltet und bleiben daher so lange am Leben, wie es mindestens einen starken Bezug auf Sie gibt.</span><span class="sxs-lookup"><span data-stu-id="7f32d-191">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="7f32d-192">Alles, was sich nicht im JavaScript-Heap befindet, wird als **systemeigenes Objekt**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7f32d-192">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="7f32d-193">Systemeigene Objekte werden im Gegensatz zu Heap Objekten nicht vom V8-Garbage Collector während ihrer gesamten Lebensdauer verwaltet und können nur über JavaScript mit dem JavaScript-Wrapperobjekt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7f32d-193">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="7f32d-194">**Cons String** ist ein Objekt, das aus Paaren von Zeichenfolgen besteht, die gespeichert und dann verknüpft sind und ein Ergebnis der Verkettung sind.</span><span class="sxs-lookup"><span data-stu-id="7f32d-194">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="7f32d-195">Die Verknüpfung des **Cons-Zeichenfolgen** Inhalts erfolgt nur bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="7f32d-195">The joining of the **cons string** contents occurs only as needed.</span></span> <span data-ttu-id="7f32d-196">Ein Beispiel wäre, wenn eine Teilzeichenfolge einer verknüpften Zeichenfolge erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="7f32d-196">An example would be when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="7f32d-197">Wenn Sie beispielsweise verketten `a` und `b` erhalten Sie eine Zeichenfolge, die `(a, b)` das Ergebnis der Verkettung darstellt.</span><span class="sxs-lookup"><span data-stu-id="7f32d-197">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="7f32d-198">Wenn Sie später `d` mit diesem Ergebnis verkettet haben, erhalten Sie eine weitere **Cons-Zeichenfolge**: `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="7f32d-198">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="7f32d-199">**Matrix** ist ein Objekt mit numerischen Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="7f32d-199">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="7f32d-200">**Arrays** werden in der V8-VM umfassend verwendet, um große Datenmengen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7f32d-200">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="7f32d-201">Sätze von Schlüssel-Wert-Paaren, wie Wörterbücher, werden von **Arrays**gesichert.</span><span class="sxs-lookup"><span data-stu-id="7f32d-201">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="7f32d-202">Ein typisches JavaScript-Objekt wird nur als einer von zwei **Array** Typen gespeichert:</span><span class="sxs-lookup"><span data-stu-id="7f32d-202">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="7f32d-203">benannte Eigenschaften und</span><span class="sxs-lookup"><span data-stu-id="7f32d-203">named properties, and</span></span>  
*   <span data-ttu-id="7f32d-204">numerische Elemente</span><span class="sxs-lookup"><span data-stu-id="7f32d-204">numeric elements</span></span>  

<span data-ttu-id="7f32d-205">Wenn eine geringe Anzahl von Eigenschaften vorhanden ist, werden die Eigenschaften intern im JavaScript-Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7f32d-205">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="7f32d-206">**Map** ist ein Objekt, das sowohl die Art des Objekts als auch das Layout beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7f32d-206">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="7f32d-207">Karten werden beispielsweise verwendet, um implizite Objekthierarchien für den [schnellen Eigenschaftenzugriff][V8FastProperties]zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7f32d-207">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <span data-ttu-id="7f32d-208">Objektgruppen</span><span class="sxs-lookup"><span data-stu-id="7f32d-208">Object groups</span></span>  

<span data-ttu-id="7f32d-209">Jede Gruppe **systemeigene Objekte** besteht aus Objekten, die gegenseitige Bezüge aufeinander abhalten.</span><span class="sxs-lookup"><span data-stu-id="7f32d-209">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="7f32d-210">Nehmen Sie beispielsweise eine DOM-Unterstruktur in Frage, bei der jeder Knoten über einen Link zum relativen übergeordneten Element und Links zum nächsten untergeordneten Element und zum nächsten nebengeordneten Element verfügt, wodurch ein verbundenes Diagramm entsteht.</span><span class="sxs-lookup"><span data-stu-id="7f32d-210">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="7f32d-211">Systemeigene Objekte werden nicht im JavaScript-Heap dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7f32d-211">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="7f32d-212">Das Fehlen einer Darstellung ist der Grund dafür, dass systemeigene Objekte die Größe 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7f32d-212">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="7f32d-213">Stattdessen werden Wrapper Objekte erstellt.</span><span class="sxs-lookup"><span data-stu-id="7f32d-213">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="7f32d-214">Jedes Wrapperobjekt enthält einen Verweis auf das entsprechende systemeigene Objekt für die Umleitung von Befehlen an ihn.</span><span class="sxs-lookup"><span data-stu-id="7f32d-214">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="7f32d-215">Eine Objektgruppe enthält wiederum Wrapper Objekte.</span><span class="sxs-lookup"><span data-stu-id="7f32d-215">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="7f32d-216">Dadurch wird jedoch kein nicht sammelbarer Zyklus erstellt, da der Garbage Collector \ (GC \) intelligent genug ist, Objektgruppen freizugeben, deren Wrapper nicht mehr referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="7f32d-216">However, this does not create an uncollectable cycle, as Garbage Collector \(GC\) is smart enough to release object groups whose wrappers are no longer referenced.</span></span> <span data-ttu-id="7f32d-217">Aber zu vergessen, einen einzelnen Wrapper freizugeben, enthält die gesamte Gruppe und zugehörige Wrapper.</span><span class="sxs-lookup"><span data-stu-id="7f32d-217">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <span data-ttu-id="7f32d-218">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="7f32d-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Aufzeichnen von Heap-Snapshots | Microsoft docs"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Fast-Eigenschaften in V8 | V8"  

> [!NOTE]
> <span data-ttu-id="7f32d-221">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f32d-221">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7f32d-222">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) gefunden und von [Meggin Kearney][MegginKearney] (Technical Writer \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="7f32d-222">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="7f32d-224">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7f32d-224">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney

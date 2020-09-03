---
description: In diesem Abschnitt werden allgemeine Ausdrücke beschrieben, die in der Speicheranalyse verwendet werden, und Sie gelten für eine Vielzahl von Arbeitsspeicherprofil Tools für verschiedene Sprachen.
title: Speicher Terminologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 3455b05cf19f3aa5a69de5571ab3a24d5654dfe4
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992750"
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

# <span data-ttu-id="d5a1b-104">Speicher Terminologie</span><span class="sxs-lookup"><span data-stu-id="d5a1b-104">Memory Terminology</span></span>  

<span data-ttu-id="d5a1b-105">In diesem Abschnitt werden allgemeine Ausdrücke beschrieben, die in der Speicheranalyse verwendet werden, und Sie gelten für eine Vielzahl von Arbeitsspeicherprofil Tools für verschiedene Sprachen.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-105">This section describes common terms used in memory analysis, and is applicable to a variety of memory profiling tools for different languages.</span></span>  

<span data-ttu-id="d5a1b-106">Die hier beschriebenen Begriffe und Begriffe beziehen sich auf das [Speicher Panel][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="d5a1b-106">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="d5a1b-107">Wenn Sie jemals mit dem Java-, .net-oder einem anderen Speicher Profiler gearbeitet haben, ist dies möglicherweise eine Auffrischung.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-107">If you have ever worked with either the Java, .NET, or some other memory profiler, then this may be a refresher.</span></span>  

## <span data-ttu-id="d5a1b-108">Objektgrößen</span><span class="sxs-lookup"><span data-stu-id="d5a1b-108">Object sizes</span></span>  

<span data-ttu-id="d5a1b-109">Denken Sie an Arbeitsspeicher als ein Diagramm mit primitiven Typen \ (wie Zahlen und Zeichenfolgen \) und Objekten \ (assoziative Arrays \).</span><span class="sxs-lookup"><span data-stu-id="d5a1b-109">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="d5a1b-110">Sie wird möglicherweise visuell als Diagramm mit einer Reihe von miteinander verbundenen Punkten wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="d5a1b-110">It might visually be represented as a graph with a number of interconnected points as follows:</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Visuelle Darstellung des Arbeitsspeichers" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="d5a1b-112">Visuelle Darstellung des Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="d5a1b-112">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="d5a1b-113">Ein Objekt kann Speicher auf zwei Arten enthalten:</span><span class="sxs-lookup"><span data-stu-id="d5a1b-113">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="d5a1b-114">Direkt vom Objekt.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-114">Directly by the object.</span></span>  
*   <span data-ttu-id="d5a1b-115">Implizit durch Speichern von Verweisen auf andere Objekte, wodurch verhindert wird, dass diese Objekte automatisch von einem Garbage Collector entfernt werden \ (**GC** für Short \).</span><span class="sxs-lookup"><span data-stu-id="d5a1b-115">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector \(**GC** for short\).</span></span>  

<span data-ttu-id="d5a1b-116">Bei der Arbeit mit dem [Speicher][DevtoolsMemoryProblemsHeapSnapshots] Bereich in devtools \ (ein Tool zur Untersuchung von Speicherproblemen, die unter " **Arbeits**Speicher" gefunden wurden) finden Sie möglicherweise einige verschiedene Informationsspalten.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-116">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="d5a1b-117">Zwei, die sich hervorheben, sind eine **flache Größe** und eine **Beibehaltungs Größe**, doch was stellen diese dar?</span><span class="sxs-lookup"><span data-stu-id="d5a1b-117">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Flache und gespeicherte Größe" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="d5a1b-119">Flache und gespeicherte Größe</span><span class="sxs-lookup"><span data-stu-id="d5a1b-119">Shallow and Retained Size</span></span>  
:::image-end:::  

### <span data-ttu-id="d5a1b-120">Flache Größe</span><span class="sxs-lookup"><span data-stu-id="d5a1b-120">Shallow size</span></span>  

<span data-ttu-id="d5a1b-121">Dies ist die Größe des Speichers, der vom Objekt gehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-121">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="d5a1b-122">Typische JavaScript-Objekte verfügen über einen Speicherplatz, der für die Beschreibung reserviert ist, und zum Speichern unmittelbarer Werte.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-122">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="d5a1b-123">In der Regel können nur Arrays und Zeichenfolgen eine beträchtliche flache Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-123">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="d5a1b-124">Zeichenfolgen und externe Arrays verfügen jedoch häufig über Ihren Hauptspeicher im rendererspeicher, wodurch nur ein kleines Wrapperobjekt auf dem JavaScript-Heap verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-124">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="d5a1b-125">Der Renderer-Arbeitsspeicher ist der gesamte Arbeitsspeicher des Prozesses, in dem eine geprüfte Seite gerendert wird: nativer Arbeitsspeicher + js-Heapspeicher des Page + js-Heapspeichers aller dedizierten Arbeitskräfte, die von der Seite gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-125">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="d5a1b-126">Dennoch kann selbst ein kleines Objekt eine große Menge an Arbeitsspeicher indirekt aufnehmen, indem verhindert wird, dass andere Objekte vom automatischen Garbage Collection-Prozess verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-126">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <span data-ttu-id="d5a1b-127">Beibehaltungs Größe</span><span class="sxs-lookup"><span data-stu-id="d5a1b-127">Retained size</span></span>  

<span data-ttu-id="d5a1b-128">Hierbei handelt es sich um die Größe des Arbeitsspeichers, der freigegeben wird, sobald das Objekt zusammen mit den abhängigen Objekten gelöscht wird, die aus den **Garbage Collector-Stämmen** (GC-Stämme \) nicht erreichbar sind.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-128">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots** \(GC roots\) .</span></span>  

<span data-ttu-id="d5a1b-129">**Garbage Collector-Stämme** \ (GC-Stämme \) bestehen aus **Handles** , die \ (entweder lokal oder Global \) erstellt werden, wenn Sie einen Verweis vom systemeigenen Code auf ein JavaScript-Objekt außerhalb von V8 erstellen.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-129">**Garbage Collector roots** \(GC roots\) are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="d5a1b-130">Alle derartigen Handles befinden sich möglicherweise in einem Heap-Snapshot unter **GC-Roots**  >  -**Handles** und globalen **GC-Stamm**  >  **Handles**.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-130">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="d5a1b-131">Die Beschreibung der Handles in dieser Dokumentation, ohne die Details der Browser Implementierung zu untertauchen, ist möglicherweise verwirrend.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-131">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="d5a1b-132">Sowohl Garbage Collector (GC)-Stämme als auch die Ziehpunkte sind keine Grund zur Sorge.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-132">Both Garbage Collector (GC) roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="d5a1b-133">Es gibt viele interne GC-Stämme, von denen die meisten nicht für die Benutzer interessant sind.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-133">There are lots of internal GC roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="d5a1b-134">Aus Sicht der Anwendungen gibt es folgende Arten von Stämmen:</span><span class="sxs-lookup"><span data-stu-id="d5a1b-134">From the applications standpoint there are following kinds of roots.</span></span>  

*   <span data-ttu-id="d5a1b-135">Globales Window-Objekt \ (in jedem IFRAME \).</span><span class="sxs-lookup"><span data-stu-id="d5a1b-135">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="d5a1b-136">In den Heap-Schnappschüssen gibt es ein Entfernungs Feld, bei dem es sich um die Anzahl der Eigenschaftsverweise auf dem kürzesten Beibehaltungs Pfad aus dem Fenster handelt.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-136">There is a distance field in the heap snapshots which is the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="d5a1b-137">Dokument-DOM-Struktur, bestehend aus allen systemeigenen DOM-Knoten, die durch Durchlaufen des Dokuments erreichbar sind.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-137">Document DOM tree consisting of all native DOM nodes reachable by traversing the document.</span></span>  <span data-ttu-id="d5a1b-138">Nicht alle Knoten können js-Wrapper aufweisen, aber wenn ein Knoten über einen Wrapper verfügt, ist er lebendig, während das Dokument aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-138">Not all of the nodes may have JS wrappers but if a node has a wrapper, it is alive while the document is alive.</span></span>  
*   <span data-ttu-id="d5a1b-139">Manchmal werden Objekte im Debugger-Kontext im **Quellen** Panel und in der **Konsole** (beispielsweise nach der Konsolen Auswertung \) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-139">Sometimes objects may be retained by the debugger context in the **Sources** panel and the **Console** \(for example after Console evaluation\).</span></span>  <span data-ttu-id="d5a1b-140">Erstellen Sie Heap-Schnappschüsse mit einem gelöschten **Konsolen** Panel und keine aktiven Haltepunkte im Debugger im **Quellen** Panel.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-140">Create heap snapshots with a cleared **Console** panel and no active breakpoints in the debugger in the **Sources** panel.</span></span>

>[!TIP]
> <span data-ttu-id="d5a1b-141">Deaktivieren Sie die **Konsolen** Leiste, indem Sie die `clear()` Haltepunkte im **Quellen** Panel ausführen und deaktivieren, bevor Sie einen Heap-Schnappschuss im [Speicher Panel][DevtoolsMemoryProblemsHeapSnapshots]aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-141">Clear the **Console** panel by running `clear()` and deactivate breakpoints in the **Sources** panel before taking a heap snapshot in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>

<span data-ttu-id="d5a1b-142">Der Speicher Graph beginnt mit einem Stamm, der das Objekt des `window` Browsers oder das `Global` Objekt eines Node.js Moduls sein kann.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-142">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="d5a1b-143">Sie steuern nicht, wie dieses Stammobjekt Garbage Collection (GGT) ist.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-143">You do not control how this root object is garbage collected (GCd).</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Sie können nicht steuern, wie das Stammobjekt als Garbage Collection erfasst wird." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="d5a1b-145">Sie können nicht steuern, wie das Stammobjekt als Garbage Collection erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-145">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="d5a1b-146">Was nicht über den Stamm erreichbar ist, erhält Garbage Collection \ (GGT \).</span><span class="sxs-lookup"><span data-stu-id="d5a1b-146">Whatever is not reachable from the root gets garbage collected \(GCd\).</span></span>  

> [!NOTE]
> <span data-ttu-id="d5a1b-147">Die Spalten " [flache Größe](#shallow-size) " und " [Größe beibehalten](#retained-size) " stellen Daten in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-147">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <span data-ttu-id="d5a1b-148">Objekte, die die Struktur beibehalten</span><span class="sxs-lookup"><span data-stu-id="d5a1b-148">Objects retaining tree</span></span>  

<span data-ttu-id="d5a1b-149">Der Heap ist ein Netzwerk von miteinander verbundenen Objekten.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-149">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="d5a1b-150">In der mathematischen Welt wird diese Struktur als **Diagramm** oder Speicher Diagramm bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-150">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="d5a1b-151">Ein Diagramm wird aus **Knoten** erstellt, die über **Kanten**verbunden sind, wobei beide Bezeichnungen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-151">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="d5a1b-152">**Knoten** \ (oder **Objekte**\) werden mit dem Namen der **Konstruktorfunktion** gekennzeichnet, die zum Erstellen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-152">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="d5a1b-153">**Kanten** werden mit den Namen der **Eigenschaften**gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-153">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="d5a1b-154">Erfahren Sie [, wie Sie ein Profil mit dem Heap Profiler aufzeichnen][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="d5a1b-154">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="d5a1b-155">In der folgenden Abbildung sind einige der auffälligen Dinge, die bei der Aufzeichnung des Heap-Schnappschusses im [Speicher Panel][DevtoolsMemoryProblemsHeapSnapshots] angezeigt werden können, Distance: der Abstand vom Garbage Collector \ (GC \)-Stammverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-155">In the following figure, some of the eye-catching things that you may see in the Heap Snapshot recording in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots] include distance:  the distance from the Garbage Collector \(GC\) root.</span></span>  <span data-ttu-id="d5a1b-156">Wenn sich fast alle Objekte desselben Typs im gleichen Abstand befinden und einige wenige in größerer Entfernung sind, ist das eine Untersuchung Wert.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-156">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Abstand vom Stamm" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="d5a1b-158">Abstand vom Stamm</span><span class="sxs-lookup"><span data-stu-id="d5a1b-158">Distance from root</span></span>  
:::image-end:::  

## <span data-ttu-id="d5a1b-159">Dominators</span><span class="sxs-lookup"><span data-stu-id="d5a1b-159">Dominators</span></span>  

<span data-ttu-id="d5a1b-160">Dominator-Objekte bestehen aus einer Struktur, da jedes Objekt genau einen Dominator hat.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-160">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="d5a1b-161">Ein Dominator eines Objekts kann keine direkten Bezüge auf ein Objekt aufweisen, das es dominiert; Das bedeutet, dass die Struktur des Dominators keine Spanning-Struktur des Diagramms ist.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-161">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="d5a1b-162">In der folgenden Abbildung ist die folgende Anweisung wahr.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-162">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="d5a1b-163">Knoten 1 dominiert Knoten 2</span><span class="sxs-lookup"><span data-stu-id="d5a1b-163">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="d5a1b-164">Knoten 2 dominiert die Knoten 3, 4 und 6</span><span class="sxs-lookup"><span data-stu-id="d5a1b-164">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="d5a1b-165">Knoten 3 dominiert Knoten 5</span><span class="sxs-lookup"><span data-stu-id="d5a1b-165">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="d5a1b-166">Knoten 5 dominiert Knoten 8</span><span class="sxs-lookup"><span data-stu-id="d5a1b-166">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="d5a1b-167">Knoten 6 dominiert Knoten 7</span><span class="sxs-lookup"><span data-stu-id="d5a1b-167">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Struktur des Dominators" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="d5a1b-169">Struktur des Dominators</span><span class="sxs-lookup"><span data-stu-id="d5a1b-169">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="d5a1b-170">In der folgenden Abbildung `#3` ist der Knoten der Dominator von `#10` , aber er ist `#7` auch in jedem einfachen Pfad vom Garbage Collector \ (GC \) bis `#10` .</span><span class="sxs-lookup"><span data-stu-id="d5a1b-170">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector \(GC\) to `#10`.</span></span>  <span data-ttu-id="d5a1b-171">Daher ist ein Objekt b ein Dominator eines Objekts a, wenn b in jedem einfachen Pfad vom Stamm zum Objekt a vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-171">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Animierte Dominator-Illustration" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="d5a1b-173">Animierte Dominator-Illustration</span><span class="sxs-lookup"><span data-stu-id="d5a1b-173">Animated dominator illustration</span></span>  
:::image-end:::  

## <span data-ttu-id="d5a1b-174">V8-Besonderheiten</span><span class="sxs-lookup"><span data-stu-id="d5a1b-174">V8 specifics</span></span>  

<span data-ttu-id="d5a1b-175">Bei der Profilerstellung von Arbeitsspeicher ist es hilfreich zu verstehen, warum Heap Momentaufnahmen auf eine bestimmte Weise aussehen.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-175">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="d5a1b-176">In diesem Abschnitt werden einige speicherbezogene Themen beschrieben, die speziell der **virtuellen V8-JavaScript-Maschine** \ (V8 VM oder VM \) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-176">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <span data-ttu-id="d5a1b-177">JavaScript-Objektdarstellung</span><span class="sxs-lookup"><span data-stu-id="d5a1b-177">JavaScript object representation</span></span>  

<span data-ttu-id="d5a1b-178">Es gibt drei primitive Typen:</span><span class="sxs-lookup"><span data-stu-id="d5a1b-178">There are three primitive types:</span></span>  

*   <span data-ttu-id="d5a1b-179">Zahlen \ (Beispiel `3.14159...` : \)</span><span class="sxs-lookup"><span data-stu-id="d5a1b-179">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="d5a1b-180">Boolesche Werte \ ( `true` oder `false` \)</span><span class="sxs-lookup"><span data-stu-id="d5a1b-180">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="d5a1b-181">Zeichenfolgen \ (Beispiel `"Werner Heisenberg"` : \)</span><span class="sxs-lookup"><span data-stu-id="d5a1b-181">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="d5a1b-182">Primitive können nicht auf andere Werte verweisen und sind immer Blatt-oder Endpunkt Knoten.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-182">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="d5a1b-183">**Nummern** können entweder wie folgt gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="d5a1b-183">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="d5a1b-184">eine direkte 31-Bit-Ganzzahl, die als **kleine ganze Zahlen** (**SMI**s \) bezeichnet wird, oder</span><span class="sxs-lookup"><span data-stu-id="d5a1b-184">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="d5a1b-185">Heap-Objekte, die als **Heap-Nummern**bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-185">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="d5a1b-186">Heap-Nummern werden zum Speichern von Werten verwendet, die nicht in das SMI-Formular passen, wie etwa **Doubles**, oder wenn ein Wert **geschachtelt**werden muss, wie beispielsweise das Festlegen von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-186">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="d5a1b-187">**Zeichenfolgen** können entweder in folgendem gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="d5a1b-187">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="d5a1b-188">der **VM-Heap**oder</span><span class="sxs-lookup"><span data-stu-id="d5a1b-188">the **VM heap**, or</span></span>
*   <span data-ttu-id="d5a1b-189">extern im **Speicher des Renderers**.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-189">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="d5a1b-190">Ein **Wrapperobjekt** wird erstellt und für den Zugriff auf externen Speicher verwendet, wenn beispielsweise Skript Quellen und andere Inhalte, die aus dem Web empfangen werden, gespeichert werden, anstatt auf den VM-Heap kopiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-190">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="d5a1b-191">Der Arbeitsspeicher für neue JavaScript-Objekte wird von einem dedizierten JavaScript-Heap zugeordnet \ (oder **VM-Heap**\).</span><span class="sxs-lookup"><span data-stu-id="d5a1b-191">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="d5a1b-192">Diese Objekte werden vom Garbage Collector in V8 verwaltet und bleiben daher so lange am Leben, wie es mindestens einen starken Bezug auf Sie gibt.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-192">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="d5a1b-193">Alles, was sich nicht im JavaScript-Heap befindet, wird als **systemeigenes Objekt**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-193">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="d5a1b-194">Systemeigene Objekte werden im Gegensatz zu Heap Objekten nicht vom V8-Garbage Collector während ihrer gesamten Lebensdauer verwaltet und können nur über JavaScript mit dem JavaScript-Wrapperobjekt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-194">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="d5a1b-195">**Cons String** ist ein Objekt, das aus Paaren von Zeichenfolgen besteht, die gespeichert und dann verknüpft sind und ein Ergebnis der Verkettung sind.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-195">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="d5a1b-196">Die Verknüpfung des **Cons-Zeichenfolgen** Inhalts erfolgt nur bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-196">The joining of the **cons string** contents occurs only as needed.</span></span> <span data-ttu-id="d5a1b-197">Ein Beispiel wäre, wenn eine Teilzeichenfolge einer verknüpften Zeichenfolge erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-197">An example would be when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="d5a1b-198">Wenn Sie beispielsweise verketten `a` und `b` erhalten Sie eine Zeichenfolge, die `(a, b)` das Ergebnis der Verkettung darstellt.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-198">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="d5a1b-199">Wenn Sie später `d` mit diesem Ergebnis verkettet haben, erhalten Sie eine weitere **Cons-Zeichenfolge**: `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="d5a1b-199">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="d5a1b-200">**Matrix** ist ein Objekt mit numerischen Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-200">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="d5a1b-201">**Arrays** werden in der V8-VM umfassend verwendet, um große Datenmengen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-201">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="d5a1b-202">Sätze von Schlüssel-Wert-Paaren, wie Wörterbücher, werden von **Arrays**gesichert.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-202">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="d5a1b-203">Ein typisches JavaScript-Objekt wird nur als einer von zwei **Array** Typen gespeichert:</span><span class="sxs-lookup"><span data-stu-id="d5a1b-203">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="d5a1b-204">benannte Eigenschaften und</span><span class="sxs-lookup"><span data-stu-id="d5a1b-204">named properties, and</span></span>  
*   <span data-ttu-id="d5a1b-205">numerische Elemente</span><span class="sxs-lookup"><span data-stu-id="d5a1b-205">numeric elements</span></span>  

<span data-ttu-id="d5a1b-206">Wenn eine geringe Anzahl von Eigenschaften vorhanden ist, werden die Eigenschaften intern im JavaScript-Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-206">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="d5a1b-207">**Map** ist ein Objekt, das sowohl die Art des Objekts als auch das Layout beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-207">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="d5a1b-208">Karten werden beispielsweise verwendet, um implizite Objekthierarchien für den [schnellen Eigenschaftenzugriff][V8FastProperties]zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-208">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <span data-ttu-id="d5a1b-209">Objektgruppen</span><span class="sxs-lookup"><span data-stu-id="d5a1b-209">Object groups</span></span>  

<span data-ttu-id="d5a1b-210">Jede Gruppe **systemeigene Objekte** besteht aus Objekten, die gegenseitige Bezüge aufeinander abhalten.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-210">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="d5a1b-211">Nehmen Sie beispielsweise eine DOM-Unterstruktur in Frage, bei der jeder Knoten über einen Link zum relativen übergeordneten Element und Links zum nächsten untergeordneten Element und zum nächsten nebengeordneten Element verfügt, wodurch ein verbundenes Diagramm entsteht.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-211">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="d5a1b-212">Systemeigene Objekte werden nicht im JavaScript-Heap dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-212">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="d5a1b-213">Das Fehlen einer Darstellung ist der Grund dafür, dass systemeigene Objekte die Größe 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-213">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="d5a1b-214">Stattdessen werden Wrapper Objekte erstellt.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-214">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="d5a1b-215">Jedes Wrapperobjekt enthält einen Verweis auf das entsprechende systemeigene Objekt für die Umleitung von Befehlen an ihn.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-215">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="d5a1b-216">Eine Objektgruppe enthält wiederum Wrapper Objekte.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-216">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="d5a1b-217">Dadurch wird jedoch kein nicht sammelbarer Zyklus erstellt, da der Garbage Collector \ (GC \) intelligent genug ist, Objektgruppen freizugeben, deren Wrapper nicht mehr referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-217">However, this does not create an uncollectable cycle, as Garbage Collector \(GC\) is smart enough to release object groups whose wrappers are no longer referenced.</span></span> <span data-ttu-id="d5a1b-218">Aber zu vergessen, einen einzelnen Wrapper freizugeben, enthält die gesamte Gruppe und zugehörige Wrapper.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-218">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <span data-ttu-id="d5a1b-219">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="d5a1b-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Aufzeichnen von Heap-Snapshots | Microsoft docs"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Fast-Eigenschaften in V8 | V8"  

> [!NOTE]
> <span data-ttu-id="d5a1b-222">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-222">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d5a1b-223">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) gefunden und von [Meggin Kearney][MegginKearney] (Technical Writer \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d5a1b-223">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="d5a1b-225">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d5a1b-225">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney

---
description: Verwenden Sie den Speicher-Panel, um
title: DevTools – Arbeitsspeicher
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Arbeitsspeicher, Heap, GC, Garbage Collection, Aufbewahrungs Größe, dominierer
ms.custom: seodec18
ms.openlocfilehash: 416ba144f7e22bd50f5d2a3437bc21d9d31a9035
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567610"
---
# <span data-ttu-id="b74cd-104">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="b74cd-104">Memory</span></span>

<span data-ttu-id="b74cd-105">Verwenden Sie den **Speicher** Panel, um ihre Verwendung von Systemressourcen zu messen und Heap-Snapshots in verschiedenen Zuständen der Codeausführung zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-105">Use the **Memory** panel to measure your use of system resources and compare heap snapshots at different states of code execution.</span></span> <span data-ttu-id="b74cd-106">Damit haben Sie folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="b74cd-106">With it, you can:</span></span>

- <span data-ttu-id="b74cd-107">Zeichnen Sie [den Speicherverbrauch Ihrer Seite in Echtzeit ab](#memory-usage-timeline) , und nehmen Sie Schnappschüsse des Heaps auf</span><span class="sxs-lookup"><span data-stu-id="b74cd-107">[Graph the memory consumption of your page in real time](#memory-usage-timeline) and take snapshots of the heap</span></span>
- <span data-ttu-id="b74cd-108">[Ermitteln potenzieller Arbeitsspeicherprobleme](#snapshot-summary) in Ihrem Code, beispielsweise aufbewahrte Objekte, die nicht an das DOM angefügt sind</span><span class="sxs-lookup"><span data-stu-id="b74cd-108">[Identify potential memory issues](#snapshot-summary) in your code, such as retained objects not attached to the DOM</span></span>
- <span data-ttu-id="b74cd-109">[Überprüfen von Speicher Nutzungsdaten](#snapshot-details) nach Objekttyp, instanzenanzahl, Größe und verweisen, um Probleme zu isolieren</span><span class="sxs-lookup"><span data-stu-id="b74cd-109">[Review memory usage data](#snapshot-details) by object type, instance count, size, and references to help isolate issues</span></span>
- <span data-ttu-id="b74cd-110">[Anwenden von Snapshot-Daten filtern](#filters) , um das Rauschen nicht umsetzbar Informationen zu verringern</span><span class="sxs-lookup"><span data-stu-id="b74cd-110">[Apply snapshot data filters](#filters) to reduce the noise of non-actionable information</span></span>
- <span data-ttu-id="b74cd-111">[Ermitteln der Speicherkosten für ein bestimmtes Objekt](#object-references) und die Verweise, die es beibehalten</span><span class="sxs-lookup"><span data-stu-id="b74cd-111">[Identify the memory cost of a specific object](#object-references) and the references keeping it alive</span></span>
- <span data-ttu-id="b74cd-112">Untersuchen Sie [den Heap in verschiedenen Phasen der Untersuchung](#snapshot-comparison) , um die Quelle von Speicherverlusten und anderen Problemen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="b74cd-112">[Diff the heap at different phases of your investigation](#snapshot-comparison) to track down the source of memory leaks and other problems</span></span>

![Der Microsoft Edge devtools-Speicher Panel](./media/memory.png)


## <span data-ttu-id="b74cd-114">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="b74cd-114">Toolbar</span></span>

1. <span data-ttu-id="b74cd-115">**Starten/Beenden der Profilerstellungssitzung (STRG + E)**: Wenn Sie den Profiler aktivieren, können Sie die Speicherauslastung nachvollziehen und Snapshots des Heaps aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-115">**Start/Stop profiling session (Ctrl+E)**: Turning on the profiler enables you to track memory usage and take snapshots of the heap.</span></span>
2. <span data-ttu-id="b74cd-116">**Profilerstellungssitzung importieren (STRG + O)**: Laden Sie eine gespeicherte devtools-Speicherdiagnose Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b74cd-116">**Import profiling session (Ctrl+O)**: Load a saved  DevTools memory diagnostic session.</span></span>
3. <span data-ttu-id="b74cd-117">**Profilerstellungssitzung exportieren (STRG + S)**: Speichern Sie die aktuelle Diagnosesitzung auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="b74cd-117">**Export profiling session (Ctrl+S)**: Save the current diagnostic session to disk.</span></span>
4. <span data-ttu-id="b74cd-118">Erstellen eines **Heap-Snapshots (STRG + UMSCHALT + T)**: Aufzeichnen der aktuellen Speicherzuweisungen für einen bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="b74cd-118">**Take heap snapshot (Ctrl+Shift+T)**: Record current memory allocations for a given point of time.</span></span>


## <span data-ttu-id="b74cd-119">Speicher Auslastungs Zeitachse</span><span class="sxs-lookup"><span data-stu-id="b74cd-119">Memory usage timeline</span></span>

<span data-ttu-id="b74cd-120">Speicherprobleme können ein Hauptverursacher von Leistungsproblemen sein, was dazu führt, dass Ihre Seite zunehmend nicht mehr reagiert und im Laufe der zeitverzögert wird.</span><span class="sxs-lookup"><span data-stu-id="b74cd-120">Memory problems can be a major culprit of performance issues, causing your page to become increasingly unresponsive and laggy over time.</span></span>

<span data-ttu-id="b74cd-121">Der erste Schritt bei der Analyse der Speichernutzung Ihrer Seite besteht darin, [eine Profilerstellungssitzung zu starten](#toolbar) , um vor/nach-Snapshots des Heaps zu erstellen, während Sie die Schritte zum Aufblasen des Arbeitsspeichers oder einen vermuteten Speicherverlust durchführen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-121">The first step to analyzing the memory usage of your page is to [start a profiling session](#toolbar) in order to take before/after snapshots of the heap as you repro the steps causing memory bloat or a suspected memory leak.</span></span>

<span data-ttu-id="b74cd-122">Wenn Sie den Speicher Profiler starten, wird ein Prozess Speicher Diagramm angezeigt, in dem Sie den gesamten privaten Arbeitssatz (die Menge des von der Seite verbrauchten Arbeitsspeichers) über einen Zeitraum beobachten können.</span><span class="sxs-lookup"><span data-stu-id="b74cd-122">When you start the memory profiler, you will see a process memory graph that allows you to observe the overall private working set (the amount of memory consumed by the page) over time.</span></span> <span data-ttu-id="b74cd-123">Im Arbeitsspeicher Diagramm wird eine Live Ansicht des Arbeitsspeichers der Registerkarte angezeigt, die private Bytes, systemeigenen Speicher und den JavaScript-Heap umfasst.</span><span class="sxs-lookup"><span data-stu-id="b74cd-123">The memory graph shows you a live view of the tab's process memory, which includes private bytes, native memory, and the JavaScript heap.</span></span> 

![Speicher Auslastungs Zeitachse](./media/memory_timeline.png)

 <span data-ttu-id="b74cd-125">Das Diagramm zeigt den speichertrend für die Seite an, mit dem Sie beurteilen können, wann [ein Heap-Schnappschuss für einen](#toolbar) späteren Vergleich geeignet ist, beispielsweise wenn Sie Zeiträume mit unerwarteter Speicher Aufbewahrung sehen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-125">The graph gives you an indication of the memory trend for the page which enables you to judge when it is appropriate to [take a heap snapshot](#toolbar) for later comparison, such as when you see periods of unexpected memory retention.</span></span>

### <span data-ttu-id="b74cd-126">Performance. Mark ()</span><span class="sxs-lookup"><span data-stu-id="b74cd-126">Performance.mark()</span></span>

<span data-ttu-id="b74cd-127">Sie können der Zeitachse benutzerdefinierte **Benutzermarkierungen** hinzufügen, um wichtige Ereignisse im Verlauf der Analysesitzung zu identifizieren, indem Sie die [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) Methode im Code oder in der devtools- [**Konsole**](./console.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-127">You can add custom **User marks** to the timeline to help identify  key events during the course of your analysis session by calling the [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) method from within your code or the  DevTools [**Console**](./console.md).</span></span>

### <span data-ttu-id="b74cd-128">Console. takeheapSnapshot ()</span><span class="sxs-lookup"><span data-stu-id="b74cd-128">Console.takeheapSnapshot()</span></span>

<span data-ttu-id="b74cd-129">Manchmal müssen Sie Schnappschüsse zu sehr bestimmten Zeitpunkten aufnehmen, beispielsweise unmittelbar vor einer großen Mutation des DOM.</span><span class="sxs-lookup"><span data-stu-id="b74cd-129">Sometimes you need to take snapshots at very specific points in time, such as immediately before a large mutation of the DOM.</span></span> <span data-ttu-id="b74cd-130">In diesen Fällen können Sie Schnappschüsse programmgesteuert mit ausführen [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots) .</span><span class="sxs-lookup"><span data-stu-id="b74cd-130">In these cases,you can take snapshots programmatically with [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots).</span></span>

## <span data-ttu-id="b74cd-131">Zusammenfassung der Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="b74cd-131">Snapshot summary</span></span>

<span data-ttu-id="b74cd-132">Wenn Sie [einen Schnappschuss](#toolbar) erstellen, wird eine Zusammenfassungs Kachel generiert, die die Größe des JavaScript-Heaps zum Zeitpunkt des Schnappschusses sowie die Anzahl der zugewiesenen Objekte und einen Screenshot der Seite angibt.</span><span class="sxs-lookup"><span data-stu-id="b74cd-132">[Taking a snapshot](#toolbar) will generate a summary tile that indicates the size of the JavaScript heap at the time the snapshot was taken, along with the number of objects allocated and a screenshot of the page.</span></span> <span data-ttu-id="b74cd-133">Sie können jederzeit während der Ausführung des Benutzerszenarios, in dem eine Analyse erforderlich ist, Snapshots aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-133">You can continue to take snapshots at any time as you run through the user scenario requiring analysis.</span></span> <span data-ttu-id="b74cd-134">Die Snapshots generieren zusätzliche Kacheln, die jeweils den Unterschied im JavaScript-Speicher aus dem vorherigen Snapshot angeben.</span><span class="sxs-lookup"><span data-stu-id="b74cd-134">The snapshots generate additional tiles, each of which indicates the difference in JavaScript memory from the previous snapshot.</span></span>

![Heap-Snapshot](./media/memory_snapshot.png)

<span data-ttu-id="b74cd-136">Durch Klicken auf die Werte in der Zusammenfassungs Kachel wechseln Sie zu dem Bereich, in dem [Details zu den Momentaufnahme Daten](#snapshot-details)angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b74cd-136">Clicking on the values in the summary tile will switch to the pane showing [details of the snapshot data](#snapshot-details).</span></span> <span data-ttu-id="b74cd-137">Potenzielle [Speicherprobleme werden](#snapshot-details) mit einem blauen Informationssymbol ("i") angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b74cd-137">Potential [memory issues are indicated](#snapshot-details) with a blue informational ("i") icon.</span></span>

## <span data-ttu-id="b74cd-138">Details zur Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="b74cd-138">Snapshot details</span></span>

<span data-ttu-id="b74cd-139">Die Daten im *Momentaufnahme* Bereich zeigen die von Ihrer Seite erstellten Objekte zusammen mit allen von JavaScript-Frameworks zugewiesenen Arbeitsspeichers, die Sie möglicherweise verwenden.</span><span class="sxs-lookup"><span data-stu-id="b74cd-139">The data in the *Snapshot* pane shows the objects created by your page along with any memory allocated by JavaScript frameworks you may be consuming.</span></span>

![Snapshot-Detailtabelle](./media/memory_details.png)

<span data-ttu-id="b74cd-141">Die drei Registerkarten stellen unterschiedliche Ansichten der Daten dar:</span><span class="sxs-lookup"><span data-stu-id="b74cd-141">The three tabs represent different views of the data:</span></span>

#### <span data-ttu-id="b74cd-142">Typen</span><span class="sxs-lookup"><span data-stu-id="b74cd-142">Types</span></span>

<span data-ttu-id="b74cd-143">Zeigt die Anzahl der Instanzen und die Gesamtgröße von Objekten im Heap, gruppiert nach Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="b74cd-143">Shows the instance count and total size of objects on the heap, grouped by object type.</span></span> <span data-ttu-id="b74cd-144">Standardmäßig werden diese nach instanzenanzahl sortiert.</span><span class="sxs-lookup"><span data-stu-id="b74cd-144">By default, these are sorted by instance count.</span></span>

<span data-ttu-id="b74cd-145">Wenn Sie ein Objekt im Bereich obere *Typen* auswählen, werden in der Tabelle [Objektverweise](#object-references) im unteren Bereich alle Objekte aufgelistet, die auf das Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-145">When you select an object in the upper *Types* pane, the [Object references](#object-references) table in the lower pane will list all the objects that point to that object.</span></span>

#### <span data-ttu-id="b74cd-146">Wurzeln</span><span class="sxs-lookup"><span data-stu-id="b74cd-146">Roots</span></span>

<span data-ttu-id="b74cd-147">Zeigt eine hierarchische Ansicht der untergeordneten Bezüge an, um zu beschreiben, wie Objekte zum globalen Objekt verwurzelt sind, wodurch verhindert wird, dass Sie von der Garbage Collection erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="b74cd-147">Shows a hierarchical view of child references to describe how objects are rooted to the global object, thus preventing them from being garbage-collected.</span></span>

<span data-ttu-id="b74cd-148">Standardmäßig werden die untergeordneten Knoten nach der Spalte mit der Beibehaltungs Größe sortiert, wobei der größte oben ist.</span><span class="sxs-lookup"><span data-stu-id="b74cd-148">By default, the child nodes are sorted by the retained size column, with the largest at the top.</span></span>

#### <span data-ttu-id="b74cd-149">Dominators</span><span class="sxs-lookup"><span data-stu-id="b74cd-149">Dominators</span></span>

<span data-ttu-id="b74cd-150">Zeigt eine Liste der Objekte auf dem Heap, die exklusive Bezüge zu anderen Objekten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-150">Shows a list of objects on the heap that have exclusive references to other objects.</span></span> <span data-ttu-id="b74cd-151">Die dominierer werden nach Beibehaltungs Größe sortiert, um die Objekte anzugeben, die den meisten Speicher verbrauchen, die möglicherweise am einfachsten zu befreien sind.</span><span class="sxs-lookup"><span data-stu-id="b74cd-151">Dominators are sorted by retained size to indicate the objects consuming the most memory that are potentially easiest to free.</span></span>

<span data-ttu-id="b74cd-152">Hier erfahren Sie, wie Sie die Spalten in den Ansichten *Typen, Stämme* und *Dominanzen* interpretieren:</span><span class="sxs-lookup"><span data-stu-id="b74cd-152">Here's how to interpret the columns in the *Types, Roots* and *Dominators* views:</span></span>

<span data-ttu-id="b74cd-153">Spalte</span><span class="sxs-lookup"><span data-stu-id="b74cd-153">Column</span></span> | <span data-ttu-id="b74cd-154">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b74cd-154">Description</span></span>
:------------ | :-------------
<span data-ttu-id="b74cd-155">Kennung (en)</span><span class="sxs-lookup"><span data-stu-id="b74cd-155">Identifier(s)</span></span> | <span data-ttu-id="b74cd-156">Der Name, der das Objekt am besten identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b74cd-156">Name that best identifies the object.</span></span> <span data-ttu-id="b74cd-157">Bei HTML-Elementen zeigt die momentaufnahmedetails beispielsweise den ID-Attributwert an, wenn eine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b74cd-157">For example, for HTML elements the snapshot details show the ID attribute value, if one is used.</span></span>
<span data-ttu-id="b74cd-158">Typ</span><span class="sxs-lookup"><span data-stu-id="b74cd-158">Type</span></span> | <span data-ttu-id="b74cd-159">Objekttyp (beispielsweise *HTMLDivElement*).</span><span class="sxs-lookup"><span data-stu-id="b74cd-159">Object type (for example, *HTMLDivElement*).</span></span>
<span data-ttu-id="b74cd-160">Size</span><span class="sxs-lookup"><span data-stu-id="b74cd-160">Size</span></span> | <span data-ttu-id="b74cd-161">Objektgröße, ohne die Größe von referenzierten Objekten.</span><span class="sxs-lookup"><span data-stu-id="b74cd-161">Object size, not including the size of any referenced objects.</span></span>
<span data-ttu-id="b74cd-162">Beibehaltungs Größe</span><span class="sxs-lookup"><span data-stu-id="b74cd-162">Retained size</span></span> | <span data-ttu-id="b74cd-163">Objektgröße plus die Größe aller untergeordneten Objekte, die keine anderen übergeordneten Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-163">Object size plus the size of all child objects that have no other parents.</span></span> <span data-ttu-id="b74cd-164">Für praktische Zwecke ist dies die Größe des vom Objekt aufbewahrten Arbeitsspeichers, wenn Sie also das Objekt löschen, wird die angegebene Speichermenge zurückgefordert.</span><span class="sxs-lookup"><span data-stu-id="b74cd-164">For practical purposes, this is the amount of memory retained by the object, so if you delete the object you reclaim the specified amount of memory.</span></span>
<span data-ttu-id="b74cd-165">Anzahl</span><span class="sxs-lookup"><span data-stu-id="b74cd-165">Count</span></span> | <span data-ttu-id="b74cd-166">Die Anzahl der Objektinstanzen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-166">Number of object instances.</span></span> <span data-ttu-id="b74cd-167">Dieser Wert wird nur in der Ansicht Typen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b74cd-167">This value appears only in the Types view.</span></span>

<span data-ttu-id="b74cd-168">Wenn Sie ein Objekt im Bereich obere *Dominanz* auswählen, werden in der Tabelle [Objektverweise](#object-references) im unteren Bereich alle Objekte aufgelistet, die auf das Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-168">When you select an object in the upper *Dominators* pane, the [Object references](#object-references) table in the lower pane will list all the objects that point to that object.</span></span>

### <span data-ttu-id="b74cd-169">Filter</span><span class="sxs-lookup"><span data-stu-id="b74cd-169">Filters</span></span>

<span data-ttu-id="b74cd-170">Sie können die Daten in der Tabelle mit den folgenden Schritten weiter anpassen:</span><span class="sxs-lookup"><span data-stu-id="b74cd-170">You can further adjust data in the table with the following:</span></span>

![Filtern nach integrierten und Objekt-IDs](./media/memory_filter.png)

1. <span data-ttu-id="b74cd-172">**Kennzeichnungs Filter**: Filtern von Daten durchsuchen nach einer bestimmten Objektkennung</span><span class="sxs-lookup"><span data-stu-id="b74cd-172">**Identifier filter**: Filter out data by searching for a particular object identifier</span></span>
2. <span data-ttu-id="b74cd-173">**Gruppieren nach Dominator**: nur Objekte mit *exklusiven* Bezügen auf andere Objekte werden in der Ansicht der obersten Ebene der Objekte angezeigt (Dies ist die Standardansicht auf der Registerkarte " *Herrscher* ").</span><span class="sxs-lookup"><span data-stu-id="b74cd-173">**Group by dominator**: Only objects with *exclusive* references to other objects are shown in the top-level view of objects (this is the default view in the *Dominators* tab).</span></span>
3. <span data-ttu-id="b74cd-174">**Integrierter/IDs-Filter**: Standardmäßig sind [JavaScript-integrierte Objekte](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) in der Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="b74cd-174">**Built-ins / IDs filter**: By default, [JavaScript built-in objects](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) are included in the list.</span></span> <span data-ttu-id="b74cd-175">Das Auflisten von Objekt-IDs kann hilfreich sein, wenn mehrere anonyme Objekte unterschieden werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-175">Listing object IDs can be useful if there are multiple anonymous objects which need to be differentiated.</span></span>

<span data-ttu-id="b74cd-176">Die Ansichten *Typen, Stämme* und *Dominanzen* verfügen jeweils über einen eigenen Filter, sodass der Filter nicht beibehalten wird, wenn Sie zu einer anderen Ansicht wechseln.</span><span class="sxs-lookup"><span data-stu-id="b74cd-176">The *Types, Roots* and *Dominators* views each has its own filter, so the filter isn't preserved when you switch to another view.</span></span>

### <span data-ttu-id="b74cd-177">Objekt Bezüge</span><span class="sxs-lookup"><span data-stu-id="b74cd-177">Object references</span></span>

<span data-ttu-id="b74cd-178">In den Ansichten [**Typen**](#types) und [**Dominanzen**](#dominators) enthält der untere Bereich eine **Objektverweis** Liste, in der freigegebene Verweise angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b74cd-178">In the [**Types**](#types) and [**Dominators**](#dominators) views, the lower pane contains an **Object references** list that displays shared references.</span></span> <span data-ttu-id="b74cd-179">Wenn Sie ein Objekt im oberen Bereich auswählen, werden in dieser Liste alle Objekte angezeigt, die auf das Objekt verweisen, also die Objekte, die das ausgewählte Objekt am Leben erhalten.</span><span class="sxs-lookup"><span data-stu-id="b74cd-179">When you choose an object in the upper pane, this list displays all objects that point to that object--in other words, the objects that are keeping the selected object alive.</span></span>

<span data-ttu-id="b74cd-180">Zirkelbezüge werden mit einem Sternchen (\*) und Informations ToolTip angezeigt und können nicht erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="b74cd-180">Circular references are shown with an asterisk (\*) and informational tooltip, and cannot be expanded.</span></span> <span data-ttu-id="b74cd-181">Andernfalls verhindern Sie, dass Sie die Referenzstruktur hinauflaufen und Objekte identifizieren, die Speicher erhalten.</span><span class="sxs-lookup"><span data-stu-id="b74cd-181">Otherwise, they would prevent you from walking up the reference tree and identifying objects that are retaining memory.</span></span>

<span data-ttu-id="b74cd-182">Um gleichwertige Objekte schnell zu identifizieren, markieren Sie die Option " [*Objekt-IDs anzeigen*](#filters) ", um Objekt-IDs neben Objektnamen in der Spalte " *Identifier (s)* " anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-182">To quickly identify equivalent objects, tick the [*Display object IDs*](#filters) filter option to display object IDs next to object names in the *Identifier(s)* column.</span></span> <span data-ttu-id="b74cd-183">Objekte mit der gleichen ID sind freigegebene Verweise.</span><span class="sxs-lookup"><span data-stu-id="b74cd-183">Objects that have the same ID are shared references.</span></span>

### <span data-ttu-id="b74cd-184">Snapshot-Vergleich</span><span class="sxs-lookup"><span data-stu-id="b74cd-184">Snapshot comparison</span></span>

<span data-ttu-id="b74cd-185">Durch Klicken auf die [Registerkarte "Snapshot-Vergleich"](#snapshot-details) oder den Vergleichs Link auf der [Kachel "Snapshot-Zusammenfassung](#snapshot-summary) " wird ein Unterschied zwischen den beiden Schnappschüssen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b74cd-185">Clicking on a [snapshot comparison tab](#snapshot-details) or comparison link on the [snapshot summary tile](#snapshot-summary)  will show a diff of information between the two snapshots.</span></span> <span data-ttu-id="b74cd-186">Im Vergleichsbereich bieten die Vorwahlen *, Typen* und *Stamm* Ansichten dieselben Snapshot- [*Details*](#snapshot-details) , die Sie für einzelne Schnappschüsse sehen würden, mit den folgenden zusätzlichen Werten:</span><span class="sxs-lookup"><span data-stu-id="b74cd-186">In the comparison pane, the *Dominators, Types* and *Roots* views provide the same [*snapshot details*](#snapshot-details) you would see for a single snapshots, with these additional values:</span></span>

<span data-ttu-id="b74cd-187">Spalte</span><span class="sxs-lookup"><span data-stu-id="b74cd-187">Column</span></span> | <span data-ttu-id="b74cd-188">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b74cd-188">Description</span></span>
:------------ | :-------------
<span data-ttu-id="b74cd-189">Größenunterschied.</span><span class="sxs-lookup"><span data-stu-id="b74cd-189">Size diff.</span></span> | <span data-ttu-id="b74cd-190">Unterschied zwischen der Größe des Objekts im aktuellen Snapshot und seiner Größe im vorherigen Snapshot, ohne die Größe von referenzierten Objekten.</span><span class="sxs-lookup"><span data-stu-id="b74cd-190">Difference between the size of the object in the current snapshot and its size in the previous snapshot, not including the size of any referenced objects.</span></span>
<span data-ttu-id="b74cd-191">Unterschiede bei der Beibehaltungs Größe</span><span class="sxs-lookup"><span data-stu-id="b74cd-191">Retained size diff.</span></span> | <span data-ttu-id="b74cd-192">Unterschied zwischen der aufbewahrten Größe des Objekts im aktuellen Snapshot und der Beibehaltungs Größe im vorherigen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="b74cd-192">Difference between the retained size of the object in the current snapshot and its retained size in the previous snapshot.</span></span> <span data-ttu-id="b74cd-193">Die Beibehaltungs Größe umfasst die Objektgröße plus die Größe aller untergeordneten Objekte, die keine anderen übergeordneten Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-193">The retained size includes the object size plus the size of all its child objects that have no other parents.</span></span> <span data-ttu-id="b74cd-194">Für praktische Zwecke ist die Größe des Speichers, der vom Objekt aufbewahrt wird, also, wenn Sie das Objekt löschen, das Sie den angegebenen Arbeitsspeicher zurückfordern.</span><span class="sxs-lookup"><span data-stu-id="b74cd-194">For practical purposes, the retained size is the amount of memory retained by the object, so if you delete the object you reclaim the specified amount of memory.</span></span>

<span data-ttu-id="b74cd-195">Sie können die Dropdownliste **Bereichs** verwenden, um differenzielle Informationen zwischen Snapshots zu filtern:</span><span class="sxs-lookup"><span data-stu-id="b74cd-195">You can use the **Scope** dropdown to filter differential info between snapshots:</span></span>

![Bereichsfilter für Snapshot-Vergleiche](./media/memory_comparison_scope_filter.png)

- <strong><span data-ttu-id="b74cd-197">Objekte, die von "Snapshot #" übrig <number></strong> sind, zeigt die Differenz zwischen den Objekten, die dem Heap hinzugefügt wurden, und aus dem Heap vom Basisplan zum vorherigen Snapshot entfernt.</span><span class="sxs-lookup"><span data-stu-id="b74cd-197">Objects left over from Snapshot #<number></strong>: Shows the diff between the objects added to the heap and removed from the heap from the baseline snapshot to the previous snapshot.</span></span> <span data-ttu-id="b74cd-198">Wenn beispielsweise in der Zusammenfassung der Momentaufnahme <em> + 205/-195 </em> in der Objektanzahl angezeigt wird, werden in diesem Filter die zehn Objekte angezeigt, die hinzugefügt, aber nicht entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="b74cd-198">For example, if the snapshot summary shows <em>+205 / -195</em> in the object count, this filter will show you the ten objects that were added but not removed.</span></span>

- <strong><span data-ttu-id="b74cd-199">Zwischen Snapshot # und #: hinzugefügte Objekte <number> <number></strong> zeigt alle Objekte, die dem Heap aus dem vorherigen Snapshot hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="b74cd-199">Objects added between Snapshot #<number> and #<number></strong>: Shows all objects added to the heap from the previous snapshot.</span></span>

- <strong><span data-ttu-id="b74cd-200">Alle Objekte in Snapshot # <number></strong> : zeigt alle Objekte auf dem Heap an (also eine <em> ungefilterte </em> Ansicht).</span><span class="sxs-lookup"><span data-stu-id="b74cd-200">All objects in Snapshot #<number></strong>: Shows all objects on the heap (in other words, an <em>unfiltered</em> view).</span></span>

<span data-ttu-id="b74cd-201">Standardmäßig wird der Filter *nicht übereinstimmende Bezüge anzeigen* auf die Vergleichsansicht angewendet, um Objekt Bezüge anzugeben, die dem aktuellen Bereichsfilter nicht entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-201">By default, the *Show non-matching references* filter is applied to the comparison view to indicate object references that don't match the current Scope filter.</span></span> <span data-ttu-id="b74cd-202">Sie können es über das Dropdown-Menü deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="b74cd-202">You can turn it off from the dropdown menu:</span></span>

![Filter für nicht übereinstimmende Bezüge für Snapshot-Vergleiche](./media/memory_comparison_matching_filter.png)


## <span data-ttu-id="b74cd-204">Kombinationen</span><span class="sxs-lookup"><span data-stu-id="b74cd-204">Shortcuts</span></span>

 <span data-ttu-id="b74cd-205">Aktion</span><span class="sxs-lookup"><span data-stu-id="b74cd-205">Action</span></span> | <span data-ttu-id="b74cd-206">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="b74cd-206">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="b74cd-207">Starten/Beenden der Profilerstellungssitzung</span><span class="sxs-lookup"><span data-stu-id="b74cd-207">Start / Stop profiling session</span></span>  | `Ctrl` + `E`
<span data-ttu-id="b74cd-208">Profilerstellungssitzung importieren</span><span class="sxs-lookup"><span data-stu-id="b74cd-208">Import profiling session</span></span> | `Ctrl` + `O`
<span data-ttu-id="b74cd-209">Profilerstellungssitzung exportieren</span><span class="sxs-lookup"><span data-stu-id="b74cd-209">Export profiling session</span></span> | `Ctrl` + `S`
<span data-ttu-id="b74cd-210">Snapshot des Heaps aufnehmen</span><span class="sxs-lookup"><span data-stu-id="b74cd-210">Take heap snapshot</span></span> | `Ctrl` + `Shift` + `T`

## <span data-ttu-id="b74cd-211">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="b74cd-211">Known Issues</span></span>

### <span data-ttu-id="b74cd-212">Beim Starten der Profilerstellungssitzung ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b74cd-212">An error occurred while starting the profiling session</span></span>

<span data-ttu-id="b74cd-213">Wenn diese Fehlermeldung angezeigt wird: **beim Starten der Profilerstellungssitzung im Speicher Tool ist ein Fehler aufgetreten** , führen Sie die folgenden Schritte aus, um eine Problemumgehung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b74cd-213">If you see this error message: **An error occurred while starting the profiling session** in the Memory tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="b74cd-214">Drücken Sie `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="b74cd-214">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="b74cd-215">Geben Sie im Dialogfeld Ausführen den **Dienst "Services. msc**" ein.</span><span class="sxs-lookup"><span data-stu-id="b74cd-215">In the Run dialog, enter **services.msc**.</span></span>
![Bekannte Probleme-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="b74cd-217">Suchen Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst** , und klicken Sie mit der rechten Maustaste darauf.</span><span class="sxs-lookup"><span data-stu-id="b74cd-217">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![Bekannte Probleme-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="b74cd-219">Starten Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst**erneut.</span><span class="sxs-lookup"><span data-stu-id="b74cd-219">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![Bekannte Probleme-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="b74cd-221">Schließen Sie die Microsoft Edge-Entwickler Tools und die Registerkarte. Öffnen Sie eine neue Registerkarte, navigieren Sie zu Ihrer Seite, und drücken Sie `F12` .</span><span class="sxs-lookup"><span data-stu-id="b74cd-221">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="b74cd-222">Sie sollten jetzt in der Lage sein, mit der Profilerstellung zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="b74cd-222">You should now be able to begin profiling.</span></span> 
![Bekannte Probleme-4](./media/known_issues_4-memory.PNG)

<span data-ttu-id="b74cd-224">Gibt es immer noch Probleme?</span><span class="sxs-lookup"><span data-stu-id="b74cd-224">Still running into problems?</span></span> <span data-ttu-id="b74cd-225">Senden Sie uns Ihr Feedback über das Symbol **Feedback senden** !</span><span class="sxs-lookup"><span data-stu-id="b74cd-225">Please send us your feedback using the **Send feedback** icon!</span></span> 

![Bekannte Probleme-5](./media/known_issues_5.PNG)

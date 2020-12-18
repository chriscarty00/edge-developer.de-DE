---
description: Verwenden der Konsolen-API zum programmgesteuerten Debuggen und profilieren Ihres Codes
title: DevTools-Console-Console-API
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Konsolen-API
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46a74b80b504358ff7dbea40970528c8e2b228cf
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233704"
---
# <span data-ttu-id="a29f5-104">Konsolen-API</span><span class="sxs-lookup"><span data-stu-id="a29f5-104">Console API</span></span>

<span data-ttu-id="a29f5-105">Die *Konsolen-API* bietet Befehlszeilen-und programmgesteuerten Zugriff auf die devtools-Konsole über das globale `console` Objekt, sodass Sie:</span><span class="sxs-lookup"><span data-stu-id="a29f5-105">The *Console API* provides command-line and programmatic access to the  DevTools Console through the global `console` object, allowing you to:</span></span>

 - <span data-ttu-id="a29f5-106">[Protokollieren von benutzerdefinierten Nachrichten](#logging-custom-messages) von Ihrem Code</span><span class="sxs-lookup"><span data-stu-id="a29f5-106">[Log custom messages](#logging-custom-messages) from you code</span></span>
 - <span data-ttu-id="a29f5-107">Über [Prüfen von Objekten und Elementen](#inspecting-objects-and-elements) und Protokollieren der zugehörigen Informationen</span><span class="sxs-lookup"><span data-stu-id="a29f5-107">[Inspect objects and elements](#inspecting-objects-and-elements) and log their information</span></span>
 - <span data-ttu-id="a29f5-108">[Testen und Messen Ihres Codes](#testing-and-measuring) durch Festlegen von Assertionen, Timer und Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="a29f5-108">[Test and measure your code](#testing-and-measuring) by setting assertions, timers and counters</span></span>
 - <span data-ttu-id="a29f5-109">Erstellen [Sie Schnappschüsse des Heaps](#taking-heap-snapshots) , um den Speicherverbrauch Ihres ausgeführten Codes zu bewerten und Speicherverluste zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a29f5-109">[Take snapshots of the heap](#taking-heap-snapshots) to assess the memory consumption of your running code and identify memory leaks</span></span>
 - <span data-ttu-id="a29f5-110">[Verfolgen Sie Ihre callstacks](#tracing-callstacks) , um zu verstehen, woher Ihr Code aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a29f5-110">[Trace your callstacks](#tracing-callstacks) to understand where your code is being called from</span></span> 
 - <span data-ttu-id="a29f5-111">[Organisieren der Protokollausgabe](#organizing-log-output) , um das Debuggen zu rationalisieren</span><span class="sxs-lookup"><span data-stu-id="a29f5-111">[Organize your log output](#organizing-log-output) to streamline your debugging</span></span>

<span data-ttu-id="a29f5-112">Im folgenden finden Sie die Befehle und Formatierungsparameter, die von Microsoft Edge zurzeit unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a29f5-112">The following are the commands and formatting parameters currently supported by Microsoft Edge.</span></span> <span data-ttu-id="a29f5-113">Sie funktionieren ähnlich wie bei wichtigen Browsern.</span><span class="sxs-lookup"><span data-stu-id="a29f5-113">They work similarly on major browsers.</span></span>

## <span data-ttu-id="a29f5-114">Protokollieren benutzerdefinierter Nachrichten</span><span class="sxs-lookup"><span data-stu-id="a29f5-114">Logging custom messages</span></span>

<span data-ttu-id="a29f5-115">Ihr Code kann verschiedene Typen von benutzerdefinierten Nachrichten an die Konsole senden, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="a29f5-115">Your code can send several types of custom messages to the console, including:</span></span>

<span data-ttu-id="a29f5-116">Nachrichtentyp</span><span class="sxs-lookup"><span data-stu-id="a29f5-116">Message type</span></span>  | &nbsp;   |
:------------------- | :------ |
<span data-ttu-id="a29f5-117">[**Error ()**](https://developer.mozilla.org/docs/Web/API/Console/error) und [ **Exception ()**](https://developer.mozilla.org/docs/Web/API/Console/error)</span><span class="sxs-lookup"><span data-stu-id="a29f5-117">[**error()**](https://developer.mozilla.org/docs/Web/API/Console/error) and [**exception()**](https://developer.mozilla.org/docs/Web/API/Console/error)</span></span>| <span data-ttu-id="a29f5-118">Kritische Fehler und Fehler</span><span class="sxs-lookup"><span data-stu-id="a29f5-118">Critical errors and failures</span></span>
[**<span data-ttu-id="a29f5-119">Warnung ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-119">warn()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/warn) | <span data-ttu-id="a29f5-120">Mögliche Fehler oder unerwartetes Verhalten</span><span class="sxs-lookup"><span data-stu-id="a29f5-120">Possible errors or unexpected behavior</span></span> 
[**<span data-ttu-id="a29f5-121">Info ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-121">info()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/info) | <span data-ttu-id="a29f5-122">Nützliche, aber nicht kritische Informationen</span><span class="sxs-lookup"><span data-stu-id="a29f5-122">Useful, but non-critical information</span></span>
<span data-ttu-id="a29f5-123">[**Log ()**](https://developer.mozilla.org/docs/Web/API/Console/log) und [ **Debug ()**](https://developer.mozilla.org/docs/Web/API/Console/log)</span><span class="sxs-lookup"><span data-stu-id="a29f5-123">[**log()**](https://developer.mozilla.org/docs/Web/API/Console/log) and [**debug()**](https://developer.mozilla.org/docs/Web/API/Console/log)</span></span> | <span data-ttu-id="a29f5-124">Allgemeines Debuggen (ohne ein System Warnungssymbol in der Konsole zu generieren)</span><span class="sxs-lookup"><span data-stu-id="a29f5-124">General debugging (without generating a system alert icon in the console)</span></span>

   
<span data-ttu-id="a29f5-125">Sie können diese zusammen mit den anderen Nachrichten, die von Microsoft Edge generiert wurden, aus dem Konsolenbereich gruppieren und filtern.</span><span class="sxs-lookup"><span data-stu-id="a29f5-125">You can group and filter these along with the other messages generated from Microsoft Edge from the  Console panel.</span></span> <span data-ttu-id="a29f5-126">Alle benutzerdefinierten Nachrichten Methoden erfordern einen Zeichenfolgenparameter (Message) und optionale Format Ersetzungsparameter.</span><span class="sxs-lookup"><span data-stu-id="a29f5-126">All custom message methods require a string (message) parameter and optional format substitution parameters.</span></span> <span data-ttu-id="a29f5-127">Microsoft Edge unterstützt die folgenden Formatierungsoptionen:</span><span class="sxs-lookup"><span data-stu-id="a29f5-127">Microsoft Edge supports the following formatting options:</span></span>

<span data-ttu-id="a29f5-128">Format-Parameter</span><span class="sxs-lookup"><span data-stu-id="a29f5-128">Format parameter</span></span> | &nbsp;
:------------------- | :--- |
**<span data-ttu-id="a29f5-129">% b</span><span class="sxs-lookup"><span data-stu-id="a29f5-129">%b</span></span>** | <span data-ttu-id="a29f5-130">Binär</span><span class="sxs-lookup"><span data-stu-id="a29f5-130">Binary</span></span>
**<span data-ttu-id="a29f5-131">% c</span><span class="sxs-lookup"><span data-stu-id="a29f5-131">%c</span></span>** | <span data-ttu-id="a29f5-132">Inline-CSS-Formatvorlage (siehe Beispiel unten)</span><span class="sxs-lookup"><span data-stu-id="a29f5-132">Inline CSS style (see example below)</span></span>
<span data-ttu-id="a29f5-133">**% d**, **% i**</span><span class="sxs-lookup"><span data-stu-id="a29f5-133">**%d**, **%i**</span></span> | <span data-ttu-id="a29f5-134">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="a29f5-134">Integer</span></span> 
**<span data-ttu-id="a29f5-135">% f</span><span class="sxs-lookup"><span data-stu-id="a29f5-135">%f</span></span>** | <span data-ttu-id="a29f5-136">Gleitkomma</span><span class="sxs-lookup"><span data-stu-id="a29f5-136">Float</span></span>  
**<span data-ttu-id="a29f5-137">% s</span><span class="sxs-lookup"><span data-stu-id="a29f5-137">%s</span></span>** | <span data-ttu-id="a29f5-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a29f5-138">String</span></span> 
**<span data-ttu-id="a29f5-139">% x</span><span class="sxs-lookup"><span data-stu-id="a29f5-139">%x</span></span>** | <span data-ttu-id="a29f5-140">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="a29f5-140">Hexadecimal</span></span> 
**<span data-ttu-id="a29f5-141">% e</span><span class="sxs-lookup"><span data-stu-id="a29f5-141">%e</span></span>** | <span data-ttu-id="a29f5-142">Exponent</span><span class="sxs-lookup"><span data-stu-id="a29f5-142">Exponent</span></span> 

<span data-ttu-id="a29f5-143">So können Sie beispielsweise Zeichenfolgen-und ganzzahlige Variablen in Ihre Protokollmeldung einbeziehen:</span><span class="sxs-lookup"><span data-stu-id="a29f5-143">For example, here's how you would include string and integer variables in your log message:</span></span>

```javascript
var myText = 'pieces';
var myVal = 5;
console.log("The number of %s is %d.", myText, myVal);
```

>`The number of pieces is 5.`

<span data-ttu-id="a29f5-144">Und so können Sie einer Protokollnachricht mit Inline-CSS () einen grünen Hervorhebungseffekt hinzufügen `%c` :</span><span class="sxs-lookup"><span data-stu-id="a29f5-144">And here's how you might add a green highlight effect to a log message with inline CSS (`%c`):</span></span>

```javascript
console.log("%cHighlight this log message in green", "background-color: #10ff00; text-transform: uppercase;");
```

![Konsolenprotokoll mit Inlineformatvorlagen](../media/console_api_css.png)

## <span data-ttu-id="a29f5-146">Untersuchen von Objekten und Elementen</span><span class="sxs-lookup"><span data-stu-id="a29f5-146">Inspecting objects and elements</span></span>

<span data-ttu-id="a29f5-147">Überprüfbare Objekte werden in der Konsole in einer reduzierten Strukturansicht mit erweiterbaren Knoten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a29f5-147">Inspectable objects appear in the console in a collapsed tree view with expandable nodes.</span></span> <span data-ttu-id="a29f5-148">Die Konsole erkennt, ob Sie einen DOM-Knoten (wie ein div) oder ein JavaScript-Objekt (wie ein Ereignis) senden, und zeigt diese automatisch als erkannten Typ an.</span><span class="sxs-lookup"><span data-stu-id="a29f5-148">The console detects whether you are sending a DOM node (like a div) or a JavaScript object (like an event) and displays them as the detected type automatically.</span></span>

<span data-ttu-id="a29f5-149">Sie können auch eine bestimmte Ausgabe erzwingen:</span><span class="sxs-lookup"><span data-stu-id="a29f5-149">You can also force a specific output:</span></span>

<span data-ttu-id="a29f5-150">Befehl</span><span class="sxs-lookup"><span data-stu-id="a29f5-150">Command</span></span> | &nbsp;
:------------------- | :--- |
[**<span data-ttu-id="a29f5-151">dir ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-151">dir()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/dir) | <span data-ttu-id="a29f5-152">Wird als über JavaScript-Objekt angezeigt</span><span class="sxs-lookup"><span data-stu-id="a29f5-152">Displays as inspectable JavaScript object</span></span>
[**<span data-ttu-id="a29f5-153">DirXML ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-153">dirxml()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/dirxml) | <span data-ttu-id="a29f5-154">Anzeige als über DOM-Knoten</span><span class="sxs-lookup"><span data-stu-id="a29f5-154">Displays as inspectable DOM node</span></span>

<span data-ttu-id="a29f5-155">Versuchen Sie beispielsweise, die Konsole zu öffnen und die folgenden Ausgaben für das `<div id='main'>` Element auf dieser Seite zu vergleichen:</span><span class="sxs-lookup"><span data-stu-id="a29f5-155">For example, try opening the console and compare the following outputs for the `<div id='main'>` element on this page:</span></span>

```javascript
console.dir(document.querySelector('#main'));
console.dirxml(document.querySelector('#main'));
```

![Vergleich der Ausgabe "dir" versus "DirXML"](../media/console_api_dir.png)

### <span data-ttu-id="a29f5-157">Auswählen eines **Elements im Element Panel**</span><span class="sxs-lookup"><span data-stu-id="a29f5-157">Selecting an element in the **Elements** panel</span></span>

<span data-ttu-id="a29f5-158">Sie können ein Element innerhalb des HTML-Struktur Kontexts der Seite direkt aus der Konsole für das sofortige Layout und das Debuggen von Stilen auswählen.</span><span class="sxs-lookup"><span data-stu-id="a29f5-158">You can select an element within the HTML tree context of the page directly from the console for immediate layout and style debugging.</span></span>

<span data-ttu-id="a29f5-159">Befehl</span><span class="sxs-lookup"><span data-stu-id="a29f5-159">Command</span></span> | &nbsp;
:------------------- | :--- |
**<span data-ttu-id="a29f5-160">Select ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-160">select()</span></span>** | <span data-ttu-id="a29f5-161">Wechselt zum Element **Panel und legt den Fokus** auf das angegebene Element fest.</span><span class="sxs-lookup"><span data-stu-id="a29f5-161">Switches to the **Elements** panel and sets focus to the specified element.</span></span>

<span data-ttu-id="a29f5-162">Wenn Sie beispielsweise die Konsole auf dieser Seite öffnen, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="a29f5-162">For example, if you open the console on this page and type:</span></span>

```javascript
console.select(document.querySelector("body"));
```

<span data-ttu-id="a29f5-163">Der devtools wechselt zum **Element Panel (** sofern es nicht bereits der aktuelle ist) und legt den Fokus in der [*HTML-Strukturansicht*](../elements.md#html-tree-view) auf das angegebene Element fest.</span><span class="sxs-lookup"><span data-stu-id="a29f5-163">The DevTools will switch to the **Elements** panel (if its not already the current) and set focus in the [*HTML tree view*](../elements.md#html-tree-view) to the specified element.</span></span>

![Beispiel für die "Select"-Methode](../media/console_api_select.png)

## <span data-ttu-id="a29f5-165">Testen und Messen</span><span class="sxs-lookup"><span data-stu-id="a29f5-165">Testing and measuring</span></span>

### <span data-ttu-id="a29f5-166">Testen des Codes</span><span class="sxs-lookup"><span data-stu-id="a29f5-166">Testing your code</span></span>

<span data-ttu-id="a29f5-167">Fügen Sie dem Code Konsolen-API-Test Assertionen hinzu, um Komponententests durchführen und den Code während der Ausführung im Browser Debuggen zu können.</span><span class="sxs-lookup"><span data-stu-id="a29f5-167">Add Console API test assertions to your code for unit testing and debugging your code as it runs in the browser.</span></span>

<span data-ttu-id="a29f5-168">Befehl</span><span class="sxs-lookup"><span data-stu-id="a29f5-168">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="a29f5-169">Assert ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-169">assert()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/assert) | <span data-ttu-id="a29f5-170">Protokolliert eine Fehlermeldung einer Konsole, wenn der bereitgestellte Ausdruck *false*ergibt.</span><span class="sxs-lookup"><span data-stu-id="a29f5-170">Logs a console error message if the provided expression evaluates to *false*.</span></span>

<span data-ttu-id="a29f5-171">Zusätzlich zum logischen Ausdruck, den Sie als testbare Assertion angeben, können Sie eine optionale Nachricht und Formatierungsparameter hinzufügen, wie Sie dies für andere [benutzerdefinierte Konsolen Nachrichten](#logging-custom-messages)verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="a29f5-171">In addition to the logical expression you supply as the testable assertion, you can add an optional message and formatting parameters as you would use with other [custom console messages](#logging-custom-messages).</span></span> <span data-ttu-id="a29f5-172">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a29f5-172">For example:</span></span>

```javascript
var x = 26.8;
console.assert(x < 25, 'The value of x is %f (it is NOT less than %i)', x, 25);
```

![Beispiel für die "Assert"-Methode](../media/console_api_assert.png)

### <span data-ttu-id="a29f5-174">Zählen von Ausführungen im Code</span><span class="sxs-lookup"><span data-stu-id="a29f5-174">Counting executions in your code</span></span>

<span data-ttu-id="a29f5-175">Sie können Indikatoren in Ihrem Code so einstellen, dass Sie nachverfolgen, wie oft der umgebende Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a29f5-175">You can set counters in your code to keep track of how many times the surrounding code gets executed.</span></span> <span data-ttu-id="a29f5-176">Durch das Festlegen von Indikatoren können Sie sicherstellen, dass Ihr Code wie erwartet ausgeführt wird, und Sie bei der Diagnose von Leistungsengpässen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a29f5-176">Setting counters can help ensure your code is running as expected and assist you in diagnosing performance bottlenecks.</span></span>

<span data-ttu-id="a29f5-177">Befehl</span><span class="sxs-lookup"><span data-stu-id="a29f5-177">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="a29f5-178">Anzahl ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-178">count()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/count) | <span data-ttu-id="a29f5-179">Inkrementiert und protokolliert die Anzahl der Male, die *count ()* für die angegebene Bezeichnung ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a29f5-179">Increments and logs the number of times *count()* for the given label has been executed.</span></span>
[**<span data-ttu-id="a29f5-180">countReset()</span><span class="sxs-lookup"><span data-stu-id="a29f5-180">countReset()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/countReset) | <span data-ttu-id="a29f5-181">Setzt die Anzahl für die angegebene Indikator Beschriftung auf NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="a29f5-181">Resets the count to zero for the given counter label.</span></span>

<span data-ttu-id="a29f5-182">So können Sie beispielsweise die folgenden Zeilen in der Konsole ausführen:</span><span class="sxs-lookup"><span data-stu-id="a29f5-182">For example, executing the following lines in console:</span></span>

```javascript
console.count('My Counter');
console.count('My Counter');
console.countReset('My Counter');
console.count('My Counter');
```

 <span data-ttu-id="a29f5-183">.</span><span class="sxs-lookup"><span data-stu-id="a29f5-183">.</span></span> <span data-ttu-id="a29f5-184">.</span><span class="sxs-lookup"><span data-stu-id="a29f5-184">.</span></span> <span data-ttu-id="a29f5-185">.</span><span class="sxs-lookup"><span data-stu-id="a29f5-185">.</span></span> <span data-ttu-id="a29f5-186">führt zu:</span><span class="sxs-lookup"><span data-stu-id="a29f5-186">will result in:</span></span>
> <span data-ttu-id="a29f5-187">Mein Counter: 1</span><span class="sxs-lookup"><span data-stu-id="a29f5-187">My Counter: 1</span></span>

### <span data-ttu-id="a29f5-188">Timing Ihres Codes</span><span class="sxs-lookup"><span data-stu-id="a29f5-188">Timing your code</span></span>

<span data-ttu-id="a29f5-189">Instrumentieren Sie Ihren Code mit beschrifteten Timern, um zu messen, wie lange es dauert, einen bestimmten Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a29f5-189">Instrument your code with labeled timers to measure how long it takes to complete a given operation.</span></span>

<span data-ttu-id="a29f5-190">Befehl</span><span class="sxs-lookup"><span data-stu-id="a29f5-190">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="a29f5-191">Zeit ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-191">time()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/time) | <span data-ttu-id="a29f5-192">Startet einen Zeitgeber mit der angegebenen Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="a29f5-192">Starts a timer with the given label.</span></span>
[**<span data-ttu-id="a29f5-193">timeEnd()</span><span class="sxs-lookup"><span data-stu-id="a29f5-193">timeEnd()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/timeEnd) | <span data-ttu-id="a29f5-194">Beendet den Zeitgeber mit der angegebenen Bezeichnung und meldet die verstrichene Zeit (in Millisekunden).</span><span class="sxs-lookup"><span data-stu-id="a29f5-194">Ends the timer with the given label and reports the time elapsed (in milliseconds).</span></span>
[**<span data-ttu-id="a29f5-195">Timestamp ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-195">timeStamp()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/timeStamp) | <span data-ttu-id="a29f5-196">Meldet die aktuelle Systemzeit (in Millisekunden).</span><span class="sxs-lookup"><span data-stu-id="a29f5-196">Reports the current system time (in milliseconds).</span></span>

<span data-ttu-id="a29f5-197">Versuchen Sie beispielsweise, die folgenden Zeilen in der Konsole auszuführen:</span><span class="sxs-lookup"><span data-stu-id="a29f5-197">For example, try executing the following lines in console:</span></span>

```javascript
console.time('My Timer');
console.timeEnd('My Timer');
```

### <span data-ttu-id="a29f5-198">Erstellen von Heap-Schnappschüssen</span><span class="sxs-lookup"><span data-stu-id="a29f5-198">Taking heap snapshots</span></span>

<span data-ttu-id="a29f5-199">Erstellen Sie Schnappschüsse des Heaps, um den Speicherverbrauch Ihres ausgeführten Codes zu bewerten und Speicherverluste zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a29f5-199">Take snapshots of the heap to assess the memory consumption of your running code and identify memory leaks.</span></span>

<span data-ttu-id="a29f5-200">Befehl</span><span class="sxs-lookup"><span data-stu-id="a29f5-200">Command</span></span> | &nbsp;
:------------ | :-------------
**<span data-ttu-id="a29f5-201">takeHeapSnapshot()</span><span class="sxs-lookup"><span data-stu-id="a29f5-201">takeHeapSnapshot()</span></span>** | <span data-ttu-id="a29f5-202">Zeichnet Details über den aktuellen JavaScript-Heap und die zugeordneten Objekte auf.</span><span class="sxs-lookup"><span data-stu-id="a29f5-202">Captures details about the current JavaScript heap and its allocated objects.</span></span>

<span data-ttu-id="a29f5-203">Der devtools- [Speicher Profiler](../memory.md#toolbar) muss ausgeführt werden, um Heap-Schnappschüsse aufnehmen zu können.</span><span class="sxs-lookup"><span data-stu-id="a29f5-203">The  DevTools [memory profiler](../memory.md#toolbar) must be running in order to take heap snapshots.</span></span> <span data-ttu-id="a29f5-204">Jeder Schnappschuss wird in der [*Zusammenfassung*](../memory.md#snapshot-summary) des [**Speicher**](../memory.md) Bereichs zur weiteren Überprüfung als Kachel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a29f5-204">Each snapshot will appear as a tile in the [*Snapshot summary*](../memory.md#snapshot-summary) of the [**Memory**](../memory.md) panel for further inspection.</span></span>

## <span data-ttu-id="a29f5-205">Ablauf Verfolgungs callstacks</span><span class="sxs-lookup"><span data-stu-id="a29f5-205">Tracing callstacks</span></span>

<span data-ttu-id="a29f5-206">Verstehen, woher der Code aufgerufen wird, welcher Code ausgeführt wird und wie lange die Ausführung dauert, kann hilfreich sein, um Langsamkeit oder unerwartetes Verhalten zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="a29f5-206">Understanding where your code is being called from, what code is running, and how long that execution takes can be useful in analyzing slowness or unexpected behavior.</span></span> <span data-ttu-id="a29f5-207">Eine Stapelüberwachung zeigt Ihnen den Ausführungspfad, den Ihr Code zum Erreichen des Codes benötigte, von der Ablaufverfolgungsanforderung aufwärts durch den Pfad.</span><span class="sxs-lookup"><span data-stu-id="a29f5-207">A stack trace shows you the execution path your code took to reach it, from the trace request upward through the path.</span></span> 

<span data-ttu-id="a29f5-208">Befehl</span><span class="sxs-lookup"><span data-stu-id="a29f5-208">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="a29f5-209">Trace ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-209">trace()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/trace) | <span data-ttu-id="a29f5-210">Gibt eine Ablaufverfolgung der aktuellen Skript Ausführungs callstack aus.</span><span class="sxs-lookup"><span data-stu-id="a29f5-210">Outputs a trace of the current script execution callstack.</span></span>

<span data-ttu-id="a29f5-211">Führen Sie beispielsweise den folgenden Code in der Konsole aus:</span><span class="sxs-lookup"><span data-stu-id="a29f5-211">For example, running the following code in the console:</span></span>

```javascript
function a(){
  c();
}
function b(){
  c();
}
function c(){
  console.trace()
}
function d(){
  b();
}

a();
d();
```

<span data-ttu-id="a29f5-212">.</span><span class="sxs-lookup"><span data-stu-id="a29f5-212">.</span></span> <span data-ttu-id="a29f5-213">.</span><span class="sxs-lookup"><span data-stu-id="a29f5-213">.</span></span> <span data-ttu-id="a29f5-214">.</span><span class="sxs-lookup"><span data-stu-id="a29f5-214">.</span></span> <span data-ttu-id="a29f5-215">Gibt die folgenden Stapelablaufverfolgungen aus:</span><span class="sxs-lookup"><span data-stu-id="a29f5-215">will output the following stack traces:</span></span>
> <span data-ttu-id="a29f5-216">Console. Trace () bei c (eval Code: 8:3) at a (eval Code: 2:3) at eval Code (eval Code: 14:1)</span><span class="sxs-lookup"><span data-stu-id="a29f5-216">console.trace() at c (eval code:8:3) at a (eval code:2:3) at eval code (eval code:14:1)</span></span>
> 
> <span data-ttu-id="a29f5-217">Console. Trace () bei c (eval Code: 8:3) at b (eval Code: 5:3) at d (eval Code: 11:3) at eval Code (eval Code: 15:1)</span><span class="sxs-lookup"><span data-stu-id="a29f5-217">console.trace() at c (eval code:8:3) at b (eval code:5:3) at d (eval code:11:3) at eval code (eval code:15:1)</span></span>

## <span data-ttu-id="a29f5-218">Organisieren der Protokollausgabe</span><span class="sxs-lookup"><span data-stu-id="a29f5-218">Organizing log output</span></span>

<span data-ttu-id="a29f5-219">Um die gesamte vorherige Konsolenausgabe einfach zu löschen, verwenden Sie *Console. Clear ()* (oder `CTRL + L` ).</span><span class="sxs-lookup"><span data-stu-id="a29f5-219">To simply clear all previous console output, use *console.clear()* (or `CTRL + L`).</span></span> <span data-ttu-id="a29f5-220">Dadurch wird der BackStack des befehlsverlaufs der Konsole nicht gelöscht (Sie können ihn weiterhin mit der nach-oben-und nach-unten-Taste durchlaufen).</span><span class="sxs-lookup"><span data-stu-id="a29f5-220">This does not clear the backstack of your console command history (you can still traverse it with the up and down arrow keys).</span></span>

<span data-ttu-id="a29f5-221">Befehl</span><span class="sxs-lookup"><span data-stu-id="a29f5-221">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="a29f5-222">Clear ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-222">clear()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/clear) | <span data-ttu-id="a29f5-223">Löscht alle vorherigen Konsolenausgaben.</span><span class="sxs-lookup"><span data-stu-id="a29f5-223">Clears all previous console output.</span></span>

<span data-ttu-id="a29f5-224">Wenn Ihr Code viele Konsolen Nachrichten ausgibt, können Sie ihn mit den folgenden Befehlen visuell in geschachtelte Blöcke organisieren:</span><span class="sxs-lookup"><span data-stu-id="a29f5-224">If your code outputs a lot of console messages, you can visually organize them into nested blocks with the following commands:</span></span>

 <span data-ttu-id="a29f5-225">Befehl</span><span class="sxs-lookup"><span data-stu-id="a29f5-225">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="a29f5-226">Group ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-226">group()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/group) | <span data-ttu-id="a29f5-227">Startet eine neue Schachtelungsebene für die Konsolenausgabe mit der angegebenen (optionalen) Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="a29f5-227">Starts a new level of nesting for console output with the specified (optional) label.</span></span>
[**<span data-ttu-id="a29f5-228">groupCollapsed()</span><span class="sxs-lookup"><span data-stu-id="a29f5-228">groupCollapsed()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/groupCollapsed) | <span data-ttu-id="a29f5-229">Startet eine neue Schachtelungsebene für die Konsolenausgabe mit der angegebenen (optionalen) Bezeichnung, das Gruppierungssteuerelement wird jedoch standardmäßig reduziert und muss erweitert werden (durch Klicken auf das Pfeil-Steuerelement), um die untergeordnete Ausgabe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a29f5-229">Starts a new level of nesting for console output with the specified (optional) label, however the grouping control is collapsed by default and must be expanded (by clicking on the arrow control) to display the child output.</span></span>
[**<span data-ttu-id="a29f5-230">groupEnd()</span><span class="sxs-lookup"><span data-stu-id="a29f5-230">groupEnd()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/groupEnd) | <span data-ttu-id="a29f5-231">Beendet die Schachtelungs Gruppe für die angegebene Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="a29f5-231">Ends the nesting group for the specified label.</span></span>

<span data-ttu-id="a29f5-232">Versuchen Sie beispielsweise, die folgenden Befehle in der Konsole einzugeben:</span><span class="sxs-lookup"><span data-stu-id="a29f5-232">For example, try entering the following commands in the console:</span></span>

```javascript
console.groupCollapsed('Group 1');
console.log('In Group 1');
console.groupCollapsed('Group 1.1');
console.log('In Group 1.1');
console.groupEnd('Group 1.1');
console.groupEnd('Group 1');
console.log('No longer in a group');
```

<span data-ttu-id="a29f5-233">.</span><span class="sxs-lookup"><span data-stu-id="a29f5-233">.</span></span> <span data-ttu-id="a29f5-234">.</span><span class="sxs-lookup"><span data-stu-id="a29f5-234">.</span></span> <span data-ttu-id="a29f5-235">.</span><span class="sxs-lookup"><span data-stu-id="a29f5-235">.</span></span> <span data-ttu-id="a29f5-236">und erweitern Sie dann die Steuerelemente *Gruppe 1* und *Gruppe 1,1* , um zu sehen, wie die Protokoll Kommentare geschachtelt sind:</span><span class="sxs-lookup"><span data-stu-id="a29f5-236">and then expand the *Group 1* and *Group 1.1* controls to see how the log comments are nested:</span></span>

![Gruppieren von Nachrichten in der Konsole](../media/console_api_group.png)

<span data-ttu-id="a29f5-238">Manchmal ist es einfacher, ein JavaScript-Objekt oder-Array in tabellarischer Form zu visualisieren, anstatt eine flache Liste zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a29f5-238">Sometimes its easier to visualize a JavaScript object or array in tabular form, rather than a flat list.</span></span> <span data-ttu-id="a29f5-239">Dazu können Sie den Befehl *Console. Table ()* verwenden:</span><span class="sxs-lookup"><span data-stu-id="a29f5-239">For that, you can use the *console.table()* command:</span></span>

<span data-ttu-id="a29f5-240">Befehl</span><span class="sxs-lookup"><span data-stu-id="a29f5-240">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="a29f5-241">Tabelle ()</span><span class="sxs-lookup"><span data-stu-id="a29f5-241">table()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/table) | <span data-ttu-id="a29f5-242">Gibt das angegebene Array oder Objekt in tabellarischer Form an die Konsole aus.</span><span class="sxs-lookup"><span data-stu-id="a29f5-242">Outputs the supplied array or object to the console in tabular form.</span></span>

<span data-ttu-id="a29f5-243">Beispielsweise das folgende Object-Array:</span><span class="sxs-lookup"><span data-stu-id="a29f5-243">For example, the following object array:</span></span>

```javascript
var orders = [{'Size':'XL', 'Quantity':1},{'Size':'M', 'Quantity':3}, {'Size':'L', 'Quantity':2}];
console.table(orders);
```

<span data-ttu-id="a29f5-244">.</span><span class="sxs-lookup"><span data-stu-id="a29f5-244">.</span></span> <span data-ttu-id="a29f5-245">.</span><span class="sxs-lookup"><span data-stu-id="a29f5-245">.</span></span> <span data-ttu-id="a29f5-246">.</span><span class="sxs-lookup"><span data-stu-id="a29f5-246">.</span></span> <span data-ttu-id="a29f5-247">wird als Tabelle in der Konsole gerendert:</span><span class="sxs-lookup"><span data-stu-id="a29f5-247">will render as this table in the console:</span></span>

![Anzeigen eines Objektarrays als Tabelle in der Konsole](../media/console_api_table.png)

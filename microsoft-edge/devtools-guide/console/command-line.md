---
description: Verwenden der Konsolen Befehlszeile für die Interaktion mit einer ausgeführten Seite
title: DevTools-Console-Befehlszeile
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Befehlszeile der Konsole
ms.custom: seodec18
ms.openlocfilehash: c661736e5ea264f60279c89cfa0f9c55361d2288
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568456"
---
# <span data-ttu-id="02ddf-104">Befehlszeile der Konsole</span><span class="sxs-lookup"><span data-stu-id="02ddf-104">Console command line</span></span>

<span data-ttu-id="02ddf-105">Verwenden Sie die Befehlszeile der Konsole, um Werte auf einer Seite anzuzeigen und zu ändern, und führen Sie im Handumdrehen Debugcode aus, während Sie alle die Vorteile der automatischen Codevervollständigung in Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) nutzen.</span><span class="sxs-lookup"><span data-stu-id="02ddf-105">Use the Console command line to view and change values on a page and execute debug code on the fly, all while taking advantage of Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) auto code completion.</span></span> 

<span data-ttu-id="02ddf-106">Geben Sie einfach ein beliebiges gültiges JavaScript an der Eingabeaufforderung ein, und drücken Sie `Enter` zum Ausführen.</span><span class="sxs-lookup"><span data-stu-id="02ddf-106">Simply enter any valid JavaScript at the command line prompt and press `Enter` to execute.</span></span> <span data-ttu-id="02ddf-107">Verwenden Sie die mehrzeiligen Eingabe `Shift+Enter` , um eine Zeile zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="02ddf-107">For multi-line input use `Shift+Enter` to add a line-break.</span></span> <span data-ttu-id="02ddf-108">Verwenden `Up` Sie die `Down` Pfeiltasten, um durch die vorherigen Konsolenbefehle zu navigieren, die Sie während der aktuellen devtools-Sitzung eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="02ddf-108">Use the `Up` and `Down` arrow keys to navigate through previous console commands you entered during the current  DevTools session.</span></span> <span data-ttu-id="02ddf-109">Neben dem Standard-JavaScript und der [Konsolen-API](./console-api.md)unterstützt die Konsole auch die folgenden Befehle für:</span><span class="sxs-lookup"><span data-stu-id="02ddf-109">In addition to standard JavaScript and the [Console API](./console-api.md), the Console also supports the following commands for:</span></span>

 - [<span data-ttu-id="02ddf-110">Auswählen von DOM-Objekten</span><span class="sxs-lookup"><span data-stu-id="02ddf-110">Selecting DOM objects</span></span>](#dom-selectors)
 - [<span data-ttu-id="02ddf-111">Überprüfen von Objekteigenschaften</span><span class="sxs-lookup"><span data-stu-id="02ddf-111">Inspecting object properties</span></span>](#object-inspection)
 - [<span data-ttu-id="02ddf-112">Auffinden aller Ereignis-Listener für ein bestimmtes Objekt</span><span class="sxs-lookup"><span data-stu-id="02ddf-112">Finding all the event listeners on a given object</span></span>](#event-listeners)

<span data-ttu-id="02ddf-113">Das in die Befehlszeile eingegebene Skript wird im [globalen Bereich](/scripting/javascript/advanced/variable-scope-javascript) des aktuell ausgewählten Fensters ausgeführt, es sei denn, die Seite wird an einem Haltepunkt angehalten.</span><span class="sxs-lookup"><span data-stu-id="02ddf-113">Script entered in the command line executes in the [global scope](/scripting/javascript/advanced/variable-scope-javascript) of the currently selected window, unless the page is paused at a breakpoint.</span></span> <span data-ttu-id="02ddf-114">Die während der angehenden Seite eingegebenen Konsolenbefehle werden im [lokalen Bereich](/scripting/javascript/advanced/variable-scope-javascript) der aktuellen Funktion innerhalb der Aufrufliste ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02ddf-114">Console commands entered while the page is paused will execute in the [local scope](/scripting/javascript/advanced/variable-scope-javascript) of the current function within the call stack.</span></span>

<span data-ttu-id="02ddf-115">Die Konsole hat eine Dropdownliste für den **Ziel** Ausführungskontext direkt oberhalb des Ausgabebereichs der Konsole.</span><span class="sxs-lookup"><span data-stu-id="02ddf-115">The Console has a **Target** execution context drop-down just above the Console output area.</span></span> <span data-ttu-id="02ddf-116">Die Standardauswahl ist das Dokument auf oberster Ebene, **_top**.</span><span class="sxs-lookup"><span data-stu-id="02ddf-116">The default selection is the top-level document, **_top**.</span></span> <span data-ttu-id="02ddf-117">Alle iframes im Dokument oder in ausgeführten Erweiterungen werden auch als Optionen angezeigt, sodass Sie abwechselnd Befehle in diesen Bereichen ausführen können.</span><span class="sxs-lookup"><span data-stu-id="02ddf-117">Any iframes in the document or running extensions will also appear as options, allowing you to alternately run commands within those scopes.</span></span>

## <span data-ttu-id="02ddf-118">Dom-Auswahlen</span><span class="sxs-lookup"><span data-stu-id="02ddf-118">DOM selectors</span></span>
<span data-ttu-id="02ddf-119">Diese Konsolen Auswahl bietet einfache Abkürzungen für den schnellen Zugriff auf Objekte innerhalb des Dom:</span><span class="sxs-lookup"><span data-stu-id="02ddf-119">These console selectors provide simple shorthands for quickly accessing objects within the DOM:</span></span>

### <span data-ttu-id="02ddf-120">$ (*CSS-Auswahlzeichenfolge*)</span><span class="sxs-lookup"><span data-stu-id="02ddf-120">$(*CSS selector string*)</span></span>
<span data-ttu-id="02ddf-121">Gibt das erste Element innerhalb des Dokuments zurück, das der angegebenen [CSS-Auswahl](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors) Zeichenfolge (oder einer durch Trennzeichen getrennten Gruppe von Selektoren) entspricht.</span><span class="sxs-lookup"><span data-stu-id="02ddf-121">Returns the first element within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="02ddf-122">Kurzform für [Document. querySelector ()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span><span class="sxs-lookup"><span data-stu-id="02ddf-122">Shorthand for [document.querySelector()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span></span>

<span data-ttu-id="02ddf-123">Beispiel: Öffnen Sie die Konsole, und geben `$('#main')` Sie ein, um das DIV-Objekt `id='main'` auf dieser Seite zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="02ddf-123">Example: Open the console and type `$('#main')` to return the div object with `id='main'` on this page.</span></span>

![Beispiel für die Verwendung von "$"-Auswahl](../media/console_cmd_$.png)

### <span data-ttu-id="02ddf-125">$ $ (*CSS-Auswahlzeichenfolge*)</span><span class="sxs-lookup"><span data-stu-id="02ddf-125">$$(*CSS selector string*)</span></span>
<span data-ttu-id="02ddf-126">Gibt ein Array von Elementen innerhalb des Dokuments zurück, die der angegebenen [CSS-Auswahl](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors) Zeichenfolge (oder einer durch Trennzeichen getrennten Gruppe von Selektoren) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="02ddf-126">Returns an array of elements within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="02ddf-127">Kurzform für [Document. querySelectorAll ()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span><span class="sxs-lookup"><span data-stu-id="02ddf-127">Shorthand for [document.querySelectorAll()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span></span>

<span data-ttu-id="02ddf-128">Beispiel: Öffnen Sie die Konsole, und geben `$$('.container')` Sie ein, um alle div-Objekte `class='container'` auf dieser Seite zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="02ddf-128">Example: Open the console and type `$$('.container')` to return all the div objects with `class='container'` on this page.</span></span>

![Beispiel für die Verwendung von "$ $"-Auswahl](../media/console_cmd_$$.png)

### <span data-ttu-id="02ddf-130">$0, $1, $2,...</span><span class="sxs-lookup"><span data-stu-id="02ddf-130">$0, $1, $2,...</span></span>
<span data-ttu-id="02ddf-131">Gibt die letzten Elemente zurück, die im Bereich " [**Elemente**](../elements.md) " ausgewählt sind, wobei `$0` das aktuell ausgewählte Element, `$1` das ausgewählte Element davor usw. ist.</span><span class="sxs-lookup"><span data-stu-id="02ddf-131">Returns the last elements selected in the [**Elements**](../elements.md) panel, where `$0` represents the currently selected item, `$1` was the selected item before that, and so on.</span></span>

<span data-ttu-id="02ddf-132">Beispiel: Öffnen Sie devtools auf der Registerkarte **Elemente** , drücken Sie, `CTRL + B` um das Tool **Element auswählen** zu aktivieren, und klicken Sie mit der Maus auf einen Bereich auf dieser Seite.</span><span class="sxs-lookup"><span data-stu-id="02ddf-132">Example: Open  DevTools to the **Elements** tab, press `CTRL + B` to activate the **Select element** tool and click some area on this page with your mouse.</span></span> <span data-ttu-id="02ddf-133">Öffnen Sie nun die Konsole, und geben `$0` Sie ein, um das Element zurückzugeben, auf das Sie gerade geklickt haben.</span><span class="sxs-lookup"><span data-stu-id="02ddf-133">Now open the Console and type `$0` to return the element you just clicked.</span></span>

![Beispiel für die Verwendung der Auswahl "$0"](../media/console_cmd_$0.png)

### <span data-ttu-id="02ddf-135">$x (*XPath-Ausdruck*)</span><span class="sxs-lookup"><span data-stu-id="02ddf-135">$x(*XPath expression*)</span></span>
<span data-ttu-id="02ddf-136">Gibt ein Array von Elementen zurück, die mit dem angegebenen [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) -Ausdruck übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="02ddf-136">Returns an array of elements matched by the specified [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) expression.</span></span> 

<span data-ttu-id="02ddf-137">Beispiel: Öffnen Sie die Konsole, und geben `$x('//script[@defer]')` Sie ein, um alle `<script>` Elemente auf dieser Seite zurückzugeben, die ein `defer` Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="02ddf-137">Example: Open the console and type `$x('//script[@defer]')` to return all the `<script>` elements on this page that contain a `defer` attribute.</span></span>

![Beispiel für die Verwendung der Auswahl "$x"](../media/console_cmd_$x.png)

## <span data-ttu-id="02ddf-139">Objektprüfung</span><span class="sxs-lookup"><span data-stu-id="02ddf-139">Object inspection</span></span>

<span data-ttu-id="02ddf-140">Diese Befehle bieten schnelle Möglichkeiten zum Überprüfen der Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="02ddf-140">These commands provide quick ways to inspect the properties of an object.</span></span> <span data-ttu-id="02ddf-141">Das angegebene Objekt muss entweder im globalen Namespace oder im aktuellen Bereich des Debuggers definiert sein.</span><span class="sxs-lookup"><span data-stu-id="02ddf-141">The specified object must either be defined in the global namespace or the current scope of the debugger.</span></span>

### <span data-ttu-id="02ddf-142">dir (*Objekt*)</span><span class="sxs-lookup"><span data-stu-id="02ddf-142">dir(*object*)</span></span>
<span data-ttu-id="02ddf-143">Gibt eine Strukturansicht-Liste der Eigenschaften für das angegebene Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="02ddf-143">Returns a tree view list of properties for the specified object.</span></span>

<span data-ttu-id="02ddf-144">Beispiel: Öffnen Sie die Konsole, und geben `dir(document)` Sie die Objekteigenschaften für das Dokumentobjekt ein, das diese Seite darstellt.</span><span class="sxs-lookup"><span data-stu-id="02ddf-144">Example: Open the console and type `dir(document)` to see the object properties for the document object representing this page.</span></span>

![Beispiel für die Verwendung der "dir"-Methode](../media/console_cmd_dir.png)

### <span data-ttu-id="02ddf-146">Keys (*Objekt*)</span><span class="sxs-lookup"><span data-stu-id="02ddf-146">keys(*object*)</span></span>
<span data-ttu-id="02ddf-147">Gibt ein Array von Eigenschaftennamen zurück, die dem angegebenen Objekt angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="02ddf-147">Returns an array of property names attached to the specified object.</span></span>

<span data-ttu-id="02ddf-148">Beispiel: Öffnen Sie die Konsole, und geben `keys(window)` Sie einen Wert ein, um alle Eigenschaften zurückzugeben, die für das globale Fensterobjekt definiert sind.</span><span class="sxs-lookup"><span data-stu-id="02ddf-148">Example: Open the console and type `keys(window)` to return all of the properties defined on the global window object.</span></span>

![Beispiel für die Verwendung der "Keys"-Methode](../media/console_cmd_keys.png)

### <span data-ttu-id="02ddf-150">Werte (*Objekt*)</span><span class="sxs-lookup"><span data-stu-id="02ddf-150">values(*object*)</span></span>
<span data-ttu-id="02ddf-151">Gibt ein Array von Eigenschaftswerten zurück, die an das angegebene Objekt angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="02ddf-151">Returns an array of property values attached to the specified object.</span></span>

<span data-ttu-id="02ddf-152">Beispiel: Öffnen Sie die Konsole, und geben `values(window)` Sie die Werte aller Eigenschaften (Schlüssel) zurück, die für das globale Fensterobjekt definiert sind.</span><span class="sxs-lookup"><span data-stu-id="02ddf-152">Example: Open the console and type `values(window)` to return the values of all the properties (keys) defined on the global window object.</span></span>

![Beispiel für die Verwendung der "Values"-Methode](../media/console_cmd_values.png)

## <span data-ttu-id="02ddf-154">Ereignis-Listener</span><span class="sxs-lookup"><span data-stu-id="02ddf-154">Event listeners</span></span>

<span data-ttu-id="02ddf-155">Mit diesem Befehl können Sie die für ein bestimmtes Objekt registrierten Ereignislistener untersuchen.</span><span class="sxs-lookup"><span data-stu-id="02ddf-155">This command allows you to inspect the event listeners registered to a given object.</span></span> <span data-ttu-id="02ddf-156">Das angegebene Objekt muss entweder im globalen Namespace oder im aktuellen Bereich des Debuggers definiert sein.</span><span class="sxs-lookup"><span data-stu-id="02ddf-156">The specified object must either be defined in the global namespace or the current scope of the  debugger.</span></span>

### <span data-ttu-id="02ddf-157">getEventListeners (*Objekt*)</span><span class="sxs-lookup"><span data-stu-id="02ddf-157">getEventListeners(*object*)</span></span>
<span data-ttu-id="02ddf-158">Gibt ein Objekt zurück, das einen Schlüssel für die einzelnen registrierten Ereignistypen für das angegebene Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="02ddf-158">Returns an object containing a key for each registered event type on the given object.</span></span> <span data-ttu-id="02ddf-159">Der Wert der einzelnen Schlüssel ist ein Array von Ereignislistener und zugehörigen Informationen.</span><span class="sxs-lookup"><span data-stu-id="02ddf-159">The value of each key is an array of event listeners and their related info.</span></span> 

<span data-ttu-id="02ddf-160">Beispiel: Öffnen Sie die Konsole, und geben `getEventListeners(document)` Sie ein, um alle Ereignislistener anzuzeigen, die für das Document-Objekt dieser Seite registriert sind.</span><span class="sxs-lookup"><span data-stu-id="02ddf-160">Example: Open the console and type `getEventListeners(document)` to see all the event listeners registered on the document object of this page.</span></span>

![Beispiel für die Verwendung der "getEventListeners"-Methode](../media/console_cmd_getEventListeners.png)

---
description: Use the Console command line to interact with a running page
title: DevTools - Console - Command Line
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, console command line
ms.custom: seodec18
ms.openlocfilehash: c661736e5ea264f60279c89cfa0f9c55361d2288
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568456"
---
# <span data-ttu-id="12159-104">Console command line</span><span class="sxs-lookup"><span data-stu-id="12159-104">Console command line</span></span>

<span data-ttu-id="12159-105">Use the Console command line to view and change values on a page and execute debug code on the fly, all while taking advantage of Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) auto code completion.</span><span class="sxs-lookup"><span data-stu-id="12159-105">Use the Console command line to view and change values on a page and execute debug code on the fly, all while taking advantage of Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) auto code completion.</span></span> 

<span data-ttu-id="12159-106">Simply enter any valid JavaScript at the command line prompt and press `Enter` to execute.</span><span class="sxs-lookup"><span data-stu-id="12159-106">Simply enter any valid JavaScript at the command line prompt and press `Enter` to execute.</span></span> <span data-ttu-id="12159-107">For multi-line input use `Shift+Enter` to add a line-break.</span><span class="sxs-lookup"><span data-stu-id="12159-107">For multi-line input use `Shift+Enter` to add a line-break.</span></span> <span data-ttu-id="12159-108">Use the `Up` and `Down` arrow keys to navigate through previous console commands you entered during the current  DevTools session.</span><span class="sxs-lookup"><span data-stu-id="12159-108">Use the `Up` and `Down` arrow keys to navigate through previous console commands you entered during the current  DevTools session.</span></span> <span data-ttu-id="12159-109">In addition to standard JavaScript and the [Console API](./console-api.md), the Console also supports the following commands for:</span><span class="sxs-lookup"><span data-stu-id="12159-109">In addition to standard JavaScript and the [Console API](./console-api.md), the Console also supports the following commands for:</span></span>

 - [<span data-ttu-id="12159-110">Selecting DOM objects</span><span class="sxs-lookup"><span data-stu-id="12159-110">Selecting DOM objects</span></span>](#dom-selectors)
 - [<span data-ttu-id="12159-111">Inspecting object properties</span><span class="sxs-lookup"><span data-stu-id="12159-111">Inspecting object properties</span></span>](#object-inspection)
 - [<span data-ttu-id="12159-112">Finding all the event listeners on a given object</span><span class="sxs-lookup"><span data-stu-id="12159-112">Finding all the event listeners on a given object</span></span>](#event-listeners)

<span data-ttu-id="12159-113">Script entered in the command line executes in the [global scope](/scripting/javascript/advanced/variable-scope-javascript) of the currently selected window, unless the page is paused at a breakpoint.</span><span class="sxs-lookup"><span data-stu-id="12159-113">Script entered in the command line executes in the [global scope](/scripting/javascript/advanced/variable-scope-javascript) of the currently selected window, unless the page is paused at a breakpoint.</span></span> <span data-ttu-id="12159-114">Console commands entered while the page is paused will execute in the [local scope](/scripting/javascript/advanced/variable-scope-javascript) of the current function within the call stack.</span><span class="sxs-lookup"><span data-stu-id="12159-114">Console commands entered while the page is paused will execute in the [local scope](/scripting/javascript/advanced/variable-scope-javascript) of the current function within the call stack.</span></span>

<span data-ttu-id="12159-115">The Console has a **Target** execution context drop-down just above the Console output area.</span><span class="sxs-lookup"><span data-stu-id="12159-115">The Console has a **Target** execution context drop-down just above the Console output area.</span></span> <span data-ttu-id="12159-116">The default selection is the top-level document, **_top**.</span><span class="sxs-lookup"><span data-stu-id="12159-116">The default selection is the top-level document, **_top**.</span></span> <span data-ttu-id="12159-117">Any iframes in the document or running extensions will also appear as options, allowing you to alternately run commands within those scopes.</span><span class="sxs-lookup"><span data-stu-id="12159-117">Any iframes in the document or running extensions will also appear as options, allowing you to alternately run commands within those scopes.</span></span>

## <span data-ttu-id="12159-118">DOM selectors</span><span class="sxs-lookup"><span data-stu-id="12159-118">DOM selectors</span></span>
<span data-ttu-id="12159-119">These console selectors provide simple shorthands for quickly accessing objects within the DOM:</span><span class="sxs-lookup"><span data-stu-id="12159-119">These console selectors provide simple shorthands for quickly accessing objects within the DOM:</span></span>

### <span data-ttu-id="12159-120">$(*CSS selector string*)</span><span class="sxs-lookup"><span data-stu-id="12159-120">$(*CSS selector string*)</span></span>
<span data-ttu-id="12159-121">Returns the first element within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span><span class="sxs-lookup"><span data-stu-id="12159-121">Returns the first element within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="12159-122">Shorthand for [document.querySelector()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span><span class="sxs-lookup"><span data-stu-id="12159-122">Shorthand for [document.querySelector()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span></span>

<span data-ttu-id="12159-123">Example: Open the console and type `$('#main')` to return the div object with `id='main'` on this page.</span><span class="sxs-lookup"><span data-stu-id="12159-123">Example: Open the console and type `$('#main')` to return the div object with `id='main'` on this page.</span></span>

![Example use of '$' selector](../media/console_cmd_$.png)

### <span data-ttu-id="12159-125">$$(*CSS selector string*)</span><span class="sxs-lookup"><span data-stu-id="12159-125">$$(*CSS selector string*)</span></span>
<span data-ttu-id="12159-126">Returns an array of elements within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span><span class="sxs-lookup"><span data-stu-id="12159-126">Returns an array of elements within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="12159-127">Shorthand for [document.querySelectorAll()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span><span class="sxs-lookup"><span data-stu-id="12159-127">Shorthand for [document.querySelectorAll()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span></span>

<span data-ttu-id="12159-128">Example: Open the console and type `$$('.container')` to return all the div objects with `class='container'` on this page.</span><span class="sxs-lookup"><span data-stu-id="12159-128">Example: Open the console and type `$$('.container')` to return all the div objects with `class='container'` on this page.</span></span>

![Example use of '$$' selector](../media/console_cmd_$$.png)

### <span data-ttu-id="12159-130">$0, $1, $2,...</span><span class="sxs-lookup"><span data-stu-id="12159-130">$0, $1, $2,...</span></span>
<span data-ttu-id="12159-131">Returns the last elements selected in the [**Elements**](../elements.md) panel, where `$0` represents the currently selected item, `$1` was the selected item before that, and so on.</span><span class="sxs-lookup"><span data-stu-id="12159-131">Returns the last elements selected in the [**Elements**](../elements.md) panel, where `$0` represents the currently selected item, `$1` was the selected item before that, and so on.</span></span>

<span data-ttu-id="12159-132">Example: Open  DevTools to the **Elements** tab, press `CTRL + B` to activate the **Select element** tool and click some area on this page with your mouse.</span><span class="sxs-lookup"><span data-stu-id="12159-132">Example: Open  DevTools to the **Elements** tab, press `CTRL + B` to activate the **Select element** tool and click some area on this page with your mouse.</span></span> <span data-ttu-id="12159-133">Now open the Console and type `$0` to return the element you just clicked.</span><span class="sxs-lookup"><span data-stu-id="12159-133">Now open the Console and type `$0` to return the element you just clicked.</span></span>

![Example use of '$0' selector](../media/console_cmd_$0.png)

### <span data-ttu-id="12159-135">$x(*XPath expression*)</span><span class="sxs-lookup"><span data-stu-id="12159-135">$x(*XPath expression*)</span></span>
<span data-ttu-id="12159-136">Returns an array of elements matched by the specified [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) expression.</span><span class="sxs-lookup"><span data-stu-id="12159-136">Returns an array of elements matched by the specified [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) expression.</span></span> 

<span data-ttu-id="12159-137">Example: Open the console and type `$x('//script[@defer]')` to return all the `<script>` elements on this page that contain a `defer` attribute.</span><span class="sxs-lookup"><span data-stu-id="12159-137">Example: Open the console and type `$x('//script[@defer]')` to return all the `<script>` elements on this page that contain a `defer` attribute.</span></span>

![Example use of '$x' selector](../media/console_cmd_$x.png)

## <span data-ttu-id="12159-139">Object inspection</span><span class="sxs-lookup"><span data-stu-id="12159-139">Object inspection</span></span>

<span data-ttu-id="12159-140">These commands provide quick ways to inspect the properties of an object.</span><span class="sxs-lookup"><span data-stu-id="12159-140">These commands provide quick ways to inspect the properties of an object.</span></span> <span data-ttu-id="12159-141">The specified object must either be defined in the global namespace or the current scope of the debugger.</span><span class="sxs-lookup"><span data-stu-id="12159-141">The specified object must either be defined in the global namespace or the current scope of the debugger.</span></span>

### <span data-ttu-id="12159-142">dir(*object*)</span><span class="sxs-lookup"><span data-stu-id="12159-142">dir(*object*)</span></span>
<span data-ttu-id="12159-143">Returns a tree view list of properties for the specified object.</span><span class="sxs-lookup"><span data-stu-id="12159-143">Returns a tree view list of properties for the specified object.</span></span>

<span data-ttu-id="12159-144">Example: Open the console and type `dir(document)` to see the object properties for the document object representing this page.</span><span class="sxs-lookup"><span data-stu-id="12159-144">Example: Open the console and type `dir(document)` to see the object properties for the document object representing this page.</span></span>

![Example use of 'dir' method](../media/console_cmd_dir.png)

### <span data-ttu-id="12159-146">keys(*object*)</span><span class="sxs-lookup"><span data-stu-id="12159-146">keys(*object*)</span></span>
<span data-ttu-id="12159-147">Returns an array of property names attached to the specified object.</span><span class="sxs-lookup"><span data-stu-id="12159-147">Returns an array of property names attached to the specified object.</span></span>

<span data-ttu-id="12159-148">Example: Open the console and type `keys(window)` to return all of the properties defined on the global window object.</span><span class="sxs-lookup"><span data-stu-id="12159-148">Example: Open the console and type `keys(window)` to return all of the properties defined on the global window object.</span></span>

![Example use of 'keys' method](../media/console_cmd_keys.png)

### <span data-ttu-id="12159-150">values(*object*)</span><span class="sxs-lookup"><span data-stu-id="12159-150">values(*object*)</span></span>
<span data-ttu-id="12159-151">Returns an array of property values attached to the specified object.</span><span class="sxs-lookup"><span data-stu-id="12159-151">Returns an array of property values attached to the specified object.</span></span>

<span data-ttu-id="12159-152">Example: Open the console and type `values(window)` to return the values of all the properties (keys) defined on the global window object.</span><span class="sxs-lookup"><span data-stu-id="12159-152">Example: Open the console and type `values(window)` to return the values of all the properties (keys) defined on the global window object.</span></span>

![Example use of 'values' method](../media/console_cmd_values.png)

## <span data-ttu-id="12159-154">Event listeners</span><span class="sxs-lookup"><span data-stu-id="12159-154">Event listeners</span></span>

<span data-ttu-id="12159-155">This command allows you to inspect the event listeners registered to a given object.</span><span class="sxs-lookup"><span data-stu-id="12159-155">This command allows you to inspect the event listeners registered to a given object.</span></span> <span data-ttu-id="12159-156">The specified object must either be defined in the global namespace or the current scope of the  debugger.</span><span class="sxs-lookup"><span data-stu-id="12159-156">The specified object must either be defined in the global namespace or the current scope of the  debugger.</span></span>

### <span data-ttu-id="12159-157">getEventListeners(*object*)</span><span class="sxs-lookup"><span data-stu-id="12159-157">getEventListeners(*object*)</span></span>
<span data-ttu-id="12159-158">Returns an object containing a key for each registered event type on the given object.</span><span class="sxs-lookup"><span data-stu-id="12159-158">Returns an object containing a key for each registered event type on the given object.</span></span> <span data-ttu-id="12159-159">The value of each key is an array of event listeners and their related info.</span><span class="sxs-lookup"><span data-stu-id="12159-159">The value of each key is an array of event listeners and their related info.</span></span> 

<span data-ttu-id="12159-160">Example: Open the console and type `getEventListeners(document)` to see all the event listeners registered on the document object of this page.</span><span class="sxs-lookup"><span data-stu-id="12159-160">Example: Open the console and type `getEventListeners(document)` to see all the event listeners registered on the document object of this page.</span></span>

![Example use of 'getEventListeners' method](../media/console_cmd_getEventListeners.png)

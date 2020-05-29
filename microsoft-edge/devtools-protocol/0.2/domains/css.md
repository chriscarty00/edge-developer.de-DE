---
description: Referenz für die CSS-Domäne Diese Domäne macht CSS-Lese-und Schreibvorgänge verfügbar. Alle CSS-Objekte (Stylesheets, Regeln und Formatvorlagen) verfügen über ein zugeordnetes `id` Objekt, das in nachfolgenden Vorgängen des verknüpften Objekts verwendet wird. Jeder Objekttyp hat eine bestimmte `id` Struktur, die nicht zwischen Objekten unterschiedlicher Art austauschbar sind. CSS-Objekte können mithilfe der `get*ForNode()` Aufrufe (die eine DOM-Knoten-ID akzeptieren) geladen werden. Ein Client kann über die Ereignisse auch Stylesheets nachverfolgen `styleSheetAdded` / `styleSheetRemoved` und anschließend die erforderlichen Stylesheet-Inhalte mit den `getStyleSheet[Text]()` Methoden laden.
title: CSS-Domäne – devtools-Protokoll Version 0,2
author: pelavall
ms.author: pelavall
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 939eda0ae2f5228657d35899ab75b39493eff917
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567545"
---
# <span data-ttu-id="d043d-108">CSS</span><span class="sxs-lookup"><span data-stu-id="d043d-108">CSS</span></span>
<span data-ttu-id="d043d-109">Diese Domäne macht CSS-Lese-und Schreibvorgänge verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d043d-109">This domain exposes CSS read/write operations.</span></span> <span data-ttu-id="d043d-110">Alle CSS-Objekte (Stylesheets, Regeln und Formatvorlagen) verfügen über ein zugeordnetes `id` Objekt, das in nachfolgenden Vorgängen des verknüpften Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d043d-110">All CSS objects (stylesheets, rules, and styles) have an associated `id` used in subsequent operations on the related object.</span></span> <span data-ttu-id="d043d-111">Jeder Objekttyp hat eine bestimmte `id` Struktur, die nicht zwischen Objekten unterschiedlicher Art austauschbar sind.</span><span class="sxs-lookup"><span data-stu-id="d043d-111">Each object type has a specific `id` structure, and those are not interchangeable between objects of different kinds.</span></span> <span data-ttu-id="d043d-112">CSS-Objekte können mithilfe der `get*ForNode()` Aufrufe (die eine DOM-Knoten-ID akzeptieren) geladen werden.</span><span class="sxs-lookup"><span data-stu-id="d043d-112">CSS objects can be loaded using the `get*ForNode()` calls (which accept a DOM node id).</span></span> <span data-ttu-id="d043d-113">Ein Client kann über die Ereignisse auch Stylesheets nachverfolgen `styleSheetAdded` / `styleSheetRemoved` und anschließend die erforderlichen Stylesheet-Inhalte mit den `getStyleSheet[Text]()` Methoden laden.</span><span class="sxs-lookup"><span data-stu-id="d043d-113">A client can also keep track of stylesheets via the `styleSheetAdded`/`styleSheetRemoved` events and subsequently load the required stylesheet contents using the `getStyleSheet[Text]()` methods.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="d043d-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="d043d-114">Methods</span></span>**](#methods) | <span data-ttu-id="d043d-115">[aktivieren](#enable), [Deaktivieren](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span><span class="sxs-lookup"><span data-stu-id="d043d-115">[enable](#enable), [disable](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span></span> |
| [**<span data-ttu-id="d043d-116">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="d043d-116">Events</span></span>**](#events) | <span data-ttu-id="d043d-117">[styleSheetAdded](#stylesheetadded), [stylesheetd](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span><span class="sxs-lookup"><span data-stu-id="d043d-117">[styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span></span> |
| [**<span data-ttu-id="d043d-118">Typen</span><span class="sxs-lookup"><span data-stu-id="d043d-118">Types</span></span>**](#types) | <span data-ttu-id="d043d-119">[Stylesheet](#stylesheetid)- [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Wert](#value), [selectorlist](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader)</span><span class="sxs-lookup"><span data-stu-id="d043d-119">[StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader)</span></span> |
| [**<span data-ttu-id="d043d-120">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="d043d-120">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="d043d-121">DOM</span><span class="sxs-lookup"><span data-stu-id="d043d-121">DOM</span></span>](dom.md) |
## <span data-ttu-id="d043d-122">Methoden</span><span class="sxs-lookup"><span data-stu-id="d043d-122">Methods</span></span>

### <span data-ttu-id="d043d-123">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="d043d-123">enable</span></span>
<span data-ttu-id="d043d-124">Aktiviert den CSS-Agent für die angegebene Seite.</span><span class="sxs-lookup"><span data-stu-id="d043d-124">Enables the CSS agent for the given page.</span></span> <span data-ttu-id="d043d-125">Clients sollten nicht davon ausgehen, dass der CSS-Agent aktiviert wurde, bis das Ergebnis dieses Befehls empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="d043d-125">Clients should not assume that the CSS agent has been enabled until the result of this command is received.</span></span>

</p>

---

### <span data-ttu-id="d043d-126">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="d043d-126">disable</span></span>
<span data-ttu-id="d043d-127">Deaktiviert den CSS-Agent für die angegebene Seite.</span><span class="sxs-lookup"><span data-stu-id="d043d-127">Disables the CSS agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="d043d-128">getInlineStylesForNode</span><span class="sxs-lookup"><span data-stu-id="d043d-128">getInlineStylesForNode</span></span>
<span data-ttu-id="d043d-129">Gibt die Inline definierten Formatvorlagen (explizit im "Style"-Attribut und implizit unter Verwendung von Dom-Attributen) für einen DOM-Knoten zurück, der von angegeben wird `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="d043d-129">Returns the styles defined inline (explicitly in the "style" attribute and implicitly, using DOM attributes) for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="d043d-130">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-131">NodeId</span><span class="sxs-lookup"><span data-stu-id="d043d-131">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-132">Gibt</span><span class="sxs-lookup"><span data-stu-id="d043d-132">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-133">ininlinestyle</span><span class="sxs-lookup"><span data-stu-id="d043d-133">inlineStyle</span></span> <br /> <i><span data-ttu-id="d043d-134">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-134">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="d043d-135">Inline Formatvorlage für den angegebenen DOM-Knoten.</span><span class="sxs-lookup"><span data-stu-id="d043d-135">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-136">Attributes</span><span class="sxs-lookup"><span data-stu-id="d043d-136">attributesStyle</span></span> <br /> <i><span data-ttu-id="d043d-137">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-137">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="d043d-138">Attribut definierte Element Formatvorlage (z. b. durch "Width = 20 height = 100%").</span><span class="sxs-lookup"><span data-stu-id="d043d-138">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d043d-139">getMatchedStylesForNode</span><span class="sxs-lookup"><span data-stu-id="d043d-139">getMatchedStylesForNode</span></span>
<span data-ttu-id="d043d-140">Gibt angeforderte Formatvorlagen für einen DOM-Knoten zurück, der von angegeben wird `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="d043d-140">Returns requested styles for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-141">Parameter</span><span class="sxs-lookup"><span data-stu-id="d043d-141">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-142">NodeId</span><span class="sxs-lookup"><span data-stu-id="d043d-142">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-143">Gibt</span><span class="sxs-lookup"><span data-stu-id="d043d-143">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-144">ininlinestyle</span><span class="sxs-lookup"><span data-stu-id="d043d-144">inlineStyle</span></span> <br /> <i><span data-ttu-id="d043d-145">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-145">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="d043d-146">Inline Formatvorlage für den angegebenen DOM-Knoten.</span><span class="sxs-lookup"><span data-stu-id="d043d-146">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-147">Attributes</span><span class="sxs-lookup"><span data-stu-id="d043d-147">attributesStyle</span></span> <br /> <i><span data-ttu-id="d043d-148">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-148">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="d043d-149">Attribut definierte Element Formatvorlage (z. b. durch "Width = 20 height = 100%").</span><span class="sxs-lookup"><span data-stu-id="d043d-149">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-150">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="d043d-150">matchedCSSRules</span></span> <br /> <i><span data-ttu-id="d043d-151">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-151">optional</span></span></i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="d043d-152">CSS-Regeln, die diesem Knoten entsprechen, aus allen anwendbaren Stylesheets.</span><span class="sxs-lookup"><span data-stu-id="d043d-152">CSS rules matching this node, from all applicable stylesheets.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-153">pseudoElements</span><span class="sxs-lookup"><span data-stu-id="d043d-153">pseudoElements</span></span> <br /> <i><span data-ttu-id="d043d-154">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-154">optional</span></span></i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td><span data-ttu-id="d043d-155">Pseudo Format Übereinstimmungen für diesen Knoten</span><span class="sxs-lookup"><span data-stu-id="d043d-155">Pseudo style matches for this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-156">geerbt</span><span class="sxs-lookup"><span data-stu-id="d043d-156">inherited</span></span> <br /> <i><span data-ttu-id="d043d-157">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-157">optional</span></span></i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td><span data-ttu-id="d043d-158">Eine Kette geerbter Formatvorlagen (vom übergeordneten Element des unmittelbaren Knotens bis zum Stammverzeichnis der DOM-Struktur).</span><span class="sxs-lookup"><span data-stu-id="d043d-158">A chain of inherited styles (from the immediate node parent up to the DOM tree root).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-159">cssKeyframesRules</span><span class="sxs-lookup"><span data-stu-id="d043d-159">cssKeyframesRules</span></span> <br /> <i><span data-ttu-id="d043d-160">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-160">optional</span></span></i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td><span data-ttu-id="d043d-161">Eine Liste der CSS-Keyframes-Animationen, die diesem Knoten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d043d-161">A list of CSS keyframed animations matching this node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d043d-162">getPlatformFontsForNode</span><span class="sxs-lookup"><span data-stu-id="d043d-162">getPlatformFontsForNode</span></span>
<span data-ttu-id="d043d-163">Fordert Informationen zu Platt Form Schriftarten an, die zum Rendern untergeordneter textnodes im angegebenen Knoten verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d043d-163">Requests information about platform fonts which we used to render child TextNodes in the given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-164">Parameter</span><span class="sxs-lookup"><span data-stu-id="d043d-164">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-165">NodeId</span><span class="sxs-lookup"><span data-stu-id="d043d-165">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-166">Gibt</span><span class="sxs-lookup"><span data-stu-id="d043d-166">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-167">Schriftarten</span><span class="sxs-lookup"><span data-stu-id="d043d-167">fonts</span></span></td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td><span data-ttu-id="d043d-168">Verwendungsstatistiken für jede verwendete Platt Form Schriftart</span><span class="sxs-lookup"><span data-stu-id="d043d-168">Usage statistics for every employed platform font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d043d-169">getComputedStyleForNode</span><span class="sxs-lookup"><span data-stu-id="d043d-169">getComputedStyleForNode</span></span>
<span data-ttu-id="d043d-170">Gibt den berechneten Stil für einen DOM-Knoten zurück, der von identifiziert wird `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="d043d-170">Returns the computed style for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-171">Parameter</span><span class="sxs-lookup"><span data-stu-id="d043d-171">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-172">NodeId</span><span class="sxs-lookup"><span data-stu-id="d043d-172">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-173">Gibt</span><span class="sxs-lookup"><span data-stu-id="d043d-173">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-174">computestyle</span><span class="sxs-lookup"><span data-stu-id="d043d-174">computedStyle</span></span></td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td><span data-ttu-id="d043d-175">Berechnete Formatvorlage für den angegebenen DOM-Knoten.</span><span class="sxs-lookup"><span data-stu-id="d043d-175">Computed style for the specified DOM node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="d043d-176">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="d043d-176">Events</span></span>

### <span data-ttu-id="d043d-177">styleSheetAdded</span><span class="sxs-lookup"><span data-stu-id="d043d-177">styleSheetAdded</span></span>
<span data-ttu-id="d043d-178">Wird ausgelöst, wenn ein Active Document-Stylesheet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d043d-178">Fired whenever an active document stylesheet is added.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-179">Parameter</span><span class="sxs-lookup"><span data-stu-id="d043d-179">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-180">header</span><span class="sxs-lookup"><span data-stu-id="d043d-180">header</span></span></td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td><span data-ttu-id="d043d-181">Stylesheet-Metainformationen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d043d-181">Added stylesheet metainfo.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d043d-182">stylesheetd</span><span class="sxs-lookup"><span data-stu-id="d043d-182">styleSheetChanged</span></span>
<span data-ttu-id="d043d-183">Wird ausgelöst, wenn ein Stylesheet als Ergebnis des Client Vorgangs geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d043d-183">Fired whenever a stylesheet is changed as a result of the client operation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-184">Parameter</span><span class="sxs-lookup"><span data-stu-id="d043d-184">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-185">Stylesheet-Nr</span><span class="sxs-lookup"><span data-stu-id="d043d-185">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d043d-186">styleSheetRemoved</span><span class="sxs-lookup"><span data-stu-id="d043d-186">styleSheetRemoved</span></span>
<span data-ttu-id="d043d-187">Wird ausgelöst, wenn ein Active Document-Stylesheet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d043d-187">Fired whenever an active document stylesheet is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-188">Parameter</span><span class="sxs-lookup"><span data-stu-id="d043d-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-189">Stylesheet-Nr</span><span class="sxs-lookup"><span data-stu-id="d043d-189">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="d043d-190">Bezeichner des entfernten Stylesheets.</span><span class="sxs-lookup"><span data-stu-id="d043d-190">Identifier of the removed stylesheet.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="d043d-191">Typen</span><span class="sxs-lookup"><span data-stu-id="d043d-191">Types</span></span>

### <a name="stylesheetid"></a> <span data-ttu-id="d043d-192">Stylesheet-Nr</span><span class="sxs-lookup"><span data-stu-id="d043d-192">StyleSheetId</span></span> `string`



</p>

---

### <a name="pseudoelementmatches"></a> <span data-ttu-id="d043d-193">PseudoElementMatches</span><span class="sxs-lookup"><span data-stu-id="d043d-193">PseudoElementMatches</span></span> `object`

<span data-ttu-id="d043d-194">CSS-Regelsammlung für eine einzelne Pseudo Formatvorlage.</span><span class="sxs-lookup"><span data-stu-id="d043d-194">CSS rule collection for a single pseudo style.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-195">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-195">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-196">Pseudotyp</span><span class="sxs-lookup"><span data-stu-id="d043d-196">pseudoType</span></span></td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td><span data-ttu-id="d043d-197">Pseudo Elementtyp.</span><span class="sxs-lookup"><span data-stu-id="d043d-197">Pseudo element type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-198">entspricht</span><span class="sxs-lookup"><span data-stu-id="d043d-198">matches</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="d043d-199">Übereinstimmungen der CSS-Regeln, die für das Pseudo Format gelten.</span><span class="sxs-lookup"><span data-stu-id="d043d-199">Matches of CSS rules applicable to the pseudo style.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> <span data-ttu-id="d043d-200">InheritedStyleEntry</span><span class="sxs-lookup"><span data-stu-id="d043d-200">InheritedStyleEntry</span></span> `object`

<span data-ttu-id="d043d-201">Geerbte CSS-Regelsammlung aus dem Vorgängerknoten</span><span class="sxs-lookup"><span data-stu-id="d043d-201">Inherited CSS rule collection from ancestor node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-202">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-202">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-203">ininlinestyle</span><span class="sxs-lookup"><span data-stu-id="d043d-203">inlineStyle</span></span> <br /> <i><span data-ttu-id="d043d-204">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-204">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="d043d-205">Die Inlineformatvorlage des Vorgänger Knotens, falls vorhanden, in der Stil Vererbungskette.</span><span class="sxs-lookup"><span data-stu-id="d043d-205">The ancestor node's inline style, if any, in the style inheritance chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-206">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="d043d-206">matchedCSSRules</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="d043d-207">Übereinstimmungen mit CSS-Regeln, die dem Vorgängerknoten in der Stil Vererbungskette entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d043d-207">Matches of CSS rules matching the ancestor node in the style inheritance chain.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> <span data-ttu-id="d043d-208">RuleMatch</span><span class="sxs-lookup"><span data-stu-id="d043d-208">RuleMatch</span></span> `object`

<span data-ttu-id="d043d-209">Vergleichen von Daten für eine CSS-Regel</span><span class="sxs-lookup"><span data-stu-id="d043d-209">Match data for a CSS rule.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-210">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-210">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-211">Regel</span><span class="sxs-lookup"><span data-stu-id="d043d-211">rule</span></span></td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td><span data-ttu-id="d043d-212">CSS-Regel in der Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="d043d-212">CSS rule in the match.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> <span data-ttu-id="d043d-213">Wert</span><span class="sxs-lookup"><span data-stu-id="d043d-213">Value</span></span> `object`

<span data-ttu-id="d043d-214">Daten für eine einfache Auswahl (diese werden durch Kommas in einer Auswahlliste getrennt).</span><span class="sxs-lookup"><span data-stu-id="d043d-214">Data for a simple selector (these are delimited by commas in a selector list).</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-215">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-215">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-216">Text</span><span class="sxs-lookup"><span data-stu-id="d043d-216">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-217">Wert Text</span><span class="sxs-lookup"><span data-stu-id="d043d-217">Value text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-218">Bereich</span><span class="sxs-lookup"><span data-stu-id="d043d-218">range</span></span> <br /> <i><span data-ttu-id="d043d-219">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-219">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="d043d-220">Wertbereich in der zugrunde liegenden Ressource (sofern verfügbar).</span><span class="sxs-lookup"><span data-stu-id="d043d-220">Value range in the underlying resource (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> <span data-ttu-id="d043d-221">Selektorliste</span><span class="sxs-lookup"><span data-stu-id="d043d-221">SelectorList</span></span> `object`

<span data-ttu-id="d043d-222">Auswahllisten Daten.</span><span class="sxs-lookup"><span data-stu-id="d043d-222">Selector list data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-223">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-223">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-224">Selektoren</span><span class="sxs-lookup"><span data-stu-id="d043d-224">selectors</span></span></td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td><span data-ttu-id="d043d-225">Wählen Sie in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="d043d-225">Selectors in the list.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-226">Text</span><span class="sxs-lookup"><span data-stu-id="d043d-226">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-227">Regel Auswahl Text</span><span class="sxs-lookup"><span data-stu-id="d043d-227">Rule selector text.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> <span data-ttu-id="d043d-228">CSSRule</span><span class="sxs-lookup"><span data-stu-id="d043d-228">CSSRule</span></span> `object`

<span data-ttu-id="d043d-229">CSS-Regel Darstellung</span><span class="sxs-lookup"><span data-stu-id="d043d-229">CSS rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-230">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-230">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-231">Stylesheet-Nr</span><span class="sxs-lookup"><span data-stu-id="d043d-231">styleSheetId</span></span> <br /> <i><span data-ttu-id="d043d-232">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-232">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="d043d-233">Die CSS-Stylesheet-ID (abwesend für Benutzer-Agent-Stylesheets und benutzerdefinierte Stylesheetregeln) diese Regel kam.</span><span class="sxs-lookup"><span data-stu-id="d043d-233">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-234">selektorliste</span><span class="sxs-lookup"><span data-stu-id="d043d-234">selectorList</span></span> <br /> <i><span data-ttu-id="d043d-235">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-235">optional</span></span></i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td><span data-ttu-id="d043d-236">Regel Auswahldaten.</span><span class="sxs-lookup"><span data-stu-id="d043d-236">Rule selector data.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-237">Ursprung</span><span class="sxs-lookup"><span data-stu-id="d043d-237">origin</span></span> <br /> <i><span data-ttu-id="d043d-238">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-238">optional</span></span></i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="d043d-239">Herkunft des übergeordneten Stylesheets</span><span class="sxs-lookup"><span data-stu-id="d043d-239">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-240">Formatvorlage</span><span class="sxs-lookup"><span data-stu-id="d043d-240">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="d043d-241">Zugeordnete Formatvorlagendeklaration.</span><span class="sxs-lookup"><span data-stu-id="d043d-241">Associated style declaration.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-242">Medien</span><span class="sxs-lookup"><span data-stu-id="d043d-242">media</span></span> <br /> <i><span data-ttu-id="d043d-243">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-243">optional</span></span></i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td><span data-ttu-id="d043d-244">Array für Medienlisten (für Regeln mit medienabfragen)</span><span class="sxs-lookup"><span data-stu-id="d043d-244">Media list array (for rules involving media queries).</span></span> <span data-ttu-id="d043d-245">Das Array listet medienabfragen auf, die mit dem innersten beginnen und nach außen gehen.</span><span class="sxs-lookup"><span data-stu-id="d043d-245">The array enumerates media queries starting with the innermost one, going outwards.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> <span data-ttu-id="d043d-246">SourceRange</span><span class="sxs-lookup"><span data-stu-id="d043d-246">SourceRange</span></span> `object`

<span data-ttu-id="d043d-247">Text Bereich innerhalb einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="d043d-247">Text range within a resource.</span></span> <span data-ttu-id="d043d-248">Alle Zahlen sind nullbasiert.</span><span class="sxs-lookup"><span data-stu-id="d043d-248">All numbers are zero-based.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-249">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-249">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-250">startLine</span><span class="sxs-lookup"><span data-stu-id="d043d-250">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="d043d-251">Start Linie des Bereichs</span><span class="sxs-lookup"><span data-stu-id="d043d-251">Start line of range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-252">startColumn</span><span class="sxs-lookup"><span data-stu-id="d043d-252">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="d043d-253">Start Spalte des Bereichs (inklusive).</span><span class="sxs-lookup"><span data-stu-id="d043d-253">Start column of range (inclusive).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-254">endLine</span><span class="sxs-lookup"><span data-stu-id="d043d-254">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="d043d-255">Endzeile des Bereichs</span><span class="sxs-lookup"><span data-stu-id="d043d-255">End line of range</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-256">endColumn</span><span class="sxs-lookup"><span data-stu-id="d043d-256">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="d043d-257">Ende der Spalte des Bereichs (exklusiv).</span><span class="sxs-lookup"><span data-stu-id="d043d-257">End column of range (exclusive).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> <span data-ttu-id="d043d-258">ShorthandEntry</span><span class="sxs-lookup"><span data-stu-id="d043d-258">ShorthandEntry</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-259">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-259">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-260">name</span><span class="sxs-lookup"><span data-stu-id="d043d-260">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-261">Kurzbezeichnung</span><span class="sxs-lookup"><span data-stu-id="d043d-261">Shorthand name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-262">value</span><span class="sxs-lookup"><span data-stu-id="d043d-262">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-263">Kurzform-Wert.</span><span class="sxs-lookup"><span data-stu-id="d043d-263">Shorthand value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-264">wichtig</span><span class="sxs-lookup"><span data-stu-id="d043d-264">important</span></span> <br /> <i><span data-ttu-id="d043d-265">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-265">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d043d-266">Gibt an, ob die Eigenschaft eine "! Important"-Anmerkung hat (impliziert, `false` Wenn nicht vorhanden).</span><span class="sxs-lookup"><span data-stu-id="d043d-266">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> <span data-ttu-id="d043d-267">CSSStyle</span><span class="sxs-lookup"><span data-stu-id="d043d-267">CSSStyle</span></span> `object`

<span data-ttu-id="d043d-268">Darstellung des CSS-Formats</span><span class="sxs-lookup"><span data-stu-id="d043d-268">CSS style representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-269">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-269">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-270">Stylesheet-Nr</span><span class="sxs-lookup"><span data-stu-id="d043d-270">styleSheetId</span></span> <br /> <i><span data-ttu-id="d043d-271">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-271">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="d043d-272">Die CSS-Stylesheet-ID (abwesend für Benutzer-Agent-Stylesheets und benutzerdefinierte Stylesheetregeln) diese Regel kam.</span><span class="sxs-lookup"><span data-stu-id="d043d-272">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-273">cssProperties</span><span class="sxs-lookup"><span data-stu-id="d043d-273">cssProperties</span></span></td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td><span data-ttu-id="d043d-274">CSS-Eigenschaften in der Formatvorlage.</span><span class="sxs-lookup"><span data-stu-id="d043d-274">CSS properties in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-275">shorthandEntries</span><span class="sxs-lookup"><span data-stu-id="d043d-275">shorthandEntries</span></span></td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td><span data-ttu-id="d043d-276">Berechnete Werte für alle in der Formatvorlage gefundenen Abkürzungen.</span><span class="sxs-lookup"><span data-stu-id="d043d-276">Computed values for all shorthands found in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-277">cssText</span><span class="sxs-lookup"><span data-stu-id="d043d-277">cssText</span></span> <br /> <i><span data-ttu-id="d043d-278">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-278">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-279">Text für die Formatvorlagendeklaration (sofern verfügbar).</span><span class="sxs-lookup"><span data-stu-id="d043d-279">Style declaration text (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-280">Bereich</span><span class="sxs-lookup"><span data-stu-id="d043d-280">range</span></span> <br /> <i><span data-ttu-id="d043d-281">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-281">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="d043d-282">Der Stil Deklarationsbereich im einschließenden Stylesheet (sofern verfügbar).</span><span class="sxs-lookup"><span data-stu-id="d043d-282">Style declaration range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> <span data-ttu-id="d043d-283">CSSProperty</span><span class="sxs-lookup"><span data-stu-id="d043d-283">CSSProperty</span></span> `object`

<span data-ttu-id="d043d-284">CSS-Eigenschaften Deklarationsdaten.</span><span class="sxs-lookup"><span data-stu-id="d043d-284">CSS property declaration data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-285">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-285">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-286">name</span><span class="sxs-lookup"><span data-stu-id="d043d-286">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-287">Der Name der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d043d-287">The property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-288">value</span><span class="sxs-lookup"><span data-stu-id="d043d-288">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-289">Der Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="d043d-289">The property value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-290">wichtig</span><span class="sxs-lookup"><span data-stu-id="d043d-290">important</span></span> <br /> <i><span data-ttu-id="d043d-291">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-291">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d043d-292">Gibt an, ob die Eigenschaft eine "! Important"-Anmerkung hat (impliziert, `false` Wenn nicht vorhanden).</span><span class="sxs-lookup"><span data-stu-id="d043d-292">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-293">implizite</span><span class="sxs-lookup"><span data-stu-id="d043d-293">implicit</span></span> <br /> <i><span data-ttu-id="d043d-294">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-294">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d043d-295">Gibt an, ob die Eigenschaft implizit ist (impliziert, `false` Wenn nicht vorhanden).</span><span class="sxs-lookup"><span data-stu-id="d043d-295">Whether the property is implicit (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-296">Text</span><span class="sxs-lookup"><span data-stu-id="d043d-296">text</span></span> <br /> <i><span data-ttu-id="d043d-297">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-297">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-298">Der vollständige Eigenschafts Text wie in der Formatvorlage angegeben.</span><span class="sxs-lookup"><span data-stu-id="d043d-298">The full property text as specified in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-299">parsedOk</span><span class="sxs-lookup"><span data-stu-id="d043d-299">parsedOk</span></span> <br /> <i><span data-ttu-id="d043d-300">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-300">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d043d-301">Gibt an, ob die Eigenschaft vom Browser verstanden wird (impliziert, `true` Wenn nicht vorhanden).</span><span class="sxs-lookup"><span data-stu-id="d043d-301">Whether the property is understood by the browser (implies `true` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-302">deaktiviert</span><span class="sxs-lookup"><span data-stu-id="d043d-302">disabled</span></span> <br /> <i><span data-ttu-id="d043d-303">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-303">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d043d-304">Gibt an, ob die Eigenschaft vom Benutzer deaktiviert wurde (nur für Quell basierte Eigenschaften vorhanden).</span><span class="sxs-lookup"><span data-stu-id="d043d-304">Whether the property is disabled by the user (present for source-based properties only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-305">Bereich</span><span class="sxs-lookup"><span data-stu-id="d043d-305">range</span></span> <br /> <i><span data-ttu-id="d043d-306">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-306">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="d043d-307">Der gesamte Eigenschaftenbereich in der einschließenden Formatvorlagendeklaration (sofern verfügbar).</span><span class="sxs-lookup"><span data-stu-id="d043d-307">The entire property range in the enclosing style declaration (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> <span data-ttu-id="d043d-308">CSSMedia</span><span class="sxs-lookup"><span data-stu-id="d043d-308">CSSMedia</span></span> `object`

<span data-ttu-id="d043d-309">CSS Media Rule Descriptor.</span><span class="sxs-lookup"><span data-stu-id="d043d-309">CSS media rule descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-310">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-310">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-311">Text</span><span class="sxs-lookup"><span data-stu-id="d043d-311">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-312">Medienabfrage Text</span><span class="sxs-lookup"><span data-stu-id="d043d-312">Media query text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-313">Quelle</span><span class="sxs-lookup"><span data-stu-id="d043d-313">source</span></span></td>
            <td><code class="flyout">string</code> <br /> <i><span data-ttu-id="d043d-314">Zulässige Werte: mediaRule, importRule, linkedSheet, inlineSheet</span><span class="sxs-lookup"><span data-stu-id="d043d-314">Allowed values: mediaRule, importRule, linkedSheet, inlineSheet</span></span></i></td>
            <td><span data-ttu-id="d043d-315">Quelle der medienabfrage: "mediaRule", wenn Sie durch eine @Media Regel angegeben wird, "importRule", wenn Sie durch eine @Import Regel angegeben wird, "linkedSheet", wenn Sie durch ein "Medien"-Attribut im Linktag eines verknüpften Stylesheets angegeben wird, "inlineSheet", wenn es durch ein "Medien"-Attribut im Style-Tag eines Inlinestylesheets angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d043d-315">Source of the media query: "mediaRule" if specified by a @media rule, "importRule" if specified by an @import rule, "linkedSheet" if specified by a "media" attribute in a linked stylesheet's LINK tag, "inlineSheet" if specified by a "media" attribute in an inline stylesheet's STYLE tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-316">sourceURL</span><span class="sxs-lookup"><span data-stu-id="d043d-316">sourceURL</span></span> <br /> <i><span data-ttu-id="d043d-317">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-317">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-318">Die URL des Dokuments, das die Beschreibung der medienabfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="d043d-318">URL of the document containing the media query description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-319">Bereich</span><span class="sxs-lookup"><span data-stu-id="d043d-319">range</span></span> <br /> <i><span data-ttu-id="d043d-320">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-320">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="d043d-321">Der zugeordnete Regelbereich (@Media oder @Import) im einschließenden Stylesheet (sofern verfügbar).</span><span class="sxs-lookup"><span data-stu-id="d043d-321">The associated rule (@media or @import) header range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-322">Stylesheet-Nr</span><span class="sxs-lookup"><span data-stu-id="d043d-322">styleSheetId</span></span> <br /> <i><span data-ttu-id="d043d-323">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-323">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="d043d-324">Bezeichner des Stylesheets, das dieses Objekt enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="d043d-324">Identifier of the stylesheet containing this object (if exists).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-325">medialist</span><span class="sxs-lookup"><span data-stu-id="d043d-325">mediaList</span></span> <br /> <i><span data-ttu-id="d043d-326">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-326">optional</span></span></i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td><span data-ttu-id="d043d-327">Array von medienabfragen</span><span class="sxs-lookup"><span data-stu-id="d043d-327">Array of media queries.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> <span data-ttu-id="d043d-328">MediaQuery</span><span class="sxs-lookup"><span data-stu-id="d043d-328">MediaQuery</span></span> `object`

<span data-ttu-id="d043d-329">Beschreibung der medienabfrage</span><span class="sxs-lookup"><span data-stu-id="d043d-329">Media query descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-330">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-331">Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="d043d-331">expressions</span></span></td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td><span data-ttu-id="d043d-332">Array von medienabfrage Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="d043d-332">Array of media query expressions.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-333">active</span><span class="sxs-lookup"><span data-stu-id="d043d-333">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d043d-334">Gibt an, ob die medienabfrage Bedingung erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="d043d-334">Whether the media query condition is satisfied.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> <span data-ttu-id="d043d-335">MediaQueryExpression</span><span class="sxs-lookup"><span data-stu-id="d043d-335">MediaQueryExpression</span></span> `object`

<span data-ttu-id="d043d-336">Medienabfrage-Ausdrucks Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="d043d-336">Media query expression descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-337">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-338">value</span><span class="sxs-lookup"><span data-stu-id="d043d-338">value</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="d043d-339">Medienabfrage Ausdruckswert.</span><span class="sxs-lookup"><span data-stu-id="d043d-339">Media query expression value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-340">Einheit</span><span class="sxs-lookup"><span data-stu-id="d043d-340">unit</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-341">Medienabfrage Ausdrucks Einheiten</span><span class="sxs-lookup"><span data-stu-id="d043d-341">Media query expression units.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-342">Features</span><span class="sxs-lookup"><span data-stu-id="d043d-342">feature</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-343">Medienabfrage Ausdrucks-Feature.</span><span class="sxs-lookup"><span data-stu-id="d043d-343">Media query expression feature.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-344">valueRange</span><span class="sxs-lookup"><span data-stu-id="d043d-344">valueRange</span></span> <br /> <i><span data-ttu-id="d043d-345">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-345">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="d043d-346">Der zugeordnete Bereich des Wert Texts im einschließenden Stylesheet (sofern verfügbar).</span><span class="sxs-lookup"><span data-stu-id="d043d-346">The associated range of the value text in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-347">computedLength</span><span class="sxs-lookup"><span data-stu-id="d043d-347">computedLength</span></span> <br /> <i><span data-ttu-id="d043d-348">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-348">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="d043d-349">Berechnete Länge des medienabfrage Ausdrucks (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="d043d-349">Computed length of media query expression (if applicable).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> <span data-ttu-id="d043d-350">PlatformFontUsage</span><span class="sxs-lookup"><span data-stu-id="d043d-350">PlatformFontUsage</span></span> `object`

<span data-ttu-id="d043d-351">Informationen über die Anzahl der Glyphen, die mit der angegebenen Schriftart gerendert wurden.</span><span class="sxs-lookup"><span data-stu-id="d043d-351">Information about amount of glyphs that were rendered with given font.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-352">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-352">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-353">familyName</span><span class="sxs-lookup"><span data-stu-id="d043d-353">familyName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-354">Der von Platform gemeldete Familienname der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="d043d-354">Font's family name reported by platform.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-355">isCustomFont</span><span class="sxs-lookup"><span data-stu-id="d043d-355">isCustomFont</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d043d-356">Gibt an, ob die Schriftart heruntergeladen oder lokal aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="d043d-356">Indicates if the font was downloaded or resolved locally.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-357">glyphCount</span><span class="sxs-lookup"><span data-stu-id="d043d-357">glyphCount</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="d043d-358">Die Anzahl der Glyphen, die mit dieser Schriftart gerendert wurden.</span><span class="sxs-lookup"><span data-stu-id="d043d-358">Amount of glyphs that were rendered with this font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> <span data-ttu-id="d043d-359">CSSKeyframesRule</span><span class="sxs-lookup"><span data-stu-id="d043d-359">CSSKeyframesRule</span></span> `object`

<span data-ttu-id="d043d-360">CSS-Keyframes-Regel Darstellung</span><span class="sxs-lookup"><span data-stu-id="d043d-360">CSS keyframes rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-361">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-361">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-362">Animations</span><span class="sxs-lookup"><span data-stu-id="d043d-362">animationName</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="d043d-363">Animations Name</span><span class="sxs-lookup"><span data-stu-id="d043d-363">Animation name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-364">Keyframes</span><span class="sxs-lookup"><span data-stu-id="d043d-364">keyframes</span></span></td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td><span data-ttu-id="d043d-365">Liste der Keyframes.</span><span class="sxs-lookup"><span data-stu-id="d043d-365">List of keyframes.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> <span data-ttu-id="d043d-366">CSSKeyframeRule</span><span class="sxs-lookup"><span data-stu-id="d043d-366">CSSKeyframeRule</span></span> `object`

<span data-ttu-id="d043d-367">CSS-Keyframe-Regel Darstellung</span><span class="sxs-lookup"><span data-stu-id="d043d-367">CSS keyframe rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-368">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-369">Stylesheet-Nr</span><span class="sxs-lookup"><span data-stu-id="d043d-369">styleSheetId</span></span> <br /> <i><span data-ttu-id="d043d-370">Optional</span><span class="sxs-lookup"><span data-stu-id="d043d-370">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="d043d-371">Die CSS-Stylesheet-ID (abwesend für Benutzer-Agent-Stylesheets und benutzerdefinierte Stylesheetregeln) diese Regel kam.</span><span class="sxs-lookup"><span data-stu-id="d043d-371">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-372">Ursprung</span><span class="sxs-lookup"><span data-stu-id="d043d-372">origin</span></span></td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="d043d-373">Herkunft des übergeordneten Stylesheets</span><span class="sxs-lookup"><span data-stu-id="d043d-373">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-374">keyText</span><span class="sxs-lookup"><span data-stu-id="d043d-374">keyText</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="d043d-375">Zugeordneter Schlüssel Text</span><span class="sxs-lookup"><span data-stu-id="d043d-375">Associated key text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-376">Formatvorlage</span><span class="sxs-lookup"><span data-stu-id="d043d-376">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="d043d-377">Zugeordnete Formatvorlagendeklaration.</span><span class="sxs-lookup"><span data-stu-id="d043d-377">Associated style declaration.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> <span data-ttu-id="d043d-378">CSSComputedStyleProperty</span><span class="sxs-lookup"><span data-stu-id="d043d-378">CSSComputedStyleProperty</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-379">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-379">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-380">name</span><span class="sxs-lookup"><span data-stu-id="d043d-380">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-381">Eigenschaftsname für berechnete Formatvorlage</span><span class="sxs-lookup"><span data-stu-id="d043d-381">Computed style property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-382">value</span><span class="sxs-lookup"><span data-stu-id="d043d-382">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-383">Eigenschaftswert des berechneten Stils.</span><span class="sxs-lookup"><span data-stu-id="d043d-383">Computed style property value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> <span data-ttu-id="d043d-384">CSSStyleSheetHeader</span><span class="sxs-lookup"><span data-stu-id="d043d-384">CSSStyleSheetHeader</span></span> `object`

<span data-ttu-id="d043d-385">Metainformationen für CSS-Stylesheets.</span><span class="sxs-lookup"><span data-stu-id="d043d-385">CSS stylesheet metainformation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d043d-386">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d043d-386">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d043d-387">Stylesheet-Nr</span><span class="sxs-lookup"><span data-stu-id="d043d-387">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="d043d-388">Der Stylesheet-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d043d-388">The stylesheet identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-389">sourceURL</span><span class="sxs-lookup"><span data-stu-id="d043d-389">sourceURL</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d043d-390">Stylesheet-Ressourcen-URL.</span><span class="sxs-lookup"><span data-stu-id="d043d-390">Stylesheet resource URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-391">deaktiviert</span><span class="sxs-lookup"><span data-stu-id="d043d-391">disabled</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d043d-392">Kennzeichnet, ob das Stylesheet deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d043d-392">Denotes whether the stylesheet is disabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-393">IsInline</span><span class="sxs-lookup"><span data-stu-id="d043d-393">isInline</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="d043d-394">Gibt an, ob dieses Stylesheet für Style-Tags nach Parser erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d043d-394">Whether this stylesheet is created for STYLE tag by parser.</span></span> <span data-ttu-id="d043d-395">Dieses Flag ist nicht für Document. written-Stil Kategorien definiert.</span><span class="sxs-lookup"><span data-stu-id="d043d-395">This flag is not set for document.written STYLE tags.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-396">startLine</span><span class="sxs-lookup"><span data-stu-id="d043d-396">startLine</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="d043d-397">Der Versatz des Stylesheets innerhalb der Ressource (nullbasiert)</span><span class="sxs-lookup"><span data-stu-id="d043d-397">Line offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-398">startColumn</span><span class="sxs-lookup"><span data-stu-id="d043d-398">startColumn</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="d043d-399">Spaltenoffset des Stylesheets innerhalb der Ressource (nullbasiert).</span><span class="sxs-lookup"><span data-stu-id="d043d-399">Column offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d043d-400">Länge</span><span class="sxs-lookup"><span data-stu-id="d043d-400">length</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="d043d-401">Die Größe des Inhalts (in Zeichen).</span><span class="sxs-lookup"><span data-stu-id="d043d-401">Size of the content (in characters).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="d043d-402">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="d043d-402">Dependencies</span></span>

[<span data-ttu-id="d043d-403">DOM</span><span class="sxs-lookup"><span data-stu-id="d043d-403">DOM</span></span>](dom.md)

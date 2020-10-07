---
description: Discover new workflows for viewing and changing CSS in Microsoft Edge DevTools.
title: CSS Reference
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: de0fb33e1e080045383f3c0fb50919297cbff5bc
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993072"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="9945a-104">CSS reference</span><span class="sxs-lookup"><span data-stu-id="9945a-104">CSS reference</span></span>  

<span data-ttu-id="9945a-105">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span><span class="sxs-lookup"><span data-stu-id="9945a-105">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="9945a-106">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span><span class="sxs-lookup"><span data-stu-id="9945a-106">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="9945a-107">Select an element</span><span class="sxs-lookup"><span data-stu-id="9945a-107">Select an element</span></span>  

<span data-ttu-id="9945a-108">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span><span class="sxs-lookup"><span data-stu-id="9945a-108">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="9945a-109">The selected element is highlighted in the **DOM Tree**.</span><span class="sxs-lookup"><span data-stu-id="9945a-109">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="9945a-110">The styles of the element are shown in the **Styles** pane.</span><span class="sxs-lookup"><span data-stu-id="9945a-110">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="9945a-111">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span><span class="sxs-lookup"><span data-stu-id="9945a-111">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="9945a-112">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span><span class="sxs-lookup"><span data-stu-id="9945a-112">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="9945a-113">On the right, the styles of the element are shown in the **Styles** pane.</span><span class="sxs-lookup"><span data-stu-id="9945a-113">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="9945a-114">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span><span class="sxs-lookup"><span data-stu-id="9945a-114">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="9945a-116">An example of a selected element</span><span class="sxs-lookup"><span data-stu-id="9945a-116">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="9945a-117">Use one the following actions to select an element.</span><span class="sxs-lookup"><span data-stu-id="9945a-117">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="9945a-118">In your viewport, hover on the element, open the contextual menu \(right-click\), and select **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="9945a-118">In your viewport, hover on the element, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
*   <span data-ttu-id="9945a-119">In DevTools, choose **Select an element** \(![Select an element][ImageSelectAnElementIcon]\) or select `Control`+`Shift`+`C` \(Windows\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span><span class="sxs-lookup"><span data-stu-id="9945a-119">In DevTools, choose **Select an element** \(![Select an element][ImageSelectAnElementIcon]\) or select `Control`+`Shift`+`C` \(Windows\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="9945a-120">In DevTools, choose the element in the **DOM Tree**.</span><span class="sxs-lookup"><span data-stu-id="9945a-120">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="9945a-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and select **Reveal in Elements panel**.</span><span class="sxs-lookup"><span data-stu-id="9945a-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and select **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="9945a-122">View CSS</span><span class="sxs-lookup"><span data-stu-id="9945a-122">View CSS</span></span>  

### <span data-ttu-id="9945a-123">View the external stylesheet where a rule is defined</span><span class="sxs-lookup"><span data-stu-id="9945a-123">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="9945a-124">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span><span class="sxs-lookup"><span data-stu-id="9945a-124">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="9945a-125">If the stylesheet is minified, see [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="9945a-125">If the stylesheet is minified, see [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="9945a-126">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span><span class="sxs-lookup"><span data-stu-id="9945a-126">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="9945a-128">Viewing the stylesheet where a rule is defined</span><span class="sxs-lookup"><span data-stu-id="9945a-128">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <span data-ttu-id="9945a-129">View only the CSS that is actually applied to an element</span><span class="sxs-lookup"><span data-stu-id="9945a-129">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="9945a-130">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span><span class="sxs-lookup"><span data-stu-id="9945a-130">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="9945a-131">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span><span class="sxs-lookup"><span data-stu-id="9945a-131">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="9945a-132">[Select an element](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="9945a-132">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="9945a-133">Go to the **Computed** tab in the **Elements** panel.</span><span class="sxs-lookup"><span data-stu-id="9945a-133">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="9945a-134">On a wide DevTools window, the **Computed** tab does not exist.</span><span class="sxs-lookup"><span data-stu-id="9945a-134">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="9945a-135">The contents of the **Computed** tab are shown on the **Styles** tab.</span><span class="sxs-lookup"><span data-stu-id="9945a-135">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="9945a-136">Inherited properties are opaque.</span><span class="sxs-lookup"><span data-stu-id="9945a-136">Inherited properties are opaque.</span></span>  <span data-ttu-id="9945a-137">Check the **Show All** checkbox to see all inherited values.</span><span class="sxs-lookup"><span data-stu-id="9945a-137">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="9945a-138">In the following figure, the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span><span class="sxs-lookup"><span data-stu-id="9945a-138">In the following figure, the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="9945a-140">The **Computed** tab</span><span class="sxs-lookup"><span data-stu-id="9945a-140">The **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="9945a-141">View CSS properties in alphabetical order</span><span class="sxs-lookup"><span data-stu-id="9945a-141">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="9945a-142">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="9945a-142">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="9945a-143">View inherited CSS properties</span><span class="sxs-lookup"><span data-stu-id="9945a-143">View inherited CSS properties</span></span>  

<span data-ttu-id="9945a-144">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="9945a-144">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="9945a-145">View the box model for an element</span><span class="sxs-lookup"><span data-stu-id="9945a-145">View the box model for an element</span></span>  

<span data-ttu-id="9945a-146">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span><span class="sxs-lookup"><span data-stu-id="9945a-146">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="9945a-147">Choose and edit on a value to change a value.</span><span class="sxs-lookup"><span data-stu-id="9945a-147">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="9945a-148">In the following figure, the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span><span class="sxs-lookup"><span data-stu-id="9945a-148">In the following figure, the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="9945a-150">The **Box Model** diagram</span><span class="sxs-lookup"><span data-stu-id="9945a-150">The **Box Model** diagram</span></span>  
:::image-end:::  

### <span data-ttu-id="9945a-151">Search and filter the CSS of an element</span><span class="sxs-lookup"><span data-stu-id="9945a-151">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="9945a-152">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span><span class="sxs-lookup"><span data-stu-id="9945a-152">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="9945a-153">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span><span class="sxs-lookup"><span data-stu-id="9945a-153">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="9945a-154">In the following figure, the **Styles** tab is filtered to only show rules that include the search query `color`.</span><span class="sxs-lookup"><span data-stu-id="9945a-154">In the following figure, the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="9945a-156">Filter the **Styles** tab</span><span class="sxs-lookup"><span data-stu-id="9945a-156">Filter the **Styles** tab</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9945a-157">In the following figure, the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span><span class="sxs-lookup"><span data-stu-id="9945a-157">In the following figure, the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="9945a-159">Filter the **Computed** tab</span><span class="sxs-lookup"><span data-stu-id="9945a-159">Filter the **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="9945a-160">Toggle a pseudo-class</span><span class="sxs-lookup"><span data-stu-id="9945a-160">Toggle a pseudo-class</span></span>  

<span data-ttu-id="9945a-161">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span><span class="sxs-lookup"><span data-stu-id="9945a-161">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="9945a-162">[Select an element](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="9945a-162">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="9945a-163">On the **Elements** panel, go to the **Styles** tab.</span><span class="sxs-lookup"><span data-stu-id="9945a-163">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="9945a-164">Choose **:hov**.</span><span class="sxs-lookup"><span data-stu-id="9945a-164">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="9945a-165">Check the pseudo-class that you want to enable.</span><span class="sxs-lookup"><span data-stu-id="9945a-165">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="9945a-166">In the following figure, toggle the `:hover` pseudo-class.</span><span class="sxs-lookup"><span data-stu-id="9945a-166">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="9945a-167">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span><span class="sxs-lookup"><span data-stu-id="9945a-167">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="9945a-169">Toggle the `:hover` pseudo-class</span><span class="sxs-lookup"><span data-stu-id="9945a-169">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="9945a-170">For an interactive tutorial, see [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span><span class="sxs-lookup"><span data-stu-id="9945a-170">For an interactive tutorial, see [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <span data-ttu-id="9945a-171">View a page in print mode</span><span class="sxs-lookup"><span data-stu-id="9945a-171">View a page in print mode</span></span>  

<span data-ttu-id="9945a-172">Complete the following actions to view a page in print mode.</span><span class="sxs-lookup"><span data-stu-id="9945a-172">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="9945a-173">[Open the Command Menu][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="9945a-173">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="9945a-174">Start typing `Rendering` and select `Show Rendering`.</span><span class="sxs-lookup"><span data-stu-id="9945a-174">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="9945a-175">For the **Emulate CSS Media** dropdown, select **print**.</span><span class="sxs-lookup"><span data-stu-id="9945a-175">For the **Emulate CSS Media** dropdown, select **print**.</span></span>  

### <span data-ttu-id="9945a-176">View used and unused CSS with the Coverage tab</span><span class="sxs-lookup"><span data-stu-id="9945a-176">View used and unused CSS with the Coverage tab</span></span>  

<span data-ttu-id="9945a-177">The Coverage tab shows you what CSS a page actually uses.</span><span class="sxs-lookup"><span data-stu-id="9945a-177">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="9945a-178">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="9945a-178">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="9945a-179">Start typing `coverage` and select **Show Coverage**.</span><span class="sxs-lookup"><span data-stu-id="9945a-179">Start typing `coverage` and select **Show Coverage**.</span></span>  <span data-ttu-id="9945a-180">The Coverage tab appears.</span><span class="sxs-lookup"><span data-stu-id="9945a-180">The Coverage tab appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="An example of a selected element" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="9945a-182">Open the **Coverage** tab from the **Command Menu**</span><span class="sxs-lookup"><span data-stu-id="9945a-182">Open the **Coverage** tab from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="An example of a selected element" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="9945a-184">The **Coverage** tab</span><span class="sxs-lookup"><span data-stu-id="9945a-184">The **Coverage** tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="9945a-185">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page][ImageRefreshIcon]\).</span><span class="sxs-lookup"><span data-stu-id="9945a-185">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="9945a-186">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span><span class="sxs-lookup"><span data-stu-id="9945a-186">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="9945a-187">Green represents used CSS.</span><span class="sxs-lookup"><span data-stu-id="9945a-187">Green represents used CSS.</span></span>  <span data-ttu-id="9945a-188">Red represents unused CSS.</span><span class="sxs-lookup"><span data-stu-id="9945a-188">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="An example of a selected element" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="9945a-190">An overview of how much CSS \(and JavaScript\) is used and unused</span><span class="sxs-lookup"><span data-stu-id="9945a-190">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="9945a-191">Choose a CSS file to see a line-by-line breakdown of what CSS it uses.</span><span class="sxs-lookup"><span data-stu-id="9945a-191">Choose a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9945a-192">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span><span class="sxs-lookup"><span data-stu-id="9945a-192">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="An example of a selected element" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="9945a-194">A line-by-line breakdown of used and unused CSS</span><span class="sxs-lookup"><span data-stu-id="9945a-194">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="9945a-195">Force print preview mode</span><span class="sxs-lookup"><span data-stu-id="9945a-195">Force print preview mode</span></span>  

<span data-ttu-id="9945a-196">See [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="9945a-196">See [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="9945a-197">Change CSS</span><span class="sxs-lookup"><span data-stu-id="9945a-197">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="9945a-198">Add a CSS declaration to an element</span><span class="sxs-lookup"><span data-stu-id="9945a-198">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="9945a-199">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span><span class="sxs-lookup"><span data-stu-id="9945a-199">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="9945a-200">[Add a inline declaration](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="9945a-200">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="9945a-201">Equivalent to adding a `style` attribute to the HTML of an element.</span><span class="sxs-lookup"><span data-stu-id="9945a-201">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="9945a-202">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="9945a-202">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="9945a-203">What workflow should you use?</span><span class="sxs-lookup"><span data-stu-id="9945a-203">What workflow should you use?</span></span>** <span data-ttu-id="9945a-204">For most scenarios, you probably want to use the inline declaration workflow.</span><span class="sxs-lookup"><span data-stu-id="9945a-204">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="9945a-205">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span><span class="sxs-lookup"><span data-stu-id="9945a-205">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="9945a-206">For more information about specificity, see [Selector Types][MDNSelectorTypes].</span><span class="sxs-lookup"><span data-stu-id="9945a-206">For more information about specificity, see [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="9945a-207">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span><span class="sxs-lookup"><span data-stu-id="9945a-207">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="9945a-208">Add an inline declaration</span><span class="sxs-lookup"><span data-stu-id="9945a-208">Add an inline declaration</span></span>  

<span data-ttu-id="9945a-209">Complete the following actions to add an inline declaration.</span><span class="sxs-lookup"><span data-stu-id="9945a-209">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="9945a-210">[Select an element](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="9945a-210">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="9945a-211">In the **Styles** pane, choose between the brackets of the **element.style** section.</span><span class="sxs-lookup"><span data-stu-id="9945a-211">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="9945a-212">The cursor focuses, allowing you to enter text.</span><span class="sxs-lookup"><span data-stu-id="9945a-212">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="9945a-213">Enter a property name and select `Enter`.</span><span class="sxs-lookup"><span data-stu-id="9945a-213">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="9945a-214">Enter a valid value for that property and select `Enter`.</span><span class="sxs-lookup"><span data-stu-id="9945a-214">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="9945a-215">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span><span class="sxs-lookup"><span data-stu-id="9945a-215">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="9945a-216">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span><span class="sxs-lookup"><span data-stu-id="9945a-216">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="9945a-217">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span><span class="sxs-lookup"><span data-stu-id="9945a-217">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="9945a-219">Add inline declarations</span><span class="sxs-lookup"><span data-stu-id="9945a-219">Add inline declarations</span></span>  
:::image-end:::  

#### <span data-ttu-id="9945a-220">Add a declaration to a style rule</span><span class="sxs-lookup"><span data-stu-id="9945a-220">Add a declaration to a style rule</span></span>  

<span data-ttu-id="9945a-221">Complete the following actions to add a declaration to an existing style rule.</span><span class="sxs-lookup"><span data-stu-id="9945a-221">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="9945a-222">[Select an element](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="9945a-222">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="9945a-223">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span><span class="sxs-lookup"><span data-stu-id="9945a-223">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="9945a-224">The cursor focuses, allowing you to enter text.</span><span class="sxs-lookup"><span data-stu-id="9945a-224">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="9945a-225">Enter a property name and select `Enter`.</span><span class="sxs-lookup"><span data-stu-id="9945a-225">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="9945a-226">Enter a valid value for that property and select `Enter`.</span><span class="sxs-lookup"><span data-stu-id="9945a-226">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="9945a-228">Add the `border-bottom-style:groove` declaration to a style rule</span><span class="sxs-lookup"><span data-stu-id="9945a-228">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <span data-ttu-id="9945a-229">Change a declaration name or value</span><span class="sxs-lookup"><span data-stu-id="9945a-229">Change a declaration name or value</span></span>  

<span data-ttu-id="9945a-230">Choose and edit the name or value of a declaration to change it.</span><span class="sxs-lookup"><span data-stu-id="9945a-230">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="9945a-231">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span><span class="sxs-lookup"><span data-stu-id="9945a-231">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="9945a-233">Change the value of the `border-bottom-style` declaration</span><span class="sxs-lookup"><span data-stu-id="9945a-233">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="9945a-234">Change declaration values with keyboard shortcuts</span><span class="sxs-lookup"><span data-stu-id="9945a-234">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="9945a-235">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span><span class="sxs-lookup"><span data-stu-id="9945a-235">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="9945a-236">Select `Alt`+`Up` \(Windows\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span><span class="sxs-lookup"><span data-stu-id="9945a-236">Select `Alt`+`Up` \(Windows\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="9945a-237">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span><span class="sxs-lookup"><span data-stu-id="9945a-237">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="9945a-238">Select `Shift`+`Up` to increment by `10`.</span><span class="sxs-lookup"><span data-stu-id="9945a-238">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="9945a-239">Select `Shift`+`Page Up` \(Windows\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span><span class="sxs-lookup"><span data-stu-id="9945a-239">Select `Shift`+`Page Up` \(Windows\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="9945a-240">Decrementing also works.</span><span class="sxs-lookup"><span data-stu-id="9945a-240">Decrementing also works.</span></span>  <span data-ttu-id="9945a-241">Just replace each instance of `Up` mentioned above with `Down`.</span><span class="sxs-lookup"><span data-stu-id="9945a-241">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="9945a-242">Add a class to an element</span><span class="sxs-lookup"><span data-stu-id="9945a-242">Add a class to an element</span></span>  

<span data-ttu-id="9945a-243">Complete the following actions to add a class to an element.</span><span class="sxs-lookup"><span data-stu-id="9945a-243">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="9945a-244">[Select the element](#select-an-element) in the **DOM Tree**.</span><span class="sxs-lookup"><span data-stu-id="9945a-244">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="9945a-245">Choose **.cls**.</span><span class="sxs-lookup"><span data-stu-id="9945a-245">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="9945a-246">Enter the name of the class in the **Add New Class** text box.</span><span class="sxs-lookup"><span data-stu-id="9945a-246">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="9945a-247">Select `Enter`.</span><span class="sxs-lookup"><span data-stu-id="9945a-247">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="9945a-249">The **Element Classes** pane</span><span class="sxs-lookup"><span data-stu-id="9945a-249">The **Element Classes** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="9945a-250">Toggle a class</span><span class="sxs-lookup"><span data-stu-id="9945a-250">Toggle a class</span></span>  

<span data-ttu-id="9945a-251">Complete the following actions to enable or disable a class on an element.</span><span class="sxs-lookup"><span data-stu-id="9945a-251">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="9945a-252">[Select the element](#select-an-element) in the **DOM Tree**.</span><span class="sxs-lookup"><span data-stu-id="9945a-252">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="9945a-253">Open the **Element Classes** pane.</span><span class="sxs-lookup"><span data-stu-id="9945a-253">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="9945a-254">See [Add a class to an element](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="9945a-254">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="9945a-255">Below the **Add New Class** text box are all of the classes that are being applied to the specific element.</span><span class="sxs-lookup"><span data-stu-id="9945a-255">Below the **Add New Class** text box are all of the classes that are being applied to the specific element.</span></span>  
1.  <span data-ttu-id="9945a-256">Toggle the checkbox next to the class that you want to enable or disable.</span><span class="sxs-lookup"><span data-stu-id="9945a-256">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="9945a-257">Add a style rule</span><span class="sxs-lookup"><span data-stu-id="9945a-257">Add a style rule</span></span>  

<span data-ttu-id="9945a-258">Complete the following actions to add a new style rule.</span><span class="sxs-lookup"><span data-stu-id="9945a-258">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="9945a-259">[Select an element](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="9945a-259">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="9945a-260">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\).</span><span class="sxs-lookup"><span data-stu-id="9945a-260">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\).</span></span>  <span data-ttu-id="9945a-261">DevTools inserts a new rule beneath the **element.style** rule.</span><span class="sxs-lookup"><span data-stu-id="9945a-261">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="9945a-262">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span><span class="sxs-lookup"><span data-stu-id="9945a-262">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="9945a-264">Add a new style rule</span><span class="sxs-lookup"><span data-stu-id="9945a-264">Add a new style rule</span></span>  
:::image-end:::  

#### <span data-ttu-id="9945a-265">Choose which stylesheet to add a rule to</span><span class="sxs-lookup"><span data-stu-id="9945a-265">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="9945a-266">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) to choose which stylesheet to add the style rule to.</span><span class="sxs-lookup"><span data-stu-id="9945a-266">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="9945a-268">Choose a stylesheet</span><span class="sxs-lookup"><span data-stu-id="9945a-268">Choose a stylesheet</span></span>  
:::image-end:::  

#### <span data-ttu-id="9945a-269">Add a style rule to a specific location</span><span class="sxs-lookup"><span data-stu-id="9945a-269">Add a style rule to a specific location</span></span>  

<span data-ttu-id="9945a-270">Complete the following actions to add a style rule to a specific location in the **Styles** tab.</span><span class="sxs-lookup"><span data-stu-id="9945a-270">Complete the following actions to add a style rule to a specific location in the **Styles** tab.</span></span>  

1.  <span data-ttu-id="9945a-271">Hover over the style rule that is directly above where you want to add your new style rule.</span><span class="sxs-lookup"><span data-stu-id="9945a-271">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="9945a-272">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="9945a-272">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="9945a-273">Choose **Insert Style Rule Below** \(![Insert Style Rule Below][ImageNewStyleRuleIcon]\).</span><span class="sxs-lookup"><span data-stu-id="9945a-273">Choose **Insert Style Rule Below** \(![Insert Style Rule Below][ImageNewStyleRuleIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="9945a-275">Insert Style Rule Below</span><span class="sxs-lookup"><span data-stu-id="9945a-275">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <span data-ttu-id="9945a-276">Reveal the More Actions toolbar</span><span class="sxs-lookup"><span data-stu-id="9945a-276">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="9945a-277">The **More Actions** toolbar lets you perform the following actions.</span><span class="sxs-lookup"><span data-stu-id="9945a-277">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="9945a-278">Insert a style rule directly below the one you are focused on.</span><span class="sxs-lookup"><span data-stu-id="9945a-278">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="9945a-279">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span><span class="sxs-lookup"><span data-stu-id="9945a-279">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="9945a-280">Complete the following actions to reveal the **More Actions** toolbar.</span><span class="sxs-lookup"><span data-stu-id="9945a-280">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="9945a-281">In the **Styles** tab, hover over a style rule.</span><span class="sxs-lookup"><span data-stu-id="9945a-281">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="9945a-282">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span><span class="sxs-lookup"><span data-stu-id="9945a-282">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9945a-283">In the following figure, hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span><span class="sxs-lookup"><span data-stu-id="9945a-283">In the following figure, hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="9945a-285">Reveal **More Actions** \(`...`\)</span><span class="sxs-lookup"><span data-stu-id="9945a-285">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9945a-286">Hover over **More Actions** \(`...`\) to reveal the actions mentioned above.</span><span class="sxs-lookup"><span data-stu-id="9945a-286">Hover over **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9945a-287">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span><span class="sxs-lookup"><span data-stu-id="9945a-287">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="9945a-289">The **More Actions** toolbar</span><span class="sxs-lookup"><span data-stu-id="9945a-289">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="9945a-290">Toggle a declaration</span><span class="sxs-lookup"><span data-stu-id="9945a-290">Toggle a declaration</span></span>  

<span data-ttu-id="9945a-291">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span><span class="sxs-lookup"><span data-stu-id="9945a-291">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="9945a-292">[Select an element](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="9945a-292">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="9945a-293">In the **Styles** pane, hover over the rule that defines the declaration.</span><span class="sxs-lookup"><span data-stu-id="9945a-293">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="9945a-294">A checkbox appears next to each declaration.</span><span class="sxs-lookup"><span data-stu-id="9945a-294">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="9945a-295">Check \(or uncheck\) the checkbox next to the declaration.</span><span class="sxs-lookup"><span data-stu-id="9945a-295">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="9945a-296">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span><span class="sxs-lookup"><span data-stu-id="9945a-296">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="9945a-297">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span><span class="sxs-lookup"><span data-stu-id="9945a-297">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="9945a-299">Toggle a declaration</span><span class="sxs-lookup"><span data-stu-id="9945a-299">Toggle a declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="9945a-300">Add a background-color declaration</span><span class="sxs-lookup"><span data-stu-id="9945a-300">Add a background-color declaration</span></span>  

<span data-ttu-id="9945a-301">Complete the following actions to add a `background-color` declaration to an element.</span><span class="sxs-lookup"><span data-stu-id="9945a-301">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="9945a-302">Hover over the style rule that you want to add the `background-color` declaration to.</span><span class="sxs-lookup"><span data-stu-id="9945a-302">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="9945a-303">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="9945a-303">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="9945a-304">Choose **Add Background Color** \(![Add Background Color][ImageAddBackgroundColorIcon]\).</span><span class="sxs-lookup"><span data-stu-id="9945a-304">Choose **Add Background Color** \(![Add Background Color][ImageAddBackgroundColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="9945a-306">Add Background Color</span><span class="sxs-lookup"><span data-stu-id="9945a-306">Add Background Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="9945a-307">Add a color declaration</span><span class="sxs-lookup"><span data-stu-id="9945a-307">Add a color declaration</span></span>  

<span data-ttu-id="9945a-308">Complete the following actions to add a `color` declaration to an element.</span><span class="sxs-lookup"><span data-stu-id="9945a-308">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="9945a-309">Hover over the style rule that you want to add the `color` declaration to.</span><span class="sxs-lookup"><span data-stu-id="9945a-309">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="9945a-310">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="9945a-310">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="9945a-311">Choose **Add Color** \(![Add Color][ImageAddColorIcon]\).</span><span class="sxs-lookup"><span data-stu-id="9945a-311">Choose **Add Color** \(![Add Color][ImageAddColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="9945a-313">Add Color</span><span class="sxs-lookup"><span data-stu-id="9945a-313">Add Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="9945a-314">Add a box-shadow declaration</span><span class="sxs-lookup"><span data-stu-id="9945a-314">Add a box-shadow declaration</span></span>  

<span data-ttu-id="9945a-315">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span><span class="sxs-lookup"><span data-stu-id="9945a-315">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="9945a-316">Hover over the style rule that you want to add the `box-shadow` declaration to.</span><span class="sxs-lookup"><span data-stu-id="9945a-316">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="9945a-317">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="9945a-317">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="9945a-318">Choose **Add Box Shadow** \(![Add Box Shadow][ImageAddBoxShadowIcon]\).</span><span class="sxs-lookup"><span data-stu-id="9945a-318">Choose **Add Box Shadow** \(![Add Box Shadow][ImageAddBoxShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="9945a-320">Add Box Shadow</span><span class="sxs-lookup"><span data-stu-id="9945a-320">Add Box Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="9945a-321">Add a text-shadow declaration</span><span class="sxs-lookup"><span data-stu-id="9945a-321">Add a text-shadow declaration</span></span>  

<span data-ttu-id="9945a-322">Complete the following actions to add a `text-shadow` declaration to an element.</span><span class="sxs-lookup"><span data-stu-id="9945a-322">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="9945a-323">Hover over the style rule that you want to add the `text-shadow` declaration to.</span><span class="sxs-lookup"><span data-stu-id="9945a-323">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="9945a-324">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="9945a-324">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="9945a-325">Choose **Add Text Shadow** \(![Add Text Shadow][ImageAddTextShadowIcon]\).</span><span class="sxs-lookup"><span data-stu-id="9945a-325">Choose **Add Text Shadow** \(![Add Text Shadow][ImageAddTextShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="9945a-327">Add Text Shadow</span><span class="sxs-lookup"><span data-stu-id="9945a-327">Add Text Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="9945a-328">Change colors with the Color Picker</span><span class="sxs-lookup"><span data-stu-id="9945a-328">Change colors with the Color Picker</span></span>  

<span data-ttu-id="9945a-329">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span><span class="sxs-lookup"><span data-stu-id="9945a-329">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="9945a-330">Complete the following actions to open the **Color Picker**.</span><span class="sxs-lookup"><span data-stu-id="9945a-330">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="9945a-331">[Select an element](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="9945a-331">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="9945a-332">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span><span class="sxs-lookup"><span data-stu-id="9945a-332">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="9945a-333">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span><span class="sxs-lookup"><span data-stu-id="9945a-333">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9945a-334">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span><span class="sxs-lookup"><span data-stu-id="9945a-334">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="9945a-336">Color preview</span><span class="sxs-lookup"><span data-stu-id="9945a-336">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9945a-337">Choose the preview to open the **Color Picker**.</span><span class="sxs-lookup"><span data-stu-id="9945a-337">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="9945a-339">The **Color Picker**</span><span class="sxs-lookup"><span data-stu-id="9945a-339">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="9945a-340">The following figure and list descries of each of the UI elements of the **Color Picker**.</span><span class="sxs-lookup"><span data-stu-id="9945a-340">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="An example of a selected element" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="9945a-342">The **Color Picker**, annotated</span><span class="sxs-lookup"><span data-stu-id="9945a-342">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="9945a-343">1</span><span class="sxs-lookup"><span data-stu-id="9945a-343">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9945a-344">Shades</span><span class="sxs-lookup"><span data-stu-id="9945a-344">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9945a-345">2</span><span class="sxs-lookup"><span data-stu-id="9945a-345">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9945a-346">Eyedropper</span><span class="sxs-lookup"><span data-stu-id="9945a-346">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9945a-347">For more information, see [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="9945a-347">For more information, see [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9945a-348">3</span><span class="sxs-lookup"><span data-stu-id="9945a-348">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9945a-349">Copy To Clipboard</span><span class="sxs-lookup"><span data-stu-id="9945a-349">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9945a-350">Copy the **Display Value** to your clipboard.</span><span class="sxs-lookup"><span data-stu-id="9945a-350">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9945a-351">4</span><span class="sxs-lookup"><span data-stu-id="9945a-351">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9945a-352">Display Value</span><span class="sxs-lookup"><span data-stu-id="9945a-352">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9945a-353">The RGBA, HSLA, or Hex representation of the color.</span><span class="sxs-lookup"><span data-stu-id="9945a-353">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9945a-354">5</span><span class="sxs-lookup"><span data-stu-id="9945a-354">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9945a-355">Color Palette</span><span class="sxs-lookup"><span data-stu-id="9945a-355">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9945a-356">Choose one of the squares to change the color to that square.</span><span class="sxs-lookup"><span data-stu-id="9945a-356">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9945a-357">6</span><span class="sxs-lookup"><span data-stu-id="9945a-357">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9945a-358">Hue</span><span class="sxs-lookup"><span data-stu-id="9945a-358">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9945a-359">7</span><span class="sxs-lookup"><span data-stu-id="9945a-359">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9945a-360">Opacity</span><span class="sxs-lookup"><span data-stu-id="9945a-360">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9945a-361">8</span><span class="sxs-lookup"><span data-stu-id="9945a-361">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9945a-362">Display Value Switcher</span><span class="sxs-lookup"><span data-stu-id="9945a-362">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9945a-363">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span><span class="sxs-lookup"><span data-stu-id="9945a-363">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9945a-364">9</span><span class="sxs-lookup"><span data-stu-id="9945a-364">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9945a-365">Color Palette Switcher</span><span class="sxs-lookup"><span data-stu-id="9945a-365">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9945a-366">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span><span class="sxs-lookup"><span data-stu-id="9945a-366">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="9945a-367">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span><span class="sxs-lookup"><span data-stu-id="9945a-367">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="9945a-368">Sample a color off the page with the Eyedropper</span><span class="sxs-lookup"><span data-stu-id="9945a-368">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="9945a-369">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper][ImageEyedropperIcon]\) is on by default.</span><span class="sxs-lookup"><span data-stu-id="9945a-369">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper][ImageEyedropperIcon]\) is on by default.</span></span>  <span data-ttu-id="9945a-370">Complete the following actions to change the selected color to some other color on the page.</span><span class="sxs-lookup"><span data-stu-id="9945a-370">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="9945a-371">Hover over the target color in the viewport.</span><span class="sxs-lookup"><span data-stu-id="9945a-371">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="9945a-372">Choose to confirm.</span><span class="sxs-lookup"><span data-stu-id="9945a-372">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9945a-373">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span><span class="sxs-lookup"><span data-stu-id="9945a-373">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="9945a-374">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span><span class="sxs-lookup"><span data-stu-id="9945a-374">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="An example of a selected element" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="9945a-376">Using the Eyedropper</span><span class="sxs-lookup"><span data-stu-id="9945a-376">Using the Eyedropper</span></span>  
    :::image-end:::  
    
<!-- image links -->  

[ImageAddBackgroundColorIcon]: ../media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: ../media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: ../media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: ../media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: ../media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: ../media/select-an-element-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Run Commands With The Microsoft Edge DevTools Command Menu | Microsoft Docs"  
[DevToolsCSSGetStarted]: ../css/index.md "Get Started With Viewing And Changing CSS | Microsoft Docs"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Add a pseudostate to a class - Get Started With Viewing And Changing CSS | Microsoft Docs"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "View the CSS for an Element - Get Started With Viewing And Changing CSS | Microsoft Docs"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Force Microsoft Edge DevTools Into Print Preview Mode (CSS Print Media Type) | Microsoft Docs"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Make a minified file readable - JavaScript Debugging Reference | Microsoft Docs"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "The color system - Material Design"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "The box model | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Selector Types - Specificity | MDN"  

> [!NOTE]
> <span data-ttu-id="9945a-386">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9945a-386">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9945a-387">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="9945a-387">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="9945a-389">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9945a-389">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
description: Snippets are small scripts that you can author and run within the Sources panel of Microsoft Edge DevTools.  You can access and run them from any page.  When you run a Snippet, it runs from the context of the currently open page.
title: Run Snippets Of JavaScript On Any Page With Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: 5f6284179aacb471116a2d732507b010c37ef235
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993387"
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





# <span data-ttu-id="5dc5a-106">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5dc5a-106">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="5dc5a-107">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-107">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="5dc5a-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span></span>  <span data-ttu-id="5dc5a-109">They have access to the JavaScript context of the page, and you can run them on any page.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-109">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="5dc5a-110">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="5dc5a-110">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="5dc5a-111">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span><span class="sxs-lookup"><span data-stu-id="5dc5a-111">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="5dc5a-112">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-112">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="How the page looks before running the Snippet" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   <span data-ttu-id="5dc5a-114">How the page looks before running the Snippet</span><span class="sxs-lookup"><span data-stu-id="5dc5a-114">How the page looks before running the Snippet</span></span>  
:::image-end:::  

<span data-ttu-id="5dc5a-115">The Snippet source code from the previous figure.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-115">The Snippet source code from the previous figure.</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="5dc5a-116">In the following figure, the page appears after running the Snippet.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-116">In the following figure, the page appears after running the Snippet.</span></span>  <span data-ttu-id="5dc5a-117">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-117">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="How the page looks before running the Snippet" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="5dc5a-119">How the page looks after running the Snippet</span><span class="sxs-lookup"><span data-stu-id="5dc5a-119">How the page looks after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="5dc5a-120">Open the Snippets pane</span><span class="sxs-lookup"><span data-stu-id="5dc5a-120">Open the Snippets pane</span></span>   

<span data-ttu-id="5dc5a-121">The **Snippets** pane lists your Snippets.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-121">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="5dc5a-122">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-122">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="How the page looks before running the Snippet" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="5dc5a-124">The **Snippets** pane</span><span class="sxs-lookup"><span data-stu-id="5dc5a-124">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="5dc5a-125">Open the Snippets pane with a mouse</span><span class="sxs-lookup"><span data-stu-id="5dc5a-125">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="5dc5a-126">Click the **Sources** tab to open the **Sources** panel.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="5dc5a-127">The **Page** pane usually opens by default.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-127">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="How the page looks before running the Snippet" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="5dc5a-129">The **Sources** panel with the **Page** pane open on the left</span><span class="sxs-lookup"><span data-stu-id="5dc5a-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5dc5a-130">Click the **Snippets** tab to open the **Snippets** pane.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-130">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="5dc5a-131">You might need to click **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-131">You might need to click **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="5dc5a-132">Open the Snippets pane with the Command Menu</span><span class="sxs-lookup"><span data-stu-id="5dc5a-132">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="5dc5a-133">Focus your cursor somewhere inside of DevTools.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-133">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="5dc5a-134">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-134">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="5dc5a-135">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-135">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="How the page looks before running the Snippet" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="5dc5a-137">The **Show Snippets** command</span><span class="sxs-lookup"><span data-stu-id="5dc5a-137">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="5dc5a-138">Create Snippets</span><span class="sxs-lookup"><span data-stu-id="5dc5a-138">Create Snippets</span></span>   

### <span data-ttu-id="5dc5a-139">Create a Snippet through the Sources panel</span><span class="sxs-lookup"><span data-stu-id="5dc5a-139">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="5dc5a-140">[Open the **Snippets** pane](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="5dc5a-140">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="5dc5a-141">Click **New snippet**.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-141">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="5dc5a-142">Enter a name for your Snippet then press `Enter` to save.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-142">Enter a name for your Snippet then press `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="How the page looks before running the Snippet" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="5dc5a-144">Name a Snippet</span><span class="sxs-lookup"><span data-stu-id="5dc5a-144">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="5dc5a-145">Create a Snippet through the Command Menu</span><span class="sxs-lookup"><span data-stu-id="5dc5a-145">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="5dc5a-146">Focus your cursor somewhere inside of DevTools.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-146">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="5dc5a-147">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-147">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="5dc5a-148">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-148">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="How the page looks before running the Snippet" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="5dc5a-150">The command for creating a new Snippet</span><span class="sxs-lookup"><span data-stu-id="5dc5a-150">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="5dc5a-151">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-151">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="5dc5a-152">Edit Snippets</span><span class="sxs-lookup"><span data-stu-id="5dc5a-152">Edit Snippets</span></span>   

1.  <span data-ttu-id="5dc5a-153">[Open the **Snippets** pane](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="5dc5a-153">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="5dc5a-154">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-154">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="How the page looks before running the Snippet" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="5dc5a-156">The **Code Editor**</span><span class="sxs-lookup"><span data-stu-id="5dc5a-156">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5dc5a-157">Use the **Code Editor** to add JavaScript to your Snippet.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-157">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="5dc5a-158">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-158">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="5dc5a-159">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-159">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="How the page looks before running the Snippet" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="5dc5a-161">An asterisk next to the Snippet name, which indicates unsaved code</span><span class="sxs-lookup"><span data-stu-id="5dc5a-161">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="5dc5a-162">Run Snippets</span><span class="sxs-lookup"><span data-stu-id="5dc5a-162">Run Snippets</span></span>   

### <span data-ttu-id="5dc5a-163">Run a Snippet from the Sources panel</span><span class="sxs-lookup"><span data-stu-id="5dc5a-163">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="5dc5a-164">[Open the **Snippets** pane](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="5dc5a-164">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="5dc5a-165">Click the name of the Snippet that you want to run.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-165">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="5dc5a-166">The Snippet opens in the **Code Editor**.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-166">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="5dc5a-167">Click **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="5dc5a-167">Click **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="5dc5a-168">Run a Snippet with the Command Menu</span><span class="sxs-lookup"><span data-stu-id="5dc5a-168">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="5dc5a-169">Focus your cursor somewhere inside of DevTools.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-169">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="5dc5a-170">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-170">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="5dc5a-171">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-171">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="How the page looks before running the Snippet" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="5dc5a-173">Running a Snippet from the **Command Menu**</span><span class="sxs-lookup"><span data-stu-id="5dc5a-173">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5dc5a-174">Press `Enter` to run the Snippet.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-174">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="5dc5a-175">Rename Snippets</span><span class="sxs-lookup"><span data-stu-id="5dc5a-175">Rename Snippets</span></span>   

1.  <span data-ttu-id="5dc5a-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="5dc5a-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="5dc5a-177">Right-click the Snippet name and select **Rename**.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-177">Right-click the Snippet name and select **Rename**.</span></span>  
    
## <span data-ttu-id="5dc5a-178">Delete Snippets</span><span class="sxs-lookup"><span data-stu-id="5dc5a-178">Delete Snippets</span></span>   

1.  <span data-ttu-id="5dc5a-179">[Open the **Snippets** pane](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="5dc5a-179">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="5dc5a-180">Right-click the Snippet name and select **Remove**.</span><span class="sxs-lookup"><span data-stu-id="5dc5a-180">Right-click the Snippet name and select **Remove**.</span></span>  
    
<!--  
 


-->  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Console overview | Microsoft Docs"  
[DevToolsSourcesPanel]: ../sources.md "Sources panel overview | Microsoft Docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="5dc5a-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5dc5a-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5dc5a-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="5dc5a-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="5dc5a-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5dc5a-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

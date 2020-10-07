---
description: Emulate color vision deficiencies, Dock To Left in the Command Menu, and more.
title: What's new in DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: f9eb306ab7b30495c91ff4a70797898459d7e722
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015482"
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

# <span data-ttu-id="8745a-104">What's New In DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="8745a-104">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="8745a-105">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span><span class="sxs-lookup"><span data-stu-id="8745a-105">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="8745a-106">Check out our [blog post][WindowsBlogStableRelease] for more info.</span><span class="sxs-lookup"><span data-stu-id="8745a-106">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="8745a-107">Here are the new features available in the DevTools in Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="8745a-107">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <span data-ttu-id="8745a-108">Announcements from the Microsoft Edge DevTools team</span><span class="sxs-lookup"><span data-stu-id="8745a-108">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="8745a-109">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span><span class="sxs-lookup"><span data-stu-id="8745a-109">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="8745a-110">Check them out to try new features in the DevTools, Visual Studio Code extensions, and more.</span><span class="sxs-lookup"><span data-stu-id="8745a-110">Check them out to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="8745a-111">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="8745a-111">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="8745a-112">Remotely debug Microsoft Edge on Windows 10 Devices</span><span class="sxs-lookup"><span data-stu-id="8745a-112">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="8745a-113">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="8745a-113">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="8745a-114">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PprgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span><span class="sxs-lookup"><span data-stu-id="8745a-114">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PprgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="8745a-116">The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="8745a-116">The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span><span class="sxs-lookup"><span data-stu-id="8745a-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="8745a-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span><span class="sxs-lookup"><span data-stu-id="8745a-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

### <span data-ttu-id="8745a-119">New ways to access Settings</span><span class="sxs-lookup"><span data-stu-id="8745a-119">New ways to access Settings</span></span>  

<span data-ttu-id="8745a-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span><span class="sxs-lookup"><span data-stu-id="8745a-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="8745a-121">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span><span class="sxs-lookup"><span data-stu-id="8745a-121">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="8745a-122">Open Settings with the gear icon next to Console alerts and the main menu.</span><span class="sxs-lookup"><span data-stu-id="8745a-122">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="8745a-124">The gear icon opens **Settings** in the DevTools</span><span class="sxs-lookup"><span data-stu-id="8745a-124">The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-125">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span><span class="sxs-lookup"><span data-stu-id="8745a-125">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="8745a-127">**Main Menu** > **More tools** > **Settings**</span><span class="sxs-lookup"><span data-stu-id="8745a-127">**Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-128">Chromium issue [#1050855][CR1050855]</span><span class="sxs-lookup"><span data-stu-id="8745a-128">Chromium issue [#1050855][CR1050855]</span></span>

### <span data-ttu-id="8745a-129">New and improved infobars</span><span class="sxs-lookup"><span data-stu-id="8745a-129">New and improved infobars</span></span>

<span data-ttu-id="8745a-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span><span class="sxs-lookup"><span data-stu-id="8745a-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="8745a-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span><span class="sxs-lookup"><span data-stu-id="8745a-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="8745a-133">Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span><span class="sxs-lookup"><span data-stu-id="8745a-133">Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-134">Chromium issue [#1056348][CR1056348]</span><span class="sxs-lookup"><span data-stu-id="8745a-134">Chromium issue [#1056348][CR1056348]</span></span>

### <span data-ttu-id="8745a-135">Navigate the Color Picker with your keyboard</span><span class="sxs-lookup"><span data-stu-id="8745a-135">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="8745a-136">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span><span class="sxs-lookup"><span data-stu-id="8745a-136">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="8745a-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span><span class="sxs-lookup"><span data-stu-id="8745a-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="8745a-139">You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span><span class="sxs-lookup"><span data-stu-id="8745a-139">You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-140">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span><span class="sxs-lookup"><span data-stu-id="8745a-140">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="8745a-141">Chromium issue [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="8745a-141">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="8745a-142">Properties tab now populates after a page refresh</span><span class="sxs-lookup"><span data-stu-id="8745a-142">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="8745a-143">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span><span class="sxs-lookup"><span data-stu-id="8745a-143">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="8745a-144">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span><span class="sxs-lookup"><span data-stu-id="8745a-144">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="8745a-146">In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span><span class="sxs-lookup"><span data-stu-id="8745a-146">In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-147">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span><span class="sxs-lookup"><span data-stu-id="8745a-147">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="8745a-149">In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span><span class="sxs-lookup"><span data-stu-id="8745a-149">In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-150">Chromium issue [#1050999][CR1050999]</span><span class="sxs-lookup"><span data-stu-id="8745a-150">Chromium issue [#1050999][CR1050999]</span></span>  

### <span data-ttu-id="8745a-151">Use the arrow keys to scroll in the Changes tool</span><span class="sxs-lookup"><span data-stu-id="8745a-151">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="8745a-152">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span><span class="sxs-lookup"><span data-stu-id="8745a-152">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="8745a-153">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span><span class="sxs-lookup"><span data-stu-id="8745a-153">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="8745a-154">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span><span class="sxs-lookup"><span data-stu-id="8745a-154">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="8745a-155">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span><span class="sxs-lookup"><span data-stu-id="8745a-155">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="8745a-156">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span><span class="sxs-lookup"><span data-stu-id="8745a-156">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="8745a-157">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span><span class="sxs-lookup"><span data-stu-id="8745a-157">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="8745a-159">In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span><span class="sxs-lookup"><span data-stu-id="8745a-159">In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-160">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span><span class="sxs-lookup"><span data-stu-id="8745a-160">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="8745a-161">Chromium issue [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="8745a-161">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="8745a-162">Announcements from the Chromium project</span><span class="sxs-lookup"><span data-stu-id="8745a-162">Announcements from the Chromium project</span></span>  

<span data-ttu-id="8745a-163">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span><span class="sxs-lookup"><span data-stu-id="8745a-163">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="8745a-164">Emulate vision deficiencies</span><span class="sxs-lookup"><span data-stu-id="8745a-164">Emulate vision deficiencies</span></span>  

<span data-ttu-id="8745a-165">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span><span class="sxs-lookup"><span data-stu-id="8745a-165">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="8745a-167">Emulating blurred vision</span><span class="sxs-lookup"><span data-stu-id="8745a-167">Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-168">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span><span class="sxs-lookup"><span data-stu-id="8745a-168">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="8745a-169">Color Vision Deficiency</span><span class="sxs-lookup"><span data-stu-id="8745a-169">Color Vision Deficiency</span></span> | <span data-ttu-id="8745a-170">Details</span><span class="sxs-lookup"><span data-stu-id="8745a-170">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8745a-171">Protanopia</span><span class="sxs-lookup"><span data-stu-id="8745a-171">Protanopia</span></span> | <span data-ttu-id="8745a-172">The inability to perceive any red light.</span><span class="sxs-lookup"><span data-stu-id="8745a-172">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="8745a-173">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="8745a-173">Deuteranopia</span></span> | <span data-ttu-id="8745a-174">The inability to perceive any green light.</span><span class="sxs-lookup"><span data-stu-id="8745a-174">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="8745a-175">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="8745a-175">Tritanopia</span></span> | <span data-ttu-id="8745a-176">The inability to perceive any blue light.</span><span class="sxs-lookup"><span data-stu-id="8745a-176">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="8745a-177">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="8745a-177">Achromatopsia</span></span> | <span data-ttu-id="8745a-178">The inability to perceive any color, except for shades of grey \(extremely rare\).</span><span class="sxs-lookup"><span data-stu-id="8745a-178">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="8745a-179">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span><span class="sxs-lookup"><span data-stu-id="8745a-179">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="8745a-180">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span><span class="sxs-lookup"><span data-stu-id="8745a-180">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="8745a-181">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span><span class="sxs-lookup"><span data-stu-id="8745a-181">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>  

<span data-ttu-id="8745a-182">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span><span class="sxs-lookup"><span data-stu-id="8745a-182">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="8745a-183">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span><span class="sxs-lookup"><span data-stu-id="8745a-183">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="8745a-184">Chromium issue [#1003700][CR1003700]</span><span class="sxs-lookup"><span data-stu-id="8745a-184">Chromium issue [#1003700][CR1003700]</span></span>  

### <span data-ttu-id="8745a-185">Emulate locales</span><span class="sxs-lookup"><span data-stu-id="8745a-185">Emulate locales</span></span>  

<span data-ttu-id="8745a-186">Emulate locales by setting a location in **Sensors** > **Location**.</span><span class="sxs-lookup"><span data-stu-id="8745a-186">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="8745a-187">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span><span class="sxs-lookup"><span data-stu-id="8745a-187">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="8745a-188">APIs, for example:</span><span class="sxs-lookup"><span data-stu-id="8745a-188">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="8745a-189">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span><span class="sxs-lookup"><span data-stu-id="8745a-189">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="8745a-190">DOM APIs such as `navigator.language` and</span><span class="sxs-lookup"><span data-stu-id="8745a-190">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="8745a-191">The [Accept-Language][MDNAcceptLanguage] HTTP request header</span><span class="sxs-lookup"><span data-stu-id="8745a-191">The [Accept-Language][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="8745a-192">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span><span class="sxs-lookup"><span data-stu-id="8745a-192">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="8745a-193">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span><span class="sxs-lookup"><span data-stu-id="8745a-193">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="8745a-195">Emulating a locale</span><span class="sxs-lookup"><span data-stu-id="8745a-195">Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-196">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="8745a-196">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="8745a-197">Chromium issue [#1051822][CR1051822]</span><span class="sxs-lookup"><span data-stu-id="8745a-197">Chromium issue [#1051822][CR1051822]</span></span>

### <span data-ttu-id="8745a-198">Cross-Origin Embedder Policy (COEP) debugging</span><span class="sxs-lookup"><span data-stu-id="8745a-198">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="8745a-199">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span><span class="sxs-lookup"><span data-stu-id="8745a-199">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="8745a-200">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span><span class="sxs-lookup"><span data-stu-id="8745a-200">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="8745a-202">Blocked requests in the **Status** column</span><span class="sxs-lookup"><span data-stu-id="8745a-202">Blocked requests in the **Status** column</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-203">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span><span class="sxs-lookup"><span data-stu-id="8745a-203">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="8745a-205">More guidance in the **Response Headers** section</span><span class="sxs-lookup"><span data-stu-id="8745a-205">More guidance in the **Response Headers** section</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-206">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span><span class="sxs-lookup"><span data-stu-id="8745a-206">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="8745a-207">Chromium issue [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="8745a-207">Chromium issue [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="8745a-208">New icons for breakpoints, conditional breakpoints, and logpoints</span><span class="sxs-lookup"><span data-stu-id="8745a-208">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="8745a-209">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span><span class="sxs-lookup"><span data-stu-id="8745a-209">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="8745a-210">Breakpoints \(</span><span class="sxs-lookup"><span data-stu-id="8745a-210">Breakpoints \(</span></span>![Breakpoint](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="8745a-212">\) are represented by red circles.</span><span class="sxs-lookup"><span data-stu-id="8745a-212">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="8745a-213">Conditional Breakpoints \(</span><span class="sxs-lookup"><span data-stu-id="8745a-213">Conditional Breakpoints \(</span></span>![Conditional Breakpoint](../../media/2020/03/conditional.msft.png)<span data-ttu-id="8745a-215">\) are represented by half-red half-white circles.</span><span class="sxs-lookup"><span data-stu-id="8745a-215">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="8745a-216">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="8745a-216">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="8745a-218">\) are represented by red circles with Console icons.</span><span class="sxs-lookup"><span data-stu-id="8745a-218">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="8745a-219">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span><span class="sxs-lookup"><span data-stu-id="8745a-219">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="8745a-220">Chromium issue [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="8745a-220">Chromium issue [#1041830][CR1041830]</span></span>  

### <span data-ttu-id="8745a-221">View network requests that set a specific cookie path</span><span class="sxs-lookup"><span data-stu-id="8745a-221">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="8745a-222">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span><span class="sxs-lookup"><span data-stu-id="8745a-222">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="8745a-223">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span><span class="sxs-lookup"><span data-stu-id="8745a-223">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="8745a-224">Dock to left from the Command Menu</span><span class="sxs-lookup"><span data-stu-id="8745a-224">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="8745a-225">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span><span class="sxs-lookup"><span data-stu-id="8745a-225">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="8745a-227">DevTools docked to the left of the viewport</span><span class="sxs-lookup"><span data-stu-id="8745a-227">DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8745a-228">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [Main Menu][DevtoolsCustomizePlacementsChangeMainMenu].</span><span class="sxs-lookup"><span data-stu-id="8745a-228">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [Main Menu][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="8745a-229">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span><span class="sxs-lookup"><span data-stu-id="8745a-229">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="8745a-230">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span><span class="sxs-lookup"><span data-stu-id="8745a-230">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="8745a-231">Chromium issue [#1011679][CR1011679]</span><span class="sxs-lookup"><span data-stu-id="8745a-231">Chromium issue [#1011679][CR1011679]</span></span>  

### <span data-ttu-id="8745a-232">The Audits panel is now the Lighthouse panel</span><span class="sxs-lookup"><span data-stu-id="8745a-232">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="8745a-233">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span><span class="sxs-lookup"><span data-stu-id="8745a-233">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="8745a-235">The Lighthouse panel</span><span class="sxs-lookup"><span data-stu-id="8745a-235">The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8745a-236">The **Lighthouse** panel provides links to content hosted on third-party websites.</span><span class="sxs-lookup"><span data-stu-id="8745a-236">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="8745a-237">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span><span class="sxs-lookup"><span data-stu-id="8745a-237">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="8745a-238">Delete all Local Overrides in a folder</span><span class="sxs-lookup"><span data-stu-id="8745a-238">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="8745a-239">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span><span class="sxs-lookup"><span data-stu-id="8745a-239">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="8745a-241">Delete all overrides</span><span class="sxs-lookup"><span data-stu-id="8745a-241">Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-242">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span><span class="sxs-lookup"><span data-stu-id="8745a-242">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="8745a-243">Chromium issue [#1016501][CR1016501]</span><span class="sxs-lookup"><span data-stu-id="8745a-243">Chromium issue [#1016501][CR1016501]</span></span>  

### <span data-ttu-id="8745a-244">Updated Long tasks UI</span><span class="sxs-lookup"><span data-stu-id="8745a-244">Updated Long tasks UI</span></span>  

<span data-ttu-id="8745a-245">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span><span class="sxs-lookup"><span data-stu-id="8745a-245">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="8745a-246">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span><span class="sxs-lookup"><span data-stu-id="8745a-246">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="8745a-247">The Long Task portion of a task is now colored with a striped red background.</span><span class="sxs-lookup"><span data-stu-id="8745a-247">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="8745a-249">The new Long Task UI</span><span class="sxs-lookup"><span data-stu-id="8745a-249">The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="8745a-250">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span><span class="sxs-lookup"><span data-stu-id="8745a-250">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="8745a-251">Chromium issue [#1054447][CR1054447]</span><span class="sxs-lookup"><span data-stu-id="8745a-251">Chromium issue [#1054447][CR1054447]</span></span>  

### <span data-ttu-id="8745a-252">Maskable icon support in the Manifest pane</span><span class="sxs-lookup"><span data-stu-id="8745a-252">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="8745a-253">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span><span class="sxs-lookup"><span data-stu-id="8745a-253">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="8745a-254">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PprgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span><span class="sxs-lookup"><span data-stu-id="8745a-254">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PprgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="8745a-255">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span><span class="sxs-lookup"><span data-stu-id="8745a-255">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="The Remote Tools for Microsoft Edge (Beta) app available in the Microsoft Store" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="8745a-257">The **Show only the minimum safe area for maskable icons** checkbox</span><span class="sxs-lookup"><span data-stu-id="8745a-257">The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8745a-258">This feature launched in Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="8745a-258">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="8745a-259">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span><span class="sxs-lookup"><span data-stu-id="8745a-259">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="8745a-260">Download the Microsoft Edge preview channels</span><span class="sxs-lookup"><span data-stu-id="8745a-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="8745a-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span><span class="sxs-lookup"><span data-stu-id="8745a-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="8745a-262">The preview channels give you access to the latest DevTools features.</span><span class="sxs-lookup"><span data-stu-id="8745a-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="8745a-263">Getting in touch with Microsoft Edge DevTools team</span><span class="sxs-lookup"><span data-stu-id="8745a-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "What's New In DevTools (Microsoft Edge 81) | Microsoft Docs"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Run Commands With The Microsoft Edge DevTools Command Menu | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Change colors with the Color Picker | Microsoft Docs"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Get Started With Viewing And Changing CSS | Microsoft Docs"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Change placement from the main menu | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "View main thread activity | Microsoft Docs"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyze rendering performance with the Rendering tab | Microsoft Docs"  
[PprgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Progressive Web Apps on Windows | Microsoft Docs"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Get Started with Remote Debugging Windows 10 Devices | Microsoft Docs"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Line-of-code breakpoints - How To Pause Your Code With Breakpoints In Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filter requests by properties - Network analysis reference | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Settings - Customize Microsoft Edge DevTools  | Microsoft Docs"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Windows Device Portal overview"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Remote Tools for Microsoft Edge (Beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Preview Channels"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Update on Stable channel releases for Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "New Issue - MicrosoftDocs/edge-developer - GitHub"  

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Post a Tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools Twitter account"  
[TheWebWeWant]: https://webwewant.fyi "The Web We Want"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Types of Colour Blindness"  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-Cookie | MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Locale-dependent code example"  

[CR963183]: https://crbug.com/963183 "Issue 963183: DevTools are not WCAG compliant"  
[CR1003700]: https://crbug.com/1003700 "Issue 1003700: Add DevTools support for Color Vision Deficiency simulation"  
[CR1011679]: https://crbug.com/1011679 "Issue 1011679: Introduce 'Dock to Left' using the Command Menu"  
[CR1016501]: https://crbug.com/1016501 "Issue 1016501: Feature Request: Button to delete all local overrides"  
[CR1050999]: https://crbug.com/1050999 "Issue 1050999: Properties Tab"  
[CR1051466]: https://crbug.com/1051466 "Issue 1051466: Support COOP/COEP debugging in DevTools"  
[CR1054447]: https://crbug.com/1054447 "Issue 1054447: Update performance metrics in DevTools Timeline"  
[CR1051822]: https://crbug.com/1051822 "Issue 1051822: DevTools: add UI to emulate locale"
[CR1041830]: https://crbug.com/1041830 "Issue 1041830: Improve colors for breakpoints"
[CR1050855]: https://crbug.com/1050855 "Issue 1050855: Settings view is difficult to discover"
[CR1056348]: https://crbug.com/1056348 "Issue 1056348: Infobar Component Refresh"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "COOP and COEP explained - Cross-Origin Opener Policy"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "COOP and COEP explained - Cross-Origin Embedder Policy"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Lighthouse | GitHub"  

> [!NOTE]
> <span data-ttu-id="8745a-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8745a-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8745a-306">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="8745a-306">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="8745a-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8745a-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

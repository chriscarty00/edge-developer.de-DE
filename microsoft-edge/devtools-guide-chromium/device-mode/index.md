---
description: Verwenden Sie virtuelle Geräte in Microsoft Edge zum Erstellen von mobilen First-Websites.
title: Emulieren von mobilen Geräten in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web Development, F12 Tools, devtools, Emulation, Device, Simulation, Mobile
ms.openlocfilehash: c70b81eabb145461eac7d1b9a8f438d6a18fbc89
ms.sourcegitcommit: cc96ada9679b23feb841e46f19d8077251c4a4df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "10997089"
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

# <span data-ttu-id="cbda5-104">Emulieren von mobilen Geräten in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="cbda5-104">Emulate mobile devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="cbda5-105">Verwenden Sie die **Geräteemulation** , um ungefähr zu sehen, wie Ihre Seite auf einem mobilen Gerät aussieht und reagiert.</span><span class="sxs-lookup"><span data-stu-id="cbda5-105">Use **Device emulation** to approximate how your page looks and responds on a mobile device.</span></span>  <span data-ttu-id="cbda5-106">Die Microsoft Edge-devtools bieten eine Sammlung von Features, die Ihnen beim emulieren mobiler Geräte helfen.</span><span class="sxs-lookup"><span data-stu-id="cbda5-106">The Microsoft Edge DevTools provide a collection of features to help you emulate mobile devices.</span></span>  <span data-ttu-id="cbda5-107">Die Sammlung umfasst die folgenden Features.</span><span class="sxs-lookup"><span data-stu-id="cbda5-107">The collection includes the following features.</span></span>  

*   [<span data-ttu-id="cbda5-108">Simulieren eines mobilen Viewports</span><span class="sxs-lookup"><span data-stu-id="cbda5-108">Simulate a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="cbda5-109">Netzwerk drosseln</span><span class="sxs-lookup"><span data-stu-id="cbda5-109">Throttle the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="cbda5-110">Drosseln der CPU</span><span class="sxs-lookup"><span data-stu-id="cbda5-110">Throttle the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="cbda5-111">Geolokation simulieren</span><span class="sxs-lookup"><span data-stu-id="cbda5-111">Simulate geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="cbda5-112">Ausrichtung einstellen</span><span class="sxs-lookup"><span data-stu-id="cbda5-112">Set orientation</span></span>](#set-orientation)  
*   [<span data-ttu-id="cbda5-113">Benutzer-Agent-Zeichenfolge einrichten</span><span class="sxs-lookup"><span data-stu-id="cbda5-113">Set the user agent string</span></span>](#set-user-agent-string)  

## <span data-ttu-id="cbda5-114">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="cbda5-114">Limitations</span></span>  

<span data-ttu-id="cbda5-115">Die **Geräteemulation** ist eine Näherung des Erscheinungsbild Ihrer Seite auf einem mobilen Gerät in [erster Reihe][WikiApproximation] .</span><span class="sxs-lookup"><span data-stu-id="cbda5-115">**Device emulation** is a [first-order approximation][WikiApproximation] of the look and feel of your page on a mobile device.</span></span>  <span data-ttu-id="cbda5-116">Die **Geräteemulation** führt Ihren Code nicht auf einem mobilen Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-116">**Device emulation** does not actually run your code on a mobile device.</span></span>  <span data-ttu-id="cbda5-117">Stattdessen simulieren Sie die mobile Benutzeroberfläche auf Ihrem Laptop oder Desktop.</span><span class="sxs-lookup"><span data-stu-id="cbda5-117">Instead you simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="cbda5-118">Einige Aspekte von mobilen Geräten werden in devtools nie emuliert.</span><span class="sxs-lookup"><span data-stu-id="cbda5-118">Some aspects of mobile devices are never emulated in DevTools.</span></span>  <span data-ttu-id="cbda5-119">Die Architektur von mobilen CPUs unterscheidet sich beispielsweise von der Architektur von Laptop-oder Desktop-CPUs.</span><span class="sxs-lookup"><span data-stu-id="cbda5-119">For example, the architecture of mobile CPUs is different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="cbda5-120">Im Zweifelsfall ist es am besten, wenn Sie Ihre Seite auf einem mobilen Gerät ausführen.</span><span class="sxs-lookup"><span data-stu-id="cbda5-120">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="cbda5-121">Verwenden Sie [Remote Debuggen] [DevToolsRemoteDebugging], um mit dem Code einer Seite von Ihrem Computer zu interagieren, während Ihre Seite auf einem mobilen Gerät ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cbda5-121">Use [Remote Debugging][DevToolsRemoteDebugging] to interact with the code of a page from your machine while your page actually runs on a mobile device.</span></span>  <span data-ttu-id="cbda5-122">Sie können anzeigen, ändern, Debuggen, Profil oder alle vier während der Interaktion mit dem Code.</span><span class="sxs-lookup"><span data-stu-id="cbda5-122">You may view, change, debug, profile, or all four while you interact with the code.</span></span>  <span data-ttu-id="cbda5-123">Ihr Computer kann ein Notizbuch oder ein Desktopcomputer sein.</span><span class="sxs-lookup"><span data-stu-id="cbda5-123">Your machine may be a notebook or desktop computer.</span></span>  

## <span data-ttu-id="cbda5-124">Simulieren eines mobilen Viewports</span><span class="sxs-lookup"><span data-stu-id="cbda5-124">Simulate a mobile viewport</span></span>  

<span data-ttu-id="cbda5-125">Wählen Sie **Geräteemulation umschalten**  \ ( ![ Gerätesymbolleiste umschalten ][ImageDeviceToolbarIcon] \) aus, oder wählen Sie **anpassen und Steuern devtools** \ ( `...` \) > **Geräteemulation** aus, um die Benutzeroberfläche zu öffnen, mit der Sie ein mobiles Viewport simulieren können.</span><span class="sxs-lookup"><span data-stu-id="cbda5-125">Choose **Toggle device emulation**  \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) or choose **Customize and control DevTools** \(`...`\) > **Device emulation** to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    <span data-ttu-id="cbda5-127">Die Gerätesymbolleiste</span><span class="sxs-lookup"><span data-stu-id="cbda5-127">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="cbda5-128">Standardmäßig wird die Gerätesymbolleiste im reaktionsfähigen Ansichtsfenster Modus geöffnet.</span><span class="sxs-lookup"><span data-stu-id="cbda5-128">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="cbda5-129">Reaktionsfähiger viewportmodus</span><span class="sxs-lookup"><span data-stu-id="cbda5-129">Responsive Viewport Mode</span></span>  

<span data-ttu-id="cbda5-130">Ziehen Sie die Ziehpunkte, um das Aussehen und Verhalten Ihrer Seite über mehrere Bildschirmgrößen schnell zu testen, um die Größe des Viewports auf die gewünschten Abmessungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cbda5-130">To quickly test the look and feel of your page across multiple screen sizes, drag the handles to resize the viewport to your required dimensions.</span></span>  <span data-ttu-id="cbda5-131">Sie können auch bestimmte Werte in die Felder Breite und Höhe eingeben.</span><span class="sxs-lookup"><span data-stu-id="cbda5-131">You may also enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="cbda5-132">In der folgenden Abbildung ist die Breite auf festzulegen, `626` und die Höhe ist auf festzulegen `516` .</span><span class="sxs-lookup"><span data-stu-id="cbda5-132">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    <span data-ttu-id="cbda5-134">Die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus</span><span class="sxs-lookup"><span data-stu-id="cbda5-134">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <span data-ttu-id="cbda5-135">Anzeigen von medienabfragen</span><span class="sxs-lookup"><span data-stu-id="cbda5-135">Show media queries</span></span>  

<span data-ttu-id="cbda5-136">Wenn Sie medienabfragen auf der Seite definiert haben, wechseln Sie zu den Viewport-Dimensionen, in denen diese medienabfragen wirksam werden, indem Sie medienabfrage Haltepunkte oberhalb des Viewports anzeigen.</span><span class="sxs-lookup"><span data-stu-id="cbda5-136">If you have defined media queries on your page, jump to the viewport dimensions where those media queries take effect by showing media query breakpoints above your viewport.</span></span>  <span data-ttu-id="cbda5-137">Wählen Sie **Weitere Optionen**  >  **Anzeigen von medienabfragen**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-137">Choose **More options** > **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Anzeigen von medienabfragen" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="cbda5-139">Anzeigen von medienabfragen</span><span class="sxs-lookup"><span data-stu-id="cbda5-139">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="cbda5-140">Wählen Sie einen Haltepunkt aus, um die Breite des Viewports so zu ändern, dass die medienabfrage ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="cbda5-140">Choose a breakpoint to change the width of the viewport so that the media query gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Wählen Sie einen Haltepunkt aus, um die Breite des Viewports zu ändern." lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="cbda5-142">Wählen Sie einen Haltepunkt aus, um die Breite des Viewports zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cbda5-142">Choose a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <span data-ttu-id="cbda5-143">Einrichten des Gerätetyps</span><span class="sxs-lookup"><span data-stu-id="cbda5-143">Set the device type</span></span>  

<span data-ttu-id="cbda5-144">Verwenden Sie die Liste **Gerätetyp** , um ein mobiles Gerät oder ein Desktop Gerät zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="cbda5-144">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Liste der Gerätetypen" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="cbda5-146">Liste der **Gerätetypen**</span><span class="sxs-lookup"><span data-stu-id="cbda5-146">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="cbda5-147">In der folgenden Tabelle werden die Unterschiede zwischen den verfügbaren Optionen für Gerätetypen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cbda5-147">The following table describes the differences between the available device type options.</span></span>  <span data-ttu-id="cbda5-148">Die Spalte "Rendering-Methode" bezieht sich darauf, ob Microsoft Edge die Seite als mobiles oder Desktop-Viewport rendert.</span><span class="sxs-lookup"><span data-stu-id="cbda5-148">The Rendering method column refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="cbda5-149">Die Spalte Cursor Symbol bezieht sich auf den Typ des Cursors, den Sie sehen, wenn Sie auf der Seite zeigen.</span><span class="sxs-lookup"><span data-stu-id="cbda5-149">The Cursor icon column refers to what type of cursor you see when you hover on the page.</span></span>  <span data-ttu-id="cbda5-150">Die Spalte "ausgelöste Ereignisse" bezieht sich darauf, ob die Seite ausgelöst `touch` `click` wird oder Ereignisse bei der Interaktion mit der Seite ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="cbda5-150">The Events triggered column refers to whether the page triggers `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="cbda5-151">Option</span><span class="sxs-lookup"><span data-stu-id="cbda5-151">Option</span></span> | <span data-ttu-id="cbda5-152">Rendering-Methode</span><span class="sxs-lookup"><span data-stu-id="cbda5-152">Rendering method</span></span> | <span data-ttu-id="cbda5-153">Cursor Symbol</span><span class="sxs-lookup"><span data-stu-id="cbda5-153">Cursor icon</span></span> | <span data-ttu-id="cbda5-154">Ausgelöste Ereignisse</span><span class="sxs-lookup"><span data-stu-id="cbda5-154">Events triggered</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="cbda5-155">Mobilgeräte</span><span class="sxs-lookup"><span data-stu-id="cbda5-155">Mobile</span></span> | <span data-ttu-id="cbda5-156">Mobilgeräte</span><span class="sxs-lookup"><span data-stu-id="cbda5-156">Mobile</span></span> | <span data-ttu-id="cbda5-157">Kreis</span><span class="sxs-lookup"><span data-stu-id="cbda5-157">Circle</span></span> | <span data-ttu-id="cbda5-158">Toucheingabe</span><span class="sxs-lookup"><span data-stu-id="cbda5-158">touch</span></span> |  
| <span data-ttu-id="cbda5-159">Mobil \ (kein Touch \)</span><span class="sxs-lookup"><span data-stu-id="cbda5-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="cbda5-160">Mobilgeräte</span><span class="sxs-lookup"><span data-stu-id="cbda5-160">Mobile</span></span> | <span data-ttu-id="cbda5-161">Normal</span><span class="sxs-lookup"><span data-stu-id="cbda5-161">Normal</span></span> | <span data-ttu-id="cbda5-162"> auf </span><span class="sxs-lookup"><span data-stu-id="cbda5-162">click</span></span> |  
| <span data-ttu-id="cbda5-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="cbda5-163">Desktop</span></span> | <span data-ttu-id="cbda5-164">Desktop</span><span class="sxs-lookup"><span data-stu-id="cbda5-164">Desktop</span></span> | <span data-ttu-id="cbda5-165">Normal</span><span class="sxs-lookup"><span data-stu-id="cbda5-165">Normal</span></span> | <span data-ttu-id="cbda5-166"> auf </span><span class="sxs-lookup"><span data-stu-id="cbda5-166">click</span></span> |  
| <span data-ttu-id="cbda5-167">Desktop \ (tippen Sie auf \)</span><span class="sxs-lookup"><span data-stu-id="cbda5-167">Desktop \(touch\)</span></span> | <span data-ttu-id="cbda5-168">Desktop</span><span class="sxs-lookup"><span data-stu-id="cbda5-168">Desktop</span></span> | <span data-ttu-id="cbda5-169">Kreis</span><span class="sxs-lookup"><span data-stu-id="cbda5-169">Circle</span></span> | <span data-ttu-id="cbda5-170">Toucheingabe</span><span class="sxs-lookup"><span data-stu-id="cbda5-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="cbda5-171">Wenn die Liste **Gerätetyp** nicht angezeigt wird, wählen Sie **Weitere Optionen**  >  **Add Device Type**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-171">If the **Device Type** list is not displayed, choose **More options** > **Add device type**.</span></span>  

### <span data-ttu-id="cbda5-172">Ansichtsfenster Modus für mobile Geräte</span><span class="sxs-lookup"><span data-stu-id="cbda5-172">Mobile Device Viewport Mode</span></span>  

<span data-ttu-id="cbda5-173">Wenn Sie die Abmessungen eines bestimmten mobilen Geräts simulieren möchten, wählen Sie das Gerät in der **Geräte** Liste aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Geräteliste" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="cbda5-175">**Geräte** Liste</span><span class="sxs-lookup"><span data-stu-id="cbda5-175">The **Device** list</span></span>  
:::image-end:::  

#### <span data-ttu-id="cbda5-176">Drehen des Viewports in Querformat</span><span class="sxs-lookup"><span data-stu-id="cbda5-176">Rotate the viewport to landscape orientation</span></span>  

<span data-ttu-id="cbda5-177">Testen Sie Ihre Webseite im Querformat.</span><span class="sxs-lookup"><span data-stu-id="cbda5-177">Test your webpage in landscape orientation.</span></span>  

*   <span data-ttu-id="cbda5-178">Wenn Sie das Ansichtsfenster in Querformat drehen möchten, wählen Sie **drehen** \ ( ![ drehen ][ImageRotateIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-178">To rotate the viewport to landscape orientation, choose **Rotate** \(![Rotate][ImageRotateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Im Querformat angezeigte Seite" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       <span data-ttu-id="cbda5-180">Im Querformat angezeigte Seite</span><span class="sxs-lookup"><span data-stu-id="cbda5-180">Page displayed in landscape orientation</span></span>  
    :::image-end:::  
    
> [!NOTE]
> <span data-ttu-id="cbda5-181">Die Schaltfläche **drehen** verschwindet, wenn die **Gerätesymbolleiste** schmal ist.</span><span class="sxs-lookup"><span data-stu-id="cbda5-181">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="cbda5-183">Die **Gerätesymbolleiste**</span><span class="sxs-lookup"><span data-stu-id="cbda5-183">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="cbda5-184">Weitere Informationen finden Sie unter [Ausrichtung einstellen](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="cbda5-184">For more information, go to [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="cbda5-185">Geräterahmen anzeigen</span><span class="sxs-lookup"><span data-stu-id="cbda5-185">Show device frame</span></span>  

<span data-ttu-id="cbda5-186">Zeigen Sie den Frame des physikalischen Geräts um das Viewport an, wenn Sie die Abmessungen eines bestimmten mobilen Geräts wie einem iPhone 6 simulieren.</span><span class="sxs-lookup"><span data-stu-id="cbda5-186">Display the physical device frame around the viewport when you simulate the dimensions of a specific mobile device such as an iPhone 6.</span></span>  

1.  <span data-ttu-id="cbda5-187">Öffnen Sie **Weitere Optionen**.</span><span class="sxs-lookup"><span data-stu-id="cbda5-187">Open **More options**.</span></span>  
1.  <span data-ttu-id="cbda5-188">Wählen Sie **Geräterahmen anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-188">Choose **Show device frame**.</span></span>  

> [!NOTE]
> <span data-ttu-id="cbda5-189">Wenn ein Geräterahmen für ein bestimmtes Gerät nicht angezeigt wird, bedeutet dies, dass devtools keine Grafiken für diese Option besitzt.</span><span class="sxs-lookup"><span data-stu-id="cbda5-189">If you do not see a device frame for a particular device, it means that DevTools does not have art for that option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Geräterahmen anzeigen" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="cbda5-191">Geräterahmen anzeigen</span><span class="sxs-lookup"><span data-stu-id="cbda5-191">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Der Geräterahmen für das iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="cbda5-193">Der Geräterahmen für das iPhone 6</span><span class="sxs-lookup"><span data-stu-id="cbda5-193">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="cbda5-194">Hinzufügen eines benutzerdefinierten mobilen Geräts</span><span class="sxs-lookup"><span data-stu-id="cbda5-194">Add a custom mobile device</span></span>  

<span data-ttu-id="cbda5-195">Wenn die von Ihnen benötigte Option für das Mobile Gerät nicht in der Standardliste enthalten ist, können Sie ein benutzerdefiniertes Gerät hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cbda5-195">If the mobile device option that you need is not included on the default list, you may add a custom device.</span></span>  <span data-ttu-id="cbda5-196">Führen Sie die folgenden Schritte aus, um ein benutzerdefiniertes Gerät hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cbda5-196">To add a custom device, complete the following steps.</span></span>  

1.  <span data-ttu-id="cbda5-197">Wählen Sie die **Geräte** Liste > **Bearbeiten**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-197">Choose the **Device** list > **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Wählen Sie bearbeiten aus." lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="cbda5-199">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-199">Select **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cbda5-200">Wählen Sie **Benutzerdefiniertes Gerät hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-200">Choose **Add custom device**.</span></span>  
1.  <span data-ttu-id="cbda5-201">Geben Sie auf **emulierten Geräten**einen Gerätenamen, eine Bildschirmbreite und eine Bildschirmhöhe für das benutzerdefinierte Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="cbda5-201">On **Emulated Devices**, enter a device name, screen width, and screen height for the custom device.</span></span>  <span data-ttu-id="cbda5-202">Die Felder für das [Pixel Verhältnis des Geräts][MDNWindowDevicePixelRatio], die [Zeichenfolge des Benutzer-Agents][MDNUserAgent]und die [Gerätetypen](#set-the-device-type) sind optional.</span><span class="sxs-lookup"><span data-stu-id="cbda5-202">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="cbda5-203">Das Feld "Gerätetyp" ist standardmäßig auf " **Mobil**" eingestellt.</span><span class="sxs-lookup"><span data-stu-id="cbda5-203">The device type field defaults to **Mobile**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Erstellen eines benutzerdefinierten Geräts" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="cbda5-205">Erstellen eines benutzerdefinierten Geräts</span><span class="sxs-lookup"><span data-stu-id="cbda5-205">Create a custom device</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="cbda5-206">Lineale anzeigen</span><span class="sxs-lookup"><span data-stu-id="cbda5-206">Show rulers</span></span>  

<span data-ttu-id="cbda5-207">Wenn Sie Bildschirmdimensionen messen müssen, können Sie die Bildschirmgröße in Pixeln mithilfe von Linealen messen.</span><span class="sxs-lookup"><span data-stu-id="cbda5-207">If you need to measure screen dimensions, you may use rulers to measure the screen size in pixels.</span></span>  <span data-ttu-id="cbda5-208">Wählen Sie **Weitere Optionen**  >  **Lineale anzeigen** aus, um die Lineale oberhalb und Links des Viewports anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cbda5-208">Choose **More options** > **Show rulers** to display rulers above and to the left of your viewport.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Menüelement zum Anzeigen von Linealen" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         <span data-ttu-id="cbda5-210">Menüelement zum Anzeigen von Linealen</span><span class="sxs-lookup"><span data-stu-id="cbda5-210">Menu item to display rulers</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Lineale oberhalb und Links des Viewports" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="cbda5-212">Lineale oberhalb und Links des Viewports</span><span class="sxs-lookup"><span data-stu-id="cbda5-212">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="cbda5-213">Zoomen des Viewports</span><span class="sxs-lookup"><span data-stu-id="cbda5-213">Zoom the viewport</span></span>  

<span data-ttu-id="cbda5-214">Wenn Sie das Aussehen und Verhalten Ihrer Seite mit mehreren Zoomstufen testen möchten, verwenden Sie die **zoomliste** , um die Ansicht zu vergrößern oder zu verkleinern.</span><span class="sxs-lookup"><span data-stu-id="cbda5-214">To test the look and feel of your page at multiple zoom levels, use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="cbda5-216">Zoom</span><span class="sxs-lookup"><span data-stu-id="cbda5-216">Zoom</span></span>**  
:::image-end:::  

## <span data-ttu-id="cbda5-217">Netzwerk und CPU drosseln</span><span class="sxs-lookup"><span data-stu-id="cbda5-217">Throttle the network and CPU</span></span>  

<span data-ttu-id="cbda5-218">Mobile Geräte verfügen häufig über Netzwerk-und CPU-Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="cbda5-218">Mobile devices often have network and CPU constraints.</span></span>  <span data-ttu-id="cbda5-219">Stellen Sie sicher, dass Sie testen, wie schnell Ihre Seite geladen wird und wie Sie mit unterschiedlichen Internet-und CPU-Geschwindigkeiten reagiert.</span><span class="sxs-lookup"><span data-stu-id="cbda5-219">Ensure you test how quickly your page loads and how it responds at different internet and CPU speeds.</span></span>  

<span data-ttu-id="cbda5-220">Drosseln Sie das Netzwerk und die CPU.</span><span class="sxs-lookup"><span data-stu-id="cbda5-220">Throttle the network and CPU.</span></span>  

1.  <span data-ttu-id="cbda5-221">Wählen Sie **Drosselungs** Liste aus, und ändern Sie die voreingestellten auf **Mid-Tier-Handy** oder **Low-End-Mobiltelefon**.</span><span class="sxs-lookup"><span data-stu-id="cbda5-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span></span>  
    *   <span data-ttu-id="cbda5-222">**Mid-Tier-Handy** simuliert `fast 3G` und drosselt Ihre CPU.</span><span class="sxs-lookup"><span data-stu-id="cbda5-222">**Mid-tier mobile** simulates `fast 3G` and throttles your CPU.</span></span>  <span data-ttu-id="cbda5-223">Sie ist viermal langsamer als normal.</span><span class="sxs-lookup"><span data-stu-id="cbda5-223">It is four times slower than normal.</span></span>  
    *   <span data-ttu-id="cbda5-224">**Low-End Mobile** simuliert `slow 3G` und drosselt Ihre CPU.</span><span class="sxs-lookup"><span data-stu-id="cbda5-224">**Low-end mobile** simulates `slow 3G` and throttles your CPU.</span></span>  <span data-ttu-id="cbda5-225">Sie ist sechsmal langsamer als normal.</span><span class="sxs-lookup"><span data-stu-id="cbda5-225">It is six times slower than normal.</span></span>  
    
<span data-ttu-id="cbda5-226">Die gesamte Drosselung basiert auf der normalen Funktion Ihres Laptops oder Desktops.</span><span class="sxs-lookup"><span data-stu-id="cbda5-226">All of the throttling is based upon the normal capability of your laptop or desktop.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Die Drosselungs Liste auf der Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="cbda5-228">Die **Drosselungs** Liste auf der Gerätesymbolleiste</span><span class="sxs-lookup"><span data-stu-id="cbda5-228">The **Throttle** list in the Device Toolbar</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="cbda5-229">Wenn die **Drosselungs Liste** ausgeblendet ist, ist die **Gerätesymbolleiste** zu schmal.</span><span class="sxs-lookup"><span data-stu-id="cbda5-229">If the **Throttle list** is hidden, your **Device Toolbar** is too narrow.</span></span>  <span data-ttu-id="cbda5-230">Um auf die **Drosselungs Liste**zuzugreifen, vergrößern Sie die Breite der **Gerätesymbolleiste**.</span><span class="sxs-lookup"><span data-stu-id="cbda5-230">To access the **Throttle list**, increase the width of the **Device Toolbar**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="cbda5-232">Die **Gerätesymbolleiste**</span><span class="sxs-lookup"><span data-stu-id="cbda5-232">The **Device Toolbar**</span></span>  
:::image-end:::  

### <span data-ttu-id="cbda5-233">Nur die CPU drosseln</span><span class="sxs-lookup"><span data-stu-id="cbda5-233">Throttle the CPU only</span></span>  

<span data-ttu-id="cbda5-234">Führen Sie die folgenden Schritte aus, um nur die CPU und nicht das Netzwerk zu drosseln.</span><span class="sxs-lookup"><span data-stu-id="cbda5-234">To throttle the CPU only and not the network, complete the following steps.</span></span>

1.  <span data-ttu-id="cbda5-235">Wählen Sie das Panel **Leistung** aus, und wählen Sie **Aufnahmeeinstellungen** \ ( ![ Aufnahmeeinstellungen ][ImageCaptureIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-235">Choose the **Performance** panel, and choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>
1.  <span data-ttu-id="cbda5-236">Wählen Sie **CPU**  >  **4X Verlangsamung** oder **6x Verlangsamung**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-236">Choose **CPU** > **4x slowdown** or **6x slowdown**.</span></span>
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Die CPU-Liste im Leistungs Panel" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       <span data-ttu-id="cbda5-238">Die **CPU** -Liste im **Leistungs** Panel</span><span class="sxs-lookup"><span data-stu-id="cbda5-238">The **CPU** list in the **Performance** panel</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="cbda5-239">Nur das Netzwerk drosseln</span><span class="sxs-lookup"><span data-stu-id="cbda5-239">Throttle the network only</span></span>  

<span data-ttu-id="cbda5-240">Führen Sie die folgenden Schritte aus, um nur das Netzwerk zu drosseln:</span><span class="sxs-lookup"><span data-stu-id="cbda5-240">To throttle the network only, complete the following steps.</span></span>

1.  <span data-ttu-id="cbda5-241">Wählen Sie das **Netzwerk** Panel aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-241">Choose the **Network** panel.</span></span>
1.  <span data-ttu-id="cbda5-242">Wählen Sie **Online**  >  **fast 3G** oder **Slow 3G**.</span><span class="sxs-lookup"><span data-stu-id="cbda5-242">Choose **Online** > **Fast 3G** or **Slow 3G**.</span></span>
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Die Drosselungs Liste im Netzwerk Panel" lightbox="../media/device-mode-network-throttle.msft.png":::
       <span data-ttu-id="cbda5-244">Die **Drosselungs** Liste im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="cbda5-244">The **Throttle** list in the Network panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="cbda5-245">Oder wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das **Befehlsmenü**zu öffnen, geben Sie ein `3G` , und wählen Sie **fast 3G-Drosselung aktivieren** oder **langsame 3G-Drosselung aktivieren**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-245">Or select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and choose **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       <span data-ttu-id="cbda5-247">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="cbda5-247">The **Command Menu**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="cbda5-248">Sie können die Netzwerk Drosselung auch über das **Leistungs** Panel einstellen.</span><span class="sxs-lookup"><span data-stu-id="cbda5-248">You may also set network throttling from the **Performance** panel.</span></span>  

1.  <span data-ttu-id="cbda5-249">Wählen Sie **aufnahmeeinstellungen** \ ( ![ Aufnahme ][ImageCaptureIcon] Einstellungen \) aus, und wählen Sie die **Netzwerk** Liste aus, und ändern Sie die Voreinstellung auf **fast 3G** oder **Slow 3G**.</span><span class="sxs-lookup"><span data-stu-id="cbda5-249">Choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and choose the **Network** list and change the preset to **Fast 3G** or **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Einrichten der Netzwerk Drosselung im Leistungs Panel" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       <span data-ttu-id="cbda5-251">Einrichten der Netzwerk Drosselung im **Leistungs** Panel</span><span class="sxs-lookup"><span data-stu-id="cbda5-251">Set network throttling from the **Performance** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="cbda5-252">Überschreiben von Geolocation</span><span class="sxs-lookup"><span data-stu-id="cbda5-252">Override geolocation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cbda5-253">Wenn Ihre Seite von Geolocation-Informationen eines mobilen Geräts abhängt, um Sie ordnungsgemäß zu rendern, stellen Sie unterschiedliche geolokationen mithilfe der Benutzeroberfläche Überschreiben von Geolocation bereit.</span><span class="sxs-lookup"><span data-stu-id="cbda5-253">If your page depends on geolocation information from a mobile device to render properly, provide different geolocations using the geolocation overriding UI.</span></span>  

      1.  <span data-ttu-id="cbda5-254">Wählen Sie **anpassen und Steuern devtools** \ ( `...` \) > **Weitere Tools**-  >  **Sensoren**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-254">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensoren für geolocation" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="cbda5-256">**Sensoren** für geolocation</span><span class="sxs-lookup"><span data-stu-id="cbda5-256">**Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="cbda5-257">Öffnen des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="cbda5-257">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="cbda5-258">Wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-258">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="cbda5-259">Geben `Sensors` Sie ein, und wählen Sie **Sensoren anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-259">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Sensoren für Geolocation anzeigen" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="cbda5-261">**Sensoren** für Geolocation anzeigen</span><span class="sxs-lookup"><span data-stu-id="cbda5-261">**Show Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="cbda5-262">Im Bereich " **Sensoren** " können Sie mithilfe des Dropdownmenüs " **Standort** " einen der vordefinierten Speicherorte auswählen, die in devtools enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cbda5-262">On the **Sensors** panel, you may select one of the preset locations included in DevTools using the **Location** drop-down menu.</span></span>  <span data-ttu-id="cbda5-263">Wenn Sie einen benutzerdefinierten Speicherort eingeben möchten, wählen Sie **andere** aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-263">To enter a custom location, choose **Other…**</span></span> <span data-ttu-id="cbda5-264">und geben Sie die Koordinaten des benutzerdefinierten Speicherorts ein.</span><span class="sxs-lookup"><span data-stu-id="cbda5-264">and enter the coordinates of your custom location.</span></span>  <span data-ttu-id="cbda5-265">Wenn Sie Ihre Seite in einem Fehlerzustand testen möchten, wenn Standortinformationen nicht verfügbar sind, wählen Sie **Speicherort nicht verfügbar**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-265">To test your page in an error state when location information is unavailable, choose **Location unavailable**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Sensorbereich mit ausgewähltem voreingestellten Speicherort" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    <span data-ttu-id="cbda5-267">Bereich " **Sensoren** " mit ausgewählter Vorwahl Position.</span><span class="sxs-lookup"><span data-stu-id="cbda5-267">**Sensors** panel with a preset location selected.</span></span>  
:::image-end:::

## <span data-ttu-id="cbda5-268">Ausrichtung einstellen</span><span class="sxs-lookup"><span data-stu-id="cbda5-268">Set orientation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cbda5-269">Wenn Ihre Seite von den Orientierungs Informationen eines mobilen Geräts abhängt, um Sie ordnungsgemäß zu rendern, öffnen Sie die Benutzeroberfläche für die Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="cbda5-269">If your page depends on orientation information from a mobile device to render properly, open the orientation UI.</span></span>  

      1.  <span data-ttu-id="cbda5-270">Wählen Sie **anpassen und Steuern devtools** \ ( `...` \) > **Weitere Tools**-  >  **Sensoren**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-270">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensoren zur Ausrichtung" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="cbda5-272">**Sensoren** zur Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="cbda5-272">**Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="cbda5-273">Öffnen des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="cbda5-273">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="cbda5-274">Wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-274">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="cbda5-275">Geben `Sensors` Sie ein, und wählen Sie **Sensoren anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-275">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Anzeigen von Sensoren zur Ausrichtung" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="cbda5-277">**Anzeigen von Sensoren** zur Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="cbda5-277">**Show Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="cbda5-278">Im **Sensor** Panel können Sie eine voreingestellte Ausrichtung aus dem Dropdownmenü **Ausrichtung** auswählen.</span><span class="sxs-lookup"><span data-stu-id="cbda5-278">On the **Sensors** panel, you may select a preset orientation from the **Orientation** drop-down menu.</span></span>  <span data-ttu-id="cbda5-279">Wenn Sie eine eigene Ausrichtung eingeben möchten, wählen Sie **benutzerdefinierte Ausrichtung**aus, und geben Sie Ihre eigenen [Alpha][MDNDeviceOrientaitonAlpha]-, [Beta][MDNDeviceOrientaitonBeta]-und [Gammawerte][MDNDeviceOrientaitonGamma] ein.</span><span class="sxs-lookup"><span data-stu-id="cbda5-279">To enter your own orientation, choose **Custom orientation**, and enter your own [alpha][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta], and [gamma][MDNDeviceOrientaitonGamma] values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Ausrichtungsoptionen im Sensor Panel" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    <span data-ttu-id="cbda5-281">**Ausrichtungs** Optionen im **Sensor** Panel</span><span class="sxs-lookup"><span data-stu-id="cbda5-281">**Orientation** options on the **Sensors** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="cbda5-282">Benutzer-Agent-Zeichenfolge einrichten</span><span class="sxs-lookup"><span data-stu-id="cbda5-282">Set user agent string</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cbda5-283">Wenn Ihre Seite davon abhängt, ob die Benutzer-Agent-Zeichenfolge von einem mobilen Gerät ordnungsgemäß gerendert wird, verwenden Sie den Panel **Netzwerkbedingungen** , um unterschiedliche Benutzer-Agent-Zeichenfolgen bereitzustellen</span><span class="sxs-lookup"><span data-stu-id="cbda5-283">If your page depends on the user agent string from a mobile device to render properly, use the **Network conditions** panel to provide different user agent strings.</span></span>  
      
      1.  <span data-ttu-id="cbda5-284">Wählen Sie **anpassen und Steuern devtools** \ ( `...` \) > **Weitere Tools**  >  **Netzwerkbedingungen**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-284">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Eintrag "Netzwerkbedingungen" im Menü "Weitere Tools"" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         <span data-ttu-id="cbda5-286">Eintrag " **Netzwerkbedingungen** " im Menü " **Weitere Tools** "</span><span class="sxs-lookup"><span data-stu-id="cbda5-286">**Network conditions** entry in the **More tools** menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="cbda5-287">Öffnen des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="cbda5-287">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="cbda5-288">Wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-288">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="cbda5-289">Geben `Network conditions` Sie ein, und wählen Sie **Netzwerkbedingungen anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="cbda5-289">Type `Network conditions`, and choose **Show Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Netzwerkbedingungen anzeigen" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **<span data-ttu-id="cbda5-291">Netzwerkbedingungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="cbda5-291">Show Network conditions</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="cbda5-292">Deaktivieren Sie neben **Benutzer-Agent**das Kontrollkästchen **automatisch auswählen** .</span><span class="sxs-lookup"><span data-stu-id="cbda5-292">Next to **User agent**, clear the **Select automatically** checkbox.</span></span>  <span data-ttu-id="cbda5-293">Wählen Sie dann **Benutzerdefiniert** aus, um aus einer Liste vordefinierter Benutzer-Agent-Zeichenfolgen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="cbda5-293">Then, select **Custom...** to select from a list of predefined user agent strings.</span></span>  <span data-ttu-id="cbda5-294">Wenn Sie eine eigene Benutzer-Agent-Zeichenfolge eingeben möchten, geben Sie die Zeichenfolge in **Geben Sie einen benutzerdefinierten Benutzer-Agent ein**.</span><span class="sxs-lookup"><span data-stu-id="cbda5-294">To enter your own user agent string, enter the string in **Enter a custom user agent**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Einrichten der Benutzer-Agent-Zeichenfolge auf Microsoft Edge unter macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    <span data-ttu-id="cbda5-296">Einrichten der Benutzer-Agent-Zeichenfolge auf Microsoft Edge unter macOS</span><span class="sxs-lookup"><span data-stu-id="cbda5-296">Set the user agent string to Microsoft Edge on macOS</span></span>  
:::image-end:::  

## <span data-ttu-id="cbda5-297">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="cbda5-297">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/Index.MD "erste Schritte mit dem Remotedebuggen von Android-Geräten | Microsoft docs "  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Benutzer-Agent | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent. Alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent. Beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent. Gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Reihenfolge der Näherung – First-Order – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="cbda5-305">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cbda5-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cbda5-306">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="cbda5-306">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="cbda5-308">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cbda5-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
description: Verwenden Sie virtuelle Geräte in Microsoft Edge, um Mobile-First-Websites zu erstellen.
title: Emulieren mobiler Geräte in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, emulation, device, simulation, mobile
ms.openlocfilehash: 1a83dece95acba386385bfea035a9e2c91639240
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398784"
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

# <a name="emulate-mobile-devices-in-microsoft-edge-devtools"></a><span data-ttu-id="96c51-104">Emulieren mobiler Geräte in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="96c51-104">Emulate mobile devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="96c51-105">Verwenden **Sie die Geräteemulation,** um das Aussehen und Reagieren Ihrer Seite auf einem mobilen Gerät zu erahnen.</span><span class="sxs-lookup"><span data-stu-id="96c51-105">Use **Device emulation** to approximate how your page looks and responds on a mobile device.</span></span>  <span data-ttu-id="96c51-106">Die Microsoft Edge DevTools bieten eine Sammlung von Features, mit deren Hilfe Sie mobile Geräte emulieren können.</span><span class="sxs-lookup"><span data-stu-id="96c51-106">The Microsoft Edge DevTools provide a collection of features to help you emulate mobile devices.</span></span>  <span data-ttu-id="96c51-107">Die Auflistung enthält die folgenden Features.</span><span class="sxs-lookup"><span data-stu-id="96c51-107">The collection includes the following features.</span></span>  

*   [<span data-ttu-id="96c51-108">Simulieren eines mobilen Viewports</span><span class="sxs-lookup"><span data-stu-id="96c51-108">Simulate a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="96c51-109">Drosseln des Netzwerks</span><span class="sxs-lookup"><span data-stu-id="96c51-109">Throttle the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="96c51-110">Drosseln der CPU</span><span class="sxs-lookup"><span data-stu-id="96c51-110">Throttle the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="96c51-111">Simulieren von Geolocation</span><span class="sxs-lookup"><span data-stu-id="96c51-111">Simulate geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="96c51-112">Festlegen der Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="96c51-112">Set orientation</span></span>](#set-orientation)  
*   [<span data-ttu-id="96c51-113">Festlegen der Benutzer-Agent-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="96c51-113">Set the user agent string</span></span>](#set-user-agent-string)  

## <a name="limitations"></a><span data-ttu-id="96c51-114">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="96c51-114">Limitations</span></span>  

<span data-ttu-id="96c51-115">**Bei der Geräteemulation** [handelt][WikiApproximation] es sich um eine Näherung des Aussehens und Fühlungsgefühls Ihrer Seite auf einem mobilen Gerät in erster Ordnung.</span><span class="sxs-lookup"><span data-stu-id="96c51-115">**Device emulation** is a [first-order approximation][WikiApproximation] of the look and feel of your page on a mobile device.</span></span>  <span data-ttu-id="96c51-116">**Bei der Geräteemulation** wird Der Code nicht tatsächlich auf einem mobilen Gerät ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96c51-116">**Device emulation** does not actually run your code on a mobile device.</span></span>  <span data-ttu-id="96c51-117">Stattdessen simulieren Sie die mobile Benutzeroberfläche von Ihrem Laptop oder Desktop aus.</span><span class="sxs-lookup"><span data-stu-id="96c51-117">Instead you simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="96c51-118">Einige Aspekte mobiler Geräte werden in DevTools nie emuliert.</span><span class="sxs-lookup"><span data-stu-id="96c51-118">Some aspects of mobile devices are never emulated in DevTools.</span></span>  <span data-ttu-id="96c51-119">Beispielsweise ist die Architektur mobiler CPUs anders als die Architektur von Laptop- oder Desktop-CPUs.</span><span class="sxs-lookup"><span data-stu-id="96c51-119">For example, the architecture of mobile CPUs is different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="96c51-120">Im Zweifelsfall sollten Sie Ihre Seite am besten auf einem mobilen Gerät ausführen.</span><span class="sxs-lookup"><span data-stu-id="96c51-120">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="96c51-121">Verwenden Sie [Remotedebugging][DevToolsRemoteDebugging] zum Interagieren mit dem Code einer Seite von Ihrem Computer, während Ihre Seite tatsächlich auf einem mobilen Gerät ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96c51-121">Use [Remote Debugging][DevToolsRemoteDebugging] to interact with the code of a page from your machine while your page actually runs on a mobile device.</span></span>  <span data-ttu-id="96c51-122">Sie können alle vier anzeigen, ändern, debuggen, profilieren oder alle vier anzeigen, während Sie mit dem Code interagieren.</span><span class="sxs-lookup"><span data-stu-id="96c51-122">You may view, change, debug, profile, or all four while you interact with the code.</span></span>  <span data-ttu-id="96c51-123">Ihr Computer kann ein Notizbuch oder ein Desktopcomputer sein.</span><span class="sxs-lookup"><span data-stu-id="96c51-123">Your machine may be a notebook or desktop computer.</span></span>  

## <a name="simulate-a-mobile-viewport"></a><span data-ttu-id="96c51-124">Simulieren eines mobilen Viewports</span><span class="sxs-lookup"><span data-stu-id="96c51-124">Simulate a mobile viewport</span></span>  

<span data-ttu-id="96c51-125">Wählen **Sie Geräteemulation** umschalten \( ![ Gerätesymbolleiste ][ImageDeviceToolbarIcon] umschalten \) oder **DevTools** anpassen und steuern \( `...` \) > Geräteemulation, \*\*\*\* um die Benutzeroberfläche zu öffnen, mit der Sie einen mobilen Ansichtsfenster simulieren können.</span><span class="sxs-lookup"><span data-stu-id="96c51-125">Choose **Toggle device emulation**  \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) or choose **Customize and control DevTools** \(`...`\) > **Device emulation** to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    <span data-ttu-id="96c51-127">Die Gerätesymbolleiste</span><span class="sxs-lookup"><span data-stu-id="96c51-127">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="96c51-128">Standardmäßig wird die Gerätesymbolleiste im Modus "Responsive Viewport" geöffnet.</span><span class="sxs-lookup"><span data-stu-id="96c51-128">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <a name="responsive-viewport-mode"></a><span data-ttu-id="96c51-129">Responsive Viewport Mode</span><span class="sxs-lookup"><span data-stu-id="96c51-129">Responsive Viewport Mode</span></span>  

<span data-ttu-id="96c51-130">Ziehen Sie die Ziehpunkte, um das Aussehen und Aussehen Ihrer Seite in mehreren Bildschirmgrößen schnell zu testen, um die Größe des Ansichtsfensters auf die erforderlichen Dimensionen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="96c51-130">To quickly test the look and feel of your page across multiple screen sizes, drag the handles to resize the viewport to your required dimensions.</span></span>  <span data-ttu-id="96c51-131">Sie können auch bestimmte Werte in die Felder Breite und Höhe eingeben.</span><span class="sxs-lookup"><span data-stu-id="96c51-131">You may also enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="96c51-132">In der folgenden Abbildung wird die Breite auf und `626` die Höhe auf `516` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="96c51-132">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Die Ziehpunkte zum Ändern der Dimensionen des Ansichtsfensters im Modus "Responsive Viewport"" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    <span data-ttu-id="96c51-134">Die Ziehpunkte zum Ändern der Dimensionen des Ansichtsfensters im Modus "Responsive Viewport"</span><span class="sxs-lookup"><span data-stu-id="96c51-134">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <a name="show-media-queries"></a><span data-ttu-id="96c51-135">Anzeigen von Medienabfragen</span><span class="sxs-lookup"><span data-stu-id="96c51-135">Show media queries</span></span>  

<span data-ttu-id="96c51-136">Wenn Sie Medienabfragen auf Ihrer Seite definiert haben, springen Sie zu den Viewportdimensionen, in denen diese Medienabfragen wirksam werden, indem Sie Haltepunkte für Medienabfragen über Dem Viewport anzeigen.</span><span class="sxs-lookup"><span data-stu-id="96c51-136">If you have defined media queries on your page, jump to the viewport dimensions where those media queries take effect by showing media query breakpoints above your viewport.</span></span>  <span data-ttu-id="96c51-137">Wählen **Sie Weitere Optionen**  >  **Medienabfragen anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-137">Choose **More options** > **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Anzeigen von Medienabfragen" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="96c51-139">Anzeigen von Medienabfragen</span><span class="sxs-lookup"><span data-stu-id="96c51-139">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="96c51-140">Wählen Sie einen Haltepunkt aus, um die Breite des Viewports so zu ändern, dass die Medienabfrage ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="96c51-140">Choose a breakpoint to change the width of the viewport so that the media query gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Wählen Sie einen Haltepunkt aus, um die Breite des Ansichtsfensters zu ändern." lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="96c51-142">Wählen Sie einen Haltepunkt aus, um die Breite des Ansichtsfensters zu ändern.</span><span class="sxs-lookup"><span data-stu-id="96c51-142">Choose a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <a name="set-the-device-type"></a><span data-ttu-id="96c51-143">Festlegen des Gerätetyps</span><span class="sxs-lookup"><span data-stu-id="96c51-143">Set the device type</span></span>  

<span data-ttu-id="96c51-144">Verwenden Sie die **Liste Gerätetyp,** um ein mobiles Gerät oder Desktopgerät zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="96c51-144">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Die Liste "Gerätetyp"" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="96c51-146">Die **Liste "Gerätetyp"**</span><span class="sxs-lookup"><span data-stu-id="96c51-146">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="96c51-147">In der folgenden Tabelle werden die Unterschiede zwischen den verfügbaren Gerätetypoptionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="96c51-147">The following table describes the differences between the available device type options.</span></span>  <span data-ttu-id="96c51-148">Die Spalte Rendering-Methode bezieht sich darauf, ob Microsoft Edge die Seite als Mobile- oder Desktop-Viewport rendert.</span><span class="sxs-lookup"><span data-stu-id="96c51-148">The Rendering method column refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="96c51-149">Die Spalte Cursorsymbol bezieht sich auf den Cursortyp, der angezeigt wird, wenn Sie auf die Seite zeigen.</span><span class="sxs-lookup"><span data-stu-id="96c51-149">The Cursor icon column refers to what type of cursor is displayed when you hover on the page.</span></span>  <span data-ttu-id="96c51-150">Die Spalte Ereignisse, die ausgelöst wird, bezieht sich darauf, ob die Seite ausgelöst wird oder ob Ereignisse ausgelöst `touch` `click` werden, wenn Sie mit der Seite interagieren.</span><span class="sxs-lookup"><span data-stu-id="96c51-150">The Events triggered column refers to whether the page triggers `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="96c51-151">Option</span><span class="sxs-lookup"><span data-stu-id="96c51-151">Option</span></span> | <span data-ttu-id="96c51-152">Renderingmethode</span><span class="sxs-lookup"><span data-stu-id="96c51-152">Rendering method</span></span> | <span data-ttu-id="96c51-153">Cursorsymbol</span><span class="sxs-lookup"><span data-stu-id="96c51-153">Cursor icon</span></span> | <span data-ttu-id="96c51-154">Ausgelöste Ereignisse</span><span class="sxs-lookup"><span data-stu-id="96c51-154">Events triggered</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="96c51-155">Mobilgeräte</span><span class="sxs-lookup"><span data-stu-id="96c51-155">Mobile</span></span> | <span data-ttu-id="96c51-156">Mobilgeräte</span><span class="sxs-lookup"><span data-stu-id="96c51-156">Mobile</span></span> | <span data-ttu-id="96c51-157">Kreis</span><span class="sxs-lookup"><span data-stu-id="96c51-157">Circle</span></span> | <span data-ttu-id="96c51-158">Toucheingabe</span><span class="sxs-lookup"><span data-stu-id="96c51-158">touch</span></span> |  
| <span data-ttu-id="96c51-159">Mobil \(keine Berührung\)</span><span class="sxs-lookup"><span data-stu-id="96c51-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="96c51-160">Mobilgeräte</span><span class="sxs-lookup"><span data-stu-id="96c51-160">Mobile</span></span> | <span data-ttu-id="96c51-161">Normal</span><span class="sxs-lookup"><span data-stu-id="96c51-161">Normal</span></span> | <span data-ttu-id="96c51-162"> wählen Sie </span><span class="sxs-lookup"><span data-stu-id="96c51-162">choose</span></span> |  
| <span data-ttu-id="96c51-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="96c51-163">Desktop</span></span> | <span data-ttu-id="96c51-164">Desktop</span><span class="sxs-lookup"><span data-stu-id="96c51-164">Desktop</span></span> | <span data-ttu-id="96c51-165">Normal</span><span class="sxs-lookup"><span data-stu-id="96c51-165">Normal</span></span> | <span data-ttu-id="96c51-166"> wählen Sie </span><span class="sxs-lookup"><span data-stu-id="96c51-166">choose</span></span> |  
| <span data-ttu-id="96c51-167">Desktop \(touch\)</span><span class="sxs-lookup"><span data-stu-id="96c51-167">Desktop \(touch\)</span></span> | <span data-ttu-id="96c51-168">Desktop</span><span class="sxs-lookup"><span data-stu-id="96c51-168">Desktop</span></span> | <span data-ttu-id="96c51-169">Kreis</span><span class="sxs-lookup"><span data-stu-id="96c51-169">Circle</span></span> | <span data-ttu-id="96c51-170">Toucheingabe</span><span class="sxs-lookup"><span data-stu-id="96c51-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="96c51-171">Wenn die **Liste Gerätetyp** nicht angezeigt wird, wählen Sie **Weitere Optionen**  >  **Gerätetyp hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-171">If the **Device Type** list is not displayed, choose **More options** > **Add device type**.</span></span>  

### <a name="mobile-device-viewport-mode"></a><span data-ttu-id="96c51-172">Ansichtsportmodus für mobile Geräte</span><span class="sxs-lookup"><span data-stu-id="96c51-172">Mobile Device Viewport Mode</span></span>  

<span data-ttu-id="96c51-173">Um die Abmessungen eines bestimmten mobilen Geräts zu simulieren, wählen Sie das Gerät in der Liste **Gerät** aus.</span><span class="sxs-lookup"><span data-stu-id="96c51-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Die Geräteliste" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="96c51-175">Die **Geräteliste**</span><span class="sxs-lookup"><span data-stu-id="96c51-175">The **Device** list</span></span>  
:::image-end:::  

#### <a name="rotate-the-viewport-to-landscape-orientation"></a><span data-ttu-id="96c51-176">Drehen des Ansichtsfensters in die Querformatausrichtung</span><span class="sxs-lookup"><span data-stu-id="96c51-176">Rotate the viewport to landscape orientation</span></span>  

<span data-ttu-id="96c51-177">Testen Sie Ihre Webseite im Querformat.</span><span class="sxs-lookup"><span data-stu-id="96c51-177">Test your webpage in landscape orientation.</span></span>  

*   <span data-ttu-id="96c51-178">Um den Ansichtsfenster in die Querformatausrichtung zu drehen, wählen Sie **Drehen** \( ![ Drehen ][ImageRotateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="96c51-178">To rotate the viewport to landscape orientation, choose **Rotate** \(![Rotate][ImageRotateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Seite, die im Querformat angezeigt wird" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       <span data-ttu-id="96c51-180">Seite, die im Querformat angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="96c51-180">Page displayed in landscape orientation</span></span>  
    :::image-end:::  
    
> [!NOTE]
> <span data-ttu-id="96c51-181">Die **Schaltfläche Drehen** wird ausgeblendet, wenn die **Gerätesymbolleiste** schmal ist.</span><span class="sxs-lookup"><span data-stu-id="96c51-181">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="96c51-183">Die **Gerätesymbolleiste**</span><span class="sxs-lookup"><span data-stu-id="96c51-183">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="96c51-184">Weitere Informationen finden Sie unter Festlegen [der Ausrichtung](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="96c51-184">For more information, navigate to [Set orientation](#set-orientation).</span></span>  

#### <a name="show-device-frame"></a><span data-ttu-id="96c51-185">Anzeigen des Geräteframes</span><span class="sxs-lookup"><span data-stu-id="96c51-185">Show device frame</span></span>  

<span data-ttu-id="96c51-186">Zeigen Sie den physischen Geräterahmen um den Viewport an, wenn Sie die Abmessungen eines bestimmten mobilen Geräts, z. B. eines iPhone 6, simulieren.</span><span class="sxs-lookup"><span data-stu-id="96c51-186">Display the physical device frame around the viewport when you simulate the dimensions of a specific mobile device such as an iPhone 6.</span></span>  

1.  <span data-ttu-id="96c51-187">Öffnen **Sie Weitere Optionen**.</span><span class="sxs-lookup"><span data-stu-id="96c51-187">Open **More options**.</span></span>  
1.  <span data-ttu-id="96c51-188">Wählen **Sie Geräterahmen anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-188">Choose **Show device frame**.</span></span>  

> [!NOTE]
> <span data-ttu-id="96c51-189">Wenn ein Geräterahmen für ein bestimmtes Gerät nicht angezeigt wird, bedeutet dies, dass DevTools keine Art für die Option hat.</span><span class="sxs-lookup"><span data-stu-id="96c51-189">If a device frame for a particular device is not displayed, it means that DevTools does not have art for the option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Anzeigen des Geräteframes" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="96c51-191">Anzeigen des Geräteframes</span><span class="sxs-lookup"><span data-stu-id="96c51-191">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Der Geräterahmen für das iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="96c51-193">Der Geräterahmen für das iPhone 6</span><span class="sxs-lookup"><span data-stu-id="96c51-193">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="add-a-custom-mobile-device"></a><span data-ttu-id="96c51-194">Hinzufügen eines benutzerdefinierten mobilen Geräts</span><span class="sxs-lookup"><span data-stu-id="96c51-194">Add a custom mobile device</span></span>  

<span data-ttu-id="96c51-195">Wenn die option für mobile Geräte, die Sie benötigen, nicht in der Standardliste enthalten ist, können Sie ein benutzerdefiniertes Gerät hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="96c51-195">If the mobile device option that you need is not included on the default list, you may add a custom device.</span></span>  <span data-ttu-id="96c51-196">Führen Sie die folgenden Schritte aus, um ein benutzerdefiniertes Gerät hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="96c51-196">To add a custom device, complete the following steps.</span></span>  

1.  <span data-ttu-id="96c51-197">Wählen Sie **die Liste Gerät** > Bearbeiten **aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-197">Choose the **Device** list > **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Wählen Sie Bearbeiten aus" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="96c51-199">Wählen Sie **Bearbeiten aus**</span><span class="sxs-lookup"><span data-stu-id="96c51-199">Choose **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="96c51-200">Wählen **Sie Benutzerdefiniertes Gerät hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-200">Choose **Add custom device**.</span></span>  
1.  <span data-ttu-id="96c51-201">Geben **Sie unter Emulierte**Geräte den Gerätenamen, die Bildschirmbreite und die Bildschirmhöhe für das benutzerdefinierte Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="96c51-201">On **Emulated Devices**, enter a device name, screen width, and screen height for the custom device.</span></span>  <span data-ttu-id="96c51-202">Das [Gerätepixelverhältnis,][MDNWindowDevicePixelRatio] [die Benutzer-Agent-Zeichenfolge][MDNUserAgent]und [die Gerätetypfelder](#set-the-device-type) sind optional.</span><span class="sxs-lookup"><span data-stu-id="96c51-202">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="96c51-203">Das Gerätetypfeld ist standardmäßig **auf Mobile festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="96c51-203">The device type field defaults to **Mobile**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Erstellen eines benutzerdefinierten Geräts" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="96c51-205">Erstellen eines benutzerdefinierten Geräts</span><span class="sxs-lookup"><span data-stu-id="96c51-205">Create a custom device</span></span>  
    :::image-end:::  
    
### <a name="show-rulers"></a><span data-ttu-id="96c51-206">Anzeigen von Lineale</span><span class="sxs-lookup"><span data-stu-id="96c51-206">Show rulers</span></span>  

<span data-ttu-id="96c51-207">Wenn Sie Bildschirmmaße messen müssen, können Sie Lineale verwenden, um die Bildschirmgröße in Pixeln zu messen.</span><span class="sxs-lookup"><span data-stu-id="96c51-207">If you need to measure screen dimensions, you may use rulers to measure the screen size in pixels.</span></span>  <span data-ttu-id="96c51-208">Wählen **Sie Weitere Optionen**  >  **Lineale anzeigen** aus, um Lineale oben und links vom Viewport anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="96c51-208">Choose **More options** > **Show rulers** to display rulers above and to the left of your viewport.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Menüelement zum Anzeigen von Lineale" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         <span data-ttu-id="96c51-210">Menüelement zum Anzeigen von Lineale</span><span class="sxs-lookup"><span data-stu-id="96c51-210">Menu item to display rulers</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Lineale oberhalb und links vom Viewport" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="96c51-212">Lineale oberhalb und links vom Viewport</span><span class="sxs-lookup"><span data-stu-id="96c51-212">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="zoom-the-viewport"></a><span data-ttu-id="96c51-213">Zoomen des Viewports</span><span class="sxs-lookup"><span data-stu-id="96c51-213">Zoom the viewport</span></span>  

<span data-ttu-id="96c51-214">Verwenden Sie die Zoomliste zum Vergrößern oder Verkleinern, um das Aussehen und Das Gefühl Ihrer Seite auf mehreren Zoomstufen zu testen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="96c51-214">To test the look and feel of your page at multiple zoom levels, use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="96c51-216">Zoom</span><span class="sxs-lookup"><span data-stu-id="96c51-216">Zoom</span></span>**  
:::image-end:::  

## <a name="throttle-the-network-and-cpu"></a><span data-ttu-id="96c51-217">Drosseln des Netzwerks und der CPU</span><span class="sxs-lookup"><span data-stu-id="96c51-217">Throttle the network and CPU</span></span>  

<span data-ttu-id="96c51-218">Mobile Geräte haben häufig Netzwerk- und CPU-Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="96c51-218">Mobile devices often have network and CPU constraints.</span></span>  <span data-ttu-id="96c51-219">Stellen Sie sicher, dass Sie testen, wie schnell Ihre Seite geladen wird und wie sie mit unterschiedlichen Internet- und CPU-Geschwindigkeiten reagiert.</span><span class="sxs-lookup"><span data-stu-id="96c51-219">Ensure you test how quickly your page loads and how it responds at different internet and CPU speeds.</span></span>  

<span data-ttu-id="96c51-220">Drosseln Sie das Netzwerk und die CPU.</span><span class="sxs-lookup"><span data-stu-id="96c51-220">Throttle the network and CPU.</span></span>  

1.  <span data-ttu-id="96c51-221">Wählen **Sie Drosselungsliste** aus, und ändern Sie die Voreinstellung in **Mobile** Oder **Low-End Mobile der Mittleren Ebene.**</span><span class="sxs-lookup"><span data-stu-id="96c51-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span></span>  
    *   <span data-ttu-id="96c51-222">**Mid-Tier Mobile** simuliert `fast 3G` und drosselt Ihre CPU.</span><span class="sxs-lookup"><span data-stu-id="96c51-222">**Mid-tier mobile** simulates `fast 3G` and throttles your CPU.</span></span>  <span data-ttu-id="96c51-223">Er ist viermal langsamer als normal.</span><span class="sxs-lookup"><span data-stu-id="96c51-223">It is four times slower than normal.</span></span>  
    *   <span data-ttu-id="96c51-224">**Low-End Mobile** simuliert `slow 3G` und drosselt Ihre CPU.</span><span class="sxs-lookup"><span data-stu-id="96c51-224">**Low-end mobile** simulates `slow 3G` and throttles your CPU.</span></span>  <span data-ttu-id="96c51-225">Sie ist sechsmal langsamer als normal.</span><span class="sxs-lookup"><span data-stu-id="96c51-225">It is six times slower than normal.</span></span>  
    
<span data-ttu-id="96c51-226">Die Drosselung basiert auf der normalen Funktion Ihres Laptops oder Desktops.</span><span class="sxs-lookup"><span data-stu-id="96c51-226">All of the throttling is based upon the normal capability of your laptop or desktop.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Die Einschränkungsliste in der Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="96c51-228">Die **Einschränkungsliste** in der Gerätesymbolleiste</span><span class="sxs-lookup"><span data-stu-id="96c51-228">The **Throttle** list in the Device Toolbar</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="96c51-229">Wenn die **Einschränkungsliste** ausgeblendet ist, ist **die Gerätesymbolleiste** zu schmal.</span><span class="sxs-lookup"><span data-stu-id="96c51-229">If the **Throttle list** is hidden, your **Device Toolbar** is too narrow.</span></span>  <span data-ttu-id="96c51-230">Erhöhen Sie die Breite **der**Gerätesymbolleiste, um auf die Einschränkungsliste **zu zugreifen.**</span><span class="sxs-lookup"><span data-stu-id="96c51-230">To access the **Throttle list**, increase the width of the **Device Toolbar**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="96c51-232">Die **Gerätesymbolleiste**</span><span class="sxs-lookup"><span data-stu-id="96c51-232">The **Device Toolbar**</span></span>  
:::image-end:::  

### <a name="throttle-the-cpu-only"></a><span data-ttu-id="96c51-233">Nur die CPU drosseln</span><span class="sxs-lookup"><span data-stu-id="96c51-233">Throttle the CPU only</span></span>  

<span data-ttu-id="96c51-234">Führen Sie die folgenden Schritte aus, um nur die CPU und nicht das Netzwerk zu drosseln.</span><span class="sxs-lookup"><span data-stu-id="96c51-234">To throttle the CPU only and not the network, complete the following steps.</span></span>

1.  <span data-ttu-id="96c51-235">Wählen Sie **den Bereich** Leistung aus, und wählen Sie **Aufnahmeeinstellungen** \( ![ Aufnahmeeinstellungen ][ImageCaptureIcon] \).</span><span class="sxs-lookup"><span data-stu-id="96c51-235">Choose the **Performance** panel, and choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>
1.  <span data-ttu-id="96c51-236">Wählen **Sie CPU**  >  **4x Verlangsamung** oder **6x Verlangsamung aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-236">Choose **CPU** > **4x slowdown** or **6x slowdown**.</span></span>
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Die CPU-Liste im Leistungsbereich" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       <span data-ttu-id="96c51-238">Die **CPU-Liste** im **Leistungsbereich**</span><span class="sxs-lookup"><span data-stu-id="96c51-238">The **CPU** list in the **Performance** panel</span></span>  
    :::image-end:::  
    
### <a name="throttle-the-network-only"></a><span data-ttu-id="96c51-239">Drosseln des Netzwerks</span><span class="sxs-lookup"><span data-stu-id="96c51-239">Throttle the network only</span></span>  

<span data-ttu-id="96c51-240">Führen Sie die folgenden Schritte aus, um das Netzwerk zu drosseln.</span><span class="sxs-lookup"><span data-stu-id="96c51-240">To throttle the network only, complete the following steps.</span></span>

1.  <span data-ttu-id="96c51-241">Wählen Sie das **Netzwerktool** aus.</span><span class="sxs-lookup"><span data-stu-id="96c51-241">Choose the **Network** tool.</span></span>
1.  <span data-ttu-id="96c51-242">Wählen **Sie Online**Fast  >  **3G** oder Slow **3G**aus.</span><span class="sxs-lookup"><span data-stu-id="96c51-242">Choose **Online** > **Fast 3G** or **Slow 3G**.</span></span>
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Die Einschränkungsliste im Netzwerkbereich" lightbox="../media/device-mode-network-throttle.msft.png":::
       <span data-ttu-id="96c51-244">Die **Einschränkungsliste** im Netzwerkbereich</span><span class="sxs-lookup"><span data-stu-id="96c51-244">The **Throttle** list in the Network panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="96c51-245">Oder wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \*\*\*\* \(macOS\) `3G` \*\*\*\* \*\*\*\* aus, um das Befehlsmenü zu öffnen, geben Sie ein, und wählen Sie Schnelle 3G Drosselung aktivieren oder langsame 3G aktivieren aus.</span><span class="sxs-lookup"><span data-stu-id="96c51-245">Or select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and choose **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       <span data-ttu-id="96c51-247">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="96c51-247">The **Command Menu**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="96c51-248">Sie können die Netzwerkeinschränkung auch im Bereich **Leistung** festlegen.</span><span class="sxs-lookup"><span data-stu-id="96c51-248">You may also set network throttling from the **Performance** panel.</span></span>  

1.  <span data-ttu-id="96c51-249">Wählen **Sie Aufnahmeeinstellungen** \( ![ Aufnahmeeinstellungen ][ImageCaptureIcon] \) aus, \*\*\*\* \*\*\*\* und wählen Sie \*\*\*\* die Liste Netzwerk aus, und ändern Sie die Voreinstellung in Fast 3G oder Slow 3G .</span><span class="sxs-lookup"><span data-stu-id="96c51-249">Choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and choose the **Network** list and change the preset to **Fast 3G** or **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Festlegen der Netzwerkeinschränkung aus dem Leistungsbereich" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       <span data-ttu-id="96c51-251">Festlegen der Netzwerkeinschränkung aus dem **Leistungsbereich**</span><span class="sxs-lookup"><span data-stu-id="96c51-251">Set network throttling from the **Performance** panel</span></span>  
    :::image-end:::  
    
## <a name="override-geolocation"></a><span data-ttu-id="96c51-252">Außerkraftsetzung der Geolocation</span><span class="sxs-lookup"><span data-stu-id="96c51-252">Override geolocation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="96c51-253">Wenn Ihre Seite von Geolocationinformationen von einem mobilen Gerät abhängt, um ordnungsgemäß gerendert zu werden, stellen Sie unterschiedliche Geolocations mithilfe der geolocation-überschreibenden Benutzeroberfläche zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="96c51-253">If your page depends on geolocation information from a mobile device to render properly, provide different geolocations using the geolocation overriding UI.</span></span>  

      1.  <span data-ttu-id="96c51-254">Wählen **Sie Anpassen und Steuern devTools** \( `...` \) > Weitere Tools **Sensoren**  >  **aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-254">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensoren für Geolocation" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="96c51-256">**Sensoren** für Geolocation</span><span class="sxs-lookup"><span data-stu-id="96c51-256">**Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="96c51-257">Öffnen Sie das Befehlsmenü.</span><span class="sxs-lookup"><span data-stu-id="96c51-257">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="96c51-258">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="96c51-258">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="96c51-259">Geben `Sensors` Sie ein, und wählen **Sie Sensoren anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-259">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Anzeigen von Sensoren für geolocation" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="96c51-261">**Anzeigen von Sensoren** für geolocation</span><span class="sxs-lookup"><span data-stu-id="96c51-261">**Show Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="96c51-262">Im Bereich **Sensoren** können Sie einen der vordefinierten Speicherorte auswählen, die in DevTools enthalten sind, indem Sie das **Dropdownmenü** Speicherort verwenden.</span><span class="sxs-lookup"><span data-stu-id="96c51-262">On the **Sensors** panel, you may select one of the preset locations included in DevTools using the **Location** drop-down menu.</span></span>  <span data-ttu-id="96c51-263">Wenn Sie einen benutzerdefinierten Speicherort eingeben, wählen Sie **Andere...**</span><span class="sxs-lookup"><span data-stu-id="96c51-263">To enter a custom location, choose **Other…**</span></span> <span data-ttu-id="96c51-264">und geben Sie die Koordinaten Ihres benutzerdefinierten Speicherorts ein.</span><span class="sxs-lookup"><span data-stu-id="96c51-264">and enter the coordinates of your custom location.</span></span>  <span data-ttu-id="96c51-265">Wenn Sie Ihre Seite in einem Fehlerzustand testen möchten, wenn Standortinformationen nicht verfügbar sind, wählen Sie **Location unavailable aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-265">To test your page in an error state when location information is unavailable, choose **Location unavailable**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Sensorbereich mit ausgewählter voreingestellter Position" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    <span data-ttu-id="96c51-267">**Sensorbereich** mit ausgewählter voreingestellter Position.</span><span class="sxs-lookup"><span data-stu-id="96c51-267">**Sensors** panel with a preset location selected.</span></span>  
:::image-end:::

## <a name="set-orientation"></a><span data-ttu-id="96c51-268">Festlegen der Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="96c51-268">Set orientation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="96c51-269">Wenn Ihre Seite von Ausrichtungsinformationen eines mobilen Geräts abhängt, um ordnungsgemäß gerendert zu werden, öffnen Sie die Ausrichtungsbenutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="96c51-269">If your page depends on orientation information from a mobile device to render properly, open the orientation UI.</span></span>  

      1.  <span data-ttu-id="96c51-270">Wählen **Sie Anpassen und Steuern devTools** \( `...` \) > Weitere Tools **Sensoren**  >  **aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-270">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensoren für die Ausrichtung" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="96c51-272">**Sensoren für** die Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="96c51-272">**Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="96c51-273">Öffnen Sie das Befehlsmenü.</span><span class="sxs-lookup"><span data-stu-id="96c51-273">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="96c51-274">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="96c51-274">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="96c51-275">Geben `Sensors` Sie ein, und wählen **Sie Sensoren anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-275">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Anzeigen von Sensoren für die Ausrichtung" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="96c51-277">**Anzeigen von Sensoren** für die Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="96c51-277">**Show Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="96c51-278">Im **Bereich Sensoren** können Sie im Dropdownmenü Ausrichtung eine voreingestellte Ausrichtung auswählen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="96c51-278">On the **Sensors** panel, you may select a preset orientation from the **Orientation** drop-down menu.</span></span>  <span data-ttu-id="96c51-279">Wenn Sie Ihre eigene Ausrichtung eingeben, wählen Sie **Benutzerdefinierte**Ausrichtung aus, und geben Sie Ihre eigenen [Alpha-,][MDNDeviceOrientaitonAlpha] [Beta-][MDNDeviceOrientaitonBeta]und [Gammawerte][MDNDeviceOrientaitonGamma] ein.</span><span class="sxs-lookup"><span data-stu-id="96c51-279">To enter your own orientation, choose **Custom orientation**, and enter your own [alpha][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta], and [gamma][MDNDeviceOrientaitonGamma] values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Ausrichtungsoptionen im Bereich Sensoren" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    <span data-ttu-id="96c51-281">**Ausrichtungsoptionen** im **Bereich Sensoren**</span><span class="sxs-lookup"><span data-stu-id="96c51-281">**Orientation** options on the **Sensors** panel</span></span>  
:::image-end:::  

## <a name="set-user-agent-string"></a><span data-ttu-id="96c51-282">Festlegen der Zeichenfolge des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="96c51-282">Set user agent string</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="96c51-283">Wenn Ihre Seite von der Benutzer-Agent-Zeichenfolge eines mobilen Geräts abhängt, um ordnungsgemäß gerendert zu werden, verwenden Sie den Bereich Netzwerkbedingungen, um unterschiedliche Zeichenfolgen für den Benutzer-Agent zur Verfügung zu stellen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="96c51-283">If your page depends on the user agent string from a mobile device to render properly, use the **Network conditions** panel to provide different user agent strings.</span></span>  
      
      1.  <span data-ttu-id="96c51-284">Wählen **Sie Anpassen und Steuern devTools** \( `...` \) > Weitere **Tools**  >  **Netzwerkbedingungen aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-284">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Eintrag "Netzwerkbedingungen" im Menü Weitere Tools" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         <span data-ttu-id="96c51-286">**Eintrag "Netzwerkbedingungen"** im Menü **Weitere** Tools</span><span class="sxs-lookup"><span data-stu-id="96c51-286">**Network conditions** entry in the **More tools** menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="96c51-287">Öffnen Sie das Befehlsmenü.</span><span class="sxs-lookup"><span data-stu-id="96c51-287">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="96c51-288">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="96c51-288">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="96c51-289">Geben `Network conditions` Sie ein, und wählen **Sie Netzwerkbedingungen anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="96c51-289">Type `Network conditions`, and choose **Show Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Anzeigen von Netzwerkbedingungen" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **<span data-ttu-id="96c51-291">Anzeigen von Netzwerkbedingungen</span><span class="sxs-lookup"><span data-stu-id="96c51-291">Show Network conditions</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="96c51-292">Aktivieren Sie **neben Benutzer-Agent**das **Kontrollkästchen** Automatisch auswählen.</span><span class="sxs-lookup"><span data-stu-id="96c51-292">Next to **User agent**, clear the **Select automatically** checkbox.</span></span>  <span data-ttu-id="96c51-293">Wählen Sie dann **Custom...** aus, um aus einer Liste vordefinierter Benutzer-Agent-Zeichenfolgen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="96c51-293">Then, choose **Custom...** to select from a list of predefined user agent strings.</span></span>  <span data-ttu-id="96c51-294">Geben Sie die Zeichenfolge in Enter a custom user agent ein, um Eine eigene Zeichenfolge für den **Benutzer-Agent ein eingeben.**</span><span class="sxs-lookup"><span data-stu-id="96c51-294">To enter your own user agent string, enter the string in **Enter a custom user agent**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Festlegen der Benutzer-Agent-Zeichenfolge auf Microsoft Edge unter macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    <span data-ttu-id="96c51-296">Festlegen der Benutzer-Agent-Zeichenfolge auf Microsoft Edge unter macOS</span><span class="sxs-lookup"><span data-stu-id="96c51-296">Set the user agent string to Microsoft Edge on macOS</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="96c51-297">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="96c51-297">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /remote-debugging/index.md "Erste Schritte mit remote debuggen von Android-Geräten | Microsoft Docs"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window.devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Benutzer-Agent-| MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent.alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent.beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent.gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Reihenfolge der Näherung – Erste Reihenfolge – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="96c51-305">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96c51-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="96c51-306">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="96c51-306">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="96c51-308">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="96c51-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

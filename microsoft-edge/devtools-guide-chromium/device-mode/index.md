---
title: Simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 6973f28a0cb530e8928976adb1354fa7471ee343
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985286"
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





# <span data-ttu-id="22044-103">Simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="22044-103">Simulate mobile devices with Device Mode in Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="22044-104">Verwenden Sie den Gerätemodus, um zu sehen, wie Ihre Seite auf einem mobilen Gerät aussieht und ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22044-104">Use Device Mode to approximate how your page looks and performs on a mobile device.</span></span>  

<span data-ttu-id="22044-105">Der Gerätemodus ist der Name für die lose Sammlung von Features in Microsoft Edge devtools, mit denen Sie mobile Geräte simulieren können.</span><span class="sxs-lookup"><span data-stu-id="22044-105">Device Mode is the name for the loose collection of features in Microsoft Edge DevTools that help you simulate mobile devices.</span></span>  <span data-ttu-id="22044-106">Verfügbare Features:</span><span class="sxs-lookup"><span data-stu-id="22044-106">These features include:</span></span>  

*   [<span data-ttu-id="22044-107">Simulieren eines mobilen Viewports</span><span class="sxs-lookup"><span data-stu-id="22044-107">Simulating a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="22044-108">Einschränken des Netzwerks</span><span class="sxs-lookup"><span data-stu-id="22044-108">Throttling the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="22044-109">Drosseln der CPU</span><span class="sxs-lookup"><span data-stu-id="22044-109">Throttling the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="22044-110">Simulieren von geolokationen</span><span class="sxs-lookup"><span data-stu-id="22044-110">Simulating geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="22044-111">Festlegen der Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="22044-111">Setting orientation</span></span>](#set-orientation)  

## <span data-ttu-id="22044-112">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="22044-112">Limitations</span></span>   

<span data-ttu-id="22044-113">Denken Sie an den Gerätemodus als Näherungswert für die [erste Reihenfolge][WikiApproximation] , wie Ihre Seite auf einem mobilen Gerät aussieht und sich anfühlt.</span><span class="sxs-lookup"><span data-stu-id="22044-113">Think of Device Mode as a [first-order approximation][WikiApproximation] of how your page looks and feels on a mobile device.</span></span>  <span data-ttu-id="22044-114">Mit dem Gerätemodus führen Sie Ihren Code nicht auf einem mobilen Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="22044-114">With Device Mode you do not actually run your code on a mobile device.</span></span>  <span data-ttu-id="22044-115">Sie simulieren die mobile Benutzeroberfläche auf Ihrem Laptop oder Desktop.</span><span class="sxs-lookup"><span data-stu-id="22044-115">You simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="22044-116">Es gibt einige Aspekte von mobilen Geräten, die von devtools niemals simuliert werden können.</span><span class="sxs-lookup"><span data-stu-id="22044-116">There are some aspects of mobile devices that DevTools will never be able to simulate.</span></span>  <span data-ttu-id="22044-117">Die Architektur von mobilen CPUs unterscheidet sich beispielsweise von der Architektur von Laptop-oder Desktop-CPUs.</span><span class="sxs-lookup"><span data-stu-id="22044-117">For example, the architecture of mobile CPUs is very different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="22044-118">Im Zweifelsfall ist es am besten, wenn Sie Ihre Seite auf einem mobilen Gerät ausführen.</span><span class="sxs-lookup"><span data-stu-id="22044-118">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="22044-119">Verwenden Sie [Remote Debuggen] [DevToolsRemoteDebugging], um den Code einer Seite von Ihrem Laptop oder Desktop aus anzuzeigen, zu ändern, zu Debuggen und zu profilieren, während Sie auf einem mobilen Gerät ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22044-119">Use [Remote Debugging][DevToolsRemoteDebugging] to view, change, debug, and profile the code of a page from your laptop or desktop while it actually runs on a mobile device.</span></span>  

## <span data-ttu-id="22044-120">Simulieren eines mobilen Viewports</span><span class="sxs-lookup"><span data-stu-id="22044-120">Simulate a mobile viewport</span></span>   

<span data-ttu-id="22044-121">Klicken Sie auf **Gerätesymbolleiste umschalten** \ ( ![ Gerätesymbolleiste umschalten ][ImageDeviceToolbarIcon] \), um die Benutzeroberfläche zu öffnen, mit der Sie ein mobiles Viewport simulieren können.</span><span class="sxs-lookup"><span data-stu-id="22044-121">Click **Toggle Device Toolbar** \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="22044-123">Die Gerätesymbolleiste</span><span class="sxs-lookup"><span data-stu-id="22044-123">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="22044-124">Standardmäßig wird die Gerätesymbolleiste im reaktionsfähigen Ansichtsfenster Modus geöffnet.</span><span class="sxs-lookup"><span data-stu-id="22044-124">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="22044-125">Reaktionsfähiger viewportmodus</span><span class="sxs-lookup"><span data-stu-id="22044-125">Responsive Viewport Mode</span></span>   

<span data-ttu-id="22044-126">Ziehen Sie die Ziehpunkte, um die Größe des Viewports auf die gewünschten Bemaßungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="22044-126">Drag the handles to resize the viewport to whatever dimensions you need.</span></span>  <span data-ttu-id="22044-127">Oder geben Sie bestimmte Werte in die Felder Breite und Höhe ein.</span><span class="sxs-lookup"><span data-stu-id="22044-127">Or, enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="22044-128">In der folgenden Abbildung ist die Breite auf festzulegen, `626` und die Höhe ist auf festzulegen `516` .</span><span class="sxs-lookup"><span data-stu-id="22044-128">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
   <span data-ttu-id="22044-130">Die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus</span><span class="sxs-lookup"><span data-stu-id="22044-130">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <span data-ttu-id="22044-131">Anzeigen von medienabfragen</span><span class="sxs-lookup"><span data-stu-id="22044-131">Show media queries</span></span>   

<span data-ttu-id="22044-132">Wenn Sie medienabfrage Haltepunkte oberhalb des Viewports anzeigen möchten, klicken Sie auf **Weitere Optionen** , und wählen Sie dann **medienabfragen anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="22044-132">To show media query breakpoints above your viewport, click **More options** and then select **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Anzeigen von medienabfragen" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="22044-134">Anzeigen von medienabfragen</span><span class="sxs-lookup"><span data-stu-id="22044-134">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="22044-135">Klicken Sie auf einen Haltepunkt, um die Breite des Viewports so zu ändern, dass der Haltepunkt ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="22044-135">Click a breakpoint to change the width of the viewport so that the breakpoint gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Klicken Sie auf einen Haltepunkt, um die Breite des Viewports zu ändern." lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="22044-137">Klicken Sie auf einen Haltepunkt, um die Breite des Viewports zu ändern.</span><span class="sxs-lookup"><span data-stu-id="22044-137">Click a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <span data-ttu-id="22044-138">Einrichten des Gerätetyps</span><span class="sxs-lookup"><span data-stu-id="22044-138">Set the device type</span></span>   

<span data-ttu-id="22044-139">Verwenden Sie die Liste **Gerätetyp** , um ein mobiles Gerät oder ein Desktop Gerät zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="22044-139">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Liste der Gerätetypen" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="22044-141">Liste der **Gerätetypen**</span><span class="sxs-lookup"><span data-stu-id="22044-141">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="22044-142">In der nachstehenden Tabelle werden die Unterschiede zwischen den Optionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="22044-142">The table below describes the differences between the options.</span></span>  <span data-ttu-id="22044-143">Die **Rendering-Methode** bezieht sich darauf, ob Microsoft Edge die Seite als mobiles oder Desktop-Viewport rendert.</span><span class="sxs-lookup"><span data-stu-id="22044-143">**Rendering method** refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="22044-144">Das **Cursor Symbol** bezieht sich auf den Typ des Cursors, den Sie sehen, wenn Sie auf die Seite zeigen.</span><span class="sxs-lookup"><span data-stu-id="22044-144">**Cursor icon** refers to what type of cursor you see when you hover over the page.</span></span>  <span data-ttu-id="22044-145">**Ausgelöste Ereignisse** bezieht sich darauf, ob die Seite ausgelöst `touch` wird, oder `click` Ereignisse, wenn Sie mit der Seite interagieren.</span><span class="sxs-lookup"><span data-stu-id="22044-145">**Events fired** refers to whether the page fires `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="22044-146">Option</span><span class="sxs-lookup"><span data-stu-id="22044-146">Option</span></span> | <span data-ttu-id="22044-147">Rendering-Methode</span><span class="sxs-lookup"><span data-stu-id="22044-147">Rendering method</span></span> | <span data-ttu-id="22044-148">Cursor Symbol</span><span class="sxs-lookup"><span data-stu-id="22044-148">Cursor icon</span></span> | <span data-ttu-id="22044-149">Ausgelöste Ereignisse</span><span class="sxs-lookup"><span data-stu-id="22044-149">Events fired</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="22044-150">Mobilgeräte</span><span class="sxs-lookup"><span data-stu-id="22044-150">Mobile</span></span> | <span data-ttu-id="22044-151">Mobilgeräte</span><span class="sxs-lookup"><span data-stu-id="22044-151">Mobile</span></span> | <span data-ttu-id="22044-152">Kreis</span><span class="sxs-lookup"><span data-stu-id="22044-152">Circle</span></span> | <span data-ttu-id="22044-153">Toucheingabe</span><span class="sxs-lookup"><span data-stu-id="22044-153">touch</span></span> |  
| <span data-ttu-id="22044-154">Mobil \ (kein Touch \)</span><span class="sxs-lookup"><span data-stu-id="22044-154">Mobile \(no touch\)</span></span> | <span data-ttu-id="22044-155">Mobilgeräte</span><span class="sxs-lookup"><span data-stu-id="22044-155">Mobile</span></span> | <span data-ttu-id="22044-156">Normal</span><span class="sxs-lookup"><span data-stu-id="22044-156">Normal</span></span> | <span data-ttu-id="22044-157"> auf </span><span class="sxs-lookup"><span data-stu-id="22044-157">click</span></span> |  
| <span data-ttu-id="22044-158">Desktop</span><span class="sxs-lookup"><span data-stu-id="22044-158">Desktop</span></span> | <span data-ttu-id="22044-159">Desktop</span><span class="sxs-lookup"><span data-stu-id="22044-159">Desktop</span></span> | <span data-ttu-id="22044-160">Normal</span><span class="sxs-lookup"><span data-stu-id="22044-160">Normal</span></span> | <span data-ttu-id="22044-161"> auf </span><span class="sxs-lookup"><span data-stu-id="22044-161">click</span></span> |  
| <span data-ttu-id="22044-162">Desktop \ (tippen Sie auf \)</span><span class="sxs-lookup"><span data-stu-id="22044-162">Desktop \(touch\)</span></span> | <span data-ttu-id="22044-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="22044-163">Desktop</span></span> | <span data-ttu-id="22044-164">Kreis</span><span class="sxs-lookup"><span data-stu-id="22044-164">Circle</span></span> | <span data-ttu-id="22044-165">Toucheingabe</span><span class="sxs-lookup"><span data-stu-id="22044-165">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="22044-166">Wenn die Liste **Gerätetyp** nicht angezeigt wird, klicken Sie auf **Weitere Optionen** , und wählen Sie **Gerätetyp hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="22044-166">If you do not see the **Device Type** list, click **More options** and select **Add device type**.</span></span>  

### <span data-ttu-id="22044-167">Ansichtsfenster Modus für mobile Geräte</span><span class="sxs-lookup"><span data-stu-id="22044-167">Mobile Device Viewport Mode</span></span>   

<span data-ttu-id="22044-168">Wenn Sie die Abmessungen eines bestimmten mobilen Geräts simulieren möchten, wählen Sie das Gerät in der **Geräte** Liste aus.</span><span class="sxs-lookup"><span data-stu-id="22044-168">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Geräteliste" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="22044-170">**Geräte** Liste</span><span class="sxs-lookup"><span data-stu-id="22044-170">The **Device** list</span></span>  
:::image-end:::  

#### <span data-ttu-id="22044-171">Drehen des Viewports in Querformat</span><span class="sxs-lookup"><span data-stu-id="22044-171">Rotate the viewport to landscape orientation</span></span>   

<span data-ttu-id="22044-172">Klicken Sie auf **drehen** \ ( ![ drehen ][ImageRotateIcon] \), um das Ansichtsfenster in Querformat zu drehen.</span><span class="sxs-lookup"><span data-stu-id="22044-172">Click **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Querformat" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
   <span data-ttu-id="22044-174">Querformat</span><span class="sxs-lookup"><span data-stu-id="22044-174">Landscape orientation</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="22044-175">Die Schaltfläche **drehen** verschwindet, wenn die **Gerätesymbolleiste** schmal ist.</span><span class="sxs-lookup"><span data-stu-id="22044-175">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="22044-177">Die **Gerätesymbolleiste**</span><span class="sxs-lookup"><span data-stu-id="22044-177">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="22044-178">Siehe auch [Ausrichtung einstellen](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="22044-178">See also [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="22044-179">Geräterahmen anzeigen</span><span class="sxs-lookup"><span data-stu-id="22044-179">Show device frame</span></span>   

<span data-ttu-id="22044-180">Wenn Sie die Abmessungen eines bestimmten mobilen Geräts wie ein iPhone 6 simulieren, öffnen Sie **Weitere Optionen** , und wählen Sie dann **Geräterahmen anzeigen** aus, um den Frame des physikalischen Geräts um den Viewport anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22044-180">When simulating the dimensions of a specific mobile device like an iPhone 6, open **More options** and then select **Show device frame** to show the physical device frame around the viewport.</span></span>  

> [!NOTE]
> <span data-ttu-id="22044-181">Wenn ein Geräterahmen für ein bestimmtes Gerät nicht angezeigt wird, bedeutet dies wahrscheinlich, dass devtools gerade keine Grafiken für diese bestimmte Option hat.</span><span class="sxs-lookup"><span data-stu-id="22044-181">If you do not see a device frame for a particular device, it probably means that DevTools just does not have art for that specific option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Geräterahmen anzeigen" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="22044-183">Geräterahmen anzeigen</span><span class="sxs-lookup"><span data-stu-id="22044-183">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Der Geräterahmen für das iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="22044-185">Der Geräterahmen für das iPhone 6</span><span class="sxs-lookup"><span data-stu-id="22044-185">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="22044-186">Hinzufügen eines benutzerdefinierten mobilen Geräts</span><span class="sxs-lookup"><span data-stu-id="22044-186">Add a custom mobile device</span></span>   

<span data-ttu-id="22044-187">So fügen Sie ein benutzerdefiniertes Gerät hinzu:</span><span class="sxs-lookup"><span data-stu-id="22044-187">To add a custom device:</span></span>  

1.  <span data-ttu-id="22044-188">Klicken Sie auf die **Geräte** Liste, und wählen Sie dann **Bearbeiten**aus.</span><span class="sxs-lookup"><span data-stu-id="22044-188">Click the **Device** list and then select **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Wählen Sie bearbeiten aus." lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="22044-190">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="22044-190">Select **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="22044-191">Klicken Sie auf **Benutzerdefiniertes Gerät hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="22044-191">Click **Add custom device**.</span></span>  
1.  <span data-ttu-id="22044-192">Geben Sie einen Namen, eine Breite und eine Höhe für das Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="22044-192">Enter a name, width, and height for the device.</span></span>  <span data-ttu-id="22044-193">Die Felder für das [Pixel Verhältnis des Geräts][MDNWindowDevicePixelRatio], die [Zeichenfolge des Benutzer-Agents][MDNUserAgent]und die [Gerätetypen](#set-the-device-type) sind optional.</span><span class="sxs-lookup"><span data-stu-id="22044-193">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="22044-194">Das Feld "Gerätetyp" ist die Liste, die standardmäßig auf " **Mobiltelefon** " festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="22044-194">The device type field is the list that is set to **Mobile** by default.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Erstellen eines benutzerdefinierten Geräts" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="22044-196">Erstellen eines benutzerdefinierten Geräts</span><span class="sxs-lookup"><span data-stu-id="22044-196">Createa custom device</span></span>  
    :::image-end:::  

### <span data-ttu-id="22044-197">Lineale anzeigen</span><span class="sxs-lookup"><span data-stu-id="22044-197">Show rulers</span></span>   

<span data-ttu-id="22044-198">Klicken Sie auf **Weitere Optionen** , und wählen Sie dann **Lineale anzeigen** aus, um die Lineale oberhalb und Links des Viewports anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22044-198">Click **More options** and then select **Show rulers** to see rulers above and to the left of your viewport.</span></span>  <span data-ttu-id="22044-199">Die Größeneinheit der Lineale ist Pixel.</span><span class="sxs-lookup"><span data-stu-id="22044-199">The sizing unit of the rulers is pixels.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Lineale anzeigen" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         **<span data-ttu-id="22044-201">Lineale anzeigen</span><span class="sxs-lookup"><span data-stu-id="22044-201">Show rulers</span></span>**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Lineale oberhalb und Links des Viewports" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="22044-203">Lineale oberhalb und Links des Viewports</span><span class="sxs-lookup"><span data-stu-id="22044-203">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="22044-204">Zoomen des Viewports</span><span class="sxs-lookup"><span data-stu-id="22044-204">Zoom the viewport</span></span>   

<span data-ttu-id="22044-205">Verwenden Sie die **zoomliste** , um die Ansicht zu vergrößern oder zu verkleinern.</span><span class="sxs-lookup"><span data-stu-id="22044-205">Use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="22044-207">Zoom</span><span class="sxs-lookup"><span data-stu-id="22044-207">Zoom</span></span>**  
:::image-end:::  

## <span data-ttu-id="22044-208">Netzwerk und CPU drosseln</span><span class="sxs-lookup"><span data-stu-id="22044-208">Throttle the network and CPU</span></span>   

<span data-ttu-id="22044-209">Wenn Sie das Netzwerk und die CPU Drosseln möchten, wählen Sie **Mid-Tier-Handy** oder **Low-End-Handy** aus der **Drosselungs** Liste aus.</span><span class="sxs-lookup"><span data-stu-id="22044-209">To throttle the network and CPU, select **Mid-tier mobile** or **Low-end mobile** from the **Throttle** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Die Drosselungs Liste" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="22044-211">Die **Drosselungs** Liste</span><span class="sxs-lookup"><span data-stu-id="22044-211">The **Throttle** list</span></span>  
:::image-end:::  

<span data-ttu-id="22044-212">**Mid-Tier-Handy** simuliert schnelles 3G und drosselt Ihre CPU so, dass Sie viermal langsamer als normal ist.</span><span class="sxs-lookup"><span data-stu-id="22044-212">**Mid-tier mobile** simulates fast 3G and throttles your CPU so that it is 4 times slower than normal.</span></span>  <span data-ttu-id="22044-213">**Low-End-Mobile** simuliert langsames 3G und bremst Ihre CPU sechsmal langsamer als normal.</span><span class="sxs-lookup"><span data-stu-id="22044-213">**Low-end mobile** simulates slow 3G and throttles your CPU 6 times slower than normal.</span></span>  <span data-ttu-id="22044-214">Beachten Sie, dass die Drosselung relativ zur normalen Funktion Ihres Laptops oder Desktops ist.</span><span class="sxs-lookup"><span data-stu-id="22044-214">Keep in mind that the throttling is relative to the normal capability of your laptop or desktop.</span></span>  

> [!NOTE]
> <span data-ttu-id="22044-215">Die **Drosselungs** Liste ist ausgeblendet, wenn die **Gerätesymbolleiste** schmal ist.</span><span class="sxs-lookup"><span data-stu-id="22044-215">The **Throttle** list is hidden if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Die Gerätesymbolleiste" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="22044-217">Die **Gerätesymbolleiste**</span><span class="sxs-lookup"><span data-stu-id="22044-217">The **Device Toolbar**</span></span>  
:::image-end:::  

### <span data-ttu-id="22044-218">Nur die CPU drosseln</span><span class="sxs-lookup"><span data-stu-id="22044-218">Throttle the CPU only</span></span>   

<span data-ttu-id="22044-219">Wenn Sie nur die CPU und nicht das Netzwerk Drosseln möchten, wechseln Sie zum **Leistungs** Panel, klicken Sie auf **Aufnahmeeinstellungen** \ ( ![ Aufnahmeeinstellungen ][ImageCaptureIcon] \), und wählen Sie dann in der **CPU** -Liste die Option **4X Verlangsamung** oder **6x Verlangsamung** aus.</span><span class="sxs-lookup"><span data-stu-id="22044-219">To throttle the CPU only and not the network, go to the **Performance** panel, click **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\), and then select **4x slowdown** or **6x slowdown** from the **CPU** list.</span></span>  

:::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Die CPU-Liste" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
   <span data-ttu-id="22044-221">Die **CPU** -Liste</span><span class="sxs-lookup"><span data-stu-id="22044-221">The **CPU** list</span></span>  
:::image-end:::  

### <span data-ttu-id="22044-222">Nur das Netzwerk drosseln</span><span class="sxs-lookup"><span data-stu-id="22044-222">Throttle the network only</span></span>   

<span data-ttu-id="22044-223">Wenn Sie nur das Netzwerk und nicht die CPU Drosseln möchten, gehen Sie zum **Netzwerk** Panel, und wählen Sie **fast 3G** oder **Slow 3G** aus der **Drosselungs** Liste aus.</span><span class="sxs-lookup"><span data-stu-id="22044-223">To throttle the network only and not the CPU, go the **Network** panel and select **Fast 3G** or **Slow 3G** from the **Throttle** list.</span></span>  

:::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Die Drosselungs Liste" lightbox="../media/device-mode-network-throttle.msft.png":::
   <span data-ttu-id="22044-225">Die **Drosselungs** Liste</span><span class="sxs-lookup"><span data-stu-id="22044-225">The **Throttle** list</span></span>  
:::image-end:::  

<span data-ttu-id="22044-226">Oder drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen, geben `3G` Sie ein, und wählen Sie **fast 3G-Drosselung aktivieren** oder **langsame 3G-Drosselung aktivieren**aus.</span><span class="sxs-lookup"><span data-stu-id="22044-226">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and select **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  

:::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
   <span data-ttu-id="22044-228">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="22044-228">The **Command Menu**</span></span>  
:::image-end:::  

<span data-ttu-id="22044-229">Sie können die Netzwerk Drosselung auch über das **Leistungs** Panel einstellen.</span><span class="sxs-lookup"><span data-stu-id="22044-229">You can also set network throttling from the **Performance** panel.</span></span>  <span data-ttu-id="22044-230">Klicken Sie auf **aufnahmeeinstellungen** \ ( ![ Aufnahmeeinstellungen ][ImageCaptureIcon] \), und wählen Sie dann in der Liste **Netzwerk** die Option **fast 3G** oder **Slow 3G** aus.</span><span class="sxs-lookup"><span data-stu-id="22044-230">Click **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and then select **Fast 3G** or **Slow 3G** from the **Network** list.</span></span>  

:::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Einrichten der Netzwerk Drosselung im Leistungs Panel" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
   <span data-ttu-id="22044-232">Einrichten der Netzwerk Drosselung im **Leistungs** Panel</span><span class="sxs-lookup"><span data-stu-id="22044-232">Set network throttling from the **Performance** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="22044-233">Überschreiben von Geolocation</span><span class="sxs-lookup"><span data-stu-id="22044-233">Override geolocation</span></span>   

<span data-ttu-id="22044-234">Klicken Sie zum Öffnen der Benutzeroberfläche für Geolocation auf **anpassen und Steuern von devtools** \ ( `...` \), und wählen Sie dann **Weitere Tools**-  >  **Sensoren**aus.</span><span class="sxs-lookup"><span data-stu-id="22044-234">To open the geolocation overriding UI click **Customize and control DevTools** \(`...`\) and then select **More tools** > **Sensors**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensoren" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
   **<span data-ttu-id="22044-236">Sensoren</span><span class="sxs-lookup"><span data-stu-id="22044-236">Sensors</span></span>**  
:::image-end:::  

<span data-ttu-id="22044-237">Oder drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Menübefehl zu öffnen, geben `Sensors` Sie ein, und wählen Sie dann **Sensoren anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="22044-237">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Sensoren anzeigen" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
   **<span data-ttu-id="22044-239">Sensoren anzeigen</span><span class="sxs-lookup"><span data-stu-id="22044-239">Show Sensors</span></span>**  
:::image-end:::  

<span data-ttu-id="22044-240">Wählen Sie eine der Voreinstellungen aus der Liste **Geolocation** aus, oder wählen Sie **benutzerdefinierter Speicherort** aus, um Ihre eigenen Koordinaten einzugeben, oder wählen Sie **nicht verfügbarer Speicherort** aus, um zu testen, wie sich die Seite verhält, wenn sich die Geolokation in einem Fehlerzustand befindet.</span><span class="sxs-lookup"><span data-stu-id="22044-240">Select one of the presets from the **Geolocation** list, or select **Custom location** to enter your own coordinates, or select **Location unavailable** to test out how your page behaves when geolocation is in an error state.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Geolocation" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
   **<span data-ttu-id="22044-242">Geolocation</span><span class="sxs-lookup"><span data-stu-id="22044-242">Geolocation</span></span>**  
:::image-end:::  

## <span data-ttu-id="22044-243">Ausrichtung einstellen</span><span class="sxs-lookup"><span data-stu-id="22044-243">Set orientation</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="22044-244">Klicken Sie zum Öffnen der UI für die Ausrichtung auf **anpassen und Steuern von devtools** `...` , und wählen Sie dann **Weitere Tools**-  >  **Sensoren**aus.</span><span class="sxs-lookup"><span data-stu-id="22044-244">To open the orientation UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensoren" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **<span data-ttu-id="22044-246">Sensoren</span><span class="sxs-lookup"><span data-stu-id="22044-246">Sensors</span></span>**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="22044-247">Oder drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Menübefehl zu öffnen, geben `Sensors` Sie ein, und wählen Sie dann **Sensoren anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="22044-247">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Sensoren anzeigen" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **<span data-ttu-id="22044-249">Sensoren anzeigen</span><span class="sxs-lookup"><span data-stu-id="22044-249">Show Sensors</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="22044-250">Wählen Sie eine der Voreinstellungen aus der **Ausrichtungs** Liste aus, oder wählen Sie **benutzerdefinierte Ausrichtung** aus, um Ihre eigenen Alpha-, Beta-und Gammawerte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="22044-250">Select one of the presets from the **Orientation** list or select **Custom orientation** to set your own alpha, beta, and gamma values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Ausrichtung" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
   **<span data-ttu-id="22044-252">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="22044-252">Orientation</span></span>**  
:::image-end:::  

<!--  
 


-->  

<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/Index.MD "erste Schritte mit dem Remotedebuggen von Android-Geräten | Microsoft docs "  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Benutzer-Agent | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Reihenfolge der Näherung – First-Order – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="22044-257">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22044-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="22044-258">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="22044-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="22044-260">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="22044-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

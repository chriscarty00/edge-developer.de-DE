---
title: Simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 10c1ee12777965778ebec2d257399dc231e2a01a
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607426"
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





# <span data-ttu-id="efd4b-103">Simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="efd4b-103">Simulate Mobile Devices with Device Mode in Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="efd4b-104">Verwenden Sie den Gerätemodus, um zu sehen, wie Ihre Seite auf einem mobilen Gerät aussieht und ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efd4b-104">Use Device Mode to approximate how your page looks and performs on a mobile device.</span></span>  

<span data-ttu-id="efd4b-105">Der Gerätemodus ist der Name für die lose Sammlung von Features in Microsoft Edge devtools, mit denen Sie mobile Geräte simulieren können.</span><span class="sxs-lookup"><span data-stu-id="efd4b-105">Device Mode is the name for the loose collection of features in Microsoft Edge DevTools that help you simulate mobile devices.</span></span>  <span data-ttu-id="efd4b-106">Verfügbare Features:</span><span class="sxs-lookup"><span data-stu-id="efd4b-106">These features include:</span></span>  

*   [<span data-ttu-id="efd4b-107">Simulieren eines mobilen Viewports</span><span class="sxs-lookup"><span data-stu-id="efd4b-107">Simulating a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="efd4b-108">Einschränken des Netzwerks</span><span class="sxs-lookup"><span data-stu-id="efd4b-108">Throttling the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="efd4b-109">Drosseln der CPU</span><span class="sxs-lookup"><span data-stu-id="efd4b-109">Throttling the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="efd4b-110">Simulieren von geolokationen</span><span class="sxs-lookup"><span data-stu-id="efd4b-110">Simulating geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="efd4b-111">Festlegen der Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="efd4b-111">Setting orientation</span></span>](#set-orientation)  

## <span data-ttu-id="efd4b-112">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="efd4b-112">Limitations</span></span>   

<span data-ttu-id="efd4b-113">Denken Sie an den Gerätemodus als Näherungswert für die [erste Reihenfolge][WikiApproximation] , wie Ihre Seite auf einem mobilen Gerät aussieht und sich anfühlt.</span><span class="sxs-lookup"><span data-stu-id="efd4b-113">Think of Device Mode as a [first-order approximation][WikiApproximation] of how your page looks and feels on a mobile device.</span></span>  <span data-ttu-id="efd4b-114">Mit dem Gerätemodus führen Sie Ihren Code nicht auf einem mobilen Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-114">With Device Mode you do not actually run your code on a mobile device.</span></span>  <span data-ttu-id="efd4b-115">Sie simulieren die mobile Benutzeroberfläche auf Ihrem Laptop oder Desktop.</span><span class="sxs-lookup"><span data-stu-id="efd4b-115">You simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="efd4b-116">Es gibt einige Aspekte von mobilen Geräten, die von devtools niemals simuliert werden können.</span><span class="sxs-lookup"><span data-stu-id="efd4b-116">There are some aspects of mobile devices that DevTools will never be able to simulate.</span></span>  <span data-ttu-id="efd4b-117">Die Architektur von mobilen CPUs unterscheidet sich beispielsweise von der Architektur von Laptop-oder Desktop-CPUs.</span><span class="sxs-lookup"><span data-stu-id="efd4b-117">For example, the architecture of mobile CPUs is very different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="efd4b-118">Im Zweifelsfall ist es am besten, wenn Sie Ihre Seite auf einem mobilen Gerät ausführen.</span><span class="sxs-lookup"><span data-stu-id="efd4b-118">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="efd4b-119">Verwenden Sie [Remote Debuggen] [DevToolsRemoteDebugging], um den Code einer Seite von Ihrem Laptop oder Desktop aus anzuzeigen, zu ändern, zu Debuggen und zu profilieren, während Sie auf einem mobilen Gerät ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efd4b-119">Use [Remote Debugging][DevToolsRemoteDebugging] to view, change, debug, and profile the code of a page from your laptop or desktop while it actually runs on a mobile device.</span></span>  

## <span data-ttu-id="efd4b-120">Simulieren eines mobilen Viewports</span><span class="sxs-lookup"><span data-stu-id="efd4b-120">Simulate a mobile viewport</span></span>   

<span data-ttu-id="efd4b-121">Klicken Sie auf **Geräte** Symbolleiste Umschalten auf Geräte ![ Symbolleiste ][ImageDeviceToolbarIcon] , um die Benutzeroberfläche zu öffnen, mit der Sie ein mobiles Viewport simulieren können.</span><span class="sxs-lookup"><span data-stu-id="efd4b-121">Click **Toggle Device Toolbar** ![Toggle Device Toolbar][ImageDeviceToolbarIcon] to open the UI that enables you to simulate a mobile viewport.</span></span>  

> ##### <span data-ttu-id="efd4b-122">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="efd4b-122">Figure 1</span></span>  
> <span data-ttu-id="efd4b-123">Die Gerätesymbolleiste</span><span class="sxs-lookup"><span data-stu-id="efd4b-123">The Device Toolbar</span></span>  
> ![Die Gerätesymbolleiste][ImageDeviceToolbar]  

<span data-ttu-id="efd4b-125">Standardmäßig wird die Gerätesymbolleiste im reaktionsfähigen Ansichtsfenster Modus geöffnet.</span><span class="sxs-lookup"><span data-stu-id="efd4b-125">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="efd4b-126">Reaktionsfähiger viewportmodus</span><span class="sxs-lookup"><span data-stu-id="efd4b-126">Responsive Viewport Mode</span></span>   

<span data-ttu-id="efd4b-127">Ziehen Sie die Ziehpunkte, um die Größe des Viewports auf die gewünschten Bemaßungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="efd4b-127">Drag the handles to resize the viewport to whatever dimensions you need.</span></span>  <span data-ttu-id="efd4b-128">Oder geben Sie bestimmte Werte in die Felder Breite und Höhe ein.</span><span class="sxs-lookup"><span data-stu-id="efd4b-128">Or, enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="efd4b-129">In [Abbildung 2](#figure-2)ist die Breite auf festzulegen, `626` und die Höhe ist auf festzulegen `516` .</span><span class="sxs-lookup"><span data-stu-id="efd4b-129">In [Figure 2](#figure-2), the width is set to `626` and the height is set to `516`.</span></span>  

> ##### <span data-ttu-id="efd4b-130">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="efd4b-130">Figure 2</span></span>  
> <span data-ttu-id="efd4b-131">Die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus</span><span class="sxs-lookup"><span data-stu-id="efd4b-131">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
> ![Die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus][ImageResponsiveHandles]  

#### <span data-ttu-id="efd4b-133">Anzeigen von medienabfragen</span><span class="sxs-lookup"><span data-stu-id="efd4b-133">Show media queries</span></span>   

<span data-ttu-id="efd4b-134">Wenn Sie medienabfrage Haltepunkte oberhalb des Viewports anzeigen möchten, klicken Sie auf **Weitere Optionen** , und wählen Sie dann **medienabfragen anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-134">To show media query breakpoints above your viewport, click **More options** and then select **Show media queries**.</span></span>  

> ##### <span data-ttu-id="efd4b-135">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="efd4b-135">Figure 3</span></span>  
> <span data-ttu-id="efd4b-136">Anzeigen von medienabfragen</span><span class="sxs-lookup"><span data-stu-id="efd4b-136">Show media queries</span></span>  
> ![Anzeigen von medienabfragen][ImageShowMediaQueries]  

<span data-ttu-id="efd4b-138">Klicken Sie auf einen Haltepunkt, um die Breite des Viewports so zu ändern, dass der Haltepunkt ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="efd4b-138">Click a breakpoint to change the width of the viewport so that the breakpoint gets triggered.</span></span>  

> ##### <span data-ttu-id="efd4b-139">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="efd4b-139">Figure 4</span></span>  
> <span data-ttu-id="efd4b-140">Klicken Sie auf einen Haltepunkt, um die Breite des Viewports zu ändern.</span><span class="sxs-lookup"><span data-stu-id="efd4b-140">Click a breakpoint to change the width of the viewport</span></span>  
> ![Klicken Sie auf einen Haltepunkt, um die Breite des Viewports zu ändern.][ImageBreakpoint]  

#### <span data-ttu-id="efd4b-142">Einrichten des Gerätetyps</span><span class="sxs-lookup"><span data-stu-id="efd4b-142">Set the device type</span></span>   

<span data-ttu-id="efd4b-143">Verwenden Sie die Liste **Gerätetyp** , um ein mobiles Gerät oder ein Desktop Gerät zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="efd4b-143">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

> ##### <span data-ttu-id="efd4b-144">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="efd4b-144">Figure 5</span></span>  
> <span data-ttu-id="efd4b-145">Liste der **Gerätetypen**</span><span class="sxs-lookup"><span data-stu-id="efd4b-145">The **Device Type** list</span></span>  
> ![Liste der Gerätetypen][ImageDeviceType]  

<span data-ttu-id="efd4b-147">In der nachstehenden Tabelle werden die Unterschiede zwischen den Optionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="efd4b-147">The table below describes the differences between the options.</span></span>  <span data-ttu-id="efd4b-148">Die **Rendering-Methode** bezieht sich darauf, ob Microsoft Edge die Seite als mobiles oder Desktop-Viewport rendert.</span><span class="sxs-lookup"><span data-stu-id="efd4b-148">**Rendering method** refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="efd4b-149">Das **Cursor Symbol** bezieht sich auf den Typ des Cursors, den Sie sehen, wenn Sie auf die Seite zeigen.</span><span class="sxs-lookup"><span data-stu-id="efd4b-149">**Cursor icon** refers to what type of cursor you see when you hover over the page.</span></span>  <span data-ttu-id="efd4b-150">**Ausgelöste Ereignisse** bezieht sich darauf, ob die Seite ausgelöst `touch` wird, oder `click` Ereignisse, wenn Sie mit der Seite interagieren.</span><span class="sxs-lookup"><span data-stu-id="efd4b-150">**Events fired** refers to whether the page fires `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="efd4b-151">Option</span><span class="sxs-lookup"><span data-stu-id="efd4b-151">Option</span></span> | <span data-ttu-id="efd4b-152">Rendering-Methode</span><span class="sxs-lookup"><span data-stu-id="efd4b-152">Rendering method</span></span> | <span data-ttu-id="efd4b-153">Cursor Symbol</span><span class="sxs-lookup"><span data-stu-id="efd4b-153">Cursor icon</span></span> | <span data-ttu-id="efd4b-154">Ausgelöste Ereignisse</span><span class="sxs-lookup"><span data-stu-id="efd4b-154">Events fired</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="efd4b-155">Mobilgeräte</span><span class="sxs-lookup"><span data-stu-id="efd4b-155">Mobile</span></span> | <span data-ttu-id="efd4b-156">Mobilgeräte</span><span class="sxs-lookup"><span data-stu-id="efd4b-156">Mobile</span></span> | <span data-ttu-id="efd4b-157">Kreis</span><span class="sxs-lookup"><span data-stu-id="efd4b-157">Circle</span></span> | <span data-ttu-id="efd4b-158">Toucheingabe</span><span class="sxs-lookup"><span data-stu-id="efd4b-158">touch</span></span> |  
| <span data-ttu-id="efd4b-159">Mobil \ (kein Touch \)</span><span class="sxs-lookup"><span data-stu-id="efd4b-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="efd4b-160">Mobilgeräte</span><span class="sxs-lookup"><span data-stu-id="efd4b-160">Mobile</span></span> | <span data-ttu-id="efd4b-161">Normal</span><span class="sxs-lookup"><span data-stu-id="efd4b-161">Normal</span></span> | <span data-ttu-id="efd4b-162"> auf </span><span class="sxs-lookup"><span data-stu-id="efd4b-162">click</span></span> |  
| <span data-ttu-id="efd4b-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="efd4b-163">Desktop</span></span> | <span data-ttu-id="efd4b-164">Desktop</span><span class="sxs-lookup"><span data-stu-id="efd4b-164">Desktop</span></span> | <span data-ttu-id="efd4b-165">Normal</span><span class="sxs-lookup"><span data-stu-id="efd4b-165">Normal</span></span> | <span data-ttu-id="efd4b-166"> auf </span><span class="sxs-lookup"><span data-stu-id="efd4b-166">click</span></span> |  
| <span data-ttu-id="efd4b-167">Desktop \ (tippen Sie auf \)</span><span class="sxs-lookup"><span data-stu-id="efd4b-167">Desktop \(touch\)</span></span> | <span data-ttu-id="efd4b-168">Desktop</span><span class="sxs-lookup"><span data-stu-id="efd4b-168">Desktop</span></span> | <span data-ttu-id="efd4b-169">Kreis</span><span class="sxs-lookup"><span data-stu-id="efd4b-169">Circle</span></span> | <span data-ttu-id="efd4b-170">Toucheingabe</span><span class="sxs-lookup"><span data-stu-id="efd4b-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="efd4b-171">Wenn die Liste **Gerätetyp** nicht angezeigt wird, klicken Sie auf **Weitere Optionen** , und wählen Sie **Gerätetyp hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-171">If you do not see the **Device Type** list, click **More options** and select **Add device type**.</span></span>  

### <span data-ttu-id="efd4b-172">Ansichtsfenster Modus für mobile Geräte</span><span class="sxs-lookup"><span data-stu-id="efd4b-172">Mobile Device Viewport Mode</span></span>   

<span data-ttu-id="efd4b-173">Wenn Sie die Abmessungen eines bestimmten mobilen Geräts simulieren möchten, wählen Sie das Gerät in der **Geräte** Liste aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

> ##### <span data-ttu-id="efd4b-174">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="efd4b-174">Figure 6</span></span>  
> <span data-ttu-id="efd4b-175">Geräteliste</span><span class="sxs-lookup"><span data-stu-id="efd4b-175">The Device list</span></span>  
> ![Geräteliste][ImageDeviceList]  

#### <span data-ttu-id="efd4b-177">Drehen des Viewports in Querformat</span><span class="sxs-lookup"><span data-stu-id="efd4b-177">Rotate the viewport to landscape orientation</span></span>   

<span data-ttu-id="efd4b-178">Klicken **Sie auf Drehung drehen** ![ ][ImageRotateIcon] , um das Ansichtsfenster in Querformat zu drehen.</span><span class="sxs-lookup"><span data-stu-id="efd4b-178">Click **Rotate** ![Rotate][ImageRotateIcon] to rotate the viewport to landscape orientation.</span></span>  

> ##### <span data-ttu-id="efd4b-179">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="efd4b-179">Figure 7</span></span>  
> <span data-ttu-id="efd4b-180">Querformat</span><span class="sxs-lookup"><span data-stu-id="efd4b-180">Landscape orientation</span></span>  
> ![Querformat][ImageLandscape]  

> [!NOTE]
> <span data-ttu-id="efd4b-182">Die Schaltfläche **drehen** verschwindet, wenn die **Gerätesymbolleiste** schmal ist.</span><span class="sxs-lookup"><span data-stu-id="efd4b-182">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

> ##### <span data-ttu-id="efd4b-183">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="efd4b-183">Figure 8</span></span>  
> <span data-ttu-id="efd4b-184">Die Gerätesymbolleiste</span><span class="sxs-lookup"><span data-stu-id="efd4b-184">The Device Toolbar</span></span>  
> ![Die Gerätesymbolleiste][ImageDeviceToolbar2]  

<span data-ttu-id="efd4b-186">Siehe auch [Ausrichtung einstellen](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="efd4b-186">See also [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="efd4b-187">Geräterahmen anzeigen</span><span class="sxs-lookup"><span data-stu-id="efd4b-187">Show device frame</span></span>   

<span data-ttu-id="efd4b-188">Wenn Sie die Abmessungen eines bestimmten mobilen Geräts wie ein iPhone 6 simulieren, öffnen Sie **Weitere Optionen** , und wählen Sie dann **Geräterahmen anzeigen** aus, um den Frame des physikalischen Geräts um den Viewport anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="efd4b-188">When simulating the dimensions of a specific mobile device like an iPhone 6, open **More options** and then select **Show device frame** to show the physical device frame around the viewport.</span></span>  

> [!NOTE]
> <span data-ttu-id="efd4b-189">Wenn ein Geräterahmen für ein bestimmtes Gerät nicht angezeigt wird, bedeutet dies wahrscheinlich, dass devtools gerade keine Grafiken für diese bestimmte Option hat.</span><span class="sxs-lookup"><span data-stu-id="efd4b-189">If you do not see a device frame for a particular device, it probably means that DevTools just does not have art for that specific option.</span></span>  

> ##### <span data-ttu-id="efd4b-190">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="efd4b-190">Figure 9</span></span>  
> <span data-ttu-id="efd4b-191">Geräterahmen anzeigen</span><span class="sxs-lookup"><span data-stu-id="efd4b-191">Show device frame</span></span>  
> ![Geräterahmen anzeigen][ImageShowDeviceFrame]  

> ##### <span data-ttu-id="efd4b-193">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="efd4b-193">Figure 10</span></span>  
> <span data-ttu-id="efd4b-194">Der Geräterahmen für das iPhone 6</span><span class="sxs-lookup"><span data-stu-id="efd4b-194">The device frame for the iPhone 6</span></span>  
> ![Der Geräterahmen für das iPhone 6][ImageIphoneFrame]  

#### <span data-ttu-id="efd4b-196">Hinzufügen eines benutzerdefinierten mobilen Geräts</span><span class="sxs-lookup"><span data-stu-id="efd4b-196">Add a custom mobile device</span></span>   

<span data-ttu-id="efd4b-197">So fügen Sie ein benutzerdefiniertes Gerät hinzu:</span><span class="sxs-lookup"><span data-stu-id="efd4b-197">To add a custom device:</span></span>  

1.  <span data-ttu-id="efd4b-198">Klicken Sie auf die **Geräte** Liste, und wählen Sie dann **Bearbeiten**aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-198">Click the **Device** list and then select **Edit**.</span></span>  

> ##### <span data-ttu-id="efd4b-199">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="efd4b-199">Figure 11</span></span>  
> <span data-ttu-id="efd4b-200">Auswählen **von "Bearbeiten"** 
> ![ Auswählen von "Bearbeiten"][ImageEdit]</span><span class="sxs-lookup"><span data-stu-id="efd4b-200">Selecting **Edit**
![Selecting Edit][ImageEdit]</span></span>  

1.  <span data-ttu-id="efd4b-201">Klicken Sie auf **Benutzerdefiniertes Gerät hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="efd4b-201">Click **Add custom device**.</span></span>  

1.  <span data-ttu-id="efd4b-202">Geben Sie einen Namen, eine Breite und eine Höhe für das Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="efd4b-202">Enter a name, width, and height for the device.</span></span>  <span data-ttu-id="efd4b-203">Die Felder für das [Pixel Verhältnis des Geräts][MDNWindowDevicePixelRatio], die [Zeichenfolge des Benutzer-Agents][MDNUserAgent]und die [Gerätetypen](#set-the-device-type) sind optional.</span><span class="sxs-lookup"><span data-stu-id="efd4b-203">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="efd4b-204">Das Feld "Gerätetyp" ist die Liste, die standardmäßig auf " **Mobiltelefon** " festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="efd4b-204">The device type field is the list that is set to **Mobile** by default.</span></span>  

> ##### <span data-ttu-id="efd4b-205">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="efd4b-205">Figure 12</span></span>  
> <span data-ttu-id="efd4b-206">Erstellen eines benutzerdefinierten Geräts</span><span class="sxs-lookup"><span data-stu-id="efd4b-206">Creating a custom device</span></span>  
> ![Erstellen eines benutzerdefinierten Geräts][ImageAddCustomDevice]  

### <span data-ttu-id="efd4b-208">Lineale anzeigen</span><span class="sxs-lookup"><span data-stu-id="efd4b-208">Show rulers</span></span>   

<span data-ttu-id="efd4b-209">Klicken Sie auf **Weitere Optionen** , und wählen Sie dann **Lineale anzeigen** aus, um die Lineale oberhalb und Links des Viewports anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="efd4b-209">Click **More options** and then select **Show rulers** to see rulers above and to the left of your viewport.</span></span>  <span data-ttu-id="efd4b-210">Die Größeneinheit der Lineale ist Pixel.</span><span class="sxs-lookup"><span data-stu-id="efd4b-210">The sizing unit of the rulers is pixels.</span></span>  

> ##### <span data-ttu-id="efd4b-211">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="efd4b-211">Figure 13</span></span>  
> <span data-ttu-id="efd4b-212">Lineale anzeigen</span><span class="sxs-lookup"><span data-stu-id="efd4b-212">Show rulers</span></span>  
> ![Lineale anzeigen][ImageShowRulers]  

> ##### <span data-ttu-id="efd4b-214">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="efd4b-214">Figure 14</span></span>  
> <span data-ttu-id="efd4b-215">Lineale oberhalb und Links des Viewports</span><span class="sxs-lookup"><span data-stu-id="efd4b-215">Rulers above and to the left of the viewport</span></span>  
> ![Lineale oberhalb und Links des Viewports][ImageRulers]  

### <span data-ttu-id="efd4b-217">Zoomen des Viewports</span><span class="sxs-lookup"><span data-stu-id="efd4b-217">Zoom the viewport</span></span>   

<span data-ttu-id="efd4b-218">Verwenden Sie die **zoomliste** , um die Ansicht zu vergrößern oder zu verkleinern.</span><span class="sxs-lookup"><span data-stu-id="efd4b-218">Use the **Zoom** list to zoom in or out.</span></span>  

> ##### <span data-ttu-id="efd4b-219">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="efd4b-219">Figure 15</span></span>  
> <span data-ttu-id="efd4b-220">Zoom</span><span class="sxs-lookup"><span data-stu-id="efd4b-220">Zoom</span></span>  
> ![Zoom][ImageZoomViewport]  

## <span data-ttu-id="efd4b-222">Netzwerk und CPU drosseln</span><span class="sxs-lookup"><span data-stu-id="efd4b-222">Throttle the network and CPU</span></span>   

<span data-ttu-id="efd4b-223">Wenn Sie das Netzwerk und die CPU Drosseln möchten, wählen Sie **Mid-Tier-Handy** oder **Low-End-Handy** aus der **Drosselungs** Liste aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-223">To throttle the network and CPU, select **Mid-tier mobile** or **Low-end mobile** from the **Throttle** list.</span></span>  

> ##### <span data-ttu-id="efd4b-224">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="efd4b-224">Figure 16</span></span>  
> <span data-ttu-id="efd4b-225">Die Drosselungs Liste</span><span class="sxs-lookup"><span data-stu-id="efd4b-225">The Throttle list</span></span>  
> ![Die Drosselungs Liste][ImageThrottling]  

<span data-ttu-id="efd4b-227">**Mid-Tier-Handy** simuliert schnelles 3G und drosselt Ihre CPU so, dass Sie viermal langsamer als normal ist.</span><span class="sxs-lookup"><span data-stu-id="efd4b-227">**Mid-tier mobile** simulates fast 3G and throttles your CPU so that it is 4 times slower than normal.</span></span>  <span data-ttu-id="efd4b-228">**Low-End-Mobile** simuliert langsames 3G und bremst Ihre CPU sechsmal langsamer als normal.</span><span class="sxs-lookup"><span data-stu-id="efd4b-228">**Low-end mobile** simulates slow 3G and throttles your CPU 6 times slower than normal.</span></span>  <span data-ttu-id="efd4b-229">Beachten Sie, dass die Drosselung relativ zur normalen Funktion Ihres Laptops oder Desktops ist.</span><span class="sxs-lookup"><span data-stu-id="efd4b-229">Keep in mind that the throttling is relative to the normal capability of your laptop or desktop.</span></span>  

> [!NOTE]
> <span data-ttu-id="efd4b-230">Die **Drosselungs** Liste wird ausgeblendet, wenn die **Gerätesymbolleiste** schmal ist.</span><span class="sxs-lookup"><span data-stu-id="efd4b-230">The **Throttle** list will be hidden if your **Device Toolbar** is narrow.</span></span>  

> ##### <span data-ttu-id="efd4b-231">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="efd4b-231">Figure 17</span></span>  
> <span data-ttu-id="efd4b-232">Die Gerätesymbolleiste</span><span class="sxs-lookup"><span data-stu-id="efd4b-232">The Device Toolbar</span></span>  
> ![Die Gerätesymbolleiste][ImageDeviceToolbar3]  

### <span data-ttu-id="efd4b-234">Nur die CPU drosseln</span><span class="sxs-lookup"><span data-stu-id="efd4b-234">Throttle the CPU only</span></span>   

<span data-ttu-id="efd4b-235">Wenn Sie nur die CPU und nicht das Netzwerk Drosseln möchten, wechseln Sie zum **Leistungs** Panel, klicken Sie auf Einstellungen für **Aufnahmeeinstellungen** ![ ][ImageCaptureIcon] , und wählen Sie dann in der Liste **CPU** die Option **4X Verlangsamung** oder **6x Verlangsamung** aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-235">To throttle the CPU only and not the network, go to the **Performance** panel, click **Capture Settings** ![Capture Settings][ImageCaptureIcon], and then select **4x slowdown** or **6x slowdown** from the **CPU** list.</span></span>  

> ##### <span data-ttu-id="efd4b-236">Abbildung 18</span><span class="sxs-lookup"><span data-stu-id="efd4b-236">Figure 18</span></span>  
> <span data-ttu-id="efd4b-237">Die CPU-Liste</span><span class="sxs-lookup"><span data-stu-id="efd4b-237">The CPU list</span></span>  
> ![Die CPU-Liste][ImageCPU]  

### <span data-ttu-id="efd4b-239">Nur das Netzwerk drosseln</span><span class="sxs-lookup"><span data-stu-id="efd4b-239">Throttle the network only</span></span>   

<span data-ttu-id="efd4b-240">Wenn Sie nur das Netzwerk und nicht die CPU Drosseln möchten, gehen Sie zum **Netzwerk** Panel, und wählen Sie **fast 3G** oder **Slow 3G** aus der **Drosselungs** Liste aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-240">To throttle the network only and not the CPU, go the **Network** panel and select **Fast 3G** or **Slow 3G** from the **Throttle** list.</span></span>  

> ##### <span data-ttu-id="efd4b-241">Abbildung 19</span><span class="sxs-lookup"><span data-stu-id="efd4b-241">Figure 19</span></span>  
> <span data-ttu-id="efd4b-242">Die Drosselungs Liste</span><span class="sxs-lookup"><span data-stu-id="efd4b-242">The Throttle list</span></span>  
> ![Die Drosselungs Liste][ImageNetwork]  

<span data-ttu-id="efd4b-244">Oder drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen, geben `3G` Sie ein, und wählen Sie **fast 3G-Drosselung aktivieren** oder **langsame 3G-Drosselung aktivieren**aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-244">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `3G`, and select **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  

> ##### <span data-ttu-id="efd4b-245">Abbildung 20</span><span class="sxs-lookup"><span data-stu-id="efd4b-245">Figure 20</span></span>  
> <span data-ttu-id="efd4b-246">Das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="efd4b-246">The Command Menu</span></span>  
> ![Das Befehlsmenü][ImageCommandMenu]  

<span data-ttu-id="efd4b-248">Sie können die Netzwerk Drosselung auch über das **Leistungs** Panel einstellen.</span><span class="sxs-lookup"><span data-stu-id="efd4b-248">You can also set network throttling from the **Performance** panel.</span></span>  <span data-ttu-id="efd4b-249">Klicken Sie auf **Aufnahme** Einstellungen aufzeichnen ![ ][ImageCaptureIcon] , und wählen Sie dann in der Liste **Netzwerk** die Option **fast 3G** oder **Slow 3G** aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-249">Click **Capture Settings** ![Capture Settings][ImageCaptureIcon] and then select **Fast 3G** or **Slow 3G** from the **Network** list.</span></span>  

> ##### <span data-ttu-id="efd4b-250">Abbildung 21</span><span class="sxs-lookup"><span data-stu-id="efd4b-250">Figure 21</span></span>  
> <span data-ttu-id="efd4b-251">Festlegen der Netzwerk Drosselung im Leistungs Panel</span><span class="sxs-lookup"><span data-stu-id="efd4b-251">Setting network throttling from the Performance panel</span></span>  
> ![Festlegen der Netzwerk Drosselung im Leistungs Panel][ImageNetwork2]  

## <span data-ttu-id="efd4b-253">Überschreiben von Geolocation</span><span class="sxs-lookup"><span data-stu-id="efd4b-253">Override geolocation</span></span>   

<span data-ttu-id="efd4b-254">Klicken Sie auf **anpassen und Steuern von devtools** , `...` und wählen Sie dann **Weitere Tools**-  >  **Sensoren**aus, um die Benutzeroberfläche für Geolocation zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="efd4b-254">To open the geolocation overriding UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  

> ##### <span data-ttu-id="efd4b-255">Abbildung 22</span><span class="sxs-lookup"><span data-stu-id="efd4b-255">Figure 22</span></span>  
> <span data-ttu-id="efd4b-256">Sensoren</span><span class="sxs-lookup"><span data-stu-id="efd4b-256">Sensors</span></span>  
> ![Sensoren][ImageSensors]  

<span data-ttu-id="efd4b-258">Oder drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Menübefehl zu öffnen, geben `Sensors` Sie ein, und wählen Sie dann **Sensoren anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-258">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

> ##### <span data-ttu-id="efd4b-259">Abbildung 23</span><span class="sxs-lookup"><span data-stu-id="efd4b-259">Figure 23</span></span>  
> <span data-ttu-id="efd4b-260">Sensoren anzeigen</span><span class="sxs-lookup"><span data-stu-id="efd4b-260">Show Sensors</span></span>  
> ![Sensoren anzeigen][ImageShowSensors]  

<span data-ttu-id="efd4b-262">Wählen Sie eine der Voreinstellungen aus der Liste **Geolocation** aus, oder wählen Sie **benutzerdefinierter Speicherort** aus, um Ihre eigenen Koordinaten einzugeben, oder wählen Sie **nicht verfügbarer Speicherort** aus, um zu testen, wie sich die Seite verhält, wenn sich die Geolokation in einem Fehlerzustand befindet.</span><span class="sxs-lookup"><span data-stu-id="efd4b-262">Select one of the presets from the **Geolocation** list, or select **Custom location** to enter your own coordinates, or select **Location unavailable** to test out how your page behaves when geolocation is in an error state.</span></span>  

> ##### <span data-ttu-id="efd4b-263">Abbildung 24</span><span class="sxs-lookup"><span data-stu-id="efd4b-263">Figure 24</span></span>  
> <span data-ttu-id="efd4b-264">Geolocation</span><span class="sxs-lookup"><span data-stu-id="efd4b-264">Geolocation</span></span>  
> ![Geolocation][ImageGeolocation]  

## <span data-ttu-id="efd4b-266">Ausrichtung einstellen</span><span class="sxs-lookup"><span data-stu-id="efd4b-266">Set orientation</span></span>   

<span data-ttu-id="efd4b-267">Klicken Sie zum Öffnen der UI für die Ausrichtung auf **anpassen und Steuern von devtools** `...` , und wählen Sie dann **Weitere Tools**-  >  **Sensoren**aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-267">To open the orientation UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  

> ##### <span data-ttu-id="efd4b-268">Abbildung 25</span><span class="sxs-lookup"><span data-stu-id="efd4b-268">Figure 25</span></span>  
> <span data-ttu-id="efd4b-269">Sensoren</span><span class="sxs-lookup"><span data-stu-id="efd4b-269">Sensors</span></span>  
> ![Sensoren][ImageSensors2]  

<span data-ttu-id="efd4b-271">Oder drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Menübefehl zu öffnen, geben `Sensors` Sie ein, und wählen Sie dann **Sensoren anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="efd4b-271">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

> ##### <span data-ttu-id="efd4b-272">Abbildung 26</span><span class="sxs-lookup"><span data-stu-id="efd4b-272">Figure 26</span></span>  
> <span data-ttu-id="efd4b-273">Sensoren anzeigen</span><span class="sxs-lookup"><span data-stu-id="efd4b-273">Show Sensors</span></span>  
> ![Sensoren anzeigen][ImageShowSensors2]  

<span data-ttu-id="efd4b-275">Wählen Sie eine der Voreinstellungen aus der **Ausrichtungs** Liste aus, oder wählen Sie **benutzerdefinierte Ausrichtung** aus, um Ihre eigenen Alpha-, Beta-und Gammawerte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="efd4b-275">Select one of the presets from the **Orientation** list or select **Custom orientation** to set your own alpha, beta, and gamma values.</span></span>  

> ##### <span data-ttu-id="efd4b-276">Abbildung 27</span><span class="sxs-lookup"><span data-stu-id="efd4b-276">Figure 27</span></span>  
> <span data-ttu-id="efd4b-277">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="efd4b-277">Orientation</span></span>  
> ![Ausrichtung][ImageOrientation]  

 



<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageCustomizeIcon]: /microsoft-edge/devtools-guide-chromium/media/customize-and-control-devtools-icon.msft.png  
[ImageDeviceToolbarIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-dark-icon.msft.png  

[ImageDeviceToolbar]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Abbildung 1: die Gerätesymbolleiste"  
[ImageResponsiveHandles]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png "Abbildung 2: die Ziehpunkte zum Ändern der Bemaßungen des Viewports im reaktionsfähigen Ansichtsfenster Modus"  
[ImageShowMediaQueries]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png "Abbildung 3: Anzeigen von medienabfragen"  
[ImageBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png "Abbildung 4: Klicken Sie auf einen Haltepunkt, um die Breite des Viewports zu ändern."  
[ImageDeviceType]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-type-list.msft.png "Abbildung 5: Gerätetypen Liste"  
[ImageDeviceList]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list.msft.png "Abbildung 6: Geräteliste"  
[ImageLandscape]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-landscape.msft.png "Abbildung 7: Querformat"  
[ImageDeviceToolbar2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Abbildung 8: die Gerätesymbolleiste"  
[ImageShowDeviceFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png "Abbildung 9: Anzeigen des geräterahmens"  
[ImageIphoneFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png "Abbildung 10: der Geräterahmen für das iPhone 6"  
[ImageEdit]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list-edit.msft.png "Abbildung 11: Auswählen von "Bearbeiten""  
[ImageAddCustomDevice]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png "Abbildung 12: Erstellen eines benutzerdefinierten Geräts"  
[ImageShowRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png "Abbildung 13: Anzeigen der Lineale"  
[ImageRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-rulers.msft.png "Abbildung 14: Lineale oberhalb und Links vom Viewport"  
[ImageZoomViewport]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-zoom.msft.png "Abbildung 15: Zoom"  
[ImageThrottling]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-throttle.msft.png "Abbildung 16: die Drosselungs Liste"  
[ImageDeviceToolbar3]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Abbildung 17: die Gerätesymbolleiste"  
[ImageCPU]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-cpu-throttle.msft.png "Abbildung 18: die CPU-Liste"  
[ImageNetwork]: /microsoft-edge/devtools-guide-chromium/media/device-mode-network-throttle.msft.png "Abbildung 19: die Drosselungs Liste"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-command-menu-throttle.msft.png "Abbildung 20: Befehlsmenü"  
[ImageNetwork2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-network-throttle.msft.png "Abbildung 21: Festlegen der Netzwerk Drosselung im Leistungs Panel"  
[ImageSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Abbildung 22: Sensoren"  
[ImageShowSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Abbildung 23: Anzeigen von Sensoren"  
[ImageGeolocation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png "Abbildung 24: Geolocation"  
[ImageSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Abbildung 25: Sensoren"  
[ImageShowSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Abbildung 26: Anzeigen von Sensoren"  
[ImageOrientation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png "Abbildung 27: Ausrichtung"  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community"  -->
[DevToolsRemoteDebugging]:/Microsoft-Edge/devtools-Guide-Chromium/Remote-Debugging/Index "erste Schritte mit dem Remotedebuggen von Android-Geräten"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Benutzer-Agent | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Reihenfolge der Näherung – First-Order – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="efd4b-310">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efd4b-310">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="efd4b-311">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="efd4b-311">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="efd4b-313">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="efd4b-313">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

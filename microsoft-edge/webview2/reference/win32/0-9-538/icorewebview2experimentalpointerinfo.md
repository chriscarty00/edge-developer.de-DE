---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ef0546c03e2d2ccc87677125772b1663f2ec6362
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698879"
---
# <span data-ttu-id="d7215-104">Schnittstellen ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="d7215-104">interface ICoreWebView2ExperimentalPointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="d7215-105">Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.538 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="d7215-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="d7215-106">Dies stellt in erster Linie ein kombiniertes Win32-POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="d7215-106">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="d7215-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d7215-107">Summary</span></span>

 <span data-ttu-id="d7215-108">Member</span><span class="sxs-lookup"><span data-stu-id="d7215-108">Members</span></span>                        | <span data-ttu-id="d7215-109">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d7215-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d7215-110">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="d7215-110">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="d7215-111">Rufen Sie die ButtonChangeKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-111">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="d7215-112">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="d7215-112">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="d7215-113">Rufen Sie die DisplayRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-113">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="d7215-114">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="d7215-114">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="d7215-115">Rufen Sie die Frame-Nr des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-115">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="d7215-116">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="d7215-116">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="d7215-117">Rufen Sie die HimetricLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-117">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="d7215-118">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="d7215-118">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="d7215-119">Rufen Sie die HimetricLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-119">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="d7215-120">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="d7215-120">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="d7215-121">Rufen Sie die HistoryCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-121">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="d7215-122">get_InputData</span><span class="sxs-lookup"><span data-stu-id="d7215-122">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="d7215-123">Rufen Sie die inputData des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-123">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="d7215-124">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="d7215-124">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="d7215-125">Rufen Sie die KeyStates des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-125">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="d7215-126">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="d7215-126">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="d7215-127">Rufen Sie die PenFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-127">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="d7215-128">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="d7215-128">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="d7215-129">Rufen Sie die PenMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-129">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="d7215-130">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="d7215-130">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="d7215-131">Rufen Sie die PenPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-131">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="d7215-132">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="d7215-132">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="d7215-133">Rufen Sie die PenRotation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-133">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="d7215-134">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="d7215-134">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="d7215-135">Rufen Sie die PenTiltX des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-135">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="d7215-136">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="d7215-136">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="d7215-137">Rufen Sie die PenTiltY des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-137">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="d7215-138">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="d7215-138">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="d7215-139">Rufen Sie die PerformanceCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-139">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="d7215-140">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="d7215-140">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="d7215-141">Rufen Sie die PixelLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-141">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="d7215-142">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="d7215-142">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="d7215-143">Rufen Sie die PixelLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-143">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="d7215-144">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="d7215-144">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="d7215-145">Rufen Sie die PointerDeviceRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-145">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="d7215-146">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="d7215-146">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="d7215-147">Rufen Sie die PointerFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-147">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="d7215-148">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="d7215-148">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="d7215-149">Rufen Sie die Zeiger-Nr. des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-149">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="d7215-150">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="d7215-150">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="d7215-151">Rufen Sie die PointerKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-151">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="d7215-152">get_Time</span><span class="sxs-lookup"><span data-stu-id="d7215-152">get_Time</span></span>](#get_time) | <span data-ttu-id="d7215-153">Rufen Sie die Uhrzeit des Zeiger Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-153">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="d7215-154">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="d7215-154">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="d7215-155">Rufen Sie die TouchContact des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-155">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="d7215-156">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="d7215-156">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="d7215-157">Rufen Sie die TouchContactRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-157">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="d7215-158">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="d7215-158">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="d7215-159">Rufen Sie die TouchFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-159">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="d7215-160">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="d7215-160">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="d7215-161">Rufen Sie die TouchMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-161">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="d7215-162">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="d7215-162">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="d7215-163">Rufen Sie die TouchOrientation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-163">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="d7215-164">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="d7215-164">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="d7215-165">Rufen Sie die TouchPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-165">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="d7215-166">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="d7215-166">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="d7215-167">Legt die ButtonChangeKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-167">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="d7215-168">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="d7215-168">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="d7215-169">Setzen Sie die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-169">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="d7215-170">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="d7215-170">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="d7215-171">Legt die Frame-Nr des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-171">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="d7215-172">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="d7215-172">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="d7215-173">Legt die HimetricLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-173">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="d7215-174">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="d7215-174">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="d7215-175">Legt die HimetricLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-175">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="d7215-176">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="d7215-176">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="d7215-177">Legt die HistoryCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-177">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="d7215-178">put_InputData</span><span class="sxs-lookup"><span data-stu-id="d7215-178">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="d7215-179">Legt die inputData des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-179">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="d7215-180">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="d7215-180">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="d7215-181">Die KeyStates des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d7215-181">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="d7215-182">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="d7215-182">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="d7215-183">Legt die PenFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-183">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="d7215-184">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="d7215-184">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="d7215-185">Legt die PenMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-185">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="d7215-186">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="d7215-186">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="d7215-187">Legt die PenPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-187">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="d7215-188">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="d7215-188">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="d7215-189">Legt die PenRotation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-189">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="d7215-190">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="d7215-190">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="d7215-191">Legt die PenTiltX des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-191">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="d7215-192">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="d7215-192">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="d7215-193">Legt die PenTiltY des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-193">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="d7215-194">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="d7215-194">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="d7215-195">Legt die PerformanceCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-195">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="d7215-196">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="d7215-196">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="d7215-197">Legt die PixelLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-197">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="d7215-198">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="d7215-198">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="d7215-199">Legt die PixelLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-199">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="d7215-200">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="d7215-200">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="d7215-201">Setzen Sie die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-201">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="d7215-202">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="d7215-202">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="d7215-203">Legt die PointerFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-203">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="d7215-204">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="d7215-204">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="d7215-205">Die Zeiger-Nr. des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d7215-205">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="d7215-206">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="d7215-206">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="d7215-207">Legt die PointerKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-207">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="d7215-208">put_Time</span><span class="sxs-lookup"><span data-stu-id="d7215-208">put_Time</span></span>](#put_time) | <span data-ttu-id="d7215-209">Legt die Uhrzeit des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-209">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="d7215-210">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="d7215-210">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="d7215-211">Legt die TouchContact des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-211">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="d7215-212">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="d7215-212">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="d7215-213">Legt die TouchContactRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-213">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="d7215-214">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="d7215-214">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="d7215-215">Legt die TouchFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-215">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="d7215-216">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="d7215-216">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="d7215-217">Legt die TouchMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-217">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="d7215-218">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="d7215-218">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="d7215-219">Legt die TouchOrientation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-219">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="d7215-220">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="d7215-220">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="d7215-221">Legt die TouchPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-221">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="d7215-222">Sie nimmt Felder aus allen dreien auf und schließt einige Win32-spezifische Datentypen wie HWND und handle aus.</span><span class="sxs-lookup"><span data-stu-id="d7215-222">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="d7215-223">Beachten Sie, dass sourceDevice herausgenommen wird, aber wir erwarten, dass PointerDeviceRect und DisplayRect die vorhandenen Anwendungsfälle von sourceDevice abdecken.</span><span class="sxs-lookup"><span data-stu-id="d7215-223">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="d7215-224">Ein weiterer großer Unterschied besteht darin, dass eine der Punkt-oder Rect-Positionen in WebView-physikalischen Koordinaten erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="d7215-224">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="d7215-225">Das heißt, Koordinaten relativ zum WebView und keine DPI-Skalierung angewendet.</span><span class="sxs-lookup"><span data-stu-id="d7215-225">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="d7215-226">Member</span><span class="sxs-lookup"><span data-stu-id="d7215-226">Members</span></span>

#### <span data-ttu-id="d7215-227">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="d7215-227">get_ButtonChangeKind</span></span> 

<span data-ttu-id="d7215-228">Rufen Sie die ButtonChangeKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-228">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="d7215-229">Public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(Int32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="d7215-229">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="d7215-230">Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-230">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="d7215-231">Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-231">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-232">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="d7215-232">get_DisplayRect</span></span> 

<span data-ttu-id="d7215-233">Rufen Sie die DisplayRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-233">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="d7215-234">Public HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="d7215-234">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="d7215-235">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="d7215-235">get_FrameId</span></span> 

<span data-ttu-id="d7215-236">Rufen Sie die Frame-Nr des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-236">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="d7215-237">Public HRESULT [get_FrameId](#get_frameid)(UInt32 \* Frame-Nr)</span><span class="sxs-lookup"><span data-stu-id="d7215-237">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="d7215-238">Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-238">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-239">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="d7215-239">get_HimetricLocation</span></span> 

<span data-ttu-id="d7215-240">Rufen Sie die HimetricLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-240">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="d7215-241">öffentliche HRESULT- [get_HimetricLocation](#get_himetriclocation)(Point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="d7215-241">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="d7215-242">Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-242">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-243">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="d7215-243">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="d7215-244">Rufen Sie die HimetricLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-244">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="d7215-245">öffentliche HRESULT- [get_HimetricLocationRaw](#get_himetriclocationraw)(Point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="d7215-245">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="d7215-246">Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-246">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-247">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="d7215-247">get_HistoryCount</span></span> 

<span data-ttu-id="d7215-248">Rufen Sie die HistoryCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-248">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="d7215-249">Public HRESULT [get_HistoryCount](#get_historycount)(UInt32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="d7215-249">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="d7215-250">Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-250">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-251">get_InputData</span><span class="sxs-lookup"><span data-stu-id="d7215-251">get_InputData</span></span> 

<span data-ttu-id="d7215-252">Rufen Sie die inputData des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-252">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="d7215-253">Public HRESULT [get_InputData](#get_inputdata)(Int32 \* inputData)</span><span class="sxs-lookup"><span data-stu-id="d7215-253">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="d7215-254">Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-254">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-255">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="d7215-255">get_KeyStates</span></span> 

<span data-ttu-id="d7215-256">Rufen Sie die KeyStates des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-256">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="d7215-257">öffentliche HRESULT- [get_KeyStates](#get_keystates)(DWORD \*-KeyStates)</span><span class="sxs-lookup"><span data-stu-id="d7215-257">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="d7215-258">Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-258">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-259">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="d7215-259">get_PenFlags</span></span> 

<span data-ttu-id="d7215-260">Rufen Sie die PenFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-260">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="d7215-261">Public HRESULT [get_PenFlags](#get_penflags)(UInt32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="d7215-261">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="d7215-262">Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-262">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="d7215-263">Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-263">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-264">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="d7215-264">get_PenMask</span></span> 

<span data-ttu-id="d7215-265">Rufen Sie die PenMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-265">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="d7215-266">Public HRESULT [get_PenMask](#get_penmask)(UInt32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="d7215-266">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="d7215-267">Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-267">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="d7215-268">Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-268">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-269">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="d7215-269">get_PenPressure</span></span> 

<span data-ttu-id="d7215-270">Rufen Sie die PenPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-270">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="d7215-271">Public HRESULT [get_PenPressure](#get_penpressure)(UInt32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="d7215-271">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="d7215-272">Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-272">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-273">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="d7215-273">get_PenRotation</span></span> 

<span data-ttu-id="d7215-274">Rufen Sie die PenRotation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-274">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="d7215-275">Public HRESULT [get_PenRotation](#get_penrotation)(UInt32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="d7215-275">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="d7215-276">Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-276">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-277">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="d7215-277">get_PenTiltX</span></span> 

<span data-ttu-id="d7215-278">Rufen Sie die PenTiltX des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-278">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="d7215-279">Public HRESULT [get_PenTiltX](#get_pentiltx)(Int32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="d7215-279">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="d7215-280">Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-280">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-281">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="d7215-281">get_PenTiltY</span></span> 

<span data-ttu-id="d7215-282">Rufen Sie die PenTiltY des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-282">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="d7215-283">Public HRESULT [get_PenTiltY](#get_pentilty)(Int32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="d7215-283">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="d7215-284">Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-284">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-285">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="d7215-285">get_PerformanceCount</span></span> 

<span data-ttu-id="d7215-286">Rufen Sie die PerformanceCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-286">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="d7215-287">Public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="d7215-287">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="d7215-288">Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-288">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-289">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="d7215-289">get_PixelLocation</span></span> 

<span data-ttu-id="d7215-290">Rufen Sie die PixelLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-290">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="d7215-291">öffentliche HRESULT- [get_PixelLocation](#get_pixellocation)(Point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="d7215-291">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="d7215-292">Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-292">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-293">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="d7215-293">get_PixelLocationRaw</span></span> 

<span data-ttu-id="d7215-294">Rufen Sie die PixelLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-294">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="d7215-295">öffentliche HRESULT- [get_PixelLocationRaw](#get_pixellocationraw)(Point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="d7215-295">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="d7215-296">Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-296">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-297">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="d7215-297">get_PointerDeviceRect</span></span> 

<span data-ttu-id="d7215-298">Rufen Sie die PointerDeviceRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-298">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="d7215-299">Public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="d7215-299">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="d7215-300">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="d7215-300">get_PointerFlags</span></span> 

<span data-ttu-id="d7215-301">Rufen Sie die PointerFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-301">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="d7215-302">Public HRESULT [get_PointerFlags](#get_pointerflags)(UInt32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="d7215-302">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="d7215-303">Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-303">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="d7215-304">Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-304">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-305">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="d7215-305">get_PointerId</span></span> 

<span data-ttu-id="d7215-306">Rufen Sie die Zeiger-Nr. des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-306">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="d7215-307">öffentliche HRESULT- [get_PointerId](#get_pointerid)(UInt32 \* Pointer-Nr.)</span><span class="sxs-lookup"><span data-stu-id="d7215-307">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="d7215-308">Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-308">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-309">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="d7215-309">get_PointerKind</span></span> 

<span data-ttu-id="d7215-310">Rufen Sie die PointerKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-310">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="d7215-311">Public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="d7215-311">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="d7215-312">Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-312">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="d7215-313">Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-313">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="d7215-314">Unterstützt PT_PEN und PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="d7215-314">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="d7215-315">get_Time</span><span class="sxs-lookup"><span data-stu-id="d7215-315">get_Time</span></span> 

<span data-ttu-id="d7215-316">Rufen Sie die Uhrzeit des Zeiger Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-316">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="d7215-317">öffentliche HRESULT- [get_Time](#get_time)(DWORD \* Zeit)</span><span class="sxs-lookup"><span data-stu-id="d7215-317">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="d7215-318">Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-318">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-319">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="d7215-319">get_TouchContact</span></span> 

<span data-ttu-id="d7215-320">Rufen Sie die TouchContact des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-320">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="d7215-321">Public HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="d7215-321">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="d7215-322">Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-322">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-323">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="d7215-323">get_TouchContactRaw</span></span> 

<span data-ttu-id="d7215-324">Rufen Sie die TouchContactRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-324">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="d7215-325">Public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="d7215-325">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="d7215-326">Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-326">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-327">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="d7215-327">get_TouchFlags</span></span> 

<span data-ttu-id="d7215-328">Rufen Sie die TouchFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-328">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="d7215-329">Public HRESULT [get_TouchFlags](#get_touchflags)(UInt32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="d7215-329">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="d7215-330">Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-330">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="d7215-331">Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-331">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-332">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="d7215-332">get_TouchMask</span></span> 

<span data-ttu-id="d7215-333">Rufen Sie die TouchMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-333">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="d7215-334">Public HRESULT [get_TouchMask](#get_touchmask)(UInt32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="d7215-334">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="d7215-335">Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-335">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="d7215-336">Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-336">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-337">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="d7215-337">get_TouchOrientation</span></span> 

<span data-ttu-id="d7215-338">Rufen Sie die TouchOrientation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-338">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="d7215-339">Public HRESULT [get_TouchOrientation](#get_touchorientation)(UInt32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="d7215-339">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="d7215-340">Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-340">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-341">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="d7215-341">get_TouchPressure</span></span> 

<span data-ttu-id="d7215-342">Rufen Sie die TouchPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="d7215-342">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="d7215-343">Public HRESULT [get_TouchPressure](#get_touchpressure)(UInt32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="d7215-343">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="d7215-344">Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-344">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-345">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="d7215-345">put_ButtonChangeKind</span></span> 

<span data-ttu-id="d7215-346">Legt die ButtonChangeKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-346">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="d7215-347">Public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(Int32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="d7215-347">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="d7215-348">Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-348">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="d7215-349">Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-349">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-350">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="d7215-350">put_DisplayRect</span></span> 

<span data-ttu-id="d7215-351">Setzen Sie die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-351">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="d7215-352">Public HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="d7215-352">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="d7215-353">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="d7215-353">put_FrameId</span></span> 

<span data-ttu-id="d7215-354">Legt die Frame-Nr des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-354">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="d7215-355">Public HRESULT [put_FrameId](#put_frameid)(UInt32-Frame-Nr)</span><span class="sxs-lookup"><span data-stu-id="d7215-355">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="d7215-356">Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-356">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-357">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="d7215-357">put_HimetricLocation</span></span> 

<span data-ttu-id="d7215-358">Legt die HimetricLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-358">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="d7215-359">öffentliche HRESULT- [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="d7215-359">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="d7215-360">Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-360">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-361">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="d7215-361">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="d7215-362">Legt die HimetricLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-362">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="d7215-363">öffentliche HRESULT- [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="d7215-363">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="d7215-364">Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-364">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-365">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="d7215-365">put_HistoryCount</span></span> 

<span data-ttu-id="d7215-366">Legt die HistoryCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-366">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="d7215-367">Public HRESULT [put_HistoryCount](#put_historycount)(UInt32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="d7215-367">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="d7215-368">Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-368">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-369">put_InputData</span><span class="sxs-lookup"><span data-stu-id="d7215-369">put_InputData</span></span> 

<span data-ttu-id="d7215-370">Legt die inputData des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-370">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="d7215-371">Public HRESULT [put_InputData](#put_inputdata)(Int32 inputData)</span><span class="sxs-lookup"><span data-stu-id="d7215-371">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="d7215-372">Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-372">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-373">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="d7215-373">put_KeyStates</span></span> 

<span data-ttu-id="d7215-374">Die KeyStates des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d7215-374">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="d7215-375">Public HRESULT [put_KeyStates](#put_keystates)(DWORD-KeyStates)</span><span class="sxs-lookup"><span data-stu-id="d7215-375">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="d7215-376">Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-376">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-377">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="d7215-377">put_PenFlags</span></span> 

<span data-ttu-id="d7215-378">Legt die PenFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-378">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="d7215-379">Public HRESULT [put_PenFlags](#put_penflags)(UInt32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="d7215-379">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="d7215-380">Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-380">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="d7215-381">Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-381">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-382">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="d7215-382">put_PenMask</span></span> 

<span data-ttu-id="d7215-383">Legt die PenMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-383">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="d7215-384">Public HRESULT [put_PenMask](#put_penmask)(UInt32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="d7215-384">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="d7215-385">Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-385">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="d7215-386">Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-386">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-387">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="d7215-387">put_PenPressure</span></span> 

<span data-ttu-id="d7215-388">Legt die PenPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-388">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="d7215-389">Public HRESULT [put_PenPressure](#put_penpressure)(UInt32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="d7215-389">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="d7215-390">Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-390">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-391">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="d7215-391">put_PenRotation</span></span> 

<span data-ttu-id="d7215-392">Legt die PenRotation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-392">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="d7215-393">Public HRESULT [put_PenRotation](#put_penrotation)(UInt32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="d7215-393">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="d7215-394">Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-394">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-395">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="d7215-395">put_PenTiltX</span></span> 

<span data-ttu-id="d7215-396">Legt die PenTiltX des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-396">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="d7215-397">Public HRESULT [put_PenTiltX](#put_pentiltx)(Int32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="d7215-397">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="d7215-398">Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-398">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-399">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="d7215-399">put_PenTiltY</span></span> 

<span data-ttu-id="d7215-400">Legt die PenTiltY des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-400">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="d7215-401">Public HRESULT [put_PenTiltY](#put_pentilty)(Int32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="d7215-401">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="d7215-402">Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-402">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-403">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="d7215-403">put_PerformanceCount</span></span> 

<span data-ttu-id="d7215-404">Legt die PerformanceCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-404">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="d7215-405">Public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="d7215-405">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="d7215-406">Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-406">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-407">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="d7215-407">put_PixelLocation</span></span> 

<span data-ttu-id="d7215-408">Legt die PixelLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-408">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="d7215-409">öffentliche HRESULT- [put_PixelLocation](#put_pixellocation)(Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="d7215-409">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="d7215-410">Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-410">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-411">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="d7215-411">put_PixelLocationRaw</span></span> 

<span data-ttu-id="d7215-412">Legt die PixelLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-412">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="d7215-413">öffentliche HRESULT- [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="d7215-413">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="d7215-414">Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-414">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-415">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="d7215-415">put_PointerDeviceRect</span></span> 

<span data-ttu-id="d7215-416">Setzen Sie die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-416">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="d7215-417">Public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="d7215-417">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="d7215-418">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="d7215-418">put_PointerFlags</span></span> 

<span data-ttu-id="d7215-419">Legt die PointerFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-419">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="d7215-420">Public HRESULT [put_PointerFlags](#put_pointerflags)(UInt32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="d7215-420">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="d7215-421">Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-421">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="d7215-422">Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-422">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-423">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="d7215-423">put_PointerId</span></span> 

<span data-ttu-id="d7215-424">Die Zeiger-Nr. des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d7215-424">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="d7215-425">Public HRESULT [put_PointerId](#put_pointerid)(UInt32-Zeiger-Nr.)</span><span class="sxs-lookup"><span data-stu-id="d7215-425">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="d7215-426">Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-426">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-427">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="d7215-427">put_PointerKind</span></span> 

<span data-ttu-id="d7215-428">Legt die PointerKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-428">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="d7215-429">Public HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="d7215-429">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="d7215-430">Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-430">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="d7215-431">Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-431">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="d7215-432">Unterstützt PT_PEN und PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="d7215-432">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="d7215-433">put_Time</span><span class="sxs-lookup"><span data-stu-id="d7215-433">put_Time</span></span> 

<span data-ttu-id="d7215-434">Legt die Uhrzeit des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-434">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="d7215-435">Public HRESULT [put_Time](#put_time)(DWORD-Zeit)</span><span class="sxs-lookup"><span data-stu-id="d7215-435">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="d7215-436">Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-436">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-437">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="d7215-437">put_TouchContact</span></span> 

<span data-ttu-id="d7215-438">Legt die TouchContact des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-438">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="d7215-439">Public HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="d7215-439">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="d7215-440">Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-440">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-441">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="d7215-441">put_TouchContactRaw</span></span> 

<span data-ttu-id="d7215-442">Legt die TouchContactRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-442">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="d7215-443">Public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="d7215-443">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="d7215-444">Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-444">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-445">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="d7215-445">put_TouchFlags</span></span> 

<span data-ttu-id="d7215-446">Legt die TouchFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-446">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="d7215-447">Public HRESULT [put_TouchFlags](#put_touchflags)(UInt32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="d7215-447">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="d7215-448">Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-448">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="d7215-449">Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-449">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-450">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="d7215-450">put_TouchMask</span></span> 

<span data-ttu-id="d7215-451">Legt die TouchMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-451">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="d7215-452">Public HRESULT [put_TouchMask](#put_touchmask)(UInt32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="d7215-452">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="d7215-453">Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7215-453">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="d7215-454">Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="d7215-454">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-455">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="d7215-455">put_TouchOrientation</span></span> 

<span data-ttu-id="d7215-456">Legt die TouchOrientation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-456">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="d7215-457">Public HRESULT [put_TouchOrientation](#put_touchorientation)(UInt32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="d7215-457">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="d7215-458">Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-458">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="d7215-459">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="d7215-459">put_TouchPressure</span></span> 

<span data-ttu-id="d7215-460">Legt die TouchPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="d7215-460">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="d7215-461">Public HRESULT [put_TouchPressure](#put_touchpressure)(UInt32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="d7215-461">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="d7215-462">Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="d7215-462">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 2141dff54b44fe6d9a2758f571e61b81877079da
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653941"
---
# <span data-ttu-id="56c7c-104">Schnittstellen ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="56c7c-104">interface ICoreWebView2ExperimentalPointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="56c7c-105">Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.488 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="56c7c-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="56c7c-106">Dies stellt in erster Linie ein kombiniertes Win32-POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="56c7c-106">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="56c7c-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="56c7c-107">Summary</span></span>

 <span data-ttu-id="56c7c-108">Member</span><span class="sxs-lookup"><span data-stu-id="56c7c-108">Members</span></span>                        | <span data-ttu-id="56c7c-109">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="56c7c-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="56c7c-110">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="56c7c-110">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="56c7c-111">Rufen Sie die ButtonChangeKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-111">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="56c7c-112">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="56c7c-112">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="56c7c-113">Rufen Sie die DisplayRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-113">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="56c7c-114">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="56c7c-114">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="56c7c-115">Rufen Sie die Frame-Nr des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-115">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="56c7c-116">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="56c7c-116">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="56c7c-117">Rufen Sie die HimetricLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-117">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="56c7c-118">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="56c7c-118">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="56c7c-119">Rufen Sie die HimetricLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-119">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="56c7c-120">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="56c7c-120">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="56c7c-121">Rufen Sie die HistoryCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-121">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="56c7c-122">get_InputData</span><span class="sxs-lookup"><span data-stu-id="56c7c-122">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="56c7c-123">Rufen Sie die inputData des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-123">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="56c7c-124">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="56c7c-124">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="56c7c-125">Rufen Sie die KeyStates des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-125">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="56c7c-126">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="56c7c-126">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="56c7c-127">Rufen Sie die PenFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-127">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="56c7c-128">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="56c7c-128">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="56c7c-129">Rufen Sie die PenMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-129">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="56c7c-130">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="56c7c-130">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="56c7c-131">Rufen Sie die PenPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-131">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="56c7c-132">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="56c7c-132">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="56c7c-133">Rufen Sie die PenRotation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-133">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="56c7c-134">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="56c7c-134">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="56c7c-135">Rufen Sie die PenTiltX des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-135">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="56c7c-136">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="56c7c-136">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="56c7c-137">Rufen Sie die PenTiltY des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-137">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="56c7c-138">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="56c7c-138">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="56c7c-139">Rufen Sie die PerformanceCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-139">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="56c7c-140">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="56c7c-140">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="56c7c-141">Rufen Sie die PixelLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-141">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="56c7c-142">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="56c7c-142">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="56c7c-143">Rufen Sie die PixelLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-143">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="56c7c-144">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="56c7c-144">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="56c7c-145">Rufen Sie die PointerDeviceRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-145">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="56c7c-146">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="56c7c-146">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="56c7c-147">Rufen Sie die PointerFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-147">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="56c7c-148">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="56c7c-148">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="56c7c-149">Rufen Sie die Zeiger-Nr. des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-149">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="56c7c-150">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="56c7c-150">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="56c7c-151">Rufen Sie die PointerKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-151">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="56c7c-152">get_Time</span><span class="sxs-lookup"><span data-stu-id="56c7c-152">get_Time</span></span>](#get_time) | <span data-ttu-id="56c7c-153">Rufen Sie die Uhrzeit des Zeiger Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-153">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="56c7c-154">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="56c7c-154">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="56c7c-155">Rufen Sie die TouchContact des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-155">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="56c7c-156">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="56c7c-156">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="56c7c-157">Rufen Sie die TouchContactRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-157">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="56c7c-158">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="56c7c-158">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="56c7c-159">Rufen Sie die TouchFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-159">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="56c7c-160">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="56c7c-160">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="56c7c-161">Rufen Sie die TouchMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-161">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="56c7c-162">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="56c7c-162">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="56c7c-163">Rufen Sie die TouchOrientation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-163">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="56c7c-164">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="56c7c-164">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="56c7c-165">Rufen Sie die TouchPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-165">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="56c7c-166">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="56c7c-166">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="56c7c-167">Legt die ButtonChangeKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-167">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="56c7c-168">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="56c7c-168">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="56c7c-169">Setzen Sie die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-169">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="56c7c-170">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="56c7c-170">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="56c7c-171">Legt die Frame-Nr des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-171">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="56c7c-172">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="56c7c-172">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="56c7c-173">Legt die HimetricLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-173">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="56c7c-174">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="56c7c-174">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="56c7c-175">Legt die HimetricLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-175">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="56c7c-176">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="56c7c-176">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="56c7c-177">Legt die HistoryCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-177">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="56c7c-178">put_InputData</span><span class="sxs-lookup"><span data-stu-id="56c7c-178">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="56c7c-179">Legt die inputData des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-179">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="56c7c-180">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="56c7c-180">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="56c7c-181">Die KeyStates des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="56c7c-181">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="56c7c-182">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="56c7c-182">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="56c7c-183">Legt die PenFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-183">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="56c7c-184">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="56c7c-184">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="56c7c-185">Legt die PenMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-185">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="56c7c-186">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="56c7c-186">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="56c7c-187">Legt die PenPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-187">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="56c7c-188">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="56c7c-188">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="56c7c-189">Legt die PenRotation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-189">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="56c7c-190">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="56c7c-190">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="56c7c-191">Legt die PenTiltX des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-191">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="56c7c-192">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="56c7c-192">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="56c7c-193">Legt die PenTiltY des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-193">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="56c7c-194">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="56c7c-194">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="56c7c-195">Legt die PerformanceCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-195">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="56c7c-196">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="56c7c-196">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="56c7c-197">Legt die PixelLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-197">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="56c7c-198">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="56c7c-198">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="56c7c-199">Legt die PixelLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-199">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="56c7c-200">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="56c7c-200">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="56c7c-201">Setzen Sie die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-201">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="56c7c-202">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="56c7c-202">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="56c7c-203">Legt die PointerFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-203">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="56c7c-204">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="56c7c-204">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="56c7c-205">Die Zeiger-Nr. des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="56c7c-205">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="56c7c-206">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="56c7c-206">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="56c7c-207">Legt die PointerKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-207">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="56c7c-208">put_Time</span><span class="sxs-lookup"><span data-stu-id="56c7c-208">put_Time</span></span>](#put_time) | <span data-ttu-id="56c7c-209">Legt die Uhrzeit des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-209">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="56c7c-210">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="56c7c-210">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="56c7c-211">Legt die TouchContact des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-211">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="56c7c-212">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="56c7c-212">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="56c7c-213">Legt die TouchContactRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-213">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="56c7c-214">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="56c7c-214">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="56c7c-215">Legt die TouchFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-215">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="56c7c-216">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="56c7c-216">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="56c7c-217">Legt die TouchMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-217">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="56c7c-218">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="56c7c-218">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="56c7c-219">Legt die TouchOrientation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-219">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="56c7c-220">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="56c7c-220">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="56c7c-221">Legt die TouchPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-221">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="56c7c-222">Sie nimmt Felder aus allen dreien auf und schließt einige Win32-spezifische Datentypen wie HWND und handle aus.</span><span class="sxs-lookup"><span data-stu-id="56c7c-222">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="56c7c-223">Beachten Sie, dass sourceDevice herausgenommen wird, aber wir erwarten, dass PointerDeviceRect und DisplayRect die vorhandenen Anwendungsfälle von sourceDevice abdecken.</span><span class="sxs-lookup"><span data-stu-id="56c7c-223">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="56c7c-224">Ein weiterer großer Unterschied besteht darin, dass eine der Punkt-oder Rect-Positionen in WebView-physikalischen Koordinaten erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="56c7c-224">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="56c7c-225">Das heißt, Koordinaten relativ zum WebView und keine DPI-Skalierung angewendet.</span><span class="sxs-lookup"><span data-stu-id="56c7c-225">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="56c7c-226">Member</span><span class="sxs-lookup"><span data-stu-id="56c7c-226">Members</span></span>

#### <span data-ttu-id="56c7c-227">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="56c7c-227">get_ButtonChangeKind</span></span> 

<span data-ttu-id="56c7c-228">Rufen Sie die ButtonChangeKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-228">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="56c7c-229">Public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(Int32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="56c7c-229">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="56c7c-230">Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-230">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="56c7c-231">Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-231">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-232">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="56c7c-232">get_DisplayRect</span></span> 

<span data-ttu-id="56c7c-233">Rufen Sie die DisplayRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-233">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="56c7c-234">Public HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="56c7c-234">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="56c7c-235">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="56c7c-235">get_FrameId</span></span> 

<span data-ttu-id="56c7c-236">Rufen Sie die Frame-Nr des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-236">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="56c7c-237">Public HRESULT [get_FrameId](#get_frameid)(UInt32 \* Frame-Nr)</span><span class="sxs-lookup"><span data-stu-id="56c7c-237">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="56c7c-238">Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-238">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-239">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="56c7c-239">get_HimetricLocation</span></span> 

<span data-ttu-id="56c7c-240">Rufen Sie die HimetricLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-240">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="56c7c-241">öffentliche HRESULT- [get_HimetricLocation](#get_himetriclocation)(Point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="56c7c-241">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="56c7c-242">Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-242">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-243">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="56c7c-243">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="56c7c-244">Rufen Sie die HimetricLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-244">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="56c7c-245">öffentliche HRESULT- [get_HimetricLocationRaw](#get_himetriclocationraw)(Point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="56c7c-245">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="56c7c-246">Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-246">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-247">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="56c7c-247">get_HistoryCount</span></span> 

<span data-ttu-id="56c7c-248">Rufen Sie die HistoryCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-248">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="56c7c-249">Public HRESULT [get_HistoryCount](#get_historycount)(UInt32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="56c7c-249">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="56c7c-250">Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-250">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-251">get_InputData</span><span class="sxs-lookup"><span data-stu-id="56c7c-251">get_InputData</span></span> 

<span data-ttu-id="56c7c-252">Rufen Sie die inputData des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-252">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="56c7c-253">Public HRESULT [get_InputData](#get_inputdata)(Int32 \* inputData)</span><span class="sxs-lookup"><span data-stu-id="56c7c-253">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="56c7c-254">Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-254">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-255">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="56c7c-255">get_KeyStates</span></span> 

<span data-ttu-id="56c7c-256">Rufen Sie die KeyStates des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-256">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="56c7c-257">öffentliche HRESULT- [get_KeyStates](#get_keystates)(DWORD \*-KeyStates)</span><span class="sxs-lookup"><span data-stu-id="56c7c-257">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="56c7c-258">Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-258">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-259">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="56c7c-259">get_PenFlags</span></span> 

<span data-ttu-id="56c7c-260">Rufen Sie die PenFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-260">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="56c7c-261">Public HRESULT [get_PenFlags](#get_penflags)(UInt32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="56c7c-261">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="56c7c-262">Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-262">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="56c7c-263">Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-263">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-264">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="56c7c-264">get_PenMask</span></span> 

<span data-ttu-id="56c7c-265">Rufen Sie die PenMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-265">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="56c7c-266">Public HRESULT [get_PenMask](#get_penmask)(UInt32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="56c7c-266">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="56c7c-267">Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-267">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="56c7c-268">Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-268">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-269">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="56c7c-269">get_PenPressure</span></span> 

<span data-ttu-id="56c7c-270">Rufen Sie die PenPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-270">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="56c7c-271">Public HRESULT [get_PenPressure](#get_penpressure)(UInt32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="56c7c-271">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="56c7c-272">Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-272">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-273">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="56c7c-273">get_PenRotation</span></span> 

<span data-ttu-id="56c7c-274">Rufen Sie die PenRotation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-274">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="56c7c-275">Public HRESULT [get_PenRotation](#get_penrotation)(UInt32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="56c7c-275">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="56c7c-276">Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-276">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-277">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="56c7c-277">get_PenTiltX</span></span> 

<span data-ttu-id="56c7c-278">Rufen Sie die PenTiltX des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-278">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="56c7c-279">Public HRESULT [get_PenTiltX](#get_pentiltx)(Int32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="56c7c-279">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="56c7c-280">Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-280">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-281">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="56c7c-281">get_PenTiltY</span></span> 

<span data-ttu-id="56c7c-282">Rufen Sie die PenTiltY des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-282">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="56c7c-283">Public HRESULT [get_PenTiltY](#get_pentilty)(Int32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="56c7c-283">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="56c7c-284">Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-284">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-285">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="56c7c-285">get_PerformanceCount</span></span> 

<span data-ttu-id="56c7c-286">Rufen Sie die PerformanceCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-286">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="56c7c-287">Public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="56c7c-287">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="56c7c-288">Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-288">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-289">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="56c7c-289">get_PixelLocation</span></span> 

<span data-ttu-id="56c7c-290">Rufen Sie die PixelLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-290">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="56c7c-291">öffentliche HRESULT- [get_PixelLocation](#get_pixellocation)(Point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="56c7c-291">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="56c7c-292">Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-292">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-293">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="56c7c-293">get_PixelLocationRaw</span></span> 

<span data-ttu-id="56c7c-294">Rufen Sie die PixelLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-294">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="56c7c-295">öffentliche HRESULT- [get_PixelLocationRaw](#get_pixellocationraw)(Point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="56c7c-295">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="56c7c-296">Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-296">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-297">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="56c7c-297">get_PointerDeviceRect</span></span> 

<span data-ttu-id="56c7c-298">Rufen Sie die PointerDeviceRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-298">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="56c7c-299">Public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="56c7c-299">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="56c7c-300">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="56c7c-300">get_PointerFlags</span></span> 

<span data-ttu-id="56c7c-301">Rufen Sie die PointerFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-301">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="56c7c-302">Public HRESULT [get_PointerFlags](#get_pointerflags)(UInt32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="56c7c-302">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="56c7c-303">Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-303">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="56c7c-304">Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-304">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-305">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="56c7c-305">get_PointerId</span></span> 

<span data-ttu-id="56c7c-306">Rufen Sie die Zeiger-Nr. des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-306">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="56c7c-307">öffentliche HRESULT- [get_PointerId](#get_pointerid)(UInt32 \* Pointer-Nr.)</span><span class="sxs-lookup"><span data-stu-id="56c7c-307">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="56c7c-308">Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-308">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-309">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="56c7c-309">get_PointerKind</span></span> 

<span data-ttu-id="56c7c-310">Rufen Sie die PointerKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-310">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="56c7c-311">Public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="56c7c-311">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="56c7c-312">Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-312">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="56c7c-313">Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-313">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="56c7c-314">Unterstützt PT_PEN und PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="56c7c-314">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="56c7c-315">get_Time</span><span class="sxs-lookup"><span data-stu-id="56c7c-315">get_Time</span></span> 

<span data-ttu-id="56c7c-316">Rufen Sie die Uhrzeit des Zeiger Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-316">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="56c7c-317">öffentliche HRESULT- [get_Time](#get_time)(DWORD \* Zeit)</span><span class="sxs-lookup"><span data-stu-id="56c7c-317">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="56c7c-318">Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-318">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-319">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="56c7c-319">get_TouchContact</span></span> 

<span data-ttu-id="56c7c-320">Rufen Sie die TouchContact des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-320">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="56c7c-321">Public HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="56c7c-321">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="56c7c-322">Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-322">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-323">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="56c7c-323">get_TouchContactRaw</span></span> 

<span data-ttu-id="56c7c-324">Rufen Sie die TouchContactRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-324">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="56c7c-325">Public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="56c7c-325">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="56c7c-326">Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-326">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-327">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="56c7c-327">get_TouchFlags</span></span> 

<span data-ttu-id="56c7c-328">Rufen Sie die TouchFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-328">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="56c7c-329">Public HRESULT [get_TouchFlags](#get_touchflags)(UInt32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="56c7c-329">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="56c7c-330">Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-330">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="56c7c-331">Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-331">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-332">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="56c7c-332">get_TouchMask</span></span> 

<span data-ttu-id="56c7c-333">Rufen Sie die TouchMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-333">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="56c7c-334">Public HRESULT [get_TouchMask](#get_touchmask)(UInt32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="56c7c-334">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="56c7c-335">Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-335">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="56c7c-336">Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-336">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-337">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="56c7c-337">get_TouchOrientation</span></span> 

<span data-ttu-id="56c7c-338">Rufen Sie die TouchOrientation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-338">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="56c7c-339">Public HRESULT [get_TouchOrientation](#get_touchorientation)(UInt32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="56c7c-339">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="56c7c-340">Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-340">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-341">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="56c7c-341">get_TouchPressure</span></span> 

<span data-ttu-id="56c7c-342">Rufen Sie die TouchPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="56c7c-342">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="56c7c-343">Public HRESULT [get_TouchPressure](#get_touchpressure)(UInt32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="56c7c-343">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="56c7c-344">Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-344">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-345">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="56c7c-345">put_ButtonChangeKind</span></span> 

<span data-ttu-id="56c7c-346">Legt die ButtonChangeKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-346">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="56c7c-347">Public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(Int32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="56c7c-347">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="56c7c-348">Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-348">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="56c7c-349">Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-349">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-350">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="56c7c-350">put_DisplayRect</span></span> 

<span data-ttu-id="56c7c-351">Setzen Sie die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-351">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="56c7c-352">Public HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="56c7c-352">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="56c7c-353">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="56c7c-353">put_FrameId</span></span> 

<span data-ttu-id="56c7c-354">Legt die Frame-Nr des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-354">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="56c7c-355">Public HRESULT [put_FrameId](#put_frameid)(UInt32-Frame-Nr)</span><span class="sxs-lookup"><span data-stu-id="56c7c-355">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="56c7c-356">Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-356">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-357">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="56c7c-357">put_HimetricLocation</span></span> 

<span data-ttu-id="56c7c-358">Legt die HimetricLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-358">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="56c7c-359">öffentliche HRESULT- [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="56c7c-359">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="56c7c-360">Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-360">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-361">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="56c7c-361">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="56c7c-362">Legt die HimetricLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-362">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="56c7c-363">öffentliche HRESULT- [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="56c7c-363">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="56c7c-364">Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-364">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-365">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="56c7c-365">put_HistoryCount</span></span> 

<span data-ttu-id="56c7c-366">Legt die HistoryCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-366">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="56c7c-367">Public HRESULT [put_HistoryCount](#put_historycount)(UInt32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="56c7c-367">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="56c7c-368">Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-368">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-369">put_InputData</span><span class="sxs-lookup"><span data-stu-id="56c7c-369">put_InputData</span></span> 

<span data-ttu-id="56c7c-370">Legt die inputData des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-370">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="56c7c-371">Public HRESULT [put_InputData](#put_inputdata)(Int32 inputData)</span><span class="sxs-lookup"><span data-stu-id="56c7c-371">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="56c7c-372">Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-372">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-373">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="56c7c-373">put_KeyStates</span></span> 

<span data-ttu-id="56c7c-374">Die KeyStates des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="56c7c-374">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="56c7c-375">Public HRESULT [put_KeyStates](#put_keystates)(DWORD-KeyStates)</span><span class="sxs-lookup"><span data-stu-id="56c7c-375">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="56c7c-376">Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-376">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-377">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="56c7c-377">put_PenFlags</span></span> 

<span data-ttu-id="56c7c-378">Legt die PenFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-378">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="56c7c-379">Public HRESULT [put_PenFlags](#put_penflags)(UInt32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="56c7c-379">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="56c7c-380">Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-380">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="56c7c-381">Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-381">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-382">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="56c7c-382">put_PenMask</span></span> 

<span data-ttu-id="56c7c-383">Legt die PenMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-383">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="56c7c-384">Public HRESULT [put_PenMask](#put_penmask)(UInt32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="56c7c-384">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="56c7c-385">Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-385">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="56c7c-386">Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-386">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-387">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="56c7c-387">put_PenPressure</span></span> 

<span data-ttu-id="56c7c-388">Legt die PenPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-388">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="56c7c-389">Public HRESULT [put_PenPressure](#put_penpressure)(UInt32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="56c7c-389">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="56c7c-390">Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-390">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-391">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="56c7c-391">put_PenRotation</span></span> 

<span data-ttu-id="56c7c-392">Legt die PenRotation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-392">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="56c7c-393">Public HRESULT [put_PenRotation](#put_penrotation)(UInt32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="56c7c-393">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="56c7c-394">Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-394">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-395">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="56c7c-395">put_PenTiltX</span></span> 

<span data-ttu-id="56c7c-396">Legt die PenTiltX des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-396">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="56c7c-397">Public HRESULT [put_PenTiltX](#put_pentiltx)(Int32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="56c7c-397">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="56c7c-398">Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-398">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-399">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="56c7c-399">put_PenTiltY</span></span> 

<span data-ttu-id="56c7c-400">Legt die PenTiltY des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-400">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="56c7c-401">Public HRESULT [put_PenTiltY](#put_pentilty)(Int32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="56c7c-401">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="56c7c-402">Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-402">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-403">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="56c7c-403">put_PerformanceCount</span></span> 

<span data-ttu-id="56c7c-404">Legt die PerformanceCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-404">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="56c7c-405">Public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="56c7c-405">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="56c7c-406">Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-406">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-407">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="56c7c-407">put_PixelLocation</span></span> 

<span data-ttu-id="56c7c-408">Legt die PixelLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-408">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="56c7c-409">öffentliche HRESULT- [put_PixelLocation](#put_pixellocation)(Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="56c7c-409">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="56c7c-410">Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-410">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-411">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="56c7c-411">put_PixelLocationRaw</span></span> 

<span data-ttu-id="56c7c-412">Legt die PixelLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-412">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="56c7c-413">öffentliche HRESULT- [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="56c7c-413">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="56c7c-414">Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-414">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-415">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="56c7c-415">put_PointerDeviceRect</span></span> 

<span data-ttu-id="56c7c-416">Setzen Sie die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-416">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="56c7c-417">Public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="56c7c-417">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="56c7c-418">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="56c7c-418">put_PointerFlags</span></span> 

<span data-ttu-id="56c7c-419">Legt die PointerFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-419">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="56c7c-420">Public HRESULT [put_PointerFlags](#put_pointerflags)(UInt32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="56c7c-420">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="56c7c-421">Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-421">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="56c7c-422">Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-422">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-423">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="56c7c-423">put_PointerId</span></span> 

<span data-ttu-id="56c7c-424">Die Zeiger-Nr. des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="56c7c-424">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="56c7c-425">Public HRESULT [put_PointerId](#put_pointerid)(UInt32-Zeiger-Nr.)</span><span class="sxs-lookup"><span data-stu-id="56c7c-425">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="56c7c-426">Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-426">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-427">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="56c7c-427">put_PointerKind</span></span> 

<span data-ttu-id="56c7c-428">Legt die PointerKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-428">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="56c7c-429">Public HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="56c7c-429">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="56c7c-430">Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-430">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="56c7c-431">Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-431">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="56c7c-432">Unterstützt PT_PEN und PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="56c7c-432">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="56c7c-433">put_Time</span><span class="sxs-lookup"><span data-stu-id="56c7c-433">put_Time</span></span> 

<span data-ttu-id="56c7c-434">Legt die Uhrzeit des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-434">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="56c7c-435">Public HRESULT [put_Time](#put_time)(DWORD-Zeit)</span><span class="sxs-lookup"><span data-stu-id="56c7c-435">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="56c7c-436">Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-436">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-437">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="56c7c-437">put_TouchContact</span></span> 

<span data-ttu-id="56c7c-438">Legt die TouchContact des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-438">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="56c7c-439">Public HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="56c7c-439">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="56c7c-440">Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-440">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-441">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="56c7c-441">put_TouchContactRaw</span></span> 

<span data-ttu-id="56c7c-442">Legt die TouchContactRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-442">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="56c7c-443">Public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="56c7c-443">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="56c7c-444">Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-444">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-445">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="56c7c-445">put_TouchFlags</span></span> 

<span data-ttu-id="56c7c-446">Legt die TouchFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-446">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="56c7c-447">Public HRESULT [put_TouchFlags](#put_touchflags)(UInt32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="56c7c-447">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="56c7c-448">Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-448">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="56c7c-449">Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-449">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-450">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="56c7c-450">put_TouchMask</span></span> 

<span data-ttu-id="56c7c-451">Legt die TouchMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-451">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="56c7c-452">Public HRESULT [put_TouchMask](#put_touchmask)(UInt32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="56c7c-452">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="56c7c-453">Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="56c7c-453">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="56c7c-454">Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="56c7c-454">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-455">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="56c7c-455">put_TouchOrientation</span></span> 

<span data-ttu-id="56c7c-456">Legt die TouchOrientation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-456">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="56c7c-457">Public HRESULT [put_TouchOrientation](#put_touchorientation)(UInt32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="56c7c-457">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="56c7c-458">Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-458">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="56c7c-459">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="56c7c-459">put_TouchPressure</span></span> 

<span data-ttu-id="56c7c-460">Legt die TouchPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="56c7c-460">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="56c7c-461">Public HRESULT [put_TouchPressure](#put_touchpressure)(UInt32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="56c7c-461">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="56c7c-462">Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="56c7c-462">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


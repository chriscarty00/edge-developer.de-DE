---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalPointerInfo
ms.openlocfilehash: bc35ebaf3f1b5acf12a1d379336cd006f962390e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012154"
---
# <span data-ttu-id="8eb6d-104">Schnittstellen ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="8eb6d-104">interface ICoreWebView2ExperimentalPointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="8eb6d-105">Dies stellt in erster Linie ein kombiniertes Win32-POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-105">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="8eb6d-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8eb6d-106">Summary</span></span>

 <span data-ttu-id="8eb6d-107">Member</span><span class="sxs-lookup"><span data-stu-id="8eb6d-107">Members</span></span>                        | <span data-ttu-id="8eb6d-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8eb6d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8eb6d-109">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="8eb6d-109">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="8eb6d-110">Rufen Sie die ButtonChangeKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-110">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-111">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="8eb6d-111">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="8eb6d-112">Rufen Sie die DisplayRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-112">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="8eb6d-113">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="8eb6d-113">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="8eb6d-114">Rufen Sie die Frame-Nr des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-114">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-115">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-115">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="8eb6d-116">Rufen Sie die HimetricLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-116">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-117">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="8eb6d-117">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="8eb6d-118">Rufen Sie die HimetricLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-118">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-119">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="8eb6d-119">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="8eb6d-120">Rufen Sie die HistoryCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-120">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-121">get_InputData</span><span class="sxs-lookup"><span data-stu-id="8eb6d-121">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="8eb6d-122">Rufen Sie die inputData des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-122">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-123">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="8eb6d-123">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="8eb6d-124">Rufen Sie die KeyStates des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-124">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-125">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="8eb6d-125">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="8eb6d-126">Rufen Sie die PenFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-126">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-127">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="8eb6d-127">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="8eb6d-128">Rufen Sie die PenMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-128">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-129">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="8eb6d-129">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="8eb6d-130">Rufen Sie die PenPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-130">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-131">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-131">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="8eb6d-132">Rufen Sie die PenRotation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-132">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-133">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="8eb6d-133">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="8eb6d-134">Rufen Sie die PenTiltX des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-134">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-135">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="8eb6d-135">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="8eb6d-136">Rufen Sie die PenTiltY des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-136">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-137">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="8eb6d-137">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="8eb6d-138">Rufen Sie die PerformanceCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-138">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-139">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-139">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="8eb6d-140">Rufen Sie die PixelLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-140">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-141">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="8eb6d-141">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="8eb6d-142">Rufen Sie die PixelLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-142">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-143">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="8eb6d-143">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="8eb6d-144">Rufen Sie die PointerDeviceRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-144">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="8eb6d-145">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="8eb6d-145">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="8eb6d-146">Rufen Sie die PointerFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-146">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-147">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="8eb6d-147">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="8eb6d-148">Rufen Sie die Zeiger-Nr. des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-148">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-149">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="8eb6d-149">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="8eb6d-150">Rufen Sie die PointerKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-150">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-151">get_Time</span><span class="sxs-lookup"><span data-stu-id="8eb6d-151">get_Time</span></span>](#get_time) | <span data-ttu-id="8eb6d-152">Rufen Sie die Uhrzeit des Zeiger Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-152">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-153">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="8eb6d-153">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="8eb6d-154">Rufen Sie die TouchContact des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-154">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-155">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="8eb6d-155">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="8eb6d-156">Rufen Sie die TouchContactRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-156">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-157">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="8eb6d-157">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="8eb6d-158">Rufen Sie die TouchFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-158">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-159">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="8eb6d-159">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="8eb6d-160">Rufen Sie die TouchMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-160">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-161">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-161">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="8eb6d-162">Rufen Sie die TouchOrientation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-162">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-163">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="8eb6d-163">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="8eb6d-164">Rufen Sie die TouchPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-164">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-165">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="8eb6d-165">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="8eb6d-166">Legt die ButtonChangeKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-166">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-167">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="8eb6d-167">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="8eb6d-168">Setzen Sie die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-168">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="8eb6d-169">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="8eb6d-169">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="8eb6d-170">Legt die Frame-Nr des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-170">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-171">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-171">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="8eb6d-172">Legt die HimetricLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-172">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-173">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="8eb6d-173">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="8eb6d-174">Legt die HimetricLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-174">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-175">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="8eb6d-175">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="8eb6d-176">Legt die HistoryCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-176">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-177">put_InputData</span><span class="sxs-lookup"><span data-stu-id="8eb6d-177">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="8eb6d-178">Legt die inputData des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-178">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-179">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="8eb6d-179">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="8eb6d-180">Die KeyStates des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-180">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-181">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="8eb6d-181">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="8eb6d-182">Legt die PenFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-182">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-183">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="8eb6d-183">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="8eb6d-184">Legt die PenMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-184">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-185">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="8eb6d-185">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="8eb6d-186">Legt die PenPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-186">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-187">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-187">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="8eb6d-188">Legt die PenRotation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-188">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-189">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="8eb6d-189">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="8eb6d-190">Legt die PenTiltX des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-190">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-191">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="8eb6d-191">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="8eb6d-192">Legt die PenTiltY des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-192">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-193">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="8eb6d-193">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="8eb6d-194">Legt die PerformanceCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-194">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-195">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-195">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="8eb6d-196">Legt die PixelLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-196">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-197">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="8eb6d-197">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="8eb6d-198">Legt die PixelLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-198">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-199">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="8eb6d-199">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="8eb6d-200">Setzen Sie die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-200">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="8eb6d-201">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="8eb6d-201">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="8eb6d-202">Legt die PointerFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-202">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-203">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="8eb6d-203">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="8eb6d-204">Die Zeiger-Nr. des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-204">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-205">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="8eb6d-205">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="8eb6d-206">Legt die PointerKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-206">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-207">put_Time</span><span class="sxs-lookup"><span data-stu-id="8eb6d-207">put_Time</span></span>](#put_time) | <span data-ttu-id="8eb6d-208">Legt die Uhrzeit des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-208">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-209">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="8eb6d-209">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="8eb6d-210">Legt die TouchContact des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-210">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-211">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="8eb6d-211">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="8eb6d-212">Legt die TouchContactRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-212">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-213">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="8eb6d-213">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="8eb6d-214">Legt die TouchFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-214">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-215">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="8eb6d-215">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="8eb6d-216">Legt die TouchMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-216">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-217">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-217">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="8eb6d-218">Legt die TouchOrientation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-218">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="8eb6d-219">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="8eb6d-219">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="8eb6d-220">Legt die TouchPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-220">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="8eb6d-221">Sie nimmt Felder aus allen dreien auf und schließt einige Win32-spezifische Datentypen wie HWND und handle aus.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-221">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="8eb6d-222">Beachten Sie, dass sourceDevice herausgenommen wird, aber wir erwarten, dass PointerDeviceRect und DisplayRect die vorhandenen Anwendungsfälle von sourceDevice abdecken.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-222">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="8eb6d-223">Ein weiterer großer Unterschied besteht darin, dass eine der Punkt-oder Rect-Positionen in WebView-physikalischen Koordinaten erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-223">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="8eb6d-224">Das heißt, Koordinaten relativ zum WebView und keine DPI-Skalierung angewendet.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-224">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="8eb6d-225">Member</span><span class="sxs-lookup"><span data-stu-id="8eb6d-225">Members</span></span>

#### <span data-ttu-id="8eb6d-226">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="8eb6d-226">get_ButtonChangeKind</span></span> 

<span data-ttu-id="8eb6d-227">Rufen Sie die ButtonChangeKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-227">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-228">Public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(Int32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-228">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="8eb6d-229">Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-229">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="8eb6d-230">Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-230">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-231">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="8eb6d-231">get_DisplayRect</span></span> 

<span data-ttu-id="8eb6d-232">Rufen Sie die DisplayRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-232">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="8eb6d-233">Public HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-233">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="8eb6d-234">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="8eb6d-234">get_FrameId</span></span> 

<span data-ttu-id="8eb6d-235">Rufen Sie die Frame-Nr des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-235">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-236">Public HRESULT [get_FrameId](#get_frameid)(UInt32 \* Frame-Nr)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-236">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="8eb6d-237">Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-237">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-238">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-238">get_HimetricLocation</span></span> 

<span data-ttu-id="8eb6d-239">Rufen Sie die HimetricLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-239">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-240">öffentliche HRESULT- [get_HimetricLocation](#get_himetriclocation)(Point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-240">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="8eb6d-241">Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-241">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-242">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="8eb6d-242">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="8eb6d-243">Rufen Sie die HimetricLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-243">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-244">öffentliche HRESULT- [get_HimetricLocationRaw](#get_himetriclocationraw)(Point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-244">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="8eb6d-245">Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-245">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-246">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="8eb6d-246">get_HistoryCount</span></span> 

<span data-ttu-id="8eb6d-247">Rufen Sie die HistoryCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-247">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-248">Public HRESULT [get_HistoryCount](#get_historycount)(UInt32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-248">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="8eb6d-249">Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-249">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-250">get_InputData</span><span class="sxs-lookup"><span data-stu-id="8eb6d-250">get_InputData</span></span> 

<span data-ttu-id="8eb6d-251">Rufen Sie die inputData des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-251">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-252">Public HRESULT [get_InputData](#get_inputdata)(Int32 \* inputData)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-252">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="8eb6d-253">Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-253">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-254">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="8eb6d-254">get_KeyStates</span></span> 

<span data-ttu-id="8eb6d-255">Rufen Sie die KeyStates des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-255">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-256">öffentliche HRESULT- [get_KeyStates](#get_keystates)(DWORD \*-KeyStates)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-256">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="8eb6d-257">Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-257">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-258">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="8eb6d-258">get_PenFlags</span></span> 

<span data-ttu-id="8eb6d-259">Rufen Sie die PenFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-259">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-260">Public HRESULT [get_PenFlags](#get_penflags)(UInt32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-260">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="8eb6d-261">Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-261">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="8eb6d-262">Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-262">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-263">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="8eb6d-263">get_PenMask</span></span> 

<span data-ttu-id="8eb6d-264">Rufen Sie die PenMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-264">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-265">Public HRESULT [get_PenMask](#get_penmask)(UInt32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-265">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="8eb6d-266">Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-266">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="8eb6d-267">Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-267">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-268">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="8eb6d-268">get_PenPressure</span></span> 

<span data-ttu-id="8eb6d-269">Rufen Sie die PenPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-269">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-270">Public HRESULT [get_PenPressure](#get_penpressure)(UInt32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-270">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="8eb6d-271">Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-271">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-272">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-272">get_PenRotation</span></span> 

<span data-ttu-id="8eb6d-273">Rufen Sie die PenRotation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-273">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-274">Public HRESULT [get_PenRotation](#get_penrotation)(UInt32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-274">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="8eb6d-275">Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-275">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-276">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="8eb6d-276">get_PenTiltX</span></span> 

<span data-ttu-id="8eb6d-277">Rufen Sie die PenTiltX des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-277">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-278">Public HRESULT [get_PenTiltX](#get_pentiltx)(Int32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-278">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="8eb6d-279">Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-279">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-280">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="8eb6d-280">get_PenTiltY</span></span> 

<span data-ttu-id="8eb6d-281">Rufen Sie die PenTiltY des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-281">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-282">Public HRESULT [get_PenTiltY](#get_pentilty)(Int32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-282">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="8eb6d-283">Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-283">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-284">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="8eb6d-284">get_PerformanceCount</span></span> 

<span data-ttu-id="8eb6d-285">Rufen Sie die PerformanceCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-285">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-286">Public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-286">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="8eb6d-287">Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-287">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-288">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-288">get_PixelLocation</span></span> 

<span data-ttu-id="8eb6d-289">Rufen Sie die PixelLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-289">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-290">öffentliche HRESULT- [get_PixelLocation](#get_pixellocation)(Point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-290">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="8eb6d-291">Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-291">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-292">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="8eb6d-292">get_PixelLocationRaw</span></span> 

<span data-ttu-id="8eb6d-293">Rufen Sie die PixelLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-293">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-294">öffentliche HRESULT- [get_PixelLocationRaw](#get_pixellocationraw)(Point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-294">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="8eb6d-295">Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-295">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-296">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="8eb6d-296">get_PointerDeviceRect</span></span> 

<span data-ttu-id="8eb6d-297">Rufen Sie die PointerDeviceRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-297">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="8eb6d-298">Public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-298">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="8eb6d-299">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="8eb6d-299">get_PointerFlags</span></span> 

<span data-ttu-id="8eb6d-300">Rufen Sie die PointerFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-300">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-301">Public HRESULT [get_PointerFlags](#get_pointerflags)(UInt32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-301">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="8eb6d-302">Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-302">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="8eb6d-303">Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-303">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-304">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="8eb6d-304">get_PointerId</span></span> 

<span data-ttu-id="8eb6d-305">Rufen Sie die Zeiger-Nr. des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-305">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-306">öffentliche HRESULT- [get_PointerId](#get_pointerid)(UInt32 \* Pointer-Nr.)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-306">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="8eb6d-307">Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-307">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-308">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="8eb6d-308">get_PointerKind</span></span> 

<span data-ttu-id="8eb6d-309">Rufen Sie die PointerKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-309">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-310">Public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-310">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="8eb6d-311">Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-311">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="8eb6d-312">Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-312">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="8eb6d-313">Unterstützt PT_PEN und PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-313">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="8eb6d-314">get_Time</span><span class="sxs-lookup"><span data-stu-id="8eb6d-314">get_Time</span></span> 

<span data-ttu-id="8eb6d-315">Rufen Sie die Uhrzeit des Zeiger Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-315">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-316">öffentliche HRESULT- [get_Time](#get_time)(DWORD \* Zeit)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-316">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="8eb6d-317">Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-317">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-318">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="8eb6d-318">get_TouchContact</span></span> 

<span data-ttu-id="8eb6d-319">Rufen Sie die TouchContact des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-319">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-320">Public HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-320">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="8eb6d-321">Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-321">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-322">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="8eb6d-322">get_TouchContactRaw</span></span> 

<span data-ttu-id="8eb6d-323">Rufen Sie die TouchContactRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-323">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-324">Public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-324">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="8eb6d-325">Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-325">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-326">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="8eb6d-326">get_TouchFlags</span></span> 

<span data-ttu-id="8eb6d-327">Rufen Sie die TouchFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-327">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-328">Public HRESULT [get_TouchFlags](#get_touchflags)(UInt32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-328">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="8eb6d-329">Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-329">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="8eb6d-330">Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-330">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-331">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="8eb6d-331">get_TouchMask</span></span> 

<span data-ttu-id="8eb6d-332">Rufen Sie die TouchMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-332">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-333">Public HRESULT [get_TouchMask](#get_touchmask)(UInt32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-333">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="8eb6d-334">Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-334">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="8eb6d-335">Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-335">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-336">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-336">get_TouchOrientation</span></span> 

<span data-ttu-id="8eb6d-337">Rufen Sie die TouchOrientation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-337">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-338">Public HRESULT [get_TouchOrientation](#get_touchorientation)(UInt32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-338">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="8eb6d-339">Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-339">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-340">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="8eb6d-340">get_TouchPressure</span></span> 

<span data-ttu-id="8eb6d-341">Rufen Sie die TouchPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-341">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-342">Public HRESULT [get_TouchPressure](#get_touchpressure)(UInt32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-342">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="8eb6d-343">Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-343">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-344">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="8eb6d-344">put_ButtonChangeKind</span></span> 

<span data-ttu-id="8eb6d-345">Legt die ButtonChangeKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-345">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-346">Public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(Int32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-346">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="8eb6d-347">Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-347">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="8eb6d-348">Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-348">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-349">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="8eb6d-349">put_DisplayRect</span></span> 

<span data-ttu-id="8eb6d-350">Setzen Sie die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-350">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="8eb6d-351">Public HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-351">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="8eb6d-352">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="8eb6d-352">put_FrameId</span></span> 

<span data-ttu-id="8eb6d-353">Legt die Frame-Nr des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-353">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-354">Public HRESULT [put_FrameId](#put_frameid)(UInt32-Frame-Nr)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-354">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="8eb6d-355">Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-355">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-356">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-356">put_HimetricLocation</span></span> 

<span data-ttu-id="8eb6d-357">Legt die HimetricLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-357">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-358">öffentliche HRESULT- [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-358">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="8eb6d-359">Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-359">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-360">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="8eb6d-360">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="8eb6d-361">Legt die HimetricLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-361">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-362">öffentliche HRESULT- [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-362">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="8eb6d-363">Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-363">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-364">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="8eb6d-364">put_HistoryCount</span></span> 

<span data-ttu-id="8eb6d-365">Legt die HistoryCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-365">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-366">Public HRESULT [put_HistoryCount](#put_historycount)(UInt32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-366">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="8eb6d-367">Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-367">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-368">put_InputData</span><span class="sxs-lookup"><span data-stu-id="8eb6d-368">put_InputData</span></span> 

<span data-ttu-id="8eb6d-369">Legt die inputData des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-369">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-370">Public HRESULT [put_InputData](#put_inputdata)(Int32 inputData)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-370">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="8eb6d-371">Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-371">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-372">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="8eb6d-372">put_KeyStates</span></span> 

<span data-ttu-id="8eb6d-373">Die KeyStates des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-373">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-374">Public HRESULT [put_KeyStates](#put_keystates)(DWORD-KeyStates)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-374">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="8eb6d-375">Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-375">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-376">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="8eb6d-376">put_PenFlags</span></span> 

<span data-ttu-id="8eb6d-377">Legt die PenFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-377">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-378">Public HRESULT [put_PenFlags](#put_penflags)(UInt32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-378">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="8eb6d-379">Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-379">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="8eb6d-380">Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-380">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-381">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="8eb6d-381">put_PenMask</span></span> 

<span data-ttu-id="8eb6d-382">Legt die PenMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-382">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-383">Public HRESULT [put_PenMask](#put_penmask)(UInt32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-383">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="8eb6d-384">Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-384">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="8eb6d-385">Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-385">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-386">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="8eb6d-386">put_PenPressure</span></span> 

<span data-ttu-id="8eb6d-387">Legt die PenPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-387">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-388">Public HRESULT [put_PenPressure](#put_penpressure)(UInt32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-388">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="8eb6d-389">Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-389">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-390">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-390">put_PenRotation</span></span> 

<span data-ttu-id="8eb6d-391">Legt die PenRotation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-391">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-392">Public HRESULT [put_PenRotation](#put_penrotation)(UInt32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-392">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="8eb6d-393">Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-393">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-394">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="8eb6d-394">put_PenTiltX</span></span> 

<span data-ttu-id="8eb6d-395">Legt die PenTiltX des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-395">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-396">Public HRESULT [put_PenTiltX](#put_pentiltx)(Int32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-396">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="8eb6d-397">Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-397">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-398">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="8eb6d-398">put_PenTiltY</span></span> 

<span data-ttu-id="8eb6d-399">Legt die PenTiltY des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-399">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-400">Public HRESULT [put_PenTiltY](#put_pentilty)(Int32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-400">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="8eb6d-401">Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-401">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-402">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="8eb6d-402">put_PerformanceCount</span></span> 

<span data-ttu-id="8eb6d-403">Legt die PerformanceCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-403">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-404">Public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-404">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="8eb6d-405">Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-405">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-406">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-406">put_PixelLocation</span></span> 

<span data-ttu-id="8eb6d-407">Legt die PixelLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-407">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-408">öffentliche HRESULT- [put_PixelLocation](#put_pixellocation)(Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-408">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="8eb6d-409">Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-409">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-410">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="8eb6d-410">put_PixelLocationRaw</span></span> 

<span data-ttu-id="8eb6d-411">Legt die PixelLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-411">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-412">öffentliche HRESULT- [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-412">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="8eb6d-413">Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-413">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-414">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="8eb6d-414">put_PointerDeviceRect</span></span> 

<span data-ttu-id="8eb6d-415">Setzen Sie die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-415">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="8eb6d-416">Public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-416">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="8eb6d-417">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="8eb6d-417">put_PointerFlags</span></span> 

<span data-ttu-id="8eb6d-418">Legt die PointerFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-418">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-419">Public HRESULT [put_PointerFlags](#put_pointerflags)(UInt32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-419">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="8eb6d-420">Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-420">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="8eb6d-421">Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-421">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-422">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="8eb6d-422">put_PointerId</span></span> 

<span data-ttu-id="8eb6d-423">Die Zeiger-Nr. des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-423">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-424">Public HRESULT [put_PointerId](#put_pointerid)(UInt32-Zeiger-Nr.)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-424">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="8eb6d-425">Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-425">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-426">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="8eb6d-426">put_PointerKind</span></span> 

<span data-ttu-id="8eb6d-427">Legt die PointerKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-427">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-428">Public HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-428">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="8eb6d-429">Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-429">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="8eb6d-430">Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-430">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="8eb6d-431">Unterstützt PT_PEN und PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-431">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="8eb6d-432">put_Time</span><span class="sxs-lookup"><span data-stu-id="8eb6d-432">put_Time</span></span> 

<span data-ttu-id="8eb6d-433">Legt die Uhrzeit des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-433">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-434">Public HRESULT [put_Time](#put_time)(DWORD-Zeit)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-434">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="8eb6d-435">Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-435">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-436">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="8eb6d-436">put_TouchContact</span></span> 

<span data-ttu-id="8eb6d-437">Legt die TouchContact des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-437">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-438">Public HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-438">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="8eb6d-439">Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-439">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-440">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="8eb6d-440">put_TouchContactRaw</span></span> 

<span data-ttu-id="8eb6d-441">Legt die TouchContactRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-441">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-442">Public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-442">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="8eb6d-443">Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-443">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-444">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="8eb6d-444">put_TouchFlags</span></span> 

<span data-ttu-id="8eb6d-445">Legt die TouchFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-445">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-446">Public HRESULT [put_TouchFlags](#put_touchflags)(UInt32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-446">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="8eb6d-447">Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-447">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="8eb6d-448">Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-448">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-449">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="8eb6d-449">put_TouchMask</span></span> 

<span data-ttu-id="8eb6d-450">Legt die TouchMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-450">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-451">Public HRESULT [put_TouchMask](#put_touchmask)(UInt32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-451">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="8eb6d-452">Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-452">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="8eb6d-453">Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-453">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-454">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="8eb6d-454">put_TouchOrientation</span></span> 

<span data-ttu-id="8eb6d-455">Legt die TouchOrientation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-455">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-456">Public HRESULT [put_TouchOrientation](#put_touchorientation)(UInt32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-456">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="8eb6d-457">Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-457">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="8eb6d-458">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="8eb6d-458">put_TouchPressure</span></span> 

<span data-ttu-id="8eb6d-459">Legt die TouchPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="8eb6d-459">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="8eb6d-460">Public HRESULT [put_TouchPressure](#put_touchpressure)(UInt32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="8eb6d-460">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="8eb6d-461">Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="8eb6d-461">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


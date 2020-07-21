---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalPointerInfo
ms.openlocfilehash: 6a5727fbcae24f7fd65c6c4a7a49b1a0b4746eb3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883717"
---
# <span data-ttu-id="b5929-104">Schnittstellen ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="b5929-104">interface ICoreWebView2ExperimentalPointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="b5929-105">Dies stellt in erster Linie ein kombiniertes Win32-POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="b5929-105">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="b5929-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b5929-106">Summary</span></span>

 <span data-ttu-id="b5929-107">Member</span><span class="sxs-lookup"><span data-stu-id="b5929-107">Members</span></span>                        | <span data-ttu-id="b5929-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b5929-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b5929-109">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="b5929-109">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="b5929-110">Rufen Sie die ButtonChangeKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-110">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="b5929-111">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="b5929-111">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="b5929-112">Rufen Sie die DisplayRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-112">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="b5929-113">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="b5929-113">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="b5929-114">Rufen Sie die Frame-Nr des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-114">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="b5929-115">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="b5929-115">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="b5929-116">Rufen Sie die HimetricLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-116">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="b5929-117">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b5929-117">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="b5929-118">Rufen Sie die HimetricLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-118">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="b5929-119">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="b5929-119">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="b5929-120">Rufen Sie die HistoryCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-120">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="b5929-121">get_InputData</span><span class="sxs-lookup"><span data-stu-id="b5929-121">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="b5929-122">Rufen Sie die inputData des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-122">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="b5929-123">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="b5929-123">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="b5929-124">Rufen Sie die KeyStates des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-124">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="b5929-125">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="b5929-125">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="b5929-126">Rufen Sie die PenFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-126">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="b5929-127">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="b5929-127">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="b5929-128">Rufen Sie die PenMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-128">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="b5929-129">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="b5929-129">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="b5929-130">Rufen Sie die PenPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-130">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="b5929-131">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="b5929-131">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="b5929-132">Rufen Sie die PenRotation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-132">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="b5929-133">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="b5929-133">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="b5929-134">Rufen Sie die PenTiltX des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-134">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="b5929-135">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="b5929-135">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="b5929-136">Rufen Sie die PenTiltY des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-136">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="b5929-137">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="b5929-137">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="b5929-138">Rufen Sie die PerformanceCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-138">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="b5929-139">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="b5929-139">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="b5929-140">Rufen Sie die PixelLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-140">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="b5929-141">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b5929-141">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="b5929-142">Rufen Sie die PixelLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-142">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="b5929-143">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="b5929-143">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="b5929-144">Rufen Sie die PointerDeviceRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-144">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="b5929-145">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="b5929-145">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="b5929-146">Rufen Sie die PointerFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-146">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="b5929-147">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="b5929-147">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="b5929-148">Rufen Sie die Zeiger-Nr. des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-148">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="b5929-149">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="b5929-149">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="b5929-150">Rufen Sie die PointerKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-150">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="b5929-151">get_Time</span><span class="sxs-lookup"><span data-stu-id="b5929-151">get_Time</span></span>](#get_time) | <span data-ttu-id="b5929-152">Rufen Sie die Uhrzeit des Zeiger Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-152">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="b5929-153">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="b5929-153">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="b5929-154">Rufen Sie die TouchContact des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-154">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="b5929-155">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="b5929-155">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="b5929-156">Rufen Sie die TouchContactRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-156">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="b5929-157">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="b5929-157">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="b5929-158">Rufen Sie die TouchFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-158">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="b5929-159">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="b5929-159">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="b5929-160">Rufen Sie die TouchMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-160">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="b5929-161">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="b5929-161">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="b5929-162">Rufen Sie die TouchOrientation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-162">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="b5929-163">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="b5929-163">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="b5929-164">Rufen Sie die TouchPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-164">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="b5929-165">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="b5929-165">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="b5929-166">Legt die ButtonChangeKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-166">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="b5929-167">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="b5929-167">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="b5929-168">Setzen Sie die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-168">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="b5929-169">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="b5929-169">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="b5929-170">Legt die Frame-Nr des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-170">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="b5929-171">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="b5929-171">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="b5929-172">Legt die HimetricLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-172">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="b5929-173">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b5929-173">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="b5929-174">Legt die HimetricLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-174">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="b5929-175">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="b5929-175">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="b5929-176">Legt die HistoryCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-176">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="b5929-177">put_InputData</span><span class="sxs-lookup"><span data-stu-id="b5929-177">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="b5929-178">Legt die inputData des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-178">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="b5929-179">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="b5929-179">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="b5929-180">Die KeyStates des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b5929-180">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="b5929-181">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="b5929-181">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="b5929-182">Legt die PenFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-182">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="b5929-183">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="b5929-183">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="b5929-184">Legt die PenMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-184">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="b5929-185">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="b5929-185">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="b5929-186">Legt die PenPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-186">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="b5929-187">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="b5929-187">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="b5929-188">Legt die PenRotation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-188">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="b5929-189">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="b5929-189">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="b5929-190">Legt die PenTiltX des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-190">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="b5929-191">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="b5929-191">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="b5929-192">Legt die PenTiltY des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-192">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="b5929-193">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="b5929-193">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="b5929-194">Legt die PerformanceCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-194">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="b5929-195">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="b5929-195">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="b5929-196">Legt die PixelLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-196">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="b5929-197">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b5929-197">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="b5929-198">Legt die PixelLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-198">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="b5929-199">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="b5929-199">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="b5929-200">Setzen Sie die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-200">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="b5929-201">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="b5929-201">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="b5929-202">Legt die PointerFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-202">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="b5929-203">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="b5929-203">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="b5929-204">Die Zeiger-Nr. des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b5929-204">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="b5929-205">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="b5929-205">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="b5929-206">Legt die PointerKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-206">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="b5929-207">put_Time</span><span class="sxs-lookup"><span data-stu-id="b5929-207">put_Time</span></span>](#put_time) | <span data-ttu-id="b5929-208">Legt die Uhrzeit des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-208">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="b5929-209">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="b5929-209">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="b5929-210">Legt die TouchContact des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-210">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="b5929-211">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="b5929-211">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="b5929-212">Legt die TouchContactRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-212">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="b5929-213">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="b5929-213">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="b5929-214">Legt die TouchFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-214">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="b5929-215">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="b5929-215">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="b5929-216">Legt die TouchMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-216">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="b5929-217">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="b5929-217">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="b5929-218">Legt die TouchOrientation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-218">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="b5929-219">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="b5929-219">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="b5929-220">Legt die TouchPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-220">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="b5929-221">Sie nimmt Felder aus allen dreien auf und schließt einige Win32-spezifische Datentypen wie HWND und handle aus.</span><span class="sxs-lookup"><span data-stu-id="b5929-221">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="b5929-222">Beachten Sie, dass sourceDevice herausgenommen wird, aber wir erwarten, dass PointerDeviceRect und DisplayRect die vorhandenen Anwendungsfälle von sourceDevice abdecken.</span><span class="sxs-lookup"><span data-stu-id="b5929-222">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="b5929-223">Ein weiterer großer Unterschied besteht darin, dass eine der Punkt-oder Rect-Positionen in WebView-physikalischen Koordinaten erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="b5929-223">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="b5929-224">Das heißt, Koordinaten relativ zum WebView und keine DPI-Skalierung angewendet.</span><span class="sxs-lookup"><span data-stu-id="b5929-224">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="b5929-225">Member</span><span class="sxs-lookup"><span data-stu-id="b5929-225">Members</span></span>

#### <span data-ttu-id="b5929-226">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="b5929-226">get_ButtonChangeKind</span></span> 

<span data-ttu-id="b5929-227">Rufen Sie die ButtonChangeKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-227">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="b5929-228">Public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(Int32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="b5929-228">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="b5929-229">Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-229">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="b5929-230">Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-230">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-231">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="b5929-231">get_DisplayRect</span></span> 

<span data-ttu-id="b5929-232">Rufen Sie die DisplayRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-232">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="b5929-233">Public HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="b5929-233">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="b5929-234">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="b5929-234">get_FrameId</span></span> 

<span data-ttu-id="b5929-235">Rufen Sie die Frame-Nr des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-235">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="b5929-236">Public HRESULT [get_FrameId](#get_frameid)(UInt32 \* Frame-Nr)</span><span class="sxs-lookup"><span data-stu-id="b5929-236">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="b5929-237">Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-237">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-238">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="b5929-238">get_HimetricLocation</span></span> 

<span data-ttu-id="b5929-239">Rufen Sie die HimetricLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-239">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="b5929-240">öffentliche HRESULT- [get_HimetricLocation](#get_himetriclocation)(Point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="b5929-240">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="b5929-241">Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-241">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-242">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b5929-242">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="b5929-243">Rufen Sie die HimetricLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-243">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="b5929-244">öffentliche HRESULT- [get_HimetricLocationRaw](#get_himetriclocationraw)(Point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="b5929-244">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="b5929-245">Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-245">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-246">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="b5929-246">get_HistoryCount</span></span> 

<span data-ttu-id="b5929-247">Rufen Sie die HistoryCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-247">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="b5929-248">Public HRESULT [get_HistoryCount](#get_historycount)(UInt32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="b5929-248">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="b5929-249">Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-249">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-250">get_InputData</span><span class="sxs-lookup"><span data-stu-id="b5929-250">get_InputData</span></span> 

<span data-ttu-id="b5929-251">Rufen Sie die inputData des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-251">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="b5929-252">Public HRESULT [get_InputData](#get_inputdata)(Int32 \* inputData)</span><span class="sxs-lookup"><span data-stu-id="b5929-252">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="b5929-253">Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-253">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-254">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="b5929-254">get_KeyStates</span></span> 

<span data-ttu-id="b5929-255">Rufen Sie die KeyStates des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-255">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="b5929-256">öffentliche HRESULT- [get_KeyStates](#get_keystates)(DWORD \*-KeyStates)</span><span class="sxs-lookup"><span data-stu-id="b5929-256">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="b5929-257">Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-257">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-258">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="b5929-258">get_PenFlags</span></span> 

<span data-ttu-id="b5929-259">Rufen Sie die PenFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-259">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="b5929-260">Public HRESULT [get_PenFlags](#get_penflags)(UInt32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="b5929-260">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="b5929-261">Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-261">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="b5929-262">Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-262">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-263">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="b5929-263">get_PenMask</span></span> 

<span data-ttu-id="b5929-264">Rufen Sie die PenMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-264">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="b5929-265">Public HRESULT [get_PenMask](#get_penmask)(UInt32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="b5929-265">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="b5929-266">Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-266">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="b5929-267">Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-267">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-268">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="b5929-268">get_PenPressure</span></span> 

<span data-ttu-id="b5929-269">Rufen Sie die PenPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-269">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="b5929-270">Public HRESULT [get_PenPressure](#get_penpressure)(UInt32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="b5929-270">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="b5929-271">Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-271">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-272">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="b5929-272">get_PenRotation</span></span> 

<span data-ttu-id="b5929-273">Rufen Sie die PenRotation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-273">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="b5929-274">Public HRESULT [get_PenRotation](#get_penrotation)(UInt32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="b5929-274">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="b5929-275">Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-275">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-276">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="b5929-276">get_PenTiltX</span></span> 

<span data-ttu-id="b5929-277">Rufen Sie die PenTiltX des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-277">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="b5929-278">Public HRESULT [get_PenTiltX](#get_pentiltx)(Int32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="b5929-278">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="b5929-279">Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-279">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-280">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="b5929-280">get_PenTiltY</span></span> 

<span data-ttu-id="b5929-281">Rufen Sie die PenTiltY des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-281">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="b5929-282">Public HRESULT [get_PenTiltY](#get_pentilty)(Int32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="b5929-282">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="b5929-283">Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-283">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-284">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="b5929-284">get_PerformanceCount</span></span> 

<span data-ttu-id="b5929-285">Rufen Sie die PerformanceCount des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-285">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="b5929-286">Public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="b5929-286">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="b5929-287">Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-287">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-288">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="b5929-288">get_PixelLocation</span></span> 

<span data-ttu-id="b5929-289">Rufen Sie die PixelLocation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-289">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="b5929-290">öffentliche HRESULT- [get_PixelLocation](#get_pixellocation)(Point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="b5929-290">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="b5929-291">Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-291">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-292">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b5929-292">get_PixelLocationRaw</span></span> 

<span data-ttu-id="b5929-293">Rufen Sie die PixelLocationRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-293">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="b5929-294">öffentliche HRESULT- [get_PixelLocationRaw](#get_pixellocationraw)(Point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="b5929-294">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="b5929-295">Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-295">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-296">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="b5929-296">get_PointerDeviceRect</span></span> 

<span data-ttu-id="b5929-297">Rufen Sie die PointerDeviceRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-297">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="b5929-298">Public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="b5929-298">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="b5929-299">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="b5929-299">get_PointerFlags</span></span> 

<span data-ttu-id="b5929-300">Rufen Sie die PointerFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-300">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="b5929-301">Public HRESULT [get_PointerFlags](#get_pointerflags)(UInt32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="b5929-301">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="b5929-302">Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-302">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="b5929-303">Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-303">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-304">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="b5929-304">get_PointerId</span></span> 

<span data-ttu-id="b5929-305">Rufen Sie die Zeiger-Nr. des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-305">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="b5929-306">öffentliche HRESULT- [get_PointerId](#get_pointerid)(UInt32 \* Pointer-Nr.)</span><span class="sxs-lookup"><span data-stu-id="b5929-306">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="b5929-307">Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-307">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-308">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="b5929-308">get_PointerKind</span></span> 

<span data-ttu-id="b5929-309">Rufen Sie die PointerKind des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-309">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="b5929-310">Public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="b5929-310">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="b5929-311">Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-311">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="b5929-312">Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-312">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="b5929-313">Unterstützt PT_PEN und PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="b5929-313">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="b5929-314">get_Time</span><span class="sxs-lookup"><span data-stu-id="b5929-314">get_Time</span></span> 

<span data-ttu-id="b5929-315">Rufen Sie die Uhrzeit des Zeiger Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-315">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="b5929-316">öffentliche HRESULT- [get_Time](#get_time)(DWORD \* Zeit)</span><span class="sxs-lookup"><span data-stu-id="b5929-316">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="b5929-317">Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-317">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-318">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="b5929-318">get_TouchContact</span></span> 

<span data-ttu-id="b5929-319">Rufen Sie die TouchContact des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-319">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="b5929-320">Public HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="b5929-320">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="b5929-321">Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-321">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-322">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="b5929-322">get_TouchContactRaw</span></span> 

<span data-ttu-id="b5929-323">Rufen Sie die TouchContactRaw des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-323">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="b5929-324">Public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="b5929-324">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="b5929-325">Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-325">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-326">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="b5929-326">get_TouchFlags</span></span> 

<span data-ttu-id="b5929-327">Rufen Sie die TouchFlags des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-327">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="b5929-328">Public HRESULT [get_TouchFlags](#get_touchflags)(UInt32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="b5929-328">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="b5929-329">Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-329">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="b5929-330">Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-330">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-331">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="b5929-331">get_TouchMask</span></span> 

<span data-ttu-id="b5929-332">Rufen Sie die TouchMask des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-332">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="b5929-333">Public HRESULT [get_TouchMask](#get_touchmask)(UInt32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="b5929-333">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="b5929-334">Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-334">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="b5929-335">Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-335">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-336">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="b5929-336">get_TouchOrientation</span></span> 

<span data-ttu-id="b5929-337">Rufen Sie die TouchOrientation des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-337">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="b5929-338">Public HRESULT [get_TouchOrientation](#get_touchorientation)(UInt32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="b5929-338">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="b5929-339">Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-339">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-340">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="b5929-340">get_TouchPressure</span></span> 

<span data-ttu-id="b5929-341">Rufen Sie die TouchPressure des Pointer-Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="b5929-341">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="b5929-342">Public HRESULT [get_TouchPressure](#get_touchpressure)(UInt32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="b5929-342">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="b5929-343">Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-343">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-344">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="b5929-344">put_ButtonChangeKind</span></span> 

<span data-ttu-id="b5929-345">Legt die ButtonChangeKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-345">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="b5929-346">Public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(Int32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="b5929-346">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="b5929-347">Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-347">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="b5929-348">Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-348">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-349">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="b5929-349">put_DisplayRect</span></span> 

<span data-ttu-id="b5929-350">Setzen Sie die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-350">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="b5929-351">Public HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="b5929-351">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="b5929-352">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="b5929-352">put_FrameId</span></span> 

<span data-ttu-id="b5929-353">Legt die Frame-Nr des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-353">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="b5929-354">Public HRESULT [put_FrameId](#put_frameid)(UInt32-Frame-Nr)</span><span class="sxs-lookup"><span data-stu-id="b5929-354">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="b5929-355">Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-355">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-356">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="b5929-356">put_HimetricLocation</span></span> 

<span data-ttu-id="b5929-357">Legt die HimetricLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-357">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="b5929-358">öffentliche HRESULT- [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="b5929-358">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="b5929-359">Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-359">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-360">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b5929-360">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="b5929-361">Legt die HimetricLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-361">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="b5929-362">öffentliche HRESULT- [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="b5929-362">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="b5929-363">Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-363">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-364">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="b5929-364">put_HistoryCount</span></span> 

<span data-ttu-id="b5929-365">Legt die HistoryCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-365">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="b5929-366">Public HRESULT [put_HistoryCount](#put_historycount)(UInt32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="b5929-366">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="b5929-367">Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-367">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-368">put_InputData</span><span class="sxs-lookup"><span data-stu-id="b5929-368">put_InputData</span></span> 

<span data-ttu-id="b5929-369">Legt die inputData des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-369">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="b5929-370">Public HRESULT [put_InputData](#put_inputdata)(Int32 inputData)</span><span class="sxs-lookup"><span data-stu-id="b5929-370">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="b5929-371">Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-371">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-372">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="b5929-372">put_KeyStates</span></span> 

<span data-ttu-id="b5929-373">Die KeyStates des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b5929-373">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="b5929-374">Public HRESULT [put_KeyStates](#put_keystates)(DWORD-KeyStates)</span><span class="sxs-lookup"><span data-stu-id="b5929-374">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="b5929-375">Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-375">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-376">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="b5929-376">put_PenFlags</span></span> 

<span data-ttu-id="b5929-377">Legt die PenFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-377">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="b5929-378">Public HRESULT [put_PenFlags](#put_penflags)(UInt32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="b5929-378">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="b5929-379">Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-379">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="b5929-380">Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-380">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-381">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="b5929-381">put_PenMask</span></span> 

<span data-ttu-id="b5929-382">Legt die PenMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-382">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="b5929-383">Public HRESULT [put_PenMask](#put_penmask)(UInt32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="b5929-383">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="b5929-384">Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-384">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="b5929-385">Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-385">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-386">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="b5929-386">put_PenPressure</span></span> 

<span data-ttu-id="b5929-387">Legt die PenPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-387">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="b5929-388">Public HRESULT [put_PenPressure](#put_penpressure)(UInt32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="b5929-388">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="b5929-389">Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-389">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-390">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="b5929-390">put_PenRotation</span></span> 

<span data-ttu-id="b5929-391">Legt die PenRotation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-391">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="b5929-392">Public HRESULT [put_PenRotation](#put_penrotation)(UInt32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="b5929-392">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="b5929-393">Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-393">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-394">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="b5929-394">put_PenTiltX</span></span> 

<span data-ttu-id="b5929-395">Legt die PenTiltX des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-395">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="b5929-396">Public HRESULT [put_PenTiltX](#put_pentiltx)(Int32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="b5929-396">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="b5929-397">Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-397">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-398">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="b5929-398">put_PenTiltY</span></span> 

<span data-ttu-id="b5929-399">Legt die PenTiltY des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-399">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="b5929-400">Public HRESULT [put_PenTiltY](#put_pentilty)(Int32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="b5929-400">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="b5929-401">Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-401">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-402">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="b5929-402">put_PerformanceCount</span></span> 

<span data-ttu-id="b5929-403">Legt die PerformanceCount des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-403">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="b5929-404">Public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="b5929-404">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="b5929-405">Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-405">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-406">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="b5929-406">put_PixelLocation</span></span> 

<span data-ttu-id="b5929-407">Legt die PixelLocation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-407">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="b5929-408">öffentliche HRESULT- [put_PixelLocation](#put_pixellocation)(Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="b5929-408">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="b5929-409">Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-409">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-410">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b5929-410">put_PixelLocationRaw</span></span> 

<span data-ttu-id="b5929-411">Legt die PixelLocationRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-411">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="b5929-412">öffentliche HRESULT- [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="b5929-412">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="b5929-413">Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-413">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-414">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="b5929-414">put_PointerDeviceRect</span></span> 

<span data-ttu-id="b5929-415">Setzen Sie die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-415">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="b5929-416">Public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="b5929-416">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="b5929-417">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="b5929-417">put_PointerFlags</span></span> 

<span data-ttu-id="b5929-418">Legt die PointerFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-418">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="b5929-419">Public HRESULT [put_PointerFlags](#put_pointerflags)(UInt32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="b5929-419">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="b5929-420">Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-420">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="b5929-421">Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-421">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-422">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="b5929-422">put_PointerId</span></span> 

<span data-ttu-id="b5929-423">Die Zeiger-Nr. des Pointer-Ereignisses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b5929-423">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="b5929-424">Public HRESULT [put_PointerId](#put_pointerid)(UInt32-Zeiger-Nr.)</span><span class="sxs-lookup"><span data-stu-id="b5929-424">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="b5929-425">Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-425">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-426">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="b5929-426">put_PointerKind</span></span> 

<span data-ttu-id="b5929-427">Legt die PointerKind des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-427">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="b5929-428">Public HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="b5929-428">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="b5929-429">Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-429">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="b5929-430">Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-430">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="b5929-431">Unterstützt PT_PEN und PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="b5929-431">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="b5929-432">put_Time</span><span class="sxs-lookup"><span data-stu-id="b5929-432">put_Time</span></span> 

<span data-ttu-id="b5929-433">Legt die Uhrzeit des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-433">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="b5929-434">Public HRESULT [put_Time](#put_time)(DWORD-Zeit)</span><span class="sxs-lookup"><span data-stu-id="b5929-434">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="b5929-435">Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-435">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-436">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="b5929-436">put_TouchContact</span></span> 

<span data-ttu-id="b5929-437">Legt die TouchContact des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-437">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="b5929-438">Public HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="b5929-438">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="b5929-439">Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-439">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-440">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="b5929-440">put_TouchContactRaw</span></span> 

<span data-ttu-id="b5929-441">Legt die TouchContactRaw des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-441">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="b5929-442">Public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="b5929-442">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="b5929-443">Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-443">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-444">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="b5929-444">put_TouchFlags</span></span> 

<span data-ttu-id="b5929-445">Legt die TouchFlags des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-445">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="b5929-446">Public HRESULT [put_TouchFlags](#put_touchflags)(UInt32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="b5929-446">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="b5929-447">Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-447">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="b5929-448">Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-448">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-449">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="b5929-449">put_TouchMask</span></span> 

<span data-ttu-id="b5929-450">Legt die TouchMask des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-450">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="b5929-451">Public HRESULT [put_TouchMask](#put_touchmask)(UInt32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="b5929-451">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="b5929-452">Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5929-452">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="b5929-453">Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="b5929-453">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-454">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="b5929-454">put_TouchOrientation</span></span> 

<span data-ttu-id="b5929-455">Legt die TouchOrientation des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-455">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="b5929-456">Public HRESULT [put_TouchOrientation](#put_touchorientation)(UInt32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="b5929-456">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="b5929-457">Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-457">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b5929-458">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="b5929-458">put_TouchPressure</span></span> 

<span data-ttu-id="b5929-459">Legt die TouchPressure des Zeiger Ereignisses fest.</span><span class="sxs-lookup"><span data-stu-id="b5929-459">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="b5929-460">Public HRESULT [put_TouchPressure](#put_touchpressure)(UInt32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="b5929-460">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="b5929-461">Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b5929-461">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


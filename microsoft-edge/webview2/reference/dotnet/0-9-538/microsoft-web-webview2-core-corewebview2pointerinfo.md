---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
ms.openlocfilehash: 8a5e5f4188b5115e1c6b836f80aad69c4bf2da7e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878758"
---
# <span data-ttu-id="502e9-104">Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo Klasse</span><span class="sxs-lookup"><span data-stu-id="502e9-104">Microsoft.Web.WebView2.Core.CoreWebView2PointerInfo class</span></span> 

<span data-ttu-id="502e9-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="502e9-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="502e9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="502e9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="502e9-107">Dies stellt in erster Linie ein kombiniertes Win32-POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="502e9-107">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="502e9-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="502e9-108">Summary</span></span>

 <span data-ttu-id="502e9-109">Member</span><span class="sxs-lookup"><span data-stu-id="502e9-109">Members</span></span>                        | <span data-ttu-id="502e9-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="502e9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="502e9-111">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="502e9-111">ButtonChangeKind</span></span>](#buttonchangekind) | <span data-ttu-id="502e9-112">Die ButtonChangeKind des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-112">The ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="502e9-113">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="502e9-113">DisplayRect</span></span>](#displayrect) | <span data-ttu-id="502e9-114">Die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-114">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="502e9-115">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="502e9-115">FrameId</span></span>](#frameid) | <span data-ttu-id="502e9-116">Die Frame-Nr des Pointer-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-116">The FrameID of the pointer event.</span></span>
[<span data-ttu-id="502e9-117">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="502e9-117">HimetricLocation</span></span>](#himetriclocation) | <span data-ttu-id="502e9-118">Die HimetricLocation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-118">The HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="502e9-119">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="502e9-119">HimetricLocationRaw</span></span>](#himetriclocationraw) | <span data-ttu-id="502e9-120">Die HimetricLocationRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-120">The HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="502e9-121">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="502e9-121">HistoryCount</span></span>](#historycount) | <span data-ttu-id="502e9-122">Die HistoryCount des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-122">The HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="502e9-123">InputData</span><span class="sxs-lookup"><span data-stu-id="502e9-123">InputData</span></span>](#inputdata) | <span data-ttu-id="502e9-124">Die inputData des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-124">The InputData of the pointer event.</span></span>
[<span data-ttu-id="502e9-125">KeyStates</span><span class="sxs-lookup"><span data-stu-id="502e9-125">KeyStates</span></span>](#keystates) | <span data-ttu-id="502e9-126">Die KeyStates des Pointer-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-126">The KeyStates of the pointer event.</span></span>
[<span data-ttu-id="502e9-127">PenFlags</span><span class="sxs-lookup"><span data-stu-id="502e9-127">PenFlags</span></span>](#penflags) | <span data-ttu-id="502e9-128">Die PenFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-128">The PenFlags of the pointer event.</span></span>
[<span data-ttu-id="502e9-129">PenMask</span><span class="sxs-lookup"><span data-stu-id="502e9-129">PenMask</span></span>](#penmask) | <span data-ttu-id="502e9-130">Die PenMask des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-130">The PenMask of the pointer event.</span></span>
[<span data-ttu-id="502e9-131">PenPressure</span><span class="sxs-lookup"><span data-stu-id="502e9-131">PenPressure</span></span>](#penpressure) | <span data-ttu-id="502e9-132">Die PenPressure des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-132">The PenPressure of the pointer event.</span></span>
[<span data-ttu-id="502e9-133">PenRotation</span><span class="sxs-lookup"><span data-stu-id="502e9-133">PenRotation</span></span>](#penrotation) | <span data-ttu-id="502e9-134">Die PenRotation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-134">The PenRotation of the pointer event.</span></span>
[<span data-ttu-id="502e9-135">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="502e9-135">PenTiltX</span></span>](#pentiltx) | <span data-ttu-id="502e9-136">Die PenTiltX des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-136">The PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="502e9-137">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="502e9-137">PenTiltY</span></span>](#pentilty) | <span data-ttu-id="502e9-138">Die PenTiltY des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-138">The PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="502e9-139">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="502e9-139">PerformanceCount</span></span>](#performancecount) | <span data-ttu-id="502e9-140">Die PerformanceCount des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-140">The PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="502e9-141">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="502e9-141">PixelLocation</span></span>](#pixellocation) | <span data-ttu-id="502e9-142">Die PixelLocation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-142">The PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="502e9-143">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="502e9-143">PixelLocationRaw</span></span>](#pixellocationraw) | <span data-ttu-id="502e9-144">Die PixelLocationRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-144">The PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="502e9-145">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="502e9-145">PointerDeviceRect</span></span>](#pointerdevicerect) | <span data-ttu-id="502e9-146">Die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-146">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="502e9-147">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="502e9-147">PointerFlags</span></span>](#pointerflags) | <span data-ttu-id="502e9-148">Die PointerFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-148">The PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="502e9-149">Zeiger-Nr</span><span class="sxs-lookup"><span data-stu-id="502e9-149">PointerId</span></span>](#pointerid) | <span data-ttu-id="502e9-150">Die Zeiger-Nr des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-150">The PointerId of the pointer event.</span></span>
[<span data-ttu-id="502e9-151">PointerKind</span><span class="sxs-lookup"><span data-stu-id="502e9-151">PointerKind</span></span>](#pointerkind) | <span data-ttu-id="502e9-152">Die PointerKind des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-152">The PointerKind of the pointer event.</span></span>
[<span data-ttu-id="502e9-153">Zeit</span><span class="sxs-lookup"><span data-stu-id="502e9-153">Time</span></span>](#time) | <span data-ttu-id="502e9-154">Die Uhrzeit des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-154">The Time of the pointer event.</span></span>
[<span data-ttu-id="502e9-155">TouchContact</span><span class="sxs-lookup"><span data-stu-id="502e9-155">TouchContact</span></span>](#touchcontact) | <span data-ttu-id="502e9-156">Die TouchContact des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-156">The TouchContact of the pointer event.</span></span>
[<span data-ttu-id="502e9-157">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="502e9-157">TouchContactRaw</span></span>](#touchcontactraw) | <span data-ttu-id="502e9-158">Die TouchContactRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-158">The TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="502e9-159">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="502e9-159">TouchFlags</span></span>](#touchflags) | <span data-ttu-id="502e9-160">Die TouchFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-160">The TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="502e9-161">TouchMask</span><span class="sxs-lookup"><span data-stu-id="502e9-161">TouchMask</span></span>](#touchmask) | <span data-ttu-id="502e9-162">Die TouchMask des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-162">The TouchMask of the pointer event.</span></span>
[<span data-ttu-id="502e9-163">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="502e9-163">TouchOrientation</span></span>](#touchorientation) | <span data-ttu-id="502e9-164">Die TouchOrientation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-164">The TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="502e9-165">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="502e9-165">TouchPressure</span></span>](#touchpressure) | <span data-ttu-id="502e9-166">Die TouchPressure des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-166">The TouchPressure of the pointer event.</span></span>

## <span data-ttu-id="502e9-167">Member</span><span class="sxs-lookup"><span data-stu-id="502e9-167">Members</span></span>

#### <span data-ttu-id="502e9-168">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="502e9-168">ButtonChangeKind</span></span> 

<span data-ttu-id="502e9-169">Die ButtonChangeKind des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-169">The ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="502e9-170">public int [ButtonChangeKind](#buttonchangekind)</span><span class="sxs-lookup"><span data-stu-id="502e9-170">public int [ButtonChangeKind](#buttonchangekind)</span></span>

<span data-ttu-id="502e9-171">Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="502e9-171">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="502e9-172">Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="502e9-172">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-173">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="502e9-173">DisplayRect</span></span> 

<span data-ttu-id="502e9-174">Die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-174">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="502e9-175">öffentliche Rect- [DisplayRect](#displayrect)</span><span class="sxs-lookup"><span data-stu-id="502e9-175">public Rect [DisplayRect](#displayrect)</span></span>

#### <span data-ttu-id="502e9-176">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="502e9-176">FrameId</span></span> 

<span data-ttu-id="502e9-177">Die Frame-Nr des Pointer-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-177">The FrameID of the pointer event.</span></span>

> <span data-ttu-id="502e9-178">öffentliche uint- [Frame](#frameid) -Nr</span><span class="sxs-lookup"><span data-stu-id="502e9-178">public uint [FrameId](#frameid)</span></span>

<span data-ttu-id="502e9-179">Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-179">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-180">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="502e9-180">HimetricLocation</span></span> 

<span data-ttu-id="502e9-181">Die HimetricLocation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-181">The HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="502e9-182">öffentlicher Punkt [HimetricLocation](#himetriclocation)</span><span class="sxs-lookup"><span data-stu-id="502e9-182">public Point [HimetricLocation](#himetriclocation)</span></span>

<span data-ttu-id="502e9-183">Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-183">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-184">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="502e9-184">HimetricLocationRaw</span></span> 

<span data-ttu-id="502e9-185">Die HimetricLocationRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-185">The HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="502e9-186">öffentlicher Punkt [HimetricLocationRaw](#himetriclocationraw)</span><span class="sxs-lookup"><span data-stu-id="502e9-186">public Point [HimetricLocationRaw](#himetriclocationraw)</span></span>

<span data-ttu-id="502e9-187">Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-187">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-188">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="502e9-188">HistoryCount</span></span> 

<span data-ttu-id="502e9-189">Die HistoryCount des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-189">The HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="502e9-190">public uint [HistoryCount](#historycount)</span><span class="sxs-lookup"><span data-stu-id="502e9-190">public uint [HistoryCount](#historycount)</span></span>

<span data-ttu-id="502e9-191">Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-191">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-192">InputData</span><span class="sxs-lookup"><span data-stu-id="502e9-192">InputData</span></span> 

<span data-ttu-id="502e9-193">Die inputData des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-193">The InputData of the pointer event.</span></span>

> <span data-ttu-id="502e9-194">public int [inputData](#inputdata)</span><span class="sxs-lookup"><span data-stu-id="502e9-194">public int [InputData](#inputdata)</span></span>

<span data-ttu-id="502e9-195">Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-195">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-196">KeyStates</span><span class="sxs-lookup"><span data-stu-id="502e9-196">KeyStates</span></span> 

<span data-ttu-id="502e9-197">Die KeyStates des Pointer-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-197">The KeyStates of the pointer event.</span></span>

> <span data-ttu-id="502e9-198">öffentliche uint- [KeyStates](#keystates)</span><span class="sxs-lookup"><span data-stu-id="502e9-198">public uint [KeyStates](#keystates)</span></span>

<span data-ttu-id="502e9-199">Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-199">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-200">PenFlags</span><span class="sxs-lookup"><span data-stu-id="502e9-200">PenFlags</span></span> 

<span data-ttu-id="502e9-201">Die PenFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-201">The PenFlags of the pointer event.</span></span>

> <span data-ttu-id="502e9-202">public uint [PenFlags](#penflags)</span><span class="sxs-lookup"><span data-stu-id="502e9-202">public uint [PenFlags](#penflags)</span></span>

<span data-ttu-id="502e9-203">Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="502e9-203">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="502e9-204">Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="502e9-204">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-205">PenMask</span><span class="sxs-lookup"><span data-stu-id="502e9-205">PenMask</span></span> 

<span data-ttu-id="502e9-206">Die PenMask des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-206">The PenMask of the pointer event.</span></span>

> <span data-ttu-id="502e9-207">public uint [PenMask](#penmask)</span><span class="sxs-lookup"><span data-stu-id="502e9-207">public uint [PenMask](#penmask)</span></span>

<span data-ttu-id="502e9-208">Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="502e9-208">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="502e9-209">Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="502e9-209">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-210">PenPressure</span><span class="sxs-lookup"><span data-stu-id="502e9-210">PenPressure</span></span> 

<span data-ttu-id="502e9-211">Die PenPressure des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-211">The PenPressure of the pointer event.</span></span>

> <span data-ttu-id="502e9-212">public uint [PenPressure](#penpressure)</span><span class="sxs-lookup"><span data-stu-id="502e9-212">public uint [PenPressure](#penpressure)</span></span>

<span data-ttu-id="502e9-213">Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-213">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-214">PenRotation</span><span class="sxs-lookup"><span data-stu-id="502e9-214">PenRotation</span></span> 

<span data-ttu-id="502e9-215">Die PenRotation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-215">The PenRotation of the pointer event.</span></span>

> <span data-ttu-id="502e9-216">public uint [PenRotation](#penrotation)</span><span class="sxs-lookup"><span data-stu-id="502e9-216">public uint [PenRotation](#penrotation)</span></span>

<span data-ttu-id="502e9-217">Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-217">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-218">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="502e9-218">PenTiltX</span></span> 

<span data-ttu-id="502e9-219">Die PenTiltX des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-219">The PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="502e9-220">public int [PenTiltX](#pentiltx)</span><span class="sxs-lookup"><span data-stu-id="502e9-220">public int [PenTiltX](#pentiltx)</span></span>

<span data-ttu-id="502e9-221">Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-221">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-222">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="502e9-222">PenTiltY</span></span> 

<span data-ttu-id="502e9-223">Die PenTiltY des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-223">The PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="502e9-224">public int [PenTiltY](#pentilty)</span><span class="sxs-lookup"><span data-stu-id="502e9-224">public int [PenTiltY](#pentilty)</span></span>

<span data-ttu-id="502e9-225">Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-225">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-226">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="502e9-226">PerformanceCount</span></span> 

<span data-ttu-id="502e9-227">Die PerformanceCount des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-227">The PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="502e9-228">Public ULONG [PerformanceCount](#performancecount)</span><span class="sxs-lookup"><span data-stu-id="502e9-228">public ulong [PerformanceCount](#performancecount)</span></span>

<span data-ttu-id="502e9-229">Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-229">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-230">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="502e9-230">PixelLocation</span></span> 

<span data-ttu-id="502e9-231">Die PixelLocation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-231">The PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="502e9-232">öffentlicher Punkt [PixelLocation](#pixellocation)</span><span class="sxs-lookup"><span data-stu-id="502e9-232">public Point [PixelLocation](#pixellocation)</span></span>

<span data-ttu-id="502e9-233">Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-233">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-234">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="502e9-234">PixelLocationRaw</span></span> 

<span data-ttu-id="502e9-235">Die PixelLocationRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-235">The PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="502e9-236">öffentlicher Punkt [PixelLocationRaw](#pixellocationraw)</span><span class="sxs-lookup"><span data-stu-id="502e9-236">public Point [PixelLocationRaw](#pixellocationraw)</span></span>

<span data-ttu-id="502e9-237">Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-237">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-238">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="502e9-238">PointerDeviceRect</span></span> 

<span data-ttu-id="502e9-239">Die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-239">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="502e9-240">öffentliche Rect- [PointerDeviceRect](#pointerdevicerect)</span><span class="sxs-lookup"><span data-stu-id="502e9-240">public Rect [PointerDeviceRect](#pointerdevicerect)</span></span>

#### <span data-ttu-id="502e9-241">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="502e9-241">PointerFlags</span></span> 

<span data-ttu-id="502e9-242">Die PointerFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-242">The PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="502e9-243">public uint [PointerFlags](#pointerflags)</span><span class="sxs-lookup"><span data-stu-id="502e9-243">public uint [PointerFlags](#pointerflags)</span></span>

<span data-ttu-id="502e9-244">Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="502e9-244">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="502e9-245">Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="502e9-245">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-246">Zeiger-Nr</span><span class="sxs-lookup"><span data-stu-id="502e9-246">PointerId</span></span> 

<span data-ttu-id="502e9-247">Die Zeiger-Nr des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-247">The PointerId of the pointer event.</span></span>

> <span data-ttu-id="502e9-248">öffentliche uint- [Zeiger](#pointerid) -Nr</span><span class="sxs-lookup"><span data-stu-id="502e9-248">public uint [PointerId](#pointerid)</span></span>

<span data-ttu-id="502e9-249">Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-249">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-250">PointerKind</span><span class="sxs-lookup"><span data-stu-id="502e9-250">PointerKind</span></span> 

<span data-ttu-id="502e9-251">Die PointerKind des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-251">The PointerKind of the pointer event.</span></span>

> <span data-ttu-id="502e9-252">public uint [PointerKind](#pointerkind)</span><span class="sxs-lookup"><span data-stu-id="502e9-252">public uint [PointerKind](#pointerkind)</span></span>

<span data-ttu-id="502e9-253">Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="502e9-253">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="502e9-254">Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="502e9-254">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="502e9-255">Unterstützt PT_PEN und PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="502e9-255">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="502e9-256">Zeit</span><span class="sxs-lookup"><span data-stu-id="502e9-256">Time</span></span> 

<span data-ttu-id="502e9-257">Die Uhrzeit des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-257">The Time of the pointer event.</span></span>

> <span data-ttu-id="502e9-258">öffentliche uint- [Zeit](#time)</span><span class="sxs-lookup"><span data-stu-id="502e9-258">public uint [Time](#time)</span></span>

<span data-ttu-id="502e9-259">Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-259">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-260">TouchContact</span><span class="sxs-lookup"><span data-stu-id="502e9-260">TouchContact</span></span> 

<span data-ttu-id="502e9-261">Die TouchContact des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-261">The TouchContact of the pointer event.</span></span>

> <span data-ttu-id="502e9-262">öffentliche Rect- [TouchContact](#touchcontact)</span><span class="sxs-lookup"><span data-stu-id="502e9-262">public Rect [TouchContact](#touchcontact)</span></span>

<span data-ttu-id="502e9-263">Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-263">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-264">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="502e9-264">TouchContactRaw</span></span> 

<span data-ttu-id="502e9-265">Die TouchContactRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-265">The TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="502e9-266">öffentliche Rect- [TouchContactRaw](#touchcontactraw)</span><span class="sxs-lookup"><span data-stu-id="502e9-266">public Rect [TouchContactRaw](#touchcontactraw)</span></span>

<span data-ttu-id="502e9-267">Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-267">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-268">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="502e9-268">TouchFlags</span></span> 

<span data-ttu-id="502e9-269">Die TouchFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-269">The TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="502e9-270">public uint [TouchFlags](#touchflags)</span><span class="sxs-lookup"><span data-stu-id="502e9-270">public uint [TouchFlags](#touchflags)</span></span>

<span data-ttu-id="502e9-271">Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="502e9-271">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="502e9-272">Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="502e9-272">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-273">TouchMask</span><span class="sxs-lookup"><span data-stu-id="502e9-273">TouchMask</span></span> 

<span data-ttu-id="502e9-274">Die TouchMask des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-274">The TouchMask of the pointer event.</span></span>

> <span data-ttu-id="502e9-275">public uint [TouchMask](#touchmask)</span><span class="sxs-lookup"><span data-stu-id="502e9-275">public uint [TouchMask](#touchmask)</span></span>

<span data-ttu-id="502e9-276">Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="502e9-276">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="502e9-277">Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="502e9-277">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-278">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="502e9-278">TouchOrientation</span></span> 

<span data-ttu-id="502e9-279">Die TouchOrientation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-279">The TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="502e9-280">public uint [TouchOrientation](#touchorientation)</span><span class="sxs-lookup"><span data-stu-id="502e9-280">public uint [TouchOrientation](#touchorientation)</span></span>

<span data-ttu-id="502e9-281">Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-281">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="502e9-282">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="502e9-282">TouchPressure</span></span> 

<span data-ttu-id="502e9-283">Die TouchPressure des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="502e9-283">The TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="502e9-284">public uint [TouchPressure](#touchpressure)</span><span class="sxs-lookup"><span data-stu-id="502e9-284">public uint [TouchPressure](#touchpressure)</span></span>

<span data-ttu-id="502e9-285">Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="502e9-285">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


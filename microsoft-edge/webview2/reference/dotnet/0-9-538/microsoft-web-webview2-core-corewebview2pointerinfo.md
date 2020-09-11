---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
ms.openlocfilehash: 9ce4c9c3f076d54f03295ffda84c5fb0f03b4166
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010901"
---
# <span data-ttu-id="fc421-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo Klasse</span><span class="sxs-lookup"><span data-stu-id="fc421-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2PointerInfo class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="fc421-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="fc421-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="fc421-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="fc421-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="fc421-107">Dies stellt in erster Linie ein kombiniertes Win32-POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="fc421-107">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="fc421-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fc421-108">Summary</span></span>

 <span data-ttu-id="fc421-109">Member</span><span class="sxs-lookup"><span data-stu-id="fc421-109">Members</span></span>                        | <span data-ttu-id="fc421-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="fc421-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fc421-111">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="fc421-111">ButtonChangeKind</span></span>](#buttonchangekind) | <span data-ttu-id="fc421-112">Die ButtonChangeKind des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-112">The ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="fc421-113">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="fc421-113">DisplayRect</span></span>](#displayrect) | <span data-ttu-id="fc421-114">Die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-114">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="fc421-115">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="fc421-115">FrameId</span></span>](#frameid) | <span data-ttu-id="fc421-116">Die Frame-Nr des Pointer-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-116">The FrameID of the pointer event.</span></span>
[<span data-ttu-id="fc421-117">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="fc421-117">HimetricLocation</span></span>](#himetriclocation) | <span data-ttu-id="fc421-118">Die HimetricLocation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-118">The HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="fc421-119">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="fc421-119">HimetricLocationRaw</span></span>](#himetriclocationraw) | <span data-ttu-id="fc421-120">Die HimetricLocationRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-120">The HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="fc421-121">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="fc421-121">HistoryCount</span></span>](#historycount) | <span data-ttu-id="fc421-122">Die HistoryCount des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-122">The HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="fc421-123">InputData</span><span class="sxs-lookup"><span data-stu-id="fc421-123">InputData</span></span>](#inputdata) | <span data-ttu-id="fc421-124">Die inputData des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-124">The InputData of the pointer event.</span></span>
[<span data-ttu-id="fc421-125">KeyStates</span><span class="sxs-lookup"><span data-stu-id="fc421-125">KeyStates</span></span>](#keystates) | <span data-ttu-id="fc421-126">Die KeyStates des Pointer-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-126">The KeyStates of the pointer event.</span></span>
[<span data-ttu-id="fc421-127">PenFlags</span><span class="sxs-lookup"><span data-stu-id="fc421-127">PenFlags</span></span>](#penflags) | <span data-ttu-id="fc421-128">Die PenFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-128">The PenFlags of the pointer event.</span></span>
[<span data-ttu-id="fc421-129">PenMask</span><span class="sxs-lookup"><span data-stu-id="fc421-129">PenMask</span></span>](#penmask) | <span data-ttu-id="fc421-130">Die PenMask des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-130">The PenMask of the pointer event.</span></span>
[<span data-ttu-id="fc421-131">PenPressure</span><span class="sxs-lookup"><span data-stu-id="fc421-131">PenPressure</span></span>](#penpressure) | <span data-ttu-id="fc421-132">Die PenPressure des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-132">The PenPressure of the pointer event.</span></span>
[<span data-ttu-id="fc421-133">PenRotation</span><span class="sxs-lookup"><span data-stu-id="fc421-133">PenRotation</span></span>](#penrotation) | <span data-ttu-id="fc421-134">Die PenRotation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-134">The PenRotation of the pointer event.</span></span>
[<span data-ttu-id="fc421-135">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="fc421-135">PenTiltX</span></span>](#pentiltx) | <span data-ttu-id="fc421-136">Die PenTiltX des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-136">The PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="fc421-137">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="fc421-137">PenTiltY</span></span>](#pentilty) | <span data-ttu-id="fc421-138">Die PenTiltY des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-138">The PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="fc421-139">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="fc421-139">PerformanceCount</span></span>](#performancecount) | <span data-ttu-id="fc421-140">Die PerformanceCount des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-140">The PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="fc421-141">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="fc421-141">PixelLocation</span></span>](#pixellocation) | <span data-ttu-id="fc421-142">Die PixelLocation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-142">The PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="fc421-143">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="fc421-143">PixelLocationRaw</span></span>](#pixellocationraw) | <span data-ttu-id="fc421-144">Die PixelLocationRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-144">The PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="fc421-145">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="fc421-145">PointerDeviceRect</span></span>](#pointerdevicerect) | <span data-ttu-id="fc421-146">Die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-146">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="fc421-147">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="fc421-147">PointerFlags</span></span>](#pointerflags) | <span data-ttu-id="fc421-148">Die PointerFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-148">The PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="fc421-149">Zeiger-Nr</span><span class="sxs-lookup"><span data-stu-id="fc421-149">PointerId</span></span>](#pointerid) | <span data-ttu-id="fc421-150">Die Zeiger-Nr des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-150">The PointerId of the pointer event.</span></span>
[<span data-ttu-id="fc421-151">PointerKind</span><span class="sxs-lookup"><span data-stu-id="fc421-151">PointerKind</span></span>](#pointerkind) | <span data-ttu-id="fc421-152">Die PointerKind des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-152">The PointerKind of the pointer event.</span></span>
[<span data-ttu-id="fc421-153">Zeit</span><span class="sxs-lookup"><span data-stu-id="fc421-153">Time</span></span>](#time) | <span data-ttu-id="fc421-154">Die Uhrzeit des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-154">The Time of the pointer event.</span></span>
[<span data-ttu-id="fc421-155">TouchContact</span><span class="sxs-lookup"><span data-stu-id="fc421-155">TouchContact</span></span>](#touchcontact) | <span data-ttu-id="fc421-156">Die TouchContact des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-156">The TouchContact of the pointer event.</span></span>
[<span data-ttu-id="fc421-157">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="fc421-157">TouchContactRaw</span></span>](#touchcontactraw) | <span data-ttu-id="fc421-158">Die TouchContactRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-158">The TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="fc421-159">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="fc421-159">TouchFlags</span></span>](#touchflags) | <span data-ttu-id="fc421-160">Die TouchFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-160">The TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="fc421-161">TouchMask</span><span class="sxs-lookup"><span data-stu-id="fc421-161">TouchMask</span></span>](#touchmask) | <span data-ttu-id="fc421-162">Die TouchMask des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-162">The TouchMask of the pointer event.</span></span>
[<span data-ttu-id="fc421-163">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="fc421-163">TouchOrientation</span></span>](#touchorientation) | <span data-ttu-id="fc421-164">Die TouchOrientation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-164">The TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="fc421-165">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="fc421-165">TouchPressure</span></span>](#touchpressure) | <span data-ttu-id="fc421-166">Die TouchPressure des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-166">The TouchPressure of the pointer event.</span></span>

## <span data-ttu-id="fc421-167">Member</span><span class="sxs-lookup"><span data-stu-id="fc421-167">Members</span></span>

#### <span data-ttu-id="fc421-168">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="fc421-168">ButtonChangeKind</span></span> 

<span data-ttu-id="fc421-169">Die ButtonChangeKind des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-169">The ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="fc421-170">public int [ButtonChangeKind](#buttonchangekind)</span><span class="sxs-lookup"><span data-stu-id="fc421-170">public int [ButtonChangeKind](#buttonchangekind)</span></span>

<span data-ttu-id="fc421-171">Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="fc421-171">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="fc421-172">Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="fc421-172">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-173">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="fc421-173">DisplayRect</span></span> 

<span data-ttu-id="fc421-174">Die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-174">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="fc421-175">öffentliche Rect- [DisplayRect](#displayrect)</span><span class="sxs-lookup"><span data-stu-id="fc421-175">public Rect [DisplayRect](#displayrect)</span></span>

#### <span data-ttu-id="fc421-176">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="fc421-176">FrameId</span></span> 

<span data-ttu-id="fc421-177">Die Frame-Nr des Pointer-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-177">The FrameID of the pointer event.</span></span>

> <span data-ttu-id="fc421-178">öffentliche uint- [Frame](#frameid) -Nr</span><span class="sxs-lookup"><span data-stu-id="fc421-178">public uint [FrameId](#frameid)</span></span>

<span data-ttu-id="fc421-179">Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-179">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-180">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="fc421-180">HimetricLocation</span></span> 

<span data-ttu-id="fc421-181">Die HimetricLocation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-181">The HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="fc421-182">öffentlicher Punkt [HimetricLocation](#himetriclocation)</span><span class="sxs-lookup"><span data-stu-id="fc421-182">public Point [HimetricLocation](#himetriclocation)</span></span>

<span data-ttu-id="fc421-183">Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-183">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-184">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="fc421-184">HimetricLocationRaw</span></span> 

<span data-ttu-id="fc421-185">Die HimetricLocationRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-185">The HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="fc421-186">öffentlicher Punkt [HimetricLocationRaw](#himetriclocationraw)</span><span class="sxs-lookup"><span data-stu-id="fc421-186">public Point [HimetricLocationRaw](#himetriclocationraw)</span></span>

<span data-ttu-id="fc421-187">Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-187">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-188">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="fc421-188">HistoryCount</span></span> 

<span data-ttu-id="fc421-189">Die HistoryCount des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-189">The HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="fc421-190">public uint [HistoryCount](#historycount)</span><span class="sxs-lookup"><span data-stu-id="fc421-190">public uint [HistoryCount](#historycount)</span></span>

<span data-ttu-id="fc421-191">Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-191">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-192">InputData</span><span class="sxs-lookup"><span data-stu-id="fc421-192">InputData</span></span> 

<span data-ttu-id="fc421-193">Die inputData des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-193">The InputData of the pointer event.</span></span>

> <span data-ttu-id="fc421-194">public int [inputData](#inputdata)</span><span class="sxs-lookup"><span data-stu-id="fc421-194">public int [InputData](#inputdata)</span></span>

<span data-ttu-id="fc421-195">Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-195">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-196">KeyStates</span><span class="sxs-lookup"><span data-stu-id="fc421-196">KeyStates</span></span> 

<span data-ttu-id="fc421-197">Die KeyStates des Pointer-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-197">The KeyStates of the pointer event.</span></span>

> <span data-ttu-id="fc421-198">öffentliche uint- [KeyStates](#keystates)</span><span class="sxs-lookup"><span data-stu-id="fc421-198">public uint [KeyStates](#keystates)</span></span>

<span data-ttu-id="fc421-199">Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-199">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-200">PenFlags</span><span class="sxs-lookup"><span data-stu-id="fc421-200">PenFlags</span></span> 

<span data-ttu-id="fc421-201">Die PenFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-201">The PenFlags of the pointer event.</span></span>

> <span data-ttu-id="fc421-202">public uint [PenFlags](#penflags)</span><span class="sxs-lookup"><span data-stu-id="fc421-202">public uint [PenFlags](#penflags)</span></span>

<span data-ttu-id="fc421-203">Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="fc421-203">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="fc421-204">Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="fc421-204">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-205">PenMask</span><span class="sxs-lookup"><span data-stu-id="fc421-205">PenMask</span></span> 

<span data-ttu-id="fc421-206">Die PenMask des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-206">The PenMask of the pointer event.</span></span>

> <span data-ttu-id="fc421-207">public uint [PenMask](#penmask)</span><span class="sxs-lookup"><span data-stu-id="fc421-207">public uint [PenMask](#penmask)</span></span>

<span data-ttu-id="fc421-208">Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="fc421-208">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="fc421-209">Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="fc421-209">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-210">PenPressure</span><span class="sxs-lookup"><span data-stu-id="fc421-210">PenPressure</span></span> 

<span data-ttu-id="fc421-211">Die PenPressure des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-211">The PenPressure of the pointer event.</span></span>

> <span data-ttu-id="fc421-212">public uint [PenPressure](#penpressure)</span><span class="sxs-lookup"><span data-stu-id="fc421-212">public uint [PenPressure](#penpressure)</span></span>

<span data-ttu-id="fc421-213">Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-213">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-214">PenRotation</span><span class="sxs-lookup"><span data-stu-id="fc421-214">PenRotation</span></span> 

<span data-ttu-id="fc421-215">Die PenRotation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-215">The PenRotation of the pointer event.</span></span>

> <span data-ttu-id="fc421-216">public uint [PenRotation](#penrotation)</span><span class="sxs-lookup"><span data-stu-id="fc421-216">public uint [PenRotation](#penrotation)</span></span>

<span data-ttu-id="fc421-217">Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-217">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-218">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="fc421-218">PenTiltX</span></span> 

<span data-ttu-id="fc421-219">Die PenTiltX des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-219">The PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="fc421-220">public int [PenTiltX](#pentiltx)</span><span class="sxs-lookup"><span data-stu-id="fc421-220">public int [PenTiltX](#pentiltx)</span></span>

<span data-ttu-id="fc421-221">Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-221">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-222">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="fc421-222">PenTiltY</span></span> 

<span data-ttu-id="fc421-223">Die PenTiltY des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-223">The PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="fc421-224">public int [PenTiltY](#pentilty)</span><span class="sxs-lookup"><span data-stu-id="fc421-224">public int [PenTiltY](#pentilty)</span></span>

<span data-ttu-id="fc421-225">Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-225">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-226">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="fc421-226">PerformanceCount</span></span> 

<span data-ttu-id="fc421-227">Die PerformanceCount des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-227">The PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="fc421-228">Public ULONG [PerformanceCount](#performancecount)</span><span class="sxs-lookup"><span data-stu-id="fc421-228">public ulong [PerformanceCount](#performancecount)</span></span>

<span data-ttu-id="fc421-229">Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-229">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-230">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="fc421-230">PixelLocation</span></span> 

<span data-ttu-id="fc421-231">Die PixelLocation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-231">The PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="fc421-232">öffentlicher Punkt [PixelLocation](#pixellocation)</span><span class="sxs-lookup"><span data-stu-id="fc421-232">public Point [PixelLocation](#pixellocation)</span></span>

<span data-ttu-id="fc421-233">Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-233">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-234">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="fc421-234">PixelLocationRaw</span></span> 

<span data-ttu-id="fc421-235">Die PixelLocationRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-235">The PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="fc421-236">öffentlicher Punkt [PixelLocationRaw](#pixellocationraw)</span><span class="sxs-lookup"><span data-stu-id="fc421-236">public Point [PixelLocationRaw](#pixellocationraw)</span></span>

<span data-ttu-id="fc421-237">Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-237">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-238">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="fc421-238">PointerDeviceRect</span></span> 

<span data-ttu-id="fc421-239">Die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-239">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="fc421-240">öffentliche Rect- [PointerDeviceRect](#pointerdevicerect)</span><span class="sxs-lookup"><span data-stu-id="fc421-240">public Rect [PointerDeviceRect](#pointerdevicerect)</span></span>

#### <span data-ttu-id="fc421-241">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="fc421-241">PointerFlags</span></span> 

<span data-ttu-id="fc421-242">Die PointerFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-242">The PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="fc421-243">public uint [PointerFlags](#pointerflags)</span><span class="sxs-lookup"><span data-stu-id="fc421-243">public uint [PointerFlags](#pointerflags)</span></span>

<span data-ttu-id="fc421-244">Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="fc421-244">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="fc421-245">Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="fc421-245">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-246">Zeiger-Nr</span><span class="sxs-lookup"><span data-stu-id="fc421-246">PointerId</span></span> 

<span data-ttu-id="fc421-247">Die Zeiger-Nr des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-247">The PointerId of the pointer event.</span></span>

> <span data-ttu-id="fc421-248">öffentliche uint- [Zeiger](#pointerid) -Nr</span><span class="sxs-lookup"><span data-stu-id="fc421-248">public uint [PointerId](#pointerid)</span></span>

<span data-ttu-id="fc421-249">Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-249">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-250">PointerKind</span><span class="sxs-lookup"><span data-stu-id="fc421-250">PointerKind</span></span> 

<span data-ttu-id="fc421-251">Die PointerKind des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-251">The PointerKind of the pointer event.</span></span>

> <span data-ttu-id="fc421-252">public uint [PointerKind](#pointerkind)</span><span class="sxs-lookup"><span data-stu-id="fc421-252">public uint [PointerKind](#pointerkind)</span></span>

<span data-ttu-id="fc421-253">Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="fc421-253">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="fc421-254">Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="fc421-254">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="fc421-255">Unterstützt PT_PEN und PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="fc421-255">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="fc421-256">Zeit</span><span class="sxs-lookup"><span data-stu-id="fc421-256">Time</span></span> 

<span data-ttu-id="fc421-257">Die Uhrzeit des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-257">The Time of the pointer event.</span></span>

> <span data-ttu-id="fc421-258">öffentliche uint- [Zeit](#time)</span><span class="sxs-lookup"><span data-stu-id="fc421-258">public uint [Time](#time)</span></span>

<span data-ttu-id="fc421-259">Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-259">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-260">TouchContact</span><span class="sxs-lookup"><span data-stu-id="fc421-260">TouchContact</span></span> 

<span data-ttu-id="fc421-261">Die TouchContact des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-261">The TouchContact of the pointer event.</span></span>

> <span data-ttu-id="fc421-262">öffentliche Rect- [TouchContact](#touchcontact)</span><span class="sxs-lookup"><span data-stu-id="fc421-262">public Rect [TouchContact](#touchcontact)</span></span>

<span data-ttu-id="fc421-263">Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-263">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-264">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="fc421-264">TouchContactRaw</span></span> 

<span data-ttu-id="fc421-265">Die TouchContactRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-265">The TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="fc421-266">öffentliche Rect- [TouchContactRaw](#touchcontactraw)</span><span class="sxs-lookup"><span data-stu-id="fc421-266">public Rect [TouchContactRaw](#touchcontactraw)</span></span>

<span data-ttu-id="fc421-267">Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-267">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-268">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="fc421-268">TouchFlags</span></span> 

<span data-ttu-id="fc421-269">Die TouchFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-269">The TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="fc421-270">public uint [TouchFlags](#touchflags)</span><span class="sxs-lookup"><span data-stu-id="fc421-270">public uint [TouchFlags](#touchflags)</span></span>

<span data-ttu-id="fc421-271">Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="fc421-271">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="fc421-272">Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="fc421-272">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-273">TouchMask</span><span class="sxs-lookup"><span data-stu-id="fc421-273">TouchMask</span></span> 

<span data-ttu-id="fc421-274">Die TouchMask des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-274">The TouchMask of the pointer event.</span></span>

> <span data-ttu-id="fc421-275">public uint [TouchMask](#touchmask)</span><span class="sxs-lookup"><span data-stu-id="fc421-275">public uint [TouchMask](#touchmask)</span></span>

<span data-ttu-id="fc421-276">Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="fc421-276">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="fc421-277">Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="fc421-277">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-278">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="fc421-278">TouchOrientation</span></span> 

<span data-ttu-id="fc421-279">Die TouchOrientation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-279">The TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="fc421-280">public uint [TouchOrientation](#touchorientation)</span><span class="sxs-lookup"><span data-stu-id="fc421-280">public uint [TouchOrientation](#touchorientation)</span></span>

<span data-ttu-id="fc421-281">Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-281">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="fc421-282">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="fc421-282">TouchPressure</span></span> 

<span data-ttu-id="fc421-283">Die TouchPressure des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fc421-283">The TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="fc421-284">public uint [TouchPressure](#touchpressure)</span><span class="sxs-lookup"><span data-stu-id="fc421-284">public uint [TouchPressure](#touchpressure)</span></span>

<span data-ttu-id="fc421-285">Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="fc421-285">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


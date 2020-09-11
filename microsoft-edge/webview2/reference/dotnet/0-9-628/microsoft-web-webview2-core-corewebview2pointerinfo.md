---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
ms.openlocfilehash: 34ffa5fe0eabfe8e822db2792d2b25ab5106442a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012057"
---
# <span data-ttu-id="2a296-104">Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo Klasse</span><span class="sxs-lookup"><span data-stu-id="2a296-104">Microsoft.Web.WebView2.Core.CoreWebView2PointerInfo class</span></span> 

<span data-ttu-id="2a296-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2a296-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2a296-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="2a296-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2a296-107">Dies stellt in erster Linie ein kombiniertes Win32-POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="2a296-107">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="2a296-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2a296-108">Summary</span></span>

 <span data-ttu-id="2a296-109">Member</span><span class="sxs-lookup"><span data-stu-id="2a296-109">Members</span></span>                        | <span data-ttu-id="2a296-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2a296-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2a296-111">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="2a296-111">ButtonChangeKind</span></span>](#buttonchangekind) | <span data-ttu-id="2a296-112">Die ButtonChangeKind des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-112">The ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="2a296-113">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="2a296-113">DisplayRect</span></span>](#displayrect) | <span data-ttu-id="2a296-114">Die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-114">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="2a296-115">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="2a296-115">FrameId</span></span>](#frameid) | <span data-ttu-id="2a296-116">Die Frame-Nr des Pointer-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-116">The FrameID of the pointer event.</span></span>
[<span data-ttu-id="2a296-117">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="2a296-117">HimetricLocation</span></span>](#himetriclocation) | <span data-ttu-id="2a296-118">Die HimetricLocation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-118">The HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="2a296-119">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="2a296-119">HimetricLocationRaw</span></span>](#himetriclocationraw) | <span data-ttu-id="2a296-120">Die HimetricLocationRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-120">The HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="2a296-121">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="2a296-121">HistoryCount</span></span>](#historycount) | <span data-ttu-id="2a296-122">Die HistoryCount des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-122">The HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="2a296-123">InputData</span><span class="sxs-lookup"><span data-stu-id="2a296-123">InputData</span></span>](#inputdata) | <span data-ttu-id="2a296-124">Die inputData des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-124">The InputData of the pointer event.</span></span>
[<span data-ttu-id="2a296-125">KeyStates</span><span class="sxs-lookup"><span data-stu-id="2a296-125">KeyStates</span></span>](#keystates) | <span data-ttu-id="2a296-126">Die KeyStates des Pointer-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-126">The KeyStates of the pointer event.</span></span>
[<span data-ttu-id="2a296-127">PenFlags</span><span class="sxs-lookup"><span data-stu-id="2a296-127">PenFlags</span></span>](#penflags) | <span data-ttu-id="2a296-128">Die PenFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-128">The PenFlags of the pointer event.</span></span>
[<span data-ttu-id="2a296-129">PenMask</span><span class="sxs-lookup"><span data-stu-id="2a296-129">PenMask</span></span>](#penmask) | <span data-ttu-id="2a296-130">Die PenMask des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-130">The PenMask of the pointer event.</span></span>
[<span data-ttu-id="2a296-131">PenPressure</span><span class="sxs-lookup"><span data-stu-id="2a296-131">PenPressure</span></span>](#penpressure) | <span data-ttu-id="2a296-132">Die PenPressure des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-132">The PenPressure of the pointer event.</span></span>
[<span data-ttu-id="2a296-133">PenRotation</span><span class="sxs-lookup"><span data-stu-id="2a296-133">PenRotation</span></span>](#penrotation) | <span data-ttu-id="2a296-134">Die PenRotation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-134">The PenRotation of the pointer event.</span></span>
[<span data-ttu-id="2a296-135">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="2a296-135">PenTiltX</span></span>](#pentiltx) | <span data-ttu-id="2a296-136">Die PenTiltX des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-136">The PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="2a296-137">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="2a296-137">PenTiltY</span></span>](#pentilty) | <span data-ttu-id="2a296-138">Die PenTiltY des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-138">The PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="2a296-139">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="2a296-139">PerformanceCount</span></span>](#performancecount) | <span data-ttu-id="2a296-140">Die PerformanceCount des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-140">The PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="2a296-141">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="2a296-141">PixelLocation</span></span>](#pixellocation) | <span data-ttu-id="2a296-142">Die PixelLocation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-142">The PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="2a296-143">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="2a296-143">PixelLocationRaw</span></span>](#pixellocationraw) | <span data-ttu-id="2a296-144">Die PixelLocationRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-144">The PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="2a296-145">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="2a296-145">PointerDeviceRect</span></span>](#pointerdevicerect) | <span data-ttu-id="2a296-146">Die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-146">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="2a296-147">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="2a296-147">PointerFlags</span></span>](#pointerflags) | <span data-ttu-id="2a296-148">Die PointerFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-148">The PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="2a296-149">Zeiger-Nr</span><span class="sxs-lookup"><span data-stu-id="2a296-149">PointerId</span></span>](#pointerid) | <span data-ttu-id="2a296-150">Die Zeiger-Nr des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-150">The PointerId of the pointer event.</span></span>
[<span data-ttu-id="2a296-151">PointerKind</span><span class="sxs-lookup"><span data-stu-id="2a296-151">PointerKind</span></span>](#pointerkind) | <span data-ttu-id="2a296-152">Die PointerKind des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-152">The PointerKind of the pointer event.</span></span>
[<span data-ttu-id="2a296-153">Zeit</span><span class="sxs-lookup"><span data-stu-id="2a296-153">Time</span></span>](#time) | <span data-ttu-id="2a296-154">Die Uhrzeit des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-154">The Time of the pointer event.</span></span>
[<span data-ttu-id="2a296-155">TouchContact</span><span class="sxs-lookup"><span data-stu-id="2a296-155">TouchContact</span></span>](#touchcontact) | <span data-ttu-id="2a296-156">Die TouchContact des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-156">The TouchContact of the pointer event.</span></span>
[<span data-ttu-id="2a296-157">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="2a296-157">TouchContactRaw</span></span>](#touchcontactraw) | <span data-ttu-id="2a296-158">Die TouchContactRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-158">The TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="2a296-159">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="2a296-159">TouchFlags</span></span>](#touchflags) | <span data-ttu-id="2a296-160">Die TouchFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-160">The TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="2a296-161">TouchMask</span><span class="sxs-lookup"><span data-stu-id="2a296-161">TouchMask</span></span>](#touchmask) | <span data-ttu-id="2a296-162">Die TouchMask des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-162">The TouchMask of the pointer event.</span></span>
[<span data-ttu-id="2a296-163">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="2a296-163">TouchOrientation</span></span>](#touchorientation) | <span data-ttu-id="2a296-164">Die TouchOrientation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-164">The TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="2a296-165">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="2a296-165">TouchPressure</span></span>](#touchpressure) | <span data-ttu-id="2a296-166">Die TouchPressure des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-166">The TouchPressure of the pointer event.</span></span>

## <span data-ttu-id="2a296-167">Member</span><span class="sxs-lookup"><span data-stu-id="2a296-167">Members</span></span>

#### <span data-ttu-id="2a296-168">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="2a296-168">ButtonChangeKind</span></span> 

<span data-ttu-id="2a296-169">Die ButtonChangeKind des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-169">The ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="2a296-170">public int [ButtonChangeKind](#buttonchangekind)</span><span class="sxs-lookup"><span data-stu-id="2a296-170">public int [ButtonChangeKind](#buttonchangekind)</span></span>

<span data-ttu-id="2a296-171">Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2a296-171">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="2a296-172">Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="2a296-172">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-173">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="2a296-173">DisplayRect</span></span> 

<span data-ttu-id="2a296-174">Die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-174">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="2a296-175">öffentliches Rechteck [DisplayRect](#displayrect)</span><span class="sxs-lookup"><span data-stu-id="2a296-175">public Rectangle [DisplayRect](#displayrect)</span></span>

#### <span data-ttu-id="2a296-176">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="2a296-176">FrameId</span></span> 

<span data-ttu-id="2a296-177">Die Frame-Nr des Pointer-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-177">The FrameID of the pointer event.</span></span>

> <span data-ttu-id="2a296-178">öffentliche uint- [Frame](#frameid) -Nr</span><span class="sxs-lookup"><span data-stu-id="2a296-178">public uint [FrameId](#frameid)</span></span>

<span data-ttu-id="2a296-179">Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-179">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-180">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="2a296-180">HimetricLocation</span></span> 

<span data-ttu-id="2a296-181">Die HimetricLocation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-181">The HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="2a296-182">öffentlicher Punkt [HimetricLocation](#himetriclocation)</span><span class="sxs-lookup"><span data-stu-id="2a296-182">public Point [HimetricLocation](#himetriclocation)</span></span>

<span data-ttu-id="2a296-183">Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-183">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-184">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="2a296-184">HimetricLocationRaw</span></span> 

<span data-ttu-id="2a296-185">Die HimetricLocationRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-185">The HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="2a296-186">öffentlicher Punkt [HimetricLocationRaw](#himetriclocationraw)</span><span class="sxs-lookup"><span data-stu-id="2a296-186">public Point [HimetricLocationRaw](#himetriclocationraw)</span></span>

<span data-ttu-id="2a296-187">Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-187">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-188">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="2a296-188">HistoryCount</span></span> 

<span data-ttu-id="2a296-189">Die HistoryCount des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-189">The HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="2a296-190">public uint [HistoryCount](#historycount)</span><span class="sxs-lookup"><span data-stu-id="2a296-190">public uint [HistoryCount](#historycount)</span></span>

<span data-ttu-id="2a296-191">Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-191">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-192">InputData</span><span class="sxs-lookup"><span data-stu-id="2a296-192">InputData</span></span> 

<span data-ttu-id="2a296-193">Die inputData des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-193">The InputData of the pointer event.</span></span>

> <span data-ttu-id="2a296-194">public int [inputData](#inputdata)</span><span class="sxs-lookup"><span data-stu-id="2a296-194">public int [InputData](#inputdata)</span></span>

<span data-ttu-id="2a296-195">Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-195">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-196">KeyStates</span><span class="sxs-lookup"><span data-stu-id="2a296-196">KeyStates</span></span> 

<span data-ttu-id="2a296-197">Die KeyStates des Pointer-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-197">The KeyStates of the pointer event.</span></span>

> <span data-ttu-id="2a296-198">öffentliche uint- [KeyStates](#keystates)</span><span class="sxs-lookup"><span data-stu-id="2a296-198">public uint [KeyStates](#keystates)</span></span>

<span data-ttu-id="2a296-199">Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-199">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-200">PenFlags</span><span class="sxs-lookup"><span data-stu-id="2a296-200">PenFlags</span></span> 

<span data-ttu-id="2a296-201">Die PenFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-201">The PenFlags of the pointer event.</span></span>

> <span data-ttu-id="2a296-202">public uint [PenFlags](#penflags)</span><span class="sxs-lookup"><span data-stu-id="2a296-202">public uint [PenFlags](#penflags)</span></span>

<span data-ttu-id="2a296-203">Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2a296-203">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="2a296-204">Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="2a296-204">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-205">PenMask</span><span class="sxs-lookup"><span data-stu-id="2a296-205">PenMask</span></span> 

<span data-ttu-id="2a296-206">Die PenMask des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-206">The PenMask of the pointer event.</span></span>

> <span data-ttu-id="2a296-207">public uint [PenMask](#penmask)</span><span class="sxs-lookup"><span data-stu-id="2a296-207">public uint [PenMask](#penmask)</span></span>

<span data-ttu-id="2a296-208">Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2a296-208">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="2a296-209">Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="2a296-209">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-210">PenPressure</span><span class="sxs-lookup"><span data-stu-id="2a296-210">PenPressure</span></span> 

<span data-ttu-id="2a296-211">Die PenPressure des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-211">The PenPressure of the pointer event.</span></span>

> <span data-ttu-id="2a296-212">public uint [PenPressure](#penpressure)</span><span class="sxs-lookup"><span data-stu-id="2a296-212">public uint [PenPressure](#penpressure)</span></span>

<span data-ttu-id="2a296-213">Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-213">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-214">PenRotation</span><span class="sxs-lookup"><span data-stu-id="2a296-214">PenRotation</span></span> 

<span data-ttu-id="2a296-215">Die PenRotation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-215">The PenRotation of the pointer event.</span></span>

> <span data-ttu-id="2a296-216">public uint [PenRotation](#penrotation)</span><span class="sxs-lookup"><span data-stu-id="2a296-216">public uint [PenRotation](#penrotation)</span></span>

<span data-ttu-id="2a296-217">Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-217">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-218">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="2a296-218">PenTiltX</span></span> 

<span data-ttu-id="2a296-219">Die PenTiltX des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-219">The PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="2a296-220">public int [PenTiltX](#pentiltx)</span><span class="sxs-lookup"><span data-stu-id="2a296-220">public int [PenTiltX](#pentiltx)</span></span>

<span data-ttu-id="2a296-221">Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-221">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-222">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="2a296-222">PenTiltY</span></span> 

<span data-ttu-id="2a296-223">Die PenTiltY des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-223">The PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="2a296-224">public int [PenTiltY](#pentilty)</span><span class="sxs-lookup"><span data-stu-id="2a296-224">public int [PenTiltY](#pentilty)</span></span>

<span data-ttu-id="2a296-225">Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-225">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-226">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="2a296-226">PerformanceCount</span></span> 

<span data-ttu-id="2a296-227">Die PerformanceCount des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-227">The PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="2a296-228">Public ULONG [PerformanceCount](#performancecount)</span><span class="sxs-lookup"><span data-stu-id="2a296-228">public ulong [PerformanceCount](#performancecount)</span></span>

<span data-ttu-id="2a296-229">Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-229">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-230">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="2a296-230">PixelLocation</span></span> 

<span data-ttu-id="2a296-231">Die PixelLocation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-231">The PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="2a296-232">öffentlicher Punkt [PixelLocation](#pixellocation)</span><span class="sxs-lookup"><span data-stu-id="2a296-232">public Point [PixelLocation](#pixellocation)</span></span>

<span data-ttu-id="2a296-233">Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-233">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-234">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="2a296-234">PixelLocationRaw</span></span> 

<span data-ttu-id="2a296-235">Die PixelLocationRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-235">The PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="2a296-236">öffentlicher Punkt [PixelLocationRaw](#pixellocationraw)</span><span class="sxs-lookup"><span data-stu-id="2a296-236">public Point [PixelLocationRaw](#pixellocationraw)</span></span>

<span data-ttu-id="2a296-237">Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-237">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-238">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="2a296-238">PointerDeviceRect</span></span> 

<span data-ttu-id="2a296-239">Die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-239">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="2a296-240">öffentliches Rechteck [PointerDeviceRect](#pointerdevicerect)</span><span class="sxs-lookup"><span data-stu-id="2a296-240">public Rectangle [PointerDeviceRect](#pointerdevicerect)</span></span>

#### <span data-ttu-id="2a296-241">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="2a296-241">PointerFlags</span></span> 

<span data-ttu-id="2a296-242">Die PointerFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-242">The PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="2a296-243">public uint [PointerFlags](#pointerflags)</span><span class="sxs-lookup"><span data-stu-id="2a296-243">public uint [PointerFlags](#pointerflags)</span></span>

<span data-ttu-id="2a296-244">Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2a296-244">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="2a296-245">Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="2a296-245">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-246">Zeiger-Nr</span><span class="sxs-lookup"><span data-stu-id="2a296-246">PointerId</span></span> 

<span data-ttu-id="2a296-247">Die Zeiger-Nr des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-247">The PointerId of the pointer event.</span></span>

> <span data-ttu-id="2a296-248">öffentliche uint- [Zeiger](#pointerid) -Nr</span><span class="sxs-lookup"><span data-stu-id="2a296-248">public uint [PointerId](#pointerid)</span></span>

<span data-ttu-id="2a296-249">Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-249">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-250">PointerKind</span><span class="sxs-lookup"><span data-stu-id="2a296-250">PointerKind</span></span> 

<span data-ttu-id="2a296-251">Die PointerKind des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-251">The PointerKind of the pointer event.</span></span>

> <span data-ttu-id="2a296-252">public uint [PointerKind](#pointerkind)</span><span class="sxs-lookup"><span data-stu-id="2a296-252">public uint [PointerKind](#pointerkind)</span></span>

<span data-ttu-id="2a296-253">Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2a296-253">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="2a296-254">Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="2a296-254">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="2a296-255">Unterstützt PT_PEN und PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="2a296-255">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="2a296-256">Zeit</span><span class="sxs-lookup"><span data-stu-id="2a296-256">Time</span></span> 

<span data-ttu-id="2a296-257">Die Uhrzeit des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-257">The Time of the pointer event.</span></span>

> <span data-ttu-id="2a296-258">öffentliche uint- [Zeit](#time)</span><span class="sxs-lookup"><span data-stu-id="2a296-258">public uint [Time](#time)</span></span>

<span data-ttu-id="2a296-259">Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-259">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-260">TouchContact</span><span class="sxs-lookup"><span data-stu-id="2a296-260">TouchContact</span></span> 

<span data-ttu-id="2a296-261">Die TouchContact des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-261">The TouchContact of the pointer event.</span></span>

> <span data-ttu-id="2a296-262">öffentliches Rechteck [TouchContact](#touchcontact)</span><span class="sxs-lookup"><span data-stu-id="2a296-262">public Rectangle [TouchContact](#touchcontact)</span></span>

<span data-ttu-id="2a296-263">Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-263">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-264">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="2a296-264">TouchContactRaw</span></span> 

<span data-ttu-id="2a296-265">Die TouchContactRaw des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-265">The TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="2a296-266">öffentliches Rechteck [TouchContactRaw](#touchcontactraw)</span><span class="sxs-lookup"><span data-stu-id="2a296-266">public Rectangle [TouchContactRaw](#touchcontactraw)</span></span>

<span data-ttu-id="2a296-267">Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-267">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-268">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="2a296-268">TouchFlags</span></span> 

<span data-ttu-id="2a296-269">Die TouchFlags des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-269">The TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="2a296-270">public uint [TouchFlags](#touchflags)</span><span class="sxs-lookup"><span data-stu-id="2a296-270">public uint [TouchFlags](#touchflags)</span></span>

<span data-ttu-id="2a296-271">Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2a296-271">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="2a296-272">Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="2a296-272">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-273">TouchMask</span><span class="sxs-lookup"><span data-stu-id="2a296-273">TouchMask</span></span> 

<span data-ttu-id="2a296-274">Die TouchMask des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-274">The TouchMask of the pointer event.</span></span>

> <span data-ttu-id="2a296-275">public uint [TouchMask](#touchmask)</span><span class="sxs-lookup"><span data-stu-id="2a296-275">public uint [TouchMask](#touchmask)</span></span>

<span data-ttu-id="2a296-276">Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2a296-276">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="2a296-277">Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.</span><span class="sxs-lookup"><span data-stu-id="2a296-277">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-278">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="2a296-278">TouchOrientation</span></span> 

<span data-ttu-id="2a296-279">Die TouchOrientation des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-279">The TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="2a296-280">public uint [TouchOrientation](#touchorientation)</span><span class="sxs-lookup"><span data-stu-id="2a296-280">public uint [TouchOrientation](#touchorientation)</span></span>

<span data-ttu-id="2a296-281">Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-281">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2a296-282">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="2a296-282">TouchPressure</span></span> 

<span data-ttu-id="2a296-283">Die TouchPressure des Zeiger Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="2a296-283">The TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="2a296-284">public uint [TouchPressure](#touchpressure)</span><span class="sxs-lookup"><span data-stu-id="2a296-284">public uint [TouchPressure](#touchpressure)</span></span>

<span data-ttu-id="2a296-285">Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2a296-285">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


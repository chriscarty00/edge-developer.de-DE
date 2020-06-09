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
ms.openlocfilehash: e8563bdd77972945a1e4b81662071d07d1efeb02
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698802"
---
# <span data-ttu-id="411a2-104">Microsoft. Web. WebView2. Core. CoreWebView2Matrix4x4-Struktur</span><span class="sxs-lookup"><span data-stu-id="411a2-104">Microsoft.Web.WebView2.Core.CoreWebView2Matrix4x4 struct</span></span> 

> [!NOTE]
> <span data-ttu-id="411a2-105">Hierbei handelt es sich um eine [experimentelle API](../../../concepts/versioning.md#experimental-apis) , die mit unserer SDK [-Version 0.9.538-Prerelease](../../../releasenotes.md#09538)ausgeliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="411a2-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="411a2-106">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="411a2-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="411a2-107">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="411a2-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="411a2-108">Diese Transformation wird verwendet, um korrekte Koordinaten beim Aufrufen von CreateCoreWebView2PointerInfoFromPointerId zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="411a2-108">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span>

## <span data-ttu-id="411a2-109">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="411a2-109">Summary</span></span>

 <span data-ttu-id="411a2-110">Member</span><span class="sxs-lookup"><span data-stu-id="411a2-110">Members</span></span>                        | <span data-ttu-id="411a2-111">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="411a2-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="411a2-112">_11</span><span class="sxs-lookup"><span data-stu-id="411a2-112">_11</span></span>](#_11) | <span data-ttu-id="411a2-113">Der Wert in der ersten Zeile und ersten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-113">The value in the first row and first column of the matrix.</span></span>
[<span data-ttu-id="411a2-114">_12</span><span class="sxs-lookup"><span data-stu-id="411a2-114">_12</span></span>](#_12) | <span data-ttu-id="411a2-115">Der Wert in der ersten Zeile und zweiten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-115">The value in the first row and second column of the matrix.</span></span>
[<span data-ttu-id="411a2-116">_13</span><span class="sxs-lookup"><span data-stu-id="411a2-116">_13</span></span>](#_13) | <span data-ttu-id="411a2-117">Der Wert in der ersten Zeile und dritten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-117">The value in the first row and third column of the matrix.</span></span>
[<span data-ttu-id="411a2-118">_14</span><span class="sxs-lookup"><span data-stu-id="411a2-118">_14</span></span>](#_14) | <span data-ttu-id="411a2-119">Der Wert in der ersten Zeile und vierten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-119">The value in the first row and fourth column of the matrix.</span></span>
[<span data-ttu-id="411a2-120">_21</span><span class="sxs-lookup"><span data-stu-id="411a2-120">_21</span></span>](#_21) | <span data-ttu-id="411a2-121">Der Wert in der zweiten Zeile und ersten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-121">The value in the second row and first column of the matrix.</span></span>
[<span data-ttu-id="411a2-122">_22</span><span class="sxs-lookup"><span data-stu-id="411a2-122">_22</span></span>](#_22) | <span data-ttu-id="411a2-123">Der Wert in der zweiten Zeile und zweiten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-123">The value in the second row and second column of the matrix.</span></span>
[<span data-ttu-id="411a2-124">_23</span><span class="sxs-lookup"><span data-stu-id="411a2-124">_23</span></span>](#_23) | <span data-ttu-id="411a2-125">Der Wert in der zweiten Zeile und dritten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-125">The value in the second row and third column of the matrix.</span></span>
[<span data-ttu-id="411a2-126">_24</span><span class="sxs-lookup"><span data-stu-id="411a2-126">_24</span></span>](#_24) | <span data-ttu-id="411a2-127">Der Wert in der zweiten Zeile und vierten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-127">The value in the second row and fourth column of the matrix.</span></span>
[<span data-ttu-id="411a2-128">_31</span><span class="sxs-lookup"><span data-stu-id="411a2-128">_31</span></span>](#_31) | <span data-ttu-id="411a2-129">Der Wert in der dritten Zeile und ersten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-129">The value in the third row and first column of the matrix.</span></span>
[<span data-ttu-id="411a2-130">_32</span><span class="sxs-lookup"><span data-stu-id="411a2-130">_32</span></span>](#_32) | <span data-ttu-id="411a2-131">Der Wert in der dritten Zeile und zweiten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-131">The value in the third row and second column of the matrix.</span></span>
[<span data-ttu-id="411a2-132">_33</span><span class="sxs-lookup"><span data-stu-id="411a2-132">_33</span></span>](#_33) | <span data-ttu-id="411a2-133">Der Wert in der dritten Zeile und dritten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-133">The value in the third row and third column of the matrix.</span></span>
[<span data-ttu-id="411a2-134">_34</span><span class="sxs-lookup"><span data-stu-id="411a2-134">_34</span></span>](#_34) | <span data-ttu-id="411a2-135">Der Wert in der dritten Zeile und vierten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-135">The value in the third row and fourth column of the matrix.</span></span>
[<span data-ttu-id="411a2-136">_41</span><span class="sxs-lookup"><span data-stu-id="411a2-136">_41</span></span>](#_41) | <span data-ttu-id="411a2-137">Der Wert in der vierten Zeile und ersten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-137">The value in the fourth row and first column of the matrix.</span></span>
[<span data-ttu-id="411a2-138">_42</span><span class="sxs-lookup"><span data-stu-id="411a2-138">_42</span></span>](#_42) | <span data-ttu-id="411a2-139">Der Wert in der vierten Zeile und zweiten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-139">The value in the fourth row and second column of the matrix.</span></span>
[<span data-ttu-id="411a2-140">_43</span><span class="sxs-lookup"><span data-stu-id="411a2-140">_43</span></span>](#_43) | <span data-ttu-id="411a2-141">Der Wert in der vierten Zeile und dritten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-141">The value in the fourth row and third column of the matrix.</span></span>
[<span data-ttu-id="411a2-142">_44</span><span class="sxs-lookup"><span data-stu-id="411a2-142">_44</span></span>](#_44) | <span data-ttu-id="411a2-143">Der Wert in der vierten Zeile und vierten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-143">The value in the fourth row and fourth column of the matrix.</span></span>

<span data-ttu-id="411a2-144">Dies entspricht einer D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="411a2-144">This is equivalent to a D2D1_MATRIX_4X4_F.</span></span>

## <span data-ttu-id="411a2-145">Member</span><span class="sxs-lookup"><span data-stu-id="411a2-145">Members</span></span>

#### <span data-ttu-id="411a2-146">_11</span><span class="sxs-lookup"><span data-stu-id="411a2-146">_11</span></span> 

<span data-ttu-id="411a2-147">Der Wert in der ersten Zeile und ersten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-147">The value in the first row and first column of the matrix.</span></span>

> <span data-ttu-id="411a2-148">öffentliche einzelne [_11](#_11)</span><span class="sxs-lookup"><span data-stu-id="411a2-148">public Single [_11](#_11)</span></span>

#### <span data-ttu-id="411a2-149">_12</span><span class="sxs-lookup"><span data-stu-id="411a2-149">_12</span></span> 

<span data-ttu-id="411a2-150">Der Wert in der ersten Zeile und zweiten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-150">The value in the first row and second column of the matrix.</span></span>

> <span data-ttu-id="411a2-151">öffentliche einzelne [_12](#_12)</span><span class="sxs-lookup"><span data-stu-id="411a2-151">public Single [_12](#_12)</span></span>

#### <span data-ttu-id="411a2-152">_13</span><span class="sxs-lookup"><span data-stu-id="411a2-152">_13</span></span> 

<span data-ttu-id="411a2-153">Der Wert in der ersten Zeile und dritten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-153">The value in the first row and third column of the matrix.</span></span>

> <span data-ttu-id="411a2-154">öffentliche einzelne [_13](#_13)</span><span class="sxs-lookup"><span data-stu-id="411a2-154">public Single [_13](#_13)</span></span>

#### <span data-ttu-id="411a2-155">_14</span><span class="sxs-lookup"><span data-stu-id="411a2-155">_14</span></span> 

<span data-ttu-id="411a2-156">Der Wert in der ersten Zeile und vierten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-156">The value in the first row and fourth column of the matrix.</span></span>

> <span data-ttu-id="411a2-157">öffentliche einzelne [_14](#_14)</span><span class="sxs-lookup"><span data-stu-id="411a2-157">public Single [_14](#_14)</span></span>

#### <span data-ttu-id="411a2-158">_21</span><span class="sxs-lookup"><span data-stu-id="411a2-158">_21</span></span> 

<span data-ttu-id="411a2-159">Der Wert in der zweiten Zeile und ersten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-159">The value in the second row and first column of the matrix.</span></span>

> <span data-ttu-id="411a2-160">öffentliche einzelne [_21](#_21)</span><span class="sxs-lookup"><span data-stu-id="411a2-160">public Single [_21](#_21)</span></span>

#### <span data-ttu-id="411a2-161">_22</span><span class="sxs-lookup"><span data-stu-id="411a2-161">_22</span></span> 

<span data-ttu-id="411a2-162">Der Wert in der zweiten Zeile und zweiten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-162">The value in the second row and second column of the matrix.</span></span>

> <span data-ttu-id="411a2-163">öffentliche einzelne [_22](#_22)</span><span class="sxs-lookup"><span data-stu-id="411a2-163">public Single [_22](#_22)</span></span>

#### <span data-ttu-id="411a2-164">_23</span><span class="sxs-lookup"><span data-stu-id="411a2-164">_23</span></span> 

<span data-ttu-id="411a2-165">Der Wert in der zweiten Zeile und dritten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-165">The value in the second row and third column of the matrix.</span></span>

> <span data-ttu-id="411a2-166">öffentliche einzelne [_23](#_23)</span><span class="sxs-lookup"><span data-stu-id="411a2-166">public Single [_23](#_23)</span></span>

#### <span data-ttu-id="411a2-167">_24</span><span class="sxs-lookup"><span data-stu-id="411a2-167">_24</span></span> 

<span data-ttu-id="411a2-168">Der Wert in der zweiten Zeile und vierten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-168">The value in the second row and fourth column of the matrix.</span></span>

> <span data-ttu-id="411a2-169">öffentliche einzelne [_24](#_24)</span><span class="sxs-lookup"><span data-stu-id="411a2-169">public Single [_24](#_24)</span></span>

#### <span data-ttu-id="411a2-170">_31</span><span class="sxs-lookup"><span data-stu-id="411a2-170">_31</span></span> 

<span data-ttu-id="411a2-171">Der Wert in der dritten Zeile und ersten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-171">The value in the third row and first column of the matrix.</span></span>

> <span data-ttu-id="411a2-172">öffentliche einzelne [_31](#_31)</span><span class="sxs-lookup"><span data-stu-id="411a2-172">public Single [_31](#_31)</span></span>

#### <span data-ttu-id="411a2-173">_32</span><span class="sxs-lookup"><span data-stu-id="411a2-173">_32</span></span> 

<span data-ttu-id="411a2-174">Der Wert in der dritten Zeile und zweiten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-174">The value in the third row and second column of the matrix.</span></span>

> <span data-ttu-id="411a2-175">öffentliche einzelne [_32](#_32)</span><span class="sxs-lookup"><span data-stu-id="411a2-175">public Single [_32](#_32)</span></span>

#### <span data-ttu-id="411a2-176">_33</span><span class="sxs-lookup"><span data-stu-id="411a2-176">_33</span></span> 

<span data-ttu-id="411a2-177">Der Wert in der dritten Zeile und dritten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-177">The value in the third row and third column of the matrix.</span></span>

> <span data-ttu-id="411a2-178">öffentliche einzelne [_33](#_33)</span><span class="sxs-lookup"><span data-stu-id="411a2-178">public Single [_33](#_33)</span></span>

#### <span data-ttu-id="411a2-179">_34</span><span class="sxs-lookup"><span data-stu-id="411a2-179">_34</span></span> 

<span data-ttu-id="411a2-180">Der Wert in der dritten Zeile und vierten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-180">The value in the third row and fourth column of the matrix.</span></span>

> <span data-ttu-id="411a2-181">öffentliche einzelne [_34](#_34)</span><span class="sxs-lookup"><span data-stu-id="411a2-181">public Single [_34](#_34)</span></span>

#### <span data-ttu-id="411a2-182">_41</span><span class="sxs-lookup"><span data-stu-id="411a2-182">_41</span></span> 

<span data-ttu-id="411a2-183">Der Wert in der vierten Zeile und ersten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-183">The value in the fourth row and first column of the matrix.</span></span>

> <span data-ttu-id="411a2-184">öffentliche einzelne [_41](#_41)</span><span class="sxs-lookup"><span data-stu-id="411a2-184">public Single [_41](#_41)</span></span>

#### <span data-ttu-id="411a2-185">_42</span><span class="sxs-lookup"><span data-stu-id="411a2-185">_42</span></span> 

<span data-ttu-id="411a2-186">Der Wert in der vierten Zeile und zweiten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-186">The value in the fourth row and second column of the matrix.</span></span>

> <span data-ttu-id="411a2-187">öffentliche einzelne [_42](#_42)</span><span class="sxs-lookup"><span data-stu-id="411a2-187">public Single [_42](#_42)</span></span>

#### <span data-ttu-id="411a2-188">_43</span><span class="sxs-lookup"><span data-stu-id="411a2-188">_43</span></span> 

<span data-ttu-id="411a2-189">Der Wert in der vierten Zeile und dritten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-189">The value in the fourth row and third column of the matrix.</span></span>

> <span data-ttu-id="411a2-190">öffentliche einzelne [_43](#_43)</span><span class="sxs-lookup"><span data-stu-id="411a2-190">public Single [_43](#_43)</span></span>

#### <span data-ttu-id="411a2-191">_44</span><span class="sxs-lookup"><span data-stu-id="411a2-191">_44</span></span> 

<span data-ttu-id="411a2-192">Der Wert in der vierten Zeile und vierten Spalte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="411a2-192">The value in the fourth row and fourth column of the matrix.</span></span>

> <span data-ttu-id="411a2-193">öffentliche einzelne [_44](#_44)</span><span class="sxs-lookup"><span data-stu-id="411a2-193">public Single [_44](#_44)</span></span>


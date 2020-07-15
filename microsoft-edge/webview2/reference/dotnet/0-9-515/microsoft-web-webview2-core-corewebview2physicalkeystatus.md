---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: da7069fb4dad164720bb697a250a216a0bd452ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881200"
---
# <span data-ttu-id="692d8-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus-Struktur</span><span class="sxs-lookup"><span data-stu-id="692d8-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

> [!NOTE]
> <span data-ttu-id="692d8-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="692d8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="692d8-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="692d8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="692d8-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="692d8-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="692d8-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="692d8-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="692d8-109">Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="692d8-109">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="692d8-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="692d8-110">Summary</span></span>

 <span data-ttu-id="692d8-111">Member</span><span class="sxs-lookup"><span data-stu-id="692d8-111">Members</span></span>                        | <span data-ttu-id="692d8-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="692d8-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="692d8-113">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="692d8-113">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="692d8-114">Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="692d8-114">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="692d8-115">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="692d8-115">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="692d8-116">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="692d8-116">The transition state.</span></span>
[<span data-ttu-id="692d8-117">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="692d8-117">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="692d8-118">Der kontextcode.</span><span class="sxs-lookup"><span data-stu-id="692d8-118">The context code.</span></span>
[<span data-ttu-id="692d8-119">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="692d8-119">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="692d8-120">Die Anzahl der Wiederholungen für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="692d8-120">The repeat count for the current message.</span></span>
[<span data-ttu-id="692d8-121">ScanCode</span><span class="sxs-lookup"><span data-stu-id="692d8-121">ScanCode</span></span>](#scancode) | <span data-ttu-id="692d8-122">Der Überprüfungscode.</span><span class="sxs-lookup"><span data-stu-id="692d8-122">The scan code.</span></span>
[<span data-ttu-id="692d8-123">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="692d8-123">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="692d8-124">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="692d8-124">The previous key state.</span></span>

<span data-ttu-id="692d8-125">Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="692d8-125">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="692d8-126">Member</span><span class="sxs-lookup"><span data-stu-id="692d8-126">Members</span></span>

#### <span data-ttu-id="692d8-127">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="692d8-127">IsExtendedKey</span></span> 

<span data-ttu-id="692d8-128">Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="692d8-128">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="692d8-129">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="692d8-129">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="692d8-130">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="692d8-130">IsKeyReleased</span></span> 

<span data-ttu-id="692d8-131">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="692d8-131">The transition state.</span></span>

> <span data-ttu-id="692d8-132">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="692d8-132">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="692d8-133">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="692d8-133">IsMenuKeyDown</span></span> 

<span data-ttu-id="692d8-134">Der kontextcode.</span><span class="sxs-lookup"><span data-stu-id="692d8-134">The context code.</span></span>

> <span data-ttu-id="692d8-135">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="692d8-135">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="692d8-136">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="692d8-136">RepeatCount</span></span> 

<span data-ttu-id="692d8-137">Die Anzahl der Wiederholungen für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="692d8-137">The repeat count for the current message.</span></span>

> <span data-ttu-id="692d8-138">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="692d8-138">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="692d8-139">ScanCode</span><span class="sxs-lookup"><span data-stu-id="692d8-139">ScanCode</span></span> 

<span data-ttu-id="692d8-140">Der Überprüfungscode.</span><span class="sxs-lookup"><span data-stu-id="692d8-140">The scan code.</span></span>

> <span data-ttu-id="692d8-141">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="692d8-141">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="692d8-142">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="692d8-142">WasKeyDown</span></span> 

<span data-ttu-id="692d8-143">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="692d8-143">The previous key state.</span></span>

> <span data-ttu-id="692d8-144">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="692d8-144">public int [WasKeyDown](#waskeydown)</span></span>


---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: 280fe2d970d78bf1ea7a79b21f5081510ee27053
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878771"
---
# <span data-ttu-id="e83bb-104">Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus-Struktur</span><span class="sxs-lookup"><span data-stu-id="e83bb-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="e83bb-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e83bb-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e83bb-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e83bb-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e83bb-107">Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="e83bb-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="e83bb-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e83bb-108">Summary</span></span>

 <span data-ttu-id="e83bb-109">Member</span><span class="sxs-lookup"><span data-stu-id="e83bb-109">Members</span></span>                        | <span data-ttu-id="e83bb-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e83bb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e83bb-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="e83bb-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="e83bb-112">Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="e83bb-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="e83bb-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="e83bb-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="e83bb-114">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="e83bb-114">The transition state.</span></span>
[<span data-ttu-id="e83bb-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="e83bb-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="e83bb-116">Der kontextcode.</span><span class="sxs-lookup"><span data-stu-id="e83bb-116">The context code.</span></span>
[<span data-ttu-id="e83bb-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="e83bb-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="e83bb-118">Die Anzahl der Wiederholungen für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e83bb-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="e83bb-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="e83bb-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="e83bb-120">Der Überprüfungscode.</span><span class="sxs-lookup"><span data-stu-id="e83bb-120">The scan code.</span></span>
[<span data-ttu-id="e83bb-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="e83bb-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="e83bb-122">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="e83bb-122">The previous key state.</span></span>

<span data-ttu-id="e83bb-123">Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="e83bb-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="e83bb-124">Member</span><span class="sxs-lookup"><span data-stu-id="e83bb-124">Members</span></span>

#### <span data-ttu-id="e83bb-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="e83bb-125">IsExtendedKey</span></span> 

<span data-ttu-id="e83bb-126">Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="e83bb-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="e83bb-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="e83bb-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="e83bb-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="e83bb-128">IsKeyReleased</span></span> 

<span data-ttu-id="e83bb-129">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="e83bb-129">The transition state.</span></span>

> <span data-ttu-id="e83bb-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="e83bb-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="e83bb-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="e83bb-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="e83bb-132">Der kontextcode.</span><span class="sxs-lookup"><span data-stu-id="e83bb-132">The context code.</span></span>

> <span data-ttu-id="e83bb-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="e83bb-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="e83bb-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="e83bb-134">RepeatCount</span></span> 

<span data-ttu-id="e83bb-135">Die Anzahl der Wiederholungen für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e83bb-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="e83bb-136">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="e83bb-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="e83bb-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="e83bb-137">ScanCode</span></span> 

<span data-ttu-id="e83bb-138">Der Überprüfungscode.</span><span class="sxs-lookup"><span data-stu-id="e83bb-138">The scan code.</span></span>

> <span data-ttu-id="e83bb-139">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="e83bb-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="e83bb-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="e83bb-140">WasKeyDown</span></span> 

<span data-ttu-id="e83bb-141">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="e83bb-141">The previous key state.</span></span>

> <span data-ttu-id="e83bb-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="e83bb-142">public int [WasKeyDown](#waskeydown)</span></span>


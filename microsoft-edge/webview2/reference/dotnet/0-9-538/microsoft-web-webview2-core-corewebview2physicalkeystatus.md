---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: 17ed4a578234a056a7e6ff347829a12e39fa93bd
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010922"
---
# <span data-ttu-id="70b58-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus-Struktur</span><span class="sxs-lookup"><span data-stu-id="70b58-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="70b58-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="70b58-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="70b58-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="70b58-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="70b58-107">Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="70b58-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="70b58-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="70b58-108">Summary</span></span>

 <span data-ttu-id="70b58-109">Member</span><span class="sxs-lookup"><span data-stu-id="70b58-109">Members</span></span>                        | <span data-ttu-id="70b58-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="70b58-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="70b58-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="70b58-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="70b58-112">Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="70b58-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="70b58-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="70b58-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="70b58-114">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="70b58-114">The transition state.</span></span>
[<span data-ttu-id="70b58-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="70b58-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="70b58-116">Der kontextcode.</span><span class="sxs-lookup"><span data-stu-id="70b58-116">The context code.</span></span>
[<span data-ttu-id="70b58-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="70b58-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="70b58-118">Die Anzahl der Wiederholungen für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="70b58-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="70b58-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="70b58-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="70b58-120">Der Überprüfungscode.</span><span class="sxs-lookup"><span data-stu-id="70b58-120">The scan code.</span></span>
[<span data-ttu-id="70b58-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="70b58-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="70b58-122">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="70b58-122">The previous key state.</span></span>

<span data-ttu-id="70b58-123">Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="70b58-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="70b58-124">Member</span><span class="sxs-lookup"><span data-stu-id="70b58-124">Members</span></span>

#### <span data-ttu-id="70b58-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="70b58-125">IsExtendedKey</span></span> 

<span data-ttu-id="70b58-126">Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="70b58-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="70b58-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="70b58-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="70b58-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="70b58-128">IsKeyReleased</span></span> 

<span data-ttu-id="70b58-129">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="70b58-129">The transition state.</span></span>

> <span data-ttu-id="70b58-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="70b58-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="70b58-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="70b58-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="70b58-132">Der kontextcode.</span><span class="sxs-lookup"><span data-stu-id="70b58-132">The context code.</span></span>

> <span data-ttu-id="70b58-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="70b58-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="70b58-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="70b58-134">RepeatCount</span></span> 

<span data-ttu-id="70b58-135">Die Anzahl der Wiederholungen für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="70b58-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="70b58-136">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="70b58-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="70b58-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="70b58-137">ScanCode</span></span> 

<span data-ttu-id="70b58-138">Der Überprüfungscode.</span><span class="sxs-lookup"><span data-stu-id="70b58-138">The scan code.</span></span>

> <span data-ttu-id="70b58-139">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="70b58-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="70b58-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="70b58-140">WasKeyDown</span></span> 

<span data-ttu-id="70b58-141">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="70b58-141">The previous key state.</span></span>

> <span data-ttu-id="70b58-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="70b58-142">public int [WasKeyDown](#waskeydown)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: eecf4dd59d12c30667defd4e078e8624718bde26
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884589"
---
# <span data-ttu-id="9752a-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus-Struktur</span><span class="sxs-lookup"><span data-stu-id="9752a-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="9752a-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="9752a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="9752a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="9752a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="9752a-107">Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="9752a-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="9752a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9752a-108">Summary</span></span>

 <span data-ttu-id="9752a-109">Member</span><span class="sxs-lookup"><span data-stu-id="9752a-109">Members</span></span>                        | <span data-ttu-id="9752a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9752a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9752a-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="9752a-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="9752a-112">Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="9752a-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="9752a-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="9752a-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="9752a-114">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="9752a-114">The transition state.</span></span>
[<span data-ttu-id="9752a-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="9752a-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="9752a-116">Der kontextcode.</span><span class="sxs-lookup"><span data-stu-id="9752a-116">The context code.</span></span>
[<span data-ttu-id="9752a-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="9752a-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="9752a-118">Die Anzahl der Wiederholungen für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9752a-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="9752a-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="9752a-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="9752a-120">Der Überprüfungscode.</span><span class="sxs-lookup"><span data-stu-id="9752a-120">The scan code.</span></span>
[<span data-ttu-id="9752a-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="9752a-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="9752a-122">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="9752a-122">The previous key state.</span></span>

<span data-ttu-id="9752a-123">Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="9752a-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="9752a-124">Member</span><span class="sxs-lookup"><span data-stu-id="9752a-124">Members</span></span>

#### <span data-ttu-id="9752a-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="9752a-125">IsExtendedKey</span></span> 

<span data-ttu-id="9752a-126">Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="9752a-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="9752a-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="9752a-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="9752a-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="9752a-128">IsKeyReleased</span></span> 

<span data-ttu-id="9752a-129">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="9752a-129">The transition state.</span></span>

> <span data-ttu-id="9752a-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="9752a-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="9752a-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="9752a-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="9752a-132">Der kontextcode.</span><span class="sxs-lookup"><span data-stu-id="9752a-132">The context code.</span></span>

> <span data-ttu-id="9752a-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="9752a-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="9752a-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="9752a-134">RepeatCount</span></span> 

<span data-ttu-id="9752a-135">Die Anzahl der Wiederholungen für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9752a-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="9752a-136">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="9752a-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="9752a-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="9752a-137">ScanCode</span></span> 

<span data-ttu-id="9752a-138">Der Überprüfungscode.</span><span class="sxs-lookup"><span data-stu-id="9752a-138">The scan code.</span></span>

> <span data-ttu-id="9752a-139">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="9752a-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="9752a-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="9752a-140">WasKeyDown</span></span> 

<span data-ttu-id="9752a-141">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="9752a-141">The previous key state.</span></span>

> <span data-ttu-id="9752a-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="9752a-142">public int [WasKeyDown](#waskeydown)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: bd63bda6b7835ff5edb30b8b1b22f877f4c96e14
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697595"
---
# <span data-ttu-id="18c70-104">Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus-Struktur</span><span class="sxs-lookup"><span data-stu-id="18c70-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

> [!NOTE]
> <span data-ttu-id="18c70-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="18c70-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="18c70-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="18c70-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="18c70-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="18c70-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="18c70-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="18c70-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="18c70-109">Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="18c70-109">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="18c70-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="18c70-110">Summary</span></span>

 <span data-ttu-id="18c70-111">Member</span><span class="sxs-lookup"><span data-stu-id="18c70-111">Members</span></span>                        | <span data-ttu-id="18c70-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="18c70-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="18c70-113">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="18c70-113">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="18c70-114">Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="18c70-114">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="18c70-115">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="18c70-115">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="18c70-116">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="18c70-116">The transition state.</span></span>
[<span data-ttu-id="18c70-117">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="18c70-117">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="18c70-118">Der kontextcode.</span><span class="sxs-lookup"><span data-stu-id="18c70-118">The context code.</span></span>
[<span data-ttu-id="18c70-119">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="18c70-119">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="18c70-120">Die Anzahl der Wiederholungen für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="18c70-120">The repeat count for the current message.</span></span>
[<span data-ttu-id="18c70-121">ScanCode</span><span class="sxs-lookup"><span data-stu-id="18c70-121">ScanCode</span></span>](#scancode) | <span data-ttu-id="18c70-122">Der Überprüfungscode.</span><span class="sxs-lookup"><span data-stu-id="18c70-122">The scan code.</span></span>
[<span data-ttu-id="18c70-123">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="18c70-123">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="18c70-124">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="18c70-124">The previous key state.</span></span>

<span data-ttu-id="18c70-125">Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="18c70-125">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="18c70-126">Member</span><span class="sxs-lookup"><span data-stu-id="18c70-126">Members</span></span>

#### <span data-ttu-id="18c70-127">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="18c70-127">IsExtendedKey</span></span> 

<span data-ttu-id="18c70-128">Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="18c70-128">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="18c70-129">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="18c70-129">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="18c70-130">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="18c70-130">IsKeyReleased</span></span> 

<span data-ttu-id="18c70-131">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="18c70-131">The transition state.</span></span>

> <span data-ttu-id="18c70-132">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="18c70-132">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="18c70-133">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="18c70-133">IsMenuKeyDown</span></span> 

<span data-ttu-id="18c70-134">Der kontextcode.</span><span class="sxs-lookup"><span data-stu-id="18c70-134">The context code.</span></span>

> <span data-ttu-id="18c70-135">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="18c70-135">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="18c70-136">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="18c70-136">RepeatCount</span></span> 

<span data-ttu-id="18c70-137">Die Anzahl der Wiederholungen für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="18c70-137">The repeat count for the current message.</span></span>

> <span data-ttu-id="18c70-138">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="18c70-138">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="18c70-139">ScanCode</span><span class="sxs-lookup"><span data-stu-id="18c70-139">ScanCode</span></span> 

<span data-ttu-id="18c70-140">Der Überprüfungscode.</span><span class="sxs-lookup"><span data-stu-id="18c70-140">The scan code.</span></span>

> <span data-ttu-id="18c70-141">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="18c70-141">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="18c70-142">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="18c70-142">WasKeyDown</span></span> 

<span data-ttu-id="18c70-143">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="18c70-143">The previous key state.</span></span>

> <span data-ttu-id="18c70-144">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="18c70-144">public int [WasKeyDown](#waskeydown)</span></span>


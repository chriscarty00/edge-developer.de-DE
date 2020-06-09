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
ms.openlocfilehash: e0fb3f9ff7114b0c4f2a42893adabfd72e9616de
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698775"
---
# <span data-ttu-id="f94f6-104">Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus-Struktur</span><span class="sxs-lookup"><span data-stu-id="f94f6-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="f94f6-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f94f6-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f94f6-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="f94f6-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f94f6-107">Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="f94f6-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="f94f6-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f94f6-108">Summary</span></span>

 <span data-ttu-id="f94f6-109">Member</span><span class="sxs-lookup"><span data-stu-id="f94f6-109">Members</span></span>                        | <span data-ttu-id="f94f6-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f94f6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f94f6-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="f94f6-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="f94f6-112">Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="f94f6-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="f94f6-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="f94f6-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="f94f6-114">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="f94f6-114">The transition state.</span></span>
[<span data-ttu-id="f94f6-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="f94f6-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="f94f6-116">Der kontextcode.</span><span class="sxs-lookup"><span data-stu-id="f94f6-116">The context code.</span></span>
[<span data-ttu-id="f94f6-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="f94f6-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="f94f6-118">Die Anzahl der Wiederholungen für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f94f6-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="f94f6-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="f94f6-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="f94f6-120">Der Überprüfungscode.</span><span class="sxs-lookup"><span data-stu-id="f94f6-120">The scan code.</span></span>
[<span data-ttu-id="f94f6-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="f94f6-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="f94f6-122">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="f94f6-122">The previous key state.</span></span>

<span data-ttu-id="f94f6-123">Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="f94f6-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="f94f6-124">Member</span><span class="sxs-lookup"><span data-stu-id="f94f6-124">Members</span></span>

#### <span data-ttu-id="f94f6-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="f94f6-125">IsExtendedKey</span></span> 

<span data-ttu-id="f94f6-126">Gibt an, ob es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="f94f6-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="f94f6-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="f94f6-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="f94f6-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="f94f6-128">IsKeyReleased</span></span> 

<span data-ttu-id="f94f6-129">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="f94f6-129">The transition state.</span></span>

> <span data-ttu-id="f94f6-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="f94f6-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="f94f6-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="f94f6-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="f94f6-132">Der kontextcode.</span><span class="sxs-lookup"><span data-stu-id="f94f6-132">The context code.</span></span>

> <span data-ttu-id="f94f6-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="f94f6-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="f94f6-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="f94f6-134">RepeatCount</span></span> 

<span data-ttu-id="f94f6-135">Die Anzahl der Wiederholungen für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f94f6-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="f94f6-136">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="f94f6-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="f94f6-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="f94f6-137">ScanCode</span></span> 

<span data-ttu-id="f94f6-138">Der Überprüfungscode.</span><span class="sxs-lookup"><span data-stu-id="f94f6-138">The scan code.</span></span>

> <span data-ttu-id="f94f6-139">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="f94f6-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="f94f6-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="f94f6-140">WasKeyDown</span></span> 

<span data-ttu-id="f94f6-141">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="f94f6-141">The previous key state.</span></span>

> <span data-ttu-id="f94f6-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="f94f6-142">public int [WasKeyDown](#waskeydown)</span></span>


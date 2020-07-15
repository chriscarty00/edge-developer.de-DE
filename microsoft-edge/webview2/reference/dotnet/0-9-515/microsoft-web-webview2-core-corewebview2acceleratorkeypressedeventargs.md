---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ecf68bfc338d06fdd2d1a104126685ca105810b0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879380"
---
# <span data-ttu-id="f850d-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="f850d-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="f850d-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="f850d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f850d-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f850d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="f850d-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f850d-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f850d-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f850d-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f850d-109">Ereignis-args für das AcceleratorKeyPressed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f850d-109">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="f850d-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f850d-110">Summary</span></span>

 <span data-ttu-id="f850d-111">Member</span><span class="sxs-lookup"><span data-stu-id="f850d-111">Members</span></span>                        | <span data-ttu-id="f850d-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f850d-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f850d-113">Handled</span><span class="sxs-lookup"><span data-stu-id="f850d-113">Handled</span></span>](#handled) | <span data-ttu-id="f850d-114">Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="f850d-114">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="f850d-115">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="f850d-115">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="f850d-116">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="f850d-116">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="f850d-117">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="f850d-117">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="f850d-118">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="f850d-118">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="f850d-119">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="f850d-119">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="f850d-120">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="f850d-120">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="f850d-121">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="f850d-121">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="f850d-122">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f850d-122">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="f850d-123">Member</span><span class="sxs-lookup"><span data-stu-id="f850d-123">Members</span></span>

#### <span data-ttu-id="f850d-124">Handled</span><span class="sxs-lookup"><span data-stu-id="f850d-124">Handled</span></span> 

<span data-ttu-id="f850d-125">Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="f850d-125">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="f850d-126">öffentliche bool- [Behandlung](#handled)</span><span class="sxs-lookup"><span data-stu-id="f850d-126">public bool [Handled](#handled)</span></span>

<span data-ttu-id="f850d-127">Wenn die Handled-Eigenschaft auf true festgelegt ist, wird dadurch verhindert, dass die WebView die Standardaktion für diese Zugriffstaste ausführt.</span><span class="sxs-lookup"><span data-stu-id="f850d-127">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="f850d-128">Andernfalls führt WebView die Standardaktion für die Zugriffstasten Taste aus.</span><span class="sxs-lookup"><span data-stu-id="f850d-128">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="f850d-129">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="f850d-129">KeyEventKind</span></span> 

<span data-ttu-id="f850d-130">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="f850d-130">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="f850d-131">öffentliche [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) - [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="f850d-131">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="f850d-132">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="f850d-132">KeyEventLParam</span></span> 

<span data-ttu-id="f850d-133">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="f850d-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="f850d-134">public int [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="f850d-134">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="f850d-135">Lesen Sie die Dokumentation zu den WM_KEYDOWN-und WM_KEYUP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="f850d-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="f850d-136">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="f850d-136">PhysicalKeyStatus</span></span> 

<span data-ttu-id="f850d-137">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="f850d-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="f850d-138">öffentliche [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) - [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="f850d-138">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="f850d-139">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="f850d-139">VirtualKey</span></span> 

<span data-ttu-id="f850d-140">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f850d-140">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="f850d-141">public uint [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="f850d-141">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="f850d-142">Hierbei handelt es sich um eine der virtuellen Win32-Schlüssel Konstanten wie VK_RETURN oder einen (Großbuchstaben) ASCII-Wert wie "A".</span><span class="sxs-lookup"><span data-stu-id="f850d-142">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="f850d-143">Sie können überprüfen, ob STRG oder ALT gedrückt werden, indem Sie GetKeyState (VK_CONTROL) oder GetKeyState (VK_MENU) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f850d-143">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>


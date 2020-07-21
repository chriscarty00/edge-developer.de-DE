---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 10694292c7943f87753ae87f6129655b27f425f3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885142"
---
# <span data-ttu-id="97b62-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="97b62-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="97b62-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="97b62-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="97b62-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="97b62-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="97b62-107">Ereignis-args für das AcceleratorKeyPressed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="97b62-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="97b62-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="97b62-108">Summary</span></span>

 <span data-ttu-id="97b62-109">Member</span><span class="sxs-lookup"><span data-stu-id="97b62-109">Members</span></span>                        | <span data-ttu-id="97b62-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="97b62-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="97b62-111">Handled</span><span class="sxs-lookup"><span data-stu-id="97b62-111">Handled</span></span>](#handled) | <span data-ttu-id="97b62-112">Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="97b62-112">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="97b62-113">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="97b62-113">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="97b62-114">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="97b62-114">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="97b62-115">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="97b62-115">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="97b62-116">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="97b62-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="97b62-117">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="97b62-117">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="97b62-118">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="97b62-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="97b62-119">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="97b62-119">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="97b62-120">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="97b62-120">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="97b62-121">Member</span><span class="sxs-lookup"><span data-stu-id="97b62-121">Members</span></span>

#### <span data-ttu-id="97b62-122">Handled</span><span class="sxs-lookup"><span data-stu-id="97b62-122">Handled</span></span> 

<span data-ttu-id="97b62-123">Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="97b62-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="97b62-124">öffentliche bool- [Behandlung](#handled)</span><span class="sxs-lookup"><span data-stu-id="97b62-124">public bool [Handled](#handled)</span></span>

<span data-ttu-id="97b62-125">Wenn die Handled-Eigenschaft auf true festgelegt ist, wird dadurch verhindert, dass die WebView die Standardaktion für diese Zugriffstaste ausführt.</span><span class="sxs-lookup"><span data-stu-id="97b62-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="97b62-126">Andernfalls führt WebView die Standardaktion für die Zugriffstasten Taste aus.</span><span class="sxs-lookup"><span data-stu-id="97b62-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="97b62-127">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="97b62-127">KeyEventKind</span></span> 

<span data-ttu-id="97b62-128">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="97b62-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="97b62-129">öffentliche [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) - [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="97b62-129">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="97b62-130">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="97b62-130">KeyEventLParam</span></span> 

<span data-ttu-id="97b62-131">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="97b62-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="97b62-132">public int [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="97b62-132">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="97b62-133">Lesen Sie die Dokumentation zu den WM_KEYDOWN-und WM_KEYUP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="97b62-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="97b62-134">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="97b62-134">PhysicalKeyStatus</span></span> 

<span data-ttu-id="97b62-135">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="97b62-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="97b62-136">öffentliche [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) - [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="97b62-136">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="97b62-137">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="97b62-137">VirtualKey</span></span> 

<span data-ttu-id="97b62-138">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="97b62-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="97b62-139">public uint [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="97b62-139">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="97b62-140">Hierbei handelt es sich um eine der virtuellen Win32-Schlüssel Konstanten wie VK_RETURN oder einen (Großbuchstaben) ASCII-Wert wie "A".</span><span class="sxs-lookup"><span data-stu-id="97b62-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="97b62-141">Sie können überprüfen, ob STRG oder ALT gedrückt werden, indem Sie GetKeyState (VK_CONTROL) oder GetKeyState (VK_MENU) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="97b62-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>


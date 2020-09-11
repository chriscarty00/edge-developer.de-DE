---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
ms.openlocfilehash: 16af4247c494d1d09155110755d7936487f2e84e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012102"
---
# <span data-ttu-id="ddb3d-104">Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="ddb3d-104">Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

<span data-ttu-id="ddb3d-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ddb3d-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ddb3d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="ddb3d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ddb3d-107">Ereignis-args für das AcceleratorKeyPressed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="ddb3d-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ddb3d-108">Summary</span></span>

 <span data-ttu-id="ddb3d-109">Member</span><span class="sxs-lookup"><span data-stu-id="ddb3d-109">Members</span></span>                        | <span data-ttu-id="ddb3d-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ddb3d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ddb3d-111">Handled</span><span class="sxs-lookup"><span data-stu-id="ddb3d-111">Handled</span></span>](#handled) | <span data-ttu-id="ddb3d-112">Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-112">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="ddb3d-113">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="ddb3d-113">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="ddb3d-114">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-114">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="ddb3d-115">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="ddb3d-115">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="ddb3d-116">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="ddb3d-117">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="ddb3d-117">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="ddb3d-118">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="ddb3d-119">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="ddb3d-119">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="ddb3d-120">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-120">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="ddb3d-121">Member</span><span class="sxs-lookup"><span data-stu-id="ddb3d-121">Members</span></span>

#### <span data-ttu-id="ddb3d-122">Handled</span><span class="sxs-lookup"><span data-stu-id="ddb3d-122">Handled</span></span> 

<span data-ttu-id="ddb3d-123">Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="ddb3d-124">öffentliche bool- [Behandlung](#handled)</span><span class="sxs-lookup"><span data-stu-id="ddb3d-124">public bool [Handled](#handled)</span></span>

<span data-ttu-id="ddb3d-125">Wenn die Handled-Eigenschaft auf true festgelegt ist, wird dadurch verhindert, dass die WebView die Standardaktion für diese Zugriffstaste ausführt.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="ddb3d-126">Andernfalls führt WebView die Standardaktion für die Zugriffstasten Taste aus.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="ddb3d-127">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="ddb3d-127">KeyEventKind</span></span> 

<span data-ttu-id="ddb3d-128">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="ddb3d-129">öffentliche [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) - [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="ddb3d-129">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="ddb3d-130">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="ddb3d-130">KeyEventLParam</span></span> 

<span data-ttu-id="ddb3d-131">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="ddb3d-132">public int [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="ddb3d-132">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="ddb3d-133">Lesen Sie die Dokumentation zu den WM_KEYDOWN-und WM_KEYUP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="ddb3d-134">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="ddb3d-134">PhysicalKeyStatus</span></span> 

<span data-ttu-id="ddb3d-135">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="ddb3d-136">öffentliche [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) - [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="ddb3d-136">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="ddb3d-137">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="ddb3d-137">VirtualKey</span></span> 

<span data-ttu-id="ddb3d-138">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="ddb3d-139">public uint [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="ddb3d-139">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="ddb3d-140">Hierbei handelt es sich um eine der virtuellen Win32-Schlüssel Konstanten wie VK_RETURN oder einen (Großbuchstaben) ASCII-Wert wie "A".</span><span class="sxs-lookup"><span data-stu-id="ddb3d-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="ddb3d-141">Sie können überprüfen, ob STRG oder ALT gedrückt werden, indem Sie GetKeyState (VK_CONTROL) oder GetKeyState (VK_MENU) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ddb3d-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>


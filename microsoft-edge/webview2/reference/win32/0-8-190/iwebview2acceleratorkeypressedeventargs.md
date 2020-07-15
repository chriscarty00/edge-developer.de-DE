---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 5d052488d23f3d016ba2fd71eb929d5aa2ebea6e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877364"
---
# <span data-ttu-id="23077-104">0.8.355-Interface-IWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="23077-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="23077-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="23077-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="23077-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="23077-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="23077-107">Ereignis-args für das AcceleratorKeyPressed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="23077-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="23077-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="23077-108">Summary</span></span>

 <span data-ttu-id="23077-109">Member</span><span class="sxs-lookup"><span data-stu-id="23077-109">Members</span></span>                        | <span data-ttu-id="23077-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="23077-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="23077-111">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="23077-111">get_KeyEventType</span></span>](#get_keyeventtype) | <span data-ttu-id="23077-112">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="23077-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="23077-113">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="23077-113">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="23077-114">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="23077-114">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="23077-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="23077-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="23077-116">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="23077-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="23077-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="23077-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="23077-118">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="23077-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="23077-119">Behandeln</span><span class="sxs-lookup"><span data-stu-id="23077-119">Handle</span></span>](#handle) | <span data-ttu-id="23077-120">Durch diesen Aufruf kann der Browserprozess fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="23077-120">Calling this will allow the browser process to continue.</span></span>

## <span data-ttu-id="23077-121">Member</span><span class="sxs-lookup"><span data-stu-id="23077-121">Members</span></span>

#### <span data-ttu-id="23077-122">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="23077-122">get_KeyEventType</span></span> 

<span data-ttu-id="23077-123">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="23077-123">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="23077-124">Public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyeventtype)</span><span class="sxs-lookup"><span data-stu-id="23077-124">public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyEventType)</span></span>

<span data-ttu-id="23077-125">Hierbei handelt es sich um einen WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN oder WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span><span class="sxs-lookup"><span data-stu-id="23077-125">This is one of WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN, or WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span></span>

#### <span data-ttu-id="23077-126">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="23077-126">get_VirtualKey</span></span> 

<span data-ttu-id="23077-127">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="23077-127">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="23077-128">Public HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="23077-128">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="23077-129">Hierbei handelt es sich um eine der virtuellen Win32-Schlüssel Konstanten wie VK_RETURN oder einen (Großbuchstaben) ASCII-Wert wie "A".</span><span class="sxs-lookup"><span data-stu-id="23077-129">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="23077-130">Sie können überprüfen, ob STRG oder ALT gedrückt werden, indem Sie GetKeyState (VK_CONTROL) oder GetKeyState (VK_MENU) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="23077-130">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="23077-131">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="23077-131">get_KeyEventLParam</span></span> 

<span data-ttu-id="23077-132">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="23077-132">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="23077-133">Public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* LPARAM)</span><span class="sxs-lookup"><span data-stu-id="23077-133">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="23077-134">Lesen Sie die Dokumentation zu den WM_KEYDOWN-und WM_KEYUP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="23077-134">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="23077-135">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="23077-135">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="23077-136">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="23077-136">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="23077-137">Public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="23077-137">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="23077-138">Behandeln</span><span class="sxs-lookup"><span data-stu-id="23077-138">Handle</span></span> 

<span data-ttu-id="23077-139">Durch diesen Aufruf kann der Browserprozess fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="23077-139">Calling this will allow the browser process to continue.</span></span>

> <span data-ttu-id="23077-140">öffentliches HRESULT- [handle](#handle)(bool Handled)</span><span class="sxs-lookup"><span data-stu-id="23077-140">public HRESULT [Handle](#handle)(BOOL handled)</span></span>

<span data-ttu-id="23077-141">Durch das Übergeben von true wird verhindert, dass der Browser die Standardaktion für diese Zugriffstaste ausführt.</span><span class="sxs-lookup"><span data-stu-id="23077-141">Passing TRUE will prevent the browser from performing the default action for this accelerator key.</span></span> <span data-ttu-id="23077-142">Wenn der Ereignishandler ohne Aufrufen des [Handles ()](#handle)zurückgibt, entspricht dies dem aufrufenden handle (false).</span><span class="sxs-lookup"><span data-stu-id="23077-142">If the event handler returns without calling [Handle()](#handle), it is equivalent to calling Handle(FALSE).</span></span> <span data-ttu-id="23077-143">Das Aufrufen des [Handles ()](#handle) , nachdem es bereits aufgerufen wurde oder der Ereignishandler zurückgegeben wurde, bewirkt nichts.</span><span class="sxs-lookup"><span data-stu-id="23077-143">Calling [Handle()](#handle) after it has already been called or the event handler has returned will do nothing.</span></span>


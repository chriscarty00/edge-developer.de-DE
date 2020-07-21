---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 885ad6b161fbde6721e1812735ab50d7e0c3e8d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885052"
---
# <span data-ttu-id="66222-104">0.8.355-Interface-IWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="66222-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="66222-105">Ereignis-args für das AcceleratorKeyPressed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="66222-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="66222-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="66222-106">Summary</span></span>

 <span data-ttu-id="66222-107">Member</span><span class="sxs-lookup"><span data-stu-id="66222-107">Members</span></span>                        | <span data-ttu-id="66222-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="66222-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="66222-109">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="66222-109">get_KeyEventType</span></span>](#get_keyeventtype) | <span data-ttu-id="66222-110">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="66222-110">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="66222-111">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="66222-111">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="66222-112">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="66222-112">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="66222-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="66222-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="66222-114">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="66222-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="66222-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="66222-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="66222-116">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="66222-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="66222-117">Behandeln</span><span class="sxs-lookup"><span data-stu-id="66222-117">Handle</span></span>](#handle) | <span data-ttu-id="66222-118">Durch diesen Aufruf kann der Browserprozess fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="66222-118">Calling this will allow the browser process to continue.</span></span>

## <span data-ttu-id="66222-119">Member</span><span class="sxs-lookup"><span data-stu-id="66222-119">Members</span></span>

#### <span data-ttu-id="66222-120">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="66222-120">get_KeyEventType</span></span> 

<span data-ttu-id="66222-121">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="66222-121">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="66222-122">Public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyeventtype)</span><span class="sxs-lookup"><span data-stu-id="66222-122">public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyEventType)</span></span>

<span data-ttu-id="66222-123">Hierbei handelt es sich um einen WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN oder WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span><span class="sxs-lookup"><span data-stu-id="66222-123">This is one of WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN, or WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span></span>

#### <span data-ttu-id="66222-124">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="66222-124">get_VirtualKey</span></span> 

<span data-ttu-id="66222-125">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="66222-125">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="66222-126">Public HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="66222-126">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="66222-127">Hierbei handelt es sich um eine der virtuellen Win32-Schlüssel Konstanten wie VK_RETURN oder einen (Großbuchstaben) ASCII-Wert wie "A".</span><span class="sxs-lookup"><span data-stu-id="66222-127">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="66222-128">Sie können überprüfen, ob STRG oder ALT gedrückt werden, indem Sie GetKeyState (VK_CONTROL) oder GetKeyState (VK_MENU) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="66222-128">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="66222-129">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="66222-129">get_KeyEventLParam</span></span> 

<span data-ttu-id="66222-130">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="66222-130">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="66222-131">Public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* LPARAM)</span><span class="sxs-lookup"><span data-stu-id="66222-131">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="66222-132">Lesen Sie die Dokumentation zu den WM_KEYDOWN-und WM_KEYUP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="66222-132">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="66222-133">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="66222-133">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="66222-134">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="66222-134">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="66222-135">Public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="66222-135">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="66222-136">Behandeln</span><span class="sxs-lookup"><span data-stu-id="66222-136">Handle</span></span> 

<span data-ttu-id="66222-137">Durch diesen Aufruf kann der Browserprozess fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="66222-137">Calling this will allow the browser process to continue.</span></span>

> <span data-ttu-id="66222-138">öffentliches HRESULT- [handle](#handle)(bool Handled)</span><span class="sxs-lookup"><span data-stu-id="66222-138">public HRESULT [Handle](#handle)(BOOL handled)</span></span>

<span data-ttu-id="66222-139">Durch das Übergeben von true wird verhindert, dass der Browser die Standardaktion für diese Zugriffstaste ausführt.</span><span class="sxs-lookup"><span data-stu-id="66222-139">Passing TRUE will prevent the browser from performing the default action for this accelerator key.</span></span> <span data-ttu-id="66222-140">Wenn der Ereignishandler ohne Aufrufen des [Handles ()](#handle)zurückgibt, entspricht dies dem aufrufenden handle (false).</span><span class="sxs-lookup"><span data-stu-id="66222-140">If the event handler returns without calling [Handle()](#handle), it is equivalent to calling Handle(FALSE).</span></span> <span data-ttu-id="66222-141">Das Aufrufen des [Handles ()](#handle) , nachdem es bereits aufgerufen wurde oder der Ereignishandler zurückgegeben wurde, bewirkt nichts.</span><span class="sxs-lookup"><span data-stu-id="66222-141">Calling [Handle()](#handle) after it has already been called or the event handler has returned will do nothing.</span></span>


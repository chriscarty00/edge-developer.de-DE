---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 25d11995dd305a1958d6252c2ddf3afdb313fad1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697182"
---
# <span data-ttu-id="709e0-104">Schnittstellen ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="709e0-104">interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="709e0-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="709e0-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="709e0-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="709e0-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="709e0-107">Ereignis-args für das AcceleratorKeyPressed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="709e0-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="709e0-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="709e0-108">Summary</span></span>

 <span data-ttu-id="709e0-109">Member</span><span class="sxs-lookup"><span data-stu-id="709e0-109">Members</span></span>                        | <span data-ttu-id="709e0-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="709e0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="709e0-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="709e0-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="709e0-112">Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="709e0-112">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="709e0-113">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="709e0-113">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="709e0-114">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="709e0-114">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="709e0-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="709e0-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="709e0-116">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="709e0-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="709e0-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="709e0-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="709e0-118">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="709e0-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="709e0-119">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="709e0-119">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="709e0-120">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="709e0-120">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="709e0-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="709e0-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="709e0-122">Legt die Handled-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="709e0-122">Sets the Handled property.</span></span>

## <span data-ttu-id="709e0-123">Member</span><span class="sxs-lookup"><span data-stu-id="709e0-123">Members</span></span>

#### <span data-ttu-id="709e0-124">get_Handled</span><span class="sxs-lookup"><span data-stu-id="709e0-124">get_Handled</span></span> 

<span data-ttu-id="709e0-125">Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="709e0-125">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="709e0-126">öffentliche HRESULT- [get_Handled](#get_handled)(bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="709e0-126">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="709e0-127">Wenn die Handled-Eigenschaft auf true festgelegt ist, wird dadurch verhindert, dass die WebView die Standardaktion für diese Zugriffstaste ausführt.</span><span class="sxs-lookup"><span data-stu-id="709e0-127">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="709e0-128">Andernfalls führt WebView die Standardaktion für die Zugriffstasten Taste aus.</span><span class="sxs-lookup"><span data-stu-id="709e0-128">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="709e0-129">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="709e0-129">get_KeyEventKind</span></span> 

<span data-ttu-id="709e0-130">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="709e0-130">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="709e0-131">Public HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="709e0-131">public HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="709e0-132">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="709e0-132">get_KeyEventLParam</span></span> 

<span data-ttu-id="709e0-133">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="709e0-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="709e0-134">Public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* LPARAM)</span><span class="sxs-lookup"><span data-stu-id="709e0-134">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="709e0-135">Lesen Sie die Dokumentation zu den WM_KEYDOWN-und WM_KEYUP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="709e0-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="709e0-136">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="709e0-136">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="709e0-137">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="709e0-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="709e0-138">Public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="709e0-138">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="709e0-139">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="709e0-139">get_VirtualKey</span></span> 

<span data-ttu-id="709e0-140">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="709e0-140">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="709e0-141">Public HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="709e0-141">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="709e0-142">Hierbei handelt es sich um eine der virtuellen Win32-Schlüssel Konstanten wie VK_RETURN oder einen (Großbuchstaben) ASCII-Wert wie "A".</span><span class="sxs-lookup"><span data-stu-id="709e0-142">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="709e0-143">Sie können überprüfen, ob STRG oder ALT gedrückt werden, indem Sie GetKeyState (VK_CONTROL) oder GetKeyState (VK_MENU) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="709e0-143">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="709e0-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="709e0-144">put_Handled</span></span> 

<span data-ttu-id="709e0-145">Legt die Handled-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="709e0-145">Sets the Handled property.</span></span>

> <span data-ttu-id="709e0-146">öffentliche HRESULT- [put_Handled](#put_handled)(bool Handled)</span><span class="sxs-lookup"><span data-stu-id="709e0-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>


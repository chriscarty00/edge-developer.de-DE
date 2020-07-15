---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e7a512201c1ef7917a54b93dbd06587294e76f78
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881179"
---
# <span data-ttu-id="82d27-104">0.9.430-Interface-ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="82d27-104">0.9.430 - interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="82d27-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="82d27-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="82d27-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="82d27-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="82d27-107">Ereignis-args für das AcceleratorKeyPressed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82d27-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="82d27-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="82d27-108">Summary</span></span>

 <span data-ttu-id="82d27-109">Member</span><span class="sxs-lookup"><span data-stu-id="82d27-109">Members</span></span>                        | <span data-ttu-id="82d27-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="82d27-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="82d27-111">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="82d27-111">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="82d27-112">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="82d27-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="82d27-113">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="82d27-113">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="82d27-114">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="82d27-114">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="82d27-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="82d27-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="82d27-116">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="82d27-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="82d27-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="82d27-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="82d27-118">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="82d27-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="82d27-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="82d27-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="82d27-120">Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="82d27-120">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="82d27-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="82d27-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="82d27-122">Legt die Handled-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="82d27-122">Sets the Handled property.</span></span>

## <span data-ttu-id="82d27-123">Member</span><span class="sxs-lookup"><span data-stu-id="82d27-123">Members</span></span>

#### <span data-ttu-id="82d27-124">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="82d27-124">get_KeyEventKind</span></span> 

<span data-ttu-id="82d27-125">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="82d27-125">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="82d27-126">Public HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="82d27-126">public HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="82d27-127">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="82d27-127">get_VirtualKey</span></span> 

<span data-ttu-id="82d27-128">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="82d27-128">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="82d27-129">Public HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="82d27-129">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="82d27-130">Hierbei handelt es sich um eine der virtuellen Win32-Schlüssel Konstanten wie VK_RETURN oder einen (Großbuchstaben) ASCII-Wert wie "A".</span><span class="sxs-lookup"><span data-stu-id="82d27-130">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="82d27-131">Sie können überprüfen, ob STRG oder ALT gedrückt werden, indem Sie GetKeyState (VK_CONTROL) oder GetKeyState (VK_MENU) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="82d27-131">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="82d27-132">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="82d27-132">get_KeyEventLParam</span></span> 

<span data-ttu-id="82d27-133">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="82d27-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="82d27-134">Public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* LPARAM)</span><span class="sxs-lookup"><span data-stu-id="82d27-134">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="82d27-135">Lesen Sie die Dokumentation zu den WM_KEYDOWN-und WM_KEYUP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="82d27-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="82d27-136">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="82d27-136">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="82d27-137">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="82d27-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="82d27-138">Public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="82d27-138">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="82d27-139">get_Handled</span><span class="sxs-lookup"><span data-stu-id="82d27-139">get_Handled</span></span> 

<span data-ttu-id="82d27-140">Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="82d27-140">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="82d27-141">öffentliche HRESULT- [get_Handled](#get_handled)(bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="82d27-141">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="82d27-142">Wenn die Handled-Eigenschaft auf true festgelegt ist, wird dadurch verhindert, dass die WebView die Standardaktion für diese Zugriffstaste ausführt.</span><span class="sxs-lookup"><span data-stu-id="82d27-142">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="82d27-143">Andernfalls führt WebView die Standardaktion für die Zugriffstasten Taste aus.</span><span class="sxs-lookup"><span data-stu-id="82d27-143">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="82d27-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="82d27-144">put_Handled</span></span> 

<span data-ttu-id="82d27-145">Legt die Handled-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="82d27-145">Sets the Handled property.</span></span>

> <span data-ttu-id="82d27-146">öffentliche HRESULT- [put_Handled](#put_handled)(bool Handled)</span><span class="sxs-lookup"><span data-stu-id="82d27-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>


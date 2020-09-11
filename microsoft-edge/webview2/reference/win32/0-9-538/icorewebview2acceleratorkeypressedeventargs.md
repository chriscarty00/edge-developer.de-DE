---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2AcceleratorKeyPressedEventArgs
ms.openlocfilehash: b646846c85c0e36fbcf7a55cd98f7495c252f8f9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010614"
---
# <span data-ttu-id="eaabf-104">0.9.579-Interface-ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="eaabf-104">0.9.579 - interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="eaabf-105">Ereignis-args für das AcceleratorKeyPressed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="eaabf-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="eaabf-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="eaabf-106">Summary</span></span>

 <span data-ttu-id="eaabf-107">Member</span><span class="sxs-lookup"><span data-stu-id="eaabf-107">Members</span></span>                        | <span data-ttu-id="eaabf-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="eaabf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eaabf-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="eaabf-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="eaabf-110">Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="eaabf-110">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="eaabf-111">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="eaabf-111">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="eaabf-112">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="eaabf-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="eaabf-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="eaabf-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="eaabf-114">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="eaabf-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="eaabf-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="eaabf-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="eaabf-116">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="eaabf-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="eaabf-117">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="eaabf-117">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="eaabf-118">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="eaabf-118">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="eaabf-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="eaabf-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="eaabf-120">Legt die Handled-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="eaabf-120">Sets the Handled property.</span></span>

## <span data-ttu-id="eaabf-121">Member</span><span class="sxs-lookup"><span data-stu-id="eaabf-121">Members</span></span>

#### <span data-ttu-id="eaabf-122">get_Handled</span><span class="sxs-lookup"><span data-stu-id="eaabf-122">get_Handled</span></span> 

<span data-ttu-id="eaabf-123">Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="eaabf-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="eaabf-124">öffentliche HRESULT- [get_Handled](#get_handled)(bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="eaabf-124">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="eaabf-125">Wenn die Handled-Eigenschaft auf true festgelegt ist, wird dadurch verhindert, dass die WebView die Standardaktion für diese Zugriffstaste ausführt.</span><span class="sxs-lookup"><span data-stu-id="eaabf-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="eaabf-126">Andernfalls führt WebView die Standardaktion für die Zugriffstasten Taste aus.</span><span class="sxs-lookup"><span data-stu-id="eaabf-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="eaabf-127">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="eaabf-127">get_KeyEventKind</span></span> 

<span data-ttu-id="eaabf-128">Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="eaabf-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="eaabf-129">Public HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="eaabf-129">public HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="eaabf-130">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="eaabf-130">get_KeyEventLParam</span></span> 

<span data-ttu-id="eaabf-131">Der lParam-Wert, der die Fenstermeldung begleitet hat.</span><span class="sxs-lookup"><span data-stu-id="eaabf-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="eaabf-132">Public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* LPARAM)</span><span class="sxs-lookup"><span data-stu-id="eaabf-132">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="eaabf-133">Lesen Sie die Dokumentation zu den WM_KEYDOWN-und WM_KEYUP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="eaabf-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="eaabf-134">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="eaabf-134">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="eaabf-135">Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="eaabf-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="eaabf-136">Public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="eaabf-136">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="eaabf-137">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="eaabf-137">get_VirtualKey</span></span> 

<span data-ttu-id="eaabf-138">Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="eaabf-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="eaabf-139">Public HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="eaabf-139">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="eaabf-140">Hierbei handelt es sich um eine der virtuellen Win32-Schlüssel Konstanten wie VK_RETURN oder einen (Großbuchstaben) ASCII-Wert wie "A".</span><span class="sxs-lookup"><span data-stu-id="eaabf-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="eaabf-141">Sie können überprüfen, ob STRG oder ALT gedrückt werden, indem Sie GetKeyState (VK_CONTROL) oder GetKeyState (VK_MENU) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eaabf-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="eaabf-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="eaabf-142">put_Handled</span></span> 

<span data-ttu-id="eaabf-143">Legt die Handled-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="eaabf-143">Sets the Handled property.</span></span>

> <span data-ttu-id="eaabf-144">öffentliche HRESULT- [put_Handled](#put_handled)(bool Handled)</span><span class="sxs-lookup"><span data-stu-id="eaabf-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>


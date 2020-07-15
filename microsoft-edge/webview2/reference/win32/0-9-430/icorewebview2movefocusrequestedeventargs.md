---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: fe0c0fae0ec33cbc5ba50ca163b3f4fc8baa61b9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880955"
---
# <span data-ttu-id="5fd2d-104">0.9.430-Interface-ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5fd2d-104">0.9.430 - interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="5fd2d-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="5fd2d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="5fd2d-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="5fd2d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="5fd2d-107">Ereignis-args für das MoveFocusRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5fd2d-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="5fd2d-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5fd2d-108">Summary</span></span>

 <span data-ttu-id="5fd2d-109">Member</span><span class="sxs-lookup"><span data-stu-id="5fd2d-109">Members</span></span>                        | <span data-ttu-id="5fd2d-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5fd2d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5fd2d-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="5fd2d-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="5fd2d-112">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="5fd2d-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="5fd2d-113">get_Handled</span><span class="sxs-lookup"><span data-stu-id="5fd2d-113">get_Handled</span></span>](#get_handled) | <span data-ttu-id="5fd2d-114">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="5fd2d-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="5fd2d-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="5fd2d-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="5fd2d-116">Festlegen der Handled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5fd2d-116">Set the Handled property.</span></span>

## <span data-ttu-id="5fd2d-117">Member</span><span class="sxs-lookup"><span data-stu-id="5fd2d-117">Members</span></span>

#### <span data-ttu-id="5fd2d-118">get_Reason</span><span class="sxs-lookup"><span data-stu-id="5fd2d-118">get_Reason</span></span> 

<span data-ttu-id="5fd2d-119">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="5fd2d-119">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="5fd2d-120">Public HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="5fd2d-120">public HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="5fd2d-121">get_Handled</span><span class="sxs-lookup"><span data-stu-id="5fd2d-121">get_Handled</span></span> 

<span data-ttu-id="5fd2d-122">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="5fd2d-122">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="5fd2d-123">Public HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="5fd2d-123">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="5fd2d-124">Wenn die APP den Fokus an die gewünschte Position verschoben hat, sollte Sie die Handled-Eigenschaft auf true festlegen.</span><span class="sxs-lookup"><span data-stu-id="5fd2d-124">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="5fd2d-125">Wenn Handled-Eigenschaft auf false festgelegt ist, nachdem der Ereignishandler zurückgegeben wurde, wird Standardaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fd2d-125">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="5fd2d-126">Die Standardaktion besteht darin, das nächste Tabstopp-untergeordnete Fenster in der APP zu finden und zu versuchen, den Fokus auf dieses Fenster zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5fd2d-126">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="5fd2d-127">Wenn kein anderes Fenster zum Verschieben des Fokus vorhanden ist, wird der Fokus innerhalb des Webinhalts der WebView-Webinhalte durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="5fd2d-127">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="5fd2d-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="5fd2d-128">put_Handled</span></span> 

<span data-ttu-id="5fd2d-129">Festlegen der Handled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5fd2d-129">Set the Handled property.</span></span>

> <span data-ttu-id="5fd2d-130">Public HRESULT [put_Handled](#put_handled)(bool-Wert)</span><span class="sxs-lookup"><span data-stu-id="5fd2d-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>


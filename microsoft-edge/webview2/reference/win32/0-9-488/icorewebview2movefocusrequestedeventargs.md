---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: dc6c904150605dc05b2fef00600785b9840f0eb8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880528"
---
# <span data-ttu-id="7b726-104">0.9.515-Interface-ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7b726-104">0.9.515 - interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="7b726-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="7b726-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="7b726-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="7b726-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="7b726-107">Ereignis-args für das MoveFocusRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7b726-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="7b726-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7b726-108">Summary</span></span>

 <span data-ttu-id="7b726-109">Member</span><span class="sxs-lookup"><span data-stu-id="7b726-109">Members</span></span>                        | <span data-ttu-id="7b726-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7b726-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7b726-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="7b726-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="7b726-112">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="7b726-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="7b726-113">get_Reason</span><span class="sxs-lookup"><span data-stu-id="7b726-113">get_Reason</span></span>](#get_reason) | <span data-ttu-id="7b726-114">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="7b726-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="7b726-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="7b726-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="7b726-116">Festlegen der Handled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7b726-116">Set the Handled property.</span></span>

## <span data-ttu-id="7b726-117">Member</span><span class="sxs-lookup"><span data-stu-id="7b726-117">Members</span></span>

#### <span data-ttu-id="7b726-118">get_Handled</span><span class="sxs-lookup"><span data-stu-id="7b726-118">get_Handled</span></span> 

<span data-ttu-id="7b726-119">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="7b726-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="7b726-120">Public HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="7b726-120">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="7b726-121">Wenn die APP den Fokus an die gewünschte Position verschoben hat, sollte Sie die Handled-Eigenschaft auf true festlegen.</span><span class="sxs-lookup"><span data-stu-id="7b726-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="7b726-122">Wenn Handled-Eigenschaft auf false festgelegt ist, nachdem der Ereignishandler zurückgegeben wurde, wird Standardaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b726-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="7b726-123">Die Standardaktion besteht darin, das nächste Tabstopp-untergeordnete Fenster in der APP zu finden und zu versuchen, den Fokus auf dieses Fenster zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="7b726-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="7b726-124">Wenn kein anderes Fenster zum Verschieben des Fokus vorhanden ist, wird der Fokus innerhalb des Webinhalts der WebView-Webinhalte durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="7b726-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="7b726-125">get_Reason</span><span class="sxs-lookup"><span data-stu-id="7b726-125">get_Reason</span></span> 

<span data-ttu-id="7b726-126">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="7b726-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="7b726-127">Public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="7b726-127">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="7b726-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="7b726-128">put_Handled</span></span> 

<span data-ttu-id="7b726-129">Festlegen der Handled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7b726-129">Set the Handled property.</span></span>

> <span data-ttu-id="7b726-130">Public HRESULT [put_Handled](#put_handled)(bool-Wert)</span><span class="sxs-lookup"><span data-stu-id="7b726-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 643e2e998cc8ca70bfd90fbcb9bbf1f6c690322b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884547"
---
# <span data-ttu-id="d88a1-104">0.9.430-Interface-ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d88a1-104">0.9.430 - interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="d88a1-105">Ereignis-args für das MoveFocusRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d88a1-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="d88a1-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d88a1-106">Summary</span></span>

 <span data-ttu-id="d88a1-107">Member</span><span class="sxs-lookup"><span data-stu-id="d88a1-107">Members</span></span>                        | <span data-ttu-id="d88a1-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d88a1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d88a1-109">get_Reason</span><span class="sxs-lookup"><span data-stu-id="d88a1-109">get_Reason</span></span>](#get_reason) | <span data-ttu-id="d88a1-110">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="d88a1-110">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="d88a1-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="d88a1-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="d88a1-112">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="d88a1-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="d88a1-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="d88a1-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="d88a1-114">Festlegen der Handled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d88a1-114">Set the Handled property.</span></span>

## <span data-ttu-id="d88a1-115">Member</span><span class="sxs-lookup"><span data-stu-id="d88a1-115">Members</span></span>

#### <span data-ttu-id="d88a1-116">get_Reason</span><span class="sxs-lookup"><span data-stu-id="d88a1-116">get_Reason</span></span> 

<span data-ttu-id="d88a1-117">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="d88a1-117">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="d88a1-118">Public HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="d88a1-118">public HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="d88a1-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="d88a1-119">get_Handled</span></span> 

<span data-ttu-id="d88a1-120">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="d88a1-120">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="d88a1-121">Public HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="d88a1-121">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="d88a1-122">Wenn die APP den Fokus an die gewünschte Position verschoben hat, sollte Sie die Handled-Eigenschaft auf true festlegen.</span><span class="sxs-lookup"><span data-stu-id="d88a1-122">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="d88a1-123">Wenn Handled-Eigenschaft auf false festgelegt ist, nachdem der Ereignishandler zurückgegeben wurde, wird Standardaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d88a1-123">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="d88a1-124">Die Standardaktion besteht darin, das nächste Tabstopp-untergeordnete Fenster in der APP zu finden und zu versuchen, den Fokus auf dieses Fenster zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="d88a1-124">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="d88a1-125">Wenn kein anderes Fenster zum Verschieben des Fokus vorhanden ist, wird der Fokus innerhalb des Webinhalts der WebView-Webinhalte durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="d88a1-125">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="d88a1-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="d88a1-126">put_Handled</span></span> 

<span data-ttu-id="d88a1-127">Festlegen der Handled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d88a1-127">Set the Handled property.</span></span>

> <span data-ttu-id="d88a1-128">Public HRESULT [put_Handled](#put_handled)(bool-Wert)</span><span class="sxs-lookup"><span data-stu-id="d88a1-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>


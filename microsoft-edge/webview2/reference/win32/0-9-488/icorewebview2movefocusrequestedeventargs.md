---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 38cd243a5af924da008c3735e43489684deabd0e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883700"
---
# <span data-ttu-id="58c7f-104">0.9.515-Interface-ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="58c7f-104">0.9.515 - interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="58c7f-105">Ereignis-args für das MoveFocusRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="58c7f-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="58c7f-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="58c7f-106">Summary</span></span>

 <span data-ttu-id="58c7f-107">Member</span><span class="sxs-lookup"><span data-stu-id="58c7f-107">Members</span></span>                        | <span data-ttu-id="58c7f-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="58c7f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="58c7f-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="58c7f-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="58c7f-110">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="58c7f-110">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="58c7f-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="58c7f-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="58c7f-112">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="58c7f-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="58c7f-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="58c7f-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="58c7f-114">Festlegen der Handled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="58c7f-114">Set the Handled property.</span></span>

## <span data-ttu-id="58c7f-115">Member</span><span class="sxs-lookup"><span data-stu-id="58c7f-115">Members</span></span>

#### <span data-ttu-id="58c7f-116">get_Handled</span><span class="sxs-lookup"><span data-stu-id="58c7f-116">get_Handled</span></span> 

<span data-ttu-id="58c7f-117">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="58c7f-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="58c7f-118">Public HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="58c7f-118">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="58c7f-119">Wenn die APP den Fokus an die gewünschte Position verschoben hat, sollte Sie die Handled-Eigenschaft auf true festlegen.</span><span class="sxs-lookup"><span data-stu-id="58c7f-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="58c7f-120">Wenn Handled-Eigenschaft auf false festgelegt ist, nachdem der Ereignishandler zurückgegeben wurde, wird Standardaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58c7f-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="58c7f-121">Die Standardaktion besteht darin, das nächste Tabstopp-untergeordnete Fenster in der APP zu finden und zu versuchen, den Fokus auf dieses Fenster zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="58c7f-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="58c7f-122">Wenn kein anderes Fenster zum Verschieben des Fokus vorhanden ist, wird der Fokus innerhalb des Webinhalts der WebView-Webinhalte durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="58c7f-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="58c7f-123">get_Reason</span><span class="sxs-lookup"><span data-stu-id="58c7f-123">get_Reason</span></span> 

<span data-ttu-id="58c7f-124">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="58c7f-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="58c7f-125">Public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="58c7f-125">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="58c7f-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="58c7f-126">put_Handled</span></span> 

<span data-ttu-id="58c7f-127">Festlegen der Handled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="58c7f-127">Set the Handled property.</span></span>

> <span data-ttu-id="58c7f-128">Public HRESULT [put_Handled](#put_handled)(bool-Wert)</span><span class="sxs-lookup"><span data-stu-id="58c7f-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>


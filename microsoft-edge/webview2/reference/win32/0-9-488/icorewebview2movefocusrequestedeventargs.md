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
ms.openlocfilehash: de0319060b6e618c30fc685815bcbcc41e8c3005
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697847"
---
# <span data-ttu-id="4b79e-104">Schnittstellen ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4b79e-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="4b79e-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="4b79e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="4b79e-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="4b79e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="4b79e-107">Ereignis-args für das MoveFocusRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4b79e-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="4b79e-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4b79e-108">Summary</span></span>

 <span data-ttu-id="4b79e-109">Member</span><span class="sxs-lookup"><span data-stu-id="4b79e-109">Members</span></span>                        | <span data-ttu-id="4b79e-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4b79e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4b79e-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="4b79e-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="4b79e-112">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="4b79e-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="4b79e-113">get_Reason</span><span class="sxs-lookup"><span data-stu-id="4b79e-113">get_Reason</span></span>](#get_reason) | <span data-ttu-id="4b79e-114">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="4b79e-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="4b79e-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="4b79e-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="4b79e-116">Festlegen der Handled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4b79e-116">Set the Handled property.</span></span>

## <span data-ttu-id="4b79e-117">Member</span><span class="sxs-lookup"><span data-stu-id="4b79e-117">Members</span></span>

#### <span data-ttu-id="4b79e-118">get_Handled</span><span class="sxs-lookup"><span data-stu-id="4b79e-118">get_Handled</span></span> 

<span data-ttu-id="4b79e-119">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="4b79e-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="4b79e-120">Public HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="4b79e-120">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="4b79e-121">Wenn die APP den Fokus an die gewünschte Position verschoben hat, sollte Sie die Handled-Eigenschaft auf true festlegen.</span><span class="sxs-lookup"><span data-stu-id="4b79e-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="4b79e-122">Wenn Handled-Eigenschaft auf false festgelegt ist, nachdem der Ereignishandler zurückgegeben wurde, wird Standardaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b79e-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="4b79e-123">Die Standardaktion besteht darin, das nächste Tabstopp-untergeordnete Fenster in der APP zu finden und zu versuchen, den Fokus auf dieses Fenster zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="4b79e-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="4b79e-124">Wenn kein anderes Fenster zum Verschieben des Fokus vorhanden ist, wird der Fokus innerhalb des Webinhalts der WebView-Webinhalte durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="4b79e-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="4b79e-125">get_Reason</span><span class="sxs-lookup"><span data-stu-id="4b79e-125">get_Reason</span></span> 

<span data-ttu-id="4b79e-126">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="4b79e-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="4b79e-127">Public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="4b79e-127">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="4b79e-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="4b79e-128">put_Handled</span></span> 

<span data-ttu-id="4b79e-129">Festlegen der Handled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4b79e-129">Set the Handled property.</span></span>

> <span data-ttu-id="4b79e-130">Public HRESULT [put_Handled](#put_handled)(bool-Wert)</span><span class="sxs-lookup"><span data-stu-id="4b79e-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>


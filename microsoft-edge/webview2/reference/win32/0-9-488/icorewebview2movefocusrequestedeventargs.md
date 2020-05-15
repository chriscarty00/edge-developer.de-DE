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
ms.openlocfilehash: 8ca8de3c430eda3bde089ca53501d880f4d8e35e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653935"
---
# <span data-ttu-id="c1675-104">Schnittstellen ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c1675-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="c1675-105">Ereignis-args für das MoveFocusRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c1675-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="c1675-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c1675-106">Summary</span></span>

 <span data-ttu-id="c1675-107">Member</span><span class="sxs-lookup"><span data-stu-id="c1675-107">Members</span></span>                        | <span data-ttu-id="c1675-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c1675-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c1675-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="c1675-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="c1675-110">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="c1675-110">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="c1675-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="c1675-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="c1675-112">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="c1675-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="c1675-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="c1675-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="c1675-114">Festlegen der Handled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c1675-114">Set the Handled property.</span></span>

## <span data-ttu-id="c1675-115">Member</span><span class="sxs-lookup"><span data-stu-id="c1675-115">Members</span></span>

#### <span data-ttu-id="c1675-116">get_Handled</span><span class="sxs-lookup"><span data-stu-id="c1675-116">get_Handled</span></span> 

<span data-ttu-id="c1675-117">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="c1675-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="c1675-118">Public HRESULT [get_Handled](#get_handled)(bool \* value)</span><span class="sxs-lookup"><span data-stu-id="c1675-118">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="c1675-119">Wenn die APP den Fokus an die gewünschte Position verschoben hat, sollte Sie die Handled-Eigenschaft auf true festlegen.</span><span class="sxs-lookup"><span data-stu-id="c1675-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="c1675-120">Wenn Handled-Eigenschaft auf false festgelegt ist, nachdem der Ereignishandler zurückgegeben wurde, wird Standardaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1675-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="c1675-121">Die Standardaktion besteht darin, das nächste Tabstopp-untergeordnete Fenster in der APP zu finden und zu versuchen, den Fokus auf dieses Fenster zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="c1675-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="c1675-122">Wenn kein anderes Fenster zum Verschieben des Fokus vorhanden ist, wird der Fokus innerhalb des Webinhalts der WebView-Webinhalte durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="c1675-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="c1675-123">get_Reason</span><span class="sxs-lookup"><span data-stu-id="c1675-123">get_Reason</span></span> 

<span data-ttu-id="c1675-124">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="c1675-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="c1675-125">Public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="c1675-125">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="c1675-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="c1675-126">put_Handled</span></span> 

<span data-ttu-id="c1675-127">Festlegen der Handled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c1675-127">Set the Handled property.</span></span>

> <span data-ttu-id="c1675-128">Public HRESULT [put_Handled](#put_handled)(bool-Wert)</span><span class="sxs-lookup"><span data-stu-id="c1675-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>


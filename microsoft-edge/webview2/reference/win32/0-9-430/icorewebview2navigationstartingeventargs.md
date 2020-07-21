---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: bd9d10d5f281b2e8f0a5d0687235560c44edc170
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886437"
---
# <span data-ttu-id="10dbc-104">0.9.430-Interface-ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="10dbc-104">0.9.430 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="10dbc-105">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="10dbc-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="10dbc-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="10dbc-106">Summary</span></span>

 <span data-ttu-id="10dbc-107">Member</span><span class="sxs-lookup"><span data-stu-id="10dbc-107">Members</span></span>                        | <span data-ttu-id="10dbc-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="10dbc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10dbc-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="10dbc-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="10dbc-110">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="10dbc-110">The uri of the requested navigation.</span></span>
[<span data-ttu-id="10dbc-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="10dbc-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="10dbc-112">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="10dbc-112">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="10dbc-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="10dbc-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="10dbc-114">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="10dbc-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="10dbc-115">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="10dbc-115">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="10dbc-116">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="10dbc-116">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="10dbc-117">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="10dbc-117">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="10dbc-118">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="10dbc-118">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="10dbc-119">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="10dbc-119">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="10dbc-120">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="10dbc-120">Set the Cancel property.</span></span>
[<span data-ttu-id="10dbc-121">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="10dbc-121">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="10dbc-122">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="10dbc-122">The ID of the navigation.</span></span>

## <span data-ttu-id="10dbc-123">Member</span><span class="sxs-lookup"><span data-stu-id="10dbc-123">Members</span></span>

#### <span data-ttu-id="10dbc-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="10dbc-124">get_Uri</span></span> 

<span data-ttu-id="10dbc-125">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="10dbc-125">The uri of the requested navigation.</span></span>

> <span data-ttu-id="10dbc-126">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="10dbc-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="10dbc-127">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="10dbc-127">get_IsUserInitiated</span></span> 

<span data-ttu-id="10dbc-128">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="10dbc-128">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="10dbc-129">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="10dbc-129">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="10dbc-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="10dbc-130">get_IsRedirected</span></span> 

<span data-ttu-id="10dbc-131">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="10dbc-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="10dbc-132">öffentliche HRESULT- [get_IsRedirected](#get_isredirected)(bool \* isumgeleitet)</span><span class="sxs-lookup"><span data-stu-id="10dbc-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="10dbc-133">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="10dbc-133">get_RequestHeaders</span></span> 

<span data-ttu-id="10dbc-134">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="10dbc-134">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="10dbc-135">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="10dbc-135">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="10dbc-136">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="10dbc-136">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="10dbc-137">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="10dbc-137">get_Cancel</span></span> 

<span data-ttu-id="10dbc-138">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="10dbc-138">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="10dbc-139">öffentliche HRESULT- [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="10dbc-139">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="10dbc-140">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="10dbc-140">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="10dbc-141">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="10dbc-141">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="10dbc-142">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="10dbc-142">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="10dbc-143">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="10dbc-143">put_Cancel</span></span> 

<span data-ttu-id="10dbc-144">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="10dbc-144">Set the Cancel property.</span></span>

> <span data-ttu-id="10dbc-145">öffentliche HRESULT- [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="10dbc-145">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

#### <span data-ttu-id="10dbc-146">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="10dbc-146">get_NavigationId</span></span> 

<span data-ttu-id="10dbc-147">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="10dbc-147">The ID of the navigation.</span></span>

> <span data-ttu-id="10dbc-148">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="10dbc-148">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


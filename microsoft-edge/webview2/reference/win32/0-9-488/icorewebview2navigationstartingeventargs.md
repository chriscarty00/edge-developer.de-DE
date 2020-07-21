---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a9219266412c2872d9236ef93ce0e03e2dd5f7f2
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886397"
---
# <span data-ttu-id="173bc-104">0.9.515-Interface-ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="173bc-104">0.9.515 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="173bc-105">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="173bc-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="173bc-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="173bc-106">Summary</span></span>

 <span data-ttu-id="173bc-107">Member</span><span class="sxs-lookup"><span data-stu-id="173bc-107">Members</span></span>                        | <span data-ttu-id="173bc-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="173bc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="173bc-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="173bc-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="173bc-110">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="173bc-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="173bc-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="173bc-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="173bc-112">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="173bc-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="173bc-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="173bc-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="173bc-114">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="173bc-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="173bc-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="173bc-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="173bc-116">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="173bc-116">The ID of the navigation.</span></span>
[<span data-ttu-id="173bc-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="173bc-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="173bc-118">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="173bc-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="173bc-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="173bc-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="173bc-120">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="173bc-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="173bc-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="173bc-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="173bc-122">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="173bc-122">Set the Cancel property.</span></span>

## <span data-ttu-id="173bc-123">Member</span><span class="sxs-lookup"><span data-stu-id="173bc-123">Members</span></span>

#### <span data-ttu-id="173bc-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="173bc-124">get_Cancel</span></span> 

<span data-ttu-id="173bc-125">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="173bc-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="173bc-126">öffentliche HRESULT- [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="173bc-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="173bc-127">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="173bc-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="173bc-128">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="173bc-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="173bc-129">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="173bc-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="173bc-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="173bc-130">get_IsRedirected</span></span> 

<span data-ttu-id="173bc-131">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="173bc-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="173bc-132">öffentliche HRESULT- [get_IsRedirected](#get_isredirected)(bool \* isumgeleitet)</span><span class="sxs-lookup"><span data-stu-id="173bc-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="173bc-133">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="173bc-133">get_IsUserInitiated</span></span> 

<span data-ttu-id="173bc-134">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="173bc-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="173bc-135">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="173bc-135">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="173bc-136">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="173bc-136">get_NavigationId</span></span> 

<span data-ttu-id="173bc-137">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="173bc-137">The ID of the navigation.</span></span>

> <span data-ttu-id="173bc-138">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="173bc-138">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="173bc-139">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="173bc-139">get_RequestHeaders</span></span> 

<span data-ttu-id="173bc-140">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="173bc-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="173bc-141">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="173bc-141">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="173bc-142">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="173bc-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="173bc-143">get_Uri</span><span class="sxs-lookup"><span data-stu-id="173bc-143">get_Uri</span></span> 

<span data-ttu-id="173bc-144">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="173bc-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="173bc-145">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="173bc-145">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="173bc-146">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="173bc-146">put_Cancel</span></span> 

<span data-ttu-id="173bc-147">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="173bc-147">Set the Cancel property.</span></span>

> <span data-ttu-id="173bc-148">öffentliche HRESULT- [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="173bc-148">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>


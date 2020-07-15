---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 8f4f366d02280163141c9591d04d72c5f5d9d082
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879758"
---
# <span data-ttu-id="39785-104">Schnittstellen ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="39785-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="39785-105">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="39785-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="39785-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="39785-106">Summary</span></span>

 <span data-ttu-id="39785-107">Member</span><span class="sxs-lookup"><span data-stu-id="39785-107">Members</span></span>                        | <span data-ttu-id="39785-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="39785-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="39785-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="39785-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="39785-110">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="39785-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="39785-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="39785-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="39785-112">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="39785-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="39785-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="39785-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="39785-114">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="39785-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="39785-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="39785-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="39785-116">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="39785-116">The ID of the navigation.</span></span>
[<span data-ttu-id="39785-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="39785-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="39785-118">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="39785-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="39785-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="39785-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="39785-120">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="39785-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="39785-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="39785-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="39785-122">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="39785-122">Set the Cancel property.</span></span>

## <span data-ttu-id="39785-123">Member</span><span class="sxs-lookup"><span data-stu-id="39785-123">Members</span></span>

#### <span data-ttu-id="39785-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="39785-124">get_Cancel</span></span> 

<span data-ttu-id="39785-125">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="39785-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="39785-126">öffentliche HRESULT- [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="39785-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="39785-127">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="39785-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="39785-128">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="39785-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="39785-129">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="39785-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="39785-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="39785-130">get_IsRedirected</span></span> 

<span data-ttu-id="39785-131">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="39785-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="39785-132">öffentliche HRESULT- [get_IsRedirected](#get_isredirected)(bool \* isumgeleitet)</span><span class="sxs-lookup"><span data-stu-id="39785-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="39785-133">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="39785-133">get_IsUserInitiated</span></span> 

<span data-ttu-id="39785-134">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="39785-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="39785-135">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="39785-135">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="39785-136">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="39785-136">get_NavigationId</span></span> 

<span data-ttu-id="39785-137">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="39785-137">The ID of the navigation.</span></span>

> <span data-ttu-id="39785-138">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="39785-138">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="39785-139">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="39785-139">get_RequestHeaders</span></span> 

<span data-ttu-id="39785-140">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="39785-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="39785-141">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="39785-141">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="39785-142">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="39785-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="39785-143">get_Uri</span><span class="sxs-lookup"><span data-stu-id="39785-143">get_Uri</span></span> 

<span data-ttu-id="39785-144">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="39785-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="39785-145">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="39785-145">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="39785-146">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="39785-146">put_Cancel</span></span> 

<span data-ttu-id="39785-147">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="39785-147">Set the Cancel property.</span></span>

> <span data-ttu-id="39785-148">öffentliche HRESULT- [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="39785-148">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c2ac2e499e6bbd49f411a001e061af72fda524b5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877882"
---
# <span data-ttu-id="39aca-104">0.9.430-Interface-ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="39aca-104">0.9.430 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="39aca-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="39aca-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="39aca-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="39aca-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="39aca-107">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="39aca-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="39aca-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="39aca-108">Summary</span></span>

 <span data-ttu-id="39aca-109">Member</span><span class="sxs-lookup"><span data-stu-id="39aca-109">Members</span></span>                        | <span data-ttu-id="39aca-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="39aca-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="39aca-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="39aca-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="39aca-112">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="39aca-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="39aca-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="39aca-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="39aca-114">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="39aca-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="39aca-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="39aca-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="39aca-116">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="39aca-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="39aca-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="39aca-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="39aca-118">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="39aca-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="39aca-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="39aca-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="39aca-120">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="39aca-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="39aca-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="39aca-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="39aca-122">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="39aca-122">Set the Cancel property.</span></span>
[<span data-ttu-id="39aca-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="39aca-123">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="39aca-124">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="39aca-124">The ID of the navigation.</span></span>

## <span data-ttu-id="39aca-125">Member</span><span class="sxs-lookup"><span data-stu-id="39aca-125">Members</span></span>

#### <span data-ttu-id="39aca-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="39aca-126">get_Uri</span></span> 

<span data-ttu-id="39aca-127">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="39aca-127">The uri of the requested navigation.</span></span>

> <span data-ttu-id="39aca-128">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="39aca-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="39aca-129">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="39aca-129">get_IsUserInitiated</span></span> 

<span data-ttu-id="39aca-130">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="39aca-130">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="39aca-131">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="39aca-131">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="39aca-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="39aca-132">get_IsRedirected</span></span> 

<span data-ttu-id="39aca-133">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="39aca-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="39aca-134">öffentliche HRESULT- [get_IsRedirected](#get_isredirected)(bool \* isumgeleitet)</span><span class="sxs-lookup"><span data-stu-id="39aca-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="39aca-135">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="39aca-135">get_RequestHeaders</span></span> 

<span data-ttu-id="39aca-136">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="39aca-136">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="39aca-137">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="39aca-137">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="39aca-138">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="39aca-138">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="39aca-139">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="39aca-139">get_Cancel</span></span> 

<span data-ttu-id="39aca-140">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="39aca-140">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="39aca-141">öffentliche HRESULT- [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="39aca-141">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="39aca-142">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="39aca-142">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="39aca-143">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="39aca-143">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="39aca-144">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="39aca-144">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="39aca-145">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="39aca-145">put_Cancel</span></span> 

<span data-ttu-id="39aca-146">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="39aca-146">Set the Cancel property.</span></span>

> <span data-ttu-id="39aca-147">öffentliche HRESULT- [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="39aca-147">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

#### <span data-ttu-id="39aca-148">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="39aca-148">get_NavigationId</span></span> 

<span data-ttu-id="39aca-149">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="39aca-149">The ID of the navigation.</span></span>

> <span data-ttu-id="39aca-150">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="39aca-150">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


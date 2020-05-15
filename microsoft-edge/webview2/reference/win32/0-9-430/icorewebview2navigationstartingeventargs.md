---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b0b868b99d3f77679b3684a20e7744d7a22fd715
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653900"
---
# <span data-ttu-id="be7cf-104">Schnittstellen ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="be7cf-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="be7cf-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="be7cf-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="be7cf-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="be7cf-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="be7cf-107">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="be7cf-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="be7cf-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="be7cf-108">Summary</span></span>

 <span data-ttu-id="be7cf-109">Member</span><span class="sxs-lookup"><span data-stu-id="be7cf-109">Members</span></span>                        | <span data-ttu-id="be7cf-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="be7cf-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="be7cf-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="be7cf-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="be7cf-112">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="be7cf-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="be7cf-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="be7cf-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="be7cf-114">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="be7cf-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="be7cf-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="be7cf-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="be7cf-116">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="be7cf-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="be7cf-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="be7cf-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="be7cf-118">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="be7cf-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="be7cf-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="be7cf-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="be7cf-120">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="be7cf-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="be7cf-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="be7cf-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="be7cf-122">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="be7cf-122">Set the Cancel property.</span></span>
[<span data-ttu-id="be7cf-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="be7cf-123">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="be7cf-124">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="be7cf-124">The ID of the navigation.</span></span>

## <span data-ttu-id="be7cf-125">Member</span><span class="sxs-lookup"><span data-stu-id="be7cf-125">Members</span></span>

#### <span data-ttu-id="be7cf-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="be7cf-126">get_Uri</span></span> 

<span data-ttu-id="be7cf-127">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="be7cf-127">The uri of the requested navigation.</span></span>

> <span data-ttu-id="be7cf-128">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="be7cf-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="be7cf-129">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="be7cf-129">get_IsUserInitiated</span></span> 

<span data-ttu-id="be7cf-130">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="be7cf-130">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="be7cf-131">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="be7cf-131">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="be7cf-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="be7cf-132">get_IsRedirected</span></span> 

<span data-ttu-id="be7cf-133">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="be7cf-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="be7cf-134">öffentliche HRESULT- [get_IsRedirected](#get_isredirected)(bool \* isumgeleitet)</span><span class="sxs-lookup"><span data-stu-id="be7cf-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="be7cf-135">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="be7cf-135">get_RequestHeaders</span></span> 

<span data-ttu-id="be7cf-136">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="be7cf-136">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="be7cf-137">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="be7cf-137">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="be7cf-138">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="be7cf-138">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="be7cf-139">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="be7cf-139">get_Cancel</span></span> 

<span data-ttu-id="be7cf-140">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="be7cf-140">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="be7cf-141">öffentliche HRESULT- [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="be7cf-141">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="be7cf-142">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="be7cf-142">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="be7cf-143">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="be7cf-143">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="be7cf-144">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="be7cf-144">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="be7cf-145">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="be7cf-145">put_Cancel</span></span> 

<span data-ttu-id="be7cf-146">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="be7cf-146">Set the Cancel property.</span></span>

> <span data-ttu-id="be7cf-147">öffentliche HRESULT- [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="be7cf-147">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

#### <span data-ttu-id="be7cf-148">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="be7cf-148">get_NavigationId</span></span> 

<span data-ttu-id="be7cf-149">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="be7cf-149">The ID of the navigation.</span></span>

> <span data-ttu-id="be7cf-150">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="be7cf-150">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


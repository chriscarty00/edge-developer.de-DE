---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: d56f40a9780313c79f421559eaf54750828542a5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697189"
---
# <span data-ttu-id="0b605-104">Schnittstellen ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="0b605-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="0b605-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="0b605-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="0b605-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="0b605-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="0b605-107">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0b605-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="0b605-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0b605-108">Summary</span></span>

 <span data-ttu-id="0b605-109">Member</span><span class="sxs-lookup"><span data-stu-id="0b605-109">Members</span></span>                        | <span data-ttu-id="0b605-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="0b605-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0b605-111">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="0b605-111">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="0b605-112">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="0b605-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="0b605-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="0b605-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="0b605-114">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="0b605-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="0b605-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0b605-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="0b605-116">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0b605-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="0b605-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="0b605-117">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="0b605-118">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="0b605-118">The ID of the navigation.</span></span>
[<span data-ttu-id="0b605-119">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="0b605-119">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="0b605-120">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="0b605-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="0b605-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="0b605-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="0b605-122">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="0b605-122">The uri of the requested navigation.</span></span>
[<span data-ttu-id="0b605-123">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="0b605-123">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="0b605-124">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0b605-124">Set the Cancel property.</span></span>

## <span data-ttu-id="0b605-125">Member</span><span class="sxs-lookup"><span data-stu-id="0b605-125">Members</span></span>

#### <span data-ttu-id="0b605-126">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="0b605-126">get_Cancel</span></span> 

<span data-ttu-id="0b605-127">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="0b605-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="0b605-128">öffentliche HRESULT- [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="0b605-128">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="0b605-129">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="0b605-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="0b605-130">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="0b605-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="0b605-131">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0b605-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="0b605-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="0b605-132">get_IsRedirected</span></span> 

<span data-ttu-id="0b605-133">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="0b605-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="0b605-134">öffentliche HRESULT- [get_IsRedirected](#get_isredirected)(bool \* isumgeleitet)</span><span class="sxs-lookup"><span data-stu-id="0b605-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="0b605-135">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0b605-135">get_IsUserInitiated</span></span> 

<span data-ttu-id="0b605-136">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0b605-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="0b605-137">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="0b605-137">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="0b605-138">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="0b605-138">get_NavigationId</span></span> 

<span data-ttu-id="0b605-139">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="0b605-139">The ID of the navigation.</span></span>

> <span data-ttu-id="0b605-140">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="0b605-140">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="0b605-141">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="0b605-141">get_RequestHeaders</span></span> 

<span data-ttu-id="0b605-142">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="0b605-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="0b605-143">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="0b605-143">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="0b605-144">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0b605-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="0b605-145">get_Uri</span><span class="sxs-lookup"><span data-stu-id="0b605-145">get_Uri</span></span> 

<span data-ttu-id="0b605-146">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="0b605-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="0b605-147">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="0b605-147">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="0b605-148">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="0b605-148">put_Cancel</span></span> 

<span data-ttu-id="0b605-149">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0b605-149">Set the Cancel property.</span></span>

> <span data-ttu-id="0b605-150">öffentliche HRESULT- [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="0b605-150">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>


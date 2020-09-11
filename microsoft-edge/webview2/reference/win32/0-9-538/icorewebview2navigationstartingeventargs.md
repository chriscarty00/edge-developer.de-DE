---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 8bf2cf37ef76256987a52fd5491e5c995244dd65
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011300"
---
# <span data-ttu-id="97232-104">0.9.579-Interface-ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="97232-104">0.9.579 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="97232-105">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="97232-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="97232-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="97232-106">Summary</span></span>

 <span data-ttu-id="97232-107">Member</span><span class="sxs-lookup"><span data-stu-id="97232-107">Members</span></span>                        | <span data-ttu-id="97232-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="97232-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="97232-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="97232-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="97232-110">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="97232-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="97232-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="97232-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="97232-112">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="97232-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="97232-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="97232-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="97232-114">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="97232-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="97232-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="97232-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="97232-116">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="97232-116">The ID of the navigation.</span></span>
[<span data-ttu-id="97232-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="97232-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="97232-118">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="97232-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="97232-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="97232-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="97232-120">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="97232-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="97232-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="97232-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="97232-122">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="97232-122">Set the Cancel property.</span></span>

## <span data-ttu-id="97232-123">Member</span><span class="sxs-lookup"><span data-stu-id="97232-123">Members</span></span>

#### <span data-ttu-id="97232-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="97232-124">get_Cancel</span></span> 

<span data-ttu-id="97232-125">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="97232-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="97232-126">öffentliche HRESULT- [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="97232-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="97232-127">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="97232-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="97232-128">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="97232-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="97232-129">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="97232-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="97232-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="97232-130">get_IsRedirected</span></span> 

<span data-ttu-id="97232-131">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="97232-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="97232-132">öffentliche HRESULT- [get_IsRedirected](#get_isredirected)(bool \* isumgeleitet)</span><span class="sxs-lookup"><span data-stu-id="97232-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="97232-133">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="97232-133">get_IsUserInitiated</span></span> 

<span data-ttu-id="97232-134">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="97232-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="97232-135">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="97232-135">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="97232-136">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="97232-136">get_NavigationId</span></span> 

<span data-ttu-id="97232-137">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="97232-137">The ID of the navigation.</span></span>

> <span data-ttu-id="97232-138">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="97232-138">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="97232-139">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="97232-139">get_RequestHeaders</span></span> 

<span data-ttu-id="97232-140">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="97232-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="97232-141">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="97232-141">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="97232-142">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="97232-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="97232-143">get_Uri</span><span class="sxs-lookup"><span data-stu-id="97232-143">get_Uri</span></span> 

<span data-ttu-id="97232-144">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="97232-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="97232-145">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="97232-145">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="97232-146">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="97232-146">put_Cancel</span></span> 

<span data-ttu-id="97232-147">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="97232-147">Set the Cancel property.</span></span>

> <span data-ttu-id="97232-148">öffentliche HRESULT- [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="97232-148">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>


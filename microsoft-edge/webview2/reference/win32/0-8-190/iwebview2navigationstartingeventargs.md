---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 5996f0eff4db17530750eb39c7693ea0f8496a4d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885898"
---
# <span data-ttu-id="fd6a1-104">0.8.355-Interface-IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="fd6a1-104">0.8.355 - interface IWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="fd6a1-105">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="fd6a1-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fd6a1-106">Summary</span></span>

 <span data-ttu-id="fd6a1-107">Member</span><span class="sxs-lookup"><span data-stu-id="fd6a1-107">Members</span></span>                        | <span data-ttu-id="fd6a1-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="fd6a1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fd6a1-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="fd6a1-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="fd6a1-110">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-110">The uri of the requested navigation.</span></span>
[<span data-ttu-id="fd6a1-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="fd6a1-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="fd6a1-112">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-112">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="fd6a1-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="fd6a1-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="fd6a1-114">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="fd6a1-115">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="fd6a1-115">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="fd6a1-116">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-116">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="fd6a1-117">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="fd6a1-117">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="fd6a1-118">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-118">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="fd6a1-119">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="fd6a1-119">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="fd6a1-120">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fd6a1-120">Set the Cancel property.</span></span>

## <span data-ttu-id="fd6a1-121">Member</span><span class="sxs-lookup"><span data-stu-id="fd6a1-121">Members</span></span>

#### <span data-ttu-id="fd6a1-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="fd6a1-122">get_Uri</span></span> 

<span data-ttu-id="fd6a1-123">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-123">The uri of the requested navigation.</span></span>

> <span data-ttu-id="fd6a1-124">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="fd6a1-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="fd6a1-125">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="fd6a1-125">get_IsUserInitiated</span></span> 

<span data-ttu-id="fd6a1-126">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-126">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="fd6a1-127">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="fd6a1-127">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="fd6a1-128">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="fd6a1-128">get_IsRedirected</span></span> 

<span data-ttu-id="fd6a1-129">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-129">True when the navigation is redirected.</span></span>

> <span data-ttu-id="fd6a1-130">öffentliche HRESULT- [get_IsRedirected](#get_isredirected)(bool \* isumgeleitet)</span><span class="sxs-lookup"><span data-stu-id="fd6a1-130">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="fd6a1-131">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="fd6a1-131">get_RequestHeaders</span></span> 

<span data-ttu-id="fd6a1-132">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-132">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="fd6a1-133">Public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="fd6a1-133">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="fd6a1-134">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-134">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="fd6a1-135">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="fd6a1-135">get_Cancel</span></span> 

<span data-ttu-id="fd6a1-136">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-136">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="fd6a1-137">öffentliche HRESULT- [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="fd6a1-137">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="fd6a1-138">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-138">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="fd6a1-139">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-139">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="fd6a1-140">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="fd6a1-140">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="fd6a1-141">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="fd6a1-141">put_Cancel</span></span> 

<span data-ttu-id="fd6a1-142">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fd6a1-142">Set the Cancel property.</span></span>

> <span data-ttu-id="fd6a1-143">öffentliche HRESULT- [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="fd6a1-143">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 98e242ace5eb0ae5958ddb1eb6cd380d194294be
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697630"
---
# <span data-ttu-id="a2b49-104">Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="a2b49-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="a2b49-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="a2b49-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a2b49-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="a2b49-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="a2b49-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a2b49-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a2b49-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="a2b49-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a2b49-109">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a2b49-109">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="a2b49-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a2b49-110">Summary</span></span>

 <span data-ttu-id="a2b49-111">Member</span><span class="sxs-lookup"><span data-stu-id="a2b49-111">Members</span></span>                        | <span data-ttu-id="a2b49-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a2b49-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a2b49-113">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="a2b49-113">Cancel</span></span>](#cancel) | <span data-ttu-id="a2b49-114">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="a2b49-114">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="a2b49-115">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="a2b49-115">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="a2b49-116">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="a2b49-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="a2b49-117">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a2b49-117">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="a2b49-118">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a2b49-118">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="a2b49-119">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="a2b49-119">NavigationId</span></span>](#navigationid) | <span data-ttu-id="a2b49-120">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="a2b49-120">The ID of the navigation.</span></span>
[<span data-ttu-id="a2b49-121">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="a2b49-121">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="a2b49-122">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="a2b49-122">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="a2b49-123">URI</span><span class="sxs-lookup"><span data-stu-id="a2b49-123">Uri</span></span>](#uri) | <span data-ttu-id="a2b49-124">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="a2b49-124">The uri of the requested navigation.</span></span>

## <span data-ttu-id="a2b49-125">Member</span><span class="sxs-lookup"><span data-stu-id="a2b49-125">Members</span></span>

#### <span data-ttu-id="a2b49-126">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="a2b49-126">Cancel</span></span> 

<span data-ttu-id="a2b49-127">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="a2b49-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="a2b49-128">öffentlicher bool- [Abbruch](#cancel)</span><span class="sxs-lookup"><span data-stu-id="a2b49-128">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="a2b49-129">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="a2b49-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="a2b49-130">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="a2b49-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="a2b49-131">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a2b49-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="a2b49-132">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="a2b49-132">IsRedirected</span></span> 

<span data-ttu-id="a2b49-133">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="a2b49-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="a2b49-134">öffentliche bool- [isumgeleitet](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="a2b49-134">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="a2b49-135">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a2b49-135">IsUserInitiated</span></span> 

<span data-ttu-id="a2b49-136">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a2b49-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="a2b49-137">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="a2b49-137">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="a2b49-138">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="a2b49-138">NavigationId</span></span> 

<span data-ttu-id="a2b49-139">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="a2b49-139">The ID of the navigation.</span></span>

> <span data-ttu-id="a2b49-140">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="a2b49-140">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="a2b49-141">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="a2b49-141">RequestHeaders</span></span> 

<span data-ttu-id="a2b49-142">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="a2b49-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="a2b49-143">öffentliche HttpRequestHeaders- [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="a2b49-143">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="a2b49-144">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="a2b49-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="a2b49-145">URI</span><span class="sxs-lookup"><span data-stu-id="a2b49-145">Uri</span></span> 

<span data-ttu-id="a2b49-146">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="a2b49-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="a2b49-147">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="a2b49-147">public string [Uri](#uri)</span></span>


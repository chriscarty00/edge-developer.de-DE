---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ea3936ac1267fa085f62db843f5cac3fad2635b5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879786"
---
# <span data-ttu-id="ef9d5-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="ef9d5-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="ef9d5-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ef9d5-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ef9d5-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="ef9d5-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ef9d5-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ef9d5-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="ef9d5-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ef9d5-109">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-109">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="ef9d5-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ef9d5-110">Summary</span></span>

 <span data-ttu-id="ef9d5-111">Member</span><span class="sxs-lookup"><span data-stu-id="ef9d5-111">Members</span></span>                        | <span data-ttu-id="ef9d5-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ef9d5-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ef9d5-113">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="ef9d5-113">Cancel</span></span>](#cancel) | <span data-ttu-id="ef9d5-114">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-114">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="ef9d5-115">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="ef9d5-115">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="ef9d5-116">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="ef9d5-117">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ef9d5-117">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="ef9d5-118">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-118">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="ef9d5-119">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="ef9d5-119">NavigationId</span></span>](#navigationid) | <span data-ttu-id="ef9d5-120">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-120">The ID of the navigation.</span></span>
[<span data-ttu-id="ef9d5-121">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="ef9d5-121">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="ef9d5-122">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-122">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="ef9d5-123">URI</span><span class="sxs-lookup"><span data-stu-id="ef9d5-123">Uri</span></span>](#uri) | <span data-ttu-id="ef9d5-124">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-124">The uri of the requested navigation.</span></span>

## <span data-ttu-id="ef9d5-125">Member</span><span class="sxs-lookup"><span data-stu-id="ef9d5-125">Members</span></span>

#### <span data-ttu-id="ef9d5-126">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="ef9d5-126">Cancel</span></span> 

<span data-ttu-id="ef9d5-127">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="ef9d5-128">öffentlicher bool- [Abbruch](#cancel)</span><span class="sxs-lookup"><span data-stu-id="ef9d5-128">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="ef9d5-129">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="ef9d5-130">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="ef9d5-131">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="ef9d5-132">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="ef9d5-132">IsRedirected</span></span> 

<span data-ttu-id="ef9d5-133">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="ef9d5-134">öffentliche bool- [isumgeleitet](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="ef9d5-134">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="ef9d5-135">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ef9d5-135">IsUserInitiated</span></span> 

<span data-ttu-id="ef9d5-136">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="ef9d5-137">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="ef9d5-137">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="ef9d5-138">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="ef9d5-138">NavigationId</span></span> 

<span data-ttu-id="ef9d5-139">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-139">The ID of the navigation.</span></span>

> <span data-ttu-id="ef9d5-140">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="ef9d5-140">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="ef9d5-141">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="ef9d5-141">RequestHeaders</span></span> 

<span data-ttu-id="ef9d5-142">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="ef9d5-143">öffentliche HttpRequestHeaders- [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="ef9d5-143">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="ef9d5-144">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="ef9d5-145">URI</span><span class="sxs-lookup"><span data-stu-id="ef9d5-145">Uri</span></span> 

<span data-ttu-id="ef9d5-146">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="ef9d5-147">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="ef9d5-147">public string [Uri](#uri)</span></span>


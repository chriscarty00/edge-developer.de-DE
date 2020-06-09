---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 58ca180e73c3e4644e466e13c4059f32102f1896
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698778"
---
# <span data-ttu-id="80a0a-104">Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="80a0a-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="80a0a-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="80a0a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="80a0a-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="80a0a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="80a0a-107">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="80a0a-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="80a0a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="80a0a-108">Summary</span></span>

 <span data-ttu-id="80a0a-109">Member</span><span class="sxs-lookup"><span data-stu-id="80a0a-109">Members</span></span>                        | <span data-ttu-id="80a0a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="80a0a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="80a0a-111">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="80a0a-111">Cancel</span></span>](#cancel) | <span data-ttu-id="80a0a-112">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="80a0a-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="80a0a-113">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="80a0a-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="80a0a-114">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="80a0a-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="80a0a-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="80a0a-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="80a0a-116">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="80a0a-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="80a0a-117">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="80a0a-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="80a0a-118">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="80a0a-118">The ID of the navigation.</span></span>
[<span data-ttu-id="80a0a-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="80a0a-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="80a0a-120">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="80a0a-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="80a0a-121">URI</span><span class="sxs-lookup"><span data-stu-id="80a0a-121">Uri</span></span>](#uri) | <span data-ttu-id="80a0a-122">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="80a0a-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="80a0a-123">Member</span><span class="sxs-lookup"><span data-stu-id="80a0a-123">Members</span></span>

#### <span data-ttu-id="80a0a-124">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="80a0a-124">Cancel</span></span> 

<span data-ttu-id="80a0a-125">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="80a0a-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="80a0a-126">öffentlicher bool- [Abbruch](#cancel)</span><span class="sxs-lookup"><span data-stu-id="80a0a-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="80a0a-127">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="80a0a-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="80a0a-128">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="80a0a-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="80a0a-129">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="80a0a-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="80a0a-130">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="80a0a-130">IsRedirected</span></span> 

<span data-ttu-id="80a0a-131">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="80a0a-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="80a0a-132">öffentliche bool- [isumgeleitet](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="80a0a-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="80a0a-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="80a0a-133">IsUserInitiated</span></span> 

<span data-ttu-id="80a0a-134">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="80a0a-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="80a0a-135">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="80a0a-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="80a0a-136">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="80a0a-136">NavigationId</span></span> 

<span data-ttu-id="80a0a-137">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="80a0a-137">The ID of the navigation.</span></span>

> <span data-ttu-id="80a0a-138">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="80a0a-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="80a0a-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="80a0a-139">RequestHeaders</span></span> 

<span data-ttu-id="80a0a-140">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="80a0a-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="80a0a-141">öffentliche HttpRequestHeaders- [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="80a0a-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="80a0a-142">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="80a0a-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="80a0a-143">URI</span><span class="sxs-lookup"><span data-stu-id="80a0a-143">Uri</span></span> 

<span data-ttu-id="80a0a-144">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="80a0a-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="80a0a-145">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="80a0a-145">public string [Uri](#uri)</span></span>


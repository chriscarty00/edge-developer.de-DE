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
ms.openlocfilehash: 8b7ac3ab27cf5a2d9e80a77eabc488599820a02f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654138"
---
# <span data-ttu-id="9468e-104">Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="9468e-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="9468e-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="9468e-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="9468e-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="9468e-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="9468e-107">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9468e-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="9468e-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9468e-108">Summary</span></span>

 <span data-ttu-id="9468e-109">Member</span><span class="sxs-lookup"><span data-stu-id="9468e-109">Members</span></span>                        | <span data-ttu-id="9468e-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9468e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9468e-111">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="9468e-111">Cancel</span></span>](#cancel) | <span data-ttu-id="9468e-112">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="9468e-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="9468e-113">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="9468e-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="9468e-114">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="9468e-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="9468e-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="9468e-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="9468e-116">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9468e-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="9468e-117">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="9468e-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="9468e-118">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="9468e-118">The ID of the navigation.</span></span>
[<span data-ttu-id="9468e-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="9468e-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="9468e-120">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="9468e-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="9468e-121">URI</span><span class="sxs-lookup"><span data-stu-id="9468e-121">Uri</span></span>](#uri) | <span data-ttu-id="9468e-122">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="9468e-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="9468e-123">Member</span><span class="sxs-lookup"><span data-stu-id="9468e-123">Members</span></span>

#### <span data-ttu-id="9468e-124">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="9468e-124">Cancel</span></span> 

<span data-ttu-id="9468e-125">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="9468e-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="9468e-126">öffentlicher bool- [Abbruch](#cancel)</span><span class="sxs-lookup"><span data-stu-id="9468e-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="9468e-127">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="9468e-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="9468e-128">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="9468e-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="9468e-129">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9468e-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="9468e-130">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="9468e-130">IsRedirected</span></span> 

<span data-ttu-id="9468e-131">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="9468e-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="9468e-132">öffentliche bool- [isumgeleitet](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="9468e-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="9468e-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="9468e-133">IsUserInitiated</span></span> 

<span data-ttu-id="9468e-134">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9468e-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="9468e-135">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="9468e-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="9468e-136">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="9468e-136">NavigationId</span></span> 

<span data-ttu-id="9468e-137">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="9468e-137">The ID of the navigation.</span></span>

> <span data-ttu-id="9468e-138">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="9468e-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="9468e-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="9468e-139">RequestHeaders</span></span> 

<span data-ttu-id="9468e-140">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="9468e-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="9468e-141">öffentliche HttpRequestHeaders- [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="9468e-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="9468e-142">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="9468e-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="9468e-143">URI</span><span class="sxs-lookup"><span data-stu-id="9468e-143">Uri</span></span> 

<span data-ttu-id="9468e-144">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="9468e-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="9468e-145">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="9468e-145">public string [Uri](#uri)</span></span>


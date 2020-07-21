---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 2f129f36502ccc404da74904c73c4bdab1d9f472
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886374"
---
# <span data-ttu-id="084ec-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="084ec-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="084ec-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="084ec-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="084ec-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="084ec-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="084ec-107">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="084ec-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="084ec-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="084ec-108">Summary</span></span>

 <span data-ttu-id="084ec-109">Member</span><span class="sxs-lookup"><span data-stu-id="084ec-109">Members</span></span>                        | <span data-ttu-id="084ec-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="084ec-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="084ec-111">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="084ec-111">Cancel</span></span>](#cancel) | <span data-ttu-id="084ec-112">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="084ec-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="084ec-113">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="084ec-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="084ec-114">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="084ec-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="084ec-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="084ec-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="084ec-116">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="084ec-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="084ec-117">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="084ec-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="084ec-118">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="084ec-118">The ID of the navigation.</span></span>
[<span data-ttu-id="084ec-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="084ec-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="084ec-120">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="084ec-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="084ec-121">URI</span><span class="sxs-lookup"><span data-stu-id="084ec-121">Uri</span></span>](#uri) | <span data-ttu-id="084ec-122">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="084ec-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="084ec-123">Member</span><span class="sxs-lookup"><span data-stu-id="084ec-123">Members</span></span>

#### <span data-ttu-id="084ec-124">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="084ec-124">Cancel</span></span> 

<span data-ttu-id="084ec-125">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="084ec-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="084ec-126">öffentlicher bool- [Abbruch](#cancel)</span><span class="sxs-lookup"><span data-stu-id="084ec-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="084ec-127">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="084ec-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="084ec-128">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="084ec-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="084ec-129">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="084ec-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="084ec-130">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="084ec-130">IsRedirected</span></span> 

<span data-ttu-id="084ec-131">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="084ec-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="084ec-132">öffentliche bool- [isumgeleitet](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="084ec-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="084ec-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="084ec-133">IsUserInitiated</span></span> 

<span data-ttu-id="084ec-134">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="084ec-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="084ec-135">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="084ec-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="084ec-136">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="084ec-136">NavigationId</span></span> 

<span data-ttu-id="084ec-137">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="084ec-137">The ID of the navigation.</span></span>

> <span data-ttu-id="084ec-138">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="084ec-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="084ec-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="084ec-139">RequestHeaders</span></span> 

<span data-ttu-id="084ec-140">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="084ec-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="084ec-141">öffentliche HttpRequestHeaders- [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="084ec-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="084ec-142">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="084ec-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="084ec-143">URI</span><span class="sxs-lookup"><span data-stu-id="084ec-143">Uri</span></span> 

<span data-ttu-id="084ec-144">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="084ec-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="084ec-145">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="084ec-145">public string [Uri](#uri)</span></span>


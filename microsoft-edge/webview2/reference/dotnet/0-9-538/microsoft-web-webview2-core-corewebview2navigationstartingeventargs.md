---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: cd692de6aaa3dc694fb2fe149411e5fd64de1ee2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878869"
---
# <span data-ttu-id="7beee-104">Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="7beee-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="7beee-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="7beee-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="7beee-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="7beee-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="7beee-107">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7beee-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="7beee-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7beee-108">Summary</span></span>

 <span data-ttu-id="7beee-109">Member</span><span class="sxs-lookup"><span data-stu-id="7beee-109">Members</span></span>                        | <span data-ttu-id="7beee-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7beee-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7beee-111">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="7beee-111">Cancel</span></span>](#cancel) | <span data-ttu-id="7beee-112">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="7beee-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="7beee-113">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="7beee-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="7beee-114">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7beee-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="7beee-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7beee-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="7beee-116">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7beee-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="7beee-117">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="7beee-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="7beee-118">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="7beee-118">The ID of the navigation.</span></span>
[<span data-ttu-id="7beee-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="7beee-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="7beee-120">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="7beee-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="7beee-121">URI</span><span class="sxs-lookup"><span data-stu-id="7beee-121">Uri</span></span>](#uri) | <span data-ttu-id="7beee-122">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="7beee-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="7beee-123">Member</span><span class="sxs-lookup"><span data-stu-id="7beee-123">Members</span></span>

#### <span data-ttu-id="7beee-124">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="7beee-124">Cancel</span></span> 

<span data-ttu-id="7beee-125">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="7beee-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="7beee-126">öffentlicher bool- [Abbruch](#cancel)</span><span class="sxs-lookup"><span data-stu-id="7beee-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="7beee-127">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="7beee-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="7beee-128">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="7beee-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="7beee-129">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7beee-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="7beee-130">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="7beee-130">IsRedirected</span></span> 

<span data-ttu-id="7beee-131">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7beee-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="7beee-132">öffentliche bool- [isumgeleitet](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="7beee-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="7beee-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7beee-133">IsUserInitiated</span></span> 

<span data-ttu-id="7beee-134">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7beee-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="7beee-135">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="7beee-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="7beee-136">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="7beee-136">NavigationId</span></span> 

<span data-ttu-id="7beee-137">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="7beee-137">The ID of the navigation.</span></span>

> <span data-ttu-id="7beee-138">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="7beee-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="7beee-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="7beee-139">RequestHeaders</span></span> 

<span data-ttu-id="7beee-140">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="7beee-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="7beee-141">öffentliche HttpRequestHeaders- [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="7beee-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="7beee-142">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="7beee-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="7beee-143">URI</span><span class="sxs-lookup"><span data-stu-id="7beee-143">Uri</span></span> 

<span data-ttu-id="7beee-144">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="7beee-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="7beee-145">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="7beee-145">public string [Uri](#uri)</span></span>


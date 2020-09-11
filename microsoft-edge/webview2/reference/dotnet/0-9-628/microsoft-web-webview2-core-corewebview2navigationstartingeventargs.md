---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 1b80b42bc26316d1fcc8ac74656f24cb0db75bae
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012062"
---
# <span data-ttu-id="1fed5-104">Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="1fed5-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="1fed5-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="1fed5-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="1fed5-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="1fed5-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="1fed5-107">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1fed5-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="1fed5-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1fed5-108">Summary</span></span>

 <span data-ttu-id="1fed5-109">Member</span><span class="sxs-lookup"><span data-stu-id="1fed5-109">Members</span></span>                        | <span data-ttu-id="1fed5-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1fed5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1fed5-111">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="1fed5-111">Cancel</span></span>](#cancel) | <span data-ttu-id="1fed5-112">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="1fed5-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="1fed5-113">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="1fed5-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="1fed5-114">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="1fed5-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="1fed5-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="1fed5-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="1fed5-116">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1fed5-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="1fed5-117">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="1fed5-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="1fed5-118">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="1fed5-118">The ID of the navigation.</span></span>
[<span data-ttu-id="1fed5-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="1fed5-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="1fed5-120">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="1fed5-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="1fed5-121">URI</span><span class="sxs-lookup"><span data-stu-id="1fed5-121">Uri</span></span>](#uri) | <span data-ttu-id="1fed5-122">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="1fed5-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="1fed5-123">Member</span><span class="sxs-lookup"><span data-stu-id="1fed5-123">Members</span></span>

#### <span data-ttu-id="1fed5-124">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="1fed5-124">Cancel</span></span> 

<span data-ttu-id="1fed5-125">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="1fed5-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="1fed5-126">öffentlicher bool- [Abbruch](#cancel)</span><span class="sxs-lookup"><span data-stu-id="1fed5-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="1fed5-127">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="1fed5-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="1fed5-128">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="1fed5-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="1fed5-129">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1fed5-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="1fed5-130">Isumgeleitet</span><span class="sxs-lookup"><span data-stu-id="1fed5-130">IsRedirected</span></span> 

<span data-ttu-id="1fed5-131">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="1fed5-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="1fed5-132">öffentliche bool- [isumgeleitet](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="1fed5-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="1fed5-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="1fed5-133">IsUserInitiated</span></span> 

<span data-ttu-id="1fed5-134">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1fed5-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="1fed5-135">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="1fed5-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="1fed5-136">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="1fed5-136">NavigationId</span></span> 

<span data-ttu-id="1fed5-137">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="1fed5-137">The ID of the navigation.</span></span>

> <span data-ttu-id="1fed5-138">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="1fed5-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="1fed5-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="1fed5-139">RequestHeaders</span></span> 

<span data-ttu-id="1fed5-140">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="1fed5-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="1fed5-141">öffentliche CoreWebView2HttpRequestHeaders- [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="1fed5-141">public CoreWebView2HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="1fed5-142">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1fed5-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="1fed5-143">URI</span><span class="sxs-lookup"><span data-stu-id="1fed5-143">Uri</span></span> 

<span data-ttu-id="1fed5-144">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="1fed5-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="1fed5-145">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="1fed5-145">public string [Uri](#uri)</span></span>


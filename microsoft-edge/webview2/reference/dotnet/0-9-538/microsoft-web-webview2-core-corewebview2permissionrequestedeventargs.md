---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: ede6cef20a1a0f5fcd0780376b5ddec07bf05d26
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878799"
---
# <span data-ttu-id="a5b44-104">Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="a5b44-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="a5b44-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a5b44-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a5b44-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="a5b44-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a5b44-107">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a5b44-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="a5b44-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a5b44-108">Summary</span></span>

 <span data-ttu-id="a5b44-109">Member</span><span class="sxs-lookup"><span data-stu-id="a5b44-109">Members</span></span>                        | <span data-ttu-id="a5b44-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a5b44-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a5b44-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a5b44-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="a5b44-112">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a5b44-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="a5b44-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="a5b44-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="a5b44-114">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="a5b44-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="a5b44-115">Status</span><span class="sxs-lookup"><span data-stu-id="a5b44-115">State</span></span>](#state) | <span data-ttu-id="a5b44-116">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="a5b44-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="a5b44-117">URI</span><span class="sxs-lookup"><span data-stu-id="a5b44-117">Uri</span></span>](#uri) | <span data-ttu-id="a5b44-118">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="a5b44-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="a5b44-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a5b44-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="a5b44-120">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a5b44-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="a5b44-121">Member</span><span class="sxs-lookup"><span data-stu-id="a5b44-121">Members</span></span>

#### <span data-ttu-id="a5b44-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a5b44-122">IsUserInitiated</span></span> 

<span data-ttu-id="a5b44-123">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a5b44-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="a5b44-124">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="a5b44-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="a5b44-125">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="a5b44-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="a5b44-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="a5b44-126">PermissionKind</span></span> 

<span data-ttu-id="a5b44-127">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="a5b44-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="a5b44-128">öffentliche CoreWebView2PermissionKind- [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="a5b44-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="a5b44-129">Status</span><span class="sxs-lookup"><span data-stu-id="a5b44-129">State</span></span> 

<span data-ttu-id="a5b44-130">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="a5b44-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="a5b44-131">öffentlicher CoreWebView2PermissionState- [Zustand](#state)</span><span class="sxs-lookup"><span data-stu-id="a5b44-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="a5b44-132">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="a5b44-132">whether the request is granted.</span></span>

<span data-ttu-id="a5b44-133">Der Standardwert ist CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="a5b44-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="a5b44-134">URI</span><span class="sxs-lookup"><span data-stu-id="a5b44-134">Uri</span></span> 

<span data-ttu-id="a5b44-135">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="a5b44-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="a5b44-136">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="a5b44-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="a5b44-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a5b44-137">GetDeferral</span></span> 

<span data-ttu-id="a5b44-138">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a5b44-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="a5b44-139">Public CoreWebView2Deferral [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="a5b44-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="a5b44-140">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="a5b44-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>


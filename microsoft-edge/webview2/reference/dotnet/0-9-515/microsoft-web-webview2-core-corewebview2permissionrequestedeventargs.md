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
ms.openlocfilehash: 5aeeebfc3d8434c096e6946e5161437809f207d3
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653733"
---
# <span data-ttu-id="1f1b5-104">Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="1f1b5-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="1f1b5-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="1f1b5-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="1f1b5-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="1f1b5-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="1f1b5-107">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="1f1b5-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1f1b5-108">Summary</span></span>

 <span data-ttu-id="1f1b5-109">Member</span><span class="sxs-lookup"><span data-stu-id="1f1b5-109">Members</span></span>                        | <span data-ttu-id="1f1b5-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1f1b5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1f1b5-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="1f1b5-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="1f1b5-112">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="1f1b5-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="1f1b5-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="1f1b5-114">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="1f1b5-115">Status</span><span class="sxs-lookup"><span data-stu-id="1f1b5-115">State</span></span>](#state) | <span data-ttu-id="1f1b5-116">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="1f1b5-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="1f1b5-117">URI</span><span class="sxs-lookup"><span data-stu-id="1f1b5-117">Uri</span></span>](#uri) | <span data-ttu-id="1f1b5-118">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="1f1b5-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="1f1b5-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="1f1b5-120">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="1f1b5-121">Member</span><span class="sxs-lookup"><span data-stu-id="1f1b5-121">Members</span></span>

#### <span data-ttu-id="1f1b5-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="1f1b5-122">IsUserInitiated</span></span> 

<span data-ttu-id="1f1b5-123">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="1f1b5-124">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="1f1b5-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="1f1b5-125">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="1f1b5-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="1f1b5-126">PermissionKind</span></span> 

<span data-ttu-id="1f1b5-127">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="1f1b5-128">öffentliche CoreWebView2PermissionKind- [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="1f1b5-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="1f1b5-129">Status</span><span class="sxs-lookup"><span data-stu-id="1f1b5-129">State</span></span> 

<span data-ttu-id="1f1b5-130">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="1f1b5-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="1f1b5-131">öffentlicher CoreWebView2PermissionState- [Zustand](#state)</span><span class="sxs-lookup"><span data-stu-id="1f1b5-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="1f1b5-132">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-132">whether the request is granted.</span></span>

<span data-ttu-id="1f1b5-133">Der Standardwert ist CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="1f1b5-134">URI</span><span class="sxs-lookup"><span data-stu-id="1f1b5-134">Uri</span></span> 

<span data-ttu-id="1f1b5-135">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="1f1b5-136">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="1f1b5-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="1f1b5-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="1f1b5-137">GetDeferral</span></span> 

<span data-ttu-id="1f1b5-138">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="1f1b5-139">Public CoreWebView2Deferral [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="1f1b5-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="1f1b5-140">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="1f1b5-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>


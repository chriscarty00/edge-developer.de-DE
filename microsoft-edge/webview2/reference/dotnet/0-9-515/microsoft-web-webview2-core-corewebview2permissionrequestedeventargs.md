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
ms.openlocfilehash: 743cd0fc6a1a9b21605dfa427273a7a457f806d7
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697609"
---
# <span data-ttu-id="6aea7-104">Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="6aea7-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="6aea7-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="6aea7-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="6aea7-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="6aea7-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="6aea7-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6aea7-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6aea7-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="6aea7-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6aea7-109">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6aea7-109">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="6aea7-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6aea7-110">Summary</span></span>

 <span data-ttu-id="6aea7-111">Member</span><span class="sxs-lookup"><span data-stu-id="6aea7-111">Members</span></span>                        | <span data-ttu-id="6aea7-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6aea7-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6aea7-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6aea7-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="6aea7-114">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6aea7-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="6aea7-115">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="6aea7-115">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="6aea7-116">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="6aea7-116">The type of the permission that is requested.</span></span>
[<span data-ttu-id="6aea7-117">Status</span><span class="sxs-lookup"><span data-stu-id="6aea7-117">State</span></span>](#state) | <span data-ttu-id="6aea7-118">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="6aea7-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="6aea7-119">URI</span><span class="sxs-lookup"><span data-stu-id="6aea7-119">Uri</span></span>](#uri) | <span data-ttu-id="6aea7-120">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="6aea7-120">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="6aea7-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6aea7-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="6aea7-122">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="6aea7-122">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="6aea7-123">Member</span><span class="sxs-lookup"><span data-stu-id="6aea7-123">Members</span></span>

#### <span data-ttu-id="6aea7-124">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6aea7-124">IsUserInitiated</span></span> 

<span data-ttu-id="6aea7-125">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6aea7-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="6aea7-126">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="6aea7-126">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="6aea7-127">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="6aea7-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="6aea7-128">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="6aea7-128">PermissionKind</span></span> 

<span data-ttu-id="6aea7-129">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="6aea7-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="6aea7-130">öffentliche CoreWebView2PermissionKind- [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="6aea7-130">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="6aea7-131">Status</span><span class="sxs-lookup"><span data-stu-id="6aea7-131">State</span></span> 

<span data-ttu-id="6aea7-132">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="6aea7-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="6aea7-133">öffentlicher CoreWebView2PermissionState- [Zustand](#state)</span><span class="sxs-lookup"><span data-stu-id="6aea7-133">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="6aea7-134">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="6aea7-134">whether the request is granted.</span></span>

<span data-ttu-id="6aea7-135">Der Standardwert ist CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="6aea7-135">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="6aea7-136">URI</span><span class="sxs-lookup"><span data-stu-id="6aea7-136">Uri</span></span> 

<span data-ttu-id="6aea7-137">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="6aea7-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="6aea7-138">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="6aea7-138">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="6aea7-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6aea7-139">GetDeferral</span></span> 

<span data-ttu-id="6aea7-140">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="6aea7-140">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="6aea7-141">Public CoreWebView2Deferral [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="6aea7-141">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="6aea7-142">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="6aea7-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>


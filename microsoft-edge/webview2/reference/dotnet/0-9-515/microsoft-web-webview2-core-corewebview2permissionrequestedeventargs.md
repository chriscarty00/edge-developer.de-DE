---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 22fc8ec74c8da0a0ff072cacf91a792b9246900f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879800"
---
# <span data-ttu-id="ca7d4-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="ca7d4-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="ca7d4-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ca7d4-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ca7d4-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="ca7d4-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ca7d4-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ca7d4-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="ca7d4-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ca7d4-109">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-109">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="ca7d4-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ca7d4-110">Summary</span></span>

 <span data-ttu-id="ca7d4-111">Member</span><span class="sxs-lookup"><span data-stu-id="ca7d4-111">Members</span></span>                        | <span data-ttu-id="ca7d4-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ca7d4-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ca7d4-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ca7d4-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="ca7d4-114">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="ca7d4-115">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="ca7d4-115">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="ca7d4-116">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-116">The type of the permission that is requested.</span></span>
[<span data-ttu-id="ca7d4-117">Status</span><span class="sxs-lookup"><span data-stu-id="ca7d4-117">State</span></span>](#state) | <span data-ttu-id="ca7d4-118">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="ca7d4-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="ca7d4-119">URI</span><span class="sxs-lookup"><span data-stu-id="ca7d4-119">Uri</span></span>](#uri) | <span data-ttu-id="ca7d4-120">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-120">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="ca7d4-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ca7d4-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="ca7d4-122">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-122">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="ca7d4-123">Member</span><span class="sxs-lookup"><span data-stu-id="ca7d4-123">Members</span></span>

#### <span data-ttu-id="ca7d4-124">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ca7d4-124">IsUserInitiated</span></span> 

<span data-ttu-id="ca7d4-125">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="ca7d4-126">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="ca7d4-126">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="ca7d4-127">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="ca7d4-128">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="ca7d4-128">PermissionKind</span></span> 

<span data-ttu-id="ca7d4-129">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="ca7d4-130">öffentliche CoreWebView2PermissionKind- [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="ca7d4-130">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="ca7d4-131">Status</span><span class="sxs-lookup"><span data-stu-id="ca7d4-131">State</span></span> 

<span data-ttu-id="ca7d4-132">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="ca7d4-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="ca7d4-133">öffentlicher CoreWebView2PermissionState- [Zustand](#state)</span><span class="sxs-lookup"><span data-stu-id="ca7d4-133">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="ca7d4-134">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-134">whether the request is granted.</span></span>

<span data-ttu-id="ca7d4-135">Der Standardwert ist CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-135">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="ca7d4-136">URI</span><span class="sxs-lookup"><span data-stu-id="ca7d4-136">Uri</span></span> 

<span data-ttu-id="ca7d4-137">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="ca7d4-138">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="ca7d4-138">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="ca7d4-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ca7d4-139">GetDeferral</span></span> 

<span data-ttu-id="ca7d4-140">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-140">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="ca7d4-141">Public CoreWebView2Deferral [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="ca7d4-141">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="ca7d4-142">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="ca7d4-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>


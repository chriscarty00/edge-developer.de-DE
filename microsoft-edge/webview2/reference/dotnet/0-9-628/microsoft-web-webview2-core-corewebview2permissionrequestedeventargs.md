---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 87993559d4d70daef84cbd86a2305f09cc017aa9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012059"
---
# <span data-ttu-id="efa94-104">Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="efa94-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="efa94-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="efa94-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="efa94-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="efa94-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="efa94-107">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="efa94-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="efa94-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="efa94-108">Summary</span></span>

 <span data-ttu-id="efa94-109">Member</span><span class="sxs-lookup"><span data-stu-id="efa94-109">Members</span></span>                        | <span data-ttu-id="efa94-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="efa94-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="efa94-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="efa94-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="efa94-112">"True", wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="efa94-112">True when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="efa94-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="efa94-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="efa94-114">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="efa94-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="efa94-115">Status</span><span class="sxs-lookup"><span data-stu-id="efa94-115">State</span></span>](#state) | <span data-ttu-id="efa94-116">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="efa94-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="efa94-117">URI</span><span class="sxs-lookup"><span data-stu-id="efa94-117">Uri</span></span>](#uri) | <span data-ttu-id="efa94-118">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="efa94-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="efa94-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="efa94-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="efa94-120">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="efa94-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="efa94-121">Member</span><span class="sxs-lookup"><span data-stu-id="efa94-121">Members</span></span>

#### <span data-ttu-id="efa94-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="efa94-122">IsUserInitiated</span></span> 

<span data-ttu-id="efa94-123">"True", wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="efa94-123">True when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="efa94-124">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="efa94-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="efa94-125">Der Edge-Popupblocker ist für WebView deaktiviert, damit die APP dieses Flag verwenden kann, um nicht vom Benutzer initiierte Popups zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="efa94-125">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="efa94-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="efa94-126">PermissionKind</span></span> 

<span data-ttu-id="efa94-127">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="efa94-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="efa94-128">öffentliche CoreWebView2PermissionKind- [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="efa94-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="efa94-129">Status</span><span class="sxs-lookup"><span data-stu-id="efa94-129">State</span></span> 

<span data-ttu-id="efa94-130">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="efa94-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="efa94-131">öffentlicher CoreWebView2PermissionState- [Zustand](#state)</span><span class="sxs-lookup"><span data-stu-id="efa94-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="efa94-132">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="efa94-132">whether the request is granted.</span></span>

<span data-ttu-id="efa94-133">Der Standardwert ist CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="efa94-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="efa94-134">URI</span><span class="sxs-lookup"><span data-stu-id="efa94-134">Uri</span></span> 

<span data-ttu-id="efa94-135">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="efa94-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="efa94-136">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="efa94-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="efa94-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="efa94-137">GetDeferral</span></span> 

<span data-ttu-id="efa94-138">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="efa94-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="efa94-139">Public CoreWebView2Deferral [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="efa94-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="efa94-140">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="efa94-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>


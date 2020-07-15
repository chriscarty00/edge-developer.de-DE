---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: b3178f3c012bc19b9221fbf6961ce0665245d551
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879338"
---
# <span data-ttu-id="c3c45-104">Schnittstellen ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c3c45-104">interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="c3c45-105">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3c45-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="c3c45-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c3c45-106">Summary</span></span>

 <span data-ttu-id="c3c45-107">Member</span><span class="sxs-lookup"><span data-stu-id="c3c45-107">Members</span></span>                        | <span data-ttu-id="c3c45-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c3c45-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c3c45-109">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c3c45-109">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="c3c45-110">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c3c45-110">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="c3c45-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="c3c45-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="c3c45-112">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="c3c45-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="c3c45-113">get_State</span><span class="sxs-lookup"><span data-stu-id="c3c45-113">get_State</span></span>](#get_state) | <span data-ttu-id="c3c45-114">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="c3c45-114">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="c3c45-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="c3c45-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="c3c45-116">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="c3c45-116">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="c3c45-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c3c45-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="c3c45-118">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c3c45-118">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="c3c45-119">put_State</span><span class="sxs-lookup"><span data-stu-id="c3c45-119">put_State</span></span>](#put_state) | <span data-ttu-id="c3c45-120">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="c3c45-120">Set the State property.</span></span>

## <span data-ttu-id="c3c45-121">Member</span><span class="sxs-lookup"><span data-stu-id="c3c45-121">Members</span></span>

#### <span data-ttu-id="c3c45-122">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c3c45-122">get_IsUserInitiated</span></span> 

<span data-ttu-id="c3c45-123">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c3c45-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="c3c45-124">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="c3c45-124">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="c3c45-125">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="c3c45-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="c3c45-126">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="c3c45-126">get_PermissionKind</span></span> 

<span data-ttu-id="c3c45-127">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="c3c45-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="c3c45-128">Public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="c3c45-128">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="c3c45-129">get_State</span><span class="sxs-lookup"><span data-stu-id="c3c45-129">get_State</span></span> 

<span data-ttu-id="c3c45-130">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="c3c45-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="c3c45-131">Public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="c3c45-131">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="c3c45-132">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="c3c45-132">whether the request is granted.</span></span> <span data-ttu-id="c3c45-133">Der Standardwert ist COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="c3c45-133">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="c3c45-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="c3c45-134">get_Uri</span></span> 

<span data-ttu-id="c3c45-135">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="c3c45-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="c3c45-136">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="c3c45-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="c3c45-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c3c45-137">GetDeferral</span></span> 

<span data-ttu-id="c3c45-138">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c3c45-138">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="c3c45-139">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="c3c45-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="c3c45-140">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="c3c45-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="c3c45-141">put_State</span><span class="sxs-lookup"><span data-stu-id="c3c45-141">put_State</span></span> 

<span data-ttu-id="c3c45-142">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="c3c45-142">Set the State property.</span></span>

> <span data-ttu-id="c3c45-143">Public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE Wert)</span><span class="sxs-lookup"><span data-stu-id="c3c45-143">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 88f5008dbc9a4ebfccfe96299899a2474ecc6d95
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880409"
---
# <span data-ttu-id="ac58a-104">0.9.515-Interface-ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ac58a-104">0.9.515 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="ac58a-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ac58a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ac58a-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ac58a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="ac58a-107">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ac58a-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="ac58a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ac58a-108">Summary</span></span>

 <span data-ttu-id="ac58a-109">Member</span><span class="sxs-lookup"><span data-stu-id="ac58a-109">Members</span></span>                        | <span data-ttu-id="ac58a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ac58a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ac58a-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ac58a-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="ac58a-112">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ac58a-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="ac58a-113">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="ac58a-113">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="ac58a-114">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="ac58a-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="ac58a-115">get_State</span><span class="sxs-lookup"><span data-stu-id="ac58a-115">get_State</span></span>](#get_state) | <span data-ttu-id="ac58a-116">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="ac58a-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="ac58a-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ac58a-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="ac58a-118">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="ac58a-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="ac58a-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ac58a-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="ac58a-120">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ac58a-120">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="ac58a-121">put_State</span><span class="sxs-lookup"><span data-stu-id="ac58a-121">put_State</span></span>](#put_state) | <span data-ttu-id="ac58a-122">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="ac58a-122">Set the State property.</span></span>

## <span data-ttu-id="ac58a-123">Member</span><span class="sxs-lookup"><span data-stu-id="ac58a-123">Members</span></span>

#### <span data-ttu-id="ac58a-124">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ac58a-124">get_IsUserInitiated</span></span> 

<span data-ttu-id="ac58a-125">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ac58a-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="ac58a-126">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="ac58a-126">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="ac58a-127">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="ac58a-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="ac58a-128">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="ac58a-128">get_PermissionKind</span></span> 

<span data-ttu-id="ac58a-129">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="ac58a-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="ac58a-130">Public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="ac58a-130">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="ac58a-131">get_State</span><span class="sxs-lookup"><span data-stu-id="ac58a-131">get_State</span></span> 

<span data-ttu-id="ac58a-132">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="ac58a-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="ac58a-133">Public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="ac58a-133">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="ac58a-134">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="ac58a-134">whether the request is granted.</span></span> <span data-ttu-id="ac58a-135">Der Standardwert ist COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="ac58a-135">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="ac58a-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ac58a-136">get_Uri</span></span> 

<span data-ttu-id="ac58a-137">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="ac58a-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="ac58a-138">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="ac58a-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="ac58a-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ac58a-139">GetDeferral</span></span> 

<span data-ttu-id="ac58a-140">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ac58a-140">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="ac58a-141">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="ac58a-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="ac58a-142">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="ac58a-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="ac58a-143">put_State</span><span class="sxs-lookup"><span data-stu-id="ac58a-143">put_State</span></span> 

<span data-ttu-id="ac58a-144">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="ac58a-144">Set the State property.</span></span>

> <span data-ttu-id="ac58a-145">Public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE Wert)</span><span class="sxs-lookup"><span data-stu-id="ac58a-145">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>


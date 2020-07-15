---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 75f88a08f5a94df85a471658704fcd77a5926417
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877791"
---
# <span data-ttu-id="41611-104">0.9.430-Interface-ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="41611-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="41611-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="41611-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="41611-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="41611-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="41611-107">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="41611-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="41611-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="41611-108">Summary</span></span>

 <span data-ttu-id="41611-109">Member</span><span class="sxs-lookup"><span data-stu-id="41611-109">Members</span></span>                        | <span data-ttu-id="41611-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="41611-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="41611-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="41611-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="41611-112">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="41611-112">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="41611-113">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="41611-113">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="41611-114">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="41611-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="41611-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="41611-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="41611-116">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="41611-116">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="41611-117">get_State</span><span class="sxs-lookup"><span data-stu-id="41611-117">get_State</span></span>](#get_state) | <span data-ttu-id="41611-118">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="41611-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="41611-119">put_State</span><span class="sxs-lookup"><span data-stu-id="41611-119">put_State</span></span>](#put_state) | <span data-ttu-id="41611-120">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="41611-120">Set the State property.</span></span>
[<span data-ttu-id="41611-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="41611-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="41611-122">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="41611-122">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="41611-123">Member</span><span class="sxs-lookup"><span data-stu-id="41611-123">Members</span></span>

#### <span data-ttu-id="41611-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="41611-124">get_Uri</span></span> 

<span data-ttu-id="41611-125">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="41611-125">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="41611-126">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="41611-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="41611-127">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="41611-127">get_PermissionKind</span></span> 

<span data-ttu-id="41611-128">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="41611-128">The type of the permission that is requested.</span></span>

> <span data-ttu-id="41611-129">Public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="41611-129">public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="41611-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="41611-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="41611-131">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="41611-131">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="41611-132">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="41611-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="41611-133">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="41611-133">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="41611-134">get_State</span><span class="sxs-lookup"><span data-stu-id="41611-134">get_State</span></span> 

<span data-ttu-id="41611-135">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="41611-135">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="41611-136">Public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="41611-136">public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="41611-137">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="41611-137">whether the request is granted.</span></span> <span data-ttu-id="41611-138">Der Standardwert ist CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="41611-138">Default value is CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="41611-139">put_State</span><span class="sxs-lookup"><span data-stu-id="41611-139">put_State</span></span> 

<span data-ttu-id="41611-140">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="41611-140">Set the State property.</span></span>

> <span data-ttu-id="41611-141">Public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE Wert)</span><span class="sxs-lookup"><span data-stu-id="41611-141">public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="41611-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="41611-142">GetDeferral</span></span> 

<span data-ttu-id="41611-143">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="41611-143">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="41611-144">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="41611-144">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="41611-145">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="41611-145">Developer can use the deferral object to make the permission decision at a later time.</span></span>


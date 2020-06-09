---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: bfc802d160f7516f5f65e5526fecfd9742504045
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698923"
---
# <span data-ttu-id="a4f9a-104">Schnittstellen ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a4f9a-104">interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="a4f9a-105">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="a4f9a-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a4f9a-106">Summary</span></span>

 <span data-ttu-id="a4f9a-107">Member</span><span class="sxs-lookup"><span data-stu-id="a4f9a-107">Members</span></span>                        | <span data-ttu-id="a4f9a-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a4f9a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a4f9a-109">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a4f9a-109">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="a4f9a-110">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-110">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="a4f9a-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="a4f9a-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="a4f9a-112">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="a4f9a-113">get_State</span><span class="sxs-lookup"><span data-stu-id="a4f9a-113">get_State</span></span>](#get_state) | <span data-ttu-id="a4f9a-114">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="a4f9a-114">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="a4f9a-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a4f9a-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="a4f9a-116">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-116">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="a4f9a-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a4f9a-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="a4f9a-118">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-118">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="a4f9a-119">put_State</span><span class="sxs-lookup"><span data-stu-id="a4f9a-119">put_State</span></span>](#put_state) | <span data-ttu-id="a4f9a-120">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-120">Set the State property.</span></span>

## <span data-ttu-id="a4f9a-121">Member</span><span class="sxs-lookup"><span data-stu-id="a4f9a-121">Members</span></span>

#### <span data-ttu-id="a4f9a-122">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a4f9a-122">get_IsUserInitiated</span></span> 

<span data-ttu-id="a4f9a-123">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="a4f9a-124">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="a4f9a-124">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="a4f9a-125">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="a4f9a-126">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="a4f9a-126">get_PermissionKind</span></span> 

<span data-ttu-id="a4f9a-127">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="a4f9a-128">Public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="a4f9a-128">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="a4f9a-129">get_State</span><span class="sxs-lookup"><span data-stu-id="a4f9a-129">get_State</span></span> 

<span data-ttu-id="a4f9a-130">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="a4f9a-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="a4f9a-131">Public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="a4f9a-131">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="a4f9a-132">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-132">whether the request is granted.</span></span> <span data-ttu-id="a4f9a-133">Der Standardwert ist COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-133">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="a4f9a-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a4f9a-134">get_Uri</span></span> 

<span data-ttu-id="a4f9a-135">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="a4f9a-136">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="a4f9a-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="a4f9a-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a4f9a-137">GetDeferral</span></span> 

<span data-ttu-id="a4f9a-138">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-138">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="a4f9a-139">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="a4f9a-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="a4f9a-140">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="a4f9a-141">put_State</span><span class="sxs-lookup"><span data-stu-id="a4f9a-141">put_State</span></span> 

<span data-ttu-id="a4f9a-142">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="a4f9a-142">Set the State property.</span></span>

> <span data-ttu-id="a4f9a-143">Public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE Wert)</span><span class="sxs-lookup"><span data-stu-id="a4f9a-143">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>


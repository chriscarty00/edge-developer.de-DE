---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 85cba958c5c918bb99f14cb7202c7645b0ae6c52
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885205"
---
# <span data-ttu-id="32f21-104">0.9.515-Interface-ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="32f21-104">0.9.515 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="32f21-105">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="32f21-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="32f21-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="32f21-106">Summary</span></span>

 <span data-ttu-id="32f21-107">Member</span><span class="sxs-lookup"><span data-stu-id="32f21-107">Members</span></span>                        | <span data-ttu-id="32f21-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="32f21-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="32f21-109">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="32f21-109">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="32f21-110">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="32f21-110">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="32f21-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="32f21-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="32f21-112">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="32f21-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="32f21-113">get_State</span><span class="sxs-lookup"><span data-stu-id="32f21-113">get_State</span></span>](#get_state) | <span data-ttu-id="32f21-114">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="32f21-114">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="32f21-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="32f21-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="32f21-116">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="32f21-116">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="32f21-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="32f21-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="32f21-118">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="32f21-118">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="32f21-119">put_State</span><span class="sxs-lookup"><span data-stu-id="32f21-119">put_State</span></span>](#put_state) | <span data-ttu-id="32f21-120">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="32f21-120">Set the State property.</span></span>

## <span data-ttu-id="32f21-121">Member</span><span class="sxs-lookup"><span data-stu-id="32f21-121">Members</span></span>

#### <span data-ttu-id="32f21-122">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="32f21-122">get_IsUserInitiated</span></span> 

<span data-ttu-id="32f21-123">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="32f21-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="32f21-124">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="32f21-124">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="32f21-125">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="32f21-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="32f21-126">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="32f21-126">get_PermissionKind</span></span> 

<span data-ttu-id="32f21-127">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="32f21-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="32f21-128">Public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="32f21-128">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="32f21-129">get_State</span><span class="sxs-lookup"><span data-stu-id="32f21-129">get_State</span></span> 

<span data-ttu-id="32f21-130">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="32f21-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="32f21-131">Public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="32f21-131">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="32f21-132">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="32f21-132">whether the request is granted.</span></span> <span data-ttu-id="32f21-133">Der Standardwert ist COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="32f21-133">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="32f21-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="32f21-134">get_Uri</span></span> 

<span data-ttu-id="32f21-135">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="32f21-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="32f21-136">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="32f21-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="32f21-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="32f21-137">GetDeferral</span></span> 

<span data-ttu-id="32f21-138">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="32f21-138">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="32f21-139">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="32f21-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="32f21-140">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="32f21-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="32f21-141">put_State</span><span class="sxs-lookup"><span data-stu-id="32f21-141">put_State</span></span> 

<span data-ttu-id="32f21-142">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="32f21-142">Set the State property.</span></span>

> <span data-ttu-id="32f21-143">Public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE Wert)</span><span class="sxs-lookup"><span data-stu-id="32f21-143">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>


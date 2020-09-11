---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 18048222a9d6bf4d3ad80346a41e4ef5950ca0e6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012168"
---
# <span data-ttu-id="dfadc-104">Schnittstellen ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="dfadc-104">interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="dfadc-105">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="dfadc-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="dfadc-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="dfadc-106">Summary</span></span>

 <span data-ttu-id="dfadc-107">Member</span><span class="sxs-lookup"><span data-stu-id="dfadc-107">Members</span></span>                        | <span data-ttu-id="dfadc-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="dfadc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dfadc-109">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="dfadc-109">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="dfadc-110">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="dfadc-110">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="dfadc-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="dfadc-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="dfadc-112">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="dfadc-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="dfadc-113">get_State</span><span class="sxs-lookup"><span data-stu-id="dfadc-113">get_State</span></span>](#get_state) | <span data-ttu-id="dfadc-114">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="dfadc-114">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="dfadc-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="dfadc-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="dfadc-116">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="dfadc-116">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="dfadc-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="dfadc-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="dfadc-118">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="dfadc-118">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="dfadc-119">put_State</span><span class="sxs-lookup"><span data-stu-id="dfadc-119">put_State</span></span>](#put_state) | <span data-ttu-id="dfadc-120">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="dfadc-120">Set the State property.</span></span>

## <span data-ttu-id="dfadc-121">Member</span><span class="sxs-lookup"><span data-stu-id="dfadc-121">Members</span></span>

#### <span data-ttu-id="dfadc-122">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="dfadc-122">get_IsUserInitiated</span></span> 

<span data-ttu-id="dfadc-123">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="dfadc-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="dfadc-124">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="dfadc-124">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="dfadc-125">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="dfadc-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="dfadc-126">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="dfadc-126">get_PermissionKind</span></span> 

<span data-ttu-id="dfadc-127">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="dfadc-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="dfadc-128">Public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* PermissionKind)</span><span class="sxs-lookup"><span data-stu-id="dfadc-128">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* permissionKind)</span></span>

#### <span data-ttu-id="dfadc-129">get_State</span><span class="sxs-lookup"><span data-stu-id="dfadc-129">get_State</span></span> 

<span data-ttu-id="dfadc-130">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="dfadc-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="dfadc-131">öffentliche HRESULT- [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* Status)</span><span class="sxs-lookup"><span data-stu-id="dfadc-131">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* state)</span></span>

<span data-ttu-id="dfadc-132">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="dfadc-132">whether the request is granted.</span></span> <span data-ttu-id="dfadc-133">Der Standardwert ist COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="dfadc-133">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="dfadc-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="dfadc-134">get_Uri</span></span> 

<span data-ttu-id="dfadc-135">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="dfadc-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="dfadc-136">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="dfadc-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="dfadc-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="dfadc-137">GetDeferral</span></span> 

<span data-ttu-id="dfadc-138">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="dfadc-138">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="dfadc-139">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="dfadc-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="dfadc-140">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="dfadc-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="dfadc-141">put_State</span><span class="sxs-lookup"><span data-stu-id="dfadc-141">put_State</span></span> 

<span data-ttu-id="dfadc-142">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="dfadc-142">Set the State property.</span></span>

> <span data-ttu-id="dfadc-143">Public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE Zustand)</span><span class="sxs-lookup"><span data-stu-id="dfadc-143">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE state)</span></span>


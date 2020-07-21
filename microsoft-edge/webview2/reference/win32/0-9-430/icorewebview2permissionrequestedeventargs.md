---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e29765a4b8a3e620b8c627c7b05b9f0b4ff63f95
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886416"
---
# <span data-ttu-id="b598c-104">0.9.430-Interface-ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b598c-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="b598c-105">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b598c-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="b598c-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b598c-106">Summary</span></span>

 <span data-ttu-id="b598c-107">Member</span><span class="sxs-lookup"><span data-stu-id="b598c-107">Members</span></span>                        | <span data-ttu-id="b598c-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b598c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b598c-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b598c-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="b598c-110">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="b598c-110">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="b598c-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="b598c-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="b598c-112">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="b598c-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="b598c-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="b598c-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="b598c-114">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b598c-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="b598c-115">get_State</span><span class="sxs-lookup"><span data-stu-id="b598c-115">get_State</span></span>](#get_state) | <span data-ttu-id="b598c-116">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="b598c-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="b598c-117">put_State</span><span class="sxs-lookup"><span data-stu-id="b598c-117">put_State</span></span>](#put_state) | <span data-ttu-id="b598c-118">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="b598c-118">Set the State property.</span></span>
[<span data-ttu-id="b598c-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b598c-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="b598c-120">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="b598c-120">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="b598c-121">Member</span><span class="sxs-lookup"><span data-stu-id="b598c-121">Members</span></span>

#### <span data-ttu-id="b598c-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b598c-122">get_Uri</span></span> 

<span data-ttu-id="b598c-123">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="b598c-123">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="b598c-124">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="b598c-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="b598c-125">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="b598c-125">get_PermissionKind</span></span> 

<span data-ttu-id="b598c-126">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="b598c-126">The type of the permission that is requested.</span></span>

> <span data-ttu-id="b598c-127">Public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="b598c-127">public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="b598c-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="b598c-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="b598c-129">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b598c-129">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="b598c-130">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="b598c-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="b598c-131">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="b598c-131">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="b598c-132">get_State</span><span class="sxs-lookup"><span data-stu-id="b598c-132">get_State</span></span> 

<span data-ttu-id="b598c-133">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="b598c-133">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="b598c-134">Public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="b598c-134">public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="b598c-135">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="b598c-135">whether the request is granted.</span></span> <span data-ttu-id="b598c-136">Der Standardwert ist CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="b598c-136">Default value is CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="b598c-137">put_State</span><span class="sxs-lookup"><span data-stu-id="b598c-137">put_State</span></span> 

<span data-ttu-id="b598c-138">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="b598c-138">Set the State property.</span></span>

> <span data-ttu-id="b598c-139">Public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE Wert)</span><span class="sxs-lookup"><span data-stu-id="b598c-139">public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="b598c-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b598c-140">GetDeferral</span></span> 

<span data-ttu-id="b598c-141">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="b598c-141">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="b598c-142">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="b598c-142">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="b598c-143">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="b598c-143">Developer can use the deferral object to make the permission decision at a later time.</span></span>


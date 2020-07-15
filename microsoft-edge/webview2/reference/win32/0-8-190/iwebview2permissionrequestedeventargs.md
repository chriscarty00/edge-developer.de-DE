---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 92c08d199aa607dae9cc575955a1eb0bf016a9c0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878330"
---
# <span data-ttu-id="82943-104">0.8.355-Interface-IWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="82943-104">0.8.355 - interface IWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="82943-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="82943-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="82943-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="82943-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="82943-107">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="82943-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="82943-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="82943-108">Summary</span></span>

 <span data-ttu-id="82943-109">Member</span><span class="sxs-lookup"><span data-stu-id="82943-109">Members</span></span>                        | <span data-ttu-id="82943-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="82943-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="82943-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="82943-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="82943-112">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="82943-112">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="82943-113">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="82943-113">get_PermissionType</span></span>](#get_permissiontype) | <span data-ttu-id="82943-114">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="82943-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="82943-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="82943-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="82943-116">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="82943-116">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="82943-117">get_State</span><span class="sxs-lookup"><span data-stu-id="82943-117">get_State</span></span>](#get_state) | <span data-ttu-id="82943-118">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="82943-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="82943-119">put_State</span><span class="sxs-lookup"><span data-stu-id="82943-119">put_State</span></span>](#put_state) | <span data-ttu-id="82943-120">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="82943-120">Set the State property.</span></span>
[<span data-ttu-id="82943-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="82943-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="82943-122">Getstundung kann aufgerufen werden, um ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="82943-122">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="82943-123">Member</span><span class="sxs-lookup"><span data-stu-id="82943-123">Members</span></span>

#### <span data-ttu-id="82943-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="82943-124">get_Uri</span></span> 

<span data-ttu-id="82943-125">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="82943-125">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="82943-126">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="82943-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="82943-127">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="82943-127">get_PermissionType</span></span> 

<span data-ttu-id="82943-128">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="82943-128">The type of the permission that is requested.</span></span>

> <span data-ttu-id="82943-129">Public HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="82943-129">public HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* value)</span></span>

#### <span data-ttu-id="82943-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="82943-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="82943-131">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="82943-131">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="82943-132">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="82943-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="82943-133">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="82943-133">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="82943-134">get_State</span><span class="sxs-lookup"><span data-stu-id="82943-134">get_State</span></span> 

<span data-ttu-id="82943-135">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="82943-135">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="82943-136">Public HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="82943-136">public HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="82943-137">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="82943-137">whether the request is granted.</span></span> <span data-ttu-id="82943-138">Der Standardwert ist WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="82943-138">Default value is WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="82943-139">put_State</span><span class="sxs-lookup"><span data-stu-id="82943-139">put_State</span></span> 

<span data-ttu-id="82943-140">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="82943-140">Set the State property.</span></span>

> <span data-ttu-id="82943-141">Public HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE Wert)</span><span class="sxs-lookup"><span data-stu-id="82943-141">public HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="82943-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="82943-142">GetDeferral</span></span> 

<span data-ttu-id="82943-143">Getstundung kann aufgerufen werden, um ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="82943-143">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="82943-144">öffentliche HRESULT [getstundung](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="82943-144">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="82943-145">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="82943-145">Developer can use the deferral object to make the permission decision at a later time.</span></span>


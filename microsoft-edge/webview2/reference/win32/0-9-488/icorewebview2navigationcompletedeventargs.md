---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c13d0625669d6303c115c3d415d12278cfbe8320
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880500"
---
# <span data-ttu-id="3163b-104">0.9.515-Interface-ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="3163b-104">0.9.515 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="3163b-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="3163b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="3163b-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="3163b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="3163b-107">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="3163b-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="3163b-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3163b-108">Summary</span></span>

 <span data-ttu-id="3163b-109">Member</span><span class="sxs-lookup"><span data-stu-id="3163b-109">Members</span></span>                        | <span data-ttu-id="3163b-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3163b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3163b-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="3163b-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="3163b-112">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="3163b-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="3163b-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="3163b-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="3163b-114">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="3163b-114">The ID of the navigation.</span></span>
[<span data-ttu-id="3163b-115">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="3163b-115">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="3163b-116">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="3163b-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="3163b-117">Member</span><span class="sxs-lookup"><span data-stu-id="3163b-117">Members</span></span>

#### <span data-ttu-id="3163b-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="3163b-118">get_IsSuccess</span></span> 

<span data-ttu-id="3163b-119">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="3163b-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="3163b-120">öffentliche HRESULT- [get_IsSuccess](#get_issuccess)(bool \* issuccess)</span><span class="sxs-lookup"><span data-stu-id="3163b-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="3163b-121">Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3163b-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="3163b-122">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="3163b-122">get_NavigationId</span></span> 

<span data-ttu-id="3163b-123">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="3163b-123">The ID of the navigation.</span></span>

> <span data-ttu-id="3163b-124">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="3163b-124">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="3163b-125">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="3163b-125">get_WebErrorStatus</span></span> 

<span data-ttu-id="3163b-126">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="3163b-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="3163b-127">öffentliche HRESULT- [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="3163b-127">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>


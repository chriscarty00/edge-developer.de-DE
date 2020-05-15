---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: f9d24d10d9487198988b4c6d3ad4a941a32dc396
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654113"
---
# <span data-ttu-id="0b010-104">Schnittstellen ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="0b010-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="0b010-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="0b010-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="0b010-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="0b010-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="0b010-107">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0b010-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="0b010-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0b010-108">Summary</span></span>

 <span data-ttu-id="0b010-109">Member</span><span class="sxs-lookup"><span data-stu-id="0b010-109">Members</span></span>                        | <span data-ttu-id="0b010-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="0b010-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0b010-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="0b010-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="0b010-112">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="0b010-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="0b010-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="0b010-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="0b010-114">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="0b010-114">The error code if the navigation failed.</span></span>
[<span data-ttu-id="0b010-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="0b010-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="0b010-116">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="0b010-116">The ID of the navigation.</span></span>

## <span data-ttu-id="0b010-117">Member</span><span class="sxs-lookup"><span data-stu-id="0b010-117">Members</span></span>

#### <span data-ttu-id="0b010-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="0b010-118">get_IsSuccess</span></span> 

<span data-ttu-id="0b010-119">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="0b010-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="0b010-120">öffentliche HRESULT- [get_IsSuccess](#get_issuccess)(bool \* issuccess)</span><span class="sxs-lookup"><span data-stu-id="0b010-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="0b010-121">Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0b010-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="0b010-122">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="0b010-122">get_WebErrorStatus</span></span> 

<span data-ttu-id="0b010-123">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="0b010-123">The error code if the navigation failed.</span></span>

> <span data-ttu-id="0b010-124">öffentliche HRESULT- [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="0b010-124">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span></span>

#### <span data-ttu-id="0b010-125">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="0b010-125">get_NavigationId</span></span> 

<span data-ttu-id="0b010-126">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="0b010-126">The ID of the navigation.</span></span>

> <span data-ttu-id="0b010-127">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="0b010-127">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


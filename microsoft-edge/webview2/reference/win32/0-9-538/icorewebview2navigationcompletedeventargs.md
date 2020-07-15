---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: d40ee75eb77e8de6eab1188e6c17edacce00f635
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879807"
---
# <span data-ttu-id="a0595-104">Schnittstellen ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0595-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="a0595-105">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a0595-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="a0595-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a0595-106">Summary</span></span>

 <span data-ttu-id="a0595-107">Member</span><span class="sxs-lookup"><span data-stu-id="a0595-107">Members</span></span>                        | <span data-ttu-id="a0595-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a0595-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a0595-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="a0595-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="a0595-110">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a0595-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="a0595-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a0595-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="a0595-112">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="a0595-112">The ID of the navigation.</span></span>
[<span data-ttu-id="a0595-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="a0595-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="a0595-114">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="a0595-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="a0595-115">Member</span><span class="sxs-lookup"><span data-stu-id="a0595-115">Members</span></span>

#### <span data-ttu-id="a0595-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="a0595-116">get_IsSuccess</span></span> 

<span data-ttu-id="a0595-117">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a0595-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="a0595-118">öffentliche HRESULT- [get_IsSuccess](#get_issuccess)(bool \* issuccess)</span><span class="sxs-lookup"><span data-stu-id="a0595-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="a0595-119">Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a0595-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="a0595-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a0595-120">get_NavigationId</span></span> 

<span data-ttu-id="a0595-121">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="a0595-121">The ID of the navigation.</span></span>

> <span data-ttu-id="a0595-122">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="a0595-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="a0595-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="a0595-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="a0595-124">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="a0595-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="a0595-125">öffentliche HRESULT- [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="a0595-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>


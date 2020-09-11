---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: b45920cfdab8a01d1288fbaf566748545b8a2c98
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012073"
---
# <span data-ttu-id="7c59e-104">Schnittstellen ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7c59e-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="7c59e-105">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7c59e-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="7c59e-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7c59e-106">Summary</span></span>

 <span data-ttu-id="7c59e-107">Member</span><span class="sxs-lookup"><span data-stu-id="7c59e-107">Members</span></span>                        | <span data-ttu-id="7c59e-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7c59e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7c59e-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="7c59e-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="7c59e-110">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="7c59e-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="7c59e-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7c59e-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="7c59e-112">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="7c59e-112">The ID of the navigation.</span></span>
[<span data-ttu-id="7c59e-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="7c59e-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="7c59e-114">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="7c59e-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="7c59e-115">Member</span><span class="sxs-lookup"><span data-stu-id="7c59e-115">Members</span></span>

#### <span data-ttu-id="7c59e-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="7c59e-116">get_IsSuccess</span></span> 

<span data-ttu-id="7c59e-117">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="7c59e-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="7c59e-118">öffentliche HRESULT- [get_IsSuccess](#get_issuccess)(bool \* issuccess)</span><span class="sxs-lookup"><span data-stu-id="7c59e-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="7c59e-119">Dies ist falsch für eine Navigation, die sich auf einer Fehlerseite befand (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), aber auch für zusätzliche Szenarien wie Window. Stop (), die auf navigierten Seite aufgerufen wurden, falsch sein.</span><span class="sxs-lookup"><span data-stu-id="7c59e-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional scenarios such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="7c59e-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7c59e-120">get_NavigationId</span></span> 

<span data-ttu-id="7c59e-121">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="7c59e-121">The ID of the navigation.</span></span>

> <span data-ttu-id="7c59e-122">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \*-Navigations-Nr)</span><span class="sxs-lookup"><span data-stu-id="7c59e-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigationId)</span></span>

#### <span data-ttu-id="7c59e-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="7c59e-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="7c59e-124">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="7c59e-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="7c59e-125">Public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* WebErrorStatus)</span><span class="sxs-lookup"><span data-stu-id="7c59e-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* webErrorStatus)</span></span>


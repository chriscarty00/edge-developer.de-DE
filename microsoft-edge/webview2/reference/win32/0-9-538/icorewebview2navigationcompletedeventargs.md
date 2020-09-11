---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: 482137fd0ffa10c60381d5b0f3dc3d7db6f9fdf7
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011293"
---
# <span data-ttu-id="bd99d-104">0.9.579-Interface-ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="bd99d-104">0.9.579 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="bd99d-105">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="bd99d-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="bd99d-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bd99d-106">Summary</span></span>

 <span data-ttu-id="bd99d-107">Member</span><span class="sxs-lookup"><span data-stu-id="bd99d-107">Members</span></span>                        | <span data-ttu-id="bd99d-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="bd99d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bd99d-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="bd99d-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="bd99d-110">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="bd99d-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="bd99d-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="bd99d-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="bd99d-112">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="bd99d-112">The ID of the navigation.</span></span>
[<span data-ttu-id="bd99d-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="bd99d-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="bd99d-114">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="bd99d-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="bd99d-115">Member</span><span class="sxs-lookup"><span data-stu-id="bd99d-115">Members</span></span>

#### <span data-ttu-id="bd99d-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="bd99d-116">get_IsSuccess</span></span> 

<span data-ttu-id="bd99d-117">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="bd99d-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="bd99d-118">öffentliche HRESULT- [get_IsSuccess](#get_issuccess)(bool \* issuccess)</span><span class="sxs-lookup"><span data-stu-id="bd99d-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="bd99d-119">Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bd99d-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="bd99d-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="bd99d-120">get_NavigationId</span></span> 

<span data-ttu-id="bd99d-121">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="bd99d-121">The ID of the navigation.</span></span>

> <span data-ttu-id="bd99d-122">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="bd99d-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="bd99d-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="bd99d-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="bd99d-124">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="bd99d-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="bd99d-125">öffentliche HRESULT- [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="bd99d-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>


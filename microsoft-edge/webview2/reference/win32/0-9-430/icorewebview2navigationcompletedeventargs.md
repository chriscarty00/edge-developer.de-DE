---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 099a022fef47beca0e0163e6e0e070aa37520a06
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883728"
---
# <span data-ttu-id="be5b3-104">0.9.430-Interface-ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="be5b3-104">0.9.430 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="be5b3-105">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="be5b3-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="be5b3-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="be5b3-106">Summary</span></span>

 <span data-ttu-id="be5b3-107">Member</span><span class="sxs-lookup"><span data-stu-id="be5b3-107">Members</span></span>                        | <span data-ttu-id="be5b3-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="be5b3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="be5b3-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="be5b3-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="be5b3-110">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="be5b3-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="be5b3-111">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="be5b3-111">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="be5b3-112">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="be5b3-112">The error code if the navigation failed.</span></span>
[<span data-ttu-id="be5b3-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="be5b3-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="be5b3-114">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="be5b3-114">The ID of the navigation.</span></span>

## <span data-ttu-id="be5b3-115">Member</span><span class="sxs-lookup"><span data-stu-id="be5b3-115">Members</span></span>

#### <span data-ttu-id="be5b3-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="be5b3-116">get_IsSuccess</span></span> 

<span data-ttu-id="be5b3-117">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="be5b3-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="be5b3-118">öffentliche HRESULT- [get_IsSuccess](#get_issuccess)(bool \* issuccess)</span><span class="sxs-lookup"><span data-stu-id="be5b3-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="be5b3-119">Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="be5b3-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="be5b3-120">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="be5b3-120">get_WebErrorStatus</span></span> 

<span data-ttu-id="be5b3-121">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="be5b3-121">The error code if the navigation failed.</span></span>

> <span data-ttu-id="be5b3-122">öffentliche HRESULT- [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="be5b3-122">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span></span>

#### <span data-ttu-id="be5b3-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="be5b3-123">get_NavigationId</span></span> 

<span data-ttu-id="be5b3-124">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="be5b3-124">The ID of the navigation.</span></span>

> <span data-ttu-id="be5b3-125">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="be5b3-125">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


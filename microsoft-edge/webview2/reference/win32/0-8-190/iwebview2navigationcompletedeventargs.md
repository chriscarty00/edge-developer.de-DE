---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: fa1debd3b212492eea03e4ecf6e5daff5751f89b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653916"
---
# <span data-ttu-id="438ff-104">Schnittstellen IWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="438ff-104">interface IWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="438ff-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="438ff-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="438ff-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="438ff-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="438ff-107">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="438ff-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="438ff-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="438ff-108">Summary</span></span>

 <span data-ttu-id="438ff-109">Member</span><span class="sxs-lookup"><span data-stu-id="438ff-109">Members</span></span>                        | <span data-ttu-id="438ff-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="438ff-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="438ff-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="438ff-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="438ff-112">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="438ff-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="438ff-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="438ff-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="438ff-114">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="438ff-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="438ff-115">Member</span><span class="sxs-lookup"><span data-stu-id="438ff-115">Members</span></span>

#### <span data-ttu-id="438ff-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="438ff-116">get_IsSuccess</span></span> 

<span data-ttu-id="438ff-117">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="438ff-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="438ff-118">öffentliche HRESULT- [get_IsSuccess](#get_issuccess)(bool \* issuccess)</span><span class="sxs-lookup"><span data-stu-id="438ff-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="438ff-119">Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="438ff-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="438ff-120">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="438ff-120">get_WebErrorStatus</span></span> 

<span data-ttu-id="438ff-121">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="438ff-121">The error code if the navigation failed.</span></span>

> <span data-ttu-id="438ff-122">öffentliche HRESULT- [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="438ff-122">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span></span>


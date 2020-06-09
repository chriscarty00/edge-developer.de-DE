---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: d3b3f4e78ef37ad2101a3a8f817279e999cea3e3
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697616"
---
# <span data-ttu-id="cf7d2-104">Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="cf7d2-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="cf7d2-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="cf7d2-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="cf7d2-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="cf7d2-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="cf7d2-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="cf7d2-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="cf7d2-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="cf7d2-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="cf7d2-109">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="cf7d2-109">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="cf7d2-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="cf7d2-110">Summary</span></span>

 <span data-ttu-id="cf7d2-111">Member</span><span class="sxs-lookup"><span data-stu-id="cf7d2-111">Members</span></span>                        | <span data-ttu-id="cf7d2-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="cf7d2-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cf7d2-113">Issuccess</span><span class="sxs-lookup"><span data-stu-id="cf7d2-113">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="cf7d2-114">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cf7d2-114">True when the navigation is successful.</span></span>
[<span data-ttu-id="cf7d2-115">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="cf7d2-115">NavigationId</span></span>](#navigationid) | <span data-ttu-id="cf7d2-116">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="cf7d2-116">The ID of the navigation.</span></span>
[<span data-ttu-id="cf7d2-117">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="cf7d2-117">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="cf7d2-118">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="cf7d2-118">The error code if the navigation failed.</span></span>

## <span data-ttu-id="cf7d2-119">Member</span><span class="sxs-lookup"><span data-stu-id="cf7d2-119">Members</span></span>

#### <span data-ttu-id="cf7d2-120">Issuccess</span><span class="sxs-lookup"><span data-stu-id="cf7d2-120">IsSuccess</span></span> 

<span data-ttu-id="cf7d2-121">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cf7d2-121">True when the navigation is successful.</span></span>

> <span data-ttu-id="cf7d2-122">public bool [issuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="cf7d2-122">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="cf7d2-123">Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cf7d2-123">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="cf7d2-124">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="cf7d2-124">NavigationId</span></span> 

<span data-ttu-id="cf7d2-125">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="cf7d2-125">The ID of the navigation.</span></span>

> <span data-ttu-id="cf7d2-126">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="cf7d2-126">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="cf7d2-127">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="cf7d2-127">WebErrorStatus</span></span> 

<span data-ttu-id="cf7d2-128">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="cf7d2-128">The error code if the navigation failed.</span></span>

> <span data-ttu-id="cf7d2-129">öffentliche CoreWebView2WebErrorStatus- [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="cf7d2-129">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>


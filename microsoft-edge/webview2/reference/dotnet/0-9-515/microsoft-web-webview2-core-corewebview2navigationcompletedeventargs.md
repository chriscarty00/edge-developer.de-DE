---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e2e973e2ee1817decd24bbc1d0dc3daa9709795c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885079"
---
# <span data-ttu-id="fb5f2-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="fb5f2-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="fb5f2-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="fb5f2-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="fb5f2-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="fb5f2-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="fb5f2-107">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fb5f2-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="fb5f2-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fb5f2-108">Summary</span></span>

 <span data-ttu-id="fb5f2-109">Member</span><span class="sxs-lookup"><span data-stu-id="fb5f2-109">Members</span></span>                        | <span data-ttu-id="fb5f2-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="fb5f2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fb5f2-111">Issuccess</span><span class="sxs-lookup"><span data-stu-id="fb5f2-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="fb5f2-112">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="fb5f2-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="fb5f2-113">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="fb5f2-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="fb5f2-114">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="fb5f2-114">The ID of the navigation.</span></span>
[<span data-ttu-id="fb5f2-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="fb5f2-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="fb5f2-116">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="fb5f2-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="fb5f2-117">Member</span><span class="sxs-lookup"><span data-stu-id="fb5f2-117">Members</span></span>

#### <span data-ttu-id="fb5f2-118">Issuccess</span><span class="sxs-lookup"><span data-stu-id="fb5f2-118">IsSuccess</span></span> 

<span data-ttu-id="fb5f2-119">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="fb5f2-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="fb5f2-120">public bool [issuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="fb5f2-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="fb5f2-121">Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fb5f2-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="fb5f2-122">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="fb5f2-122">NavigationId</span></span> 

<span data-ttu-id="fb5f2-123">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="fb5f2-123">The ID of the navigation.</span></span>

> <span data-ttu-id="fb5f2-124">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="fb5f2-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="fb5f2-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="fb5f2-125">WebErrorStatus</span></span> 

<span data-ttu-id="fb5f2-126">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="fb5f2-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="fb5f2-127">öffentliche CoreWebView2WebErrorStatus- [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="fb5f2-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c82c37d7127d69700f35fbf9e2a69f85159a7109
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698800"
---
# <span data-ttu-id="cd3c2-104">Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="cd3c2-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

<span data-ttu-id="cd3c2-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="cd3c2-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="cd3c2-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="cd3c2-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="cd3c2-107">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="cd3c2-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="cd3c2-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="cd3c2-108">Summary</span></span>

 <span data-ttu-id="cd3c2-109">Member</span><span class="sxs-lookup"><span data-stu-id="cd3c2-109">Members</span></span>                        | <span data-ttu-id="cd3c2-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="cd3c2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cd3c2-111">Issuccess</span><span class="sxs-lookup"><span data-stu-id="cd3c2-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="cd3c2-112">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cd3c2-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="cd3c2-113">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="cd3c2-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="cd3c2-114">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="cd3c2-114">The ID of the navigation.</span></span>
[<span data-ttu-id="cd3c2-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="cd3c2-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="cd3c2-116">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="cd3c2-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="cd3c2-117">Member</span><span class="sxs-lookup"><span data-stu-id="cd3c2-117">Members</span></span>

#### <span data-ttu-id="cd3c2-118">Issuccess</span><span class="sxs-lookup"><span data-stu-id="cd3c2-118">IsSuccess</span></span> 

<span data-ttu-id="cd3c2-119">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cd3c2-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="cd3c2-120">public bool [issuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="cd3c2-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="cd3c2-121">Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cd3c2-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="cd3c2-122">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="cd3c2-122">NavigationId</span></span> 

<span data-ttu-id="cd3c2-123">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="cd3c2-123">The ID of the navigation.</span></span>

> <span data-ttu-id="cd3c2-124">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="cd3c2-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="cd3c2-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="cd3c2-125">WebErrorStatus</span></span> 

<span data-ttu-id="cd3c2-126">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="cd3c2-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="cd3c2-127">öffentliche CoreWebView2WebErrorStatus- [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="cd3c2-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>


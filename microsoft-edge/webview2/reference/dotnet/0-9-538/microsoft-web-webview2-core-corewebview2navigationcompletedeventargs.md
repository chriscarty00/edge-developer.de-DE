---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: aaaad1f622887ed1c941a9cf12ee4c753b352286
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878883"
---
# <span data-ttu-id="a747f-104">Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="a747f-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

<span data-ttu-id="a747f-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a747f-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a747f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="a747f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a747f-107">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a747f-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="a747f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a747f-108">Summary</span></span>

 <span data-ttu-id="a747f-109">Member</span><span class="sxs-lookup"><span data-stu-id="a747f-109">Members</span></span>                        | <span data-ttu-id="a747f-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a747f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a747f-111">Issuccess</span><span class="sxs-lookup"><span data-stu-id="a747f-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="a747f-112">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a747f-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="a747f-113">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="a747f-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="a747f-114">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="a747f-114">The ID of the navigation.</span></span>
[<span data-ttu-id="a747f-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="a747f-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="a747f-116">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="a747f-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="a747f-117">Member</span><span class="sxs-lookup"><span data-stu-id="a747f-117">Members</span></span>

#### <span data-ttu-id="a747f-118">Issuccess</span><span class="sxs-lookup"><span data-stu-id="a747f-118">IsSuccess</span></span> 

<span data-ttu-id="a747f-119">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a747f-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="a747f-120">public bool [issuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="a747f-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="a747f-121">Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a747f-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="a747f-122">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="a747f-122">NavigationId</span></span> 

<span data-ttu-id="a747f-123">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="a747f-123">The ID of the navigation.</span></span>

> <span data-ttu-id="a747f-124">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="a747f-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="a747f-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="a747f-125">WebErrorStatus</span></span> 

<span data-ttu-id="a747f-126">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="a747f-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="a747f-127">öffentliche CoreWebView2WebErrorStatus- [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="a747f-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>


---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: dfa6aedb10e60a2af15c7b098c479f8537d6c747
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012018"
---
# <span data-ttu-id="85fb9-104">Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="85fb9-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

<span data-ttu-id="85fb9-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="85fb9-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="85fb9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="85fb9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="85fb9-107">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="85fb9-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="85fb9-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="85fb9-108">Summary</span></span>

 <span data-ttu-id="85fb9-109">Member</span><span class="sxs-lookup"><span data-stu-id="85fb9-109">Members</span></span>                        | <span data-ttu-id="85fb9-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="85fb9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="85fb9-111">Issuccess</span><span class="sxs-lookup"><span data-stu-id="85fb9-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="85fb9-112">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="85fb9-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="85fb9-113">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="85fb9-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="85fb9-114">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="85fb9-114">The ID of the navigation.</span></span>
[<span data-ttu-id="85fb9-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="85fb9-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="85fb9-116">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="85fb9-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="85fb9-117">Member</span><span class="sxs-lookup"><span data-stu-id="85fb9-117">Members</span></span>

#### <span data-ttu-id="85fb9-118">Issuccess</span><span class="sxs-lookup"><span data-stu-id="85fb9-118">IsSuccess</span></span> 

<span data-ttu-id="85fb9-119">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="85fb9-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="85fb9-120">public bool [issuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="85fb9-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="85fb9-121">Dies ist falsch für eine Navigation, die sich auf einer Fehlerseite befand (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), aber auch für zusätzliche Szenarien wie Window. Stop (), die auf navigierten Seite aufgerufen wurden, falsch sein.</span><span class="sxs-lookup"><span data-stu-id="85fb9-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional scenarios such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="85fb9-122">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="85fb9-122">NavigationId</span></span> 

<span data-ttu-id="85fb9-123">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="85fb9-123">The ID of the navigation.</span></span>

> <span data-ttu-id="85fb9-124">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="85fb9-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="85fb9-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="85fb9-125">WebErrorStatus</span></span> 

<span data-ttu-id="85fb9-126">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="85fb9-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="85fb9-127">öffentliche CoreWebView2WebErrorStatus- [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="85fb9-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>


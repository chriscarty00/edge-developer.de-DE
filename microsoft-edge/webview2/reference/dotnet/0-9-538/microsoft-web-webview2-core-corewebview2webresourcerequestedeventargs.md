---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 53cc31bc714417ab902fa8fdef9fd83f80871f10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879667"
---
# <span data-ttu-id="b9a39-104">Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="b9a39-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="b9a39-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b9a39-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b9a39-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b9a39-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b9a39-107">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b9a39-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="b9a39-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b9a39-108">Summary</span></span>

 <span data-ttu-id="b9a39-109">Member</span><span class="sxs-lookup"><span data-stu-id="b9a39-109">Members</span></span>                        | <span data-ttu-id="b9a39-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b9a39-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b9a39-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9a39-111">Request</span></span>](#request) | <span data-ttu-id="b9a39-112">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b9a39-112">The HTTP request.</span></span>
[<span data-ttu-id="b9a39-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="b9a39-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="b9a39-114">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="b9a39-114">The web resource request contexts.</span></span>
[<span data-ttu-id="b9a39-115">Antwort</span><span class="sxs-lookup"><span data-stu-id="b9a39-115">Response</span></span>](#response) | <span data-ttu-id="b9a39-116">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="b9a39-116">The HTTP response.</span></span>
[<span data-ttu-id="b9a39-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b9a39-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="b9a39-118">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="b9a39-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="b9a39-119">Member</span><span class="sxs-lookup"><span data-stu-id="b9a39-119">Members</span></span>

#### <span data-ttu-id="b9a39-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9a39-120">Request</span></span> 

<span data-ttu-id="b9a39-121">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b9a39-121">The HTTP request.</span></span>

> <span data-ttu-id="b9a39-122">öffentliche HttpRequestMessage- [Anforderung](#request)</span><span class="sxs-lookup"><span data-stu-id="b9a39-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="b9a39-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="b9a39-123">ResourceContext</span></span> 

<span data-ttu-id="b9a39-124">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="b9a39-124">The web resource request contexts.</span></span>

> <span data-ttu-id="b9a39-125">Public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) - [resourcecontext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="b9a39-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="b9a39-126">Antwort</span><span class="sxs-lookup"><span data-stu-id="b9a39-126">Response</span></span> 

<span data-ttu-id="b9a39-127">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="b9a39-127">The HTTP response.</span></span>

> <span data-ttu-id="b9a39-128">öffentliche HttpResponseMessage- [Antwort](#response)</span><span class="sxs-lookup"><span data-stu-id="b9a39-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="b9a39-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b9a39-129">GetDeferral</span></span> 

<span data-ttu-id="b9a39-130">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="b9a39-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="b9a39-131">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="b9a39-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="b9a39-132">Sie können das CoreWebView2Deferral-Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b9a39-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>


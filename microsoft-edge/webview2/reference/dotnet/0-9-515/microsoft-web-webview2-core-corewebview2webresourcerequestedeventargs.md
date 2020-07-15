---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 2f9fb899746922206ff3f6cbfd129d69389fd60e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879310"
---
# <span data-ttu-id="270b8-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="270b8-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="270b8-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="270b8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="270b8-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="270b8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="270b8-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="270b8-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="270b8-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="270b8-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="270b8-109">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="270b8-109">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="270b8-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="270b8-110">Summary</span></span>

 <span data-ttu-id="270b8-111">Member</span><span class="sxs-lookup"><span data-stu-id="270b8-111">Members</span></span>                        | <span data-ttu-id="270b8-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="270b8-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="270b8-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="270b8-113">Request</span></span>](#request) | <span data-ttu-id="270b8-114">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="270b8-114">The HTTP request.</span></span>
[<span data-ttu-id="270b8-115">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="270b8-115">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="270b8-116">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="270b8-116">The web resource request contexts.</span></span>
[<span data-ttu-id="270b8-117">Antwort</span><span class="sxs-lookup"><span data-stu-id="270b8-117">Response</span></span>](#response) | <span data-ttu-id="270b8-118">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="270b8-118">The HTTP response.</span></span>
[<span data-ttu-id="270b8-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="270b8-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="270b8-120">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="270b8-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="270b8-121">Member</span><span class="sxs-lookup"><span data-stu-id="270b8-121">Members</span></span>

#### <span data-ttu-id="270b8-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="270b8-122">Request</span></span> 

<span data-ttu-id="270b8-123">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="270b8-123">The HTTP request.</span></span>

> <span data-ttu-id="270b8-124">öffentliche HttpRequestMessage- [Anforderung](#request)</span><span class="sxs-lookup"><span data-stu-id="270b8-124">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="270b8-125">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="270b8-125">ResourceContext</span></span> 

<span data-ttu-id="270b8-126">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="270b8-126">The web resource request contexts.</span></span>

> <span data-ttu-id="270b8-127">Public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) - [resourcecontext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="270b8-127">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="270b8-128">Antwort</span><span class="sxs-lookup"><span data-stu-id="270b8-128">Response</span></span> 

<span data-ttu-id="270b8-129">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="270b8-129">The HTTP response.</span></span>

> <span data-ttu-id="270b8-130">öffentliche HttpResponseMessage- [Antwort](#response)</span><span class="sxs-lookup"><span data-stu-id="270b8-130">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="270b8-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="270b8-131">GetDeferral</span></span> 

<span data-ttu-id="270b8-132">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="270b8-132">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="270b8-133">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="270b8-133">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="270b8-134">Sie können das CoreWebView2Deferral-Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="270b8-134">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>


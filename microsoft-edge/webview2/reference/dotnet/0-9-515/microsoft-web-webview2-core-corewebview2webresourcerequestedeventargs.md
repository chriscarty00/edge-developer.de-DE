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
ms.openlocfilehash: 072ce10e7ac1f34238278366c3e8799a3268cb0b
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697532"
---
# <span data-ttu-id="4cc9a-104">Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="4cc9a-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="4cc9a-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="4cc9a-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="4cc9a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="4cc9a-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4cc9a-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4cc9a-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="4cc9a-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4cc9a-109">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-109">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="4cc9a-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4cc9a-110">Summary</span></span>

 <span data-ttu-id="4cc9a-111">Member</span><span class="sxs-lookup"><span data-stu-id="4cc9a-111">Members</span></span>                        | <span data-ttu-id="4cc9a-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4cc9a-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4cc9a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cc9a-113">Request</span></span>](#request) | <span data-ttu-id="4cc9a-114">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-114">The HTTP request.</span></span>
[<span data-ttu-id="4cc9a-115">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="4cc9a-115">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="4cc9a-116">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-116">The web resource request contexts.</span></span>
[<span data-ttu-id="4cc9a-117">Antwort</span><span class="sxs-lookup"><span data-stu-id="4cc9a-117">Response</span></span>](#response) | <span data-ttu-id="4cc9a-118">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-118">The HTTP response.</span></span>
[<span data-ttu-id="4cc9a-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4cc9a-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="4cc9a-120">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="4cc9a-121">Member</span><span class="sxs-lookup"><span data-stu-id="4cc9a-121">Members</span></span>

#### <span data-ttu-id="4cc9a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cc9a-122">Request</span></span> 

<span data-ttu-id="4cc9a-123">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-123">The HTTP request.</span></span>

> <span data-ttu-id="4cc9a-124">öffentliche HttpRequestMessage- [Anforderung](#request)</span><span class="sxs-lookup"><span data-stu-id="4cc9a-124">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="4cc9a-125">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="4cc9a-125">ResourceContext</span></span> 

<span data-ttu-id="4cc9a-126">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-126">The web resource request contexts.</span></span>

> <span data-ttu-id="4cc9a-127">Public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) - [resourcecontext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="4cc9a-127">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="4cc9a-128">Antwort</span><span class="sxs-lookup"><span data-stu-id="4cc9a-128">Response</span></span> 

<span data-ttu-id="4cc9a-129">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-129">The HTTP response.</span></span>

> <span data-ttu-id="4cc9a-130">öffentliche HttpResponseMessage- [Antwort](#response)</span><span class="sxs-lookup"><span data-stu-id="4cc9a-130">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="4cc9a-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4cc9a-131">GetDeferral</span></span> 

<span data-ttu-id="4cc9a-132">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-132">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="4cc9a-133">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="4cc9a-133">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="4cc9a-134">Sie können das CoreWebView2Deferral-Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4cc9a-134">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>


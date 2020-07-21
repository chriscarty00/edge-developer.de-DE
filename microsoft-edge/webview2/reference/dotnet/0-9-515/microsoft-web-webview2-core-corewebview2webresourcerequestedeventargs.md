---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 656510998879e77c2e7797c700dacc5966299210
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884652"
---
# <span data-ttu-id="d4682-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="d4682-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="d4682-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d4682-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d4682-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d4682-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d4682-107">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d4682-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="d4682-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d4682-108">Summary</span></span>

 <span data-ttu-id="d4682-109">Member</span><span class="sxs-lookup"><span data-stu-id="d4682-109">Members</span></span>                        | <span data-ttu-id="d4682-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d4682-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d4682-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4682-111">Request</span></span>](#request) | <span data-ttu-id="d4682-112">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d4682-112">The HTTP request.</span></span>
[<span data-ttu-id="d4682-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="d4682-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="d4682-114">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="d4682-114">The web resource request contexts.</span></span>
[<span data-ttu-id="d4682-115">Antwort</span><span class="sxs-lookup"><span data-stu-id="d4682-115">Response</span></span>](#response) | <span data-ttu-id="d4682-116">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="d4682-116">The HTTP response.</span></span>
[<span data-ttu-id="d4682-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d4682-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d4682-118">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="d4682-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="d4682-119">Member</span><span class="sxs-lookup"><span data-stu-id="d4682-119">Members</span></span>

#### <span data-ttu-id="d4682-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4682-120">Request</span></span> 

<span data-ttu-id="d4682-121">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d4682-121">The HTTP request.</span></span>

> <span data-ttu-id="d4682-122">öffentliche HttpRequestMessage- [Anforderung](#request)</span><span class="sxs-lookup"><span data-stu-id="d4682-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="d4682-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="d4682-123">ResourceContext</span></span> 

<span data-ttu-id="d4682-124">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="d4682-124">The web resource request contexts.</span></span>

> <span data-ttu-id="d4682-125">Public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) - [resourcecontext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="d4682-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="d4682-126">Antwort</span><span class="sxs-lookup"><span data-stu-id="d4682-126">Response</span></span> 

<span data-ttu-id="d4682-127">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="d4682-127">The HTTP response.</span></span>

> <span data-ttu-id="d4682-128">öffentliche HttpResponseMessage- [Antwort](#response)</span><span class="sxs-lookup"><span data-stu-id="d4682-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="d4682-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d4682-129">GetDeferral</span></span> 

<span data-ttu-id="d4682-130">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="d4682-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="d4682-131">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="d4682-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="d4682-132">Sie können das CoreWebView2Deferral-Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d4682-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>


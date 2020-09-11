---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 2282b36d3b7dfcca83f84ed50a976d4e6622ce07
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010124"
---
# <span data-ttu-id="b6635-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="b6635-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="b6635-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b6635-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b6635-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b6635-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b6635-107">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b6635-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="b6635-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b6635-108">Summary</span></span>

 <span data-ttu-id="b6635-109">Member</span><span class="sxs-lookup"><span data-stu-id="b6635-109">Members</span></span>                        | <span data-ttu-id="b6635-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b6635-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b6635-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6635-111">Request</span></span>](#request) | <span data-ttu-id="b6635-112">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b6635-112">The HTTP request.</span></span>
[<span data-ttu-id="b6635-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="b6635-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="b6635-114">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="b6635-114">The web resource request contexts.</span></span>
[<span data-ttu-id="b6635-115">Antwort</span><span class="sxs-lookup"><span data-stu-id="b6635-115">Response</span></span>](#response) | <span data-ttu-id="b6635-116">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="b6635-116">The HTTP response.</span></span>
[<span data-ttu-id="b6635-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b6635-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="b6635-118">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="b6635-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="b6635-119">Member</span><span class="sxs-lookup"><span data-stu-id="b6635-119">Members</span></span>

#### <span data-ttu-id="b6635-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6635-120">Request</span></span> 

<span data-ttu-id="b6635-121">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b6635-121">The HTTP request.</span></span>

> <span data-ttu-id="b6635-122">öffentliche HttpRequestMessage- [Anforderung](#request)</span><span class="sxs-lookup"><span data-stu-id="b6635-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="b6635-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="b6635-123">ResourceContext</span></span> 

<span data-ttu-id="b6635-124">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="b6635-124">The web resource request contexts.</span></span>

> <span data-ttu-id="b6635-125">Public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) - [resourcecontext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="b6635-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="b6635-126">Antwort</span><span class="sxs-lookup"><span data-stu-id="b6635-126">Response</span></span> 

<span data-ttu-id="b6635-127">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="b6635-127">The HTTP response.</span></span>

> <span data-ttu-id="b6635-128">öffentliche HttpResponseMessage- [Antwort](#response)</span><span class="sxs-lookup"><span data-stu-id="b6635-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="b6635-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b6635-129">GetDeferral</span></span> 

<span data-ttu-id="b6635-130">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="b6635-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="b6635-131">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="b6635-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="b6635-132">Sie können das CoreWebView2Deferral-Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b6635-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>


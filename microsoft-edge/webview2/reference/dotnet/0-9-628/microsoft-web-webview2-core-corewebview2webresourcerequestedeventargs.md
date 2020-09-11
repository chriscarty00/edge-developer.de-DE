---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 501483894a2abca58c5a1856ab587b93be904c8b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012044"
---
# <span data-ttu-id="2e35c-104">Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="2e35c-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="2e35c-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2e35c-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2e35c-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="2e35c-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2e35c-107">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="2e35c-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="2e35c-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2e35c-108">Summary</span></span>

 <span data-ttu-id="2e35c-109">Member</span><span class="sxs-lookup"><span data-stu-id="2e35c-109">Members</span></span>                        | <span data-ttu-id="2e35c-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2e35c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2e35c-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e35c-111">Request</span></span>](#request) | <span data-ttu-id="2e35c-112">Die Webressourcen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2e35c-112">The Web resource request.</span></span>
[<span data-ttu-id="2e35c-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="2e35c-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="2e35c-114">Der Webressourcen-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="2e35c-114">The web resource request context.</span></span>
[<span data-ttu-id="2e35c-115">Antwort</span><span class="sxs-lookup"><span data-stu-id="2e35c-115">Response</span></span>](#response) | <span data-ttu-id="2e35c-116">Ein Platzhalter für das Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="2e35c-116">A placeholder for the web resource response object.</span></span>
[<span data-ttu-id="2e35c-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2e35c-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2e35c-118">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="2e35c-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="2e35c-119">Member</span><span class="sxs-lookup"><span data-stu-id="2e35c-119">Members</span></span>

#### <span data-ttu-id="2e35c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e35c-120">Request</span></span> 

<span data-ttu-id="2e35c-121">Die Webressourcen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2e35c-121">The Web resource request.</span></span>

> <span data-ttu-id="2e35c-122">öffentliche [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md) - [Anforderung](#request)</span><span class="sxs-lookup"><span data-stu-id="2e35c-122">public [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md) [Request](#request)</span></span>

<span data-ttu-id="2e35c-123">Möglicherweise fehlen dem Anforderungsobjekt einige Überschriften, die später vom Netzwerkstapel hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2e35c-123">The request object may be missing some headers that are added by network stack later on.</span></span>

#### <span data-ttu-id="2e35c-124">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="2e35c-124">ResourceContext</span></span> 

<span data-ttu-id="2e35c-125">Der Webressourcen-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="2e35c-125">The web resource request context.</span></span>

> <span data-ttu-id="2e35c-126">Public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) - [resourcecontext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="2e35c-126">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="2e35c-127">Antwort</span><span class="sxs-lookup"><span data-stu-id="2e35c-127">Response</span></span> 

<span data-ttu-id="2e35c-128">Ein Platzhalter für das Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="2e35c-128">A placeholder for the web resource response object.</span></span>

> <span data-ttu-id="2e35c-129">öffentliche [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) - [Antwort](#response)</span><span class="sxs-lookup"><span data-stu-id="2e35c-129">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [Response](#response)</span></span>

<span data-ttu-id="2e35c-130">Wenn dieses Objekt gesetzt ist, wird die Web-Ressourcenanforderung mit dieser Antwort abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2e35c-130">If this object is set, the web resource request will be completed with this response.</span></span> <span data-ttu-id="2e35c-131">Ein leeres Webressourcen-Antwortobjekt kann mit CreateWebResourceResponse erstellt und dann geändert werden, um die Antwort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2e35c-131">An empty Web resource response object can be created with CreateWebResourceResponse and then modified to construct the response.</span></span>

#### <span data-ttu-id="2e35c-132">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2e35c-132">GetDeferral</span></span> 

<span data-ttu-id="2e35c-133">Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="2e35c-133">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="2e35c-134">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="2e35c-134">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="2e35c-135">Sie können das CoreWebView2Deferral-Objekt verwenden, um die Anforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2e35c-135">You can use the CoreWebView2Deferral object to complete the request at a later time.</span></span>


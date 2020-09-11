---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
ms.openlocfilehash: 5c8d164b24995cc31070232dd9b1a2d88fc16cec
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012045"
---
# <span data-ttu-id="d808f-104">Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest Klasse</span><span class="sxs-lookup"><span data-stu-id="d808f-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest class</span></span> 

<span data-ttu-id="d808f-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d808f-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d808f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d808f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d808f-107">Eine HTTP-Anforderung für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d808f-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="d808f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d808f-108">Summary</span></span>

 <span data-ttu-id="d808f-109">Member</span><span class="sxs-lookup"><span data-stu-id="d808f-109">Members</span></span>                        | <span data-ttu-id="d808f-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d808f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d808f-111">Inhalt</span><span class="sxs-lookup"><span data-stu-id="d808f-111">Content</span></span>](#content) | <span data-ttu-id="d808f-112">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="d808f-112">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="d808f-113">Header</span><span class="sxs-lookup"><span data-stu-id="d808f-113">Headers</span></span>](#headers) | <span data-ttu-id="d808f-114">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="d808f-114">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="d808f-115">Methode</span><span class="sxs-lookup"><span data-stu-id="d808f-115">Method</span></span>](#method) | <span data-ttu-id="d808f-116">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="d808f-116">The HTTP request method.</span></span>
[<span data-ttu-id="d808f-117">URI</span><span class="sxs-lookup"><span data-stu-id="d808f-117">Uri</span></span>](#uri) | <span data-ttu-id="d808f-118">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="d808f-118">The request URI.</span></span>

## <span data-ttu-id="d808f-119">Member</span><span class="sxs-lookup"><span data-stu-id="d808f-119">Members</span></span>

#### <span data-ttu-id="d808f-120">Inhalt</span><span class="sxs-lookup"><span data-stu-id="d808f-120">Content</span></span> 

<span data-ttu-id="d808f-121">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="d808f-121">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="d808f-122">[Inhalte](#content) öffentlicher Datenströme</span><span class="sxs-lookup"><span data-stu-id="d808f-122">public Stream [Content](#content)</span></span>

<span data-ttu-id="d808f-123">Post-Daten wären hier.</span><span class="sxs-lookup"><span data-stu-id="d808f-123">POST data would be here.</span></span> <span data-ttu-id="d808f-124">Wenn ein Datenstrom festgesetzt wird, der den Nachrichtentext überschreibt, muss der Datenstrom alle Inhaltsdaten aufweisen, bis die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d808f-124">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="d808f-125">Stream sollte agil sein oder aus einem background-STA erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="d808f-125">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="d808f-126">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="d808f-126">Null means no content data.</span></span> <span data-ttu-id="d808f-127">IStream-Semantik wird angewendet (geben Sie S_OK ein, um Anrufe zu lesen, bis alle Daten erschöpft sind).</span><span class="sxs-lookup"><span data-stu-id="d808f-127">IStream semantics apply (return S_OK to Read calls until all data is exhausted).</span></span>

#### <span data-ttu-id="d808f-128">Header</span><span class="sxs-lookup"><span data-stu-id="d808f-128">Headers</span></span> 

<span data-ttu-id="d808f-129">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="d808f-129">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="d808f-130">öffentliche [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md) - [Header](#headers)</span><span class="sxs-lookup"><span data-stu-id="d808f-130">public [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md) [Headers](#headers)</span></span>

#### <span data-ttu-id="d808f-131">Methode</span><span class="sxs-lookup"><span data-stu-id="d808f-131">Method</span></span> 

<span data-ttu-id="d808f-132">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="d808f-132">The HTTP request method.</span></span>

> <span data-ttu-id="d808f-133">public String [-Methode](#method)</span><span class="sxs-lookup"><span data-stu-id="d808f-133">public string [Method](#method)</span></span>

#### <span data-ttu-id="d808f-134">URI</span><span class="sxs-lookup"><span data-stu-id="d808f-134">Uri</span></span> 

<span data-ttu-id="d808f-135">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="d808f-135">The request URI.</span></span>

> <span data-ttu-id="d808f-136">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="d808f-136">public string [Uri](#uri)</span></span>


---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
ms.openlocfilehash: 5359634d83717ce844d2c1604a2645ceffc477cc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012041"
---
# <span data-ttu-id="fd43b-104">Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse Klasse</span><span class="sxs-lookup"><span data-stu-id="fd43b-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse class</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="fd43b-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="fd43b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="fd43b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="fd43b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="fd43b-107">Eine HTTP-Antwort, die mit dem WebResourceRequested-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd43b-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="fd43b-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fd43b-108">Summary</span></span>

 <span data-ttu-id="fd43b-109">Member</span><span class="sxs-lookup"><span data-stu-id="fd43b-109">Members</span></span>                        | <span data-ttu-id="fd43b-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="fd43b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fd43b-111">Inhalt</span><span class="sxs-lookup"><span data-stu-id="fd43b-111">Content</span></span>](#content) | <span data-ttu-id="fd43b-112">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="fd43b-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="fd43b-113">Header</span><span class="sxs-lookup"><span data-stu-id="fd43b-113">Headers</span></span>](#headers) | <span data-ttu-id="fd43b-114">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="fd43b-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="fd43b-115">ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="fd43b-115">ReasonPhrase</span></span>](#reasonphrase) | <span data-ttu-id="fd43b-116">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="fd43b-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="fd43b-117">Statuscode</span><span class="sxs-lookup"><span data-stu-id="fd43b-117">StatusCode</span></span>](#statuscode) | <span data-ttu-id="fd43b-118">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="fd43b-118">The HTTP response status code.</span></span>

## <span data-ttu-id="fd43b-119">Member</span><span class="sxs-lookup"><span data-stu-id="fd43b-119">Members</span></span>

#### <span data-ttu-id="fd43b-120">Inhalt</span><span class="sxs-lookup"><span data-stu-id="fd43b-120">Content</span></span> 

<span data-ttu-id="fd43b-121">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="fd43b-121">HTTP response content as stream.</span></span>

> <span data-ttu-id="fd43b-122">[Inhalte](#content) öffentlicher Datenströme</span><span class="sxs-lookup"><span data-stu-id="fd43b-122">public Stream [Content](#content)</span></span>

<span data-ttu-id="fd43b-123">Datenstrom muss alle Inhaltsdaten zur Verfügung stehen, wenn die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fd43b-123">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="fd43b-124">Stream sollte agil sein oder aus einem Hintergrundthread erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="fd43b-124">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="fd43b-125">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="fd43b-125">Null means no content data.</span></span> <span data-ttu-id="fd43b-126">IStream-Semantik wird angewendet (geben Sie S_OK ein, um Anrufe zu lesen, bis alle Daten erschöpft sind).</span><span class="sxs-lookup"><span data-stu-id="fd43b-126">IStream semantics apply (return S_OK to Read calls until all data is exhausted).</span></span>

#### <span data-ttu-id="fd43b-127">Header</span><span class="sxs-lookup"><span data-stu-id="fd43b-127">Headers</span></span> 

<span data-ttu-id="fd43b-128">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="fd43b-128">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="fd43b-129">öffentliche [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) - [Header](#headers)</span><span class="sxs-lookup"><span data-stu-id="fd43b-129">public [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) [Headers](#headers)</span></span>

#### <span data-ttu-id="fd43b-130">ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="fd43b-130">ReasonPhrase</span></span> 

<span data-ttu-id="fd43b-131">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="fd43b-131">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="fd43b-132">public String [ReasonPhrase](#reasonphrase)</span><span class="sxs-lookup"><span data-stu-id="fd43b-132">public string [ReasonPhrase](#reasonphrase)</span></span>

#### <span data-ttu-id="fd43b-133">Statuscode</span><span class="sxs-lookup"><span data-stu-id="fd43b-133">StatusCode</span></span> 

<span data-ttu-id="fd43b-134">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="fd43b-134">The HTTP response status code.</span></span>

> <span data-ttu-id="fd43b-135">public int [Statuscode](#statuscode)</span><span class="sxs-lookup"><span data-stu-id="fd43b-135">public int [StatusCode](#statuscode)</span></span>


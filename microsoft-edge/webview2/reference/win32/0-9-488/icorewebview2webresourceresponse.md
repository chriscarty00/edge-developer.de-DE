---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: d6b51600479f47eebb09d5cff8fb096455fb1766
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653758"
---
# <span data-ttu-id="c5fd8-104">Schnittstellen ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="c5fd8-104">interface ICoreWebView2WebResourceResponse</span></span> 

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="c5fd8-105">Eine HTTP-Antwort, die mit dem WebResourceRequested-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="c5fd8-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c5fd8-106">Summary</span></span>

 <span data-ttu-id="c5fd8-107">Member</span><span class="sxs-lookup"><span data-stu-id="c5fd8-107">Members</span></span>                        | <span data-ttu-id="c5fd8-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c5fd8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c5fd8-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="c5fd8-109">get_Content</span></span>](#get_content) | <span data-ttu-id="c5fd8-110">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="c5fd8-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="c5fd8-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="c5fd8-112">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-112">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="c5fd8-113">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="c5fd8-113">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="c5fd8-114">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-114">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="c5fd8-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="c5fd8-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="c5fd8-116">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-116">The HTTP response status code.</span></span>
[<span data-ttu-id="c5fd8-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="c5fd8-117">put_Content</span></span>](#put_content) | <span data-ttu-id="c5fd8-118">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c5fd8-118">Set the Content property.</span></span>
[<span data-ttu-id="c5fd8-119">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="c5fd8-119">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="c5fd8-120">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c5fd8-120">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="c5fd8-121">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="c5fd8-121">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="c5fd8-122">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-122">Set the StatusCode property.</span></span>

## <span data-ttu-id="c5fd8-123">Member</span><span class="sxs-lookup"><span data-stu-id="c5fd8-123">Members</span></span>

#### <span data-ttu-id="c5fd8-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="c5fd8-124">get_Content</span></span> 

<span data-ttu-id="c5fd8-125">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="c5fd8-126">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="c5fd8-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="c5fd8-127">Datenstrom muss alle Inhaltsdaten zur Verfügung stehen, wenn die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="c5fd8-128">Stream sollte agil sein oder aus einem Hintergrundthread erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="c5fd8-129">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-129">Null means no content data.</span></span> <span data-ttu-id="c5fd8-130">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="c5fd8-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="c5fd8-131">get_Headers</span><span class="sxs-lookup"><span data-stu-id="c5fd8-131">get_Headers</span></span> 

<span data-ttu-id="c5fd8-132">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-132">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="c5fd8-133">öffentliche HRESULT- [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="c5fd8-133">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="c5fd8-134">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="c5fd8-134">get_ReasonPhrase</span></span> 

<span data-ttu-id="c5fd8-135">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-135">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="c5fd8-136">Public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="c5fd8-136">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="c5fd8-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="c5fd8-137">get_StatusCode</span></span> 

<span data-ttu-id="c5fd8-138">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-138">The HTTP response status code.</span></span>

> <span data-ttu-id="c5fd8-139">Public HRESULT [get_StatusCode](#get_statuscode)(int \* Statuscode)</span><span class="sxs-lookup"><span data-stu-id="c5fd8-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="c5fd8-140">put_Content</span><span class="sxs-lookup"><span data-stu-id="c5fd8-140">put_Content</span></span> 

<span data-ttu-id="c5fd8-141">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c5fd8-141">Set the Content property.</span></span>

> <span data-ttu-id="c5fd8-142">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="c5fd8-142">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="c5fd8-143">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="c5fd8-143">put_ReasonPhrase</span></span> 

<span data-ttu-id="c5fd8-144">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c5fd8-144">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="c5fd8-145">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="c5fd8-145">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="c5fd8-146">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="c5fd8-146">put_StatusCode</span></span> 

<span data-ttu-id="c5fd8-147">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="c5fd8-147">Set the StatusCode property.</span></span>

> <span data-ttu-id="c5fd8-148">Public HRESULT [put_StatusCode](#put_statuscode)(int Statuscode)</span><span class="sxs-lookup"><span data-stu-id="c5fd8-148">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>


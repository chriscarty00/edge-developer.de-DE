---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 7072a25636efb638fcb42c593aa6cc77e990965a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698856"
---
# <span data-ttu-id="e4414-104">Schnittstellen ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="e4414-104">interface ICoreWebView2WebResourceResponse</span></span> 

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="e4414-105">Eine HTTP-Antwort, die mit dem WebResourceRequested-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4414-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="e4414-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e4414-106">Summary</span></span>

 <span data-ttu-id="e4414-107">Member</span><span class="sxs-lookup"><span data-stu-id="e4414-107">Members</span></span>                        | <span data-ttu-id="e4414-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e4414-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e4414-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="e4414-109">get_Content</span></span>](#get_content) | <span data-ttu-id="e4414-110">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="e4414-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="e4414-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="e4414-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="e4414-112">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="e4414-112">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="e4414-113">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="e4414-113">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="e4414-114">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="e4414-114">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="e4414-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="e4414-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="e4414-116">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="e4414-116">The HTTP response status code.</span></span>
[<span data-ttu-id="e4414-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="e4414-117">put_Content</span></span>](#put_content) | <span data-ttu-id="e4414-118">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e4414-118">Set the Content property.</span></span>
[<span data-ttu-id="e4414-119">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="e4414-119">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="e4414-120">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e4414-120">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="e4414-121">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="e4414-121">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="e4414-122">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="e4414-122">Set the StatusCode property.</span></span>

## <span data-ttu-id="e4414-123">Member</span><span class="sxs-lookup"><span data-stu-id="e4414-123">Members</span></span>

#### <span data-ttu-id="e4414-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="e4414-124">get_Content</span></span> 

<span data-ttu-id="e4414-125">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="e4414-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="e4414-126">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="e4414-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="e4414-127">Datenstrom muss alle Inhaltsdaten zur Verfügung stehen, wenn die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e4414-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="e4414-128">Stream sollte agil sein oder aus einem Hintergrundthread erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="e4414-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="e4414-129">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="e4414-129">Null means no content data.</span></span> <span data-ttu-id="e4414-130">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="e4414-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="e4414-131">get_Headers</span><span class="sxs-lookup"><span data-stu-id="e4414-131">get_Headers</span></span> 

<span data-ttu-id="e4414-132">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="e4414-132">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="e4414-133">öffentliche HRESULT- [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="e4414-133">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="e4414-134">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="e4414-134">get_ReasonPhrase</span></span> 

<span data-ttu-id="e4414-135">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="e4414-135">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="e4414-136">Public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="e4414-136">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="e4414-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="e4414-137">get_StatusCode</span></span> 

<span data-ttu-id="e4414-138">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="e4414-138">The HTTP response status code.</span></span>

> <span data-ttu-id="e4414-139">Public HRESULT [get_StatusCode](#get_statuscode)(int \* Statuscode)</span><span class="sxs-lookup"><span data-stu-id="e4414-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="e4414-140">put_Content</span><span class="sxs-lookup"><span data-stu-id="e4414-140">put_Content</span></span> 

<span data-ttu-id="e4414-141">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e4414-141">Set the Content property.</span></span>

> <span data-ttu-id="e4414-142">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="e4414-142">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="e4414-143">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="e4414-143">put_ReasonPhrase</span></span> 

<span data-ttu-id="e4414-144">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e4414-144">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="e4414-145">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="e4414-145">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="e4414-146">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="e4414-146">put_StatusCode</span></span> 

<span data-ttu-id="e4414-147">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="e4414-147">Set the StatusCode property.</span></span>

> <span data-ttu-id="e4414-148">Public HRESULT [put_StatusCode](#put_statuscode)(int Statuscode)</span><span class="sxs-lookup"><span data-stu-id="e4414-148">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>


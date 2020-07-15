---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 7a649944686df4d425141d5d22c03c5874572d1a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877343"
---
# <span data-ttu-id="7dda2-104">0.9.515-Interface-ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="7dda2-104">0.9.515 - interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="7dda2-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="7dda2-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="7dda2-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="7dda2-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="7dda2-107">Eine HTTP-Antwort, die mit dem WebResourceRequested-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7dda2-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="7dda2-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7dda2-108">Summary</span></span>

 <span data-ttu-id="7dda2-109">Member</span><span class="sxs-lookup"><span data-stu-id="7dda2-109">Members</span></span>                        | <span data-ttu-id="7dda2-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7dda2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7dda2-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="7dda2-111">get_Content</span></span>](#get_content) | <span data-ttu-id="7dda2-112">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="7dda2-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="7dda2-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="7dda2-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="7dda2-114">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="7dda2-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="7dda2-115">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="7dda2-115">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="7dda2-116">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="7dda2-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="7dda2-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="7dda2-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="7dda2-118">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="7dda2-118">The HTTP response status code.</span></span>
[<span data-ttu-id="7dda2-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="7dda2-119">put_Content</span></span>](#put_content) | <span data-ttu-id="7dda2-120">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7dda2-120">Set the Content property.</span></span>
[<span data-ttu-id="7dda2-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="7dda2-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="7dda2-122">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7dda2-122">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="7dda2-123">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="7dda2-123">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="7dda2-124">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="7dda2-124">Set the StatusCode property.</span></span>

## <span data-ttu-id="7dda2-125">Member</span><span class="sxs-lookup"><span data-stu-id="7dda2-125">Members</span></span>

#### <span data-ttu-id="7dda2-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="7dda2-126">get_Content</span></span> 

<span data-ttu-id="7dda2-127">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="7dda2-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="7dda2-128">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="7dda2-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="7dda2-129">Datenstrom muss alle Inhaltsdaten zur Verfügung stehen, wenn die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7dda2-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="7dda2-130">Stream sollte agil sein oder aus einem Hintergrundthread erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="7dda2-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="7dda2-131">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="7dda2-131">Null means no content data.</span></span> <span data-ttu-id="7dda2-132">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="7dda2-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="7dda2-133">get_Headers</span><span class="sxs-lookup"><span data-stu-id="7dda2-133">get_Headers</span></span> 

<span data-ttu-id="7dda2-134">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="7dda2-134">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="7dda2-135">öffentliche HRESULT- [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="7dda2-135">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="7dda2-136">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="7dda2-136">get_ReasonPhrase</span></span> 

<span data-ttu-id="7dda2-137">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="7dda2-137">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="7dda2-138">Public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="7dda2-138">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="7dda2-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="7dda2-139">get_StatusCode</span></span> 

<span data-ttu-id="7dda2-140">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="7dda2-140">The HTTP response status code.</span></span>

> <span data-ttu-id="7dda2-141">Public HRESULT [get_StatusCode](#get_statuscode)(int \* Statuscode)</span><span class="sxs-lookup"><span data-stu-id="7dda2-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="7dda2-142">put_Content</span><span class="sxs-lookup"><span data-stu-id="7dda2-142">put_Content</span></span> 

<span data-ttu-id="7dda2-143">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7dda2-143">Set the Content property.</span></span>

> <span data-ttu-id="7dda2-144">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="7dda2-144">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="7dda2-145">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="7dda2-145">put_ReasonPhrase</span></span> 

<span data-ttu-id="7dda2-146">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7dda2-146">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="7dda2-147">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="7dda2-147">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="7dda2-148">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="7dda2-148">put_StatusCode</span></span> 

<span data-ttu-id="7dda2-149">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="7dda2-149">Set the StatusCode property.</span></span>

> <span data-ttu-id="7dda2-150">Public HRESULT [put_StatusCode](#put_statuscode)(int Statuscode)</span><span class="sxs-lookup"><span data-stu-id="7dda2-150">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>


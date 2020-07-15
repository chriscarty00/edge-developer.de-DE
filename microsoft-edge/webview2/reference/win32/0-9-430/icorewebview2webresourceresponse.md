---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c0c33bab95f8d2c7908864b1869bc9a186216ef9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877546"
---
# <span data-ttu-id="d53aa-104">0.9.430-Interface-ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="d53aa-104">0.9.430 - interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="d53aa-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="d53aa-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d53aa-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="d53aa-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="d53aa-107">Eine HTTP-Antwort, die mit dem WebResourceRequested-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d53aa-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="d53aa-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d53aa-108">Summary</span></span>

 <span data-ttu-id="d53aa-109">Member</span><span class="sxs-lookup"><span data-stu-id="d53aa-109">Members</span></span>                        | <span data-ttu-id="d53aa-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d53aa-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d53aa-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="d53aa-111">get_Content</span></span>](#get_content) | <span data-ttu-id="d53aa-112">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="d53aa-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="d53aa-113">put_Content</span><span class="sxs-lookup"><span data-stu-id="d53aa-113">put_Content</span></span>](#put_content) | <span data-ttu-id="d53aa-114">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d53aa-114">Set the Content property.</span></span>
[<span data-ttu-id="d53aa-115">get_Headers</span><span class="sxs-lookup"><span data-stu-id="d53aa-115">get_Headers</span></span>](#get_headers) | <span data-ttu-id="d53aa-116">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="d53aa-116">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="d53aa-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="d53aa-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="d53aa-118">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="d53aa-118">The HTTP response status code.</span></span>
[<span data-ttu-id="d53aa-119">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="d53aa-119">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="d53aa-120">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="d53aa-120">Set the StatusCode property.</span></span>
[<span data-ttu-id="d53aa-121">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="d53aa-121">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="d53aa-122">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="d53aa-122">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="d53aa-123">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="d53aa-123">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="d53aa-124">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d53aa-124">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="d53aa-125">Member</span><span class="sxs-lookup"><span data-stu-id="d53aa-125">Members</span></span>

#### <span data-ttu-id="d53aa-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="d53aa-126">get_Content</span></span> 

<span data-ttu-id="d53aa-127">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="d53aa-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="d53aa-128">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="d53aa-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="d53aa-129">Datenstrom muss alle Inhaltsdaten zur Verfügung stehen, wenn die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d53aa-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="d53aa-130">Stream sollte agil sein oder aus einem Hintergrundthread erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="d53aa-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="d53aa-131">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="d53aa-131">Null means no content data.</span></span> <span data-ttu-id="d53aa-132">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="d53aa-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="d53aa-133">put_Content</span><span class="sxs-lookup"><span data-stu-id="d53aa-133">put_Content</span></span> 

<span data-ttu-id="d53aa-134">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d53aa-134">Set the Content property.</span></span>

> <span data-ttu-id="d53aa-135">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="d53aa-135">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="d53aa-136">get_Headers</span><span class="sxs-lookup"><span data-stu-id="d53aa-136">get_Headers</span></span> 

<span data-ttu-id="d53aa-137">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="d53aa-137">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="d53aa-138">öffentliche HRESULT- [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="d53aa-138">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="d53aa-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="d53aa-139">get_StatusCode</span></span> 

<span data-ttu-id="d53aa-140">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="d53aa-140">The HTTP response status code.</span></span>

> <span data-ttu-id="d53aa-141">Public HRESULT [get_StatusCode](#get_statuscode)(int \* Statuscode)</span><span class="sxs-lookup"><span data-stu-id="d53aa-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="d53aa-142">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="d53aa-142">put_StatusCode</span></span> 

<span data-ttu-id="d53aa-143">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="d53aa-143">Set the StatusCode property.</span></span>

> <span data-ttu-id="d53aa-144">Public HRESULT [put_StatusCode](#put_statuscode)(int Statuscode)</span><span class="sxs-lookup"><span data-stu-id="d53aa-144">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="d53aa-145">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="d53aa-145">get_ReasonPhrase</span></span> 

<span data-ttu-id="d53aa-146">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="d53aa-146">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="d53aa-147">Public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="d53aa-147">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="d53aa-148">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="d53aa-148">put_ReasonPhrase</span></span> 

<span data-ttu-id="d53aa-149">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d53aa-149">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="d53aa-150">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="d53aa-150">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>


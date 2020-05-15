---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: ad3f4e5e95b0309628644f17e5d647ab6d4af658
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653766"
---
# <span data-ttu-id="5894d-104">Schnittstellen IWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="5894d-104">interface IWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="5894d-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="5894d-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="5894d-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="5894d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="5894d-107">Eine HTTP-Antwort, die mit dem WebResourceRequested-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5894d-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="5894d-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5894d-108">Summary</span></span>

 <span data-ttu-id="5894d-109">Member</span><span class="sxs-lookup"><span data-stu-id="5894d-109">Members</span></span>                        | <span data-ttu-id="5894d-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5894d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5894d-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="5894d-111">get_Content</span></span>](#get_content) | <span data-ttu-id="5894d-112">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="5894d-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="5894d-113">put_Content</span><span class="sxs-lookup"><span data-stu-id="5894d-113">put_Content</span></span>](#put_content) | <span data-ttu-id="5894d-114">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5894d-114">Set the Content property.</span></span>
[<span data-ttu-id="5894d-115">get_Headers</span><span class="sxs-lookup"><span data-stu-id="5894d-115">get_Headers</span></span>](#get_headers) | <span data-ttu-id="5894d-116">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="5894d-116">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="5894d-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="5894d-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="5894d-118">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="5894d-118">The HTTP response status code.</span></span>
[<span data-ttu-id="5894d-119">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="5894d-119">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="5894d-120">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="5894d-120">Set the StatusCode property.</span></span>
[<span data-ttu-id="5894d-121">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="5894d-121">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="5894d-122">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="5894d-122">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="5894d-123">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="5894d-123">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="5894d-124">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5894d-124">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="5894d-125">Member</span><span class="sxs-lookup"><span data-stu-id="5894d-125">Members</span></span>

#### <span data-ttu-id="5894d-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="5894d-126">get_Content</span></span> 

<span data-ttu-id="5894d-127">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="5894d-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="5894d-128">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="5894d-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="5894d-129">Datenstrom muss alle Inhaltsdaten zur Verfügung stehen, wenn die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5894d-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="5894d-130">Stream sollte agil sein oder aus einem Hintergrundthread erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="5894d-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="5894d-131">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="5894d-131">Null means no content data.</span></span> <span data-ttu-id="5894d-132">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="5894d-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="5894d-133">put_Content</span><span class="sxs-lookup"><span data-stu-id="5894d-133">put_Content</span></span> 

<span data-ttu-id="5894d-134">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5894d-134">Set the Content property.</span></span>

> <span data-ttu-id="5894d-135">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="5894d-135">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="5894d-136">get_Headers</span><span class="sxs-lookup"><span data-stu-id="5894d-136">get_Headers</span></span> 

<span data-ttu-id="5894d-137">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="5894d-137">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="5894d-138">öffentliche HRESULT- [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="5894d-138">public HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="5894d-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="5894d-139">get_StatusCode</span></span> 

<span data-ttu-id="5894d-140">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="5894d-140">The HTTP response status code.</span></span>

> <span data-ttu-id="5894d-141">Public HRESULT [get_StatusCode](#get_statuscode)(int \* Statuscode)</span><span class="sxs-lookup"><span data-stu-id="5894d-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="5894d-142">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="5894d-142">put_StatusCode</span></span> 

<span data-ttu-id="5894d-143">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="5894d-143">Set the StatusCode property.</span></span>

> <span data-ttu-id="5894d-144">Public HRESULT [put_StatusCode](#put_statuscode)(int Statuscode)</span><span class="sxs-lookup"><span data-stu-id="5894d-144">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="5894d-145">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="5894d-145">get_ReasonPhrase</span></span> 

<span data-ttu-id="5894d-146">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="5894d-146">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="5894d-147">Public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="5894d-147">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="5894d-148">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="5894d-148">put_ReasonPhrase</span></span> 

<span data-ttu-id="5894d-149">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5894d-149">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="5894d-150">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="5894d-150">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 82c94869a84165de4c3b8d09937d6ea5d1f79256
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885688"
---
# <span data-ttu-id="09cf7-104">0.8.355-Interface-IWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="09cf7-104">0.8.355 - interface IWebView2WebResourceResponse</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="09cf7-105">Eine HTTP-Antwort, die mit dem WebResourceRequested-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="09cf7-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="09cf7-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="09cf7-106">Summary</span></span>

 <span data-ttu-id="09cf7-107">Member</span><span class="sxs-lookup"><span data-stu-id="09cf7-107">Members</span></span>                        | <span data-ttu-id="09cf7-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="09cf7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="09cf7-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="09cf7-109">get_Content</span></span>](#get_content) | <span data-ttu-id="09cf7-110">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="09cf7-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="09cf7-111">put_Content</span><span class="sxs-lookup"><span data-stu-id="09cf7-111">put_Content</span></span>](#put_content) | <span data-ttu-id="09cf7-112">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="09cf7-112">Set the Content property.</span></span>
[<span data-ttu-id="09cf7-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="09cf7-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="09cf7-114">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="09cf7-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="09cf7-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="09cf7-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="09cf7-116">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="09cf7-116">The HTTP response status code.</span></span>
[<span data-ttu-id="09cf7-117">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="09cf7-117">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="09cf7-118">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="09cf7-118">Set the StatusCode property.</span></span>
[<span data-ttu-id="09cf7-119">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="09cf7-119">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="09cf7-120">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="09cf7-120">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="09cf7-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="09cf7-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="09cf7-122">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="09cf7-122">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="09cf7-123">Member</span><span class="sxs-lookup"><span data-stu-id="09cf7-123">Members</span></span>

#### <span data-ttu-id="09cf7-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="09cf7-124">get_Content</span></span> 

<span data-ttu-id="09cf7-125">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="09cf7-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="09cf7-126">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="09cf7-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="09cf7-127">Datenstrom muss alle Inhaltsdaten zur Verfügung stehen, wenn die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="09cf7-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="09cf7-128">Stream sollte agil sein oder aus einem Hintergrundthread erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="09cf7-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="09cf7-129">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="09cf7-129">Null means no content data.</span></span> <span data-ttu-id="09cf7-130">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="09cf7-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="09cf7-131">put_Content</span><span class="sxs-lookup"><span data-stu-id="09cf7-131">put_Content</span></span> 

<span data-ttu-id="09cf7-132">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="09cf7-132">Set the Content property.</span></span>

> <span data-ttu-id="09cf7-133">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="09cf7-133">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="09cf7-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="09cf7-134">get_Headers</span></span> 

<span data-ttu-id="09cf7-135">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="09cf7-135">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="09cf7-136">öffentliche HRESULT- [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="09cf7-136">public HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="09cf7-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="09cf7-137">get_StatusCode</span></span> 

<span data-ttu-id="09cf7-138">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="09cf7-138">The HTTP response status code.</span></span>

> <span data-ttu-id="09cf7-139">Public HRESULT [get_StatusCode](#get_statuscode)(int \* Statuscode)</span><span class="sxs-lookup"><span data-stu-id="09cf7-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="09cf7-140">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="09cf7-140">put_StatusCode</span></span> 

<span data-ttu-id="09cf7-141">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="09cf7-141">Set the StatusCode property.</span></span>

> <span data-ttu-id="09cf7-142">Public HRESULT [put_StatusCode](#put_statuscode)(int Statuscode)</span><span class="sxs-lookup"><span data-stu-id="09cf7-142">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="09cf7-143">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="09cf7-143">get_ReasonPhrase</span></span> 

<span data-ttu-id="09cf7-144">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="09cf7-144">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="09cf7-145">Public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="09cf7-145">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="09cf7-146">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="09cf7-146">put_ReasonPhrase</span></span> 

<span data-ttu-id="09cf7-147">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="09cf7-147">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="09cf7-148">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="09cf7-148">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>


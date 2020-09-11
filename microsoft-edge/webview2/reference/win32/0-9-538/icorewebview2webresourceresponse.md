---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2WebResourceResponse
ms.openlocfilehash: f94aa86f589f49930de9186cdca4a6ae943d286f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011384"
---
# <span data-ttu-id="f66bc-104">0.9.579-Interface-ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="f66bc-104">0.9.579 - interface ICoreWebView2WebResourceResponse</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="f66bc-105">Eine HTTP-Antwort, die mit dem WebResourceRequested-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f66bc-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="f66bc-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f66bc-106">Summary</span></span>

 <span data-ttu-id="f66bc-107">Member</span><span class="sxs-lookup"><span data-stu-id="f66bc-107">Members</span></span>                        | <span data-ttu-id="f66bc-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f66bc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f66bc-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="f66bc-109">get_Content</span></span>](#get_content) | <span data-ttu-id="f66bc-110">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="f66bc-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="f66bc-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="f66bc-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="f66bc-112">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="f66bc-112">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="f66bc-113">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f66bc-113">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="f66bc-114">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="f66bc-114">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="f66bc-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f66bc-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="f66bc-116">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="f66bc-116">The HTTP response status code.</span></span>
[<span data-ttu-id="f66bc-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="f66bc-117">put_Content</span></span>](#put_content) | <span data-ttu-id="f66bc-118">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f66bc-118">Set the Content property.</span></span>
[<span data-ttu-id="f66bc-119">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f66bc-119">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="f66bc-120">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f66bc-120">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="f66bc-121">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f66bc-121">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="f66bc-122">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="f66bc-122">Set the StatusCode property.</span></span>

## <span data-ttu-id="f66bc-123">Member</span><span class="sxs-lookup"><span data-stu-id="f66bc-123">Members</span></span>

#### <span data-ttu-id="f66bc-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="f66bc-124">get_Content</span></span> 

<span data-ttu-id="f66bc-125">HTTP-Antwortinhalt als Stream.</span><span class="sxs-lookup"><span data-stu-id="f66bc-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="f66bc-126">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="f66bc-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="f66bc-127">Datenstrom muss alle Inhaltsdaten zur Verfügung stehen, wenn die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f66bc-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="f66bc-128">Stream sollte agil sein oder aus einem Hintergrundthread erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="f66bc-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="f66bc-129">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="f66bc-129">Null means no content data.</span></span> <span data-ttu-id="f66bc-130">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="f66bc-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="f66bc-131">get_Headers</span><span class="sxs-lookup"><span data-stu-id="f66bc-131">get_Headers</span></span> 

<span data-ttu-id="f66bc-132">Überschriebene HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="f66bc-132">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="f66bc-133">öffentliche HRESULT- [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="f66bc-133">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="f66bc-134">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f66bc-134">get_ReasonPhrase</span></span> 

<span data-ttu-id="f66bc-135">Der HTTP-Antwort Grund Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="f66bc-135">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="f66bc-136">Public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="f66bc-136">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="f66bc-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f66bc-137">get_StatusCode</span></span> 

<span data-ttu-id="f66bc-138">Der HTTP-Antwortstatuscode.</span><span class="sxs-lookup"><span data-stu-id="f66bc-138">The HTTP response status code.</span></span>

> <span data-ttu-id="f66bc-139">Public HRESULT [get_StatusCode](#get_statuscode)(int \* Statuscode)</span><span class="sxs-lookup"><span data-stu-id="f66bc-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="f66bc-140">put_Content</span><span class="sxs-lookup"><span data-stu-id="f66bc-140">put_Content</span></span> 

<span data-ttu-id="f66bc-141">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f66bc-141">Set the Content property.</span></span>

> <span data-ttu-id="f66bc-142">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="f66bc-142">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="f66bc-143">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f66bc-143">put_ReasonPhrase</span></span> 

<span data-ttu-id="f66bc-144">Festlegen der ReasonPhrase-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f66bc-144">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="f66bc-145">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="f66bc-145">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="f66bc-146">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f66bc-146">put_StatusCode</span></span> 

<span data-ttu-id="f66bc-147">Die Statuscode-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="f66bc-147">Set the StatusCode property.</span></span>

> <span data-ttu-id="f66bc-148">Public HRESULT [put_StatusCode](#put_statuscode)(int Statuscode)</span><span class="sxs-lookup"><span data-stu-id="f66bc-148">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>


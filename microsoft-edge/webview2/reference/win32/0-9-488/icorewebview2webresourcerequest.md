---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: cdea3b4d4643e6f14e546eb9edd27bf1534beadd
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877350"
---
# <span data-ttu-id="fd03a-104">0.9.515-Interface-ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="fd03a-104">0.9.515 - interface ICoreWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="fd03a-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="fd03a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="fd03a-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="fd03a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="fd03a-107">Eine HTTP-Anforderung für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd03a-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="fd03a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fd03a-108">Summary</span></span>

 <span data-ttu-id="fd03a-109">Member</span><span class="sxs-lookup"><span data-stu-id="fd03a-109">Members</span></span>                        | <span data-ttu-id="fd03a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="fd03a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fd03a-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="fd03a-111">get_Content</span></span>](#get_content) | <span data-ttu-id="fd03a-112">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="fd03a-112">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="fd03a-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="fd03a-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="fd03a-114">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="fd03a-114">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="fd03a-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="fd03a-115">get_Method</span></span>](#get_method) | <span data-ttu-id="fd03a-116">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="fd03a-116">The HTTP request method.</span></span>
[<span data-ttu-id="fd03a-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="fd03a-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="fd03a-118">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="fd03a-118">The request URI.</span></span>
[<span data-ttu-id="fd03a-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="fd03a-119">put_Content</span></span>](#put_content) | <span data-ttu-id="fd03a-120">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fd03a-120">Set the Content property.</span></span>
[<span data-ttu-id="fd03a-121">put_Method</span><span class="sxs-lookup"><span data-stu-id="fd03a-121">put_Method</span></span>](#put_method) | <span data-ttu-id="fd03a-122">Festlegen der Method-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fd03a-122">Set the Method property.</span></span>
[<span data-ttu-id="fd03a-123">put_Uri</span><span class="sxs-lookup"><span data-stu-id="fd03a-123">put_Uri</span></span>](#put_uri) | <span data-ttu-id="fd03a-124">Die URI-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="fd03a-124">Set the Uri property.</span></span>

## <span data-ttu-id="fd03a-125">Member</span><span class="sxs-lookup"><span data-stu-id="fd03a-125">Members</span></span>

#### <span data-ttu-id="fd03a-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="fd03a-126">get_Content</span></span> 

<span data-ttu-id="fd03a-127">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="fd03a-127">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="fd03a-128">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="fd03a-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="fd03a-129">Post-Daten wären hier.</span><span class="sxs-lookup"><span data-stu-id="fd03a-129">POST data would be here.</span></span> <span data-ttu-id="fd03a-130">Wenn ein Datenstrom festgesetzt wird, der den Nachrichtentext überschreibt, muss der Datenstrom alle Inhaltsdaten aufweisen, bis die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fd03a-130">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="fd03a-131">Stream sollte agil sein oder aus einem background-STA erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="fd03a-131">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="fd03a-132">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="fd03a-132">Null means no content data.</span></span> <span data-ttu-id="fd03a-133">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="fd03a-133">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="fd03a-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="fd03a-134">get_Headers</span></span> 

<span data-ttu-id="fd03a-135">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="fd03a-135">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="fd03a-136">öffentliche HRESULT- [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="fd03a-136">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="fd03a-137">get_Method</span><span class="sxs-lookup"><span data-stu-id="fd03a-137">get_Method</span></span> 

<span data-ttu-id="fd03a-138">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="fd03a-138">The HTTP request method.</span></span>

> <span data-ttu-id="fd03a-139">öffentliche HRESULT- [get_Method](#get_method)(LPWSTR \*-Methode)</span><span class="sxs-lookup"><span data-stu-id="fd03a-139">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="fd03a-140">get_Uri</span><span class="sxs-lookup"><span data-stu-id="fd03a-140">get_Uri</span></span> 

<span data-ttu-id="fd03a-141">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="fd03a-141">The request URI.</span></span>

> <span data-ttu-id="fd03a-142">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="fd03a-142">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="fd03a-143">put_Content</span><span class="sxs-lookup"><span data-stu-id="fd03a-143">put_Content</span></span> 

<span data-ttu-id="fd03a-144">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fd03a-144">Set the Content property.</span></span>

> <span data-ttu-id="fd03a-145">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="fd03a-145">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="fd03a-146">put_Method</span><span class="sxs-lookup"><span data-stu-id="fd03a-146">put_Method</span></span> 

<span data-ttu-id="fd03a-147">Festlegen der Method-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fd03a-147">Set the Method property.</span></span>

> <span data-ttu-id="fd03a-148">Public HRESULT [put_Method](#put_method)(LPCWSTR-Methode)</span><span class="sxs-lookup"><span data-stu-id="fd03a-148">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="fd03a-149">put_Uri</span><span class="sxs-lookup"><span data-stu-id="fd03a-149">put_Uri</span></span> 

<span data-ttu-id="fd03a-150">Die URI-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="fd03a-150">Set the Uri property.</span></span>

> <span data-ttu-id="fd03a-151">öffentliche HRESULT- [put_Uri](#put_uri)(LPCWSTR-URI)</span><span class="sxs-lookup"><span data-stu-id="fd03a-151">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>


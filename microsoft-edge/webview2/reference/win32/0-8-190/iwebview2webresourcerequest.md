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
ms.openlocfilehash: 69bf9eeae4b6736ac6df6ddaa9594b7438cbf58c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653778"
---
# <span data-ttu-id="94b0f-104">Schnittstellen IWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="94b0f-104">interface IWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="94b0f-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="94b0f-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="94b0f-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="94b0f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="94b0f-107">Eine HTTP-Anforderung für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="94b0f-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="94b0f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="94b0f-108">Summary</span></span>

 <span data-ttu-id="94b0f-109">Member</span><span class="sxs-lookup"><span data-stu-id="94b0f-109">Members</span></span>                        | <span data-ttu-id="94b0f-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="94b0f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="94b0f-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="94b0f-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="94b0f-112">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="94b0f-112">The request URI.</span></span>
[<span data-ttu-id="94b0f-113">put_Uri</span><span class="sxs-lookup"><span data-stu-id="94b0f-113">put_Uri</span></span>](#put_uri) | <span data-ttu-id="94b0f-114">Die URI-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="94b0f-114">Set the Uri property.</span></span>
[<span data-ttu-id="94b0f-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="94b0f-115">get_Method</span></span>](#get_method) | <span data-ttu-id="94b0f-116">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="94b0f-116">The HTTP request method.</span></span>
[<span data-ttu-id="94b0f-117">put_Method</span><span class="sxs-lookup"><span data-stu-id="94b0f-117">put_Method</span></span>](#put_method) | <span data-ttu-id="94b0f-118">Festlegen der Method-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="94b0f-118">Set the Method property.</span></span>
[<span data-ttu-id="94b0f-119">get_Content</span><span class="sxs-lookup"><span data-stu-id="94b0f-119">get_Content</span></span>](#get_content) | <span data-ttu-id="94b0f-120">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="94b0f-120">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="94b0f-121">put_Content</span><span class="sxs-lookup"><span data-stu-id="94b0f-121">put_Content</span></span>](#put_content) | <span data-ttu-id="94b0f-122">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="94b0f-122">Set the Content property.</span></span>
[<span data-ttu-id="94b0f-123">get_Headers</span><span class="sxs-lookup"><span data-stu-id="94b0f-123">get_Headers</span></span>](#get_headers) | <span data-ttu-id="94b0f-124">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="94b0f-124">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="94b0f-125">Member</span><span class="sxs-lookup"><span data-stu-id="94b0f-125">Members</span></span>

#### <span data-ttu-id="94b0f-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="94b0f-126">get_Uri</span></span> 

<span data-ttu-id="94b0f-127">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="94b0f-127">The request URI.</span></span>

> <span data-ttu-id="94b0f-128">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="94b0f-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="94b0f-129">put_Uri</span><span class="sxs-lookup"><span data-stu-id="94b0f-129">put_Uri</span></span> 

<span data-ttu-id="94b0f-130">Die URI-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="94b0f-130">Set the Uri property.</span></span>

> <span data-ttu-id="94b0f-131">öffentliche HRESULT- [put_Uri](#put_uri)(LPCWSTR-URI)</span><span class="sxs-lookup"><span data-stu-id="94b0f-131">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="94b0f-132">get_Method</span><span class="sxs-lookup"><span data-stu-id="94b0f-132">get_Method</span></span> 

<span data-ttu-id="94b0f-133">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="94b0f-133">The HTTP request method.</span></span>

> <span data-ttu-id="94b0f-134">öffentliche HRESULT- [get_Method](#get_method)(LPWSTR \*-Methode)</span><span class="sxs-lookup"><span data-stu-id="94b0f-134">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="94b0f-135">put_Method</span><span class="sxs-lookup"><span data-stu-id="94b0f-135">put_Method</span></span> 

<span data-ttu-id="94b0f-136">Festlegen der Method-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="94b0f-136">Set the Method property.</span></span>

> <span data-ttu-id="94b0f-137">Public HRESULT [put_Method](#put_method)(LPCWSTR-Methode)</span><span class="sxs-lookup"><span data-stu-id="94b0f-137">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="94b0f-138">get_Content</span><span class="sxs-lookup"><span data-stu-id="94b0f-138">get_Content</span></span> 

<span data-ttu-id="94b0f-139">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="94b0f-139">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="94b0f-140">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="94b0f-140">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="94b0f-141">Post-Daten wären hier.</span><span class="sxs-lookup"><span data-stu-id="94b0f-141">POST data would be here.</span></span> <span data-ttu-id="94b0f-142">Wenn ein Datenstrom festgesetzt wird, der den Nachrichtentext überschreibt, muss der Datenstrom alle Inhaltsdaten aufweisen, bis die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="94b0f-142">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="94b0f-143">Stream sollte agil sein oder aus einem background-STA erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="94b0f-143">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="94b0f-144">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="94b0f-144">Null means no content data.</span></span> <span data-ttu-id="94b0f-145">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="94b0f-145">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="94b0f-146">put_Content</span><span class="sxs-lookup"><span data-stu-id="94b0f-146">put_Content</span></span> 

<span data-ttu-id="94b0f-147">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="94b0f-147">Set the Content property.</span></span>

> <span data-ttu-id="94b0f-148">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="94b0f-148">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="94b0f-149">get_Headers</span><span class="sxs-lookup"><span data-stu-id="94b0f-149">get_Headers</span></span> 

<span data-ttu-id="94b0f-150">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="94b0f-150">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="94b0f-151">öffentliche HRESULT- [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="94b0f-151">public HRESULT [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* headers)</span></span>


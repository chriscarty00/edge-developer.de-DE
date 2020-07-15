---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 3c9736c8b5a3cfb0de994285f3a1f90d62666fd0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878148"
---
# <span data-ttu-id="33677-104">0.8.355-Interface-IWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="33677-104">0.8.355 - interface IWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="33677-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="33677-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="33677-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="33677-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="33677-107">Eine HTTP-Anforderung für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="33677-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="33677-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="33677-108">Summary</span></span>

 <span data-ttu-id="33677-109">Member</span><span class="sxs-lookup"><span data-stu-id="33677-109">Members</span></span>                        | <span data-ttu-id="33677-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="33677-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="33677-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="33677-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="33677-112">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="33677-112">The request URI.</span></span>
[<span data-ttu-id="33677-113">put_Uri</span><span class="sxs-lookup"><span data-stu-id="33677-113">put_Uri</span></span>](#put_uri) | <span data-ttu-id="33677-114">Die URI-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="33677-114">Set the Uri property.</span></span>
[<span data-ttu-id="33677-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="33677-115">get_Method</span></span>](#get_method) | <span data-ttu-id="33677-116">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="33677-116">The HTTP request method.</span></span>
[<span data-ttu-id="33677-117">put_Method</span><span class="sxs-lookup"><span data-stu-id="33677-117">put_Method</span></span>](#put_method) | <span data-ttu-id="33677-118">Festlegen der Method-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33677-118">Set the Method property.</span></span>
[<span data-ttu-id="33677-119">get_Content</span><span class="sxs-lookup"><span data-stu-id="33677-119">get_Content</span></span>](#get_content) | <span data-ttu-id="33677-120">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="33677-120">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="33677-121">put_Content</span><span class="sxs-lookup"><span data-stu-id="33677-121">put_Content</span></span>](#put_content) | <span data-ttu-id="33677-122">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33677-122">Set the Content property.</span></span>
[<span data-ttu-id="33677-123">get_Headers</span><span class="sxs-lookup"><span data-stu-id="33677-123">get_Headers</span></span>](#get_headers) | <span data-ttu-id="33677-124">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="33677-124">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="33677-125">Member</span><span class="sxs-lookup"><span data-stu-id="33677-125">Members</span></span>

#### <span data-ttu-id="33677-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="33677-126">get_Uri</span></span> 

<span data-ttu-id="33677-127">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="33677-127">The request URI.</span></span>

> <span data-ttu-id="33677-128">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="33677-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="33677-129">put_Uri</span><span class="sxs-lookup"><span data-stu-id="33677-129">put_Uri</span></span> 

<span data-ttu-id="33677-130">Die URI-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="33677-130">Set the Uri property.</span></span>

> <span data-ttu-id="33677-131">öffentliche HRESULT- [put_Uri](#put_uri)(LPCWSTR-URI)</span><span class="sxs-lookup"><span data-stu-id="33677-131">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="33677-132">get_Method</span><span class="sxs-lookup"><span data-stu-id="33677-132">get_Method</span></span> 

<span data-ttu-id="33677-133">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="33677-133">The HTTP request method.</span></span>

> <span data-ttu-id="33677-134">öffentliche HRESULT- [get_Method](#get_method)(LPWSTR \*-Methode)</span><span class="sxs-lookup"><span data-stu-id="33677-134">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="33677-135">put_Method</span><span class="sxs-lookup"><span data-stu-id="33677-135">put_Method</span></span> 

<span data-ttu-id="33677-136">Festlegen der Method-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33677-136">Set the Method property.</span></span>

> <span data-ttu-id="33677-137">Public HRESULT [put_Method](#put_method)(LPCWSTR-Methode)</span><span class="sxs-lookup"><span data-stu-id="33677-137">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="33677-138">get_Content</span><span class="sxs-lookup"><span data-stu-id="33677-138">get_Content</span></span> 

<span data-ttu-id="33677-139">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="33677-139">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="33677-140">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="33677-140">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="33677-141">Post-Daten wären hier.</span><span class="sxs-lookup"><span data-stu-id="33677-141">POST data would be here.</span></span> <span data-ttu-id="33677-142">Wenn ein Datenstrom festgesetzt wird, der den Nachrichtentext überschreibt, muss der Datenstrom alle Inhaltsdaten aufweisen, bis die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="33677-142">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="33677-143">Stream sollte agil sein oder aus einem background-STA erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="33677-143">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="33677-144">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="33677-144">Null means no content data.</span></span> <span data-ttu-id="33677-145">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="33677-145">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="33677-146">put_Content</span><span class="sxs-lookup"><span data-stu-id="33677-146">put_Content</span></span> 

<span data-ttu-id="33677-147">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33677-147">Set the Content property.</span></span>

> <span data-ttu-id="33677-148">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="33677-148">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="33677-149">get_Headers</span><span class="sxs-lookup"><span data-stu-id="33677-149">get_Headers</span></span> 

<span data-ttu-id="33677-150">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="33677-150">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="33677-151">öffentliche HRESULT- [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="33677-151">public HRESULT [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* headers)</span></span>


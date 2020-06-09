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
ms.openlocfilehash: c715a195a52d95e91095e006c71e50de46dc05e4
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698860"
---
# <span data-ttu-id="ae3da-104">Schnittstellen ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="ae3da-104">interface ICoreWebView2WebResourceRequest</span></span> 

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="ae3da-105">Eine HTTP-Anforderung für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ae3da-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="ae3da-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ae3da-106">Summary</span></span>

 <span data-ttu-id="ae3da-107">Member</span><span class="sxs-lookup"><span data-stu-id="ae3da-107">Members</span></span>                        | <span data-ttu-id="ae3da-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ae3da-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ae3da-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="ae3da-109">get_Content</span></span>](#get_content) | <span data-ttu-id="ae3da-110">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="ae3da-110">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="ae3da-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="ae3da-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="ae3da-112">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="ae3da-112">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="ae3da-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="ae3da-113">get_Method</span></span>](#get_method) | <span data-ttu-id="ae3da-114">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="ae3da-114">The HTTP request method.</span></span>
[<span data-ttu-id="ae3da-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ae3da-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="ae3da-116">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="ae3da-116">The request URI.</span></span>
[<span data-ttu-id="ae3da-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="ae3da-117">put_Content</span></span>](#put_content) | <span data-ttu-id="ae3da-118">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ae3da-118">Set the Content property.</span></span>
[<span data-ttu-id="ae3da-119">put_Method</span><span class="sxs-lookup"><span data-stu-id="ae3da-119">put_Method</span></span>](#put_method) | <span data-ttu-id="ae3da-120">Festlegen der Method-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ae3da-120">Set the Method property.</span></span>
[<span data-ttu-id="ae3da-121">put_Uri</span><span class="sxs-lookup"><span data-stu-id="ae3da-121">put_Uri</span></span>](#put_uri) | <span data-ttu-id="ae3da-122">Die URI-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="ae3da-122">Set the Uri property.</span></span>

## <span data-ttu-id="ae3da-123">Member</span><span class="sxs-lookup"><span data-stu-id="ae3da-123">Members</span></span>

#### <span data-ttu-id="ae3da-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="ae3da-124">get_Content</span></span> 

<span data-ttu-id="ae3da-125">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="ae3da-125">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="ae3da-126">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="ae3da-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="ae3da-127">Post-Daten wären hier.</span><span class="sxs-lookup"><span data-stu-id="ae3da-127">POST data would be here.</span></span> <span data-ttu-id="ae3da-128">Wenn ein Datenstrom festgesetzt wird, der den Nachrichtentext überschreibt, muss der Datenstrom alle Inhaltsdaten aufweisen, bis die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ae3da-128">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="ae3da-129">Stream sollte agil sein oder aus einem background-STA erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="ae3da-129">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="ae3da-130">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="ae3da-130">Null means no content data.</span></span> <span data-ttu-id="ae3da-131">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="ae3da-131">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="ae3da-132">get_Headers</span><span class="sxs-lookup"><span data-stu-id="ae3da-132">get_Headers</span></span> 

<span data-ttu-id="ae3da-133">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="ae3da-133">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="ae3da-134">öffentliche HRESULT- [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="ae3da-134">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="ae3da-135">get_Method</span><span class="sxs-lookup"><span data-stu-id="ae3da-135">get_Method</span></span> 

<span data-ttu-id="ae3da-136">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="ae3da-136">The HTTP request method.</span></span>

> <span data-ttu-id="ae3da-137">öffentliche HRESULT- [get_Method](#get_method)(LPWSTR \*-Methode)</span><span class="sxs-lookup"><span data-stu-id="ae3da-137">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="ae3da-138">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ae3da-138">get_Uri</span></span> 

<span data-ttu-id="ae3da-139">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="ae3da-139">The request URI.</span></span>

> <span data-ttu-id="ae3da-140">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="ae3da-140">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="ae3da-141">put_Content</span><span class="sxs-lookup"><span data-stu-id="ae3da-141">put_Content</span></span> 

<span data-ttu-id="ae3da-142">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ae3da-142">Set the Content property.</span></span>

> <span data-ttu-id="ae3da-143">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="ae3da-143">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="ae3da-144">put_Method</span><span class="sxs-lookup"><span data-stu-id="ae3da-144">put_Method</span></span> 

<span data-ttu-id="ae3da-145">Festlegen der Method-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ae3da-145">Set the Method property.</span></span>

> <span data-ttu-id="ae3da-146">Public HRESULT [put_Method](#put_method)(LPCWSTR-Methode)</span><span class="sxs-lookup"><span data-stu-id="ae3da-146">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="ae3da-147">put_Uri</span><span class="sxs-lookup"><span data-stu-id="ae3da-147">put_Uri</span></span> 

<span data-ttu-id="ae3da-148">Die URI-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="ae3da-148">Set the Uri property.</span></span>

> <span data-ttu-id="ae3da-149">öffentliche HRESULT- [put_Uri](#put_uri)(LPCWSTR-URI)</span><span class="sxs-lookup"><span data-stu-id="ae3da-149">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>


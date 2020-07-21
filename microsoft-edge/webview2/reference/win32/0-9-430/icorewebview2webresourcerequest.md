---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ca7063ff1cd527032e9548d22a0346f8d1590480
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885702"
---
# <span data-ttu-id="858b9-104">0.9.430-Interface-ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="858b9-104">0.9.430 - interface ICoreWebView2WebResourceRequest</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="858b9-105">Eine HTTP-Anforderung für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="858b9-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="858b9-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="858b9-106">Summary</span></span>

 <span data-ttu-id="858b9-107">Member</span><span class="sxs-lookup"><span data-stu-id="858b9-107">Members</span></span>                        | <span data-ttu-id="858b9-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="858b9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="858b9-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="858b9-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="858b9-110">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="858b9-110">The request URI.</span></span>
[<span data-ttu-id="858b9-111">put_Uri</span><span class="sxs-lookup"><span data-stu-id="858b9-111">put_Uri</span></span>](#put_uri) | <span data-ttu-id="858b9-112">Die URI-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="858b9-112">Set the Uri property.</span></span>
[<span data-ttu-id="858b9-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="858b9-113">get_Method</span></span>](#get_method) | <span data-ttu-id="858b9-114">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="858b9-114">The HTTP request method.</span></span>
[<span data-ttu-id="858b9-115">put_Method</span><span class="sxs-lookup"><span data-stu-id="858b9-115">put_Method</span></span>](#put_method) | <span data-ttu-id="858b9-116">Festlegen der Method-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="858b9-116">Set the Method property.</span></span>
[<span data-ttu-id="858b9-117">get_Content</span><span class="sxs-lookup"><span data-stu-id="858b9-117">get_Content</span></span>](#get_content) | <span data-ttu-id="858b9-118">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="858b9-118">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="858b9-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="858b9-119">put_Content</span></span>](#put_content) | <span data-ttu-id="858b9-120">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="858b9-120">Set the Content property.</span></span>
[<span data-ttu-id="858b9-121">get_Headers</span><span class="sxs-lookup"><span data-stu-id="858b9-121">get_Headers</span></span>](#get_headers) | <span data-ttu-id="858b9-122">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="858b9-122">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="858b9-123">Member</span><span class="sxs-lookup"><span data-stu-id="858b9-123">Members</span></span>

#### <span data-ttu-id="858b9-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="858b9-124">get_Uri</span></span> 

<span data-ttu-id="858b9-125">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="858b9-125">The request URI.</span></span>

> <span data-ttu-id="858b9-126">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="858b9-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="858b9-127">put_Uri</span><span class="sxs-lookup"><span data-stu-id="858b9-127">put_Uri</span></span> 

<span data-ttu-id="858b9-128">Die URI-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="858b9-128">Set the Uri property.</span></span>

> <span data-ttu-id="858b9-129">öffentliche HRESULT- [put_Uri](#put_uri)(LPCWSTR-URI)</span><span class="sxs-lookup"><span data-stu-id="858b9-129">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="858b9-130">get_Method</span><span class="sxs-lookup"><span data-stu-id="858b9-130">get_Method</span></span> 

<span data-ttu-id="858b9-131">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="858b9-131">The HTTP request method.</span></span>

> <span data-ttu-id="858b9-132">öffentliche HRESULT- [get_Method](#get_method)(LPWSTR \*-Methode)</span><span class="sxs-lookup"><span data-stu-id="858b9-132">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="858b9-133">put_Method</span><span class="sxs-lookup"><span data-stu-id="858b9-133">put_Method</span></span> 

<span data-ttu-id="858b9-134">Festlegen der Method-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="858b9-134">Set the Method property.</span></span>

> <span data-ttu-id="858b9-135">Public HRESULT [put_Method](#put_method)(LPCWSTR-Methode)</span><span class="sxs-lookup"><span data-stu-id="858b9-135">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="858b9-136">get_Content</span><span class="sxs-lookup"><span data-stu-id="858b9-136">get_Content</span></span> 

<span data-ttu-id="858b9-137">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="858b9-137">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="858b9-138">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="858b9-138">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="858b9-139">Post-Daten wären hier.</span><span class="sxs-lookup"><span data-stu-id="858b9-139">POST data would be here.</span></span> <span data-ttu-id="858b9-140">Wenn ein Datenstrom festgesetzt wird, der den Nachrichtentext überschreibt, muss der Datenstrom alle Inhaltsdaten aufweisen, bis die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="858b9-140">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="858b9-141">Stream sollte agil sein oder aus einem background-STA erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="858b9-141">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="858b9-142">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="858b9-142">Null means no content data.</span></span> <span data-ttu-id="858b9-143">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="858b9-143">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="858b9-144">put_Content</span><span class="sxs-lookup"><span data-stu-id="858b9-144">put_Content</span></span> 

<span data-ttu-id="858b9-145">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="858b9-145">Set the Content property.</span></span>

> <span data-ttu-id="858b9-146">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="858b9-146">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="858b9-147">get_Headers</span><span class="sxs-lookup"><span data-stu-id="858b9-147">get_Headers</span></span> 

<span data-ttu-id="858b9-148">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="858b9-148">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="858b9-149">öffentliche HRESULT- [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="858b9-149">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* headers)</span></span>


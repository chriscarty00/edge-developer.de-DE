---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 201b9af4a5838c9537014864c31cd2121f9dfe76
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653741"
---
# <span data-ttu-id="64c11-104">Schnittstellen ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="64c11-104">interface ICoreWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="64c11-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="64c11-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="64c11-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="64c11-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="64c11-107">Eine HTTP-Anforderung für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="64c11-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="64c11-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="64c11-108">Summary</span></span>

 <span data-ttu-id="64c11-109">Member</span><span class="sxs-lookup"><span data-stu-id="64c11-109">Members</span></span>                        | <span data-ttu-id="64c11-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="64c11-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="64c11-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="64c11-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="64c11-112">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="64c11-112">The request URI.</span></span>
[<span data-ttu-id="64c11-113">put_Uri</span><span class="sxs-lookup"><span data-stu-id="64c11-113">put_Uri</span></span>](#put_uri) | <span data-ttu-id="64c11-114">Die URI-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="64c11-114">Set the Uri property.</span></span>
[<span data-ttu-id="64c11-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="64c11-115">get_Method</span></span>](#get_method) | <span data-ttu-id="64c11-116">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="64c11-116">The HTTP request method.</span></span>
[<span data-ttu-id="64c11-117">put_Method</span><span class="sxs-lookup"><span data-stu-id="64c11-117">put_Method</span></span>](#put_method) | <span data-ttu-id="64c11-118">Festlegen der Method-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="64c11-118">Set the Method property.</span></span>
[<span data-ttu-id="64c11-119">get_Content</span><span class="sxs-lookup"><span data-stu-id="64c11-119">get_Content</span></span>](#get_content) | <span data-ttu-id="64c11-120">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="64c11-120">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="64c11-121">put_Content</span><span class="sxs-lookup"><span data-stu-id="64c11-121">put_Content</span></span>](#put_content) | <span data-ttu-id="64c11-122">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="64c11-122">Set the Content property.</span></span>
[<span data-ttu-id="64c11-123">get_Headers</span><span class="sxs-lookup"><span data-stu-id="64c11-123">get_Headers</span></span>](#get_headers) | <span data-ttu-id="64c11-124">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="64c11-124">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="64c11-125">Member</span><span class="sxs-lookup"><span data-stu-id="64c11-125">Members</span></span>

#### <span data-ttu-id="64c11-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="64c11-126">get_Uri</span></span> 

<span data-ttu-id="64c11-127">Der Anforderungs-URI.</span><span class="sxs-lookup"><span data-stu-id="64c11-127">The request URI.</span></span>

> <span data-ttu-id="64c11-128">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="64c11-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="64c11-129">put_Uri</span><span class="sxs-lookup"><span data-stu-id="64c11-129">put_Uri</span></span> 

<span data-ttu-id="64c11-130">Die URI-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="64c11-130">Set the Uri property.</span></span>

> <span data-ttu-id="64c11-131">öffentliche HRESULT- [put_Uri](#put_uri)(LPCWSTR-URI)</span><span class="sxs-lookup"><span data-stu-id="64c11-131">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="64c11-132">get_Method</span><span class="sxs-lookup"><span data-stu-id="64c11-132">get_Method</span></span> 

<span data-ttu-id="64c11-133">Die http-Anforderungsmethode.</span><span class="sxs-lookup"><span data-stu-id="64c11-133">The HTTP request method.</span></span>

> <span data-ttu-id="64c11-134">öffentliche HRESULT- [get_Method](#get_method)(LPWSTR \*-Methode)</span><span class="sxs-lookup"><span data-stu-id="64c11-134">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="64c11-135">put_Method</span><span class="sxs-lookup"><span data-stu-id="64c11-135">put_Method</span></span> 

<span data-ttu-id="64c11-136">Festlegen der Method-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="64c11-136">Set the Method property.</span></span>

> <span data-ttu-id="64c11-137">Public HRESULT [put_Method](#put_method)(LPCWSTR-Methode)</span><span class="sxs-lookup"><span data-stu-id="64c11-137">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="64c11-138">get_Content</span><span class="sxs-lookup"><span data-stu-id="64c11-138">get_Content</span></span> 

<span data-ttu-id="64c11-139">Der HTTP-Request-Nachrichtentext als Stream.</span><span class="sxs-lookup"><span data-stu-id="64c11-139">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="64c11-140">öffentliche HRESULT- [get_Content](#get_content)(IStream \* \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="64c11-140">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="64c11-141">Post-Daten wären hier.</span><span class="sxs-lookup"><span data-stu-id="64c11-141">POST data would be here.</span></span> <span data-ttu-id="64c11-142">Wenn ein Datenstrom festgesetzt wird, der den Nachrichtentext überschreibt, muss der Datenstrom alle Inhaltsdaten aufweisen, bis die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="64c11-142">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="64c11-143">Stream sollte agil sein oder aus einem background-STA erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="64c11-143">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="64c11-144">NULL bedeutet keine Inhaltsdaten.</span><span class="sxs-lookup"><span data-stu-id="64c11-144">Null means no content data.</span></span> <span data-ttu-id="64c11-145">Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)</span><span class="sxs-lookup"><span data-stu-id="64c11-145">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="64c11-146">put_Content</span><span class="sxs-lookup"><span data-stu-id="64c11-146">put_Content</span></span> 

<span data-ttu-id="64c11-147">Festlegen der Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="64c11-147">Set the Content property.</span></span>

> <span data-ttu-id="64c11-148">öffentliche HRESULT- [put_Content](#put_content)(IStream \*-Inhalt)</span><span class="sxs-lookup"><span data-stu-id="64c11-148">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="64c11-149">get_Headers</span><span class="sxs-lookup"><span data-stu-id="64c11-149">get_Headers</span></span> 

<span data-ttu-id="64c11-150">Die änderbaren HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="64c11-150">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="64c11-151">öffentliche HRESULT- [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \*-Header)</span><span class="sxs-lookup"><span data-stu-id="64c11-151">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* headers)</span></span>


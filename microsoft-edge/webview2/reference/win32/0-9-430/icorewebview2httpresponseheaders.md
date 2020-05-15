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
ms.openlocfilehash: b23b724977b9d164c48dc99d0da2e64d61539549
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654067"
---
# <span data-ttu-id="a15d5-104">Schnittstellen ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="a15d5-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="a15d5-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="a15d5-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="a15d5-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="a15d5-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="a15d5-107">HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="a15d5-107">HTTP response headers.</span></span>

## <span data-ttu-id="a15d5-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a15d5-108">Summary</span></span>

 <span data-ttu-id="a15d5-109">Member</span><span class="sxs-lookup"><span data-stu-id="a15d5-109">Members</span></span>                        | <span data-ttu-id="a15d5-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a15d5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a15d5-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="a15d5-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="a15d5-112">Fügt Headerzeile mit Name und Wert an.</span><span class="sxs-lookup"><span data-stu-id="a15d5-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="a15d5-113">Contains</span><span class="sxs-lookup"><span data-stu-id="a15d5-113">Contains</span></span>](#contains) | <span data-ttu-id="a15d5-114">Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a15d5-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="a15d5-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="a15d5-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="a15d5-116">Ruft den ersten Headerwert in der Sammlung ab, die mit dem Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a15d5-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="a15d5-117">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="a15d5-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="a15d5-118">Ruft die Überschriften Werte ab, die dem Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a15d5-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="a15d5-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="a15d5-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="a15d5-120">Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="a15d5-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="a15d5-121">Wird zum Erstellen eines WebResourceResponse für das WebResourceRequested-Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="a15d5-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="a15d5-122">Member</span><span class="sxs-lookup"><span data-stu-id="a15d5-122">Members</span></span>

#### <span data-ttu-id="a15d5-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="a15d5-123">AppendHeader</span></span> 

<span data-ttu-id="a15d5-124">Fügt Headerzeile mit Name und Wert an.</span><span class="sxs-lookup"><span data-stu-id="a15d5-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="a15d5-125">Public HRESULT [Appendheader](#appendheader)(LPCWSTR-Name; LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="a15d5-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="a15d5-126">Contains</span><span class="sxs-lookup"><span data-stu-id="a15d5-126">Contains</span></span> 

<span data-ttu-id="a15d5-127">Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a15d5-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="a15d5-128">Public HRESULT [Contains](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="a15d5-128">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="a15d5-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="a15d5-129">GetHeader</span></span> 

<span data-ttu-id="a15d5-130">Ruft den ersten Headerwert in der Sammlung ab, die mit dem Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a15d5-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="a15d5-131">Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="a15d5-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="a15d5-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="a15d5-132">GetHeaders</span></span> 

<span data-ttu-id="a15d5-133">Ruft die Überschriften Werte ab, die dem Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a15d5-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="a15d5-134">öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="a15d5-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="a15d5-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="a15d5-135">GetIterator</span></span> 

<span data-ttu-id="a15d5-136">Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="a15d5-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="a15d5-137">öffentlicher HRESULT- [getIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="a15d5-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


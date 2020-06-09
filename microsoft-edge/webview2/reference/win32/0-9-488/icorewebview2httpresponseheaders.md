---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 63044cae80aebfb1e759070ec797673b0c9378d2
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697252"
---
# <span data-ttu-id="cdd9a-104">Schnittstellen ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="cdd9a-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="cdd9a-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="cdd9a-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="cdd9a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="cdd9a-107">HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-107">HTTP response headers.</span></span>

## <span data-ttu-id="cdd9a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="cdd9a-108">Summary</span></span>

 <span data-ttu-id="cdd9a-109">Member</span><span class="sxs-lookup"><span data-stu-id="cdd9a-109">Members</span></span>                        | <span data-ttu-id="cdd9a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="cdd9a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cdd9a-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="cdd9a-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="cdd9a-112">Fügt Headerzeile mit Name und Wert an.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="cdd9a-113">Contains</span><span class="sxs-lookup"><span data-stu-id="cdd9a-113">Contains</span></span>](#contains) | <span data-ttu-id="cdd9a-114">Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="cdd9a-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="cdd9a-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="cdd9a-116">Ruft den ersten Headerwert in der Sammlung ab, die mit dem Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="cdd9a-117">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="cdd9a-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="cdd9a-118">Ruft die Überschriften Werte ab, die dem Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="cdd9a-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="cdd9a-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="cdd9a-120">Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="cdd9a-121">Wird zum Erstellen eines WebResourceResponse für das WebResourceRequested-Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="cdd9a-122">Member</span><span class="sxs-lookup"><span data-stu-id="cdd9a-122">Members</span></span>

#### <span data-ttu-id="cdd9a-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="cdd9a-123">AppendHeader</span></span> 

<span data-ttu-id="cdd9a-124">Fügt Headerzeile mit Name und Wert an.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="cdd9a-125">Public HRESULT [Appendheader](#appendheader)(LPCWSTR-Name; LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="cdd9a-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="cdd9a-126">Contains</span><span class="sxs-lookup"><span data-stu-id="cdd9a-126">Contains</span></span> 

<span data-ttu-id="cdd9a-127">Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="cdd9a-128">Public HRESULT [Contains](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="cdd9a-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="cdd9a-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="cdd9a-129">GetHeader</span></span> 

<span data-ttu-id="cdd9a-130">Ruft den ersten Headerwert in der Sammlung ab, die mit dem Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="cdd9a-131">Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="cdd9a-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="cdd9a-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="cdd9a-132">GetHeaders</span></span> 

<span data-ttu-id="cdd9a-133">Ruft die Überschriften Werte ab, die dem Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="cdd9a-134">öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="cdd9a-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="cdd9a-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="cdd9a-135">GetIterator</span></span> 

<span data-ttu-id="cdd9a-136">Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="cdd9a-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="cdd9a-137">öffentlicher HRESULT- [getIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="cdd9a-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>


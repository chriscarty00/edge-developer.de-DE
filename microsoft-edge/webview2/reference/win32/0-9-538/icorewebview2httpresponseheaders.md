---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2HttpResponseHeaders
ms.openlocfilehash: 359e79b2ecfd92ee0b7dc608a5ae5748ff6f20ce
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878743"
---
# <span data-ttu-id="8cdce-104">Schnittstellen ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="8cdce-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="8cdce-105">HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="8cdce-105">HTTP response headers.</span></span>

## <span data-ttu-id="8cdce-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8cdce-106">Summary</span></span>

 <span data-ttu-id="8cdce-107">Member</span><span class="sxs-lookup"><span data-stu-id="8cdce-107">Members</span></span>                        | <span data-ttu-id="8cdce-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8cdce-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8cdce-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="8cdce-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="8cdce-110">Fügt Headerzeile mit Name und Wert an.</span><span class="sxs-lookup"><span data-stu-id="8cdce-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="8cdce-111">Contains</span><span class="sxs-lookup"><span data-stu-id="8cdce-111">Contains</span></span>](#contains) | <span data-ttu-id="8cdce-112">Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8cdce-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="8cdce-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="8cdce-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="8cdce-114">Ruft den ersten Headerwert in der Sammlung ab, die mit dem Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8cdce-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="8cdce-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="8cdce-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="8cdce-116">Ruft die Überschriften Werte ab, die dem Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8cdce-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="8cdce-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="8cdce-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="8cdce-118">Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="8cdce-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="8cdce-119">Wird zum Erstellen eines WebResourceResponse für das WebResourceRequested-Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="8cdce-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="8cdce-120">Member</span><span class="sxs-lookup"><span data-stu-id="8cdce-120">Members</span></span>

#### <span data-ttu-id="8cdce-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="8cdce-121">AppendHeader</span></span> 

<span data-ttu-id="8cdce-122">Fügt Headerzeile mit Name und Wert an.</span><span class="sxs-lookup"><span data-stu-id="8cdce-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="8cdce-123">Public HRESULT [Appendheader](#appendheader)(LPCWSTR-Name; LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="8cdce-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="8cdce-124">Contains</span><span class="sxs-lookup"><span data-stu-id="8cdce-124">Contains</span></span> 

<span data-ttu-id="8cdce-125">Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8cdce-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="8cdce-126">Public HRESULT [Contains](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="8cdce-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="8cdce-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="8cdce-127">GetHeader</span></span> 

<span data-ttu-id="8cdce-128">Ruft den ersten Headerwert in der Sammlung ab, die mit dem Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8cdce-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="8cdce-129">Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="8cdce-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="8cdce-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="8cdce-130">GetHeaders</span></span> 

<span data-ttu-id="8cdce-131">Ruft die Überschriften Werte ab, die dem Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8cdce-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="8cdce-132">öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="8cdce-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="8cdce-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="8cdce-133">GetIterator</span></span> 

<span data-ttu-id="8cdce-134">Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="8cdce-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="8cdce-135">öffentlicher HRESULT- [getIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="8cdce-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>


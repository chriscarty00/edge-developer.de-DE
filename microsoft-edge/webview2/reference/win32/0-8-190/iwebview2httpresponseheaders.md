---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 48a04ea60dff4cf9b6b52377927ee9085fb8bea2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878435"
---
# <span data-ttu-id="bc171-104">0.8.355-Interface-IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="bc171-104">0.8.355 - interface IWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="bc171-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="bc171-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="bc171-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="bc171-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="bc171-107">HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="bc171-107">HTTP response headers.</span></span>

## <span data-ttu-id="bc171-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bc171-108">Summary</span></span>

 <span data-ttu-id="bc171-109">Member</span><span class="sxs-lookup"><span data-stu-id="bc171-109">Members</span></span>                        | <span data-ttu-id="bc171-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="bc171-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bc171-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="bc171-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="bc171-112">Fügt Headerzeile mit Name und Wert an.</span><span class="sxs-lookup"><span data-stu-id="bc171-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="bc171-113">Contains</span><span class="sxs-lookup"><span data-stu-id="bc171-113">Contains</span></span>](#contains) | <span data-ttu-id="bc171-114">Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bc171-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="bc171-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="bc171-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="bc171-116">Ruft die Überschriften Werte ab, die dem Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bc171-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="bc171-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="bc171-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="bc171-118">Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="bc171-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="bc171-119">Wird zum Erstellen eines WebResourceResponse für das WebResourceRequested-Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc171-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="bc171-120">Member</span><span class="sxs-lookup"><span data-stu-id="bc171-120">Members</span></span>

#### <span data-ttu-id="bc171-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="bc171-121">AppendHeader</span></span> 

<span data-ttu-id="bc171-122">Fügt Headerzeile mit Name und Wert an.</span><span class="sxs-lookup"><span data-stu-id="bc171-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="bc171-123">Public HRESULT [Appendheader](#appendheader)(LPCWSTR-Name; LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="bc171-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="bc171-124">Contains</span><span class="sxs-lookup"><span data-stu-id="bc171-124">Contains</span></span> 

<span data-ttu-id="bc171-125">Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bc171-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="bc171-126">Public HRESULT [Contains](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="bc171-126">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="bc171-127">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="bc171-127">GetHeaders</span></span> 

<span data-ttu-id="bc171-128">Ruft die Überschriften Werte ab, die dem Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bc171-128">Gets the header values matching the name.</span></span>

> <span data-ttu-id="bc171-129">öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="bc171-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="bc171-130">GetIterator</span><span class="sxs-lookup"><span data-stu-id="bc171-130">GetIterator</span></span> 

<span data-ttu-id="bc171-131">Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="bc171-131">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="bc171-132">öffentlicher HRESULT- [getIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="bc171-132">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


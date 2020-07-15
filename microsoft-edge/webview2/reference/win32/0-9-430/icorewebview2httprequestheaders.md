---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a67c5c267178ea873cd12d8a22dea7409b260d52
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880997"
---
# <span data-ttu-id="3194a-104">0.9.430-Interface-ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="3194a-104">0.9.430 - interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="3194a-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="3194a-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="3194a-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="3194a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="3194a-107">HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="3194a-107">HTTP request headers.</span></span>

## <span data-ttu-id="3194a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3194a-108">Summary</span></span>

 <span data-ttu-id="3194a-109">Member</span><span class="sxs-lookup"><span data-stu-id="3194a-109">Members</span></span>                        | <span data-ttu-id="3194a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3194a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3194a-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="3194a-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="3194a-112">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="3194a-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="3194a-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="3194a-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="3194a-114">Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.</span><span class="sxs-lookup"><span data-stu-id="3194a-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="3194a-115">Contains</span><span class="sxs-lookup"><span data-stu-id="3194a-115">Contains</span></span>](#contains) | <span data-ttu-id="3194a-116">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="3194a-116">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="3194a-117">SetHeader</span><span class="sxs-lookup"><span data-stu-id="3194a-117">SetHeader</span></span>](#setheader) | <span data-ttu-id="3194a-118">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="3194a-118">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="3194a-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="3194a-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="3194a-120">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="3194a-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="3194a-121">GetIterator</span><span class="sxs-lookup"><span data-stu-id="3194a-121">GetIterator</span></span>](#getiterator) | <span data-ttu-id="3194a-122">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="3194a-122">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="3194a-123">Wird verwendet, um die HTTP-Anforderung für das WebResourceRequested-Ereignis und das NavigationStarting-Ereignis zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3194a-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="3194a-124">Beachten Sie, dass Sie die HTTP-Anforderungs Kopfzeilen aus einem WebResourceRequested-Ereignis, aber nicht aus einem NavigationStarting-Ereignis ändern können.</span><span class="sxs-lookup"><span data-stu-id="3194a-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="3194a-125">Member</span><span class="sxs-lookup"><span data-stu-id="3194a-125">Members</span></span>

#### <span data-ttu-id="3194a-126">GetHeader</span><span class="sxs-lookup"><span data-stu-id="3194a-126">GetHeader</span></span> 

<span data-ttu-id="3194a-127">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="3194a-127">Gets the header value matching the name.</span></span>

> <span data-ttu-id="3194a-128">Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="3194a-128">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="3194a-129">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="3194a-129">GetHeaders</span></span> 

<span data-ttu-id="3194a-130">Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.</span><span class="sxs-lookup"><span data-stu-id="3194a-130">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="3194a-131">öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="3194a-131">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="3194a-132">Contains</span><span class="sxs-lookup"><span data-stu-id="3194a-132">Contains</span></span> 

<span data-ttu-id="3194a-133">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="3194a-133">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="3194a-134">Public HRESULT [Contains](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="3194a-134">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="3194a-135">SetHeader</span><span class="sxs-lookup"><span data-stu-id="3194a-135">SetHeader</span></span> 

<span data-ttu-id="3194a-136">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="3194a-136">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="3194a-137">Public HRESULT [setHeader](#setheader)(LPCWSTR-Name, LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="3194a-137">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="3194a-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="3194a-138">RemoveHeader</span></span> 

<span data-ttu-id="3194a-139">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="3194a-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="3194a-140">Public HRESULT [RemoveHeader](#removeheader)(LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="3194a-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="3194a-141">GetIterator</span><span class="sxs-lookup"><span data-stu-id="3194a-141">GetIterator</span></span> 

<span data-ttu-id="3194a-142">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="3194a-142">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="3194a-143">öffentlicher HRESULT- [getIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="3194a-143">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


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
ms.openlocfilehash: e12809d1db7e8c7764ad75e9a10f44ac3f445fa4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653865"
---
# <span data-ttu-id="33aa4-104">Schnittstellen ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="33aa4-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="33aa4-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="33aa4-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="33aa4-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="33aa4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="33aa4-107">HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="33aa4-107">HTTP request headers.</span></span>

## <span data-ttu-id="33aa4-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="33aa4-108">Summary</span></span>

 <span data-ttu-id="33aa4-109">Member</span><span class="sxs-lookup"><span data-stu-id="33aa4-109">Members</span></span>                        | <span data-ttu-id="33aa4-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="33aa4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="33aa4-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="33aa4-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="33aa4-112">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="33aa4-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="33aa4-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="33aa4-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="33aa4-114">Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.</span><span class="sxs-lookup"><span data-stu-id="33aa4-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="33aa4-115">Contains</span><span class="sxs-lookup"><span data-stu-id="33aa4-115">Contains</span></span>](#contains) | <span data-ttu-id="33aa4-116">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="33aa4-116">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="33aa4-117">SetHeader</span><span class="sxs-lookup"><span data-stu-id="33aa4-117">SetHeader</span></span>](#setheader) | <span data-ttu-id="33aa4-118">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="33aa4-118">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="33aa4-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="33aa4-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="33aa4-120">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="33aa4-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="33aa4-121">GetIterator</span><span class="sxs-lookup"><span data-stu-id="33aa4-121">GetIterator</span></span>](#getiterator) | <span data-ttu-id="33aa4-122">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="33aa4-122">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="33aa4-123">Wird verwendet, um die HTTP-Anforderung für das WebResourceRequested-Ereignis und das NavigationStarting-Ereignis zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="33aa4-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="33aa4-124">Beachten Sie, dass Sie die HTTP-Anforderungs Kopfzeilen aus einem WebResourceRequested-Ereignis, aber nicht aus einem NavigationStarting-Ereignis ändern können.</span><span class="sxs-lookup"><span data-stu-id="33aa4-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="33aa4-125">Member</span><span class="sxs-lookup"><span data-stu-id="33aa4-125">Members</span></span>

#### <span data-ttu-id="33aa4-126">GetHeader</span><span class="sxs-lookup"><span data-stu-id="33aa4-126">GetHeader</span></span> 

<span data-ttu-id="33aa4-127">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="33aa4-127">Gets the header value matching the name.</span></span>

> <span data-ttu-id="33aa4-128">Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="33aa4-128">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="33aa4-129">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="33aa4-129">GetHeaders</span></span> 

<span data-ttu-id="33aa4-130">Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.</span><span class="sxs-lookup"><span data-stu-id="33aa4-130">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="33aa4-131">öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="33aa4-131">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="33aa4-132">Contains</span><span class="sxs-lookup"><span data-stu-id="33aa4-132">Contains</span></span> 

<span data-ttu-id="33aa4-133">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="33aa4-133">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="33aa4-134">Public HRESULT [Contains](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="33aa4-134">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="33aa4-135">SetHeader</span><span class="sxs-lookup"><span data-stu-id="33aa4-135">SetHeader</span></span> 

<span data-ttu-id="33aa4-136">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="33aa4-136">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="33aa4-137">Public HRESULT [setHeader](#setheader)(LPCWSTR-Name, LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="33aa4-137">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="33aa4-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="33aa4-138">RemoveHeader</span></span> 

<span data-ttu-id="33aa4-139">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="33aa4-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="33aa4-140">Public HRESULT [RemoveHeader](#removeheader)(LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="33aa4-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="33aa4-141">GetIterator</span><span class="sxs-lookup"><span data-stu-id="33aa4-141">GetIterator</span></span> 

<span data-ttu-id="33aa4-142">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="33aa4-142">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="33aa4-143">öffentlicher HRESULT- [getIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="33aa4-143">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


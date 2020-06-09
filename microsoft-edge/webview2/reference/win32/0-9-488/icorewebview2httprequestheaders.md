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
ms.openlocfilehash: effceb6fafb062b1747f39876b8d2a5e02721aa8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697273"
---
# <span data-ttu-id="6ddb8-104">Schnittstellen ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="6ddb8-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="6ddb8-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="6ddb8-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="6ddb8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="6ddb8-107">HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-107">HTTP request headers.</span></span>

## <span data-ttu-id="6ddb8-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6ddb8-108">Summary</span></span>

 <span data-ttu-id="6ddb8-109">Member</span><span class="sxs-lookup"><span data-stu-id="6ddb8-109">Members</span></span>                        | <span data-ttu-id="6ddb8-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6ddb8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6ddb8-111">Contains</span><span class="sxs-lookup"><span data-stu-id="6ddb8-111">Contains</span></span>](#contains) | <span data-ttu-id="6ddb8-112">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="6ddb8-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="6ddb8-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="6ddb8-114">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="6ddb8-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="6ddb8-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="6ddb8-116">Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="6ddb8-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="6ddb8-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="6ddb8-118">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="6ddb8-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="6ddb8-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="6ddb8-120">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="6ddb8-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="6ddb8-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="6ddb8-122">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="6ddb8-123">Wird verwendet, um die HTTP-Anforderung für das WebResourceRequested-Ereignis und das NavigationStarting-Ereignis zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="6ddb8-124">Beachten Sie, dass Sie die HTTP-Anforderungs Kopfzeilen aus einem WebResourceRequested-Ereignis, aber nicht aus einem NavigationStarting-Ereignis ändern können.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="6ddb8-125">Member</span><span class="sxs-lookup"><span data-stu-id="6ddb8-125">Members</span></span>

#### <span data-ttu-id="6ddb8-126">Contains</span><span class="sxs-lookup"><span data-stu-id="6ddb8-126">Contains</span></span> 

<span data-ttu-id="6ddb8-127">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="6ddb8-128">Public HRESULT [Contains](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="6ddb8-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="6ddb8-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="6ddb8-129">GetHeader</span></span> 

<span data-ttu-id="6ddb8-130">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="6ddb8-131">Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="6ddb8-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="6ddb8-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="6ddb8-132">GetHeaders</span></span> 

<span data-ttu-id="6ddb8-133">Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="6ddb8-134">öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="6ddb8-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="6ddb8-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="6ddb8-135">GetIterator</span></span> 

<span data-ttu-id="6ddb8-136">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="6ddb8-137">öffentlicher HRESULT- [getIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="6ddb8-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="6ddb8-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="6ddb8-138">RemoveHeader</span></span> 

<span data-ttu-id="6ddb8-139">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="6ddb8-140">Public HRESULT [RemoveHeader](#removeheader)(LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="6ddb8-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="6ddb8-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="6ddb8-141">SetHeader</span></span> 

<span data-ttu-id="6ddb8-142">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6ddb8-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="6ddb8-143">Public HRESULT [setHeader](#setheader)(LPCWSTR-Name, LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="6ddb8-143">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>


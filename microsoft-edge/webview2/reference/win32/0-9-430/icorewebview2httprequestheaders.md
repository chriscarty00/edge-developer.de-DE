---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 04a8bf376ad7649021c4ab1555c3090cce5b52fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885611"
---
# <span data-ttu-id="b198f-104">0.9.430-Interface-ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="b198f-104">0.9.430 - interface ICoreWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="b198f-105">HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="b198f-105">HTTP request headers.</span></span>

## <span data-ttu-id="b198f-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b198f-106">Summary</span></span>

 <span data-ttu-id="b198f-107">Member</span><span class="sxs-lookup"><span data-stu-id="b198f-107">Members</span></span>                        | <span data-ttu-id="b198f-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b198f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b198f-109">GetHeader</span><span class="sxs-lookup"><span data-stu-id="b198f-109">GetHeader</span></span>](#getheader) | <span data-ttu-id="b198f-110">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b198f-110">Gets the header value matching the name.</span></span>
[<span data-ttu-id="b198f-111">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="b198f-111">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="b198f-112">Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.</span><span class="sxs-lookup"><span data-stu-id="b198f-112">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="b198f-113">Contains</span><span class="sxs-lookup"><span data-stu-id="b198f-113">Contains</span></span>](#contains) | <span data-ttu-id="b198f-114">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b198f-114">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="b198f-115">SetHeader</span><span class="sxs-lookup"><span data-stu-id="b198f-115">SetHeader</span></span>](#setheader) | <span data-ttu-id="b198f-116">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b198f-116">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="b198f-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="b198f-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="b198f-118">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b198f-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="b198f-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="b198f-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="b198f-120">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="b198f-120">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="b198f-121">Wird verwendet, um die HTTP-Anforderung für das WebResourceRequested-Ereignis und das NavigationStarting-Ereignis zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b198f-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="b198f-122">Beachten Sie, dass Sie die HTTP-Anforderungs Kopfzeilen aus einem WebResourceRequested-Ereignis, aber nicht aus einem NavigationStarting-Ereignis ändern können.</span><span class="sxs-lookup"><span data-stu-id="b198f-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="b198f-123">Member</span><span class="sxs-lookup"><span data-stu-id="b198f-123">Members</span></span>

#### <span data-ttu-id="b198f-124">GetHeader</span><span class="sxs-lookup"><span data-stu-id="b198f-124">GetHeader</span></span> 

<span data-ttu-id="b198f-125">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b198f-125">Gets the header value matching the name.</span></span>

> <span data-ttu-id="b198f-126">Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="b198f-126">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="b198f-127">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="b198f-127">GetHeaders</span></span> 

<span data-ttu-id="b198f-128">Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.</span><span class="sxs-lookup"><span data-stu-id="b198f-128">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="b198f-129">öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="b198f-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="b198f-130">Contains</span><span class="sxs-lookup"><span data-stu-id="b198f-130">Contains</span></span> 

<span data-ttu-id="b198f-131">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b198f-131">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="b198f-132">Public HRESULT [Contains](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="b198f-132">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="b198f-133">SetHeader</span><span class="sxs-lookup"><span data-stu-id="b198f-133">SetHeader</span></span> 

<span data-ttu-id="b198f-134">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b198f-134">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="b198f-135">Public HRESULT [setHeader](#setheader)(LPCWSTR-Name, LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="b198f-135">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="b198f-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="b198f-136">RemoveHeader</span></span> 

<span data-ttu-id="b198f-137">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b198f-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="b198f-138">Public HRESULT [RemoveHeader](#removeheader)(LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="b198f-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="b198f-139">GetIterator</span><span class="sxs-lookup"><span data-stu-id="b198f-139">GetIterator</span></span> 

<span data-ttu-id="b198f-140">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="b198f-140">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="b198f-141">öffentlicher HRESULT- [getIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="b198f-141">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


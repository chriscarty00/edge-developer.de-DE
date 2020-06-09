---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 19018ff63b62b0d76bed6dcce9cf1dbce2a37b11
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698813"
---
# <span data-ttu-id="4eb68-104">Schnittstellen ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="4eb68-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="4eb68-105">HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="4eb68-105">HTTP request headers.</span></span>

## <span data-ttu-id="4eb68-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4eb68-106">Summary</span></span>

 <span data-ttu-id="4eb68-107">Member</span><span class="sxs-lookup"><span data-stu-id="4eb68-107">Members</span></span>                        | <span data-ttu-id="4eb68-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4eb68-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4eb68-109">Contains</span><span class="sxs-lookup"><span data-stu-id="4eb68-109">Contains</span></span>](#contains) | <span data-ttu-id="4eb68-110">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="4eb68-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="4eb68-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="4eb68-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="4eb68-112">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="4eb68-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="4eb68-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="4eb68-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="4eb68-114">Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.</span><span class="sxs-lookup"><span data-stu-id="4eb68-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="4eb68-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="4eb68-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="4eb68-116">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="4eb68-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="4eb68-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="4eb68-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="4eb68-118">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="4eb68-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="4eb68-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="4eb68-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="4eb68-120">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="4eb68-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="4eb68-121">Wird verwendet, um die HTTP-Anforderung für das WebResourceRequested-Ereignis und das NavigationStarting-Ereignis zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4eb68-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="4eb68-122">Beachten Sie, dass Sie die HTTP-Anforderungs Kopfzeilen aus einem WebResourceRequested-Ereignis, aber nicht aus einem NavigationStarting-Ereignis ändern können.</span><span class="sxs-lookup"><span data-stu-id="4eb68-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="4eb68-123">Member</span><span class="sxs-lookup"><span data-stu-id="4eb68-123">Members</span></span>

#### <span data-ttu-id="4eb68-124">Contains</span><span class="sxs-lookup"><span data-stu-id="4eb68-124">Contains</span></span> 

<span data-ttu-id="4eb68-125">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="4eb68-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="4eb68-126">Public HRESULT [Contains](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="4eb68-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="4eb68-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="4eb68-127">GetHeader</span></span> 

<span data-ttu-id="4eb68-128">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="4eb68-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="4eb68-129">Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="4eb68-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="4eb68-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="4eb68-130">GetHeaders</span></span> 

<span data-ttu-id="4eb68-131">Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.</span><span class="sxs-lookup"><span data-stu-id="4eb68-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="4eb68-132">öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="4eb68-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="4eb68-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="4eb68-133">GetIterator</span></span> 

<span data-ttu-id="4eb68-134">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="4eb68-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="4eb68-135">öffentlicher HRESULT- [getIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="4eb68-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="4eb68-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="4eb68-136">RemoveHeader</span></span> 

<span data-ttu-id="4eb68-137">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="4eb68-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="4eb68-138">Public HRESULT [RemoveHeader](#removeheader)(LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="4eb68-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="4eb68-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="4eb68-139">SetHeader</span></span> 

<span data-ttu-id="4eb68-140">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="4eb68-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="4eb68-141">Public HRESULT [setHeader](#setheader)(LPCWSTR-Name, LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="4eb68-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>


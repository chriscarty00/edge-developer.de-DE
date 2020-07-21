---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 1e0148c0d1e27cb4f1c52fb6ad55cc2e7613a94b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885968"
---
# <span data-ttu-id="14514-104">0.8.355-Interface-IWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="14514-104">0.8.355 - interface IWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="14514-105">HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="14514-105">HTTP request headers.</span></span>

## <span data-ttu-id="14514-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="14514-106">Summary</span></span>

 <span data-ttu-id="14514-107">Member</span><span class="sxs-lookup"><span data-stu-id="14514-107">Members</span></span>                        | <span data-ttu-id="14514-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="14514-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="14514-109">GetHeader</span><span class="sxs-lookup"><span data-stu-id="14514-109">GetHeader</span></span>](#getheader) | <span data-ttu-id="14514-110">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="14514-110">Gets the header value matching the name.</span></span>
[<span data-ttu-id="14514-111">Contains</span><span class="sxs-lookup"><span data-stu-id="14514-111">Contains</span></span>](#contains) | <span data-ttu-id="14514-112">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="14514-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="14514-113">SetHeader</span><span class="sxs-lookup"><span data-stu-id="14514-113">SetHeader</span></span>](#setheader) | <span data-ttu-id="14514-114">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="14514-114">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="14514-115">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="14514-115">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="14514-116">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="14514-116">Removes header that matches the name.</span></span>
[<span data-ttu-id="14514-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="14514-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="14514-118">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="14514-118">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="14514-119">Wird verwendet, um die HTTP-Anforderung für das WebResourceRequested-Ereignis und das NavigationStarting-Ereignis zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="14514-119">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="14514-120">Beachten Sie, dass Sie die HTTP-Anforderungs Kopfzeilen aus einem WebResourceRequested-Ereignis, aber nicht aus einem NavigationStarting-Ereignis ändern können.</span><span class="sxs-lookup"><span data-stu-id="14514-120">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="14514-121">Member</span><span class="sxs-lookup"><span data-stu-id="14514-121">Members</span></span>

#### <span data-ttu-id="14514-122">GetHeader</span><span class="sxs-lookup"><span data-stu-id="14514-122">GetHeader</span></span> 

<span data-ttu-id="14514-123">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="14514-123">Gets the header value matching the name.</span></span>

> <span data-ttu-id="14514-124">Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="14514-124">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="14514-125">Contains</span><span class="sxs-lookup"><span data-stu-id="14514-125">Contains</span></span> 

<span data-ttu-id="14514-126">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="14514-126">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="14514-127">Public HRESULT [Contains](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="14514-127">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="14514-128">SetHeader</span><span class="sxs-lookup"><span data-stu-id="14514-128">SetHeader</span></span> 

<span data-ttu-id="14514-129">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="14514-129">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="14514-130">Public HRESULT [setHeader](#setheader)(LPCWSTR-Name, LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="14514-130">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="14514-131">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="14514-131">RemoveHeader</span></span> 

<span data-ttu-id="14514-132">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="14514-132">Removes header that matches the name.</span></span>

> <span data-ttu-id="14514-133">Public HRESULT [RemoveHeader](#removeheader)(LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="14514-133">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="14514-134">GetIterator</span><span class="sxs-lookup"><span data-stu-id="14514-134">GetIterator</span></span> 

<span data-ttu-id="14514-135">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="14514-135">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="14514-136">öffentlicher HRESULT- [getIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="14514-136">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


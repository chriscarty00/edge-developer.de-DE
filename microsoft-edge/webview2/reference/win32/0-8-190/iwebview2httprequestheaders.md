---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: aea00f37f28034e1b7a33d4fd11c5ed78f779d00
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654000"
---
# <span data-ttu-id="5b0bf-104">Schnittstellen IWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="5b0bf-104">interface IWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="5b0bf-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="5b0bf-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="5b0bf-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="5b0bf-107">HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-107">HTTP request headers.</span></span>

## <span data-ttu-id="5b0bf-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5b0bf-108">Summary</span></span>

 <span data-ttu-id="5b0bf-109">Member</span><span class="sxs-lookup"><span data-stu-id="5b0bf-109">Members</span></span>                        | <span data-ttu-id="5b0bf-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5b0bf-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5b0bf-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="5b0bf-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="5b0bf-112">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="5b0bf-113">Contains</span><span class="sxs-lookup"><span data-stu-id="5b0bf-113">Contains</span></span>](#contains) | <span data-ttu-id="5b0bf-114">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-114">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="5b0bf-115">SetHeader</span><span class="sxs-lookup"><span data-stu-id="5b0bf-115">SetHeader</span></span>](#setheader) | <span data-ttu-id="5b0bf-116">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-116">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="5b0bf-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="5b0bf-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="5b0bf-118">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="5b0bf-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="5b0bf-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="5b0bf-120">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-120">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="5b0bf-121">Wird verwendet, um die HTTP-Anforderung für das WebResourceRequested-Ereignis und das NavigationStarting-Ereignis zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="5b0bf-122">Beachten Sie, dass Sie die HTTP-Anforderungs Kopfzeilen aus einem WebResourceRequested-Ereignis, aber nicht aus einem NavigationStarting-Ereignis ändern können.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="5b0bf-123">Member</span><span class="sxs-lookup"><span data-stu-id="5b0bf-123">Members</span></span>

#### <span data-ttu-id="5b0bf-124">GetHeader</span><span class="sxs-lookup"><span data-stu-id="5b0bf-124">GetHeader</span></span> 

<span data-ttu-id="5b0bf-125">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-125">Gets the header value matching the name.</span></span>

> <span data-ttu-id="5b0bf-126">Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="5b0bf-126">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="5b0bf-127">Contains</span><span class="sxs-lookup"><span data-stu-id="5b0bf-127">Contains</span></span> 

<span data-ttu-id="5b0bf-128">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-128">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="5b0bf-129">Public HRESULT [Contains](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="5b0bf-129">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="5b0bf-130">SetHeader</span><span class="sxs-lookup"><span data-stu-id="5b0bf-130">SetHeader</span></span> 

<span data-ttu-id="5b0bf-131">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-131">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="5b0bf-132">Public HRESULT [setHeader](#setheader)(LPCWSTR-Name, LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="5b0bf-132">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="5b0bf-133">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="5b0bf-133">RemoveHeader</span></span> 

<span data-ttu-id="5b0bf-134">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-134">Removes header that matches the name.</span></span>

> <span data-ttu-id="5b0bf-135">Public HRESULT [RemoveHeader](#removeheader)(LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="5b0bf-135">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="5b0bf-136">GetIterator</span><span class="sxs-lookup"><span data-stu-id="5b0bf-136">GetIterator</span></span> 

<span data-ttu-id="5b0bf-137">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="5b0bf-137">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="5b0bf-138">öffentlicher HRESULT- [getIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="5b0bf-138">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


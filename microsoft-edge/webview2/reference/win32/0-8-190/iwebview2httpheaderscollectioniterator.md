---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 7abc6119d893cd1e9432d255969549f07d7e3a00
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878463"
---
# <span data-ttu-id="16495-104">0.8.355-Interface-IWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="16495-104">0.8.355 - interface IWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="16495-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="16495-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="16495-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="16495-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="16495-107">Iterator für eine Sammlung von HTTP-Headern.</span><span class="sxs-lookup"><span data-stu-id="16495-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="16495-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="16495-108">Summary</span></span>

 <span data-ttu-id="16495-109">Member</span><span class="sxs-lookup"><span data-stu-id="16495-109">Members</span></span>                        | <span data-ttu-id="16495-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="16495-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="16495-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="16495-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="16495-112">Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.</span><span class="sxs-lookup"><span data-stu-id="16495-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="16495-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="16495-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="16495-114">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="16495-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="16495-115">Siehe [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) und [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="16495-115">See [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) and [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span></span>

## <span data-ttu-id="16495-116">Member</span><span class="sxs-lookup"><span data-stu-id="16495-116">Members</span></span>

#### <span data-ttu-id="16495-117">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="16495-117">GetCurrentHeader</span></span> 

<span data-ttu-id="16495-118">Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.</span><span class="sxs-lookup"><span data-stu-id="16495-118">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="16495-119">Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="16495-119">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="16495-120">Diese Methode schlägt fehl, wenn der letzte Aufruf von MoveNext has_next auf "false" festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="16495-120">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="16495-121">MoveNext</span><span class="sxs-lookup"><span data-stu-id="16495-121">MoveNext</span></span> 

<span data-ttu-id="16495-122">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="16495-122">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="16495-123">Public HRESULT [MoveNext](#movenext)(bool \* has_next)</span><span class="sxs-lookup"><span data-stu-id="16495-123">public HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span></span>

<span data-ttu-id="16495-124">Der has_next-Parameter wird auf "false" festgelegt, wenn keine weiteren HTTP-Header vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="16495-124">The has_next parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="16495-125">Nachdem dies erfolgt ist, schlägt die GetCurrentHeader-Methode fehl, wenn Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="16495-125">After this occurs the GetCurrentHeader method will fail if called.</span></span>


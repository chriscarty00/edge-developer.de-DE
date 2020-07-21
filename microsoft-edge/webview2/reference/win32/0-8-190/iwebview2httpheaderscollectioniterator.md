---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: dbcc5b10ce1973df61554f3f27174f600fb25280
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885981"
---
# <span data-ttu-id="990b5-104">0.8.355-Interface-IWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="990b5-104">0.8.355 - interface IWebView2HttpHeadersCollectionIterator</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="990b5-105">Iterator für eine Sammlung von HTTP-Headern.</span><span class="sxs-lookup"><span data-stu-id="990b5-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="990b5-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="990b5-106">Summary</span></span>

 <span data-ttu-id="990b5-107">Member</span><span class="sxs-lookup"><span data-stu-id="990b5-107">Members</span></span>                        | <span data-ttu-id="990b5-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="990b5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="990b5-109">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="990b5-109">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="990b5-110">Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.</span><span class="sxs-lookup"><span data-stu-id="990b5-110">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="990b5-111">MoveNext</span><span class="sxs-lookup"><span data-stu-id="990b5-111">MoveNext</span></span>](#movenext) | <span data-ttu-id="990b5-112">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="990b5-112">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="990b5-113">Siehe [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) und [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="990b5-113">See [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) and [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span></span>

## <span data-ttu-id="990b5-114">Member</span><span class="sxs-lookup"><span data-stu-id="990b5-114">Members</span></span>

#### <span data-ttu-id="990b5-115">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="990b5-115">GetCurrentHeader</span></span> 

<span data-ttu-id="990b5-116">Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.</span><span class="sxs-lookup"><span data-stu-id="990b5-116">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="990b5-117">Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* Name, LPWSTR \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="990b5-117">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="990b5-118">Diese Methode schlägt fehl, wenn der letzte Aufruf von MoveNext has_next auf "false" festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="990b5-118">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="990b5-119">MoveNext</span><span class="sxs-lookup"><span data-stu-id="990b5-119">MoveNext</span></span> 

<span data-ttu-id="990b5-120">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="990b5-120">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="990b5-121">Public HRESULT [MoveNext](#movenext)(bool \* has_next)</span><span class="sxs-lookup"><span data-stu-id="990b5-121">public HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span></span>

<span data-ttu-id="990b5-122">Der has_next-Parameter wird auf "false" festgelegt, wenn keine weiteren HTTP-Header vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="990b5-122">The has_next parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="990b5-123">Nachdem dies erfolgt ist, schlägt die GetCurrentHeader-Methode fehl, wenn Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="990b5-123">After this occurs the GetCurrentHeader method will fail if called.</span></span>


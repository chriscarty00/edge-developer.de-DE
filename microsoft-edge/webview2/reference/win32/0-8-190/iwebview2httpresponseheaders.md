---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 077c85b2458c2cf843c4d2f0548d17ec01ba4751
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885961"
---
# <span data-ttu-id="a500b-104">0.8.355-Interface-IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="a500b-104">0.8.355 - interface IWebView2HttpResponseHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="a500b-105">HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="a500b-105">HTTP response headers.</span></span>

## <span data-ttu-id="a500b-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a500b-106">Summary</span></span>

 <span data-ttu-id="a500b-107">Member</span><span class="sxs-lookup"><span data-stu-id="a500b-107">Members</span></span>                        | <span data-ttu-id="a500b-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a500b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a500b-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="a500b-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="a500b-110">Fügt Headerzeile mit Name und Wert an.</span><span class="sxs-lookup"><span data-stu-id="a500b-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="a500b-111">Contains</span><span class="sxs-lookup"><span data-stu-id="a500b-111">Contains</span></span>](#contains) | <span data-ttu-id="a500b-112">Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a500b-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="a500b-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="a500b-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="a500b-114">Ruft die Überschriften Werte ab, die dem Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a500b-114">Gets the header values matching the name.</span></span>
[<span data-ttu-id="a500b-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="a500b-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="a500b-116">Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="a500b-116">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="a500b-117">Wird zum Erstellen eines WebResourceResponse für das WebResourceRequested-Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="a500b-117">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="a500b-118">Member</span><span class="sxs-lookup"><span data-stu-id="a500b-118">Members</span></span>

#### <span data-ttu-id="a500b-119">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="a500b-119">AppendHeader</span></span> 

<span data-ttu-id="a500b-120">Fügt Headerzeile mit Name und Wert an.</span><span class="sxs-lookup"><span data-stu-id="a500b-120">Appends header line with name and value.</span></span>

> <span data-ttu-id="a500b-121">Public HRESULT [Appendheader](#appendheader)(LPCWSTR-Name; LPCWSTR-Wert)</span><span class="sxs-lookup"><span data-stu-id="a500b-121">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="a500b-122">Contains</span><span class="sxs-lookup"><span data-stu-id="a500b-122">Contains</span></span> 

<span data-ttu-id="a500b-123">Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a500b-123">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="a500b-124">Public HRESULT [Contains](#contains)(LPCWSTR Name, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="a500b-124">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="a500b-125">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="a500b-125">GetHeaders</span></span> 

<span data-ttu-id="a500b-126">Ruft die Überschriften Werte ab, die dem Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a500b-126">Gets the header values matching the name.</span></span>

> <span data-ttu-id="a500b-127">öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="a500b-127">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="a500b-128">GetIterator</span><span class="sxs-lookup"><span data-stu-id="a500b-128">GetIterator</span></span> 

<span data-ttu-id="a500b-129">Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="a500b-129">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="a500b-130">öffentlicher HRESULT- [getIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \*-Iterator)</span><span class="sxs-lookup"><span data-stu-id="a500b-130">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


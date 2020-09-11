---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: e7aad408372acbbd19ecab9d04312f21e2396e88
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012091"
---
# <span data-ttu-id="7eb55-104">Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator Klasse</span><span class="sxs-lookup"><span data-stu-id="7eb55-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpHeadersCollectionIterator class</span></span> 

<span data-ttu-id="7eb55-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="7eb55-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="7eb55-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="7eb55-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="7eb55-107">Iterator für eine Sammlung von HTTP-Headern.</span><span class="sxs-lookup"><span data-stu-id="7eb55-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="7eb55-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7eb55-108">Summary</span></span>

 <span data-ttu-id="7eb55-109">Member</span><span class="sxs-lookup"><span data-stu-id="7eb55-109">Members</span></span>                        | <span data-ttu-id="7eb55-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7eb55-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7eb55-111">HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="7eb55-111">HasCurrentHeader</span></span>](#hascurrentheader) | <span data-ttu-id="7eb55-112">"True", wenn der Iterator keine Überschriften mehr ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="7eb55-112">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="7eb55-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="7eb55-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="7eb55-114">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="7eb55-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="7eb55-115">Siehe CoreWebView2HttpRequestHeaders und CoreWebView2HttpResponseHeaders.</span><span class="sxs-lookup"><span data-stu-id="7eb55-115">See CoreWebView2HttpRequestHeaders and CoreWebView2HttpResponseHeaders.</span></span>

## <span data-ttu-id="7eb55-116">Member</span><span class="sxs-lookup"><span data-stu-id="7eb55-116">Members</span></span>

#### <span data-ttu-id="7eb55-117">HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="7eb55-117">HasCurrentHeader</span></span> 

<span data-ttu-id="7eb55-118">"True", wenn der Iterator keine Überschriften mehr ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="7eb55-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="7eb55-119">public bool [HasCurrentHeader](#hascurrentheader)</span><span class="sxs-lookup"><span data-stu-id="7eb55-119">public bool [HasCurrentHeader](#hascurrentheader)</span></span>

<span data-ttu-id="7eb55-120">Wenn die Sammlung, über die der Iterator durchlaufen wird, leer ist oder der Iterator über das Ende der Auflistung hinausgegangen ist, ist dies false.</span><span class="sxs-lookup"><span data-stu-id="7eb55-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="7eb55-121">MoveNext</span><span class="sxs-lookup"><span data-stu-id="7eb55-121">MoveNext</span></span> 

<span data-ttu-id="7eb55-122">Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.</span><span class="sxs-lookup"><span data-stu-id="7eb55-122">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="7eb55-123">public bool [MoveNext](#movenext)()</span><span class="sxs-lookup"><span data-stu-id="7eb55-123">public bool [MoveNext](#movenext)()</span></span>

<span data-ttu-id="7eb55-124">Der hasNext "-Parameter wird auf" false "festgelegt, wenn keine weiteren HTTP-Header vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7eb55-124">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="7eb55-125">Nachdem dies erfolgt ist, schlägt die GetCurrentHeader-Methode fehl, wenn Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7eb55-125">After this occurs the GetCurrentHeader method will fail if called.</span></span>


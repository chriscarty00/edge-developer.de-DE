---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
ms.openlocfilehash: 1441d5a45caf4e8f561de2487438b66e067760f6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012024"
---
# <span data-ttu-id="903d3-104">Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders Klasse</span><span class="sxs-lookup"><span data-stu-id="903d3-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpRequestHeaders class</span></span> 

<span data-ttu-id="903d3-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="903d3-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="903d3-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="903d3-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="903d3-107">HTTP-Anforderungsheader.</span><span class="sxs-lookup"><span data-stu-id="903d3-107">HTTP request headers.</span></span>

## <span data-ttu-id="903d3-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="903d3-108">Summary</span></span>

 <span data-ttu-id="903d3-109">Member</span><span class="sxs-lookup"><span data-stu-id="903d3-109">Members</span></span>                        | <span data-ttu-id="903d3-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="903d3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="903d3-111">Contains</span><span class="sxs-lookup"><span data-stu-id="903d3-111">Contains</span></span>](#contains) | <span data-ttu-id="903d3-112">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="903d3-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="903d3-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="903d3-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="903d3-114">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="903d3-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="903d3-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="903d3-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="903d3-116">Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.</span><span class="sxs-lookup"><span data-stu-id="903d3-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="903d3-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="903d3-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="903d3-118">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="903d3-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="903d3-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="903d3-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="903d3-120">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="903d3-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="903d3-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="903d3-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="903d3-122">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="903d3-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="903d3-123">Wird verwendet, um die HTTP-Anforderung für das WebResourceRequested-Ereignis und das NavigationStarting-Ereignis zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="903d3-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="903d3-124">Beachten Sie, dass Sie die HTTP-Anforderungs Kopfzeilen aus einem WebResourceRequested-Ereignis, aber nicht aus einem NavigationStarting-Ereignis ändern können.</span><span class="sxs-lookup"><span data-stu-id="903d3-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="903d3-125">Member</span><span class="sxs-lookup"><span data-stu-id="903d3-125">Members</span></span>

#### <span data-ttu-id="903d3-126">Contains</span><span class="sxs-lookup"><span data-stu-id="903d3-126">Contains</span></span> 

<span data-ttu-id="903d3-127">Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="903d3-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="903d3-128">public bool [Contains](#contains)(Zeichenfolgenname)</span><span class="sxs-lookup"><span data-stu-id="903d3-128">public bool [Contains](#contains)(string name)</span></span>

#### <span data-ttu-id="903d3-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="903d3-129">GetHeader</span></span> 

<span data-ttu-id="903d3-130">Ruft den Headerwert ab, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="903d3-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="903d3-131">öffentliche Zeichenfolge [GetHeader](#getheader)(Zeichenfolgenname)</span><span class="sxs-lookup"><span data-stu-id="903d3-131">public string [GetHeader](#getheader)(string name)</span></span>

#### <span data-ttu-id="903d3-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="903d3-132">GetHeaders</span></span> 

<span data-ttu-id="903d3-133">Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.</span><span class="sxs-lookup"><span data-stu-id="903d3-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="903d3-134">öffentliche CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(Zeichenfolgenname)</span><span class="sxs-lookup"><span data-stu-id="903d3-134">public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(string name)</span></span>

#### <span data-ttu-id="903d3-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="903d3-135">GetIterator</span></span> 

<span data-ttu-id="903d3-136">Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.</span><span class="sxs-lookup"><span data-stu-id="903d3-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="903d3-137">Public CoreWebView2HttpHeadersCollectionIterator [getIterator](#getiterator)()</span><span class="sxs-lookup"><span data-stu-id="903d3-137">public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span></span>

#### <span data-ttu-id="903d3-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="903d3-138">RemoveHeader</span></span> 

<span data-ttu-id="903d3-139">Entfernt den Header, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="903d3-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="903d3-140">publicvoid [RemoveHeader](#removeheader)(String Name)</span><span class="sxs-lookup"><span data-stu-id="903d3-140">public void [RemoveHeader](#removeheader)(string name)</span></span>

#### <span data-ttu-id="903d3-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="903d3-141">SetHeader</span></span> 

<span data-ttu-id="903d3-142">Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="903d3-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="903d3-143">publicvoid [setHeader](#setheader)(Zeichenfolgenname, Zeichenfolgenwert)</span><span class="sxs-lookup"><span data-stu-id="903d3-143">public void [SetHeader](#setheader)(string name, string value)</span></span>


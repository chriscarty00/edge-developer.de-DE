---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
ms.openlocfilehash: 51218283460975421859c65da8a43553767ad216
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012088"
---
# <span data-ttu-id="edb7a-104">Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders Klasse</span><span class="sxs-lookup"><span data-stu-id="edb7a-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpResponseHeaders class</span></span> 

<span data-ttu-id="edb7a-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="edb7a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="edb7a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="edb7a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="edb7a-107">HTTP-Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="edb7a-107">HTTP response headers.</span></span>

## <span data-ttu-id="edb7a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="edb7a-108">Summary</span></span>

 <span data-ttu-id="edb7a-109">Member</span><span class="sxs-lookup"><span data-stu-id="edb7a-109">Members</span></span>                        | <span data-ttu-id="edb7a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="edb7a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="edb7a-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="edb7a-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="edb7a-112">Fügt Headerzeile mit Name und Wert an.</span><span class="sxs-lookup"><span data-stu-id="edb7a-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="edb7a-113">Contains</span><span class="sxs-lookup"><span data-stu-id="edb7a-113">Contains</span></span>](#contains) | <span data-ttu-id="edb7a-114">Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="edb7a-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="edb7a-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="edb7a-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="edb7a-116">Ruft den ersten Headerwert in der Sammlung ab, die mit dem Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="edb7a-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="edb7a-117">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="edb7a-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="edb7a-118">Ruft die Überschriften Werte ab, die dem Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="edb7a-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="edb7a-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="edb7a-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="edb7a-120">Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="edb7a-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="edb7a-121">Wird zum Erstellen eines WebResourceResponse für das WebResourceRequested-Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="edb7a-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="edb7a-122">Member</span><span class="sxs-lookup"><span data-stu-id="edb7a-122">Members</span></span>

#### <span data-ttu-id="edb7a-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="edb7a-123">AppendHeader</span></span> 

<span data-ttu-id="edb7a-124">Fügt Headerzeile mit Name und Wert an.</span><span class="sxs-lookup"><span data-stu-id="edb7a-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="edb7a-125">publicvoid [Appendheader](#appendheader)(String Name, String value)</span><span class="sxs-lookup"><span data-stu-id="edb7a-125">public void [AppendHeader](#appendheader)(string name, string value)</span></span>

#### <span data-ttu-id="edb7a-126">Contains</span><span class="sxs-lookup"><span data-stu-id="edb7a-126">Contains</span></span> 

<span data-ttu-id="edb7a-127">Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="edb7a-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="edb7a-128">public bool [Contains](#contains)(Zeichenfolgenname)</span><span class="sxs-lookup"><span data-stu-id="edb7a-128">public bool [Contains](#contains)(string name)</span></span>

#### <span data-ttu-id="edb7a-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="edb7a-129">GetHeader</span></span> 

<span data-ttu-id="edb7a-130">Ruft den ersten Headerwert in der Sammlung ab, die mit dem Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="edb7a-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="edb7a-131">öffentliche Zeichenfolge [GetHeader](#getheader)(Zeichenfolgenname)</span><span class="sxs-lookup"><span data-stu-id="edb7a-131">public string [GetHeader](#getheader)(string name)</span></span>

#### <span data-ttu-id="edb7a-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="edb7a-132">GetHeaders</span></span> 

<span data-ttu-id="edb7a-133">Ruft die Überschriften Werte ab, die dem Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="edb7a-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="edb7a-134">öffentliche CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(Zeichenfolgenname)</span><span class="sxs-lookup"><span data-stu-id="edb7a-134">public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(string name)</span></span>

#### <span data-ttu-id="edb7a-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="edb7a-135">GetIterator</span></span> 

<span data-ttu-id="edb7a-136">Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="edb7a-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="edb7a-137">Public CoreWebView2HttpHeadersCollectionIterator [getIterator](#getiterator)()</span><span class="sxs-lookup"><span data-stu-id="edb7a-137">public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span></span>


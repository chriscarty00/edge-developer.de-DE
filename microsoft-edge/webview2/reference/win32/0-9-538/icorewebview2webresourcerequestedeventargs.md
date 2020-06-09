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
ms.openlocfilehash: e83078b6ac45fbc0b479c5d6b0fde3263a8f34fd
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698858"
---
# <span data-ttu-id="c0c83-104">Schnittstellen ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c0c83-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="c0c83-105">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c0c83-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="c0c83-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c0c83-106">Summary</span></span>

 <span data-ttu-id="c0c83-107">Member</span><span class="sxs-lookup"><span data-stu-id="c0c83-107">Members</span></span>                        | <span data-ttu-id="c0c83-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c0c83-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c0c83-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="c0c83-109">get_Request</span></span>](#get_request) | <span data-ttu-id="c0c83-110">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c0c83-110">The HTTP request.</span></span>
[<span data-ttu-id="c0c83-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="c0c83-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="c0c83-112">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="c0c83-112">The web resource request contexts.</span></span>
[<span data-ttu-id="c0c83-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="c0c83-113">get_Response</span></span>](#get_response) | <span data-ttu-id="c0c83-114">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="c0c83-114">The HTTP response.</span></span>
[<span data-ttu-id="c0c83-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c0c83-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="c0c83-116">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="c0c83-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="c0c83-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="c0c83-117">put_Response</span></span>](#put_response) | <span data-ttu-id="c0c83-118">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c0c83-118">Set the Response property.</span></span>

## <span data-ttu-id="c0c83-119">Member</span><span class="sxs-lookup"><span data-stu-id="c0c83-119">Members</span></span>

#### <span data-ttu-id="c0c83-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="c0c83-120">get_Request</span></span> 

<span data-ttu-id="c0c83-121">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c0c83-121">The HTTP request.</span></span>

> <span data-ttu-id="c0c83-122">öffentliche HRESULT- [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="c0c83-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="c0c83-123">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="c0c83-123">get_ResourceContext</span></span> 

<span data-ttu-id="c0c83-124">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="c0c83-124">The web resource request contexts.</span></span>

> <span data-ttu-id="c0c83-125">öffentliche HRESULT- [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \*-Kontext)</span><span class="sxs-lookup"><span data-stu-id="c0c83-125">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="c0c83-126">get_Response</span><span class="sxs-lookup"><span data-stu-id="c0c83-126">get_Response</span></span> 

<span data-ttu-id="c0c83-127">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="c0c83-127">The HTTP response.</span></span>

> <span data-ttu-id="c0c83-128">öffentliche HRESULT- [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="c0c83-128">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="c0c83-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c0c83-129">GetDeferral</span></span> 

<span data-ttu-id="c0c83-130">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="c0c83-130">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="c0c83-131">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="c0c83-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="c0c83-132">Sie können das [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c0c83-132">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="c0c83-133">put_Response</span><span class="sxs-lookup"><span data-stu-id="c0c83-133">put_Response</span></span> 

<span data-ttu-id="c0c83-134">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c0c83-134">Set the Response property.</span></span>

> <span data-ttu-id="c0c83-135">öffentliche HRESULT- [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* Response)</span><span class="sxs-lookup"><span data-stu-id="c0c83-135">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>


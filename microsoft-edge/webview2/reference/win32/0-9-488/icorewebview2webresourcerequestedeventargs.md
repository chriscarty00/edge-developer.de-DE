---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 85954a3f866ed9fd778af93fc27872af2d20eb2e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697945"
---
# <span data-ttu-id="32135-104">Schnittstellen ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="32135-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="32135-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="32135-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="32135-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="32135-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="32135-107">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="32135-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="32135-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="32135-108">Summary</span></span>

 <span data-ttu-id="32135-109">Member</span><span class="sxs-lookup"><span data-stu-id="32135-109">Members</span></span>                        | <span data-ttu-id="32135-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="32135-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="32135-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="32135-111">get_Request</span></span>](#get_request) | <span data-ttu-id="32135-112">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="32135-112">The HTTP request.</span></span>
[<span data-ttu-id="32135-113">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="32135-113">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="32135-114">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="32135-114">The web resource request contexts.</span></span>
[<span data-ttu-id="32135-115">get_Response</span><span class="sxs-lookup"><span data-stu-id="32135-115">get_Response</span></span>](#get_response) | <span data-ttu-id="32135-116">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="32135-116">The HTTP response.</span></span>
[<span data-ttu-id="32135-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="32135-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="32135-118">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="32135-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="32135-119">put_Response</span><span class="sxs-lookup"><span data-stu-id="32135-119">put_Response</span></span>](#put_response) | <span data-ttu-id="32135-120">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="32135-120">Set the Response property.</span></span>

## <span data-ttu-id="32135-121">Member</span><span class="sxs-lookup"><span data-stu-id="32135-121">Members</span></span>

#### <span data-ttu-id="32135-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="32135-122">get_Request</span></span> 

<span data-ttu-id="32135-123">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="32135-123">The HTTP request.</span></span>

> <span data-ttu-id="32135-124">öffentliche HRESULT- [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="32135-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="32135-125">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="32135-125">get_ResourceContext</span></span> 

<span data-ttu-id="32135-126">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="32135-126">The web resource request contexts.</span></span>

> <span data-ttu-id="32135-127">öffentliche HRESULT- [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \*-Kontext)</span><span class="sxs-lookup"><span data-stu-id="32135-127">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="32135-128">get_Response</span><span class="sxs-lookup"><span data-stu-id="32135-128">get_Response</span></span> 

<span data-ttu-id="32135-129">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="32135-129">The HTTP response.</span></span>

> <span data-ttu-id="32135-130">öffentliche HRESULT- [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="32135-130">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="32135-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="32135-131">GetDeferral</span></span> 

<span data-ttu-id="32135-132">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="32135-132">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="32135-133">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="32135-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="32135-134">Sie können das [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="32135-134">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="32135-135">put_Response</span><span class="sxs-lookup"><span data-stu-id="32135-135">put_Response</span></span> 

<span data-ttu-id="32135-136">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="32135-136">Set the Response property.</span></span>

> <span data-ttu-id="32135-137">öffentliche HRESULT- [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* Response)</span><span class="sxs-lookup"><span data-stu-id="32135-137">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>


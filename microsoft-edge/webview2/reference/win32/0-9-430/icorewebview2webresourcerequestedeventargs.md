---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 826cdf960a20e32b8e0fa6b5a8ddad720ac137a6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877581"
---
# <span data-ttu-id="09594-104">0.9.430-Interface-ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="09594-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="09594-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="09594-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="09594-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="09594-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="09594-107">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="09594-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="09594-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="09594-108">Summary</span></span>

 <span data-ttu-id="09594-109">Member</span><span class="sxs-lookup"><span data-stu-id="09594-109">Members</span></span>                        | <span data-ttu-id="09594-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="09594-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="09594-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="09594-111">get_Request</span></span>](#get_request) | <span data-ttu-id="09594-112">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="09594-112">The HTTP request.</span></span>
[<span data-ttu-id="09594-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="09594-113">get_Response</span></span>](#get_response) | <span data-ttu-id="09594-114">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="09594-114">The HTTP response.</span></span>
[<span data-ttu-id="09594-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="09594-115">put_Response</span></span>](#put_response) | <span data-ttu-id="09594-116">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="09594-116">Set the Response property.</span></span>
[<span data-ttu-id="09594-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="09594-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="09594-118">Rufen Sie ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="09594-118">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="09594-119">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="09594-119">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="09594-120">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="09594-120">The web resource request contexts.</span></span>

## <span data-ttu-id="09594-121">Member</span><span class="sxs-lookup"><span data-stu-id="09594-121">Members</span></span>

#### <span data-ttu-id="09594-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="09594-122">get_Request</span></span> 

<span data-ttu-id="09594-123">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="09594-123">The HTTP request.</span></span>

> <span data-ttu-id="09594-124">öffentliche HRESULT- [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="09594-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="09594-125">get_Response</span><span class="sxs-lookup"><span data-stu-id="09594-125">get_Response</span></span> 

<span data-ttu-id="09594-126">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="09594-126">The HTTP response.</span></span>

> <span data-ttu-id="09594-127">öffentliche HRESULT- [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="09594-127">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="09594-128">put_Response</span><span class="sxs-lookup"><span data-stu-id="09594-128">put_Response</span></span> 

<span data-ttu-id="09594-129">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="09594-129">Set the Response property.</span></span>

> <span data-ttu-id="09594-130">öffentliche HRESULT- [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* Response)</span><span class="sxs-lookup"><span data-stu-id="09594-130">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="09594-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="09594-131">GetDeferral</span></span> 

<span data-ttu-id="09594-132">Rufen Sie ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="09594-132">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="09594-133">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="09594-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="09594-134">Sie können das [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="09594-134">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="09594-135">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="09594-135">get_ResourceContext</span></span> 

<span data-ttu-id="09594-136">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="09594-136">The web resource request contexts.</span></span>

> <span data-ttu-id="09594-137">öffentliche HRESULT- [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \*-Kontext)</span><span class="sxs-lookup"><span data-stu-id="09594-137">public HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>


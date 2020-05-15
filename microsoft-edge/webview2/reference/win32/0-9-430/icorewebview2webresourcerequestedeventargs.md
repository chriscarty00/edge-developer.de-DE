---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 59557ca86e8b044fb937fe93b3060c0879abb6f1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654041"
---
# <span data-ttu-id="9316b-104">Schnittstellen ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9316b-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="9316b-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="9316b-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="9316b-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="9316b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="9316b-107">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9316b-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="9316b-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9316b-108">Summary</span></span>

 <span data-ttu-id="9316b-109">Member</span><span class="sxs-lookup"><span data-stu-id="9316b-109">Members</span></span>                        | <span data-ttu-id="9316b-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9316b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9316b-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="9316b-111">get_Request</span></span>](#get_request) | <span data-ttu-id="9316b-112">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9316b-112">The HTTP request.</span></span>
[<span data-ttu-id="9316b-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="9316b-113">get_Response</span></span>](#get_response) | <span data-ttu-id="9316b-114">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="9316b-114">The HTTP response.</span></span>
[<span data-ttu-id="9316b-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="9316b-115">put_Response</span></span>](#put_response) | <span data-ttu-id="9316b-116">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9316b-116">Set the Response property.</span></span>
[<span data-ttu-id="9316b-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9316b-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="9316b-118">Rufen Sie ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="9316b-118">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="9316b-119">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9316b-119">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="9316b-120">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="9316b-120">The web resource request contexts.</span></span>

## <span data-ttu-id="9316b-121">Member</span><span class="sxs-lookup"><span data-stu-id="9316b-121">Members</span></span>

#### <span data-ttu-id="9316b-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="9316b-122">get_Request</span></span> 

<span data-ttu-id="9316b-123">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9316b-123">The HTTP request.</span></span>

> <span data-ttu-id="9316b-124">öffentliche HRESULT- [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="9316b-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="9316b-125">get_Response</span><span class="sxs-lookup"><span data-stu-id="9316b-125">get_Response</span></span> 

<span data-ttu-id="9316b-126">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="9316b-126">The HTTP response.</span></span>

> <span data-ttu-id="9316b-127">öffentliche HRESULT- [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="9316b-127">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="9316b-128">put_Response</span><span class="sxs-lookup"><span data-stu-id="9316b-128">put_Response</span></span> 

<span data-ttu-id="9316b-129">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9316b-129">Set the Response property.</span></span>

> <span data-ttu-id="9316b-130">öffentliche HRESULT- [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* Response)</span><span class="sxs-lookup"><span data-stu-id="9316b-130">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="9316b-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9316b-131">GetDeferral</span></span> 

<span data-ttu-id="9316b-132">Rufen Sie ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="9316b-132">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="9316b-133">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="9316b-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="9316b-134">Sie können das [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9316b-134">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="9316b-135">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9316b-135">get_ResourceContext</span></span> 

<span data-ttu-id="9316b-136">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="9316b-136">The web resource request contexts.</span></span>

> <span data-ttu-id="9316b-137">öffentliche HRESULT- [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \*-Kontext)</span><span class="sxs-lookup"><span data-stu-id="9316b-137">public HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>


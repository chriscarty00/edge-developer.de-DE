---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 00aaddcc732076e4f7aa808b04132641fe7fe969
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886444"
---
# <span data-ttu-id="5f276-104">0.9.430-Interface-ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5f276-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="5f276-105">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5f276-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="5f276-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5f276-106">Summary</span></span>

 <span data-ttu-id="5f276-107">Member</span><span class="sxs-lookup"><span data-stu-id="5f276-107">Members</span></span>                        | <span data-ttu-id="5f276-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5f276-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5f276-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="5f276-109">get_Request</span></span>](#get_request) | <span data-ttu-id="5f276-110">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5f276-110">The HTTP request.</span></span>
[<span data-ttu-id="5f276-111">get_Response</span><span class="sxs-lookup"><span data-stu-id="5f276-111">get_Response</span></span>](#get_response) | <span data-ttu-id="5f276-112">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="5f276-112">The HTTP response.</span></span>
[<span data-ttu-id="5f276-113">put_Response</span><span class="sxs-lookup"><span data-stu-id="5f276-113">put_Response</span></span>](#put_response) | <span data-ttu-id="5f276-114">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5f276-114">Set the Response property.</span></span>
[<span data-ttu-id="5f276-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="5f276-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="5f276-116">Rufen Sie ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="5f276-116">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="5f276-117">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="5f276-117">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="5f276-118">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="5f276-118">The web resource request contexts.</span></span>

## <span data-ttu-id="5f276-119">Member</span><span class="sxs-lookup"><span data-stu-id="5f276-119">Members</span></span>

#### <span data-ttu-id="5f276-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="5f276-120">get_Request</span></span> 

<span data-ttu-id="5f276-121">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5f276-121">The HTTP request.</span></span>

> <span data-ttu-id="5f276-122">öffentliche HRESULT- [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="5f276-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="5f276-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="5f276-123">get_Response</span></span> 

<span data-ttu-id="5f276-124">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="5f276-124">The HTTP response.</span></span>

> <span data-ttu-id="5f276-125">öffentliche HRESULT- [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="5f276-125">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="5f276-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="5f276-126">put_Response</span></span> 

<span data-ttu-id="5f276-127">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5f276-127">Set the Response property.</span></span>

> <span data-ttu-id="5f276-128">öffentliche HRESULT- [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* Response)</span><span class="sxs-lookup"><span data-stu-id="5f276-128">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="5f276-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="5f276-129">GetDeferral</span></span> 

<span data-ttu-id="5f276-130">Rufen Sie ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="5f276-130">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="5f276-131">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="5f276-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="5f276-132">Sie können das [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="5f276-132">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="5f276-133">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="5f276-133">get_ResourceContext</span></span> 

<span data-ttu-id="5f276-134">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="5f276-134">The web resource request contexts.</span></span>

> <span data-ttu-id="5f276-135">öffentliche HRESULT- [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \*-Kontext)</span><span class="sxs-lookup"><span data-stu-id="5f276-135">public HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>


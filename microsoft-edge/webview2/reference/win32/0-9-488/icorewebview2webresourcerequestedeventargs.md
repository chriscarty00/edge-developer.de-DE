---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: dec8bfb2927e823c85f472bd2cab0800ff5f00c7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883749"
---
# <span data-ttu-id="098e6-104">0.9.515-Interface-ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="098e6-104">0.9.515 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="098e6-105">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="098e6-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="098e6-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="098e6-106">Summary</span></span>

 <span data-ttu-id="098e6-107">Member</span><span class="sxs-lookup"><span data-stu-id="098e6-107">Members</span></span>                        | <span data-ttu-id="098e6-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="098e6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="098e6-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="098e6-109">get_Request</span></span>](#get_request) | <span data-ttu-id="098e6-110">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="098e6-110">The HTTP request.</span></span>
[<span data-ttu-id="098e6-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="098e6-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="098e6-112">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="098e6-112">The web resource request contexts.</span></span>
[<span data-ttu-id="098e6-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="098e6-113">get_Response</span></span>](#get_response) | <span data-ttu-id="098e6-114">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="098e6-114">The HTTP response.</span></span>
[<span data-ttu-id="098e6-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="098e6-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="098e6-116">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="098e6-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="098e6-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="098e6-117">put_Response</span></span>](#put_response) | <span data-ttu-id="098e6-118">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="098e6-118">Set the Response property.</span></span>

## <span data-ttu-id="098e6-119">Member</span><span class="sxs-lookup"><span data-stu-id="098e6-119">Members</span></span>

#### <span data-ttu-id="098e6-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="098e6-120">get_Request</span></span> 

<span data-ttu-id="098e6-121">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="098e6-121">The HTTP request.</span></span>

> <span data-ttu-id="098e6-122">öffentliche HRESULT- [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="098e6-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="098e6-123">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="098e6-123">get_ResourceContext</span></span> 

<span data-ttu-id="098e6-124">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="098e6-124">The web resource request contexts.</span></span>

> <span data-ttu-id="098e6-125">öffentliche HRESULT- [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \*-Kontext)</span><span class="sxs-lookup"><span data-stu-id="098e6-125">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="098e6-126">get_Response</span><span class="sxs-lookup"><span data-stu-id="098e6-126">get_Response</span></span> 

<span data-ttu-id="098e6-127">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="098e6-127">The HTTP response.</span></span>

> <span data-ttu-id="098e6-128">öffentliche HRESULT- [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="098e6-128">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="098e6-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="098e6-129">GetDeferral</span></span> 

<span data-ttu-id="098e6-130">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="098e6-130">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="098e6-131">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="098e6-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="098e6-132">Sie können das [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="098e6-132">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="098e6-133">put_Response</span><span class="sxs-lookup"><span data-stu-id="098e6-133">put_Response</span></span> 

<span data-ttu-id="098e6-134">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="098e6-134">Set the Response property.</span></span>

> <span data-ttu-id="098e6-135">öffentliche HRESULT- [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* Response)</span><span class="sxs-lookup"><span data-stu-id="098e6-135">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>


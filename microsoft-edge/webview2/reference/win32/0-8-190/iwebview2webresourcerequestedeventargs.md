---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 40474d6b1169467022e5bb47e82eba3883edc2aa
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878099"
---
# <span data-ttu-id="22e88-104">0.8.355-Interface-IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="22e88-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="22e88-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="22e88-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="22e88-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="22e88-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="22e88-107">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="22e88-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="22e88-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="22e88-108">Summary</span></span>

 <span data-ttu-id="22e88-109">Member</span><span class="sxs-lookup"><span data-stu-id="22e88-109">Members</span></span>                        | <span data-ttu-id="22e88-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="22e88-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="22e88-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="22e88-111">get_Request</span></span>](#get_request) | <span data-ttu-id="22e88-112">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="22e88-112">The HTTP request.</span></span>
[<span data-ttu-id="22e88-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="22e88-113">get_Response</span></span>](#get_response) | <span data-ttu-id="22e88-114">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="22e88-114">The HTTP response.</span></span>
[<span data-ttu-id="22e88-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="22e88-115">put_Response</span></span>](#put_response) | <span data-ttu-id="22e88-116">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22e88-116">Set the Response property.</span></span>
[<span data-ttu-id="22e88-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="22e88-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="22e88-118">Rufen Sie ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="22e88-118">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="22e88-119">Member</span><span class="sxs-lookup"><span data-stu-id="22e88-119">Members</span></span>

#### <span data-ttu-id="22e88-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="22e88-120">get_Request</span></span> 

<span data-ttu-id="22e88-121">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="22e88-121">The HTTP request.</span></span>

> <span data-ttu-id="22e88-122">öffentliche HRESULT- [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="22e88-122">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="22e88-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="22e88-123">get_Response</span></span> 

<span data-ttu-id="22e88-124">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="22e88-124">The HTTP response.</span></span>

> <span data-ttu-id="22e88-125">öffentliche HRESULT- [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="22e88-125">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="22e88-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="22e88-126">put_Response</span></span> 

<span data-ttu-id="22e88-127">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22e88-127">Set the Response property.</span></span>

> <span data-ttu-id="22e88-128">öffentliche HRESULT- [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* Response)</span><span class="sxs-lookup"><span data-stu-id="22e88-128">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="22e88-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="22e88-129">GetDeferral</span></span> 

<span data-ttu-id="22e88-130">Rufen Sie ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="22e88-130">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="22e88-131">öffentliche HRESULT [getstundung](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="22e88-131">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="22e88-132">Sie können das [IWebView2Deferral](IWebView2Deferral.md) -Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="22e88-132">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>


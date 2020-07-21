---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: aa5206be13790fd7a783f2afb4471de90fc8f2ae
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885718"
---
# <span data-ttu-id="99313-104">0.8.355-Interface-IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="99313-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="99313-105">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="99313-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="99313-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="99313-106">Summary</span></span>

 <span data-ttu-id="99313-107">Member</span><span class="sxs-lookup"><span data-stu-id="99313-107">Members</span></span>                        | <span data-ttu-id="99313-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="99313-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="99313-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="99313-109">get_Request</span></span>](#get_request) | <span data-ttu-id="99313-110">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="99313-110">The HTTP request.</span></span>
[<span data-ttu-id="99313-111">get_Response</span><span class="sxs-lookup"><span data-stu-id="99313-111">get_Response</span></span>](#get_response) | <span data-ttu-id="99313-112">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="99313-112">The HTTP response.</span></span>
[<span data-ttu-id="99313-113">put_Response</span><span class="sxs-lookup"><span data-stu-id="99313-113">put_Response</span></span>](#put_response) | <span data-ttu-id="99313-114">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="99313-114">Set the Response property.</span></span>
[<span data-ttu-id="99313-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="99313-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="99313-116">Rufen Sie ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="99313-116">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="99313-117">Member</span><span class="sxs-lookup"><span data-stu-id="99313-117">Members</span></span>

#### <span data-ttu-id="99313-118">get_Request</span><span class="sxs-lookup"><span data-stu-id="99313-118">get_Request</span></span> 

<span data-ttu-id="99313-119">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="99313-119">The HTTP request.</span></span>

> <span data-ttu-id="99313-120">öffentliche HRESULT- [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="99313-120">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="99313-121">get_Response</span><span class="sxs-lookup"><span data-stu-id="99313-121">get_Response</span></span> 

<span data-ttu-id="99313-122">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="99313-122">The HTTP response.</span></span>

> <span data-ttu-id="99313-123">öffentliche HRESULT- [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="99313-123">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="99313-124">put_Response</span><span class="sxs-lookup"><span data-stu-id="99313-124">put_Response</span></span> 

<span data-ttu-id="99313-125">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="99313-125">Set the Response property.</span></span>

> <span data-ttu-id="99313-126">öffentliche HRESULT- [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* Response)</span><span class="sxs-lookup"><span data-stu-id="99313-126">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="99313-127">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="99313-127">GetDeferral</span></span> 

<span data-ttu-id="99313-128">Rufen Sie ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="99313-128">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="99313-129">öffentliche HRESULT [getstundung](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="99313-129">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="99313-130">Sie können das [IWebView2Deferral](IWebView2Deferral.md) -Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="99313-130">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>


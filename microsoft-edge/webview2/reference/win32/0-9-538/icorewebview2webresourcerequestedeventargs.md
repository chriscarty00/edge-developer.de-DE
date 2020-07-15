---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 3613ed9b2ef562e8760de1a88322ef028ddf4ca9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879219"
---
# <span data-ttu-id="df285-104">Schnittstellen ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="df285-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="df285-105">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="df285-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="df285-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="df285-106">Summary</span></span>

 <span data-ttu-id="df285-107">Member</span><span class="sxs-lookup"><span data-stu-id="df285-107">Members</span></span>                        | <span data-ttu-id="df285-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="df285-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="df285-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="df285-109">get_Request</span></span>](#get_request) | <span data-ttu-id="df285-110">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="df285-110">The HTTP request.</span></span>
[<span data-ttu-id="df285-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="df285-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="df285-112">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="df285-112">The web resource request contexts.</span></span>
[<span data-ttu-id="df285-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="df285-113">get_Response</span></span>](#get_response) | <span data-ttu-id="df285-114">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="df285-114">The HTTP response.</span></span>
[<span data-ttu-id="df285-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="df285-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="df285-116">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="df285-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="df285-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="df285-117">put_Response</span></span>](#put_response) | <span data-ttu-id="df285-118">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df285-118">Set the Response property.</span></span>

## <span data-ttu-id="df285-119">Member</span><span class="sxs-lookup"><span data-stu-id="df285-119">Members</span></span>

#### <span data-ttu-id="df285-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="df285-120">get_Request</span></span> 

<span data-ttu-id="df285-121">Die HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="df285-121">The HTTP request.</span></span>

> <span data-ttu-id="df285-122">öffentliche HRESULT- [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="df285-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="df285-123">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="df285-123">get_ResourceContext</span></span> 

<span data-ttu-id="df285-124">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="df285-124">The web resource request contexts.</span></span>

> <span data-ttu-id="df285-125">öffentliche HRESULT- [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \*-Kontext)</span><span class="sxs-lookup"><span data-stu-id="df285-125">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="df285-126">get_Response</span><span class="sxs-lookup"><span data-stu-id="df285-126">get_Response</span></span> 

<span data-ttu-id="df285-127">Die HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="df285-127">The HTTP response.</span></span>

> <span data-ttu-id="df285-128">öffentliche HRESULT- [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="df285-128">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="df285-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="df285-129">GetDeferral</span></span> 

<span data-ttu-id="df285-130">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="df285-130">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="df285-131">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="df285-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="df285-132">Sie können das [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="df285-132">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="df285-133">put_Response</span><span class="sxs-lookup"><span data-stu-id="df285-133">put_Response</span></span> 

<span data-ttu-id="df285-134">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df285-134">Set the Response property.</span></span>

> <span data-ttu-id="df285-135">öffentliche HRESULT- [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* Response)</span><span class="sxs-lookup"><span data-stu-id="df285-135">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>


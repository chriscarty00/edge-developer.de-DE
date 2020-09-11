---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 2e55a43282a7548acefdb0b1ed1b8cac2254ef21
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010390"
---
# <span data-ttu-id="40d5e-104">0.9.579-Interface-ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="40d5e-104">0.9.579 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="40d5e-105">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="40d5e-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="40d5e-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="40d5e-106">Summary</span></span>

 <span data-ttu-id="40d5e-107">Member</span><span class="sxs-lookup"><span data-stu-id="40d5e-107">Members</span></span>                        | <span data-ttu-id="40d5e-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="40d5e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="40d5e-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="40d5e-109">get_Request</span></span>](#get_request) | <span data-ttu-id="40d5e-110">Die Webressourcen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="40d5e-110">The Web resource request.</span></span>
[<span data-ttu-id="40d5e-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="40d5e-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="40d5e-112">Der Webressourcen-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="40d5e-112">The web resource request context.</span></span>
[<span data-ttu-id="40d5e-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="40d5e-113">get_Response</span></span>](#get_response) | <span data-ttu-id="40d5e-114">Ein Platzhalter für das Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="40d5e-114">A placeholder for the web resource response object.</span></span>
[<span data-ttu-id="40d5e-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="40d5e-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="40d5e-116">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="40d5e-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="40d5e-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="40d5e-117">put_Response</span></span>](#put_response) | <span data-ttu-id="40d5e-118">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="40d5e-118">Set the Response property.</span></span>

## <span data-ttu-id="40d5e-119">Member</span><span class="sxs-lookup"><span data-stu-id="40d5e-119">Members</span></span>

#### <span data-ttu-id="40d5e-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="40d5e-120">get_Request</span></span> 

<span data-ttu-id="40d5e-121">Die Webressourcen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="40d5e-121">The Web resource request.</span></span>

> <span data-ttu-id="40d5e-122">öffentliche HRESULT- [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="40d5e-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

<span data-ttu-id="40d5e-123">Möglicherweise fehlen dem Anforderungsobjekt einige Überschriften, die später vom Netzwerkstapel hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="40d5e-123">The request object may be missing some headers that are added by network stack later on.</span></span>

#### <span data-ttu-id="40d5e-124">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="40d5e-124">get_ResourceContext</span></span> 

<span data-ttu-id="40d5e-125">Der Webressourcen-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="40d5e-125">The web resource request context.</span></span>

> <span data-ttu-id="40d5e-126">öffentliche HRESULT- [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \*-Kontext)</span><span class="sxs-lookup"><span data-stu-id="40d5e-126">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="40d5e-127">get_Response</span><span class="sxs-lookup"><span data-stu-id="40d5e-127">get_Response</span></span> 

<span data-ttu-id="40d5e-128">Ein Platzhalter für das Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="40d5e-128">A placeholder for the web resource response object.</span></span>

> <span data-ttu-id="40d5e-129">öffentliche HRESULT- [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="40d5e-129">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

<span data-ttu-id="40d5e-130">Wenn dieses Objekt gesetzt ist, wird die Web-Ressourcenanforderung mit dieser Antwort abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="40d5e-130">If this object is set, the web resource request will be completed with this response.</span></span>

#### <span data-ttu-id="40d5e-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="40d5e-131">GetDeferral</span></span> 

<span data-ttu-id="40d5e-132">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="40d5e-132">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="40d5e-133">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="40d5e-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="40d5e-134">Sie können das [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt verwenden, um die Anforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="40d5e-134">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the request at a later time.</span></span>

#### <span data-ttu-id="40d5e-135">put_Response</span><span class="sxs-lookup"><span data-stu-id="40d5e-135">put_Response</span></span> 

<span data-ttu-id="40d5e-136">Festlegen der Response-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="40d5e-136">Set the Response property.</span></span>

> <span data-ttu-id="40d5e-137">öffentliche HRESULT- [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* Response)</span><span class="sxs-lookup"><span data-stu-id="40d5e-137">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

<span data-ttu-id="40d5e-138">Ein leeres Webressourcen-Antwortobjekt kann mit CreateWebResourceResponse erstellt und dann geändert werden, um die Antwort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="40d5e-138">An empty Web resource response object can be created with CreateWebResourceResponse and then modified to construct the response.</span></span>


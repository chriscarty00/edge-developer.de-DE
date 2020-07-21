---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
ms.openlocfilehash: 056667b4ee1995763fee81c8d7a9be31496f7f3e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886533"
---
# <span data-ttu-id="617d3-104">Schnittstellen ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="617d3-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="617d3-105">Ereignis-args für das WebResourceResponseReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="617d3-105">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="617d3-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="617d3-106">Summary</span></span>

 <span data-ttu-id="617d3-107">Member</span><span class="sxs-lookup"><span data-stu-id="617d3-107">Members</span></span>                        | <span data-ttu-id="617d3-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="617d3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="617d3-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="617d3-109">get_Request</span></span>](#get_request) | <span data-ttu-id="617d3-110">Web-Ressourcen Anforderungsobjekt</span><span class="sxs-lookup"><span data-stu-id="617d3-110">Web resource request object.</span></span> <span data-ttu-id="617d3-111">Alle Änderungen an diesem Objekt werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="617d3-111">Any modifications to this object will be ignored.</span></span>
[<span data-ttu-id="617d3-112">get_Response</span><span class="sxs-lookup"><span data-stu-id="617d3-112">get_Response</span></span>](#get_response) | <span data-ttu-id="617d3-113">Webressourcen-Antwortobjekt</span><span class="sxs-lookup"><span data-stu-id="617d3-113">Web resource response object.</span></span>
[<span data-ttu-id="617d3-114">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="617d3-114">PopulateResponseContent</span></span>](#populateresponsecontent) | <span data-ttu-id="617d3-115">Async-Methode, um den Inhaltsdatenstrom der Antwort anzufordern.</span><span class="sxs-lookup"><span data-stu-id="617d3-115">Async method to request the Content stream of the response.</span></span>

<span data-ttu-id="617d3-116">Enthält die Anforderung, während Sie gesendet wurde, und die Antwort, wie Sie empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="617d3-116">Will contain the request as it was sent and the response as it was received.</span></span> <span data-ttu-id="617d3-117">Hinweis: um den Antwort Inhaltsdatenstrom abzurufen, rufen Sie zunächst PopulateResponseContent auf, und warten Sie, bis der asynchrone Aufruf abgeschlossen ist, da andernfalls das zurückgegebene Inhaltsdatenstrom-Objekt NULL ist.</span><span class="sxs-lookup"><span data-stu-id="617d3-117">Note: To get the response content stream, first call PopulateResponseContent and wait for the async call to complete, otherwise the content stream object returned will be null.</span></span>

## <span data-ttu-id="617d3-118">Member</span><span class="sxs-lookup"><span data-stu-id="617d3-118">Members</span></span>

#### <span data-ttu-id="617d3-119">get_Request</span><span class="sxs-lookup"><span data-stu-id="617d3-119">get_Request</span></span> 

<span data-ttu-id="617d3-120">Web-Ressourcen Anforderungsobjekt</span><span class="sxs-lookup"><span data-stu-id="617d3-120">Web resource request object.</span></span> <span data-ttu-id="617d3-121">Alle Änderungen an diesem Objekt werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="617d3-121">Any modifications to this object will be ignored.</span></span>

> <span data-ttu-id="617d3-122">öffentliche HRESULT- [get_Request](#get_request)(ICoreWebView2WebResourceRequest \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="617d3-122">public HRESULT [get_Request](#get_request)(ICoreWebView2WebResourceRequest \*\* request)</span></span>

#### <span data-ttu-id="617d3-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="617d3-123">get_Response</span></span> 

<span data-ttu-id="617d3-124">Webressourcen-Antwortobjekt</span><span class="sxs-lookup"><span data-stu-id="617d3-124">Web resource response object.</span></span>

> <span data-ttu-id="617d3-125">öffentliche HRESULT- [get_Response](#get_response)(ICoreWebView2WebResourceResponse \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="617d3-125">public HRESULT [get_Response](#get_response)(ICoreWebView2WebResourceResponse \*\* response)</span></span>

<span data-ttu-id="617d3-126">Alle Änderungen an diesem Objekt werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="617d3-126">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="617d3-127">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="617d3-127">PopulateResponseContent</span></span> 

<span data-ttu-id="617d3-128">Async-Methode, um den Inhaltsdatenstrom der Antwort anzufordern.</span><span class="sxs-lookup"><span data-stu-id="617d3-128">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="617d3-129">Public HRESULT [PopulateResponseContent](#populateresponsecontent)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \*-Handler)</span><span class="sxs-lookup"><span data-stu-id="617d3-129">public HRESULT [PopulateResponseContent](#populateresponsecontent)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \* handler)</span></span>

```cpp
                    args->PopulateResponseContent(
                        Callback<
                            ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler>(
                            [this, webResourceRequest, webResourceResponse](HRESULT result) {
                                std::wstring message =
                                    L"{ \"kind\": \"event\", \"name\": "
                                    L"\"WebResourceResponseReceived\", \"args\": {"
                                    L"\"request\": " +
                                    RequestToJsonString(webResourceRequest.get()) +
                                    L", "
                                    L"\"response\": " +
                                    ResponseToJsonString(webResourceResponse.get()) + L"}";

                                message +=
                                    WebViewPropertiesToJsonString(m_webviewEventSource.get());
                                message += L"}";
                                PostEventMessage(message);
                                return S_OK;
                            })
                            .Get());
```


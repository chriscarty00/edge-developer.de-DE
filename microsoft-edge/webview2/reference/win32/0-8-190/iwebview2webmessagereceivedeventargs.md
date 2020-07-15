---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: d70162803cfb2f9d1f0cfbf7e7397ee1cdbeec0e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878190"
---
# <span data-ttu-id="1e510-104">0.8.355-Interface-IWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1e510-104">0.8.355 - interface IWebView2WebMessageReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="1e510-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="1e510-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="1e510-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="1e510-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="1e510-107">Ereignis-args für das WebMessageReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1e510-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="1e510-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1e510-108">Summary</span></span>

 <span data-ttu-id="1e510-109">Member</span><span class="sxs-lookup"><span data-stu-id="1e510-109">Members</span></span>                        | <span data-ttu-id="1e510-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1e510-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1e510-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="1e510-111">get_Source</span></span>](#get_source) | <span data-ttu-id="1e510-112">Der URI des Dokuments, das diese Webnachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="1e510-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="1e510-113">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="1e510-113">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="1e510-114">Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1e510-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="1e510-115">get_WebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="1e510-115">get_WebMessageAsString</span></span>](#get_webmessageasstring) | <span data-ttu-id="1e510-116">Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="1e510-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="1e510-117">Member</span><span class="sxs-lookup"><span data-stu-id="1e510-117">Members</span></span>

#### <span data-ttu-id="1e510-118">get_Source</span><span class="sxs-lookup"><span data-stu-id="1e510-118">get_Source</span></span> 

<span data-ttu-id="1e510-119">Der URI des Dokuments, das diese Webnachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="1e510-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="1e510-120">öffentliche HRESULT- [get_Source](#get_source)(LPWSTR \* Source)</span><span class="sxs-lookup"><span data-stu-id="1e510-120">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="1e510-121">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="1e510-121">get_WebMessageAsJson</span></span> 

<span data-ttu-id="1e510-122">Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1e510-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="1e510-123">Public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="1e510-123">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="1e510-124">Verwenden Sie diese, um über JavaScript-Objekte zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1e510-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="1e510-125">Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsJson-Werten:</span><span class="sxs-lookup"><span data-stu-id="1e510-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="1e510-126">get_WebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="1e510-126">get_WebMessageAsString</span></span> 

<span data-ttu-id="1e510-127">Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="1e510-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="1e510-128">Public HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR \* WebMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="1e510-128">public HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="1e510-129">Wenn die gesendete Nachricht eine andere Art von JavaScript-Typ ist, schlägt diese Methode mit E_INVALIDARG fehl.</span><span class="sxs-lookup"><span data-stu-id="1e510-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="1e510-130">Verwenden Sie diese, um über einfache Zeichenfolgen zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1e510-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="1e510-131">Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsString-Werten:</span><span class="sxs-lookup"><span data-stu-id="1e510-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c7d3d03fc1a0d53db403dab6c91dcdcf5ad6fd28
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698891"
---
# <span data-ttu-id="189c2-104">Schnittstellen ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="189c2-104">interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="189c2-105">Ereignis-args für das WebMessageReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="189c2-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="189c2-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="189c2-106">Summary</span></span>

 <span data-ttu-id="189c2-107">Member</span><span class="sxs-lookup"><span data-stu-id="189c2-107">Members</span></span>                        | <span data-ttu-id="189c2-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="189c2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="189c2-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="189c2-109">get_Source</span></span>](#get_source) | <span data-ttu-id="189c2-110">Der URI des Dokuments, das diese Webnachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="189c2-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="189c2-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="189c2-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="189c2-112">Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="189c2-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="189c2-113">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="189c2-113">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="189c2-114">Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="189c2-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="189c2-115">Member</span><span class="sxs-lookup"><span data-stu-id="189c2-115">Members</span></span>

#### <span data-ttu-id="189c2-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="189c2-116">get_Source</span></span> 

<span data-ttu-id="189c2-117">Der URI des Dokuments, das diese Webnachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="189c2-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="189c2-118">öffentliche HRESULT- [get_Source](#get_source)(LPWSTR \* Source)</span><span class="sxs-lookup"><span data-stu-id="189c2-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="189c2-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="189c2-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="189c2-120">Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="189c2-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="189c2-121">Public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="189c2-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="189c2-122">Verwenden Sie diese, um über JavaScript-Objekte zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="189c2-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="189c2-123">Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsJson-Werten:</span><span class="sxs-lookup"><span data-stu-id="189c2-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="189c2-124">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="189c2-124">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="189c2-125">Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="189c2-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="189c2-126">Public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="189c2-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="189c2-127">Wenn die gesendete Nachricht eine andere Art von JavaScript-Typ ist, schlägt diese Methode mit E_INVALIDARG fehl.</span><span class="sxs-lookup"><span data-stu-id="189c2-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="189c2-128">Verwenden Sie diese, um über einfache Zeichenfolgen zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="189c2-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="189c2-129">Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsString-Werten:</span><span class="sxs-lookup"><span data-stu-id="189c2-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```


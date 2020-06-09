---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b917f309194316b26ee94aa94dc8289ef4430007
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697539"
---
# <span data-ttu-id="49618-104">Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="49618-104">Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="49618-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="49618-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="49618-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="49618-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="49618-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="49618-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="49618-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="49618-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="49618-109">Ereignis-args für das WebMessageReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="49618-109">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="49618-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="49618-110">Summary</span></span>

 <span data-ttu-id="49618-111">Member</span><span class="sxs-lookup"><span data-stu-id="49618-111">Members</span></span>                        | <span data-ttu-id="49618-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="49618-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49618-113">Source</span><span class="sxs-lookup"><span data-stu-id="49618-113">Source</span></span>](#source) | <span data-ttu-id="49618-114">Der URI des Dokuments, das diese Webnachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="49618-114">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="49618-115">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="49618-115">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="49618-116">Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="49618-116">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="49618-117">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="49618-117">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="49618-118">Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="49618-118">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="49618-119">Member</span><span class="sxs-lookup"><span data-stu-id="49618-119">Members</span></span>

#### <span data-ttu-id="49618-120">Source</span><span class="sxs-lookup"><span data-stu-id="49618-120">Source</span></span> 

<span data-ttu-id="49618-121">Der URI des Dokuments, das diese Webnachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="49618-121">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="49618-122">öffentliche Zeichenfolgen [Quelle](#source)</span><span class="sxs-lookup"><span data-stu-id="49618-122">public string [Source](#source)</span></span>

#### <span data-ttu-id="49618-123">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="49618-123">WebMessageAsJson</span></span> 

<span data-ttu-id="49618-124">Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="49618-124">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="49618-125">public String [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="49618-125">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="49618-126">Verwenden Sie diese, um über JavaScript-Objekte zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="49618-126">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="49618-127">Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsJson-Werten:</span><span class="sxs-lookup"><span data-stu-id="49618-127">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="49618-128">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="49618-128">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="49618-129">Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="49618-129">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="49618-130">public String [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="49618-130">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="49618-131">Wenn die gesendete Nachricht eine andere Art von JavaScript-Typ ist, schlägt diese Methode mit E_INVALIDARG fehl.</span><span class="sxs-lookup"><span data-stu-id="49618-131">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="49618-132">Verwenden Sie diese, um über einfache Zeichenfolgen zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="49618-132">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="49618-133">Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsString-Werten:</span><span class="sxs-lookup"><span data-stu-id="49618-133">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```


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
ms.openlocfilehash: f9bedb19620b0669d4aac35be4786702940b2a72
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653799"
---
# <span data-ttu-id="7a76f-104">Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="7a76f-104">Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

<span data-ttu-id="7a76f-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="7a76f-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="7a76f-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="7a76f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="7a76f-107">Ereignis-args für das WebMessageReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7a76f-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="7a76f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7a76f-108">Summary</span></span>

 <span data-ttu-id="7a76f-109">Member</span><span class="sxs-lookup"><span data-stu-id="7a76f-109">Members</span></span>                        | <span data-ttu-id="7a76f-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7a76f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a76f-111">Source</span><span class="sxs-lookup"><span data-stu-id="7a76f-111">Source</span></span>](#source) | <span data-ttu-id="7a76f-112">Der URI des Dokuments, das diese Webnachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="7a76f-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="7a76f-113">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="7a76f-113">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="7a76f-114">Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7a76f-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="7a76f-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="7a76f-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="7a76f-116">Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="7a76f-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="7a76f-117">Member</span><span class="sxs-lookup"><span data-stu-id="7a76f-117">Members</span></span>

#### <span data-ttu-id="7a76f-118">Source</span><span class="sxs-lookup"><span data-stu-id="7a76f-118">Source</span></span> 

<span data-ttu-id="7a76f-119">Der URI des Dokuments, das diese Webnachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="7a76f-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="7a76f-120">öffentliche Zeichenfolgen [Quelle](#source)</span><span class="sxs-lookup"><span data-stu-id="7a76f-120">public string [Source](#source)</span></span>

#### <span data-ttu-id="7a76f-121">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="7a76f-121">WebMessageAsJson</span></span> 

<span data-ttu-id="7a76f-122">Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7a76f-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="7a76f-123">public String [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="7a76f-123">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="7a76f-124">Verwenden Sie diese, um über JavaScript-Objekte zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="7a76f-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="7a76f-125">Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsJson-Werten:</span><span class="sxs-lookup"><span data-stu-id="7a76f-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="7a76f-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="7a76f-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="7a76f-127">Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="7a76f-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="7a76f-128">public String [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="7a76f-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="7a76f-129">Wenn die gesendete Nachricht eine andere Art von JavaScript-Typ ist, schlägt diese Methode mit E_INVALIDARG fehl.</span><span class="sxs-lookup"><span data-stu-id="7a76f-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="7a76f-130">Verwenden Sie diese, um über einfache Zeichenfolgen zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="7a76f-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="7a76f-131">Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsString-Werten:</span><span class="sxs-lookup"><span data-stu-id="7a76f-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```


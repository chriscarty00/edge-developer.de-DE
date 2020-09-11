---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: ab273337307eeef6e8842d337296756877939aff
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012046"
---
# <span data-ttu-id="77a7a-104">Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="77a7a-104">Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

<span data-ttu-id="77a7a-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="77a7a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="77a7a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="77a7a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="77a7a-107">Ereignis-args für das WebMessageReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="77a7a-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="77a7a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="77a7a-108">Summary</span></span>

 <span data-ttu-id="77a7a-109">Member</span><span class="sxs-lookup"><span data-stu-id="77a7a-109">Members</span></span>                        | <span data-ttu-id="77a7a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="77a7a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="77a7a-111">Source</span><span class="sxs-lookup"><span data-stu-id="77a7a-111">Source</span></span>](#source) | <span data-ttu-id="77a7a-112">Der URI des Dokuments, das diese Webnachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="77a7a-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="77a7a-113">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="77a7a-113">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="77a7a-114">Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="77a7a-114">The message posted from the WebView content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="77a7a-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="77a7a-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="77a7a-116">Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="77a7a-116">If the message posted from the WebView content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="77a7a-117">Member</span><span class="sxs-lookup"><span data-stu-id="77a7a-117">Members</span></span>

#### <span data-ttu-id="77a7a-118">Source</span><span class="sxs-lookup"><span data-stu-id="77a7a-118">Source</span></span> 

<span data-ttu-id="77a7a-119">Der URI des Dokuments, das diese Webnachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="77a7a-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="77a7a-120">öffentliche Zeichenfolgen [Quelle](#source)</span><span class="sxs-lookup"><span data-stu-id="77a7a-120">public string [Source](#source)</span></span>

#### <span data-ttu-id="77a7a-121">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="77a7a-121">WebMessageAsJson</span></span> 

<span data-ttu-id="77a7a-122">Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="77a7a-122">The message posted from the WebView content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="77a7a-123">public String [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="77a7a-123">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="77a7a-124">Verwenden Sie diese, um über JavaScript-Objekte zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="77a7a-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="77a7a-125">Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsJson-Werten:</span><span class="sxs-lookup"><span data-stu-id="77a7a-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="77a7a-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="77a7a-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="77a7a-127">Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="77a7a-127">If the message posted from the WebView content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="77a7a-128">public String [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="77a7a-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="77a7a-129">Wenn die gesendete Nachricht eine andere Art von JavaScript-Typ ist, schlägt diese Methode mit E_INVALIDARG fehl.</span><span class="sxs-lookup"><span data-stu-id="77a7a-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="77a7a-130">Verwenden Sie diese, um über einfache Zeichenfolgen zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="77a7a-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="77a7a-131">Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsString-Werten:</span><span class="sxs-lookup"><span data-stu-id="77a7a-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```


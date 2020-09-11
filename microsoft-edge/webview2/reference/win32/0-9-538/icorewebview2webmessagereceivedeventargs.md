---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: 58bb4b7f34b2917ec16ead051d1df8d6e6885f6d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010383"
---
# <span data-ttu-id="a7d3c-104">0.9.579-Interface-ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a7d3c-104">0.9.579 - interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="a7d3c-105">Ereignis-args für das WebMessageReceived-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a7d3c-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="a7d3c-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a7d3c-106">Summary</span></span>

 <span data-ttu-id="a7d3c-107">Member</span><span class="sxs-lookup"><span data-stu-id="a7d3c-107">Members</span></span>                        | <span data-ttu-id="a7d3c-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a7d3c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a7d3c-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="a7d3c-109">get_Source</span></span>](#get_source) | <span data-ttu-id="a7d3c-110">Der URI des Dokuments, das diese Webnachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="a7d3c-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="a7d3c-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="a7d3c-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="a7d3c-112">Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a7d3c-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="a7d3c-113">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="a7d3c-113">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="a7d3c-114">Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="a7d3c-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="a7d3c-115">Member</span><span class="sxs-lookup"><span data-stu-id="a7d3c-115">Members</span></span>

#### <span data-ttu-id="a7d3c-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="a7d3c-116">get_Source</span></span> 

<span data-ttu-id="a7d3c-117">Der URI des Dokuments, das diese Webnachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="a7d3c-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="a7d3c-118">öffentliche HRESULT- [get_Source](#get_source)(LPWSTR \* Source)</span><span class="sxs-lookup"><span data-stu-id="a7d3c-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="a7d3c-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="a7d3c-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="a7d3c-120">Die Nachricht, die vom WebView-Inhalt an den Host gesendet wurde, der in eine JSON-Zeichenfolge konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a7d3c-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="a7d3c-121">Public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="a7d3c-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="a7d3c-122">Verwenden Sie diese, um über JavaScript-Objekte zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="a7d3c-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="a7d3c-123">Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsJson-Werten:</span><span class="sxs-lookup"><span data-stu-id="a7d3c-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="a7d3c-124">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="a7d3c-124">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="a7d3c-125">Wenn die vom WebView-Inhalt an den Host gesendete Nachricht ein Zeichenfolgentyp ist, gibt diese Methode den Wert dieser Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="a7d3c-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="a7d3c-126">Public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="a7d3c-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="a7d3c-127">Wenn die gesendete Nachricht eine andere Art von JavaScript-Typ ist, schlägt diese Methode mit E_INVALIDARG fehl.</span><span class="sxs-lookup"><span data-stu-id="a7d3c-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="a7d3c-128">Verwenden Sie diese, um über einfache Zeichenfolgen zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="a7d3c-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="a7d3c-129">Beispielsweise führen die folgenden PostMessage-Aufrufe zu den folgenden WebMessageAsString-Werten:</span><span class="sxs-lookup"><span data-stu-id="a7d3c-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```


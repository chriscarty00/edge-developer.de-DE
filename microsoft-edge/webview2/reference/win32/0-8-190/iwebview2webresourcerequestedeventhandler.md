---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: c0980f26ef06497cded81e2f9c7c00162af18d9b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878092"
---
# <span data-ttu-id="7e7c8-104">0.8.355-Interface-IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7e7c8-104">0.8.355 - interface IWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7e7c8-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="7e7c8-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="7e7c8-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="7e7c8-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="7e7c8-107">Wird ausgelöst, wenn eine HTTP-Anforderung in der WebView erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7e7c8-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="7e7c8-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7e7c8-108">Summary</span></span>

 <span data-ttu-id="7e7c8-109">Member</span><span class="sxs-lookup"><span data-stu-id="7e7c8-109">Members</span></span>                        | <span data-ttu-id="7e7c8-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7e7c8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7e7c8-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="7e7c8-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7e7c8-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7e7c8-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="7e7c8-113">Der Host kann Anforderung, Antwortheader und Antwortinhalt außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="7e7c8-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="7e7c8-114">Member</span><span class="sxs-lookup"><span data-stu-id="7e7c8-114">Members</span></span>

#### <span data-ttu-id="7e7c8-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="7e7c8-115">Invoke</span></span> 

<span data-ttu-id="7e7c8-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7e7c8-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7e7c8-117">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7e7c8-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>


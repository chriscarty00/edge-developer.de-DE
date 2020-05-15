---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 602c00258e9ff3362269ebe90de8306ecbd7503e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653767"
---
# <span data-ttu-id="66782-104">Schnittstellen IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="66782-104">interface IWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="66782-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="66782-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="66782-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="66782-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="66782-107">Wird ausgelöst, wenn eine HTTP-Anforderung in der WebView erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="66782-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="66782-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="66782-108">Summary</span></span>

 <span data-ttu-id="66782-109">Member</span><span class="sxs-lookup"><span data-stu-id="66782-109">Members</span></span>                        | <span data-ttu-id="66782-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="66782-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="66782-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="66782-111">Invoke</span></span>](#invoke) | <span data-ttu-id="66782-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="66782-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="66782-113">Der Host kann Anforderung, Antwortheader und Antwortinhalt außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="66782-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="66782-114">Member</span><span class="sxs-lookup"><span data-stu-id="66782-114">Members</span></span>

#### <span data-ttu-id="66782-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="66782-115">Invoke</span></span> 

<span data-ttu-id="66782-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="66782-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="66782-117">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="66782-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: d2b1aa9bbfc15aa44023a43425bb2fc939165cae
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880157"
---
# <span data-ttu-id="c5ba6-104">0.9.430-Interface-ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c5ba6-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="c5ba6-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="c5ba6-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="c5ba6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="c5ba6-107">Wird ausgelöst, wenn eine HTTP-Anforderung in der WebView erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="c5ba6-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c5ba6-108">Summary</span></span>

 <span data-ttu-id="c5ba6-109">Member</span><span class="sxs-lookup"><span data-stu-id="c5ba6-109">Members</span></span>                        | <span data-ttu-id="c5ba6-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c5ba6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c5ba6-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="c5ba6-111">Invoke</span></span>](#invoke) | <span data-ttu-id="c5ba6-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c5ba6-113">Der Host kann Anforderung, Antwortheader und Antwortinhalt außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="c5ba6-114">Member</span><span class="sxs-lookup"><span data-stu-id="c5ba6-114">Members</span></span>

#### <span data-ttu-id="c5ba6-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="c5ba6-115">Invoke</span></span> 

<span data-ttu-id="c5ba6-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c5ba6-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c5ba6-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>


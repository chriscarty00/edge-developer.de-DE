---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: d35e21fde7788b1df5b201f8690196ecd0d82a34
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884092"
---
# <span data-ttu-id="64af2-104">0.9.430-Interface-ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="64af2-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="64af2-105">Wird ausgelöst, wenn eine HTTP-Anforderung in der WebView erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="64af2-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="64af2-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="64af2-106">Summary</span></span>

 <span data-ttu-id="64af2-107">Member</span><span class="sxs-lookup"><span data-stu-id="64af2-107">Members</span></span>                        | <span data-ttu-id="64af2-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="64af2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="64af2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="64af2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="64af2-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="64af2-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="64af2-111">Der Host kann Anforderung, Antwortheader und Antwortinhalt außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="64af2-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="64af2-112">Member</span><span class="sxs-lookup"><span data-stu-id="64af2-112">Members</span></span>

#### <span data-ttu-id="64af2-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="64af2-113">Invoke</span></span> 

<span data-ttu-id="64af2-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="64af2-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="64af2-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="64af2-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>


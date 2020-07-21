---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 70ecc1898f9a72656f12b912d103116c381d4218
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885674"
---
# <span data-ttu-id="d9f7a-104">0.8.355-Interface-IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d9f7a-104">0.8.355 - interface IWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="d9f7a-105">Wird ausgelöst, wenn eine HTTP-Anforderung in der WebView erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d9f7a-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="d9f7a-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d9f7a-106">Summary</span></span>

 <span data-ttu-id="d9f7a-107">Member</span><span class="sxs-lookup"><span data-stu-id="d9f7a-107">Members</span></span>                        | <span data-ttu-id="d9f7a-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d9f7a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d9f7a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d9f7a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d9f7a-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d9f7a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="d9f7a-111">Der Host kann Anforderung, Antwortheader und Antwortinhalt außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="d9f7a-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="d9f7a-112">Member</span><span class="sxs-lookup"><span data-stu-id="d9f7a-112">Members</span></span>

#### <span data-ttu-id="d9f7a-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="d9f7a-113">Invoke</span></span> 

<span data-ttu-id="d9f7a-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d9f7a-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d9f7a-115">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d9f7a-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>


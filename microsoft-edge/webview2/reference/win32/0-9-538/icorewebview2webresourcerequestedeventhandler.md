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
ms.openlocfilehash: 64f29f8c771a14d569fd45f7359614795bbc0386
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698917"
---
# <span data-ttu-id="10c02-104">Schnittstellen ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="10c02-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="10c02-105">Wird ausgelöst, wenn eine HTTP-Anforderung in der WebView erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="10c02-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="10c02-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="10c02-106">Summary</span></span>

 <span data-ttu-id="10c02-107">Member</span><span class="sxs-lookup"><span data-stu-id="10c02-107">Members</span></span>                        | <span data-ttu-id="10c02-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="10c02-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10c02-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="10c02-109">Invoke</span></span>](#invoke) | <span data-ttu-id="10c02-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="10c02-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="10c02-111">Der Host kann Anforderung, Antwortheader und Antwortinhalt außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="10c02-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="10c02-112">Member</span><span class="sxs-lookup"><span data-stu-id="10c02-112">Members</span></span>

#### <span data-ttu-id="10c02-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="10c02-113">Invoke</span></span> 

<span data-ttu-id="10c02-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="10c02-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="10c02-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="10c02-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>


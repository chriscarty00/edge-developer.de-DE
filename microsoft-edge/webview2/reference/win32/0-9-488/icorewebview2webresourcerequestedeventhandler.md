---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 2f3effd612303d1532c7220d566791a800753b37
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653750"
---
# <span data-ttu-id="80b82-104">Schnittstellen ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="80b82-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="80b82-105">Wird ausgelöst, wenn eine HTTP-Anforderung in der WebView erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="80b82-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="80b82-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="80b82-106">Summary</span></span>

 <span data-ttu-id="80b82-107">Member</span><span class="sxs-lookup"><span data-stu-id="80b82-107">Members</span></span>                        | <span data-ttu-id="80b82-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="80b82-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="80b82-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="80b82-109">Invoke</span></span>](#invoke) | <span data-ttu-id="80b82-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="80b82-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="80b82-111">Der Host kann Anforderung, Antwortheader und Antwortinhalt außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="80b82-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="80b82-112">Member</span><span class="sxs-lookup"><span data-stu-id="80b82-112">Members</span></span>

#### <span data-ttu-id="80b82-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="80b82-113">Invoke</span></span> 

<span data-ttu-id="80b82-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="80b82-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="80b82-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="80b82-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>


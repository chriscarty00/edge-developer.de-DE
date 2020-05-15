---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c4f76c468cc5001c9eae347247dd5ffb8a60594f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654066"
---
# <span data-ttu-id="78cd2-104">Schnittstellen ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="78cd2-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="78cd2-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="78cd2-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="78cd2-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="78cd2-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="78cd2-107">Wird ausgelöst, wenn eine HTTP-Anforderung in der WebView erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="78cd2-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="78cd2-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="78cd2-108">Summary</span></span>

 <span data-ttu-id="78cd2-109">Member</span><span class="sxs-lookup"><span data-stu-id="78cd2-109">Members</span></span>                        | <span data-ttu-id="78cd2-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="78cd2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="78cd2-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="78cd2-111">Invoke</span></span>](#invoke) | <span data-ttu-id="78cd2-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="78cd2-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="78cd2-113">Der Host kann Anforderung, Antwortheader und Antwortinhalt außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="78cd2-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="78cd2-114">Member</span><span class="sxs-lookup"><span data-stu-id="78cd2-114">Members</span></span>

#### <span data-ttu-id="78cd2-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="78cd2-115">Invoke</span></span> 

<span data-ttu-id="78cd2-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="78cd2-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="78cd2-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="78cd2-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>


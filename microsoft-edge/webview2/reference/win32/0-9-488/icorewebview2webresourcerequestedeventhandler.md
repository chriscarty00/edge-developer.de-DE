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
ms.openlocfilehash: 622a7e93912a3380cc0d7dabae9293734cd3fcfa
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697938"
---
# <span data-ttu-id="cb49e-104">Schnittstellen ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="cb49e-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="cb49e-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="cb49e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="cb49e-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="cb49e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="cb49e-107">Wird ausgelöst, wenn eine HTTP-Anforderung in der WebView erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cb49e-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="cb49e-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="cb49e-108">Summary</span></span>

 <span data-ttu-id="cb49e-109">Member</span><span class="sxs-lookup"><span data-stu-id="cb49e-109">Members</span></span>                        | <span data-ttu-id="cb49e-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="cb49e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cb49e-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="cb49e-111">Invoke</span></span>](#invoke) | <span data-ttu-id="cb49e-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cb49e-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="cb49e-113">Der Host kann Anforderung, Antwortheader und Antwortinhalt außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="cb49e-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="cb49e-114">Member</span><span class="sxs-lookup"><span data-stu-id="cb49e-114">Members</span></span>

#### <span data-ttu-id="cb49e-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="cb49e-115">Invoke</span></span> 

<span data-ttu-id="cb49e-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cb49e-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="cb49e-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="cb49e-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>


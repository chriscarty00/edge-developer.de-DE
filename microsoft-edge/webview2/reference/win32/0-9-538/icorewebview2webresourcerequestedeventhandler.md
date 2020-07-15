---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 9cd221ac1b528b0be52201daa0c15217534944a6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879226"
---
# <span data-ttu-id="25df9-104">Schnittstellen ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="25df9-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="25df9-105">Wird ausgelöst, wenn eine HTTP-Anforderung in der WebView erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="25df9-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="25df9-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="25df9-106">Summary</span></span>

 <span data-ttu-id="25df9-107">Member</span><span class="sxs-lookup"><span data-stu-id="25df9-107">Members</span></span>                        | <span data-ttu-id="25df9-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="25df9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="25df9-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="25df9-109">Invoke</span></span>](#invoke) | <span data-ttu-id="25df9-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="25df9-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="25df9-111">Der Host kann Anforderung, Antwortheader und Antwortinhalt außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="25df9-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="25df9-112">Member</span><span class="sxs-lookup"><span data-stu-id="25df9-112">Members</span></span>

#### <span data-ttu-id="25df9-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="25df9-113">Invoke</span></span> 

<span data-ttu-id="25df9-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="25df9-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="25df9-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="25df9-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>


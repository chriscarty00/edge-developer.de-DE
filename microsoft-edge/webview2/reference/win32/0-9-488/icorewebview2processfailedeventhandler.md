---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 56e66d109b6ae39e1f3937c643dc90ef71c5ecb2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880346"
---
# <span data-ttu-id="93305-104">0.9.515-Interface-ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="93305-104">0.9.515 - interface ICoreWebView2ProcessFailedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="93305-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="93305-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="93305-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="93305-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="93305-107">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ProcessFailed-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="93305-107">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="93305-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="93305-108">Summary</span></span>

 <span data-ttu-id="93305-109">Member</span><span class="sxs-lookup"><span data-stu-id="93305-109">Members</span></span>                        | <span data-ttu-id="93305-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="93305-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="93305-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="93305-111">Invoke</span></span>](#invoke) | <span data-ttu-id="93305-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="93305-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="93305-113">Member</span><span class="sxs-lookup"><span data-stu-id="93305-113">Members</span></span>

#### <span data-ttu-id="93305-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="93305-114">Invoke</span></span> 

<span data-ttu-id="93305-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="93305-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="93305-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="93305-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>


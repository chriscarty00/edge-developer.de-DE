---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 6ec01c2b66c625c9961384b5c2ef04a8820a29e9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880479"
---
# <span data-ttu-id="d0aa1-104">0.9.515-Interface-ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="d0aa1-104">0.9.515 - interface ICoreWebView2NavigationStartingEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="d0aa1-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="d0aa1-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="d0aa1-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="d0aa1-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="d0aa1-107">Der Aufrufer implementiert diese Schnittstelle, um das NavigationStarting-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d0aa1-107">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="d0aa1-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d0aa1-108">Summary</span></span>

 <span data-ttu-id="d0aa1-109">Member</span><span class="sxs-lookup"><span data-stu-id="d0aa1-109">Members</span></span>                        | <span data-ttu-id="d0aa1-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d0aa1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d0aa1-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="d0aa1-111">Invoke</span></span>](#invoke) | <span data-ttu-id="d0aa1-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d0aa1-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d0aa1-113">Member</span><span class="sxs-lookup"><span data-stu-id="d0aa1-113">Members</span></span>

#### <span data-ttu-id="d0aa1-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="d0aa1-114">Invoke</span></span> 

<span data-ttu-id="d0aa1-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d0aa1-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d0aa1-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d0aa1-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span></span>


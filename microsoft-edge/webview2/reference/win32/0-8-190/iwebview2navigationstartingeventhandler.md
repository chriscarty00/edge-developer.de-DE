---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 14fe3e2260412a861ef07726309ed4df29f2a60b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878372"
---
# <span data-ttu-id="abd0f-104">0.8.355-Interface-IWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="abd0f-104">0.8.355 - interface IWebView2NavigationStartingEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="abd0f-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="abd0f-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="abd0f-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="abd0f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="abd0f-107">Der Aufrufer implementiert diese Schnittstelle, um das NavigationStarting-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="abd0f-107">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="abd0f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="abd0f-108">Summary</span></span>

 <span data-ttu-id="abd0f-109">Member</span><span class="sxs-lookup"><span data-stu-id="abd0f-109">Members</span></span>                        | <span data-ttu-id="abd0f-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="abd0f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="abd0f-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="abd0f-111">Invoke</span></span>](#invoke) | <span data-ttu-id="abd0f-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="abd0f-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="abd0f-113">Member</span><span class="sxs-lookup"><span data-stu-id="abd0f-113">Members</span></span>

#### <span data-ttu-id="abd0f-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="abd0f-114">Invoke</span></span> 

<span data-ttu-id="abd0f-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="abd0f-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="abd0f-116">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NavigationStartingEventArgs](IWebView2NavigationStartingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="abd0f-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NavigationStartingEventArgs](IWebView2NavigationStartingEventArgs.md) \* args)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: a3452d30edc595a6d7b2a8b45fb283073d079749
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653732"
---
# <span data-ttu-id="262d9-104">Schnittstellen IWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="262d9-104">interface IWebView2ProcessFailedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="262d9-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="262d9-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="262d9-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="262d9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="262d9-107">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ProcessFailed-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="262d9-107">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="262d9-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="262d9-108">Summary</span></span>

 <span data-ttu-id="262d9-109">Member</span><span class="sxs-lookup"><span data-stu-id="262d9-109">Members</span></span>                        | <span data-ttu-id="262d9-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="262d9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="262d9-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="262d9-111">Invoke</span></span>](#invoke) | <span data-ttu-id="262d9-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="262d9-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="262d9-113">Member</span><span class="sxs-lookup"><span data-stu-id="262d9-113">Members</span></span>

#### <span data-ttu-id="262d9-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="262d9-114">Invoke</span></span> 

<span data-ttu-id="262d9-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="262d9-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="262d9-116">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="262d9-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) \* args)</span></span>


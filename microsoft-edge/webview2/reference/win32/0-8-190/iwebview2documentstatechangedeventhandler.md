---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: b669d04ba46b1670610e1efb00b552b2b6b1a4fc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878568"
---
# <span data-ttu-id="3917b-104">0.8.355-Interface-IWebView2DocumentStateChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3917b-104">0.8.355 - interface IWebView2DocumentStateChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="3917b-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="3917b-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="3917b-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="3917b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="3917b-107">Der Aufrufer implementiert diese Schnittstelle, um das DocumentStateChanged-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="3917b-107">The caller implements this interface to receive the DocumentStateChanged event.</span></span>

## <span data-ttu-id="3917b-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3917b-108">Summary</span></span>

 <span data-ttu-id="3917b-109">Member</span><span class="sxs-lookup"><span data-stu-id="3917b-109">Members</span></span>                        | <span data-ttu-id="3917b-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3917b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3917b-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="3917b-111">Invoke</span></span>](#invoke) | <span data-ttu-id="3917b-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3917b-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3917b-113">Member</span><span class="sxs-lookup"><span data-stu-id="3917b-113">Members</span></span>

#### <span data-ttu-id="3917b-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="3917b-114">Invoke</span></span> 

<span data-ttu-id="3917b-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3917b-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3917b-116">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3917b-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span></span>


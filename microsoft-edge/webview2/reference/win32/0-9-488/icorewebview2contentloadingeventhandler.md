---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 6f817fd5e602582c47c2785459d2a3987174a7b8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880773"
---
# <span data-ttu-id="b038d-104">0.9.515-Interface-ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="b038d-104">0.9.515 - interface ICoreWebView2ContentLoadingEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="b038d-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="b038d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b038d-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="b038d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="b038d-107">Der Aufrufer implementiert diese Schnittstelle, um das ContentLoading-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b038d-107">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="b038d-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b038d-108">Summary</span></span>

 <span data-ttu-id="b038d-109">Member</span><span class="sxs-lookup"><span data-stu-id="b038d-109">Members</span></span>                        | <span data-ttu-id="b038d-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b038d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b038d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="b038d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="b038d-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b038d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b038d-113">Member</span><span class="sxs-lookup"><span data-stu-id="b038d-113">Members</span></span>

#### <span data-ttu-id="b038d-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="b038d-114">Invoke</span></span> 

<span data-ttu-id="b038d-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b038d-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b038d-116">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b038d-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>


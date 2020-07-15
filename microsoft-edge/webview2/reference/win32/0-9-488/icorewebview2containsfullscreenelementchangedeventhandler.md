---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ff5cedad802f0f367e694ddf5c62290276fa4aa4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880920"
---
# <span data-ttu-id="eb356-104">0.9.515-Interface-ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="eb356-104">0.9.515 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="eb356-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="eb356-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="eb356-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="eb356-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="eb356-107">Der Aufrufer implementiert diese Methode, um die ContainsFullScreenElementChanged-Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="eb356-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="eb356-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="eb356-108">Summary</span></span>

 <span data-ttu-id="eb356-109">Member</span><span class="sxs-lookup"><span data-stu-id="eb356-109">Members</span></span>                        | <span data-ttu-id="eb356-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="eb356-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eb356-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="eb356-111">Invoke</span></span>](#invoke) | <span data-ttu-id="eb356-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eb356-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="eb356-113">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="eb356-113">There are no event args for this event.</span></span>

## <span data-ttu-id="eb356-114">Member</span><span class="sxs-lookup"><span data-stu-id="eb356-114">Members</span></span>

#### <span data-ttu-id="eb356-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="eb356-115">Invoke</span></span> 

<span data-ttu-id="eb356-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eb356-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="eb356-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="eb356-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="eb356-118">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="eb356-118">There are no event args and the args parameter will be null.</span></span>


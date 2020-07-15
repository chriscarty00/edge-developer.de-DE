---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 1d9d6618d7720fe2d5b44cbeef22b2c2e526d3bc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880486"
---
# <span data-ttu-id="eafde-104">0.9.515-Interface-ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="eafde-104">0.9.515 - interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="eafde-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="eafde-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="eafde-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="eafde-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="eafde-107">Der Aufrufer implementiert diese Schnittstelle, um das NavigationCompleted-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="eafde-107">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="eafde-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="eafde-108">Summary</span></span>

 <span data-ttu-id="eafde-109">Member</span><span class="sxs-lookup"><span data-stu-id="eafde-109">Members</span></span>                        | <span data-ttu-id="eafde-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="eafde-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eafde-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="eafde-111">Invoke</span></span>](#invoke) | <span data-ttu-id="eafde-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eafde-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="eafde-113">Member</span><span class="sxs-lookup"><span data-stu-id="eafde-113">Members</span></span>

#### <span data-ttu-id="eafde-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="eafde-114">Invoke</span></span> 

<span data-ttu-id="eafde-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eafde-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="eafde-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="eafde-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>


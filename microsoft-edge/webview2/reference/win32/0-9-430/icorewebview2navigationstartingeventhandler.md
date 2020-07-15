---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 161e36312c5acb8612c9399178917158807012a7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877868"
---
# <span data-ttu-id="d3a88-104">0.9.430-Interface-ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="d3a88-104">0.9.430 - interface ICoreWebView2NavigationStartingEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="d3a88-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="d3a88-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d3a88-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="d3a88-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="d3a88-107">Der Aufrufer implementiert diese Schnittstelle, um das NavigationStarting-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d3a88-107">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="d3a88-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d3a88-108">Summary</span></span>

 <span data-ttu-id="d3a88-109">Member</span><span class="sxs-lookup"><span data-stu-id="d3a88-109">Members</span></span>                        | <span data-ttu-id="d3a88-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d3a88-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d3a88-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="d3a88-111">Invoke</span></span>](#invoke) | <span data-ttu-id="d3a88-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d3a88-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d3a88-113">Member</span><span class="sxs-lookup"><span data-stu-id="d3a88-113">Members</span></span>

#### <span data-ttu-id="d3a88-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="d3a88-114">Invoke</span></span> 

<span data-ttu-id="d3a88-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d3a88-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d3a88-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2NavigationStartingEventArgs](ICoreWebView2NavigationStartingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d3a88-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationStartingEventArgs](ICoreWebView2NavigationStartingEventArgs.md) \* args)</span></span>


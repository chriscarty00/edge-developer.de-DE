---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 14c238a5a625e40e9abba3d786d6b80aef8f7773
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877833"
---
# <span data-ttu-id="e87ba-104">0.9.430-Interface-ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e87ba-104">0.9.430 - interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e87ba-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="e87ba-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="e87ba-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e87ba-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="e87ba-107">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="e87ba-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="e87ba-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e87ba-108">Summary</span></span>

 <span data-ttu-id="e87ba-109">Member</span><span class="sxs-lookup"><span data-stu-id="e87ba-109">Members</span></span>                        | <span data-ttu-id="e87ba-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e87ba-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e87ba-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="e87ba-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e87ba-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e87ba-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e87ba-113">Member</span><span class="sxs-lookup"><span data-stu-id="e87ba-113">Members</span></span>

#### <span data-ttu-id="e87ba-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="e87ba-114">Invoke</span></span> 

<span data-ttu-id="e87ba-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e87ba-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e87ba-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2NewWindowRequestedEventArgs](ICoreWebView2NewWindowRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e87ba-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NewWindowRequestedEventArgs](ICoreWebView2NewWindowRequestedEventArgs.md) \* args)</span></span>


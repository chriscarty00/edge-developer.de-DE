---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8a826b5693bce0970c4360fb40c7e13ccacc1f01
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880976"
---
# <span data-ttu-id="76a2a-104">0.9.430-Interface-ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="76a2a-104">0.9.430 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="76a2a-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="76a2a-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="76a2a-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="76a2a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="76a2a-107">Der Aufrufer implementiert diese Methode, um das MoveFocusRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="76a2a-107">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="76a2a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="76a2a-108">Summary</span></span>

 <span data-ttu-id="76a2a-109">Member</span><span class="sxs-lookup"><span data-stu-id="76a2a-109">Members</span></span>                        | <span data-ttu-id="76a2a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="76a2a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="76a2a-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="76a2a-111">Invoke</span></span>](#invoke) | <span data-ttu-id="76a2a-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="76a2a-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="76a2a-113">Member</span><span class="sxs-lookup"><span data-stu-id="76a2a-113">Members</span></span>

#### <span data-ttu-id="76a2a-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="76a2a-114">Invoke</span></span> 

<span data-ttu-id="76a2a-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="76a2a-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="76a2a-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender;[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="76a2a-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>


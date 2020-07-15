---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 1e3e9d3f661a6e0643d7094c9127fdf33501624a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880178"
---
# <span data-ttu-id="8872f-104">0.9.430-Interface-ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8872f-104">0.9.430 - interface ICoreWebView2SourceChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="8872f-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="8872f-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="8872f-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="8872f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="8872f-107">Der Aufrufer implementiert diese Schnittstelle, um das Quellpfad-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="8872f-107">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="8872f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8872f-108">Summary</span></span>

 <span data-ttu-id="8872f-109">Member</span><span class="sxs-lookup"><span data-stu-id="8872f-109">Members</span></span>                        | <span data-ttu-id="8872f-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8872f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8872f-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="8872f-111">Invoke</span></span>](#invoke) | <span data-ttu-id="8872f-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8872f-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8872f-113">Member</span><span class="sxs-lookup"><span data-stu-id="8872f-113">Members</span></span>

#### <span data-ttu-id="8872f-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="8872f-114">Invoke</span></span> 

<span data-ttu-id="8872f-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8872f-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8872f-116">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](ICoreWebView2.md) \* WebView,[ICoreWebView2SourceChangedEventArgs](ICoreWebView2SourceChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8872f-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,[ICoreWebView2SourceChangedEventArgs](ICoreWebView2SourceChangedEventArgs.md) \* args)</span></span>


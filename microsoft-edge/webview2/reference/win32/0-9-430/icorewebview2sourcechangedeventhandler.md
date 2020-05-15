---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 1f7eb0237e43913ffcd147ff28dde0c14561643d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654094"
---
# <span data-ttu-id="f9157-104">Schnittstellen ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f9157-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f9157-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f9157-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="f9157-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f9157-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="f9157-107">Der Aufrufer implementiert diese Schnittstelle, um das Quellpfad-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f9157-107">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="f9157-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f9157-108">Summary</span></span>

 <span data-ttu-id="f9157-109">Member</span><span class="sxs-lookup"><span data-stu-id="f9157-109">Members</span></span>                        | <span data-ttu-id="f9157-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f9157-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f9157-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="f9157-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f9157-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9157-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f9157-113">Member</span><span class="sxs-lookup"><span data-stu-id="f9157-113">Members</span></span>

#### <span data-ttu-id="f9157-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f9157-114">Invoke</span></span> 

<span data-ttu-id="f9157-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9157-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f9157-116">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](ICoreWebView2.md) \* WebView,[ICoreWebView2SourceChangedEventArgs](ICoreWebView2SourceChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f9157-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,[ICoreWebView2SourceChangedEventArgs](ICoreWebView2SourceChangedEventArgs.md) \* args)</span></span>


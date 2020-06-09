---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 9135ba6bce6b5260413f47531062ea4c96d196cc
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698134"
---
# <span data-ttu-id="940ee-104">Schnittstellen ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="940ee-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="940ee-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="940ee-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="940ee-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="940ee-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="940ee-107">Der Aufrufer implementiert diese Schnittstelle, um das Quellpfad-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="940ee-107">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="940ee-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="940ee-108">Summary</span></span>

 <span data-ttu-id="940ee-109">Member</span><span class="sxs-lookup"><span data-stu-id="940ee-109">Members</span></span>                        | <span data-ttu-id="940ee-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="940ee-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="940ee-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="940ee-111">Invoke</span></span>](#invoke) | <span data-ttu-id="940ee-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="940ee-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="940ee-113">Member</span><span class="sxs-lookup"><span data-stu-id="940ee-113">Members</span></span>

#### <span data-ttu-id="940ee-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="940ee-114">Invoke</span></span> 

<span data-ttu-id="940ee-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="940ee-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="940ee-116">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="940ee-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>


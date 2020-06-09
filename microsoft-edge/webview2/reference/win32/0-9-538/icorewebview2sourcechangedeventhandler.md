---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: abf819c5b3a52cb45fb2ad057e94e31819541e0d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698894"
---
# <span data-ttu-id="09ca8-104">Schnittstellen ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="09ca8-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="09ca8-105">Der Aufrufer implementiert diese Schnittstelle, um das Quellpfad-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="09ca8-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="09ca8-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="09ca8-106">Summary</span></span>

 <span data-ttu-id="09ca8-107">Member</span><span class="sxs-lookup"><span data-stu-id="09ca8-107">Members</span></span>                        | <span data-ttu-id="09ca8-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="09ca8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="09ca8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="09ca8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="09ca8-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="09ca8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="09ca8-111">Member</span><span class="sxs-lookup"><span data-stu-id="09ca8-111">Members</span></span>

#### <span data-ttu-id="09ca8-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="09ca8-112">Invoke</span></span> 

<span data-ttu-id="09ca8-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="09ca8-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="09ca8-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="09ca8-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>


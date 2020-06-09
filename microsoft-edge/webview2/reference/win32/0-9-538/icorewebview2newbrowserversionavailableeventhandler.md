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
ms.openlocfilehash: c8444741480ba3b07d2755dcac0ec11f7194a783
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698930"
---
# <span data-ttu-id="d3d15-104">Schnittstellen ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="d3d15-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="d3d15-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von NewBrowserVersionAvailable-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="d3d15-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="d3d15-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d3d15-106">Summary</span></span>

 <span data-ttu-id="d3d15-107">Member</span><span class="sxs-lookup"><span data-stu-id="d3d15-107">Members</span></span>                        | <span data-ttu-id="d3d15-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d3d15-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d3d15-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d3d15-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d3d15-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d3d15-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d3d15-111">Member</span><span class="sxs-lookup"><span data-stu-id="d3d15-111">Members</span></span>

#### <span data-ttu-id="d3d15-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="d3d15-112">Invoke</span></span> 

<span data-ttu-id="d3d15-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d3d15-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d3d15-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="d3d15-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>


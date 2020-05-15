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
ms.openlocfilehash: 9196f2d9503efbaf9f15b43e7e6d7e80c2de00f7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653968"
---
# <span data-ttu-id="ddb02-104">Schnittstellen ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="ddb02-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="ddb02-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von NewBrowserVersionAvailable-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="ddb02-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="ddb02-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ddb02-106">Summary</span></span>

 <span data-ttu-id="ddb02-107">Member</span><span class="sxs-lookup"><span data-stu-id="ddb02-107">Members</span></span>                        | <span data-ttu-id="ddb02-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ddb02-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ddb02-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ddb02-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ddb02-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ddb02-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ddb02-111">Member</span><span class="sxs-lookup"><span data-stu-id="ddb02-111">Members</span></span>

#### <span data-ttu-id="ddb02-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ddb02-112">Invoke</span></span> 

<span data-ttu-id="ddb02-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ddb02-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ddb02-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ddb02-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>


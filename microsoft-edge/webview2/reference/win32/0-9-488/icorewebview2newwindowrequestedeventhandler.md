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
ms.openlocfilehash: a8cd4dd948aa00aca7c2ef7d8c0c744b30db37e3
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653961"
---
# <span data-ttu-id="283f9-104">Schnittstellen ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="283f9-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="283f9-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="283f9-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="283f9-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="283f9-106">Summary</span></span>

 <span data-ttu-id="283f9-107">Member</span><span class="sxs-lookup"><span data-stu-id="283f9-107">Members</span></span>                        | <span data-ttu-id="283f9-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="283f9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="283f9-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="283f9-109">Invoke</span></span>](#invoke) | <span data-ttu-id="283f9-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="283f9-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="283f9-111">Member</span><span class="sxs-lookup"><span data-stu-id="283f9-111">Members</span></span>

#### <span data-ttu-id="283f9-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="283f9-112">Invoke</span></span> 

<span data-ttu-id="283f9-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="283f9-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="283f9-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="283f9-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>


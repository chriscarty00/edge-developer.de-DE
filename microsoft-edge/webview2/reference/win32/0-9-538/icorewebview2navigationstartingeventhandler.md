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
ms.openlocfilehash: faeafdb0f2da5fa5037f41faab0d0b5ee8434eb4
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698864"
---
# <span data-ttu-id="74efa-104">Schnittstellen ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="74efa-104">interface ICoreWebView2NavigationStartingEventHandler</span></span> 

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="74efa-105">Der Aufrufer implementiert diese Schnittstelle, um das NavigationStarting-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="74efa-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="74efa-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="74efa-106">Summary</span></span>

 <span data-ttu-id="74efa-107">Member</span><span class="sxs-lookup"><span data-stu-id="74efa-107">Members</span></span>                        | <span data-ttu-id="74efa-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="74efa-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="74efa-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="74efa-109">Invoke</span></span>](#invoke) | <span data-ttu-id="74efa-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="74efa-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="74efa-111">Member</span><span class="sxs-lookup"><span data-stu-id="74efa-111">Members</span></span>

#### <span data-ttu-id="74efa-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="74efa-112">Invoke</span></span> 

<span data-ttu-id="74efa-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="74efa-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="74efa-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="74efa-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span></span>


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
ms.openlocfilehash: 85de243c00364f7fb57d3842b2ddbf78848905f6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654043"
---
# <span data-ttu-id="eb660-104">Schnittstellen ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="eb660-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="eb660-105">Der Aufrufer implementiert diese Methode, um die ContainsFullScreenElementChanged-Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="eb660-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="eb660-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="eb660-106">Summary</span></span>

 <span data-ttu-id="eb660-107">Member</span><span class="sxs-lookup"><span data-stu-id="eb660-107">Members</span></span>                        | <span data-ttu-id="eb660-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="eb660-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eb660-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="eb660-109">Invoke</span></span>](#invoke) | <span data-ttu-id="eb660-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eb660-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="eb660-111">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="eb660-111">There are no event args for this event.</span></span>

## <span data-ttu-id="eb660-112">Member</span><span class="sxs-lookup"><span data-stu-id="eb660-112">Members</span></span>

#### <span data-ttu-id="eb660-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="eb660-113">Invoke</span></span> 

<span data-ttu-id="eb660-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eb660-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="eb660-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="eb660-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="eb660-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="eb660-116">There are no event args and the args parameter will be null.</span></span>


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
ms.openlocfilehash: 17c912605a90dba73e5876cd6d3c26b15cdd98ec
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653971"
---
# <span data-ttu-id="2f959-104">Schnittstellen ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2f959-104">interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="2f959-105">Der Aufrufer implementiert diese Schnittstelle, um das NavigationCompleted-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="2f959-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="2f959-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2f959-106">Summary</span></span>

 <span data-ttu-id="2f959-107">Member</span><span class="sxs-lookup"><span data-stu-id="2f959-107">Members</span></span>                        | <span data-ttu-id="2f959-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2f959-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2f959-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2f959-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2f959-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2f959-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="2f959-111">Member</span><span class="sxs-lookup"><span data-stu-id="2f959-111">Members</span></span>

#### <span data-ttu-id="2f959-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="2f959-112">Invoke</span></span> 

<span data-ttu-id="2f959-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2f959-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2f959-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2f959-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>


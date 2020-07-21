---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 30c39bf10c874c17787c235ebb1589de1c9449ff
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885555"
---
# <span data-ttu-id="f00e5-104">0.9.515-Interface-ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f00e5-104">0.9.515 - interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="f00e5-105">Der Aufrufer implementiert diese Schnittstelle, um das NavigationCompleted-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f00e5-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="f00e5-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f00e5-106">Summary</span></span>

 <span data-ttu-id="f00e5-107">Member</span><span class="sxs-lookup"><span data-stu-id="f00e5-107">Members</span></span>                        | <span data-ttu-id="f00e5-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f00e5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f00e5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f00e5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f00e5-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f00e5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f00e5-111">Member</span><span class="sxs-lookup"><span data-stu-id="f00e5-111">Members</span></span>

#### <span data-ttu-id="f00e5-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f00e5-112">Invoke</span></span> 

<span data-ttu-id="f00e5-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f00e5-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f00e5-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f00e5-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>


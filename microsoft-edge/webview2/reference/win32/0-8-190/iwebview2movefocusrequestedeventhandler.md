---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: fe84f29798b01aed2787559c717f2893c9eda7f9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885940"
---
# <span data-ttu-id="c8825-104">0.8.355-Interface-IWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c8825-104">0.8.355 - interface IWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="c8825-105">Der Aufrufer implementiert diese Methode, um das MoveFocusRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c8825-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="c8825-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c8825-106">Summary</span></span>

 <span data-ttu-id="c8825-107">Member</span><span class="sxs-lookup"><span data-stu-id="c8825-107">Members</span></span>                        | <span data-ttu-id="c8825-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c8825-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c8825-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c8825-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c8825-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c8825-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c8825-111">Member</span><span class="sxs-lookup"><span data-stu-id="c8825-111">Members</span></span>

#### <span data-ttu-id="c8825-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c8825-112">Invoke</span></span> 

<span data-ttu-id="c8825-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c8825-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c8825-114">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c8825-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>


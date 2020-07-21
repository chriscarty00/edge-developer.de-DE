---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: cf799ae12b977f66bfba4d1b7664e3abc6241304
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885921"
---
# <span data-ttu-id="0c370-104">0.8.355-Interface-IWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0c370-104">0.8.355 - interface IWebView2NavigationCompletedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="0c370-105">Der Aufrufer implementiert diese Schnittstelle, um das NavigationCompleted-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="0c370-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="0c370-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0c370-106">Summary</span></span>

 <span data-ttu-id="0c370-107">Member</span><span class="sxs-lookup"><span data-stu-id="0c370-107">Members</span></span>                        | <span data-ttu-id="0c370-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="0c370-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0c370-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0c370-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0c370-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0c370-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="0c370-111">Member</span><span class="sxs-lookup"><span data-stu-id="0c370-111">Members</span></span>

#### <span data-ttu-id="0c370-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="0c370-112">Invoke</span></span> 

<span data-ttu-id="0c370-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0c370-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0c370-114">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NavigationCompletedEventArgs](IWebView2NavigationCompletedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="0c370-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NavigationCompletedEventArgs](IWebView2NavigationCompletedEventArgs.md) \* args)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 2fe743f0ffe39107252a184e2e98cc2904e3c640
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884974"
---
# <span data-ttu-id="e74bb-104">0.8.355-Interface-IWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e74bb-104">0.8.355 - interface IWebView2NewWindowRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="e74bb-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="e74bb-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="e74bb-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e74bb-106">Summary</span></span>

 <span data-ttu-id="e74bb-107">Member</span><span class="sxs-lookup"><span data-stu-id="e74bb-107">Members</span></span>                        | <span data-ttu-id="e74bb-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e74bb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e74bb-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e74bb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e74bb-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e74bb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e74bb-111">Member</span><span class="sxs-lookup"><span data-stu-id="e74bb-111">Members</span></span>

#### <span data-ttu-id="e74bb-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e74bb-112">Invoke</span></span> 

<span data-ttu-id="e74bb-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e74bb-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e74bb-114">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e74bb-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) \* args)</span></span>


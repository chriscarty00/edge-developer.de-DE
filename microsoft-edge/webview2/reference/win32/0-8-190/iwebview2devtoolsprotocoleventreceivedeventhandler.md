---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: a26a2c18c402bffe11353b2f53f0559acde3663b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886164"
---
# <span data-ttu-id="9469e-104">0.8.355-Interface-IWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9469e-104">0.8.355 - interface IWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="9469e-105">Der Aufrufer implementiert diese Schnittstelle, um DevToolsProtocolEventReceived-Ereignisse aus dem [IWebView2WebView](IWebView2WebView.md)zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="9469e-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the [IWebView2WebView](IWebView2WebView.md).</span></span>

## <span data-ttu-id="9469e-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9469e-106">Summary</span></span>

 <span data-ttu-id="9469e-107">Member</span><span class="sxs-lookup"><span data-stu-id="9469e-107">Members</span></span>                        | <span data-ttu-id="9469e-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9469e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9469e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9469e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9469e-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9469e-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="9469e-111">Member</span><span class="sxs-lookup"><span data-stu-id="9469e-111">Members</span></span>

#### <span data-ttu-id="9469e-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9469e-112">Invoke</span></span> 

<span data-ttu-id="9469e-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9469e-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9469e-114">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DevToolsProtocolEventReceivedEventArgs](IWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="9469e-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DevToolsProtocolEventReceivedEventArgs](IWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 97a0d8f2afda5f6391a574e6ad62fbd2e17abcc1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884939"
---
# <span data-ttu-id="853b4-104">0.8.355-Interface-IWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="853b4-104">0.8.355 - interface IWebView2ProcessFailedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="853b4-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ProcessFailed-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="853b4-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="853b4-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="853b4-106">Summary</span></span>

 <span data-ttu-id="853b4-107">Member</span><span class="sxs-lookup"><span data-stu-id="853b4-107">Members</span></span>                        | <span data-ttu-id="853b4-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="853b4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="853b4-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="853b4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="853b4-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="853b4-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="853b4-111">Member</span><span class="sxs-lookup"><span data-stu-id="853b4-111">Members</span></span>

#### <span data-ttu-id="853b4-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="853b4-112">Invoke</span></span> 

<span data-ttu-id="853b4-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="853b4-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="853b4-114">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="853b4-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) \* args)</span></span>


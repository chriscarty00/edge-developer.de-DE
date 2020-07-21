---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 772ad4ce7bd1ae0c1f02475206380c146ecabf7b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885744"
---
# <span data-ttu-id="ff4b7-104">0.8.355-Interface-IWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ff4b7-104">0.8.355 - interface IWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="ff4b7-105">Der Aufrufer implementiert diese Schnittstelle, um das WebMessageReceived-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ff4b7-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="ff4b7-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ff4b7-106">Summary</span></span>

 <span data-ttu-id="ff4b7-107">Member</span><span class="sxs-lookup"><span data-stu-id="ff4b7-107">Members</span></span>                        | <span data-ttu-id="ff4b7-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ff4b7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ff4b7-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ff4b7-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ff4b7-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ff4b7-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ff4b7-111">Member</span><span class="sxs-lookup"><span data-stu-id="ff4b7-111">Members</span></span>

#### <span data-ttu-id="ff4b7-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ff4b7-112">Invoke</span></span> 

<span data-ttu-id="ff4b7-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ff4b7-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ff4b7-114">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ff4b7-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>


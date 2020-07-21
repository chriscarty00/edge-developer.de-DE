---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: b1d0bf7ea5f472d5a1c3682c2cbef564947ee54b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886185"
---
# <span data-ttu-id="6fc86-104">0.8.355-Interface-IWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6fc86-104">0.8.355 - interface IWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="6fc86-105">Der Aufrufer implementiert diese Methode, um die ContainsFullScreenElementChanged-Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="6fc86-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="6fc86-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6fc86-106">Summary</span></span>

 <span data-ttu-id="6fc86-107">Member</span><span class="sxs-lookup"><span data-stu-id="6fc86-107">Members</span></span>                        | <span data-ttu-id="6fc86-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6fc86-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6fc86-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6fc86-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6fc86-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6fc86-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="6fc86-111">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6fc86-111">There are no event args for this event.</span></span>

## <span data-ttu-id="6fc86-112">Member</span><span class="sxs-lookup"><span data-stu-id="6fc86-112">Members</span></span>

#### <span data-ttu-id="6fc86-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="6fc86-113">Invoke</span></span> 

<span data-ttu-id="6fc86-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6fc86-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6fc86-115">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView5](IWebView2WebView5.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="6fc86-115">public HRESULT [Invoke](#invoke)([IWebView2WebView5](IWebView2WebView5.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="6fc86-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="6fc86-116">There are no event args and the args parameter will be null.</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8afab2e15381c99f5f677b13e539e4b6a9279b63
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884323"
---
# <span data-ttu-id="d3a39-104">0.9.430-Interface-ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d3a39-104">0.9.430 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="d3a39-105">Der Aufrufer implementiert diese Methode, um die ContainsFullScreenElementChanged-Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d3a39-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="d3a39-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d3a39-106">Summary</span></span>

 <span data-ttu-id="d3a39-107">Member</span><span class="sxs-lookup"><span data-stu-id="d3a39-107">Members</span></span>                        | <span data-ttu-id="d3a39-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d3a39-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d3a39-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d3a39-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d3a39-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d3a39-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="d3a39-111">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d3a39-111">There are no event args for this event.</span></span>

## <span data-ttu-id="d3a39-112">Member</span><span class="sxs-lookup"><span data-stu-id="d3a39-112">Members</span></span>

#### <span data-ttu-id="d3a39-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="d3a39-113">Invoke</span></span> 

<span data-ttu-id="d3a39-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d3a39-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d3a39-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="d3a39-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="d3a39-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="d3a39-116">There are no event args and the args parameter will be null.</span></span>


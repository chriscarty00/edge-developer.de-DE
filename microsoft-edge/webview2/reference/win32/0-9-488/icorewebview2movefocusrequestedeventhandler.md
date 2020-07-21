---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 45f9b638347d096ce89c9fcaac1bfb7e904ebee9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886297"
---
# <span data-ttu-id="266c4-104">0.9.515-Interface-ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="266c4-104">0.9.515 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="266c4-105">Der Aufrufer implementiert diese Methode, um das MoveFocusRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="266c4-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="266c4-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="266c4-106">Summary</span></span>

 <span data-ttu-id="266c4-107">Member</span><span class="sxs-lookup"><span data-stu-id="266c4-107">Members</span></span>                        | <span data-ttu-id="266c4-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="266c4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="266c4-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="266c4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="266c4-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="266c4-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="266c4-111">Member</span><span class="sxs-lookup"><span data-stu-id="266c4-111">Members</span></span>

#### <span data-ttu-id="266c4-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="266c4-112">Invoke</span></span> 

<span data-ttu-id="266c4-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="266c4-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="266c4-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="266c4-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>


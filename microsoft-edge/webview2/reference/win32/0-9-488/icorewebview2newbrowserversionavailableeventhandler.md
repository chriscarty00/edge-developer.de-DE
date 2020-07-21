---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: aa59efbb0b47977b41236950c47a01d6d95ee123
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886292"
---
# <span data-ttu-id="3b6bf-104">0.9.515-Interface-ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="3b6bf-104">0.9.515 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="3b6bf-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von NewBrowserVersionAvailable-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="3b6bf-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3b6bf-106">Summary</span></span>

 <span data-ttu-id="3b6bf-107">Member</span><span class="sxs-lookup"><span data-stu-id="3b6bf-107">Members</span></span>                        | <span data-ttu-id="3b6bf-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3b6bf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3b6bf-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3b6bf-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3b6bf-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3b6bf-111">Member</span><span class="sxs-lookup"><span data-stu-id="3b6bf-111">Members</span></span>

#### <span data-ttu-id="3b6bf-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="3b6bf-112">Invoke</span></span> 

<span data-ttu-id="3b6bf-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3b6bf-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3b6bf-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="3b6bf-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>


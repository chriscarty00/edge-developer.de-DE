---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a90e7d3479f93d58d72db5c69cca53669a6d4501
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698810"
---
# <span data-ttu-id="2076b-104">Schnittstellen ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2076b-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="2076b-105">Der Aufrufer implementiert diese Methode, um das MoveFocusRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="2076b-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="2076b-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2076b-106">Summary</span></span>

 <span data-ttu-id="2076b-107">Member</span><span class="sxs-lookup"><span data-stu-id="2076b-107">Members</span></span>                        | <span data-ttu-id="2076b-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2076b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2076b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2076b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2076b-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2076b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="2076b-111">Member</span><span class="sxs-lookup"><span data-stu-id="2076b-111">Members</span></span>

#### <span data-ttu-id="2076b-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="2076b-112">Invoke</span></span> 

<span data-ttu-id="2076b-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2076b-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2076b-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2076b-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>


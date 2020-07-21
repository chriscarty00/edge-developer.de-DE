---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ffa7f6e42802e8303a2ab68f3923dcc293c28d2a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885450"
---
# <span data-ttu-id="271fc-104">0.9.515-Interface-ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="271fc-104">0.9.515 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="271fc-105">Der Aufrufer implementiert diese Schnittstelle, um DevToolsProtocolEventReceived-Ereignisse aus der WebView zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="271fc-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="271fc-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="271fc-106">Summary</span></span>

 <span data-ttu-id="271fc-107">Member</span><span class="sxs-lookup"><span data-stu-id="271fc-107">Members</span></span>                        | <span data-ttu-id="271fc-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="271fc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="271fc-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="271fc-109">Invoke</span></span>](#invoke) | <span data-ttu-id="271fc-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="271fc-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="271fc-111">Member</span><span class="sxs-lookup"><span data-stu-id="271fc-111">Members</span></span>

#### <span data-ttu-id="271fc-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="271fc-112">Invoke</span></span> 

<span data-ttu-id="271fc-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="271fc-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="271fc-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="271fc-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>


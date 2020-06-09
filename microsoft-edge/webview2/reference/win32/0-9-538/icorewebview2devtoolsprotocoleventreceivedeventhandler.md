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
ms.openlocfilehash: c154b80e29476666bc0b2121b3eba63009946b36
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698827"
---
# <span data-ttu-id="365e5-104">Schnittstellen ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="365e5-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="365e5-105">Der Aufrufer implementiert diese Schnittstelle, um DevToolsProtocolEventReceived-Ereignisse aus der WebView zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="365e5-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="365e5-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="365e5-106">Summary</span></span>

 <span data-ttu-id="365e5-107">Member</span><span class="sxs-lookup"><span data-stu-id="365e5-107">Members</span></span>                        | <span data-ttu-id="365e5-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="365e5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="365e5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="365e5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="365e5-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="365e5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="365e5-111">Member</span><span class="sxs-lookup"><span data-stu-id="365e5-111">Members</span></span>

#### <span data-ttu-id="365e5-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="365e5-112">Invoke</span></span> 

<span data-ttu-id="365e5-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="365e5-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="365e5-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="365e5-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>


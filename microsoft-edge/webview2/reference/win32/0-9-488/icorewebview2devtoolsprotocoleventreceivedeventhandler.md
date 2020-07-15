---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 1e59d8d830c3357fafd4f8315388ee5fff93a3d2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880808"
---
# <span data-ttu-id="f4c62-104">0.9.515-Interface-ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f4c62-104">0.9.515 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f4c62-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="f4c62-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f4c62-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f4c62-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="f4c62-107">Der Aufrufer implementiert diese Schnittstelle, um DevToolsProtocolEventReceived-Ereignisse aus der WebView zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f4c62-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="f4c62-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f4c62-108">Summary</span></span>

 <span data-ttu-id="f4c62-109">Member</span><span class="sxs-lookup"><span data-stu-id="f4c62-109">Members</span></span>                        | <span data-ttu-id="f4c62-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f4c62-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f4c62-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="f4c62-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f4c62-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f4c62-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f4c62-113">Member</span><span class="sxs-lookup"><span data-stu-id="f4c62-113">Members</span></span>

#### <span data-ttu-id="f4c62-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f4c62-114">Invoke</span></span> 

<span data-ttu-id="f4c62-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f4c62-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f4c62-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f4c62-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>


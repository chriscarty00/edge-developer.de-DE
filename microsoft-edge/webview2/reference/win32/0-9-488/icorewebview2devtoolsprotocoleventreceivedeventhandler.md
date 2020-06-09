---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a38d451f4ee99e4ab1392f4685a66abf1f274ddb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698064"
---
# <span data-ttu-id="e7cdc-104">Schnittstellen ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e7cdc-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e7cdc-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="e7cdc-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e7cdc-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e7cdc-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="e7cdc-107">Der Aufrufer implementiert diese Schnittstelle, um DevToolsProtocolEventReceived-Ereignisse aus der WebView zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e7cdc-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="e7cdc-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e7cdc-108">Summary</span></span>

 <span data-ttu-id="e7cdc-109">Member</span><span class="sxs-lookup"><span data-stu-id="e7cdc-109">Members</span></span>                        | <span data-ttu-id="e7cdc-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e7cdc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e7cdc-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="e7cdc-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e7cdc-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e7cdc-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e7cdc-113">Member</span><span class="sxs-lookup"><span data-stu-id="e7cdc-113">Members</span></span>

#### <span data-ttu-id="e7cdc-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="e7cdc-114">Invoke</span></span> 

<span data-ttu-id="e7cdc-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e7cdc-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e7cdc-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e7cdc-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>


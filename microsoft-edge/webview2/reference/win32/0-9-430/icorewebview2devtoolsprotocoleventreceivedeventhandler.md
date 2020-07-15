---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 63c053e98c3e4af32aaa9ac981930792504f34a7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877961"
---
# <span data-ttu-id="a1fd9-104">0.9.430-Interface-ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a1fd9-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a1fd9-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="a1fd9-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="a1fd9-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="a1fd9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="a1fd9-107">Der Aufrufer implementiert diese Schnittstelle, um DevToolsProtocolEventReceived-Ereignisse aus der WebView zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="a1fd9-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="a1fd9-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a1fd9-108">Summary</span></span>

 <span data-ttu-id="a1fd9-109">Member</span><span class="sxs-lookup"><span data-stu-id="a1fd9-109">Members</span></span>                        | <span data-ttu-id="a1fd9-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a1fd9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a1fd9-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="a1fd9-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a1fd9-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a1fd9-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a1fd9-113">Member</span><span class="sxs-lookup"><span data-stu-id="a1fd9-113">Members</span></span>

#### <span data-ttu-id="a1fd9-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="a1fd9-114">Invoke</span></span> 

<span data-ttu-id="a1fd9-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a1fd9-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a1fd9-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a1fd9-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>


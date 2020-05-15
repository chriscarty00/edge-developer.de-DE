---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: b33d7de85d1a74e2115d8e3ea4bc84eb185b03b5
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653955"
---
# <span data-ttu-id="18e26-104">Schnittstellen IWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="18e26-104">interface IWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="18e26-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="18e26-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="18e26-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="18e26-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="18e26-107">Der Aufrufer implementiert diese Schnittstelle, um DevToolsProtocolEventReceived-Ereignisse aus dem [IWebView2WebView](IWebView2WebView.md)zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="18e26-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the [IWebView2WebView](IWebView2WebView.md).</span></span>

## <span data-ttu-id="18e26-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="18e26-108">Summary</span></span>

 <span data-ttu-id="18e26-109">Member</span><span class="sxs-lookup"><span data-stu-id="18e26-109">Members</span></span>                        | <span data-ttu-id="18e26-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="18e26-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="18e26-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="18e26-111">Invoke</span></span>](#invoke) | <span data-ttu-id="18e26-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="18e26-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="18e26-113">Member</span><span class="sxs-lookup"><span data-stu-id="18e26-113">Members</span></span>

#### <span data-ttu-id="18e26-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="18e26-114">Invoke</span></span> 

<span data-ttu-id="18e26-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="18e26-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="18e26-116">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DevToolsProtocolEventReceivedEventArgs](IWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="18e26-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DevToolsProtocolEventReceivedEventArgs](IWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>


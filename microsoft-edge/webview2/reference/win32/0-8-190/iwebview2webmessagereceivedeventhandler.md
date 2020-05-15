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
ms.openlocfilehash: 0bc1ed55a41e790c742ca5732eb7177e56468727
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653780"
---
# <span data-ttu-id="6a287-104">Schnittstellen IWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6a287-104">interface IWebView2WebMessageReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="6a287-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="6a287-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="6a287-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="6a287-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="6a287-107">Der Aufrufer implementiert diese Schnittstelle, um das WebMessageReceived-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="6a287-107">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="6a287-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6a287-108">Summary</span></span>

 <span data-ttu-id="6a287-109">Member</span><span class="sxs-lookup"><span data-stu-id="6a287-109">Members</span></span>                        | <span data-ttu-id="6a287-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6a287-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6a287-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="6a287-111">Invoke</span></span>](#invoke) | <span data-ttu-id="6a287-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6a287-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="6a287-113">Member</span><span class="sxs-lookup"><span data-stu-id="6a287-113">Members</span></span>

#### <span data-ttu-id="6a287-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="6a287-114">Invoke</span></span> 

<span data-ttu-id="6a287-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6a287-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6a287-116">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="6a287-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>


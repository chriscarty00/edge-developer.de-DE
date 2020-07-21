---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c08a851eb21947cae4af465a233dc4c49508c84c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884211"
---
# <span data-ttu-id="eac53-104">0.9.430-Interface-ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="eac53-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="eac53-105">Der Aufrufer implementiert diese Schnittstelle, um DevToolsProtocolEventReceived-Ereignisse aus der WebView zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="eac53-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="eac53-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="eac53-106">Summary</span></span>

 <span data-ttu-id="eac53-107">Member</span><span class="sxs-lookup"><span data-stu-id="eac53-107">Members</span></span>                        | <span data-ttu-id="eac53-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="eac53-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eac53-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="eac53-109">Invoke</span></span>](#invoke) | <span data-ttu-id="eac53-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eac53-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="eac53-111">Member</span><span class="sxs-lookup"><span data-stu-id="eac53-111">Members</span></span>

#### <span data-ttu-id="eac53-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="eac53-112">Invoke</span></span> 

<span data-ttu-id="eac53-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eac53-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="eac53-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="eac53-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>


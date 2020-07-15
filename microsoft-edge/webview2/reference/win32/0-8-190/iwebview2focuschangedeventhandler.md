---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 44e24ef8e0e4b41968835ff7cd70fd9904482c6c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878449"
---
# <span data-ttu-id="237a9-104">0.8.355-Interface-IWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="237a9-104">0.8.355 - interface IWebView2FocusChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="237a9-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="237a9-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="237a9-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="237a9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="237a9-107">Der Aufrufer implementiert diese Methode, um das GotFocus-Ereignis und das LostFocus-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="237a9-107">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="237a9-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="237a9-108">Summary</span></span>

 <span data-ttu-id="237a9-109">Member</span><span class="sxs-lookup"><span data-stu-id="237a9-109">Members</span></span>                        | <span data-ttu-id="237a9-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="237a9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="237a9-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="237a9-111">Invoke</span></span>](#invoke) | <span data-ttu-id="237a9-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="237a9-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="237a9-113">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="237a9-113">There are no event args for this event.</span></span>

## <span data-ttu-id="237a9-114">Member</span><span class="sxs-lookup"><span data-stu-id="237a9-114">Members</span></span>

#### <span data-ttu-id="237a9-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="237a9-115">Invoke</span></span> 

<span data-ttu-id="237a9-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="237a9-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="237a9-117">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="237a9-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="237a9-118">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="237a9-118">There are no event args and the args parameter will be null.</span></span>


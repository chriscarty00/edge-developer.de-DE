---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: e4969ecbb5068f634eeb9a10f4de07277051ef45
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878001"
---
# <span data-ttu-id="5d315-104">0.8.355-Interface-IWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="5d315-104">0.8.355 - interface IWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="5d315-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="5d315-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="5d315-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="5d315-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="5d315-107">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ZoomFactorChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="5d315-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="5d315-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5d315-108">Summary</span></span>

 <span data-ttu-id="5d315-109">Member</span><span class="sxs-lookup"><span data-stu-id="5d315-109">Members</span></span>                        | <span data-ttu-id="5d315-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5d315-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5d315-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="5d315-111">Invoke</span></span>](#invoke) | <span data-ttu-id="5d315-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5d315-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="5d315-113">Verwenden Sie die IWebView2WebView. ZoomFactor-Eigenschaft, um den geänderten Zoomfaktor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5d315-113">Use the IWebView2WebView.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="5d315-114">Member</span><span class="sxs-lookup"><span data-stu-id="5d315-114">Members</span></span>

#### <span data-ttu-id="5d315-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="5d315-115">Invoke</span></span> 

<span data-ttu-id="5d315-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5d315-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5d315-117">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="5d315-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="5d315-118">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="5d315-118">There are no event args and the args parameter will be null.</span></span>


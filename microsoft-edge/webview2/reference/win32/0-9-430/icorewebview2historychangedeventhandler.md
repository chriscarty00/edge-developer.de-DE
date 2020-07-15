---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 6afd1983b90b4412fd3011dc35f192809a9583b7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881018"
---
# <span data-ttu-id="9803a-104">0.9.430-Interface-ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9803a-104">0.9.430 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="9803a-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="9803a-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="9803a-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="9803a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="9803a-107">Der Aufrufer implementiert diese Schnittstelle, um das Ereignis "History" zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="9803a-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="9803a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9803a-108">Summary</span></span>

 <span data-ttu-id="9803a-109">Member</span><span class="sxs-lookup"><span data-stu-id="9803a-109">Members</span></span>                        | <span data-ttu-id="9803a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9803a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9803a-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="9803a-111">Invoke</span></span>](#invoke) | <span data-ttu-id="9803a-112">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="9803a-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="9803a-113">Member</span><span class="sxs-lookup"><span data-stu-id="9803a-113">Members</span></span>

#### <span data-ttu-id="9803a-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="9803a-114">Invoke</span></span> 

<span data-ttu-id="9803a-115">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="9803a-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="9803a-116">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](ICoreWebView2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="9803a-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,IUnknown \* args)</span></span>


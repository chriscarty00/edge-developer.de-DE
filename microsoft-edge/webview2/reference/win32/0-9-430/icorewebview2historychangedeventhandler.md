---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e47ca26475ba1b59fa4ea8c87a7aada0d8d6695f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884134"
---
# <span data-ttu-id="9c3c4-104">0.9.430-Interface-ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9c3c4-104">0.9.430 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="9c3c4-105">Der Aufrufer implementiert diese Schnittstelle, um das Ereignis "History" zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="9c3c4-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="9c3c4-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9c3c4-106">Summary</span></span>

 <span data-ttu-id="9c3c4-107">Member</span><span class="sxs-lookup"><span data-stu-id="9c3c4-107">Members</span></span>                        | <span data-ttu-id="9c3c4-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9c3c4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9c3c4-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9c3c4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9c3c4-110">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="9c3c4-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="9c3c4-111">Member</span><span class="sxs-lookup"><span data-stu-id="9c3c4-111">Members</span></span>

#### <span data-ttu-id="9c3c4-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9c3c4-112">Invoke</span></span> 

<span data-ttu-id="9c3c4-113">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="9c3c4-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="9c3c4-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](ICoreWebView2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="9c3c4-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,IUnknown \* args)</span></span>


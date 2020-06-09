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
ms.openlocfilehash: 0305517d17bfa812dbaee9b238403f2d9f1fb22d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697805"
---
# <span data-ttu-id="ae987-104">Schnittstellen ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ae987-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ae987-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ae987-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ae987-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ae987-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ae987-107">Der Aufrufer implementiert diese Schnittstelle, um das Ereignis "History" zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ae987-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="ae987-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ae987-108">Summary</span></span>

 <span data-ttu-id="ae987-109">Member</span><span class="sxs-lookup"><span data-stu-id="ae987-109">Members</span></span>                        | <span data-ttu-id="ae987-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ae987-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ae987-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="ae987-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ae987-112">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="ae987-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="ae987-113">Member</span><span class="sxs-lookup"><span data-stu-id="ae987-113">Members</span></span>

#### <span data-ttu-id="ae987-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="ae987-114">Invoke</span></span> 

<span data-ttu-id="ae987-115">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="ae987-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="ae987-116">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ae987-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>


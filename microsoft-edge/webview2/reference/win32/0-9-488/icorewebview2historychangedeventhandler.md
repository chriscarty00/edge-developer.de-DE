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
ms.openlocfilehash: 42e3767ad2a42a1d9e9931efa8a4fe844ea80dba
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653764"
---
# <span data-ttu-id="ba52d-104">Schnittstellen ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ba52d-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ba52d-105">Der Aufrufer implementiert diese Schnittstelle, um das Ereignis "History" zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ba52d-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="ba52d-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ba52d-106">Summary</span></span>

 <span data-ttu-id="ba52d-107">Member</span><span class="sxs-lookup"><span data-stu-id="ba52d-107">Members</span></span>                        | <span data-ttu-id="ba52d-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ba52d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ba52d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ba52d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ba52d-110">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="ba52d-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="ba52d-111">Member</span><span class="sxs-lookup"><span data-stu-id="ba52d-111">Members</span></span>

#### <span data-ttu-id="ba52d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ba52d-112">Invoke</span></span> 

<span data-ttu-id="ba52d-113">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="ba52d-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="ba52d-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ba52d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>


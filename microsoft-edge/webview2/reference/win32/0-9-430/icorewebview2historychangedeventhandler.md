---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8fd3533d8f479866989f719be6e48c437fae4ddb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654059"
---
# <span data-ttu-id="91a62-104">Schnittstellen ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="91a62-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="91a62-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="91a62-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="91a62-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="91a62-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="91a62-107">Der Aufrufer implementiert diese Schnittstelle, um das Ereignis "History" zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="91a62-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="91a62-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="91a62-108">Summary</span></span>

 <span data-ttu-id="91a62-109">Member</span><span class="sxs-lookup"><span data-stu-id="91a62-109">Members</span></span>                        | <span data-ttu-id="91a62-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="91a62-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="91a62-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="91a62-111">Invoke</span></span>](#invoke) | <span data-ttu-id="91a62-112">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="91a62-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="91a62-113">Member</span><span class="sxs-lookup"><span data-stu-id="91a62-113">Members</span></span>

#### <span data-ttu-id="91a62-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="91a62-114">Invoke</span></span> 

<span data-ttu-id="91a62-115">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="91a62-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="91a62-116">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](ICoreWebView2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="91a62-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,IUnknown \* args)</span></span>


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
ms.openlocfilehash: 748c4affa73001270e2cf97b3d19db8c8ed23686
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654099"
---
# <span data-ttu-id="23d89-104">Schnittstellen IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="23d89-104">interface IWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="23d89-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="23d89-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="23d89-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="23d89-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="23d89-107">Ereignis-args für das ProcessFailed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="23d89-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="23d89-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="23d89-108">Summary</span></span>

 <span data-ttu-id="23d89-109">Member</span><span class="sxs-lookup"><span data-stu-id="23d89-109">Members</span></span>                        | <span data-ttu-id="23d89-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="23d89-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="23d89-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="23d89-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="23d89-112">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="23d89-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="23d89-113">Member</span><span class="sxs-lookup"><span data-stu-id="23d89-113">Members</span></span>

#### <span data-ttu-id="23d89-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="23d89-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="23d89-115">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="23d89-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="23d89-116">Public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="23d89-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


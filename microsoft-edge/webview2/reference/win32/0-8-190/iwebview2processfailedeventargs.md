---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 5ceb24d0d20f580e14e0d5af7ec09881c9ab0eb2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878246"
---
# <span data-ttu-id="de714-104">0.8.355-Interface-IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="de714-104">0.8.355 - interface IWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="de714-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="de714-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="de714-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="de714-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="de714-107">Ereignis-args für das ProcessFailed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="de714-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="de714-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="de714-108">Summary</span></span>

 <span data-ttu-id="de714-109">Member</span><span class="sxs-lookup"><span data-stu-id="de714-109">Members</span></span>                        | <span data-ttu-id="de714-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="de714-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="de714-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="de714-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="de714-112">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="de714-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="de714-113">Member</span><span class="sxs-lookup"><span data-stu-id="de714-113">Members</span></span>

#### <span data-ttu-id="de714-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="de714-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="de714-115">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="de714-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="de714-116">Public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="de714-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


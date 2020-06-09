---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c01d98ca997a0b4e288ecaa8ede609c93fc84ea1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698797"
---
# <span data-ttu-id="1ac7f-104">Schnittstellen ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1ac7f-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="1ac7f-105">Ereignis-args für das ProcessFailed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1ac7f-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="1ac7f-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1ac7f-106">Summary</span></span>

 <span data-ttu-id="1ac7f-107">Member</span><span class="sxs-lookup"><span data-stu-id="1ac7f-107">Members</span></span>                        | <span data-ttu-id="1ac7f-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1ac7f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1ac7f-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="1ac7f-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="1ac7f-110">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="1ac7f-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="1ac7f-111">Member</span><span class="sxs-lookup"><span data-stu-id="1ac7f-111">Members</span></span>

#### <span data-ttu-id="1ac7f-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="1ac7f-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="1ac7f-113">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="1ac7f-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="1ac7f-114">Public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="1ac7f-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


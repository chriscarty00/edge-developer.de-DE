---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a19f8c445d7ff1f6bee24cdd8871c28d41eedebe
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886411"
---
# <span data-ttu-id="a3161-104">0.9.430-Interface-ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a3161-104">0.9.430 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="a3161-105">Ereignis-args für das ProcessFailed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a3161-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="a3161-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a3161-106">Summary</span></span>

 <span data-ttu-id="a3161-107">Member</span><span class="sxs-lookup"><span data-stu-id="a3161-107">Members</span></span>                        | <span data-ttu-id="a3161-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a3161-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a3161-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="a3161-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="a3161-110">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="a3161-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="a3161-111">Member</span><span class="sxs-lookup"><span data-stu-id="a3161-111">Members</span></span>

#### <span data-ttu-id="a3161-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="a3161-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="a3161-113">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="a3161-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="a3161-114">Public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="a3161-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


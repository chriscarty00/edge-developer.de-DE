---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 697a49bfe68f83085f6c961ee2cdd5ab21f3b59b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885821"
---
# <span data-ttu-id="b9909-104">0.8.355-Interface-IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b9909-104">0.8.355 - interface IWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="b9909-105">Ereignis-args für das ProcessFailed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b9909-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="b9909-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b9909-106">Summary</span></span>

 <span data-ttu-id="b9909-107">Member</span><span class="sxs-lookup"><span data-stu-id="b9909-107">Members</span></span>                        | <span data-ttu-id="b9909-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b9909-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b9909-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="b9909-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="b9909-110">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="b9909-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="b9909-111">Member</span><span class="sxs-lookup"><span data-stu-id="b9909-111">Members</span></span>

#### <span data-ttu-id="b9909-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="b9909-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="b9909-113">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="b9909-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="b9909-114">Public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="b9909-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


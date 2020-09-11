---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: af27c39b2ed9ba197ab1c567bcf18a43c3dee932
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010019"
---
# <span data-ttu-id="1f8f4-104">0.9.579-Interface-ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1f8f4-104">0.9.579 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="1f8f4-105">Ereignis-args für das ProcessFailed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1f8f4-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="1f8f4-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1f8f4-106">Summary</span></span>

 <span data-ttu-id="1f8f4-107">Member</span><span class="sxs-lookup"><span data-stu-id="1f8f4-107">Members</span></span>                        | <span data-ttu-id="1f8f4-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1f8f4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1f8f4-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="1f8f4-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="1f8f4-110">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="1f8f4-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="1f8f4-111">Member</span><span class="sxs-lookup"><span data-stu-id="1f8f4-111">Members</span></span>

#### <span data-ttu-id="1f8f4-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="1f8f4-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="1f8f4-113">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="1f8f4-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="1f8f4-114">Public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="1f8f4-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


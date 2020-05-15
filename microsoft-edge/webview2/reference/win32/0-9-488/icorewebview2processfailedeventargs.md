---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 0efc1656b8204b9775002db49e0e4a5734682cc4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653723"
---
# <span data-ttu-id="f9197-104">Schnittstellen ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f9197-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="f9197-105">Ereignis-args für das ProcessFailed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f9197-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="f9197-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f9197-106">Summary</span></span>

 <span data-ttu-id="f9197-107">Member</span><span class="sxs-lookup"><span data-stu-id="f9197-107">Members</span></span>                        | <span data-ttu-id="f9197-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f9197-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f9197-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="f9197-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="f9197-110">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="f9197-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="f9197-111">Member</span><span class="sxs-lookup"><span data-stu-id="f9197-111">Members</span></span>

#### <span data-ttu-id="f9197-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="f9197-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="f9197-113">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="f9197-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="f9197-114">Public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="f9197-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


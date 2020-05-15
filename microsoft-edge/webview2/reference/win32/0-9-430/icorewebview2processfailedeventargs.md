---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8fba2759ce0e264dcde515ee1191ec819f26eef9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653930"
---
# <span data-ttu-id="16464-104">Schnittstellen ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="16464-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="16464-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="16464-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="16464-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="16464-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="16464-107">Ereignis-args für das ProcessFailed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="16464-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="16464-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="16464-108">Summary</span></span>

 <span data-ttu-id="16464-109">Member</span><span class="sxs-lookup"><span data-stu-id="16464-109">Members</span></span>                        | <span data-ttu-id="16464-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="16464-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="16464-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="16464-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="16464-112">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="16464-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="16464-113">Member</span><span class="sxs-lookup"><span data-stu-id="16464-113">Members</span></span>

#### <span data-ttu-id="16464-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="16464-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="16464-115">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="16464-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="16464-116">Public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="16464-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 80ea596f28d1afeb451ce20d495961ca4eed507a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878113"
---
# <span data-ttu-id="310d6-104">0.8.355-Interface-IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="310d6-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs2</span></span> 

> [!NOTE]
> <span data-ttu-id="310d6-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="310d6-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="310d6-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="310d6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="310d6-107">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="310d6-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="310d6-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="310d6-108">Summary</span></span>

 <span data-ttu-id="310d6-109">Member</span><span class="sxs-lookup"><span data-stu-id="310d6-109">Members</span></span>                        | <span data-ttu-id="310d6-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="310d6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="310d6-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="310d6-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="310d6-112">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="310d6-112">The web resource request contexts.</span></span>

## <span data-ttu-id="310d6-113">Member</span><span class="sxs-lookup"><span data-stu-id="310d6-113">Members</span></span>

#### <span data-ttu-id="310d6-114">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="310d6-114">get_ResourceContext</span></span> 

<span data-ttu-id="310d6-115">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="310d6-115">The web resource request contexts.</span></span>

> <span data-ttu-id="310d6-116">öffentliche HRESULT- [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \*-Kontext)</span><span class="sxs-lookup"><span data-stu-id="310d6-116">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>


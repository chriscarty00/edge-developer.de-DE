---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 7f710b4da71a4a4e61869f06e5d2a4a95a2d0891
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885709"
---
# <span data-ttu-id="891de-104">0.8.355-Interface-IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="891de-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="891de-105">Ereignis-args für das WebResourceRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="891de-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="891de-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="891de-106">Summary</span></span>

 <span data-ttu-id="891de-107">Member</span><span class="sxs-lookup"><span data-stu-id="891de-107">Members</span></span>                        | <span data-ttu-id="891de-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="891de-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="891de-109">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="891de-109">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="891de-110">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="891de-110">The web resource request contexts.</span></span>

## <span data-ttu-id="891de-111">Member</span><span class="sxs-lookup"><span data-stu-id="891de-111">Members</span></span>

#### <span data-ttu-id="891de-112">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="891de-112">get_ResourceContext</span></span> 

<span data-ttu-id="891de-113">Der Webressource-Anforderungskontext.</span><span class="sxs-lookup"><span data-stu-id="891de-113">The web resource request contexts.</span></span>

> <span data-ttu-id="891de-114">öffentliche HRESULT- [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \*-Kontext)</span><span class="sxs-lookup"><span data-stu-id="891de-114">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>


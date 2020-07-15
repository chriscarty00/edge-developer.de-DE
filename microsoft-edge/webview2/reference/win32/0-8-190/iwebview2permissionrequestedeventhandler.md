---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 3019f58ab1c0f01a63ddd906b6bd9e3137c0d0ee
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878337"
---
# <span data-ttu-id="258e0-104">0.8.355-Interface-IWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="258e0-104">0.8.355 - interface IWebView2PermissionRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="258e0-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="258e0-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="258e0-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="258e0-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="258e0-107">Der Aufrufer implementiert diese Schnittstelle, um das PermissionRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="258e0-107">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="258e0-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="258e0-108">Summary</span></span>

 <span data-ttu-id="258e0-109">Member</span><span class="sxs-lookup"><span data-stu-id="258e0-109">Members</span></span>                        | <span data-ttu-id="258e0-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="258e0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="258e0-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="258e0-111">Invoke</span></span>](#invoke) | <span data-ttu-id="258e0-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="258e0-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="258e0-113">Member</span><span class="sxs-lookup"><span data-stu-id="258e0-113">Members</span></span>

#### <span data-ttu-id="258e0-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="258e0-114">Invoke</span></span> 

<span data-ttu-id="258e0-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="258e0-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="258e0-116">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="258e0-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span></span>


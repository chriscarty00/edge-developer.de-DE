---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 236dacec6db871fbc07c9f0067f3c8fa4fd6815d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880416"
---
# <span data-ttu-id="9b606-104">0.9.515-Interface-ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9b606-104">0.9.515 - interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="9b606-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="9b606-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="9b606-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="9b606-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="9b606-107">Der Aufrufer implementiert diese Schnittstelle, um das PermissionRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="9b606-107">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="9b606-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9b606-108">Summary</span></span>

 <span data-ttu-id="9b606-109">Member</span><span class="sxs-lookup"><span data-stu-id="9b606-109">Members</span></span>                        | <span data-ttu-id="9b606-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9b606-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9b606-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="9b606-111">Invoke</span></span>](#invoke) | <span data-ttu-id="9b606-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9b606-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="9b606-113">Member</span><span class="sxs-lookup"><span data-stu-id="9b606-113">Members</span></span>

#### <span data-ttu-id="9b606-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="9b606-114">Invoke</span></span> 

<span data-ttu-id="9b606-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9b606-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9b606-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="9b606-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>


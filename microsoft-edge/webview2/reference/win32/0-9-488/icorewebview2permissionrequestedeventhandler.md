---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 4ba3a5acd293b67947622ef4a409319164a23d35
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698029"
---
# <span data-ttu-id="8cc35-104">Schnittstellen ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8cc35-104">interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="8cc35-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="8cc35-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="8cc35-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="8cc35-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="8cc35-107">Der Aufrufer implementiert diese Schnittstelle, um das PermissionRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="8cc35-107">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="8cc35-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8cc35-108">Summary</span></span>

 <span data-ttu-id="8cc35-109">Member</span><span class="sxs-lookup"><span data-stu-id="8cc35-109">Members</span></span>                        | <span data-ttu-id="8cc35-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8cc35-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8cc35-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="8cc35-111">Invoke</span></span>](#invoke) | <span data-ttu-id="8cc35-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8cc35-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8cc35-113">Member</span><span class="sxs-lookup"><span data-stu-id="8cc35-113">Members</span></span>

#### <span data-ttu-id="8cc35-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="8cc35-114">Invoke</span></span> 

<span data-ttu-id="8cc35-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8cc35-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8cc35-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8cc35-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>


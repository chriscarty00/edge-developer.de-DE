---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: dc6af50c8e02bf556a5d6245be03bbe030fee9d6
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698772"
---
# <span data-ttu-id="e045d-104">Schnittstellen ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e045d-104">interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="e045d-105">Der Aufrufer implementiert diese Schnittstelle, um das PermissionRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e045d-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="e045d-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e045d-106">Summary</span></span>

 <span data-ttu-id="e045d-107">Member</span><span class="sxs-lookup"><span data-stu-id="e045d-107">Members</span></span>                        | <span data-ttu-id="e045d-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e045d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e045d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e045d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e045d-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e045d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e045d-111">Member</span><span class="sxs-lookup"><span data-stu-id="e045d-111">Members</span></span>

#### <span data-ttu-id="e045d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e045d-112">Invoke</span></span> 

<span data-ttu-id="e045d-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e045d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e045d-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e045d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>


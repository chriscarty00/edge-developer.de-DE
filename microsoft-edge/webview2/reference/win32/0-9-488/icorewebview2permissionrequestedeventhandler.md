---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e8e318caf3195afc58e9d4c33e09841377cbeb64
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884806"
---
# <span data-ttu-id="42d66-104">0.9.515-Interface-ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="42d66-104">0.9.515 - interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="42d66-105">Der Aufrufer implementiert diese Schnittstelle, um das PermissionRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="42d66-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="42d66-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="42d66-106">Summary</span></span>

 <span data-ttu-id="42d66-107">Member</span><span class="sxs-lookup"><span data-stu-id="42d66-107">Members</span></span>                        | <span data-ttu-id="42d66-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="42d66-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="42d66-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="42d66-109">Invoke</span></span>](#invoke) | <span data-ttu-id="42d66-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="42d66-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="42d66-111">Member</span><span class="sxs-lookup"><span data-stu-id="42d66-111">Members</span></span>

#### <span data-ttu-id="42d66-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="42d66-112">Invoke</span></span> 

<span data-ttu-id="42d66-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="42d66-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="42d66-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="42d66-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>


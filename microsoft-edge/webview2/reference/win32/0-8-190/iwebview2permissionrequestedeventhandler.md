---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: aeb6e2e25ca9f8c454f5dff891f2c488591d2a48
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884932"
---
# <span data-ttu-id="e599c-104">0.8.355-Interface-IWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e599c-104">0.8.355 - interface IWebView2PermissionRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="e599c-105">Der Aufrufer implementiert diese Schnittstelle, um das PermissionRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e599c-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="e599c-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e599c-106">Summary</span></span>

 <span data-ttu-id="e599c-107">Member</span><span class="sxs-lookup"><span data-stu-id="e599c-107">Members</span></span>                        | <span data-ttu-id="e599c-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e599c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e599c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e599c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e599c-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e599c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e599c-111">Member</span><span class="sxs-lookup"><span data-stu-id="e599c-111">Members</span></span>

#### <span data-ttu-id="e599c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e599c-112">Invoke</span></span> 

<span data-ttu-id="e599c-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e599c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e599c-114">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e599c-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span></span>


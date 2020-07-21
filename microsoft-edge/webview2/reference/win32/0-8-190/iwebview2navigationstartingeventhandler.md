---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: e6f47382eb3f086618a5d0c46c2eec57a9891ff5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885877"
---
# <span data-ttu-id="50513-104">0.8.355-Interface-IWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="50513-104">0.8.355 - interface IWebView2NavigationStartingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="50513-105">Der Aufrufer implementiert diese Schnittstelle, um das NavigationStarting-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="50513-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="50513-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="50513-106">Summary</span></span>

 <span data-ttu-id="50513-107">Member</span><span class="sxs-lookup"><span data-stu-id="50513-107">Members</span></span>                        | <span data-ttu-id="50513-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="50513-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="50513-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="50513-109">Invoke</span></span>](#invoke) | <span data-ttu-id="50513-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="50513-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="50513-111">Member</span><span class="sxs-lookup"><span data-stu-id="50513-111">Members</span></span>

#### <span data-ttu-id="50513-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="50513-112">Invoke</span></span> 

<span data-ttu-id="50513-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="50513-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="50513-114">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NavigationStartingEventArgs](IWebView2NavigationStartingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="50513-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NavigationStartingEventArgs](IWebView2NavigationStartingEventArgs.md) \* args)</span></span>


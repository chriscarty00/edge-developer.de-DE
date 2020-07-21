---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 57a0b844181c7c1ea14a56e87cc11dc008773a28
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886304"
---
# <span data-ttu-id="f0838-104">0.9.430-Interface-ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f0838-104">0.9.430 - interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="f0838-105">Der Aufrufer implementiert diese Schnittstelle, um das NavigationCompleted-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f0838-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="f0838-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f0838-106">Summary</span></span>

 <span data-ttu-id="f0838-107">Member</span><span class="sxs-lookup"><span data-stu-id="f0838-107">Members</span></span>                        | <span data-ttu-id="f0838-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f0838-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f0838-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f0838-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f0838-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f0838-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f0838-111">Member</span><span class="sxs-lookup"><span data-stu-id="f0838-111">Members</span></span>

#### <span data-ttu-id="f0838-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f0838-112">Invoke</span></span> 

<span data-ttu-id="f0838-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f0838-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f0838-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2NavigationCompletedEventArgs](ICoreWebView2NavigationCompletedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f0838-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationCompletedEventArgs](ICoreWebView2NavigationCompletedEventArgs.md) \* args)</span></span>


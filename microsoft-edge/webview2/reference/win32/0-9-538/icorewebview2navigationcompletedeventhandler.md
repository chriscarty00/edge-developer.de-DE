---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NavigationCompletedEventHandler
ms.openlocfilehash: 24651585298998eaa42b2be242785de1bf4d6f84
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879793"
---
# <span data-ttu-id="c63c8-104">Schnittstellen ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c63c8-104">interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="c63c8-105">Der Aufrufer implementiert diese Schnittstelle, um das NavigationCompleted-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c63c8-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="c63c8-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c63c8-106">Summary</span></span>

 <span data-ttu-id="c63c8-107">Member</span><span class="sxs-lookup"><span data-stu-id="c63c8-107">Members</span></span>                        | <span data-ttu-id="c63c8-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c63c8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c63c8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c63c8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c63c8-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c63c8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c63c8-111">Member</span><span class="sxs-lookup"><span data-stu-id="c63c8-111">Members</span></span>

#### <span data-ttu-id="c63c8-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c63c8-112">Invoke</span></span> 

<span data-ttu-id="c63c8-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c63c8-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c63c8-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c63c8-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>


---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ProcessFailedEventHandler
ms.openlocfilehash: 5ae5a64bfbcd0692d7c284974e960f9ed6249e50
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877399"
---
# <span data-ttu-id="e5f66-104">Schnittstellen ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e5f66-104">interface ICoreWebView2ProcessFailedEventHandler</span></span> 

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="e5f66-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ProcessFailed-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="e5f66-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="e5f66-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e5f66-106">Summary</span></span>

 <span data-ttu-id="e5f66-107">Member</span><span class="sxs-lookup"><span data-stu-id="e5f66-107">Members</span></span>                        | <span data-ttu-id="e5f66-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e5f66-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e5f66-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e5f66-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e5f66-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e5f66-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e5f66-111">Member</span><span class="sxs-lookup"><span data-stu-id="e5f66-111">Members</span></span>

#### <span data-ttu-id="e5f66-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e5f66-112">Invoke</span></span> 

<span data-ttu-id="e5f66-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e5f66-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e5f66-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e5f66-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>


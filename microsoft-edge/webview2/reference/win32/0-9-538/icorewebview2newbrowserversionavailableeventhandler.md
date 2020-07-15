---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NewBrowserVersionAvailableEventHandler
ms.openlocfilehash: 82a5e73b8b928897e5c0af1610631c9e7d636337
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879744"
---
# <span data-ttu-id="f3122-104">Schnittstellen ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="f3122-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="f3122-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von NewBrowserVersionAvailable-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="f3122-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="f3122-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f3122-106">Summary</span></span>

 <span data-ttu-id="f3122-107">Member</span><span class="sxs-lookup"><span data-stu-id="f3122-107">Members</span></span>                        | <span data-ttu-id="f3122-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f3122-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f3122-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f3122-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f3122-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f3122-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f3122-111">Member</span><span class="sxs-lookup"><span data-stu-id="f3122-111">Members</span></span>

#### <span data-ttu-id="f3122-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f3122-112">Invoke</span></span> 

<span data-ttu-id="f3122-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f3122-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f3122-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f3122-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>


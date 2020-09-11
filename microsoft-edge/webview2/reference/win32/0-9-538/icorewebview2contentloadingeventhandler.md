---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ContentLoadingEventHandler
ms.openlocfilehash: 906b09ad99d6d6d9e74c52c0582584b9e46f74ba
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010537"
---
# <span data-ttu-id="fb450-104">0.9.579-Interface-ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="fb450-104">0.9.579 - interface ICoreWebView2ContentLoadingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="fb450-105">Der Aufrufer implementiert diese Schnittstelle, um das ContentLoading-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="fb450-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="fb450-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fb450-106">Summary</span></span>

 <span data-ttu-id="fb450-107">Member</span><span class="sxs-lookup"><span data-stu-id="fb450-107">Members</span></span>                        | <span data-ttu-id="fb450-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="fb450-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fb450-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="fb450-109">Invoke</span></span>](#invoke) | <span data-ttu-id="fb450-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fb450-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="fb450-111">Member</span><span class="sxs-lookup"><span data-stu-id="fb450-111">Members</span></span>

#### <span data-ttu-id="fb450-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="fb450-112">Invoke</span></span> 

<span data-ttu-id="fb450-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fb450-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fb450-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="fb450-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>


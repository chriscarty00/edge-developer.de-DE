---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ContentLoadingEventHandler
ms.openlocfilehash: fb6e3cfabae0116ac746d6e8e5cc03efa0f1c1b6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877447"
---
# <span data-ttu-id="8f6f7-104">Schnittstellen ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="8f6f7-104">interface ICoreWebView2ContentLoadingEventHandler</span></span> 

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="8f6f7-105">Der Aufrufer implementiert diese Schnittstelle, um das ContentLoading-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="8f6f7-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="8f6f7-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8f6f7-106">Summary</span></span>

 <span data-ttu-id="8f6f7-107">Member</span><span class="sxs-lookup"><span data-stu-id="8f6f7-107">Members</span></span>                        | <span data-ttu-id="8f6f7-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8f6f7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8f6f7-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="8f6f7-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8f6f7-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8f6f7-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8f6f7-111">Member</span><span class="sxs-lookup"><span data-stu-id="8f6f7-111">Members</span></span>

#### <span data-ttu-id="8f6f7-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="8f6f7-112">Invoke</span></span> 

<span data-ttu-id="8f6f7-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8f6f7-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8f6f7-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8f6f7-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>


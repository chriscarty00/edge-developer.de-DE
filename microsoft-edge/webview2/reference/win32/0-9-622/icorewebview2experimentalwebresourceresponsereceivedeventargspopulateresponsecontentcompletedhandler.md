---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: 6c97e0591d55570f4076f6a5c4f2eebc2cc7c5ad
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012030"
---
# <span data-ttu-id="af660-104">Schnittstellen ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="af660-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="af660-105">Vervollständigungshandler für PopulateResponseContent-Async-Methode.</span><span class="sxs-lookup"><span data-stu-id="af660-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="af660-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="af660-106">Summary</span></span>

 <span data-ttu-id="af660-107">Member</span><span class="sxs-lookup"><span data-stu-id="af660-107">Members</span></span>                        | <span data-ttu-id="af660-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="af660-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="af660-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="af660-109">Invoke</span></span>](#invoke) | <span data-ttu-id="af660-110">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="af660-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="af660-111">Sie wird aufgerufen, wenn der Inhaltsdatenstrom der Antwort eines WebResourceResponseReceieved-Ereignisses verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="af660-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="af660-112">Member</span><span class="sxs-lookup"><span data-stu-id="af660-112">Members</span></span>

#### <span data-ttu-id="af660-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="af660-113">Invoke</span></span> 

<span data-ttu-id="af660-114">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="af660-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="af660-115">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode)</span><span class="sxs-lookup"><span data-stu-id="af660-115">public HRESULT [Invoke](#invoke)(HRESULT errorCode)</span></span>


---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: c021cfa866e55bfdf30185eeaf6015db1b523271
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886541"
---
# <span data-ttu-id="13aa2-104">Schnittstellen ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="13aa2-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="13aa2-105">Vervollständigungshandler für PopulateResponseContent-Async-Methode.</span><span class="sxs-lookup"><span data-stu-id="13aa2-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="13aa2-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="13aa2-106">Summary</span></span>

 <span data-ttu-id="13aa2-107">Member</span><span class="sxs-lookup"><span data-stu-id="13aa2-107">Members</span></span>                        | <span data-ttu-id="13aa2-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="13aa2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="13aa2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="13aa2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="13aa2-110">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="13aa2-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="13aa2-111">Sie wird aufgerufen, wenn der Inhaltsdatenstrom der Antwort eines WebResourceResponseReceieved-Ereignisses verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="13aa2-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="13aa2-112">Member</span><span class="sxs-lookup"><span data-stu-id="13aa2-112">Members</span></span>

#### <span data-ttu-id="13aa2-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="13aa2-113">Invoke</span></span> 

<span data-ttu-id="13aa2-114">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="13aa2-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="13aa2-115">Public HRESULT [Invoke](#invoke)(HRESULT-Ergebnis)</span><span class="sxs-lookup"><span data-stu-id="13aa2-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


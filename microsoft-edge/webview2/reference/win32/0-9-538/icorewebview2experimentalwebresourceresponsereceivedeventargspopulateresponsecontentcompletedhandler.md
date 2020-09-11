---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: 6a854eb9ca73f45e366edfa144c273f780bcee94
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011412"
---
# <span data-ttu-id="eebb2-104">0.9.579-Interface-ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="eebb2-104">0.9.579 - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="eebb2-105">Vervollständigungshandler für PopulateResponseContent-Async-Methode.</span><span class="sxs-lookup"><span data-stu-id="eebb2-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="eebb2-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="eebb2-106">Summary</span></span>

 <span data-ttu-id="eebb2-107">Member</span><span class="sxs-lookup"><span data-stu-id="eebb2-107">Members</span></span>                        | <span data-ttu-id="eebb2-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="eebb2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eebb2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="eebb2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="eebb2-110">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eebb2-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="eebb2-111">Sie wird aufgerufen, wenn der Inhaltsdatenstrom der Antwort eines WebResourceResponseReceieved-Ereignisses verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="eebb2-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="eebb2-112">Member</span><span class="sxs-lookup"><span data-stu-id="eebb2-112">Members</span></span>

#### <span data-ttu-id="eebb2-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="eebb2-113">Invoke</span></span> 

<span data-ttu-id="eebb2-114">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eebb2-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="eebb2-115">Public HRESULT [Invoke](#invoke)(HRESULT-Ergebnis)</span><span class="sxs-lookup"><span data-stu-id="eebb2-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


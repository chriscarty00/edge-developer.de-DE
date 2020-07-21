---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: ab811f717c90ce77293c74a0e54bd3a66c896e72
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885268"
---
# <span data-ttu-id="e6966-104">Schnittstellen ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e6966-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e6966-105">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2CompositionController erstellte CoreWebView2Controller zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e6966-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="e6966-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e6966-106">Summary</span></span>

 <span data-ttu-id="e6966-107">Member</span><span class="sxs-lookup"><span data-stu-id="e6966-107">Members</span></span>                        | <span data-ttu-id="e6966-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e6966-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e6966-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e6966-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e6966-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e6966-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e6966-111">Member</span><span class="sxs-lookup"><span data-stu-id="e6966-111">Members</span></span>

#### <span data-ttu-id="e6966-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e6966-112">Invoke</span></span> 

<span data-ttu-id="e6966-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e6966-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e6966-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="e6966-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>


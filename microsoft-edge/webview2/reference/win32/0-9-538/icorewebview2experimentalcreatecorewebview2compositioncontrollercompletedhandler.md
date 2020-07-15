---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: 898b76b1865cbda1909fa710707019582439db93
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879996"
---
# <span data-ttu-id="de108-104">Schnittstellen ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="de108-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="de108-105">Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.538 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="de108-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="de108-106">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2CompositionController erstellte CoreWebView2Controller zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="de108-106">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="de108-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="de108-107">Summary</span></span>

 <span data-ttu-id="de108-108">Member</span><span class="sxs-lookup"><span data-stu-id="de108-108">Members</span></span>                        | <span data-ttu-id="de108-109">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="de108-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="de108-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="de108-110">Invoke</span></span>](#invoke) | <span data-ttu-id="de108-111">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="de108-111">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="de108-112">Member</span><span class="sxs-lookup"><span data-stu-id="de108-112">Members</span></span>

#### <span data-ttu-id="de108-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="de108-113">Invoke</span></span> 

<span data-ttu-id="de108-114">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="de108-114">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="de108-115">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="de108-115">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>


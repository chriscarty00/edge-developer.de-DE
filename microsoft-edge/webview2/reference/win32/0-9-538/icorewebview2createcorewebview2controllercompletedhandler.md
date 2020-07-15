---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: e26d711c24758f82d42067fa28e71bc6ac1177ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877413"
---
# <span data-ttu-id="e2d8f-104">Schnittstellen ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e2d8f-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e2d8f-105">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Controller erstellte CoreWebView2Controller zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e2d8f-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="e2d8f-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e2d8f-106">Summary</span></span>

 <span data-ttu-id="e2d8f-107">Member</span><span class="sxs-lookup"><span data-stu-id="e2d8f-107">Members</span></span>                        | <span data-ttu-id="e2d8f-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e2d8f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e2d8f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e2d8f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e2d8f-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e2d8f-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e2d8f-111">Member</span><span class="sxs-lookup"><span data-stu-id="e2d8f-111">Members</span></span>

#### <span data-ttu-id="e2d8f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e2d8f-112">Invoke</span></span> 

<span data-ttu-id="e2d8f-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e2d8f-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e2d8f-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="e2d8f-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>


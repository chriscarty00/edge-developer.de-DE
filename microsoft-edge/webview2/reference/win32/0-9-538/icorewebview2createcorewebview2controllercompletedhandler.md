---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: 3ecafb8181b04032bf121a93af3771cfcad8fa91
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011167"
---
# <span data-ttu-id="d3c1d-104">0.9.579-Interface-ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="d3c1d-104">0.9.579 - interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="d3c1d-105">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Controller erstellte CoreWebView2Controller zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="d3c1d-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d3c1d-106">Summary</span></span>

 <span data-ttu-id="d3c1d-107">Member</span><span class="sxs-lookup"><span data-stu-id="d3c1d-107">Members</span></span>                        | <span data-ttu-id="d3c1d-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d3c1d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d3c1d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d3c1d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d3c1d-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="d3c1d-111">Member</span><span class="sxs-lookup"><span data-stu-id="d3c1d-111">Members</span></span>

#### <span data-ttu-id="d3c1d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="d3c1d-112">Invoke</span></span> 

<span data-ttu-id="d3c1d-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="d3c1d-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="d3c1d-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>


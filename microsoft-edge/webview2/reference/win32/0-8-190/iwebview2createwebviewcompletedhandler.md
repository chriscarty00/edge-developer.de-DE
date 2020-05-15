---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 2788a18898da1f878520f4c4eb072c1a8b43375b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653727"
---
# <span data-ttu-id="dae2e-104">Schnittstellen IWebView2CreateWebViewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="dae2e-104">interface IWebView2CreateWebViewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="dae2e-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="dae2e-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="dae2e-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="dae2e-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CreateWebViewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="dae2e-107">Der Aufrufer implementiert diese Schnittstelle, um die über WebView erstellte WebView zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="dae2e-107">The caller implements this interface to receive the WebView created via CreateWebView.</span></span>

## <span data-ttu-id="dae2e-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="dae2e-108">Summary</span></span>

 <span data-ttu-id="dae2e-109">Member</span><span class="sxs-lookup"><span data-stu-id="dae2e-109">Members</span></span>                        | <span data-ttu-id="dae2e-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="dae2e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dae2e-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="dae2e-111">Invoke</span></span>](#invoke) | <span data-ttu-id="dae2e-112">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="dae2e-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="dae2e-113">Member</span><span class="sxs-lookup"><span data-stu-id="dae2e-113">Members</span></span>

#### <span data-ttu-id="dae2e-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="dae2e-114">Invoke</span></span> 

<span data-ttu-id="dae2e-115">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="dae2e-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="dae2e-116">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis,[IWebView2WebView](IWebView2WebView.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="dae2e-116">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2WebView](IWebView2WebView.md) \* webView)</span></span>


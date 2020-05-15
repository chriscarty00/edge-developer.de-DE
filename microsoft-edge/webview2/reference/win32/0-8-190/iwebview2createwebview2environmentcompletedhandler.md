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
ms.openlocfilehash: 7a4e074d445b4bab11e8e79dc6cfe5346effbb3f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654070"
---
# <span data-ttu-id="c89ce-104">Schnittstellen IWebView2CreateWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="c89ce-104">interface IWebView2CreateWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="c89ce-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="c89ce-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="c89ce-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="c89ce-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CreateWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="c89ce-107">Der Aufrufer implementiert diese Schnittstelle, um die über CreateWebView2Environment erstellte WebView2Environment zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c89ce-107">The caller implements this interface to receive the WebView2Environment created via CreateWebView2Environment.</span></span>

## <span data-ttu-id="c89ce-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c89ce-108">Summary</span></span>

 <span data-ttu-id="c89ce-109">Member</span><span class="sxs-lookup"><span data-stu-id="c89ce-109">Members</span></span>                        | <span data-ttu-id="c89ce-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c89ce-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c89ce-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="c89ce-111">Invoke</span></span>](#invoke) | <span data-ttu-id="c89ce-112">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c89ce-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="c89ce-113">Member</span><span class="sxs-lookup"><span data-stu-id="c89ce-113">Members</span></span>

#### <span data-ttu-id="c89ce-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="c89ce-114">Invoke</span></span> 

<span data-ttu-id="c89ce-115">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c89ce-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="c89ce-116">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span><span class="sxs-lookup"><span data-stu-id="c89ce-116">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span></span>


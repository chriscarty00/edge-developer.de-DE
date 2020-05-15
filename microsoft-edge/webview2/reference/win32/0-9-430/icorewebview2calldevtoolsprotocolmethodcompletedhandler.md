---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: d7f44614e7322759446812481c9fa05c807b5eac
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653886"
---
# <span data-ttu-id="e44e7-104">Schnittstellen ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e44e7-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e44e7-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="e44e7-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="e44e7-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e44e7-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e44e7-107">Der Aufrufer implementiert diese Schnittstelle, um CallDevToolsProtocolMethod-Abschlussergebnisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e44e7-107">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="e44e7-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e44e7-108">Summary</span></span>

 <span data-ttu-id="e44e7-109">Member</span><span class="sxs-lookup"><span data-stu-id="e44e7-109">Members</span></span>                        | <span data-ttu-id="e44e7-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e44e7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e44e7-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="e44e7-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e44e7-112">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e44e7-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e44e7-113">Member</span><span class="sxs-lookup"><span data-stu-id="e44e7-113">Members</span></span>

#### <span data-ttu-id="e44e7-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="e44e7-114">Invoke</span></span> 

<span data-ttu-id="e44e7-115">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e44e7-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e44e7-116">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="e44e7-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR returnObjectAsJson)</span></span>


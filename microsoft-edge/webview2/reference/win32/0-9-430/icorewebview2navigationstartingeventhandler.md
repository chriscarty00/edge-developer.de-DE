---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ce6673f8cf188ba4f1d6d9b4dc847464a7e39f61
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654083"
---
# <span data-ttu-id="aea11-104">Schnittstellen ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="aea11-104">interface ICoreWebView2NavigationStartingEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="aea11-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="aea11-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="aea11-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="aea11-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="aea11-107">Der Aufrufer implementiert diese Schnittstelle, um das NavigationStarting-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="aea11-107">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="aea11-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="aea11-108">Summary</span></span>

 <span data-ttu-id="aea11-109">Member</span><span class="sxs-lookup"><span data-stu-id="aea11-109">Members</span></span>                        | <span data-ttu-id="aea11-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="aea11-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aea11-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="aea11-111">Invoke</span></span>](#invoke) | <span data-ttu-id="aea11-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="aea11-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="aea11-113">Member</span><span class="sxs-lookup"><span data-stu-id="aea11-113">Members</span></span>

#### <span data-ttu-id="aea11-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="aea11-114">Invoke</span></span> 

<span data-ttu-id="aea11-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="aea11-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="aea11-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2NavigationStartingEventArgs](ICoreWebView2NavigationStartingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="aea11-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationStartingEventArgs](ICoreWebView2NavigationStartingEventArgs.md) \* args)</span></span>


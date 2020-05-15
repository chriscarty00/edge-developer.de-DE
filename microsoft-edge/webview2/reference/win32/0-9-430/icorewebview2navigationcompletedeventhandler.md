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
ms.openlocfilehash: 9a1f86bbc3f07b67cccb3c5c47fe7032bd13844e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654111"
---
# <span data-ttu-id="f7ba1-104">Schnittstellen ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f7ba1-104">interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f7ba1-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="f7ba1-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f7ba1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="f7ba1-107">Der Aufrufer implementiert diese Schnittstelle, um das NavigationCompleted-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-107">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="f7ba1-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f7ba1-108">Summary</span></span>

 <span data-ttu-id="f7ba1-109">Member</span><span class="sxs-lookup"><span data-stu-id="f7ba1-109">Members</span></span>                        | <span data-ttu-id="f7ba1-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f7ba1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f7ba1-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="f7ba1-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f7ba1-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f7ba1-113">Member</span><span class="sxs-lookup"><span data-stu-id="f7ba1-113">Members</span></span>

#### <span data-ttu-id="f7ba1-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f7ba1-114">Invoke</span></span> 

<span data-ttu-id="f7ba1-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f7ba1-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f7ba1-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2NavigationCompletedEventArgs](ICoreWebView2NavigationCompletedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f7ba1-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationCompletedEventArgs](ICoreWebView2NavigationCompletedEventArgs.md) \* args)</span></span>


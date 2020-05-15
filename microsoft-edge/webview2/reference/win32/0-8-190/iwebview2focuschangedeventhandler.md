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
ms.openlocfilehash: 23cce166d4ef2d05b6ffe5814c1568f75a72be0e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653783"
---
# <span data-ttu-id="e9d66-104">Schnittstellen IWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9d66-104">interface IWebView2FocusChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e9d66-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="e9d66-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e9d66-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d66-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e9d66-107">Der Aufrufer implementiert diese Methode, um das GotFocus-Ereignis und das LostFocus-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e9d66-107">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="e9d66-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e9d66-108">Summary</span></span>

 <span data-ttu-id="e9d66-109">Member</span><span class="sxs-lookup"><span data-stu-id="e9d66-109">Members</span></span>                        | <span data-ttu-id="e9d66-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e9d66-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e9d66-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="e9d66-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e9d66-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e9d66-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e9d66-113">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e9d66-113">There are no event args for this event.</span></span>

## <span data-ttu-id="e9d66-114">Member</span><span class="sxs-lookup"><span data-stu-id="e9d66-114">Members</span></span>

#### <span data-ttu-id="e9d66-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="e9d66-115">Invoke</span></span> 

<span data-ttu-id="e9d66-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e9d66-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e9d66-117">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e9d66-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="e9d66-118">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="e9d66-118">There are no event args and the args parameter will be null.</span></span>


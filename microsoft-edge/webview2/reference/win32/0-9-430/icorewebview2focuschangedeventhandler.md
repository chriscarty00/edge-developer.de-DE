---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 20b9fe69f4aa02f2ec96082ec995bb5c1c4b218e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881046"
---
# <span data-ttu-id="ff4fe-104">0.9.430-Interface-ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ff4fe-104">0.9.430 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ff4fe-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="ff4fe-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ff4fe-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ff4fe-107">Der Aufrufer implementiert diese Methode, um das GotFocus-Ereignis und das LostFocus-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-107">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="ff4fe-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ff4fe-108">Summary</span></span>

 <span data-ttu-id="ff4fe-109">Member</span><span class="sxs-lookup"><span data-stu-id="ff4fe-109">Members</span></span>                        | <span data-ttu-id="ff4fe-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ff4fe-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ff4fe-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="ff4fe-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ff4fe-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ff4fe-113">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-113">There are no event args for this event.</span></span>

## <span data-ttu-id="ff4fe-114">Member</span><span class="sxs-lookup"><span data-stu-id="ff4fe-114">Members</span></span>

#### <span data-ttu-id="ff4fe-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="ff4fe-115">Invoke</span></span> 

<span data-ttu-id="ff4fe-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ff4fe-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ff4fe-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="ff4fe-118">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-118">There are no event args and the args parameter will be null.</span></span>


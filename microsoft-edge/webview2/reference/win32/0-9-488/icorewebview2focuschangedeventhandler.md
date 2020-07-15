---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: f4976cc5077f211970a953cebe7f2c3647879861
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880600"
---
# <span data-ttu-id="54166-104">0.9.515-Interface-ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="54166-104">0.9.515 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="54166-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="54166-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="54166-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="54166-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="54166-107">Der Aufrufer implementiert diese Methode, um das GotFocus-Ereignis und das LostFocus-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="54166-107">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="54166-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="54166-108">Summary</span></span>

 <span data-ttu-id="54166-109">Member</span><span class="sxs-lookup"><span data-stu-id="54166-109">Members</span></span>                        | <span data-ttu-id="54166-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="54166-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="54166-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="54166-111">Invoke</span></span>](#invoke) | <span data-ttu-id="54166-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="54166-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="54166-113">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="54166-113">There are no event args for this event.</span></span>

## <span data-ttu-id="54166-114">Member</span><span class="sxs-lookup"><span data-stu-id="54166-114">Members</span></span>

#### <span data-ttu-id="54166-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="54166-115">Invoke</span></span> 

<span data-ttu-id="54166-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="54166-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="54166-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="54166-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="54166-118">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="54166-118">There are no event args and the args parameter will be null.</span></span>


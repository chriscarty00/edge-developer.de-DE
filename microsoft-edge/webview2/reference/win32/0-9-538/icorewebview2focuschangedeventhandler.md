---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 6fc29b620df5bcd265a7576e4b7ca1c7ebd73e6f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698876"
---
# <span data-ttu-id="d6868-104">Schnittstellen ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d6868-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="d6868-105">Der Aufrufer implementiert diese Methode, um das GotFocus-Ereignis und das LostFocus-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d6868-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="d6868-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d6868-106">Summary</span></span>

 <span data-ttu-id="d6868-107">Member</span><span class="sxs-lookup"><span data-stu-id="d6868-107">Members</span></span>                        | <span data-ttu-id="d6868-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d6868-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d6868-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d6868-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d6868-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d6868-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="d6868-111">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d6868-111">There are no event args for this event.</span></span>

## <span data-ttu-id="d6868-112">Member</span><span class="sxs-lookup"><span data-stu-id="d6868-112">Members</span></span>

#### <span data-ttu-id="d6868-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="d6868-113">Invoke</span></span> 

<span data-ttu-id="d6868-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d6868-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d6868-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="d6868-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="d6868-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="d6868-116">There are no event args and the args parameter will be null.</span></span>


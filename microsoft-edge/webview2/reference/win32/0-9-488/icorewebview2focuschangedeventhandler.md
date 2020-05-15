---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e80dca6411534968822d9994f9911828a4fddeeb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653939"
---
# <span data-ttu-id="54951-104">Schnittstellen ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="54951-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="54951-105">Der Aufrufer implementiert diese Methode, um das GotFocus-Ereignis und das LostFocus-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="54951-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="54951-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="54951-106">Summary</span></span>

 <span data-ttu-id="54951-107">Member</span><span class="sxs-lookup"><span data-stu-id="54951-107">Members</span></span>                        | <span data-ttu-id="54951-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="54951-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="54951-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="54951-109">Invoke</span></span>](#invoke) | <span data-ttu-id="54951-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="54951-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="54951-111">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="54951-111">There are no event args for this event.</span></span>

## <span data-ttu-id="54951-112">Member</span><span class="sxs-lookup"><span data-stu-id="54951-112">Members</span></span>

#### <span data-ttu-id="54951-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="54951-113">Invoke</span></span> 

<span data-ttu-id="54951-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="54951-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="54951-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="54951-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="54951-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="54951-116">There are no event args and the args parameter will be null.</span></span>


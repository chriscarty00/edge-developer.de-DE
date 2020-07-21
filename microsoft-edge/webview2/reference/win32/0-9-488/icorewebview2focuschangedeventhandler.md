---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 5a0c15cf56283c9d2ba71b9f8261288977c6ef39
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885471"
---
# <span data-ttu-id="412b5-104">0.9.515-Interface-ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="412b5-104">0.9.515 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="412b5-105">Der Aufrufer implementiert diese Methode, um das GotFocus-Ereignis und das LostFocus-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="412b5-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="412b5-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="412b5-106">Summary</span></span>

 <span data-ttu-id="412b5-107">Member</span><span class="sxs-lookup"><span data-stu-id="412b5-107">Members</span></span>                        | <span data-ttu-id="412b5-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="412b5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="412b5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="412b5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="412b5-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="412b5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="412b5-111">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="412b5-111">There are no event args for this event.</span></span>

## <span data-ttu-id="412b5-112">Member</span><span class="sxs-lookup"><span data-stu-id="412b5-112">Members</span></span>

#### <span data-ttu-id="412b5-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="412b5-113">Invoke</span></span> 

<span data-ttu-id="412b5-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="412b5-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="412b5-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="412b5-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="412b5-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="412b5-116">There are no event args and the args parameter will be null.</span></span>


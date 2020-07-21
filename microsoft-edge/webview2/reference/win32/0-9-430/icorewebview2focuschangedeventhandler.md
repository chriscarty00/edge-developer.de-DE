---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ff7c4fb51916d17df3fddc3d183fe8831029703a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884148"
---
# <span data-ttu-id="74b65-104">0.9.430-Interface-ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="74b65-104">0.9.430 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="74b65-105">Der Aufrufer implementiert diese Methode, um das GotFocus-Ereignis und das LostFocus-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="74b65-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="74b65-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="74b65-106">Summary</span></span>

 <span data-ttu-id="74b65-107">Member</span><span class="sxs-lookup"><span data-stu-id="74b65-107">Members</span></span>                        | <span data-ttu-id="74b65-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="74b65-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="74b65-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="74b65-109">Invoke</span></span>](#invoke) | <span data-ttu-id="74b65-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="74b65-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="74b65-111">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="74b65-111">There are no event args for this event.</span></span>

## <span data-ttu-id="74b65-112">Member</span><span class="sxs-lookup"><span data-stu-id="74b65-112">Members</span></span>

#### <span data-ttu-id="74b65-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="74b65-113">Invoke</span></span> 

<span data-ttu-id="74b65-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="74b65-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="74b65-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="74b65-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="74b65-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="74b65-116">There are no event args and the args parameter will be null.</span></span>


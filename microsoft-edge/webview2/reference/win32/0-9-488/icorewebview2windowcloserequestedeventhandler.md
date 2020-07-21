---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 9163eb811e018e346f610dae71d5fdb7e39de186
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885436"
---
# <span data-ttu-id="9c4ca-104">0.9.515-Interface-ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9c4ca-104">0.9.515 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="9c4ca-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="9c4ca-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="9c4ca-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9c4ca-106">Summary</span></span>

 <span data-ttu-id="9c4ca-107">Member</span><span class="sxs-lookup"><span data-stu-id="9c4ca-107">Members</span></span>                        | <span data-ttu-id="9c4ca-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9c4ca-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9c4ca-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9c4ca-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9c4ca-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9c4ca-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="9c4ca-111">Member</span><span class="sxs-lookup"><span data-stu-id="9c4ca-111">Members</span></span>

#### <span data-ttu-id="9c4ca-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9c4ca-112">Invoke</span></span> 

<span data-ttu-id="9c4ca-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9c4ca-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9c4ca-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="9c4ca-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="9c4ca-115">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="9c4ca-115">There are no event args and the args parameter will be null.</span></span>


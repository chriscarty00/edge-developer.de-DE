---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 8b7a588122b93cf56f7ce4473db87a0df16522b7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885996"
---
# <span data-ttu-id="b0922-104">0.8.355-Interface-IWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b0922-104">0.8.355 - interface IWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="b0922-105">Der Aufrufer implementiert diese Methode, um das GotFocus-Ereignis und das LostFocus-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b0922-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="b0922-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b0922-106">Summary</span></span>

 <span data-ttu-id="b0922-107">Member</span><span class="sxs-lookup"><span data-stu-id="b0922-107">Members</span></span>                        | <span data-ttu-id="b0922-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b0922-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b0922-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b0922-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b0922-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b0922-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="b0922-111">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b0922-111">There are no event args for this event.</span></span>

## <span data-ttu-id="b0922-112">Member</span><span class="sxs-lookup"><span data-stu-id="b0922-112">Members</span></span>

#### <span data-ttu-id="b0922-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="b0922-113">Invoke</span></span> 

<span data-ttu-id="b0922-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b0922-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b0922-115">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b0922-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="b0922-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="b0922-116">There are no event args and the args parameter will be null.</span></span>


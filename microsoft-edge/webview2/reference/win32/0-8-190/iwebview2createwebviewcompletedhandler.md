---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2CreateWebViewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 381f46c6682a77905d9caa720e4ba9b2d1d531b7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886152"
---
# <span data-ttu-id="b9c68-104">0.8.355-Interface-IWebView2CreateWebViewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b9c68-104">0.8.355 - interface IWebView2CreateWebViewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CreateWebViewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b9c68-105">Der Aufrufer implementiert diese Schnittstelle, um die über WebView erstellte WebView zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b9c68-105">The caller implements this interface to receive the WebView created via CreateWebView.</span></span>

## <span data-ttu-id="b9c68-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b9c68-106">Summary</span></span>

 <span data-ttu-id="b9c68-107">Member</span><span class="sxs-lookup"><span data-stu-id="b9c68-107">Members</span></span>                        | <span data-ttu-id="b9c68-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b9c68-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b9c68-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b9c68-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b9c68-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b9c68-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b9c68-111">Member</span><span class="sxs-lookup"><span data-stu-id="b9c68-111">Members</span></span>

#### <span data-ttu-id="b9c68-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b9c68-112">Invoke</span></span> 

<span data-ttu-id="b9c68-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b9c68-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b9c68-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis,[IWebView2WebView](IWebView2WebView.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="b9c68-114">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2WebView](IWebView2WebView.md) \* webView)</span></span>


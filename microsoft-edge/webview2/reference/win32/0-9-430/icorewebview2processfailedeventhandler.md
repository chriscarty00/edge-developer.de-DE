---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ed9b94b5bd9015b07cf44cf2cbeec330688242ff
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884106"
---
# <span data-ttu-id="b1bc1-104">0.9.430-Interface-ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b1bc1-104">0.9.430 - interface ICoreWebView2ProcessFailedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="b1bc1-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ProcessFailed-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="b1bc1-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b1bc1-106">Summary</span></span>

 <span data-ttu-id="b1bc1-107">Member</span><span class="sxs-lookup"><span data-stu-id="b1bc1-107">Members</span></span>                        | <span data-ttu-id="b1bc1-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b1bc1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b1bc1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b1bc1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b1bc1-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b1bc1-111">Member</span><span class="sxs-lookup"><span data-stu-id="b1bc1-111">Members</span></span>

#### <span data-ttu-id="b1bc1-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b1bc1-112">Invoke</span></span> 

<span data-ttu-id="b1bc1-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b1bc1-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b1bc1-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2ProcessFailedEventArgs](ICoreWebView2ProcessFailedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b1bc1-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ProcessFailedEventArgs](ICoreWebView2ProcessFailedEventArgs.md) \* args)</span></span>


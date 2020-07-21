---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 3d6bf8345e88dde213c15e51c26056d0239f0230
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886110"
---
# <span data-ttu-id="d544c-104">0.8.355-Interface-IWebView2DocumentStateChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d544c-104">0.8.355 - interface IWebView2DocumentStateChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentStateChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="d544c-105">Der Aufrufer implementiert diese Schnittstelle, um das DocumentStateChanged-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d544c-105">The caller implements this interface to receive the DocumentStateChanged event.</span></span>

## <span data-ttu-id="d544c-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d544c-106">Summary</span></span>

 <span data-ttu-id="d544c-107">Member</span><span class="sxs-lookup"><span data-stu-id="d544c-107">Members</span></span>                        | <span data-ttu-id="d544c-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d544c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d544c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d544c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d544c-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d544c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d544c-111">Member</span><span class="sxs-lookup"><span data-stu-id="d544c-111">Members</span></span>

#### <span data-ttu-id="d544c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="d544c-112">Invoke</span></span> 

<span data-ttu-id="d544c-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d544c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d544c-114">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d544c-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span></span>


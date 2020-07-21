---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: d50f84edeb532d90a1268f553b38e4cbf256556a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884087"
---
# <span data-ttu-id="193d8-104">0.9.430-Interface-ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="193d8-104">0.9.430 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="193d8-105">Der Aufrufer implementiert diese Methode, um das MoveFocusRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="193d8-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="193d8-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="193d8-106">Summary</span></span>

 <span data-ttu-id="193d8-107">Member</span><span class="sxs-lookup"><span data-stu-id="193d8-107">Members</span></span>                        | <span data-ttu-id="193d8-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="193d8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="193d8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="193d8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="193d8-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="193d8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="193d8-111">Member</span><span class="sxs-lookup"><span data-stu-id="193d8-111">Members</span></span>

#### <span data-ttu-id="193d8-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="193d8-112">Invoke</span></span> 

<span data-ttu-id="193d8-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="193d8-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="193d8-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender;[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="193d8-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>


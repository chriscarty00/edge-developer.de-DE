---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 606b9f87dfbce1f4c9a899ad6f78ec8c52794682
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886392"
---
# <span data-ttu-id="a7cf1-104">0.9.430-Interface-ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a7cf1-104">0.9.430 - interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="a7cf1-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="a7cf1-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a7cf1-106">Summary</span></span>

 <span data-ttu-id="a7cf1-107">Member</span><span class="sxs-lookup"><span data-stu-id="a7cf1-107">Members</span></span>                        | <span data-ttu-id="a7cf1-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a7cf1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a7cf1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a7cf1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a7cf1-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a7cf1-111">Member</span><span class="sxs-lookup"><span data-stu-id="a7cf1-111">Members</span></span>

#### <span data-ttu-id="a7cf1-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a7cf1-112">Invoke</span></span> 

<span data-ttu-id="a7cf1-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a7cf1-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2NewWindowRequestedEventArgs](ICoreWebView2NewWindowRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a7cf1-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NewWindowRequestedEventArgs](ICoreWebView2NewWindowRequestedEventArgs.md) \* args)</span></span>


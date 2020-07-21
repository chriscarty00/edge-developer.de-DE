---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 53410d7592f6a217ffd72e410d46491c78262f87
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883868"
---
# <span data-ttu-id="8c4a0-104">0.9.515-Interface-ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="8c4a0-104">0.9.515 - interface ICoreWebView2ContentLoadingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="8c4a0-105">Der Aufrufer implementiert diese Schnittstelle, um das ContentLoading-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="8c4a0-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="8c4a0-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8c4a0-106">Summary</span></span>

 <span data-ttu-id="8c4a0-107">Member</span><span class="sxs-lookup"><span data-stu-id="8c4a0-107">Members</span></span>                        | <span data-ttu-id="8c4a0-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8c4a0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8c4a0-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="8c4a0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8c4a0-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8c4a0-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8c4a0-111">Member</span><span class="sxs-lookup"><span data-stu-id="8c4a0-111">Members</span></span>

#### <span data-ttu-id="8c4a0-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="8c4a0-112">Invoke</span></span> 

<span data-ttu-id="8c4a0-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8c4a0-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8c4a0-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8c4a0-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>


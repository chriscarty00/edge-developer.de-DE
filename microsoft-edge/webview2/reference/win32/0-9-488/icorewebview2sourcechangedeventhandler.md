---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b3eb56101c6e69bab018cbb549339fd5deb2eb3e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885191"
---
# <span data-ttu-id="042d2-104">0.9.515-Interface-ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="042d2-104">0.9.515 - interface ICoreWebView2SourceChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="042d2-105">Der Aufrufer implementiert diese Schnittstelle, um das Quellpfad-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="042d2-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="042d2-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="042d2-106">Summary</span></span>

 <span data-ttu-id="042d2-107">Member</span><span class="sxs-lookup"><span data-stu-id="042d2-107">Members</span></span>                        | <span data-ttu-id="042d2-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="042d2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="042d2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="042d2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="042d2-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="042d2-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="042d2-111">Member</span><span class="sxs-lookup"><span data-stu-id="042d2-111">Members</span></span>

#### <span data-ttu-id="042d2-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="042d2-112">Invoke</span></span> 

<span data-ttu-id="042d2-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="042d2-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="042d2-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="042d2-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>


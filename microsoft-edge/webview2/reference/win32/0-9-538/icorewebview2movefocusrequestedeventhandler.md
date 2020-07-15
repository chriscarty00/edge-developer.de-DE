---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2MoveFocusRequestedEventHandler
ms.openlocfilehash: b0e7f3f005b90c5656eeeac09716130544b0ee20
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879835"
---
# <span data-ttu-id="31c96-104">Schnittstellen ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="31c96-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="31c96-105">Der Aufrufer implementiert diese Methode, um das MoveFocusRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="31c96-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="31c96-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="31c96-106">Summary</span></span>

 <span data-ttu-id="31c96-107">Member</span><span class="sxs-lookup"><span data-stu-id="31c96-107">Members</span></span>                        | <span data-ttu-id="31c96-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="31c96-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="31c96-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="31c96-109">Invoke</span></span>](#invoke) | <span data-ttu-id="31c96-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="31c96-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="31c96-111">Member</span><span class="sxs-lookup"><span data-stu-id="31c96-111">Members</span></span>

#### <span data-ttu-id="31c96-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="31c96-112">Invoke</span></span> 

<span data-ttu-id="31c96-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="31c96-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="31c96-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="31c96-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>


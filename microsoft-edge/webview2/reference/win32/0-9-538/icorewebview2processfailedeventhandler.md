---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ProcessFailedEventHandler
ms.openlocfilehash: d65c6ae63f5c79540587f99e3ff42c4ebb3e409e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010831"
---
# <span data-ttu-id="7e61c-104">0.9.579-Interface-ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7e61c-104">0.9.579 - interface ICoreWebView2ProcessFailedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="7e61c-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ProcessFailed-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="7e61c-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="7e61c-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7e61c-106">Summary</span></span>

 <span data-ttu-id="7e61c-107">Member</span><span class="sxs-lookup"><span data-stu-id="7e61c-107">Members</span></span>                        | <span data-ttu-id="7e61c-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7e61c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7e61c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7e61c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7e61c-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7e61c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="7e61c-111">Member</span><span class="sxs-lookup"><span data-stu-id="7e61c-111">Members</span></span>

#### <span data-ttu-id="7e61c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="7e61c-112">Invoke</span></span> 

<span data-ttu-id="7e61c-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7e61c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7e61c-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7e61c-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>


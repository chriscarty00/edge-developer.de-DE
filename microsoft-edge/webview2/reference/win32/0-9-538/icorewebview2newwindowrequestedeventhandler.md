---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NewWindowRequestedEventHandler
ms.openlocfilehash: 6b9bf26b4788819d890d54b3484ee376a3968b87
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010820"
---
# <span data-ttu-id="b3d42-104">0.9.579-Interface-ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b3d42-104">0.9.579 - interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="b3d42-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="b3d42-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="b3d42-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b3d42-106">Summary</span></span>

 <span data-ttu-id="b3d42-107">Member</span><span class="sxs-lookup"><span data-stu-id="b3d42-107">Members</span></span>                        | <span data-ttu-id="b3d42-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b3d42-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b3d42-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b3d42-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b3d42-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b3d42-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b3d42-111">Member</span><span class="sxs-lookup"><span data-stu-id="b3d42-111">Members</span></span>

#### <span data-ttu-id="b3d42-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b3d42-112">Invoke</span></span> 

<span data-ttu-id="b3d42-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b3d42-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b3d42-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b3d42-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>


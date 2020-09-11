---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NewWindowRequestedEventHandler
ms.openlocfilehash: 99fb8261e6ed170b09bc87f9a1372e0e2cc53954
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012169"
---
# <span data-ttu-id="57536-104">Schnittstellen ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="57536-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="57536-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="57536-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="57536-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="57536-106">Summary</span></span>

 <span data-ttu-id="57536-107">Member</span><span class="sxs-lookup"><span data-stu-id="57536-107">Members</span></span>                        | <span data-ttu-id="57536-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="57536-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="57536-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="57536-109">Invoke</span></span>](#invoke) | <span data-ttu-id="57536-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="57536-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="57536-111">Member</span><span class="sxs-lookup"><span data-stu-id="57536-111">Members</span></span>

#### <span data-ttu-id="57536-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="57536-112">Invoke</span></span> 

<span data-ttu-id="57536-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="57536-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="57536-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="57536-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>


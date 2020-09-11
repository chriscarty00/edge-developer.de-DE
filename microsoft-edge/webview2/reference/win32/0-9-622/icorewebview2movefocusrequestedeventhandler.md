---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2MoveFocusRequestedEventHandler
ms.openlocfilehash: 89b1e7fada56bcf535ae07be109acbb340fdc9a8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012075"
---
# <span data-ttu-id="78f73-104">Schnittstellen ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="78f73-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="78f73-105">Der Aufrufer implementiert diese Methode, um das MoveFocusRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="78f73-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="78f73-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="78f73-106">Summary</span></span>

 <span data-ttu-id="78f73-107">Member</span><span class="sxs-lookup"><span data-stu-id="78f73-107">Members</span></span>                        | <span data-ttu-id="78f73-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="78f73-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="78f73-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="78f73-109">Invoke</span></span>](#invoke) | <span data-ttu-id="78f73-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="78f73-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="78f73-111">Member</span><span class="sxs-lookup"><span data-stu-id="78f73-111">Members</span></span>

#### <span data-ttu-id="78f73-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="78f73-112">Invoke</span></span> 

<span data-ttu-id="78f73-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="78f73-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="78f73-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="78f73-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>


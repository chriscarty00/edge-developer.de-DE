---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2MoveFocusRequestedEventHandler
ms.openlocfilehash: bd07256203944b4d640d859451fa000cbc1fcd46
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011320"
---
# <span data-ttu-id="29097-104">0.9.579-Interface-ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="29097-104">0.9.579 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="29097-105">Der Aufrufer implementiert diese Methode, um das MoveFocusRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="29097-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="29097-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="29097-106">Summary</span></span>

 <span data-ttu-id="29097-107">Member</span><span class="sxs-lookup"><span data-stu-id="29097-107">Members</span></span>                        | <span data-ttu-id="29097-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="29097-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="29097-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="29097-109">Invoke</span></span>](#invoke) | <span data-ttu-id="29097-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="29097-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="29097-111">Member</span><span class="sxs-lookup"><span data-stu-id="29097-111">Members</span></span>

#### <span data-ttu-id="29097-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="29097-112">Invoke</span></span> 

<span data-ttu-id="29097-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="29097-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="29097-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="29097-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>


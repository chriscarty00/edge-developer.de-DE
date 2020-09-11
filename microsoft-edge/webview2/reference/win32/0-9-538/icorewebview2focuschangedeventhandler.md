---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2FocusChangedEventHandler
ms.openlocfilehash: 7e02fb9480f70dbffe6d33cfd7fb436c26c97da3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011363"
---
# <span data-ttu-id="ec633-104">0.9.579-Interface-ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ec633-104">0.9.579 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ec633-105">Der Aufrufer implementiert diese Methode, um das GotFocus-Ereignis und das LostFocus-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ec633-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="ec633-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ec633-106">Summary</span></span>

 <span data-ttu-id="ec633-107">Member</span><span class="sxs-lookup"><span data-stu-id="ec633-107">Members</span></span>                        | <span data-ttu-id="ec633-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ec633-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ec633-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ec633-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ec633-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ec633-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ec633-111">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ec633-111">There are no event args for this event.</span></span>

## <span data-ttu-id="ec633-112">Member</span><span class="sxs-lookup"><span data-stu-id="ec633-112">Members</span></span>

#### <span data-ttu-id="ec633-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="ec633-113">Invoke</span></span> 

<span data-ttu-id="ec633-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ec633-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ec633-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ec633-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="ec633-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="ec633-116">There are no event args and the args parameter will be null.</span></span>


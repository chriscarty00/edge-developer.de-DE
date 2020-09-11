---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ContainsFullScreenElementChangedEventHandler
ms.openlocfilehash: e1c51ee30a7b61d5a5638adb4130b1add3bddb23
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010558"
---
# <span data-ttu-id="ea1fd-104">0.9.579-Interface-ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ea1fd-104">0.9.579 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ea1fd-105">Der Aufrufer implementiert diese Methode, um die ContainsFullScreenElementChanged-Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ea1fd-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="ea1fd-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ea1fd-106">Summary</span></span>

 <span data-ttu-id="ea1fd-107">Member</span><span class="sxs-lookup"><span data-stu-id="ea1fd-107">Members</span></span>                        | <span data-ttu-id="ea1fd-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ea1fd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ea1fd-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ea1fd-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ea1fd-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ea1fd-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ea1fd-111">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ea1fd-111">There are no event args for this event.</span></span>

## <span data-ttu-id="ea1fd-112">Member</span><span class="sxs-lookup"><span data-stu-id="ea1fd-112">Members</span></span>

#### <span data-ttu-id="ea1fd-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="ea1fd-113">Invoke</span></span> 

<span data-ttu-id="ea1fd-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ea1fd-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ea1fd-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ea1fd-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="ea1fd-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="ea1fd-116">There are no event args and the args parameter will be null.</span></span>


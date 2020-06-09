---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 05dd401064635a6b20f1936b1efaac025b45749f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698849"
---
# <span data-ttu-id="3f3b8-104">Schnittstellen ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3f3b8-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="3f3b8-105">Der Aufrufer implementiert diese Schnittstelle, um das AcceleratorKeyPressed-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="3f3b8-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="3f3b8-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3f3b8-106">Summary</span></span>

 <span data-ttu-id="3f3b8-107">Member</span><span class="sxs-lookup"><span data-stu-id="3f3b8-107">Members</span></span>                        | <span data-ttu-id="3f3b8-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3f3b8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3f3b8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3f3b8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3f3b8-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3f3b8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3f3b8-111">Member</span><span class="sxs-lookup"><span data-stu-id="3f3b8-111">Members</span></span>

#### <span data-ttu-id="3f3b8-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="3f3b8-112">Invoke</span></span> 

<span data-ttu-id="3f3b8-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3f3b8-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3f3b8-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3f3b8-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>


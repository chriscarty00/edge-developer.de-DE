---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 5f568c10f98a5375ffb0d0444b2b74b8a4e8c4c2
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697210"
---
# <span data-ttu-id="e0aa2-104">Schnittstellen ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e0aa2-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e0aa2-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="e0aa2-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e0aa2-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e0aa2-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="e0aa2-107">Der Aufrufer implementiert diese Schnittstelle, um das AcceleratorKeyPressed-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e0aa2-107">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="e0aa2-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e0aa2-108">Summary</span></span>

 <span data-ttu-id="e0aa2-109">Member</span><span class="sxs-lookup"><span data-stu-id="e0aa2-109">Members</span></span>                        | <span data-ttu-id="e0aa2-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e0aa2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e0aa2-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="e0aa2-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e0aa2-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e0aa2-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e0aa2-113">Member</span><span class="sxs-lookup"><span data-stu-id="e0aa2-113">Members</span></span>

#### <span data-ttu-id="e0aa2-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="e0aa2-114">Invoke</span></span> 

<span data-ttu-id="e0aa2-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e0aa2-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e0aa2-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e0aa2-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>


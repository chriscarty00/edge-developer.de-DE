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
ms.openlocfilehash: 2c109e02de28101c88ea55d849db5701f36795a9
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698796"
---
# <span data-ttu-id="a3f11-104">Schnittstellen ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a3f11-104">interface ICoreWebView2ProcessFailedEventHandler</span></span> 

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="a3f11-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ProcessFailed-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="a3f11-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="a3f11-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a3f11-106">Summary</span></span>

 <span data-ttu-id="a3f11-107">Member</span><span class="sxs-lookup"><span data-stu-id="a3f11-107">Members</span></span>                        | <span data-ttu-id="a3f11-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a3f11-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a3f11-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a3f11-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a3f11-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a3f11-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a3f11-111">Member</span><span class="sxs-lookup"><span data-stu-id="a3f11-111">Members</span></span>

#### <span data-ttu-id="a3f11-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a3f11-112">Invoke</span></span> 

<span data-ttu-id="a3f11-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a3f11-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a3f11-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a3f11-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>


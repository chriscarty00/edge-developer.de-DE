---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 2e12f96307b86fe4c3416c4bde2379869b269cb8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884358"
---
# <span data-ttu-id="22234-104">0.9.430-Interface-ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="22234-104">0.9.430 - interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="22234-105">Der Aufrufer implementiert diese Schnittstelle, um das AcceleratorKeyPressed-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="22234-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="22234-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="22234-106">Summary</span></span>

 <span data-ttu-id="22234-107">Member</span><span class="sxs-lookup"><span data-stu-id="22234-107">Members</span></span>                        | <span data-ttu-id="22234-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="22234-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="22234-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="22234-109">Invoke</span></span>](#invoke) | <span data-ttu-id="22234-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="22234-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="22234-111">Member</span><span class="sxs-lookup"><span data-stu-id="22234-111">Members</span></span>

#### <span data-ttu-id="22234-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="22234-112">Invoke</span></span> 

<span data-ttu-id="22234-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="22234-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="22234-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender;[ICoreWebView2AcceleratorKeyPressedEventArgs](ICoreWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="22234-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2AcceleratorKeyPressedEventArgs](ICoreWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span></span>


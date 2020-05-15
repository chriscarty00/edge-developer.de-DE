---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 30b879b1dd74d0194b9aad24af1cff9a5d34c43c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653967"
---
# <span data-ttu-id="ebac2-104">Schnittstellen IWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ebac2-104">interface IWebView2AcceleratorKeyPressedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ebac2-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="ebac2-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="ebac2-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ebac2-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="ebac2-107">Der Aufrufer implementiert diese Schnittstelle, um das AcceleratorKeyPressed-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ebac2-107">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="ebac2-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ebac2-108">Summary</span></span>

 <span data-ttu-id="ebac2-109">Member</span><span class="sxs-lookup"><span data-stu-id="ebac2-109">Members</span></span>                        | <span data-ttu-id="ebac2-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ebac2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ebac2-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="ebac2-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ebac2-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ebac2-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ebac2-113">Member</span><span class="sxs-lookup"><span data-stu-id="ebac2-113">Members</span></span>

#### <span data-ttu-id="ebac2-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="ebac2-114">Invoke</span></span> 

<span data-ttu-id="ebac2-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ebac2-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ebac2-116">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2AcceleratorKeyPressedEventArgs](IWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ebac2-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2AcceleratorKeyPressedEventArgs](IWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span></span>


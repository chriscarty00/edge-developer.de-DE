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
ms.openlocfilehash: d669b73edd8def1d8a44491705e0f80888da2b3f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653913"
---
# <span data-ttu-id="d7159-104">Schnittstellen IWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d7159-104">interface IWebView2PermissionRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="d7159-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="d7159-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="d7159-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="d7159-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="d7159-107">Der Aufrufer implementiert diese Schnittstelle, um das PermissionRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d7159-107">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="d7159-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d7159-108">Summary</span></span>

 <span data-ttu-id="d7159-109">Member</span><span class="sxs-lookup"><span data-stu-id="d7159-109">Members</span></span>                        | <span data-ttu-id="d7159-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d7159-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d7159-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="d7159-111">Invoke</span></span>](#invoke) | <span data-ttu-id="d7159-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d7159-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d7159-113">Member</span><span class="sxs-lookup"><span data-stu-id="d7159-113">Members</span></span>

#### <span data-ttu-id="d7159-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="d7159-114">Invoke</span></span> 

<span data-ttu-id="d7159-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d7159-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d7159-116">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d7159-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span></span>


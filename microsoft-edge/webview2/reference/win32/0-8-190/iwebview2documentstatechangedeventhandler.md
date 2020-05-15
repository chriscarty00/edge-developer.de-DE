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
ms.openlocfilehash: 062d6d3201acc71e58ab4cedd85f697f560bb7c0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653953"
---
# <span data-ttu-id="66739-104">Schnittstellen IWebView2DocumentStateChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="66739-104">interface IWebView2DocumentStateChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="66739-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="66739-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="66739-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="66739-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="66739-107">Der Aufrufer implementiert diese Schnittstelle, um das DocumentStateChanged-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="66739-107">The caller implements this interface to receive the DocumentStateChanged event.</span></span>

## <span data-ttu-id="66739-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="66739-108">Summary</span></span>

 <span data-ttu-id="66739-109">Member</span><span class="sxs-lookup"><span data-stu-id="66739-109">Members</span></span>                        | <span data-ttu-id="66739-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="66739-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="66739-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="66739-111">Invoke</span></span>](#invoke) | <span data-ttu-id="66739-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="66739-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="66739-113">Member</span><span class="sxs-lookup"><span data-stu-id="66739-113">Members</span></span>

#### <span data-ttu-id="66739-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="66739-114">Invoke</span></span> 

<span data-ttu-id="66739-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="66739-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="66739-116">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="66739-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span></span>


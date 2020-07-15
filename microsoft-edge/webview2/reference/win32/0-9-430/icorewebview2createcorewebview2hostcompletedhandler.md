---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2HostCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 6a707465fa08667e9915a77fdc93ee018e0f9631
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881123"
---
# <span data-ttu-id="67837-104">0.9.430-Interface-ICoreWebView2CreateCoreWebView2HostCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="67837-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="67837-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="67837-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="67837-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="67837-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2HostCompletedHandler
  : public IUnknown
```

<span data-ttu-id="67837-107">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Host erstellte CoreWebView2Host zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="67837-107">The caller implements this interface to receive the CoreWebView2Host created via CreateCoreWebView2Host.</span></span>

## <span data-ttu-id="67837-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="67837-108">Summary</span></span>

 <span data-ttu-id="67837-109">Member</span><span class="sxs-lookup"><span data-stu-id="67837-109">Members</span></span>                        | <span data-ttu-id="67837-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="67837-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="67837-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="67837-111">Invoke</span></span>](#invoke) | <span data-ttu-id="67837-112">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="67837-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="67837-113">Member</span><span class="sxs-lookup"><span data-stu-id="67837-113">Members</span></span>

#### <span data-ttu-id="67837-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="67837-114">Invoke</span></span> 

<span data-ttu-id="67837-115">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="67837-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="67837-116">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span><span class="sxs-lookup"><span data-stu-id="67837-116">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span></span>


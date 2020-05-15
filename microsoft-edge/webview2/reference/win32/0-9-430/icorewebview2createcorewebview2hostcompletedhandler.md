---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 1d2956aee178c2bdc581d51a93006e14cfb539e3
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653873"
---
# <span data-ttu-id="f8396-104">Schnittstellen ICoreWebView2CreateCoreWebView2HostCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f8396-104">interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f8396-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f8396-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="f8396-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f8396-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2HostCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f8396-107">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Host erstellte CoreWebView2Host zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f8396-107">The caller implements this interface to receive the CoreWebView2Host created via CreateCoreWebView2Host.</span></span>

## <span data-ttu-id="f8396-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f8396-108">Summary</span></span>

 <span data-ttu-id="f8396-109">Member</span><span class="sxs-lookup"><span data-stu-id="f8396-109">Members</span></span>                        | <span data-ttu-id="f8396-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f8396-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f8396-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="f8396-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f8396-112">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f8396-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f8396-113">Member</span><span class="sxs-lookup"><span data-stu-id="f8396-113">Members</span></span>

#### <span data-ttu-id="f8396-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f8396-114">Invoke</span></span> 

<span data-ttu-id="f8396-115">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f8396-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f8396-116">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span><span class="sxs-lookup"><span data-stu-id="f8396-116">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span></span>


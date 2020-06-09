---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e3618b7dc7b866031709ee276c80ba45ec89512d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698036"
---
# <span data-ttu-id="ac93f-104">Schnittstellen ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ac93f-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ac93f-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ac93f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ac93f-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ac93f-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ac93f-107">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der executeScript-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ac93f-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="ac93f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ac93f-108">Summary</span></span>

 <span data-ttu-id="ac93f-109">Member</span><span class="sxs-lookup"><span data-stu-id="ac93f-109">Members</span></span>                        | <span data-ttu-id="ac93f-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ac93f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ac93f-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="ac93f-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ac93f-112">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ac93f-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="ac93f-113">Member</span><span class="sxs-lookup"><span data-stu-id="ac93f-113">Members</span></span>

#### <span data-ttu-id="ac93f-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="ac93f-114">Invoke</span></span> 

<span data-ttu-id="ac93f-115">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ac93f-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ac93f-116">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="ac93f-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


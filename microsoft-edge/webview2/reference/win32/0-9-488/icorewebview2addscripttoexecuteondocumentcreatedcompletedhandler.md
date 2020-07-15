---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 336a4204a69c596a8423c32f3ef49cf7d12f51d4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880948"
---
# <span data-ttu-id="ec6bc-104">0.9.515-Interface-ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ec6bc-104">0.9.515 - interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ec6bc-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ec6bc-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ec6bc-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ec6bc-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ec6bc-107">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der AddScriptToExecuteOnDocumentCreated-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ec6bc-107">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="ec6bc-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ec6bc-108">Summary</span></span>

 <span data-ttu-id="ec6bc-109">Member</span><span class="sxs-lookup"><span data-stu-id="ec6bc-109">Members</span></span>                        | <span data-ttu-id="ec6bc-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ec6bc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ec6bc-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="ec6bc-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ec6bc-112">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ec6bc-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="ec6bc-113">Member</span><span class="sxs-lookup"><span data-stu-id="ec6bc-113">Members</span></span>

#### <span data-ttu-id="ec6bc-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="ec6bc-114">Invoke</span></span> 

<span data-ttu-id="ec6bc-115">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ec6bc-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ec6bc-116">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-ID)</span><span class="sxs-lookup"><span data-stu-id="ec6bc-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>


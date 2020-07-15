---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExecuteScriptCompletedHandler
ms.openlocfilehash: ee59ef42852fc8f0b0529b9a3ca08e53972dee1a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879940"
---
# <span data-ttu-id="82f50-104">Schnittstellen ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="82f50-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="82f50-105">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der executeScript-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="82f50-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="82f50-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="82f50-106">Summary</span></span>

 <span data-ttu-id="82f50-107">Member</span><span class="sxs-lookup"><span data-stu-id="82f50-107">Members</span></span>                        | <span data-ttu-id="82f50-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="82f50-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="82f50-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="82f50-109">Invoke</span></span>](#invoke) | <span data-ttu-id="82f50-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="82f50-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="82f50-111">Member</span><span class="sxs-lookup"><span data-stu-id="82f50-111">Members</span></span>

#### <span data-ttu-id="82f50-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="82f50-112">Invoke</span></span> 

<span data-ttu-id="82f50-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="82f50-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="82f50-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="82f50-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


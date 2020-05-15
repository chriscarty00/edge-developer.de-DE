---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 480b79cce673be530219718fb7f4920f5d1e80ae
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654042"
---
# <span data-ttu-id="86d40-104">Schnittstellen ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="86d40-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="86d40-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="86d40-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="86d40-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="86d40-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="86d40-107">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der executeScript-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="86d40-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="86d40-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="86d40-108">Summary</span></span>

 <span data-ttu-id="86d40-109">Member</span><span class="sxs-lookup"><span data-stu-id="86d40-109">Members</span></span>                        | <span data-ttu-id="86d40-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="86d40-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="86d40-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="86d40-111">Invoke</span></span>](#invoke) | <span data-ttu-id="86d40-112">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="86d40-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="86d40-113">Member</span><span class="sxs-lookup"><span data-stu-id="86d40-113">Members</span></span>

#### <span data-ttu-id="86d40-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="86d40-114">Invoke</span></span> 

<span data-ttu-id="86d40-115">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="86d40-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="86d40-116">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="86d40-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>


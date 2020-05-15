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
ms.openlocfilehash: da7b12d382776bb1755e90b0ce1c2728b555c8c8
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654020"
---
# <span data-ttu-id="9eca7-104">Schnittstellen ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="9eca7-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="9eca7-105">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der executeScript-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="9eca7-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="9eca7-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9eca7-106">Summary</span></span>

 <span data-ttu-id="9eca7-107">Member</span><span class="sxs-lookup"><span data-stu-id="9eca7-107">Members</span></span>                        | <span data-ttu-id="9eca7-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9eca7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9eca7-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9eca7-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9eca7-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9eca7-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="9eca7-111">Member</span><span class="sxs-lookup"><span data-stu-id="9eca7-111">Members</span></span>

#### <span data-ttu-id="9eca7-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9eca7-112">Invoke</span></span> 

<span data-ttu-id="9eca7-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9eca7-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="9eca7-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="9eca7-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


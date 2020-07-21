---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: da66c70724a6ce2c1102fcc2ef248963c11f0d1d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885303"
---
# <span data-ttu-id="a872a-104">0.9.515-Interface-ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a872a-104">0.9.515 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="a872a-105">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der executeScript-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="a872a-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="a872a-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a872a-106">Summary</span></span>

 <span data-ttu-id="a872a-107">Member</span><span class="sxs-lookup"><span data-stu-id="a872a-107">Members</span></span>                        | <span data-ttu-id="a872a-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a872a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a872a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a872a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a872a-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a872a-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="a872a-111">Member</span><span class="sxs-lookup"><span data-stu-id="a872a-111">Members</span></span>

#### <span data-ttu-id="a872a-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a872a-112">Invoke</span></span> 

<span data-ttu-id="a872a-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a872a-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="a872a-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="a872a-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


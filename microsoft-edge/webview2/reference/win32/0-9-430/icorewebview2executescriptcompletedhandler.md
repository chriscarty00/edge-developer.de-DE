---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 9a96e18b8c0b56cd75d4f0fe7b0c90c0634fe68b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884197"
---
# <span data-ttu-id="9d1b4-104">0.9.430-Interface-ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="9d1b4-104">0.9.430 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="9d1b4-105">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der executeScript-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="9d1b4-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9d1b4-106">Summary</span></span>

 <span data-ttu-id="9d1b4-107">Member</span><span class="sxs-lookup"><span data-stu-id="9d1b4-107">Members</span></span>                        | <span data-ttu-id="9d1b4-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9d1b4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9d1b4-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9d1b4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9d1b4-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="9d1b4-111">Member</span><span class="sxs-lookup"><span data-stu-id="9d1b4-111">Members</span></span>

#### <span data-ttu-id="9d1b4-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9d1b4-112">Invoke</span></span> 

<span data-ttu-id="9d1b4-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d1b4-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="9d1b4-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="9d1b4-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>


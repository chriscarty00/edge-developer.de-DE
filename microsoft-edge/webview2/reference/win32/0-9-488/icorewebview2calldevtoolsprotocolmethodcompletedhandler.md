---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 7a983d313e242cc163fb16a9c0d0068a9d6663d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883931"
---
# <span data-ttu-id="da81c-104">0.9.515-Interface-ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="da81c-104">0.9.515 - interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="da81c-105">Der Aufrufer implementiert diese Schnittstelle, um CallDevToolsProtocolMethod-Abschlussergebnisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="da81c-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="da81c-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="da81c-106">Summary</span></span>

 <span data-ttu-id="da81c-107">Member</span><span class="sxs-lookup"><span data-stu-id="da81c-107">Members</span></span>                        | <span data-ttu-id="da81c-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="da81c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="da81c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="da81c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="da81c-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="da81c-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="da81c-111">Member</span><span class="sxs-lookup"><span data-stu-id="da81c-111">Members</span></span>

#### <span data-ttu-id="da81c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="da81c-112">Invoke</span></span> 

<span data-ttu-id="da81c-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="da81c-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="da81c-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="da81c-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


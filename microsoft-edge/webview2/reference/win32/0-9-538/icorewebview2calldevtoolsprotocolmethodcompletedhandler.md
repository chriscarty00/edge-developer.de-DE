---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
ms.openlocfilehash: aed9cb6a748730e7bb7872b02e06233e97600e17
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010621"
---
# <span data-ttu-id="982b1-104">0.9.579-Interface-ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="982b1-104">0.9.579 - interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="982b1-105">Der Aufrufer implementiert diese Schnittstelle, um CallDevToolsProtocolMethod-Abschlussergebnisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="982b1-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="982b1-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="982b1-106">Summary</span></span>

 <span data-ttu-id="982b1-107">Member</span><span class="sxs-lookup"><span data-stu-id="982b1-107">Members</span></span>                        | <span data-ttu-id="982b1-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="982b1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="982b1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="982b1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="982b1-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="982b1-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="982b1-111">Member</span><span class="sxs-lookup"><span data-stu-id="982b1-111">Members</span></span>

#### <span data-ttu-id="982b1-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="982b1-112">Invoke</span></span> 

<span data-ttu-id="982b1-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="982b1-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="982b1-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="982b1-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


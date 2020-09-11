---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
ms.openlocfilehash: f6c0037177843d65ce5fe7cc56f206d5661d4b2a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012193"
---
# <span data-ttu-id="6e891-104">Schnittstellen ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="6e891-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6e891-105">Der Aufrufer implementiert diese Schnittstelle, um CallDevToolsProtocolMethod-Abschlussergebnisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6e891-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="6e891-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6e891-106">Summary</span></span>

 <span data-ttu-id="6e891-107">Member</span><span class="sxs-lookup"><span data-stu-id="6e891-107">Members</span></span>                        | <span data-ttu-id="6e891-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6e891-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6e891-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6e891-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6e891-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6e891-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="6e891-111">Member</span><span class="sxs-lookup"><span data-stu-id="6e891-111">Members</span></span>

#### <span data-ttu-id="6e891-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="6e891-112">Invoke</span></span> 

<span data-ttu-id="6e891-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6e891-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6e891-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="6e891-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


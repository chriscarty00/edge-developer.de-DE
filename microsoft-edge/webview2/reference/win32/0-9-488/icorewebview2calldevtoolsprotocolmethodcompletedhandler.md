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
ms.openlocfilehash: fda3ab31405a7d6353af1a670a2804e973577c8e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653918"
---
# <span data-ttu-id="b46d4-104">Schnittstellen ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b46d4-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b46d4-105">Der Aufrufer implementiert diese Schnittstelle, um CallDevToolsProtocolMethod-Abschlussergebnisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b46d4-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="b46d4-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b46d4-106">Summary</span></span>

 <span data-ttu-id="b46d4-107">Member</span><span class="sxs-lookup"><span data-stu-id="b46d4-107">Members</span></span>                        | <span data-ttu-id="b46d4-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b46d4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b46d4-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b46d4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b46d4-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b46d4-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b46d4-111">Member</span><span class="sxs-lookup"><span data-stu-id="b46d4-111">Members</span></span>

#### <span data-ttu-id="b46d4-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b46d4-112">Invoke</span></span> 

<span data-ttu-id="b46d4-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b46d4-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b46d4-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="b46d4-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>


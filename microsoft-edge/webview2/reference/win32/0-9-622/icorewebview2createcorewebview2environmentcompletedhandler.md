---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
ms.openlocfilehash: 3f6b6b9a2d4df2a450b4589c351c3ea98f7cc28f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012183"
---
# <span data-ttu-id="fc531-104">Schnittstellen ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="fc531-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="fc531-105">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Environment erstellte WebView2Environment zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="fc531-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="fc531-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fc531-106">Summary</span></span>

 <span data-ttu-id="fc531-107">Member</span><span class="sxs-lookup"><span data-stu-id="fc531-107">Members</span></span>                        | <span data-ttu-id="fc531-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="fc531-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fc531-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="fc531-109">Invoke</span></span>](#invoke) | <span data-ttu-id="fc531-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fc531-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="fc531-111">Member</span><span class="sxs-lookup"><span data-stu-id="fc531-111">Members</span></span>

#### <span data-ttu-id="fc531-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="fc531-112">Invoke</span></span> 

<span data-ttu-id="fc531-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fc531-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="fc531-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, [ICoreWebView2Environment](icorewebview2environment.md) \* createdEnvironment)</span><span class="sxs-lookup"><span data-stu-id="fc531-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, [ICoreWebView2Environment](icorewebview2environment.md) \* createdEnvironment)</span></span>


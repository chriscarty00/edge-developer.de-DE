---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 1082ea61b98b953277219d78a2944a2487b47a4d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884442"
---
# <span data-ttu-id="86384-104">0.9.515-Interface-ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="86384-104">0.9.515 - interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="86384-105">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Environment erstellte WebView2Environment zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="86384-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="86384-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="86384-106">Summary</span></span>

 <span data-ttu-id="86384-107">Member</span><span class="sxs-lookup"><span data-stu-id="86384-107">Members</span></span>                        | <span data-ttu-id="86384-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="86384-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="86384-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="86384-109">Invoke</span></span>](#invoke) | <span data-ttu-id="86384-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="86384-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="86384-111">Member</span><span class="sxs-lookup"><span data-stu-id="86384-111">Members</span></span>

#### <span data-ttu-id="86384-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="86384-112">Invoke</span></span> 

<span data-ttu-id="86384-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="86384-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="86384-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="86384-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>


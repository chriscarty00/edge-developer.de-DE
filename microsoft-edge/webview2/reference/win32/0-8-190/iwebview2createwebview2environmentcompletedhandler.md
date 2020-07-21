---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2CreateWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 9937fe08f440ce468f178e4ac17935bbb8a1a8ed
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886171"
---
# <span data-ttu-id="f3977-104">0.8.355-Interface-IWebView2CreateWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f3977-104">0.8.355 - interface IWebView2CreateWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CreateWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f3977-105">Der Aufrufer implementiert diese Schnittstelle, um die über CreateWebView2Environment erstellte WebView2Environment zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f3977-105">The caller implements this interface to receive the WebView2Environment created via CreateWebView2Environment.</span></span>

## <span data-ttu-id="f3977-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f3977-106">Summary</span></span>

 <span data-ttu-id="f3977-107">Member</span><span class="sxs-lookup"><span data-stu-id="f3977-107">Members</span></span>                        | <span data-ttu-id="f3977-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f3977-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f3977-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f3977-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f3977-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f3977-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f3977-111">Member</span><span class="sxs-lookup"><span data-stu-id="f3977-111">Members</span></span>

#### <span data-ttu-id="f3977-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f3977-112">Invoke</span></span> 

<span data-ttu-id="f3977-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f3977-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f3977-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span><span class="sxs-lookup"><span data-stu-id="f3977-114">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span></span>


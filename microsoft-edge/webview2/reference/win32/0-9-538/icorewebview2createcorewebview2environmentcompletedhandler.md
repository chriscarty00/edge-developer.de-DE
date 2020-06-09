---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: dbc1a3e05f9cdc5b5ced2e0b7d489b06392e6100
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698829"
---
# <span data-ttu-id="b85f3-104">Schnittstellen ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b85f3-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b85f3-105">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Environment erstellte WebView2Environment zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b85f3-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="b85f3-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b85f3-106">Summary</span></span>

 <span data-ttu-id="b85f3-107">Member</span><span class="sxs-lookup"><span data-stu-id="b85f3-107">Members</span></span>                        | <span data-ttu-id="b85f3-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b85f3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b85f3-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b85f3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b85f3-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b85f3-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b85f3-111">Member</span><span class="sxs-lookup"><span data-stu-id="b85f3-111">Members</span></span>

#### <span data-ttu-id="b85f3-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b85f3-112">Invoke</span></span> 

<span data-ttu-id="b85f3-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b85f3-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b85f3-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="b85f3-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>


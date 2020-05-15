---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: da49c1762ad7b7f3f366754bb9b05b7d16b861b7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653985"
---
# <span data-ttu-id="9990c-104">Schnittstellen ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="9990c-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="9990c-105">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Environment erstellte WebView2Environment zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="9990c-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="9990c-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9990c-106">Summary</span></span>

 <span data-ttu-id="9990c-107">Member</span><span class="sxs-lookup"><span data-stu-id="9990c-107">Members</span></span>                        | <span data-ttu-id="9990c-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9990c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9990c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9990c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9990c-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9990c-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="9990c-111">Member</span><span class="sxs-lookup"><span data-stu-id="9990c-111">Members</span></span>

#### <span data-ttu-id="9990c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9990c-112">Invoke</span></span> 

<span data-ttu-id="9990c-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9990c-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="9990c-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="9990c-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>


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
ms.openlocfilehash: 91c4e7885526def5de6fd1910a4a6f06c6a6953a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653804"
---
# <span data-ttu-id="bdf49-104">Schnittstellen ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="bdf49-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="bdf49-105">Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.488 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="bdf49-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="bdf49-106">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2CompositionController erstellte CoreWebView2Controller zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="bdf49-106">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="bdf49-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bdf49-107">Summary</span></span>

 <span data-ttu-id="bdf49-108">Member</span><span class="sxs-lookup"><span data-stu-id="bdf49-108">Members</span></span>                        | <span data-ttu-id="bdf49-109">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="bdf49-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bdf49-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="bdf49-110">Invoke</span></span>](#invoke) | <span data-ttu-id="bdf49-111">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bdf49-111">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="bdf49-112">Member</span><span class="sxs-lookup"><span data-stu-id="bdf49-112">Members</span></span>

#### <span data-ttu-id="bdf49-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="bdf49-113">Invoke</span></span> 

<span data-ttu-id="bdf49-114">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bdf49-114">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="bdf49-115">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="bdf49-115">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>


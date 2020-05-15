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
ms.openlocfilehash: 49b2baf825d65b97b4b1fa62d06b2f6d6b7bd26d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653989"
---
# <span data-ttu-id="b59c0-104">Schnittstellen ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b59c0-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b59c0-105">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Controller erstellte CoreWebView2Controller zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b59c0-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="b59c0-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b59c0-106">Summary</span></span>

 <span data-ttu-id="b59c0-107">Member</span><span class="sxs-lookup"><span data-stu-id="b59c0-107">Members</span></span>                        | <span data-ttu-id="b59c0-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b59c0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b59c0-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b59c0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b59c0-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b59c0-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b59c0-111">Member</span><span class="sxs-lookup"><span data-stu-id="b59c0-111">Members</span></span>

#### <span data-ttu-id="b59c0-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b59c0-112">Invoke</span></span> 

<span data-ttu-id="b59c0-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b59c0-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b59c0-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="b59c0-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>


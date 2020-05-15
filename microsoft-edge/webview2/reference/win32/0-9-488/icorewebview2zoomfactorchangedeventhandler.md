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
ms.openlocfilehash: e2469dd9a587735efcf88a48e0ce950cb4f85239
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654002"
---
# <span data-ttu-id="fab6f-104">Schnittstellen ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="fab6f-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="fab6f-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ZoomFactorChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="fab6f-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="fab6f-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fab6f-106">Summary</span></span>

 <span data-ttu-id="fab6f-107">Member</span><span class="sxs-lookup"><span data-stu-id="fab6f-107">Members</span></span>                        | <span data-ttu-id="fab6f-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="fab6f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fab6f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="fab6f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="fab6f-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fab6f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="fab6f-111">Verwenden Sie die ICoreWebView2Controller. ZoomFactor-Eigenschaft, um den geänderten Zoomfaktor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fab6f-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="fab6f-112">Member</span><span class="sxs-lookup"><span data-stu-id="fab6f-112">Members</span></span>

#### <span data-ttu-id="fab6f-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="fab6f-113">Invoke</span></span> 

<span data-ttu-id="fab6f-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fab6f-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fab6f-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="fab6f-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="fab6f-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="fab6f-116">There are no event args and the args parameter will be null.</span></span>


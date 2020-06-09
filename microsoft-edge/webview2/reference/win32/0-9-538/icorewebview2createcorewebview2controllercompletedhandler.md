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
ms.openlocfilehash: 45ac3cf4728f8b09f9ce65a30b53506fc2829c9d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698836"
---
# <span data-ttu-id="5e3d8-104">Schnittstellen ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="5e3d8-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="5e3d8-105">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Controller erstellte CoreWebView2Controller zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="5e3d8-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5e3d8-106">Summary</span></span>

 <span data-ttu-id="5e3d8-107">Member</span><span class="sxs-lookup"><span data-stu-id="5e3d8-107">Members</span></span>                        | <span data-ttu-id="5e3d8-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5e3d8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5e3d8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5e3d8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5e3d8-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="5e3d8-111">Member</span><span class="sxs-lookup"><span data-stu-id="5e3d8-111">Members</span></span>

#### <span data-ttu-id="5e3d8-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="5e3d8-112">Invoke</span></span> 

<span data-ttu-id="5e3d8-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="5e3d8-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="5e3d8-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>


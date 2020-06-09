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
ms.openlocfilehash: 290d82666e5b9c5062132e1eb7515e39e2deb978
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698844"
---
# <span data-ttu-id="52e10-104">Schnittstellen ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="52e10-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="52e10-105">Der Aufrufer implementiert diese Methode, um das Ergebnis der CapturePreview-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="52e10-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="52e10-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="52e10-106">Summary</span></span>

 <span data-ttu-id="52e10-107">Member</span><span class="sxs-lookup"><span data-stu-id="52e10-107">Members</span></span>                        | <span data-ttu-id="52e10-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="52e10-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="52e10-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="52e10-109">Invoke</span></span>](#invoke) | <span data-ttu-id="52e10-110">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="52e10-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="52e10-111">Das Ergebnis wird in den Stream geschrieben, der im CapturePreview-Methodenaufruf bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="52e10-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="52e10-112">Member</span><span class="sxs-lookup"><span data-stu-id="52e10-112">Members</span></span>

#### <span data-ttu-id="52e10-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="52e10-113">Invoke</span></span> 

<span data-ttu-id="52e10-114">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="52e10-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="52e10-115">Public HRESULT [Invoke](#invoke)(HRESULT-Ergebnis)</span><span class="sxs-lookup"><span data-stu-id="52e10-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


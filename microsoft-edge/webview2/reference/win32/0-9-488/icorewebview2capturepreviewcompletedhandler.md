---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 6aaac0d062d0e97d3ec0c87bec243c5cf682ad6f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697049"
---
# <span data-ttu-id="ef550-104">Schnittstellen ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ef550-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ef550-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ef550-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ef550-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ef550-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ef550-107">Der Aufrufer implementiert diese Methode, um das Ergebnis der CapturePreview-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ef550-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="ef550-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ef550-108">Summary</span></span>

 <span data-ttu-id="ef550-109">Member</span><span class="sxs-lookup"><span data-stu-id="ef550-109">Members</span></span>                        | <span data-ttu-id="ef550-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ef550-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ef550-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="ef550-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ef550-112">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ef550-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="ef550-113">Das Ergebnis wird in den Stream geschrieben, der im CapturePreview-Methodenaufruf bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ef550-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="ef550-114">Member</span><span class="sxs-lookup"><span data-stu-id="ef550-114">Members</span></span>

#### <span data-ttu-id="ef550-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="ef550-115">Invoke</span></span> 

<span data-ttu-id="ef550-116">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ef550-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ef550-117">Public HRESULT [Invoke](#invoke)(HRESULT-Ergebnis)</span><span class="sxs-lookup"><span data-stu-id="ef550-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8a9e3c1c5d2e9b7053d09518e3086f9e038e181a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883924"
---
# <span data-ttu-id="7e5e6-104">0.9.515-Interface-ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="7e5e6-104">0.9.515 - interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="7e5e6-105">Der Aufrufer implementiert diese Methode, um das Ergebnis der CapturePreview-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="7e5e6-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7e5e6-106">Summary</span></span>

 <span data-ttu-id="7e5e6-107">Member</span><span class="sxs-lookup"><span data-stu-id="7e5e6-107">Members</span></span>                        | <span data-ttu-id="7e5e6-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7e5e6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7e5e6-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7e5e6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7e5e6-110">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="7e5e6-111">Das Ergebnis wird in den Stream geschrieben, der im CapturePreview-Methodenaufruf bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="7e5e6-112">Member</span><span class="sxs-lookup"><span data-stu-id="7e5e6-112">Members</span></span>

#### <span data-ttu-id="7e5e6-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="7e5e6-113">Invoke</span></span> 

<span data-ttu-id="7e5e6-114">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="7e5e6-115">Public HRESULT [Invoke](#invoke)(HRESULT-Ergebnis)</span><span class="sxs-lookup"><span data-stu-id="7e5e6-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


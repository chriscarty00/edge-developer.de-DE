---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: 013a7076648b93bf259d28422f418365d988a586
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877440"
---
# <span data-ttu-id="07305-104">Schnittstellen ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="07305-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="07305-105">Der Aufrufer implementiert diese Methode, um das Ergebnis der CapturePreview-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="07305-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="07305-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="07305-106">Summary</span></span>

 <span data-ttu-id="07305-107">Member</span><span class="sxs-lookup"><span data-stu-id="07305-107">Members</span></span>                        | <span data-ttu-id="07305-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="07305-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="07305-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="07305-109">Invoke</span></span>](#invoke) | <span data-ttu-id="07305-110">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="07305-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="07305-111">Das Ergebnis wird in den Stream geschrieben, der im CapturePreview-Methodenaufruf bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="07305-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="07305-112">Member</span><span class="sxs-lookup"><span data-stu-id="07305-112">Members</span></span>

#### <span data-ttu-id="07305-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="07305-113">Invoke</span></span> 

<span data-ttu-id="07305-114">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="07305-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="07305-115">Public HRESULT [Invoke](#invoke)(HRESULT-Ergebnis)</span><span class="sxs-lookup"><span data-stu-id="07305-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


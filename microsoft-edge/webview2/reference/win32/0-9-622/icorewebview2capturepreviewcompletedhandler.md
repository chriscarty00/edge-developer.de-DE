---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: e526b723f111d7212a5da4b25840c89b69eb2e52
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012006"
---
# <span data-ttu-id="09db3-104">Schnittstellen ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="09db3-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="09db3-105">Der Aufrufer implementiert diese Methode, um das Ergebnis der CapturePreview-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="09db3-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="09db3-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="09db3-106">Summary</span></span>

 <span data-ttu-id="09db3-107">Member</span><span class="sxs-lookup"><span data-stu-id="09db3-107">Members</span></span>                        | <span data-ttu-id="09db3-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="09db3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="09db3-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="09db3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="09db3-110">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="09db3-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="09db3-111">Das Ergebnis wird in den Stream geschrieben, der im CapturePreview-Methodenaufruf bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="09db3-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="09db3-112">Member</span><span class="sxs-lookup"><span data-stu-id="09db3-112">Members</span></span>

#### <span data-ttu-id="09db3-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="09db3-113">Invoke</span></span> 

<span data-ttu-id="09db3-114">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="09db3-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="09db3-115">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode)</span><span class="sxs-lookup"><span data-stu-id="09db3-115">public HRESULT [Invoke](#invoke)(HRESULT errorCode)</span></span>


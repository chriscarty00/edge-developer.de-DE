---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: 96fff3ab67331bf5a8cf8323af5dddbca04f9e0e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010565"
---
# <span data-ttu-id="33cee-104">0.9.579-Interface-ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="33cee-104">0.9.579 - interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="33cee-105">Der Aufrufer implementiert diese Methode, um das Ergebnis der CapturePreview-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="33cee-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="33cee-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="33cee-106">Summary</span></span>

 <span data-ttu-id="33cee-107">Member</span><span class="sxs-lookup"><span data-stu-id="33cee-107">Members</span></span>                        | <span data-ttu-id="33cee-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="33cee-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="33cee-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="33cee-109">Invoke</span></span>](#invoke) | <span data-ttu-id="33cee-110">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="33cee-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="33cee-111">Das Ergebnis wird in den Stream geschrieben, der im CapturePreview-Methodenaufruf bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="33cee-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="33cee-112">Member</span><span class="sxs-lookup"><span data-stu-id="33cee-112">Members</span></span>

#### <span data-ttu-id="33cee-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="33cee-113">Invoke</span></span> 

<span data-ttu-id="33cee-114">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="33cee-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="33cee-115">Public HRESULT [Invoke](#invoke)(HRESULT-Ergebnis)</span><span class="sxs-lookup"><span data-stu-id="33cee-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


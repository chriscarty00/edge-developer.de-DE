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
ms.openlocfilehash: 793dbde462e25ae0bfe0dc0bc475cc49e7237fb2
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654006"
---
# <span data-ttu-id="8690f-104">Schnittstellen ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8690f-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="8690f-105">Der Aufrufer implementiert diese Methode, um das Ergebnis der CapturePreview-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="8690f-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="8690f-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8690f-106">Summary</span></span>

 <span data-ttu-id="8690f-107">Member</span><span class="sxs-lookup"><span data-stu-id="8690f-107">Members</span></span>                        | <span data-ttu-id="8690f-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8690f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8690f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="8690f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8690f-110">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8690f-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="8690f-111">Das Ergebnis wird in den Stream geschrieben, der im CapturePreview-Methodenaufruf bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8690f-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="8690f-112">Member</span><span class="sxs-lookup"><span data-stu-id="8690f-112">Members</span></span>

#### <span data-ttu-id="8690f-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="8690f-113">Invoke</span></span> 

<span data-ttu-id="8690f-114">Wird aufgerufen, um dem Implementierer den Abschlussstatus des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8690f-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="8690f-115">Public HRESULT [Invoke](#invoke)(HRESULT-Ergebnis)</span><span class="sxs-lookup"><span data-stu-id="8690f-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>


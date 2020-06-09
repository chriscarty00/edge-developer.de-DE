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
ms.openlocfilehash: a3dde4581692fb30cada16d9166bda62a0d69179
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698816"
---
# <span data-ttu-id="09021-104">Schnittstellen ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="09021-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="09021-105">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der executeScript-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="09021-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="09021-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="09021-106">Summary</span></span>

 <span data-ttu-id="09021-107">Member</span><span class="sxs-lookup"><span data-stu-id="09021-107">Members</span></span>                        | <span data-ttu-id="09021-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="09021-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="09021-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="09021-109">Invoke</span></span>](#invoke) | <span data-ttu-id="09021-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="09021-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="09021-111">Member</span><span class="sxs-lookup"><span data-stu-id="09021-111">Members</span></span>

#### <span data-ttu-id="09021-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="09021-112">Invoke</span></span> 

<span data-ttu-id="09021-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="09021-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="09021-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="09021-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


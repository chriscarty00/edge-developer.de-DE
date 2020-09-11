---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExecuteScriptCompletedHandler
ms.openlocfilehash: 4a3b5999d38f74fb6b78063e32b3abb0cb59c6b6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012071"
---
# <span data-ttu-id="f0c63-104">Schnittstellen ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f0c63-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f0c63-105">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der executeScript-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f0c63-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="f0c63-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f0c63-106">Summary</span></span>

 <span data-ttu-id="f0c63-107">Member</span><span class="sxs-lookup"><span data-stu-id="f0c63-107">Members</span></span>                        | <span data-ttu-id="f0c63-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f0c63-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f0c63-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f0c63-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f0c63-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f0c63-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f0c63-111">Member</span><span class="sxs-lookup"><span data-stu-id="f0c63-111">Members</span></span>

#### <span data-ttu-id="f0c63-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f0c63-112">Invoke</span></span> 

<span data-ttu-id="f0c63-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f0c63-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f0c63-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="f0c63-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>


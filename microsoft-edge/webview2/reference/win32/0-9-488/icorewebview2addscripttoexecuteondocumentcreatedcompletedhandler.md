---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 5a74464f841a0c8320bef7f81c83567d58f6caca
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884477"
---
# <span data-ttu-id="e829f-104">0.9.515-Interface-ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e829f-104">0.9.515 - interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e829f-105">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der AddScriptToExecuteOnDocumentCreated-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e829f-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="e829f-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e829f-106">Summary</span></span>

 <span data-ttu-id="e829f-107">Member</span><span class="sxs-lookup"><span data-stu-id="e829f-107">Members</span></span>                        | <span data-ttu-id="e829f-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e829f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e829f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e829f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e829f-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e829f-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e829f-111">Member</span><span class="sxs-lookup"><span data-stu-id="e829f-111">Members</span></span>

#### <span data-ttu-id="e829f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e829f-112">Invoke</span></span> 

<span data-ttu-id="e829f-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e829f-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e829f-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-ID)</span><span class="sxs-lookup"><span data-stu-id="e829f-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>


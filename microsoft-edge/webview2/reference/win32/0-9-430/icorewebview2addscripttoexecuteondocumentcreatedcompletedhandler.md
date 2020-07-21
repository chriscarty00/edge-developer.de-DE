---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 3c34c75e62fd73530d338e618469e071648f2fcb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884344"
---
# <span data-ttu-id="b898e-104">0.9.430-Interface-ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b898e-104">0.9.430 - interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b898e-105">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der AddScriptToExecuteOnDocumentCreated-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b898e-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="b898e-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b898e-106">Summary</span></span>

 <span data-ttu-id="b898e-107">Member</span><span class="sxs-lookup"><span data-stu-id="b898e-107">Members</span></span>                        | <span data-ttu-id="b898e-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b898e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b898e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b898e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b898e-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b898e-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b898e-111">Member</span><span class="sxs-lookup"><span data-stu-id="b898e-111">Members</span></span>

#### <span data-ttu-id="b898e-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b898e-112">Invoke</span></span> 

<span data-ttu-id="b898e-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b898e-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b898e-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-ID)</span><span class="sxs-lookup"><span data-stu-id="b898e-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR id)</span></span>


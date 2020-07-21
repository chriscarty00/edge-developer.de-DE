---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 464192c119ddb7dd59ee7cb5981f172eb44dbb78
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885016"
---
# <span data-ttu-id="a7b73-104">0.8.355-Interface-IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a7b73-104">0.8.355 - interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="a7b73-105">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der AddScriptToExecuteOnDocumentCreated-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="a7b73-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="a7b73-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a7b73-106">Summary</span></span>

 <span data-ttu-id="a7b73-107">Member</span><span class="sxs-lookup"><span data-stu-id="a7b73-107">Members</span></span>                        | <span data-ttu-id="a7b73-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a7b73-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a7b73-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a7b73-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a7b73-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a7b73-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="a7b73-111">Member</span><span class="sxs-lookup"><span data-stu-id="a7b73-111">Members</span></span>

#### <span data-ttu-id="a7b73-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a7b73-112">Invoke</span></span> 

<span data-ttu-id="a7b73-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a7b73-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="a7b73-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-ID)</span><span class="sxs-lookup"><span data-stu-id="a7b73-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR id)</span></span>


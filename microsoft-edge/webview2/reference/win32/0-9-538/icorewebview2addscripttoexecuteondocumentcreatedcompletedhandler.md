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
ms.openlocfilehash: 9777a27c1b9252d0d1a5f91a4692b9043fffc569
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698848"
---
# <span data-ttu-id="476a7-104">Schnittstellen ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="476a7-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="476a7-105">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der AddScriptToExecuteOnDocumentCreated-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="476a7-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="476a7-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="476a7-106">Summary</span></span>

 <span data-ttu-id="476a7-107">Member</span><span class="sxs-lookup"><span data-stu-id="476a7-107">Members</span></span>                        | <span data-ttu-id="476a7-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="476a7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="476a7-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="476a7-109">Invoke</span></span>](#invoke) | <span data-ttu-id="476a7-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="476a7-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="476a7-111">Member</span><span class="sxs-lookup"><span data-stu-id="476a7-111">Members</span></span>

#### <span data-ttu-id="476a7-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="476a7-112">Invoke</span></span> 

<span data-ttu-id="476a7-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="476a7-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="476a7-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-ID)</span><span class="sxs-lookup"><span data-stu-id="476a7-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>


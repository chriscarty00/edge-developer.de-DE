---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e9f98b43463fe5259d2f9f723b62b78c1d1a4758
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654008"
---
# <span data-ttu-id="9aa2d-104">Schnittstellen ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="9aa2d-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="9aa2d-105">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der AddScriptToExecuteOnDocumentCreated-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="9aa2d-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="9aa2d-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9aa2d-106">Summary</span></span>

 <span data-ttu-id="9aa2d-107">Member</span><span class="sxs-lookup"><span data-stu-id="9aa2d-107">Members</span></span>                        | <span data-ttu-id="9aa2d-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9aa2d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9aa2d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9aa2d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9aa2d-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9aa2d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="9aa2d-111">Member</span><span class="sxs-lookup"><span data-stu-id="9aa2d-111">Members</span></span>

#### <span data-ttu-id="9aa2d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9aa2d-112">Invoke</span></span> 

<span data-ttu-id="9aa2d-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9aa2d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="9aa2d-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-ID)</span><span class="sxs-lookup"><span data-stu-id="9aa2d-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>


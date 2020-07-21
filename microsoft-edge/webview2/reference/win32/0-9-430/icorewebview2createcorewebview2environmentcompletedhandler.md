---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 5cc3ca23dcababc35a73b44a81c54439d0dbe1a3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884309"
---
# <span data-ttu-id="7597c-104">0.9.430-Interface-ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="7597c-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="7597c-105">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Environment erstellte WebView2Environment zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="7597c-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="7597c-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7597c-106">Summary</span></span>

 <span data-ttu-id="7597c-107">Member</span><span class="sxs-lookup"><span data-stu-id="7597c-107">Members</span></span>                        | <span data-ttu-id="7597c-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7597c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7597c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7597c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7597c-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7597c-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="7597c-111">Member</span><span class="sxs-lookup"><span data-stu-id="7597c-111">Members</span></span>

#### <span data-ttu-id="7597c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="7597c-112">Invoke</span></span> 

<span data-ttu-id="7597c-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7597c-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="7597c-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="7597c-114">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span></span>


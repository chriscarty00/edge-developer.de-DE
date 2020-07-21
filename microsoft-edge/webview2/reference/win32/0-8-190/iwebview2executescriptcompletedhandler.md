---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 9a075cf5e5d3e5222e76b9ba7550636a67e5696a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886010"
---
# <span data-ttu-id="f1599-104">0.8.355-Interface-IWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f1599-104">0.8.355 - interface IWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f1599-105">Der Aufrufer implementiert diese Schnittstelle, um das Ergebnis der executeScript-Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f1599-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="f1599-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f1599-106">Summary</span></span>

 <span data-ttu-id="f1599-107">Member</span><span class="sxs-lookup"><span data-stu-id="f1599-107">Members</span></span>                        | <span data-ttu-id="f1599-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f1599-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f1599-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f1599-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f1599-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f1599-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f1599-111">Member</span><span class="sxs-lookup"><span data-stu-id="f1599-111">Members</span></span>

#### <span data-ttu-id="f1599-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f1599-112">Invoke</span></span> 

<span data-ttu-id="f1599-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f1599-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f1599-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-ErrorCode, LPCWSTR-resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="f1599-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>


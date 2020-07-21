---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2HostCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 9c2b5568e6a276b07dc91bd639c730b2009aa9e5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884281"
---
# <span data-ttu-id="ca17d-104">0.9.430-Interface-ICoreWebView2CreateCoreWebView2HostCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ca17d-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2HostCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ca17d-105">Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Host erstellte CoreWebView2Host zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ca17d-105">The caller implements this interface to receive the CoreWebView2Host created via CreateCoreWebView2Host.</span></span>

## <span data-ttu-id="ca17d-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ca17d-106">Summary</span></span>

 <span data-ttu-id="ca17d-107">Member</span><span class="sxs-lookup"><span data-stu-id="ca17d-107">Members</span></span>                        | <span data-ttu-id="ca17d-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ca17d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ca17d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ca17d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ca17d-110">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ca17d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="ca17d-111">Member</span><span class="sxs-lookup"><span data-stu-id="ca17d-111">Members</span></span>

#### <span data-ttu-id="ca17d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ca17d-112">Invoke</span></span> 

<span data-ttu-id="ca17d-113">Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ca17d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ca17d-114">öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span><span class="sxs-lookup"><span data-stu-id="ca17d-114">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span></span>


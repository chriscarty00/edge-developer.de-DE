---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: cf9d04c14f39a9ba1686d5cc9b002041313b645d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879912"
---
# <span data-ttu-id="2a376-104">Schnittstellen ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2a376-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="2a376-105">Der Aufrufer implementiert diese Schnittstelle, um das Ereignis "History" zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="2a376-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="2a376-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2a376-106">Summary</span></span>

 <span data-ttu-id="2a376-107">Member</span><span class="sxs-lookup"><span data-stu-id="2a376-107">Members</span></span>                        | <span data-ttu-id="2a376-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2a376-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2a376-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2a376-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2a376-110">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="2a376-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="2a376-111">Member</span><span class="sxs-lookup"><span data-stu-id="2a376-111">Members</span></span>

#### <span data-ttu-id="2a376-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="2a376-112">Invoke</span></span> 

<span data-ttu-id="2a376-113">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="2a376-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="2a376-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="2a376-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>


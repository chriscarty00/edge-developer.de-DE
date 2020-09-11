---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: 68cecdec63e64bde978156f17d6755a483abcc66
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011342"
---
# <span data-ttu-id="bbec8-104">0.9.579-Interface-ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="bbec8-104">0.9.579 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="bbec8-105">Der Aufrufer implementiert diese Schnittstelle, um das Ereignis "History" zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="bbec8-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="bbec8-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bbec8-106">Summary</span></span>

 <span data-ttu-id="bbec8-107">Member</span><span class="sxs-lookup"><span data-stu-id="bbec8-107">Members</span></span>                        | <span data-ttu-id="bbec8-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="bbec8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bbec8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="bbec8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="bbec8-110">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="bbec8-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="bbec8-111">Member</span><span class="sxs-lookup"><span data-stu-id="bbec8-111">Members</span></span>

#### <span data-ttu-id="bbec8-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="bbec8-112">Invoke</span></span> 

<span data-ttu-id="bbec8-113">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="bbec8-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="bbec8-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="bbec8-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>


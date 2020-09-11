---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: 909b055af0f9594bb3c85b215cb8e02f13606aa0
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012110"
---
# <span data-ttu-id="3e9bd-104">Schnittstellen ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3e9bd-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="3e9bd-105">Der Aufrufer implementiert diese Schnittstelle, um das Ereignis "History" zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="3e9bd-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3e9bd-106">Summary</span></span>

 <span data-ttu-id="3e9bd-107">Member</span><span class="sxs-lookup"><span data-stu-id="3e9bd-107">Members</span></span>                        | <span data-ttu-id="3e9bd-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3e9bd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3e9bd-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3e9bd-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3e9bd-110">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="3e9bd-111">Member</span><span class="sxs-lookup"><span data-stu-id="3e9bd-111">Members</span></span>

#### <span data-ttu-id="3e9bd-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="3e9bd-112">Invoke</span></span> 

<span data-ttu-id="3e9bd-113">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="3e9bd-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="3e9bd-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>


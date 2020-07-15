---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NavigationStartingEventHandler
ms.openlocfilehash: aca4e1090356b2dec147485f0290e1d19869ec63
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879751"
---
# <span data-ttu-id="a4e42-104">Schnittstellen ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="a4e42-104">interface ICoreWebView2NavigationStartingEventHandler</span></span> 

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="a4e42-105">Der Aufrufer implementiert diese Schnittstelle, um das NavigationStarting-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="a4e42-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="a4e42-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a4e42-106">Summary</span></span>

 <span data-ttu-id="a4e42-107">Member</span><span class="sxs-lookup"><span data-stu-id="a4e42-107">Members</span></span>                        | <span data-ttu-id="a4e42-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a4e42-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a4e42-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a4e42-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a4e42-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a4e42-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a4e42-111">Member</span><span class="sxs-lookup"><span data-stu-id="a4e42-111">Members</span></span>

#### <span data-ttu-id="a4e42-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a4e42-112">Invoke</span></span> 

<span data-ttu-id="a4e42-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a4e42-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a4e42-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a4e42-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span></span>


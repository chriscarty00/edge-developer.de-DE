---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ProcessFailedEventHandler
ms.openlocfilehash: 98f3f092bc1feb75ea2f94857c31dd80bcb907ee
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012137"
---
# <span data-ttu-id="e0ba3-104">Schnittstellen ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e0ba3-104">interface ICoreWebView2ProcessFailedEventHandler</span></span> 

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="e0ba3-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von ProcessFailed-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="e0ba3-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="e0ba3-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e0ba3-106">Summary</span></span>

 <span data-ttu-id="e0ba3-107">Member</span><span class="sxs-lookup"><span data-stu-id="e0ba3-107">Members</span></span>                        | <span data-ttu-id="e0ba3-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e0ba3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e0ba3-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e0ba3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e0ba3-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e0ba3-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e0ba3-111">Member</span><span class="sxs-lookup"><span data-stu-id="e0ba3-111">Members</span></span>

#### <span data-ttu-id="e0ba3-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e0ba3-112">Invoke</span></span> 

<span data-ttu-id="e0ba3-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e0ba3-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e0ba3-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e0ba3-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>


---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2WindowCloseRequestedEventHandler
ms.openlocfilehash: f5c1799225df5460029b3ad0c40db63a2e16113c
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012005"
---
# <span data-ttu-id="4747d-104">Schnittstellen ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4747d-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="4747d-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="4747d-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="4747d-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4747d-106">Summary</span></span>

 <span data-ttu-id="4747d-107">Member</span><span class="sxs-lookup"><span data-stu-id="4747d-107">Members</span></span>                        | <span data-ttu-id="4747d-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4747d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4747d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4747d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4747d-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4747d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="4747d-111">Member</span><span class="sxs-lookup"><span data-stu-id="4747d-111">Members</span></span>

#### <span data-ttu-id="4747d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="4747d-112">Invoke</span></span> 

<span data-ttu-id="4747d-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4747d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4747d-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="4747d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="4747d-115">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="4747d-115">There are no event args and the args parameter will be null.</span></span>


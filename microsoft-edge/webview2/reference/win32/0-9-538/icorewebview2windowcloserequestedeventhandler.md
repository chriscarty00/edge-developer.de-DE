---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2WindowCloseRequestedEventHandler
ms.openlocfilehash: fcfdb3b28f4f1d1e1d1159e6664cb898613d0601
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879961"
---
# <span data-ttu-id="97d6f-104">Schnittstellen ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="97d6f-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="97d6f-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="97d6f-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="97d6f-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="97d6f-106">Summary</span></span>

 <span data-ttu-id="97d6f-107">Member</span><span class="sxs-lookup"><span data-stu-id="97d6f-107">Members</span></span>                        | <span data-ttu-id="97d6f-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="97d6f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="97d6f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="97d6f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="97d6f-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="97d6f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="97d6f-111">Member</span><span class="sxs-lookup"><span data-stu-id="97d6f-111">Members</span></span>

#### <span data-ttu-id="97d6f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="97d6f-112">Invoke</span></span> 

<span data-ttu-id="97d6f-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="97d6f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="97d6f-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="97d6f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="97d6f-115">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="97d6f-115">There are no event args and the args parameter will be null.</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8bf8dcf40524425a7ef166c5007d60de738efb67
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698838"
---
# <span data-ttu-id="ef30a-104">Schnittstellen ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef30a-104">interface ICoreWebView2ContentLoadingEventHandler</span></span> 

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="ef30a-105">Der Aufrufer implementiert diese Schnittstelle, um das ContentLoading-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ef30a-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="ef30a-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ef30a-106">Summary</span></span>

 <span data-ttu-id="ef30a-107">Member</span><span class="sxs-lookup"><span data-stu-id="ef30a-107">Members</span></span>                        | <span data-ttu-id="ef30a-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ef30a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ef30a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ef30a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ef30a-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ef30a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ef30a-111">Member</span><span class="sxs-lookup"><span data-stu-id="ef30a-111">Members</span></span>

#### <span data-ttu-id="ef30a-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ef30a-112">Invoke</span></span> 

<span data-ttu-id="ef30a-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ef30a-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ef30a-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ef30a-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 889728489b6c4b06cd224915a0e12ee0a4144653
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653757"
---
# <span data-ttu-id="3f70b-104">Schnittstellen ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3f70b-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="3f70b-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="3f70b-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="3f70b-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3f70b-106">Summary</span></span>

 <span data-ttu-id="3f70b-107">Member</span><span class="sxs-lookup"><span data-stu-id="3f70b-107">Members</span></span>                        | <span data-ttu-id="3f70b-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3f70b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3f70b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3f70b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3f70b-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3f70b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3f70b-111">Member</span><span class="sxs-lookup"><span data-stu-id="3f70b-111">Members</span></span>

#### <span data-ttu-id="3f70b-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="3f70b-112">Invoke</span></span> 

<span data-ttu-id="3f70b-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3f70b-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3f70b-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="3f70b-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="3f70b-115">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="3f70b-115">There are no event args and the args parameter will be null.</span></span>


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
ms.openlocfilehash: 0d02fb1c8605bc6817085748154055cdfa489da8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698890"
---
# <span data-ttu-id="b28c9-104">Schnittstellen ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b28c9-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="b28c9-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="b28c9-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="b28c9-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b28c9-106">Summary</span></span>

 <span data-ttu-id="b28c9-107">Member</span><span class="sxs-lookup"><span data-stu-id="b28c9-107">Members</span></span>                        | <span data-ttu-id="b28c9-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b28c9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b28c9-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b28c9-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b28c9-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b28c9-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b28c9-111">Member</span><span class="sxs-lookup"><span data-stu-id="b28c9-111">Members</span></span>

#### <span data-ttu-id="b28c9-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b28c9-112">Invoke</span></span> 

<span data-ttu-id="b28c9-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b28c9-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b28c9-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b28c9-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="b28c9-115">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="b28c9-115">There are no event args and the args parameter will be null.</span></span>


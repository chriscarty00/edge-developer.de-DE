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
ms.openlocfilehash: 1d5c015e3ec7a3306c5ae93ed3668b42f5a47aa5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698861"
---
# <span data-ttu-id="fb68d-104">Schnittstellen ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="fb68d-104">interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="fb68d-105">Der Aufrufer implementiert diese Schnittstelle, um das WebMessageReceived-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="fb68d-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="fb68d-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fb68d-106">Summary</span></span>

 <span data-ttu-id="fb68d-107">Member</span><span class="sxs-lookup"><span data-stu-id="fb68d-107">Members</span></span>                        | <span data-ttu-id="fb68d-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="fb68d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fb68d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="fb68d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="fb68d-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fb68d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="fb68d-111">Member</span><span class="sxs-lookup"><span data-stu-id="fb68d-111">Members</span></span>

#### <span data-ttu-id="fb68d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="fb68d-112">Invoke</span></span> 

<span data-ttu-id="fb68d-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fb68d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fb68d-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="fb68d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>


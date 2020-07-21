---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: f566cb8aa876304d17e11bb47f24692aefda3b26
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883756"
---
# <span data-ttu-id="4ed92-104">0.9.430-Interface-ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4ed92-104">0.9.430 - interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="4ed92-105">Der Aufrufer implementiert diese Schnittstelle, um das WebMessageReceived-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="4ed92-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="4ed92-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4ed92-106">Summary</span></span>

 <span data-ttu-id="4ed92-107">Member</span><span class="sxs-lookup"><span data-stu-id="4ed92-107">Members</span></span>                        | <span data-ttu-id="4ed92-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4ed92-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4ed92-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4ed92-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4ed92-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4ed92-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="4ed92-111">Member</span><span class="sxs-lookup"><span data-stu-id="4ed92-111">Members</span></span>

#### <span data-ttu-id="4ed92-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="4ed92-112">Invoke</span></span> 

<span data-ttu-id="4ed92-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4ed92-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4ed92-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="4ed92-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>


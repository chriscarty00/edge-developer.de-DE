---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2WebMessageReceivedEventHandler
ms.openlocfilehash: 77af4fc8c3e05e46883e6d2428d9fa9015815f8b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010372"
---
# <span data-ttu-id="977ba-104">0.9.579-Interface-ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="977ba-104">0.9.579 - interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="977ba-105">Der Aufrufer implementiert diese Schnittstelle, um das WebMessageReceived-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="977ba-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="977ba-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="977ba-106">Summary</span></span>

 <span data-ttu-id="977ba-107">Member</span><span class="sxs-lookup"><span data-stu-id="977ba-107">Members</span></span>                        | <span data-ttu-id="977ba-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="977ba-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="977ba-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="977ba-109">Invoke</span></span>](#invoke) | <span data-ttu-id="977ba-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="977ba-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="977ba-111">Member</span><span class="sxs-lookup"><span data-stu-id="977ba-111">Members</span></span>

#### <span data-ttu-id="977ba-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="977ba-112">Invoke</span></span> 

<span data-ttu-id="977ba-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="977ba-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="977ba-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="977ba-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>


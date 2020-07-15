---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 6a1b472a4a37c31d4914794784767f8e0b9b6b94
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877777"
---
# <span data-ttu-id="f7cf3-104">0.9.430-Interface-ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f7cf3-104">0.9.430 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f7cf3-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f7cf3-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="f7cf3-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f7cf3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="f7cf3-107">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von mswebviewnewwindowrequested-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="f7cf3-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="f7cf3-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f7cf3-108">Summary</span></span>

 <span data-ttu-id="f7cf3-109">Member</span><span class="sxs-lookup"><span data-stu-id="f7cf3-109">Members</span></span>                        | <span data-ttu-id="f7cf3-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f7cf3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f7cf3-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="f7cf3-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f7cf3-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f7cf3-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f7cf3-113">Member</span><span class="sxs-lookup"><span data-stu-id="f7cf3-113">Members</span></span>

#### <span data-ttu-id="f7cf3-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f7cf3-114">Invoke</span></span> 

<span data-ttu-id="f7cf3-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f7cf3-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f7cf3-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f7cf3-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="f7cf3-117">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="f7cf3-117">There are no event args and the args parameter will be null.</span></span>


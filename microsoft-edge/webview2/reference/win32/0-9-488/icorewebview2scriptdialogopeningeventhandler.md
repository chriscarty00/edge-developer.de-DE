---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 86bb854bbce1a3cc842f656ffea3cf600136f38d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880311"
---
# <span data-ttu-id="654e3-104">0.9.515-Interface-ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="654e3-104">0.9.515 - interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="654e3-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="654e3-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="654e3-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="654e3-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="654e3-107">Der Aufrufer implementiert diese Schnittstelle, um das ScriptDialogOpening-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="654e3-107">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="654e3-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="654e3-108">Summary</span></span>

 <span data-ttu-id="654e3-109">Member</span><span class="sxs-lookup"><span data-stu-id="654e3-109">Members</span></span>                        | <span data-ttu-id="654e3-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="654e3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="654e3-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="654e3-111">Invoke</span></span>](#invoke) | <span data-ttu-id="654e3-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="654e3-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="654e3-113">Member</span><span class="sxs-lookup"><span data-stu-id="654e3-113">Members</span></span>

#### <span data-ttu-id="654e3-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="654e3-114">Invoke</span></span> 

<span data-ttu-id="654e3-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="654e3-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="654e3-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="654e3-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>


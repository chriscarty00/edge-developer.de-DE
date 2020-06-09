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
ms.openlocfilehash: d594e009a7a125866268ea62a0bc6d235c282b46
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698920"
---
# <span data-ttu-id="397c5-104">Schnittstellen ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="397c5-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="397c5-105">Der Aufrufer implementiert diese Schnittstelle, um das ScriptDialogOpening-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="397c5-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="397c5-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="397c5-106">Summary</span></span>

 <span data-ttu-id="397c5-107">Member</span><span class="sxs-lookup"><span data-stu-id="397c5-107">Members</span></span>                        | <span data-ttu-id="397c5-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="397c5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="397c5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="397c5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="397c5-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="397c5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="397c5-111">Member</span><span class="sxs-lookup"><span data-stu-id="397c5-111">Members</span></span>

#### <span data-ttu-id="397c5-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="397c5-112">Invoke</span></span> 

<span data-ttu-id="397c5-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="397c5-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="397c5-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="397c5-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>


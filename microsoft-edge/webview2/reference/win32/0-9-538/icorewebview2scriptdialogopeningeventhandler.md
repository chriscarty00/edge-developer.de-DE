---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ScriptDialogOpeningEventHandler
ms.openlocfilehash: f6cb9a893f6372bb412dcf17de36def71884bf53
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879170"
---
# <span data-ttu-id="0d348-104">Schnittstellen ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="0d348-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="0d348-105">Der Aufrufer implementiert diese Schnittstelle, um das ScriptDialogOpening-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="0d348-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="0d348-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0d348-106">Summary</span></span>

 <span data-ttu-id="0d348-107">Member</span><span class="sxs-lookup"><span data-stu-id="0d348-107">Members</span></span>                        | <span data-ttu-id="0d348-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="0d348-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0d348-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0d348-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0d348-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0d348-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="0d348-111">Member</span><span class="sxs-lookup"><span data-stu-id="0d348-111">Members</span></span>

#### <span data-ttu-id="0d348-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="0d348-112">Invoke</span></span> 

<span data-ttu-id="0d348-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0d348-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0d348-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="0d348-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>


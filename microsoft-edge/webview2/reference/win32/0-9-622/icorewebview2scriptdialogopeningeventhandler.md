---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ScriptDialogOpeningEventHandler
ms.openlocfilehash: 72d8f198e8a212dfd2088591453ea2885a1dbc0d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012130"
---
# <span data-ttu-id="5c1a9-104">Schnittstellen ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="5c1a9-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="5c1a9-105">Der Aufrufer implementiert diese Schnittstelle, um das ScriptDialogOpening-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="5c1a9-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="5c1a9-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5c1a9-106">Summary</span></span>

 <span data-ttu-id="5c1a9-107">Member</span><span class="sxs-lookup"><span data-stu-id="5c1a9-107">Members</span></span>                        | <span data-ttu-id="5c1a9-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5c1a9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5c1a9-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5c1a9-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5c1a9-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5c1a9-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="5c1a9-111">Member</span><span class="sxs-lookup"><span data-stu-id="5c1a9-111">Members</span></span>

#### <span data-ttu-id="5c1a9-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="5c1a9-112">Invoke</span></span> 

<span data-ttu-id="5c1a9-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5c1a9-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5c1a9-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="5c1a9-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>


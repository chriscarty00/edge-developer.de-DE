---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ScriptDialogOpeningEventHandler
ms.openlocfilehash: fea5ace11a4d1f1ecec9b13382184514d789a308
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010649"
---
# <span data-ttu-id="3d9ed-104">0.9.579-Interface-ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="3d9ed-104">0.9.579 - interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="3d9ed-105">Der Aufrufer implementiert diese Schnittstelle, um das ScriptDialogOpening-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="3d9ed-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="3d9ed-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3d9ed-106">Summary</span></span>

 <span data-ttu-id="3d9ed-107">Member</span><span class="sxs-lookup"><span data-stu-id="3d9ed-107">Members</span></span>                        | <span data-ttu-id="3d9ed-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3d9ed-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3d9ed-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3d9ed-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3d9ed-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3d9ed-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3d9ed-111">Member</span><span class="sxs-lookup"><span data-stu-id="3d9ed-111">Members</span></span>

#### <span data-ttu-id="3d9ed-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="3d9ed-112">Invoke</span></span> 

<span data-ttu-id="3d9ed-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3d9ed-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3d9ed-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3d9ed-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>


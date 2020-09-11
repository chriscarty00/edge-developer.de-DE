---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NavigationStartingEventHandler
ms.openlocfilehash: bec7596457800713eda5286c4ea1584bcfe9ed35
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011258"
---
# <span data-ttu-id="b787f-104">0.9.579-Interface-ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="b787f-104">0.9.579 - interface ICoreWebView2NavigationStartingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="b787f-105">Der Aufrufer implementiert diese Schnittstelle, um das NavigationStarting-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b787f-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="b787f-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b787f-106">Summary</span></span>

 <span data-ttu-id="b787f-107">Member</span><span class="sxs-lookup"><span data-stu-id="b787f-107">Members</span></span>                        | <span data-ttu-id="b787f-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b787f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b787f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b787f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b787f-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b787f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b787f-111">Member</span><span class="sxs-lookup"><span data-stu-id="b787f-111">Members</span></span>

#### <span data-ttu-id="b787f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b787f-112">Invoke</span></span> 

<span data-ttu-id="b787f-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b787f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b787f-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b787f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span></span>


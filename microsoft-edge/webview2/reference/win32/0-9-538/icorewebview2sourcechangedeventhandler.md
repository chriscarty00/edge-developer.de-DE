---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2SourceChangedEventHandler
ms.openlocfilehash: 9c5054c296657d851f0a88773d5eb96cba2af64a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010446"
---
# <span data-ttu-id="08405-104">0.9.579-Interface-ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="08405-104">0.9.579 - interface ICoreWebView2SourceChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="08405-105">Der Aufrufer implementiert diese Schnittstelle, um das Quellpfad-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="08405-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="08405-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="08405-106">Summary</span></span>

 <span data-ttu-id="08405-107">Member</span><span class="sxs-lookup"><span data-stu-id="08405-107">Members</span></span>                        | <span data-ttu-id="08405-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="08405-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="08405-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="08405-109">Invoke</span></span>](#invoke) | <span data-ttu-id="08405-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="08405-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="08405-111">Member</span><span class="sxs-lookup"><span data-stu-id="08405-111">Members</span></span>

#### <span data-ttu-id="08405-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="08405-112">Invoke</span></span> 

<span data-ttu-id="08405-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="08405-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="08405-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="08405-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>


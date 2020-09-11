---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2SourceChangedEventHandler
ms.openlocfilehash: 2c174d498843b7cc1d680d58eb36b5f53d652ad3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012135"
---
# <span data-ttu-id="c4b3c-104">Schnittstellen ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c4b3c-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="c4b3c-105">Der Aufrufer implementiert diese Schnittstelle, um das Quellpfad-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c4b3c-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="c4b3c-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c4b3c-106">Summary</span></span>

 <span data-ttu-id="c4b3c-107">Member</span><span class="sxs-lookup"><span data-stu-id="c4b3c-107">Members</span></span>                        | <span data-ttu-id="c4b3c-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c4b3c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c4b3c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c4b3c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c4b3c-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c4b3c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c4b3c-111">Member</span><span class="sxs-lookup"><span data-stu-id="c4b3c-111">Members</span></span>

#### <span data-ttu-id="c4b3c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c4b3c-112">Invoke</span></span> 

<span data-ttu-id="c4b3c-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c4b3c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c4b3c-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c4b3c-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>


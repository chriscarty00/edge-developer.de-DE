---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2SourceChangedEventHandler
ms.openlocfilehash: b856211b8a4b4088acc741d4d5626b49340124d1
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879331"
---
# <span data-ttu-id="538da-104">Schnittstellen ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="538da-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="538da-105">Der Aufrufer implementiert diese Schnittstelle, um das Quellpfad-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="538da-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="538da-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="538da-106">Summary</span></span>

 <span data-ttu-id="538da-107">Member</span><span class="sxs-lookup"><span data-stu-id="538da-107">Members</span></span>                        | <span data-ttu-id="538da-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="538da-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="538da-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="538da-109">Invoke</span></span>](#invoke) | <span data-ttu-id="538da-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="538da-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="538da-111">Member</span><span class="sxs-lookup"><span data-stu-id="538da-111">Members</span></span>

#### <span data-ttu-id="538da-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="538da-112">Invoke</span></span> 

<span data-ttu-id="538da-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="538da-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="538da-114">öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="538da-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 58e76c377d8d5709c006cb3a4da2e0edf73ec8fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884911"
---
# <span data-ttu-id="c18d3-104">0.8.355-Interface-IWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="c18d3-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="c18d3-105">Der Aufrufer implementiert diese Schnittstelle, um das ScriptDialogOpening-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c18d3-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="c18d3-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c18d3-106">Summary</span></span>

 <span data-ttu-id="c18d3-107">Member</span><span class="sxs-lookup"><span data-stu-id="c18d3-107">Members</span></span>                        | <span data-ttu-id="c18d3-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c18d3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c18d3-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c18d3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c18d3-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c18d3-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c18d3-111">Member</span><span class="sxs-lookup"><span data-stu-id="c18d3-111">Members</span></span>

#### <span data-ttu-id="c18d3-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c18d3-112">Invoke</span></span> 

<span data-ttu-id="c18d3-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c18d3-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c18d3-114">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c18d3-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>


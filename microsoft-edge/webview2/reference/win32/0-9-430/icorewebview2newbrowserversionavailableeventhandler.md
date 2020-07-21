---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 04859c0a22e8571a4fe8015a089c9b7d708c1dd3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884876"
---
# <span data-ttu-id="e5154-104">0.9.430-Interface-ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="e5154-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="e5154-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von NewBrowserVersionAvailable-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="e5154-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="e5154-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e5154-106">Summary</span></span>

 <span data-ttu-id="e5154-107">Member</span><span class="sxs-lookup"><span data-stu-id="e5154-107">Members</span></span>                        | <span data-ttu-id="e5154-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e5154-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e5154-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e5154-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e5154-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e5154-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e5154-111">Verwenden Sie die get_NewVersion-Methode von [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) , um die neue Versionsnummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e5154-111">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="e5154-112">Member</span><span class="sxs-lookup"><span data-stu-id="e5154-112">Members</span></span>

#### <span data-ttu-id="e5154-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="e5154-113">Invoke</span></span> 

<span data-ttu-id="e5154-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e5154-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e5154-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e5154-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>


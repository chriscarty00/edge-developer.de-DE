---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 42f63855c97363dab1a19cc784cf654afc40de74
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877847"
---
# <span data-ttu-id="2f57f-104">0.9.430-Interface-ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="2f57f-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="2f57f-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="2f57f-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="2f57f-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="2f57f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="2f57f-107">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von NewBrowserVersionAvailable-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="2f57f-107">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="2f57f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2f57f-108">Summary</span></span>

 <span data-ttu-id="2f57f-109">Member</span><span class="sxs-lookup"><span data-stu-id="2f57f-109">Members</span></span>                        | <span data-ttu-id="2f57f-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2f57f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2f57f-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="2f57f-111">Invoke</span></span>](#invoke) | <span data-ttu-id="2f57f-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2f57f-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="2f57f-113">Verwenden Sie die get_NewVersion-Methode von [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) , um die neue Versionsnummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2f57f-113">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="2f57f-114">Member</span><span class="sxs-lookup"><span data-stu-id="2f57f-114">Members</span></span>

#### <span data-ttu-id="2f57f-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="2f57f-115">Invoke</span></span> 

<span data-ttu-id="2f57f-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2f57f-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2f57f-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2f57f-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>


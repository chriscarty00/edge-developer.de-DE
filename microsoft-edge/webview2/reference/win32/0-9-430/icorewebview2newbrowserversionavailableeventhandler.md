---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b44724f8e18e11374f88ed2cd22711f06f59f12d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653951"
---
# <span data-ttu-id="488d3-104">Schnittstellen ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="488d3-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="488d3-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="488d3-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="488d3-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="488d3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="488d3-107">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von NewBrowserVersionAvailable-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="488d3-107">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="488d3-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="488d3-108">Summary</span></span>

 <span data-ttu-id="488d3-109">Member</span><span class="sxs-lookup"><span data-stu-id="488d3-109">Members</span></span>                        | <span data-ttu-id="488d3-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="488d3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="488d3-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="488d3-111">Invoke</span></span>](#invoke) | <span data-ttu-id="488d3-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="488d3-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="488d3-113">Verwenden Sie die get_NewVersion-Methode von [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) , um die neue Versionsnummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="488d3-113">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="488d3-114">Member</span><span class="sxs-lookup"><span data-stu-id="488d3-114">Members</span></span>

#### <span data-ttu-id="488d3-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="488d3-115">Invoke</span></span> 

<span data-ttu-id="488d3-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="488d3-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="488d3-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="488d3-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>


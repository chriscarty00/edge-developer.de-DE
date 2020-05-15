---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: a02a7ac3e31f959e80d5a3bdc41e39f653b9949c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654047"
---
# <span data-ttu-id="f8c18-104">Schnittstellen IWebView2NewVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8c18-104">interface IWebView2NewVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f8c18-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f8c18-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="f8c18-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f8c18-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="f8c18-107">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von NewVersionAvailable-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="f8c18-107">The caller implements this interface to receive NewVersionAvailable events.</span></span>

## <span data-ttu-id="f8c18-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f8c18-108">Summary</span></span>

 <span data-ttu-id="f8c18-109">Member</span><span class="sxs-lookup"><span data-stu-id="f8c18-109">Members</span></span>                        | <span data-ttu-id="f8c18-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f8c18-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f8c18-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="f8c18-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f8c18-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f8c18-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="f8c18-113">Verwenden Sie die get_NewVersion-Methode von [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) , um die neue Versionsnummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f8c18-113">Use the get_NewVersion method of [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="f8c18-114">Member</span><span class="sxs-lookup"><span data-stu-id="f8c18-114">Members</span></span>

#### <span data-ttu-id="f8c18-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="f8c18-115">Invoke</span></span> 

<span data-ttu-id="f8c18-116">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f8c18-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f8c18-117">Public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f8c18-117">public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span></span>


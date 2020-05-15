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
ms.openlocfilehash: 0314c796865d3d745b831d050498f59868e38e8f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654048"
---
# <span data-ttu-id="5bdaf-104">Schnittstellen IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="5bdaf-104">interface IWebView2NewVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="5bdaf-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="5bdaf-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="5bdaf-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="5bdaf-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="5bdaf-107">Ereignis-args für das NewVersionAvailable-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5bdaf-107">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="5bdaf-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5bdaf-108">Summary</span></span>

 <span data-ttu-id="5bdaf-109">Member</span><span class="sxs-lookup"><span data-stu-id="5bdaf-109">Members</span></span>                        | <span data-ttu-id="5bdaf-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5bdaf-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5bdaf-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="5bdaf-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="5bdaf-112">Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="5bdaf-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="5bdaf-113">Member</span><span class="sxs-lookup"><span data-stu-id="5bdaf-113">Members</span></span>

#### <span data-ttu-id="5bdaf-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="5bdaf-114">get_NewVersion</span></span> 

<span data-ttu-id="5bdaf-115">Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="5bdaf-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="5bdaf-116">Public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \*-Version)</span><span class="sxs-lookup"><span data-stu-id="5bdaf-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>


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
ms.openlocfilehash: 3ac37f7d90fc03214381b991c8becae602bac738
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653949"
---
# <span data-ttu-id="4dcc1-104">Schnittstellen ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="4dcc1-104">interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="4dcc1-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="4dcc1-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="4dcc1-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="4dcc1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="4dcc1-107">Ereignis-args für das NewBrowserVersionAvailable-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4dcc1-107">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="4dcc1-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4dcc1-108">Summary</span></span>

 <span data-ttu-id="4dcc1-109">Member</span><span class="sxs-lookup"><span data-stu-id="4dcc1-109">Members</span></span>                        | <span data-ttu-id="4dcc1-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4dcc1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4dcc1-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="4dcc1-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="4dcc1-112">Die Browser Versionsinformationen des aktuellen [ICoreWebView2Environment](ICoreWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="4dcc1-112">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="4dcc1-113">Member</span><span class="sxs-lookup"><span data-stu-id="4dcc1-113">Members</span></span>

#### <span data-ttu-id="4dcc1-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="4dcc1-114">get_NewVersion</span></span> 

<span data-ttu-id="4dcc1-115">Die Browser Versionsinformationen des aktuellen [ICoreWebView2Environment](ICoreWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="4dcc1-115">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="4dcc1-116">Public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \*-Version)</span><span class="sxs-lookup"><span data-stu-id="4dcc1-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>


---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: e8965ebe2e0434d83b4d6e8eabe74466adb7cec6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878344"
---
# <span data-ttu-id="2cf2d-104">0.8.355-Interface-IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="2cf2d-104">0.8.355 - interface IWebView2NewVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="2cf2d-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="2cf2d-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="2cf2d-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="2cf2d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="2cf2d-107">Ereignis-args für das NewVersionAvailable-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="2cf2d-107">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="2cf2d-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2cf2d-108">Summary</span></span>

 <span data-ttu-id="2cf2d-109">Member</span><span class="sxs-lookup"><span data-stu-id="2cf2d-109">Members</span></span>                        | <span data-ttu-id="2cf2d-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2cf2d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2cf2d-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="2cf2d-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="2cf2d-112">Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="2cf2d-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="2cf2d-113">Member</span><span class="sxs-lookup"><span data-stu-id="2cf2d-113">Members</span></span>

#### <span data-ttu-id="2cf2d-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="2cf2d-114">get_NewVersion</span></span> 

<span data-ttu-id="2cf2d-115">Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="2cf2d-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="2cf2d-116">Public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \*-Version)</span><span class="sxs-lookup"><span data-stu-id="2cf2d-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>


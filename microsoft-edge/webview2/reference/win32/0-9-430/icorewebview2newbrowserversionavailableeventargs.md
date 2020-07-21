---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 9f56ba33534c76cb1bd60c01a88eedfced45f1fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884862"
---
# <span data-ttu-id="d43f5-104">0.9.430-Interface-ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="d43f5-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="d43f5-105">Ereignis-args für das NewBrowserVersionAvailable-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d43f5-105">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="d43f5-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d43f5-106">Summary</span></span>

 <span data-ttu-id="d43f5-107">Member</span><span class="sxs-lookup"><span data-stu-id="d43f5-107">Members</span></span>                        | <span data-ttu-id="d43f5-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d43f5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d43f5-109">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="d43f5-109">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="d43f5-110">Die Browser Versionsinformationen des aktuellen [ICoreWebView2Environment](ICoreWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="d43f5-110">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="d43f5-111">Member</span><span class="sxs-lookup"><span data-stu-id="d43f5-111">Members</span></span>

#### <span data-ttu-id="d43f5-112">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="d43f5-112">get_NewVersion</span></span> 

<span data-ttu-id="d43f5-113">Die Browser Versionsinformationen des aktuellen [ICoreWebView2Environment](ICoreWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="d43f5-113">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="d43f5-114">Public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \*-Version)</span><span class="sxs-lookup"><span data-stu-id="d43f5-114">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>


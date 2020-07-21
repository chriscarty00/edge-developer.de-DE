---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 4271cc1002de70db2803a5bd6d4be73748bf5bbb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885870"
---
# <span data-ttu-id="70972-104">0.8.355-Interface-IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="70972-104">0.8.355 - interface IWebView2NewVersionAvailableEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="70972-105">Ereignis-args für das NewVersionAvailable-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="70972-105">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="70972-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="70972-106">Summary</span></span>

 <span data-ttu-id="70972-107">Member</span><span class="sxs-lookup"><span data-stu-id="70972-107">Members</span></span>                        | <span data-ttu-id="70972-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="70972-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="70972-109">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="70972-109">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="70972-110">Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="70972-110">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="70972-111">Member</span><span class="sxs-lookup"><span data-stu-id="70972-111">Members</span></span>

#### <span data-ttu-id="70972-112">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="70972-112">get_NewVersion</span></span> 

<span data-ttu-id="70972-113">Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="70972-113">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="70972-114">Public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \*-Version)</span><span class="sxs-lookup"><span data-stu-id="70972-114">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>


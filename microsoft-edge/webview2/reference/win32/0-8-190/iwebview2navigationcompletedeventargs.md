---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: b496c37949e934fadf0af736059566edcab9f5c3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885933"
---
# <span data-ttu-id="5cfbf-104">0.8.355-Interface-IWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5cfbf-104">0.8.355 - interface IWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="5cfbf-105">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="5cfbf-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5cfbf-106">Summary</span></span>

 <span data-ttu-id="5cfbf-107">Member</span><span class="sxs-lookup"><span data-stu-id="5cfbf-107">Members</span></span>                        | <span data-ttu-id="5cfbf-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5cfbf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5cfbf-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="5cfbf-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="5cfbf-110">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="5cfbf-111">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="5cfbf-111">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="5cfbf-112">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-112">The error code if the navigation failed.</span></span>

## <span data-ttu-id="5cfbf-113">Member</span><span class="sxs-lookup"><span data-stu-id="5cfbf-113">Members</span></span>

#### <span data-ttu-id="5cfbf-114">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="5cfbf-114">get_IsSuccess</span></span> 

<span data-ttu-id="5cfbf-115">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-115">True when the navigation is successful.</span></span>

> <span data-ttu-id="5cfbf-116">öffentliche HRESULT- [get_IsSuccess](#get_issuccess)(bool \* issuccess)</span><span class="sxs-lookup"><span data-stu-id="5cfbf-116">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="5cfbf-117">Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-117">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="5cfbf-118">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="5cfbf-118">get_WebErrorStatus</span></span> 

<span data-ttu-id="5cfbf-119">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-119">The error code if the navigation failed.</span></span>

> <span data-ttu-id="5cfbf-120">öffentliche HRESULT- [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="5cfbf-120">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span></span>


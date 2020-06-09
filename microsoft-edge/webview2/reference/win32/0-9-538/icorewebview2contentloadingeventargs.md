---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8acec97ec6060cd53adc3821f6a51db2048935fb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698845"
---
# <span data-ttu-id="f5484-104">Schnittstellen ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="f5484-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="f5484-105">Ereignis-args für das ContentLoading-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f5484-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="f5484-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f5484-106">Summary</span></span>

 <span data-ttu-id="f5484-107">Member</span><span class="sxs-lookup"><span data-stu-id="f5484-107">Members</span></span>                        | <span data-ttu-id="f5484-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f5484-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f5484-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="f5484-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="f5484-110">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="f5484-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="f5484-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="f5484-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="f5484-112">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="f5484-112">The ID of the navigation.</span></span>

## <span data-ttu-id="f5484-113">Member</span><span class="sxs-lookup"><span data-stu-id="f5484-113">Members</span></span>

#### <span data-ttu-id="f5484-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="f5484-114">get_IsErrorPage</span></span> 

<span data-ttu-id="f5484-115">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="f5484-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="f5484-116">Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="f5484-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="f5484-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="f5484-117">get_NavigationId</span></span> 

<span data-ttu-id="f5484-118">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="f5484-118">The ID of the navigation.</span></span>

> <span data-ttu-id="f5484-119">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="f5484-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


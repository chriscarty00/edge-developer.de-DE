---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c6bb99078b5574ba89c0d66b49e2c63cd6888d28
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653992"
---
# <span data-ttu-id="1b3d7-104">Schnittstellen ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="1b3d7-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="1b3d7-105">Ereignis-args für das ContentLoading-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1b3d7-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="1b3d7-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1b3d7-106">Summary</span></span>

 <span data-ttu-id="1b3d7-107">Member</span><span class="sxs-lookup"><span data-stu-id="1b3d7-107">Members</span></span>                        | <span data-ttu-id="1b3d7-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1b3d7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1b3d7-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="1b3d7-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="1b3d7-110">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="1b3d7-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="1b3d7-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="1b3d7-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="1b3d7-112">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="1b3d7-112">The ID of the navigation.</span></span>

## <span data-ttu-id="1b3d7-113">Member</span><span class="sxs-lookup"><span data-stu-id="1b3d7-113">Members</span></span>

#### <span data-ttu-id="1b3d7-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="1b3d7-114">get_IsErrorPage</span></span> 

<span data-ttu-id="1b3d7-115">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="1b3d7-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="1b3d7-116">Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="1b3d7-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="1b3d7-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="1b3d7-117">get_NavigationId</span></span> 

<span data-ttu-id="1b3d7-118">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="1b3d7-118">The ID of the navigation.</span></span>

> <span data-ttu-id="1b3d7-119">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="1b3d7-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


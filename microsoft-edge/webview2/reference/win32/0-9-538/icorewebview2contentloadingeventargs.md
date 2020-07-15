---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ContentLoadingEventArgs
ms.openlocfilehash: 571aae9e1e00938c9bf0f3fb872fccf340269105
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877455"
---
# <span data-ttu-id="7ba43-104">Schnittstellen ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="7ba43-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="7ba43-105">Ereignis-args für das ContentLoading-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7ba43-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="7ba43-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7ba43-106">Summary</span></span>

 <span data-ttu-id="7ba43-107">Member</span><span class="sxs-lookup"><span data-stu-id="7ba43-107">Members</span></span>                        | <span data-ttu-id="7ba43-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="7ba43-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7ba43-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="7ba43-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="7ba43-110">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="7ba43-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="7ba43-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7ba43-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="7ba43-112">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="7ba43-112">The ID of the navigation.</span></span>

## <span data-ttu-id="7ba43-113">Member</span><span class="sxs-lookup"><span data-stu-id="7ba43-113">Members</span></span>

#### <span data-ttu-id="7ba43-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="7ba43-114">get_IsErrorPage</span></span> 

<span data-ttu-id="7ba43-115">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="7ba43-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="7ba43-116">Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="7ba43-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="7ba43-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7ba43-117">get_NavigationId</span></span> 

<span data-ttu-id="7ba43-118">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="7ba43-118">The ID of the navigation.</span></span>

> <span data-ttu-id="7ba43-119">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="7ba43-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


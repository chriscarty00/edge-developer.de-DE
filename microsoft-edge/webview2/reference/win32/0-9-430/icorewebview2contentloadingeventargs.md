---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 95fa97268fb5695aebf5c1414752cf12cf1da57b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881144"
---
# <span data-ttu-id="17776-104">0.9.430-Interface-ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="17776-104">0.9.430 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="17776-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="17776-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="17776-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="17776-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="17776-107">Ereignis-args für das ContentLoading-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="17776-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="17776-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="17776-108">Summary</span></span>

 <span data-ttu-id="17776-109">Member</span><span class="sxs-lookup"><span data-stu-id="17776-109">Members</span></span>                        | <span data-ttu-id="17776-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="17776-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="17776-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="17776-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="17776-112">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="17776-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="17776-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="17776-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="17776-114">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="17776-114">The ID of the navigation.</span></span>

## <span data-ttu-id="17776-115">Member</span><span class="sxs-lookup"><span data-stu-id="17776-115">Members</span></span>

#### <span data-ttu-id="17776-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="17776-116">get_IsErrorPage</span></span> 

<span data-ttu-id="17776-117">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="17776-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="17776-118">Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="17776-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="17776-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="17776-119">get_NavigationId</span></span> 

<span data-ttu-id="17776-120">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="17776-120">The ID of the navigation.</span></span>

> <span data-ttu-id="17776-121">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="17776-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


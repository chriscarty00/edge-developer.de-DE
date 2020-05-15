---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: c3ba6ac3a2478861abb7b26e726a9cbd606b0eb9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653883"
---
# <span data-ttu-id="c06ec-104">Schnittstellen ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="c06ec-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c06ec-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="c06ec-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="c06ec-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="c06ec-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="c06ec-107">Ereignis-args für das ContentLoading-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c06ec-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="c06ec-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c06ec-108">Summary</span></span>

 <span data-ttu-id="c06ec-109">Member</span><span class="sxs-lookup"><span data-stu-id="c06ec-109">Members</span></span>                        | <span data-ttu-id="c06ec-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c06ec-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c06ec-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="c06ec-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="c06ec-112">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="c06ec-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="c06ec-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="c06ec-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="c06ec-114">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="c06ec-114">The ID of the navigation.</span></span>

## <span data-ttu-id="c06ec-115">Member</span><span class="sxs-lookup"><span data-stu-id="c06ec-115">Members</span></span>

#### <span data-ttu-id="c06ec-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="c06ec-116">get_IsErrorPage</span></span> 

<span data-ttu-id="c06ec-117">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="c06ec-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="c06ec-118">Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="c06ec-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="c06ec-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="c06ec-119">get_NavigationId</span></span> 

<span data-ttu-id="c06ec-120">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="c06ec-120">The ID of the navigation.</span></span>

> <span data-ttu-id="c06ec-121">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="c06ec-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


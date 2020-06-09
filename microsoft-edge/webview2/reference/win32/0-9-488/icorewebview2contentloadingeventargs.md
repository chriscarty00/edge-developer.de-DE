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
ms.openlocfilehash: c720b700257554891f13477f5f3508e331ac6b25
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698204"
---
# <span data-ttu-id="d4596-104">Schnittstellen ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="d4596-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="d4596-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="d4596-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="d4596-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="d4596-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="d4596-107">Ereignis-args für das ContentLoading-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d4596-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="d4596-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d4596-108">Summary</span></span>

 <span data-ttu-id="d4596-109">Member</span><span class="sxs-lookup"><span data-stu-id="d4596-109">Members</span></span>                        | <span data-ttu-id="d4596-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d4596-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d4596-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="d4596-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="d4596-112">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="d4596-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="d4596-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="d4596-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="d4596-114">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="d4596-114">The ID of the navigation.</span></span>

## <span data-ttu-id="d4596-115">Member</span><span class="sxs-lookup"><span data-stu-id="d4596-115">Members</span></span>

#### <span data-ttu-id="d4596-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="d4596-116">get_IsErrorPage</span></span> 

<span data-ttu-id="d4596-117">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="d4596-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="d4596-118">Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="d4596-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="d4596-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="d4596-119">get_NavigationId</span></span> 

<span data-ttu-id="d4596-120">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="d4596-120">The ID of the navigation.</span></span>

> <span data-ttu-id="d4596-121">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="d4596-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


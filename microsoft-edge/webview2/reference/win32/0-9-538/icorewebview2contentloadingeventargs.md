---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ContentLoadingEventArgs
ms.openlocfilehash: d70673714e3641e19f5c3d6367278c0c7bd2729b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010299"
---
# <span data-ttu-id="e24c4-104">0.9.579-Interface-ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="e24c4-104">0.9.579 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="e24c4-105">Ereignis-args für das ContentLoading-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e24c4-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="e24c4-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e24c4-106">Summary</span></span>

 <span data-ttu-id="e24c4-107">Member</span><span class="sxs-lookup"><span data-stu-id="e24c4-107">Members</span></span>                        | <span data-ttu-id="e24c4-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e24c4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e24c4-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="e24c4-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="e24c4-110">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="e24c4-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="e24c4-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="e24c4-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="e24c4-112">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="e24c4-112">The ID of the navigation.</span></span>

## <span data-ttu-id="e24c4-113">Member</span><span class="sxs-lookup"><span data-stu-id="e24c4-113">Members</span></span>

#### <span data-ttu-id="e24c4-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="e24c4-114">get_IsErrorPage</span></span> 

<span data-ttu-id="e24c4-115">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="e24c4-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="e24c4-116">Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="e24c4-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="e24c4-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="e24c4-117">get_NavigationId</span></span> 

<span data-ttu-id="e24c4-118">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="e24c4-118">The ID of the navigation.</span></span>

> <span data-ttu-id="e24c4-119">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="e24c4-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


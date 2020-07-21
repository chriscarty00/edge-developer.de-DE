---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 32b0f46b00195a265238541f8715ec21ca3757a1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883875"
---
# <span data-ttu-id="3aeba-104">0.9.515-Interface-ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="3aeba-104">0.9.515 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="3aeba-105">Ereignis-args für das ContentLoading-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="3aeba-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="3aeba-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3aeba-106">Summary</span></span>

 <span data-ttu-id="3aeba-107">Member</span><span class="sxs-lookup"><span data-stu-id="3aeba-107">Members</span></span>                        | <span data-ttu-id="3aeba-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3aeba-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3aeba-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="3aeba-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="3aeba-110">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="3aeba-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="3aeba-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="3aeba-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="3aeba-112">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="3aeba-112">The ID of the navigation.</span></span>

## <span data-ttu-id="3aeba-113">Member</span><span class="sxs-lookup"><span data-stu-id="3aeba-113">Members</span></span>

#### <span data-ttu-id="3aeba-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="3aeba-114">get_IsErrorPage</span></span> 

<span data-ttu-id="3aeba-115">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="3aeba-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="3aeba-116">Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="3aeba-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="3aeba-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="3aeba-117">get_NavigationId</span></span> 

<span data-ttu-id="3aeba-118">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="3aeba-118">The ID of the navigation.</span></span>

> <span data-ttu-id="3aeba-119">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="3aeba-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


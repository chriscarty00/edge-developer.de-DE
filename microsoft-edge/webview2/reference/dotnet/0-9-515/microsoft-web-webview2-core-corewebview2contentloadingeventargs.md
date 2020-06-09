---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: abe167548b7e604bd60c792660ea5b52dec9b848
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697301"
---
# <span data-ttu-id="95fad-104">Microsoft. Web. WebView2. Core. CoreWebView2ContentLoadingEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="95fad-104">Microsoft.Web.WebView2.Core.CoreWebView2ContentLoadingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="95fad-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="95fad-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="95fad-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="95fad-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="95fad-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="95fad-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="95fad-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="95fad-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="95fad-109">Ereignis-args für das ContentLoading-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="95fad-109">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="95fad-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="95fad-110">Summary</span></span>

 <span data-ttu-id="95fad-111">Member</span><span class="sxs-lookup"><span data-stu-id="95fad-111">Members</span></span>                        | <span data-ttu-id="95fad-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="95fad-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95fad-113">IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="95fad-113">IsErrorPage</span></span>](#iserrorpage) | <span data-ttu-id="95fad-114">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="95fad-114">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="95fad-115">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="95fad-115">NavigationId</span></span>](#navigationid) | <span data-ttu-id="95fad-116">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="95fad-116">The ID of the navigation.</span></span>

## <span data-ttu-id="95fad-117">Member</span><span class="sxs-lookup"><span data-stu-id="95fad-117">Members</span></span>

#### <span data-ttu-id="95fad-118">IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="95fad-118">IsErrorPage</span></span> 

<span data-ttu-id="95fad-119">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="95fad-119">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="95fad-120">public bool [IsErrorPage](#iserrorpage)</span><span class="sxs-lookup"><span data-stu-id="95fad-120">public bool [IsErrorPage](#iserrorpage)</span></span>

#### <span data-ttu-id="95fad-121">Navigations-Nr</span><span class="sxs-lookup"><span data-stu-id="95fad-121">NavigationId</span></span> 

<span data-ttu-id="95fad-122">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="95fad-122">The ID of the navigation.</span></span>

> <span data-ttu-id="95fad-123">öffentliche ULONG- [Navigations](#navigationid) -Nr</span><span class="sxs-lookup"><span data-stu-id="95fad-123">public ulong [NavigationId](#navigationid)</span></span>


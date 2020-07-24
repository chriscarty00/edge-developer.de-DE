---
description: Navigation
title: Navigation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 0df8e12acb11824006515ac711250d776d276e36
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895578"
---
# <span data-ttu-id="37a5b-104">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="37a5b-104">Navigation events</span></span>  

<span data-ttu-id="37a5b-105">Die normale Abfolge von Navigations Ereignissen ist,,, `NavigationStarting` `SourceChanged` `ContentLoading` `HistoryChanged` und dann `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="37a5b-105">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="37a5b-106">Die folgenden Ereignisse beschreiben den Zustand von WebView2 während jeder Navigation.</span><span class="sxs-lookup"><span data-stu-id="37a5b-106">The following events describe the state of WebView2 during each navigation.</span></span>  

| <span data-ttu-id="37a5b-107">Sequenz</span><span class="sxs-lookup"><span data-stu-id="37a5b-107">Sequence</span></span> | <span data-ttu-id="37a5b-108">Ereignisname</span><span class="sxs-lookup"><span data-stu-id="37a5b-108">Event name</span></span> | <span data-ttu-id="37a5b-109">Details</span><span class="sxs-lookup"><span data-stu-id="37a5b-109">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="37a5b-110">1</span><span class="sxs-lookup"><span data-stu-id="37a5b-110">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="37a5b-111">WebView2 beginnt zu navigieren, und die Navigation führt zu einer Netzwerkanforderung.</span><span class="sxs-lookup"><span data-stu-id="37a5b-111">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="37a5b-112">Der Host kann die Anforderung während des Ereignisses nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="37a5b-112">The host is able to disallow the request during the event.</span></span>  |  
| <span data-ttu-id="37a5b-113">2</span><span class="sxs-lookup"><span data-stu-id="37a5b-113">2</span></span> | `SourceChanged`  |  <span data-ttu-id="37a5b-114">Die Quelle von WebView2 Änderungen an einer neuen URL.</span><span class="sxs-lookup"><span data-stu-id="37a5b-114">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="37a5b-115">Das Ereignis kann durch eine Navigation entstehen, die keine Netzwerkanforderung wie eine Fragment-Navigation verursacht.</span><span class="sxs-lookup"><span data-stu-id="37a5b-115">The event may result from a navigation that does not cause a network request such as a fragment navigation.</span></span>  |  
| <span data-ttu-id="37a5b-116">3</span><span class="sxs-lookup"><span data-stu-id="37a5b-116">3</span></span> | `HistoryChanged`  |  <span data-ttu-id="37a5b-117">Das Protokoll der WebView2-Updates als Ergebnis der Navigation.</span><span class="sxs-lookup"><span data-stu-id="37a5b-117">The history of WebView2 updates as a result of the navigation.</span></span>  |  
| <span data-ttu-id="37a5b-118">4</span><span class="sxs-lookup"><span data-stu-id="37a5b-118">4</span></span> | `ContentLoading`  |  <span data-ttu-id="37a5b-119">WebView startet das Laden von Inhalten für die neue Seite.</span><span class="sxs-lookup"><span data-stu-id="37a5b-119">WebView starts loading content for the new page.</span></span>  |  
| <span data-ttu-id="37a5b-120">5</span><span class="sxs-lookup"><span data-stu-id="37a5b-120">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="37a5b-121">WebView2 vervollständigt das Laden von Inhalten auf der neuen Seite.</span><span class="sxs-lookup"><span data-stu-id="37a5b-121">WebView2 completes loading content on the new page.</span></span>  |  

<span data-ttu-id="37a5b-122">`navigations`Nachvollziehen jedes neuen Dokuments mithilfe der Navigations-ID \ ( `NavigationId` \).</span><span class="sxs-lookup"><span data-stu-id="37a5b-122">Track `navigations` to each new document using the navigation ID \(`NavigationId`\).</span></span>  <span data-ttu-id="37a5b-123">Die `NavigationId` von WebView ändert sich jedes Mal, wenn eine erfolgreiche Navigation zu einem neuen Dokument vorliegt.</span><span class="sxs-lookup"><span data-stu-id="37a5b-123">The `NavigationId` of WebView changes every time there is a successful navigation to a new document.</span></span>

:::image type="complex" source="../media/navigation-graph.png" alt-text="Navigationsereignisse für Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   <span data-ttu-id="37a5b-125">Navigationsereignisse für Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="37a5b-125">The Microsoft Edge WebView2 Navigation Events</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="37a5b-126">Die vorherige Abbildung stellt Navigationsereignisse mit der gleichen `NavigationId` Eigenschaft für das jeweilige Ereignis arg dar.</span><span class="sxs-lookup"><span data-stu-id="37a5b-126">The previous figure represents navigation events with the same `NavigationId` property on the respective event arg.</span></span>  

 `Navigations` <span data-ttu-id="37a5b-127">Ereignisse mit unterschiedlichen `NavigationId` Ereignisinstanzen können sich überlappen.</span><span class="sxs-lookup"><span data-stu-id="37a5b-127">events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="37a5b-128">Wenn Sie beispielsweise eine Navigation starten, müssen Sie auf das zugehörige Ereignis warten `NavigationStarting` .</span><span class="sxs-lookup"><span data-stu-id="37a5b-128">For instance when you start a navigation, you have to wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="37a5b-129">Wenn Sie dann eine andere Navigation starten, sollten Sie das `NavigationStarting` Ereignis für die erste Navigation, gefolgt vom `NavigationStarting` Ereignis für die zweite Navigate, gefolgt vom `NavigationCompleted` Ereignis für die erste Navigation und dann alle restlichen geeigneten Navigationsereignisse für die zweite Navigation sehen.</span><span class="sxs-lookup"><span data-stu-id="37a5b-129">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="37a5b-130">In Fehlerfällen kann es sich um ein Ereignis handeln `ContentLoading` , das davon abhängt, ob die Navigation auf einer Fehlerseite fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="37a5b-130">In error cases there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="37a5b-131">Im Fall einer HTTP-Umleitung gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile, bei denen nachfolgende Ereignisargumente die `IsRedirect` Eigenschaft festzulegen, jedoch `NavigationId` bleibt die gleiche.</span><span class="sxs-lookup"><span data-stu-id="37a5b-131">In the case of an HTTP redirect, there are multiple `NavigationStarting` events in a row, where subsequent event args have the `IsRedirect` property set, however the `NavigationId` remains the same.</span></span>  
 
 <span data-ttu-id="37a5b-132">Dasselbe Dokument `navigations` , beispielsweise das Navigieren zu einem Fragment, führt nicht zu dem `NavigationStarting` Ereignis und erhöht nicht das `NavigationId` .</span><span class="sxs-lookup"><span data-stu-id="37a5b-132">Same document `navigations`, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId`.</span></span>  

<span data-ttu-id="37a5b-133">Zum Überwachen oder Abbrechen `navigations` innerhalb von unter Frames in der WebView verwenden Sie das `FrameNavigationStarting` und die Ereignisse, die `FrameNavigationCompleted` wie die entsprechenden nicht-Frame-Entsprechungs Ereignisse fungieren.</span><span class="sxs-lookup"><span data-stu-id="37a5b-133">To monitor or cancel `navigations` inside subframes in the WebView, use the `FrameNavigationStarting` and the `FrameNavigationCompleted` events which act just like the equivalent non-frame counterpart events.</span></span>  

<!-- links -->  

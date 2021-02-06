---
description: Navigation
title: Navigation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/05/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: ac15b9f32a29c64bbdc2a7886fa654a2d71a5453
ms.sourcegitcommit: 4cea8cf99b5f12db9d2daba99bbf48f3ccc537fe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314797"
---
# <span data-ttu-id="7a7f6-104">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="7a7f6-104">Navigation events</span></span>  

<span data-ttu-id="7a7f6-105">Die normale Abfolge von Navigationsereignissen ist `NavigationStarting` , , und dann `SourceChanged` `ContentLoading` `HistoryChanged` `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="7a7f6-105">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="7a7f6-106">Die folgenden Ereignisse beschreiben den Status von WebView2 während jeder Navigation.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-106">The following events describe the state of WebView2 during each navigation.</span></span>  

| <span data-ttu-id="7a7f6-107">Sequence</span><span class="sxs-lookup"><span data-stu-id="7a7f6-107">Sequence</span></span> | <span data-ttu-id="7a7f6-108">Ereignisname</span><span class="sxs-lookup"><span data-stu-id="7a7f6-108">Event name</span></span> | <span data-ttu-id="7a7f6-109">Details</span><span class="sxs-lookup"><span data-stu-id="7a7f6-109">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="7a7f6-110">1</span><span class="sxs-lookup"><span data-stu-id="7a7f6-110">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="7a7f6-111">WebView2 beginnt zu navigieren, und die Navigation führt zu einer Netzwerkanforderung.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-111">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="7a7f6-112">Der Host kann die Anforderung während des Ereignisses disallowen.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-112">The host is able to disallow the request during the event.</span></span>  |  
| <span data-ttu-id="7a7f6-113">2</span><span class="sxs-lookup"><span data-stu-id="7a7f6-113">2</span></span> | `SourceChanged`  |  <span data-ttu-id="7a7f6-114">Die Quelle von WebView2 ändert sich in eine neue URL.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-114">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="7a7f6-115">Das Ereignis kann durch eine Navigation verursacht werden, die keine Netzwerkanforderung verursacht, z. B. eine Fragmentnavigation.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-115">The event may result from a navigation that does not cause a network request such as a fragment navigation.</span></span>  |  
| <span data-ttu-id="7a7f6-116">3</span><span class="sxs-lookup"><span data-stu-id="7a7f6-116">3</span></span> | `HistoryChanged`  |  <span data-ttu-id="7a7f6-117">Der Verlauf von WebView2 wird als Ergebnis der Navigation aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-117">The history of WebView2 updates as a result of the navigation.</span></span>  |  
| <span data-ttu-id="7a7f6-118">4</span><span class="sxs-lookup"><span data-stu-id="7a7f6-118">4</span></span> | `ContentLoading`  |  <span data-ttu-id="7a7f6-119">WebView2 beginnt mit dem Laden von Inhalten für die neue Seite.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-119">WebView2 starts loading content for the new page.</span></span>  |  
| <span data-ttu-id="7a7f6-120">5</span><span class="sxs-lookup"><span data-stu-id="7a7f6-120">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="7a7f6-121">WebView2 schließt das Laden von Inhalten auf der neuen Seite ab.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-121">WebView2 completes loading content on the new page.</span></span>  |  

<span data-ttu-id="7a7f6-122">Verfolgen `navigations` Sie jedes neue Dokument mithilfe der Navigations-ID \( `NavigationId` \).</span><span class="sxs-lookup"><span data-stu-id="7a7f6-122">Track `navigations` to each new document using the navigation ID \(`NavigationId`\).</span></span>  <span data-ttu-id="7a7f6-123">Die `NavigationId` WebView ändert sich jedes Mal, wenn eine erfolgreiche Navigation zu einem neuen Dokument besteht.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-123">The `NavigationId` of WebView changes every time there is a successful navigation to a new document.</span></span>

:::image type="complex" source="../media/navigation-graph.png" alt-text="Die Microsoft Edge WebView2-Navigationsereignisse" lightbox="../media/navigation-graph.png":::
   <span data-ttu-id="7a7f6-125">Die Microsoft Edge WebView2-Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="7a7f6-125">The Microsoft Edge WebView2 Navigation Events</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="7a7f6-126">Die vorherige Abbildung stellt Navigationsereignisse mit derselben `NavigationId` Eigenschaft für das entsprechende Ereignis arg dar.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-126">The previous figure represents navigation events with the same `NavigationId` property on the respective event arg.</span></span>  

 `Navigations` <span data-ttu-id="7a7f6-127">Ereignisse mit unterschiedlichen `NavigationId` Ereignisinstanzen überlappen können.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-127">events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="7a7f6-128">Wenn Sie beispielsweise eine Navigation starten, müssen Sie auf das zugehörige Ereignis `NavigationStarting` warten.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-128">For instance when you start a navigation, you have to wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="7a7f6-129">Wenn Sie dann eine andere Navigation starten, sollte das Ereignis für die erste Navigation gefolgt vom Ereignis für die zweite Navigation angezeigt werden, gefolgt vom Ereignis für die erste Navigation und dann von allen anderen geeigneten Navigationsereignissen für die zweite `NavigationStarting` `NavigationStarting` `NavigationCompleted` Navigation.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-129">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="7a7f6-130">In Fehlerfällen kann es je nachdem, ob die Navigation zu einer Fehlerseite fortgesetzt wird, ein Ereignis sein oder `ContentLoading` nicht.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-130">In error cases there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="7a7f6-131">Im Fall einer HTTP-Umleitung gibt es mehrere Ereignisse in einer Zeile, bei denen nachfolgende Ereignis-Args den Eigenschaftensatz `NavigationStarting` `IsRedirect` haben, dies bleibt jedoch `NavigationId` gleich.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-131">In the case of an HTTP redirect, there are multiple `NavigationStarting` events in a row, where subsequent event args have the `IsRedirect` property set, however the `NavigationId` remains the same.</span></span>  
 
 <span data-ttu-id="7a7f6-132">Dasselbe Dokument, z. B. das Navigieren zu einem Fragment, führt nicht zu dem Ereignis `navigations` und erhöht nicht das `NavigationStarting` `NavigationId` .</span><span class="sxs-lookup"><span data-stu-id="7a7f6-132">Same document `navigations`, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId`.</span></span>  

<span data-ttu-id="7a7f6-133">Verwenden Sie zum Überwachen oder Abbrechen innerhalb von Unterframes in der WebView die Ereignisse und die Ereignisse, die genau wie die entsprechenden Ereignisse, die keine Frames sind, `navigations` `FrameNavigationStarting` `FrameNavigationCompleted` agieren.</span><span class="sxs-lookup"><span data-stu-id="7a7f6-133">To monitor or cancel `navigations` inside subframes in the WebView, use the `FrameNavigationStarting` and the `FrameNavigationCompleted` events which act just like the equivalent non-frame counterpart events.</span></span>  

<!-- links -->  

---
description: Navigation
title: Navigations-| WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, Webview2, Webview, wpf-Apps, Wpf, Microsoft Edge, ICoreWebView2, ICoreWebView2Host, Browsersteuerung, Edge-HTML
ms.openlocfilehash: e87994d6205f81e01385a131e17091d0c8b001d5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470844"
---
# <a name="navigation-events"></a><span data-ttu-id="59045-104">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="59045-104">Navigation events</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="59045-105">Unterstützte Plattformen:</span><span class="sxs-lookup"><span data-stu-id="59045-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="59045-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="59045-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="59045-107">Navigationsereignisse werden ausgeführt, wenn bestimmte asynchrone Aktionen für den inhalt auftreten, der in einer WebView2-Instanz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="59045-107">Navigation events run when specific asynchronous actions occur to the content displayed in a WebView2 instance.</span></span>  <span data-ttu-id="59045-108">Wenn ein WebView2-Benutzer beispielsweise zu einer neuen Website navigiert, lauscht der systemeigene Inhalt auf die Änderung mithilfe des `NavigationStarting` Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="59045-108">For example, when a WebView2 user navigates to a new website, the native content listens for the change using `NavigationStarting` event.</span></span>  <span data-ttu-id="59045-109">Wenn die Navigationsaktion abgeschlossen ist, `NavigationCompleted` wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59045-109">When the navigation action completes, `NavigationCompleted` runs.</span></span>  <span data-ttu-id="59045-110">Ein gutes Beispiel für Navigationsereignisse finden Sie unter Erste Schritte in [WebView2.][Webview2IndexGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="59045-110">For a good example of navigation events, navigate to [WebView2 getting started guide][Webview2IndexGettingStarted].</span></span>  

<!--todo:  Move the relevant information out of the getting started guide to better focus the content and leave the most concise elements in the getting started guide.  -->   

<span data-ttu-id="59045-111">Die normale Sequenz von Navigationsereignissen ist `NavigationStarting` , , , und dann `SourceChanged` `ContentLoading` `HistoryChanged` `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="59045-111">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="59045-112">Die folgenden Ereignisse beschreiben den Status von WebView2 während jeder Navigation.</span><span class="sxs-lookup"><span data-stu-id="59045-112">The following events describe the state of WebView2 during each navigation.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/navigation-graph.png" alt-text="Die Microsoft Edge WebView2-Navigationsereignisse" lightbox="../media/navigation-graph.png":::
         <span data-ttu-id="59045-114">Die Microsoft Edge WebView2-Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="59045-114">The Microsoft Edge WebView2 Navigation Events</span></span>  
      :::image-end:::  
      
      > [!NOTE]
      > <span data-ttu-id="59045-115">Die Abbildung stellt Navigationsereignisse mit derselben `NavigationId` Eigenschaft für das jeweilige Ereignisargument dar.</span><span class="sxs-lookup"><span data-stu-id="59045-115">The figure represents navigation events with the same `NavigationId` property on the respective event argument.</span></span>  
   :::column-end:::
   :::column span="2":::
      | <span data-ttu-id="59045-116">Sequence</span><span class="sxs-lookup"><span data-stu-id="59045-116">Sequence</span></span> | <span data-ttu-id="59045-117">Ereignisname</span><span class="sxs-lookup"><span data-stu-id="59045-117">Event name</span></span> | <span data-ttu-id="59045-118">Details</span><span class="sxs-lookup"><span data-stu-id="59045-118">Details</span></span> |  
      |:--- |:--- |:--- |  
      | <span data-ttu-id="59045-119">1</span><span class="sxs-lookup"><span data-stu-id="59045-119">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="59045-120">WebView2 beginnt zu navigieren, und die Navigation führt zu einer Netzwerkanforderung.</span><span class="sxs-lookup"><span data-stu-id="59045-120">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="59045-121">Der Host kann die Anforderung während des Ereignisses nicht mehr senden.</span><span class="sxs-lookup"><span data-stu-id="59045-121">The host may disallow the request during the event.</span></span>  |  
      | <span data-ttu-id="59045-122">2</span><span class="sxs-lookup"><span data-stu-id="59045-122">2</span></span> | `SourceChanged`  |  <span data-ttu-id="59045-123">Die Quelle von WebView2 wird in eine neue URL geändert.</span><span class="sxs-lookup"><span data-stu-id="59045-123">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="59045-124">Das Ereignis kann durch eine Navigationsaktion verursacht werden, die keine Netzwerkanforderung verursacht, z. B. eine Fragmentnavigation.</span><span class="sxs-lookup"><span data-stu-id="59045-124">The event may result from a navigation action that does not cause a network request such as a fragment navigation.</span></span>  |  
      | <span data-ttu-id="59045-125">3</span><span class="sxs-lookup"><span data-stu-id="59045-125">3</span></span> | `ContentLoading`  |  <span data-ttu-id="59045-126">WebView beginnt mit dem Laden von Inhalten für die neue Seite.</span><span class="sxs-lookup"><span data-stu-id="59045-126">WebView starts loading content for the new page.</span></span>  |  
      | <span data-ttu-id="59045-127">4</span><span class="sxs-lookup"><span data-stu-id="59045-127">4</span></span> | `HistoryChanged`  |  <span data-ttu-id="59045-128">Die Navigation bewirkt, dass der Verlauf von WebView2 aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="59045-128">The navigation causes the history of WebView2 to update.</span></span>  |  
      | <span data-ttu-id="59045-129">5</span><span class="sxs-lookup"><span data-stu-id="59045-129">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="59045-130">WebView2 schließt das Laden von Inhalten auf der neuen Seite ab.</span><span class="sxs-lookup"><span data-stu-id="59045-130">WebView2 completes loading content on the new page.</span></span>  |  
   :::column-end:::
:::row-end:::

<span data-ttu-id="59045-131">Nachverfolgen von Navigationsereignissen zu jedem neuen Dokument mithilfe der Navigations-ID \( `NavigationId` Event\).</span><span class="sxs-lookup"><span data-stu-id="59045-131">Track navigation events to each new document using the navigation ID \(`NavigationId` event\).</span></span>  <span data-ttu-id="59045-132">Das `NavigationId` Ereignis von WebView ändert sich jedes Mal, wenn eine erfolgreiche Navigation zu einem neuen Dokument abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="59045-132">The `NavigationId` event of WebView changes every time a successful navigation to a new document completes.</span></span>  

 <span data-ttu-id="59045-133">Navigationsereignisse mit unterschiedlichen `NavigationId` Ereignisinstanzen können überlappen.</span><span class="sxs-lookup"><span data-stu-id="59045-133">Navigation events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="59045-134">Wenn Sie beispielsweise ein Navigationsereignis starten, müssen Sie auf das zugehörige Ereignis `NavigationStarting` warten.</span><span class="sxs-lookup"><span data-stu-id="59045-134">For instance, when you start a navigation event, you must wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="59045-135">Wenn Sie dann eine andere Navigation starten, sollte das Ereignis für die erste Navigation angezeigt werden, gefolgt von dem Ereignis für die zweite Navigation, gefolgt von dem Ereignis für die erste Navigation und dann alle anderen entsprechenden Navigationsereignisse für die zweite `NavigationStarting` `NavigationStarting` `NavigationCompleted` Navigation.</span><span class="sxs-lookup"><span data-stu-id="59045-135">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="59045-136">In Fehlerfällen gibt es möglicherweise ein Ereignis, je nachdem, ob die Navigation zu einer Fehlerseite `ContentLoading` fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="59045-136">In error cases, there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="59045-137">Wenn eine HTTP-Umleitung auftritt, gibt es mehrere Ereignisse in einer Zeile, bei denen für spätere Ereignisargumente die Eigenschaft festgelegt ist, das Ereignis `NavigationStarting` `IsRedirect` jedoch unverändert `NavigationId` bleibt.</span><span class="sxs-lookup"><span data-stu-id="59045-137">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row, where later event arguments have the `IsRedirect` property set, however the `NavigationId` event remains the same.</span></span>  
 
 <span data-ttu-id="59045-138">Dieselben Dokumentnavigationsereignisse, z. B. die Navigation zu einem Fragment, führen nicht zu dem Ereignis und erhöhen `NavigationStarting` das Ereignis `NavigationId` nicht.</span><span class="sxs-lookup"><span data-stu-id="59045-138">Same document navigation events, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId` event.</span></span>  

<span data-ttu-id="59045-139">Verwenden Sie zum Überwachen oder Abbrechen von Navigationsereignissen innerhalb von Unterframes in einer WebView2-Instanz die Ereignisse and, die genau wie die entsprechenden Ereignisse außerhalb des `FrameNavigationStarting` `FrameNavigationCompleted` Frames agieren.</span><span class="sxs-lookup"><span data-stu-id="59045-139">To monitor or cancel navigation events inside subframes in a WebView2 instance, use the `FrameNavigationStarting` and `FrameNavigationCompleted` events that act just like the equivalent non-frame counterpart events.</span></span>  

## <a name="see-also"></a><span data-ttu-id="59045-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="59045-140">See also</span></span>  

*   <span data-ttu-id="59045-141">Um mit WebView2 zu beginnen, navigieren Sie zu [WebView2 Anleitungen für erste Schritte.][Webview2IndexGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="59045-141">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2IndexGettingStarted] guides.</span></span>  
*   <span data-ttu-id="59045-142">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samples] auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="59045-142">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="59045-143">Weitere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="59045-143">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="59045-144">Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="59045-144">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="59045-145">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="59045-145">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2-Klasse | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

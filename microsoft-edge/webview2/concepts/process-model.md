---
description: Prozessmodell
title: Prozessmodell | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, Webview2, Webview, wpf-Apps, Wpf, Microsoft Edge, ICoreWebView2, ICoreWebView2Host, Browsersteuerung, Edge-HTML
ms.openlocfilehash: 149234fe99485460f9d0c677b176a42d3b1e5050
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470851"
---
# <a name="process-model"></a><span data-ttu-id="9907b-104">Prozessmodell</span><span class="sxs-lookup"><span data-stu-id="9907b-104">Process model</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="9907b-105">Unterstützte Plattformen:</span><span class="sxs-lookup"><span data-stu-id="9907b-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9907b-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="9907b-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="9907b-107">WebView2 verwendet dasselbe Prozessmodell wie der Microsoft Edge-Browser.</span><span class="sxs-lookup"><span data-stu-id="9907b-107">WebView2 uses the same process model as the Microsoft Edge browser.</span></span>  <span data-ttu-id="9907b-108">Weitere Informationen zum Browserprozessmodell finden Sie unter [Browserarchitektur – Innen sehen Sie sich modernen Webbrowser an.][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]</span><span class="sxs-lookup"><span data-stu-id="9907b-108">For more information about the browser process model, navigate to [Browser Architecture - Inside look at modern web browser][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span></span>  

<span data-ttu-id="9907b-109">Ein Browserprozess ist den Rendererprozessen und anderen Hilfsprozessen zugeordnet, wie in diesem Artikel beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9907b-109">One browser process is associated with the renderer processes and other utility processes as described in that article.</span></span>  <span data-ttu-id="9907b-110">Wenn WebView2 angegeben ist, verwenden die anfordernden Host-App-Prozesse außerdem WebView2.</span><span class="sxs-lookup"><span data-stu-id="9907b-110">Additionally, if WebView2 is specified, the host app requesting processes use WebView2.</span></span>  

:::image type="complex" source="../media/process-model-1.png" alt-text="Prozess 1" lightbox="../media/process-model-1.png":::
   <span data-ttu-id="9907b-112">Prozess 1</span><span class="sxs-lookup"><span data-stu-id="9907b-112">Process 1</span></span>  
:::image-end:::  

<span data-ttu-id="9907b-113">Ein Browserprozess ist nur einem Benutzerdatenordner zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9907b-113">A browser process is associated with only one user data folder.</span></span>  <span data-ttu-id="9907b-114">Ein Anforderungsprozess kann mehrere Benutzerdatenordner angeben.</span><span class="sxs-lookup"><span data-stu-id="9907b-114">A request process may specify more than one user data folder.</span></span>  <span data-ttu-id="9907b-115">Ein Anforderungsprozess, der mehrere Benutzerdatenordner angibt, ist der gleichen Anzahl von Browserprozessen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9907b-115">A request process that specifies more than one user data folder is associated with the same number of browser processes.</span></span>  
<span data-ttu-id="9907b-116">Bei einem Anforderungsprozess, der Zugriff auf zwei Benutzerdatenordner anfordert, werden beispielsweise zwei Browserprozesse verwendet.</span><span class="sxs-lookup"><span data-stu-id="9907b-116">For example, a request process that requests access to two user data folders uses two browser processes.</span></span>  

:::image type="complex" source="../media/process-model-2.png" alt-text="Prozess 2" lightbox="../media/process-model-2.png":::
   <span data-ttu-id="9907b-118">Prozess 2</span><span class="sxs-lookup"><span data-stu-id="9907b-118">Process 2</span></span>  
:::image-end:::  

<span data-ttu-id="9907b-119">Ein Browserprozess ist mehreren Rendererprozessen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9907b-119">A browser process is associated with several renderer processes.</span></span>  <span data-ttu-id="9907b-120">Eine WebView 2-Instanz erstellt einen Browserprozess für Serviceframes.</span><span class="sxs-lookup"><span data-stu-id="9907b-120">A WebView 2 instance creates a browser process to service frames.</span></span>  <span data-ttu-id="9907b-121">Ein Browserprozess kann mehreren Frames zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="9907b-121">A browser process may be associated with multiple frames.</span></span>  <span data-ttu-id="9907b-122">Ein Browserprozess kann verschiedenen Instanzen von WebView2 zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="9907b-122">A browser process may be associated with different instances of WebView2.</span></span>  <span data-ttu-id="9907b-123">Die Anzahl der Renderprozesse variiert je nach den folgenden Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="9907b-123">The number of render processes varies based on the following conditions.</span></span>  

*   <span data-ttu-id="9907b-124">Verwenden des Websiteisolationsfeatures in Ihrem Browser.</span><span class="sxs-lookup"><span data-stu-id="9907b-124">Use of the website isolation feature in your browser.</span></span>  
*   <span data-ttu-id="9907b-125">Die Anzahl unterschiedlicher getrennter Ursprünge, die in zugeordneten Instanzen von WebView2 gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="9907b-125">The number of distinct disconnected origins rendered in associated instances of WebView2.</span></span>  

<span data-ttu-id="9907b-126">Die Websiteisolationsbrowserfunktion wird in den vorherigen Inhalten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9907b-126">The website isolation browser feature is described in the previous content.</span></span> 
<!--todo:  which previous content?  -->  
 

<span data-ttu-id="9907b-127">Der `CoreWebView2Environment` stellt einen Benutzerdatenordner und Browserprozess dar.</span><span class="sxs-lookup"><span data-stu-id="9907b-127">The `CoreWebView2Environment` represents a user data folder and browser process.</span></span>  <span data-ttu-id="9907b-128">Der entspricht nicht direkt einem Satz von Prozessen, da verschiedene Rendererprozesse von einem WebView2 abhängig von der Zuvor beschriebenen Websiteisolation `CoreWebView2` verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9907b-128">The `CoreWebView2` does not directly correspond to any one set of processes since various renderer processes are used by a WebView2 depending on website isolation as previously described.</span></span>  

<span data-ttu-id="9907b-129">Verwenden Sie das Ereignis von , um auf Abstürze und Hänge im Browser und renderer-Prozessen `ProcessFailed` zu `CoreWebView2` reagieren.</span><span class="sxs-lookup"><span data-stu-id="9907b-129">To react to crashes and hangs in the browser and renderer processes, use the `ProcessFailed` event of `CoreWebView2`.</span></span>  

<span data-ttu-id="9907b-130">Verwenden Sie die Methode von , um zugeordnete Browser- und Rendererprozesse `Close` sicher herunterfahren zu `CoreWebView2Controller` können.</span><span class="sxs-lookup"><span data-stu-id="9907b-130">To safely shut down associated browser and renderer processes, use the `Close` method of `CoreWebView2Controller`.</span></span>  

<span data-ttu-id="9907b-131">Führen Sie zum Öffnen des Fensters Browser Task Manager aus dem **DevTools-Fenster** einer WebView2-Instanz die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="9907b-131">To open the Browser Task Manager window from the **DevTools** window of a WebView2 instance, complete on of the following actions.</span></span>  

*   <span data-ttu-id="9907b-132">Wählen Sie `Shift` + `Escape` aus.</span><span class="sxs-lookup"><span data-stu-id="9907b-132">Select `Shift`+`Escape`.</span></span>  
*   <span data-ttu-id="9907b-133">Zeigen Sie auf die Titelleiste des DevTools-Fensters, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie `Browser task manager` aus.</span><span class="sxs-lookup"><span data-stu-id="9907b-133">Hover on the DevTools window title bar, open the contextual menu \(right-click\), and choose `Browser task manager`.</span></span>  

<span data-ttu-id="9907b-134">Alle Prozesse, die mit dem Browserprozess Ihrer WebView2 verknüpft sind, werden einschließlich der zugehörigen Zwecke angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9907b-134">All processes associated with the browser process of your WebView2 are displayed including associated purposes.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9907b-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9907b-135">See also</span></span>  

*   <span data-ttu-id="9907b-136">Um mit WebView2 zu beginnen, navigieren Sie zu [WebView2-Anleitungen für erste Schritte.][Webview2IndexGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="9907b-136">To Get Started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2IndexGettingStarted] guides.</span></span>  
*   <span data-ttu-id="9907b-137">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samples] auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="9907b-137">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="9907b-138">Weitere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="9907b-138">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="9907b-139">Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="9907b-139">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="9907b-140">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="9907b-140">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2-Klasse | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Browserarchitektur – Innenseite des modernen Webbrowsers (Teil 1)"  

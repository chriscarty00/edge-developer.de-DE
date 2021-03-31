---
description: Prozessmodell
title: Prozessmodell
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8548308896815266fbd1e150da979b56cfb268e2
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895565"
---
# <span data-ttu-id="47990-104">Prozessmodell</span><span class="sxs-lookup"><span data-stu-id="47990-104">Process model</span></span>  

<span data-ttu-id="47990-105">WebView2 verwendet das gleiche Prozessmodell wie der Microsoft Edge-Browser.</span><span class="sxs-lookup"><span data-stu-id="47990-105">WebView2 uses the same process model as the Microsoft Edge browser.</span></span>  <span data-ttu-id="47990-106">Weitere Informationen zum Browser-Prozessmodell finden Sie unter [Browser Architektur – Innenansicht des modernen Webbrowsers][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span><span class="sxs-lookup"><span data-stu-id="47990-106">For more information about the browser process model, see [Browser Architecture - Inside look at modern web browser][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span></span> 

<span data-ttu-id="47990-107">Ein Browserprozess ist mit den Renderer-Prozessen und anderen Dienstprogrammen verknüpft, wie in diesem Artikel beschrieben.</span><span class="sxs-lookup"><span data-stu-id="47990-107">One browser process is associated with the renderer processes and other utility processes as described in that article.</span></span>  <span data-ttu-id="47990-108">Darüber hinaus gibt es im Fall von WebView2 eine Host-APP, die mithilfe von WebView2 Prozesse anfordert.</span><span class="sxs-lookup"><span data-stu-id="47990-108">Additionally, in the case of WebView2, there are host app requesting processes using WebView2.</span></span>  

:::image type="complex" source="../media/process-model-1.png" alt-text="Prozess 1" lightbox="../media/process-model-1.png":::
   <span data-ttu-id="47990-110">Prozess 1</span><span class="sxs-lookup"><span data-stu-id="47990-110">Process 1</span></span>  
:::image-end:::  

<span data-ttu-id="47990-111">Ein Browserprozess wird pro benutzerdatenordner in einer Benutzersitzung angegeben, die einem beliebigen WebView2-Prozess dient, der den benutzerdatenordner angibt.</span><span class="sxs-lookup"><span data-stu-id="47990-111">One browser process is specified per user data folder in a user session that serve any WebView2 requesting process that specifies that user data folder.</span></span>  <span data-ttu-id="47990-112">Dies bedeutet, dass ein Browserprozess möglicherweise mehrere anfordernde Prozesse bedient und ein anfordernder Prozess möglicherweise mehrere Browserprozesse verwendet.</span><span class="sxs-lookup"><span data-stu-id="47990-112">This means one browser process may be serving multiple requesting processes and one requesting process may be using multiple browser processes.</span></span>  

:::image type="complex" source="../media/process-model-2.png" alt-text="Prozess 2" lightbox="../media/process-model-2.png":::
   <span data-ttu-id="47990-114">Prozess 2</span><span class="sxs-lookup"><span data-stu-id="47990-114">Process 2</span></span>  
:::image-end:::  

<span data-ttu-id="47990-115">Ein Browserprozess verfügt über eine Reihe zugeordneter Renderer-Prozesse.</span><span class="sxs-lookup"><span data-stu-id="47990-115">A browser process has some number of associated renderer processes.</span></span>  <span data-ttu-id="47990-116">Die Browserprozesse werden nach Bedarf erstellt, um potenziell mehrere Frames in verschiedenen Instanzen von WebView2 zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="47990-116">The browser processes are created as required to service potentially multiple frames in different instances of WebView2.</span></span>  <span data-ttu-id="47990-117">Die Anzahl der Renderer-Prozesse variiert basierend auf dem Feature "Website Isolierungs Browser" und der Anzahl der unterschiedlichen getrennten Ursprünge, die in zugeordneten Instanzen von WebView2 gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="47990-117">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated instances of WebView2.</span></span>  <span data-ttu-id="47990-118">Das Feature "Website Isolierungs Browser" wird im vorherigen Inhalt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="47990-118">The site isolation browser feature is described in the previous content.</span></span>  

<span data-ttu-id="47990-119">Der `CoreWebView2Environment` stellt einen benutzerdatenordner und einen Browserprozess dar.</span><span class="sxs-lookup"><span data-stu-id="47990-119">The `CoreWebView2Environment` represents a user data folder and browser process.</span></span>  <span data-ttu-id="47990-120">Der entspricht `CoreWebView2` nicht direkt einem Satz von Prozessen, da verschiedene Renderer-Prozesse von einem WebView2-Element abhängig von der Standort Isolierung wie zuvor beschrieben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47990-120">The `CoreWebView2` does not directly correspond to any one set of processes since various renderer processes are used by a WebView2 depending on site isolation as previously described.</span></span>  

<span data-ttu-id="47990-121">Sie können in diesen Browser-und Renderer-Prozessen mit dem `ProcessFailed` Ereignis von `CoreWebView2` .</span><span class="sxs-lookup"><span data-stu-id="47990-121">You are able to react to crashes and hangs in these browser and renderer processes using the `ProcessFailed` event of `CoreWebView2`.</span></span>  

<span data-ttu-id="47990-122">Sie können zugeordnete Browser-und Renderer-Prozesse mithilfe der `Close` Methode von sicher Herunterfahren `CoreWebView2Controller` .</span><span class="sxs-lookup"><span data-stu-id="47990-122">You are able to safely shutdown associated browser and renderer processes using the `Close` method of `CoreWebView2Controller`.</span></span>  

<span data-ttu-id="47990-123">Um das Fenster des Task-Managers des Browsers über das **devtools** -Fenster einer WebView2-Instanz zu öffnen, können Sie `Shift` + `Escape` auf der Titelleiste des devtools-Fensters auswählen oder darauf zeigen, das Kontextmenü öffnen \(Klicken Sie mit der rechten Maustaste auf \), und wählen Sie aus `Browser task manager` .</span><span class="sxs-lookup"><span data-stu-id="47990-123">To open the Browser Task Manager window from the **DevTools** window of a WebView2 instance, you are able to select `Shift`+`Escape` or hover on the DevTools window title bar, open the contextual menu \(right-click\), and choose `Browser task manager`.</span></span>  <span data-ttu-id="47990-124">Alle Prozesse, die dem Browserprozess ihrer WebView2 zugeordnet sind, werden einschließlich der zugehörigen Zwecke angezeigt.</span><span class="sxs-lookup"><span data-stu-id="47990-124">All processes associated with the browser process of your WebView2 are displayed including associated purposes.</span></span>  

<!-- links -->  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Browser Architektur – Einblick in den modernen Webbrowser (Teil 1)"  

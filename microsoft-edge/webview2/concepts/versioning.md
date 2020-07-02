---
description: Für Microsoft Edge-WebView2 verwendete Versions Verwaltungsmodelle
title: Versionsverwaltung von Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 059bbeb34f372af0cef944e484599c0b50543cc9
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844425"
---
# <span data-ttu-id="7cfee-104">Grundlegendes zu WebView2 SDK-Versionen</span><span class="sxs-lookup"><span data-stu-id="7cfee-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="7cfee-105">WebView2 hängt von der Funktion von Microsoft Edge ab.</span><span class="sxs-lookup"><span data-stu-id="7cfee-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="7cfee-106">Für jedes WebView2-SDK muss mindestens eine Browserversion installiert sein.</span><span class="sxs-lookup"><span data-stu-id="7cfee-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="7cfee-107">Die Mindestversion wird in der Paketversion des SDK widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="7cfee-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="7cfee-108">Wenn Sie beispielsweise das verwenden `SDK package version 0.9.488` , müssen Sie Microsoft Edge mit einer Buildnummer von 488 oder höher installieren.</span><span class="sxs-lookup"><span data-stu-id="7cfee-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="7cfee-109">Die Browserversion ist auch in den WebView2- [Versions][Releasenotes]hinweisen angegeben.</span><span class="sxs-lookup"><span data-stu-id="7cfee-109">The browser version is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="7cfee-110">Weitere Informationen zu den neuesten Versionen des Browsers finden Sie unter [Browser Kanäle][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="7cfee-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="7cfee-111">WebView2 befindet sich derzeit in der Vorschau.</span><span class="sxs-lookup"><span data-stu-id="7cfee-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="7cfee-112">Während das WebView-Team versucht, die Abwärtskompatibilität zwischen Browserversionen und SDKs zu gewährleisten, ist dies nicht gewährleistet, da neuere Versionen des Browsers möglicherweise ältere SDK-Versionen nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7cfee-112">While the WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed since newer versions of the browser may not support older SDK versions.</span></span>  <span data-ttu-id="7cfee-113">Wenn sich die Änderungen zwischen Browserversionen und SDKs unterbrechen, gibt das WebView-Team die Änderungen in den [Versions][Releasenotes]hinweisen an.</span><span class="sxs-lookup"><span data-stu-id="7cfee-113">If there are breaking changes between browser versions and SDKs, the WebView team specifies the changes in the [release notes][Releasenotes].</span></span>  

<span data-ttu-id="7cfee-114">In Zukunft plant das WebView-Team, das Verteilungsmodell für WebView2-Anwendungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7cfee-114">In the future, the  WebView team plans to change the distribution model for WebView2 applications.</span></span>  <span data-ttu-id="7cfee-115">Weitere Informationen finden Sie unter Anzeigen des [immergrünen Verteilungsmodus][DistributionEvergreenMode].</span><span class="sxs-lookup"><span data-stu-id="7cfee-115">For more information, see see [Evergreen distribution mode][DistributionEvergreenMode].</span></span>  
 
## <span data-ttu-id="7cfee-116">Release-und Pre-Release-Paket</span><span class="sxs-lookup"><span data-stu-id="7cfee-116">Release and pre-release package</span></span>  

<span data-ttu-id="7cfee-117">In Preview enthält das Release-Paket Folgendes.</span><span class="sxs-lookup"><span data-stu-id="7cfee-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="7cfee-118">[Win32 C/C++-APIs][ReferenceWin3209538]: APIs im SDK, die bei GA unverändert bleiben sollen.</span><span class="sxs-lookup"><span data-stu-id="7cfee-118">[Win32 C/C++ APIs][ReferenceWin3209538]: APIs in the SDK that are expected to remain the same at GA.</span></span> 

<span data-ttu-id="7cfee-119">In Preview enthält das Pre-Release-Paket die folgenden Komponenten.</span><span class="sxs-lookup"><span data-stu-id="7cfee-119">In preview, the pre-release package contains the following components.</span></span>  

*   <span data-ttu-id="7cfee-120">.NET-APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]und [Core][ReferenceDotnet09538]</span><span class="sxs-lookup"><span data-stu-id="7cfee-120">.NET APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515], and [Core][ReferenceDotnet09538]</span></span>
*   <span data-ttu-id="7cfee-121">Experimentelle APIs.</span><span class="sxs-lookup"><span data-stu-id="7cfee-121">Experimental APIs.</span></span>  <span data-ttu-id="7cfee-122">Weitere Informationen finden Sie im Abschnitt [experimentelle APIs](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="7cfee-122">For more information, see the [Experimental APIs](#experimental-apis) section.</span></span>  

### <span data-ttu-id="7cfee-123">Experimentelle APIs</span><span class="sxs-lookup"><span data-stu-id="7cfee-123">Experimental APIs</span></span>  

<span data-ttu-id="7cfee-124">Das WebView-Team testet APIs, die die zukünftige Funktionalität mit dem Namen experimental-APIs darstellen.</span><span class="sxs-lookup"><span data-stu-id="7cfee-124">The WebView Team is testing APIs that represent future functionality named Experimental APIs.</span></span>  <span data-ttu-id="7cfee-125">Die experimentellen APIs sind wie `experimental` im SDK markiert.</span><span class="sxs-lookup"><span data-stu-id="7cfee-125">The Experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="7cfee-126">Einige experimentelle APIs können als vollständig stabile APIs im Release-Paket ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="7cfee-126">Some Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="7cfee-127">Sie sollten davon ausgehen, dass alle experimentellen APIs vor der Veröffentlichung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7cfee-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="7cfee-128">Bitte bewerten Sie die experimentellen APIs und geben Sie Feedback über das [WebView Feedback Repo][GithubMicrosoftedgeWebviewfeedback]frei.</span><span class="sxs-lookup"><span data-stu-id="7cfee-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>   

> [!CAUTION]
> <span data-ttu-id="7cfee-129">Vermeiden Sie es, die experimentellen APIs in Produktionsanwendungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7cfee-129">Avoid using the experimental APIs in production applications.</span></span>  

### <span data-ttu-id="7cfee-130">Roadmap</span><span class="sxs-lookup"><span data-stu-id="7cfee-130">Roadmap</span></span>  

<span data-ttu-id="7cfee-131">Nachdem WebView2 einen stabilen allgemeinen verfügbaren Zustand erreicht hat, enthält das Release-Paket alle stabilen, unterstützten Win32 C/C++-und .NET-APIs.</span><span class="sxs-lookup"><span data-stu-id="7cfee-131">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="7cfee-132">Das Pre-Release-Paket enthält experimentelle APIs, die basierend auf Entwickler Feedback und geteilten Einblicken geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="7cfee-132">The pre-release package contains experimental APIs that are subject to change based upon developer feedback and shared insights.</span></span>  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Evergreen-Verteilungsmodus – Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[Releasenotes]: ../releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

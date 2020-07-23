---
description: Für Microsoft Edge-WebView2 verwendete Versions Verwaltungsmodelle
title: Versionsverwaltung von Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: acf3103f39d33586ee0614aeb0f10de0ab71c89a
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894312"
---
# <span data-ttu-id="3d918-104">Grundlegendes zu WebView2 SDK-Versionen</span><span class="sxs-lookup"><span data-stu-id="3d918-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="3d918-105">WebView2 hängt von der Funktion von Microsoft Edge ab.</span><span class="sxs-lookup"><span data-stu-id="3d918-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="3d918-106">Für jedes WebView2-SDK muss mindestens eine Browserversion installiert sein.</span><span class="sxs-lookup"><span data-stu-id="3d918-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="3d918-107">Die Mindestversion wird in der Paketversion des SDK widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="3d918-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="3d918-108">Wenn Sie beispielsweise das verwenden `SDK package version 0.9.488` , müssen Sie Microsoft Edge mit einer Buildnummer von 488 oder höher installieren.</span><span class="sxs-lookup"><span data-stu-id="3d918-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="3d918-109">Die Browserversion ist auch in den WebView2- [Versions][Releasenotes]hinweisen angegeben.</span><span class="sxs-lookup"><span data-stu-id="3d918-109">The browser version is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="3d918-110">Weitere Informationen zu den neuesten Versionen des Browsers finden Sie unter [Browser Kanäle][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="3d918-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="3d918-111">WebView2 befindet sich derzeit in der Vorschau.</span><span class="sxs-lookup"><span data-stu-id="3d918-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="3d918-112">Während das WebView-Team versucht, die Abwärtskompatibilität zwischen Browserversionen und SDKs zu gewährleisten, ist dies nicht gewährleistet, da neuere Versionen des Browsers möglicherweise frühere SDK-Versionen nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3d918-112">While the WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed because newer versions of the browser may not support previous SDK versions.</span></span>  <span data-ttu-id="3d918-113">Wenn es zu Unterbrechungen zwischen Browserversionen und SDKs kommt, geben wir die Änderungen in den [Versions][Releasenotes]hinweisen an.</span><span class="sxs-lookup"><span data-stu-id="3d918-113">If there are breaking changes between browser versions and SDKs, we specify the changes in the [Release Notes][Releasenotes].</span></span>  

<span data-ttu-id="3d918-114">In Zukunft planen wir, das Verteilungsmodell für WebView2-Anwendungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3d918-114">In the future, we plan to change the distribution model for WebView2 applications.</span></span>  <span data-ttu-id="3d918-115">Weitere Informationen finden Sie unter [Evergreen-Verteilungsmodus][DistributionEvergreenMode].</span><span class="sxs-lookup"><span data-stu-id="3d918-115">For more information, see [Evergreen distribution mode][DistributionEvergreenMode].</span></span>  
 
## <span data-ttu-id="3d918-116">Release-und Pre-Release-Paket</span><span class="sxs-lookup"><span data-stu-id="3d918-116">Release and pre-release package</span></span>  

<span data-ttu-id="3d918-117">In Preview enthält das Release-Paket Folgendes.</span><span class="sxs-lookup"><span data-stu-id="3d918-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="3d918-118">[Win32 C/C++-APIs][ReferenceWin3209538]: APIs im SDK, die bei GA unverändert bleiben sollen.</span><span class="sxs-lookup"><span data-stu-id="3d918-118">[Win32 C/C++ APIs][ReferenceWin3209538]: APIs in the SDK that are expected to remain the same at GA.</span></span>  

<span data-ttu-id="3d918-119">In Preview enthält das Pre-Release-Paket die folgenden Komponenten.</span><span class="sxs-lookup"><span data-stu-id="3d918-119">In preview, the pre-release package contains the following components.</span></span>  

*   <span data-ttu-id="3d918-120">.NET-APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]und [Core][ReferenceDotnet09538]</span><span class="sxs-lookup"><span data-stu-id="3d918-120">.NET APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515], and [Core][ReferenceDotnet09538]</span></span>  
*   <span data-ttu-id="3d918-121">Experimentelle APIs.</span><span class="sxs-lookup"><span data-stu-id="3d918-121">Experimental APIs.</span></span>  <span data-ttu-id="3d918-122">Weitere Informationen finden Sie im Abschnitt [experimentelle APIs](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="3d918-122">For more information, see the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="3d918-123">Experimentelle APIs</span><span class="sxs-lookup"><span data-stu-id="3d918-123">Experimental APIs</span></span>  

<span data-ttu-id="3d918-124">Wir testen experimentelle APIs, die möglicherweise zukünftige Funktionen darstellen.</span><span class="sxs-lookup"><span data-stu-id="3d918-124">We are testing experimental APIs that may represent future functionality.</span></span>  <span data-ttu-id="3d918-125">Die experimentellen APIs sind wie `experimental` im SDK markiert.</span><span class="sxs-lookup"><span data-stu-id="3d918-125">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="3d918-126">Experimentelle APIs können als vollständig stabile APIs im Release-Paket ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="3d918-126">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="3d918-127">Sie sollten davon ausgehen, dass alle experimentellen APIs vor der Veröffentlichung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3d918-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="3d918-128">Bitte bewerten Sie die experimentellen APIs und geben Sie Feedback über das [WebView Feedback Repo][GithubMicrosoftedgeWebviewfeedback]frei.</span><span class="sxs-lookup"><span data-stu-id="3d918-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>   

> [!CAUTION]
> <span data-ttu-id="3d918-129">Vermeiden Sie es, die experimentellen APIs in Produktionsanwendungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d918-129">Avoid using the experimental APIs in production applications.</span></span>  

## <span data-ttu-id="3d918-130">Roadmap</span><span class="sxs-lookup"><span data-stu-id="3d918-130">Roadmap</span></span>  

<span data-ttu-id="3d918-131">Nachdem WebView2 einen stabilen allgemeinen verfügbaren Zustand erreicht hat, enthält das Release-Paket alle stabilen, unterstützten Win32 C/C++-und .NET-APIs.</span><span class="sxs-lookup"><span data-stu-id="3d918-131">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="3d918-132">Das Pre-Release-Paket enthält experimentelle APIs, die basierend auf Entwickler Feedback und geteilten Einblicken geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="3d918-132">The pre-release package contains experimental APIs that are subject to change based upon developer feedback and shared insights.</span></span>  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Evergreen-Verteilungsmodus – Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[Releasenotes]: ../releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

---
description: Für Microsoft Edge-WebView2 verwendete Versions Verwaltungsmodelle
title: Versionsverwaltung von Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/18/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8463ce403af069cf25dbf7b08bb49d44c1e54501
ms.sourcegitcommit: f1aa8925f7985a2bbfd951f188a8c19c97e4ff6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2020
ms.locfileid: "10659568"
---
# <span data-ttu-id="d4559-104">Grundlegendes zu Browserversionen und WebView2</span><span class="sxs-lookup"><span data-stu-id="d4559-104">Understanding browser versions and WebView2</span></span>  

<span data-ttu-id="d4559-105">WebView2 hängt von der Funktion von Microsoft Edge ab.</span><span class="sxs-lookup"><span data-stu-id="d4559-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="d4559-106">Für jedes WebView2-SDK muss mindestens eine Browserversion installiert sein.</span><span class="sxs-lookup"><span data-stu-id="d4559-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="d4559-107">Diese Browserversion ist in unseren [Versions][Webview2Releasenotes]hinweisen angegeben.</span><span class="sxs-lookup"><span data-stu-id="d4559-107">This browser version is specified in our [Release Notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="d4559-108">Möglicherweise sehen Sie die Mindestversion, die in der Paketversion des SDK widergespiegelt wird.</span><span class="sxs-lookup"><span data-stu-id="d4559-108">You may see the minimum version reflected in the package version of the SDK.</span></span>  <span data-ttu-id="d4559-109">Wenn Sie beispielsweise das verwenden `SDK package version 0.9.488` , müssen Sie Microsoft Edge mit einer Buildnummer von 488 oder höher installieren.</span><span class="sxs-lookup"><span data-stu-id="d4559-109">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="d4559-110">Weitere Informationen zu den neuesten Versionen des Browsers finden Sie unter [Browser Kanäle][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="d4559-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="d4559-111">WebView2 befindet sich derzeit in der Vorschau.</span><span class="sxs-lookup"><span data-stu-id="d4559-111">WebView2 is currently in Preview.</span></span>  <span data-ttu-id="d4559-112">Das Microsoft Edge-WebView-Team ist zwar bestrebt, die Abwärtskompatibilität zwischen Browserversionen und SDKs zu gewährleisten, es ist jedoch nicht gewährleistet, da einige neuere Versionen des Browsers möglicherweise ältere SDK-Versionen nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d4559-112">While, the Microsoft Edge WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed as some newer versions of the browser may not support older SDK versions.</span></span>  <span data-ttu-id="d4559-113">Wenn sich zwischen Browserversionen und SDKs Unterbrechungen ergeben, gibt das Microsoft Edge-WebView-Team die Änderungen in den [Versions][Webview2Releasenotes]hinweisen an.</span><span class="sxs-lookup"><span data-stu-id="d4559-113">If there are breaking changes between browser versions and SDKs, the Microsoft Edge WebView team indicates the changes in the [release notes][Webview2Releasenotes].</span></span>  

<span data-ttu-id="d4559-114">In Zukunft plant das Microsoft Edge-WebView-Team, das Verteilungsmodell zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d4559-114">In the future, the Microsoft Edge WebView team plans to change the distribution model.</span></span>  <span data-ttu-id="d4559-115">Das Microsoft Edge-WebView-Team plant, die direkte Abhängigkeit vom Microsoft Edge-Browser von WebView2 zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d4559-115">The Microsoft Edge WebView team plans to remove the direct dependency on the Microsoft Edge browser from WebView2.</span></span>  <!--To learn more, see [WebView2 Runtime][Webview2IndexEdgeRuntime] in the [Distribution][Webview2Distibution] section.  -->  

<!--todo: dd link to distribution.md after publication  -->  

## <span data-ttu-id="d4559-116">Experimentelle APIs</span><span class="sxs-lookup"><span data-stu-id="d4559-116">Experimental APIs</span></span>  

<span data-ttu-id="d4559-117">Während WebView2 eine Vorschau ist, wird davon ausgegangen, dass die APIs im SDK bei GA unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="d4559-117">While WebView2 is a preview, the APIs in the SDK are expected to remain the same at GA.</span></span>  <span data-ttu-id="d4559-118">Es gibt [experimentelle APIs][Webview2ReferenceWin3209488Experimental] , die im SDK enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d4559-118">There are [experimental APIs][Webview2ReferenceWin3209488Experimental] included in the SDK.</span></span>  <span data-ttu-id="d4559-119">Bitte bewerten Sie die experimentellen APIs und senden Sie Ihr Feedback über das [WebView Feedback Repo][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="d4559-119">Please evaluate the experimental APIs and send your feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

### <span data-ttu-id="d4559-120">Roadmap</span><span class="sxs-lookup"><span data-stu-id="d4559-120">Roadmap</span></span>  

<span data-ttu-id="d4559-121">Nachdem WebView2 einen stabilen allgemeinen verfügbaren Zustand erreicht hat und wir das 1.0.0-SDK freigeben, plant das Microsoft Edge WebView-Team, alle experimentellen APIs in ein Pre-Release-Paket zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="d4559-121">After WebView2 reaches a stable general available state and we release the 1.0.0 SDK, the Microsoft Edge WebView team plans to move all experimental APIs to a pre-release package.</span></span>  <span data-ttu-id="d4559-122">Das Pre-Release-Paket ermöglicht weiterhin Feedback und Einblicke in die neuesten Features, während die stable-Release-Version Abwärtskompatibilität aufrecht erhält.</span><span class="sxs-lookup"><span data-stu-id="d4559-122">The pre-release package continues to allow for feedback and insight into the latest features, while the stable release version maintains backward compatibility.</span></span>  

<!--links -->

[Webview2Distibution]: ./distribution.md "nicht vorhanden | Microsoft docs"  
[Webview2IndexEdgeRuntime]: ../index.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2 Runtime – Microsoft Edge WebView2 (Developer Preview) | Microsoft docs"  
[Webview2ReferenceWin3209488Experimental]: ../reference/win32/0-9-488-reference-webview2.md#experimental "Experimental-Reference (WebView2) | Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

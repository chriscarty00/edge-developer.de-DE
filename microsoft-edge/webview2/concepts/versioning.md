---
description: Für Microsoft Edge-WebView2 verwendete Versions Verwaltungsmodelle
title: Versionsverwaltung von Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 3ce1f0653a14d92571f1365cbfebc8bb2215ecbe
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010677"
---
# <span data-ttu-id="13683-104">Grundlegendes zu WebView2 SDK-Versionen</span><span class="sxs-lookup"><span data-stu-id="13683-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="13683-105">WebView2 hängt von der Funktion von Microsoft Edge ab.</span><span class="sxs-lookup"><span data-stu-id="13683-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="13683-106">Für jedes WebView2-SDK muss mindestens eine Browserversion installiert sein.</span><span class="sxs-lookup"><span data-stu-id="13683-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="13683-107">Die Mindestversion wird in der Paketversion des SDK widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="13683-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="13683-108">Wenn Sie beispielsweise das verwenden `SDK package version 0.9.488` , müssen Sie Microsoft Edge mit einer Buildnummer von 488 oder höher installieren.</span><span class="sxs-lookup"><span data-stu-id="13683-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="13683-109">Die Browserversion ist auch in den WebView2- [Versions][Releasenotes]hinweisen angegeben.</span><span class="sxs-lookup"><span data-stu-id="13683-109">The browser version is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="13683-110">Wenn Sie weitere Informationen zur neuesten Version des Microsoft Edge-Browsers erhalten möchten, navigieren Sie zu [Browser Kanälen][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="13683-110">For more information about the latest release of the Microsoft Edge browser, navigate to [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="13683-111">WebView2 befindet sich derzeit in der Vorschau.</span><span class="sxs-lookup"><span data-stu-id="13683-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="13683-112">Während das WebView-Team versucht, die Abwärtskompatibilität zwischen Browserversionen und SDKs zu gewährleisten, ist dies nicht gewährleistet, da neuere Versionen des Browsers möglicherweise frühere SDK-Versionen nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="13683-112">While the WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed because newer versions of the browser may not support previous SDK versions.</span></span>  <span data-ttu-id="13683-113">Wenn sich zwischen Browserversionen und SDKs Unterbrechungen ändern, werden die Änderungen in den [Versions][Releasenotes]hinweisen angegeben.</span><span class="sxs-lookup"><span data-stu-id="13683-113">If there are breaking changes between browser versions and SDKs, the changes are specified in the [Release Notes][Releasenotes].</span></span>  

<span data-ttu-id="13683-114">In Zukunft plant das WebView-Team, das Verteilungsmodell für WebView2-apps zu ändern.</span><span class="sxs-lookup"><span data-stu-id="13683-114">In the future, the WebView team plans to change the distribution model for WebView2 apps.</span></span>  <span data-ttu-id="13683-115">Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [Evergreen-Verteilungsmodus][DistributionEvergreenMode].</span><span class="sxs-lookup"><span data-stu-id="13683-115">For more information, navigate to [Evergreen distribution mode][DistributionEvergreenMode].</span></span>  

## <span data-ttu-id="13683-116">Release-und Vorabversion-Paket</span><span class="sxs-lookup"><span data-stu-id="13683-116">Release and prerelease package</span></span>  

<span data-ttu-id="13683-117">In Preview enthält das Release-Paket Folgendes.</span><span class="sxs-lookup"><span data-stu-id="13683-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="13683-118">[Win32 C/C++-APIs][ReferenceWin3209622]: APIs im SDK, die bei GA unverändert bleiben sollen.</span><span class="sxs-lookup"><span data-stu-id="13683-118">[Win32 C/C++ APIs][ReferenceWin3209622]: APIs in the SDK that are expected to remain the same at GA.</span></span>  

<span data-ttu-id="13683-119">In Preview enthält das Vorabversion-Paket die folgenden Komponenten.</span><span class="sxs-lookup"><span data-stu-id="13683-119">In preview, the prerelease package contains the following components.</span></span>  

*   <span data-ttu-id="13683-120">.NET-APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]und [Core][ReferenceDotnet09628]</span><span class="sxs-lookup"><span data-stu-id="13683-120">.NET APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515], and [Core][ReferenceDotnet09628]</span></span>  
*   <span data-ttu-id="13683-121">Experimentelle APIs.</span><span class="sxs-lookup"><span data-stu-id="13683-121">Experimental APIs.</span></span>  <span data-ttu-id="13683-122">Weitere Informationen finden Sie im Abschnitt [experimentelle APIs](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="13683-122">For more information, see the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="13683-123">Experimentelle APIs</span><span class="sxs-lookup"><span data-stu-id="13683-123">Experimental APIs</span></span>  

<span data-ttu-id="13683-124">Das WebView-Team testet experimentelle APIs, die möglicherweise zukünftige Funktionen darstellen.</span><span class="sxs-lookup"><span data-stu-id="13683-124">The WebView team is testing experimental APIs that may represent future functionality.</span></span>  <span data-ttu-id="13683-125">Die experimentellen APIs sind wie `experimental` im SDK markiert.</span><span class="sxs-lookup"><span data-stu-id="13683-125">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="13683-126">Experimentelle APIs können als vollständig stabile APIs im Release-Paket ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="13683-126">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="13683-127">Sie sollten davon ausgehen, dass alle experimentellen APIs vor der Veröffentlichung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="13683-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="13683-128">Bitte bewerten Sie die experimentellen APIs und geben Sie Feedback über das [WebView Feedback Repo][GithubMicrosoftedgeWebviewfeedback]frei.</span><span class="sxs-lookup"><span data-stu-id="13683-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="13683-129">Vermeiden Sie die Verwendung der experimentellen APIs in Produktions-apps.</span><span class="sxs-lookup"><span data-stu-id="13683-129">Avoid using the experimental APIs in production apps.</span></span>  

## <span data-ttu-id="13683-130">Übereinstimmende WebView2-Laufzeitversionen</span><span class="sxs-lookup"><span data-stu-id="13683-130">Matching WebView2 Runtime versions</span></span>  

<span data-ttu-id="13683-131">Wenn Sie eine WebView2-App mit einer bestimmten SDK-Version schreiben, kann Ihre APP von den Benutzern für Sie mit verschiedenen kompatiblen Versionen der WebView2-Laufzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="13683-131">When writing a WebView2 app using a particular SDK version, the users fo you app may run your it with various compatible versions of the WebView2 Runtime.</span></span>  <span data-ttu-id="13683-132">In Zukunft enthält eine neuere kompatible WebView2-Laufzeitversion alle nicht experimentellen APIs einer älteren kompatiblen WebView2-Laufzeitversion sowie zusätzliche neue nicht-experimentelle APIs.</span><span class="sxs-lookup"><span data-stu-id="13683-132">In the future, a newer compatible WebView2 Runtime version contains all the non-experimental APIs from an older compatible WebView2 Runtime version plus additional new non-experimental APIs.</span></span>  

*   <span data-ttu-id="13683-133">**Win32 C/C++** -Entwickler sollten bei der Verwendung `QueryInterface` zum Abrufen einer neuen Schnittstellenach einem Rückgabewert von überprüfen, der `E_NOINTERFACE` möglicherweise darauf hinweist, dass die WebView2-Laufzeit älter ist und diese bestimmte Schnittstelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="13683-133">**Win32 C/C++** developers, when using `QueryInterface` to obtain a new interface, should check for a return value of `E_NOINTERFACE`, which may indicate that the WebView2 Runtime is older and does not support that particular interface.</span></span>  
*   <span data-ttu-id="13683-134">**.Net-und WinUI-** Entwickler sollten auf eine Ausnahme überprüfen, `No such interface supported` Wenn Sie Methoden, Eigenschaften und Ereignisse verwenden, die in späteren SDKs hinzugefügt wurden, die möglicherweise auftreten, wenn die WebView2-Laufzeit älter ist und diese speziellen APIs nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="13683-134">**.NET and WinUI** developers should check for a `No such interface supported` exception when using methods, properties, and events added in later SDKs which may occur when the WebView2 Runtime is older and does not support those particular APIs.</span></span>  

<span data-ttu-id="13683-135">Wenn eine API nicht zur Verfügung steht, sollten Sie das zugeordnete Feature nach Möglichkeit deaktivieren oder den Endbenutzer anderweitig darüber informieren, dass Sie die WebView2-Laufzeitversion aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="13683-135">If an API is unavailable, consider disabling the associated feature, if possible, or otherwise informing the end user they need to update their WebView2 Runtime version.</span></span>  

<span data-ttu-id="13683-136">Experimentelle APIs werden möglicherweise eingeführt, geändert und aus SDK in SDK entfernt.</span><span class="sxs-lookup"><span data-stu-id="13683-136">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="13683-137">Wenn Sie versuchen, eine experimentelle API zu verwenden, die in der WebView2-Laufzeit nicht zur Verfügung steht, können Sie dasselbe zuvor beschriebene Verhalten beobachten.</span><span class="sxs-lookup"><span data-stu-id="13683-137">When attempting to use an experimental API that is not available in the WebView2 Runtime you may observe the same previously described behavior.</span></span>  

## <span data-ttu-id="13683-138">Roadmap</span><span class="sxs-lookup"><span data-stu-id="13683-138">Roadmap</span></span>  

<span data-ttu-id="13683-139">Nachdem WebView2 einen stabilen allgemeinen verfügbaren Zustand erreicht hat, enthält das Release-Paket alle stabilen, unterstützten Win32 C/C++-und .NET-APIs.</span><span class="sxs-lookup"><span data-stu-id="13683-139">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="13683-140">Das Vorabversion-Paket enthält experimentelle APIs, die sich aufgrund Ihres Feedbacks und der geteilten Einblicke ändern können.</span><span class="sxs-lookup"><span data-stu-id="13683-140">The prerelease package contains experimental APIs that are subject to change based upon your feedback and shared insights.</span></span>  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Evergreen-Verteilungsmodus – Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[ReferenceDotnet09628]: ../reference/dotnet/0-9-628-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWin3209622]: ../reference/win32/0-9-622-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[Releasenotes]: ../releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

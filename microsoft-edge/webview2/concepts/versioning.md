---
description: Für Microsoft Edge-WebView2 verwendete Versions Verwaltungsmodelle
title: Versionsverwaltung von Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 54d62de00a89a3c433fd77e9ec20945adbfc19c3
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "11191610"
---
# <span data-ttu-id="7538e-104">Grundlegendes zu WebView2 SDK-Versionen</span><span class="sxs-lookup"><span data-stu-id="7538e-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="7538e-105">Neue Versionen des WebView2-SDK werden mit der gleichen allgemeinen Kadenz wie der Microsoft Edge \ (Chrom \)-Browser ausgeliefert, der ungefähr alle sechs Wochen beträgt.</span><span class="sxs-lookup"><span data-stu-id="7538e-105">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

## <span data-ttu-id="7538e-106">Release-und Vorabversion-Paket</span><span class="sxs-lookup"><span data-stu-id="7538e-106">Release and prerelease package</span></span>  

<span data-ttu-id="7538e-107">Das WebView2-NuGet-Paket enthält sowohl ein Release-als auch ein Pre-Release-Paket.</span><span class="sxs-lookup"><span data-stu-id="7538e-107">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="7538e-108">Das **Release-Paket** ist Forward-kompatibel und enthält die folgenden Komponenten.</span><span class="sxs-lookup"><span data-stu-id="7538e-108">The **release package** is forward compatible and contains the following components.</span></span>  

*   [<span data-ttu-id="7538e-109">Win32 C/C++-APIs</span><span class="sxs-lookup"><span data-stu-id="7538e-109">Win32 C/C++ APIs</span></span>][ReferenceWin32]
*   <span data-ttu-id="7538e-110">.NET-APIs:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]und [Core][DotnetMicrosoftWebWebview2CoreNamespace].</span><span class="sxs-lookup"><span data-stu-id="7538e-110">.NET APIs:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace].</span></span>  
    
<span data-ttu-id="7538e-111">APIs im SDK werden vollständig unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7538e-111">APIs in the SDK are fully supported.</span></span>  

<span data-ttu-id="7538e-112">Das vorab **Version-Paket** ist ein Superset des Release-Pakets mit [experimentellen APIs](#experimental-apis).</span><span class="sxs-lookup"><span data-stu-id="7538e-112">The **prerelease package** is a superset of the release package with [Experimental APIs](#experimental-apis).</span></span>  

### <span data-ttu-id="7538e-113">Roadmap</span><span class="sxs-lookup"><span data-stu-id="7538e-113">Roadmap</span></span>  

<span data-ttu-id="7538e-114">Das Release-Paket enthält alle stabilen, unterstützten Win32 C/C++-und .NET-APIs.</span><span class="sxs-lookup"><span data-stu-id="7538e-114">The release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="7538e-115">Das Vorabversion-Paket enthält experimentelle APIs, die aufgrund Ihres Feedbacks geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="7538e-115">The prerelease package contains experimental APIs that are subject to change based on your feedback.</span></span>  

## <span data-ttu-id="7538e-116">Experimentelle APIs</span><span class="sxs-lookup"><span data-stu-id="7538e-116">Experimental APIs</span></span>  

<span data-ttu-id="7538e-117">Das WebView-Team sucht Feedback zu experimentellen APIs, die in zukünftigen Versionen enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="7538e-117">The WebView team is seeking feedback on experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="7538e-118">Die experimentellen APIs sind wie `experimental` im SDK markiert.</span><span class="sxs-lookup"><span data-stu-id="7538e-118">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="7538e-119">Navigieren Sie zum [WebView-Feedback-Repo][GithubMicrosoftedgeWebviewfeedback], um Ihnen zu helfen, die experimentellen APIs zu evaluieren und Ihr Feedback zu teilen.</span><span class="sxs-lookup"><span data-stu-id="7538e-119">To help you evaluate the Experimental APIs and share your feedback, navigate to the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="7538e-120">Experimentelle APIs werden möglicherweise eingeführt, geändert und aus SDK in SDK entfernt.</span><span class="sxs-lookup"><span data-stu-id="7538e-120">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="7538e-121">Vermeiden Sie die Verwendung der experimentellen APIs in Produktions-apps.</span><span class="sxs-lookup"><span data-stu-id="7538e-121">Avoid using the experimental APIs in production apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="7538e-122">Experimental-APIs sind möglicherweise in Ihrer installierten Version der WebView2-Laufzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7538e-122">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="7538e-123">Übereinstimmende WebView2-Laufzeitversionen</span><span class="sxs-lookup"><span data-stu-id="7538e-123">Matching WebView2 Runtime versions</span></span>  
<span data-ttu-id="7538e-124">WebView2-apps erfordern, dass Benutzer eine [WebView2-Laufzeit][MicrosoftDeveloperEdgeWebview2]installieren.</span><span class="sxs-lookup"><span data-stu-id="7538e-124">WebView2 apps require users to install a [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2].</span></span>  <span data-ttu-id="7538e-125">Die WebView2-Laufzeit wird automatisch auf die neueste verfügbare Version aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7538e-125">The WebView2 Runtime automatically updates to the latest version available.</span></span>  <span data-ttu-id="7538e-126">In einigen Szenarien möchten Benutzer möglicherweise automatische WebView2-Laufzeitupdates beenden, was zu Problemen bei der APP-Kompatibilität führen kann.</span><span class="sxs-lookup"><span data-stu-id="7538e-126">In some scenarios, users may want to stop automatic WebView2 Runtime updates, which may cause app compatibility issues.</span></span>  

<span data-ttu-id="7538e-127">Wenn WebView2-Laufzeitupdates angehalten werden, stellen Sie sicher, dass Sie die Mindestversion der [WebView2-Laufzeit][MicrosoftDeveloperEdgeWebview2] verstehen, die für Ihre APP erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7538e-127">If WebView2 Runtime updates are stopped, ensure you understand the minimum version of the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] required by your app.</span></span>  <span data-ttu-id="7538e-128">Sehen Sie sich die folgenden zwei Elemente an:</span><span class="sxs-lookup"><span data-stu-id="7538e-128">Consider the following two items:</span></span>  

1.  <span data-ttu-id="7538e-129">Die erforderliche Mindestversion des SDK, die in [den WebView2-Versions][Webview2Releasenotes] Hinweisen unter **minimaler WebView2-Laufzeitversion**enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7538e-129">The minimum required version of the SDK, in found in the WebView2 [Release Notes][Webview2Releasenotes] under **minimum WebView2 Runtime version**.</span></span>  <span data-ttu-id="7538e-130">Für SDK-Version [1.0.622.22][Webview2Releasenotes1062222]müssen Sie beispielsweise entweder die WebView2- [Laufzeit][MicrosoftDeveloperEdgeWebview2] oder einen [nicht stabilen Microsoft Edge-Kanal][MicrosoftedgeinsiderDownload] mit einer Buildnummer von `86.0.616.0` oder höher installieren.</span><span class="sxs-lookup"><span data-stu-id="7538e-130">For example, for SDK version [1.0.622.22][Webview2Releasenotes1062222], you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of `86.0.616.0` or later.</span></span>  <span data-ttu-id="7538e-131">Die Mindestversion, die vom SDK benötigt wird, ändert sich nur, wenn eine unterbrechende Änderung in der Web-Plattform auftritt.</span><span class="sxs-lookup"><span data-stu-id="7538e-131">The minimum version required by the SDK only changes when a breaking change occurs in the web platform.</span></span>  
1.  <span data-ttu-id="7538e-132">Die erforderliche Mindestversion des NuGet-Pakets zur Unterstützung der Schnittstellen und APIs, die Sie in Ihrer APP verwenden.</span><span class="sxs-lookup"><span data-stu-id="7538e-132">The minimum required version of the NuGet package required to support the interfaces and APIs that you use in your app.</span></span>  <span data-ttu-id="7538e-133">Neue Schnittstellen und APIs werden in regelmäßigen Abständen zu WebView2 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7538e-133">New interfaces and APIs are added periodically to WebView2.</span></span>  <span data-ttu-id="7538e-134">APIs und Schnittstellen, die in einem SDK gebündelt sind, erfordern unterschiedliche Versionen der WebView2-Laufzeit, da APIs und Schnittstellen dem SDK zu unterschiedlichen Zeitpunkten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7538e-134">APIs and interfaces bundled in an SDK require different versions of the WebView2 Runtime, because APIs and interface are added to the SDK at different times.</span></span>  <span data-ttu-id="7538e-135">Die erforderliche WebView2-Laufzeitversion entspricht der Buildnummer, der dritten Nummer, der SDK-Version, in der die API erstmals eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="7538e-135">The required WebView2 Runtime version matches the build number, the third number, of the SDK version the API was first introduced in.</span></span>  <span data-ttu-id="7538e-136">Beispielsweise erfordert eine neue API oder Schnittstelle, die in SDK-Version [1.0.622.22][Webview2Releasenotes1062222] hinzugefügt wurde, die WebView2-Laufzeitversion:  `86.0.622.0`  eine API oder Schnittstelle, die in einer späteren SDK-Version hinzugefügt wurde, erfordert die WebView2-Runtime mit der gleichen Versionsnummer wie das SDK.</span><span class="sxs-lookup"><span data-stu-id="7538e-136">For example, a new API or interface added in SDK version [1.0.622.22][Webview2Releasenotes1062222] requires the WebView2 Runtime version:  `86.0.622.0`  An API or interface added in a later SDK release requires the WebView2 Runtime that has the same version number as the SDK.</span></span>  <span data-ttu-id="7538e-137">Wenn Sie feststellen möchten, ob die WebView2-Laufzeitversion eine Schnittstelle oder API unterstützt, navigieren Sie zu [Ermitteln der WebView2-Lauf Zeitanforderung](#determine-webview2-runtime-requirement).</span><span class="sxs-lookup"><span data-stu-id="7538e-137">To help you determine if the WebView2 Runtime version supports an interface or API, navigate to [Determine WebView2 Runtime requirement](#determine-webview2-runtime-requirement).</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="7538e-138">Bei der Entwicklung von [immergrünen WebView2-apps][Webview2ConceptsDistributionEvergreenDistributionMode]testen Sie Ihre APP regelmäßig mit den neuesten Versionen der WebView2-Runtime und den nicht stabilen Microsoft Edge-Browsern.</span><span class="sxs-lookup"><span data-stu-id="7538e-138">When developing [Evergreen WebView2 apps][Webview2ConceptsDistributionEvergreenDistributionMode], regularly test your app against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="7538e-139">Da sich die Webplattform ständig weiterentwickelt, ist das regelmäßige testen die beste Methode, um sicherzustellen, dass Ihre APP wie beabsichtigt funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7538e-139">Because the web platform is constantly evolving, regular testing is the best way to ensure your app performs as intended.</span></span>  

### <span data-ttu-id="7538e-140">Ermitteln der WebView2-Lauf Zeitanforderung</span><span class="sxs-lookup"><span data-stu-id="7538e-140">Determine WebView2 Runtime requirement</span></span>  

<span data-ttu-id="7538e-141">Je nachdem, welches SDK Sie verwenden, sollten Sie die folgenden Elemente in Frage stellen:</span><span class="sxs-lookup"><span data-stu-id="7538e-141">Depending on which SDK you use, consider the following items:</span></span>  

*   <span data-ttu-id="7538e-142">**Win32 C/C++**.</span><span class="sxs-lookup"><span data-stu-id="7538e-142">**Win32 C/C++**.</span></span>  <span data-ttu-id="7538e-143">`QueryInterface`Überprüfen Sie bei der Verwendung zum Abrufen einer neuen Schnittstelle den Rückgabewert von `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="7538e-143">When using `QueryInterface` to obtain a new interface, verify a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="7538e-144">Der Wert kann darauf hindeuten, dass die WebView2-Laufzeit eine frühere Version ist und diese Schnittstelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7538e-144">The value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span>  <span data-ttu-id="7538e-145">Wenn Sie ein Beispiel für die Funktionsweise haben, navigieren Sie zu [Zeile 622-AppWindow. cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].</span><span class="sxs-lookup"><span data-stu-id="7538e-145">For an example of how it works, navigate to [Line 622 - AppWindow.cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].</span></span>  
*   <span data-ttu-id="7538e-146">**.Net und WinUI**.</span><span class="sxs-lookup"><span data-stu-id="7538e-146">**.NET and WinUI**.</span></span>  <span data-ttu-id="7538e-147">Überprüfen Sie auf eine `No such interface supported` Ausnahme, wenn Sie Methoden, Eigenschaften und Ereignisse verwenden, die neueren SDKs hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="7538e-147">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="7538e-148">Die Ausnahme kann auftreten, wenn die WebView2-Laufzeit eine frühere Version ist und die APIs nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7538e-148">The exception may occur when the WebView2 Runtime is a previous version, and does not support the APIs.</span></span>  
    
<span data-ttu-id="7538e-149">Wenn eine API nicht zur Verfügung steht, sollten Sie das zugehörige Feature entfernen oder Ihre Benutzer informieren, dass eine Aktualisierung der WebView2-Laufzeit erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7538e-149">If an API is unavailable, consider removing the associated feature, or inform your users that an update to the WebView2 Runtime is required.</span></span>  

<!--
## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  
1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  
    -->  

<!--links -->  

[Webview2ConceptsDistributionEvergreenDistributionMode]: ./distribution.md#evergreen-distribution-mode "Immergrüner Verteilungsmodus – Verteilung von apps mithilfe von WebView2 | Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  
[Webview2Releasenotes1062222]: ../releasenotes.md#1062222 "1.0.622.22 – Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"   

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft docs"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Microsoft. Web. WebView2. Core-Namespace | Microsoft docs"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Microsoft. Web. WebView2. WPF-Namespace | Microsoft docs"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft. Web. WebView2. WinForms-Namespace | Microsoft docs"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++-Referenz | Microsoft docs"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge-WebView2 | Microsoft-Entwickler"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622]: https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622 "Zeile 622-AppWindow. cpp-MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

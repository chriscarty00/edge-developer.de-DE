---
description: Für Microsoft Edge-WebView2 verwendete Versions Verwaltungsmodelle
title: Versionsverwaltung von Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a47c7295e87cf4295f8cdf898b62aa3b550aa9a5
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120339"
---
# <span data-ttu-id="4b1e4-104">Grundlegendes zu WebView2 SDK-Versionen</span><span class="sxs-lookup"><span data-stu-id="4b1e4-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="4b1e4-105">Zum Entwickeln einer WebView2-Anwendung müssen Sie entweder die [WebView2-Laufzeit][MicrosoftDeveloperEdgeWebview2] oder einen [nicht stabilen Microsoft Edge-Kanal][MicrosoftedgeinsiderDownload]installieren.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-105">To develop a WebView2 application, you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload].</span></span>  <span data-ttu-id="4b1e4-106">Die Mindestversion, die erforderlich ist, ist in der NuGet-Paketversion des SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-106">The minimum version that's required is included in the NuGet package version of the SDK.</span></span>  <span data-ttu-id="4b1e4-107">Wenn Sie beispielsweise das verwenden `SDK package version 0.9.488` , müssen Sie entweder die [WebView2-Laufzeit][MicrosoftDeveloperEdgeWebview2] oder einen [nicht stabilen Microsoft Edge-Kanal][MicrosoftedgeinsiderDownload] mit einer Buildnummer von 488 oder höher installieren.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-107">For example, if you use the `SDK package version 0.9.488`, then you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of 488 or later.</span></span>  <span data-ttu-id="4b1e4-108">Die erforderliche Mindestversion ist auch in den WebView2- [Versions][Releasenotes]hinweisen angegeben.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-108">The minimum version required is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="4b1e4-109">Neue Versionen des WebView2-SDK werden mit der gleichen allgemeinen Kadenz wie der Microsoft Edge \ (Chrom \)-Browser ausgeliefert, der ungefähr alle sechs Wochen beträgt.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-109">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="4b1e4-110">Bei der Entwicklung von Evergreen WebView2-Anwendungen testen Sie Ihre Anwendung regelmäßig auf die neuesten Versionen der WebView2-Runtime und der nicht stabilen Microsoft Edge-Browser.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-110">When developing Evergreen WebView2 applications, regularly test your application against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="4b1e4-111">Da sich die Webplattform ständig weiterentwickelt, ist das regelmäßige testen die beste Methode, um sicherzustellen, dass Ihre Anwendung wie beabsichtigt funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-111">Because the web platform is constantly evolving, regular testing is the best way to ensure your application performs as intended.</span></span>  

## <span data-ttu-id="4b1e4-112">Release-und Vorabversion-Paket</span><span class="sxs-lookup"><span data-stu-id="4b1e4-112">Release and prerelease package</span></span>  

<span data-ttu-id="4b1e4-113">Das WebView2-NuGet-Paket enthält sowohl ein Release-als auch ein Pre-Release-Paket.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-113">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="4b1e4-114">Das Release-Paket ist Forward-kompatibel und enthält die [Win32 C/C++-APIs][ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="4b1e4-114">The release package is forward compatible and contains the [Win32 C/C++ APIs][ReferenceWin32].</span></span>  <span data-ttu-id="4b1e4-115">APIs in diesem SDK werden vollständig unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-115">APIs in this SDK are fully supported.</span></span>  

<span data-ttu-id="4b1e4-116">Das Vorabversion-Paket ist eine Obermenge des Release-Pakets mit den nachfolgend aufgeführten zusätzlichen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-116">The prerelease package is a superset of the release package with the additional components listed below.</span></span>  

*   <span data-ttu-id="4b1e4-117">.NET-APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]und [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span><span class="sxs-lookup"><span data-stu-id="4b1e4-117">.NET APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span></span>  
*   <span data-ttu-id="4b1e4-118">Experimentelle APIs: Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zum Abschnitt [experimentelle APIs](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="4b1e4-118">Experimental APIs:  For more information, navigate to the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="4b1e4-119">Experimentelle APIs</span><span class="sxs-lookup"><span data-stu-id="4b1e4-119">Experimental APIs</span></span>  

<span data-ttu-id="4b1e4-120">Das WebView-Team testet experimentelle APIs, die in zukünftigen Versionen enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-120">The WebView team is testing experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="4b1e4-121">Die experimentellen APIs sind wie `experimental` im SDK markiert.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-121">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="4b1e4-122">Experimentelle APIs können als vollständig stabile APIs im Release-Paket ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-122">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="4b1e4-123">Sie können die experimentellen APIs auswerten und Feedback über das [WebView Feedback Repo][GithubMicrosoftedgeWebviewfeedback]freigeben.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-123">You can evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="4b1e4-124">Vermeiden Sie die Verwendung der experimentellen APIs in Produktions-apps.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-124">Avoid using the experimental APIs in production apps.</span></span>  

## <span data-ttu-id="4b1e4-125">Übereinstimmende WebView2-Laufzeitversionen</span><span class="sxs-lookup"><span data-stu-id="4b1e4-125">Matching WebView2 Runtime versions</span></span>  

<span data-ttu-id="4b1e4-126">Wenn Sie eine WebView2-App mit einer bestimmten SDK-Version schreiben, können Benutzer Ihrer APP Sie mit mehreren kompatiblen Versionen der WebView2-Laufzeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-126">When writing a WebView2 app using a particular SDK version, users of your app may run it with several compatible versions of the WebView2 Runtime.</span></span>  <span data-ttu-id="4b1e4-127">Das WebView-Team arbeitet an einer kompatiblen WebView2-Laufzeitversion, die nicht-experimentelle APIs aus früheren Versionen der Common Language Runtime und neuen nicht experimentellen APIs enthält.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-127">The WebView team is working on a compatible WebView2 Runtime version that contains non-experimental APIs from previous versions of the Runtime and new non-experimental APIs.</span></span>  

<span data-ttu-id="4b1e4-128">Je nachdem, welches SDK Sie verwenden, sollten Sie die folgenden Elemente in Frage stellen:</span><span class="sxs-lookup"><span data-stu-id="4b1e4-128">Depending on which SDK you use, consider the following items:</span></span> 

*   <span data-ttu-id="4b1e4-129">**Win32 C/C++**.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-129">**Win32 C/C++**.</span></span>  <span data-ttu-id="4b1e4-130">Wenn `QueryInterface` Sie eine neue Schnittstelle abrufen möchten, suchen Sie nach einem Rückgabewert von `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="4b1e4-130">When using `QueryInterface` to obtain a new interface, check for a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="4b1e4-131">Dieser Wert kann darauf hindeuten, dass die WebView2-Laufzeit eine frühere Version ist und diese Schnittstelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-131">This value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span>  
*   <span data-ttu-id="4b1e4-132">**.Net und WinUI**.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-132">**.NET and WinUI**.</span></span>  <span data-ttu-id="4b1e4-133">Überprüfen Sie auf eine `No such interface supported` Ausnahme, wenn Sie Methoden, Eigenschaften und Ereignisse verwenden, die neueren SDKs hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-133">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="4b1e4-134">Diese Ausnahme tritt möglicherweise auf, wenn die WebView2-Laufzeit eine frühere Version ist und diese APIs nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-134">This exception may occur when the WebView2 Runtime is a previous version, and doesn't support those APIs.</span></span>  

<span data-ttu-id="4b1e4-135">Wenn eine API nicht verfügbar ist, können Sie das zugeordnete Feature entfernen oder Ihre Benutzer informieren, dass Sie Ihre Version der WebView2-Laufzeit aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-135">If an API is unavailable, consider removing the associated feature, or inform your users that they need to update their version of the WebView2 Runtime.</span></span>  

<span data-ttu-id="4b1e4-136">Experimentelle APIs werden möglicherweise eingeführt, geändert und aus SDK in SDK entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-136">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="4b1e4-137">Experimental-APIs sind möglicherweise in Ihrer installierten Version der WebView2-Laufzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-137">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="4b1e4-138">Roadmap</span><span class="sxs-lookup"><span data-stu-id="4b1e4-138">Roadmap</span></span>  

<span data-ttu-id="4b1e4-139">Das Release-Paket enthält alle stabilen, unterstützten Win32 C/C++-APIs.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-139">The release package contains all of the stable, supported Win32 C/C++ APIs.</span></span>  <span data-ttu-id="4b1e4-140">In Zukunft enthält das Release-Paket alle stabilen, unterstützten .NET-APIs, wenn diese allgemein verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-140">In the future, the release package will contain all stable, supported .NET APIs when they are made generally available.</span></span>  <span data-ttu-id="4b1e4-141">Das Vorabversion-Paket enthält experimentelle APIs, die sich aufgrund Ihres Feedbacks und der geteilten Einblicke ändern können.</span><span class="sxs-lookup"><span data-stu-id="4b1e4-141">The prerelease package contains experimental APIs that are subject to change based upon your feedback and shared insights.</span></span>  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->  

[Releasenotes]: ../releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft docs"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Microsoft. Web. WebView2. Core-Namespace | Microsoft docs"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Microsoft. Web. WebView2. WPF-Namespace | Microsoft docs"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft. Web. WebView2. WinForms-Namespace | Microsoft docs"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++-Referenz | Microsoft docs"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge-WebView2 | Microsoft-Entwickler"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

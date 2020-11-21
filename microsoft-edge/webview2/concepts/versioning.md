---
description: Für Microsoft Edge-WebView2 verwendete Versions Verwaltungsmodelle
title: Versionsverwaltung von Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/18/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 132ccab0f9f378eedd8c83a7404c350161556f2e
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182395"
---
# <span data-ttu-id="cada4-104">Grundlegendes zu WebView2 SDK-Versionen</span><span class="sxs-lookup"><span data-stu-id="cada4-104">Understand WebView2 SDK versions</span></span>

<span data-ttu-id="cada4-105">Neue Versionen des WebView2-SDK werden mit der gleichen allgemeinen Kadenz wie der Microsoft Edge \ (Chrom \)-Browser ausgeliefert, der ungefähr alle sechs Wochen beträgt.</span><span class="sxs-lookup"><span data-stu-id="cada4-105">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

## <span data-ttu-id="cada4-106">Release-und Vorabversion-Paket</span><span class="sxs-lookup"><span data-stu-id="cada4-106">Release and prerelease package</span></span>  

<span data-ttu-id="cada4-107">Das WebView2-NuGet-Paket enthält sowohl ein Release-als auch ein Pre-Release-Paket.</span><span class="sxs-lookup"><span data-stu-id="cada4-107">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="cada4-108">Das Release-Paket ist Forward-kompatibel und enthält die [Win32 C/C++-APIs][ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="cada4-108">The release package is forward compatible and contains the [Win32 C/C++ APIs][ReferenceWin32].</span></span>  <span data-ttu-id="cada4-109">APIs in diesem SDK werden vollständig unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cada4-109">APIs in this SDK are fully supported.</span></span>  

<span data-ttu-id="cada4-110">Das Vorabversion-Paket ist eine Obermenge des Release-Pakets mit den nachfolgend aufgeführten zusätzlichen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="cada4-110">The prerelease package is a superset of the release package with the additional components listed below.</span></span>  

*   <span data-ttu-id="cada4-111">.NET-APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]und [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span><span class="sxs-lookup"><span data-stu-id="cada4-111">.NET APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span></span>  
*   <span data-ttu-id="cada4-112">Experimentelle APIs: Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zum Abschnitt [experimentelle APIs](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="cada4-112">Experimental APIs:  For more information, navigate to the [Experimental APIs](#experimental-apis) section.</span></span>  

### <span data-ttu-id="cada4-113">Roadmap</span><span class="sxs-lookup"><span data-stu-id="cada4-113">Roadmap</span></span>  

<span data-ttu-id="cada4-114">Das Release-Paket enthält alle stabilen, unterstützten Win32 C/C++-APIs.</span><span class="sxs-lookup"><span data-stu-id="cada4-114">The release package contains all of the stable, supported Win32 C/C++ APIs.</span></span>  <span data-ttu-id="cada4-115">In Zukunft enthält das Release-Paket alle stabilen, unterstützten .NET-APIs, wenn diese allgemein verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cada4-115">In the future, the release package will contain all stable, supported .NET APIs when they're made generally available.</span></span>  <span data-ttu-id="cada4-116">Das Vorabversion-Paket enthält experimentelle APIs, die aufgrund Ihres Feedbacks geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="cada4-116">The prerelease package contains experimental APIs that are subject to change based on your feedback.</span></span> 

## <span data-ttu-id="cada4-117">Experimentelle APIs</span><span class="sxs-lookup"><span data-stu-id="cada4-117">Experimental APIs</span></span>  

<span data-ttu-id="cada4-118">Das WebView-Team sucht Feedback zu experimentellen APIs, die in zukünftigen Versionen enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="cada4-118">The WebView team is seeking feedback on experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="cada4-119">Die experimentellen APIs sind wie `experimental` im SDK markiert.</span><span class="sxs-lookup"><span data-stu-id="cada4-119">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="cada4-120">Sie können die experimentellen APIs auswerten und Feedback über das [WebView Feedback Repo][GithubMicrosoftedgeWebviewfeedback]freigeben.</span><span class="sxs-lookup"><span data-stu-id="cada4-120">You can evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="cada4-121">Experimentelle APIs werden möglicherweise eingeführt, geändert und aus SDK in SDK entfernt.</span><span class="sxs-lookup"><span data-stu-id="cada4-121">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="cada4-122">Vermeiden Sie die Verwendung der experimentellen APIs in Produktions-apps.</span><span class="sxs-lookup"><span data-stu-id="cada4-122">Avoid using the experimental APIs in production apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="cada4-123">Experimental-APIs sind möglicherweise in Ihrer installierten Version der WebView2-Laufzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cada4-123">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="cada4-124">Übereinstimmende WebView2-Laufzeitversionen</span><span class="sxs-lookup"><span data-stu-id="cada4-124">Matching WebView2 Runtime versions</span></span>  
<span data-ttu-id="cada4-125">WebView2-Anwendungen erfordern, dass Benutzer eine [WebView2-Laufzeit][MicrosoftDeveloperEdgeWebview2]installieren.</span><span class="sxs-lookup"><span data-stu-id="cada4-125">WebView2 applications require users to install a [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2].</span></span> <span data-ttu-id="cada4-126">Die WebView2-Laufzeit wird automatisch auf die neueste verfügbare Version aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cada4-126">The WebView2 Runtime updates automatically to the latest version that's available.</span></span> <span data-ttu-id="cada4-127">In einigen Szenarien müssen die Benutzer möglicherweise automatische WebView2-Laufzeitupdates beenden, was zu Anwendungskompatibilitätsproblemen führen kann.</span><span class="sxs-lookup"><span data-stu-id="cada4-127">In some scenarios, users may need to stop automatic WebView2 Runtime updates, which can cause application compatibility issues.</span></span>

<span data-ttu-id="cada4-128">Wenn WebView2-Laufzeitupdates angehalten werden, stellen Sie sicher, dass Sie die Mindestversion der [WebView2-Laufzeit][MicrosoftDeveloperEdgeWebview2] verstehen, die für Ihre Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cada4-128">If WebView2 Runtime updates are stopped, ensure you understand the minimum version of the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] that's required by your application.</span></span> <span data-ttu-id="cada4-129">Sehen Sie sich die folgenden zwei Elemente an:</span><span class="sxs-lookup"><span data-stu-id="cada4-129">Consider the following two items:</span></span>  

1. <span data-ttu-id="cada4-130">Die erforderliche Mindestversion des SDK, die in [den WebView2-Versions][Releasenotes] Hinweisen unter **minimaler WebView2-Laufzeitversion**zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="cada4-130">The minimum required version of the SDK, which can be found in the WebView2 [Release Notes][Releasenotes] under **minimum WebView2 Runtime version**.</span></span> <span data-ttu-id="cada4-131">Für SDK-Version [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222)müssen Sie beispielsweise entweder die WebView2- [Laufzeit][MicrosoftDeveloperEdgeWebview2] oder einen [nicht stabilen Microsoft Edge-Kanal][MicrosoftedgeinsiderDownload] mit einer Buildnummer von **86.0.616.0** oder höher installieren.</span><span class="sxs-lookup"><span data-stu-id="cada4-131">For example, for SDK version [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222), you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of **86.0.616.0** or later.</span></span> <span data-ttu-id="cada4-132">Die Mindestversion, die vom SDK benötigt wird, ändert sich nur, wenn die Webplattform eine unterbrechende Änderung vorsieht.</span><span class="sxs-lookup"><span data-stu-id="cada4-132">The minimum version required by the SDK will only change when there's a breaking change in the web platform.</span></span>

2. <span data-ttu-id="cada4-133">Die mindestanforderungs Version des NuGet-Pakets, das für die Unterstützung der in der APP verwendeten Schnittstellen und APIs erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cada4-133">The minimum required version of the NuGet package that's required to support the interfaces and APIs used in your app.</span></span> <span data-ttu-id="cada4-134">Neue Schnittstellen und APIs werden in regelmäßigen Abständen zu WebView2 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cada4-134">New interfaces and APIs are added periodically to WebView2.</span></span> <span data-ttu-id="cada4-135">APIs und Schnittstellen, die in einem SDK gebündelt sind, erfordern unterschiedliche Versionen der WebView2-Laufzeit, da Sie zu unterschiedlichen Zeitpunkten dem SDK hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="cada4-135">APIs and interfaces bundled in an SDK will require different versions of the WebView2 Runtime because they were added to the SDK at different times.</span></span>  <span data-ttu-id="cada4-136">Die erforderliche WebView2-Laufzeitversion entspricht der Buildnummer, der dritten Nummer, der SDK-Version, in der die API erstmals eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="cada4-136">The required WebView2 Runtime version matches the build number, the third number, of the SDK version the API was first introduced in.</span></span> <span data-ttu-id="cada4-137">Eine neue API oder Schnittstelle, die in SDK-Version [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222) hinzugefügt wird, benötigt beispielsweise die WebView2-Laufzeitversion: 86,0. **622**. 0.</span><span class="sxs-lookup"><span data-stu-id="cada4-137">For example, a new API or interface added in SDK version [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222) will need the WebView2 Runtime version: 86.0.**622**.0.</span></span> <span data-ttu-id="cada4-138">Für eine API oder Schnittstelle, die in einer nachfolgenden SDK-Version hinzugefügt wurde, ist die WebView2-Laufzeit mit der gleichen Versionsnummer wie das SDK erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cada4-138">An API or interface added in a subsequent SDK release requires the WebView2 Runtime that has the same version number as the SDK.</span></span> <span data-ttu-id="cada4-139">Sie können feststellen, ob die WebView2-Laufzeitversion eine Schnittstelle oder API [programmgesteuert](#determine-webview2-runtime-requirement)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cada4-139">You can determine if the WebView2 Runtime version supports an interface or API [programmatically](#determine-webview2-runtime-requirement).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cada4-140">Bei der Entwicklung von [Evergreen WebView2-Anwendungen](distribution.md#evergreen-distribution-mode)testen Sie Ihre Anwendung regelmäßig auf die neuesten Versionen der WebView2-Runtime und der nicht stabilen Microsoft Edge-Browser.</span><span class="sxs-lookup"><span data-stu-id="cada4-140">When developing [Evergreen WebView2 applications](distribution.md#evergreen-distribution-mode), regularly test your application against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="cada4-141">Da sich die Webplattform ständig weiterentwickelt, ist das regelmäßige testen die beste Methode, um sicherzustellen, dass Ihre Anwendung wie beabsichtigt funktioniert.</span><span class="sxs-lookup"><span data-stu-id="cada4-141">Because the web platform is constantly evolving, regular testing is the best way to ensure your application performs as intended.</span></span>  

### <span data-ttu-id="cada4-142">Ermitteln der WebView2-Lauf Zeitanforderung</span><span class="sxs-lookup"><span data-stu-id="cada4-142">Determine WebView2 Runtime requirement</span></span>

<span data-ttu-id="cada4-143">Je nachdem, welches SDK Sie verwenden, sollten Sie die folgenden Elemente in Frage stellen:</span><span class="sxs-lookup"><span data-stu-id="cada4-143">Depending on which SDK you use, consider the following items:</span></span> 

*   <span data-ttu-id="cada4-144">**Win32 C/C++**.</span><span class="sxs-lookup"><span data-stu-id="cada4-144">**Win32 C/C++**.</span></span>  <span data-ttu-id="cada4-145">Wenn `QueryInterface` Sie eine neue Schnittstelle abrufen möchten, suchen Sie nach einem Rückgabewert von `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="cada4-145">When using `QueryInterface` to obtain a new interface, check for a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="cada4-146">Dieser Wert kann darauf hindeuten, dass die WebView2-Laufzeit eine frühere Version ist und diese Schnittstelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cada4-146">This value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span> <span data-ttu-id="cada4-147">Navigieren Sie zum WebView2API-Beispiel, um ein [Beispiel](https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622) für die Funktionsweise zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="cada4-147">Navigate to the WebView2API Sample for an [example](https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622) of how this works.</span></span>
*   <span data-ttu-id="cada4-148">**.Net und WinUI**.</span><span class="sxs-lookup"><span data-stu-id="cada4-148">**.NET and WinUI**.</span></span>  <span data-ttu-id="cada4-149">Überprüfen Sie auf eine `No such interface supported` Ausnahme, wenn Sie Methoden, Eigenschaften und Ereignisse verwenden, die neueren SDKs hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="cada4-149">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="cada4-150">Diese Ausnahme tritt möglicherweise auf, wenn die WebView2-Laufzeit eine frühere Version ist und diese APIs nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cada4-150">This exception may occur when the WebView2 Runtime is a previous version, and doesn't support those APIs.</span></span>  

<span data-ttu-id="cada4-151">Wenn eine API nicht verfügbar ist, können Sie das zugeordnete Feature entfernen oder Ihre Benutzer informieren, dass Sie Ihre Version der WebView2-Laufzeit aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="cada4-151">If an API is unavailable, consider removing the associated feature, or inform your users that they need to update their version of the WebView2 Runtime.</span></span>  



 

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

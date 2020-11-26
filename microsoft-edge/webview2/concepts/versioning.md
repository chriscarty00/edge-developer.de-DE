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
# Grundlegendes zu WebView2 SDK-Versionen  

Neue Versionen des WebView2-SDK werden mit der gleichen allgemeinen Kadenz wie der Microsoft Edge \ (Chrom \)-Browser ausgeliefert, der ungefähr alle sechs Wochen beträgt.  

## Release-und Vorabversion-Paket  

Das WebView2-NuGet-Paket enthält sowohl ein Release-als auch ein Pre-Release-Paket.  

Das **Release-Paket** ist Forward-kompatibel und enthält die folgenden Komponenten.  

*   [Win32 C/C++-APIs][ReferenceWin32]
*   .NET-APIs:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]und [Core][DotnetMicrosoftWebWebview2CoreNamespace].  
    
APIs im SDK werden vollständig unterstützt.  

Das vorab **Version-Paket** ist ein Superset des Release-Pakets mit [experimentellen APIs](#experimental-apis).  

### Roadmap  

Das Release-Paket enthält alle stabilen, unterstützten Win32 C/C++-und .NET-APIs.  Das Vorabversion-Paket enthält experimentelle APIs, die aufgrund Ihres Feedbacks geändert werden können.  

## Experimentelle APIs  

Das WebView-Team sucht Feedback zu experimentellen APIs, die in zukünftigen Versionen enthalten sein können.  Die experimentellen APIs sind wie `experimental` im SDK markiert.  Navigieren Sie zum [WebView-Feedback-Repo][GithubMicrosoftedgeWebviewfeedback], um Ihnen zu helfen, die experimentellen APIs zu evaluieren und Ihr Feedback zu teilen.  

> [!CAUTION]
> Experimentelle APIs werden möglicherweise eingeführt, geändert und aus SDK in SDK entfernt.  Vermeiden Sie die Verwendung der experimentellen APIs in Produktions-apps.  

> [!NOTE]
> Experimental-APIs sind möglicherweise in Ihrer installierten Version der WebView2-Laufzeit nicht verfügbar.  

## Übereinstimmende WebView2-Laufzeitversionen  
WebView2-apps erfordern, dass Benutzer eine [WebView2-Laufzeit][MicrosoftDeveloperEdgeWebview2]installieren.  Die WebView2-Laufzeit wird automatisch auf die neueste verfügbare Version aktualisiert.  In einigen Szenarien möchten Benutzer möglicherweise automatische WebView2-Laufzeitupdates beenden, was zu Problemen bei der APP-Kompatibilität führen kann.  

Wenn WebView2-Laufzeitupdates angehalten werden, stellen Sie sicher, dass Sie die Mindestversion der [WebView2-Laufzeit][MicrosoftDeveloperEdgeWebview2] verstehen, die für Ihre APP erforderlich ist.  Sehen Sie sich die folgenden zwei Elemente an:  

1.  Die erforderliche Mindestversion des SDK, die in [den WebView2-Versions][Webview2Releasenotes] Hinweisen unter **minimaler WebView2-Laufzeitversion**enthalten ist.  Für SDK-Version [1.0.622.22][Webview2Releasenotes1062222]müssen Sie beispielsweise entweder die WebView2- [Laufzeit][MicrosoftDeveloperEdgeWebview2] oder einen [nicht stabilen Microsoft Edge-Kanal][MicrosoftedgeinsiderDownload] mit einer Buildnummer von `86.0.616.0` oder höher installieren.  Die Mindestversion, die vom SDK benötigt wird, ändert sich nur, wenn eine unterbrechende Änderung in der Web-Plattform auftritt.  
1.  Die erforderliche Mindestversion des NuGet-Pakets zur Unterstützung der Schnittstellen und APIs, die Sie in Ihrer APP verwenden.  Neue Schnittstellen und APIs werden in regelmäßigen Abständen zu WebView2 hinzugefügt.  APIs und Schnittstellen, die in einem SDK gebündelt sind, erfordern unterschiedliche Versionen der WebView2-Laufzeit, da APIs und Schnittstellen dem SDK zu unterschiedlichen Zeitpunkten hinzugefügt werden.  Die erforderliche WebView2-Laufzeitversion entspricht der Buildnummer, der dritten Nummer, der SDK-Version, in der die API erstmals eingeführt wurde.  Beispielsweise erfordert eine neue API oder Schnittstelle, die in SDK-Version [1.0.622.22][Webview2Releasenotes1062222] hinzugefügt wurde, die WebView2-Laufzeitversion:  `86.0.622.0`  eine API oder Schnittstelle, die in einer späteren SDK-Version hinzugefügt wurde, erfordert die WebView2-Runtime mit der gleichen Versionsnummer wie das SDK.  Wenn Sie feststellen möchten, ob die WebView2-Laufzeitversion eine Schnittstelle oder API unterstützt, navigieren Sie zu [Ermitteln der WebView2-Lauf Zeitanforderung](#determine-webview2-runtime-requirement).  
    
> [!IMPORTANT]
> Bei der Entwicklung von [immergrünen WebView2-apps][Webview2ConceptsDistributionEvergreenDistributionMode]testen Sie Ihre APP regelmäßig mit den neuesten Versionen der WebView2-Runtime und den nicht stabilen Microsoft Edge-Browsern.  Da sich die Webplattform ständig weiterentwickelt, ist das regelmäßige testen die beste Methode, um sicherzustellen, dass Ihre APP wie beabsichtigt funktioniert.  

### Ermitteln der WebView2-Lauf Zeitanforderung  

Je nachdem, welches SDK Sie verwenden, sollten Sie die folgenden Elemente in Frage stellen:  

*   **Win32 C/C++**.  `QueryInterface`Überprüfen Sie bei der Verwendung zum Abrufen einer neuen Schnittstelle den Rückgabewert von `E_NOINTERFACE` .  Der Wert kann darauf hindeuten, dass die WebView2-Laufzeit eine frühere Version ist und diese Schnittstelle nicht unterstützt.  Wenn Sie ein Beispiel für die Funktionsweise haben, navigieren Sie zu [Zeile 622-AppWindow. cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].  
*   **.Net und WinUI**.  Überprüfen Sie auf eine `No such interface supported` Ausnahme, wenn Sie Methoden, Eigenschaften und Ereignisse verwenden, die neueren SDKs hinzugefügt wurden.  Die Ausnahme kann auftreten, wenn die WebView2-Laufzeit eine frühere Version ist und die APIs nicht unterstützt.  
    
Wenn eine API nicht zur Verfügung steht, sollten Sie das zugehörige Feature entfernen oder Ihre Benutzer informieren, dass eine Aktualisierung der WebView2-Laufzeit erforderlich ist.  

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

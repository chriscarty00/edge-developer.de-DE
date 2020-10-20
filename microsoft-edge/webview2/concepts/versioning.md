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
# Grundlegendes zu WebView2 SDK-Versionen  

Zum Entwickeln einer WebView2-Anwendung müssen Sie entweder die [WebView2-Laufzeit][MicrosoftDeveloperEdgeWebview2] oder einen [nicht stabilen Microsoft Edge-Kanal][MicrosoftedgeinsiderDownload]installieren.  Die Mindestversion, die erforderlich ist, ist in der NuGet-Paketversion des SDK enthalten.  Wenn Sie beispielsweise das verwenden `SDK package version 0.9.488` , müssen Sie entweder die [WebView2-Laufzeit][MicrosoftDeveloperEdgeWebview2] oder einen [nicht stabilen Microsoft Edge-Kanal][MicrosoftedgeinsiderDownload] mit einer Buildnummer von 488 oder höher installieren.  Die erforderliche Mindestversion ist auch in den WebView2- [Versions][Releasenotes]hinweisen angegeben.  Neue Versionen des WebView2-SDK werden mit der gleichen allgemeinen Kadenz wie der Microsoft Edge \ (Chrom \)-Browser ausgeliefert, der ungefähr alle sechs Wochen beträgt.  

> [!IMPORTANT]
> Bei der Entwicklung von Evergreen WebView2-Anwendungen testen Sie Ihre Anwendung regelmäßig auf die neuesten Versionen der WebView2-Runtime und der nicht stabilen Microsoft Edge-Browser.  Da sich die Webplattform ständig weiterentwickelt, ist das regelmäßige testen die beste Methode, um sicherzustellen, dass Ihre Anwendung wie beabsichtigt funktioniert.  

## Release-und Vorabversion-Paket  

Das WebView2-NuGet-Paket enthält sowohl ein Release-als auch ein Pre-Release-Paket.  

Das Release-Paket ist Forward-kompatibel und enthält die [Win32 C/C++-APIs][ReferenceWin32].  APIs in diesem SDK werden vollständig unterstützt.  

Das Vorabversion-Paket ist eine Obermenge des Release-Pakets mit den nachfolgend aufgeführten zusätzlichen Komponenten.  

*   .NET-APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]und [Core][DotnetMicrosoftWebWebview2CoreNamespace]  
*   Experimentelle APIs: Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zum Abschnitt [experimentelle APIs](#experimental-apis) .  

## Experimentelle APIs  

Das WebView-Team testet experimentelle APIs, die in zukünftigen Versionen enthalten sein können.  Die experimentellen APIs sind wie `experimental` im SDK markiert.  Experimentelle APIs können als vollständig stabile APIs im Release-Paket ausgeliefert werden.  Sie können die experimentellen APIs auswerten und Feedback über das [WebView Feedback Repo][GithubMicrosoftedgeWebviewfeedback]freigeben.  

> [!CAUTION]
> Vermeiden Sie die Verwendung der experimentellen APIs in Produktions-apps.  

## Übereinstimmende WebView2-Laufzeitversionen  

Wenn Sie eine WebView2-App mit einer bestimmten SDK-Version schreiben, können Benutzer Ihrer APP Sie mit mehreren kompatiblen Versionen der WebView2-Laufzeit ausführen.  Das WebView-Team arbeitet an einer kompatiblen WebView2-Laufzeitversion, die nicht-experimentelle APIs aus früheren Versionen der Common Language Runtime und neuen nicht experimentellen APIs enthält.  

Je nachdem, welches SDK Sie verwenden, sollten Sie die folgenden Elemente in Frage stellen: 

*   **Win32 C/C++**.  Wenn `QueryInterface` Sie eine neue Schnittstelle abrufen möchten, suchen Sie nach einem Rückgabewert von `E_NOINTERFACE` .  Dieser Wert kann darauf hindeuten, dass die WebView2-Laufzeit eine frühere Version ist und diese Schnittstelle nicht unterstützt.  
*   **.Net und WinUI**.  Überprüfen Sie auf eine `No such interface supported` Ausnahme, wenn Sie Methoden, Eigenschaften und Ereignisse verwenden, die neueren SDKs hinzugefügt wurden.  Diese Ausnahme tritt möglicherweise auf, wenn die WebView2-Laufzeit eine frühere Version ist und diese APIs nicht unterstützt.  

Wenn eine API nicht verfügbar ist, können Sie das zugeordnete Feature entfernen oder Ihre Benutzer informieren, dass Sie Ihre Version der WebView2-Laufzeit aktualisieren müssen.  

Experimentelle APIs werden möglicherweise eingeführt, geändert und aus SDK in SDK entfernt.  Experimental-APIs sind möglicherweise in Ihrer installierten Version der WebView2-Laufzeit nicht verfügbar.  

## Roadmap  

Das Release-Paket enthält alle stabilen, unterstützten Win32 C/C++-APIs.  In Zukunft enthält das Release-Paket alle stabilen, unterstützten .NET-APIs, wenn diese allgemein verfügbar sind.  Das Vorabversion-Paket enthält experimentelle APIs, die sich aufgrund Ihres Feedbacks und der geteilten Einblicke ändern können.  

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

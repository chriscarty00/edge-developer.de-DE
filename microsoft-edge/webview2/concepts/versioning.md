---
description: Für Microsoft Edge-WebView2 verwendete Versions Verwaltungsmodelle
title: Versionsverwaltung von Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b673a2b250e46959a2eabaeb88cd8535f9a271e4
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2020
ms.locfileid: "11118982"
---
# Grundlegendes zu WebView2 SDK-Versionen  

WebView2 hängt von der Funktion von Microsoft Edge ab.  Für jedes WebView2-SDK muss mindestens eine Browserversion installiert sein.  Die Mindestversion wird in der Paketversion des SDK widergespiegelt.  Wenn Sie beispielsweise das verwenden `SDK package version 0.9.488` , müssen Sie Microsoft Edge mit einer Buildnummer von 488 oder höher installieren.  Die Browserversion ist auch in den WebView2- [Versions][Releasenotes]hinweisen angegeben.  Wenn Sie weitere Informationen zur neuesten Version des Microsoft Edge-Browsers erhalten möchten, navigieren Sie zu [Browser Kanälen][DeployedgeChannels].  

> [!NOTE]
> WebView2 befindet sich derzeit in der Vorschau.  Während das WebView-Team versucht, die Abwärtskompatibilität zwischen Browserversionen und SDKs zu gewährleisten, ist dies nicht gewährleistet, da neuere Versionen des Browsers möglicherweise frühere SDK-Versionen nicht unterstützen.  Wenn sich zwischen Browserversionen und SDKs Unterbrechungen ändern, werden die Änderungen in den [Versions][Releasenotes]hinweisen angegeben.  

In Zukunft plant das WebView-Team, das Verteilungsmodell für WebView2-apps zu ändern.  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [Evergreen-Verteilungsmodus][DistributionEvergreenMode].  

## Release-und Vorabversion-Paket  

In Preview enthält das Release-Paket Folgendes.  

*   [Win32 C/C++-APIs][ReferenceWin32]: APIs im SDK, die bei GA unverändert bleiben sollen.  

In Preview enthält das Vorabversion-Paket die folgenden Komponenten.  

*   .NET-APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]und [Core][DotnetMicrosoftWebWebview2CoreNamespace]  
*   Experimentelle APIs.  Weitere Informationen finden Sie im Abschnitt [experimentelle APIs](#experimental-apis) .  

## Experimentelle APIs  

Das WebView-Team testet experimentelle APIs, die möglicherweise zukünftige Funktionen darstellen.  Die experimentellen APIs sind wie `experimental` im SDK markiert.  Experimentelle APIs können als vollständig stabile APIs im Release-Paket ausgeliefert werden.  Sie sollten davon ausgehen, dass alle experimentellen APIs vor der Veröffentlichung geändert werden.  Bitte bewerten Sie die experimentellen APIs und geben Sie Feedback über das [WebView Feedback Repo][GithubMicrosoftedgeWebviewfeedback]frei.  

> [!CAUTION]
> Vermeiden Sie die Verwendung der experimentellen APIs in Produktions-apps.  

## Übereinstimmende WebView2-Laufzeitversionen  

Wenn Sie eine WebView2-App mit einer bestimmten SDK-Version schreiben, kann Ihre APP von den Benutzern für Sie mit verschiedenen kompatiblen Versionen der WebView2-Laufzeit ausgeführt werden.  In Zukunft enthält eine neuere kompatible WebView2-Laufzeitversion alle nicht experimentellen APIs einer älteren kompatiblen WebView2-Laufzeitversion sowie zusätzliche neue nicht-experimentelle APIs.  

*   **Win32 C/C++** -Entwickler sollten bei der Verwendung `QueryInterface` zum Abrufen einer neuen Schnittstellenach einem Rückgabewert von überprüfen, der `E_NOINTERFACE` möglicherweise darauf hinweist, dass die WebView2-Laufzeit älter ist und diese bestimmte Schnittstelle nicht unterstützt.  
*   **.Net-und WinUI-** Entwickler sollten auf eine Ausnahme überprüfen, `No such interface supported` Wenn Sie Methoden, Eigenschaften und Ereignisse verwenden, die in späteren SDKs hinzugefügt wurden, die möglicherweise auftreten, wenn die WebView2-Laufzeit älter ist und diese speziellen APIs nicht unterstützt.  

Wenn eine API nicht zur Verfügung steht, sollten Sie das zugeordnete Feature nach Möglichkeit deaktivieren oder den Endbenutzer anderweitig darüber informieren, dass Sie die WebView2-Laufzeitversion aktualisieren müssen.  

Experimentelle APIs werden möglicherweise eingeführt, geändert und aus SDK in SDK entfernt.  Wenn Sie versuchen, eine experimentelle API zu verwenden, die in der WebView2-Laufzeit nicht zur Verfügung steht, können Sie dasselbe zuvor beschriebene Verhalten beobachten.  

## Roadmap  

Nachdem WebView2 einen stabilen allgemeinen verfügbaren Zustand erreicht hat, enthält das Release-Paket alle stabilen, unterstützten Win32 C/C++-und .NET-APIs.  Das Vorabversion-Paket enthält experimentelle APIs, die sich aufgrund Ihres Feedbacks und der geteilten Einblicke ändern können.  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Evergreen-Verteilungsmodus – Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Microsoft. Web. WebView2. Core-Namespace | Microsoft docs"
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Microsoft. Web. WebView2. WPF-Namespace | Microsoft docs"
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft. Web. WebView2. WinForms-Namespace | Microsoft docs"
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++-Referenz | Microsoft docs"  
[Releasenotes]: ../releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

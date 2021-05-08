---
description: Versionsmodelle, die für Microsoft Edge WebView2 verwendet werden
title: Verstehen von WebView2 SDK-Versionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, Webview2, Webview, wpf-Apps, Wpf, Microsoft Edge, ICoreWebView2, ICoreWebView2Host, Browsersteuerung, Edge-HTML
ms.openlocfilehash: 18ae2b8feb9310798f78e67cbb767d0642d83d24
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535713"
---
# <a name="understand-webview2-sdk-versions"></a>Verstehen von WebView2 SDK-Versionen  

Neue Versionen des WebView2 SDK werden mit der gleichen allgemeinen Schrittfrequenz wie der Microsoft Edge \(Chromium\)-Browser ausgeliefert, der ungefähr alle sechs Wochen erfolgt.  

## <a name="release-and-prerelease-package"></a>Release- und Vorabversionspaket  

Das WebView2 NuGet-Paket enthält sowohl ein Release- als auch ein Vorabversionspaket.  

Das **Releasepaket** ist vorwärtskompatibel und enthält die folgenden Komponenten.  

*   [Win32 C/C++-APIs][ReferenceWin32]
*   .NET-APIs:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]und [Core][DotnetMicrosoftWebWebview2CoreNamespace].  
    
APIs im SDK werden vollständig unterstützt.  

Das **Vorabversionspaket** ist ein Übersatz des Releasepakets mit [Experimentellen APIs](#experimental-apis).  Vermeiden Sie die Verwendung des Vorab-SDK zum Erstellen von Produktions-Apps.  

### <a name="roadmap"></a>Roadmap  

Das Releasepaket enthält alle stabilen, unterstützten Win32 C/C++- und .NET-APIs.  Das Vorabversionspaket enthält experimentelle APIs, die basierend auf Ihrem Feedback geändert werden können.  

## <a name="experimental-apis"></a>Experimentelle APIs  

Das WebView-Team bittet um Feedback zu experimentellen APIs, die in zukünftigen Versionen enthalten sein können.  Die experimentellen APIs sind als `experimental` im SDK gekennzeichnet.  Navigieren Sie zum [WebView-Feedback-Repository,][GithubMicrosoftedgeWebviewfeedback]um die experimentellen APIs auszuwerten und Ihr Feedback zu teilen.  

> [!CAUTION]
> Experimentelle APIs können vom SDK in SDK eingeführt, geändert und entfernt werden.  Vermeiden Sie die Verwendung der experimentellen APIs in Produktions-Apps.  

> [!NOTE]
> Experimentelle APIs sind möglicherweise nicht in der installierten Version der WebView2-Runtime verfügbar.  

## <a name="matching-webview2-runtime-versions"></a>Übereinstimmende WebView2-Laufzeitversionen  
Für WebView2-Apps müssen Benutzer eine [WebView2-Runtime installieren.][MicrosoftDeveloperEdgeWebview2]  Die WebView2-Laufzeit wird automatisch auf die neueste verfügbare Version aktualisiert.  In einigen Szenarien möchten Benutzer möglicherweise automatische WebView2-Laufzeitupdates beenden, was zu Problemen mit der App-Kompatibilität führen kann.  

Wenn WebView2-Laufzeitupdates beendet werden, stellen Sie sicher, dass Sie die mindestversion der [WebView2-Runtime][MicrosoftDeveloperEdgeWebview2] kennen, die für Ihre App erforderlich ist.  Berücksichtigen Sie die folgenden beiden Elemente:  

1.  Die mindestens erforderliche Version des SDK zum erfolgreichen Laden einer webview2-Instanz finden Sie in den WebView2-Versionshinweisen unter **Minimum Microsoft Edge version to load**. [][Webview2ReleaseNotes]  Die vom SDK erforderliche Mindestversion zum Laden ändert sich nur, wenn eine änderungsbelastende Änderung auf der Webplattform auftritt.  Für SDK Version [1.0.622.22][Webview2ReleaseNotes1062222]müssen Sie beispielsweise entweder die [WebView2-Runtime][MicrosoftDeveloperEdgeWebview2] oder einen nicht stabilen [Microsoft Edge-Kanal][MicrosoftedgeinsiderDownload] mit einer Buildnummer oder neuer `86.0.616.0` installieren.   
1.  Die mindestens erforderliche Version des NuGet, die für die Unterstützung der Schnittstellen und APIs in Ihrer App erforderlich ist, finden Sie in den WebView2-Versionshinweisen unter **Full API Compatibility**. [][Webview2ReleaseNotes]  Neue Schnittstellen und APIs werden regelmäßig zu WebView2 hinzugefügt.  APIs und Schnittstellen, die in einem SDK gebündelt sind, erfordern unterschiedliche Versionen der WebView2-Runtime, da APIs und Schnittstellen zu unterschiedlichen Zeiten dem SDK hinzugefügt werden.  Die erforderliche WebView2-Laufzeitversion entspricht der Buildnummer, der dritten Nummer, der SDK-Version, in der die API erstmals eingeführt wurde.  Beispielsweise erfordert eine neue API oder Schnittstelle, die in SDK Version [1.0.622.22][Webview2ReleaseNotes1062222] hinzugefügt wurde, die WebView2-Laufzeitversion oder `86.0.622.0` eine neuere Version.  Eine API oder Schnittstelle, die in einer späteren SDK-Version hinzugefügt wurde, erfordert eine WebView2-Runtime mit derselben Versionsnummer wie das SDK.  Wenn Sie feststellen möchten, ob die WebView2-Laufzeitversion eine Schnittstelle oder API unterstützt, navigieren Sie zu [Determine WebView2 Runtime requirement](#determine-webview2-runtime-requirement).  
    
> [!IMPORTANT]
> Bei der [Entwicklung von Evergreen WebView2-Apps][Webview2ConceptsDistributionEvergreenDistributionMode]testen Sie Ihre App regelmäßig mit den neuesten Versionen der WebView2-Laufzeit und nicht stabilen Microsoft Edge Kanälen.  Da sich die Webplattform ständig weiterentwickelt, sind regelmäßige Tests die beste Möglichkeit, um sicherzustellen, dass Ihre App wie beabsichtigt funktioniert.  

### <a name="determine-webview2-runtime-requirement"></a>Bestimmen der WebView2-Laufzeitanforderung  

Berücksichtigen Sie in Abhängigkeit von dem verwendeten SDK die folgenden Elemente:  

*   **Win32 C/C++**.  Überprüfen Sie `QueryInterface` beim Abrufen einer neuen Schnittstelle den Rückgabewert von `E_NOINTERFACE` .  Der Wert kann darauf hinweisen, dass die WebView2-Runtime eine frühere Version ist und diese Schnittstelle nicht unterstützt.  Ein Beispiel für die Funktionsweise finden Sie unter [Zeile 622 - AppWindow.cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].  
*   **.NET und WinUI**.  Suchen Sie bei der Verwendung von Methoden, Eigenschaften und Ereignissen, die neueren SDKs hinzugefügt wurden, nach `No such interface supported` einer Ausnahme.  Die Ausnahme kann auftreten, wenn die WebView2-Runtime eine frühere Version ist und die APIs nicht unterstützt.  
    
Wenn eine API nicht verfügbar ist, sollten Sie das zugeordnete Feature entfernen oder Ihre Benutzer darüber informieren, dass ein Update auf die WebView2-Laufzeit erforderlich ist.  

<!--
## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  
1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  
    -->  

<!--links -->  

[Webview2ConceptsDistributionEvergreenDistributionMode]: ./distribution.md#evergreen-distribution-mode "Immergrüner Verteilungsmodus – Verteilung von Apps mithilfe von WebView2 | Microsoft Docs"  
[Webview2ReleaseNotes]: ../release-notes.md "Versionshinweise für WebView2 SDK | Microsoft Docs"  
[Webview2ReleaseNotes1062222]: ../release-notes.md#1062222 "1.0.622.22 – Versionshinweise für WebView2 SDK | Microsoft Docs"   

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft-Dokumentation"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Microsoft.Web.WebView2.Core Namespace | Microsoft Docs"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Microsoft.Web.WebView2.Wpf Namespace | Microsoft Docs"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft.Web.WebView2.WinForms Namespace | Microsoft Docs"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++-Referenz | Microsoft Docs"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2-| Microsoft Developer"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622]: https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622 "Zeile 622 - AppWindow.cpp - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

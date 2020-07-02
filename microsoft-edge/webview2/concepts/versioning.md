---
description: Für Microsoft Edge-WebView2 verwendete Versions Verwaltungsmodelle
title: Versionsverwaltung von Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 059bbeb34f372af0cef944e484599c0b50543cc9
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844425"
---
# Grundlegendes zu WebView2 SDK-Versionen  

WebView2 hängt von der Funktion von Microsoft Edge ab.  Für jedes WebView2-SDK muss mindestens eine Browserversion installiert sein.  Die Mindestversion wird in der Paketversion des SDK widergespiegelt.  Wenn Sie beispielsweise das verwenden `SDK package version 0.9.488` , müssen Sie Microsoft Edge mit einer Buildnummer von 488 oder höher installieren.  Die Browserversion ist auch in den WebView2- [Versions][Releasenotes]hinweisen angegeben.  Weitere Informationen zu den neuesten Versionen des Browsers finden Sie unter [Browser Kanäle][DeployedgeChannels].  

> [!NOTE]
> WebView2 befindet sich derzeit in der Vorschau.  Während das WebView-Team versucht, die Abwärtskompatibilität zwischen Browserversionen und SDKs zu gewährleisten, ist dies nicht gewährleistet, da neuere Versionen des Browsers möglicherweise ältere SDK-Versionen nicht unterstützen.  Wenn sich die Änderungen zwischen Browserversionen und SDKs unterbrechen, gibt das WebView-Team die Änderungen in den [Versions][Releasenotes]hinweisen an.  

In Zukunft plant das WebView-Team, das Verteilungsmodell für WebView2-Anwendungen zu ändern.  Weitere Informationen finden Sie unter Anzeigen des [immergrünen Verteilungsmodus][DistributionEvergreenMode].  
 
## Release-und Pre-Release-Paket  

In Preview enthält das Release-Paket Folgendes.  

*   [Win32 C/C++-APIs][ReferenceWin3209538]: APIs im SDK, die bei GA unverändert bleiben sollen. 

In Preview enthält das Pre-Release-Paket die folgenden Komponenten.  

*   .NET-APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]und [Core][ReferenceDotnet09538]
*   Experimentelle APIs.  Weitere Informationen finden Sie im Abschnitt [experimentelle APIs](#experimental-apis) .  

### Experimentelle APIs  

Das WebView-Team testet APIs, die die zukünftige Funktionalität mit dem Namen experimental-APIs darstellen.  Die experimentellen APIs sind wie `experimental` im SDK markiert.  Einige experimentelle APIs können als vollständig stabile APIs im Release-Paket ausgeliefert werden.  Sie sollten davon ausgehen, dass alle experimentellen APIs vor der Veröffentlichung geändert werden.  Bitte bewerten Sie die experimentellen APIs und geben Sie Feedback über das [WebView Feedback Repo][GithubMicrosoftedgeWebviewfeedback]frei.   

> [!CAUTION]
> Vermeiden Sie es, die experimentellen APIs in Produktionsanwendungen zu verwenden.  

### Roadmap  

Nachdem WebView2 einen stabilen allgemeinen verfügbaren Zustand erreicht hat, enthält das Release-Paket alle stabilen, unterstützten Win32 C/C++-und .NET-APIs.  Das Pre-Release-Paket enthält experimentelle APIs, die basierend auf Entwickler Feedback und geteilten Einblicken geändert werden können.  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Evergreen-Verteilungsmodus – Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[Releasenotes]: ../releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

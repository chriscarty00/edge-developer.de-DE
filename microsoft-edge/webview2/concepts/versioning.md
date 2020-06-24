---
description: Für Microsoft Edge-WebView2 verwendete Versions Verwaltungsmodelle
title: Versionsverwaltung von Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 3862576134d1179fb24b2ce865f705b2bf1db8a6
ms.sourcegitcommit: de171a8e7ccd9f23846f3cd06519e4a0104f1c52
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "10757606"
---
# Grundlegendes zu WebView2 SDK-Versionen  

WebView2 hängt von der Funktion von Microsoft Edge ab. Für jedes WebView2-SDK muss mindestens eine Browserversion installiert sein.  Die Mindestversion wird in der Paketversion des SDK widergespiegelt.  Wenn Sie beispielsweise das verwenden `SDK package version 0.9.488` , müssen Sie Microsoft Edge mit einer Buildnummer von 488 oder höher installieren. Die Browserversion ist auch in den WebView2- [Versions][Webview2Releasenotes]hinweisen angegeben.  Weitere Informationen zu den neuesten Versionen des Browsers finden Sie unter [Browser Kanäle][DeployedgeChannels].  

> [!NOTE]
> WebView2 befindet sich derzeit in der Vorschau.  Das Microsoft Edge-WebView-Team ist zwar bestrebt, die Abwärtskompatibilität zwischen Browserversionen und SDKs zu gewährleisten, es ist jedoch nicht gewährleistet, da einige neuere Versionen des Browsers möglicherweise ältere SDK-Versionen nicht unterstützen.  Wenn es zu Unterbrechungen zwischen Browserversionen und SDKs kommt, gibt das Microsoft Edge-WebView-Team die Änderungen in den [Versions][Webview2Releasenotes]hinweisen an.  

In Zukunft ändert sich das Verteilungsmodell für WebView2-Anwendungen. Weitere Informationen finden Sie unter [WebView2-Laufzeit][Webview2IndexEdgeRuntime].  
 
## Release-und Pre-Release-Paket  

In Preview enthält das Release-Paket Folgendes.  

*   [Win32 C/C++-APIs][Webview2ReferenceWin3209538]: APIs im SDK, die bei GA unverändert bleiben sollen. 

In Preview enthält das Pre-Release-Paket Folgendes.  

*   .NET-APIs: [WPF][Webview2ReferenceWpf09515], [WinForms][Webview2ReferenceWinforms09515]und [Core][Webview2ReferenceDotnet09538]
*   Experimentelle APIs.  Weitere Informationen finden Sie im Abschnitt [Experimantal-APIs](#experimental-apis) .  

### Experimentelle APIs  

Das WebView-Team testet APIs, die die zukünftige Funktionalität mit dem Namen experimental-APIs darstellen.  Die experimentellen APIs sind wie `experimental` im SDK markiert.  Einige experimentelle APIs können als vollständig stabile APIs im Release-Paket ausgeliefert werden.  Sie sollten davon ausgehen, dass alle experimentellen APIs vor der Veröffentlichung geändert werden.  Bitte bewerten Sie die experimentellen APIs und geben Sie Feedback über das [WebView Feedback Repo][GithubMicrosoftedgeWebviewfeedback]frei.   

> [!CAUTION]
> Vermeiden Sie es, die experimentellen APIs in Produktionsanwendungen zu verwenden.  

### Roadmap  

Nachdem WebView2 einen stabilen allgemeinen verfügbaren Zustand erreicht hat, enthält das Release-Paket alle stabilen, unterstützten Win32 C/C++-und .NET-APIs.  Das Pre-Release-Paket enthält experimentelle APIs, die basierend auf Entwickler Feedback und geteilten Einblicken geändert werden können.  

<!--links -->

[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2 Runtime – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft docs"  
[Webview2ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[Webview2ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[Webview2ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[Webview2ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

---
description: Für Microsoft Edge-WebView2 verwendete Versions Verwaltungsmodelle
title: Versionsverwaltung von Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 78184d3c670aa39e0a7f4a31e1216b5bc730c16e
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659671"
---
# Grundlegendes zu Browserversionen und WebView2  

WebView2 hängt von der Funktion von Microsoft Edge ab.  Für jedes WebView2-SDK muss mindestens eine Browserversion installiert sein.  Diese Browserversion ist in unseren [Versions][Webview2Releasenotes]hinweisen angegeben.  Möglicherweise sehen Sie die Mindestversion, die in der Paketversion des SDK widergespiegelt wird.  Wenn Sie beispielsweise das verwenden `SDK package version 0.9.488` , müssen Sie Microsoft Edge mit einer Buildnummer von 488 oder höher installieren.  Weitere Informationen zu den neuesten Versionen des Browsers finden Sie unter [Browser Kanäle][DeployedgeChannels].  

> [!NOTE]
> WebView2 befindet sich derzeit in der Vorschau.  Das Microsoft Edge-WebView-Team ist zwar bestrebt, die Abwärtskompatibilität zwischen Browserversionen und SDKs zu gewährleisten, es ist jedoch nicht gewährleistet, da einige neuere Versionen des Browsers möglicherweise ältere SDK-Versionen nicht unterstützen.  Wenn sich zwischen Browserversionen und SDKs Unterbrechungen ergeben, gibt das Microsoft Edge-WebView-Team die Änderungen in den [Versions][Webview2Releasenotes]hinweisen an.  

In Zukunft plant das Microsoft Edge-WebView-Team, das Verteilungsmodell zu ändern.  Das Microsoft Edge-WebView-Team plant, die direkte Abhängigkeit vom Microsoft Edge-Browser von WebView2 zu entfernen.  Weitere Informationen finden Sie unter [WebView2-Laufzeit][Webview2IndexEdgeRuntime] im Abschnitt [Distribution][Webview2Distibution] .  

## Experimentelle APIs  

Während WebView2 eine Vorschau ist, wird davon ausgegangen, dass die APIs im SDK bei GA unverändert bleiben.  Es gibt [experimentelle APIs][Webview2ReferenceWin3209488Experimental] , die im SDK enthalten sind.  Bitte bewerten Sie die experimentellen APIs und senden Sie Ihr Feedback über das [WebView Feedback Repo][GithubMicrosoftedgeWebviewfeedback].  

### Roadmap  

Nachdem WebView2 einen stabilen allgemeinen verfügbaren Zustand erreicht hat und wir das 1.0.0-SDK freigeben, plant das Microsoft Edge WebView-Team, alle experimentellen APIs in ein Pre-Release-Paket zu verschieben.  Das Pre-Release-Paket ermöglicht weiterhin Feedback und Einblicke in die neuesten Features, während die stable-Release-Version Abwärtskompatibilität aufrecht erhält.  

<!--links -->

[Webview2Distibution]: ./distribution.md "Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2 Runtime – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft docs"  
[Webview2ReferenceWin3209488Experimental]: ../reference/win32/0-9-488-reference-webview2.md#experimental "Experimental-Reference (WebView2) | Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

---
description: Grundlegendes zum Verwalten von WebView2-Anwendungen
title: Verwalten von WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge HTML, Enterprise, Gruppenrichtlinien, Verwaltbarkeit
ms.openlocfilehash: 1eb8b9dc1637daa8d10004ab8c340fe9ae33e38b
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "11057862"
---
# Verwalten von WebView2-Anwendungen  

[WebView2][WebView2Landing] ist eine Komponente, die Entwickler verwenden, um Ihre Anwendungen zu erstellen, und die Entwickler können eine [selbst aktualisierbare, immergrüne WebView2-Runtime][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview] auf einem Benutzergerät bereitstellen, um Ihre Anwendungen zu nutzen.  In diesem Dokument wird erläutert, wie IT-Administratoren WebView2-Anwendungen und-Laufzeit verwalten können.  Feedback von IT-Administratoren und Entwicklern ist auf [WebView2 Feedback Repo][GithubMicrosoftedgeWebviewfeddback]willkommen.  

## Gruppenrichtlinien für WebView2  

IT-Administratoren können Gruppenrichtlinienobjekte \ (GPO \) verwenden, um Richtlinieneinstellungen für WebView2 zu konfigurieren.  Die folgenden Richtliniensätze gelten für WebView2 nicht,  

*   [Microsoft Edge-Update Richtlinien][EdgeUpdatePolicies] sind für IT-Administratoren verfügbar, um die Installations-und Update Aspekte der WebView2-Laufzeit zu verwalten.  Der Microsoft Edge-Browser und die WebView2-Laufzeit werden mithilfe desselben Aktualisierungsmechanismus aktualisiert.  Es sei denn, eine Richtlinie, beispielsweise `Update` Kanal spezifisch, gilt für die Browser-und die WebView2-Laufzeit.  Beispielsweise `UpdateSuppressed` können IT-Administratoren Zeit für jeden Tag einstellen, um die automatische Aktualisierung sowohl für den Browser als auch für die WebView2-Laufzeit zu unterdrücken.  So können IT-Administratoren Einstellungen und Proxys einmal für die Browser-und die WebView2-Laufzeit konfigurieren, um deren Netzwerkbandbreite/-Datenverkehr zu steuern oder für andere Zwecke.  IT-Administratoren können dem [Microsoft Edge-Leitfaden][ConfigureMicrosoftEdge] folgen, um Microsoft Edge-Update-Richtlinien zu konfigurieren.  
*   [Microsoft Edge-Browser Richtlinien][EdgeBrowserPolicies] gelten nicht für WebView2-Anwendungen.  Dies ist beabsichtigt, da apps und Browser unterschiedliche Anwendungsfälle haben und IT-Administratoren möglicherweise nicht wissen, welche Anwendungen WebView2 verwenden.  Das Anwenden von Browser Richtlinien auf WebView2 kann unbeabsichtigte Folgen haben.  Beispielsweise können IT-Administratoren JavaScript im Browser blockieren, und alle WebView2-apps, die JavaScript verwenden, sind defekt.  
*   \ (In Kürze verfügbar) WebView2-spezifische Richtlinien – WebView2 stellt in Fällen, in denen die Verwaltung von WebView2 direkt sinnvoll ist, einen kleinen zusätzlichen Satz von Gruppenrichtlinien zur Verfügung.  Wir empfehlen App-Entwicklern, ihre eigenen Gruppenrichtlinien zum Verwalten der Verwendung von WebView2 zu implementieren, da es für IT-Administratoren einfacher ist, die APP zu verwalten, anstatt direkt WebView2.  

<!-- Links -->  

[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./distribution.md#understanding-the-webview2-runtime "Grundlegendes zur WebView2-Laufzeit und zum Installationsprogramm (Preview) – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft docs"  

[WebView2Landing]: ../index.md "Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  

[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge – Update Richtlinien | Microsoft docs"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge – Browser Richtlinien | Microsoft docs"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Konfigurieren von Microsoft Edge-Richtlinieneinstellungen unter Windows | Microsoft docs"  


[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

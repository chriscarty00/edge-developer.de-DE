---
description: Verstehen der Verwaltung von WebView2-Anwendungen
title: WebView2-Anwendungen verwalten
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html, enterprise, group policy, manageability
ms.openlocfilehash: 1eb8b9dc1637daa8d10004ab8c340fe9ae33e38b
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "11057862"
---
# WebView2-Anwendungen verwalten  

[WebView2][WebView2Landing] ist eine Komponente, die Entwickler zum Erstellen ihrer Anwendungen verwenden, und die Entwickler können eine selbst aktualisierende [Evergreen WebView2-Runtime][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview] auf Benutzergerät bereitstellen, um ihre Anwendungen zu nutzen.  In diesem Dokument wird erläutert, wie IT-Administratoren WebView2-Anwendungen und Runtime verwalten können.  Feedback von IT-Administratoren und Entwicklern ist im [WebView2-Feedback-Repository willkommen.][GithubMicrosoftedgeWebviewfeddback]  

## <a name="group-policies-for-webview2'"></a>Gruppenrichtlinien für WebView2  

IT-Administratoren können Gruppenrichtlinienobjekte \(GPO\) verwenden, um Richtlinieneinstellungen für WebView2 zu konfigurieren.  Die folgenden Richtlinien gelten/gelten nicht für WebView2,  

*   [Microsoft Edge – Updaterichtlinien][EdgeUpdatePolicies] stehen FÜR IT-Administratoren zur Verfügung, um die Installations- und Updateaspekte der WebView2-Laufzeit zu verwalten.  Der Microsoft Edge Browser und die WebView2-Laufzeit werden mit demselben Updatemechanismus aktualisiert.  Sofern eine Richtlinie, z. B. , nicht kanalspezifisch ist, gilt sie sowohl für den `Update` Browser als auch für die WebView2-Laufzeit.  Beispielsweise können IT-Administratoren die Uhrzeit für jeden Tag festlegen, um die automatische Aktualisierung sowohl für den Browser als auch für `UpdateSuppressed` die WebView2-Laufzeit zu unterdrücken.  Auf diese Weise können IT-Administratoren Einstellungen und Proxys sowohl für den Browser als auch für die WebView2-Laufzeit einmal konfigurieren, um die Netzwerkbandbreite/den Datenverkehr oder andere Zwecke zu steuern.  IT-Administratoren folgen [möglicherweise Microsoft Edge Leitfaden][ConfigureMicrosoftEdge] zum Konfigurieren von Microsoft Edge - Updaterichtlinien.  
*   [Microsoft Edge : Browserrichtlinien][EdgeBrowserPolicies] gelten nicht für WebView2-Anwendungen.  Dies liegt daran, dass Apps und Browser unterschiedliche Anwendungsfälle haben und IT-Administratoren möglicherweise nicht wissen, welche Anwendungen WebView2 verwenden.  Das Anwenden von Browserrichtlinien auf WebView2 kann unbeabsichtigte Folgen haben.  Beispielsweise können IT-Administratoren JavaScript im Browser blockieren, und alle WebView2-Apps, die JavaScript verwenden, sind beschädigt.  
*   \(In Kürze\) WebView2-spezifische Richtlinien – WebView2 macht einen kleinen zusätzlichen Satz von Gruppenrichtlinien verfügbar, wenn die direkte Verwaltung von WebView2 sinnvoll ist.  Wir empfehlen App-Entwicklern, ihre eigenen Gruppenrichtlinien zu implementieren, um die Verwendung von WebView2 zu verwalten, da es für IT-Administratoren einfacher ist, die App zu verwalten, anstatt WebView2 direkt zu verwalten.  

<!-- Links -->  

[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./distribution.md#understanding-the-webview2-runtime "Verstehen der WebView2-Runtime und des Installationsprogramms (Preview) – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft Docs"  

[WebView2Landing]: ../index.md "Einführung in Microsoft Edge WebView2 (Preview) | Microsoft Docs"  

[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge – Aktualisieren von Richtlinien | Microsoft Docs"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge – Browserrichtlinien | Microsoft Docs"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Konfigurieren Microsoft Edge Richtlinieneinstellungen für Windows | Microsoft Docs"  


[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  

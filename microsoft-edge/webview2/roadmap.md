---
description: Informieren Sie sich über die nächsten Schritte für WebView2
title: Roadmap für Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 99e743db0c1fb17ea46405b08e1ed074a3386068
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182360"
---
# Roadmap für Microsoft Edge-WebView2  

##### Letzte Aktualisierung: November 2020  

Das WebView2-Steuerelement ermöglicht Entwicklern das Einbetten von Webtechnologien in ihre systemeigenen Anwendungen.  Auf der folgenden Seite werden die prospektiven Roadmaps für WebView2 erläutert.  

> [!NOTE]
> WebView2 steht unter aktiver Entwicklung, und die Roadmap entwickelt sich weiterhin basierend auf Marktveränderungen und Kundenfeedback, bitte beachten Sie, dass die hier dargelegten Pläne nicht erschöpfend sind und sich Änderungen unterwerfen.  

Wenn Sie Bedenken oder Fragen zur Roadmap haben, geben Sie Ihr Feedback in das [Feedback-Repo][GithubMicrosoftedgeWebviewfeedbackMain]ein.  

Das WebView2-Team plant die folgenden wichtigen Schritte für zukünftige Updates.  

:::row:::
   :::column span="1":::
      WebView2-Runtime-Installationsprogramm  
   :::column-end:::
   :::column span="2":::
      *   Q4 2020
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Festgelegte Version  
   :::column-end:::
   :::column span="2":::
      *   Q4 2020  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Allgemeine Verfügbarkeit  
   :::column-end:::
   :::column span="2":::
      *   Win32 C/C++ \ (Q4 2020 \)  
      *   .Net \ (Q4 2020 \)  
      *   [WinUI 3.0][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## WebView2-Laufzeit und-Installationsprogramm  

Das [Evergreen-Verteilungsmodell][ConceptDistributionEvergreenModel] ermöglicht es Ihnen, die WebView2-Laufzeit auf dem Computer Ihres Benutzers zu verwenden oder zu verketten.  Das Evergreen-WebView2-Runtime-und-Installationsprogramm hat die allgemeine Verfügbarkeit erreicht \ (GA \).  

## Feste Version  

Mit dem Modell für die [Feste Versions Verteilung][ConceptsDistributionFixedVersionModel] können Sie die Microsoft Edge-Binärdateien in der systemeigenen Anwendung verpacken.  Die feste Version hat die allgemeine Verfügbarkeit erreicht \ (GA \).  

## Allgemeine Verfügbarkeit  

### Win32 C/C++  

Das Win32 C/C++-SDK hat GA erreicht.  

### .NET  

Das .NET SDK hat GA erreicht. 

### WinUI 3.0  

Sie können in ihren UWP-Anwendungen mithilfe von [Win UI 3,0][UwpToolkitsWinui3Index], derzeit in Alpha, auf WebView2 zugreifen.  Weitere Informationen dazu, wie Sie auf dem neuesten Stand bleiben, finden Sie unter Roadmap für die [Windows-UI-Bibliothek][GithubMicrosoftUiXamlRoadmap].  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Evergreen-Verteilungsmodell – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft docs"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Festes Versions Verteilungsmodell – Verteilung von Anwendungen mit WebView2 | Microsoft docs"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows-UI-Bibliothek 3,0 Preview 1 (Mai 2020) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Roadmap für die Windows-UI-Bibliothek – Microsoft/Microsoft-UI-XAML | GitHub"  

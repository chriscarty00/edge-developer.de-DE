---
description: Erfahren Sie mehr über die nächsten Schritte für WebView2
title: Roadmap für Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 0f51b5cab32bdb9b9aa9b6baceef5fe5a17eea54
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398413"
---
# <a name="microsoft-edge-webview2-roadmap"></a>Microsoft Edge WebView2-Roadmap  

> [!NOTE]
> Last Updated: November 2020  

Das WebView2-Steuerelement ermöglicht Entwicklern das Einbetten von Webtechnologien in ihre systemeigenen Anwendungen.  Auf der folgenden Seite wird die zukünftige Roadmap für WebView2 erläutert.  

> [!NOTE]
> WebView2 befindet sich in der aktiven Entwicklung, und die Roadmap wird basierend auf Marktänderungen und Kundenfeedback weiterentwickelt. Beachten Sie daher, dass die hier beschriebenen Pläne nicht vollständig sind und änderungen unterliegen.  

Wenn Sie Bedenken oder Fragen zur Roadmap haben, geben Sie Ihr Feedback im [Feedback-Repository an.][GithubMicrosoftedgeWebviewfeedbackMain]  

Das WebView2-Team plant die folgenden großen Anstrengungen für zukünftige Updates.  

:::row:::
   :::column span="1":::
      WebView2 Runtime Installer  
   :::column-end:::
   :::column span="2":::
      *   Q4 2020
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Unveränderbare Version  
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
      *   Win32 C/C++ \(Q4 2020\)  
      *   .NET \(Q4 2020\)  
      *   [WinUI 3.0][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <a name="webview2-runtime-and-installer"></a>WebView2 Runtime and Installer  

[Mit dem immergrünen][ConceptDistributionEvergreenModel] Verteilungsmodell können Sie die WebView2-Runtime auf dem Computer Des Benutzers ziel- oder verketten.  Die Laufzeit und das Installationsprogramm von Evergreen WebView2 haben die allgemeine Verfügbarkeit \(GA\) erreicht.  

## <a name="fixed-version"></a>Feste Version  

[Mit dem Verteilungsmodell mit fester][ConceptsDistributionFixedVersionModel] Version können Sie die Microsoft Edge in Ihrer systemeigenen Anwendung packen.  Die feste Version hat die allgemeine Verfügbarkeit \(GA\) erreicht.  

## <a name="general-availability"></a>Allgemeine Verfügbarkeit  

### <a name="win32-cc"></a>Win32 C/C++  

Das Win32 C/C++-SDK hat ga erreicht.  

### <a name="net"></a>.NET  

Das .NET SDK hat ga erreicht. 

### <a name="winui-30"></a>WinUI 3.0  

Sie können auf WebView2 in Ihren UWP-Anwendungen mithilfe der [Win UI 3.0][UwpToolkitsWinui3Index]zugreifen, die sich derzeit in Alpha befindet.  Weitere Informationen zum Auf dem neuesten Stand finden Sie unter [Windows Ui Library Roadmap][GithubMicrosoftUiXamlRoadmap].  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Immergrünes Verteilungsmodell – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft Docs"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Verteilungsmodell mit fester Version – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft Docs"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows Ui Library 3.0 Preview 1 (May 2020) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Windows Roadmap für die Benutzeroberflächenbibliothek – microsoft/microsoft-ui-xaml | GitHub"  

---
description: Hosten von Webinhalten in ihren Win32-, .net-UWP-Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2-Steuerelement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML, Windows Forms, WinForms, WPF, .net, WinUI, Projekt-Wiedervereinigung
ms.openlocfilehash: d3294ce72237a323113ed9f7c8f31e37af43f5e6
ms.sourcegitcommit: efdc6369c48942bfa39e45c713300ed70f0e3655
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2020
ms.locfileid: "11013744"
---
# Einführung in Microsoft Edge WebView2 (Preview)  

Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webtechnologien (HTML, CSS und JavaScript \) in ihre systemeigenen Anwendungen einbetten.  Das WebView2-Steuerelement verwendet [Microsoft Edge (Chrom)][MicrosoftedgeinsiderMain] als Rendering-Modul, um die Webinhalte in systemeigenen Anwendungen anzuzeigen.  Mit WebView2 können Sie Webcode in verschiedenen Teilen der systemeigenen Anwendung einbetten oder die gesamte systemeigene Anwendung in einem einzigen WebView-Webpart erstellen.  Informationen zum Erstellen einer WebView2-Anwendung finden Sie unter [Erste Schritte](#getting-started).  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Was ist WebView" lightbox="./media/WebView2/whatwebview.png":::
   Was ist WebView  
:::image-end:::  

> [!NOTE]
> Die WebView2 Preview ist für frühzeitiges Prototyping vorgesehen, um Feedback zu sammeln, um die API zu gestalten.  Sie sollten die Vorschau in ihren Produktions-apps nicht verwenden, da möglicherweise wichtige Änderungen auftreten.  Weitere Informationen finden Sie unter [Webview2Releasenotes].  

## Ansatz der Hybrid Anwendung  

Entwickler müssen sich häufig zwischen dem Erstellen einer Webanwendung oder einer systemeigenen Anwendung entscheiden.  Die Entscheidung hängt vom Kompromiss zwischen Reichweite und macht ab.  Web-Anwendungen ermöglichen eine breite Reichweite.  Als Web-Entwickler können Sie die meisten, wenn nicht alle Ihren Code, auf allen verschiedenen Plattformen wieder verwenden.  Systemeigene Anwendungen nutzen jedoch die Funktionen der gesamten systemeigenen Plattform.  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native" lightbox="./media/WebView2/webnative.png":::
   Web Native  
:::image-end:::  

Hybrid Anwendungen ermöglichen Entwicklern, das Beste aus beiden Welten zu genießen.  Entwickler von Hybrid Anwendungen profitieren von der Allgegenwart und Stärke der Web-Plattform sowie von der Leistungsfähigkeit und den vollständigen Funktionen der systemeigenen Plattform.  

## WebView2-Vorteile   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="WebView-Gründe" lightbox="./media/WebView2/webviewreasons.png":::
   WebView-Gründe  
:::image-end:::  

:::row:::
   :::column span="1":::
      **Web-Ökosystem \ & skillset**  
      Verwenden Sie die gesamte Web-Plattform, Bibliotheken, Tools und Talente, die im Web-Ökosystem vorhanden sind.  
   :::column-end:::
   :::column span="1":::
      **Schnelle Innovation**  
      Web-Entwicklung ermöglicht schnellere Bereitstellung und Iteration.  
   :::column-end:::
   :::column span="1":::
      **Windows 7, 8, 10 Support**  
      Unterstützung für eine konsistente Benutzeroberfläche in Windows 7, 8 und 10.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **Systemeigene Funktionen**  
      Greifen Sie auf den vollständigen Satz nativer APIs zu.  
   :::column-end:::
   :::column span="1":::
      **Code Freigabe**  
      Durch Hinzufügen von Webcode zu ihrer CodeBase können Sie die Wiederverwendung auf mehreren Plattformen erhöhen.  
   :::column-end:::
   :::column span="1":::
      **Microsoft-Support**  
      Microsoft bietet Support und fügt neue Funktionsanforderungen hinzu, wenn WebView2 als "ga" veröffentlicht wird.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **Immergrüne Verteilung**  
      Verlassen Sie sich auf eine aktuelle Version von Chromium mit regulären Plattformupdates und Sicherheitspatches.  
   :::column-end:::
   :::column span="1":::
      **Behoben** \ (in Kürze verfügbar)  
      Wählen Sie aus, um die Chrom Bits in Ihrer Anwendung zu verpacken.  
   :::column-end:::
   :::column span="1":::
      **Inkrementelle Einführung**  
      Fügen Sie Ihrer Anwendung Stück für Stück Webkomponenten hinzu.  
   :::column-end:::
:::row-end:::

## Erste Schritte  

Wenn Sie Ihre Anwendung mithilfe des WebView2-Steuerelements erstellen und testen möchten, müssen Sie sowohl [Microsoft Edge (Chrom)][MicrosoftedgeinsiderDownload] als auch das [WebView2-SDK][NugetPackagesMicrosoftWebWebView2] installiert haben.  Wählen Sie eine der folgenden Optionen aus, um loszulegen.  

*   [Erste Schritte mit Win32 C/C++][Webview2GettingstartedWin32]  
*   [Erste Schritte mit WPF][Webview2GettingstartedWpf]  
*   [Erste Schritte mit WinForms][Webview2GettingstartedWinforms]  
*   [Erste Schritte mit WinUI3][Webview2GettingstartedWinui]  

Das [WebView2-Beispiel][GithubMicrosoftedgeWebview2samples] -Repository enthält Beispiele, die alle WebView2-SDK-Features und API-Verwendungsmuster veranschaulichen.  Wenn dem WebView2-SDK weitere Features hinzugefügt werden, werden die Beispielanwendungen aktualisiert.  

## Unterstützte Plattformen  

Eine Entwicklervorschau steht in den folgenden Programmierumgebungen zur Verfügung.  

*   Win32 C/C++  
*   .NET Framework 4.6.2 oder höher  
*   .Net Core 3,0 oder höher  
*   [WinUI 3.0][UwpToolkitsWinui3]  

Sie können WebView2-Anwendungen unter den folgenden Windows-Versionen ausführen.  

*   Windows 10  
*   Windows8.1  
*   Windows 8  
*   Windows7  
*   Windows Server 2019  
*   Windows Server 2016  
*   Windows Server 2012  
*   Windows Server-2012R2  
*   Windows Server 2008 R2  

## Nächste Schritte  

Weitere Informationen zum Erstellen und Bereitstellen von WebView2-Anwendungen finden Sie in den konzeptionellen Dokumentationen und Anleitungen.  

#### Konzepte  

*   [Grundlegendes zu WebView2 SDK-Versionen][Webview2ConceptsVersioning]
*   [Verteilung von Anwendungen mithilfe von WebView2][Webview2ConceptsDistribution]  
*   [Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen][Webview2ConceptsSecurity]
*   [Verwalten von benutzerdatenordnern in WebView2-Anwendungen][Webview2ConceptsUserdatafolder]
 
#### Anleitungen  

*   [Debuggen mit WebView2][Webview2HowtoDebug]  
*   [Automatisieren und Testen von WebView2 mit Microsoft Edge Driver][Webview2HowtoWebdriver]  

## Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

> [!NOTE]
> Während der Vorschau unterstützt die gesammelten Daten das Erstellen eines besseren Produkts.  Wenn Sie die WebView2-Datensammlung deaktivieren möchten, wechseln Sie zu `edge://settings/privacy` und deaktivieren Sie die Browserdaten Sammlung.  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen | Microsoft docs"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Verwalten des Benutzerdatenordners | Microsoft docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Grundlegendes zu WebView2 SDK-Versionen | Microsoft docs"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Erste Schritte mit WebView2 (Developer Preview) | Microsoft docs"   
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Erste Schritte mit WebView2 in Windows Forms-Apps (Preview) | Microsoft docs"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Erste Schritte mit WebView2 in WinUI3 (Preview) | Microsoft docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF (Preview) | Microsoft docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Debuggen mit WebView2 | Microsoft docs"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatisieren und Testen von WebView2 mit Microsoft Edge Driver | Microsoft docs"  
[Webview2Releasenotes]: ./releasenotes.md "Anmerkungen zu dieser Version von Webview2Releasenotes für WebView2 SDK | Microsoft docs"  

[UwpToolkitsWinui3]: ./gettingstarted/winui.md "Windows-UI-Bibliothek 3 Preview 2 (Juli 2020) | Microsoft docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge-Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Insider herunterladen"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | NuGet-Katalog"  

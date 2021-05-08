---
description: Hosten von Webinhalten in Ihren Win32-, .NET- und UWP-Apps mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge WebView2-Steuerelement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, browser control, edge html, Windows Forms, WinForms, WPF, .NET, WinUI, Project Reunion
ms.openlocfilehash: 154c18a3cc9236a8abd286918d72e1a1968fea38
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535726"
---
# <a name="introduction-to-microsoft-edge-webview2"></a>Einführung in Microsoft Edge WebView2  

Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webtechnologien \(HTML, CSS und JavaScript\) in Ihre systemeigenen Apps einbetten.  Das WebView2-Steuerelement verwendet [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] als Renderingmodul, um die Webinhalte in systemeigenen Apps anzuzeigen.  Mit WebView2 können Sie Webcode in verschiedene Teile Ihrer systemeigenen App einbetten.  Erstellen Sie alle systemeigenen Apps in einer einzelnen WebView-Instanz.  Informationen zum Erstellen einer WebView2-App finden Sie unter [Erste Schritte.](#get-started)  

:::image type="complex" source="./media/WebView2/what-webview.png" alt-text="Was ist WebView?" lightbox="./media/WebView2/what-webview.png":::
   Was ist WebView?  
:::image-end:::    

## <a name="hybrid-app-approach"></a>Hybrid-App-Ansatz  

Entwickler müssen häufig zwischen dem Erstellen einer Web-App oder einer nativen App entscheiden.  Die Entscheidung hängt vom Abhandeln zwischen Reichweite und Energie ab.  Web-Apps ermöglichen eine breite Reichweite.  Als Webentwickler können Sie den Großteil Ihres Codes auf verschiedenen Plattformen wiederverwenden.  Verwenden Sie eine systemeigene App, um auf alle Funktionen einer systemeigenen Plattform zu zugreifen.  

:::image type="complex" source="./media/WebView2/web-native.png" alt-text="Web native" lightbox="./media/WebView2/web-native.png":::
   Web native  
:::image-end:::    

Hybrid-Apps ermöglichen Entwicklern, das Beste aus beiden Welten zu genießen.  Entwickler von Hybrid-Apps profitieren von den folgenden Vorteilen.  

*   Die Ubiquitie und Stärke der Webplattform.  
*   Die Leistungsfähigkeit und die vollständigen Funktionen der systemeigenen Plattform.  
    
## <a name="webview2-benefits"></a>WebView2-Vorteile   

<!--  
:::image type="complex" source="./media/WebView2/webview-reasons.png" alt-text="WebView reasons" lightbox="./media/WebView2/webview-reasons.png":::
   WebView reasons  
:::image-end:::    
-->  

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset.msft.png":::  
      **Web ecosystem \& Skillset**  
      Nutzen Sie die gesamte Webplattform, Bibliotheken, Tools und Talente, die innerhalb des Webökosystems vorhanden sind.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation.msft.png":::  
      **Schnelle Innovation**  
      Die Webentwicklung ermöglicht eine schnellere Bereitstellung und Iteration.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support.msft.png":::  
      **Unterstützung für Windows 7, 8 und 10**  
      Unterstützung für eine konsistente Benutzeroberfläche in Windows 7, Windows 8 und Windows 10.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities.msft.png":::  
      **Systemeigene Funktionen**  
      Greifen Sie auf den vollständigen Satz systemeigener APIs zu.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing.msft.png":::  
      **Codefreigabe**  
      Das Hinzufügen von Webcode zu Ihrer Codebasis ermöglicht eine höhere Wiederverwendung auf mehreren Plattformen.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support.msft.png":::  
      **Microsoft-Support**  
      Microsoft bietet Unterstützung und fügt neue Featureanforderungen hinzu, wenn WebView2 unter Allgemeinverfügbarkeit \(GA\) veröffentlicht wird.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen.msft.png":::  
      **Immergrüne Verteilung**  
      Verlassen Sie sich auf eine aktuelle Version von Chromium mit regelmäßigen Plattformupdates und Sicherheitspatches.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed.msft.png":::  
      **Behoben**  
      \(in Kürze\) Wählen Sie aus, um die Chromium-Bits in Ihrer App zu packen.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption.msft.png":::  
      **Inkrementelle Einführung**  
      Fügen Sie Ihrer App Stück für Stück Webkomponenten hinzu.  
   :::column-end:::
:::row-end:::  

## <a name="get-started"></a>Erste Schritte  

Zum Erstellen und Testen Ihrer App mithilfe des WebView2-Steuerelements benötigen Sie <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  -->das [installierte WebView2 SDK.][NugetPackagesMicrosoftWebWebView2]  Wählen Sie eine der folgenden Optionen für die ersten Schritte aus.  

*   [Erste Schritte mit Win32 C/C++][Webview2GetStartedWin32]  
*   [Erste Schritte mit WPF][Webview2GetStartedWpf]  
*   [Erste Schritte mit WinForms][Webview2GetStartedWinforms]  
*   [Erste Schritte mit WinUI3][Webview2GetStartedWinui]  
    
Das [WebView2 Samples-Repository][GithubMicrosoftedgeWebview2samples] enthält Beispiele, die alle WebView2 SDK-Features und API-Verwendungsmuster veranschaulichen.  Wenn dem WebView2 SDK weitere Features hinzugefügt werden, werden die Beispiel-Apps aktualisiert.  

## <a name="supported-platforms"></a>Unterstützte Plattformen  

Eine Allgemeine Verfügbarkeit \(GA\) oder Vorschauversion ist in den folgenden Programmierumgebungen verfügbar.  

*   Win32 C/C++ \(GA\)  
*   .NET Framework 4.5 oder höher  
*   .NET Core 3.1 oder höher  
*   .NET 5  
*   [WinUI 3.0][UwpToolkitsWinui3] \(Preview\)  
    
Sie können WebView2-Apps unter den folgenden Versionen von Windows ausführen.  

*   Windows 10  
*   Windows8.1  
*   Windows 7 \*\*  
*   Windows Server 2019  
*   Windows Server 2016  
*   Windows Server 2012  
*   Windows Server 2012 R2  
*   Windows Server 2008 R2 \*\*  
    
> [!IMPORTANT]
> \*\* WebView2-Unterstützung für Windows 7 und Windows Server 2008 R2 hat den gleichen Supportzyklus wie Microsoft Edge.  Weitere Informationen finden Sie unter [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].  

## <a name="next-steps"></a>Nächste Schritte  

Weitere Informationen zum Erstellen und Bereitstellen von WebView2-Apps finden Sie in der konzeptionellen Dokumentation und anleitungen.  

### <a name="concepts"></a>Konzepte  

*   [Verstehen von WebView2 SDK-Versionen][Webview2ConceptsVersioning]  
*   [Verteilung von Apps mit WebView2][Webview2ConceptsDistribution]  
*   [Bewährte Methoden für die Entwicklung sicherer WebView2-Apps][Webview2ConceptsSecurity]  
*   [Verwalten des Benutzerdatenordners in WebView2-Apps][Webview2ConceptsUserDataFolder]  
 
### <a name="how-to-guides"></a>How-To Anleitungen  

*   [Debuggen mit WebView2][Webview2HowToDebug]  
*   [Automatisieren und Testen von WebView2 mit Microsoft Edge Driver][Webview2HowToWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Verteilung von Apps mithilfe von WebView2-| Microsoft Docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Bewährte Methoden für die Entwicklung sicherer WebView2-Apps | Microsoft Docs"  
[Webview2ConceptsUserDataFolder]: ./concepts/user-data-folder.md "Verwalten der Benutzerdatenordner-| Microsoft Docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Verstehen der WebView2 SDK-| Microsoft Docs"  
[Webview2GetStartedWin32]: ./get-started/win32.md "Erste Schritte mit WebView2 | Microsoft Docs"  
[Webview2GetStartedWinforms]: ./get-started/winforms.md "Erste Schritte mit WebView2 in Windows Forms-Apps (Vorschau) | Microsoft Docs"  
[Webview2GetStartedWinui]: ./get-started/winui.md "Erste Schritte mit WebView2 in WinUI3 (Vorschau) | Microsoft Docs"  
[Webview2GetStartedWpf]: ./get-started/wpf.md "Erste Schritte mit WebView2 in WPF (Preview) | Microsoft Docs"  
[Webview2HowToDebug]: ./how-to/debug.md "Debuggen mit WebView2-| Microsoft Docs"  
[Webview2HowToWebdriver]: ./how-to/webdriver.md "Automatisieren und Testen von WebView2 mit Microsoft Edge Driver | Microsoft Docs"  
[Webview2ReleaseNotes]: ./release-notes.md "Versionshinweise für WebView2 SDK | Microsoft Docs"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows UI Library 3 Preview 2 (July 2020) | Microsoft Docs"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Microsoft Edge unterstützte Betriebssysteme | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Insider herunterladen"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | NuGet Gallery"  

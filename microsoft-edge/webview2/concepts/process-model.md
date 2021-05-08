---
description: Prozessmodell
title: Prozessmodell | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, Webview2, Webview, wpf-Apps, Wpf, Microsoft Edge, ICoreWebView2, ICoreWebView2Host, Browsersteuerung, Edge-HTML
ms.openlocfilehash: 95d0c53219114c47a781317ab4b2ee2028fc586f
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535615"
---
# <a name="process-model"></a>Prozessmodell  

:::row:::
   :::column span="1":::
      Unterstützte Plattformen:
   :::column-end:::
   :::column span="2":::
      Win32, Windows Forms, WinUi, WPF
   :::column-end:::
:::row-end:::  

WebView2 verwendet dasselbe Prozessmodell wie der Microsoft Edge-Browser.  Weitere Informationen zum Browserprozessmodell finden Sie unter [Browserarchitektur – Innen sehen Sie sich modernen Webbrowser an.][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]  

Ein Browserprozess ist den Rendererprozessen und anderen Hilfsprozessen zugeordnet, wie in diesem Artikel beschrieben.  Wenn WebView2 angegeben ist, verwenden die anfordernden Host-App-Prozesse außerdem WebView2.  

:::image type="complex" source="../media/process-model-1.png" alt-text="Prozess 1" lightbox="../media/process-model-1.png":::
   Prozess 1  
:::image-end:::    

Ein Browserprozess ist nur einem Benutzerdatenordner zugeordnet.  Ein Anforderungsprozess kann mehrere Benutzerdatenordner angeben.  Ein Anforderungsprozess, der mehrere Benutzerdatenordner angibt, ist der gleichen Anzahl von Browserprozessen zugeordnet.  
Bei einem Anforderungsprozess, der Zugriff auf zwei Benutzerdatenordner anfordert, werden beispielsweise zwei Browserprozesse verwendet.  

:::image type="complex" source="../media/process-model-2.png" alt-text="Prozess 2" lightbox="../media/process-model-2.png":::
   Prozess 2  
:::image-end:::    

Ein Browserprozess ist mehreren Rendererprozessen zugeordnet.  Eine WebView 2-Instanz erstellt einen Browserprozess für Serviceframes.  Ein Browserprozess kann mehreren Frames zugeordnet sein.  Ein Browserprozess kann verschiedenen Instanzen von WebView2 zugeordnet sein.  Die Anzahl der Renderprozesse variiert je nach den folgenden Bedingungen.  

*   Verwenden des Websiteisolationsfeatures in Ihrem Browser.  
*   Die Anzahl unterschiedlicher getrennter Ursprünge, die in zugeordneten Instanzen von WebView2 gerendert werden.  
    
Die Websiteisolationsbrowserfunktion wird in den vorherigen Inhalten beschrieben. 
<!--todo:  which previous content?  -->  

Der `CoreWebView2Environment` stellt einen Benutzerdatenordner und Browserprozess dar.  Der entspricht nicht direkt einem Satz von Prozessen, da verschiedene Rendererprozesse von einem WebView2 abhängig von der Zuvor beschriebenen Websiteisolation `CoreWebView2` verwendet werden.  

Verwenden Sie das Ereignis von , um auf Abstürze und Hänge im Browser und renderer-Prozessen `ProcessFailed` zu `CoreWebView2` reagieren.  

Verwenden Sie die Methode von , um zugeordnete Browser- und Rendererprozesse `Close` sicher herunterfahren zu `CoreWebView2Controller` können.  

Führen Sie zum Öffnen des Fensters Browser Task Manager aus dem **DevTools-Fenster** einer WebView2-Instanz die folgenden Aktionen aus.  

*   Wählen Sie `Shift` + `Escape` aus.  
*   Zeigen Sie auf die Titelleiste des DevTools-Fensters, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie `Browser task manager` aus.  
    
Alle Prozesse, die mit dem Browserprozess Ihrer WebView2 verknüpft sind, werden einschließlich der zugehörigen Zwecke angezeigt.  

## <a name="see-also"></a>Weitere Informationen  

*   Navigieren Sie zu [WebView2 Get Started Guides,][Webview2IndexGetStarted] um mit WebView2 zu beginnen.  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samples] auf GitHub.  
*   Weitere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][DotnetApiMicrosoftWebWebview2WpfWebview2].  
*   Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2IndexNextSteps].  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Erste Schritte – Einführung in Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2-Klasse | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Browserarchitektur – Innenseite des modernen Webbrowsers (Teil 1)"  

---
description: Navigation
title: Navigations-| WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, Webview2, Webview, wpf-Apps, Wpf, Microsoft Edge, ICoreWebView2, ICoreWebView2Host, Browsersteuerung, Edge-HTML
ms.openlocfilehash: e87994d6205f81e01385a131e17091d0c8b001d5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470844"
---
# <a name="navigation-events"></a>Navigationsereignisse  

:::row:::
   :::column span="1":::
      Unterstützte Plattformen:
   :::column-end:::
   :::column span="2":::
      Win32, Windows Forms, WinUi, WPF
   :::column-end:::
:::row-end:::  

Navigationsereignisse werden ausgeführt, wenn bestimmte asynchrone Aktionen für den inhalt auftreten, der in einer WebView2-Instanz angezeigt wird.  Wenn ein WebView2-Benutzer beispielsweise zu einer neuen Website navigiert, lauscht der systemeigene Inhalt auf die Änderung mithilfe des `NavigationStarting` Ereignisses.  Wenn die Navigationsaktion abgeschlossen ist, `NavigationCompleted` wird ausgeführt.  Ein gutes Beispiel für Navigationsereignisse finden Sie unter Erste Schritte in [WebView2.][Webview2IndexGettingStarted]  

<!--todo:  Move the relevant information out of the getting started guide to better focus the content and leave the most concise elements in the getting started guide.  -->   

Die normale Sequenz von Navigationsereignissen ist `NavigationStarting` , , , und dann `SourceChanged` `ContentLoading` `HistoryChanged` `NavigationCompleted` .  Die folgenden Ereignisse beschreiben den Status von WebView2 während jeder Navigation.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/navigation-graph.png" alt-text="Die Microsoft Edge WebView2-Navigationsereignisse" lightbox="../media/navigation-graph.png":::
         Die Microsoft Edge WebView2-Navigationsereignisse  
      :::image-end:::  
      
      > [!NOTE]
      > Die Abbildung stellt Navigationsereignisse mit derselben `NavigationId` Eigenschaft für das jeweilige Ereignisargument dar.  
   :::column-end:::
   :::column span="2":::
      | Sequence | Ereignisname | Details |  
      |:--- |:--- |:--- |  
      | 1 | `NavigationStarting`  |  WebView2 beginnt zu navigieren, und die Navigation führt zu einer Netzwerkanforderung.  Der Host kann die Anforderung während des Ereignisses nicht mehr senden.  |  
      | 2 | `SourceChanged`  |  Die Quelle von WebView2 wird in eine neue URL geändert.  Das Ereignis kann durch eine Navigationsaktion verursacht werden, die keine Netzwerkanforderung verursacht, z. B. eine Fragmentnavigation.  |  
      | 3 | `ContentLoading`  |  WebView beginnt mit dem Laden von Inhalten für die neue Seite.  |  
      | 4 | `HistoryChanged`  |  Die Navigation bewirkt, dass der Verlauf von WebView2 aktualisiert wird.  |  
      | 5 | `NavigationCompleted`  |  WebView2 schließt das Laden von Inhalten auf der neuen Seite ab.  |  
   :::column-end:::
:::row-end:::

Nachverfolgen von Navigationsereignissen zu jedem neuen Dokument mithilfe der Navigations-ID \( `NavigationId` Event\).  Das `NavigationId` Ereignis von WebView ändert sich jedes Mal, wenn eine erfolgreiche Navigation zu einem neuen Dokument abgeschlossen ist.  

 Navigationsereignisse mit unterschiedlichen `NavigationId` Ereignisinstanzen können überlappen.  Wenn Sie beispielsweise ein Navigationsereignis starten, müssen Sie auf das zugehörige Ereignis `NavigationStarting` warten.  Wenn Sie dann eine andere Navigation starten, sollte das Ereignis für die erste Navigation angezeigt werden, gefolgt von dem Ereignis für die zweite Navigation, gefolgt von dem Ereignis für die erste Navigation und dann alle anderen entsprechenden Navigationsereignisse für die zweite `NavigationStarting` `NavigationStarting` `NavigationCompleted` Navigation.  
 
 In Fehlerfällen gibt es möglicherweise ein Ereignis, je nachdem, ob die Navigation zu einer Fehlerseite `ContentLoading` fortgesetzt wird.  
 
 Wenn eine HTTP-Umleitung auftritt, gibt es mehrere Ereignisse in einer Zeile, bei denen für spätere Ereignisargumente die Eigenschaft festgelegt ist, das Ereignis `NavigationStarting` `IsRedirect` jedoch unverändert `NavigationId` bleibt.  
 
 Dieselben Dokumentnavigationsereignisse, z. B. die Navigation zu einem Fragment, führen nicht zu dem Ereignis und erhöhen `NavigationStarting` das Ereignis `NavigationId` nicht.  

Verwenden Sie zum Überwachen oder Abbrechen von Navigationsereignissen innerhalb von Unterframes in einer WebView2-Instanz die Ereignisse and, die genau wie die entsprechenden Ereignisse außerhalb des `FrameNavigationStarting` `FrameNavigationCompleted` Frames agieren.  

## <a name="see-also"></a>Weitere Informationen  

*   Um mit WebView2 zu beginnen, navigieren Sie zu [WebView2 Anleitungen für erste Schritte.][Webview2IndexGettingStarted]  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samples] auf GitHub.  
*   Weitere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][DotnetApiMicrosoftWebWebview2WpfWebview2].  
*   Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2IndexNextSteps].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2-Klasse | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

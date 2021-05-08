---
description: Threadingmodell
title: Threadmodell| WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, Webview2, Webview, wpf-Apps, Wpf, Microsoft Edge, ICoreWebView2, ICoreWebView2Host, Browsersteuerung, Edge-HTML
ms.openlocfilehash: 9a7ce3d66e53b832d4430afb153e6539d97e5db7
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535608"
---
# <a name="threading-model"></a>Threadingmodell 

:::row:::
   :::column span="1":::
      Unterstützte Plattformen:
   :::column-end:::
   :::column span="2":::
      Win32, Windows Forms, WinUi, WPF
   :::column-end:::
:::row-end:::  

Das WebView2-Steuerelement basiert auf dem [Component Object Model (COM)][WindowsWin32ComTheComponentObjectModel] und muss in einem [Single Threaded Apartment (STA)-Thread ausgeführt][WindowsWin32ComSingleThreadedApartments] werden.  

## <a name="thread-safety"></a>Threadsicherheit  

WebView2 muss in einem Benutzeroberflächenthread erstellt werden.  Insbesondere ein Thread mit einer Nachrichtenumpumpung.  Alle Rückrufe erfolgen in diesem Thread, und Anforderungen an WebView2 müssen in diesem Thread ausgeführt werden.  Es ist nicht sicher, WebView2 aus einem anderen Thread zu verwenden.  

Die einzige Ausnahme gilt für die `Content` Eigenschaft von `CoreWebView2WebResourceRequest` .  Der `Content` Eigenschaftendatenstrom wird aus einem Hintergrundthread gelesen.  Der Datenstrom sollte agil sein oder aus einem Hintergrund-STA erstellt werden, um leistungsbeeinträchtigungen für den Benutzeroberflächenthread zu verhindern.  

## <a name="re-entrancy"></a>Erneutes Entlocken  

Rückrufe, einschließlich Ereignishandlern und Abschlusshandlern, werden seriell ausgeführt.  
Nachdem Sie einen Ereignishandler ausgeführt und eine Nachrichtenschleife begonnen haben, können Sie keinen Ereignishandler oder Abschlussrückruf erneut ausführen.  

## <a name="deferrals"></a>Verschiebungen  

Einige WebView2-Ereignisse lesen Werte, die für die zugehörigen Ereignisargumente festgelegt sind, oder starten eine Aktion, nachdem der Ereignishandler abgeschlossen wurde.  Wenn Sie auch einen asynchronen Vorgang wie einen Ereignishandler ausführen müssen, verwenden Sie die -Methode für die Ereignisargumente `GetDeferral` der zugeordneten Ereignisse.  Das zurückgegebene Objekt stellt sicher, dass der Ereignishandler erst als abgeschlossen betrachtet wird, wenn `Deferral` `Complete` die -Methode angefordert `Deferral` wird.  

Sie können das Ereignis z. B. verwenden, um eine Verbindung als untergeordnetes Fenster herzustellen, wenn `NewWindowRequested` `CoreWebView2` der Ereignishandler abgeschlossen ist.  Wenn Sie jedoch asynchron das erstellen `CoreWebView2` müssen, fordern Sie die `GetDeferral` -Methode für `NewWindowRequestedEventArgs` an.  Nachdem Sie die -Eigenschaft asynchron erstellt und für die festgelegt haben, wird die Anforderung für das Objekt mithilfe `CoreWebView2` `NewWindow` der `NewWindowRequestedEventArgs` `Complete` `Deferral` -Methode `GetDeferral` zurückgegeben.  

## <a name="block-the-ui-thread"></a>Blockieren des Benutzeroberflächenthreads  

WebView2 verwendet die Nachrichtenumpumpung des Benutzeroberflächenthreads, um Ereignishandlerrückrufe und Async-Methodenabschlussrückrufe ausführen zu können.  Wenn Sie Methoden verwenden, die die Nachrichtenumpumpung blockieren, z. B. oder, werden die WebView2-Ereignishandler und `Task.Result` async-Methodenentvollständigungshandler `WaitForSingleObject` nicht ausgeführt.  Der folgende Code ist beispielsweise nicht vollständig, da die Nachrichtenumpumpung angehalten wird, während sie `Task.Result` wartet, `ExecuteScriptAsync` bis sie abgeschlossen ist.  Da die Nachrichtenumpumpung blockiert ist, kann der Vorgang `ExecuteScriptAsync` nicht abgeschlossen werden.   

```csharp
private void Button_Click(object sender, EventArgs e)
{
    string result = webView2Control.CoreWebView2.ExecuteScriptAsync("'test'").Result;
    MessageBox.Show(this, result, "Script Result");
}
```  

Verwenden Sie einen asynchronen Mechanismus wie and , der die Nachrichtenummpung oder den `await` `async` Benutzeroberflächenthread nicht `await` blockiert.  

```csharp
private async void Button_Click(object sender, EventArgs e)
{
    string result = await webView2Control.CoreWebView2.ExecuteScriptAsync("'test'");
    MessageBox.Show(this, result, "Script Result");
}
```  

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

[WindowsWin32ComSingleThreadedApartments]: /windows/win32/com/single-threaded-apartments "Single-Threaded-| Microsoft Docs"  
[WindowsWin32ComTheComponentObjectModel]: /windows/win32/com/the-component-object-model "Das Component-Objektmodell | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

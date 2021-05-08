---
description: Informationen zur Verwendung von JavaScript in komplexen Szenarien in WebView2-Apps
title: Verwenden von JavaScript in WebView2-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: da04d1e24b95dfa7ea477bbd228fd46b64727ec3
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536524"
---
# <a name="use-javascript-in-webview-for-extended-scenarios"></a>Verwenden von JavaScript in WebView für erweiterte Szenarien  

Mithilfe von JavaScript in WebView2-Steuerelementen können Sie systemeigene Apps an Ihre Anforderungen anpassen.  In diesem Artikel wird die Verwendung von JavaScript in WebView2 und die Entwicklung mit erweiterten WebView2-Features und -Funktionen erläutert.  

## <a name="before-you-begin"></a>Vorbemerkungen  

In diesem Artikel wird davon ausgegangen, dass Sie bereits über ein funktionierendes Projekt verfügen.  Wenn Sie kein Projekt haben und mit folgen möchten, navigieren Sie zum [WebView2 Getting Started Guide][Webview2GettingstartedWpf].  

## <a name="basic-webview2-functions"></a>Grundlegende WebView2-Funktionen  

Verwenden Sie die folgenden Funktionen, um mit dem Einbetten von JavaScript in Ihre WebView-App zu beginnen.  

| API  | Beschreibung  |
|:--- |:--- |  
| [ExecuteScriptAsync][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | Führen Sie JavaScript in einem WebView-Steuerelement aus. Weitere Informationen finden Sie im Lernprogramm Erste Schritte. |
| [OnDocumentCreatedAsync][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | Wird ausgeführt, wenn das Dokumentobjektmodell \(DOM\) erstellt wird. |
      
## <a name="scenario--running-a-dedicated-script-file"></a>Szenario: Ausführen einer dedizierten Skriptdatei  

Greifen Sie in diesem Abschnitt über Ihr WebView2-Steuerelement auf eine dedizierte JavaScript-Datei zu.  

> [!NOTE]
> Obwohl das Schreiben von JavaScript-Inline für schnelle JavaScript-Befehle effizient sein kann, gehen JavaScript-Farbthemen und Zeilenformatierungen verloren, was das Schreiben großer Codeabschnitte in Visual Studio.  

Um das Problem zu lösen, erstellen Sie eine separate JavaScript-Datei mit Ihrem Code, und übergeben Sie dann einen Verweis auf diese Datei mithilfe der `ExecuteScriptAsync` Parameter.  

1.  Erstellen Sie `.js` eine Datei in Ihrem Projekt, und fügen Sie den JavaScript-Code hinzu, den Sie ausführen möchten.  Erstellen Sie beispielsweise eine Datei namens `script.js` .  
1.  Konvertieren Sie die JavaScript-Datei in eine Zeichenfolge, die an übergeben `ExecuteScriptAsync` wird.  
    1.  Um Ihre JavaScript-Datei in eine Zeichenfolge zu konvertieren, kopieren Sie den folgenden Codeausschnitt.  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  Fügen Sie den Code in `MainWindow.xaml.cs` ein.  
1.  Übergeben Sie Ihre Textvariable mithilfe `ExecuteScriptAsync` von .  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## <a name="scenario--remove-drag-and-drop-functionality"></a>Szenario: Entfernen der Drag -and-Drop-Funktionalität  

Verwenden Sie in diesem Abschnitt JavaScript, um die Drag -and-Drop-Funktionalität aus Ihrem WebView2-Steuerelement zu entfernen.  

Erkunden Sie zunächst die aktuelle Drag -and-Drop-Funktion.  

1.  Erstellen Sie `.txt` eine Datei, um drag-and-drop zu erstellen.  Erstellen Sie z. B. eine Datei mit `contoso.txt` dem Namen, und fügen Sie ihr Text hinzu.  
1.  Führen Sie Ihr Projekt aus.  
1.  Ziehen Sie die Datei per Drag -and-Drop `contoso.txt` in das WebView-Steuerelement.  Es wird ein neues Fenster geöffnet, das das Ergebnis des Codes in Ihrem Beispielprojekt ist.  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Ergebnis des Ziehens und Ablegens contoso.txt" lightbox="./media/dragtext.png":::
       Ergebnis des Ziehens und Ablegens contoso.txt  
    :::image-end:::  

Fügen Sie nun Code hinzu, um die Drag -and-Drop-Funktion aus dem WebView2-Steuerelement zu entfernen.  

1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `InitializeAsync()` in `MainWindow.xaml.cs` ein.   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  Führen Sie Ihr Projekt aus.  
1.  Versuchen Sie, drag-and-drop `contoso.txt` zu ziehen.  Vergewissern Sie sich, dass Drag -and-Drop nicht möglich ist.  

## <a name="scenario--removing-the-context-menu"></a>Szenario: Entfernen des Kontextmenüs  

Entfernen Sie in diesem Abschnitt das Standardkontextmenü aus Ihrem WebView2-Steuerelement.  

Erkunden Sie zunächst die aktuelle Kontextmenüfunktionalität.  

1.  Führen Sie Ihr Projekt aus.  
1.  Zeigen Sie auf eine beliebige Stelle im WebView2-Steuerelement, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).  Im Kontextmenü werden die Standardoptionen angezeigt.  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Das Kontextmenü mit den Standardauswahlmöglichkeiten" lightbox="./media/contextmenu.png":::
       Das Kontextmenü mit den Standardauswahlmöglichkeiten  
    :::image-end:::  
    
Fügen Sie nun Code hinzu, um die kontextbezogene Menüfunktionalität aus dem WebView2-Steuerelement zu entfernen.  

1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `InitializeAsync()` in `MainWindow.xaml.cs` ein.    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  Führen Sie den Code erneut aus.  Vergewissern Sie sich, dass Sie kein Kontextmenü öffnen können \(klicken Sie mit der rechten Maustaste\).  
   
## <a name="see-also"></a>Weitere Informationen  

*   Weitere Informationen zu den ersten Schritte mit WebView2 finden Sie unter [WebView2 Getting Started Guides][Webview2MainGettingStarted].  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie im [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samples] GitHub.  
*   Ausführliche Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].  
*   Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2MainNextSteps].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  


[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft Docs"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF (Preview) | Microsoft Docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated - 0.9.579 - interface ICoreWebView2 | Microsoft Docs"  
[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  
